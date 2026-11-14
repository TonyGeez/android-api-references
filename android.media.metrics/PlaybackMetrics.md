# PlaybackMetrics

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlaybackMetrics

Kotlin| [Java](../android/media/metrics/PlaybackMetrics.md) 
| --- | --- |

```
class PlaybackMetrics : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.metrics.PlaybackMetrics](../android/media/metrics/PlaybackMetrics.md) |

This class is used to store playback data.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/media/metrics/PlaybackMetrics.Builder.md) A builder for [PlaybackMetrics](../android/media/metrics/PlaybackMetrics.md) |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_AD](../android/media/metrics/PlaybackMetrics.md) Advertisement contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MAIN](../android/media/metrics/PlaybackMetrics.md) Main contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_OTHER](../android/media/metrics/PlaybackMetrics.md) Other contents. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_UNKNOWN](../android/media/metrics/PlaybackMetrics.md) Unknown content type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_CLEARKEY](../android/media/metrics/PlaybackMetrics.md) Clear key DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_NONE](../android/media/metrics/PlaybackMetrics.md) DRM is not used. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_OTHER](../android/media/metrics/PlaybackMetrics.md) Other DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_PLAY_READY](../android/media/metrics/PlaybackMetrics.md) Play ready DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_WIDEVINE_L1](../android/media/metrics/PlaybackMetrics.md) Widevine L1 DRM type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_WIDEVINE_L3](../android/media/metrics/PlaybackMetrics.md) Widevine L3 DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRM_TYPE_WV_L3_FALLBACK](../android/media/metrics/PlaybackMetrics.md) Widevine L3 fallback DRM type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_TYPE_LIVE](../android/media/metrics/PlaybackMetrics.md) Live playback type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_TYPE_OTHER](../android/media/metrics/PlaybackMetrics.md) Other playback type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_TYPE_UNKNOWN](../android/media/metrics/PlaybackMetrics.md) Unknown playback type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_TYPE_VOD](../android/media/metrics/PlaybackMetrics.md) VOD (Video on Demand) playback type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_SOURCE_DEVICE](../android/media/metrics/PlaybackMetrics.md) Stream from device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_SOURCE_MIXED](../android/media/metrics/PlaybackMetrics.md) Stream from more than one sources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_SOURCE_NETWORK](../android/media/metrics/PlaybackMetrics.md) Stream from network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_SOURCE_UNKNOWN](../android/media/metrics/PlaybackMetrics.md) Unknown stream source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_DASH](../android/media/metrics/PlaybackMetrics.md) DASH (Dynamic Adaptive Streaming over HTTP) stream type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_HLS](../android/media/metrics/PlaybackMetrics.md) HLS (HTTP Live Streaming) stream type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_OTHER](../android/media/metrics/PlaybackMetrics.md) Other stream type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_PROGRESSIVE](../android/media/metrics/PlaybackMetrics.md) Progressive stream type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_SS](../android/media/metrics/PlaybackMetrics.md) SS (HTTP Smooth Streaming) stream type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STREAM_TYPE_UNKNOWN](../android/media/metrics/PlaybackMetrics.md) Unknown stream type. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/metrics/PlaybackMetrics.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/media/metrics/PlaybackMetrics.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioUnderrunCount](../android/media/metrics/PlaybackMetrics.md))`()` Gets audio underrun count. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContentType](../android/media/metrics/PlaybackMetrics.md))`()` Gets content type. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getDrmSessionId](../android/media/metrics/PlaybackMetrics.md))`()` Gets DRM session ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDrmType](../android/media/metrics/PlaybackMetrics.md))`()` Gets DRM type. |
| --- | --- |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | [getExperimentIds](../android/media/metrics/PlaybackMetrics.md))`()` Gets experiment IDs. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLocalBytesRead](../android/media/metrics/PlaybackMetrics.md))`()` Gets number of local bytes read. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMediaDurationMillis](../android/media/metrics/PlaybackMetrics.md))`()` Gets the media duration in milliseconds. |
| --- | --- |
| [Bundle](../android/os/Bundle.md) | [getMetricsBundle](../android/media/metrics/PlaybackMetrics.md))`()` Gets metrics-related information that is not supported by dedicated methods. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNetworkBytesRead](../android/media/metrics/PlaybackMetrics.md))`()` Gets number of network bytes read. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNetworkTransferDurationMillis](../android/media/metrics/PlaybackMetrics.md))`()` Gets network transfer duration in milliseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPlaybackType](../android/media/metrics/PlaybackMetrics.md))`()` Gets playback type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPlayerName](../android/media/metrics/PlaybackMetrics.md))`()` Gets player name. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPlayerVersion](../android/media/metrics/PlaybackMetrics.md))`()` Gets player version. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStreamSource](../android/media/metrics/PlaybackMetrics.md))`()` Gets stream source type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStreamType](../android/media/metrics/PlaybackMetrics.md))`()` Gets stream type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoFramesDropped](../android/media/metrics/PlaybackMetrics.md))`()` Gets video frames dropped. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoFramesPlayed](../android/media/metrics/PlaybackMetrics.md))`()` Gets video frames played. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/media/metrics/PlaybackMetrics.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/media/metrics/PlaybackMetrics.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/metrics/PlaybackMetrics.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PlaybackMetrics](../android/media/metrics/PlaybackMetrics.md)!\> | [CREATOR](../android/media/metrics/PlaybackMetrics.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the audio underrun count, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](../java/lang/Integer.md) inclusive |

### getContentType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentType(): Int
```

Gets content type.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#CONTENT_TYPE_UNKNOWN](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#CONTENT_TYPE_MAIN](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#CONTENT_TYPE_AD](../android/media/metrics/PlaybackMetrics.md), or [android.media.metrics.PlaybackMetrics#CONTENT_TYPE_OTHER](../android/media/metrics/PlaybackMetrics.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#DRM_TYPE_NONE](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#DRM_TYPE_OTHER](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#DRM_TYPE_PLAY_READY](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#DRM_TYPE_WIDEVINE_L1](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#DRM_TYPE_WIDEVINE_L3](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#DRM_TYPE_WV_L3_FALLBACK](../android/media/metrics/PlaybackMetrics.md), or [android.media.metrics.PlaybackMetrics#DRM_TYPE_CLEARKEY](../android/media/metrics/PlaybackMetrics.md) |

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
| [Bundle](../android/os/Bundle.md) | This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#PLAYBACK_TYPE_UNKNOWN](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#PLAYBACK_TYPE_VOD](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#PLAYBACK_TYPE_LIVE](../android/media/metrics/PlaybackMetrics.md), or [android.media.metrics.PlaybackMetrics#PLAYBACK_TYPE_OTHER](../android/media/metrics/PlaybackMetrics.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#STREAM_SOURCE_UNKNOWN](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#STREAM_SOURCE_NETWORK](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#STREAM_SOURCE_DEVICE](../android/media/metrics/PlaybackMetrics.md), or [android.media.metrics.PlaybackMetrics#STREAM_SOURCE_MIXED](../android/media/metrics/PlaybackMetrics.md) |

### getStreamType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStreamType(): Int
```

Gets stream type.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackMetrics#STREAM_TYPE_UNKNOWN](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#STREAM_TYPE_OTHER](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#STREAM_TYPE_PROGRESSIVE](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#STREAM_TYPE_DASH](../android/media/metrics/PlaybackMetrics.md), [android.media.metrics.PlaybackMetrics#STREAM_TYPE_HLS](../android/media/metrics/PlaybackMetrics.md), or [android.media.metrics.PlaybackMetrics#STREAM_TYPE_SS](../android/media/metrics/PlaybackMetrics.md) |

### getVideoFramesDropped

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoFramesDropped(): Int
```

Gets video frames dropped.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the video frames dropped, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](../java/lang/Integer.md) inclusive |

### getVideoFramesPlayed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoFramesPlayed(): Int
```

Gets video frames played.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the video frames played, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](../java/lang/Integer.md) inclusive |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PlaybackMetrics!>
```
