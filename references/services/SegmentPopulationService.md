# SegmentPopulationService Reference

**Service**: SegmentPopulationService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/SegmentPopulationService
**Types**: 5

## Methods

### getSegmentPopulationResultsByIds
- **Request**: `long[] batchUploadIds`
- **Response**: `SegmentPopulationResults[]`

### performSegmentPopulationAction
- **Request**: `SegmentPopulationAction action`, ` long[] batchUploadIds`
- **Response**: `UpdateResult`

### updateSegmentMemberships
- **Request**: `SegmentPopulationRequest updateRequest`
- **Response**: `SegmentPopulationResponse`

## Types

### SegmentPopulationRequest

| Field | Type | Description |
|-------|------|-------------|
| `batchUploadId` | `long` | The ID of the batch that will process the identifiers. If not specified, will be provided by Google. |
| `segmentId` | `long` | The ID of the AudienceSegment that will be populated. Required. |
| `isDeletion` | `boolean` | Whether the identifiers should be added or removed from the segment. |
| `identifierType` | `IdentifierType` | The type of identifier being operated on. |
| `ids` | `string[]` | The identifiers to upload. Max 100,000 elements. |
| `consentType` | `ConsentType` | User consent type (`GRANTED`, `DENIED`, `UNSPECIFIED`). |

### SegmentPopulationResponse

| Field | Type | Description |
|-------|------|-------------|
| `batchUploadId` | `long` | The batch ID used to look up status via `getSegmentPopulationResultsByIds`. |
| `idErrors` | `IdError[]` | Errors encountered on individual identifiers. |

### SegmentPopulationResults

| Field | Type | Description |
|-------|------|-------------|
| `batchUploadId` | `long` | The batch ID used to look up the results. |
| `segmentId` | `long` | The segment ID associated with the segment population job. |
| `status` | `SegmentPopulationStatus` | The current status of the upload request (`PREPARING`, `SUCCESS`, `FAILED`, `EXPIRED`). |
| `numSuccessfulIdCount` | `long` | The number of IDs that were processed successfully. |
| `idErrors` | `IdError[]` | Identifiers with errors. |

### SegmentPopulationAction (Subclasses)
- `ProcessAction` (`{'xsi_type': 'ProcessAction'}`)

## Enumerations

### IdentifierType

| Value | Description |
|-------|-------------|
| `PUBLISHER_PROVIDED_ID` | Publisher Provided Identifier (PPID). |
| `IDFA` | iOS Advertising Identifier. |
| `AD_ID` | Google Advertising ID (AAID/GAID). |
| `RIDA` | Roku ID for Advertising. |
| `TVOS_IDFA` | Apple tvOS ID for Advertising. |
| `UNKNOWN` | Unknown identifier type. |

### SegmentPopulationStatus

| Value | Description |
|-------|-------------|
| `PREPARING` | Batch upload is being prepared. |
| `READY` | Ready to be processed via `ProcessAction`. |
| `PROCESSING` | Currently processing. |
| `SUCCESS` | Completed successfully. |
| `FAILED` | Failed. |
| `EXPIRED` | Expired. |
| `UNKNOWN` | Unknown status. |
