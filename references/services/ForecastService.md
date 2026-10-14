# ForecastService Cheatsheet

## Methods

### getAvailabilityForecast
Gets the availability forecast for a [ProspectiveLineItem](/ad-manager/api/reference/v202608/ForecastService.ProspectiveLineItem). An availability forecast
reports the maximum number of available units that the line item can book, and the total number
of units matching the line item's targeting.

### getAvailabilityForecastById
Gets an [AvailabilityForecast](/ad-manager/api/reference/v202608/ForecastService.AvailabilityForecast) for an existing [LineItem](/ad-manager/api/reference/v202608/ForecastService.LineItem) object. An availability
forecast reports the maximum number of available units that the
line item can be booked with, and also the total number of units
matching the line item's targeting.
Only line items having type [LineItemType.SPONSORSHIP](/ad-manager/api/reference/v202608/ForecastService.LineItemType#SPONSORSHIP) or [LineItemType.STANDARD](/ad-manager/api/reference/v202608/ForecastService.LineItemType#STANDARD) are valid.
Other types will result in [ReservationDetailsError.Reason.LINE\_ITEM\_TYPE\_NOT\_ALLOWED](/ad-manager/api/reference/v202608/ForecastService.ReservationDetailsError.Reason#LINE_ITEM_TYPE_NOT_ALLOWED).

### getDeliveryForecast
Gets the delivery forecast for a list of [ProspectiveLineItem](/ad-manager/api/reference/v202608/ForecastService.ProspectiveLineItem) objects in a single
delivery simulation with line items potentially contending with each other. A delivery forecast
reports the number of units that will be delivered to each line item given the line item goals
and contentions from other line items.

### getDeliveryForecastByIds
Gets the delivery forecast for a list of existing [LineItem](/ad-manager/api/reference/v202608/ForecastService.LineItem) objects in a single delivery
simulation. A delivery forecast reports the number of units that will be delivered to each line
item given the line item goals and contentions from other line items.

### getTrafficData
Returns forecasted and historical traffic data for the segment of
traffic specified by the provided request.
Calling this endpoint programmatically is only available for Ad
Manager 360 networks.
