# InventoryService Reference

**Service**: InventoryService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/InventoryService
**Types**: 8

## Methods
- `createAdUnits(AdUnit[] adUnits) -> AdUnit[]`
- `getAdUnitSizesByStatement(Statement filterStatement) -> AdUnitSize[]`
- `getAdUnitsByStatement(Statement filterStatement) -> AdUnitPage` (PQL filterable: `id`, `name`, `adUnitCode`, `status`, `parentId`, `lastModifiedDateTime`, `smartSizeMode`, `targetWindow`)
- `performAdUnitAction(AdUnitAction adUnitAction, Statement filterStatement) -> UpdateResult`
- `updateAdUnits(AdUnit[] adUnits) -> AdUnit[]`

## Types

### AdUnit
| Field | Type | Description |
|-------|------|-------------|
| `id` | `string` | Uniquely identifies the `AdUnit`. Read-only, assigned by Google on creation. |
| `parentId` | `string` | The ID of the `AdUnit`'s parent. Required on create (except root ad unit). |
| `hasChildren` | `boolean` | `True` if the `AdUnit` has children. Read-only. |
| `parentPath` | `AdUnitParent[]` | Ordered list of `AdUnitParent` objects (`id`, `name`, `adUnitCode`) from root to immediate parent. Read-only. |
| `name` | `string` | The name of the `AdUnit`. Required, max 255 characters. |
| `description` | `string` | A description of the `AdUnit`. Max 65,535 characters. |
| `targetWindow` | `AdUnitTargetWindow` | The value to use for the HTML link's `target` attribute (`TOP`, `BLANK`). |
| `status` | `InventoryStatus` | The status of the `AdUnit` (`ACTIVE`, `INACTIVE`, `ARCHIVED`). Read-only. |
| `adUnitCode` | `string` | A string used to uniquely identify the `AdUnit` in GPT ad tags. Max 100 chars. |
| `adUnitSizes` | `AdUnitSize[]` | The sizes that can be served inside this `AdUnit`. |
| `isInterstitial` | `boolean` | Whether this is an out-of-page / interstitial ad unit. |
| `isNative` | `boolean` | Whether this is a native ad unit. |
| `isFluid` | `boolean` | Whether this is a fluid size ad unit. |
| `explicitlyTargeted` | `boolean` | If `True`, line items must explicitly target this `AdUnit` to serve (Run-of-Network will not serve unless targeted). |
| `adSenseSettings` | `AdSenseSettings` | AdSense settings for this `AdUnit`. |
| `lastModifiedDateTime` | `DateTime` | The date and time this `AdUnit` was last modified. Read-only. |
| `smartSizeMode` | `SmartSizeMode` | Smart size mode (`NONE`, `SMART_BANNER`, `DYNAMIC_SIZE`). |
| `refreshRate` | `int` | Refresh rate in seconds for mobile app ad units (30..120). |
| `externalSetTopBoxChannelId` | `string` | External channel ID for set-top box. |
| `isSetTopBoxEnabled` | `boolean` | Whether enabled for set-top box. |
| `applicationId` | `long` | The ID of the `MobileApplication` this `AdUnit` is linked to. |

### AdUnitSize
| Field | Type | Description |
|-------|------|-------------|
| `size` | `Size` | The dimensions (`width`, `height`, `isAspectRatio`) of the creative. |
| `environmentType` | `EnvironmentType` | The environment type (`BROWSER`, `VIDEO_PLAYER`). |
| `companions` | `AdUnitSize[]` | The companions for this video ad unit size. |
| `fullDisplayString` | `string` | Display string (e.g. `"300x250"`). Read-only. |
| `isAudio` | `boolean` | Whether the size represents an audio ad. |

## Enumerations
- `InventoryStatus`: `ACTIVE`, `INACTIVE`, `ARCHIVED`
- `AdUnitTargetWindow`: `TOP`, `BLANK`
- `SmartSizeMode`: `NONE`, `SMART_BANNER`, `DYNAMIC_SIZE`
