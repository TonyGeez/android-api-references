# android.media.tv

# android.media.tv

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [BaseTvColumns](../android/media/tv/TvContract.BaseTvColumns.md) | Common base for the tables of TV channels/programs. |
| --- | --- |
| [OnUnhandledInputEventListener](../android/media/tv/TvView.OnUnhandledInputEventListener.md) | Interface definition for a callback to be invoked when the unhandled input event is received. |

## Classes

| [AdBuffer](AdBuffer.md) | Buffer for advertisement data. |
| --- | --- |
| [AdRequest](AdRequest.md) | An advertisement request which can be sent to TV input to request AD operations. |
| [AdResponse](AdResponse.md) | An advertisement response which can be sent to TV interactive App service to inform AD status. |
| [AitInfo](AitInfo.md) | AIT (Application Information Table) info. |
| --- | --- |
| [BroadcastInfoRequest](BroadcastInfoRequest.md) | A request for the information retrieved from broadcast signal. |
| [BroadcastInfoResponse](BroadcastInfoResponse.md) | A response of [BroadcastInfoRequest](BroadcastInfoRequest.md) for information retrieved from broadcast signal. |
| [CommandRequest](CommandRequest.md) | A request for command from broadcast signal. |
| --- | --- |
| [CommandResponse](CommandResponse.md) | A response for command from broadcast signal. |
| [DsmccRequest](DsmccRequest.md) | A request for DSM-CC from broadcast signal. |
| [DsmccResponse](DsmccResponse.md) | A response for DSM-CC from broadcast signal. |
| --- | --- |
| [PesRequest](PesRequest.md) | A request for PES from broadcast signal. |
| [PesResponse](PesResponse.md) | A response for PES from broadcast signal. |
| [SectionRequest](SectionRequest.md) | A request for Section from broadcast signal. |
| --- | --- |
| [SectionResponse](SectionResponse.md) | A response for Section from broadcast signal. |
| [SignalingDataInfo](SignalingDataInfo.md) | Describes a metadata object of a [SignalingDataResponse](SignalingDataResponse.md). |
| [SignalingDataRequest](SignalingDataRequest.md) | Request to retrieve the Low-level Signalling Tables (LLS) and Service-layer Signalling (SLS) metadata. |
| --- | --- |
| [SignalingDataResponse](SignalingDataResponse.md) | A response for the signaling data from the broadcast signal. |
| [StreamEventRequest](StreamEventRequest.md) | A request for Stream Event from broadcast signal. |
| [StreamEventResponse](StreamEventResponse.md) | A response for Stream Event from broadcast signal. |
| --- | --- |
| [TableRequest](TableRequest.md) | A request for Table from broadcast signal. |
| [TableResponse](TableResponse.md) | A response for Table from broadcast signal. |
| [TimelineRequest](TimelineRequest.md) | A request for Timeline from broadcast signal. |
| --- | --- |
| [TimelineResponse](TimelineResponse.md) | A response for Timeline from broadcast signal. |
| [TsRequest](TsRequest.md) | A request for TS (transport stream) from broadcast signal. |
| [TsResponse](TsResponse.md) | A response for TS (transport stream) from broadcast signal. |
| --- | --- |
| [TvContentRating](TvContentRating.md) | A class representing a TV content rating. |
| [TvContract](TvContract.md) | The contract between the TV provider and applications. |
| [TvInputInfo](TvInputInfo.md) | This class is used to specify meta information of a TV input. |
| --- | --- |
| [TvInputManager](TvInputManager.md) | Central system API to the overall TV input framework (TIF) architecture, which arbitrates interaction between applications and the selected TV inputs. |
| [TvInputService](TvInputService.md) | The TvInputService class represents a TV input or source such as HDMI or built-in tuner which provides pass-through video or broadcast TV programs. |
| [TvRecordingClient](TvRecordingClient.md) | The public interface object used to interact with a specific TV input service for TV program recording. |
| --- | --- |
| [TvRecordingInfo](TvRecordingInfo.md) | This class is used to describe the meta information for a TV recording. |
| [TvTrackInfo](TvTrackInfo.md) | Encapsulates the format of tracks played in [TvInputService](TvInputService.md). |
| [TvView](TvView.md) | Displays TV contents. |
| --- | --- |
