# CreativeWrapperService Cheatsheet

## Methods

### createCreativeWrappers
Creates a new `CreativeWrapper`
objects.
The following fields are required:
* [CreativeWrapper.labelId](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper#labelId)
* [CreativeWrapper.ordering](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper#ordering)
* [CreativeWrapper.header](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper#header) or [CreativeWrapper.footer](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper#footer)

### getCreativeWrappersByStatement
Gets a [CreativeWrapperPage](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapperPage) of [CreativeWrapper](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper) objects that satisfy the given
[Statement.query](/ad-manager/api/reference/v202608/CreativeWrapperService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [CreativeWrapper.id](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper#id) |
| `labelId` | [CreativeWrapper.labelId](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper#labelId) |
| `status` | [CreativeWrapper.status](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper#status) |
| `ordering` | [CreativeWrapper.ordering](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper#ordering) |

### performCreativeWrapperAction
Performs actions on [CreativeWrapper](/ad-manager/api/reference/v202608/CreativeWrapperService.CreativeWrapper) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/CreativeWrapperService.Statement#query).

### updateCreativeWrappers
Updates the specified `CreativeWrapper` objects.
