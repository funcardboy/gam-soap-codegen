# ReportService Reference

**Service**: ReportService

**Types**: 0

## Methods

### getReportDownloadURL
- **Request**: `xsd:long reportJobId`
- **Response**: `xsd:string`

### getReportDownloadUrlWithOptions
- **Request**: `xsd:long reportJobId`
- **Request**: `ReportDownloadOptions reportDownloadOptions`
- **Response**: `xsd:string`

### getReportJobStatus
- **Request**: `xsd:long reportJobId`

### getSavedQueriesByStatement
- **Request**: `Statement filterStatement`
- **Response**: `SavedQueryPage`

### runReportJob
- **Request**: `ReportJob reportJob`
- **Response**: `ReportJob`

