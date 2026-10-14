# DaiAuthenticationKeyService Cheatsheet

## Methods

### createDaiAuthenticationKeys
Creates new [DaiAuthenticationKey](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKey) objects.
The following fields are required:
* [DaiAuthenticationKey.name](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKey#name)

### getDaiAuthenticationKeysByStatement
Gets a [DaiAuthenticationKeyPage](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKeyPage) of [DaiAuthenticationKey](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKey) objects that satisfy
the given [Statement.query](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [DaiAuthenticationKey.id](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKey#id) |
| `status` | [DaiAuthenticationKey.status](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKey#status) |
| `name` | [DaiAuthenticationKey.name](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKey#name) |

### performDaiAuthenticationKeyAction
Performs actions on [DaiAuthenticationKey](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKey) objects that match
the given [Statement.query](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.Statement#query).
DAI authentication keys cannot be deactivated if there are
active [LiveStreamEvent](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent)s or Content Sources that are using them.

### updateDaiAuthenticationKeys
Updates the specified [DaiAuthenticationKey](/ad-manager/api/reference/v202608/DaiAuthenticationKeyService.DaiAuthenticationKey) objects.
