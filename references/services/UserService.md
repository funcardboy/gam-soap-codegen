# UserService Reference

**Service**: UserService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/UserService
**Types**: 5

## Methods

### createUsers
- **Request**: `User[] users`
- **Response**: `User[]`

### getAllRoles
- **Request**: None
- **Response**: `Role[]`

### getCurrentUser
- **Request**: None
- **Response**: `User`

### getUsersByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `id`, `name`, `email`, `roleId`, `roleName`, `isActive`)
- **Response**: `UserPage`

### performUserAction
- **Request**: `UserAction userAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateUsers
- **Request**: `User[] users`
- **Response**: `User[]`

## Types

### User

| Field | Type | Description |
|-------|------|-------------|
| **`UserRecord` (inherited)** | | |
| `id` | `long` | The unique ID of the `User`. This attribute is read-only. |
| `name` | `string` | The name of the `User`. Required, max 128 characters. |
| `email` | `string` | The email or login of the `User`. Required. |
| `roleId` | `long` | The unique role ID of the `User` (`-1` for Administrator). Required. |
| `roleName` | `string` | The name of the role assigned to the `User`. This attribute is read-only. |
| **`User`** | | |
| `isActive` | `boolean` | Specifies whether or not the `User` is active. An inactive user cannot log in to the system or make API calls. This attribute is read-only. |
| `isEmailNotificationAllowed` | `boolean` | Specifies whether or not the `User` wants to permit the Publisher Display Ads system to send email notifications to their email address. |
| `externalId` | `string` | An identifier for the `User` that is meaningful to the publisher. Optional, max 255 characters. |
| `isServiceAccount` | `boolean` | Whether the user is an OAuth2 service account user. This attribute is read-only. |
| `ordersUiLocalTimeZoneId` | `string` | The long format timezone id (e.g. `"Asia/Hong_Kong"`) used in the Orders and Line Items UI for this `User`. |

### UserPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `User[]` | The collection of users contained within this page. |

### Role

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the `Role`. This value is readonly and is assigned by Google. Roles that are created by Google will have negative IDs. |
| `name` | `string` | The name of the `Role`. This value is readonly and is assigned by Google. |
| `description` | `string` | The description of the `Role`. This value is readonly and is assigned by Google. |
| `status` | `RoleStatus` | The status of the `Role`. This field is read-only. |

### UserAction (Subclasses)
- `ActivateUsers` (`{'xsi_type': 'ActivateUsers'}`)
- `DeactivateUsers` (`{'xsi_type': 'DeactivateUsers'}`)

## Enumerations

### RoleStatus

| Value | Description |
|-------|-------------|
| `ACTIVE` | The status of an active role. |
| `INACTIVE` | The status of an inactive role. |
| `UNKNOWN` | Unknown role status. |
