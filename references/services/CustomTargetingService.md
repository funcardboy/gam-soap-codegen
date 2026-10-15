# CustomTargetingService Reference

**Service**: CustomTargetingService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/CustomTargetingService
**Types**: 6

## Methods
- `createCustomTargetingKeys(CustomTargetingKey[] keys) -> CustomTargetingKey[]`
- `createCustomTargetingValues(CustomTargetingValue[] values) -> CustomTargetingValue[]`
- `getCustomTargetingKeysByStatement(Statement filterStatement) -> CustomTargetingKeyPage` (PQL filterable: `id`, `name`, `displayName`, `type`, `status`)
- `getCustomTargetingValuesByStatement(Statement filterStatement) -> CustomTargetingValuePage` (PQL filterable: `customTargetingKeyId`, `id`, `name`, `displayName`, `matchType`, `status`)
- `performCustomTargetingKeyAction(CustomTargetingKeyAction customTargetingKeyAction, Statement filterStatement) -> UpdateResult`
- `performCustomTargetingValueAction(CustomTargetingValueAction customTargetingValueAction, Statement filterStatement) -> UpdateResult`
- `updateCustomTargetingKeys(CustomTargetingKey[] keys) -> CustomTargetingKey[]`
- `updateCustomTargetingValues(CustomTargetingValue[] values) -> CustomTargetingValue[]`

## Types

### CustomTargetingKey
| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The ID of the `CustomTargetingKey`. Read-only. |
| `name` | `string` | Name of the key (passed in ad tag). Max 10 chars, alphanumeric + `._-`. Required. |
| `displayName` | `string` | Descriptive name for the key in GAM UI. Max 20 chars. |
| `type` | `CustomTargetingKey.Type` | `PREDEFINED` or `FREEFORM`. Required. |
| `status` | `CustomTargetingKey.Status` | `ACTIVE`, `INACTIVE`, `UNKNOWN`. Read-only. |
| `reportableType` | `ReportableType` | `ON`, `OFF`, `CUSTOM_DIMENSION`. |

### CustomTargetingValue
| Field | Type | Description |
|-------|------|-------------|
| `customTargetingKeyId` | `long` | The ID of the `CustomTargetingKey` that owns this value. Required. |
| `id` | `long` | The ID of the `CustomTargetingValue`. Read-only. |
| `name` | `string` | Name of the value (passed in ad tag). Max 40 chars. Required. |
| `displayName` | `string` | Descriptive name in GAM UI. Max 40 chars. |
| `matchType` | `CustomTargetingValue.MatchType` | `EXACT`, `BROAD`, `PREFIX`, `BROAD_PREFIX`, `SUFFIX`, `CONTAINS`. |
| `status` | `CustomTargetingValue.Status` | `ACTIVE`, `INACTIVE`, `UNKNOWN`. Read-only. |
