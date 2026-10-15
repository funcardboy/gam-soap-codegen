# PublisherQueryLanguageService Reference

**Service**: PublisherQueryLanguageService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/PublisherQueryLanguageService
**Types**: 6

## Methods

### select
- **Request**: `Statement selectStatement` (Use `StatementBuilder.Select(...).From(...).Where(...).Limit(500).ToStatement()`)
- **Response**: `ResultSet`

## Available PQL System Tables & Common Columns

| PQL Table Name | Common Columns (`SELECT ...`) | Typical Use Case |
|----------------|-------------------------------|------------------|
| `Geo_Target` | `Id`, `Name`, `CanonicalParentId`, `ParentIds`, `CountryCode`, `Type`, `Targetable` | Resolve Geo Target IDs (Country, Region, City, District, Postal Code) |
| `Browser` | `Id`, `Name`, `MajorVersion`, `MinorVersion` | Resolve Browser Technology IDs (Safari, Chrome, Edge, Firefox, In-App) |
| `Browser_Language` | `Id`, `Name` | Resolve Browser Language IDs (`zh_HK`, `zh_TW`, `en`, etc.) |
| `Operating_System` | `Id`, `Name` | Resolve OS IDs (`iOS`, `Android`, `Windows`, `Mac OS X`) |
| `Operating_System_Version` | `Id`, `OperatingSystemId`, `MajorVersion`, `MinorVersion`, `MicroVersion` | Resolve OS Version IDs |
| `Device_Category` | `Id`, `Name` | Resolve Device Category IDs (`Desktop`, `Smartphone`, `Tablet`, `Connected TV`) |
| `Device_Capability` | `Id`, `Name` | Resolve Device Capabilities (`Mobile Apps`, `MRAID v1`, `MRAID v2`) |
| `Device_Manufacturer` | `Id`, `Name` | Resolve Device Manufacturers (`Apple`, `Samsung`, etc.) |
| `Mobile_Carrier` | `Id`, `Name`, `CountryCode` | Resolve Mobile Carriers |
| `Mobile_Device` | `Id`, `Name`, `DeviceManufacturerId` | Resolve specific Mobile Device models |
| `Mobile_Device_Submodel` | `Id`, `Name`, `MobileDeviceId`, `DeviceManufacturerId` | Resolve Mobile Device submodels |
| `Bandwidth_Group` | `Id`, `Name` | Resolve Bandwidth Group IDs |
| `Line_Item` | `Id`, `Name`, `OrderId`, `Status`, `LineItemType`, `CostType`, `StartDateTime`, `EndDateTime`, `UnitsBought` | Lightweight tabular query over Line Items |
| `Ad_Unit` | `Id`, `Name`, `AdUnitCode`, `ParentId`, `Status`, `PartnerId` | Lightweight tabular query over Ad Units |
| `User` | `Id`, `Name`, `Email`, `RoleId`, `RoleName`, `IsActive` | Lightweight tabular query over Users |
| `Company` | `Id`, `Name`, `Type`, `CreditStatus`, `ExternalId` | Lightweight tabular query over Advertisers/Agencies |
| `Programmatic_Buyer` | `BuyerAccountId`, `Name`, `PartnerClientId` | Lookup Programmatic Buyers |
| `Audience_Segment` | `Id`, `Name`, `Type`, `Status`, `Size`, `CategoryIds` | Lookup Audience Segments |
| `Change_History` | `Id`, `EntityId`, `EntityType`, `Operation`, `UserId`, `ChangeDateTime` | Audit log of entity changes |

## Types

### ResultSet

| Field | Type | Description |
|-------|------|-------------|
| `columnTypes` | `ColumnType[]` | A collection of `ColumnType` objects (`{'name': '...'}`) representing the schema header. |
| `rows` | `Row[]` | A collection of `Row` objects representing the data rows. Omitted/None if 0 rows match. |

### ColumnType

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | Represents the column's name. |

### Row

| Field | Type | Description |
|-------|------|-------------|
| `values` | `Value[]` | Represents a collection of `Value` objects (`TextValue`, `NumberValue`, `BooleanValue`, `DateTimeValue`, `DateValue`, `SetValue`) in the same order as `columnTypes`. |

### Value (Subclasses)
- `TextValue`: `{'value': str}`
- `NumberValue`: `{'value': str}` (numeric string)
- `BooleanValue`: `{'value': bool}`
- `DateValue`: `{'value': Date}`
- `DateTimeValue`: `{'value': DateTime}`
