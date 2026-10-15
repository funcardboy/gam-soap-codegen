# TargetingPresetService Reference

**Service**: TargetingPresetService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/TargetingPresetService
**Types**: 4

## Methods

### createTargetingPresets
- **Request**: `TargetingPreset[] targetingPresets`
- **Response**: `TargetingPreset[]`

### getTargetingPresetsByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `id`, `name`)
- **Response**: `TargetingPresetPage`

### performTargetingPresetAction
- **Request**: `TargetingPresetAction targetingPresetAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateTargetingPresets
- **Request**: `TargetingPreset[] targetingPresets`
- **Response**: `TargetingPreset[]`

## Types

### TargetingPreset

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the `TargetingPreset`. This value is readonly and is assigned by Google. |
| `name` | `string` | The name of the `TargetingPreset`. This value is required and has a maximum length of 255 characters. |
| `targeting` | `Targeting` | Contains the `Targeting` criteria for the `TargetingPreset`. This attribute is required. |

### TargetingPresetPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `TargetingPreset[]` | The collection of targeting presets contained within this page. |

### TargetingPresetAction (Subclasses)
- `DeleteTargetingPresets` (`{'xsi_type': 'DeleteTargetingPresets'}`)
