# LiveStreamEventService Cheatsheet

## Methods

### createLiveStreamEvents
Creates new [LiveStreamEvent](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent) objects.
The following fields are required:
* [LiveStreamEvent.name](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#name)
* [LiveStreamEvent.startDateTime](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#startDateTime)
* [LiveStreamEvent.endDateTime](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#endDateTime)
* [LiveStreamEvent.contentUrls](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#contentUrls)
* [LiveStreamEvent.adTags](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#adTags)

### createSlates
Create new slates.
A slate creative is served as backup content in a live stream
event when no other creatives are eligible to be served.

### getLiveStreamEventsByStatement
Gets a [LiveStreamEventPage](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEventPage) of [LiveStreamEvent](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent) objects that satisfy the given
[Statement.query](/ad-manager/api/reference/v202608/LiveStreamEventService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [LiveStreamEvent.id](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#id) |
| `slateCreativeId` | [LiveStreamEvent.slateCreativeId](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#slateCreativeId) |
| `assetKey` | [LiveStreamEvent.assetKey](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#assetKey) |
| `streamCreateDaiAuthenticationKeyIds` | [LiveStreamEvent.streamCreateDaiAuthenticationKeyIds](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#streamCreateDaiAuthenticationKeyIds) |
| `dynamicAdInsertionType` | [LiveStreamEvent.dynamicAdInsertionType](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#dynamicAdInsertionType) |
| `streamingFormat` | [LiveStreamEvent.streamingFormat](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#streamingFormat) |
| `customAssetKey` | [LiveStreamEvent.customAssetKey](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#customAssetKey) |
| `daiEncodingProfileIds` | [LiveStreamEvent.daiEncodingProfileIds](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#daiEncodingProfileIds) |
| `segmentUrlAuthenticationKeyIds` | [LiveStreamEvent.segmentUrlAuthenticationKeyIds](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent#segmentUrlAuthenticationKeyIds) |

### getSlatesByStatement
Gets a [SlatePage](/ad-manager/api/reference/v202608/LiveStreamEventService.SlatePage) of [Slate](/ad-manager/api/reference/v202608/LiveStreamEventService.Slate) objects that satisfy the given [Statement.query](/ad-manager/api/reference/v202608/LiveStreamEventService.Statement#query). The following fields are supported for filtering:
| PQL Property | Object Property |
| --- | --- |
| `id` | [Slate.id](/ad-manager/api/reference/v202608/LiveStreamEventService.Slate#id) |
| `name` | [Slate.name](/ad-manager/api/reference/v202608/LiveStreamEventService.Slate#name) |
| `lastModifiedDateTime` | [Slate.lastModifiedDateTime](/ad-manager/api/reference/v202608/LiveStreamEventService.Slate#lastModifiedDateTime) |

### performLiveStreamEventAction
Performs actions on [LiveStreamEvent](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent) objects that match the given [Statement.query](/ad-manager/api/reference/v202608/LiveStreamEventService.Statement#query).

### performSlateAction
Performs actions on slates that match the given [Statement](/ad-manager/api/reference/v202608/LiveStreamEventService.Statement).

### updateLiveStreamEvents
Updates the specified [LiveStreamEvent](/ad-manager/api/reference/v202608/LiveStreamEventService.LiveStreamEvent) objects.

### updateSlates
Update existing slates.
Only the slateName is editable.
