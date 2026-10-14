# NativeStyleService Cheatsheet

## Methods

### createNativeStyles
Creates new [NativeStyle](/ad-manager/api/reference/v202608/NativeStyleService.NativeStyle) objects.

### getNativeStylesByStatement
Gets a [NativeStylePage](/ad-manager/api/reference/v202608/NativeStyleService.NativeStylePage) of [NativeStyle](/ad-manager/api/reference/v202608/NativeStyleService.NativeStyle) objects that satisfy the
given [Statement](/ad-manager/api/reference/v202608/NativeStyleService.Statement). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [NativeStyle.id](/ad-manager/api/reference/v202608/NativeStyleService.NativeStyle#id) |
| `name` | [NativeStyle.name](/ad-manager/api/reference/v202608/NativeStyleService.NativeStyle#name) |

### performNativeStyleAction
Performs actions on [native styles](/ad-manager/api/reference/v202608/NativeStyleService.NativeStyle) that match the given [Statement](/ad-manager/api/reference/v202608/NativeStyleService.Statement).

### updateNativeStyles
Updates the specified [NativeStyle](/ad-manager/api/reference/v202608/NativeStyleService.NativeStyle) objects.
