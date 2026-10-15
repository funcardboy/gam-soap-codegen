# CompanyService Reference

**Service**: CompanyService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/CompanyService
**Types**: 4

## Methods
- `createCompanies(Company[] companies) -> Company[]`
- `getCompaniesByStatement(Statement filterStatement) -> CompanyPage` (PQL filterable: `id`, `name`, `type`, `creditStatus`, `externalId`, `lastModifiedDateTime`)
- `updateCompanies(Company[] companies) -> Company[]`

## Types
### Company
| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | Uniquely identifies the `Company`. Read-only. |
| `name` | `string` | The full name of the company. Required, max 127 chars, unique per `type`. |
| `type` | `Company.Type` | `ADVERTISER`, `HOUSE_ADVERTISER`, `AGENCY`, `HOUSE_AGENCY`, `AD_NETWORK`, `PARTNER`, `VIEWABILITY_PROVIDER`. Required. |
| `address` | `string` | Physical address. |
| `email` | `string` | Email address. |
| `faxPhone` / `primaryPhone` | `string` | Phone numbers. |
| `externalId` | `string` | External system ID. |
| `comment` | `string` | Notes/comments. |
| `creditStatus` | `Company.CreditStatus` | `ACTIVE`, `ON_HOLD`, `CREDIT_STOP`, `INACTIVE`, `BLOCKED`. |
| `appliedLabels` | `AppliedLabel[]` | Labels applied directly to the company. |
| `primaryContactId` | `long` | ID of the primary `Contact`. |
| `appliedTeamIds` | `long[]` | IDs of teams associated with this company. |
| `thirdPartyCompanyId` | `int` | Third-party company ID. |
| `lastModifiedDateTime` | `DateTime` | Last modified timestamp. Read-only. |
