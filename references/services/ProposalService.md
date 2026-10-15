# ProposalService Reference

**Service**: ProposalService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/ProposalService
**Types**: 8

## Methods

### createProposals
- **Request**: `Proposal[] proposals`
- **Response**: `Proposal[]`

### getMarketplaceCommentsByStatement
- **Request**: `Statement filterStatement` (PQL filterable: `proposalId`)
- **Response**: `MarketplaceCommentPage`

### getProposalsByStatement
- **Request**: `Statement filterStatement` (PQL filterable: `id`, `dfpOrderId`, `name`, `status`, `isArchived`, `startDateTime`, `endDateTime`, `lastModifiedDateTime`, `negotiationStatus`)
- **Response**: `ProposalPage`

### performProposalAction
- **Request**: `ProposalAction proposalAction`, `Statement filterStatement`
- **Response**: `UpdateResult`

### updateProposals
- **Request**: `Proposal[] proposals`
- **Response**: `Proposal[]`

## Types

### Proposal

| Field | Type | Description |
|-------|------|-------------|
| `id` | `long` | The unique ID of the `Proposal`. This attribute is read-only. |
| `isProgrammatic` | `boolean` | Whether the proposal is for programmatic trafficking. |
| `dfpOrderId` | `long` | The unique ID of corresponding `Order`. This will be `null` if the `Proposal` has not been pushed to DFP. This attribute is read-only. |
| `name` | `string` | The name of the `Proposal`. This value is required and has a maximum length of 255 characters. |
| `startDateTime` | `DateTime` | The date and time at which the order and line items associated with the `Proposal` are eligible to begin serving. This attribute is read-only and is derived from the proposal line items. |
| `endDateTime` | `DateTime` | The date and time at which the order and line items associated with the `Proposal` stop serving. This attribute is read-only and is derived from the proposal line items. |
| `status` | `ProposalStatus` | The status of the `Proposal`. This attribute is read-only. |
| `isArchived` | `boolean` |The archival status of the `Proposal`. This attribute is read-only. |
| `advertiser` | `ProposalCompanyAssociation` | The advertiser, to which this `Proposal` belongs, and a set ofContact objects associated with the advertiser. |
| `agencies` | `ProposalCompanyAssociation[]` | List of agencies and the set of Contact objects associated with each agency. |
| `internalNotes` | `string` | Provides any additional notes that may annotate the `Proposal`. This attribute is optional and has a maximum length of 65,535 characters. |
| `primarySalesperson` | `SalespersonSplit` | The primary salesperson who brokered the transaction with the advertiser. |
| `salesPlannerIds` | `long[]` | List of unique IDs of `User` objects who are the sales planners of the `Proposal`. |
| `primaryTraffickerId` | `long` | The unique ID of the `User` who is primary trafficker and is responsible for trafficking the `Proposal`. |
| `sellerContactIds` | `long[]` | The unique IDs of the `User` objects who are the seller contacts of the `Proposal`. |
| `appliedTeamIds` | `long[]` | The IDs of all teams that the `Proposal` is on directly. |
| `customFieldValues` | `BaseCustomFieldValue[]` | The values of the custom fields associated with the `Proposal`. |
| `appliedLabels` | `AppliedLabel[]` | The set of labels applied directly to the `Proposal`. |
| `effectiveAppliedLabels` | `AppliedLabel[]` | Contains the set of labels applied directly to the proposal as well as those inherited from the advertiser. |
| `currencyCode` | `string` | The currency code of this `Proposal` (e.g. `'HKD'`, `'USD'`). |
| `isSold` | `boolean` | Indicates whether the proposal has been sold (i.e., corresponds to an DFP `Order`). This attribute is read-only. |
| `approvalStatus` | `ProposalApprovalStatus` | The approval status of the `Proposal` for the active user. This attribute is read-only. |
| `lastModifiedDateTime` | `DateTime` | The date and time this `Proposal` was last modified. This attribute is read-only. |
| `marketplaceInfo` | `ProposalMarketplaceInfo` | The marketplace info of this proposal if it has a corresponding order in Marketplace. |
| `buyerRfp` | `BuyerRfp` | Buyer RFP associated with this `Proposal`. |
| `hasBuyerRfp` | `boolean` | Whether a `Proposal` contains a `BuyerRfp` field. |
| `deliveryPausingEnabled` | `boolean` | Whether pausing is consented for the `Proposal`. |

### ProposalPage

| Field | Type | Description |
|-------|------|-------------|
| `totalResultSetSize` | `int` | The size of the total result set to which this page belongs. |
| `startIndex` | `int` | The absolute index in the total result set on which this page begins. |
| `results` | `Proposal[]` | The collection of proposals contained within this page. |

### ProposalCompanyAssociation

| Field | Type | Description |
|-------|------|-------------|
| `companyId` | `long` | The unique ID of the `Company` associated with the `Proposal`. |
| `type` | `ProposalCompanyAssociationType` | The association type of the `Company` and `Proposal`. |
| `contactIds` | `long[]` | List of unique IDs of `Contact` objects of the `Company`. |

### MarketplaceComment

| Field | Type | Description |
|-------|------|-------------|
| `proposalId` | `long` | The unique ID of the `Proposal` the comment belongs to. |
| `comment` | `string` | The comment text. |
| `creationTime` | `DateTime` | The creation `DateTime` of this `MarketplaceComment`. |
| `createdBySeller` | `boolean` | Indicates whether the `MarketplaceComment` was created by seller. |

### ProposalAction (Subclasses)
- `ArchiveProposals`, `UnarchiveProposals`, `CancelProposalsForNegotiation`, `RequestBuyerAcceptance`, `RequestBuyerReview`, `ReserveProposals`, `SubmitProposalsForApproval`, `SubmitProposalsForArchival`, `BypassProposalWorkflowRules`, `EditProposalsForNegotiation`, `TerminateNegotiations`, `UpdateOrderWithSellerData`

## Enumerations

### ProposalStatus

| Value | Description |
|-------|-------------|
| `DRAFT` | The proposal is new and under creation/negotiation. |
| `PENDING_APPROVAL` | The proposal has been submitted for approval. |
| `APPROVED` | The proposal has been approved and is ready to serve. |
| `ARCHIVED` | The proposal has been archived. |
| `UNKNOWN` | The value returned if the actual value is not exposed by the requested API version. |

### NegotiationStatus

| Value | Description |
|-------|-------------|
| `BUYER_INITIATED` | Indicates that a new proposal was created by the buyer. |
| `SELLER_INITIATED` | Indicates that a new proposal was created by the seller. |
| `AWAITING_BUYER_REVIEW` | Indicates that a proposal is awaiting buyer's action. |
| `AWAITING_SELLER_REVIEW` | Indicates that a proposal is awaiting seller's action. |
| `ONLY_SELLER_ACCEPTED` | Indicates that the seller has accepted the proposal and is awaiting the buyer's acceptance. |
| `FINALIZED` | Indicates that the proposal has been finalized by both buyer and seller. |
| `CANCELLED` | Indicates that the negotiation for the proposal has been cancelled. |
| `UNKNOWN` | Unknown status. |
