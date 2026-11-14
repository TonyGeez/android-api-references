# PlaybackErrorEvent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlaybackErrorEvent

Kotlin| [Java](https://developer.android.com/reference/android/media/metrics/PlaybackErrorEvent "View this page in Java") 

```
class PlaybackErrorEvent : Event, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.media.metrics.Event](https://developer.android.com/reference/kotlin/android/media/metrics/Event) ||
| | ↳ | [android.media.metrics.PlaybackErrorEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#) |

Playback error event.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent.Builder) A builder for [PlaybackErrorEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#) |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_AUDIO_TRACK_INIT_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_AUDIO_TRACK_INIT_FAILED:kotlin.Int) Error code for an AudioTrack initialization failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_AUDIO_TRACK_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_AUDIO_TRACK_OTHER:kotlin.Int) Error code for other AudioTrack errors |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_AUDIO_TRACK_WRITE_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_AUDIO_TRACK_WRITE_FAILED:kotlin.Int) Error code for an AudioTrack write operation failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DECODER_INIT_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODER_INIT_FAILED:kotlin.Int) Error code for a decoder initialization failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DECODING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODING_FAILED:kotlin.Int) Error code for a failure while trying to decode media samples |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DECODING_FORMAT_EXCEEDS_CAPABILITIES](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODING_FORMAT_EXCEEDS_CAPABILITIES:kotlin.Int) Error code for trying to decode content whose format exceeds the capabilities of the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DECODING_FORMAT_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODING_FORMAT_UNSUPPORTED:kotlin.Int) Error code for trying to decode content whose format is not supported |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DECODING_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODING_OTHER:kotlin.Int) Error code for other decoding errors |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DRM_CONTENT_ERROR](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_CONTENT_ERROR:kotlin.Int) Error code for attempting to play incompatible DRM-protected content |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DRM_DEVICE_REVOKED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_DEVICE_REVOKED:kotlin.Int) Error code for the device having revoked DRM privileges |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DRM_DISALLOWED_OPERATION](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_DISALLOWED_OPERATION:kotlin.Int) Error code an operation being disallowed by a license policy |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DRM_LICENSE_ACQUISITION_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_LICENSE_ACQUISITION_FAILED:kotlin.Int) Error code for a failure while trying to obtain a license |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DRM_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_OTHER:kotlin.Int) Error code for other DRM errors |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DRM_PROVISIONING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_PROVISIONING_FAILED:kotlin.Int) Error code for a failure while provisioning the device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DRM_SCHEME_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_SCHEME_UNSUPPORTED:kotlin.Int) Error code for a chosen DRM protection scheme not being supported by the device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DRM_SYSTEM_ERROR](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_SYSTEM_ERROR:kotlin.Int) Error code for an error in the DRM system |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_BAD_HTTP_STATUS](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_BAD_HTTP_STATUS:kotlin.Int) Error code for an HTTP server returning an unexpected HTTP response status code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_CONNECTION_CLOSED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_CONNECTION_CLOSED:kotlin.Int) Error code for an existing network connection being unexpectedly closed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_CONNECTION_TIMEOUT](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_CONNECTION_TIMEOUT:kotlin.Int) Error code for a network timeout, meaning the server is taking too long to fulfill a request |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_DNS_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_DNS_FAILED:kotlin.Int) Error code for failing to resolve a hostname |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_FILE_NOT_FOUND](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_FILE_NOT_FOUND:kotlin.Int) Error code for a non-existent file |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_NETWORK_CONNECTION_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_NETWORK_CONNECTION_FAILED:kotlin.Int) Error code for a failure while establishing a network connection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_NETWORK_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_NETWORK_UNAVAILABLE:kotlin.Int) Error code for lack of network connectivity while trying to access a network resource |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_NO_PERMISSION](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_NO_PERMISSION:kotlin.Int) Error code for lack of permission to perform an IO operation, for example, lack of permission to access internet or external storage. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_OTHER:kotlin.Int) Error code for other Input/Output errors |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_OTHER:kotlin.Int) Error code for other errors |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PARSING_CONTAINER_MALFORMED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_CONTAINER_MALFORMED:kotlin.Int) Error code for a parsing error associated to a media container format bitstream |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PARSING_CONTAINER_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_CONTAINER_UNSUPPORTED:kotlin.Int) Error code for attempting to extract a file with an unsupported media container format, or an unsupported media container feature |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PARSING_MANIFEST_MALFORMED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_MANIFEST_MALFORMED:kotlin.Int) Error code for a parsing error associated to a media manifest |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PARSING_MANIFEST_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_MANIFEST_UNSUPPORTED:kotlin.Int) Error code for an unsupported feature in a media manifest |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PARSING_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_OTHER:kotlin.Int) Error code for other media parsing errors |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PLAYER_BEHIND_LIVE_WINDOW](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PLAYER_BEHIND_LIVE_WINDOW:kotlin.Int) Error code for the loading position falling behind the sliding window of available live content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PLAYER_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PLAYER_OTHER:kotlin.Int) Error code for other player errors |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PLAYER_REMOTE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PLAYER_REMOTE:kotlin.Int) Error code for an unidentified error in a remote controller or player |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_RUNTIME](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_RUNTIME:kotlin.Int) Error code for runtime errors |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_UNKNOWN:kotlin.Int) Unknown error code. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#getErrorCode())`()` Gets error code. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getMetricsBundle](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#getMetricsBundle())`()` Gets metrics-related information that is not supported by dedicated methods. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubErrorCode](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#getSubErrorCode())`()` Gets sub error code. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeSinceCreatedMillis](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#getTimeSinceCreatedMillis())`()` Gets the timestamp since creation of the playback session in milliseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PlaybackErrorEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ERROR_AUDIO_TRACK_INIT_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_AUDIO_TRACK_INIT_FAILED: Int
```

Error code for an AudioTrack initialization failure 

 Value: 17

### ERROR_AUDIO_TRACK_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_AUDIO_TRACK_OTHER: Int
```

Error code for other AudioTrack errors 

 Value: 19

### ERROR_AUDIO_TRACK_WRITE_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_AUDIO_TRACK_WRITE_FAILED: Int
```

Error code for an AudioTrack write operation failure 

 Value: 18

### ERROR_DECODER_INIT_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DECODER_INIT_FAILED: Int
```

Error code for a decoder initialization failure 

 Value: 13

### ERROR_DECODING_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DECODING_FAILED: Int
```

Error code for a failure while trying to decode media samples 

 Value: 14

### ERROR_DECODING_FORMAT_EXCEEDS_CAPABILITIES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DECODING_FORMAT_EXCEEDS_CAPABILITIES: Int
```

Error code for trying to decode content whose format exceeds the capabilities of the device. 

 Value: 15

### ERROR_DECODING_FORMAT_UNSUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DECODING_FORMAT_UNSUPPORTED: Int
```

Error code for trying to decode content whose format is not supported 

 Value: 35

### ERROR_DECODING_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DECODING_OTHER: Int
```

Error code for other decoding errors 

 Value: 16

### ERROR_DRM_CONTENT_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DRM_CONTENT_ERROR: Int
```

Error code for attempting to play incompatible DRM-protected content 

 Value: 28

### ERROR_DRM_DEVICE_REVOKED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DRM_DEVICE_REVOKED: Int
```

Error code for the device having revoked DRM privileges 

 Value: 29

### ERROR_DRM_DISALLOWED_OPERATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DRM_DISALLOWED_OPERATION: Int
```

Error code an operation being disallowed by a license policy 

 Value: 26

### ERROR_DRM_LICENSE_ACQUISITION_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DRM_LICENSE_ACQUISITION_FAILED: Int
```

Error code for a failure while trying to obtain a license 

 Value: 25

### ERROR_DRM_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DRM_OTHER: Int
```

Error code for other DRM errors 

 Value: 30

### ERROR_DRM_PROVISIONING_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DRM_PROVISIONING_FAILED: Int
```

Error code for a failure while provisioning the device 

 Value: 24

### ERROR_DRM_SCHEME_UNSUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DRM_SCHEME_UNSUPPORTED: Int
```

Error code for a chosen DRM protection scheme not being supported by the device 

 Value: 23

### ERROR_DRM_SYSTEM_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DRM_SYSTEM_ERROR: Int
```

Error code for an error in the DRM system 

 Value: 27

### ERROR_IO_BAD_HTTP_STATUS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_BAD_HTTP_STATUS: Int
```

Error code for an HTTP server returning an unexpected HTTP response status code 

 Value: 5

### ERROR_IO_CONNECTION_CLOSED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_CONNECTION_CLOSED: Int
```

Error code for an existing network connection being unexpectedly closed 

 Value: 8

### ERROR_IO_CONNECTION_TIMEOUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_CONNECTION_TIMEOUT: Int
```

Error code for a network timeout, meaning the server is taking too long to fulfill a request 

 Value: 7

### ERROR_IO_DNS_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_DNS_FAILED: Int
```

Error code for failing to resolve a hostname 

 Value: 6

### ERROR_IO_FILE_NOT_FOUND

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_FILE_NOT_FOUND: Int
```

Error code for a non-existent file 

 Value: 31

### ERROR_IO_NETWORK_CONNECTION_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_NETWORK_CONNECTION_FAILED: Int
```

Error code for a failure while establishing a network connection 

 Value: 4

### ERROR_IO_NETWORK_UNAVAILABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_NETWORK_UNAVAILABLE: Int
```

Error code for lack of network connectivity while trying to access a network resource 

 Value: 3

### ERROR_IO_NO_PERMISSION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_NO_PERMISSION: Int
```

Error code for lack of permission to perform an IO operation, for example, lack of permission to access internet or external storage. 

 Value: 32

### ERROR_IO_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO_OTHER: Int
```

Error code for other Input/Output errors 

 Value: 9

### ERROR_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_OTHER: Int
```

Error code for other errors 

 Value: 1

### ERROR_PARSING_CONTAINER_MALFORMED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PARSING_CONTAINER_MALFORMED: Int
```

Error code for a parsing error associated to a media container format bitstream 

 Value: 11

### ERROR_PARSING_CONTAINER_UNSUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PARSING_CONTAINER_UNSUPPORTED: Int
```

Error code for attempting to extract a file with an unsupported media container format, or an unsupported media container feature 

 Value: 34

### ERROR_PARSING_MANIFEST_MALFORMED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PARSING_MANIFEST_MALFORMED: Int
```

Error code for a parsing error associated to a media manifest 

 Value: 10

### ERROR_PARSING_MANIFEST_UNSUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PARSING_MANIFEST_UNSUPPORTED: Int
```

Error code for an unsupported feature in a media manifest 

 Value: 33

### ERROR_PARSING_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PARSING_OTHER: Int
```

Error code for other media parsing errors 

 Value: 12

### ERROR_PLAYER_BEHIND_LIVE_WINDOW

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PLAYER_BEHIND_LIVE_WINDOW: Int
```

Error code for the loading position falling behind the sliding window of available live content. 

 Value: 21

### ERROR_PLAYER_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PLAYER_OTHER: Int
```

Error code for other player errors 

 Value: 22

### ERROR_PLAYER_REMOTE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PLAYER_REMOTE: Int
```

Error code for an unidentified error in a remote controller or player 

 Value: 20

### ERROR_RUNTIME

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RUNTIME: Int
```

Error code for runtime errors 

 Value: 2

### ERROR_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN: Int
```

Unknown error code. 

 Value: 0

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getErrorCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getErrorCode(): Int
```

Gets error code.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackErrorEvent#ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_UNKNOWN:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_OTHER:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_RUNTIME](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_RUNTIME:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_NETWORK_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_NETWORK_UNAVAILABLE:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_NETWORK_CONNECTION_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_NETWORK_CONNECTION_FAILED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_BAD_HTTP_STATUS](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_BAD_HTTP_STATUS:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_DNS_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_DNS_FAILED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_CONNECTION_TIMEOUT](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_CONNECTION_TIMEOUT:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_CONNECTION_CLOSED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_CONNECTION_CLOSED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_OTHER:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_PARSING_MANIFEST_MALFORMED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_MANIFEST_MALFORMED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_PARSING_CONTAINER_MALFORMED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_CONTAINER_MALFORMED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_PARSING_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_OTHER:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DECODER_INIT_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODER_INIT_FAILED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DECODING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODING_FAILED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DECODING_FORMAT_EXCEEDS_CAPABILITIES](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODING_FORMAT_EXCEEDS_CAPABILITIES:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DECODING_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODING_OTHER:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_AUDIO_TRACK_INIT_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_AUDIO_TRACK_INIT_FAILED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_AUDIO_TRACK_WRITE_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_AUDIO_TRACK_WRITE_FAILED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_AUDIO_TRACK_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_AUDIO_TRACK_OTHER:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_PLAYER_REMOTE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PLAYER_REMOTE:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_PLAYER_BEHIND_LIVE_WINDOW](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PLAYER_BEHIND_LIVE_WINDOW:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_PLAYER_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PLAYER_OTHER:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DRM_SCHEME_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_SCHEME_UNSUPPORTED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DRM_PROVISIONING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_PROVISIONING_FAILED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DRM_LICENSE_ACQUISITION_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_LICENSE_ACQUISITION_FAILED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DRM_DISALLOWED_OPERATION](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_DISALLOWED_OPERATION:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DRM_SYSTEM_ERROR](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_SYSTEM_ERROR:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DRM_CONTENT_ERROR](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_CONTENT_ERROR:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DRM_DEVICE_REVOKED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_DEVICE_REVOKED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_DRM_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DRM_OTHER:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_FILE_NOT_FOUND](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_FILE_NOT_FOUND:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_IO_NO_PERMISSION](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_IO_NO_PERMISSION:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_PARSING_MANIFEST_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_MANIFEST_UNSUPPORTED:kotlin.Int), [android.media.metrics.PlaybackErrorEvent#ERROR_PARSING_CONTAINER_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_PARSING_CONTAINER_UNSUPPORTED:kotlin.Int), or [android.media.metrics.PlaybackErrorEvent#ERROR_DECODING_FORMAT_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent#ERROR_DECODING_FORMAT_UNSUPPORTED:kotlin.Int) |

### getMetricsBundle

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetricsBundle(): Bundle
```

Gets metrics-related information that is not supported by dedicated methods.

It is intended to be used for backwards compatibility by the metrics infrastructure.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getSubErrorCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubErrorCode(): Int
```

Gets sub error code.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between [java.lang.Integer#MIN_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MIN_VALUE:kotlin.Int) and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

### getTimeSinceCreatedMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeSinceCreatedMillis(): Long
```

Gets the timestamp since creation of the playback session in milliseconds.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the timestamp since the playback is created, or -1 if unknown. Value is -1 or greater |

**See Also**

- [android.media.metrics.LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)
- [android.media.metrics.PlaybackSession](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession) 

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PlaybackErrorEvent!>
```
