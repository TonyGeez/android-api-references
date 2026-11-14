Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Connection

```
abstract class Connection : Conferenceable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telecom.Conferenceable](Conferenceable.md) ||
| | ↳ | [android.telecom.Connection](Connection.md) |

Represents a phone call or connection to a remote endpoint that carries voice and/or video traffic.

Implementations create a custom subclass of `Connection` and return it to the framework as the return value of onCreateIncomingConnection or onCreateOutgoingConnection. Implementations are then responsible for updating the state of the `Connection`, and must call destroy to signal to the framework that the `Connection` is no longer used and associated resources may be recovered.

Subclasses of `Connection` override the `on*` methods to provide the ConnectionService's implementation of calling functionality. The `on*` methods are called by Telecom to inform an instance of a `Connection` of actions specific to that `Connection` instance.

Basic call support requires overriding the following methods: onAnswer, onDisconnect, onReject, onAbort

Where a `Connection` has `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORT_HOLD:kotlin.Int`, the onHold and onUnhold methods should be overridden to provide hold support for the `Connection`.

Where a `Connection` supports a variation of video calling (e.g. the `CAPABILITY_SUPPORTS_VT_*` capability bits), onAnswer should be overridden to support answering a call as a video call.

Where a `Connection` has `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CAN_PULL_CALL:kotlin.Int`, onPullExternalCall should be overridden to provide support for pulling the external call.

Where a `Connection` supports conference calling onSeparate should be overridden.

There are a number of other `on*` methods which a `Connection` can choose to implement, depending on whether it is concerned with the associated calls from Telecom. If, for example, call events from a InCallService are handled, onCallEvent should be overridden. Another example is onExtrasChanged, which should be overridden if the `Connection` wishes to make use of extra information provided via the putExtras and removeExtras methods.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttModifyStatus` Provides constants to represent the results of responses to session modify requests sent via sendRttRequest |
| | `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttTextStream` Provides methods to read and write RTT data to/from the in-call app. |
| abstract | `https://developer.android.com/reference/kotlin/android/telecom/Connection.VideoProvider` Provides a means of controlling the video session associated with a Connection. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_AMR:kotlin.Int` Adaptive Multi-rate audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_AMR_WB:kotlin.Int` Adaptive Multi-rate wideband audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVRC:kotlin.Int` Enhanced Variable Rate Codec. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVRC_B:kotlin.Int` Enhanced Variable Rate Codec B. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVRC_NW:kotlin.Int` Enhanced Variable Rate Narrowband-Wideband Codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVRC_WB:kotlin.Int` Enhanced Variable Rate Wideband Codec. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVS_FB:kotlin.Int` Enhanced Voice Services Fullband audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVS_NB:kotlin.Int` Enhanced Voice Services Narrowband audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVS_SWB:kotlin.Int` Enhanced Voice Services Super-Wideband audio codec. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVS_WB:kotlin.Int` Enhanced Voice Services Wideband audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G711A:kotlin.Int` ITU-T G711A audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G711AB:kotlin.Int` ITU-T G711AB audio codec. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G711U:kotlin.Int` ITU-T G711U audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G722:kotlin.Int` ITU-T G722 audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G723:kotlin.Int` ITU-T G723 audio codec. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G729:kotlin.Int` ITU-T G729 audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_GSM_EFR:kotlin.Int` GSM Enhanced Full-Rate audio codec, also known as GSM-EFR, GSM 06. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_GSM_FR:kotlin.Int` GSM Full-Rate audio codec, also known as GSM-FR, GSM 06. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_GSM_HR:kotlin.Int` GSM Half Rate audio codec. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_NONE:kotlin.Int` Indicates that the audio codec is currently not specified or is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_QCELP13K:kotlin.Int` Qualcomm code-excited linear prediction 13 kilobit audio codec. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_ADD_PARTICIPANT:kotlin.Int` When set, indicates that this Connection supports initiation of a conference call by directly adding participants using onAddConferenceParticipants. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CANNOT_DOWNGRADE_VIDEO_TO_AUDIO:kotlin.Int` When set, prevents a video call from being downgraded to an audio-only call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CAN_PAUSE_VIDEO:kotlin.Int` For video calls, indicates whether the outgoing video for the call can be paused using the `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int` VideoState. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CAN_PULL_CALL:kotlin.Int` When set for an external connection, indicates that this `Connection` can be pulled from a remote device to the current device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CAN_SEND_RESPONSE_VIA_CONNECTION:kotlin.Int` Indicates that the connection itself wants to handle any sort of reply response, rather than relying on SMS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CAN_UPGRADE_TO_VIDEO:kotlin.Int` Call can be upgraded to a video call. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_DISCONNECT_FROM_CONFERENCE:kotlin.Int` Connection is able to be individually disconnected when in a `Conference`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_HOLD:kotlin.Int` Connection can currently be put on hold or unheld. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_MANAGE_CONFERENCE:kotlin.Int` Connection supports conference management. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_MERGE_CONFERENCE:kotlin.Int` Connections within a conference can be merged. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_MUTE:kotlin.Int` Connection can be muted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_REMOTE_PARTY_SUPPORTS_RTT:kotlin.Int` Indicates whether the remote party supports RTT or not to the UI. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_RESPOND_VIA_TEXT:kotlin.Int` Connection supports responding via text option. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SEPARATE_FROM_CONFERENCE:kotlin.Int` Connection is able to be separated from its parent `Conference`, if any. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_LOCAL_BIDIRECTIONAL:kotlin.Int` Local device supports bidirectional video calling. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_LOCAL_RX:kotlin.Int` Local device supports receiving video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_LOCAL_TX:kotlin.Int` Local device supports transmitting video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_REMOTE_BIDIRECTIONAL:kotlin.Int` Remote device supports bidirectional video calling. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_REMOTE_RX:kotlin.Int` Remote device supports receiving video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_REMOTE_TX:kotlin.Int` Remote device supports transmitting video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORT_DEFLECT:kotlin.Int` Call supports the deflect feature. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORT_HOLD:kotlin.Int` Connection supports the hold feature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SWAP_CONFERENCE:kotlin.Int` Connections within a conference can be swapped between foreground and background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_TRANSFER:kotlin.Int` Indicates that this `Connection` can be transferred to another number. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_TRANSFER_CONSULTATIVE:kotlin.Int` Indicates that this `Connection` can perform a consultative transfer to another ongoing `Connection` that also has this capability. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_HOLD_FAILED:kotlin.String` Connection event used to inform Telecom when a hold operation on a call has failed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_MERGE_FAILED:kotlin.String` Connection event used to inform InCallServices when the merging of two calls has failed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_PULL_FAILED:kotlin.String` Connection event used to inform InCallServices when pulling of an external call has failed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_REMOTELY_HELD:kotlin.String` Connection event used to inform InCallServices when a call has been put on hold by the remote party. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_REMOTELY_UNHELD:kotlin.String` Connection event used to inform InCallServices when a call which was remotely held (see `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_REMOTELY_HELD:kotlin.String`) has been un-held by the remote party. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_RESUME_FAILED:kotlin.String` Connection event used to inform Telecom when a resume operation on a call has failed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_SWITCH_FAILED:kotlin.String` Connection event used to inform Telecom when a switch operation on a call has failed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_DISCONNECT_FAILED:kotlin.String` Connection event used to inform Telecom when a disconnect request fails during a call merge. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_MERGE_COMPLETE:kotlin.String` Connection event used to inform InCallServices when the process of merging a Connection into a conference has completed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_MERGE_START:kotlin.String` Connection event used to inform InCallServices when the process of merging a Connection into a conference has begun. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_ON_HOLD_TONE_END:kotlin.String` Connection event used to inform Telecom that it should stop the on hold tone. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_ON_HOLD_TONE_START:kotlin.String` Connection event used to inform Telecom that it should play the on hold tone. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_RTT_AUDIO_INDICATION_CHANGED:kotlin.String` Connection event used to inform an InCallService that the RTT audio indication has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_ANSWERING_DROPS_FG_CALL:kotlin.String` Boolean connection extra key set on a Connection in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` state to indicate that answering the call will cause the current active foreground call to be dropped. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_ANSWERING_DROPS_FG_CALL_APP_NAME:kotlin.String` String connection extra key set on a Connection in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` state to indicate the name of the third-party app which is responsible for the current foreground call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_AUDIO_CODEC:kotlin.String` The audio codec in use for the current Connection, if known. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_AUDIO_CODEC_BANDWIDTH_KHZ:kotlin.String` Float connection extra key used to store the audio codec bandwidth in khz for the current Connection. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_AUDIO_CODEC_BITRATE_KBPS:kotlin.String` Float connection extra key used to store the audio codec bitrate in kbps for the current Connection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_CALL_SUBJECT:kotlin.String` Connection extra key used to store the subject for an incoming call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_CHILD_ADDRESS:kotlin.String` Connection extra key used to store a child number associated with the current connection. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_IS_RTT_AUDIO_PRESENT:kotlin.String` Boolean connection extra key set on the extras passed to sendConnectionEvent which indicates that audio is present on the RTT call when the extra value is true. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_LAST_FORWARDED_NUMBER:kotlin.String` Connection extra key used to store the last forwarded number associated with the current connection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_LAST_KNOWN_CELL_IDENTITY:kotlin.String` Last known cell identity key `https://developer.android.com/reference/kotlin/android/telephony/CellIdentity.html#` to be used to fill geo location header in case of an emergency call. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_SIP_INVITE:kotlin.String` String Connection extra key used to store SIP invite fields for an incoming call for IMS call |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_ASSISTED_DIALING:kotlin.Int` Set by the framework to indicate that a connection is using assisted dialing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_CROSS_SIM:kotlin.Int` Connection is using cross sim technology. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_HAS_CDMA_VOICE_PRIVACY:kotlin.Int` Indicates that the connection has CDMA Enhanced Voice Privacy enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_HIGH_DEF_AUDIO:kotlin.Int` Connection is using high definition audio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_ADHOC_CONFERENCE:kotlin.Int` Set by the framework to indicate that a call is an adhoc conference call. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` When set, indicates that the `Connection` does not actually exist locally for the ConnectionService. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_RTT:kotlin.Int` Set by the framework to indicate that a connection has an active RTT session associated with it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_TETHERED_CALL:kotlin.Int` Set by a ConnectionService to indicate that this Connection represents a tethered call synchronized from a primary device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_NETWORK_IDENTIFIED_EMERGENCY_CALL:kotlin.Int` Set by the framework to indicate that the network has identified a Connection as an emergency call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_SELF_MANAGED:kotlin.Int` Set by the framework to indicate that the Connection originated from a self-managed ConnectionService. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_WIFI:kotlin.Int` Connection is using WIFI. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_ACTIVE:kotlin.Int` A connection is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_AUDIO_PROCESSING:kotlin.Int` The state of a call that is active with the network, but the audio from the call is being intercepted by an app on the local device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DIALING:kotlin.Int` An outgoing connection is in the dialing state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DISCONNECTED:kotlin.Int` A connection has been disconnected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_HOLDING:kotlin.Int` A connection is on hold. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_INITIALIZING:kotlin.Int` The connection is initializing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_NEW:kotlin.Int` The connection is new and not connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_PULLING_CALL:kotlin.Int` The state of an external connection which is in the process of being pulled from a remote device to the local device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` An incoming connection is in the ringing state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_SIMULATED_RINGING:kotlin.Int` The state of a call that is being presented to the user after being in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_AUDIO_PROCESSING:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_FAILED:kotlin.Int` Indicates that verification by the network failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_NOT_VERIFIED:kotlin.Int` Indicates that the network could not perform verification. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_PASSED:kotlin.Int` Indicates that verification by the network passed. |

| Public constructors ||
|---|---|
| Connection Create a new Connection. |

| Public methods ||
|---|---|
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | capabilitiesToString Renders a set of capability bits (`CAPABILITY_*`) as a human readable string. |
| open static [Connection](Connection.md)! | createCanceledConnection Return a `Connection` which represents a canceled connection attempt. |
| open static [Connection](Connection.md)! | createFailedConnection Return a `Connection` which represents a failed connection attempt. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | destroy Tears down the Connection object. |
| [Uri](../android.net/Uri.md)! | getAddress <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAddressPresentation <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getAudioModeIsVoip <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAudioProcessingUseCase <br /> |
| [CallAudioState](CallAudioState.md)! | getCallAudioState <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getCallerDisplayName <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCallerDisplayNamePresentation <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCallerNumberVerificationStatus Gets the verification status for the phone number of an incoming call as identified in ATIS-1000082. |
| --- | --- |
| [Conference](Conference.md)! | getConference <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Conferenceable](Conferenceable.md)!\>! | getConferenceables Returns the connections or conferences with which this connection can be conferenced. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getConnectionCapabilities Returns the connection's capabilities, as a bit mask of the `CAPABILITY_*` constants. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getConnectionProperties Returns the connection's properties, as a bit mask of the `PROPERTY_*` constants. |
| [CallEndpoint](CallEndpoint.md) | getCurrentCallEndpoint Obtains the current CallEndpoint. |
| [DisconnectCause](DisconnectCause.md)! | getDisconnectCause <br /> |
| --- | --- |
| [Bundle](../android.os/Bundle.md)! | getExtras Returns the extras associated with this connection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getState <br /> |
| [StatusHints](StatusHints.md)! | getStatusHints <br /> |
| --- | --- |
| [Connection.VideoProvider](../android/telecom/Connection.VideoProvider.md)! | getVideoProvider <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVideoState Returns the video state of the connection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | handleRttUpgradeResponse Notifies this connection of a response to a previous remotely-initiated RTT upgrade request sent via sendRemoteRttRequest. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isRingbackRequested Returns whether this connection is requesting that the system play a ringback tone on its behalf. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | notifyConferenceMergeFailed Called by a ConnectionService to notify Telecom that a onMerge request failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAbort Notifies this Connection of a request to abort. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAddConferenceParticipants Supports initiation of a conference call by directly adding participants to an ongoing call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAnswer Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to accept. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAnswer Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to accept. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAvailableCallEndpointsChanged Notifies this Connection that the available call endpoints have been changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCallAudioStateChanged Notifies this Connection that the getCallAudioState property has a new value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCallEndpointChanged Notifies this Connection that the audio endpoint has been changed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCallEvent Notifies this Connection of a Call event initiated from an InCallService. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDeflect Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to deflect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDisconnect Notifies this Connection of a request to disconnect. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onExtrasChanged Notifies this Connection of a change to the extras made outside the ConnectionService. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onHandoverComplete Notifies this Connection that a handover has completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onHold Notifies this Connection of a request to hold. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onMuteStateChanged Notifies this Connection that its audio mute state has been changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPlayDtmfTone Notifies this Connection of a request to play a DTMF tone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPostDialContinue Notifies this Connection whether the user wishes to proceed with the post-dial DTMF codes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPullExternalCall Notifies this Connection of a request to pull an external call to the local device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onReject Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to reject. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onReject Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to reject. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onReject Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to reject with a message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onSeparate Notifies this Connection of a request to separate from its parent conference. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onShowIncomingCallUi Notifies this Connection that its ConnectionService is responsible for displaying its incoming call user interface for the Connection |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onSilence Notifies this Connection of a request to silence the ringer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStartRtt Notifies this Connection that the user has requested an RTT session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStateChanged Notifies this Connection of an internal state change. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStopDtmfTone Notifies this Connection of a request to stop any currently playing DTMF tones. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStopRtt Notifies this Connection that it should terminate any existing RTT communication channel. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onTrackedByNonUiService Inform this Conenection when it will or will not be tracked by an non-UI InCallService. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onTransfer Notifies this Connection of a request to transfer to a target number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onTransfer Notifies this Connection of a request to start a CONSULTATIVE transfer to another Connection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onUnhold Notifies this Connection of a request to exit a hold state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onUsingAlternativeUi Inform this Connection when it will or will not be tracked by an InCallService which can provide an InCall UI. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | propertiesToString Renders a set of property bits (`PROPERTY_*`) as a human readable string. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putExtras Adds some extras to this `Connection`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | queryLocationForEmergency Query the device's location in order to place an Emergency Call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeExtras Removes extras from this `Connection`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeExtras Removes extras from this `Connection`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestBluetoothAudio Request audio routing to a specific bluetooth device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestCallEndpointChange Request audio routing to a specific CallEndpoint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendConnectionEvent Sends an event associated with this `Connection` with associated event extras to the InCallService. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendRemoteRttRequest Informs listeners that the remote side of the call has requested an upgrade to include an RTT session in the call. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendRttInitiationFailure Informs listeners that a previously requested RTT session via isRequestingRtt or onStartRtt has failed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendRttInitiationSuccess Informs listeners that a previously requested RTT session via isRequestingRtt or onStartRtt has succeeded. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendRttSessionRemotelyTerminated Informs listeners that a currently active RTT session has been terminated by the remote side of the coll. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setActive Sets state to active (e.g., an ongoing connection where two or more parties can actively communicate). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAddress Sets the value of the getAddress property. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAudioModeIsVoip Requests that the framework use VOIP audio mode for this connection. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAudioProcessing Sets state to audio processing (e.g. the call is active but the audio from the call is being intercepted by an app on the local device) and the usecase. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAudioRoute Sets the audio route (speaker, bluetooth, etc...). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCallerDisplayName Sets the caller display name (CNAP). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCallerNumberVerificationStatus Sets the verification status for the phone number of an incoming call as identified in ATIS-1000082. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setConferenceableConnections Sets the connections with which this connection can be conferenced. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setConferenceables Similar to setConferenceableConnections, sets a list of connections or conferences with which this connection can be conferenced. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setConnectionCapabilities Sets the connection's capabilities as a bit mask of the `CAPABILITY_*` constants. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setConnectionProperties Sets the connection's properties as a bit mask of the `PROPERTY_*` constants. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDialing Sets state to dialing (e.g., dialing an outbound connection). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDisconnected Sets state to disconnected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExtras Set some extras that can be associated with this `Connection`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInitialized Sets state to initialized (the Connection has been set up and is now ready to be used). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInitializing Sets state to initializing (this Connection is not yet ready to be used). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNextPostDialChar Informs listeners that this `Connection` has processed a character in the post-dial started state. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnHold Sets state to be on hold. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPostDialWait Informs listeners that this `Connection` is in a post-dial wait state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPulling Sets state to pulling (e.g. the connection is being pulled to the local device from another device). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRingbackRequested Requests that the framework play a ringback tone. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRinging Sets state to ringing (e.g., an inbound ringing connection). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSimulatedRinging Sets state to simulated ringing where its presented to the user after being in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_AUDIO_PROCESSING:kotlin.Int`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStatusHints Sets the label and icon status to display in the in-call UI. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVideoProvider Sets the video connection provider. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVideoState Set the video state for the connection. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | stateToString <br /> |

## Constants

### AUDIO_CODEC_AMR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_AMR: Int
```

Adaptive Multi-rate audio codec.

 Value: 1

### AUDIO_CODEC_AMR_WB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_AMR_WB: Int
```

Adaptive Multi-rate wideband audio codec.

 Value: 2

### AUDIO_CODEC_EVRC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_EVRC: Int
```

Enhanced Variable Rate Codec. See 3GPP2 C.S0014-A.

 Value: 4

### AUDIO_CODEC_EVRC_B

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_EVRC_B: Int
```

Enhanced Variable Rate Codec B. Commonly used on CDMA networks.

 Value: 5

### AUDIO_CODEC_EVRC_NW

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_EVRC_NW: Int
```

Enhanced Variable Rate Narrowband-Wideband Codec.

 Value: 7

### AUDIO_CODEC_EVRC_WB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_EVRC_WB: Int
```

Enhanced Variable Rate Wideband Codec. See RFC5188.

 Value: 6

### AUDIO_CODEC_EVS_FB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_EVS_FB: Int
```

Enhanced Voice Services Fullband audio codec. See 3GPP TS 26.441.

 Value: 20

### AUDIO_CODEC_EVS_NB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_EVS_NB: Int
```

Enhanced Voice Services Narrowband audio codec. See 3GPP TS 26.441.

 Value: 17

### AUDIO_CODEC_EVS_SWB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_EVS_SWB: Int
```

Enhanced Voice Services Super-Wideband audio codec. See 3GPP TS 26.441.

 Value: 19

### AUDIO_CODEC_EVS_WB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_EVS_WB: Int
```

Enhanced Voice Services Wideband audio codec. See 3GPP TS 26.441.

 Value: 18

### AUDIO_CODEC_G711A

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_G711A: Int
```

ITU-T G711A audio codec.

 Value: 13

### AUDIO_CODEC_G711AB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_G711AB: Int
```

ITU-T G711AB audio codec.

 Value: 15

### AUDIO_CODEC_G711U

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_G711U: Int
```

ITU-T G711U audio codec.

 Value: 11

### AUDIO_CODEC_G722

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_G722: Int
```

ITU-T G722 audio codec.

 Value: 14

### AUDIO_CODEC_G723

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_G723: Int
```

ITU-T G723 audio codec.

 Value: 12

### AUDIO_CODEC_G729

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_G729: Int
```

ITU-T G729 audio codec.

 Value: 16

### AUDIO_CODEC_GSM_EFR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_GSM_EFR: Int
```

GSM Enhanced Full-Rate audio codec, also known as GSM-EFR, GSM 06.60, or simply EFR.

 Value: 8

### AUDIO_CODEC_GSM_FR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_GSM_FR: Int
```

GSM Full-Rate audio codec, also known as GSM-FR, GSM 06.10, GSM, or simply FR.

 Value: 9

### AUDIO_CODEC_GSM_HR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_GSM_HR: Int
```

GSM Half Rate audio codec.

 Value: 10

### AUDIO_CODEC_NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_NONE: Int
```

Indicates that the audio codec is currently not specified or is unknown.

 Value: 0

### AUDIO_CODEC_QCELP13K

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_CODEC_QCELP13K: Int
```

Qualcomm code-excited linear prediction 13 kilobit audio codec.

 Value: 3

### CAPABILITY_ADD_PARTICIPANT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_ADD_PARTICIPANT: Int
```

When set, indicates that this Connection supports initiation of a conference call by directly adding participants using onAddConferenceParticipants. When participants are added to a Connection, it will be replaced by a Conference instance with `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_ADHOC_CONFERENCE:kotlin.Int` set to indicate that it is an adhoc conference call.

 Value: 67108864

### CAPABILITY_CANNOT_DOWNGRADE_VIDEO_TO_AUDIO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CANNOT_DOWNGRADE_VIDEO_TO_AUDIO: Int
```

When set, prevents a video call from being downgraded to an audio-only call.

Should be set when the VideoState has the `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int` bits set to indicate that the connection cannot be downgraded from a video call back to a VideoState of `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`.

Intuitively, a call which can be downgraded to audio should also have local and remote video capabilities (see `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_LOCAL_BIDIRECTIONAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_REMOTE_BIDIRECTIONAL:kotlin.Int`).

 Value: 8388608

### CAPABILITY_CAN_PAUSE_VIDEO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_PAUSE_VIDEO: Int
```

For video calls, indicates whether the outgoing video for the call can be paused using the `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int` VideoState.

 Value: 1048576

### CAPABILITY_CAN_PULL_CALL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_PULL_CALL: Int
```

When set for an external connection, indicates that this `Connection` can be pulled from a remote device to the current device.

Should only be set on a `Connection` where `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` is set.

 Value: 16777216

### CAPABILITY_CAN_SEND_RESPONSE_VIA_CONNECTION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_SEND_RESPONSE_VIA_CONNECTION: Int
```

Indicates that the connection itself wants to handle any sort of reply response, rather than relying on SMS.

 Value: 4194304

### CAPABILITY_CAN_UPGRADE_TO_VIDEO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_UPGRADE_TO_VIDEO: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_LOCAL_BIDIRECTIONAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORTS_VT_REMOTE_BIDIRECTIONAL:kotlin.Int` to indicate for a call whether or not video calling is supported.*

Call can be upgraded to a video call.

 Value: 524288

### CAPABILITY_DISCONNECT_FROM_CONFERENCE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_DISCONNECT_FROM_CONFERENCE: Int
```

Connection is able to be individually disconnected when in a `Conference`.

 Value: 8192

### CAPABILITY_HOLD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_HOLD: Int
```

Connection can currently be put on hold or unheld. This is distinct from `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_SUPPORT_HOLD:kotlin.Int` in that although a connection may support 'hold' most times, it does not at the moment support the function. This can be true while the call is in the state `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DIALING:kotlin.Int`, for example. During this condition, an in-call UI may display a disabled 'hold' button.

 Value: 1

### CAPABILITY_MANAGE_CONFERENCE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_MANAGE_CONFERENCE: Int
```

Connection supports conference management. This capability only applies to Conferences which can have Connections as children.

 Value: 128

### CAPABILITY_MERGE_CONFERENCE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_MERGE_CONFERENCE: Int
```

Connections within a conference can be merged. A ConnectionService has the option to add a Conference before the child Connections are merged. This is how CDMA-based Connections are implemented. For these unmerged Conferences, this capability allows a merge button to be shown while the conference is in the foreground of the in-call UI.

This is only intended for use by a Conference.

 Value: 4

### CAPABILITY_MUTE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_MUTE: Int
```

Connection can be muted.

 Value: 64

### CAPABILITY_REMOTE_PARTY_SUPPORTS_RTT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_REMOTE_PARTY_SUPPORTS_RTT: Int
```

Indicates whether the remote party supports RTT or not to the UI.

 Value: 536870912

### CAPABILITY_RESPOND_VIA_TEXT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_RESPOND_VIA_TEXT: Int
```

Connection supports responding via text option.

 Value: 32

### CAPABILITY_SEPARATE_FROM_CONFERENCE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SEPARATE_FROM_CONFERENCE: Int
```

Connection is able to be separated from its parent `Conference`, if any.

 Value: 4096

### CAPABILITY_SUPPORTS_VT_LOCAL_BIDIRECTIONAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_VT_LOCAL_BIDIRECTIONAL: Int
```

Local device supports bidirectional video calling.

 Value: 768

### CAPABILITY_SUPPORTS_VT_LOCAL_RX

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_VT_LOCAL_RX: Int
```

Local device supports receiving video.

 Value: 256

### CAPABILITY_SUPPORTS_VT_LOCAL_TX

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_VT_LOCAL_TX: Int
```

Local device supports transmitting video.

 Value: 512

### CAPABILITY_SUPPORTS_VT_REMOTE_BIDIRECTIONAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_VT_REMOTE_BIDIRECTIONAL: Int
```

Remote device supports bidirectional video calling.

 Value: 3072

### CAPABILITY_SUPPORTS_VT_REMOTE_RX

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_VT_REMOTE_RX: Int
```

Remote device supports receiving video.

 Value: 1024

### CAPABILITY_SUPPORTS_VT_REMOTE_TX

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORTS_VT_REMOTE_TX: Int
```

Remote device supports transmitting video.

 Value: 2048

### CAPABILITY_SUPPORT_DEFLECT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORT_DEFLECT: Int
```

Call supports the deflect feature.

 Value: 33554432

### CAPABILITY_SUPPORT_HOLD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SUPPORT_HOLD: Int
```

Connection supports the hold feature.

 Value: 2

### CAPABILITY_SWAP_CONFERENCE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SWAP_CONFERENCE: Int
```

Connections within a conference can be swapped between foreground and background. See `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_MERGE_CONFERENCE:kotlin.Int` for additional information.

This is only intended for use by a Conference.

 Value: 8

### CAPABILITY_TRANSFER

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_TRANSFER: Int
```

Indicates that this `Connection` can be transferred to another number. Connection supports the confirmed and unconfirmed call transfer feature.

 Value: 134217728

### CAPABILITY_TRANSFER_CONSULTATIVE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_TRANSFER_CONSULTATIVE: Int
```

Indicates that this `Connection` can perform a consultative transfer to another ongoing `Connection` that also has this capability. A consultative transfer request is initialted when onTransfer is called on a `Connection` with this capability. See 3GPP TS 24.629 for more details.

 Value: 268435456

### EVENT_CALL_HOLD_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_CALL_HOLD_FAILED: String
```

Connection event used to inform Telecom when a hold operation on a call has failed.

Sent via sendConnectionEvent. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is expected to be null when this connection event is used.

 Value: "android.telecom.event.CALL_HOLD_FAILED"

### EVENT_CALL_MERGE_FAILED

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_CALL_MERGE_FAILED: String
```

Connection event used to inform InCallServices when the merging of two calls has failed. The User Interface should use this message to inform the user of the error.

Sent via sendConnectionEvent. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is expected to be null when this connection event is used.

 Value: "android.telecom.event.CALL_MERGE_FAILED"

### EVENT_CALL_PULL_FAILED

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_CALL_PULL_FAILED: String
```

Connection event used to inform InCallServices when pulling of an external call has failed. The user interface should inform the user of the error.

Expected to be used by the ConnectionService when the pullExternalCall API is called on a Call with the properties `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#CAPABILITY_CAN_PULL_CALL:kotlin.Int`, but the ConnectionService could not pull the external call due to an error condition.

Sent via sendConnectionEvent. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is expected to be null when this connection event is used.

 Value: "android.telecom.event.CALL_PULL_FAILED"

### EVENT_CALL_REMOTELY_HELD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_CALL_REMOTELY_HELD: String
```

Connection event used to inform InCallServices when a call has been put on hold by the remote party.

This is different than the `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_HOLDING:kotlin.Int` state which indicates that the call is being held locally on the device. When a capable ConnectionService receives signalling to indicate that the remote party has put the call on hold, it can send this connection event.

 Value: "android.telecom.event.CALL_REMOTELY_HELD"

### EVENT_CALL_REMOTELY_UNHELD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_CALL_REMOTELY_UNHELD: String
```

Connection event used to inform InCallServices when a call which was remotely held (see `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_REMOTELY_HELD:kotlin.String`) has been un-held by the remote party.

This is different than the `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_HOLDING:kotlin.Int` state which indicates that the call is being held locally on the device. When a capable ConnectionService receives signalling to indicate that the remote party has taken the call off hold, it can send this connection event.

 Value: "android.telecom.event.CALL_REMOTELY_UNHELD"

### EVENT_CALL_RESUME_FAILED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_CALL_RESUME_FAILED: String
```

Connection event used to inform Telecom when a resume operation on a call has failed.

Sent via sendConnectionEvent. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is expected to be null when this connection event is used.

 Value: "android.telecom.event.CALL_RESUME_FAILED"

### EVENT_CALL_SWITCH_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_CALL_SWITCH_FAILED: String
```

Connection event used to inform Telecom when a switch operation on a call has failed.

Sent via sendConnectionEvent. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is expected to be null when this connection event is used.

 Value: "android.telecom.event.CALL_SWITCH_FAILED"

### EVENT_DISCONNECT_FAILED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_DISCONNECT_FAILED: String
```

Connection event used to inform Telecom when a disconnect request fails during a call merge.

Sent via sendConnectionEvent. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is expected to be null when this connection event is used.

 Value: "android.telecom.event.DISCONNECT_FAILED"

### EVENT_MERGE_COMPLETE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_MERGE_COMPLETE: String
```

Connection event used to inform InCallServices when the process of merging a Connection into a conference has completed.

Sent via sendConnectionEvent. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is expected to be null when this connection event is used.

 Value: "android.telecom.event.MERGE_COMPLETE"

### EVENT_MERGE_START

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_MERGE_START: String
```

Connection event used to inform InCallServices when the process of merging a Connection into a conference has begun.

Sent via sendConnectionEvent. The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is expected to be null when this connection event is used.

 Value: "android.telecom.event.MERGE_START"

### EVENT_ON_HOLD_TONE_END

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_ON_HOLD_TONE_END: String
```

Connection event used to inform Telecom that it should stop the on hold tone. This is used to stop a tone when the peer puts the current call on hold. Sent to Telecom via sendConnectionEvent.

 Value: "android.telecom.event.ON_HOLD_TONE_END"

### EVENT_ON_HOLD_TONE_START

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_ON_HOLD_TONE_START: String
```

Connection event used to inform Telecom that it should play the on hold tone. This is used to play a tone when the peer puts the current call on hold. Sent to Telecom via sendConnectionEvent.

 Value: "android.telecom.event.ON_HOLD_TONE_START"

### EVENT_RTT_AUDIO_INDICATION_CHANGED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_RTT_AUDIO_INDICATION_CHANGED: String
```

Connection event used to inform an InCallService that the RTT audio indication has changed.

 Value: "android.telecom.event.RTT_AUDIO_INDICATION_CHANGED"

### EXTRA_ANSWERING_DROPS_FG_CALL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ANSWERING_DROPS_FG_CALL: String
```

Boolean connection extra key set on a Connection in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` state to indicate that answering the call will cause the current active foreground call to be dropped.

 Value: "android.telecom.extra.ANSWERING_DROPS_FG_CALL"

### EXTRA_ANSWERING_DROPS_FG_CALL_APP_NAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ANSWERING_DROPS_FG_CALL_APP_NAME: String
```

String connection extra key set on a Connection in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int` state to indicate the name of the third-party app which is responsible for the current foreground call.

Used when `https://developer.android.com/reference/kotlin/android/telecom/Connection#EXTRA_ANSWERING_DROPS_FG_CALL:kotlin.String` is true to ensure that the default Phone app is able to inform the user that answering the new incoming call will cause a call owned by another app to be dropped when the incoming call is answered.

 Value: "android.telecom.extra.ANSWERING_DROPS_FG_CALL_APP_NAME"

### EXTRA_AUDIO_CODEC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUDIO_CODEC: String
```

The audio codec in use for the current Connection, if known. Examples of valid values include `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_AMR_WB:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVS_WB:kotlin.Int`. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_AMR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_AMR_WB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_QCELP13K:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVRC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVRC_B:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVRC_WB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVRC_NW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_GSM_EFR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_GSM_FR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_GSM_HR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G711U:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G723:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G711A:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G722:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G711AB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_G729:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVS_NB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVS_SWB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telecom/Connection#AUDIO_CODEC_EVS_FB:kotlin.Int`

<br />

 Value: "android.telecom.extra.AUDIO_CODEC"

### EXTRA_AUDIO_CODEC_BANDWIDTH_KHZ

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUDIO_CODEC_BANDWIDTH_KHZ: String
```

Float connection extra key used to store the audio codec bandwidth in khz for the current Connection.

 Value: "android.telecom.extra.AUDIO_CODEC_BANDWIDTH_KHZ"

### EXTRA_AUDIO_CODEC_BITRATE_KBPS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUDIO_CODEC_BITRATE_KBPS: String
```

Float connection extra key used to store the audio codec bitrate in kbps for the current Connection.

 Value: "android.telecom.extra.AUDIO_CODEC_BITRATE_KBPS"

### EXTRA_CALL_SUBJECT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_SUBJECT: String
```

Connection extra key used to store the subject for an incoming call. The user interface can query this extra and display its contents for incoming calls. Will only be used if the PhoneAccount supports the capability `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CALL_SUBJECT:kotlin.Int`.

 Value: "android.telecom.extra.CALL_SUBJECT"

### EXTRA_CHILD_ADDRESS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CHILD_ADDRESS: String
```

Connection extra key used to store a child number associated with the current connection. Used to communicate to the user interface that the connection was received via a child address (i.e. phone number) associated with the PhoneAccount's primary address.

 Value: "android.telecom.extra.CHILD_ADDRESS"

### EXTRA_IS_RTT_AUDIO_PRESENT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_RTT_AUDIO_PRESENT: String
```

Boolean connection extra key set on the extras passed to sendConnectionEvent which indicates that audio is present on the RTT call when the extra value is true.

 Value: "android.telecom.extra.IS_RTT_AUDIO_PRESENT"

### EXTRA_LAST_FORWARDED_NUMBER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LAST_FORWARDED_NUMBER: String
```

Connection extra key used to store the last forwarded number associated with the current connection. Used to communicate to the user interface that the connection was forwarded via the specified number.

 Value: "android.telecom.extra.LAST_FORWARDED_NUMBER"

### EXTRA_LAST_KNOWN_CELL_IDENTITY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LAST_KNOWN_CELL_IDENTITY: String
```

Last known cell identity key `https://developer.android.com/reference/kotlin/android/telephony/CellIdentity.html#` to be used to fill geo location header in case of an emergency call. This entry will not be filled if call is not identified as an emergency call. Only provided to the ConnectionService for the purpose of placing an emergency call; will not be present in the InCallService layer. The ConnectionService's implementation will be logged for fine location access when an outgoing call is placed in this case.

 Value: "android.telecom.extra.LAST_KNOWN_CELL_IDENTITY"

### EXTRA_SIP_INVITE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SIP_INVITE: String
```

String Connection extra key used to store SIP invite fields for an incoming call for IMS call

 Value: "android.telecom.extra.SIP_INVITE"

### PROPERTY_ASSISTED_DIALING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_ASSISTED_DIALING: Int
```

Set by the framework to indicate that a connection is using assisted dialing.

This is used for outgoing calls.

 Value: 512

**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#EXTRA_USE_ASSISTED_DIALING:kotlin.String`

### PROPERTY_CROSS_SIM

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_CROSS_SIM: Int
```

Connection is using cross sim technology.

Indicates that the Connection is using a cross sim technology which would register IMS over internet APN of default data subscription.

<br />

 Value: 8192

### PROPERTY_HAS_CDMA_VOICE_PRIVACY

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_HAS_CDMA_VOICE_PRIVACY: Int
```

Indicates that the connection has CDMA Enhanced Voice Privacy enabled.

 Value: 32

### PROPERTY_HIGH_DEF_AUDIO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_HIGH_DEF_AUDIO: Int
```

Connection is using high definition audio.

Indicates that the Connection is using a "high definition" audio codec. This usually implies something like AMR wideband, but the interpretation of when a call is considered high definition is left to the ConnectionService to decide.

Translates to `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_HIGH_DEF_AUDIO:kotlin.Int`.

 Value: 4

### PROPERTY_IS_ADHOC_CONFERENCE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_IS_ADHOC_CONFERENCE: Int
```

Set by the framework to indicate that a call is an adhoc conference call.

This is used for outgoing and incoming conference calls.

 Value: 4096

### PROPERTY_IS_EXTERNAL_CALL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_IS_EXTERNAL_CALL: Int
```

When set, indicates that the `Connection` does not actually exist locally for the ConnectionService.

Consider, for example, a scenario where a user has two devices with the same phone number. When a user places a call on one devices, the telephony stack can represent that call on the other device by adding is to the ConnectionService with the `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` capability set.

An ConnectionService should not assume that all InCallServices will handle external connections. Only those InCallServices which have the `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_EXTERNAL_CALLS:kotlin.String` metadata set to `true` in its manifest will see external connections.

 Value: 16

### PROPERTY_IS_RTT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_IS_RTT: Int
```

Set by the framework to indicate that a connection has an active RTT session associated with it.

 Value: 256

### PROPERTY_IS_TETHERED_CALL

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_IS_TETHERED_CALL: Int
```

Set by a ConnectionService to indicate that this Connection represents a tethered call synchronized from a primary device.

Consider, for example, a scenario where a user has a watch paired with a phone. When a user places a call on the phone, the telephony stack on the watch can represent that call by adding it to the ConnectionService with this property set.

When this property is set, the Telecom framework manages local audio focus to pause local media streams during an active call, as if that call was local. If the call does not possess this property but does have `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int`, local voice audio modes (e.g., `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#MODE_IN_CALL:kotlin.Int`) and speaker routing adjustments are bypassed.

This property cannot be set for calls with `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_SELF_MANAGED:kotlin.Int` also set.

 Value: 16384

### PROPERTY_NETWORK_IDENTIFIED_EMERGENCY_CALL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_NETWORK_IDENTIFIED_EMERGENCY_CALL: Int
```

Set by the framework to indicate that the network has identified a Connection as an emergency call.

This is used for incoming (mobile-terminated) calls to indicate the call is from emergency services.

 Value: 1024

### PROPERTY_SELF_MANAGED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SELF_MANAGED: Int
```

Set by the framework to indicate that the Connection originated from a self-managed ConnectionService.

See `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`.

 Value: 128

### PROPERTY_WIFI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_WIFI: Int
```

Connection is using WIFI.

Used to indicate that a call is taking place over WIFI versus a carrier network.

Translates to `https://developer.android.com/reference/kotlin/android/telecom/Call.Details#PROPERTY_WIFI:kotlin.Int`.

 Value: 8

### STATE_ACTIVE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_ACTIVE: Int
```

A connection is active. Both parties are connected to the call and can actively communicate.

 Value: 4

### STATE_AUDIO_PROCESSING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_AUDIO_PROCESSING: Int
```

The state of a call that is active with the network, but the audio from the call is being intercepted by an app on the local device. Telecom does not hold audio focus in this state, and the call will be invisible to the user except for a persistent notification.

 Value: 8

### STATE_DIALING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_DIALING: Int
```

An outgoing connection is in the dialing state. In this state the other party has not yet answered the call and the user traditionally hears a ringback tone.

 Value: 3

### STATE_DISCONNECTED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_DISCONNECTED: Int
```

A connection has been disconnected. This is the final state once the user has been disconnected from a call either locally, remotely or by an error in the service.

 Value: 6

### STATE_HOLDING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_HOLDING: Int
```

A connection is on hold.

 Value: 5

### STATE_INITIALIZING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_INITIALIZING: Int
```

The connection is initializing. This is generally the first state for a `Connection` returned by a ConnectionService.

 Value: 0

### STATE_NEW

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_NEW: Int
```

The connection is new and not connected.

 Value: 1

### STATE_PULLING_CALL

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_PULLING_CALL: Int
```

The state of an external connection which is in the process of being pulled from a remote device to the local device.

A connection can only be in this state if the `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` property and `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CAN_PULL_CALL:kotlin.Int` capability bits are set on the connection.

 Value: 7

### STATE_RINGING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_RINGING: Int
```

An incoming connection is in the ringing state. During this state, the user's ringer or vibration feature will be activated.

 Value: 2

### STATE_SIMULATED_RINGING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_SIMULATED_RINGING: Int
```

The state of a call that is being presented to the user after being in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_AUDIO_PROCESSING:kotlin.Int`. The call is still active with the network in this case, and Telecom will hold audio focus and play a ringtone if appropriate.

 Value: 9

### VERIFICATION_STATUS_FAILED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERIFICATION_STATUS_FAILED: Int
```

Indicates that verification by the network failed. This indicates there is a high likelihood that the call did not originate from a valid source.

 Value: 2

### VERIFICATION_STATUS_NOT_VERIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERIFICATION_STATUS_NOT_VERIFIED: Int
```

Indicates that the network could not perform verification.

 Value: 0

### VERIFICATION_STATUS_PASSED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERIFICATION_STATUS_PASSED: Int
```

Indicates that verification by the network passed. This indicates there is a high likelihood that the call originated from a valid source.

 Value: 1

## Public constructors

### Connection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Connection()
```

Create a new Connection.

## Public methods

### capabilitiesToString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun capabilitiesToString(capabilities: Int): String!
```

Renders a set of capability bits (`CAPABILITY_*`) as a human readable string.

| Parameters ||
|---|---|
| `capabilities` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A capability bit field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A human readable string representation. |

### createCanceledConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createCanceledConnection(): Connection!
```

Return a `Connection` which represents a canceled connection attempt. The returned `Connection` will have state `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DISCONNECTED:kotlin.Int`, and cannot be moved out of that state. This connection should not be used for anything, and no other `Connection`s should be attempted.

so users of this method need not maintain a reference to its return value to destroy it.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Connection#!` | A `Connection` which indicates that the underlying connection should be canceled. |

### createFailedConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFailedConnection(disconnectCause: DisconnectCause!): Connection!
```

Return a `Connection` which represents a failed connection attempt. The returned `Connection` will have a DisconnectCause and as specified, and a getState of `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_DISCONNECTED:kotlin.Int`.

The returned `Connection` can be assumed to destroy itself when appropriate, so users of this method need not maintain a reference to its return value to destroy it.

| Parameters ||
|---|---|
| `disconnectCause` | [DisconnectCause](DisconnectCause.md)!: The disconnect cause, (see android.telecomm.DisconnectCause). |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Connection#!` | A `Connection` which indicates failure. |

### destroy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun destroy(): Unit
```

Tears down the Connection object.

### getAddress

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddress(): Uri!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | The address (e.g., phone number) to which this Connection is currently communicating. |

### getAddressPresentation

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddressPresentation(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The presentation requirements for the address. See TelecomManager for valid values. |

### getAudioModeIsVoip

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAudioModeIsVoip(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the connection's audio mode is VOIP. |

### getAudioProcessingUseCase

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAudioProcessingUseCase(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The audio processing use case of the call when the state is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_AUDIO_PROCESSING:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/Call#AUDIO_PROCESSING_USE_CASE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call#AUDIO_PROCESSING_USE_CASE_VOICEMAIL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call#AUDIO_PROCESSING_USE_CASE_CALL_SCREENING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call#AUDIO_PROCESSING_USE_CASE_ASK_TO_HOLD:kotlin.Int` |

### getCallAudioState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallAudioState(): CallAudioState!
```

**Deprecated:** *Use getCurrentCallEndpoint, onAvailableCallEndpointsChanged and onMuteStateChanged instead.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState!` | The audio state of the connection, describing how its audio is currently being routed by the system. This is `null` if this Connection does not directly know about its audio state. |

### getCallerDisplayName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallerDisplayName(): String!
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The caller display name (CNAP). |

### getCallerDisplayNamePresentation

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallerDisplayNamePresentation(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The presentation requirements for the handle. See TelecomManager for valid values. |

### getCallerNumberVerificationStatus

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallerNumberVerificationStatus(): Int
```

Gets the verification status for the phone number of an incoming call as identified in ATIS-1000082.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the verification status. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_NOT_VERIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_PASSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_FAILED:kotlin.Int` |

### getConference

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConference(): Conference!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Conference!` | The conference that this connection is a part of. Null if it is not part of any conference. |

### getConferenceables

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConferenceables(): MutableList<Conferenceable!>!
```

Returns the connections or conferences with which this connection can be conferenced.

### getConnectionCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionCapabilities(): Int
```

Returns the connection's capabilities, as a bit mask of the `CAPABILITY_*` constants.

### getConnectionProperties

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionProperties(): Int
```

Returns the connection's properties, as a bit mask of the `PROPERTY_*` constants.

### getCurrentCallEndpoint

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCurrentCallEndpoint(): CallEndpoint
```

Obtains the current CallEndpoint.

| Return ||
|---|---|
| CallEndpoint | An object encapsulating the CallEndpoint. This value cannot be `null`. |

### getDisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisconnectCause(): DisconnectCause!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause!` | The DisconnectCause for this connection. |

### getExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle!
```

Returns the extras associated with this connection.

Extras should be updated using putExtras.

Telecom or an InCallService can also update the extras via putExtras, and removeExtras.

The connection is notified of changes to the extras made by Telecom or an InCallService by onExtrasChanged.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | The extras associated with this connection. |

### getState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getState(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The state of this Connection. |

### getStatusHints

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStatusHints(): StatusHints!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/StatusHints!` | The status hints for this connection. |

### getVideoProvider

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoProvider(): Connection.VideoProvider!
```

### getVideoState

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoState(): Int
```

Returns the video state of the connection. Valid values: `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The video state of the connection. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int` |

### handleRttUpgradeResponse

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun handleRttUpgradeResponse(rttTextStream: Connection.RttTextStream?): Unit
```

Notifies this connection of a response to a previous remotely-initiated RTT upgrade request sent via sendRemoteRttRequest. Acceptance of the request is indicated by the supplied `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttTextStream` being non-null, and rejection is indicated by `rttTextStream` being `null`

| Parameters ||
|---|---|
| `rttTextStream` | [Connection.RttTextStream](../android/telecom/Connection.RttTextStream.md)?: The object that should be used to send text to or receive text from the in-call app. This value may be `null`. |

### isRingbackRequested

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRingbackRequested(): Boolean
```

Returns whether this connection is requesting that the system play a ringback tone on its behalf.

### notifyConferenceMergeFailed

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifyConferenceMergeFailed(): Unit
```

Called by a ConnectionService to notify Telecom that a onMerge request failed.

### onAbort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAbort(): Unit
```

Notifies this Connection of a request to abort.

### onAddConferenceParticipants

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAddConferenceParticipants(participants: MutableList<Uri!>): Unit
```

Supports initiation of a conference call by directly adding participants to an ongoing call.

| Parameters ||
|---|---|
| `participants` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\>: with which conference call will be formed. This value cannot be `null`. |

### onAnswer

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAnswer(): Unit
```

Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to accept.

For managed ConnectionServices, this will be called when the user answers a call via the default dialer's InCallService.

Although a self-managed ConnectionService provides its own incoming call UI, the Telecom framework may request that the call is answered in the following circumstances:

- The user chooses to answer an incoming call via a Bluetooth device.
- A car mode InCallService is in use which has declared `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_SELF_MANAGED_CALLS:kotlin.String` in its manifest. Such an InCallService will be able to see calls from self-managed ConnectionServices, and will be able to display an incoming call UI on their behalf.

### onAnswer

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAnswer(videoState: Int): Unit
```

Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to accept.

For managed ConnectionServices, this will be called when the user answers a call via the default dialer's InCallService.

Although a self-managed ConnectionService provides its own incoming call UI, the Telecom framework may request that the call is answered in the following circumstances:

- The user chooses to answer an incoming call via a Bluetooth device.
- A car mode InCallService is in use which has declared `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_SELF_MANAGED_CALLS:kotlin.String` in its manifest. Such an InCallService will be able to see calls from self-managed ConnectionServices, and will be able to display an incoming call UI on their behalf.

| Parameters ||
|---|---|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The video state in which to answer the connection. |

### onAvailableCallEndpointsChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAvailableCallEndpointsChanged(availableEndpoints: MutableList<CallEndpoint!>): Unit
```

Notifies this Connection that the available call endpoints have been changed.

| Parameters ||
|---|---|
| `availableEndpoints` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CallEndpoint](CallEndpoint.md)!\>: The set of available CallEndpoint. This value cannot be `null`. |

### onCallAudioStateChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCallAudioStateChanged(state: CallAudioState!): Unit
```

**Deprecated:** *Use onCallEndpointChanged, onAvailableCallEndpointsChanged and onMuteStateChanged instead.*

Notifies this Connection that the getCallAudioState property has a new value.

| Parameters ||
|---|---|
| `state` | [CallAudioState](CallAudioState.md)!: The new connection audio state. |

### onCallEndpointChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCallEndpointChanged(callEndpoint: CallEndpoint): Unit
```

Notifies this Connection that the audio endpoint has been changed.

| Parameters ||
|---|---|
| `callEndpoint` | [CallEndpoint](CallEndpoint.md): The current CallEndpoint. This value cannot be `null`. |

### onCallEvent

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCallEvent(
    event: String!, 
    extras: Bundle!
): Unit
```

Notifies this Connection of a Call event initiated from an InCallService.

The InCallService issues a Call event via sendCallEvent.

Where possible, the Connection should make an attempt to handle Call events which are part of the `android.telecom.*` namespace. The Connection should ignore any events it does not wish to handle. Unexpected events should be handled gracefully, as it is possible that a InCallService has defined its own Call events which a Connection is not aware of.

See also sendCallEvent.

| Parameters ||
|---|---|
| `event` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The call event. |
| `extras` | [Bundle](../android.os/Bundle.md)!: Extras associated with the call event. |

### onDeflect

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDeflect(address: Uri!): Unit
```

Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to deflect.

### onDisconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDisconnect(): Unit
```

Notifies this Connection of a request to disconnect.

### onExtrasChanged

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExtrasChanged(extras: Bundle!): Unit
```

Notifies this Connection of a change to the extras made outside the ConnectionService.

These extras changes can originate from Telecom itself, or from an InCallService via the putExtras and removeExtras.

| Parameters ||
|---|---|
| `extras` | [Bundle](../android.os/Bundle.md)!: The new extras bundle. |

### onHandoverComplete

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHandoverComplete(): Unit
```

Notifies this Connection that a handover has completed.

A handover is initiated with handoverTo on the initiating side of the handover, and acceptHandover.

### onHold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHold(): Unit
```

Notifies this Connection of a request to hold. setOnHold should be within the onHold() body in order to transition the call state to `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_HOLDING:kotlin.Int`.

Note: If the Connection does not transition to `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_HOLDING:kotlin.Int` within 2 seconds, the call will be disconnected.

### onMuteStateChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onMuteStateChanged(isMuted: Boolean): Unit
```

Notifies this Connection that its audio mute state has been changed.

| Parameters ||
|---|---|
| `isMuted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The current mute state. |

### onPlayDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPlayDtmfTone(c: Char): Unit
```

Notifies this Connection of a request to play a DTMF tone.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): A DTMF character. |

### onPostDialContinue

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPostDialContinue(proceed: Boolean): Unit
```

Notifies this Connection whether the user wishes to proceed with the post-dial DTMF codes.

### onPullExternalCall

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPullExternalCall(): Unit
```

Notifies this Connection of a request to pull an external call to the local device.

The InCallService issues a request to pull an external call to the local device via pullExternalCall.

For a Connection to be pulled, both the `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CAN_PULL_CALL:kotlin.Int` capability and `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` property bits must be set.

For more information on external calls, see `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int`.

### onReject

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReject(): Unit
```

Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to reject.

For managed ConnectionServices, this will be called when the user rejects a call via the default dialer's InCallService.

Although a self-managed ConnectionService provides its own incoming call UI, the Telecom framework may request that the call is rejected in the following circumstances:

- The user chooses to reject an incoming call via a Bluetooth device.
- A car mode InCallService is in use which has declared `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#METADATA_INCLUDE_SELF_MANAGED_CALLS:kotlin.String` in its manifest. Such an InCallService will be able to see calls from self-managed ConnectionServices, and will be able to display an incoming call UI on their behalf.

### onReject

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReject(rejectReason: Int): Unit
```

Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to reject.

For managed ConnectionServices, this will be called when the user rejects a call via the default dialer's InCallService using reject.

| Parameters ||
|---|---|
| `rejectReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the reason the user provided for rejecting the call. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/Call#REJECT_REASON_DECLINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call#REJECT_REASON_UNWANTED:kotlin.Int` |

### onReject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReject(replyMessage: String!): Unit
```

Notifies this Connection, which is in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_RINGING:kotlin.Int`, of a request to reject with a message.

### onSeparate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSeparate(): Unit
```

Notifies this Connection of a request to separate from its parent conference.

### onShowIncomingCallUi

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onShowIncomingCallUi(): Unit
```

Notifies this Connection that its ConnectionService is responsible for displaying its incoming call user interface for the Connection

Will only be called for incoming calls added via a self-managed ConnectionService (see `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`), where the ConnectionService should show its own incoming call user interface.

Where there are ongoing calls in other self-managed ConnectionServices, or in a regular ConnectionService, and it is not possible to hold these other calls, the Telecom framework will display its own incoming call user interface to allow the user to choose whether to answer the new incoming call and disconnect other ongoing calls, or to reject the new incoming call.

You should trigger the display of the incoming call user interface for your application by showing a `https://developer.android.com/reference/kotlin/android/app/Notification.html#` with a full-screen `https://developer.android.com/reference/kotlin/android/content/Intent.html#` specified. In your application code, you should create a `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#` for incoming call notifications from your app:

```kotlin
<code>
  NotificationChannel channel = new NotificationChannel(YOUR_CHANNEL_ID, "Incoming Calls",
           NotificationManager.IMPORTANCE_MAX);
  // other channel setup stuff goes here.
 
  // We'll use the default system ringtone for our incoming call notification channel.  You can
  // use your own audio resource here.
  Uri ringtoneUri = RingtoneManager.getDefaultUri(RingtoneManager.TYPE_RINGTONE);
  channel.setSound(ringtoneUri, new AudioAttributes.Builder()
           // Setting the AudioAttributes is important as it identifies the purpose of your
           // notification sound.
           .setUsage(AudioAttributes.USAGE_NOTIFICATION_RINGTONE)
           .setContentType(AudioAttributes.CONTENT_TYPE_SONIFICATION)
       .build());
 
  NotificationManager mgr = getSystemService(NotificationManager.class);
  mgr.createNotificationChannel(channel);
  </code>
```
When it comes time to post a notification for your incoming call, ensure it uses your incoming call `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#`.

```kotlin
<code>
      // Create an intent which triggers your fullscreen incoming call user interface.
      Intent intent = new Intent(Intent.ACTION_MAIN, null);
      intent.setFlags(Intent.FLAG_ACTIVITY_NO_USER_ACTION | Intent.FLAG_ACTIVITY_NEW_TASK);
      intent.setClass(context, YourIncomingCallActivity.class);
      PendingIntent pendingIntent = PendingIntent.getActivity(context, 1, intent, PendingIntent.FLAG_MUTABLE_UNAUDITED);
 
      // Build the notification as an ongoing high priority item; this ensures it will show as
      // a heads up notification which slides down over top of the current content.
      final Notification.Builder builder = new Notification.Builder(context);
      builder.setOngoing(true);
      builder.setPriority(Notification.PRIORITY_HIGH);
 
      // Set notification content intent to take user to fullscreen UI if user taps on the
      // notification body.
      builder.setContentIntent(pendingIntent);
      // Set full screen intent to trigger display of the fullscreen UI when the notification
      // manager deems it appropriate.
      builder.setFullScreenIntent(pendingIntent, true);
 
      // Setup notification content.
      builder.setSmallIcon( yourIconResourceId );
      builder.setContentTitle("Your notification title");
      builder.setContentText("Your notification content.");
 
      // Set notification as insistent to cause your ringtone to loop.
      Notification notification = builder.build();
      notification.flags |= Notification.FLAG_INSISTENT;
 
      // Use builder.addAction(..) to add buttons to answer or reject the call.
      NotificationManager notificationManager = mContext.getSystemService(
          NotificationManager.class);
      notificationManager.notify(YOUR_CHANNEL_ID, YOUR_TAG, YOUR_ID, notification);
  </code>
```

### onSilence

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSilence(): Unit
```

Notifies this Connection of a request to silence the ringer.

The ringer may be silenced by any of the following methods:

- silenceRinger
- The user presses the volume-down button while a call is ringing.

Self-managed ConnectionService implementations should override this method in their Connection implementation and implement logic to silence their app's ringtone. If your app set the ringtone as part of the incoming call `https://developer.android.com/reference/kotlin/android/app/Notification.html#` (see onShowIncomingCallUi), it should re-post the notification now, except call setOnlyAlertOnce with `true`. This will ensure the ringtone sound associated with your `https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#` stops playing.

### onStartRtt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartRtt(rttTextStream: Connection.RttTextStream): Unit
```

Notifies this Connection that the user has requested an RTT session. The connection service should call sendRttInitiationSuccess or sendRttInitiationFailure to inform Telecom of the success or failure of the request, respectively.

| Parameters ||
|---|---|
| `rttTextStream` | [Connection.RttTextStream](../android/telecom/Connection.RttTextStream.md): The object that should be used to send text to or receive text from the in-call app. This value cannot be `null`. |

### onStateChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStateChanged(state: Int): Unit
```

Notifies this Connection of an internal state change. This method is called after the state is changed.

| Parameters ||
|---|---|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new state, one of the `STATE_*` constants. |

### onStopDtmfTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStopDtmfTone(): Unit
```

Notifies this Connection of a request to stop any currently playing DTMF tones.

### onStopRtt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStopRtt(): Unit
```

Notifies this Connection that it should terminate any existing RTT communication channel. No response to Telecom is needed for this method.

### onTrackedByNonUiService

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTrackedByNonUiService(isTracked: Boolean): Unit
```

Inform this Conenection when it will or will not be tracked by an non-UI InCallService.

| Parameters ||
|---|---|
| `isTracked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Indicates whether an non-UI InCallService is currently tracking the self-managed call. |

### onTransfer

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTransfer(
    address: Uri, 
    isConfirmationRequired: Boolean
): Unit
```

Notifies this Connection of a request to transfer to a target number.

| Parameters ||
|---|---|
| `address` | [Uri](../android.net/Uri.md): the address to transfer this Connection to. This value cannot be `null`. |
| `isConfirmationRequired` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): when `true`, the ConnectionService should wait until the transfer has successfully completed before disconnecting the current Connection, also known as an assured transfer. When `false`, the ConnectionService should signal the network to perform the transfer, but should immediately disconnect the call regardless of the outcome of the transfer, also known as a blind transfer. |

### onTransfer

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTransfer(toConnection: Connection): Unit
```

Notifies this Connection of a request to start a CONSULTATIVE transfer to another Connection. See 3GPP TS 24.629 for more details.

| Parameters ||
|---|---|
| `toConnection` | [Connection](Connection.md): the Connection to transfer this call to. This value cannot be `null`. |

### onUnhold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUnhold(): Unit
```

Notifies this Connection of a request to exit a hold state.

### onUsingAlternativeUi

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUsingAlternativeUi(isUsingAlternativeUi: Boolean): Unit
```

Inform this Connection when it will or will not be tracked by an InCallService which can provide an InCall UI. This is primarily intended for use by Connections reported by self-managed ConnectionService which typically maintain their own UI.

| Parameters ||
|---|---|
| `isUsingAlternativeUi` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Indicates whether an InCallService that can provide InCall UI is currently tracking the self-managed call. |

### propertiesToString

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun propertiesToString(properties: Int): String!
```

Renders a set of property bits (`PROPERTY_*`) as a human readable string.

| Parameters ||
|---|---|
| `properties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A property bit field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A human readable string representation. |

### putExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putExtras(extras: Bundle): Unit
```

Adds some extras to this `Connection`. Existing keys are replaced and new ones are added.

No assumptions should be made as to how an In-Call UI or service will handle these extras. Keys should be fully qualified (e.g., com.example.MY_EXTRA) to avoid conflicts.

| Parameters ||
|---|---|
| `extras` | [Bundle](../android.os/Bundle.md): The extras to add. This value cannot be `null`. |

### queryLocationForEmergency

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryLocationForEmergency(
    timeoutMillis: Long, 
    provider: String, 
    executor: Executor, 
    callback: OutcomeReceiver<Location!, QueryLocationException!>
): Unit
```

Query the device's location in order to place an Emergency Call. Only SIM call managers can call this method for Connections representing Emergency calls. If a previous location query request is not completed, the new location query request will be rejected and return a QueryLocationException with `QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS`

| Parameters ||
|---|---|
| `timeoutMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): long: Timeout in millis waiting for query response (MAX:5000, MIN:100). Value is between 100 and 5000 inclusive |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): String: the location provider name, This value cannot be null. It is the caller's responsibility to select an enabled provider. The caller can use getProviders to choose one of the enabled providers and pass it in. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor of where the callback will execute. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Location](../android.location/Location.md)!, [QueryLocationException](QueryLocationException.md)!\>: The callback to notify the result of queryLocation. This value cannot be `null`. |

### removeExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeExtras(vararg keys: String!): Unit
```

Removes extras from this `Connection`.

| Parameters ||
|---|---|
| `keys` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The keys of the extras to remove. |

### removeExtras

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeExtras(keys: MutableList<String!>!): Unit
```

Removes extras from this `Connection`.

| Parameters ||
|---|---|
| `keys` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: The keys of the extras to remove. |

### requestBluetoothAudio

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestBluetoothAudio(bluetoothDevice: BluetoothDevice): Unit
```

**Deprecated:** *Use requestCallEndpointChange instead.*

Request audio routing to a specific bluetooth device. Calling this method may result in the device routing audio to a different bluetooth device than the one specified if the bluetooth stack is unable to route audio to the requested device. A list of available devices can be obtained via getSupportedBluetoothDevices

Used by self-managed ConnectionServices which wish to use bluetooth audio for a self-managed Connection (see `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`.)

See also requestBluetoothAudio

| Parameters ||
|---|---|
| `bluetoothDevice` | [BluetoothDevice](../android.bluetooth/BluetoothDevice.md): The bluetooth device to connect to. This value cannot be `null`. |

### requestCallEndpointChange

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestCallEndpointChange(
    endpoint: CallEndpoint, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, CallEndpointException!>
): Unit
```

Request audio routing to a specific CallEndpoint. Clients should not define their own CallEndpoint when requesting a change. Instead, the new endpoint should be one of the valid endpoints provided by onAvailableCallEndpointsChanged. When this request is honored, there will be change to the getCurrentCallEndpoint.

Used by self-managed ConnectionServices which wish to change the CallEndpoint for a self-managed Connection (see `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`.)

See also requestCallEndpointChange.

| Parameters ||
|---|---|
| `endpoint` | [CallEndpoint](CallEndpoint.md): The call endpoint to use. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor of where the callback will execute. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [CallEndpointException](CallEndpointException.md)!\>: The callback to notify the result of the endpoint change. This value cannot be `null`. |
| --- | --- |

### sendConnectionEvent

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendConnectionEvent(
    event: String!, 
    extras: Bundle!
): Unit
```

Sends an event associated with this `Connection` with associated event extras to the InCallService.

Connection events are used to communicate point in time information from a ConnectionService to a InCallService implementations. An example of a custom connection event includes notifying the UI when a WIFI call has been handed over to LTE, which the InCall UI might use to inform the user that billing charges may apply. The Android Telephony framework will send the `https://developer.android.com/reference/kotlin/android/telecom/Connection#EVENT_CALL_MERGE_FAILED:kotlin.String` connection event when a call to mergeConference has failed to complete successfully. A connection event could also be used to trigger UI in the InCallService which prompts the user to make a choice (e.g. whether they want to incur roaming costs for making a call), which is communicated back via sendCallEvent.

Events are exposed to InCallService implementations via onConnectionEvent.

No assumptions should be made as to how an In-Call UI or service will handle these events. The ConnectionService must assume that the In-Call UI could even chose to ignore some events altogether.

Events should be fully qualified (e.g. `com.example.event.MY_EVENT`) to avoid conflicts between ConnectionService implementations. Further, custom ConnectionService implementations shall not re-purpose events in the `android.*` namespace, nor shall they define new event types in this namespace. When defining a custom event type, ensure the contents of the extras `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` is clearly defined. Extra keys for this bundle should be named similar to the event type (e.g. `com.example.extra.MY_EXTRA`).

When defining events and the associated extras, it is important to keep their behavior consistent when the associated ConnectionService is updated. Support for deprecated events/extras should me maintained to ensure backwards compatibility with older InCallService implementations which were built to support the older behavior.

| Parameters ||
|---|---|
| `event` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The connection event. |
| `extras` | [Bundle](../android.os/Bundle.md)!: Optional bundle containing extra information associated with the event. |

### sendRemoteRttRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendRemoteRttRequest(): Unit
```

Informs listeners that the remote side of the call has requested an upgrade to include an RTT session in the call.

### sendRttInitiationFailure

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendRttInitiationFailure(reason: Int): Unit
```

Informs listeners that a previously requested RTT session via isRequestingRtt or onStartRtt has failed.

| Parameters ||
|---|---|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of the reason codes defined in `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttModifyStatus`, with the exception of `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttModifyStatus#SESSION_MODIFY_REQUEST_SUCCESS:kotlin.Int`. |

### sendRttInitiationSuccess

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendRttInitiationSuccess(): Unit
```

Informs listeners that a previously requested RTT session via isRequestingRtt or onStartRtt has succeeded.

### sendRttSessionRemotelyTerminated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendRttSessionRemotelyTerminated(): Unit
```

Informs listeners that a currently active RTT session has been terminated by the remote side of the coll.

### setActive

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setActive(): Unit
```

Sets state to active (e.g., an ongoing connection where two or more parties can actively communicate).

### setAddress

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAddress(
    address: Uri!, 
    presentation: Int
): Unit
```

Sets the value of the getAddress property.

| Parameters ||
|---|---|
| `address` | [Uri](../android.net/Uri.md)!: The new address. |
| `presentation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The presentation requirements for the address. See TelecomManager for valid values. |

### setAudioModeIsVoip

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAudioModeIsVoip(isVoip: Boolean): Unit
```

Requests that the framework use VOIP audio mode for this connection.

| Parameters ||
|---|---|
| `isVoip` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the audio mode is VOIP. |

### setAudioProcessing

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAudioProcessing(useCase: Int): Unit
```

Sets state to audio processing (e.g. the call is active but the audio from the call is being intercepted by an app on the local device) and the usecase. This is applicable only for an `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int`

| Parameters ||
|---|---|
| `useCase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One of android.telecom.Call.AudioProcessingUseCase for when the call is in state `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_AUDIO_PROCESSING:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/Call#AUDIO_PROCESSING_USE_CASE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call#AUDIO_PROCESSING_USE_CASE_VOICEMAIL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call#AUDIO_PROCESSING_USE_CASE_CALL_SCREENING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Call#AUDIO_PROCESSING_USE_CASE_ASK_TO_HOLD:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if called on a non-external call. |

### setAudioRoute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAudioRoute(route: Int): Unit
```

**Deprecated:** *Use requestCallEndpointChange instead.*

Sets the audio route (speaker, bluetooth, etc...). When this request is honored, there will be change to the getCallAudioState.

Used by self-managed ConnectionServices which wish to change the audio route for a self-managed Connection (see `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_SELF_MANAGED:kotlin.Int`.)

See also setAudioRoute.

| Parameters ||
|---|---|
| `route` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The audio route to use (one of `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_EARPIECE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_SPEAKER:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_HEADSET:kotlin.Int`). |

### setCallerDisplayName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCallerDisplayName(
    callerDisplayName: String!, 
    presentation: Int
): Unit
```

Sets the caller display name (CNAP).

| Parameters ||
|---|---|
| `callerDisplayName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The new display name. |
| `presentation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The presentation requirements for the handle. See TelecomManager for valid values. |

### setCallerNumberVerificationStatus

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCallerNumberVerificationStatus(callerNumberVerificationStatus: Int): Unit
```

Sets the verification status for the phone number of an incoming call as identified in ATIS-1000082.

This property can only be set at the time of creation of a Connection being returned by onCreateIncomingConnection.

| Parameters ||
|---|---|
| `callerNumberVerificationStatus` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_NOT_VERIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_PASSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/Connection#VERIFICATION_STATUS_FAILED:kotlin.Int` |

### setConferenceableConnections

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConferenceableConnections(conferenceableConnections: MutableList<Connection!>!): Unit
```

Sets the connections with which this connection can be conferenced.

| Parameters ||
|---|---|
| `conferenceableConnections` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Connection](Connection.md)!\>!: The set of connections this connection can conference with. |

### setConferenceables

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConferenceables(conferenceables: MutableList<Conferenceable!>!): Unit
```

Similar to setConferenceableConnections, sets a list of connections or conferences with which this connection can be conferenced.

| Parameters ||
|---|---|
| `conferenceables` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Conferenceable](Conferenceable.md)!\>!: The conferenceables. |

### setConnectionCapabilities

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConnectionCapabilities(connectionCapabilities: Int): Unit
```

Sets the connection's capabilities as a bit mask of the `CAPABILITY_*` constants.

| Parameters ||
|---|---|
| `connectionCapabilities` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new connection capabilities. |

### setConnectionProperties

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConnectionProperties(connectionProperties: Int): Unit
```

Sets the connection's properties as a bit mask of the `PROPERTY_*` constants.

| Parameters ||
|---|---|
| `connectionProperties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new connection properties. |

### setDialing

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDialing(): Unit
```

Sets state to dialing (e.g., dialing an outbound connection). The Connection should not be in STATE_DIALING for more than 60 seconds. After 60 seconds, the Connection will be disconnected.

### setDisconnected

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDisconnected(disconnectCause: DisconnectCause!): Unit
```

Sets state to disconnected.

| Parameters ||
|---|---|
| `disconnectCause` | [DisconnectCause](DisconnectCause.md)!: The reason for the disconnection, as specified by DisconnectCause. |

### setExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setExtras(extras: Bundle?): Unit
```

Set some extras that can be associated with this `Connection`.

New or existing keys are replaced in the `Connection` extras. Keys which are no longer in the new extras, but were present the last time `setExtras` was called are removed.

Alternatively you may use the putExtras, and removeExtras methods to modify the extras.

No assumptions should be made as to how an In-Call UI or service will handle these extras. Keys should be fully qualified (e.g., com.example.MY_EXTRA) to avoid conflicts.

| Parameters ||
|---|---|
| `extras` | [Bundle](../android.os/Bundle.md)?: The extras associated with this `Connection`. This value may be `null`. |

### setInitialized

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setInitialized(): Unit
```

Sets state to initialized (the Connection has been set up and is now ready to be used).

### setInitializing

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setInitializing(): Unit
```

Sets state to initializing (this Connection is not yet ready to be used).

### setNextPostDialChar

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setNextPostDialChar(nextChar: Char): Unit
```

Informs listeners that this `Connection` has processed a character in the post-dial started state. This is done when (a) the `Connection` is issuing a DTMF sequence; and (b) it wishes to signal Telecom to play the corresponding DTMF tone locally.

| Parameters ||
|---|---|
| `nextChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The DTMF character that was just processed by the `Connection`. |

### setOnHold

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOnHold(): Unit
```

Sets state to be on hold.

### setPostDialWait

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPostDialWait(remaining: String!): Unit
```

Informs listeners that this `Connection` is in a post-dial wait state. This is done when (a) the `Connection` is issuing a DTMF sequence; (b) it has encountered a "wait" character; and (c) it wishes to inform the In-Call app that it is waiting for the end-user to send an onPostDialContinue signal.

| Parameters ||
|---|---|
| `remaining` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The DTMF character sequence remaining to be emitted once the onPostDialContinue is received, including any "wait" characters that remaining sequence may contain. |

### setPulling

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPulling(): Unit
```

Sets state to pulling (e.g. the connection is being pulled to the local device from another device). Only applicable for Connections with `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telecom/Connection#CAPABILITY_CAN_PULL_CALL:kotlin.Int`.

### setRingbackRequested

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRingbackRequested(ringback: Boolean): Unit
```

Requests that the framework play a ringback tone. This is to be invoked by implementations that do not play a ringback tone themselves in the connection's audio stream.

| Parameters ||
|---|---|
| `ringback` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the ringback tone is to be played. |

### setRinging

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRinging(): Unit
```

Sets state to ringing (e.g., an inbound ringing connection). The Connection should not be in STATE_RINGING for more than 60 seconds. After 60 seconds, the Connection will be disconnected.

### setSimulatedRinging

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSimulatedRinging(): Unit
```

Sets state to simulated ringing where its presented to the user after being in `https://developer.android.com/reference/kotlin/android/telecom/Connection#STATE_AUDIO_PROCESSING:kotlin.Int`. This is applicable only for an `https://developer.android.com/reference/kotlin/android/telecom/Connection#PROPERTY_IS_EXTERNAL_CALL:kotlin.Int`

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the call is non-external. |

### setStatusHints

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setStatusHints(statusHints: StatusHints!): Unit
```

Sets the label and icon status to display in the in-call UI.

| Parameters ||
|---|---|
| `statusHints` | [StatusHints](StatusHints.md)!: The status label and icon to set. |

### setVideoProvider

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setVideoProvider(videoProvider: Connection.VideoProvider!): Unit
```

Sets the video connection provider.

| Parameters ||
|---|---|
| `videoProvider` | [Connection.VideoProvider](../android/telecom/Connection.VideoProvider.md)!: The video provider. |

### setVideoState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setVideoState(videoState: Int): Unit
```

Set the video state for the connection. Valid values: `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int`.

| Parameters ||
|---|---|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new video state. |

### stateToString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun stateToString(state: Int): String!
```

| Parameters ||
|---|---|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An integer value of a `STATE_*` constant. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A string representation of the value. |
