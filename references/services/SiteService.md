# SiteService Reference

**Service**: SiteService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/SiteService
**Types**: 5

## Methods

### createSites
- **Request**: `Site[] sites`
- **Response**: `Site[]`

### getSitesByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `id`, `url`, `childNetworkCode`, `approvalStatus`, `lastModifiedDateTime`)
- **Response**: `SitePage`

### performSiteAction
- **Request**: `SiteAction siteAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateSites
- **Request**: `Site[] sites`
- **Response**: `Site[]`

## Types

### Site

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | Uniquely identifies the `Site`. Read-only. |
| `url` | `string` | The URL of the `Site`. Required. |
| `childNetworkCode` | `string` | The `Network.networkCode` of the child if the `Site` is beingichi-managed for an MCM child network, or `null` if owned by this network. |
| `approvalStatus` | `ApprovalStatus` | Status of the review performed on the `Site` by Google. Read-only. |
| `disapprovalReasons` | `DisapprovalReason[]` | Provides reasons for disapproving the site. Read-only. |

### SitePage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `Site[]` | The collection of sites contained within this page. |

### DisapprovalReason

| Field | Type | Description |
|-------|------|-------------|
| `type` | `DisapprovalReasonType` | The type of policy violation found for the `Site`. |
| `details` | `string` | Additional details Delayed/Disapproved for the `Site`. |

### SiteAction (Subclasses)
- `DeactivateSites` (`{'xsi_type': 'DeactivateSites'}`)
- `SubmitSiteForApproval` (`{'xsi_type': 'SubmitSiteForApproval'}`)

## Enumerations

### ApprovalStatus

| Value | Description |
|-------|-------------|
| `DRAFT` | The site is in draft state and has not been submitted for review. |
| `UNCHECKED` | The site has been submitted for review. |
| `APPROVED` | The site has been reviewed and approved to serve ads. |
| `DISAPPROVED` | The site has been reviewed and disapproved. |
| `REQUIRES_REVIEW` | The site requires re-review. |
| `UNKNOWN` | Unknown status. |
