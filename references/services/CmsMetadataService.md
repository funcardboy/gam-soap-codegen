# CmsMetadataService Cheatsheet

## Methods

### getCmsMetadataKeysByStatement
Returns a page of [CmsMetadataKey](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataKey)s matching the specified [Statement](/ad-manager/api/reference/v202608/CmsMetadataService.Statement). The
following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [CmsMetadataKey.cmsMetadataKeyId](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataKey#cmsMetadataKeyId) |
| `cmsKey` | [CmsMetadataKey.keyName](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataKey#keyName) |
| `status` | [CmsMetadataKey.status](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataKey#status) |

### getCmsMetadataValuesByStatement
Returns a page of [CmsMetadataValue](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataValue)s matching the specified [Statement](/ad-manager/api/reference/v202608/CmsMetadataService.Statement). The
following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [CmsMetadataValue.cmsMetadataValueId](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataValue#cmsMetadataValueId) |
| `cmsValue` | [CmsMetadataValue.valueName](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataValue#valueName) |
| `cmsKey` | [CmsMetadataValue.key](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataValue#key) |
| `cmsKeyId` | [CmsMetadataValue.key](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataValue#key) |
| `status` | [CmsMetadataValue.status](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataValue#status) |

### performCmsMetadataKeyAction
Performs actions on [CmsMetadataKey](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataKey) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/CmsMetadataService.Statement#query).

### performCmsMetadataValueAction
Performs actions on [CmsMetadataValue](/ad-manager/api/reference/v202608/CmsMetadataService.CmsMetadataValue) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/CmsMetadataService.Statement#query).
