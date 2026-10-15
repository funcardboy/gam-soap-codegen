# CreativeService Reference

**Service**: CreativeService
**Source**: https://developers.google.com/ad-manager/api/reference/v202608/CreativeService
**Types**: 25

## Methods
- `createCreatives(Creative[] creatives) -> Creative[]`
- `getCreativesByStatement(Statement filterStatement) -> CreativePage` (PQL filterable: `id`, `name`, `advertiserId`, `width`, `height`, `lastModifiedDateTime`)
- `performCreativeAction(CreativeAction creativeAction, Statement filterStatement) -> UpdateResult`
- `updateCreatives(Creative[] creatives) -> Creative[]`

## Common Creative Types (all inherit base `Creative` fields)
- **Base `Creative` fields**: `advertiserId` (`long`, required), `id` (`long`, read-only), `name` (`string`, required), `size` (`Size`, required), `previewUrl` (`string`, read-only), `policyLabels` (`PolicyLabel[]`, read-only), `appliedLabels` (`AppliedLabel[]`), `lastModifiedDateTime` (`DateTime`, read-only), `customFieldValues` (`BaseCustomFieldValue[]`), `thirdPartyUrls` (`ThirdPartyUrl[]`).
- **Subclasses (`xsi_type`)**:
  - `ImageCreative`: `destinationUrl`, `primaryImageAsset` (`CreativeAsset`), `altText`, `thirdPartyImpressionTrackingUrls`
  - `CustomCreative`: `htmlSnippet`, `customCreativeAssets`, `isInterstitial`, `isSafeFrameCompatible`, `destinationUrl`
  - `ThirdPartyCreative`: `snippet`, `expandedSnippet`, `sslScanResult`, `sslManualOverride`, `isSafeFrameCompatible`
  - `TemplateCreative`: `creativeTemplateId`, `creativeTemplateVariableValues` (`BaseCreativeTemplateVariableValue[]`), `isInterstitial`, `isNativeEligible`, `destinationUrl`
  - `VideoCreative` / `VastRedirectCreative`: `vastXmlUrl`, `vastRedirectType` (`LINEAR`, `NON_LINEAR`, `LINEAR_AND_NON_LINEAR`), `duration`, `destinationUrl`, `trackingUrls`
  - `AdExchangeCreative` / `AdSenseCreative` / `ClickTrackingCreative` / `InternalRedirectCreative` / ` Html5Creative`
