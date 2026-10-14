---
name: gam-soap-codegen
description: "Use when user describes data they want from GAM — translate natural language to GAM SOAP API v202608 Python code."
version: 2.0.0
author: sam
license: MIT
metadata:
  hermes:
    tags: [gam, soap-api, codegen, googleads, v202608]
---

# GAM SOAP API v202608 — Natural Language → Python Codegen

**GitHub**: https://github.com/funcardboy/gam-soap-codegen

## Purpose

User describes in plain language what GAM data they want (e.g. "幫我拿所有 active line items" / "get all creatives for advertiser 123"). This skill translates that into working Python code using the `googleads` SOAP API.

## Step 1 — Map request to service + method

Common mappings:

| User wants | Service | Method |
|---|---|---|
| Line items / campaigns | `LineItemService` | `getLineItemsByStatement` |
| Creatives | `CreativeService` | `getCreativesByStatement` |
| Orders | `OrderService` | `getOrdersByStatement` |
| Ad units / inventory | `InventoryService` | `getAdUnitsByStatement` |
| Forecast | `ForecastService` | `getAvailabilityForecast` |
| Reports (aggregated data) | `ReportService` | `runReportJob` |
| Audience segments | `AudienceSegmentService` | `getAudienceSegmentsByStatement` |
| Custom targeting | `CustomTargetingService` | `getCustomTargetingKeysByStatement` |

If unsure which service: `skill_view(name='gam-soap-codegen', file_path='references/examples-index.md')` to browse all 162 examples.

## Step 2 — Load service cheatsheet

```python
skill_view(name='gam-soap-codegen', file_path='references/services/<ServiceName>.md')
```

Cheatsheet contains: method signatures, request/response types, all field names + types + descriptions. **Use field names exactly as documented — never guess.**

## Step 3 — Check official examples

```python
skill_view(name='gam-soap-codegen', file_path='references/examples-index.md')
# Then read the matching example:
read_file('~/.hermes/skills/software-development/gam-soap-codegen/references/examples/<service>/<file>.py')
```

Adapt from examples — don't rewrite from scratch.

## Step 4 — Generate code

Standard client bootstrap:

```python
from googleads import ad_manager

client = ad_manager.AdManagerClient.LoadFromStorage()  # reads ~/googleads.yaml
service = client.GetService('LineItemService', version='v202608')

# Filter with PQL statement
stmt = {'query': "WHERE status = 'DELIVERING' ORDER BY id LIMIT 500"}
resp = service.getLineItemsByStatement(stmt)
results = resp.get('results', [])
```

For paginated results (>500):

```python
from googleads.ad_manager import StatementBuilder

stmt = StatementBuilder(version='v202608').Where("status = 'DELIVERING'").Limit(500)
while True:
    resp = service.getLineItemsByStatement(stmt.ToStatement())
    results = resp.get('results', [])
    if not results:
        break
    for r in results:
        print(r)
    stmt.IncreaseOffsetBy(500)
```

## Pitfalls

1. **Required vs read-only**: `id` is read-only on create; sending it → SOAP ApiError. Check field table before coding.
2. **Enum strings are exact** — e.g. `'LINEAR'` not `'linear'`.
3. **Dates are dicts**: `{'date': {'year': 2026, 'month': 10, 'day': 14}}`. DateTime adds `'hour'/'minute'/'second'` + `'timeZoneId': 'Asia/Hong_Kong'`.
4. **Statement LIMIT max is 500** — always paginate.
5. **perform*Action needs xsi_type**: `{'xsi_type': 'PauseLineItems'}` in the action dict.
6. Don’t confuse with Google Ads API — this is Ad Manager (DFP), `googleads.ad_manager`.

## Verification before handing code to Sam

- [ ] Field names verified against service cheatsheet
- [ ] Matches structure of an official example (cite the path)
- [ ] `python3 -m py_compile <generated file>` passes
- [ ] Mutating operations (create/update/perform*Action) flagged with rollback note

## Standard client bootstrap

```python
from googleads import ad_manager

client = ad_manager.AdManagerClient.LoadFromStorage()  # ~/googleads.yaml
client.api_version = "v202608"  # only if not the library default
service = client.GetService("CreativeService")
```

`~/googleads.yaml` (OAuth2 service-account or refresh-token flow):

```yaml
ad_manager:
  application_name: sam-gam-tools
  network_code: "<Sam's network code>"
  path_to_private_key_file: <service account json>   # OR:
  # refresh_token: <oauth refresh token>
  # client_id: ...
  # client_secret: ...
```

Install: `pip install googleads`. Never print/commit credentials.

## Query patterns

- **get*ByStatement** (SOAP filter):
  ```python
  stmt = {"query": "WHERE name LIKE 'test%' ORDER BY id LIMIT 500"}
  resp = service.getCreativesByStatement(stmt)
  results = resp.get("results", [])
  ```
- **PQL** (reporting/ad-hoc, via PublisherQueryLanguageService): see
  `references/examples-index.md` → `publisher_query_language_service/`.
- **Reports**: runReportJob → poll getReportJobStatus == 'COMPLETED' →
  getReportDownloadUrlWithOptions → download CSV. Example in `report_service/`.

## Pitfalls

1. **Required vs read-only**: docs mark fields like `id` read-only-on-create and
   `advertiserId` required. Sending read-only fields on create → SOAP ApiError.
   Always check the field table in `data/v202608/docs/<Type>.md` first.
2. **Enum strings are exact** — e.g. `vastRedirectType: 'LINEAR'`, not `'linear'`.
3. **Version drift**: `LoadFromStorage()` defaults to the library's newest version;
   pin `v202608` explicitly in generated code.
4. **Dates are dicts**: `{'date': {'year': 2026, 'month': 10, 'day': 14}}`, and
   DateTime adds `'hour'/'minute'/'second'` + `'timeZoneId': 'Asia/Hong_Kong'`.
5. **Statement LIMIT max is 500** — page with OFFSET/`startIndex` for more.
6. **Sandbox first**: for mutating calls (create/update/perform*Action), suggest a
   dry-run against a test network; `perform*Action` needs the action dict with
   `xsi_type` (e.g. `{'xsi_type': 'PauseLineItems'}`).
7. Don't confuse with Google Ads API — this is Ad Manager (DFP), `googleads.ad_manager`.

## Verification checklist (before handing code to Sam)

- [ ] Every field name grep-verified against `data/v202608/docs/`
- [ ] Code matches an official example's structure (cite the example path)
- [ ] `python3 -m py_compile <generated file>` passes
- [ ] Mutating operations flagged + rollback action noted (e.g. perform*Action can pause/archive)
