# CreativeService Reference

**Service**: CreativeService

**Types**: 117

## Methods

### createCreatives
- **Request**: `Creative[] creatives`
- **Response**: `Creative[]`

### getCreativesByStatement
- **Request**: `Statement filterStatement`
- **Response**: `CreativePage`

### performCreativeAction
- **Request**: `CreativeAction creativeAction`
- **Request**: `Statement filterStatement`
- **Response**: `UpdateResult`

### updateCreatives
- **Request**: `Creative[] creatives`
- **Response**: `Creative[]`

## Types

### ActivateCreatives

| Field | Type | Description |
|-------|------|-------------|
| **`CreativeAction` (inherited)** | | |
| **`ActivateCreatives`** | | |

### AdExchangeCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`BaseDynamicAllocationCreative` (inherited)** | | |
| **`HasHtmlSnippetDynamicAllocationCreative` (inherited)** | | |
| `codeSnippet` | `string` | The code snippet (ad tag) from Ad Exchange or AdSense to traffic the dynamic allocation creative. Only valid Ad Exchange or AdSense parameters will be considered. Any extraneous HTML or JavaScript ... |
| **`AdExchangeCreative`** | | |
| `isNativeEligible` | `boolean` | Whether this creative is eligible for native ad-serving. This value is optional and defaults to `false`. |
| `isInterstitial` | `boolean` | `true` if this creative is interstitial. An interstitial creative will not consider an impression served until it is fully rendered in the browser. |
| `isAllowsAllRequestedSizes` | `boolean` | `true` if this creative is eligible for all requested sizes. |

### AdSenseCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`BaseDynamicAllocationCreative` (inherited)** | | |
| **`HasHtmlSnippetDynamicAllocationCreative` (inherited)** | | |
| `codeSnippet` | `string` | The code snippet (ad tag) from Ad Exchange or AdSense to traffic the dynamic allocation creative. Only valid Ad Exchange or AdSense parameters will be considered. Any extraneous HTML or JavaScript ... |
| **`AdSenseCreative`** | | |

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

### AspectRatioImageCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`AspectRatioImageCreative`** | | |
| `imageAssets` | `CreativeAsset[]` | The images associated with this creative. The ad server will choose one based on the capabilities of the device. Each asset should have a size which is of the same aspect ratio as the Creative.size... |
| `altText` | `string` | The text that is served along with the image creative, primarily for accessibility. If no suitable image size is available for the device, this text replaces the image completely. This field is opt... |
| `thirdPartyImpressionTrackingUrls` | `string[]` | A list of impression tracking URL to ping when this creative is displayed. This field is optional and each string has a maximum length of 1024 characters. |
| `overrideSize` | `boolean` | Allows the actual image asset sizes to differ from the creative size. This attribute is optional. |

### AssetCreativeTemplateVariableValue

| Field | Type | Description |
|-------|------|-------------|
| **`BaseCreativeTemplateVariableValue` (inherited)** | | |
| `uniqueName` | `string` | A uniqueName of the CreativeTemplateVariable. |
| **`AssetCreativeTemplateVariableValue`** | | |
| `asset` | `CreativeAsset` | The associated asset. This attribute is required when creating a new `TemplateCreative`. To view the asset, use CreativeAsset.assetUrl. |

### AssetError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AssetError`** | | |

### AudioCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseAudioCreative` (inherited)** | | |
| `duration` | `int` | The expected duration of this creative in milliseconds. |
| `allowDurationOverride` | `boolean` | Allows the creative duration to differ from the actual asset durations. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `adId` | `string` | The ad id associated with the video as defined by the `adIdType` registry. This field is required if `adIdType` is not AdIdType.NONE. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |
| **`AudioCreative`** | | |
| `audioSourceUrl` | `string` | A URL that points to the source media that will be used for transcoding. |

### AudioRedirectCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseAudioCreative` (inherited)** | | |
| `duration` | `int` | The expected duration of this creative in milliseconds. |
| `allowDurationOverride` | `boolean` | Allows the creative duration to differ from the actual asset durations. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `adId` | `string` | The ad id associated with the video as defined by the `adIdType` registry. This field is required if `adIdType` is not AdIdType.NONE. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |
| **`AudioRedirectCreative`** | | |
| `audioAssets` | `VideoRedirectAsset[]` | The audio creative assets. |
| `mezzanineFile` | `VideoRedirectAsset` | The high quality mezzanine audio asset. |

### AuthenticationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`AuthenticationError`** | | |

### BaseAudioCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseAudioCreative`** | | |
| `duration` | `int` | The expected duration of this creative in milliseconds. |
| `allowDurationOverride` | `boolean` | Allows the creative duration to differ from the actual asset durations. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `adId` | `string` | The ad id associated with the video as defined by the `adIdType` registry. This field is required if `adIdType` is not AdIdType.NONE. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |

### BaseCreativeTemplateVariableValue

| Field | Type | Description |
|-------|------|-------------|
| `uniqueName` | `string` | A uniqueName of the CreativeTemplateVariable. |

### BaseDynamicAllocationCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`BaseDynamicAllocationCreative`** | | |

### BaseImageCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseImageCreative`** | | |
| `overrideSize` | `boolean` | Allows the creative size to differ from the actual image asset size. This attribute is optional. |
| `primaryImageAsset` | `CreativeAsset` | The primary image asset associated with this creative. This attribute is required. |

### BaseImageRedirectCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseImageRedirectCreative`** | | |
| `imageUrl` | `string` | The URL where the actual asset resides. This attribute is required and has a maximum length of 1024 characters. |

### BaseRichMediaStudioCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`BaseRichMediaStudioCreative`** | | |
| `studioCreativeId` | `long` | The creative ID as known by Rich Media Studio creative. This attribute is readonly. |
| `totalFileSize` | `long` | The total size of all assets in bytes. This attribute is readonly. |
| `adTagKeys` | `string[]` | Ad tag keys. This attribute is optional and updatable. |
| `customKeyValues` | `string[]` | Custom key values. This attribute is optional and updatable. |
| `surveyUrl` | `string` | The survey URL for this creative. This attribute is optional and updatable. |
| `allImpressionsUrl` | `string` | The tracking URL to be triggered when an ad starts to play, whether Rich Media or backup content is displayed. Behaves like the `/imp` URL that DART used to track impressions. This URL can't exceed... |
| `richMediaImpressionsUrl` | `string` | The tracking URL to be triggered when any rich media artwork is displayed in an ad. Behaves like the `/imp` URL that DART used to track impressions. This URL can't exceed 1024 characters and must s... |
| `backupImageImpressionsUrl` | `string` | The tracking URL to be triggered when the Rich Media backup image is served. This attribute is optional and updatable. |
| `overrideCss` | `string` | The override CSS. You can put custom CSS code here to repair creative styling; e.g. `tr td { background-color:#FBB;`}. This attribute is optional and updatable. |
| `requiredFlashPluginVersion` | `string` | The Flash plugin version required to view this creative; e.g. `Flash 10.2/AS 3`. This attribute is read only. |
| `duration` | `int` | The duration of the creative in milliseconds. This attribute is optional and updatable. |
| `richMediaStudioChildAssetProperties` | `RichMediaStudioChildAssetPr...[]` | The list of child assets associated with this creative. This attribute is read only. |

### BaseVideoCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseVideoCreative`** | | |
| `duration` | `int` | The expected duration of this creative in milliseconds. |
| `allowDurationOverride` | `boolean` | Allows the creative duration to differ from the actual asset durations. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `adId` | `string` | The ad id associated with the video as defined by the `adIdType` registry. This field is required if `adIdType` is not AdIdType.NONE. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |

### BooleanValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`BooleanValue`** | | |
| `value` | `boolean` | The boolean value. |

### ClickTag

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | Name of the click tag, follows the regex "clickTag\\d\*" |
| `url` | `string` | URL of the click tag. |

### ClickTrackingCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`ClickTrackingCreative`** | | |
| `clickTrackingUrl` | `string` | The click tracking URL. This attribute is required. |

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

### ConversionEvent_TrackingUrlsMapEntry

| Field | Type | Description |
|-------|------|-------------|
| `value` | `TrackingUrls` |  |

### Creative

| Field | Type | Description |
|-------|------|-------------|
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |

### CreativeAsset

| Field | Type | Description |
|-------|------|-------------|
| `assetId` | `long` | The ID of the asset. This attribute is generated by Google upon creation. |
| `assetByteArray` | `base64Binary` | The content of the asset as a byte array. This attribute is required when creating the creative that contains this asset if an `assetId` is not provided. When updating the content, pass a new byte ... |
| `fileName` | `string` | The file name of the asset. This attribute is required when creating a new asset (e.g. when assetByteArray is not null). |
| `fileSize` | `long` | The file size of the asset in bytes. This attribute is read-only. |
| `assetUrl` | `string` | A URL where the asset can be previewed at. This field is read-only and set by Google. |
| `size` | `Size` | The size of the asset. Note that this may not always reflect the actual physical size of the asset, but may reflect the expected size. This attribute is read-only and is populated by Google. |
| `clickTags` | `ClickTag[]` | The click tags of the asset. This field is read-only. |

### CreativeAssetMacroError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CreativeAssetMacroError`** | | |

### CreativeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CreativeError`** | | |

### CreativePage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `Creative[]` | The collection of creatives contained within this page. |

### CreativeSetError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CreativeSetError`** | | |

### CreativeTemplateError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CreativeTemplateError`** | | |

### CreativeTemplateOperationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CreativeTemplateOperationError`** | | |

### CustomCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`CustomCreative`** | | |
| `htmlSnippet` | `string` | The HTML snippet that this creative delivers. This attribute is required. |
| `customCreativeAssets` | `CustomCreativeAsset[]` | A list of file assets that are associated with this creative, and can be referenced in the snippet. |
| `isInterstitial` | `boolean` | `true` if this custom creative is interstitial. An interstitial creative will not consider an impression served until it is fully rendered in the browser. |
| `isSafeFrameCompatible` | `boolean` | Whether the Creative is compatible for SafeFrame rendering. This attribute is optional and defaults to `true`. |
| `thirdPartyImpressionTrackingUrls` | `string[]` | A list of impression tracking URLs to ping when this creative is displayed. This field is optional. |

### CustomCreativeAsset

| Field | Type | Description |
|-------|------|-------------|
| `macroName` | `string` | The name by which the associated asset will be referenced. For example, if the value is "foo", then the asset can be inserted into an HTML snippet using the macro: "%%FILE:foo%%". |
| `asset` | `CreativeAsset` | The asset. This attribute is required. To view the asset, use CreativeAsset.assetUrl. |

### CustomCreativeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CustomCreativeError`** | | |

### CustomFieldValueError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CustomFieldValueError`** | | |

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

### DeactivateCreatives

| Field | Type | Description |
|-------|------|-------------|
| **`CreativeAction` (inherited)** | | |
| **`DeactivateCreatives`** | | |

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

### FileError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`FileError`** | | |

### HasDestinationUrlCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative`** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |

### HasHtmlSnippetDynamicAllocationCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`BaseDynamicAllocationCreative` (inherited)** | | |
| **`HasHtmlSnippetDynamicAllocationCreative`** | | |
| `codeSnippet` | `string` | The code snippet (ad tag) from Ad Exchange or AdSense to traffic the dynamic allocation creative. Only valid Ad Exchange or AdSense parameters will be considered. Any extraneous HTML or JavaScript ... |

### Html5Creative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`Html5Creative`** | | |
| `overrideSize` | `boolean` | Allows the creative size to differ from the actual HTML5 asset size. This attribute is optional. |
| `thirdPartyImpressionTrackingUrls` | `string[]` | Impression tracking URLs to ping when this creative is displayed. This field is optional. |
| `thirdPartyClickTrackingUrl` | `string` | A click tracking URL to ping when this creative is clicked. This field is optional. |
| `isSafeFrameCompatible` | `boolean` | Whether the Creative is compatible for SafeFrame rendering. This attribute is optional and defaults to `true`. |
| `html5Asset` | `CreativeAsset` | The HTML5 asset. To preview the HTML5 asset, use the CreativeAsset.assetUrl. In this field, the CreativeAsset.assetByteArray must be a zip bundle and the CreativeAsset.fileName must have a zip exte... |

### HtmlBundleProcessorError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`HtmlBundleProcessorError`** | | |

### ImageCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseImageCreative` (inherited)** | | |
| `overrideSize` | `boolean` | Allows the creative size to differ from the actual image asset size. This attribute is optional. |
| `primaryImageAsset` | `CreativeAsset` | The primary image asset associated with this creative. This attribute is required. |
| **`ImageCreative`** | | |
| `altText` | `string` | Alternative text to be rendered along with the creative used mainly for accessibility. This field is optional and has a maximum length of 500 characters. |
| `thirdPartyImpressionTrackingUrls` | `string[]` | A list of impression tracking URL to ping when this creative is displayed. This field is optional and each string has a maximum length of 1024 characters. |
| `secondaryImageAssets` | `CreativeAsset[]` | The list of secondary image assets associated with this creative. This attribute is optional. Secondary image assets can be used to store different resolution versions of the primary asset for use ... |

### ImageError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ImageError`** | | |

### ImageOverlayCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseImageCreative` (inherited)** | | |
| `overrideSize` | `boolean` | Allows the creative size to differ from the actual image asset size. This attribute is optional. |
| `primaryImageAsset` | `CreativeAsset` | The primary image asset associated with this creative. This attribute is required. |
| **`ImageOverlayCreative`** | | |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. This attribute is read-only. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `duration` | `int` | Minimum suggested duration in milliseconds. This attribute is optional. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |

### ImageRedirectCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseImageRedirectCreative` (inherited)** | | |
| `imageUrl` | `string` | The URL where the actual asset resides. This attribute is required and has a maximum length of 1024 characters. |
| **`ImageRedirectCreative`** | | |
| `altText` | `string` | Alternative text to be rendered along with the creative used mainly for accessibility. This field is optional and has a maximum length of 500 characters. |
| `thirdPartyImpressionTrackingUrls` | `string[]` | A list of impression tracking URL to ping when this creative is displayed. This field is optional and each string has a maximum length of 1024 characters. |

### ImageRedirectOverlayCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseImageRedirectCreative` (inherited)** | | |
| `imageUrl` | `string` | The URL where the actual asset resides. This attribute is required and has a maximum length of 1024 characters. |
| **`ImageRedirectOverlayCreative`** | | |
| `assetSize` | `Size` | The size of the image asset. Note that this may differ from size if the asset is not expected to fill the entire video player. This attribute is optional. |
| `duration` | `int` | Minimum suggested duration in milliseconds. This attribute is optional. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |

### InternalApiError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`InternalApiError`** | | |

### InternalRedirectCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`InternalRedirectCreative`** | | |
| `assetSize` | `Size` | The asset size of an internal redirect creative. Note that this may differ from `size` if users set `overrideSize` to true. This attribute is read-only and is populated by Google. |
| `internalRedirectUrl` | `string` | The internal redirect URL of the DFA or DART for Publishers hosted creative. This attribute is required and has a maximum length of 1024 characters. |
| `overrideSize` | `boolean` | Allows the creative size to differ from the actual size specified in the internal redirect's url. This attribute is optional. |
| `isInterstitial` | `boolean` | `true` if this internal redirect creative is interstitial. |
| `thirdPartyImpressionTrackingUrls` | `string[]` | A list of impression tracking URLs to ping when this creative is displayed. This field is optional. |

### InvalidPhoneNumberError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`InvalidPhoneNumberError`** | | |

### InvalidUrlError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`InvalidUrlError`** | | |

### LabelEntityAssociationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`LabelEntityAssociationError`** | | |

### LegacyDfpCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`LegacyDfpCreative`** | | |

### LineItemCreativeAssociationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`LineItemCreativeAssociationError`** | | |

### LongCreativeTemplateVariableValue

| Field | Type | Description |
|-------|------|-------------|
| **`BaseCreativeTemplateVariableValue` (inherited)** | | |
| `uniqueName` | `string` | A uniqueName of the CreativeTemplateVariable. |
| **`LongCreativeTemplateVariableValue`** | | |
| `value` | `long` | The long value of CreativeTemplateVariable |

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

### ProgrammaticCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`ProgrammaticCreative`** | | |

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

### RichMediaStudioChildAssetProperty

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | The name of the asset as known by Rich Media Studio. This attribute is readonly. |
| `totalFileSize` | `long` | The total size of the asset in bytes. This attribute is readonly. |
| `width` | `int` | Width of the widget in pixels. This attribute is readonly. |
| `height` | `int` | Height of the widget in pixels. This attribute is readonly. |
| `url` | `string` | The URL of the asset. This attribute is readonly. |

### RichMediaStudioCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`BaseRichMediaStudioCreative` (inherited)** | | |
| `studioCreativeId` | `long` | The creative ID as known by Rich Media Studio creative. This attribute is readonly. |
| `totalFileSize` | `long` | The total size of all assets in bytes. This attribute is readonly. |
| `adTagKeys` | `string[]` | Ad tag keys. This attribute is optional and updatable. |
| `customKeyValues` | `string[]` | Custom key values. This attribute is optional and updatable. |
| `surveyUrl` | `string` | The survey URL for this creative. This attribute is optional and updatable. |
| `allImpressionsUrl` | `string` | The tracking URL to be triggered when an ad starts to play, whether Rich Media or backup content is displayed. Behaves like the `/imp` URL that DART used to track impressions. This URL can't exceed... |
| `richMediaImpressionsUrl` | `string` | The tracking URL to be triggered when any rich media artwork is displayed in an ad. Behaves like the `/imp` URL that DART used to track impressions. This URL can't exceed 1024 characters and must s... |
| `backupImageImpressionsUrl` | `string` | The tracking URL to be triggered when the Rich Media backup image is served. This attribute is optional and updatable. |
| `overrideCss` | `string` | The override CSS. You can put custom CSS code here to repair creative styling; e.g. `tr td { background-color:#FBB;`}. This attribute is optional and updatable. |
| `requiredFlashPluginVersion` | `string` | The Flash plugin version required to view this creative; e.g. `Flash 10.2/AS 3`. This attribute is read only. |
| `duration` | `int` | The duration of the creative in milliseconds. This attribute is optional and updatable. |
| `richMediaStudioChildAssetProperties` | `RichMediaStudioChildAssetPr...[]` | The list of child assets associated with this creative. This attribute is read only. |
| **`RichMediaStudioCreative`** | | |
| `isInterstitial` | `boolean` | `true` if this is interstitial. An interstitial creative will not consider an impression served until it is fully rendered in the browser. This attribute is readonly. |

### RichMediaStudioCreativeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`RichMediaStudioCreativeError`** | | |

### ServerError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`ServerError`** | | |

### SetTopBoxCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseVideoCreative` (inherited)** | | |
| `duration` | `int` | The expected duration of this creative in milliseconds. |
| `allowDurationOverride` | `boolean` | Allows the creative duration to differ from the actual asset durations. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `adId` | `string` | The ad id associated with the video as defined by the `adIdType` registry. This field is required if `adIdType` is not AdIdType.NONE. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |
| **`SetTopBoxCreative`** | | |
| `externalAssetId` | `string` | An external asset identifier that is used in the cable system. This attribute is read-only after creation. |
| `providerId` | `string` | An identifier for the provider in the cable system. This attribute is read-only after creation. |
| `availabilityRegionIds` | `string[]` | IDs of regions where the creative is available to serve from a local cable video-on-demand server. This attribute is optional. |
| `licenseWindowStartDateTime` | `DateTime` | The date and time that this creative can begin serving from a local cable video-on-demand server. This attribute is optional. |
| `licenseWindowEndDateTime` | `DateTime` | The date and time that this creative can no longer be served from a local cable video-on-demand server. This attribute is optional. |

### SetTopBoxCreativeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`SetTopBoxCreativeError`** | | |

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

### StringCreativeTemplateVariableValue

| Field | Type | Description |
|-------|------|-------------|
| **`BaseCreativeTemplateVariableValue` (inherited)** | | |
| `uniqueName` | `string` | A uniqueName of the CreativeTemplateVariable. |
| **`StringCreativeTemplateVariableValue`** | | |
| `value` | `string` | The string value of CreativeTemplateVariable |

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

### SwiffyConversionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`SwiffyConversionError`** | | |

### TemplateCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`TemplateCreative`** | | |
| `creativeTemplateId` | `long` | Creative template ID that this creative is created from. This field is required for creation and immutable. |
| `isInterstitial` | `boolean` | `true` if this template instantiated creative is interstitial. This attribute is read-only and is assigned by Google based on the creative template. |
| `isNativeEligible` | `boolean` | `true` if this template instantiated creative is eligible for native adserving. This attribute is read-only and is assigned by Google based on the creative template. |
| `isSafeFrameCompatible` | `boolean` | Whether the Creative is compatible for SafeFrame rendering. This attribute is read-only and is assigned by Google based on the CreativeTemplate. |
| `destinationUrl` | `string` | The URL the user is directed to if they click on the creative. This attribute is only required if the template snippet contains the `%u` or `%%DEST_URL%%` macro. It has a maximum length of 1024 cha... |
| `creativeTemplateVariableValues` | `BaseCreativeTemplateVariabl...[]` | Stores values of CreativeTemplateVariable in the CreativeTemplate. |

### TemplateInstantiatedCreativeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`TemplateInstantiatedCreativeError`** | | |

### TextValue

| Field | Type | Description |
|-------|------|-------------|
| **`Value` (inherited)** | | |
| **`TextValue`** | | |
| `value` | `string` | The string value. |

### ThirdPartyCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`ThirdPartyCreative`** | | |
| `snippet` | `string` | The HTML snippet that this creative delivers. This attribute is required. |
| `expandedSnippet` | `string` | The HTML snippet that this creative delivers with macros expanded. This attribute is read-only and is set by Google. |
| `isSafeFrameCompatible` | `boolean` | Whether the Creative is compatible for SafeFrame rendering. This attribute is optional and defaults to `true`. |
| `thirdPartyImpressionTrackingUrls` | `string[]` | A list of impression tracking URLs to ping when this creative is displayed. This field is optional. |
| `ampRedirectUrl` | `string` | The URL of the AMP creative. |

### ThirdPartyDataDeclaration

| Field | Type | Description |
|-------|------|-------------|
| `thirdPartyCompanyIds` | `long[]` |  |

### TrackingUrls

| Field | Type | Description |
|-------|------|-------------|
| `urls` | `string[]` | A list of all URLs that should be pinged. |

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

### UnsupportedCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`UnsupportedCreative`** | | |
| `unsupportedCreativeType` | `string` | The creative type that is unsupported by this API version. |

### UpdateResult

| Field | Type | Description |
|-------|------|-------------|
| `numChanges` | `int` | The number of objects that were changed as a result of performing the action. |

### UrlCreativeTemplateVariableValue

| Field | Type | Description |
|-------|------|-------------|
| **`BaseCreativeTemplateVariableValue` (inherited)** | | |
| `uniqueName` | `string` | A uniqueName of the CreativeTemplateVariable. |
| **`UrlCreativeTemplateVariableValue`** | | |
| `value` | `string` | The url value of CreativeTemplateVariable |

### VastRedirectCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`VastRedirectCreative`** | | |
| `vastXmlUrl` | `string` | The URL where the 3rd party VAST XML is hosted. This attribute is required. |
| `duration` | `int` | The duration of the VAST ad in milliseconds. This attribute is required. |
| `vastPricingEnabled` | `boolean` | Whether pricing information from the VAST response will be used during ad selection. |
| `isProgrammaticDemandSource` | `boolean` | Whether this is a redirect to a programmatic demand source. |
| `serverSideUnwrappingDisabled` | `boolean` | Whether server-side unwrapping is disabled. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |
| `isAudio` | `boolean` | Whether the 3rd party VAST XML points to an audio ad. When true, VastRedirectCreative.size will always be 1x1. |

### VideoCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseVideoCreative` (inherited)** | | |
| `duration` | `int` | The expected duration of this creative in milliseconds. |
| `allowDurationOverride` | `boolean` | Allows the creative duration to differ from the actual asset durations. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `adId` | `string` | The ad id associated with the video as defined by the `adIdType` registry. This field is required if `adIdType` is not AdIdType.NONE. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |
| **`VideoCreative`** | | |
| `videoSourceUrl` | `string` | A URL that points to the source media that will be used for transcoding. |

### VideoMetadata

| Field | Type | Description |
|-------|------|-------------|
| `duration` | `int` | The duration of the asset in milliseconds. This attribute is required. |
| `bitRate` | `int` | The bit rate of the asset in kbps. If the asset can play at a range of bit rates (such as an Http Live Streaming video), then set the bit rate to zero and populate the minimum and maximum bit rate ... |
| `minimumBitRate` | `int` | The minimum bitrate of the video in kbps. Only set this if the asset can play at a range of bit rates. |
| `maximumBitRate` | `int` | The maximum bitrate of the video in kbps. Only set this if the asset can play at a range of bit rates. |
| `size` | `Size` | The size (width and height) of the asset. This attribute is required. |
| `codecs` | `string[]` | The codecs of the asset. This attribute is optional and defaults to an empty list. |

### VideoRedirectAsset

| Field | Type | Description |
|-------|------|-------------|
| **`RedirectAsset` (inherited)** | | |
| `redirectUrl` | `string` | The URL where the asset is hosted. |
| **`VideoRedirectAsset`** | | |
| `metadata` | `VideoMetadata` | Metadata related to the asset. This attribute is required. |

### VideoRedirectCreative

| Field | Type | Description |
|-------|------|-------------|
| **`Creative` (inherited)** | | |
| `advertiserId` | `long` | The ID of the advertiser that owns the creative. This attribute is required. |
| `id` | `long` | Uniquely identifies the `Creative`. This value is read-only and is assigned by Google when the creative is created. This attribute is required for updates. |
| `name` | `string` | The name of the creative. This attribute is required and has a maximum length of 255 characters. |
| `size` | `Size` | The Size of the creative. This attribute is required for creation and then is read-only. |
| `previewUrl` | `string` | The URL of the creative for previewing the media. This attribute is read-only and is assigned by Google when a creative is created. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied to this creative. |
| `lastModifiedDateTime` | `DateTime` | The date and time this creative was last modified. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with this creative. |
| `thirdPartyDataDeclaration` | `ThirdPartyDataDeclaration` | The third party companies associated with this creative. This is distinct from any associated companies that Google may detect programmatically. |
| `adBadgingEnabled` | `boolean` | Whether the creative has ad badging enabled. Defaults to false for `CreativeType.VAST_REDIRECT`, `CreativeType.THIRD_PARTY`, `CreativeType.AUDIO_VAST_REDIRECT`, `CreativeType.PROGRAMMATIC`, `Creati... |
| `selfDeclaredEuropeanUnionPoliticalContent` | `boolean` | Whether the publisher has declared that the creative contains European Union political content. Support for this field will be rolled out gradually in Q3 2025. Until then, setting this field will r... |
| **`HasDestinationUrlCreative` (inherited)** | | |
| `destinationUrl` | `string` | The URL that the user is directed to if they click on the creative. This attribute is required unless the `destinationUrlType` is DestinationUrlType.NONE, and has a maximum length of 1024 characters. |
| **`BaseVideoCreative` (inherited)** | | |
| `duration` | `int` | The expected duration of this creative in milliseconds. |
| `allowDurationOverride` | `boolean` | Allows the creative duration to differ from the actual asset durations. This attribute is optional. |
| `trackingUrls` | `ConversionEvent_TrackingUrl...[]` | A map from `ConversionEvent` to a list of URLs that will be pinged when the event happens. This attribute is optional. |
| `companionCreativeIds` | `long[]` | The IDs of the companion creatives that are associated with this creative. This attribute is optional. |
| `customParameters` | `string` | A comma separated key=value list of parameters that will be supplied to the creative, written into the VAST `AdParameters` node. This attribute is optional. |
| `adId` | `string` | The ad id associated with the video as defined by the `adIdType` registry. This field is required if `adIdType` is not AdIdType.NONE. |
| `vastPreviewUrl` | `string` | An ad tag URL that will return a preview of the VAST XML response specific to this creative. This attribute is read-only. |
| **`VideoRedirectCreative`** | | |
| `videoAssets` | `VideoRedirectAsset[]` | The video creative assets. |
| `mezzanineFile` | `VideoRedirectAsset` | The high quality mezzanine video asset. |

