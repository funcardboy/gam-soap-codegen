# AudienceSegmentService Reference

**Service**: AudienceSegmentService

**Types**: 65

## Methods

### createAudienceSegments
- **Request**: `FirstPartyAudienceSegment[] segments`
- **Response**: `FirstPartyAudienceSegment[]`

### getAudienceSegmentsByStatement
- **Request**: `Statement filterStatement`
- **Response**: `AudienceSegmentPage`

### performAudienceSegmentAction
- **Request**: `AudienceSegmentAction action`
- **Request**: `Statement filterStatement`
- **Response**: `UpdateResult`

### updateAudienceSegments
- **Request**: `FirstPartyAudienceSegment[] segments`
- **Response**: `FirstPartyAudienceSegment[]`

## Types

### ActivateAudienceSegments

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegmentAction` (inherited)** | | |
| **`ActivateAudienceSegments`** | | |

### AdUnitTargeting

| Field | Type | Description |
|-------|------|-------------|
| `adUnitId` | `string` | Included or excluded ad unit id. |
| `includeDescendants` | `boolean` | Whether or not all descendants are included (or excluded) as part of including (or excluding) this ad unit. By default, the value is `true` which means targeting this ad unit will target all of its... |

### ApiError

| Field | Type | Description |
|-------|------|-------------|
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |

### ApiException

| Field | Type | Description |
|-------|------|-------------|
| **`ApplicationException` (inherited)** | | |
| `message` | `string` | Error message. |
| **`ApiException`** | | |
| `errors` | `ApiError[]` | List of errors. |

### ApiVersionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ApiVersionError`** | | |

### ApproveAudienceSegments

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegmentAction` (inherited)** | | |
| **`ApproveAudienceSegments`** | | |

### AudienceSegment

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | Id of the AudienceSegment. This attribute is readonly and is populated by Google. |
| `name` | `string` | Name of the AudienceSegment. This attribute is required and has a maximum length of 255 characters. |
| `categoryIds` | `long[]` | The ids of the categories this segment belongs to. This field is optional, it may be empty. |
| `description` | `string` | Description of the AudienceSegment. This attribute is optional and has a maximum length of 8192 characters. |
| `size` | `long` | Number of unique identifiers in the AudienceSegment. This attribute is readonly and is populated by Google. |
| `mobileWebSize` | `long` | Number of unique identifiers in the AudienceSegment for mobile web. This attribute is read-only. |
| `idfaSize` | `long` | Number of unique IDFA identifiers in the AudienceSegment. This attribute is read-only. |
| `adIdSize` | `long` | Number of unique AdID identifiers in the AudienceSegment. This attribute is read-only. |
| `ppidSize` | `long` | Number of unique PPID (publisher provided identifiers) in the AudienceSegment. This attribute is read-only. |
| `dataProvider` | `AudienceSegmentDataProvider` | Owner data provider of this segment. This attribute is readonly and is assigned by Google. |

### AudienceSegmentCriteria

| Field | Type | Description |
|-------|------|-------------|
| **`CustomCriteriaNode` (inherited)** | | |
| **`CustomCriteriaLeaf` (inherited)** | | |
| **`AudienceSegmentCriteria`** | | |
| `audienceSegmentIds` | `long[]` | The ids of AudienceSegment objects used to target audience segments. This attribute is required. |

### AudienceSegmentDataProvider

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | Name of the data provider. This attribute is readonly and is assigned by Google. |

### AudienceSegmentError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AudienceSegmentError`** | | |

### AudienceSegmentPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `AudienceSegment[]` | The collection of audience segments contained within this page. |

### AuthenticationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AuthenticationError`** | | |

### BooleanValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`BooleanValue`** | | |
| `value` | `boolean` | The boolean value. |

### CmsMetadataCriteria

| Field | Type | Description |
|-------|------|-------------|
| **`CustomCriteriaNode` (inherited)** | | |
| **`CustomCriteriaLeaf` (inherited)** | | |
| **`CmsMetadataCriteria`** | | |
| `cmsMetadataValueIds` | `long[]` | The ids of CmsMetadataValue objects used to target CMS metadata. This attribute is required. |

### CollectionSizeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CollectionSizeError`** | | |

### CommonError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CommonError`** | | |

### CustomCriteria

| Field | Type | Description |
|-------|------|-------------|
| **`CustomCriteriaNode` (inherited)** | | |
| **`CustomCriteriaLeaf` (inherited)** | | |
| **`CustomCriteria`** | | |
| `keyId` | `long` | The CustomTargetingKey.id of the CustomTargetingKey object that was created using CustomTargetingService. This attribute is required. |
| `valueIds` | `long[]` | The ids of CustomTargetingValue objects to target the custom targeting key with id CustomCriteria.keyId. This attribute is required. |

### CustomCriteriaLeaf

| Field | Type | Description |
|-------|------|-------------|
| **`CustomCriteriaNode` (inherited)** | | |
| **`CustomCriteriaLeaf`** | | |

### CustomCriteriaSet

| Field | Type | Description |
|-------|------|-------------|
| **`CustomCriteriaNode` (inherited)** | | |
| **`CustomCriteriaSet`** | | |
| `children` | `CustomCriteriaNode[]` | The custom criteria. This attribute is required. |

### CustomTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CustomTargetingError`** | | |

### Date

| Field | Type | Description |
|-------|------|-------------|
| `year` | `int` | Year (e.g., 2009) |
| `month` | `int` | Month (1..12) |
| `day` | `int` | Day (1..31) |

### DateTime

| Field | Type | Description |
|-------|------|-------------|
| `date` | `Date` |  |
| `hour` | `int` |  |
| `minute` | `int` |  |
| `second` | `int` |  |
| `timeZoneId` | `string` |  |

### DateTimeValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`DateTimeValue`** | | |
| `value` | `DateTime` | The `DateTime` value. |

### DateValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`DateValue`** | | |
| `value` | `Date` | The `Date` value. |

### DeactivateAudienceSegments

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegmentAction` (inherited)** | | |
| **`DeactivateAudienceSegments`** | | |

### EntityChildrenLimitReachedError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`EntityChildrenLimitReachedError`** | | |

### EntityLimitReachedError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`EntityLimitReachedError`** | | |

### FeatureError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`FeatureError`** | | |

### FieldPathElement

| Field | Type | Description |
|-------|------|-------------|
| `field` | `string` | The name of a field in lower camelcase. (e.g. "biddingStrategy") |
| `index` | `int` | For list fields, this is a 0-indexed position in the list. Null for non-list fields. |

### FirstPartyAudienceSegment

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegment` (inherited)** | | |
| `id` | `long` | Id of the AudienceSegment. This attribute is readonly and is populated by Google. |
| `name` | `string` | Name of the AudienceSegment. This attribute is required and has a maximum length of 255 characters. |
| `categoryIds` | `long[]` | The ids of the categories this segment belongs to. This field is optional, it may be empty. |
| `description` | `string` | Description of the AudienceSegment. This attribute is optional and has a maximum length of 8192 characters. |
| `size` | `long` | Number of unique identifiers in the AudienceSegment. This attribute is readonly and is populated by Google. |
| `mobileWebSize` | `long` | Number of unique identifiers in the AudienceSegment for mobile web. This attribute is read-only. |
| `idfaSize` | `long` | Number of unique IDFA identifiers in the AudienceSegment. This attribute is read-only. |
| `adIdSize` | `long` | Number of unique AdID identifiers in the AudienceSegment. This attribute is read-only. |
| `ppidSize` | `long` | Number of unique PPID (publisher provided identifiers) in the AudienceSegment. This attribute is read-only. |
| `dataProvider` | `AudienceSegmentDataProvider` | Owner data provider of this segment. This attribute is readonly and is assigned by Google. |
| **`FirstPartyAudienceSegment`** | | |

### FirstPartyAudienceSegmentRule

| Field | Type | Description |
|-------|------|-------------|
| `inventoryRule` | `InventoryTargeting` | Specifies the inventory (i.e. ad units and placements) that are part of the rule of a FirstPartyAudienceSegment. This attribute is required. |
| `customCriteriaRule` | `CustomCriteriaSet` | Specifies the collection of custom criteria that are part of the rule of a FirstPartyAudienceSegment. Once the FirstPartyAudienceSegment is updated or modified with custom criteria, the server may ... |

### InternalApiError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`InternalApiError`** | | |

### InventoryTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedAdUnits` | `AdUnitTargeting[]` | A list of targeted AdUnitTargeting. |
| `excludedAdUnits` | `AdUnitTargeting[]` | A list of excluded AdUnitTargeting. |
| `targetedPlacementIds` | `long[]` | A list of targeted Placement ids. |

### Money

| Field | Type | Description |
|-------|------|-------------|
| `currencyCode` | `string` | Three letter currency code in string format. |
| `microAmount` | `long` | Money values are always specified in terms of micros which are a millionth of the fundamental currency unit. For US dollars, $1 is 1,000,000 micros. |

### NonRuleBasedFirstPartyAudienceSegment

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegment` (inherited)** | | |
| `id` | `long` | Id of the AudienceSegment. This attribute is readonly and is populated by Google. |
| `name` | `string` | Name of the AudienceSegment. This attribute is required and has a maximum length of 255 characters. |
| `categoryIds` | `long[]` | The ids of the categories this segment belongs to. This field is optional, it may be empty. |
| `description` | `string` | Description of the AudienceSegment. This attribute is optional and has a maximum length of 8192 characters. |
| `size` | `long` | Number of unique identifiers in the AudienceSegment. This attribute is readonly and is populated by Google. |
| `mobileWebSize` | `long` | Number of unique identifiers in the AudienceSegment for mobile web. This attribute is read-only. |
| `idfaSize` | `long` | Number of unique IDFA identifiers in the AudienceSegment. This attribute is read-only. |
| `adIdSize` | `long` | Number of unique AdID identifiers in the AudienceSegment. This attribute is read-only. |
| `ppidSize` | `long` | Number of unique PPID (publisher provided identifiers) in the AudienceSegment. This attribute is read-only. |
| `dataProvider` | `AudienceSegmentDataProvider` | Owner data provider of this segment. This attribute is readonly and is assigned by Google. |
| **`FirstPartyAudienceSegment` (inherited)** | | |
| **`NonRuleBasedFirstPartyAudienceSegment`** | | |
| `membershipExpirationDays` | `int` | Specifies the number of days after which a user's cookie will be removed from the audience segment due to inactivity. This attribute is required and can be between 1 and 540. |

### NotNullError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`NotNullError`** | | |

### NumberValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`NumberValue`** | | |
| `value` | `string` | The numeric value represented as a string. |

### ObjectValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`ObjectValue`** | | |

### ParseError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ParseError`** | | |

### PermissionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`PermissionError`** | | |

### PopulateAudienceSegments

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegmentAction` (inherited)** | | |
| **`PopulateAudienceSegments`** | | |

### PublisherQueryLanguageContextError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`PublisherQueryLanguageContextError`** | | |

### PublisherQueryLanguageSyntaxError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`PublisherQueryLanguageSyntaxError`** | | |

### QuotaError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`QuotaError`** | | |

### RejectAudienceSegments

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegmentAction` (inherited)** | | |
| **`RejectAudienceSegments`** | | |

### RequestError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RequestError`** | | |

### RequiredCollectionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RequiredCollectionError`** | | |

### RequiredError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RequiredError`** | | |

### RuleBasedFirstPartyAudienceSegment

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegment` (inherited)** | | |
| `id` | `long` | Id of the AudienceSegment. This attribute is readonly and is populated by Google. |
| `name` | `string` | Name of the AudienceSegment. This attribute is required and has a maximum length of 255 characters. |
| `categoryIds` | `long[]` | The ids of the categories this segment belongs to. This field is optional, it may be empty. |
| `description` | `string` | Description of the AudienceSegment. This attribute is optional and has a maximum length of 8192 characters. |
| `size` | `long` | Number of unique identifiers in the AudienceSegment. This attribute is readonly and is populated by Google. |
| `mobileWebSize` | `long` | Number of unique identifiers in the AudienceSegment for mobile web. This attribute is read-only. |
| `idfaSize` | `long` | Number of unique IDFA identifiers in the AudienceSegment. This attribute is read-only. |
| `adIdSize` | `long` | Number of unique AdID identifiers in the AudienceSegment. This attribute is read-only. |
| `ppidSize` | `long` | Number of unique PPID (publisher provided identifiers) in the AudienceSegment. This attribute is read-only. |
| `dataProvider` | `AudienceSegmentDataProvider` | Owner data provider of this segment. This attribute is readonly and is assigned by Google. |
| **`FirstPartyAudienceSegment` (inherited)** | | |
| **`RuleBasedFirstPartyAudienceSegmentSummary` (inherited)** | | |
| `pageViews` | `int` | Specifies the number of times a user's cookie must match the segment rule before it's associated with the audience segment. This is used in combination with FirstPartyAudienceSegment.recencyDays to... |
| `recencyDays` | `int` | Specifies the number of days within which a user's cookie must match the segment rule before it's associated with the audience segment. This is used in combination with FirstPartyAudienceSegment.pa... |
| `membershipExpirationDays` | `int` | Specifies the number of days after which a user's cookie will be removed from the audience segment due to inactivity. This attribute is required and can be between 1 and 540. |
| **`RuleBasedFirstPartyAudienceSegment`** | | |
| `rule` | `FirstPartyAudienceSegmentRule` | Specifies the rule of the segment which determines user's eligibility criteria to be part of the segment. This attribute is required. |

### RuleBasedFirstPartyAudienceSegmentSummary

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegment` (inherited)** | | |
| `id` | `long` | Id of the AudienceSegment. This attribute is readonly and is populated by Google. |
| `name` | `string` | Name of the AudienceSegment. This attribute is required and has a maximum length of 255 characters. |
| `categoryIds` | `long[]` | The ids of the categories this segment belongs to. This field is optional, it may be empty. |
| `description` | `string` | Description of the AudienceSegment. This attribute is optional and has a maximum length of 8192 characters. |
| `size` | `long` | Number of unique identifiers in the AudienceSegment. This attribute is readonly and is populated by Google. |
| `mobileWebSize` | `long` | Number of unique identifiers in the AudienceSegment for mobile web. This attribute is read-only. |
| `idfaSize` | `long` | Number of unique IDFA identifiers in the AudienceSegment. This attribute is read-only. |
| `adIdSize` | `long` | Number of unique AdID identifiers in the AudienceSegment. This attribute is read-only. |
| `ppidSize` | `long` | Number of unique PPID (publisher provided identifiers) in the AudienceSegment. This attribute is read-only. |
| `dataProvider` | `AudienceSegmentDataProvider` | Owner data provider of this segment. This attribute is readonly and is assigned by Google. |
| **`FirstPartyAudienceSegment` (inherited)** | | |
| **`RuleBasedFirstPartyAudienceSegmentSummary`** | | |
| `pageViews` | `int` | Specifies the number of times a user's cookie must match the segment rule before it's associated with the audience segment. This is used in combination with FirstPartyAudienceSegment.recencyDays to... |
| `recencyDays` | `int` | Specifies the number of days within which a user's cookie must match the segment rule before it's associated with the audience segment. This is used in combination with FirstPartyAudienceSegment.pa... |
| `membershipExpirationDays` | `int` | Specifies the number of days after which a user's cookie will be removed from the audience segment due to inactivity. This attribute is required and can be between 1 and 540. |

### ServerError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ServerError`** | | |

### SetValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`SetValue`** | | |
| `values` | `Value[]` | The values. They must all be the same type of `Value` and not contain duplicates. |

### SharedAudienceSegment

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegment` (inherited)** | | |
| `id` | `long` | Id of the AudienceSegment. This attribute is readonly and is populated by Google. |
| `name` | `string` | Name of the AudienceSegment. This attribute is required and has a maximum length of 255 characters. |
| `categoryIds` | `long[]` | The ids of the categories this segment belongs to. This field is optional, it may be empty. |
| `description` | `string` | Description of the AudienceSegment. This attribute is optional and has a maximum length of 8192 characters. |
| `size` | `long` | Number of unique identifiers in the AudienceSegment. This attribute is readonly and is populated by Google. |
| `mobileWebSize` | `long` | Number of unique identifiers in the AudienceSegment for mobile web. This attribute is read-only. |
| `idfaSize` | `long` | Number of unique IDFA identifiers in the AudienceSegment. This attribute is read-only. |
| `adIdSize` | `long` | Number of unique AdID identifiers in the AudienceSegment. This attribute is read-only. |
| `ppidSize` | `long` | Number of unique PPID (publisher provided identifiers) in the AudienceSegment. This attribute is read-only. |
| `dataProvider` | `AudienceSegmentDataProvider` | Owner data provider of this segment. This attribute is readonly and is assigned by Google. |
| **`SharedAudienceSegment`** | | |

### Statement

| Field | Type | Description |
|-------|------|-------------|
| `query` | `string` | Holds the query in PQL syntax. The syntax is:  `[WHERE <condition> {[AND |
| `values` | `String_ValueMapEntry[]` | Holds keys and values for bind variables and their values. The key is the name of the bind variable. The value is the literal value of the variable. In the example `"WHERE status = :bindStatus ORDE... |

### StatementError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`StatementError`** | | |

### StringFormatError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`StringFormatError`** | | |

### StringLengthError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`StringLengthError`** | | |

### String_ValueMapEntry

| Field | Type | Description |
|-------|------|-------------|
| `key` | `string` |  |
| `value` | `Value` | 7. `TextValue` |

### TextValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`TextValue`** | | |
| `value` | `string` | The string value. |

### ThirdPartyAudienceSegment

| Field | Type | Description |
|-------|------|-------------|
| **`AudienceSegment` (inherited)** | | |
| `id` | `long` | Id of the AudienceSegment. This attribute is readonly and is populated by Google. |
| `name` | `string` | Name of the AudienceSegment. This attribute is required and has a maximum length of 255 characters. |
| `categoryIds` | `long[]` | The ids of the categories this segment belongs to. This field is optional, it may be empty. |
| `description` | `string` | Description of the AudienceSegment. This attribute is optional and has a maximum length of 8192 characters. |
| `size` | `long` | Number of unique identifiers in the AudienceSegment. This attribute is readonly and is populated by Google. |
| `mobileWebSize` | `long` | Number of unique identifiers in the AudienceSegment for mobile web. This attribute is read-only. |
| `idfaSize` | `long` | Number of unique IDFA identifiers in the AudienceSegment. This attribute is read-only. |
| `adIdSize` | `long` | Number of unique AdID identifiers in the AudienceSegment. This attribute is read-only. |
| `ppidSize` | `long` | Number of unique PPID (publisher provided identifiers) in the AudienceSegment. This attribute is read-only. |
| `dataProvider` | `AudienceSegmentDataProvider` | Owner data provider of this segment. This attribute is readonly and is assigned by Google. |
| **`ThirdPartyAudienceSegment`** | | |
| `cost` | `Money` | Specifies CPM cost for the given segment. This attribute is readonly and is assigned by the data provider. The CPM cost comes from the active pricing, if there is one; otherwise it comes from the l... |
| `startDateTime` | `DateTime` | Specifies the date and time at which this segment becomes available for use. This attribute is readonly and is assigned by the data provider. |
| `endDateTime` | `DateTime` | Specifies the date and time at which this segment ceases to be available for use. This attribute is readonly and is assigned by the data provider. |

### TypeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`TypeError`** | | |

### UpdateResult

| Field | Type | Description |
|-------|------|-------------|
| `numChanges` | `int` | The number of objects that were changed as a result of performing the action. |

