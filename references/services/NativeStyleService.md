# NativeStyleService Reference

**Service**: NativeStyleService

**Types**: 109

## Methods

### createNativeStyles
- **Request**: `NativeStyle[] nativeStyles`
- **Response**: `NativeStyle[]`

### getNativeStylesByStatement
- **Request**: `Statement filterStatement`
- **Response**: `NativeStylePage`

### performNativeStyleAction
- **Request**: `NativeStyleAction nativeStyleAction`
- **Request**: `Statement filterStatement`
- **Response**: `UpdateResult`

### updateNativeStyles
- **Request**: `NativeStyle[] nativeStyles`
- **Response**: `NativeStyle[]`

## Types

### ActivateNativeStyles

| Field | Type | Description |
|-------|------|-------------|
| **`NativeStyleAction` (inherited)** | | |
| **`ActivateNativeStyles`** | | |

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

### ArchiveNativeStyles

| Field | Type | Description |
|-------|------|-------------|
| **`NativeStyleAction` (inherited)** | | |
| **`ArchiveNativeStyles`** | | |

### AudienceSegmentCriteria

| Field | Type | Description |
|-------|------|-------------|
| **`CustomCriteriaNode` (inherited)** | | |
| **`CustomCriteriaLeaf` (inherited)** | | |
| **`AudienceSegmentCriteria`** | | |
| `audienceSegmentIds` | `long[]` | The ids of AudienceSegment objects used to target audience segments. This attribute is required. |

### AuthenticationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AuthenticationError`** | | |

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

### CreativeTemplateError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CreativeTemplateError`** | | |

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

### DateTimeRange

| Field | Type | Description |
|-------|------|-------------|
| `startDateTime` | `DateTime` | The start date time of this range. This field is optional and if it is not set then there is no lower bound on the date time range. If this field is not set then `endDateTime` must be specified. |
| `endDateTime` | `DateTime` | The end date time of this range. This field is optional and if it is not set then there is no upper bound on the date time range. If this field is not set then `startDateTime` must be specified. |

### DateTimeRangeTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedDateTimeRanges` | `DateTimeRange[]` |  |

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

### DeactivateNativeStyles

| Field | Type | Description |
|-------|------|-------------|
| **`NativeStyleAction` (inherited)** | | |
| **`DeactivateNativeStyles`** | | |

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

### GeoTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedLocations` | `Location[]` | The geographical locations being targeted by the LineItem. |
| `excludedLocations` | `Location[]` | The geographical locations being excluded by the LineItem. |

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

### InventoryUrl

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` |  |

### InventoryUrlTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedUrls` | `InventoryUrl[]` |  |
| `excludedUrls` | `InventoryUrl[]` |  |

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

### NativeStyle

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | Uniquely identifies the `NativeStyle`. This attribute is read-only and is assigned by Google when a native style is created. |
| `name` | `string` | The name of the native style. This attribute is required and has a maximum length of 255 characters. |
| `htmlSnippet` | `string` | The HTML snippet of the native style with placeholders for the associated variables. This attribute is required. |
| `cssSnippet` | `string` | The CSS snippet of the native style, with placeholders for the associated variables. This attribute is required. |
| `creativeTemplateId` | `long` | The creative template ID this native style associated with. This attribute is required on creation and is read-only afterwards. |
| `isFluid` | `boolean` | Whether this is a fluid size native style. If `true`, this must be used with 1x1 size. |
| `targeting` | `Targeting` | The targeting criteria for this native style. Only ad unit and key-value targeting are supported at this time. |
| `size` | `Size` | The size of the native style. This attribute is required. |

### NativeStyleError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`NativeStyleError`** | | |

### NativeStylePage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `NativeStyle[]` | The collection of native styles contained within this page. |

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

### PublisherProvidedSignalsTargeting

| Field | Type | Description |
|-------|------|-------------|
| `targetedTaxonomyCategoryIds` | `long[]` |  |
| `excludedTaxonomyCategoryIds` | `long[]` |  |

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

### RequiredSizeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RequiredSizeError`** | | |

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

### TextValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`TextValue`** | | |
| `value` | `string` | The string value. |

### TimeOfDay

| Field | Type | Description |
|-------|------|-------------|
| `hour` | `int` | Hour in 24 hour time (0..24). This field must be between 0 and 24, inclusive. This field is required. |

### UniqueError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`UniqueError`** | | |

### UpdateResult

| Field | Type | Description |
|-------|------|-------------|
| `numChanges` | `int` | The number of objects that were changed as a result of performing the action. |

### UserDomainTargeting

| Field | Type | Description |
|-------|------|-------------|
| `domains` | `string[]` | The domains or subdomains that are being targeted or excluded by the LineItem. This attribute is required and the maximum length of each domain is 67 characters. |
| `targeted` | `boolean` | Indicates whether domains should be targeted or excluded. This attribute is optional and defaults to `true`. |

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

### VideoPositionWithinPod

| Field | Type | Description |
|-------|------|-------------|
| `index` | `int` | The specific index of the pod. The index is defined as:  * 1 = first * 2 = second * 3 = third * .... * 100 = last  100 will always be the last position. For example, for a pod with 5 positions, 100... |

