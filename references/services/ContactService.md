# ContactService Cheatsheet

## Methods

### createContacts
Creates new [Contact](/ad-manager/api/reference/v202608/ContactService.Contact) objects.

### getContactsByStatement
Gets a [ContactPage](/ad-manager/api/reference/v202608/ContactService.ContactPage) of [Contact](/ad-manager/api/reference/v202608/ContactService.Contact) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/ContactService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `name` | [Contact.name](/ad-manager/api/reference/v202608/ContactService.Contact#name) |
| `email` | [Contact.email](/ad-manager/api/reference/v202608/ContactService.Contact#email) |
| `id` | [Contact.id](/ad-manager/api/reference/v202608/ContactService.Contact#id) |
| `comment` | [Contact.comment](/ad-manager/api/reference/v202608/ContactService.Contact#comment) |
| `companyId` | [Contact.companyId](/ad-manager/api/reference/v202608/ContactService.Contact#companyId) |
| `title` | [Contact.title](/ad-manager/api/reference/v202608/ContactService.Contact#title) |
| `cellPhone` | [Contact.cellPhone](/ad-manager/api/reference/v202608/ContactService.Contact#cellPhone) |
| `workPhone` | [Contact.workPhone](/ad-manager/api/reference/v202608/ContactService.Contact#workPhone) |
| `faxPhone` | [Contact.faxPhone](/ad-manager/api/reference/v202608/ContactService.Contact#faxPhone) |
| `status` | [Contact.status](/ad-manager/api/reference/v202608/ContactService.Contact#status) |

### updateContacts
Updates the specified [Contact](/ad-manager/api/reference/v202608/ContactService.Contact) objects.
