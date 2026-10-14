# CdnConfigurationService Cheatsheet

## Methods

### createCdnConfigurations
Creates new [CdnConfiguration](/ad-manager/api/reference/v202608/CdnConfigurationService.CdnConfiguration) objects.

### getCdnConfigurationsByStatement
Gets a [CdnConfigurationPage](/ad-manager/api/reference/v202608/CdnConfigurationService.CdnConfigurationPage) of [CdnConfiguration](/ad-manager/api/reference/v202608/CdnConfigurationService.CdnConfiguration) objects that satisfy the given
[Statement.query](/ad-manager/api/reference/v202608/CdnConfigurationService.Statement#query). Currently only CDN Configurations of type [CdnConfigurationType.LIVE\_STREAM\_SOURCE\_CONTENT](/ad-manager/api/reference/v202608/CdnConfigurationService.CdnConfigurationType#LIVE_STREAM_SOURCE_CONTENT) will be returned. The following fields are
supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [CdnConfiguration.id](/ad-manager/api/reference/v202608/CdnConfigurationService.CdnConfiguration#id) |
| `name` | [CdnConfiguration.name](/ad-manager/api/reference/v202608/CdnConfigurationService.CdnConfiguration#name) |

### performCdnConfigurationAction
Performs actions on [CdnConfiguration](/ad-manager/api/reference/v202608/CdnConfigurationService.CdnConfiguration) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/CdnConfigurationService.Statement#query).

### updateCdnConfigurations
Updates the specified [CdnConfiguration](/ad-manager/api/reference/v202608/CdnConfigurationService.CdnConfiguration) objects.
