# UserTeamAssociationService Reference

**Service**: UserTeamAssociationService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/UserTeamAssociationService
**Types**: 4

## Methods

### createUserTeamAssociations
- **Request**: `UserTeamAssociation[] userTeamAssociations`
- **Response**: `UserTeamAssociation[]`

### getUserTeamAssociationsByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `userId`, `teamId`)
- **Response**: `UserTeamAssociationPage`

### performUserTeamAssociationAction
- **Request**: `UserTeamAssociationAction userTeamAssociationAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateUserTeamAssociations
- **Request**: `UserTeamAssociation[] userTeamAssociations`
- **Response**: `UserTeamAssociation[]`

## Types

### UserTeamAssociation

| Field | Type | Description |
|-------|------|-------------|
| `teamId` | `long` | The `Team.id` of the team. Required. |
| `overriddenTeamAccessType` | `TeamAccessType` | The overridden team access type. This field is `null` if team access type is not overridden. |
| `defaultTeamAccessType` | `TeamAccessType` | The default team access type (`Team.teamAccessType`). This field is read-only and is populated by Google. |
| `userId` | `long` | The `User.id` of the user. Required. |

### UserTeamAssociationPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `UserTeamAssociation[]` | The collection of user team associations contained within this page. |

### UserTeamAssociationAction (Subclasses)
- `DeleteUserTeamAssociations` (`{'xsi_type': 'DeleteUserTeamAssociations'}`)

## Enumerations

### TeamAccessType

| Value | Description |
|-------|-------------|
| `NONE` | Team members cannot view or edit a team's orders. |
| `READ_ONLY` | Team members can only view a team's orders. |
| `READ_WRITE` | Team members can view and edit a team's orders. |
