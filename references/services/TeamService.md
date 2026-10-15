# TeamService Reference

**Service**: TeamService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/TeamService
**Types**: 4

## Methods

### createTeams
- **Request**: `Team[] teams`
- **Response**: `Team[]`

### getTeamsByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `id`, `name`, `description`, `status`, `hasAllCompanies`, `hasAllInventory`)
- **Response**: `TeamPage`

### performTeamAction
- **Request**: `TeamAction teamAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateTeams
- **Request**: `Team[] teams`
- **Response**: `Team[]`

## Types

### Team

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the `Team`. This value is readonly and is assigned by Google. |
| `name` | `string` | The name of the `Team`. This value is required to create a team and has a maximum length of 106 characters. |
| `description` | `string` | The description of the `Team`. This value is optional and has a maximum length of 255 characters. |
| `status` | `TeamStatus` | The status of the `Team`. This value is read-only. |
| `hasAllCompanies` | `boolean` | Whether or not users on this team have access to all companies. If this value is true, then `companyIds` must be empty. |
| `companyIds` | `long[]` | The IDs of the companies on the team. |
| `hasAllInventory` | `boolean` | Whether or not users on this team have access to all inventory. If this value is true, then `adUnitIds` must be empty. |
| `adUnitIds` | `string[]` | The IDs of the root ad units on the team. |
| `teamAccessType` | `TeamAccessType` | The default access to orders, for users on this team. |

### TeamPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `Team[]` | The collection of teams contained within this page. |

### TeamAction (Subclasses)
- `ActivateTeams` (`{'xsi_type': 'ActivateTeams'}`)
- `DeactivateTeams` (`{'xsi_type': 'DeactivateTeams'}`)

## Enumerations

### TeamStatus

| Value | Description |
|-------|-------------|
| `ACTIVE` | The status of an active team. |
| `INACTIVE` | The status of an inactive team. |
| `UNKNOWN` | Unknown status. |

### TeamAccessType

| Value | Description |
|-------|-------------|
| `NONE` | The level of access in which team members cannot view or edit a team's orders. |
| `READ_ONLY` | The level of access in which team members can only view a team's orders. |
| `READ_WRITE` | The level of access in which team members can view and edit a team's orders. |
