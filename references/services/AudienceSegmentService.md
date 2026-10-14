# AudienceSegmentService Cheatsheet

## Methods

### createAudienceSegments
Creates new [FirstPartyAudienceSegment](/ad-manager/api/reference/v202608/AudienceSegmentService.FirstPartyAudienceSegment) objects.

### getAudienceSegmentsByStatement
Gets an [AudienceSegmentPage](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegmentPage) of [AudienceSegment](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegment) objects that satisfy the given
[Statement.query](/ad-manager/api/reference/v202608/AudienceSegmentService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [AudienceSegment.id](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegment#id) |
| `name` | [AudienceSegment.name](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegment#name) |
| `status` | [AudienceSegment.status](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegment#status) |
| `type` | [AudienceSegment.type](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegment#type) |
| `size` | [AudienceSegment.size](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegment#size) |
| `dataProviderName` | [AudienceSegmentDataProvider.name](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegmentDataProvider#name) |
| `segmentType` | [AudienceSegment.type](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegment#type) |
| `approvalStatus` | [ThirdPartyAudienceSegment.approvalStatus](/ad-manager/api/reference/v202608/AudienceSegmentService.ThirdPartyAudienceSegment#approvalStatus) |
| `cost` | [ThirdPartyAudienceSegment.cost](/ad-manager/api/reference/v202608/AudienceSegmentService.ThirdPartyAudienceSegment#cost) |
| `startDateTime` | [ThirdPartyAudienceSegment.startDateTime](/ad-manager/api/reference/v202608/AudienceSegmentService.ThirdPartyAudienceSegment#startDateTime) |
| `endDateTime` | [ThirdPartyAudienceSegment.endDateTime](/ad-manager/api/reference/v202608/AudienceSegmentService.ThirdPartyAudienceSegment#endDateTime) |

### performAudienceSegmentAction
Performs the given [AudienceSegmentAction](/ad-manager/api/reference/v202608/AudienceSegmentService.AudienceSegmentAction) on the set of segments identified by the given
statement.

### updateAudienceSegments
Updates the given [FirstPartyAudienceSegment](/ad-manager/api/reference/v202608/AudienceSegmentService.FirstPartyAudienceSegment) objects.
