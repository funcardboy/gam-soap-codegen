# SuggestedAdUnitService Reference

**Service**: SuggestedAdUnitService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/SuggestedAdUnitService
**Types**: 5

## Methods

### getSuggestedAdUnitsByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `id`, `numRequests`)
- **Response**: `SuggestedAdUnitPage`

### performSuggestedAdUnitAction
- **Request**: `SuggestedAdUnitAction suggestedAdUnitAction`, `Statement filterStatement`
- **Response**: `SuggestedAdUnitUpdateResult`

## Types

### SuggestedAdUnit

| Field | Type | Description |
|-------|------|-------------|
| `id` | `string` | The unique ID of the `SuggestedAdUnit`. Read-only. |
| `numRequests` | `long` | The number of times the ad tag corresponding to this suggested ad unit has been requested in the past 7 days. Read-only. |
| `path` | `string[]` | The hierarchical path of ad unit names that precedes the suggested ad unit. Read-only. |
| `parentPath` | `AdUnitParent[]` | The existing hierarchy of ad units under which this suggested ad unit would be created. Read-only. |
| `targetWindow` | `AdUnitTargetWindow` | The target window attribute specified in the ad tag. Read-only. |
| `targetPlatform` | `TargetPlatform` | The target platform of the browser that requested the ad tag. Read-only. |
| `suggestedAdUnitSizes` | `AdUnitSize[]` | The sizes specified in the ad tag. Read-only. |

### SuggestedAdUnitPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `SuggestedAdUnit[]` | The collection of suggested ad units contained within this page. |

### SuggestedAdUnitUpdateResult

| Field | Type | Description |
|-------|------|-------------|
| `newAdUnitIds` | `string[]` | The IDs of the newly created `AdUnit` objects when approving suggested ad units. |
| `numChanges` | `int` | The number of objects that were changed as a result of the action. |

### SuggestedAdUnitAction (Subclasses)
- `ApproveSuggestedAdUnits` (`{'xsi_type': 'ApproveSuggestedAdUnits'}`)

## Enumerations

### TargetPlatform

| Value | Description |
|-------|-------------|
| `WEB` | The desktop or mobile web browser platform. |
| `MOBILE` | Mobile applications. |
| `ANY` | Both web and mobile platforms. |
