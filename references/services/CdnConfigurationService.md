# CdnConfigurationService Reference

**Service**: CdnConfigurationService

**Types**: 45

## Methods

### createCdnConfigurations
- **Request**: `CdnConfiguration[] cdnConfigurations`
- **Response**: `CdnConfiguration[]`

### getCdnConfigurationsByStatement
- **Request**: `Statement statement`
- **Response**: `CdnConfigurationPage`

### performCdnConfigurationAction
- **Request**: `CdnConfigurationAction cdnConfigurationAction`
- **Request**: `Statement filterStatement`
- **Response**: `UpdateResult`

### updateCdnConfigurations
- **Request**: `CdnConfiguration[] cdnConfigurations`
- **Response**: `CdnConfiguration[]`

## Types

### ActivateCdnConfigurations

| Field | Type | Description |
|-------|------|-------------|
| **`CdnConfigurationAction` (inherited)** | | |
| **`ActivateCdnConfigurations`** | | |

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

### ArchiveCdnConfigurations

| Field | Type | Description |
|-------|------|-------------|
| **`CdnConfigurationAction` (inherited)** | | |
| **`ArchiveCdnConfigurations`** | | |

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

### CdnConfiguration

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the CdnConfiguration. This value is read-only and is assigned by Google. |
| `name` | `string` | The name of the CdnConfiguration. This value is required to create a CDN configuration and has a maximum length of 255 characters. |
| `sourceContentConfiguration` | `SourceContentConfiguration` | Parameters about this CDN configuration as a source of content. This facilitates fetching the original content for conditioning and delivering the original content as part of a modified stream. |

### CdnConfigurationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`CdnConfigurationError`** | | |

### CdnConfigurationPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `CdnConfiguration[]` | The collection of CDN configurations contained within this page. |

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

### MediaLocationSettings

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | The name of the media location. This value is read-only and is assigned by Google. |
| `urlPrefix` | `string` | The url prefix of the media location. This value is required for a valid media location. |
| `securityPolicy` | `SecurityPolicySettings` | The security policy and authentication credentials needed to access the content in this media location. This value is required for a valid media location. |

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

### SecurityPolicySettings

| Field | Type | Description |
|-------|------|-------------|
| `tokenAuthenticationKey` | `string` | Shared security key used to generate the Akamai HMAC token for authenticating requests. This field is only applicable when the value of securityPolicyType is equal to SecurityPolicyType.AKAMAI and ... |
| `disableServerSideUrlSigning` | `boolean` | Whether the segment URLs should be signed using the tokenAuthenticationKey on the server. This is only applicable for delivery media locations that have token authentication enabled. |
| `originPathPrefix` | `string` | The origin path prefix provided by the publisher for the master playlist. This field is only applicable for delivery media locations with the value of originForwardingType set to OriginForwardingTy... |
| `mediaPlaylistOriginPathPrefix` | `string` | The origin path prefix provided by the publisher for the media playlists. This field is only applicable for delivery media locations with the value of mediaPlaylistOriginForwardingType set to Origi... |
| `keysetName` | `string` | The name of the EdgeCacheKeyset on the Media CDN configuration that will be used to validate signed requests from DAI to ingest content. |
| `signedRequestExpirationTtlSeconds` | `long` | The amount of time in seconds for which a request signed with a short token will be valid. Only required if signedRequestMaximumExpirationTtl has been set in the Media CDN configuration. |

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

### SourceContentConfiguration

| Field | Type | Description |
|-------|------|-------------|
| `ingestSettings` | `MediaLocationSettings` | Configuration for how DAI should ingest media. At ingest time, we match the url prefix of media in a stream's playlist with an ingest location and use the authentication credentials from the corres... |
| `defaultDeliverySettings` | `MediaLocationSettings` | Default configuration for how DAI should deliver the non-modified media segments. At delivery time, we replace the ingest location's url prefix with the delivery location's URL prefix and use the s... |

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

### UpdateResult

| Field | Type | Description |
|-------|------|-------------|
| `numChanges` | `int` | The number of objects that were changed as a result of performing the action. |

