# ForecastService Reference

**Service**: ForecastService

**Types**: 181

## Methods

### getAvailabilityForecast
- **Request**: `ProspectiveLineItem lineItem`
- **Request**: `AvailabilityForecastOptions forecastOptions`
- **Response**: `AvailabilityForecast`

### getAvailabilityForecastById
- **Request**: `xsd:long lineItemId`
- **Request**: `AvailabilityForecastOptions forecastOptions`
- **Response**: `AvailabilityForecast`

### getDeliveryForecast
- **Request**: `ProspectiveLineItem[] lineItems`
- **Request**: `DeliveryForecastOptions forecastOptions`
- **Response**: `DeliveryForecast`

### getDeliveryForecastByIds
- **Request**: `xsd:long[] lineItemIds`
- **Request**: `DeliveryForecastOptions forecastOptions`
- **Response**: `DeliveryForecast`

### getTrafficData
- **Request**: `TrafficDataRequest trafficDataRequest`
- **Response**: `TrafficDataResponse`

## Types

### AdProductBookingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AdProductBookingError`** | | |

### AdUnitCodeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AdUnitCodeError`** | | |

### AdUnitTargeting

| Field | Type | Description |
|-------|------|-------------|
| `adUnitId` | `string` | Included or excluded ad unit id. |
| `includeDescendants` | `boolean` | Whether or not all descendants are included (or excluded) as part of including (or excluding) this ad unit. By default, the value is `true` which means targeting this ad unit will target all of its... |

### AlternativeUnitTypeForecast

| Field | Type | Description |
|-------|------|-------------|
| `matchedUnits` | `long` | The number of units, defined by unitType, that match the specified targeting and delivery settings. |
| `availableUnits` | `long` | The number of units, defined by unitType, that can be booked without affecting the delivery of any reserved line items. Exceeding this value will not cause an overbook, but lower-priority line item... |
| `possibleUnits` | `long` | The maximum number of units, defined by unitType, that could be booked by taking inventory away from lower-priority line items. |

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

### AppliedLabel

| Field | Type | Description |
|-------|------|-------------|
| `labelId` | `long` | The ID of a created Label. |
| `isNegated` | `boolean` | `isNegated` should be set to `true` to negate the effects of `labelId`. |

### AssetError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AssetError`** | | |

### AudienceSegmentCriteria

| Field | Type | Description |
|-------|------|-------------|
| **`CustomCriteriaNode` (inherited)** | | |
| **`CustomCriteriaLeaf` (inherited)** | | |
| **`AudienceSegmentCriteria`** | | |
| `audienceSegmentIds` | `long[]` | The ids of AudienceSegment objects used to target audience segments. This attribute is required. |

### AudienceSegmentError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AudienceSegmentError`** | | |

### AuthenticationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AuthenticationError`** | | |

### AvailabilityForecast

| Field | Type | Description |
|-------|------|-------------|
| `lineItemId` | `long` | Uniquely identifies this availability forecast. This value is read-only and is assigned by Google when the forecast is created. The attribute will be either the ID of the LineItem object it represe... |
| `orderId` | `long` | The unique ID for the Order object that this line item belongs to, or `null` if the forecast represents a prospective line item without an LineItem.orderId set. |
| `availableUnits` | `long` | The number of units, defined by Goal.unitType, that can be booked without affecting the delivery of any reserved line items. Exceeding this value will not cause an overbook, but lower priority line... |
| `deliveredUnits` | `long` | The number of units, defined by Goal.unitType, that have already been served if the reservation is already running. |
| `matchedUnits` | `long` | The number of units, defined by Goal.unitType, that match the specified targeting and delivery settings. |
| `possibleUnits` | `long` | The maximum number of units, defined by Goal.unitType, that could be booked by taking inventory away from lower priority line items and some same priority line items. Please note: booking this numb... |
| `reservedUnits` | `long` | The number of reserved units, defined by Goal.unitType, requested. This can be an absolute or percentage value. |
| `breakdowns` | `ForecastBreakdown[]` | The breakdowns for each time window defined in ForecastBreakdownOptions.timeWindows. If no breakdown was requested through AvailabilityForecastOptions.breakdown, this field will be empty. If target... |
| `targetingCriteriaBreakdowns` | `TargetingCriteriaBreakdown[]` | The forecast result broken down by the targeting of the forecasted line item. |
| `contendingLineItems` | `ContendingLineItem[]` | List of contending line items for this forecast. |
| `alternativeUnitTypeForecasts` | `AlternativeUnitTypeForecast[]` | Views of this forecast, with alternative unit types. |

### AvailabilityForecastOptions

| Field | Type | Description |
|-------|------|-------------|
| `includeTargetingCriteriaBreakdown` | `boolean` | When specified, forecast result for the availability line item will also include breakdowns by its targeting in AvailabilityForecast.targetingCriteriaBreakdowns. |
| `includeContendingLineItems` | `boolean` | When specified, the forecast result for the availability line item will also include contending line items in AvailabilityForecast.contendingLineItems. |
| `breakdown` | `ForecastBreakdownOptions` |  |

### BandwidthGroup

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`BandwidthGroup`** | | |

### BandwidthGroupTargeting

| Field | Type | Description |
|-------|------|-------------|
| `isTargeted` | `boolean` | Indicates whether bandwidth groups should be targeted or excluded. This attribute is optional and defaults to `true`. |
| `bandwidthGroups` | `Technology[]` | The bandwidth groups that are being targeted or excluded by the LineItem. |

### BooleanValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`BooleanValue`** | | |
| `value` | `boolean` | The boolean value. |

### BreakdownForecast

| Field | Type | Description |
|-------|------|-------------|
| `matched` | `long` |  |
| `available` | `long` |  |
| `possible` | `long` |  |

### Browser

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`Browser`** | | |
| `majorVersion` | `string` | Browser major version. |
| `minorVersion` | `string` | Browser minor version. |

### BrowserLanguage

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`BrowserLanguage`** | | |

### BrowserLanguageTargeting

| Field | Type | Description |
|-------|------|-------------|
| `isTargeted` | `boolean` | Indicates whether browsers languages should be targeted or excluded. This attribute is optional and defaults to `true`. |
| `browserLanguages` | `Technology[]` | Browser languages that are being targeted or excluded by the LineItem. |

### BrowserTargeting

| Field | Type | Description |
|-------|------|-------------|
| `isTargeted` | `boolean` | Indicates whether browsers should be targeted or excluded. This attribute is optional and defaults to `true`. |
| `browsers` | `Technology[]` | Browsers that are being targeted or excluded by the LineItem. |

### BuyerUserListTargeting

| Field | Type | Description |
|-------|------|-------------|
| `hasBuyerUserListTargeting` | `boolean` | Whether the programmatic `LineItem` or `ProposalLineItem` object has buyer user list targeting. |

### ClickTrackingLineItemError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ClickTrackingLineItemError`** | | |

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

### CompanyCreditStatusError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CompanyCreditStatusError`** | | |

### ContendingLineItem

| Field | Type | Description |
|-------|------|-------------|
| `lineItemId` | `long` | The Id of the contending line item. |
| `contendingImpressions` | `long` | Number of impressions contended for by both the forecasted line item and this line item, but served to this line item in the forecast simulation. |

### ContentLabelTargeting

| Field | Type | Description |
|-------|------|-------------|
| `excludedContentLabelIds` | `long[]` |  |

### ContentTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedContentIds` | `long[]` | The IDs of content being targeted by the `LineItem`. |
| `excludedContentIds` | `long[]` | The IDs of content being excluded by the `LineItem`. |
| `targetedVideoContentBundleIds` | `long[]` | A list of video content bundles, represented by ContentBundle IDs, that are being targeted by the `LineItem`. |
| `excludedVideoContentBundleIds` | `long[]` | A list of video content bundles, represented by ContentBundle IDs, that are being excluded by the `LineItem`. |

### CreativeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CreativeError`** | | |

### CreativePlaceholder

| Field | Type | Description |
|-------|------|-------------|
| `size` | `Size` | The dimensions that the creative is expected to have. This attribute is required. |
| `creativeTemplateId` | `long` | The native creative template ID. This value is only required if creativeSizeType is CreativeSizeType.NATIVE. |
| `companions` | `CreativePlaceholder[]` | The companions that the creative is expected to have. This attribute can only be set if the line item it belongs to has a LineItem.environmentType of EnvironmentType.VIDEO\_PLAYER or LineItem.roadb... |
| `appliedLabels` | `AppliedLabel[]` | The set of label frequency caps applied directly to this creative placeholder. |
| `effectiveAppliedLabels` | `AppliedLabel[]` | Contains the set of labels applied directly to this creative placeholder as well as those inherited from the creative template from which this creative placeholder was instantiated. This field is r... |
| `expectedCreativeCount` | `int` | Expected number of creatives that will be uploaded corresponding to this creative placeholder. This estimate is used to improve the accuracy of forecasting; for example, if label frequency capping ... |
| `targetingName` | `string` | The name of the CreativeTargeting for creatives this placeholder represents. This attribute is optional. Specifying creative targeting here is for forecasting purposes only and has no effect on ser... |
| `isAmpOnly` | `boolean` | Indicate if the expected creative of this placeholder has an AMP only variant. This attribute is optional. It is for forecasting purposes only and has no effect on serving. |

### CreativeTargeting

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | The name of this creative targeting. This attribute is required. |
| `targeting` | `Targeting` | The Targeting criteria of this creative targeting. This attribute is required. |

### CrossSellError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CrossSellError`** | | |

### CurrencyCodeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CurrencyCodeError`** | | |

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

### CustomFieldValueError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CustomFieldValueError`** | | |

### CustomPacingCurve

| Field | Type | Description |
|-------|------|-------------|
| `customPacingGoals` | `CustomPacingGoal[]` | The list of goals that make up the custom pacing curve. |

### CustomPacingGoal

| Field | Type | Description |
|-------|------|-------------|
| `startDateTime` | `DateTime` | The start date and time of the goal. This field is required unless `useLineItemStartDateTime` is true. |
| `useLineItemStartDateTime` | `boolean` | Whether the LineItem.startDateTime should be used for the start date and time of this goal. This field is not persisted and if it is set to true, the `startDateTime` field will be populated by the ... |
| `amount` | `long` |  |

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

### DateError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`DateError`** | | |

### DateRange

| Field | Type | Description |
|-------|------|-------------|
| `startDate` | `Date` | The start date of this range. This field is optional and if it is not set then there is no lower bound on the date range. If this field is not set then `endDate` must be specified. |
| `endDate` | `Date` | The end date of this range. This field is optional and if it is not set then there is no upper bound on the date range. If this field is not set then `startDate` must be specified. |

### DateTime

| Field | Type | Description |
|-------|------|-------------|
| `date` | `Date` |  |
| `hour` | `int` |  |
| `minute` | `int` |  |
| `second` | `int` |  |
| `timeZoneId` | `string` |  |

### DateTimeRange

| Field | Type | Description |
|-------|------|-------------|
| `startDateTime` | `DateTime` | The start date time of this range. This field is optional and if it is not set then there is no lower bound on the date time range. If this field is not set then `endDateTime` must be specified. |
| `endDateTime` | `DateTime` | The end date time of this range. This field is optional and if it is not set then there is no upper bound on the date time range. If this field is not set then `startDateTime` must be specified. |

### DateTimeRangeTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedDateTimeRanges` | `DateTimeRange[]` |  |

### DateTimeRangeTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`DateTimeRangeTargetingError`** | | |

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

### DayPart

| Field | Type | Description |
|-------|------|-------------|
| `startTime` | `TimeOfDay` | Represents the start time of the targeted period (inclusive). |
| `endTime` | `TimeOfDay` | Represents the end time of the targeted period (exclusive). |

### DayPartTargeting

| Field | Type | Description |
|-------|------|-------------|
| `dayParts` | `DayPart[]` | Specifies days of the week and times at which a `LineItem` will be delivered. If targeting all days and times, this value will be ignored. |

### DayPartTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`DayPartTargetingError`** | | |

### DeliveryData

| Field | Type | Description |
|-------|------|-------------|
| `units` | `long[]` | Clicks or impressions delivered for the last 7 days. |

### DeliveryForecast

| Field | Type | Description |
|-------|------|-------------|
| `lineItemDeliveryForecasts` | `LineItemDeliveryForecast[]` | The delivery forecasts of the forecasted line items. |

### DeliveryForecastOptions

| Field | Type | Description |
|-------|------|-------------|
| `ignoredLineItemIds` | `long[]` | Line item IDs to be ignored while performing the delivery simulation. |

### DeliveryIndicator

| Field | Type | Description |
|-------|------|-------------|
| `expectedDeliveryPercentage` | `double` | How much the `LineItem` was expected to deliver as a percentage of LineItem.primaryGoal. |
| `actualDeliveryPercentage` | `double` | How much the line item actually delivered as a percentage of LineItem.primaryGoal. |

### DeviceCapability

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`DeviceCapability`** | | |

### DeviceCapabilityTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedDeviceCapabilities` | `Technology[]` | Device capabilities that are being targeted by the LineItem. |
| `excludedDeviceCapabilities` | `Technology[]` | Device capabilities that are being excluded by the LineItem. |

### DeviceCategory

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`DeviceCategory`** | | |

### DeviceCategoryTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedDeviceCategories` | `Technology[]` | Device categories that are being targeted by the LineItem. |
| `excludedDeviceCategories` | `Technology[]` | Device categories that are being excluded by the LineItem. |

### DeviceManufacturer

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`DeviceManufacturer`** | | |

### DeviceManufacturerTargeting

| Field | Type | Description |
|-------|------|-------------|
| `isTargeted` | `boolean` | Indicates whether device manufacturers should be targeted or excluded. This attribute is optional and defaults to `true`. |
| `deviceManufacturers` | `Technology[]` | Device manufacturers that are being targeted or excluded by the LineItem. |

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

### ForecastBreakdown

| Field | Type | Description |
|-------|------|-------------|
| `startTime` | `DateTime` | The starting time of the represented breakdown. |
| `endTime` | `DateTime` | The end time of the represented breakdown. |
| `breakdownEntries` | `ForecastBreakdownEntry[]` | The forecast breakdown entries in the same order as in the ForecastBreakdownOptions.targets field. |

### ForecastBreakdownEntry

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | The optional name of this entry, as specified in the corresponding ForecastBreakdownTarget.name field. |
| `forecast` | `BreakdownForecast` | The forecast of this entry. |

### ForecastBreakdownOptions

| Field | Type | Description |
|-------|------|-------------|
| `timeWindows` | `DateTime[]` | The boundaries of time windows to configure time breakdown. By default, the time window of the forecasted LineItem is assumed if none are explicitly specified in this field. But if set, at least tw... |
| `targets` | `ForecastBreakdownTarget[]` | For each time window, these are the breakdown targets. If none specified, the targeting of the forecasted LineItem is assumed. |

### ForecastBreakdownTarget

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | An optional name for this breakdown target, to be populated in the corresponding ForecastBreakdownEntry.name field. |
| `targeting` | `Targeting` | If specified, the targeting for this breakdown. |
| `creative` | `CreativePlaceholder` | If specified, restrict the breakdown to only inventory matching this creative. |

### ForecastError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ForecastError`** | | |

### FrequencyCap

| Field | Type | Description |
|-------|------|-------------|
| `maxImpressions` | `int` | The maximum number of impressions than can be served to a user within a specified time period. |
| `numTimeUnits` | `int` | The number of `FrequencyCap#timeUnit` to represent the total time period. |

### FrequencyCapError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`FrequencyCapError`** | | |

### GenericTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`GenericTargetingError`** | | |

### GeoTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedLocations` | `Location[]` | The geographical locations being targeted by the LineItem. |
| `excludedLocations` | `Location[]` | The geographical locations being excluded by the LineItem. |

### GeoTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`GeoTargetingError`** | | |

### Goal

| Field | Type | Description |
|-------|------|-------------|
| `units` | `long` | If this is a primary goal, it represents the number or percentage of impressions or clicks that will be reserved for the `LineItem`. If the line item is of type LineItemType.SPONSORSHIP, it represe... |

### GrpSettings

| Field | Type | Description |
|-------|------|-------------|
| `minTargetAge` | `long` | Specifies the minimum target age (in years) of the LineItem. This field is only applicable if provider is not null. |
| `maxTargetAge` | `long` | Specifies the maximum target age (in years) of the LineItem. This field is only applicable if provider is not null. |
| `inTargetRatioEstimateMilliPercent` | `long` | Estimate for the in-target ratio given the line item's audience targeting. This field is only applicable if provider is Nielsen, LineItem.primaryGoal is in-target impressions, and LineItem.CostType... |
| `applyTrueCoview` | `boolean` | Specifies whether to apply true coviewing in Nielsen Line Item auto pacing. This field can only be true if NielsenCtvPacingType is not NONE. |

### GrpSettingsError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`GrpSettingsError`** | | |

### ImageError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ImageError`** | | |

### InternalApiError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`InternalApiError`** | | |

### InvalidUrlError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`InvalidUrlError`** | | |

### InventorySizeTargeting

| Field | Type | Description |
|-------|------|-------------|
| `isTargeted` | `boolean` | Whether the inventory sizes should be targeted or excluded. |
| `targetedSizes` | `TargetedSize[]` | A list of `TargetedSizeDto`s. |

### InventoryTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedAdUnits` | `AdUnitTargeting[]` | A list of targeted AdUnitTargeting. |
| `excludedAdUnits` | `AdUnitTargeting[]` | A list of excluded AdUnitTargeting. |
| `targetedPlacementIds` | `long[]` | A list of targeted Placement ids. |

### InventoryTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`InventoryTargetingError`** | | |

### InventoryUnitError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`InventoryUnitError`** | | |

### InventoryUrl

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` |  |

### InventoryUrlTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedUrls` | `InventoryUrl[]` |  |
| `excludedUrls` | `InventoryUrl[]` |  |

### LabelEntityAssociationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`LabelEntityAssociationError`** | | |

### LineItem

| Field | Type | Description |
|-------|------|-------------|
| **`LineItemSummary` (inherited)** | | |
| `orderId` | `long` | The ID of the Order to which the `LineItem` belongs. This attribute is required on create and ignored on update. |
| `id` | `long` | Uniquely identifies the `LineItem`. This attribute is read-only and is assigned by Google when a line item is created. |
| `name` | `string` | The name of the line item. This attribute is required and has a maximum length of 255 characters. |
| `externalId` | `string` | An identifier for the `LineItem` that is meaningful to the publisher. This attribute is optional and has a maximum length of 255 characters. |
| `orderName` | `string` | The name of the Order. This value is read-only. |
| `startDateTime` | `DateTime` | The date and time on which the `LineItem` is enabled to begin serving. This attribute is required and must be in the future. |
| `endDateTime` | `DateTime` | The date and time on which the `LineItem` will stop serving. This attribute is required unless LineItem.unlimitedEndDateTime is set to `true`. If specified, it must be after the LineItem.startDateT... |
| `autoExtensionDays` | `int` | The number of days to allow a line item to deliver past its endDateTime. A maximum of 7 days is allowed. This is feature is only available for Ad Manager 360 accounts. |
| `unlimitedEndDateTime` | `boolean` | Specifies whether or not the `LineItem` has an end time. This attribute is optional and defaults to false. It can be be set to `true` for only line items of type LineItemType.SPONSORSHIP, LineItemT... |
| `customPacingCurve` | `CustomPacingCurve` | The curve that is used to pace the line item's delivery. This field is required if and only if the delivery forecast source is DeliveryForecastSource.CUSTOM\_PACING\_CURVE. |
| `frequencyCaps` | `FrequencyCap[]` | The set of frequency capping units for this `LineItem`. This attribute is optional. |
| `costPerUnit` | `Money` | The amount of money to spend per impression or click. This attribute is required for creating a `LineItem`. |
| `valueCostPerUnit` | `Money` | An amount to help the adserver rank inventory. LineItem.valueCostPerUnit artificially raises the value of inventory over the LineItem.costPerUnit but avoids raising the actual LineItem.costPerUnit.... |
| `discount` | `double` | The number here is either a percentage or an absolute value depending on the `LineItemDiscountType`. If the `LineItemDiscountType` is LineItemDiscountType.PERCENTAGE, then only non-fractional value... |
| `contractedUnitsBought` | `long` | This attribute is only applicable for certain line item types and acts as an "FYI" or note, which does not impact adserving or other backend systems. For LineItemType.SPONSORSHIP line items, this r... |
| `creativePlaceholders` | `CreativePlaceholder[]` | Details about the creatives that are expected to serve through this `LineItem`. This attribute is required and replaces the `creativeSizes` attribute. |
| `activityAssociations` | `LineItemActivityAssociation[]` | This attribute is required and meaningful only if the LineItem.costType is `CostType.CPA`. |
| `allowOverbook` | `boolean` | The flag indicates whether overbooking should be allowed when creating or updating reservations of line item types LineItemType.SPONSORSHIP and LineItemType.STANDARD. When true, operations on this ... |
| `skipInventoryCheck` | `boolean` | The flag indicates whether the inventory check should be skipped when creating or updating a line item. The default value is false. Note: this field will not persist on the line item itself, and th... |
| `skipCrossSellingRuleWarningChecks` | `boolean` | True to skip checks for warnings from rules applied to line items targeting inventory shared by a distributor partner for cross selling when performing an action on this line item. The default is f... |
| `reserveAtCreation` | `boolean` | The flag indicates whether inventory should be reserved when creating a line item of types LineItemType.SPONSORSHIP and LineItemType.STANDARD in an unapproved Order. The default value is false. |
| `stats` | `Stats` | Contains trafficking statistics for the line item. This attribute is readonly and is populated by Google. This will be `null` in case there are no statistics for a line item yet. |
| `deliveryIndicator` | `DeliveryIndicator` | Indicates how well the line item has been performing. This attribute is readonly and is populated by Google. This will be `null` if the delivery indicator information is not available due to one of... |
| `deliveryData` | `DeliveryData` | Delivery data provides the number of clicks or impressions delivered for a LineItem in the last 7 days. This attribute is readonly and is populated by Google. This will be `null` if the delivery da... |
| `budget` | `Money` | The amount of money allocated to the `LineItem`. This attribute is readonly and is populated by Google. The currency code is readonly. |
| `isArchived` | `boolean` | The archival status of the `LineItem`. This attribute is readonly. |
| `webPropertyCode` | `string` | The web property code used for dynamic allocation line items. This web property is only required with line item types LineItemType.AD\_EXCHANGE and LineItemType.ADSENSE. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied directly to this line item. |
| `effectiveAppliedLabels` | `AppliedLabel[]` | Contains the set of labels inherited from the order that contains this line item and the advertiser that owns the order. If a label has been negated, only the negated label is returned. This field ... |
| `disableSameAdvertiserCompetitiveExclusion` | `boolean` | If a line item has a series of competitive exclusions on it, it could be blocked from serving with line items from the same advertiser. Setting this to `true` will allow line items from the same ad... |
| `lastModifiedByApp` | `string` | The application that last modified this line item. This attribute is read only and is assigned by Google. |
| `notes` | `string` | Provides any additional notes that may annotate the `LineItem`. This attribute is optional and has a maximum length of 65,535 characters. |
| `lastModifiedDateTime` | `DateTime` | The date and time this line item was last modified. This attribute is read only. |
| `creationDateTime` | `DateTime` | This attribute may be `null` for line items created before this feature was introduced. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this line item. |
| `isMissingCreatives` | `boolean` | Indicates if a `LineItem` is missing any creatives for the `creativePlaceholders` specified. Creatives can be considered missing for several reasons including:   * Not enough creatives of a certain... |
| `thirdPartyMeasurementSettings` | `ThirdPartyMeasurementSettings` |  |
| `youtubeKidsRestricted` | `boolean` | Designates this line item as intended for YT Kids app. If true, all creatives associated with this line item must be reviewed and approved. See the Ad Manager Help Center  for more information. |
| `videoMaxDuration` | `long` | The max duration of a video creative associated with this `LineItem` in milliseconds. This attribute is only meaningful for video line items. For version v202011 and earlier, this attribute is opti... |
| `primaryGoal` | `Goal` | The primary goal that this `LineItem` is associated with, which is used in its pacing and budgeting. |
| `secondaryGoals` | `Goal[]` | The secondary goals that this `LineItem` is associated with. It is required and meaningful only if the LineItem.costType is `CostType.CPA` or if the LineItem.lineItemType is LineItemType.SPONSORSHI... |
| `grpSettings` | `GrpSettings` | Contains the information for a line item which has a target GRP demographic. |
| `dealInfo` | `LineItemDealInfoDto` | The deal information associated with this line item, if it is programmatic. |
| `viewabilityProviderCompanyIds` | `long[]` | Optional IDs of the Company that provide ad verification for this line item. Company.Type.VIEWABILITY\_PROVIDER. |
| `customVastExtension` | `string` | Custom XML to be rendered in a custom VAST response at serving time. |
| `repeatedCreativeServingEnabled` | `boolean` | Indicates whether repeated creative serving is enabled for this line item. |
| `deliveryAllocationProfileId` | `long` | The `AllocationDeliveryProfile` ID for this line item. |
| **`LineItem`** | | |
| `targeting` | `Targeting` | Contains the targeting criteria for the ad campaign. This attribute is required. |
| `creativeTargetings` | `CreativeTargeting[]` | A list of CreativeTargeting objects that can be used to specify creative level targeting for this line item. Creative level targeting is specified in a creative placeholder's CreativePlaceholder.ta... |

### LineItemActivityAssociation

| Field | Type | Description |
|-------|------|-------------|
| `activityId` | `int` | The ID of the `Activity` to which the LineItem should be associated. This attribute is required. |
| `clickThroughConversionCost` | `Money` | The amount of money to attribute per click through conversion. This attribute is required for creating a `LineItemActivityAssociation`. The currency code is readonly and should match the LineItem. |
| `viewThroughConversionCost` | `Money` | The amount of money to attribute per view through conversion. This attribute is required for creating a `LineItemActivityAssociation`. The currency code is readonly and should match the LineItem. |

### LineItemActivityAssociationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`LineItemActivityAssociationError`** | | |

### LineItemCreativeAssociationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`LineItemCreativeAssociationError`** | | |

### LineItemDealInfoDto

| Field | Type | Description |
|-------|------|-------------|
| `externalDealId` | `long` | The external deal ID shared between seller and buyer. This field is only present if the deal has been finalized. This attribute is read-only and is assigned by Google. |

### LineItemDeliveryForecast

| Field | Type | Description |
|-------|------|-------------|
| `lineItemId` | `long` | Uniquely identifies this line item delivery forecast. This value is read-only and will be either the ID of the LineItem object it represents, or `null` if the forecast represents a prospective line... |
| `orderId` | `long` | The unique ID for the Order object that this line item belongs to, or `null` if the forecast represents a prospective line item without an LineItem.orderId set. |
| `predictedDeliveryUnits` | `long` | The number of units, defined by Goal.unitType, that will be delivered by the line item. Delivery of existing line items that are of same or lower priorities may be impacted. |
| `deliveredUnits` | `long` | The number of units, defined by Goal.unitType, that have already been served if the reservation is already running. |
| `matchedUnits` | `long` | The number of units, defined by Goal.unitType, that match the specified LineItem.targeting and delivery settings. |

### LineItemError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`LineItemError`** | | |

### LineItemFlightDateError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`LineItemFlightDateError`** | | |

### LineItemOperationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`LineItemOperationError`** | | |

### Location

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | Uniquely identifies each `Location`. |
| `type` | `string` | The location type for this geographical entity (ex. "COUNTRY", "CITY", "STATE", "COUNTY", etc.) |
| `canonicalParentId` | `int` | The nearest location parent's ID for this geographical entity. |
| `displayName` | `string` | The localized name of the geographical entity. |

### MobileApplicationTargeting

| Field | Type | Description |
|-------|------|-------------|
| `mobileApplicationIds` | `long[]` | The IDs that are being targeted or excluded. |
| `isTargeted` | `boolean` | Indicates whether mobile apps should be targeted or excluded. This attribute is optional and defaults to `true`. |

### MobileApplicationTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`MobileApplicationTargetingError`** | | |

### MobileCarrier

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`MobileCarrier`** | | |

### MobileCarrierTargeting

| Field | Type | Description |
|-------|------|-------------|
| `isTargeted` | `boolean` | Indicates whether mobile carriers should be targeted or excluded. This attribute is optional and defaults to `true`. |
| `mobileCarriers` | `Technology[]` | Mobile carriers that are being targeted or excluded by the LineItem. |

### MobileDevice

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`MobileDevice`** | | |
| `manufacturerCriterionId` | `long` | Manufacturer Id. |

### MobileDeviceSubmodel

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`MobileDeviceSubmodel`** | | |
| `mobileDeviceCriterionId` | `long` | The mobile device id. |
| `deviceManufacturerCriterionId` | `long` | The device manufacturer id. |

### MobileDeviceSubmodelTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedMobileDeviceSubmodels` | `Technology[]` | Mobile device submodels that are being targeted by the LineItem. |
| `excludedMobileDeviceSubmodels` | `Technology[]` | Mobile device submodels that are being excluded by the LineItem. |

### MobileDeviceTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedMobileDevices` | `Technology[]` | Mobile devices that are being targeted by the LineItem. |
| `excludedMobileDevices` | `Technology[]` | Mobile devices that are being excluded by the LineItem. |

### Money

| Field | Type | Description |
|-------|------|-------------|
| `currencyCode` | `string` | Three letter currency code in string format. |
| `microAmount` | `long` | Money values are always specified in terms of micros which are a millionth of the fundamental currency unit. For US dollars, $1 is 1,000,000 micros. |

### NotNullError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`NotNullError`** | | |

### NullError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`NullError`** | | |

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

### OperatingSystem

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`OperatingSystem`** | | |

### OperatingSystemTargeting

| Field | Type | Description |
|-------|------|-------------|
| `isTargeted` | `boolean` | Indicates whether operating systems should be targeted or excluded. This attribute is optional and defaults to `true`. |
| `operatingSystems` | `Technology[]` | Operating systems that are being targeted or excluded by the LineItem. |

### OperatingSystemVersion

| Field | Type | Description |
|-------|------|-------------|
| **`Technology` (inherited)** | | |
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |
| **`OperatingSystemVersion`** | | |
| `majorVersion` | `int` | The operating system major version. |
| `minorVersion` | `int` | The operating system minor version. |
| `microVersion` | `int` | The operating system micro version. |

### OperatingSystemVersionTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedOperatingSystemVersions` | `Technology[]` | Operating system versions that are being targeted by the LineItem. |
| `excludedOperatingSystemVersions` | `Technology[]` | Operating system versions that are being excluded by the LineItem. |

### OrderActionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`OrderActionError`** | | |

### OrderError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`OrderError`** | | |

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

### PrecisionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`PrecisionError`** | | |

### ProgrammaticError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ProgrammaticError`** | | |

### ProposalLineItem

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the `ProposalLineItem`. This attribute is read-only. |
| `proposalId` | `long` | The unique ID of the Proposal, to which the `ProposalLineItem` belongs. This attribute is required for creation and then is readonly.  This attribute is required. |
| `name` | `string` | The name of the `ProposalLineItem` which should be unique under the same Proposal. This attribute has a maximum length of 255 characters. This attribute can be configured as editable after the prop... |
| `startDateTime` | `DateTime` | The date and time at which the line item associated with the `ProposalLineItem` is enabled to begin serving. This attribute is optional during creation, but required and must be in the future when ... |
| `endDateTime` | `DateTime` | The date and time at which the line item associated with the `ProposalLineItem` stops beening served. This attribute is optional during creation, but required and must be after the startDateTime. T... |
| `internalNotes` | `string` | Provides any additional notes that may annotate the `ProposalLineItem`. This attribute is optional and has a maximum length of 65,535 characters. This attribute can be configured as editable after ... |
| `isArchived` | `boolean` | The archival status of the `ProposalLineItem`. This attribute is read-only. |
| `goal` | `Goal` | The goal(i.e. contracted quantity, quantity or limit) that this `ProposalLineItem` is associated with, which is used in its pacing and budgeting. Goal.units must be greater than 0 when the proposal... |
| `secondaryGoals` | `Goal[]` | The secondary goals that this `ProposalLineItem` is associated with. For a programmatic line item with the properties RateType.CPM and LineItemType.SPONSORSHIP, this field will have one goal which ... |
| `contractedUnitsBought` | `long` | The contracted number of daily minimum impressions used for LineItemType.SPONSORSHIP `ProposalLineItem` deals with a rate type of RateType.CPD. This attribute is required for percentage-based-goal ... |
| `videoMaxDuration` | `long` | The max duration of a video creative associated with this `ProposalLineItem` in milliseconds. This attribute is optional, defaults to the `Product.videoMaxDuration` on the `Product` it was created ... |
| `frequencyCaps` | `FrequencyCap[]` | The set of frequency capping units for this `ProposalLineItem`. This attribute is optional during creation and defaults to the `product's frequency caps` if `Product.allowFrequencyCapsCustomization... |
| `dfpLineItemId` | `long` | The unique ID of corresponding LineItem. This will be `null` if the Proposal has not been pushed to Ad Manager. This attribute is read-only. |
| `lineItemPriority` | `int` | The priority for the corresponding LineItem of the `ProposalLineItem`. This attribute is optional during creation and defaults to the default priority of the lineItemType. For forecasting, this att... |
| `creativePlaceholders` | `CreativePlaceholder[]` | Details about the creatives that are expected to serve through the `ProposalLineItem`. This attribute is optional during creation and defaults to the `product's creative placeholders`.  This attrib... |
| `targeting` | `Targeting` | Contains the targeting criteria for the `ProposalLineItem`.  This attribute is required. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with the `ProposalLineItem`. This attribute is optional. This attribute can be configured as editable after the proposal has been submitted. Please check ... |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied directly to the `ProposalLineItem`. This attribute is optional. |
| `effectiveAppliedLabels` | `AppliedLabel[]` | Contains the set of labels applied directly to the proposal as well as those inherited ones. If a label has been negated, only the negated label is returned. This attribute is read-only. |
| `disableSameAdvertiserCompetitiveExclusion` | `boolean` | If a line item has a series of competitive exclusions on it, it could be blocked from serving with line items from the same advertiser. Setting this to `true` will allow line items from the same ad... |
| `isSold` | `boolean` | Indicates whether this `ProposalLineItem` has been sold. This attribute is read-only. |
| `netRate` | `Money` | The amount of money to spend per impression or click in proposal currency. It supports precision of 4 decimal places in terms of the fundamental currency unit, so the Money.getAmountInMicros must b... |
| `netCost` | `Money` | The cost of the `ProposalLineItem` in proposal currency. It supports precision of 2 decimal places in terms of the fundamental currency unit, so the Money.getAmountInMicros must be multiples of 100... |
| `deliveryIndicator` | `DeliveryIndicator` | Indicates how well the line item generated from this proposal line item has been performing. This will be `null` if the delivery indicator information is not available due to one of the following r... |
| `deliveryData` | `DeliveryData` | Delivery data provides the number of clicks or impressions delivered for the LineItem generated from this proposal line item in the last 7 days. This will be `null` if the delivery data cannot be c... |
| `lastModifiedDateTime` | `DateTime` | The date and time this `ProposalLineItem` was last modified. This attribute is assigned by Google when a `ProposalLineItem` is updated. This attribute is read-only. |
| `lastReservationDateTime` | `DateTime` | The last DateTime when the ProposalLineItem reserved inventory. This attribute is read-only. |
| `additionalTerms` | `string` | Additional terms shown to the buyer in Marketplace. |
| `grpSettings` | `GrpSettings` | Contains the information for a proposal line item which has a target GRP demographic. |
| `estimatedMinimumImpressions` | `long` | The estimated minimum impressions that should be delivered for a proposal line item. |
| `thirdPartyMeasurementSettings` | `ThirdPartyMeasurementSettings` | Contains third party measurement settings for cross-sell Partners |
| `makegoodInfo` | `ProposalLineItemMakegoodInfo` | Makegood info for this proposal line item. Immutable once created. Null if this proposal line item is not a makegood. |
| `hasMakegood` | `boolean` | Whether this proposal line item has an associated makegood. This attribute is read-only. |
| `canCreateMakegood` | `boolean` | Whether a new makegood associated with this line item can be created. This attribute is read-only. |
| `pauseReason` | `string` | The reason for pausing the ProposalLineItem, provided by the `pauseRole`. It is `null` when the ProposalLineItem is not paused. This attribute is read-only. |
| `deliveryAllocationProfileId` | `long` | The `AllocationDeliveryProfile` ID for this proposal line item. |

### ProposalLineItemMakegoodInfo

| Field | Type | Description |
|-------|------|-------------|
| `originalProposalLineItemId` | `long` | The ID of the original proposal line item on which this makegood is based. This attribute is read-only. |
| `reason` | `string` | The publisher-provided reason why this makegood was initiated. This is free form text. The following predefined values can be used to render predefined options in the UI.  UNDERDELIVERY: 'Impressio... |

### ProspectiveLineItem

| Field | Type | Description |
|-------|------|-------------|
| `lineItem` | `LineItem` | The target of the forecast. If LineItem.id is null or no line item exists with that ID, then a forecast is computed for the subject, predicting what would happen if it were added to the network. If... |
| `proposalLineItem` | `ProposalLineItem` | The target of the forecast if this prospective line item is a proposal line item. If ProposalLineItem.id is null or no proposal line item exists with that ID, then a forecast is computed for the su... |
| `advertiserId` | `long` | When set, the line item is assumed to be from this advertiser, and unified blocking rules will apply accordingly. If absent, line items without an existing order won't be subject to unified blockin... |

### PublisherProvidedSignalsTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedTaxonomyCategoryIds` | `long[]` |  |
| `excludedTaxonomyCategoryIds` | `long[]` |  |

### PublisherProvidedSignalsTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`PublisherProvidedSignalsTargetingError`** | | |

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

### RangeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RangeError`** | | |

### RegExError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RegExError`** | | |

### RequestError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RequestError`** | | |

### RequestPlatformTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RequestPlatformTargetingError`** | | |

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

### RequiredNumberError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RequiredNumberError`** | | |

### RequiredSizeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RequiredSizeError`** | | |

### ReservationDetailsError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ReservationDetailsError`** | | |

### ServerError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ServerError`** | | |

### SetTopBoxLineItemError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`SetTopBoxLineItemError`** | | |

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

### StatementError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`StatementError`** | | |

### Stats

| Field | Type | Description |
|-------|------|-------------|
| `impressionsDelivered` | `long` | The number of impressions delivered. |
| `clicksDelivered` | `long` | The number of clicks delivered. |
| `videoCompletionsDelivered` | `long` | The number of video completions delivered. |
| `videoStartsDelivered` | `long` | The number of video starts delivered. |
| `viewableImpressionsDelivered` | `long` | The number of viewable impressions delivered. |

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

### TargetedSize

| Field | Type | Description |
|-------|------|-------------|
| `size` | `Size` |  |

### Targeting

| Field | Type | Description |
|-------|------|-------------|
| `geoTargeting` | `GeoTargeting` | Specifies what geographical locations are targeted by the LineItem. This attribute is optional. |
| `inventoryTargeting` | `InventoryTargeting` | Specifies what inventory is targeted by the LineItem. This attribute is required. The line item must target at least one ad unit or placement. |
| `dayPartTargeting` | `DayPartTargeting` | Specifies the days of the week and times that are targeted by the LineItem. This attribute is optional. |
| `dateTimeRangeTargeting` | `DateTimeRangeTargeting` | Specifies the dates and time ranges that are targeted by the LineItem. This attribute is optional. |
| `technologyTargeting` | `TechnologyTargeting` | Specifies the browsing technologies that are targeted by the LineItem. This attribute is optional. |
| `customTargeting` | `CustomCriteriaSet` | Specifies the collection of custom criteria that is targeted by the LineItem. Once the LineItem is updated or modified with custom targeting, the server may return a normalized, but equivalent repr... |
| `userDomainTargeting` | `UserDomainTargeting` | Specifies the domains or subdomains that are targeted or excluded by the LineItem. Users visiting from an IP address associated with those domains will be targeted or excluded. This attribute is op... |
| `contentTargeting` | `ContentTargeting` | Specifies the video categories and individual videos targeted by the LineItem. |
| `videoPositionTargeting` | `VideoPositionTargeting` | Specifies targeting against video position types. |
| `mobileApplicationTargeting` | `MobileApplicationTargeting` | Specifies targeting against mobile applications. |
| `buyerUserListTargeting` | `BuyerUserListTargeting` | Specifies whether buyer user lists are targeted on a programmatic LineItem or ProposalLineItem. This attribute is readonly and is populated by Google. |
| `inventoryUrlTargeting` | `InventoryUrlTargeting` | Specifies the URLs that are targeted by the entity. This is currently only supported by YieldGroup. |
| `verticalTargeting` | `VerticalTargeting` | Specifies the verticals that are targeted by the entity. The IDs listed here correspond to the IDs in the AD\_CATEGORY table of type VERTICAL. |
| `contentLabelTargeting` | `ContentLabelTargeting` | Specifies the content labels that are excluded by the entity. The IDs listed here correspond to the IDs in the CONTENT\_LABEL table. |
| `requestPlatformTargeting` | `RequestPlatformTargeting` | Specifies the request platforms that are targeted by the LineItem. This attribute is required for video line items and for ProposalLineItem. This value is modifiable for video line items, but read-... |
| `inventorySizeTargeting` | `InventorySizeTargeting` | Specifies the sizes that are targeted by the entity. This is currently only supported on YieldGroup and TrafficDataRequest. |
| `publisherProvidedSignalsTargeting` | `PublisherProvidedSignalsTar...` |  |

### TargetingCriteriaBreakdown

| Field | Type | Description |
|-------|------|-------------|
| `targetingCriteriaId` | `long` | The unique ID of the targeting criteria. |
| `targetingCriteriaName` | `string` | The name of the targeting criteria. |
| `excluded` | `boolean` | When true, the breakdown is negative. |
| `availableUnits` | `long` | The available units for this breakdown. |
| `matchedUnits` | `long` | The matched units for this breakdown. |

### TeamError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`TeamError`** | | |

### Technology

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the `Technology`. This value is required for all forms of `TechnologyTargeting`. |
| `name` | `string` | The name of the technology being targeting. This value is read-only and is assigned by Google. |

### TechnologyTargeting

| Field | Type | Description |
|-------|------|-------------|
| `bandwidthGroupTargeting` | `BandwidthGroupTargeting` | The bandwidth groups being targeted by the LineItem. |
| `browserTargeting` | `BrowserTargeting` | The browsers being targeted by the LineItem. |
| `browserLanguageTargeting` | `BrowserLanguageTargeting` | The languages of browsers being targeted by the LineItem. |
| `deviceCapabilityTargeting` | `DeviceCapabilityTargeting` | The device capabilities being targeted by the LineItem. |
| `deviceCategoryTargeting` | `DeviceCategoryTargeting` | The device categories being targeted by the LineItem. |
| `deviceManufacturerTargeting` | `DeviceManufacturerTargeting` | The device manufacturers being targeted by the LineItem. |
| `mobileCarrierTargeting` | `MobileCarrierTargeting` | The mobile carriers being targeted by the LineItem. |
| `mobileDeviceTargeting` | `MobileDeviceTargeting` | The mobile devices being targeted by the LineItem. |
| `mobileDeviceSubmodelTargeting` | `MobileDeviceSubmodelTargeting` | The mobile device submodels being targeted by the LineItem. |
| `operatingSystemTargeting` | `OperatingSystemTargeting` | The operating systems being targeted by the LineItem. |
| `operatingSystemVersionTargeting` | `OperatingSystemVersionTarge...` | The operating system versions being targeted by the LineItem. |

### TechnologyTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`TechnologyTargetingError`** | | |

### TextValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`TextValue`** | | |
| `value` | `string` | The string value. |

### ThirdPartyMeasurementSettings

| Field | Type | Description |
|-------|------|-------------|
| `viewabilityClientId` | `string` | The third party partner id for YouTube viewability verification. |
| `viewabilityReportingId` | `string` | The reporting id that maps viewability partner data with a campaign (or a group of related campaigns) specific data. |
| `publisherViewabilityClientId` | `string` | The third party partner id for YouTube viewability verification for publisher. |
| `publisherViewabilityReportingId` | `string` | The reporting id that maps viewability partner data with a campaign (or a group of related campaigns) specific data for publisher. |
| `brandLiftClientId` | `string` | The third party partner id for YouTube brand lift verification. |
| `brandLiftReportingId` | `string` | The reporting id that maps brand lift partner data with a campaign (or a group of related campaigns) specific data. |
| `reachClientId` | `string` | The third party partner id for YouTube reach verification for advertiser. |
| `reachReportingId` | `string` | The reporting id that maps reach partner data with a campaign (or a group of related campaigns) specific data for advertiser. |
| `publisherReachClientId` | `string` | The third party partner id for YouTube reach verification for publisher. |
| `publisherReachReportingId` | `string` | The reporting id that maps reach partner data with a campaign (or a group of related campaigns) specific data for publisher. |

### TimeOfDay

| Field | Type | Description |
|-------|------|-------------|
| `hour` | `int` | Hour in 24 hour time (0..24). This field must be between 0 and 24, inclusive. This field is required. |

### TimeSeries

| Field | Type | Description |
|-------|------|-------------|
| `timeSeriesDateRange` | `DateRange` | The date range of the time series. |
| `values` | `long[]` | The daily values constituting the time series. The number of time series values must equal the number of days spanned by the time series date range, inclusive. E.g.: `timeSeriesDateRange` of 2001-0... |

### TimeZoneError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`TimeZoneError`** | | |

### TrafficDataRequest

| Field | Type | Description |
|-------|------|-------------|
| `targeting` | `Targeting` | The `TargetingDto` that defines a segment of traffic.  This attribute is required. |
| `requestedDateRange` | `DateRange` | The date range for which traffic data are requested. This range may cover historical dates, future dates, or both. The data returned are not guaranteed to cover the entire requested date range. If ... |

### TrafficDataResponse

| Field | Type | Description |
|-------|------|-------------|
| `historicalTimeSeries` | `TimeSeries` | Time series of historical traffic ad opportunity counts. This may be null if the requested date range did not contain any historical dates, or if no historical data are available for the requested ... |
| `forecastedTimeSeries` | `TimeSeries` | Time series of forecasted traffic ad opportunity counts. This may be null if the requested date range did not contain any future dates, or if no forecasted data are available for the requested traf... |
| `forecastedAssignedTimeSeries` | `TimeSeries` | Time series of future traffic volumes forecasted to be sold. This may be null if the requested date range did not contain any future dates, or if no sell-through data are available for the requeste... |
| `overallDateRange` | `DateRange` | The overall date range spanned by the union of all time series in the response. This is a summary field for convenience. The value will be set such that the start date is equal to the earliest star... |

### TranscodingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`TranscodingError`** | | |

### TypeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`TypeError`** | | |

### UniqueError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`UniqueError`** | | |

### UserDomainTargeting

| Field | Type | Description |
|-------|------|-------------|
| `domains` | `string[]` | The domains or subdomains that are being targeted or excluded by the LineItem. This attribute is required and the maximum length of each domain is 67 characters. |
| `targeted` | `boolean` | Indicates whether domains should be targeted or excluded. This attribute is optional and defaults to `true`. |

### UserDomainTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`UserDomainTargetingError`** | | |

### VerticalTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedVerticalIds` | `long[]` |  |
| `excludedVerticalIds` | `long[]` |  |

### VideoPosition

| Field | Type | Description |
|-------|------|-------------|
| `midrollIndex` | `int` | The index of the mid-roll to target. Only valid if the `positionType` is `VideoPositionType.MIDROLL`, otherwise this field will be ignored. |

### VideoPositionTarget

| Field | Type | Description |
|-------|------|-------------|
| `videoPosition` | `VideoPosition` | The video position to target. This attribute is required. |
| `videoPositionWithinPod` | `VideoPositionWithinPod` | The video position within a pod to target. To target a video position or a bumper position, this value must be null. To target a position within a pod this value must be populated. To target a cust... |
| `adSpotId` | `long` | A custom spot AdSpot to target. To target a video position, a bumper type or a video position within a pod this value must be null. |

### VideoPositionTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedPositions` | `VideoPositionTarget[]` | The `VideoTargetingPosition` objects being targeted by the video LineItem. |

### VideoPositionTargetingError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`VideoPositionTargetingError`** | | |

### VideoPositionWithinPod

| Field | Type | Description |
|-------|------|-------------|
| `index` | `int` | The specific index of the pod. The index is defined as:  * 1 = first * 2 = second * 3 = third * .... * 100 = last  100 will always be the last position. For example, for a pod with 5 positions, 100... |

