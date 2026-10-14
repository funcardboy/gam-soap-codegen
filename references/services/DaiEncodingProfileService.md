# DaiEncodingProfileService Cheatsheet

## Methods

### createDaiEncodingProfiles
Creates new [DaiEncodingProfile](/ad-manager/api/reference/v202608/DaiEncodingProfileService.DaiEncodingProfile) objects.

### getDaiEncodingProfilesByStatement
Gets a [DaiEncodingProfilePage](/ad-manager/api/reference/v202608/DaiEncodingProfileService.DaiEncodingProfilePage) of [DaiEncodingProfile](/ad-manager/api/reference/v202608/DaiEncodingProfileService.DaiEncodingProfile) objects that satisfy the
given [Statement.query](/ad-manager/api/reference/v202608/DaiEncodingProfileService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [DaiEncodingProfile.id](/ad-manager/api/reference/v202608/DaiEncodingProfileService.DaiEncodingProfile#id) |
| `status` | [DaiEncodingProfile.status](/ad-manager/api/reference/v202608/DaiEncodingProfileService.DaiEncodingProfile#status) |
| `name` | [DaiEncodingProfile.name](/ad-manager/api/reference/v202608/DaiEncodingProfileService.DaiEncodingProfile#name) |

### performDaiEncodingProfileAction
Performs actions on [DaiEncodingProfile](/ad-manager/api/reference/v202608/DaiEncodingProfileService.DaiEncodingProfile) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/DaiEncodingProfileService.Statement#query).

### updateDaiEncodingProfiles
Updates the specified [DaiEncodingProfile](/ad-manager/api/reference/v202608/DaiEncodingProfileService.DaiEncodingProfile) objects.
