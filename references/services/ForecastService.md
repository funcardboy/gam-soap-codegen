# ForecastService Reference

**Service**: ForecastService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/ForecastService
**Types**: 10

## Methods
- `getAvailabilityForecast(ProspectiveLineItem lineItem, AvailabilityForecastOptions forecastOptions) -> AvailabilityForecast`
- `getAvailabilityForecastById(long lineItemId, AvailabilityForecastOptions forecastOptions) -> AvailabilityForecast`
- `getDeliveryForecast(ProspectiveLineItem[] lineItems, DeliveryForecastOptions forecastOptions) -> DeliveryForecast`
- `getDeliveryForecastByIds(long[] lineItemIds, DeliveryForecastOptions forecastOptions) -> DeliveryForecast`
- `getTrafficData(TrafficDataRequest trafficDataRequest) -> TrafficDataResponse`

## Types

### AvailabilityForecast
| Field | Type | Description |
|-------|------|-------------|
| `lineItemId` | `long` | Uniquely identifies this availability forecast. |
| `orderId` | `long` | The unique ID for the `Order`. |
| `unitType` | `UnitType` | The unit with which the goal or cap of the `LineItem` is defined (`IMPRESSIONS`, `CLICKS`, `VIEWABLE_IMPRESSIONS`). |
| `availableUnits` | `long` | The number of units that can be booked without affecting the delivery of any reserved line items. |
| `deliveredUnits` | `long` | The number of units that have already been served if the reservation is already running. |
| `matchedUnits` | `long` | The number of units that match the specified targeting and delivery settings. |
| `possibleUnits` | `long` | The maximum number of units that could be booked by taking inventory away from lower-priority or same-priority line items. |
| `reservedUnits` | `long` | The number of reserved units requested. |
| `breakdowns` | `ForecastBreakdown[]` | Breakdowns for each time window / targeting dimension defined in `AvailabilityForecastOptions.breakdowns`. |
| `targetingCriteriaBreakdowns` | `TargetingCriteriaBreakdown[]` | Forecast breakdown by individual targeting criteria (`includeTargetingCriteriaBreakdown = True`). |
| `contendingLineItems` | `ContendingLineItem[]` | List of contending line items (`includeContendingLineItems = True`). |
| `alternativeUnitTypeForecasts` | `AlternativeUnitTypeForecast[]` | Forecasts in alternative unit types. |

### AvailabilityForecastOptions
| Field | Type | Description |
|-------|------|-------------|
| `includeTargetingCriteriaBreakdown` | `boolean` | Whether to include `targetingCriteriaBreakdowns`. |
| `includeContendingLineItems` | `boolean` | Whether to include `contendingLineItems`. |
| `breakdowns` | `ForecastBreakdownOptions` | Breakdown time windows (`timeWindows: DateTime[]`) and targets (`targets: ForecastBreakdownTarget[]`). |

### ProspectiveLineItem
| Field | Type | Description |
|-------|------|-------------|
| `lineItem` | `LineItem` | The target of the forecast (`LineItem` object). |
| `proposalLineItem` | `ProposalLineItem` | Alternatively, a `ProposalLineItem` object. |
| `advertiserId` | `long` | Optional advertiser ID for competitive exclusion simulation. |

### TrafficDataRequest / TrafficDataResponse
- `TrafficDataRequest`: `targeting` (`Targeting`), `requestedDateRange` (`DateRange`)
- `TrafficDataResponse`: `historicalTimeSeries` (`TimeSeries`: `timeSeriesDateRange`, `values: long[]`), `forecastedTimeSeries` (`TimeSeries`), `overallDateRange` (`DateRange`)
