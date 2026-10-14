# CreativeService Cheatsheet

## Methods

### createCreatives
Creates new [Creative](/ad-manager/api/reference/v202608/CreativeService.Creative) objects.

### getCreativesByStatement
Gets a [CreativePage](/ad-manager/api/reference/v202608/CreativeService.CreativePage) of [Creative](/ad-manager/api/reference/v202608/CreativeService.Creative) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/CreativeService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [Creative.id](/ad-manager/api/reference/v202608/CreativeService.Creative#id) |
| `name` | [Creative.name](/ad-manager/api/reference/v202608/CreativeService.Creative#name) |
| `advertiserId` | [Creative.advertiserId](/ad-manager/api/reference/v202608/CreativeService.Creative#advertiserId) |
| `width` | [Creative.size](/ad-manager/api/reference/v202608/CreativeService.Creative#size) |
| `height` | [Creative.size](/ad-manager/api/reference/v202608/CreativeService.Creative#size) |
| `lastModifiedDateTime` | [Creative.lastModifiedDateTime](/ad-manager/api/reference/v202608/CreativeService.Creative#lastModifiedDateTime) |

### performCreativeAction
Performs action on [Creative](/ad-manager/api/reference/v202608/CreativeService.Creative) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/CreativeService.Statement#query).

### updateCreatives
Updates the specified [Creative](/ad-manager/api/reference/v202608/CreativeService.Creative) objects.
