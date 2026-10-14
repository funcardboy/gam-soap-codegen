# CustomFieldService Cheatsheet

## Methods

### createCustomFieldOptions
Creates new [CustomFieldOption](/ad-manager/api/reference/v202608/CustomFieldService.CustomFieldOption) objects.
The following fields are required:
* [CustomFieldOption.displayName](/ad-manager/api/reference/v202608/CustomFieldService.CustomFieldOption#displayName)
* [CustomFieldOption.customFieldId](/ad-manager/api/reference/v202608/CustomFieldService.CustomFieldOption#customFieldId)

### createCustomFields
Creates new [CustomField](/ad-manager/api/reference/v202608/CustomFieldService.CustomField) objects.
The following fields are required:
* [CustomField.name](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#name)
* [CustomField.entityType](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#entityType)
* [CustomField.dataType](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#dataType)
* [CustomField.visibility](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#visibility)

### getCustomFieldOption
Returns the [CustomFieldOption](/ad-manager/api/reference/v202608/CustomFieldService.CustomFieldOption) uniquely identified by the given ID.

### getCustomFieldsByStatement
Gets a [CustomFieldPage](/ad-manager/api/reference/v202608/CustomFieldService.CustomFieldPage) of [CustomField](/ad-manager/api/reference/v202608/CustomFieldService.CustomField) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/CustomFieldService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [CustomField.id](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#id) |
| `entityType` | [CustomField.entityType](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#entityType) |
| `name` | [CustomField.name](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#name) |
| `isActive` | [CustomField.isActive](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#isActive) |
| `visibility` | [CustomField.visibility](/ad-manager/api/reference/v202608/CustomFieldService.CustomField#visibility) |

### performCustomFieldAction
Performs actions on [CustomField](/ad-manager/api/reference/v202608/CustomFieldService.CustomField) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/CustomFieldService.Statement#query).

### updateCustomFieldOptions
Updates the specified [CustomFieldOption](/ad-manager/api/reference/v202608/CustomFieldService.CustomFieldOption) objects.

### updateCustomFields
Updates the specified [CustomField](/ad-manager/api/reference/v202608/CustomFieldService.CustomField) objects.
