# DaiAuthenticationKeyService Reference

**Service**: DaiAuthenticationKeyService

**Types**: 42

## Methods

### createDaiAuthenticationKeys
- **Request**: `DaiAuthenticationKey[] daiAuthenticationKeys`
- **Response**: `DaiAuthenticationKey[]`

### getDaiAuthenticationKeysByStatement
- **Request**: `Statement filterStatement`
- **Response**: `DaiAuthenticationKeyPage`

### performDaiAuthenticationKeyAction
- **Request**: `DaiAuthenticationKeyAction daiAuthenticationKeyAction`
- **Request**: `Statement filterStatement`
- **Response**: `UpdateResult`

### updateDaiAuthenticationKeys
- **Request**: `DaiAuthenticationKey[] daiAuthenticationKeys`
- **Response**: `DaiAuthenticationKey[]`

## Types

### ActivateDaiAuthenticationKeys

| Field | Type | Description |
|-------|------|-------------|
| **`DaiAuthenticationKeyAction` (inherited)** | | |
| **`ActivateDaiAuthenticationKeys`** | | |

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

### DaiAuthenticationKey

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the DaiAuthenticationKey. This value is read-only and is assigned by Google. |
| `key` | `string` | The value of the secure key. This value is read-only and is assigned by Google. |
| `creationDateTime` | `DateTime` | The date and time this DaiAuthenticationKey was created. This value is read-only and is assigned by Google. |
| `name` | `string` | The name for this DaiAuthenticationKey. |

### DaiAuthenticationKeyActionError

| Field | Type | Description |
|-------|------|-------------|
| **`ApiError` (inherited)** | | |
| `fieldPath` | `string` | The OGNL field path to identify cause of error. |
| `fieldPathElements` | `FieldPathElement[]` | A parsed copy of the field path. For example, the field path "operations[1].operand" corresponds to this list: {FieldPathElement(field = "operations", index = 1), FieldPathElement(field = "operand"... |
| `trigger` | `string` | The data that caused the error. |
| `errorString` | `string` | A simple string representation of the error and reason. |
| **`DaiAuthenticationKeyActionError`** | | |

### DaiAuthenticationKeyPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `DaiAuthenticationKey[]` | The collection of live stream events contained within this page. |

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

### DeactivateDaiAuthenticationKeys

| Field | Type | Description |
|-------|------|-------------|
| **`DaiAuthenticationKeyAction` (inherited)** | | |
| **`DeactivateDaiAuthenticationKeys`** | | |

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

