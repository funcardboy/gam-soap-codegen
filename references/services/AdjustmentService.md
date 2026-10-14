# AdjustmentService Cheatsheet

## Methods

### calculateDailyAdOpportunityCounts
Takes a prospective forecast adjustment and calculates the daily ad opportunity counts
corresponding to its provided volume settings.

### createForecastAdjustments
Creates new [ForecastAdjustment](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment) objects.

### createTrafficForecastSegments
Creates new [TrafficForecastSegment](/ad-manager/api/reference/v202608/AdjustmentService.TrafficForecastSegment) objects.

### getForecastAdjustmentsByStatement
Gets a [ForecastAdjustmentPage](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustmentPage) of [ForecastAdjustment](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment) objects that satisfy
the given [Statement.query](/ad-manager/api/reference/v202608/AdjustmentService.Statement#query).
The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [ForecastAdjustment.id](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment#id) |
| `trafficForecastSegmentId` | [ForecastAdjustment.trafficForecastSegmentId](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment#trafficForecastSegmentId) |
| `name` | [ForecastAdjustment.name](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment#name) |
| `startDate` | [ForecastAdjustment.startDate](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment#startDate) |
| `endDate` | [ForecastAdjustment.endDate](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment#endDate) |
| `status` | [ForecastAdjustment.status](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment#status) |

### getTrafficForecastSegmentsByStatement
Gets a [TrafficForecastSegmentPage](/ad-manager/api/reference/v202608/AdjustmentService.TrafficForecastSegmentPage) of [TrafficForecastSegment](/ad-manager/api/reference/v202608/AdjustmentService.TrafficForecastSegment) objects that
satisfy the given [Statement.query](/ad-manager/api/reference/v202608/AdjustmentService.Statement#query).
The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [TrafficForecastSegment.id](/ad-manager/api/reference/v202608/AdjustmentService.TrafficForecastSegment#id) |
| `name` | [TrafficForecastSegment.name](/ad-manager/api/reference/v202608/AdjustmentService.TrafficForecastSegment#name) |
| `creationTime` | [TrafficForecastSegment.creationTime](/ad-manager/api/reference/v202608/AdjustmentService.TrafficForecastSegment#creationTime) |

### performForecastAdjustmentAction
Performs actions on [ForecastAdjustment](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/AdjustmentService.Statement#query).

### updateForecastAdjustments
Updates the specified [ForecastAdjustment](/ad-manager/api/reference/v202608/AdjustmentService.ForecastAdjustment) objects.

### updateTrafficForecastSegments
Updates the specified [TrafficForecastSegment](/ad-manager/api/reference/v202608/AdjustmentService.TrafficForecastSegment) objects.
