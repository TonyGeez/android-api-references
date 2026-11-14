# TvInputManager

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvInputManager

Kotlin| [Java](TvInputManager.md) 
| --- | --- |

```
class TvInputManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.TvInputManager](TvInputManager.md) |

Central system API to the overall TV input framework (TIF) architecture, which arbitrates interaction between applications and the selected TV inputs.

There are three primary parties involved in the TV input framework (TIF) architecture:

- The**TV input manager**as expressed by this class is the central point of the system that manages interaction between all other parts. It is expressed as the client-side API here which exists in each application context and communicates with a global system service that manages the interaction across all processes.
- A**TV input** implemented by [TvInputService](TvInputService.md) represents an input source of TV, which can be a pass-through input such as HDMI, or a tuner input which provides broadcast TV programs. The system binds to the TV input per application's request. on implementing TV inputs.
- **Applications** talk to the TV input manager to list TV inputs and check their status. Once an application find the input to use, it uses [TvView](TvView.md) or [TvRecordingClient](TvRecordingClient.md) for further interaction such as watching and recording broadcast TV programs.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md) Callback used to monitor status of the TV inputs. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_BLOCKED_RATINGS_CHANGED](TvInputManager.md) Broadcast intent action when the user blocked content ratings change. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_PARENTAL_CONTROLS_ENABLED_CHANGED](TvInputManager.md) Broadcast intent action when the parental controls enabled state changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_QUERY_CONTENT_RATING_SYSTEMS](TvInputManager.md) Broadcast intent action used to query available content rating systems. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SETUP_INPUTS](TvInputManager.md) Activity action to set up channel sources i. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_VIEW_RECORDING_SCHEDULES](TvInputManager.md) Activity action to display the recording schedules. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BROADCAST_INFO_STREAM_EVENT](TvInputManager.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BROADCAST_INFO_TYPE_COMMAND](TvInputManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BROADCAST_INFO_TYPE_DSMCC](TvInputManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BROADCAST_INFO_TYPE_PES](TvInputManager.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BROADCAST_INFO_TYPE_SECTION](TvInputManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BROADCAST_INFO_TYPE_TABLE](TvInputManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BROADCAST_INFO_TYPE_TIMELINE](TvInputManager.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BROADCAST_INFO_TYPE_TS](TvInputManager.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_STATE_CONNECTED](TvInputManager.md) State for [getInputState(java.lang.String)](TvInputManager.md))and [TvInputCallback.onInputStateChanged(String, int)](../android/media/tv/TvInputManager.TvInputCallback.md)): The input source is connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_STATE_CONNECTED_STANDBY](TvInputManager.md) State for [getInputState(java.lang.String)](TvInputManager.md))and [TvInputCallback.onInputStateChanged(String, int)](../android/media/tv/TvInputManager.TvInputCallback.md)): The input source is connected but in standby mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_STATE_DISCONNECTED](TvInputManager.md) State for [getInputState(java.lang.String)](TvInputManager.md))and [TvInputCallback.onInputStateChanged(String, int)](../android/media/tv/TvInputManager.TvInputCallback.md)): The input source is disconnected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [META_DATA_CONTENT_RATING_SYSTEMS](TvInputManager.md) Content rating systems metadata associated with [ACTION_QUERY_CONTENT_RATING_SYSTEMS](TvInputManager.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_ERROR_INSUFFICIENT_SPACE](TvInputManager.md) Error for [TvInputService.RecordingSession.notifyError(int)](../android/media/tv/TvInputService.RecordingSession.md))and [TvRecordingClient.RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)): Recording cannot proceed due to insufficient storage space. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_ERROR_RESOURCE_BUSY](TvInputManager.md) Error for [TvInputService.RecordingSession.notifyError(int)](../android/media/tv/TvInputService.RecordingSession.md))and [TvRecordingClient.RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)): Recording cannot proceed because a required recording resource was not able to be allocated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_ERROR_UNKNOWN](TvInputManager.md) Error for [TvInputService.RecordingSession.notifyError(int)](../android/media/tv/TvInputService.RecordingSession.md))and [TvRecordingClient.RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)): The requested operation cannot be completed due to a problem that does not fit under any other error codes, or the error code for the problem is defined on the higher version than application's`android:targetSdkVersion`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_AD_BUFFER](TvInputManager.md) An object of [AdBuffer](AdBuffer.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_AD_RESPONSE](TvInputManager.md) An object of [AdResponse](AdResponse.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_BROADCAST_INFO_RESPONSE](TvInputManager.md) An object of [BroadcastInfoResponse](BroadcastInfoResponse.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_CHANNEL_URI](TvInputManager.md) The URI of a channel. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_TRACKS](TvInputManager.md) A list which includes track information. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_TRACK_ID](TvInputManager.md) The ID of the track. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_TRACK_TYPE](TvInputManager.md) The type of the track. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_TV_MESSAGE_TYPE](TvInputManager.md) The type of TV message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_KEY_VIDEO_UNAVAILABLE_REASON](TvInputManager.md) The reason why the video became unavailable. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_AD_BUFFER_CONSUMED](TvInputManager.md) Notifies the advertisement buffer is consumed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_AD_RESPONSE](TvInputManager.md) Notifies response for advertisement. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_BROADCAST_INFO_RESPONSE](TvInputManager.md) Notifies response for broadcast info. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_TRACKS_CHANGED](TvInputManager.md) Sends the list of all audio/video/subtitle tracks. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_TRACK_SELECTED](TvInputManager.md) Sends the type and ID of a selected track. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_TUNED](TvInputManager.md) Informs the application that the session has been tuned to the given channel. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_TV_MESSAGE](TvInputManager.md) Sends the TV message. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_VIDEO_AVAILABLE](TvInputManager.md) Informs the application that the video is now available for watching. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SESSION_DATA_TYPE_VIDEO_UNAVAILABLE](TvInputManager.md) Informs the application that the video became unavailable for some reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_LOST](TvInputManager.md) Signal lost. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_STRONG](TvInputManager.md) Strong signal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_WEAK](TvInputManager.md) Weak signal. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [TIME_SHIFT_INVALID_TIME](TvInputManager.md) Value returned by [TvInputService.Session.onTimeShiftGetCurrentPosition()](../android/media/tv/TvInputService.Session.md))and [TvInputService.Session.onTimeShiftGetStartPosition()](../android/media/tv/TvInputService.Session.md))when time shifting has not yet started. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SHIFT_MODE_AUTO](TvInputManager.md) Time shift mode: auto. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SHIFT_MODE_LOCAL](TvInputManager.md) Time shift mode: local. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SHIFT_MODE_NETWORK](TvInputManager.md) Time shift mode: network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SHIFT_MODE_OFF](TvInputManager.md) Time shift mode: off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SHIFT_STATUS_AVAILABLE](TvInputManager.md) Status for [TvInputService.Session.notifyTimeShiftStatusChanged(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onTimeShiftStatusChanged(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Time shifting is currently available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SHIFT_STATUS_UNAVAILABLE](TvInputManager.md) Status for [TvInputService.Session.notifyTimeShiftStatusChanged(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onTimeShiftStatusChanged(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Time shifting is currently unavailable but might work again later. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SHIFT_STATUS_UNKNOWN](TvInputManager.md) Status for [TvInputService.Session.notifyTimeShiftStatusChanged(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onTimeShiftStatusChanged(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Unknown status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SHIFT_STATUS_UNSUPPORTED](TvInputManager.md) Status for [TvInputService.Session.notifyTimeShiftStatusChanged(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onTimeShiftStatusChanged(String, int)](../android/media/tv/TvView.TvInputCallback.md)): The current TV input does not support time shifting. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [TV_MESSAGE_GROUP_ID_NONE](TvInputManager.md) This value for [TV_MESSAGE_KEY_GROUP_ID](TvInputManager.md) denotes that the message doesn't belong to any group. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TV_MESSAGE_KEY_GROUP_ID](TvInputManager.md) This constant is used as a [Bundle](../android.os/Bundle.md) key for TV messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TV_MESSAGE_KEY_RAW_DATA](TvInputManager.md) This constant is used as a [Bundle](../android.os/Bundle.md) key for TV messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TV_MESSAGE_KEY_STREAM_ID](TvInputManager.md) This constant is used as a [Bundle](../android.os/Bundle.md) key for TV messages. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TV_MESSAGE_KEY_SUBTYPE](TvInputManager.md) This constant is used as a [Bundle](../android.os/Bundle.md) key for TV messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TV_MESSAGE_SUBTYPE_CC_608E](TvInputManager.md) This is a subtype for TV messages that can be potentially found as a value at [TV_MESSAGE_KEY_SUBTYPE](TvInputManager.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TV_MESSAGE_SUBTYPE_WATERMARKING_A335](TvInputManager.md) This is a subtype for TV messages that can be potentially found as a value at [TV_MESSAGE_KEY_SUBTYPE](TvInputManager.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TV_MESSAGE_TYPE_CLOSED_CAPTION](TvInputManager.md) Indicates that this TV message contains Closed Captioning data |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TV_MESSAGE_TYPE_OTHER](TvInputManager.md) Indicates that this TV message contains other data |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TV_MESSAGE_TYPE_WATERMARK](TvInputManager.md) Indicates that this TV message contains watermarking data |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_AUDIO_ONLY](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the current TV program is audio-only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_BUFFERING](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the corresponding TV input has stopped playback temporarily to buffer more data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_BLACKOUT](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because of a geographical blackout. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_CARD_INVALID](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because smart card is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_CARD_MUTE](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because smart card is muted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_INSUFFICIENT_OUTPUT_PROTECTION](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the output protection level enabled on the device is not sufficient to meet the requirements in the license policy. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_LICENSE_EXPIRED](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because Using a license in whhich the keys have expired. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_NEED_ACTIVATION](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the device need be activated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_NEED_PAIRING](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the device need be paired. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_NO_CARD](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because smart card is missed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_PVR_RECORDING_NOT_ALLOWED](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the PVR record is not allowed by the license policy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_REBOOTING](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because CAS system is rebooting. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_CAS_UNKNOWN](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because of unknown CAS error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_INSUFFICIENT_RESOURCE](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the resource is not enough to meet requirement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_NOT_CONNECTED](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the source is not physically connected, for example the HDMI cable is not connected. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_STOPPED](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because it has been stopped by [TvView.stopPlayback(int)](TvView.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_TUNING](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the corresponding TV input is in the middle of tuning to a new channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_UNKNOWN](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable due to an unspecified error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_UNAVAILABLE_REASON_WEAK_SIGNAL](TvInputManager.md) Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable due to weak TV signal. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TvContentRating](TvContentRating.md)!\>! | [getBlockedRatings](TvInputManager.md))`()` Returns the list of blocked content ratings. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputState](TvInputManager.md))`(`inputId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the state of a given TV input. |
| [TvInputInfo](TvInputInfo.md)? | [getTvInputInfo](TvInputManager.md))`(`inputId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the [TvInputInfo](TvInputInfo.md) for a given TV input. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TvInputInfo](TvInputInfo.md)!\>! | [getTvInputList](TvInputManager.md))`()` Returns the complete list of TV inputs on the system. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParentalControlsEnabled](TvInputManager.md))`()` Returns the user's parental controls enabled state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRatingBlocked](TvInputManager.md))`(`rating:` ` [TvContentRating](TvContentRating.md)`)` Checks whether a given TV content rating is blocked by the user. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](TvInputManager.md))`(`callback:` ` [TvInputManager.TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md)`, `handler:` ` [Handler](../android.os/Handler.md)`)` Registers a [TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](TvInputManager.md))`(`callback:` ` [TvInputManager.TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md)`)` Unregisters the existing [TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTvInputInfo](TvInputManager.md))`(`inputInfo:` ` [TvInputInfo](TvInputInfo.md)`)` Updates the`TvInputInfo`for an existing TV input. |
| --- | --- |

## Constants

### ACTION_BLOCKED_RATINGS_CHANGED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_BLOCKED_RATINGS_CHANGED: String
```

Broadcast intent action when the user blocked content ratings change. For use with the [isRatingBlocked](TvInputManager.md)). 

 Value: "android.media.tv.action.BLOCKED_RATINGS_CHANGED"

### ACTION_PARENTAL_CONTROLS_ENABLED_CHANGED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PARENTAL_CONTROLS_ENABLED_CHANGED: String
```

Broadcast intent action when the parental controls enabled state changes. For use with the [isParentalControlsEnabled](TvInputManager.md)). 

 Value: "android.media.tv.action.PARENTAL_CONTROLS_ENABLED_CHANGED"

### ACTION_QUERY_CONTENT_RATING_SYSTEMS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_QUERY_CONTENT_RATING_SYSTEMS: String
```

Broadcast intent action used to query available content rating systems.

The TV input manager service locates available content rating systems by querying broadcast receivers that are registered for this action. An application can offer additional content rating systems to the user by declaring a suitable broadcast receiver in its manifest.

Here is an example broadcast receiver declaration that an application might include in its AndroidManifest.xml to advertise custom content rating systems. The meta-data specifies a resource that contains a description of each content rating system that is provided by the application.

<br />

```kotlin
<receiver android:name=".TvInputReceiver">
      <intent-filter>
          <action android:name=
                  "android.media.tv.action.QUERY_CONTENT_RATING_SYSTEMS" />
      </intent-filter>
      <meta-data
              android:name="android.media.tv.metadata.CONTENT_RATING_SYSTEMS"
              android:resource="@xml/tv_content_rating_systems" />
  </receiver>
```

In the above example, the`@xml/tv_content_rating_systems`resource refers to an XML resource whose root element is`<rating-system-definitions>`that contains zero or more`<rating-system-definition>`elements. Each` <rating-system-definition>`element specifies the ratings, sub-ratings and rating orders of a particular content rating system. 

 Value: "android.media.tv.action.QUERY_CONTENT_RATING_SYSTEMS"

**See Also**

- [android.media.tv.TvContentRating](TvContentRating.md) 

### ACTION_SETUP_INPUTS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SETUP_INPUTS: String
```

Activity action to set up channel sources i.e. TV inputs of type [TvInputInfo.TYPE_TUNER](TvInputInfo.md). When invoked, the system will display an appropriate UI for the user to initiate the individual setup flow provided by [android.R.attr#setupActivity](../android/R.attr.md) of each TV input service. 

 Value: "android.media.tv.action.SETUP_INPUTS"

### ACTION_VIEW_RECORDING_SCHEDULES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_VIEW_RECORDING_SCHEDULES: String
```

Activity action to display the recording schedules. When invoked, the system will display an appropriate UI to browse the schedules. 

 Value: "android.media.tv.action.VIEW_RECORDING_SCHEDULES"

### BROADCAST_INFO_STREAM_EVENT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_INFO_STREAM_EVENT: Int
```  

 Value: 5

### BROADCAST_INFO_TYPE_COMMAND

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_INFO_TYPE_COMMAND: Int
```  

 Value: 7

### BROADCAST_INFO_TYPE_DSMCC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_INFO_TYPE_DSMCC: Int
```  

 Value: 6

### BROADCAST_INFO_TYPE_PES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_INFO_TYPE_PES: Int
```  

 Value: 4

### BROADCAST_INFO_TYPE_SECTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_INFO_TYPE_SECTION: Int
```  

 Value: 3

### BROADCAST_INFO_TYPE_TABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_INFO_TYPE_TABLE: Int
```  

 Value: 2

### BROADCAST_INFO_TYPE_TIMELINE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_INFO_TYPE_TIMELINE: Int
```  

 Value: 8

### BROADCAST_INFO_TYPE_TS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BROADCAST_INFO_TYPE_TS: Int
```  

 Value: 1

### INPUT_STATE_CONNECTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_STATE_CONNECTED: Int
```

State for [getInputState(java.lang.String)](TvInputManager.md))and [TvInputCallback.onInputStateChanged(String, int)](../android/media/tv/TvInputManager.TvInputCallback.md)): The input source is connected.

This state indicates that a source device is connected to the input port and is in the normal operation mode. It is mostly relevant to hardware inputs such as HDMI input. Non-hardware inputs are considered connected all the time. 

 Value: 0

### INPUT_STATE_CONNECTED_STANDBY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_STATE_CONNECTED_STANDBY: Int
```

State for [getInputState(java.lang.String)](TvInputManager.md))and [TvInputCallback.onInputStateChanged(String, int)](../android/media/tv/TvInputManager.TvInputCallback.md)): The input source is connected but in standby mode.

This state indicates that a source device is connected to the input port but is in standby or low power mode. It is mostly relevant to hardware inputs such as HDMI input and Component inputs. 

 Value: 1

### INPUT_STATE_DISCONNECTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_STATE_DISCONNECTED: Int
```

State for [getInputState(java.lang.String)](TvInputManager.md))and [TvInputCallback.onInputStateChanged(String, int)](../android/media/tv/TvInputManager.TvInputCallback.md)): The input source is disconnected.

This state indicates that a source device is disconnected from the input port. It is mostly relevant to hardware inputs such as HDMI input. 

 Value: 2

### META_DATA_CONTENT_RATING_SYSTEMS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val META_DATA_CONTENT_RATING_SYSTEMS: String
```

Content rating systems metadata associated with [ACTION_QUERY_CONTENT_RATING_SYSTEMS](TvInputManager.md).

Specifies the resource ID of an XML resource that describes the content rating systems that are provided by the application. 

 Value: "android.media.tv.metadata.CONTENT_RATING_SYSTEMS"

### RECORDING_ERROR_INSUFFICIENT_SPACE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_ERROR_INSUFFICIENT_SPACE: Int
```

Error for [TvInputService.RecordingSession.notifyError(int)](../android/media/tv/TvInputService.RecordingSession.md))and [TvRecordingClient.RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)): Recording cannot proceed due to insufficient storage space. 

 Value: 1

### RECORDING_ERROR_RESOURCE_BUSY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_ERROR_RESOURCE_BUSY: Int
```

Error for [TvInputService.RecordingSession.notifyError(int)](../android/media/tv/TvInputService.RecordingSession.md))and [TvRecordingClient.RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)): Recording cannot proceed because a required recording resource was not able to be allocated. 

 Value: 2

### RECORDING_ERROR_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_ERROR_UNKNOWN: Int
```

Error for [TvInputService.RecordingSession.notifyError(int)](../android/media/tv/TvInputService.RecordingSession.md))and [TvRecordingClient.RecordingCallback.onError(int)](../android/media/tv/TvRecordingClient.RecordingCallback.md)): The requested operation cannot be completed due to a problem that does not fit under any other error codes, or the error code for the problem is defined on the higher version than application's`android:targetSdkVersion`. 

 Value: 0

### SESSION_DATA_KEY_AD_BUFFER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_AD_BUFFER: String
```

An object of [AdBuffer](AdBuffer.md).

Type: android.media.tv.AdBuffer 

 Value: "ad_buffer"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_KEY_AD_RESPONSE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_AD_RESPONSE: String
```

An object of [AdResponse](AdResponse.md).

Type: android.media.tv.AdResponse 

 Value: "ad_response"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_KEY_BROADCAST_INFO_RESPONSE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_BROADCAST_INFO_RESPONSE: String
```

An object of [BroadcastInfoResponse](BroadcastInfoResponse.md).

Type: android.media.tv.BroadcastInfoResponse 

 Value: "broadcast_info_response"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_KEY_CHANNEL_URI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_CHANNEL_URI: String
```

The URI of a channel.

Type: android.net.Uri 

 Value: "channel_uri"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_KEY_TRACKS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_TRACKS: String
```

A list which includes track information.

Type:`java.util.List<android.media.tv.TvTrackInfo> ` 

 Value: "tracks"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_KEY_TRACK_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_TRACK_ID: String
```

The ID of the track.

Type: String 

 Value: "track_id"

**See Also**

- [android.media.tv.TvTrackInfo#getId()](TvTrackInfo.md))
- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_KEY_TRACK_TYPE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_TRACK_TYPE: String
```

The type of the track.

One of [TvTrackInfo.TYPE_AUDIO](TvTrackInfo.md), [TvTrackInfo.TYPE_VIDEO](TvTrackInfo.md), [TvTrackInfo.TYPE_SUBTITLE](TvTrackInfo.md).

Type: Integer 

 Value: "track_type"

**See Also**

- [android.media.tv.TvTrackInfo#getType()](TvTrackInfo.md))
- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_KEY_TV_MESSAGE_TYPE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_TV_MESSAGE_TYPE: String
```

The type of TV message.

It can be one of TV_MESSAGE_TYPE_WATERMARK, TV_MESSAGE_TYPE_CLOSED_CAPTION, TV_MESSAGE_TYPE_OTHER

Type: Integer 

 Value: "tv_message_type"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_KEY_VIDEO_UNAVAILABLE_REASON

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_KEY_VIDEO_UNAVAILABLE_REASON: String
```

The reason why the video became unavailable.

The value can be VIDEO_UNAVAILABLE_REASON_BUFFERING, VIDEO_UNAVAILABLE_REASON_AUDIO_ONLY, etc.

Type: Integer 

 Value: "video_unavailable_reason"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_AD_BUFFER_CONSUMED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_AD_BUFFER_CONSUMED: String
```

Notifies the advertisement buffer is consumed. 

 Value: "ad_buffer_consumed"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_AD_RESPONSE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_AD_RESPONSE: String
```

Notifies response for advertisement. 

 Value: "ad_response"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_BROADCAST_INFO_RESPONSE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_BROADCAST_INFO_RESPONSE: String
```

Notifies response for broadcast info. 

 Value: "broadcast_info_response"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_TRACKS_CHANGED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_TRACKS_CHANGED: String
```

Sends the list of all audio/video/subtitle tracks. 

 Value: "tracks_changed"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_TRACK_SELECTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_TRACK_SELECTED: String
```

Sends the type and ID of a selected track. This is used to inform the application that a specific track is selected. 

 Value: "track_selected"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_TUNED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_TUNED: String
```

Informs the application that the session has been tuned to the given channel. 

 Value: "tuned"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_TV_MESSAGE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_TV_MESSAGE: String
```

Sends the TV message. 

 Value: "tv_message"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md))
- [android.media.tv.TvInputService.Session#notifyTvMessage(int, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_VIDEO_AVAILABLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_VIDEO_AVAILABLE: String
```

Informs the application that the video is now available for watching. 

 Value: "video_available"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SESSION_DATA_TYPE_VIDEO_UNAVAILABLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_DATA_TYPE_VIDEO_UNAVAILABLE: String
```

Informs the application that the video became unavailable for some reason. 

 Value: "video_unavailable"

**See Also**

- [android.media.tv.TvInputService.Session#sendTvInputSessionData(String, Bundle)](../android/media/tv/TvInputService.Session.md)) 

### SIGNAL_STRENGTH_LOST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_LOST: Int
```

Signal lost. 

 Value: 1

### SIGNAL_STRENGTH_STRONG

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_STRONG: Int
```

Strong signal. 

 Value: 3

### SIGNAL_STRENGTH_WEAK

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_WEAK: Int
```

Weak signal. 

 Value: 2

### TIME_SHIFT_INVALID_TIME

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_INVALID_TIME: Long
```

Value returned by [TvInputService.Session.onTimeShiftGetCurrentPosition()](../android/media/tv/TvInputService.Session.md))and [TvInputService.Session.onTimeShiftGetStartPosition()](../android/media/tv/TvInputService.Session.md))when time shifting has not yet started. 

 Value: -9223372036854775808L

### TIME_SHIFT_MODE_AUTO

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_MODE_AUTO: Int
```

Time shift mode: auto.

Time shift mode is handled automatically. 

 Value: 4

### TIME_SHIFT_MODE_LOCAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_MODE_LOCAL: Int
```

Time shift mode: local.

Time shift is handle locally, using on-device data. E.g. playing a local file. 

 Value: 2

### TIME_SHIFT_MODE_NETWORK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_MODE_NETWORK: Int
```

Time shift mode: network.

Time shift is handle remotely via network. E.g. online streaming. 

 Value: 3

### TIME_SHIFT_MODE_OFF

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_MODE_OFF: Int
```

Time shift mode: off.

Time shift is disabled. 

 Value: 1

### TIME_SHIFT_STATUS_AVAILABLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_STATUS_AVAILABLE: Int
```

Status for [TvInputService.Session.notifyTimeShiftStatusChanged(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onTimeShiftStatusChanged(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Time shifting is currently available. In this status, the application assumes it can pause/resume playback, seek to a specified time position and set playback rate and audio mode. 

 Value: 3

### TIME_SHIFT_STATUS_UNAVAILABLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_STATUS_UNAVAILABLE: Int
```

Status for [TvInputService.Session.notifyTimeShiftStatusChanged(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onTimeShiftStatusChanged(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Time shifting is currently unavailable but might work again later. 

 Value: 2

### TIME_SHIFT_STATUS_UNKNOWN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_STATUS_UNKNOWN: Int
```

Status for [TvInputService.Session.notifyTimeShiftStatusChanged(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onTimeShiftStatusChanged(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Unknown status. Also the status prior to calling`notifyTimeShiftStatusChanged`. 

 Value: 0

### TIME_SHIFT_STATUS_UNSUPPORTED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SHIFT_STATUS_UNSUPPORTED: Int
```

Status for [TvInputService.Session.notifyTimeShiftStatusChanged(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onTimeShiftStatusChanged(String, int)](../android/media/tv/TvView.TvInputCallback.md)): The current TV input does not support time shifting. 

 Value: 1

### TV_MESSAGE_GROUP_ID_NONE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_GROUP_ID_NONE: Long
```

This value for [TV_MESSAGE_KEY_GROUP_ID](TvInputManager.md) denotes that the message doesn't belong to any group. 

 Value: -1L

### TV_MESSAGE_KEY_GROUP_ID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_KEY_GROUP_ID: String
```

This constant is used as a [Bundle](../android.os/Bundle.md) key for TV messages. This is used to optionally identify messages that belong together, such as headers and bodies of the same event. For messages that do not have a group, this value should be [TV_MESSAGE_GROUP_ID_NONE](TvInputManager.md).

As -1 is a reserved value, -1 should not be used as a valid groupId.

Type: long 

 Value: "android.media.tv.TvInputManager.group_id"

### TV_MESSAGE_KEY_RAW_DATA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_KEY_RAW_DATA: String
```

This constant is used as a [Bundle](../android.os/Bundle.md) key for TV messages. The value of the key stores the raw data contained in this TV message. The format of this data is determined by the format defined by the subtype, found using the key at [TV_MESSAGE_KEY_SUBTYPE](TvInputManager.md). See [TV_MESSAGE_KEY_SUBTYPE](TvInputManager.md) for more information on how to parse this data.

Type: byte\[\] 

 Value: "android.media.tv.TvInputManager.raw_data"

### TV_MESSAGE_KEY_STREAM_ID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_KEY_STREAM_ID: String
```

This constant is used as a [Bundle](../android.os/Bundle.md) key for TV messages. The value of the key identifies the stream on the TV input source for which the watermark event is relevant to.

Type: String 

 Value: "android.media.tv.TvInputManager.stream_id"

### TV_MESSAGE_KEY_SUBTYPE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_KEY_SUBTYPE: String
```

This constant is used as a [Bundle](../android.os/Bundle.md) key for TV messages. The value of the key identifies the subtype of the data, such as the format of the CC data. The format found at this key can then be used to identify how to parse the data at [TV_MESSAGE_KEY_RAW_DATA](TvInputManager.md).

To parse the raw data based on the subtype, please refer to the official documentation of the concerning subtype. For example, for the subtype [TV_MESSAGE_SUBTYPE_WATERMARKING_A335](TvInputManager.md), the document for A/335 from the ATSC standard details how this data is formatted. Similarly, the subtype [TV_MESSAGE_SUBTYPE_CC_608E](TvInputManager.md) is documented in the ANSI/CTA standard for 608-E. These subtypes are examples of common formats for their respective uses and other subtypes may exist.

Type: String 

 Value: "android.media.tv.TvInputManager.subtype"

### TV_MESSAGE_SUBTYPE_CC_608E

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_SUBTYPE_CC_608E: String
```

This is a subtype for TV messages that can be potentially found as a value at [TV_MESSAGE_KEY_SUBTYPE](TvInputManager.md). It identifies the subtype of the message as the CC format CTA 608-E. 

 Value: "CTA 608-E"

### TV_MESSAGE_SUBTYPE_WATERMARKING_A335

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_SUBTYPE_WATERMARKING_A335: String
```

This is a subtype for TV messages that can be potentially found as a value at [TV_MESSAGE_KEY_SUBTYPE](TvInputManager.md). It identifies the subtype of the message as the watermarking format ATSC A/335. 

 Value: "ATSC A/335"

### TV_MESSAGE_TYPE_CLOSED_CAPTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_TYPE_CLOSED_CAPTION: Int
```

Indicates that this TV message contains Closed Captioning data 

 Value: 2

### TV_MESSAGE_TYPE_OTHER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_TYPE_OTHER: Int
```

Indicates that this TV message contains other data 

 Value: 1000

### TV_MESSAGE_TYPE_WATERMARK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TV_MESSAGE_TYPE_WATERMARK: Int
```

Indicates that this TV message contains watermarking data 

 Value: 1

### VIDEO_UNAVAILABLE_REASON_AUDIO_ONLY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_AUDIO_ONLY: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the current TV program is audio-only. 

 Value: 4

### VIDEO_UNAVAILABLE_REASON_BUFFERING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_BUFFERING: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the corresponding TV input has stopped playback temporarily to buffer more data. 

 Value: 3

### VIDEO_UNAVAILABLE_REASON_CAS_BLACKOUT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_BLACKOUT: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because of a geographical blackout. 

 Value: 16

### VIDEO_UNAVAILABLE_REASON_CAS_CARD_INVALID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_CARD_INVALID: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because smart card is invalid. 

 Value: 15

### VIDEO_UNAVAILABLE_REASON_CAS_CARD_MUTE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_CARD_MUTE: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because smart card is muted. 

 Value: 14

### VIDEO_UNAVAILABLE_REASON_CAS_INSUFFICIENT_OUTPUT_PROTECTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_INSUFFICIENT_OUTPUT_PROTECTION: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the output protection level enabled on the device is not sufficient to meet the requirements in the license policy. 

 Value: 7

### VIDEO_UNAVAILABLE_REASON_CAS_LICENSE_EXPIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_LICENSE_EXPIRED: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because Using a license in whhich the keys have expired. 

 Value: 10

### VIDEO_UNAVAILABLE_REASON_CAS_NEED_ACTIVATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_NEED_ACTIVATION: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the device need be activated. 

 Value: 11

### VIDEO_UNAVAILABLE_REASON_CAS_NEED_PAIRING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_NEED_PAIRING: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the device need be paired. 

 Value: 12

### VIDEO_UNAVAILABLE_REASON_CAS_NO_CARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_NO_CARD: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because smart card is missed. 

 Value: 13

### VIDEO_UNAVAILABLE_REASON_CAS_PVR_RECORDING_NOT_ALLOWED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_PVR_RECORDING_NOT_ALLOWED: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the PVR record is not allowed by the license policy. 

 Value: 8

### VIDEO_UNAVAILABLE_REASON_CAS_REBOOTING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_REBOOTING: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because CAS system is rebooting. 

 Value: 17

### VIDEO_UNAVAILABLE_REASON_CAS_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_CAS_UNKNOWN: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because of unknown CAS error. 

 Value: 18

### VIDEO_UNAVAILABLE_REASON_INSUFFICIENT_RESOURCE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_INSUFFICIENT_RESOURCE: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the resource is not enough to meet requirement. 

 Value: 6

### VIDEO_UNAVAILABLE_REASON_NOT_CONNECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_NOT_CONNECTED: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the source is not physically connected, for example the HDMI cable is not connected. 

 Value: 5

### VIDEO_UNAVAILABLE_REASON_STOPPED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_STOPPED: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because it has been stopped by [TvView.stopPlayback(int)](TvView.md)). 

 Value: 19

### VIDEO_UNAVAILABLE_REASON_TUNING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_TUNING: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable because the corresponding TV input is in the middle of tuning to a new channel. 

 Value: 1

### VIDEO_UNAVAILABLE_REASON_UNKNOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_UNKNOWN: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable due to an unspecified error. 

 Value: 0

### VIDEO_UNAVAILABLE_REASON_WEAK_SIGNAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_UNAVAILABLE_REASON_WEAK_SIGNAL: Int
```

Reason for [TvInputService.Session.notifyVideoUnavailable(int)](../android/media/tv/TvInputService.Session.md))and [TvView.TvInputCallback.onVideoUnavailable(String, int)](../android/media/tv/TvView.TvInputCallback.md)): Video is unavailable due to weak TV signal. 

 Value: 2

## Public methods

### getBlockedRatings

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBlockedRatings(): MutableList<TvContentRating!>!
```

Returns the list of blocked content ratings.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TvContentRating](TvContentRating.md)!>! | the list of content ratings blocked by the user. |

### getInputState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputState(inputId: String): Int
```

Returns the state of a given TV input.

The state is one of the following:

- [INPUT_STATE_CONNECTED](TvInputManager.md)
- [INPUT_STATE_CONNECTED_STANDBY](TvInputManager.md)
- [INPUT_STATE_DISCONNECTED](TvInputManager.md)

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `inputId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The ID of the TV input. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.TvInputManager#INPUT_STATE_CONNECTED](TvInputManager.md), [android.media.tv.TvInputManager#INPUT_STATE_CONNECTED_STANDBY](TvInputManager.md), or [android.media.tv.TvInputManager#INPUT_STATE_DISCONNECTED](TvInputManager.md) |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the argument is`null`. |

### getTvInputInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTvInputInfo(inputId: String): TvInputInfo?
```

Returns the [TvInputInfo](TvInputInfo.md) for a given TV input.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `inputId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The ID of the TV input. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [TvInputInfo](TvInputInfo.md)? | the [TvInputInfo](TvInputInfo.md) for a given TV input.`null`if not found. |

### getTvInputList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTvInputList(): MutableList<TvInputInfo!>!
```

Returns the complete list of TV inputs on the system.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TvInputInfo](TvInputInfo.md)!>! | List of [TvInputInfo](TvInputInfo.md) for each TV input that describes its meta information. |

### isParentalControlsEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isParentalControlsEnabled(): Boolean
```

Returns the user's parental controls enabled state.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the user enabled the parental controls,`false`otherwise. |

### isRatingBlocked

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRatingBlocked(rating: TvContentRating): Boolean
```

Checks whether a given TV content rating is blocked by the user.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rating` | [TvContentRating](TvContentRating.md):The TV content rating to check. Can be [TvContentRating.UNRATED](TvContentRating.md). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given TV content rating is blocked,`false`otherwise. |

### registerCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(
    callback: TvInputManager.TvInputCallback, 
    handler: Handler
): Unit
```

Registers a [TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [TvInputManager.TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md):A callback used to monitor status of the TV inputs. This value cannot be`null`. |
| `handler` | [Handler](../android.os/Handler.md):A [Handler](../android.os/Handler.md) that the status change will be delivered to. This value cannot be`null`. |

### unregisterCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: TvInputManager.TvInputCallback): Unit
```

Unregisters the existing [TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [TvInputManager.TvInputCallback](../android/media/tv/TvInputManager.TvInputCallback.md):The existing callback to remove. This value cannot be`null`. |

### updateTvInputInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateTvInputInfo(inputInfo: TvInputInfo): Unit
```

Updates the`TvInputInfo`for an existing TV input. A TV input service implementation may call this method to pass the application and system an up-to-date`TvInputInfo`object that describes itself.

The system automatically creates a`TvInputInfo`object for each TV input, based on the information collected from the`AndroidManifest.xml`, thus it is not necessary to call this method unless such information has changed dynamically. Use [TvInputInfo.Builder](../android/media/tv/TvInputInfo.Builder.md) to build a new`TvInputInfo`object.

Attempting to change information about a TV input that the calling package does not own does nothing.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputInfo` | [TvInputInfo](TvInputInfo.md):The`TvInputInfo`object that contains new information. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the argument is`null`. |

**See Also**

- [android.media.tv.TvInputManager.TvInputCallback#onTvInputInfoUpdated(TvInputInfo)](../android/media/tv/TvInputManager.TvInputCallback.md))
