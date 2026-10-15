# ProposalLineItemService Reference

**Service**: ProposalLineItemService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/ProposalLineItemService
**Types**: 6

## Methods

### createMakegoods
- **Request**: `ProposalLineItemMakegoodInfo[] makegoodInfoList`
- **Response**: `ProposalLineItem[]`

### createProposalLineItems
- **Request**: `ProposalLineItem[] proposalLineItems`
- **Response**: `ProposalLineItem[]`

### getProposalLineItemsByStatement
- **Request**: `Statement filterStatement` (PQL filterable: `id`, `name`, `proposalId`, `isArchived`, `lastModifiedDateTime`, `useThirdPartyAdServerFromProposal`, `dfpLineItemId`)
- **Response**: `ProposalLineItemPage`

### performProposalLineItemAction
- **Request**: `ProposalLineItemAction proposalLineItemAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateProposalLineItems
- **Request**: `ProposalLineItem[] proposalLineItems`
- **Response**: `ProposalLineItem[]`

## Types

### ProposalLineItem

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the `ProposalLineItem`. This attribute is read-only. |
| `proposalId` | `long` | The unique ID of the `Proposal`, to which the `ProposalLineItem` belongs. This attribute is required for creation and then is readonly. |
| `name` | `string` | The name of the `ProposalLineItem` which should be unique under the same `Proposal`. This attribute is required and has a maximum length of 255 characters. |
| `startDateTime` | `DateTime` | The date and time at which the line item associated with the `ProposalLineItem` is enabled to begin serving. |
| `endDateTime` | `DateTime` | The date and time at which the line item associated with the `ProposalLineItem` stops serving. |
| `timeZoneId` | `string` | The time zone ID in tz database format (e.g. `'Asia/Hong_Kong'`) for this `ProposalLineItem`. |
| `internalNotes` | `string` | Provides any additional notes that may annotate the `ProposalLineItem`. |
| `isArchived` | `boolean` | The archival status of the `ProposalLineItem`. This attribute is read-only. |
| `goal` | `Goal` | The goal (impressions/percentage) for this `ProposalLineItem`. This attribute is required. |
| `secondaryGoals` | `Goal[]` | The secondary goals that this `ProposalLineItem` is associated with. |
| `contractedUnitsBought` | `long` | The contracted number of impressions or clicks. |
| `deliveryRateType` | `DeliveryRateType` | The strategy for delivering ads over the course of the `ProposalLineItem`'s duration. |
| `roadblockingType` | `RoadblockingType` | The strategy for serving roadblocked creatives. |
| `companionDeliveryOption` | `CompanionDeliveryOption` | The delivery option for companions. |
| `videoMaxDuration` | `long` | The max duration of a video creative associated with this `ProposalLineItem` in milliseconds. |
| `frequencyCaps` | `FrequencyCap[]` | The set of frequency capping units for this `ProposalLineItem`. |
| `dfpLineItemId` | `long` | The unique ID of corresponding `LineItem`. This will be `null` if the `Proposal` has not been pushed to DFP. This attribute is read-only. |
| `lineItemType` | `LineItemType` | The corresponding `LineItemType` of the `ProposalLineItem` (e.g. `STANDARD`, `SPONSORSHIP`, `PREFERRED_DEAL`). |
| `rateType` | `RateType` | The method used for billing the `ProposalLineItem` (`CPM`, `CPD`, `VCPM`). |
| `netRate` | `Money` | The cost per unit (net rate) of the `ProposalLineItem`. |
| `netCost` | `Money` | The net cost of the `ProposalLineItem`. |
| `deliveryIndicator` | `DeliveryIndicator` | Indicates how well the line item synced with this proposal line item has been performing. Read-only. |
| `deliveryData` | `DeliveryData` | Delivery data provides the number of clicks or impressions delivered in the last 7 days. Read-only. |
| `computedStatus` | `ComputedStatus` | The status of the synced `LineItem`. Read-only. |
| `lastModifiedDateTime` | `DateTime` | The date and time this `ProposalLineItem` was last modified. Read-only. |
| `reservationStatus` | `ReservationStatus` | The reservation status of the `ProposalLineItem`. Read-only. |
| `targeting` | `Targeting` | Contains the targeting criteria for the `ProposalLineItem`. |
| `creativePlaceholders` | `CreativePlaceholder[]` | Details about the creatives that are expected to serve through this `ProposalLineItem`. |
| `environmentType` | `EnvironmentType` | The environment that the `ProposalLineItem` is targeting (`BROWSER` or `VIDEO_PLAYER`). |
| `marketplaceInfo` | `ProposalLineItemMarketplaceInfo` | Marketplace info if programmatic. |

### ProposalLineItemPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `ProposalLineItem[]` | The collection of proposal line items contained within this page. |

### ProposalLineItemMakegoodInfo

| Field | Type | Description |
|-------|------|-------------|
| `originalProposalLineItemId` | `long` | The ID of the original proposal line item on which this makegood is based. |
| `reason` | `string` | The publisher-provided reason why this makegood was initiated. |

## Enumerations

### RateType

| Value | Description |
|-------|-------------|
| `CPM` | Cost per thousand impressions. |
| `CPD` | Cost per day. |
| `VCPM` | Active View cost per thousand viewable impressions. |
| `CPM_IN_TARGET` | Cost per thousand in-target impressions. |
| `UNKNOWN` | Unknown rate type. |

### ReservationStatus

| Value | Description |
|-------|-------------|
| `RESERVED` | The inventory is reserved. |
| `NOT_RESERVED` | The proposal line item's inventory is not reserved. |
| `RELEASED` | Once the proposal line item's inventory is released, it will reach this status. |
| `CHECK_LINE_ITEM_RESERVATION_STATUS` | The reservation status is managed by the corresponding `LineItem`. |
| `UNKNOWN` | Unknown status. |
