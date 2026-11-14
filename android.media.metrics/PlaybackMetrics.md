# PlaybackMetrics

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlaybackMetrics

Kotlin| [Java](https://developer.android.com/reference/android/media/metrics/PlaybackMetrics "View this page in Java") 
| --- | --- |

```
class PlaybackMetrics : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.metrics.PlaybackMetrics](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#) |

This class is used to store playback data.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics.Builder) A builder for [PlaybackMetrics](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#) |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_AD](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CONTENT_TYPE_AD:kotlin.Int) Advertisement contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MAIN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CONTENT_TYPE_MAIN:kotlin.Int) Main contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CONTENT_TYPE_OTHER:kotlin.Int) Other contents. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CONTENT_TYPE_UNKNOWN:kotlin.Int) Unknown content type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_CLEARKEY](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_CLEARKEY:kotlin.Int) Clear key DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_NONE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_NONE:kotlin.Int) DRM is not used. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_OTHER:kotlin.Int) Other DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_PLAY_READY](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_PLAY_READY:kotlin.Int) Play ready DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_WIDEVINE_L1](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_WIDEVINE_L1:kotlin.Int) Widevine L1 DRM type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_WIDEVINE_L3](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_WIDEVINE_L3:kotlin.Int) Widevine L3 DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_WV_L3_FALLBACK](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_WV_L3_FALLBACK:kotlin.Int) Widevine L3 fallback DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_TYPE_LIVE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#PLAYBACK_TYPE_LIVE:kotlin.Int) Live playback type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#PLAYBACK_TYPE_OTHER:kotlin.Int) Other playback type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#PLAYBACK_TYPE_UNKNOWN:kotlin.Int) Unknown playback type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_TYPE_VOD](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#PLAYBACK_TYPE_VOD:kotlin.Int) VOD (Video on Demand) playback type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_SOURCE_DEVICE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_SOURCE_DEVICE:kotlin.Int) Stream from device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_SOURCE_MIXED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_SOURCE_MIXED:kotlin.Int) Stream from more than one sources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_SOURCE_NETWORK](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_SOURCE_NETWORK:kotlin.Int) Stream from network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_SOURCE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_SOURCE_UNKNOWN:kotlin.Int) Unknown stream source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_DASH](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_DASH:kotlin.Int) DASH (Dynamic Adaptive Streaming over HTTP) stream type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_HLS](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_HLS:kotlin.Int) HLS (HTTP Live Streaming) stream type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_OTHER:kotlin.Int) Other stream type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_PROGRESSIVE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_PROGRESSIVE:kotlin.Int) Progressive stream type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_SS](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_SS:kotlin.Int) SS (HTTP Smooth Streaming) stream type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_UNKNOWN:kotlin.Int) Unknown stream type. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioUnderrunCount](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getAudioUnderrunCount())`()` Gets audio underrun count. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContentType](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getContentType())`()` Gets content type. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getDrmSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getDrmSessionId())`()` Gets DRM session ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDrmType](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getDrmType())`()` Gets DRM type. |
| --- | --- |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | [getExperimentIds](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getExperimentIds())`()` Gets experiment IDs. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLocalBytesRead](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getLocalBytesRead())`()` Gets number of local bytes read. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMediaDurationMillis](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getMediaDurationMillis())`()` Gets the media duration in milliseconds. |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getMetricsBundle](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getMetricsBundle())`()` Gets metrics-related information that is not supported by dedicated methods. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNetworkBytesRead](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getNetworkBytesRead())`()` Gets number of network bytes read. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNetworkTransferDurationMillis](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getNetworkTransferDurationMillis())`()` Gets network transfer duration in milliseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPlaybackType](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getPlaybackType())`()` Gets playback type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPlayerName](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getPlayerName())`()` Gets player name. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPlayerVersion](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getPlayerVersion())`()` Gets player version. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStreamSource](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getStreamSource())`()` Gets stream source type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStreamType](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getStreamType())`()` Gets stream type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoFramesDropped](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getVideoFramesDropped())`()` Gets video frames dropped. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoFramesPlayed](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#getVideoFramesPlayed())`()` Gets video frames played. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#toString())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PlaybackMetrics](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CONTENT_TYPE_AD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_AD: Int
```

Advertisement contents. 

 Value: 2

### CONTENT_TYPE_MAIN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_MAIN: Int
```

Main contents. 

 Value: 1

### CONTENT_TYPE_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_OTHER: Int
```

Other contents. 

 Value: 3

### CONTENT_TYPE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_UNKNOWN: Int
```

Unknown content type. 

 Value: 0

### DRM_TYPE_CLEARKEY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_TYPE_CLEARKEY: Int
```

Clear key DRM type. 

 Value: 6

### DRM_TYPE_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_TYPE_NONE: Int
```

DRM is not used. 

 Value: 0

### DRM_TYPE_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_TYPE_OTHER: Int
```

Other DRM type. 

 Value: 1

### DRM_TYPE_PLAY_READY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_TYPE_PLAY_READY: Int
```

Play ready DRM type. 

 Value: 2

### DRM_TYPE_WIDEVINE_L1

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_TYPE_WIDEVINE_L1: Int
```

Widevine L1 DRM type. 

 Value: 3

### DRM_TYPE_WIDEVINE_L3

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_TYPE_WIDEVINE_L3: Int
```

Widevine L3 DRM type. 

 Value: 4

### DRM_TYPE_WV_L3_FALLBACK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRM_TYPE_WV_L3_FALLBACK: Int
```

Widevine L3 fallback DRM type. 

 Value: 5

### PLAYBACK_TYPE_LIVE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYBACK_TYPE_LIVE: Int
```

Live playback type. 

 Value: 2

### PLAYBACK_TYPE_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYBACK_TYPE_OTHER: Int
```

Other playback type. 

 Value: 3

### PLAYBACK_TYPE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYBACK_TYPE_UNKNOWN: Int
```

Unknown playback type. 

 Value: 0

### PLAYBACK_TYPE_VOD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYBACK_TYPE_VOD: Int
```

VOD (Video on Demand) playback type. 

 Value: 1

### STREAM_SOURCE_DEVICE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_SOURCE_DEVICE: Int
```

Stream from device. 

 Value: 2

### STREAM_SOURCE_MIXED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_SOURCE_MIXED: Int
```

Stream from more than one sources. 

 Value: 3

### STREAM_SOURCE_NETWORK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_SOURCE_NETWORK: Int
```

Stream from network. 

 Value: 1

### STREAM_SOURCE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_SOURCE_UNKNOWN: Int
```

Unknown stream source. 

 Value: 0

### STREAM_TYPE_DASH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_TYPE_DASH: Int
```

DASH (Dynamic Adaptive Streaming over HTTP) stream type. 

 Value: 3

### STREAM_TYPE_HLS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_TYPE_HLS: Int
```

HLS (HTTP Live Streaming) stream type. 

 Value: 4

### STREAM_TYPE_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_TYPE_OTHER: Int
```

Other stream type. 

 Value: 1

### STREAM_TYPE_PROGRESSIVE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_TYPE_PROGRESSIVE: Int
```

Progressive stream type. 

 Value: 2

### STREAM_TYPE_SS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_TYPE_SS: Int
```

SS (HTTP Smooth Streaming) stream type. 

 Value: 5

### STREAM_TYPE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STREAM_TYPE_UNKNOWN: Int
```

Unknown stream type. 

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

### getAudioUnderrunCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioUnderrunCount(): Int
```

Gets audio underrun count.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the audio underrun count, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

### getContentType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentType(): Int
```

Gets content type.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#CONTENT_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CONTENT_TYPE_UNKNOWN:kotlin.Int), [android.media.metrics.PlaybackMetrics#CONTENT_TYPE_MAIN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CONTENT_TYPE_MAIN:kotlin.Int), [android.media.metrics.PlaybackMetrics#CONTENT_TYPE_AD](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CONTENT_TYPE_AD:kotlin.Int), or [android.media.metrics.PlaybackMetrics#CONTENT_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#CONTENT_TYPE_OTHER:kotlin.Int) |

### getDrmSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDrmSessionId(): ByteArray
```

Gets DRM session ID.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

### getDrmType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDrmType(): Int
```

Gets DRM type.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#DRM_TYPE_NONE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_NONE:kotlin.Int), [android.media.metrics.PlaybackMetrics#DRM_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_OTHER:kotlin.Int), [android.media.metrics.PlaybackMetrics#DRM_TYPE_PLAY_READY](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_PLAY_READY:kotlin.Int), [android.media.metrics.PlaybackMetrics#DRM_TYPE_WIDEVINE_L1](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_WIDEVINE_L1:kotlin.Int), [android.media.metrics.PlaybackMetrics#DRM_TYPE_WIDEVINE_L3](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_WIDEVINE_L3:kotlin.Int), [android.media.metrics.PlaybackMetrics#DRM_TYPE_WV_L3_FALLBACK](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_WV_L3_FALLBACK:kotlin.Int), or [android.media.metrics.PlaybackMetrics#DRM_TYPE_CLEARKEY](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#DRM_TYPE_CLEARKEY:kotlin.Int) |

### getExperimentIds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExperimentIds(): LongArray
```

Gets experiment IDs.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | This value cannot be`null`. |

### getLocalBytesRead

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocalBytesRead(): Long
```

Gets number of local bytes read.

| Return ||
|------------------------------------------------------------------------------|------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is -1 or greater |

### getMediaDurationMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaDurationMillis(): Long
```

Gets the media duration in milliseconds.

Media duration is the length of the media.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the media duration in milliseconds, or -1 if unknown. Value is -1 or greater |

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

### getNetworkBytesRead

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkBytesRead(): Long
```

Gets number of network bytes read.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of network bytes read, or -1 if unknown. Value is -1 or greater |

### getNetworkTransferDurationMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkTransferDurationMillis(): Long
```

Gets network transfer duration in milliseconds.

Total transfer time spent reading from the network in ms. For parallel requests, the overlapping time intervals are counted only once.

| Return ||
|------------------------------------------------------------------------------|------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is -1 or greater |

### getPlaybackType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlaybackType(): Int
```

Gets playback type.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#PLAYBACK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#PLAYBACK_TYPE_UNKNOWN:kotlin.Int), [android.media.metrics.PlaybackMetrics#PLAYBACK_TYPE_VOD](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#PLAYBACK_TYPE_VOD:kotlin.Int), [android.media.metrics.PlaybackMetrics#PLAYBACK_TYPE_LIVE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#PLAYBACK_TYPE_LIVE:kotlin.Int), or [android.media.metrics.PlaybackMetrics#PLAYBACK_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#PLAYBACK_TYPE_OTHER:kotlin.Int) |

### getPlayerName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlayerName(): String?
```

Gets player name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getPlayerVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlayerVersion(): String?
```

Gets player version.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getStreamSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStreamSource(): Int
```

Gets stream source type.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#STREAM_SOURCE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_SOURCE_UNKNOWN:kotlin.Int), [android.media.metrics.PlaybackMetrics#STREAM_SOURCE_NETWORK](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_SOURCE_NETWORK:kotlin.Int), [android.media.metrics.PlaybackMetrics#STREAM_SOURCE_DEVICE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_SOURCE_DEVICE:kotlin.Int), or [android.media.metrics.PlaybackMetrics#STREAM_SOURCE_MIXED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_SOURCE_MIXED:kotlin.Int) |

### getStreamType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStreamType(): Int
```

Gets stream type.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#STREAM_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_UNKNOWN:kotlin.Int), [android.media.metrics.PlaybackMetrics#STREAM_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_OTHER:kotlin.Int), [android.media.metrics.PlaybackMetrics#STREAM_TYPE_PROGRESSIVE](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_PROGRESSIVE:kotlin.Int), [android.media.metrics.PlaybackMetrics#STREAM_TYPE_DASH](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_DASH:kotlin.Int), [android.media.metrics.PlaybackMetrics#STREAM_TYPE_HLS](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_HLS:kotlin.Int), or [android.media.metrics.PlaybackMetrics#STREAM_TYPE_SS](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackMetrics#STREAM_TYPE_SS:kotlin.Int) |

### getVideoFramesDropped

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoFramesDropped(): Int
```

Gets video frames dropped.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the video frames dropped, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

### getVideoFramesPlayed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoFramesPlayed(): Int
```

Gets video frames played.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the video frames played, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

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
static val CREATOR: Parcelable.Creator<PlaybackMetrics!>
```
