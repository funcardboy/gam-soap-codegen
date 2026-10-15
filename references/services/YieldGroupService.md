# YieldGroupService Reference

**Service**: YieldGroupService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/YieldGroupService
**Types**: 6

## Methods

### createYieldGroups
- **Request**: `YieldGroup[] yieldGroups`
- **Response**: `YieldGroup[]`

### getYieldGroupsByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `yieldGroupId`, `yieldGroupName`, `status`)
- **Response**: `YieldGroupPage`

### getYieldPartners
- **Request**: None
- **Response**: `YieldPartner[]`

### updateYieldGroups
- **Request**: `YieldGroup[] yieldGroups`
- **Response**: `YieldGroup[]`

## Types

### YieldGroup

| Field | Type | Description |
|-------|------|-------------|
| `yieldGroupId` | `long` | The unique ID of the `YieldGroup`. Read-only. |
| `yieldGroupName` | `string` | The display name of the yield group. Required. |
| `exchangeStatus` | `YieldEntityStatus` | Status of Ad Exchange for this yield group. |
| `format` | `YieldFormat` | The format of the group (`BANNER`, `INTERSTITIAL`, `NATIVE`, `REWARDED`). Required. |
| `environmentType` | `YieldEnvironmentType` | The environment type of the group (`MOBILE`, `VIDEO_VAST`, `WEB`). Required. |
| `targeting` | `Targeting` | This yield group's targeting. Only Inventory, Geo, Technology, Custom, and RequestPlatform targeting are supported. |
| `adSources` | `YieldAdSource[]` | The ad sources belonging to this yield group. |

### YieldAdSource

| Field | Type | Description |
|-------|------|-------------|
| `adSourceId` | `long` | The unique ID of the ad source. Read-only. |
| `companyId` | `long` | The `Company.id` of the yield partner. |
| `displaySettings` | `AbstractDisplaySettings` | Partner-specific SDK/Open Bidding mediation settings. |
| `status` | `YieldEntityStatus` | User-assigned status of the ad source (`ACTIVE`, `INACTIVE`, `DELETED`). |
| `manualCpm` | `Money` | Manual CPM floor/valuation for the ad source. |
| `overrideDynamicCpm` | `boolean` | Whether to override automatic dynamic CPM collection. |

### YieldGroupPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `YieldGroup[]` | The collection of yield groups contained within this page. |

### YieldPartner

| Field | Type | Description |
|-------|------|-------------|
| `companyId` | `long` | The `Company.id` of the partner. |
| `settings` | `YieldPartnerSettings[]` | The settings of the partner, representing capabilities (Open Bidding / SDK Mediation). |

## Enumerations

### YieldFormat

| Value | Description |
|-------|-------------|
| `BANNER` | Standard display banner. |
| `INTERSTITIAL` | Full-screen interstitial. |
| `NATIVE` | Native ad format. |
| `VIDEO_VAST` | VAST video format. |
| `REWARDED` | Rewarded ad format. |
| `REWARDED_INTERSTITIAL` | Rewarded interstitial ad format. |
| `APP_OPEN` | App open / splash format. |
| `UNKNOWN` | Unknown format. |

### YieldEnvironmentType

| Value | Description |
|-------|-------------|
| `MOBILE` | Mobile app environment. |
| `VIDEO_VAST` | Video VAST player environment. |
| `WEB` | Web browser environment. |
| `UNKNOWN` | Unknown environment. |

### YieldEntityStatus

| Value | Description |
|-------|-------------|
| `ACTIVE` | Active. |
| `INACTIVE` | Inactive / Paused. |
| `DELETED` | Deleted. |
| `EXPERIMENTING` | Experimenting. |
| `UNKNOWN` | Unknown. |
