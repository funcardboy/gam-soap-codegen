# LineItemCreativeAssociationService Reference

**Service**: LineItemCreativeAssociationService

**Types**: 80

## Methods

### createLineItemCreativeAssociations
- **Request**: `LineItemCreativeAssociation[] lineItemCreativeAssociations`
- **Response**: `LineItemCreativeAssociation[]`

### getLineItemCreativeAssociationsByStatement
- **Request**: `Statement filterStatement`
- **Response**: `LineItemCreativeAssociation...`

### getPreviewUrl
- **Request**: `xsd:long lineItemId`
- **Request**: `xsd:long creativeId`
- **Request**: `xsd:string siteUrl`
- **Response**: `xsd:string`

### getPreviewUrlsForNativeStyles
- **Request**: `xsd:long lineItemId`
- **Request**: `xsd:long creativeId`
- **Request**: `xsd:string siteUrl`
- **Response**: `CreativeNativeStylePreview[]`

### performLineItemCreativeAssociationAction
- **Request**: `LineItemCreativeAssociation... lineItemCreativeAssociationAction`
- **Request**: `Statement filterStatement`
- **Response**: `UpdateResult`

### updateLineItemCreativeAssociations
- **Request**: `LineItemCreativeAssociation[] lineItemCreativeAssociations`
- **Response**: `LineItemCreativeAssociation[]`

## Types

### ActivateLineItemCreativeAssociations

| Field | Type | Description |
|-------|------|-------------|
| **`LineItemCreativeAssociationAction` (inherited)** | | |
| **`ActivateLineItemCreativeAssociations`** | | |

### BooleanValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`BooleanValue`** | | |
| `value` | `boolean` | The boolean value. |

### CreativeNativeStylePreview

| Field | Type | Description |
|-------|------|-------------|
| `nativeStyleId` | `long` | The id of the NativeStyle. |
| `previewUrl` | `string` | The URL for previewing this creative using this particular NativeStyle |

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

### DeactivateLineItemCreativeAssociations

| Field | Type | Description |
|-------|------|-------------|
| **`LineItemCreativeAssociationAction` (inherited)** | | |
| **`DeactivateLineItemCreativeAssociations`** | | |

### DeleteLineItemCreativeAssociations

| Field | Type | Description |
|-------|------|-------------|
| **`LineItemCreativeAssociationAction` (inherited)** | | |
| **`DeleteLineItemCreativeAssociations`** | | |

### FieldPathElement

| Field | Type | Description |
|-------|------|-------------|
| `field` | `string` | The name of a field in lower camelcase. (e.g. "biddingStrategy") |
| `index` | `int` | For list fields, this is a 0-indexed position in the list. Null for non-list fields. |

### LineItemCreativeAssociation

| Field | Type | Description |
|-------|------|-------------|
| `lineItemId` | `long` | The ID of the LineItem to which the Creative should be associated. This attribute is required. |
| `creativeId` | `long` | The ID of the Creative being associated with a LineItem. This attribute is required if this is an association between a line item and a creative.  This attribute is ignored if this is an associatio... |
| `creativeSetId` | `long` | The ID of the CreativeSet being associated with a LineItem. This attribute is required if this is an association between a line item and a creative set. This field will be `null` when retrieving as... |
| `manualCreativeRotationWeight` | `double` | The weight of the Creative. This value is only used if the line item's `creativeRotationType` is set to CreativeRotationType.MANUAL. This attribute is optional and defaults to 10. |
| `sequentialCreativeRotationIndex` | `int` | The sequential rotation index of the Creative. This value is used only if the associated line item's LineItem.creativeRotationType is set to CreativeRotationType.SEQUENTIAL. This attribute is optio... |
| `startDateTime` | `DateTime` | Overrides the value set for LineItem.startDateTime. This value is optional and is only valid for Ad Manager 360 networks. If unset, the LineItem.startDateTime will be used. |
| `endDateTime` | `DateTime` | Overrides LineItem.endDateTime. This value is optional and is only valid for Ad Manager 360 networks. If unset, the LineItem.endDateTime will be used. |
| `destinationUrl` | `string` | Overrides the value set for HasDestinationUrlCreative.destinationUrl. This value is optional and is only valid for Ad Manager 360 networks. |
| `sizes` | `Size[]` | Overrides the value set for Creative.size, which allows the creative to be served to ad units that would otherwise not be compatible for its actual size. This value is optional. |
| `stats` | `LineItemCreativeAssociation...` | Contains trafficking statistics for the association. This attribute is readonly and is populated by Google. This will be `null` in case there are no statistics for the association yet. |
| `lastModifiedDateTime` | `DateTime` | The date and time this association was last modified. |
| `targetingName` | `string` | Specifies CreativeTargeting for this line item creative association. This attribute is optional. It should match the creative targeting specified on the corresponding CreativePlaceholder in the Lin... |

### LineItemCreativeAssociationPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `LineItemCreativeAssociation[]` | The collection of line item creative associations contained within this page. |

### LineItemCreativeAssociationStats

| Field | Type | Description |
|-------|------|-------------|
| `stats` | `Stats` | A Stats object that holds delivered impressions and clicks statistics. |
| `creativeSetStats` | `Long_StatsMapEntry[]` | A map containing Stats objects for each creative belonging to a creative set, `null` for non creative set associations. |

### Long_StatsMapEntry

| Field | Type | Description |
|-------|------|-------------|
| `key` | `long` |  |
| `value` | `Stats` |  |

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

### SetValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`SetValue`** | | |
| `values` | `Value[]` | The values. They must all be the same type of `Value` and not contain duplicates. |

### Size

| Field | Type | Description |
|-------|------|-------------|
| `width` | `int` | The width of the AdUnit, LineItem or Creative. |
| `height` | `int` | The height of the AdUnit, LineItem or Creative. |
| `isAspectRatio` | `boolean` | Whether this size represents an aspect ratio. |

### Statement

| Field | Type | Description |
|-------|------|-------------|
| `query` | `string` | Holds the query in PQL syntax. The syntax is:  `[WHERE <condition> {[AND |
| `values` | `String_ValueMapEntry[]` | Holds keys and values for bind variables and their values. The key is the name of the bind variable. The value is the literal value of the variable. In the example `"WHERE status = :bindStatus ORDE... |

### Stats

| Field | Type | Description |
|-------|------|-------------|
| `impressionsDelivered` | `long` | The number of impressions delivered. |
| `clicksDelivered` | `long` | The number of clicks delivered. |
| `videoCompletionsDelivered` | `long` | The number of video completions delivered. |
| `videoStartsDelivered` | `long` | The number of video starts delivered. |
| `viewableImpressionsDelivered` | `long` | The number of viewable impressions delivered. |

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

### UpdateResult

| Field | Type | Description |
|-------|------|-------------|
| `numChanges` | `int` | The number of objects that were changed as a result of performing the action. |
