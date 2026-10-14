# MobileApplicationService Cheatsheet

## Methods

### createMobileApplications
Creates and claims [mobile applications](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication) to be used for targeting in
the network.

### getMobileApplicationsByStatement
Gets a [mobileApplicationPage](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplicationPage) of [mobile
applications](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication) that satisfy the given [Statement](/ad-manager/api/reference/v202608/MobileApplicationService.Statement). The following fields
are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [MobileApplication.id](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication#id) |
| `displayName` | [MobileApplication.displayName](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication#displayName) |
| `appStore` | [MobileApplication.appStore](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication#appStore) |
| `mobileApplicationExternalId` | [MobileApplication.appStoreId](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication#appStoreId) |
| `isArchived` | [MobileApplication.isArchived](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication#isArchived) |

### performMobileApplicationAction
Performs an action on [mobile applications](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication).

### updateMobileApplications
Updates the specified [mobile applications](/ad-manager/api/reference/v202608/MobileApplicationService.MobileApplication).
