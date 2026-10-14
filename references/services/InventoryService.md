# InventoryService Cheatsheet

## Methods

### createAdUnits
Creates new [AdUnit](/ad-manager/api/reference/v202608/InventoryService.AdUnit) objects.

### getAdUnitSizesByStatement
Returns a set of all relevant [AdUnitSize](/ad-manager/api/reference/v202608/InventoryService.AdUnitSize) objects.
The given [Statement](/ad-manager/api/reference/v202608/InventoryService.Statement) is currently ignored but may be honored in
future versions.

### getAdUnitsByStatement
Gets a [AdUnitPage](/ad-manager/api/reference/v202608/InventoryService.AdUnitPage) of [AdUnit](/ad-manager/api/reference/v202608/InventoryService.AdUnit) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/InventoryService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `adUnitCode` | [AdUnit.adUnitCode](/ad-manager/api/reference/v202608/InventoryService.AdUnit#adUnitCode) |
| `id` | [AdUnit.id](/ad-manager/api/reference/v202608/InventoryService.AdUnit#id) |
| `name` | [AdUnit.name](/ad-manager/api/reference/v202608/InventoryService.AdUnit#name) |
| `parentId` | [AdUnit.parentId](/ad-manager/api/reference/v202608/InventoryService.AdUnit#parentId) |
| `status` | [AdUnit.status](/ad-manager/api/reference/v202608/InventoryService.AdUnit#status) |
| `lastModifiedDateTime` | [AdUnit.lastModifiedDateTime](/ad-manager/api/reference/v202608/InventoryService.AdUnit#lastModifiedDateTime) |

### performAdUnitAction
Performs actions on [AdUnit](/ad-manager/api/reference/v202608/InventoryService.AdUnit) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/InventoryService.Statement#query).

### updateAdUnits
Updates the specified [AdUnit](/ad-manager/api/reference/v202608/InventoryService.AdUnit) objects.
