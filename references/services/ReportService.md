# ReportService Cheatsheet

## Methods

### getReportDownloadURL
Returns the URL at which the report file can be downloaded.
The report will be generated as a gzip archive, containing the
report file itself.

### getReportDownloadUrlWithOptions
Returns the URL at which the report file can be downloaded, and
allows for customization of the downloaded report.
By default, the report will be generated as a gzip archive,
containing the report file itself. This can be changed by setting
[ReportDownloadOptions.useGzipCompression](/ad-manager/api/reference/v202608/ReportService.ReportDownloadOptions#useGzipCompression) to false.

### getReportJobStatus
Returns the [ReportJobStatus](/ad-manager/api/reference/v202608/ReportService.ReportJobStatus) of the report job with the specified ID.

### getSavedQueriesByStatement
Retrieves a page of the saved queries either created by or shared with the current user. Each
[SavedQuery](/ad-manager/api/reference/v202608/ReportService.SavedQuery) in the page, if it is compatible with the current API version, will contain
a [ReportQuery](/ad-manager/api/reference/v202608/ReportService.ReportQuery) object which can be optionally modified and used to create a [ReportJob](/ad-manager/api/reference/v202608/ReportService.ReportJob). This can then be passed to [ReportService.runReportJob](/ad-manager/api/reference/v202608/ReportService#runReportJob). The following fields
are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [SavedQuery.id](/ad-manager/api/reference/v202608/ReportService.SavedQuery#id) |
| `name` | [SavedQuery.name](/ad-manager/api/reference/v202608/ReportService.SavedQuery#name) |

### runReportJob
Initiates the execution of a [ReportQuery](/ad-manager/api/reference/v202608/ReportService.ReportQuery) on the server.
The following fields are required:
* [ReportJob.reportQuery](/ad-manager/api/reference/v202608/ReportService.ReportJob#reportQuery)

## Types

### ReportJob
| Field | Type | Description |
|-------|------|-------------|
| `id` | long | Job ID |
| `reportQuery` | ReportQuery | Query definition |
| `status` | ReportJobStatus | Job status |
| `startDate` | Date | Start date |
| `endDate` | Date | End date |
| `readyForReportGeneration` | boolean | Ready flag |

### ReportQuery
| Field | Type | Description |
|-------|------|-------------|
| `dimensions` | Dimension[] | Report dimensions |
| `columns` | Column[] | Report columns |
| `customFieldIds` | long[] | Custom field IDs |
| `contentHierarchy` | Dimension[] | Content hierarchy |
| `dateRangeType` | DateRangeType | Date range type |
| `startDate` | Date | Start date |
| `endDate` | Date | End date |
| `statement` | String | Filter statement |
| `adxReportQuery` | boolean | AdX query flag |

## Enumerations

### ReportJobStatus
| Value | Description |
|-------|-------------|
| `IN_PROGRESS` | |
| `COMPLETED` | |
| `FAILED` | |


### DateRangeType
| Value | Description |
|-------|-------------|
| `TODAY` | |
| `YESTERDAY` | |
| `LAST_WEEK` | |
| `LAST_MONTH` | |
| `LAST_QUARTER` | |
| `LAST_YEAR` | |
| `YEAR_TO_DATE` | |
| `CURRENT_WEEK` | |
| `CURRENT_MONTH` | |
| `CURRENT_QUARTER` | |
| `CURRENT_YEAR` | |
| `CUSTOM_DATE` | |
| `ALL_TIME` | |


### Dimension
| Value | Description |
|-------|-------------|
| `ORDER_ID` | |
| `ORDER_NAME` | |
| `ADVERTISER_ID` | |
| `ADVERTISER_NAME` | |
| `AD_UNIT_ID` | |
| `AD_UNIT_NAME` | |
| `LINE_ITEM_ID` | |
| `LINE_ITEM_NAME` | |
| `LINE_ITEM_TYPE` | |
| `CREATIVE_ID` | |
| `CREATIVE_NAME` | |
| `TOTAL_LINE_ITEM_LEVEL_IMPRESSIONS` | |
| `TOTAL_LINE_ITEM_LEVEL_CLICKS` | |
| `TOTAL_LINE_ITEM_LEVEL_CPM_AND_CPC_REVENUE` | |
| `TOTAL_LINE_ITEM_LEVEL_CTR` | |


### Column
| Value | Description |
|-------|-------------|
| `MONTH` | |
| `ADVERTISER_ID` | |
| `ADVERTISER_NAME` | |
| `ORDER_ID` | |
| `ORDER_NAME` | |
| `LINE_ITEM_ID` | |
| `LINE_ITEM_NAME` | |
| `LINE_ITEM_TYPE` | |
| `AD_UNIT_ID` | |
| `AD_UNIT_NAME` | |
| `AD_UNIT_PATH` | |
| `CREATIVE_ID` | |
| `CREATIVE_NAME` | |
| `CREATIVE_SIZE` | |
| `TOTAL_LINE_ITEM_LEVEL_IMPRESSIONS` | |
| `TOTAL_LINE_ITEM_LEVEL_CLICKS` | |
| `TOTAL_LINE_ITEM_LEVEL_CTR` | |
| `TOTAL_LINE_ITEM_LEVEL_CPM_AND_CPC_REVENUE` | |

