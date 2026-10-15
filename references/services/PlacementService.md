# PlacementService Reference

**Service**: PlacementService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/PlacementService
**Types**: 6

## Methods

### createPlacements
- **Request**: `Placement[] placements`
- **Response**: `Placement[]`

### getPlacementsByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `id`, `name`, `placementCode`, `status`, `lastModifiedDateTime`)
- **Response**: `PlacementPage`

### performPlacementAction
- **Request**: `PlacementAction placementAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updatePlacements
- **Request**: `Placement[] placements`
- **Response**: `Placement[]`

## Types

### Placement

| Field | Type | Description |
|-------|------|-------------|
| **`SiteTargetingInfo` (inherited)** | | |
| **`Placement`** | | |
| `id` | `long` | Uniquely identifies the `Placement`. This attribute is read-only and is assigned by Google when a placement is created. |
| `name` | `string` | The name of the `Placement`. This value is required and has a maximum length of 255 characters. |
| `description` | `string` | A description of the `Placement`. This value is optional and its maximum length is 65,535 characters. |
| `placementCode` | `string` | A string used to uniquely identify the `Placement` for purposes oflegibility. This attribute is read-only and is assigned by Google when a placement is created. |
| `status` | `InventoryStatus` | The status of the `Placement`. This attribute is read-only. |
| `targetedAdUnitIds` | `string[]` | The collection of `AdUnit` object IDs that constitute the `Placement`. |
| `lastModifiedDateTime` | `DateTime` | The date and time this placement was last modified. |

### PlacementPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `Placement[]` | The collection of placements contained within this page. |

### PlacementAction (Subclasses)
- `ActivatePlacements` (`{'xsi_type': 'ActivatePlacements'}`)
- `ArchivePlacements` (`{'xsi_type': 'ArchivePlacements'}`)
- `DeactivatePlacements` (`{'xsi_type': 'DeactivatePlacements'}`)

## Enumerations

### InventoryStatus

| Value | Description |
|-------|-------------|
| `ACTIVE` | The object is active and eligible to serve ads. |
| `INACTIVE` | The object is no longer active. |
| `ARCHIVED` | The object has been archived. |
