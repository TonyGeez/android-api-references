# EditingEndedEvent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EditingEndedEvent

Kotlin| [Java](https://developer.android.com/reference/android/media/metrics/EditingEndedEvent "View this page in Java") 

```
class EditingEndedEvent : Event, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.media.metrics.Event](https://developer.android.com/reference/kotlin/android/media/metrics/Event) ||
| | ↳ | [android.media.metrics.EditingEndedEvent](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#) |

Event for an editing operation having ended.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent.Builder) Builder for [EditingEndedEvent](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#) |

| Constants ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_AUDIO_PROCESSING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_AUDIO_PROCESSING_FAILED:kotlin.Int) Caused by an audio processing failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_DECODER_INIT_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_DECODER_INIT_FAILED:kotlin.Int) Caused by a decoder initialization failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_DECODING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_DECODING_FAILED:kotlin.Int) Caused by a failure while trying to decode media samples. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_DECODING_FORMAT_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_DECODING_FORMAT_UNSUPPORTED:kotlin.Int) Caused by trying to decode content whose format is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_ENCODER_INIT_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_ENCODER_INIT_FAILED:kotlin.Int) Caused by an encoder initialization failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_ENCODING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_ENCODING_FAILED:kotlin.Int) Caused by a failure while trying to encode media samples. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_ENCODING_FORMAT_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_ENCODING_FORMAT_UNSUPPORTED:kotlin.Int) Caused by trying to encode content whose format is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_FAILED_RUNTIME_CHECK](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_FAILED_RUNTIME_CHECK:kotlin.Int) Error code for unexpected runtime errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_IO_BAD_HTTP_STATUS](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_BAD_HTTP_STATUS:kotlin.Int) Caused by an HTTP server returning an unexpected HTTP response status code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_IO_CLEARTEXT_NOT_PERMITTED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_CLEARTEXT_NOT_PERMITTED:kotlin.Int) Caused by failing to load data via cleartext HTTP, when the app's network security configuration does not permit it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_IO_FILE_NOT_FOUND](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_FILE_NOT_FOUND:kotlin.Int) Caused by a non-existent file. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_IO_NETWORK_CONNECTION_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_NETWORK_CONNECTION_FAILED:kotlin.Int) Error code for network connection failures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_IO_NETWORK_CONNECTION_TIMEOUT](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_NETWORK_CONNECTION_TIMEOUT:kotlin.Int) Error code for network timeouts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_IO_NO_PERMISSION](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_NO_PERMISSION:kotlin.Int) Caused by lack of permission to perform an IO operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_IO_READ_POSITION_OUT_OF_RANGE](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_READ_POSITION_OUT_OF_RANGE:kotlin.Int) Caused by reading data out of the data bounds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_IO_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_UNSPECIFIED:kotlin.Int) Error code for non-specific errors during input/output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_MUXING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_MUXING_FAILED:kotlin.Int) Caused by a failure while muxing media samples. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_NONE](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_NONE:kotlin.Int) Special value representing that no error occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CODE_VIDEO_FRAME_PROCESSING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_VIDEO_FRAME_PROCESSING_FAILED:kotlin.Int) Caused by a video frame processing failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FINAL_STATE_CANCELED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#FINAL_STATE_CANCELED:kotlin.Int) The editing operation was canceled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FINAL_STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#FINAL_STATE_ERROR:kotlin.Int) The editing operation failed due to an error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FINAL_STATE_SUCCEEDED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#FINAL_STATE_SUCCEEDED:kotlin.Int) The editing operation was successful. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [OPERATION_TYPE_AUDIO_EDIT](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_AUDIO_EDIT:kotlin.Long) Input audio was edited. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [OPERATION_TYPE_AUDIO_TRANSCODE](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_AUDIO_TRANSCODE:kotlin.Long) Input audio was decoded and re-encoded. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [OPERATION_TYPE_AUDIO_TRANSMUX](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_AUDIO_TRANSMUX:kotlin.Long) Input audio samples were written (muxed) directly to the output file without transcoding. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [OPERATION_TYPE_PAUSED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_PAUSED:kotlin.Long) The editing operation was paused before it completed. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [OPERATION_TYPE_RESUMED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_RESUMED:kotlin.Long) The editing operation resumed a previous (paused) operation. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [OPERATION_TYPE_VIDEO_EDIT](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_VIDEO_EDIT:kotlin.Long) Input video was edited. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [OPERATION_TYPE_VIDEO_TRANSCODE](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_VIDEO_TRANSCODE:kotlin.Long) Input video was decoded and re-encoded. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [OPERATION_TYPE_VIDEO_TRANSMUX](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_VIDEO_TRANSMUX:kotlin.Long) Input video samples were written (muxed) directly to the output file without transcoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROGRESS_PERCENT_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#PROGRESS_PERCENT_UNKNOWN:kotlin.Int) Special value for unknown [final progress](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getFinalProgressPercent()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_SINCE_CREATED_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#TIME_SINCE_CREATED_UNKNOWN:kotlin.Int) Special value for unknown [time since creation](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getTimeSinceCreatedMillis()). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getErrorCode())`()` Returns the error code for a [failed](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#FINAL_STATE_ERROR:kotlin.Int) editing session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getExporterName](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getExporterName())`()` Returns the name of the library implementing the exporting operation, for example, a Maven artifact ID like "androidx. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFinalProgressPercent](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getFinalProgressPercent())`()` Returns the progress of the editing operation in percent at the moment that it ended, or [PROGRESS_PERCENT_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#PROGRESS_PERCENT_UNKNOWN:kotlin.Int) if unknown. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFinalState](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getFinalState())`()` Returns the state of the editing session when it ended. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaItemInfo](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo)!\> | [getInputMediaItemInfos](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getInputMediaItemInfos())`()` Gets information about the input media items, or an empty list if unspecified. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getMetricsBundle](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getMetricsBundle())`()` Gets metrics-related information that is not supported by dedicated methods. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMuxerName](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getMuxerName())`()` Returns the name of the library implementing the media muxing operation, for example, a Maven artifact ID like "androidx. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getOperationTypes](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getOperationTypes())`()` Gets a set of flags describing the types of operations performed. |
| [MediaItemInfo](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo)? | [getOutputMediaItemInfo](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getOutputMediaItemInfo())`()` Gets information about the output media item, or`null`if unspecified. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeSinceCreatedMillis](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getTimeSinceCreatedMillis())`()` Gets the elapsed time since creating of the editing session, in milliseconds, or [TIME_SINCE_CREATED_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#TIME_SINCE_CREATED_UNKNOWN:kotlin.Int) if unknown. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#toString())`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [EditingEndedEvent](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ERROR_CODE_AUDIO_PROCESSING_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_AUDIO_PROCESSING_FAILED: Int
```

Caused by an audio processing failure. 

 Value: 18

### ERROR_CODE_DECODER_INIT_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_DECODER_INIT_FAILED: Int
```

Caused by a decoder initialization failure. 

 Value: 11

### ERROR_CODE_DECODING_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_DECODING_FAILED: Int
```

Caused by a failure while trying to decode media samples. 

 Value: 12

### ERROR_CODE_DECODING_FORMAT_UNSUPPORTED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_DECODING_FORMAT_UNSUPPORTED: Int
```

Caused by trying to decode content whose format is not supported. 

 Value: 13

### ERROR_CODE_ENCODER_INIT_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_ENCODER_INIT_FAILED: Int
```

Caused by an encoder initialization failure. 

 Value: 14

### ERROR_CODE_ENCODING_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_ENCODING_FAILED: Int
```

Caused by a failure while trying to encode media samples. 

 Value: 15

### ERROR_CODE_ENCODING_FORMAT_UNSUPPORTED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_ENCODING_FORMAT_UNSUPPORTED: Int
```

Caused by trying to encode content whose format is not supported. 

 Value: 16

### ERROR_CODE_FAILED_RUNTIME_CHECK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_FAILED_RUNTIME_CHECK: Int
```

Error code for unexpected runtime errors. 

 Value: 2

### ERROR_CODE_IO_BAD_HTTP_STATUS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_IO_BAD_HTTP_STATUS: Int
```

Caused by an HTTP server returning an unexpected HTTP response status code. 

 Value: 6

### ERROR_CODE_IO_CLEARTEXT_NOT_PERMITTED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_IO_CLEARTEXT_NOT_PERMITTED: Int
```

Caused by failing to load data via cleartext HTTP, when the app's network security configuration does not permit it. 

 Value: 9

### ERROR_CODE_IO_FILE_NOT_FOUND

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_IO_FILE_NOT_FOUND: Int
```

Caused by a non-existent file. 

 Value: 7

### ERROR_CODE_IO_NETWORK_CONNECTION_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_IO_NETWORK_CONNECTION_FAILED: Int
```

Error code for network connection failures. 

 Value: 4

### ERROR_CODE_IO_NETWORK_CONNECTION_TIMEOUT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_IO_NETWORK_CONNECTION_TIMEOUT: Int
```

Error code for network timeouts. 

 Value: 5

### ERROR_CODE_IO_NO_PERMISSION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_IO_NO_PERMISSION: Int
```

Caused by lack of permission to perform an IO operation. For example, lack of permission to access internet or external storage. 

 Value: 8

### ERROR_CODE_IO_READ_POSITION_OUT_OF_RANGE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_IO_READ_POSITION_OUT_OF_RANGE: Int
```

Caused by reading data out of the data bounds. 

 Value: 10

### ERROR_CODE_IO_UNSPECIFIED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_IO_UNSPECIFIED: Int
```

Error code for non-specific errors during input/output. 

 Value: 3

### ERROR_CODE_MUXING_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_MUXING_FAILED: Int
```

Caused by a failure while muxing media samples. 

 Value: 19

### ERROR_CODE_NONE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_NONE: Int
```

Special value representing that no error occurred. 

 Value: 1

### ERROR_CODE_VIDEO_FRAME_PROCESSING_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE_VIDEO_FRAME_PROCESSING_FAILED: Int
```

Caused by a video frame processing failure. 

 Value: 17

### FINAL_STATE_CANCELED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINAL_STATE_CANCELED: Int
```

The editing operation was canceled. 

 Value: 2

### FINAL_STATE_ERROR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINAL_STATE_ERROR: Int
```

The editing operation failed due to an error. 

 Value: 3

### FINAL_STATE_SUCCEEDED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINAL_STATE_SUCCEEDED: Int
```

The editing operation was successful. 

 Value: 1

### OPERATION_TYPE_AUDIO_EDIT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATION_TYPE_AUDIO_EDIT: Long
```

Input audio was edited. 

 Value: 8L

### OPERATION_TYPE_AUDIO_TRANSCODE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATION_TYPE_AUDIO_TRANSCODE: Long
```

Input audio was decoded and re-encoded. 

 Value: 2L

### OPERATION_TYPE_AUDIO_TRANSMUX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATION_TYPE_AUDIO_TRANSMUX: Long
```

Input audio samples were written (muxed) directly to the output file without transcoding. 

 Value: 32L

### OPERATION_TYPE_PAUSED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATION_TYPE_PAUSED: Long
```

The editing operation was paused before it completed. 

 Value: 64L

### OPERATION_TYPE_RESUMED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATION_TYPE_RESUMED: Long
```

The editing operation resumed a previous (paused) operation. 

 Value: 128L

### OPERATION_TYPE_VIDEO_EDIT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATION_TYPE_VIDEO_EDIT: Long
```

Input video was edited. 

 Value: 4L

### OPERATION_TYPE_VIDEO_TRANSCODE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATION_TYPE_VIDEO_TRANSCODE: Long
```

Input video was decoded and re-encoded. 

 Value: 1L

### OPERATION_TYPE_VIDEO_TRANSMUX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPERATION_TYPE_VIDEO_TRANSMUX: Long
```

Input video samples were written (muxed) directly to the output file without transcoding. 

 Value: 16L

### PROGRESS_PERCENT_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROGRESS_PERCENT_UNKNOWN: Int
```

Special value for unknown [final progress](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getFinalProgressPercent()). 

 Value: -1

### TIME_SINCE_CREATED_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_SINCE_CREATED_UNKNOWN: Int
```

Special value for unknown [time since creation](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#getTimeSinceCreatedMillis()). 

 Value: -1

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getErrorCode(): Int
```

Returns the error code for a [failed](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#FINAL_STATE_ERROR:kotlin.Int) editing session.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.EditingEndedEvent#ERROR_CODE_NONE](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_NONE:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_FAILED_RUNTIME_CHECK](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_FAILED_RUNTIME_CHECK:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_IO_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_UNSPECIFIED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_IO_NETWORK_CONNECTION_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_NETWORK_CONNECTION_FAILED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_IO_NETWORK_CONNECTION_TIMEOUT](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_NETWORK_CONNECTION_TIMEOUT:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_IO_BAD_HTTP_STATUS](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_BAD_HTTP_STATUS:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_IO_FILE_NOT_FOUND](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_FILE_NOT_FOUND:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_IO_NO_PERMISSION](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_NO_PERMISSION:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_IO_CLEARTEXT_NOT_PERMITTED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_CLEARTEXT_NOT_PERMITTED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_IO_READ_POSITION_OUT_OF_RANGE](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_IO_READ_POSITION_OUT_OF_RANGE:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_DECODER_INIT_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_DECODER_INIT_FAILED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_DECODING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_DECODING_FAILED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_DECODING_FORMAT_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_DECODING_FORMAT_UNSUPPORTED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_ENCODER_INIT_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_ENCODER_INIT_FAILED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_ENCODING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_ENCODING_FAILED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_ENCODING_FORMAT_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_ENCODING_FORMAT_UNSUPPORTED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_VIDEO_FRAME_PROCESSING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_VIDEO_FRAME_PROCESSING_FAILED:kotlin.Int), [android.media.metrics.EditingEndedEvent#ERROR_CODE_AUDIO_PROCESSING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_AUDIO_PROCESSING_FAILED:kotlin.Int), or [android.media.metrics.EditingEndedEvent#ERROR_CODE_MUXING_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#ERROR_CODE_MUXING_FAILED:kotlin.Int) |

### getExporterName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExporterName(): String?
```

Returns the name of the library implementing the exporting operation, for example, a Maven artifact ID like "androidx.media3.media3-transformer:1.3.0-beta01", or`null`if unknown. 

### getFinalProgressPercent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFinalProgressPercent(): Float
```

Returns the progress of the editing operation in percent at the moment that it ended, or [PROGRESS_PERCENT_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#PROGRESS_PERCENT_UNKNOWN:kotlin.Int) if unknown. 

### getFinalState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFinalState(): Int
```

Returns the state of the editing session when it ended.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.EditingEndedEvent#FINAL_STATE_SUCCEEDED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#FINAL_STATE_SUCCEEDED:kotlin.Int), [android.media.metrics.EditingEndedEvent#FINAL_STATE_CANCELED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#FINAL_STATE_CANCELED:kotlin.Int), or [android.media.metrics.EditingEndedEvent#FINAL_STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#FINAL_STATE_ERROR:kotlin.Int) |

### getInputMediaItemInfos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputMediaItemInfos(): MutableList<MediaItemInfo!>
```

Gets information about the input media items, or an empty list if unspecified.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaItemInfo](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo)!> | This value cannot be`null`. |

### getMetricsBundle

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetricsBundle(): Bundle
```

Gets metrics-related information that is not supported by dedicated methods.

It is intended to be used for backwards compatibility by the metrics infrastructure.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getMuxerName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMuxerName(): String?
```

Returns the name of the library implementing the media muxing operation, for example, a Maven artifact ID like "androidx.media3.media3-muxer:1.3.0-beta01", or`null`if unknown. 

### getOperationTypes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOperationTypes(): Long
```

Gets a set of flags describing the types of operations performed.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is either`0`or a combination of [android.media.metrics.EditingEndedEvent#OPERATION_TYPE_VIDEO_TRANSCODE](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_VIDEO_TRANSCODE:kotlin.Long), [android.media.metrics.EditingEndedEvent#OPERATION_TYPE_AUDIO_TRANSCODE](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_AUDIO_TRANSCODE:kotlin.Long), [android.media.metrics.EditingEndedEvent#OPERATION_TYPE_VIDEO_EDIT](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_VIDEO_EDIT:kotlin.Long), [android.media.metrics.EditingEndedEvent#OPERATION_TYPE_AUDIO_EDIT](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_AUDIO_EDIT:kotlin.Long), [android.media.metrics.EditingEndedEvent#OPERATION_TYPE_VIDEO_TRANSMUX](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_VIDEO_TRANSMUX:kotlin.Long), [android.media.metrics.EditingEndedEvent#OPERATION_TYPE_AUDIO_TRANSMUX](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_AUDIO_TRANSMUX:kotlin.Long), [android.media.metrics.EditingEndedEvent#OPERATION_TYPE_PAUSED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_PAUSED:kotlin.Long), and [android.media.metrics.EditingEndedEvent#OPERATION_TYPE_RESUMED](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#OPERATION_TYPE_RESUMED:kotlin.Long) |

### getOutputMediaItemInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputMediaItemInfo(): MediaItemInfo?
```

Gets information about the output media item, or`null`if unspecified. 

### getTimeSinceCreatedMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeSinceCreatedMillis(): Long
```

Gets the elapsed time since creating of the editing session, in milliseconds, or [TIME_SINCE_CREATED_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#TIME_SINCE_CREATED_UNKNOWN:kotlin.Int) if unknown.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The elapsed time since creating the editing session, in milliseconds, or [TIME_SINCE_CREATED_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#TIME_SINCE_CREATED_UNKNOWN:kotlin.Int) if unknown. Value is [android.media.metrics.EditingEndedEvent#TIME_SINCE_CREATED_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent#TIME_SINCE_CREATED_UNKNOWN:kotlin.Int) or greater |

**See Also**

- [android.media.metrics.LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)
- [android.media.metrics.EditingSession](https://developer.android.com/reference/kotlin/android/media/metrics/EditingSession) 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<EditingEndedEvent!>
```
