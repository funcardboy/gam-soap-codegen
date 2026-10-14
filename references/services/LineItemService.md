# LineItemService Cheatsheet

## Methods

### createLineItems
Creates new [LineItem](/ad-manager/api/reference/v202608/LineItemService.LineItem) objects.

### getLineItemsByStatement
Gets a [LineItemPage](/ad-manager/api/reference/v202608/LineItemService.LineItemPage) of [LineItem](/ad-manager/api/reference/v202608/LineItemService.LineItem) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/LineItemService.Statement#query). The following fields are supported for filtering:
| PQL property | Entity property |
| --- | --- |
| `CostType` | [LineItem.costType](/ad-manager/api/reference/v202608/LineItemService.LineItem#costType) |
| `CreationDateTime` | [LineItem.creationDateTime](/ad-manager/api/reference/v202608/LineItemService.LineItem#creationDateTime) |
| `DeliveryRateType` | [LineItem.deliveryRateType](/ad-manager/api/reference/v202608/LineItemService.LineItem#deliveryRateType) |
| `EndDateTime` | [LineItem.endDateTime](/ad-manager/api/reference/v202608/LineItemService.LineItem#endDateTime) |
| `ExternalId` | [LineItem.externalId](/ad-manager/api/reference/v202608/LineItemService.LineItem#externalId) |
| `Id` | [LineItem.id](/ad-manager/api/reference/v202608/LineItemService.LineItem#id) |
| `IsMissingCreatives` | [LineItem.isMissingCreatives](/ad-manager/api/reference/v202608/LineItemService.LineItem#isMissingCreatives) |
| `IsSetTopBoxEnabled` | [LineItem.isSetTopBoxEnabled](/ad-manager/api/reference/v202608/LineItemService.LineItem#isSetTopBoxEnabled) |
| `LastModifiedDateTime` | [LineItem.lastModifiedDateTime](/ad-manager/api/reference/v202608/LineItemService.LineItem#lastModifiedDateTime) |
| `LineItemType` | [LineItem.lineItemType](/ad-manager/api/reference/v202608/LineItemService.LineItem#lineItemType) |
| `Name` | [LineItem.name](/ad-manager/api/reference/v202608/LineItemService.LineItem#name) |
| `OrderId` | [LineItem.orderId](/ad-manager/api/reference/v202608/LineItemService.LineItem#orderId) |
| `StartDateTime` | [LineItem.startDateTime](/ad-manager/api/reference/v202608/LineItemService.LineItem#startDateTime) |
| `Status` | [LineItem.status](/ad-manager/api/reference/v202608/LineItemService.LineItem#status) |
| `UnitsBought` | [LineItem.unitsBought](/ad-manager/api/reference/v202608/LineItemService.LineItem#unitsBought) |

### performLineItemAction
Performs actions on [LineItem](/ad-manager/api/reference/v202608/LineItemService.LineItem) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/LineItemService.Statement#query).

### updateLineItems
Updates the specified [LineItem](/ad-manager/api/reference/v202608/LineItemService.LineItem) objects.

## Enumerations

### ComputedStatus
| Value | Description |
|-------|-------------|
| `DRAFT` | |
| `INACTIVE` | |
| `PENDING_APPROVAL` | |
| `APPROVED` | |
| `NEEDS_REVIEW` | |
| `PAUSED` | |
| `PROCESSING` | |
| `ACTIVE` | |
| `DISAPPROVED` | |
| `WAITING_FOR_CREATIVE` | |
| `COMPLETED` | |
| `ARCHIVED` | |
| `CANCELLED` | |
| `EXPIRED` | |
| `DELIVERING` | |
| `PAST_END_DATE` | |


### LineItemType
| Value | Description |
|-------|-------------|
| `STANDARD` | |
| `PREMIUM` | |
| `FIXED_PRICE` | |
| `HOUSE` | |
| `CLICK_TRACKING` | |
| `BRAND_MANAGEMENT` | |


### CostType
| Value | Description |
|-------|-------------|
| `CPM` | |
| `CPC` | |
| `CPS` | |
| `CPA` | |
| `UNKNOWN` | |


### StartDateTimeType
| Value | Description |
|-------|-------------|
| `USE_START_DATE_TIME` | |
| `IMMEDIATELY` | |


### EnvironmentType
| Value | Description |
|-------|-------------|
| `SERVING` | |
| `PAUSED` | |
| `INACTIVE` | |


### CreativeRotationType
| Value | Description |
|-------|-------------|
| `SEQUENTIAL` | |
| `WEIGHTED_RANDOM` | |


### TargetingUnitType
| Value | Description |
|-------|-------------|
| `CUSTOM` | |
| `INVENTORY` | |


### ReservationType
| Value | Description |
|-------|-------------|
| `RESERVATION` | |
| `NON_GUARANTEED` | |


### CostPerUnitType
| Value | Description |
|-------|-------------|
| `CPM` | |
| `CPC` | |
| `CPS` | |


### CreativeSizePolicy
| Value | Description |
|-------|-------------|
| `IGNORE` | |
| `DISAPPROVED` | |
| `REQUIRE_ONE_SIZE` | |

