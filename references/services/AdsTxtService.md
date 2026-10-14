# AdsTxtService Reference

**Service**: AdsTxtService

**Types**: 22

## Methods

### getMcmSupplyChainDiagnosticsDownloadUrl
- **Response**: `xsd:string`

## Types

### ApiError

| Field | Type | Description |
|-------|------|-------------|
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |

### ApiException

| Field | Type | Description |
|-------|------|-------------|
| **`ApplicationException` (inherited)** | | |
| `message` | `string` |  |
| **`ApiException`** | | |
| `errors` | `ApiError[]` | 19. `StringLengthError` |

### ApiVersionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`ApiVersionError`** | | |

### AuthenticationError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`AuthenticationError`** | | |

### CollectionSizeError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`CollectionSizeError`** | | |

### CommonError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`CommonError`** | | |

### FeatureError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`FeatureError`** | | |

### FieldPathElement

| Field | Type | Description |
|-------|------|-------------|
| `field` | `string` |  |
| `index` | `int` |  |

### InternalApiError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`InternalApiError`** | | |

### NotNullError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`NotNullError`** | | |

### ParseError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`ParseError`** | | |

### PermissionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`PermissionError`** | | |

### PublisherQueryLanguageContextError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`PublisherQueryLanguageContextError`** | | |

### PublisherQueryLanguageSyntaxError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`PublisherQueryLanguageSyntaxError`** | | |

### QuotaError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`QuotaError`** | | |

### RequestError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`RequestError`** | | |

### RequiredCollectionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`RequiredCollectionError`** | | |

### RequiredError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`RequiredError`** | | |

### ServerError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`ServerError`** | | |

### StatementError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`StatementError`** | | |

### StringFormatError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`StringFormatError`** | | |

### StringLengthError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` |  |
| `fieldPathElements` | `FieldPathElement[]` |  |
| `trigger` | `string` |  |
| `errorString` | `string` |  |
| **`StringLengthError`** | | |

