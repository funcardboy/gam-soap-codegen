# CustomTargetingService Cheatsheet

## Methods

### createCustomTargetingKeys
Creates new [CustomTargetingKey](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey) objects.
The following fields are required:
* [CustomTargetingKey.name](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey#name)
* [CustomTargetingKey.type](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey#type)

### createCustomTargetingValues
Creates new [CustomTargetingValue](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue) objects.
The following fields are required:
* [CustomTargetingValue.customTargetingKeyId](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue#customTargetingKeyId)
* [CustomTargetingValue.name](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue#name)

### getCustomTargetingKeysByStatement
Gets a [CustomTargetingKeyPage](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKeyPage) of [CustomTargetingKey](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey) objects that satisfy
the given [Statement.query](/ad-manager/api/reference/v202608/CustomTargetingService.Statement#query). The following fields are supported for
filtering:
| PQL Property | Object Property |
| --- | --- |
|  |
| `id` | [CustomTargetingKey.id](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey#id) |
| `name` | [CustomTargetingKey.name](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey#name) |
| `displayName` | [CustomTargetingKey.displayName](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey#displayName) |
| `type` | [CustomTargetingKey.type](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey#type) |

### getCustomTargetingValuesByStatement
Gets a [CustomTargetingValuePage](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValuePage) of [CustomTargetingValue](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue) objects that
satisfy the given [Statement.query](/ad-manager/api/reference/v202608/CustomTargetingService.Statement#query).
The `WHERE` clause in the
[Statement.query](/ad-manager/api/reference/v202608/CustomTargetingService.Statement#query) must always contain [CustomTargetingValue.customTargetingKeyId](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue#customTargetingKeyId) as one of its columns in a way that it is
AND'ed with the rest of the query. So, if you want to retrieve
values for a known set of key ids, valid [Statement.query](/ad-manager/api/reference/v202608/CustomTargetingService.Statement#query) would look like:
1. "WHERE customTargetingKeyId IN ('17','18','19')" retrieves all
values that are associated with keys having ids 17, 18, 19.
2. "WHERE customTargetingKeyId = '17' AND name = 'red'" retrieves
values that are associated with keys having id 17 and value name is
'red'.
The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [CustomTargetingValue.id](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue#id) |
| `customTargetingKeyId` | [CustomTargetingValue.customTargetingKeyId](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue#customTargetingKeyId) |
| `name` | [CustomTargetingValue.name](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue#name) |
| `displayName` | [CustomTargetingValue.displayName](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue#displayName) |
| `matchType` | [CustomTargetingValue.matchType](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue#matchType) |

### performCustomTargetingKeyAction
Performs actions on [CustomTargetingKey](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/CustomTargetingService.Statement#query).

### performCustomTargetingValueAction
Performs actions on [CustomTargetingValue](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/CustomTargetingService.Statement#query).

### updateCustomTargetingKeys
Updates the specified [CustomTargetingKey](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingKey) objects.

### updateCustomTargetingValues
Updates the specified [CustomTargetingValue](/ad-manager/api/reference/v202608/CustomTargetingService.CustomTargetingValue) objects.
