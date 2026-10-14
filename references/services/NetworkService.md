# NetworkService Cheatsheet

## Methods

### getAllNetworks
Returns the list of [Network](/ad-manager/api/reference/v202608/NetworkService.Network) objects to which the current login has access.
Intended to be used without a network code in the SOAP header
when the login may have more than one network associated with
it.

### getCurrentNetwork
Returns the current network for which requests are being made.

### getDefaultThirdPartyDataDeclaration
Returns the default [ThirdPartyDataDeclaration](/ad-manager/api/reference/v202608/NetworkService.ThirdPartyDataDeclaration) for this network. If this setting has
never been updated on your network, then this API response will be empty.

### makeTestNetwork
Creates a new blank network for testing purposes using the current
login.
Each login(i.e. email address) can only have one test network.
Data from any of your existing networks will not be transferred to
the new test network. Once the test network is created, the test
network can be used in the API by supplying the [Network.networkCode](/ad-manager/api/reference/v202608/NetworkService.Network#networkCode) in the SOAP
header or by logging into the Ad Manager UI.
Test networks are limited in the following ways:
* Test networks cannot serve ads.
* Because test networks cannot serve ads, reports will always
come back without data.
* Since forecasting requires serving history, forecast service
results will be faked. See [ForecastService](/ad-manager/api/reference/v202608/ForecastService) for more info.
* Test networks are, by default, Ad Manager networks and don't
have any features from Ad Manager 360. To have additional features
turned on, please contact your account manager.
* Test networks are limited to 10,000 objects per entity
type.

### updateNetwork
Updates the specified network. Currently, only the network display name can be updated.

## Types

### Network
| Field | Type | Description |
|-------|------|-------------|
| `id` | int | Network ID |
| `displayName` | string | Display name |
| `networkCode` | string | Network code |
| `timeZone` | string | Timezone |
| `secondaryTimeZoneIds` | string[] | Secondary timezones |
| `companyName` | string | Company name |
| `effectiveUserId` | string | Effective user |
| `propertyType` | PropertyType | Property type |
