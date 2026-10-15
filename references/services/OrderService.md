# OrderService Reference

**Service**: OrderService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/OrderService
**Types**: 6

## Methods

### createOrders
- **Request**: `Order[] orders`
- **Response**: `Order[]`

### getOrdersByStatement
- **Request**: `Statement filterStatement` (PQL filterable fields: `id`, `name`, `status`, `advertiserId`, `agencyId`, `salespersonId`, `traffickerId`, `startDateTime`, `endDateTime`, `lastModifiedDateTime`, `isArchived`, `externalOrderId`)
- **Response**: `OrderPage`

### performOrderAction
- **Request**: `OrderAction orderAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateOrders
- **Request**: `Order[] orders`
- **Response**: `Order[]`

## Types

### Order

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | Uniquely identifies the `Order`. Read-only, assigned by Google on creation. |
| `name` | `string` | The name of the `Order`. Required, maximum length 255 characters. |
| `startDateTime` | `DateTime` | The date and time at which the `Order` is enabled to begin serving. Read-only (derived from its LineItems). |
| `endDateTime` | `DateTime` | The date and time at which the `Order` will stop serving. Read-only (derived from its LineItems). |
| `unlimitedEndDateTime` | `boolean` | Specifies whether or not the `Order` has an unlimited end DateTime. Read-only. |
| `status` | `OrderStatus` | The status of the `Order`. Read-only. |
| `isArchived` | `boolean` | The archival status of the `Order`. Read-only. |
| `notes` | `string` | Provides any additional notes that may annotate the `Order`. Optional, max 65,535 characters. |
| `externalOrderId` | `int` | An arbitrary ID to associate to the `Order`, used as a reference to an external system. |
| `poNumber` | `string` | The purchase order number for the `Order`. Optional, max 63 characters. |
| `currencyCode` | `string` | The ISO currency code for the `Order` (e.g. `'HKD'`, `'USD'`). Defaults to network currency. |
| `advertiserId` | `long` | The unique ID of the `Company` (`Company.Type.ADVERTISER`) to which this order belongs. Required. |
| `advertiserContactIds` | `long[]` | List of IDs for advertiser `Contact` objects associated with this order. |
| `agencyId` | `long` | The unique ID of the `Company` (`Company.Type.AGENCY`) associated with this order. Optional. |
| `agencyContactIds` | `long[]` | List of IDs for agency `Contact` objects associated with this order. |
| `creatorId` | `long` | The unique ID of the `User` who created the `Order`. Read-only. |
| `traffickerId` | `long` | The unique ID of the `User` responsible for trafficking the `Order`. Required. |
| `secondaryTraffickerIds` | `long[]` | The IDs of the secondary traffickers (`User` objects) associated with the order. |
| `salespersonId` | `long` | The unique ID of the `User` responsible for the sales of the `Order`. |
| `secondarySalespersonIds` | `long[]` | The IDs of the secondary salespeople (`User` objects) associated with the order. |
| `totalImpressionsDelivered` | `long` | Total impressions delivered for all line items in this `Order`. Read-only. |
| `totalClicksDelivered` | `long` | Total clicks delivered for all line items in this `Order`. Read-only. |
| `totalViewableImpressionsDelivered` | `long` | Total Active View viewable impressions delivered for all line items in this `Order`. Read-only. |
| `totalBudget` | `Money` | Total budget (`microAmount`) for all line items in this `Order`. Read-only. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied directly to this order. |
| `effectiveAppliedLabels` | `AppliedLabel[]` | Labels applied directly plus inherited from advertiser. Read-only. |
| `lastModifiedByApp` | `string` | The application that last modified this order. Read-only. |
| `isProgrammatic` | `boolean` | Indicates whether this order is a programmatic order. |
| `appliedTeamIds` | `long[]` | The IDs of all teams that this order is on directly. |
| `lastModifiedDateTime` | `DateTime` | The date and time this order was last modified. Read-only. |
| `customFieldValues` | `BaseCustomFieldValue[]` | Values of custom fields associated with this order. |

### OrderPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `Order[]` | The collection of orders contained within this page. |

### OrderAction (Subclasses)
- `ApproveOrders`, `ApproveOrdersWithoutReservationChanges`, `ArchiveOrders`, `DeleteOrders`, `DisapproveOrders`, `DisapproveOrdersWithoutReservationChanges`, `PauseOrders`, `ResumeOrders`, `RetractOrders`, `RetractOrdersWithoutReservationChanges`, `SubmitOrdersForApproval`, `SubmitOrdersForApprovalWithoutReservationChanges`, `UnarchiveOrders`

## Enumerations

### OrderStatus

| Value | Description |
|-------|-------------|
| `DRAFT` | Indicates that the `Order` has just been created but no approval has been requested yet. |
| `PENDING_APPROVAL` | Indicates that a request for approval for the `Order` has been made. |
| `APPROVED` | Indicates that the `Order` has been approved and is ready to serve. |
| `DISAPPROVED` | Indicates that the `Order` has been disapproved and is not eligible to serve. |
| `PAUSED` | This is a legacy state. Paused status should be checked on `LineItem`s. |
| `CANCELED` | Indicates that the `Order` has been canceled and cannot serve. |
| `DELETED` | Indicates that the `Order` has been deleted by DSM. |
| `UNKNOWN` | The value returned if the actual value is not exposed by the requested API version. |
