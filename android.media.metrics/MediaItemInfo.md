# MediaItemInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaItemInfo

Kotlin | [Java](https://developer.android.com/reference/android/media/metrics/MediaItemInfo "View this page in Java") 

```
class MediaItemInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.metrics.MediaItemInfo](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#) |

Represents information about a piece of media (for example, an audio or video file).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo.Builder) Builder for [MediaItemInfo](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#). |

| Constants ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_AUDIO](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_AUDIO:kotlin.Long) The media item includes audio data. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_DEPTH](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_DEPTH:kotlin.Long) The media item includes depth (z-distance) information. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_GAIN_MAP](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_GAIN_MAP:kotlin.Long) The media item includes gain map information (for example, an Ultra HDR gain map). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_GAPLESS](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_GAPLESS:kotlin.Long) The media item includes gapless audio metadata. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_HIGH_DYNAMIC_RANGE_VIDEO](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_HIGH_DYNAMIC_RANGE_VIDEO:kotlin.Long) The media item includes high dynamic range (HDR) video. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_HIGH_FRAME_RATE](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_HIGH_FRAME_RATE:kotlin.Long) The media item includes high frame rate video data. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_IMAGE](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_IMAGE:kotlin.Long) The media item includes image data. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_METADATA](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_METADATA:kotlin.Long) The media item includes static media container metadata (for example, capture frame rate or location information). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_SPATIAL_AUDIO](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_SPATIAL_AUDIO:kotlin.Long) The media item includes spatial audio data. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_SPEED_SETTING_CUE_POINTS](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_SPEED_SETTING_CUE_POINTS:kotlin.Long) The media item includes time-dependent speed information (for example, slow motion cue points). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DATA_TYPE_VIDEO](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_VIDEO:kotlin.Long) The media item includes video data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_TYPE_CAMERA](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_CAMERA:kotlin.Int) The media item came directly from camera capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_TYPE_EDITING_SESSION](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_EDITING_SESSION:kotlin.Int) The media item was output by a previous editing session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_TYPE_GALLERY](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_GALLERY:kotlin.Int) The media item came from the device gallery. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_TYPE_GENERATED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_GENERATED:kotlin.Int) The media item was generated by another system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_TYPE_LOCAL_FILE](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_LOCAL_FILE:kotlin.Int) The media item is stored on the local device's file system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_TYPE_REMOTE_FILE](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_REMOTE_FILE:kotlin.Int) The media item is a remote file (for example, it's loaded from an HTTP server). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_TYPE_REMOTE_LIVE_STREAM](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_REMOTE_LIVE_STREAM:kotlin.Int) The media item is a remotely-served live stream. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_TYPE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_UNSPECIFIED:kotlin.Int) The media item's source is not known. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) Special value for numerical fields where the value was not specified. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioChannelCount](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getAudioChannelCount())`()` Returns the number of audio channels, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAudioSampleCount](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getAudioSampleCount())`()` Returns the number of audio frames in the item, after clipping (if applicable), or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSampleRateHz](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getAudioSampleRateHz())`()` Returns the sample rate of audio, in Hertz, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getClipDurationMillis](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getClipDurationMillis())`()` Returns the duration of the clip taken from the media item, in milliseconds, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getCodecNames](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getCodecNames())`()` Returns the [media codec names](https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#getName()) for codecs that were used as part of encoding/decoding this media item, or an empty list if not known or not applicable. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getContainerMimeType](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getContainerMimeType())`()` Returns the MIME type of the media container, or `null` if unspecified. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDataTypes](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getDataTypes())`()` Returns the data types that are present in the media item. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDurationMillis](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getDurationMillis())`()` Returns the duration of the media item, in milliseconds, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSampleMimeTypes](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getSampleMimeTypes())`()` Returns the MIME types of samples stored in the media container, or an empty list if not known. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSourceType](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getSourceType())`()` Returns where the media item came from, or [SOURCE_TYPE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_UNSPECIFIED:kotlin.Int) if not specified. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoDataSpace](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getVideoDataSpace())`()` Returns the [data space](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#) for video, as a packed integer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVideoFrameRate](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getVideoFrameRate())`()` Returns the average video frame rate, in frames per second, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getVideoSampleCount](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getVideoSampleCount())`()` Returns the number of video frames, aftrer clipping (if applicable), or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. |
| [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#) | [getVideoSize](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#getVideoSize())`()` Returns the video size, in pixels, or a [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#) with width and height set to [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#toString())`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MediaItemInfo](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### DATA_TYPE_AUDIO

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_AUDIO: Long
```

The media item includes audio data. 

 Value: 4L

### DATA_TYPE_DEPTH

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_DEPTH: Long
```

The media item includes depth (z-distance) information. 

 Value: 16L

### DATA_TYPE_GAIN_MAP

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_GAIN_MAP: Long
```

The media item includes gain map information (for example, an Ultra HDR gain map). 

 Value: 32L

### DATA_TYPE_GAPLESS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_GAPLESS: Long
```

The media item includes gapless audio metadata. 

 Value: 256L

### DATA_TYPE_HIGH_DYNAMIC_RANGE_VIDEO

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_HIGH_DYNAMIC_RANGE_VIDEO: Long
```

The media item includes high dynamic range (HDR) video. 

 Value: 1024L

### DATA_TYPE_HIGH_FRAME_RATE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_HIGH_FRAME_RATE: Long
```

The media item includes high frame rate video data. 

 Value: 64L

### DATA_TYPE_IMAGE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_IMAGE: Long
```

The media item includes image data. 

 Value: 1L

### DATA_TYPE_METADATA

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_METADATA: Long
```

The media item includes static media container metadata (for example, capture frame rate or location information). 

 Value: 8L

### DATA_TYPE_SPATIAL_AUDIO

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_SPATIAL_AUDIO: Long
```

The media item includes spatial audio data. 

 Value: 512L

### DATA_TYPE_SPEED_SETTING_CUE_POINTS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_SPEED_SETTING_CUE_POINTS: Long
```

The media item includes time-dependent speed information (for example, slow motion cue points). 

 Value: 128L

### DATA_TYPE_VIDEO

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TYPE_VIDEO: Long
```

The media item includes video data. 

 Value: 2L

### SOURCE_TYPE_CAMERA

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_TYPE_CAMERA: Int
```

The media item came directly from camera capture. 

 Value: 2

### SOURCE_TYPE_EDITING_SESSION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_TYPE_EDITING_SESSION: Int
```

The media item was output by a previous editing session. 

 Value: 3

### SOURCE_TYPE_GALLERY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_TYPE_GALLERY: Int
```

The media item came from the device gallery. 

 Value: 1

### SOURCE_TYPE_GENERATED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_TYPE_GENERATED: Int
```

The media item was generated by another system. 

 Value: 7

### SOURCE_TYPE_LOCAL_FILE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_TYPE_LOCAL_FILE: Int
```

The media item is stored on the local device's file system. 

 Value: 4

### SOURCE_TYPE_REMOTE_FILE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_TYPE_REMOTE_FILE: Int
```

The media item is a remote file (for example, it's loaded from an HTTP server). 

 Value: 5

### SOURCE_TYPE_REMOTE_LIVE_STREAM

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_TYPE_REMOTE_LIVE_STREAM: Int
```

The media item is a remotely-served live stream. 

 Value: 6

### SOURCE_TYPE_UNSPECIFIED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_TYPE_UNSPECIFIED: Int
```

The media item's source is not known. 

 Value: 0

### VALUE_UNSPECIFIED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VALUE_UNSPECIFIED: Int
```

Special value for numerical fields where the value was not specified. 

 Value: -1

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAudioChannelCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioChannelCount(): Int
```

Returns the number of audio channels, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. 

### getAudioSampleCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioSampleCount(): Long
```

Returns the number of audio frames in the item, after clipping (if applicable), or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. 

### getAudioSampleRateHz

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioSampleRateHz(): Int
```

Returns the sample rate of audio, in Hertz, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. 

### getClipDurationMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClipDurationMillis(): Long
```

Returns the duration of the clip taken from the media item, in milliseconds, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. 

### getCodecNames

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecNames(): MutableList<String!>
```

Returns the [media codec names](https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#getName()) for codecs that were used as part of encoding/decoding this media item, or an empty list if not known or not applicable.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be `null`. |

### getContainerMimeType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContainerMimeType(): String?
```

Returns the MIME type of the media container, or `null` if unspecified. 

### getDataTypes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataTypes(): Long
```

Returns the data types that are present in the media item.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is either `0` or a combination of [android.media.metrics.MediaItemInfo#DATA_TYPE_IMAGE](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_IMAGE:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_VIDEO](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_VIDEO:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_AUDIO](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_AUDIO:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_METADATA](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_METADATA:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_DEPTH](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_DEPTH:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_GAIN_MAP](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_GAIN_MAP:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_HIGH_FRAME_RATE](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_HIGH_FRAME_RATE:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_SPEED_SETTING_CUE_POINTS](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_SPEED_SETTING_CUE_POINTS:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_GAPLESS](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_GAPLESS:kotlin.Long), [android.media.metrics.MediaItemInfo#DATA_TYPE_SPATIAL_AUDIO](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_SPATIAL_AUDIO:kotlin.Long), and [android.media.metrics.MediaItemInfo#DATA_TYPE_HIGH_DYNAMIC_RANGE_VIDEO](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#DATA_TYPE_HIGH_DYNAMIC_RANGE_VIDEO:kotlin.Long) |

### getDurationMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDurationMillis(): Long
```

Returns the duration of the media item, in milliseconds, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. 

### getSampleMimeTypes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleMimeTypes(): MutableList<String!>
```

Returns the MIME types of samples stored in the media container, or an empty list if not known.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be `null`. |

### getSourceType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSourceType(): Int
```

Returns where the media item came from, or [SOURCE_TYPE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_UNSPECIFIED:kotlin.Int) if not specified.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.MediaItemInfo#SOURCE_TYPE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_UNSPECIFIED:kotlin.Int), [android.media.metrics.MediaItemInfo#SOURCE_TYPE_GALLERY](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_GALLERY:kotlin.Int), [android.media.metrics.MediaItemInfo#SOURCE_TYPE_CAMERA](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_CAMERA:kotlin.Int), [android.media.metrics.MediaItemInfo#SOURCE_TYPE_EDITING_SESSION](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_EDITING_SESSION:kotlin.Int), [android.media.metrics.MediaItemInfo#SOURCE_TYPE_LOCAL_FILE](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_LOCAL_FILE:kotlin.Int), [android.media.metrics.MediaItemInfo#SOURCE_TYPE_REMOTE_FILE](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_REMOTE_FILE:kotlin.Int), [android.media.metrics.MediaItemInfo#SOURCE_TYPE_REMOTE_LIVE_STREAM](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_REMOTE_LIVE_STREAM:kotlin.Int), or [android.media.metrics.MediaItemInfo#SOURCE_TYPE_GENERATED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#SOURCE_TYPE_GENERATED:kotlin.Int) |

### getVideoDataSpace

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoDataSpace(): Int
```

Returns the [data space](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#) for video, as a packed integer. 

### getVideoFrameRate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoFrameRate(): Float
```

Returns the average video frame rate, in frames per second, or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. 

### getVideoSampleCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoSampleCount(): Long
```

Returns the number of video frames, aftrer clipping (if applicable), or [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified. 

### getVideoSize

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoSize(): Size
```

Returns the video size, in pixels, or a [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#) with width and height set to [VALUE_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/media/metrics/MediaItemInfo#VALUE_UNSPECIFIED:kotlin.Int) if not specified.

| Return ||
|--------------------------------------------------------------------------------|------------------------------|
| [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#) | This value cannot be `null`. |

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
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be `null`. |

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
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MediaItemInfo!>
```
