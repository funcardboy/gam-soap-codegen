# LabelService Cheatsheet

## Methods

### createLabels
Creates new [Label](/ad-manager/api/reference/v202608/LabelService.Label) objects.

### getLabelsByStatement
Gets a [LabelPage](/ad-manager/api/reference/v202608/LabelService.LabelPage) of [Label](/ad-manager/api/reference/v202608/LabelService.Label) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/LabelService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [Label.id](/ad-manager/api/reference/v202608/LabelService.Label#id) |
| `type` | [Label.type](/ad-manager/api/reference/v202608/LabelService.Label#type) |
| `name` | [Label.name](/ad-manager/api/reference/v202608/LabelService.Label#name) |
| `description` | [Label.description](/ad-manager/api/reference/v202608/LabelService.Label#description) |
| `isActive` | [Label.isActive](/ad-manager/api/reference/v202608/LabelService.Label#isActive) |

### performLabelAction
Performs actions on [Label](/ad-manager/api/reference/v202608/LabelService.Label) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/LabelService.Statement#query).

### updateLabels
Updates the specified [Label](/ad-manager/api/reference/v202608/LabelService.Label) objects.
