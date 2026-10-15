# AdjustmentService Reference

**Service**: AdjustmentService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/AdjustmentService
**Types**: 9

## Methods

### calculateDailyAdOpportunityCounts
- **Request**: `ForecastAdjustment forecastAdjustment`
- **Response**: `ForecastAdjustment`

### createForecastAdjustments
- **Request**: `ForecastAdjustment[] forecastAdjustments`
- **Response**: `ForecastAdjustment[]`

### createTrafficForecastSegments
- **Request**: `TrafficForecastSegment[] trafficForecastSegments`
- **Response**: `TrafficForecastSegment[]`

### getForecastAdjustmentsByStatement
- **Request**: `Statement filterStatement` (PQL filterable: `id`, `trafficForecastSegmentId`, `name`, `startDate`, `endDate`, `status`)
- **Response**: `ForecastAdjustmentPage`

### getTrafficForecastSegmentsByStatement
- **Request**: `Statement filterStatement` (PQL filterable: `id`, `name`, `forecastAdjustmentCount`, `creationDateTime`)
- **Response**: `TrafficForecastSegmentPage`

### performForecastAdjustmentAction
- **Request**: `ForecastAdjustmentAction forecastAdjustmentAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateForecastAdjustments
- **Request**: `ForecastAdjustment[] forecastAdjustments`
- **Response**: `ForecastAdjustment[]`

### updateTrafficForecastSegments
- **Request**: `TrafficForecastSegment[] trafficForecastSegments`
- **Response**: `TrafficForecastSegment[]`

## Types

### ForecastAdjustment

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the ForecastAdjustment. This field is read-only. |
| `trafficForecastSegmentId` | `long` | The ID of the parent TrafficForecastSegment. This field is required and immutable after creation. |
| `name` | `string` | Name of the ForecastAdjustment. This field is required and has a maximum length of 255 characters. |
| `startDate` | `Date` | The start `Date` of the adjustment. Required. |
| `endDate` | `Date` | The end `Date` of the adjustment (inclusive). Required. |
| `status` | `ForecastAdjustmentStatus` | Status of the ForecastAdjustment. Read-only. |
| `volumeType` | `ForecastAdjustmentVolumeType` | The volume type of the adjustment (`DAILY_VOLUME`, `TOTAL_VOLUME`, `HISTORICAL_BASIS_VOLUME`). Required. |
| `allowAdjustingForecastAboveRecommendedLimit` | `boolean` | Whether to allow adjusting forecast above recommended limit. |
| `dailyVolumeSettings` | `DailyVolumeSettings` | Settings when `volumeType == 'DAILY_VOLUME'`. |
| `totalVolumeSettings` | `TotalVolumeSettings` | Settings when `volumeType == 'TOTAL_VOLUME'`. |
| `historicalBasisVolumeSettings` | `HistoricalBasisVolumeSettings` | Settings when `volumeType == 'HISTORICAL_BASIS_VOLUME'`. |
| `calculatedDailyAdOpportunityCounts` | `long[]` | The daily number of ad opportunities calculated for each day in the adjustment date range. Read-only. |

### TrafficForecastSegment

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | Unique ID of the `TrafficForecastSegment`. Read-only. |
| `name` | `string` | Name of the `TrafficForecastSegment`. Required, max 255 chars, unique across network. |
| `targeting` | `Targeting` | The `Targeting` that defines a segment of traffic. Required. Cannot be updated after creation if adjustments are associated. |
| `activeForecastAdjustmentCount` | `int` | The number of active `ForecastAdjustment`s associated with this segment. Read-only. |
| `creationDateTime` | `DateTime` | The date and time that the `TrafficForecastSegment` was created. Read-only. |

### DailyVolumeSettings

| Field | Type | Description |
|-------|------|-------------|
| `adOpportunityCounts` | `long[]` | List of ad opportunity counts corresponding to each day in the adjustment date range. |

### TotalVolumeSettings

| Field | Type | Description |
|-------|------|-------------|
| `adOpportunityCount` | `long` | Total ad opportunity count over the entire adjustment date range. |

### HistoricalBasisVolumeSettings

| Field | Type | Description |
|-------|------|-------------|
| `useParentTrafficForecastSegmentTargeting` | `boolean` | Whether the parent segment targeting or the `targeting` field on this settings object is used. |
| `targeting` | `Targeting` | The historical targeting criteria used as basis. |
| `historicalDateRange` | `DateRange` | The historical date range (`startDate`, `endDate`) to scale from. |
| `multiplierMilliPercent` | `long` | The multiplier applied to historical traffic in milli-percent (e.g. `110000` = 110%). |

### ForecastAdjustmentPage / TrafficForecastSegmentPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | Total result set size. |
| `startIndex` | `int` | Start index of this page. |
| `results` | `ForecastAdjustment[]` / `TrafficForecastSegment[]` | Results on this page. |

## Enumerations

### ForecastAdjustmentStatus

| Value | Description |
|-------|-------------|
| `ACTIVE` | Indicates the current adjustment is active. |
| `INACTIVE` | Indicates the current adjustment is inactive. |
| `UNKNOWN` | Unknown status. |

### ForecastAdjustmentVolumeType

| Value | Description |
|-------|-------------|
| `DAILY_VOLUME` | Volume is defined by a list of daily ad opportunity counts. |
| `TOTAL_VOLUME` | Volume is defined by a single total ad opportunity count. |
| `HISTORICAL_BASIS_VOLUME` | Volume is defined by historical traffic multiplied by a percentage factor. |
| `UNKNOWN` | Unknown volume type. |
