# StreamActivityMonitorService Reference

**Service**: StreamActivityMonitorService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/StreamActivityMonitorService
**Types**: 5

## Methods

### getSamSessionsByStatement
- **Request**: `Statement statement` (PQL filterable: `sessionId`)
- **Response**: `SamSession[]`

### registerSessionsForMonitoring
- **Request**: `string[] sessionIds`
- **Response**: `string[]`

## Types

### SamSession

| Field | Type | Description |
|-------|------|-------------|
| `sessionId` | `string` | The UUID that uniquely identifies this DAI streaming session. |
| `isVod` | `boolean` | Whether this is a VOD session (`true`) or live stream (`false`). |
| `streamCreateRequest` | `StreamCreateRequest` | The initial request from the video player to retrieve the streaming URL chunks. |
| `adBreaks` | `AdBreak[]` | The list of debugging information that occurred at each ad break in the stream. |
| `startDateTime` | `DateTime` | The date and time the session started. |
| `sessionDurationMillis` | `long` | The VOD duration in milliseconds. |
| `contentDurationMillis` | `long` | The content duration in milliseconds. |

### AdBreak

| Field | Type | Description |
|-------|------|-------------|
| `rootAdResponses` | `AdResponse[]` | The root ad responses to the `adRequest`. |
| `adDecisionCreatives` | `AdDecisionCreative[]` | Contains the precise information about the creatives that were served in the ad break. |
| `podNum` | `int` | 1-based index of this pod within the whole stream. |
| `linearAbsolutePodNum` | `int` | For live streams, the absolute pod number. |
| `adBreakDurationMillis` | `long` | The duration of the ad break in milliseconds. |
| `filledDurationMillis` | `long` | The total duration of the creatives served within the ad break in milliseconds. |
| `servedDateTime` | `DateTime` | The date and time the ad break was served. |
| `startDateTime` | `DateTime` | The date and time the ad break started. |
| `samError` | `SamError` | Any error that occurred during the ad break. |

### AdDecisionCreative

| Field | Type | Description |
|-------|------|-------------|
| `sequence` | `int` | The position of the ad within the ad break (0-based). |
| `slateDurationMills` | `long` | Duration of the slate if this is a slate creative. |
| `creativeDurationMills` | `long` | Duration of the creative in milliseconds. |
| `creativeTranscode` | `CreativeTranscode` | Information about the transcoded creative. |
| `googleVideoId` | `string` | The Google-owned video ID of the creative. |
| `samError` | `SamError` | Information about any error associated with the creative. |
| `isTranscoded` | `boolean` | Whether the creative is transcoded. |
| `isDropped` | `boolean` | Whether the creative was dropped during ad selection. |
