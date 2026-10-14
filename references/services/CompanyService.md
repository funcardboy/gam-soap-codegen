# CompanyService Cheatsheet

## Methods

### createCompanies
Creates new [Company](/ad-manager/api/reference/v202608/CompanyService.Company) objects.

### getCompaniesByStatement
Gets a [CompanyPage](/ad-manager/api/reference/v202608/CompanyService.CompanyPage) of [Company](/ad-manager/api/reference/v202608/CompanyService.Company) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/CompanyService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [Company.id](/ad-manager/api/reference/v202608/CompanyService.Company#id) |
| `name` | [Company.name](/ad-manager/api/reference/v202608/CompanyService.Company#name) |
| `type` | [Company.type](/ad-manager/api/reference/v202608/CompanyService.Company#type) |
| `lastModifiedDateTime` | [Company.lastModifiedDateTime](/ad-manager/api/reference/v202608/CompanyService.Company#lastModifiedDateTime) |

### performCompanyAction
Performs actions on [Company](/ad-manager/api/reference/v202608/CompanyService.Company) objects that match the given `Statement`.

### updateCompanies
Updates the specified [Company](/ad-manager/api/reference/v202608/CompanyService.Company) objects.
