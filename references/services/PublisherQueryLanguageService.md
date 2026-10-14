# PublisherQueryLanguageService Cheatsheet

## Methods

### Geo\_Target
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the Geo target |
| Name | The name of the Geo target |
| CanonicalParentId | The criteria ID of the direct parent that defines the canonical name of the geo target. For example, if the current geo target is "San Francisco", its canonical name would be "San Francisco, California, United States" thus the canonicalParentId would be the criteria ID of California and the canonicalParentId of California would be the criteria ID of United states |
| ParentIds | A comma separated list of criteria IDs of all parents of the geo target ordered by ascending size |
| CountryCode | Country code as defined by ISO 3166-1 alpha-2 |
| Type | Allowable values:  * Airport * Autonomous\_Community * Canton * City * Congressional\_District * Country * County * Department * DMA\_Region * Governorate * Municipality * Neighborhood * Postal\_Code * Prefecture * Province * Region * State * Territory * Tv\_Region * Union\_Territory |
| Targetable | Indicates whether geographical targeting is allowed |

### Bandwidth\_Group
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the bandwidth group |
| BandwidthName | Name of the bandwidth group |

### Browser
Note: this table only contains browsers that are available in
the Ad Manager UI targeting picker.
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the browser |
| BrowserName | Name of the browser |
| MajorVersion | Major version of the browser |
| MinorVersion | Minor version of the browser |

### Browser\_Language
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the browser language |
| BrowserLanguageName | Browser's language |

### Device\_Capability
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the device capability |
| DeviceCapabilityName | Name of the device capability |

### Device\_Category
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the device category |
| DeviceCategoryName | Name of the device category |

### Device\_Manufacturer
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the device manufacturer |
| MobileDeviceManufacturerName | Name of the device manufacturer |

### Mobile\_Carrier
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the mobile carrier |
| CountryCode | The country code of the mobile carrier |
| MobileCarrierName | Name of the mobile carrier |

### Mobile\_Device
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the mobile device |
| MobileDeviceManufacturerId | Id of the device manufacturer |
| MobileDeviceName | Name of the mobile device |

### Mobile\_Device\_Submodel
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the mobile device submodel |
| MobileDeviceId | Id of the mobile device |
| MobileDeviceSubmodelName | Name of the mobile device submodel |

### Operating\_System
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the operating system |
| OperatingSystemName | Name of the operating system |

### Operating\_System\_Version
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the operating system version |
| OperatingSystemId | Id of the operating system |
| MajorVersion | The operating system major version |
| MinorVersion | The operating system minor version |
| MicroVersion | The operating system micro version |

### Third\_Party\_Company
| Column Name | Description |
| --- | --- |
| Id | Unique identifier for the third party company |
| Name | The third party company name |
| Type | The third party company type |
| Status | The status of the third party company |

### Line\_Item
| Column name | Type | Description |
| --- | --- | --- |
| CostType | `Text` | The method used for billing this `LineItem`. |
| CreationDateTime | `Datetime` | The date and time this `LineItem` was last created. This attribute may be null for `LineItem`s created before this feature was introduced. |
| DeliveryRateType | `Text` | The strategy for delivering ads over the course of the `LineItem`'s duration. This attribute is optional and defaults to [DeliveryRateType.EVENLY](/ad-manager/api/reference/v202608/ForecastService.DeliveryRateType#EVENLY). Starting in v201306, it may default to [DeliveryRateType.FRONTLOADED](/ad-manager/api/reference/v202608/ForecastService.DeliveryRateType#FRONTLOADED) if specifically configured to on the network. |
| ExternalId | `Text` | An identifier for the `LineItem` that is meaningful to the publisher. |
| Id | `Number` | Uniquely identifies the `LineItem`. This attribute is read-only and is assigned by Google when a line item is created. |
| IsMissingCreatives | `Boolean` | Indicates if a `LineItem` is missing any [creatives](/ad-manager/api/reference/v202608/CreativeService.Creative) for the `creativePlaceholders` specified. |
| IsSetTopBoxEnabled | `Boolean` | Whether or not this line item is set-top box enabled. |
| LastModifiedDateTime | `Datetime` | The date and time this `LineItem` was last modified. |
| LatestNielsenInTargetRatioMilliPercent | `Number` | The most recently computed in-target ratio measured from Nielsen reporting data and the `LineItem`'s settings. It's provided in milli percent, or null if not applicable. |
| LineItemType | `Text` | Indicates the line item type of a `LineItem`. |
| Name | `Text` | The name of the `LineItem`. |
| OrderId | `Number` | The ID of the [Order](/ad-manager/api/reference/v202608/OrderService.Order) to which the `LineItem` belongs. |
| ServingEndTime | `Datetime` | The date and time on which the `LineItem` stops serving, inclusive of any grace period. |
| StartDateTime | `Datetime` | The date and time on which the `LineItem` is enabled to begin serving. |
| Status | `Text` | The status of the `LineItem`. |
| Targeting | `Targeting` | The targeting criteria for the ad campaign. |
| UnitsBought | `Number` | The total number of impressions or clicks that will be reserved for the `LineItem`. If the line item is of type [LineItemType.SPONSORSHIP](/ad-manager/api/reference/v202608/AdRuleService.LineItemType#SPONSORSHIP), then it represents the percentage of available impressions reserved. |

### Ad\_Unit
| Column name | Type | Description |
| --- | --- | --- |
| AdUnitCode | `Text` | A string used to uniquely identify the ad unit for the purposes of serving the ad. This attribute is read-only and is assigned by Google when an ad unit is created. |
| ExternalSetTopBoxChannelId | `Text` | The channel ID for set-top box enabled [ad units](/ad-manager/api/reference/v202608/InventoryService.AdUnit). |
| Id | `Number` | Uniquely identifies the ad unit. This value is read-only and is assigned by Google when an ad unit is created. |
| LastModifiedDateTime | `Datetime` | The date and time this ad unit was last modified. |
| Name | `Text` | The name of the ad unit. |
| ParentId | `Number` | The ID of the ad unit's parent. Every ad unit has a parent except for the root ad unit, which is created by Google. |

### User
| Column name | Type | Description |
| --- | --- | --- |
| Email | `Text` | The email or login of the user. |
| ExternalId | `Text` | An identifier for the user that is meaningful to the publisher. |
| Id | `Number` | The unique ID of the user. |
| IsServiceAccount | `Boolean` | True if this user is an OAuth2 service account user, false otherwise. |
| Name | `Text` | The name of the user. |
| RoleId | `Number` | The unique role ID of the user. [Role](/ad-manager/api/reference/v202608/UserService.Role) objects that are created by Google will have negative IDs. |
| RoleName | `Text` | The name of the [Role](/ad-manager/api/reference/v202608/UserService.Role) assigned to the user. |

### Programmatic\_Buyer
| Column name | Type | Description |
| --- | --- | --- |
| BuyerAccountId | `Number` | The ID used by Authorized Buyers to bill the appropriate buyer network for a programmatic order. |
| EnabledForPreferredDeals | `Boolean` | Whether the buyer is allowed to negotiate Preferred Deals. |
| EnabledForProgrammaticGuaranteed | `Boolean` | Whether the buyer is enabled for Programmatic Guaranteed deals. |
| IsAgency | `Boolean` | Whether the buyer is an advertising agency. |
| Name | `Text` | Display name that references the buyer. |
| ParentId | `Number` | The ID of the programmatic buyer's sponsor. If the programmatic buyer has no sponsor, this field will be -1. |
| PartnerClientId | `Text` | ID used to represent Display & Video 360 client buyer partner ID (if Display & Video 360) or Authorized Buyers client buyer account ID. |

### Audience\_Segment\_Category
| Column name | Type | Description |
| --- | --- | --- |
| Id | `Number` | The unique identifier for the audience segment category. |
| Name | `Text` | The name of the audience segment category. |
| ParentId | `Number` | The unique identifier of the audience segment category's parent. |

### Audience\_Segment
| Column name | Type | Description |
| --- | --- | --- |
| AdIdSize | `Number` | The number of AdID users in the segment. |
| CategoryIds | `Set of number` | The ids of the categories that this audience segment belongs to. |
| Id | `Number` | The unique identifier for the audience segment. |
| IdfaSize | `Number` | The number of IDFA users in the segment. |
| MobileWebSize | `Number` | The number of mobile web users in the segment. |
| Name | `Text` | The name of the audience segment. |
| OwnerAccountId | `Number` | The owner account id of the audience segment. |
| OwnerName | `Text` | The owner name of the audience segment. |
| PpidSize | `Number` | The number of PPID users in the segment. |
| SegmentType | `Text` | The type of the audience segment. |

### Time\_Zone
| Column name | Type | Description |
| --- | --- | --- |
| Id | `Text` | The id of time zone in the form of `America/New_York`. |
| StandardGmtOffset | `Text` | The standard GMT offset in current time in the form of `GMT-05:00` for `America/New_York`, excluding the Daylight Saving Time. |

### Proposal\_Terms\_And\_Conditions
| Column name | Type | Description |
| --- | --- | --- |

### Change\_History
Restrictions: Only ordering by `ChangeDateTime` descending is supported. The
`IN` operator is only supported on
the `entityType` column.
`OFFSET` is not supported. To page
through results, filter on the earliest change `Id` as a continuation token. For example
`"WHERE Id < :id"`. On each
query, both an upper bound and a lower bound for the
`ChangeDateTime` are required.
| Column name | Type | Description |
| --- | --- | --- |
| ChangeDateTime | `Datetime` | The date and time this change happened. |
| EntityId | `Number` | The ID of the entity that was changed. |
| EntityType | `Text` | The [type](/ad-manager/api/reference/v202608/PublisherQueryLanguageService.ChangeHistoryEntityType) of the entity that was changed. |
| Id | `Text` | The ID of this change. IDs may only be used with `"<"` operator for paging and are subject to change. Do not store IDs. Note that the `"<"` here does not compare the value of the ID but the row in the change history table it represents. |
| Operation | `Text` | The [operation](/ad-manager/api/reference/v202608/PublisherQueryLanguageService.ChangeHistoryOperation) that was performed on this entity. |
| UserId | `Number` | The [ID](/ad-manager/api/reference/v202608/UserService.User#id) of the user that made this change. |

### ad\_category
| Column name | Type | Description |
| --- | --- | --- |
| ChildIds | `Set of number` | Child IDs of an Ad category. Only general categories have children |
| Id | `Number` | ID of an Ad category |
| Name | `Text` | Localized name of an Ad category |
| ParentId | `Number` | Parent ID of an Ad category. Only general categories have parents |
| Type | `Text` | Type of an Ad category. Only general categories have children |

### rich\_media\_ad\_company
The global set of rich media ad companies that are known to Google.
| Column name | Type | Description |
| --- | --- | --- |
| CompanyGvlId | `Number` | IAB Global Vendor List ID of a Rich Media Ad Company |
| GdprStatus | `Text` | GDPR compliance status of a Rich Media Ad Company. Indicates whether the company has been registered with Google as a compliant company for GDPR. |
| Id | `Number` | ID of a Rich Media Ad Company |
| Name | `Text` | Name of a Rich Media Ad Company |
| PolicyUrl | `Text` | Policy URL of a Rich Media Ad Company |

### mcm\_earnings
Restriction: On each query, an expression scoping the MCM earnings
to a single month is required (e.x. "WHERE month = '2020-01'" or
"WHERE month IN ('2020-01')"). By default, child publishers are
ordered by their network code.
| Column name | Type | Description |
| --- | --- | --- |
| ChildName | `Text` | The name of the child publisher. |
| ChildNetworkCode | `Text` | The network code of the child publisher. |
| ChildPaymentCurrencyCode | `Text` | The child payment currency code as defined by ISO 4217. |
| ChildPaymentMicros | `Number` | The portion of the total earnings paid to the child publisher in micro units of the `ChildPaymentCurrencyCode` |
| DeductionsCurrencyCode | `Text` | The deductions currency code as defined by ISO 4217. Null for earnings prior to August 2020. |
| DeductionsMicros | `Number` | The deductions for the month due to spam in micro units of the `DeductionsCurrencyCode`. Null for earnings prior to August 2020. |
| DelegationType | `Text` | The current type of MCM delegation between the parent and child publisher. |
| Month | `Date` | The year and month that the MCM earnings data applies to. The date will be specified as the first of the month. |
| ParentName | `Text` | The name of the parent publisher. |
| ParentNetworkCode | `Text` | The network code of the parent publisher. |
| ParentPaymentCurrencyCode | `Text` | The parent payment currency code as defined by ISO 4217. |
| ParentPaymentMicros | `Number` | The portion of the total earnings paid to the parent publisher in micro units of the `ParentPaymentCurrencyCode`. |
| TotalEarningsCurrencyCode | `Text` | The total earnings currency code as defined by ISO 4217. |
| TotalEarningsMicros | `Number` | The total earnings for the month in micro units of the `TotalEarningsCurrencyCode`. |

### Linked\_Device
| Column name | Type | Description |
| --- | --- | --- |
| Id | `Number` | The ID of the LinkedDevice |
| Name | `Text` | The name of the LinkedDevice |
| UserId | `Number` | The ID of the user that this device belongs to. |
| Visibility | `Text` | The visibility of the LinkedDevice. |

### child\_publisher
By default, child publishers are ordered by their ID.
| Column name | Type | Description |
| --- | --- | --- |
| AddressVerificationExpirationTime | `Datetime` | Date when the child publisher's address verification (mail PIN) will expire. |
| AddressVerificationLastModifiedTime | `Datetime` | The time of the last change in the child publisher's address verification (mail PIN) process. |
| AddressVerificationStatus | `Text` | The address verification (mail PIN) status of the child publisher's Ad Manager network. Possible values are `EXEMPT`, `EXPIRED`, `FAILED`, `PENDING`, `NOT_ELIGIBLE`, and `VERIFIED`. |
| ApprovalStatus | `Text` | The approval status of the child publisher's Ad Manager network. Possible values are `APPROVED`, `CLOSED_BY_PUBLISHER`, `CLOSED_INVALID_ACTIVITY`, `CLOSED_POLICY_VIOLATION`, `DEACTIVATED_BY_AD_MANAGER`, `DISAPPROVED_DUPLICATE_ACCOUNT`, `DISAPPROVED_INELIGIBLE`, and `PENDING_GOOGLE_APPROVAL`. |
| ApprovedManageAccountRevshareMillipercent | `Number` | The approved revshare with the MCM child publisher |
| ChildNetworkAdExchangeEnabled | `Boolean` | Whether the child publisher's Ad Manager network has Ad Exchange enabled |
| ChildNetworkCode | `Text` | The network code of the MCM child publisher |
| DelegationType | `Text` | The delegation type of the MCM child publisher. This will be the approved type if the child has accepted the relationship, and the proposed type otherwise. |
| Email | `Text` | The email of the MCM child publisher |
| Id | `Number` | The ID of the MCM child publisher. |
| IdentityVerificationLastModifiedTime | `Datetime` | The time of the last change in the child publisher's identity verification process. |
| IdentityVerificationStatus | `Text` | Status of the child publisher's identity verification process. Possible values are `EXEMPT`, `EXPIRED`, `FAILED`, `PENDING`, `NOT_ELIGIBLE`, and `VERIFIED`. |
| InvitationStatus | `Text` | Status of the parent's invitation request to a child publisher. Possible values are `ACCEPTED`, `EXPIRED`, `PENDING`, `REJECTED`, and `WITHDRAWN`. |
| Name | `Text` | The name of the MCM child publisher |
| OnboardingTasks | `Set of text` | The child publisher's pending onboarding tasks. This will only be populated if the child publisher's `AccountStatus` is `PENDING_GOOGLE_APPROVAL`. |
| ReadinessStatus | `Text` | Overall onboarding readiness of the child publisher. Correlates with serving behavior, but does not include site-level approval information. Possible values are `READY`, `NOT_READY`, and `INACTIVE`. |
| SellerId | `Text` | The child publisher's seller ID, as specified in the parent publisher's sellers.json file. This field is only relevant for Manage Inventory child publishers. |

### content\_label
| Column name | Type | Description |
| --- | --- | --- |
| Id | `Number` | The ID of the Content Label |
| Label | `Text` | The name of the Content Label |

### taxonomy\_category
| Column name | Type | Description |
| --- | --- | --- |
---
Production WSDL
:   `https://ads.google.com/apis/ads/publisher/v202608/PublisherQueryLanguageService?wsdl`
Namespace
:   `https://www.google.com/apis/ads/publisher/v202608`
Operations
:   * [select](#select)
Errors
:   * [AdUnitCodeError](#AdUnitCodeError)
* [AdUnitHierarchyError](#AdUnitHierarchyError)
* [ApiVersionError](#ApiVersionError)
* [AudienceSegmentError](#AudienceSegmentError)
* [AuthenticationError](#AuthenticationError)
* [CollectionSizeError](#CollectionSizeError)
* [CommonError](#CommonError)
* [CreativeError](#CreativeError)
* [DealError](#DealError)
* [ExchangeRateError](#ExchangeRateError)
* [FeatureError](#FeatureError)
* [FileError](#FileError)
* [InternalApiError](#InternalApiError)
* [InvalidEmailError](#InvalidEmailError)
* [InvalidUrlError](#InvalidUrlError)
* [InventoryTargetingError](#InventoryTargetingError)
* [InventoryUnitError](#InventoryUnitError)
* [LineItemFlightDateError](#LineItemFlightDateError)
* [LineItemOperationError](#LineItemOperationError)
* [NotNullError](#NotNullError)
* [NullError](#NullError)
* [OrderActionError](#OrderActionError)
* [OrderError](#OrderError)
* [ParseError](#ParseError)
* [PermissionError](#PermissionError)
* [PublisherQueryLanguageContextError](#PublisherQueryLanguageContextError)
* [PublisherQueryLanguageSyntaxError](#PublisherQueryLanguageSyntaxError)
* [QuotaError](#QuotaError)
* [RangeError](#RangeError)
* [RegExError](#RegExError)
* [RequestError](#RequestError)
* [RequiredCollectionError](#RequiredCollectionError)
* [RequiredError](#RequiredError)
* [RequiredNumberError](#RequiredNumberError)
* [RequiredSizeError](#RequiredSizeError)
* [ReservationDetailsError](#ReservationDetailsError)
* [ServerError](#ServerError)
* [StatementError](#StatementError)
* [StringFormatError](#StringFormatError)
* [StringLengthError](#StringLengthError)
* [TypeError](#TypeError)
* [UniqueError](#UniqueError)

### select
Retrieves rows of data that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/PublisherQueryLanguageService.Statement#query) from the system.

## Types

### Row
| Field | Type | Description |
|-------|------|-------------|
| `values` | Value[] | Cell values |

### Value
| Field | Type | Description |
|-------|------|-------------|
| `value` | any | Cell value |
| `type` | string | Value type |

### ColumnType
| Field | Type | Description |
|-------|------|-------------|
| `label` | string | Column label |
| `name` | string | Column name |
| `type` | string | Data type |

### ResultSet
| Field | Type | Description |
|-------|------|-------------|
| `columnTypes` | ColumnType[] | Column metadata |
| `rows` | Row[] | Data rows |

## Enumerations

### DataType
| Value | Description |
|-------|-------------|
| `STRING` | |
| `INTEGER` | |
| `BOOLEAN` | |
| `DATE` | |
| `DATETIME` | |
| `ENUM` | |

