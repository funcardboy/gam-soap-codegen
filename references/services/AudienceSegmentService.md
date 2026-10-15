# AudienceSegmentService Reference

**Service**: AudienceSegmentService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/AudienceSegmentService
**Types**: 6

## Methods
- `createAudienceSegments(FirstPartyAudienceSegment[] segments) -> FirstPartyAudienceSegment[]`
- `getAudienceSegmentsByStatement(Statement filterStatement) -> AudienceSegmentPage` (PQL filterable: `id`, `name`, `status`, `type`, `size`, `dataProviderName`, `segmentType`)
- `performAudienceSegmentAction(AudienceSegmentAction action, Statement filterStatement) -> UpdateResult`
- `updateAudienceSegments(FirstPartyAudienceSegment[] segments) -> FirstPartyAudienceSegment[]`

## Types
### AudienceSegment (Subclasses: `RuleBasedFirstPartyAudienceSegment`, `NonRuleBasedFirstPartyAudienceSegment`, `ThirdPartyAudienceSegment`, `SharedAudienceSegment`)
- Fields: `id` (`long`), `name` (`string`), `categoryIds` (`long[]`), `description` (`string`), `status` (`AudienceSegmentStatus`: `ACTIVE`, `INACTIVE`, `UNUSED`), `size` (`long`), `mobileWebSize` (`long`), `idfaSize` (`long`), `adIdSize` (`long`), `ppidSize` (`long`), `dataProvider` (`AudienceSegmentDataProvider`), `type` (`AudienceSegmentType`: `FIRST_PARTY`, `SHARED`, `THIRD_PARTY`).
