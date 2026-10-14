# OrderService Cheatsheet

## Methods

### createOrders
Creates new [Order](/ad-manager/api/reference/v202608/OrderService.Order) objects.

### getOrdersByStatement
Gets an [OrderPage](/ad-manager/api/reference/v202608/OrderService.OrderPage) of [Order](/ad-manager/api/reference/v202608/OrderService.Order) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/OrderService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `advertiserId` | [Order.advertiserId](/ad-manager/api/reference/v202608/OrderService.Order#advertiserId) |
| `endDateTime` | [Order.endDateTime](/ad-manager/api/reference/v202608/OrderService.Order#endDateTime) |
| `id` | [Order.id](/ad-manager/api/reference/v202608/OrderService.Order#id) |
| `name` | [Order.name](/ad-manager/api/reference/v202608/OrderService.Order#name) |
| `salespersonId` | [Order.salespersonId](/ad-manager/api/reference/v202608/OrderService.Order#salespersonId) |
| `startDateTime` | [Order.startDateTime](/ad-manager/api/reference/v202608/OrderService.Order#startDateTime) |
| `status` | [Order.status](/ad-manager/api/reference/v202608/OrderService.Order#status) |
| `traffickerId` | [Order.traffickerId](/ad-manager/api/reference/v202608/OrderService.Order#traffickerId) |
| `lastModifiedDateTime` | [Order.lastModifiedDateTime](/ad-manager/api/reference/v202608/OrderService.Order#lastModifiedDateTime) |

### performOrderAction
Performs actions on [Order](/ad-manager/api/reference/v202608/OrderService.Order) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/OrderService.Statement#query).

### updateOrders
Updates the specified [Order](/ad-manager/api/reference/v202608/OrderService.Order) objects.

## Types

### Order
| Field | Type | Description |
|-------|------|-------------|
| `id` | long | Unique identifier |
| `name` | string | Order name |
| `advertiserId` | long | Advertiser company ID |
| `traffickerIds` | long[] | List of trafficker user IDs |
| `salespersonId` | long | Salesperson user ID |
| `status` | OrderStatus | Order status |
| `startDate` | Date | Start date (yyyy-mm-dd) |
| `endDate` | Date | End date (yyyy-mm-dd) |
| `totalBudget` | Money | Total budget |
| `currencyCode` | string | ISO 4217 currency |
| `lastModifiedDateTime` | DateTime | Last modification time |
| `appliedLabels` | AppliedLabel[] | Applied labels |

### OrderPage
| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | int | Total matching orders |
| `startIndex` | int | Index of first result |
| `results` | Order[] | Page of orders |

## Enumerations

### OrderStatus
| Value | Description |
|-------|-------------|
| `DRAFT` | |
| `PENDING_APPROVAL` | |
| `APPROVED` | |
| `PAUSED` | |
| `CANCELLED` | |
| `ARCHIVED` | |

