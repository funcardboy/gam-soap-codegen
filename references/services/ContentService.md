# ContentService Cheatsheet

## Methods

### getContentByStatement
Gets a [ContentPage](/ad-manager/api/reference/v202608/ContentService.ContentPage) of [Content](/ad-manager/api/reference/v202608/ContentService.Content) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/ContentService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [Content.id](/ad-manager/api/reference/v202608/ContentService.Content#id) |
| `status` | [Content.status](/ad-manager/api/reference/v202608/ContentService.Content#status) |
| `name` | [Content.name](/ad-manager/api/reference/v202608/ContentService.Content#name) |
| `lastModifiedDateTime` | [Content.lastModifiedDateTime](/ad-manager/api/reference/v202608/ContentService.Content#lastModifiedDateTime) |
| `lastDaiIngestDateTime` | [Content.lastDaiIngestDateTime](/ad-manager/api/reference/v202608/ContentService.Content#lastDaiIngestDateTime) |
| `daiIngestStatus` | [Content.daiIngestStatus](/ad-manager/api/reference/v202608/ContentService.Content#daiIngestStatus) |
