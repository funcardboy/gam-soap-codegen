# LineItemCreativeAssociationService Cheatsheet

## Methods

### createLineItemCreativeAssociations
Creates new [LineItemCreativeAssociation](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation) objects

### getLineItemCreativeAssociationsByStatement
Gets a [LineItemCreativeAssociationPage](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociationPage) of [LineItemCreativeAssociation](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation) objects
that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.Statement#query). The following fields are supported for
filtering:
| PQL Property | Object Property |
| --- | --- |
| `creativeId` | [LineItemCreativeAssociation.creativeId](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation#creativeId) |
| `manualCreativeRotationWeight` | [LineItemCreativeAssociation.manualCreativeRotationWeight](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation#manualCreativeRotationWeight) |
| `destinationUrl` | [LineItemCreativeAssociation.destinationUrl](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation#destinationUrl) |
| `lineItemId` | [LineItemCreativeAssociation.lineItemId](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation#lineItemId) |
| `status` | [LineItemCreativeAssociation.status](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation#status) |
| `lastModifiedDateTime` | [LineItemCreativeAssociation.lastModifiedDateTime](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation#lastModifiedDateTime) |

### getPreviewUrl
Returns an insite preview URL that references the specified site URL with the specified
creative from the association served to it. For Creative Set previewing you may specify the
master creative Id.

### getPreviewUrlsForNativeStyles
Returns a list of URLs that reference the specified site URL with the specified creative from
the association served to it. For Creative Set previewing you may specify the master creative
Id. Each URL corresponds to one available native style for previewing the specified creative.

### performLineItemCreativeAssociationAction
Performs actions on [LineItemCreativeAssociation](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.Statement#query).

### updateLineItemCreativeAssociations
Updates the specified [LineItemCreativeAssociation](/ad-manager/api/reference/v202608/LineItemCreativeAssociationService.LineItemCreativeAssociation) objects
