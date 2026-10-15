---
name: gam-soap-codegen
description: "Translate natural language data requests into Google Ad Manager (GAM / DFP) SOAP API v202608 Python code using the googleads library. Use whenever the user asks to pull, query, export, or inspect GAM data — including line items, orders, creatives, ad units/inventory, placements, custom targeting key-values, forecasts, PQL match tables, proposals, users/teams, yield groups, or delivery/inventory reports (e.g. '幫我拿GAM data', '拉 active line items', '跑 delivery report')."
version: 3.1.0
author: kahong
license: MIT
metadata:
  hermes:
    tags: [gam, soap-api, codegen, googleads, v202608, data-extraction]
---

# GAM SOAP API v202608 — Natural Language -> Python Codegen

**GitHub**: https://github.com/funcardboy/gam-soap-codegen

## Purpose

User describes in plain language what Google Ad Manager (GAM) data they want (e.g., "幫我拿所有 delivering line items 同埋佢哋嘅 impressions delivered" / "跑過去 7 日每個 Ad Unit 嘅 delivery report"). This skill translates that request into production-ready, bug-free Python code using `googleads.ad_manager` (v202608) that outputs a clean `pandas.DataFrame` or CSV.

## Step 1 — Route the Request (3-Way Decision Tree)

**Pick the right API path FIRST before choosing a service:**

1. **Object Settings / Current State / Lifetime Stats** -> `*Service.get*ByStatement`
   - *Use when*: Fetching active Line Items, Order metadata, Creative details, Ad Unit hierarchy, Placement groupings, Custom Targeting keys/values, Users/Roles, or reading `LineItem.stats.impressionsDelivered`.
2. **Aggregated Time-Series / Dimensional Breakdown** -> `ReportService` (`DataDownloader.WaitForReport`)
   - *Use when*: Breaking down impressions, clicks, CTR, fill rate, or revenue by `DATE`, `AD_UNIT_NAME`, `LINE_ITEM_NAME`, `CUSTOM_CRITERIA`, or `DEVICE_CATEGORY`.
   - *Rule*: Requests like "過去 7 日每個 Ad Unit 嘅 impressions" MUST use `ReportService`, NOT `InventoryService`.
3. **System Lookup & Match Tables** -> `PublisherQueryLanguageService.select` (PQL)
   - *Use when*: Querying system ID tables (`Geo_Target`, `Browser`, `Operating_System`, `Device_Category`, `Bandwidth_Group`, `Programmatic_Buyer`, `Change_History`).

### Complete v202608 Service Routing Table (43 Services)

| Domain | User wants | Service | Primary Read / Query Method |
|---|---|---|---|
| **Trafficking & Delivery** | Orders / IO metadata | `OrderService` | `getOrdersByStatement` |
| **Trafficking & Delivery** | Line items / campaigns / pacing / targeting | `LineItemService` | `getLineItemsByStatement` |
| **Trafficking & Delivery** | Line item templates | `LineItemTemplateService` | `getLineItemTemplatesByStatement` |
| **Trafficking & Delivery** | Creatives (Image, Custom, Third-party, Video, Native) | `CreativeService` | `getCreativesByStatement` |
| **Trafficking & Delivery** | LICA (Creative <-> LineItem links & preview URLs) | `LineItemCreativeAssociationService` | `getLineItemCreativeAssociationsByStatement`, `getPreviewUrl` |
| **Trafficking & Delivery** | Creative sets (master + companions) | `CreativeSetService` | `getCreativeSetsByStatement` |
| **Trafficking & Delivery** | Creative templates (system & user-defined) | `CreativeTemplateService` | `getCreativeTemplatesByStatement` |
| **Trafficking & Delivery** | Creative wrappers (header/footer tags) | `CreativeWrapperService` | `getCreativeWrappersByStatement` |
| **Trafficking & Delivery** | Native styles | `NativeStyleService` | `getNativeStylesByStatement` |
| **Inventory & Targeting** | Ad units & ad unit sizes | `InventoryService` | `getAdUnitsByStatement`, `getAdUnitSizesByStatement` |
| **Inventory & Targeting** | Placements (groups of Ad Units, e.g. Web A/B/C) | `PlacementService` | `getPlacementsByStatement` |
| **Inventory & Targeting** | Suggested ad units | `SuggestedAdUnitService` | `getSuggestedAdUnitsByStatement` |
| **Inventory & Targeting** | Custom targeting keys & values (Key-Values) | `CustomTargetingService` | `getCustomTargetingKeysByStatement`, `getCustomTargetingValuesByStatement` |
| **Inventory & Targeting** | Saved targeting presets | `TargetingPresetService` | `getTargetingPresetsByStatement` |
| **Reporting & PQL** | Aggregated delivery, inventory, or reach reports | `ReportService` | `runReportJob`, `getSavedQueriesByStatement` |
| **Reporting & PQL** | System match tables (Geo, Browser, OS, Device) | `PublisherQueryLanguageService` | `select` |
| **Forecasting & Adjustments** | Availability & delivery forecasts, traffic data | `ForecastService` | `getAvailabilityForecast`, `getDeliveryForecast`, `getTrafficData` |
| **Forecasting & Adjustments** | Forecast adjustments & traffic forecast segments | `AdjustmentService` | `getForecastAdjustmentsByStatement`, `getTrafficForecastSegmentsByStatement` |
| **Programmatic & Yield** | Programmatic proposals (PG / Preferred Deals) | `ProposalService` | `getProposalsByStatement`, `getMarketplaceCommentsByStatement` |
| **Programmatic & Yield** | Proposal line items | `ProposalLineItemService` | `getProposalLineItemsByStatement` |
| **Programmatic & Yield** | Yield groups & mediation partners | `YieldGroupService` | `getYieldGroupsByStatement`, `getYieldPartners` |
| **Programmatic & Yield** | MCM sites & approval status | `SiteService` | `getSitesByStatement` |
| **Programmatic & Yield** | Ads.txt file diagnostics | `AdsTxtService` | `getMcmSupplyChainDiagnosticsDownloadUrl` |
| **Audience & Custom Metadata** | 1st/3rd-party audience segments | `AudienceSegmentService` | `getAudienceSegmentsByStatement` |
| **Audience & Custom Metadata** | Audience segment batch upload results | `SegmentPopulationService` | `getSegmentPopulationResultsByIds` |
| **Audience & Custom Metadata** | Custom fields on LineItems/Orders/Creatives | `CustomFieldService` | `getCustomFieldsByStatement` |
| **Audience & Custom Metadata** | Labels (competitive exclusion, frequency cap) | `LabelService` | `getLabelsByStatement` |
| **Video, Live & CMS** | Ad rules & video podding | `AdRuleService` | `getAdRulesByStatement`, `getBreakTemplatesByStatement` |
| **Video, Live & CMS** | Video content & CMS metadata | `ContentService`, `ContentBundleService`, `CmsMetadataService` | `getContentByStatement`, `getContentBundlesByStatement`, `getCmsMetadataKeysByStatement` |
| **Video, Live & CMS** | Live stream events, CDN, DAI, stream monitoring | `LiveStreamEventService`, `CdnConfigurationService`, `DaiAuthenticationKeyService`, `DaiEncodingProfileService`, `StreamActivityMonitorService` | `getLiveStreamEventsByStatement`, `getCdnConfigurationsByStatement`, `getSamSessionsByStatement` |
| **Admin, Companies & Users** | Advertisers, agencies, viewability providers | `CompanyService` | `getCompaniesByStatement` |
| **Admin, Companies & Users** | Advertiser contacts | `ContactService` | `getContactsByStatement` |
| **Admin, Companies & Users** | Users & roles (map `traffickerId` / `salespersonId`) | `UserService` | `getUsersByStatement`, `getAllRoles`, `getCurrentUser` |
| **Admin, Companies & Users** | Teams & user-team access | `TeamService`, `UserTeamAssociationService` | `getTeamsByStatement`, `getUserTeamAssociationsByStatement` |
| **Admin, Companies & Users** | Network settings & mobile apps | `NetworkService`, `MobileApplicationService` | `getCurrentNetwork`, `getAllNetworks`, `getMobileApplicationsByStatement` |

If unsure which example matches: check `references/examples-index.md` to browse all 162 official examples.

## Step 2 — Load Service Cheatsheet

Load the target service reference file:

```python
skill_view(name='gam-soap-codegen', file_path='references/services/<ServiceName>.md')
```

Each cheatsheet in `references/services/<ServiceName>.md` contains:
- **Methods**: Exact operation names, request parameter names/types, and return types.
- **Types**: All non-error data structures and their exact field names, types, and descriptions.
- **Enumerations**: Valid uppercase enum strings.

**Strict Grounding Rule**: Use field names and enum strings *exactly* as documented in the cheatsheet. Never invent or guess field names (e.g., use `impressionsDelivered`, never `unitsDelivered` on `Stats`).

## Step 3 — Check Official Examples

```python
skill_view(name='gam-soap-codegen', file_path='references/examples-index.md')
# Load the matching example script:
skill_view(name='gam-soap-codegen', file_path='references/examples/<service_folder>/<example_file>.py')
```

Adapt from the official example rather than writing boilerplate from scratch.

## Step 4 — Generate Code Using Verified Templates

### Template A — Entity Service (`get*ByStatement` + Pagination + Safe Unpacking)

Use for fetching entities (`LineItemService`, `OrderService`, `CreativeService`, `InventoryService`, `PlacementService`, `UserService`, etc.).

```python
from googleads import ad_manager
import pandas as pd


def unpack_datetime(dt):
    """Convert GAM SOAP DateTime dict to ISO string safely (handles None / unlimitedEndDateTime)."""
    if not dt or 'date' not in dt:
        return None
    d = dt['date']
    return (
        f"{d['year']:04d}-{d['month']:02d}-{d['day']:02d}"
        f"T{dt.get('hour', 0):02d}:{dt.get('minute', 0):02d}:{dt.get('second', 0):02d}"
    )


def unpack_money(money):
    """Convert GAM SOAP Money dict (microAmount) to float currency amount."""
    if not money or money.get('microAmount') is None:
        return 0.0
    return money['microAmount'] / 1_000_000.0


client = ad_manager.AdManagerClient.LoadFromStorage()
line_item_service = client.GetService('LineItemService', version='v202608')

statement = (
    ad_manager.StatementBuilder(version='v202608')
    .Where("status = :status AND isArchived = :archived")
    .WithBindVariable('status', 'DELIVERING')
    .WithBindVariable('archived', False)
    .OrderBy('id', ascending=True)
    .Limit(ad_manager.StatementBuilder.SUGGESTED_PAGE_LIMIT)  # 500
)

rows = []
while True:
    response = line_item_service.getLineItemsByStatement(statement.ToStatement())
    results = response['results'] if response and 'results' in response else []
    if not results:
        break

    for item in results:
        stats = item['stats'] if 'stats' in item and item['stats'] else {}
        primary_goal = item['primaryGoal'] if 'primaryGoal' in item and item['primaryGoal'] else {}
        rows.append({
            'id': item['id'],
            'name': item['name'],
            'orderId': item['orderId'],
            'orderName': item['orderName'] if 'orderName' in item else None,
            'status': item['status'],
            'lineItemType': item['lineItemType'],
            'costType': item['costType'],
            'costPerUnit': unpack_money(item['costPerUnit'] if 'costPerUnit' in item else None),
            'startDateTime': unpack_datetime(item['startDateTime'] if 'startDateTime' in item else None),
            'endDateTime': (
                'UNLIMITED'
                if item.get('unlimitedEndDateTime')
                else unpack_datetime(item['endDateTime'] if 'endDateTime' in item else None)
            ),
            'goalUnits': primary_goal.get('units'),
            'goalUnitType': primary_goal.get('unitType'),
            'impressionsDelivered': stats.get('impressionsDelivered', 0),
            'clicksDelivered': stats.get('clicksDelivered', 0),
        })
    statement.IncreaseOffsetBy(ad_manager.StatementBuilder.SUGGESTED_PAGE_LIMIT)

df = pd.DataFrame(rows)
print(f"Total line items retrieved: {len(df)}")
print(df.head())
```

### Template B — `ReportService` (`WaitForReport` + Binary Gzip Stream -> `DataFrame`)

Use for aggregated performance/delivery/inventory metrics across dimensions (`DATE`, `AD_UNIT_NAME`, `LINE_ITEM_NAME`, `CUSTOM_CRITERIA`, etc.).

```python
import tempfile
from googleads import ad_manager
import pandas as pd

client = ad_manager.AdManagerClient.LoadFromStorage()
report_downloader = client.GetDataDownloader(version='v202608')

report_job = {
    'reportQuery': {
        'dimensions': ['DATE', 'AD_UNIT_NAME', 'LINE_ITEM_ID', 'LINE_ITEM_NAME'],
        'dimensionAttributes': ['LINE_ITEM_TYPE'],
        'columns': [
            'AD_SERVER_IMPRESSIONS',
            'AD_SERVER_CLICKS',
            'AD_SERVER_CTR',
        ],
        'dateRangeType': 'LAST_7_DAYS',
        'timeZoneType': 'PUBLISHER',
        # For custom date range, set 'dateRangeType': 'CUSTOM_DATE' and pass Date dicts directly:
        # 'startDate': {'year': 2026, 'month': 10, 'day': 1},
        # 'endDate': {'year': 2026, 'month': 10, 'day': 14},
    }
}

# WaitForReport submits the job and polls with backoff until COMPLETED
report_job_id = report_downloader.WaitForReport(report_job)

# CRITICAL: DownloadReportToFile requires a binary file object (mode='wb')
# and downloads gzip-compressed CSV by default (use_gzip_compression=True).
with tempfile.NamedTemporaryFile(suffix='.csv.gz', mode='wb', delete=False) as f:
    report_downloader.DownloadReportToFile(report_job_id, 'CSV_DUMP', f)
    report_file = f.name

df = pd.read_csv(report_file, compression='gzip')
print(f"Report rows: {len(df)}")
print(df.head())
```

### Template C — `PublisherQueryLanguageService` (`select` with `StatementBuilder` + Pagination)

Use for querying system match tables (`Geo_Target`, `Browser`, `Operating_System`, `Device_Category`, `Line_Item`, `Change_History`, etc.).

```python
from googleads import ad_manager
import pandas as pd

client = ad_manager.AdManagerClient.LoadFromStorage()
pql_service = client.GetService('PublisherQueryLanguageService', version='v202608')

statement = (
    ad_manager.StatementBuilder(version='v202608')
    .Select('Id, Name, CanonicalParentPath, Type')
    .From('Geo_Target')
    .Where("Targetable = true AND CountryCode = :countryCode")
    .WithBindVariable('countryCode', 'HK')
    .OrderBy('Id', ascending=True)
    .Limit(ad_manager.StatementBuilder.SUGGESTED_PAGE_LIMIT)
)

rows = []
columns = None

while True:
    # CRITICAL: pql_service.select() requires a Statement dict (statement.ToStatement()), NOT a raw string
    result_set = pql_service.select(statement.ToStatement())
    if not result_set or 'rows' not in result_set or not result_set['rows']:
        break

    if columns is None:
        columns = [col['name'] for col in result_set['columnTypes']]

    for row in result_set['rows']:
        rows.append([
            v['value'] if 'value' in v else None
            for v in row['values']
        ])

    statement.IncreaseOffsetBy(ad_manager.StatementBuilder.SUGGESTED_PAGE_LIMIT)

df = pd.DataFrame(rows, columns=columns or [])
print(f"Total PQL rows retrieved: {len(df)}")
print(df.head())
```

### Data Extraction Output Rule (MANDATORY)

Every generated script that pulls data MUST unpack nested SOAP objects into flat rows and build a `pandas.DataFrame` (or export to CSV). Never leave the user with raw `print(item)` Zeep dictionaries.

### Common Cross-Service Chaining Patterns

1. **Line Item -> Creatives -> Preview URLs**:
   - `LineItemService.getLineItemsByStatement` -> get `lineItemId`
   - `LineItemCreativeAssociationService.getLineItemCreativeAssociationsByStatement` (`WHERE lineItemId = :id`) -> get `creativeId`
   - `LineItemCreativeAssociationService.getPreviewUrl(lineItemId, creativeId, siteUrl)` -> note the 3rd positional parameter is `siteUrl` (e.g. `'https://www.hket.com'`), NOT `creativeSetId`.
2. **Order / Line Item -> Salesperson or Trafficker Name**:
   - `OrderService.getOrdersByStatement` -> returns numeric `salespersonId` and `traffickerId`
   - `UserService.getUsersByStatement` -> maps `User.id` to `User.name` and `User.email`.
3. **Placement -> Targeted Ad Units**:
   - `PlacementService.getPlacementsByStatement` -> returns `Placement.targetedAdUnitIds` (`string[]`)
   - `InventoryService.getAdUnitsByStatement` (`WHERE id IN (...)`) -> resolves Ad Unit names and codes.

## Pitfalls & PQL Filter Rules

1. **PQL `.Where()` Filterable Fields vs. Python Post-Filtering**:
   - `*Service.get*ByStatement` ONLY supports PQL filtering on **indexed top-level scalar fields**:
     - `LineItemService`: `id`, `orderId`, `name`, `status`, `lineItemType`, `startDateTime`, `endDateTime`, `lastModifiedDateTime`, `isArchived`, `externalId`
     - `OrderService`: `id`, `name`, `status`, `advertiserId`, `salespersonId`, `traffickerId`, `startDateTime`, `endDateTime`, `lastModifiedDateTime`, `isArchived`
     - `CreativeService`: `id`, `name`, `advertiserId`, `width`, `height`, `lastModifiedDateTime`
     - `InventoryService`: `id`, `name`, `adUnitCode`, `status`, `parentId`, `lastModifiedDateTime`
     - `PlacementService`: `id`, `name`, `placementCode`, `status`, `lastModifiedDateTime`
   - **Never put nested fields in `.Where()`** (such as `targeting`, `stats`, `primaryGoal`, `creativePlaceholders`) — doing so raises `PublisherQueryLanguageContextError.UNEXECUTABLE`. Fetch using top-level filters (`status = 'DELIVERING'`) and filter nested structures in Python.
2. **`Date` vs `DateTime` Dict Structure (Top Trap)**:
   - **`Date` objects** (used in `ReportQuery.startDate` and `ReportQuery.endDate` when `dateRangeType == 'CUSTOM_DATE'`): `{'year': 2026, 'month': 10, 'day': 15}` (NO outer `'date'` key!).
   - **`DateTime` objects** (used in `LineItem.startDateTime`, `Order.endDateTime`, etc.): `{'date': {'year': 2026, 'month': 10, 'day': 15}, 'hour': 0, 'minute': 0, 'second': 0, 'timeZoneId': 'Asia/Hong_Kong'}`.
3. **`DownloadReportToFile` File Handle & Compression**:
   - Always pass an open binary file object (`mode='wb'`) as the 3rd argument to `DownloadReportToFile(report_job_id, 'CSV_DUMP', f)`, and read with `pd.read_csv(f.name, compression='gzip')`.
4. **Zeep / Suds Safe Field Access**:
   - `googleads` returns Zeep compound objects that behave like dicts, but optional fields (e.g., `stats` on a newly created line item, or `endDateTime` when `unlimitedEndDateTime == True`) may be `None` or absent. Always guard nested access.
5. **Mutating Operations (`create*`, `update*`, `perform*Action`)**:
   - `id` is read-only on `create*` calls; sending it raises a SOAP `ApiError`.
   - `perform*Action` requires an action dict with `xsi_type` (e.g., `{'xsi_type': 'PauseLineItems'}`).

## Verification Checklist

Before outputting code to the user:
- [ ] Correct path chosen (`get*ByStatement` vs `ReportService` vs `PublisherQueryLanguageService`)?
- [ ] Every field name and enum string verified against `references/services/<ServiceName>.md`?
- [ ] `.Where()` clause only filters PQL-supported top-level fields (nested targeting/stats filtered in Python)?
- [ ] Pagination loop uses `statement.IncreaseOffsetBy(...)` and guards against empty `results` / `rows`?
- [ ] Output unpacked cleanly into a `pandas.DataFrame` or CSV?
