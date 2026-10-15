# ReportService Reference

**Service**: ReportService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/ReportService
**Types**: 6

## Methods

### getReportDownloadURL
- **Request**: `long reportJobId`, `ExportFormat exportFormat`
- **Response**: `string`

### getReportDownloadUrlWithOptions
- **Request**: `long reportJobId`, `ReportDownloadOptions reportDownloadOptions`
- **Response**: `string`

### getReportJobStatus
- **Request**: `long reportJobId`
- **Response**: `ReportJobStatus`

### getSavedQueriesByStatement
- **Request**: `Statement filterStatement` (PQL filterable: `id`, `name`)
- **Response**: `SavedQueryPage`

### runReportJob
- **Request**: `ReportJob reportJob`
- **Response**: `ReportJob` (Prefer using `client.GetDataDownloader(version='v202608').WaitForReport(report_job)`)

## Types

### ReportJob

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the `ReportJob`. Read-only, assigned by Google when `runReportJob` is called. |
| `reportQuery` | `ReportQuery` | Holds the filtering criteria and retrieving options for the `ReportJob`. Required. |

### ReportQuery

| Field | Type | Description |
|-------|------|-------------|
| `dimensions` | `Dimension[]` | The list of break-down dimensions being reported on. Required. |
| `adUnitView` | `AdUnitView` | The view of the ad unit hierarchy (`TOP_LEVEL`, `FLAT`, `HIERARCHICAL`). Defaults to `TOP_LEVEL`. |
| `columns` | `Column[]` | The list of trafficking/delivery/inventory statistics columns being reported on. Required. |
| `contentMetadataKeyHierarchyCustomTargetingKeyIds` | `long[]` | List of `CustomTargetingKey` IDs for content metadata hierarchy. |
| `startDate` | `Date` | The start date (`{'year': YYYY, 'month': M, 'day': D}`, NO outer `'date'` wrapper!). Required if `dateRangeType == 'CUSTOM_DATE'`. |
| `endDate` | `Date` | The end date (`{'year': YYYY, 'month': M, 'day': D}`, NO outer `'date'` wrapper!). Required if `dateRangeType == 'CUSTOM_DATE'`. |
| `dateRangeType` | `DateRangeType` | The period of time for which the reporting data is being generated. Required. |
| `statement` | `Statement` | Specifies a PQL filter `Statement` (e.g. `WHERE LINE_ITEM_ID = 12345` or `WHERE AD_UNIT_ID IN (...)`). |
| `reportCurrency` | `string` | Currency code for revenue metrics (e.g. `'HKD'`). |
| `timeZoneType` | `TimeZoneType` | The time zone used for breaking down date dimensions (`PUBLISHER` or `PROPOSAL_LOCAL`). Recommended: `'PUBLISHER'`. |
| `dimensionAttributes` | `DimensionAttribute[]` | The list of attributes to display for the specified `dimensions`. |
| `customFieldIds` | `long[]` | The list of `CustomField.id` values to include in the report. |
| `customDimensionKeyIds` | `long[]` | The list of custom dimension `CustomTargetingKey.id` values when `CUSTOM_DIMENSION` is in `dimensions`. |

### ReportDownloadOptions

| Field | Type | Description |
|-------|------|-------------|
| `exportFormat` | `ExportFormat` | The `ExportFormat` used to generate the report (`CSV_DUMP`, `TSV`, `XML`, `XLSX`). |
| `includeReportProperties` | `boolean` | Whether to include the report properties in the generated report. |
| `includeTotalsRow` | `boolean` | Whether to include the totals row. Must be `false` for `CSV_DUMP`. |
| `useGzipCompression` | `boolean` | Whether to compress the report file using gzip (`True` by default in `DataDownloader`). |

### SavedQuery

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The ID of the saved query. |
| `name` | `string` | The name of the saved query. |
| `reportQuery` | `ReportQuery` | The `ReportQuery` representing the selection criteria. May be `null` if `isCompatibleWithApiVersion == False`. |
| `isCompatibleWithApiVersion` | `boolean` | Whether or not the saved query is compatible with the current API version. |

## Enumerations

### DateRangeType

| Value | Description |
|-------|-------------|
| `TODAY` | The current day. |
| `YESTERDAY` | The previous day. |
| `LAST_WEEK` | The previous week (Monday to Sunday). |
| `LAST_MONTH` | The previous calendar month. |
| `LAST_3_MONTHS` | The last 3 full calendar months. |
| `REACH_LIFETIME` | Lifetime reach (required for certain Reach reports). |
| `CUSTOM_DATE` | Custom start and end dates (`startDate` and `endDate` must be set). |
| `NEXT_DAY` | The next day (for forecasting reports). |
| `NEXT_90_DAYS` | The next 90 days (for forecasting reports). |
| `NEXT_WEEK` | The next week. |
| `NEXT_MONTH` | The next month. |
| `CURRENT_AND_NEXT_MONTH` | Current and next month. |
| `NEXT_QUARTER` | The next quarter. |
| `NEXT_3_MONTHS` | The next 3 months. |
| `NEXT_12_MONTHS` | The next 12 months. |

### AdUnitView

| Value | Description |
|-------|-------------|
| `TOP_LEVEL` | Only the top level ad units. Metrics include children if not filtered. |
| `FLAT` | All ad units in a flat list. |
| `HIERARCHICAL` | All ad units showing full hierarchy path columns. |

### TimeZoneType

| Value | Description |
|-------|-------------|
| `PUBLISHER` | Use the publisher's network time zone (e.g. `Asia/Hong_Kong`). |
| `PROPOSAL_LOCAL` | Use the proposal's local time zone. |

### Common `Dimension` Values
- **Time**: `DATE`, `HOUR`, `WEEK`, `MONTH_AND_YEAR`
- **Trafficking**: `ORDER_ID`, `ORDER_NAME`, `LINE_ITEM_ID`, `LINE_ITEM_NAME`, `LINE_ITEM_TYPE`, `CREATIVE_ID`, `CREATIVE_NAME`, `CREATIVE_SIZE`, `CREATIVE_TYPE`, `ADVERTISER_ID`, `ADVERTISER_NAME`
- **Inventory & Placement**: `AD_UNIT_ID`, `AD_UNIT_NAME`, `PLACEMENT_ID`, `PLACEMENT_NAME`, `TARGETING`, `CUSTOM_CRITERIA`, `CUSTOM_DIMENSION`
- **Device & Geo**: `DEVICE_CATEGORY_ID`, `DEVICE_CATEGORY_NAME`, `COUNTRY_CRITERIA_ID`, `COUNTRY_NAME`, `BROWSER_ID`, `BROWSER_NAME`, `OPERATING_SYSTEM_VERSION_ID`, `OPERATING_SYSTEM_VERSION_NAME`, `MOBILE_APP_ID`, `MOBILE_APP_NAME`, `REQUEST_TYPE`
- **Programmatic**: `DEMAND_CHANNEL_ID`, `DEMAND_CHANNEL_NAME`, `YIELD_GROUP_ID`, `YIELD_GROUP_NAME`, `YIELD_PARTNER_NAME`

### Common `DimensionAttribute` Values
- **Order**: `ORDER_START_DATE_TIME`, `ORDER_END_DATE_TIME`, `ORDER_EXTERNAL_ID`, `ORDER_PO_NUMBER`, `ORDER_AGENCY`, `ORDER_TRAFFICKER`, `ORDER_SALESPERSON`
- **Line Item**: `LINE_ITEM_START_DATE_TIME`, `LINE_ITEM_END_DATE_TIME`, `LINE_ITEM_EXTERNAL_ID`, `LINE_ITEM_COST_TYPE`, `LINE_ITEM_COST_PER_UNIT`, `LINE_ITEM_GOAL_QUANTITY`, `LINE_ITEM_DELIVERY_INDICATOR`, `LINE_ITEM_DELIVERY_PACING`, `LINE_ITEM_PRIORITY`, `LINE_ITEM_UNLIMITED_END_DATE`
- **Ad Unit**: `AD_UNIT_CODE`

### Common `Column` (Metrics) Values
- **Total Delivery**: `TOTAL_LINE_ITEM_LEVEL_IMPRESSIONS`, `TOTAL_LINE_ITEM_LEVEL_CLICKS`, `TOTAL_LINE_ITEM_LEVEL_CTR`, `TOTAL_LINE_ITEM_LEVEL_CPM_AND_CPC_REVENUE`, `TOTAL_LINE_ITEM_LEVEL_ALL_REVENUE`
- **Ad Server (Direct)**: `AD_SERVER_IMPRESSIONS`, `AD_SERVER_CLICKS`, `AD_SERVER_CTR`, `AD_SERVER_CPM_AND_CPC_REVENUE`, `AD_SERVER_ALL_REVENUE`, `AD_SERVER_WITHOUT_CPD_AVERAGE_ECPM`
- **Ad Exchange / Programmatic**: `AD_EXCHANGE_LINE_ITEM_LEVEL_IMPRESSIONS`, `AD_EXCHANGE_LINE_ITEM_LEVEL_CLICKS`, `AD_EXCHANGE_LINE_ITEM_LEVEL_REVENUE`, `AD_EXCHANGE_LINE_ITEM_LEVEL_AVERAGE_ECPM`
- **Inventory & Fill / Unfilled**: `TOTAL_AD_REQUESTS`, `TOTAL_RESPONSES_SERVED`, `TOTAL_UNFILLED_REQUESTS`, `TOTAL_FILL_RATE`, `TOTAL_CODE_SERVED_COUNT`
- **Active View (Viewability)**: `TOTAL_ACTIVE_VIEW_VIEWABLE_IMPRESSIONS`, `TOTAL_ACTIVE_VIEW_MEASURABLE_IMPRESSIONS`, `TOTAL_ACTIVE_VIEW_VIEWABLE_IMPRESSIONS_RATE`, `AD_SERVER_ACTIVE_VIEW_VIEWABLE_IMPRESSIONS`, `AD_SERVER_ACTIVE_VIEW_VIEWABLE_IMPRESSIONS_RATE`
- **Reach**: `UNIQUE_REACH_FREQUENCY`, `UNIQUE_REACH_IMPRESSIONS`, `UNIQUE_REACH`

### ExportFormat

| Value | Description |
|-------|-------------|
| `CSV_DUMP` | Comma-separated values without report properties or totals row (Best for `pandas.read_csv`). |
| `TSV` | Tab-separated values. |
| `TSV_EXCEL` | Tab-separated values for Excel. |
| `XML` | XML format. |
| `XLSX` | Office Open XML spreadsheet format. |
