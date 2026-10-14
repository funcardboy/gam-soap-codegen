# CreativeSetService Cheatsheet

## Methods

### createCreativeSet
Creates a new [CreativeSet](/ad-manager/api/reference/v202608/CreativeSetService.CreativeSet).

### getCreativeSetsByStatement
Gets a [CreativeSetPage](/ad-manager/api/reference/v202608/CreativeSetService.CreativeSetPage) of [CreativeSet](/ad-manager/api/reference/v202608/CreativeSetService.CreativeSet) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/CreativeSetService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [CreativeSet.id](/ad-manager/api/reference/v202608/CreativeSetService.CreativeSet#id) |
| `name` | [CreativeSet.name](/ad-manager/api/reference/v202608/CreativeSetService.CreativeSet#name) |
| `masterCreativeId` | [CreativeSet.masterCreativeId](/ad-manager/api/reference/v202608/CreativeSetService.CreativeSet#masterCreativeId) |
| `lastModifiedDateTime` | [CreativeSet.lastModifiedDateTime](/ad-manager/api/reference/v202608/CreativeSetService.CreativeSet#lastModifiedDateTime) |

### updateCreativeSet
Updates the specified [CreativeSet](/ad-manager/api/reference/v202608/CreativeSetService.CreativeSet).
