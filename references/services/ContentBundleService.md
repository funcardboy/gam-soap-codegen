# ContentBundleService Cheatsheet

## Methods

### createContentBundles
Creates new [ContentBundle](/ad-manager/api/reference/v202608/ContentBundleService.ContentBundle) objects.

### getContentBundlesByStatement
Gets a [ContentBundlePage](/ad-manager/api/reference/v202608/ContentBundleService.ContentBundlePage) of [ContentBundle](/ad-manager/api/reference/v202608/ContentBundleService.ContentBundle) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/ContentBundleService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [ContentBundle.id](/ad-manager/api/reference/v202608/ContentBundleService.ContentBundle#id) |
| `name` | [ContentBundle.name](/ad-manager/api/reference/v202608/ContentBundleService.ContentBundle#name) |
| `status` | [ContentBundle.status](/ad-manager/api/reference/v202608/ContentBundleService.ContentBundle#status) |

### performContentBundleAction
Performs actions on [ContentBundle](/ad-manager/api/reference/v202608/ContentBundleService.ContentBundle) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/ContentBundleService.Statement#query).

### updateContentBundles
Updates the specified [ContentBundle](/ad-manager/api/reference/v202608/ContentBundleService.ContentBundle) objects.
