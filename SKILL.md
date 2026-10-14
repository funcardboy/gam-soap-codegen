---
name: gam-soap-codegen
description: "Translate natural language data requests into Google Ad Manager (GAM / DFP) SOAP API v202608 Python code using the googleads library. Use whenever the user asks to pull, query, export, or inspect GAM data — including line items, orders, creatives, ad units/inventory, custom targeting key-values, forecasts, PQL match tables, or delivery/inventory reports (e.g. '幫我拿GAM data', '拉 active line items', '跑 delivery report')."
version: 3.0.0
author: sam
license: MIT
metadata:
  hermes:
    tags: [gam, soap-api, codegen, googleads, v202608, data-extraction]
---

# GAM SOAP API v202608 — NL → Python Codegen

## Purpose

User describes in plain language what GAM data they want. This skill translates that into working Python code using the `googleads` SOAP API.

## Step 1 — Route the request

**Routing Rules — pick the right path FIRST:**

- **Object settings / current state / lifetime stats** → `*Service.get*ByStatement`
  (e.g., fetch active Line Items, get Creative metadata, read LineItem.stats.impressionsDelivered)

- **Aggregated time-series / dimensional stats** (impressions, clicks, fill rate by date/AdUnit/device) → `ReportService` + `GetDataDownloader`
  (e.g., '過去7日每個 Ad Unit 嘅 impressions' → must use ReportService, NOT InventoryService)

- **System ID lookup tables** (Geo targets, Browser, OS, Device, Change History) → `PublisherQueryLanguageService.select`

**Service / method table:**

| User wants | Service | Method |
|---|---|---|
| Line items / campaigns | `LineItemService` | `getLineItemsByStatement` |
| Creatives | `CreativeService` | `getCreativesByStatement` |
| Creative ↔ line item links + preview | `LineItemCreativeAssociationService` | `getLineItemCreativeAssociationsByStatement`, `getPreviewUrl` |
| Orders | `OrderService` | `getOrdersByStatement` |
| Ad units / inventory | `InventoryService` | `getAdUnitsByStatement` |
| Forecast | `ForecastService` | `getAvailabilityForecast` |
| Reports (aggregated data) | `ReportService` | `runReportJob` |
| Audience segments | `AudienceSegmentService` | `getAudienceSegmentsByStatement` |
| Custom targeting | `CustomTargetingService` | `getCustomTargetingKeysByStatement` |
| Geo targets / Browser / OS / Device tables | `PublisherQueryLanguageService` | `select` (PQL) |

If unsure which service: `skill_view(name='gam-soap-codegen', file_path='references/examples-index.md')` to browse all 162 examples.

## Step 2 — Load service cheatsheet

```python
skill_view(name='gam-soap-codegen', file_path='references/services/<ServiceName>.md')
```

Cheatsheet contains: method signatures, request/response types, all field names + types + descriptions. **Use field names exactly as documented — never guess.**

## Step 3 — Check official examples

```python
skill_view(name='gam-soap-codegen', file_path='references/examples-index.md')
# Then load the matching example:
skill_view(name='gam-soap-codegen', file_path='references/examples/<service>/<file>.py')
```

Adapt from examples — don't rewrite from scratch. The repo contains 162 example files under `references/examples/`, all loadable via `skill_view`.

## Step 4 — Generate code

**Client bootstrap** (YAML config file holds OAuth2 service-account or refresh-token credentials):

```python
from googleads import ad_manager

client = ad_manager.AdManagerClient.LoadFromStorage()  # reads googleads.yaml
service = client.GetService('LineItemService', version='v202608')
```

### Template A — Entity fetch (`get*ByStatement`)

Paginated fetch using StatementBuilder (always use for `get*ByStatement`):

```python
from googleads import ad_manager

stmt = (
    ad_manager.StatementBuilder(version='v202608')
    .Where("status = 'DELIVERING'")
    .WithBindVariable('advertiserId', 123)   # bind vars prevent injection
)
while True:
    resp = service.getLineItemsByStatement(stmt.ToStatement())
    results = resp.get('results', [])
    if not results:
        break
    for r in results:
        print(r)
    stmt.offset += stmt.limit
```

### Template B — Report (ReportService)

Use the official googleads pattern via `GetDataDownloader.WaitForReport` — DO NOT invent a manual polling loop:

```python
import tempfile
from googleads import ad_manager, errors
from datetime import datetime, timedelta

report_downloader = client.GetDataDownloader(version='v202608')
report_job = {
    'reportQuery': {
        'dimensions': ['DATE', 'LINE_ITEM_ID', 'LINE_ITEM_NAME'],
        'dimensionAttributes': ['ORDER_NAME', 'AD_UNIT_NAME'],
        'columns': ['AD_SERVER_IMPRESSIONS', 'AD_SERVER_CLICKS', 'AD_SERVER_CTR'],
        'dateRangeType': 'LAST_7_DAYS',  # or CUSTOM_DATE with startDate/endDate
    }
}
try:
    report_job_id = report_downloader.WaitForReport(report_job)
except errors.AdManagerReportError as e:
    print(f'Report failed: {e}')

report_file = tempfile.NamedTemporaryFile(suffix='.csv.gz', delete=False)
report_downloader.DownloadReportToFile(report_job_id, 'CSV_DUMP', report_file)
report_file.close()

# Load into pandas:
import pandas as pd
df = pd.read_csv(report_file.name, skiprows=range(1))  # skip header row
```

### Template C — PQL (Publisher Query Language)

For system ID lookup tables (Geo targets, Browser, OS, Device, Change History):

```python
report_downloader = client.GetDataDownloader(version='v202608')
pql_query = 'SELECT Id, BrowserName, MajorVersion FROM Browser ORDER BY BrowserName ASC'
report_downloader.DownloadPqlResultToCsv(pql_query, 'browsers.csv')
# or: DownloadPqlResultToJson
```

### Data Extraction output rule (MANDATORY for any data-fetching code)

GAM SOAP responses are nested Zeep dicts. Generated code MUST:

- Use `.get()` with defaults to handle missing/None fields safely
- Convert microAmount fields: `value / 1_000_000`
- Format DateTime dicts: `f"{d['date']['year']}-{d['date']['month']:02d}-{d['date']['day']:02d} {d.get('hour',0):02d}:{d.get('minute',0):02d}"`
- Default output format: pandas.DataFrame or CSV (NOT raw nested dicts)

### Cross-service chaining (e.g. line item → creatives → preview URLs)

When a task needs data from multiple services, chain them:

1. Use service A to get IDs → service B to get detail objects → service A again for derived data
2. Example — line item creatives + preview:
   ```python
   # Step 1: LICA service → get creative IDs for a line item
   lica_svc = client.GetService('LineItemCreativeAssociationService', version='v202608')
   stmt = ad_manager.StatementBuilder(version='v202608').Where('lineItemId = :lid').WithBindVariable('lid', LINE_ITEM_ID)
   licas = []  # paginate as above

   # Step 2: Creative service → get creative details
   creative_ids = [l['creativeId'] for l in licas if 'creativeId' in l]
   id_list = ', '.join(str(i) for i in creative_ids)
   stmt2 = ad_manager.StatementBuilder(version='v202608').Where(f'id IN ({id_list})')
   creatives = {}  # paginate as above

   # Step 3: getPreviewUrl — requires real ad unit page URL from the network
   preview_url = lica_svc.getPreviewUrl(LINE_ITEM_ID, creative_id, site_url)
   ```
   ⚠️ `getPreviewUrl(lineItemId, creativeId, siteUrl)` — `siteUrl` must be a live ad unit URL on the network; `example.com` returns an error.

## Pitfalls

1. **Required vs read-only**: `id` is read-only on create; `advertiserId` is required. Sending read-only fields on create → SOAP ApiError. Always check field table in the service cheatsheet first.
2. **Enum strings are exact** — e.g., `'LINEAR'` not `'linear'`; `'ACTIVE'` not `'active'`.
3. **Version drift**: `LoadFromStorage()` defaults to library's newest version; always pin `version='v202608'` in `GetService()`.
4. **Dates are dicts**: `{'date': {'year': 2026, 'month': 10, 'day': 14}}`; DateTime adds `'hour'/'minute'/'second'` + `'timeZoneId': 'Asia/Hong_Kong'`.
5. **Statement LIMIT max is 500** — always paginate; use `stmt.offset += stmt.limit` (StatementBuilder) or `OFFSET N` in raw PQL.
6. **perform*Action needs xsi_type**: e.g., `{'xsi_type': 'PauseLineItems'}` in the action dict. Suggest sandbox dry-run before running.
7. **LICA creativeId vs creative set**: LICA rows for creative sets have no `creativeId` field — always guard with `if 'creativeId' in lica` before accessing.
8. Don't confuse with Google Ads API — this is Ad Manager (DFP), `googleads.ad_manager`.

## Verification checklist

- [ ] Field names verified against service cheatsheet (never guess)
- [ ] Routing decision tree applied — correct path (entity vs report vs PQL) chosen
- [ ] Code structure matches an official example — cite the path
- [ ] `python3 -m py_compile <generated file>` passes (run it)
- [ ] Data extraction rule followed: `.get()` with defaults, microAmount/DateTime converted, DataFrame/CSV output
- [ ] Mutating operations (create/update/perform*Action) flagged with rollback note
- [ ] Cross-service chains: each service instantiated with correct `version='v202608'`
