# TrackChangeEvent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrackChangeEvent

Kotlin| [Java](https://developer.android.com/reference/android/media/metrics/TrackChangeEvent "View this page in Java") 
| --- | --- |

```
class TrackChangeEvent : Event, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.metrics.Event](https://developer.android.com/reference/kotlin/android/media/metrics/Event) ||
| | ↳ | [android.media.metrics.TrackChangeEvent](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#) |

Playback track change event.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent.Builder) A builder for [TrackChangeEvent](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#) |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_CHANGE_REASON_ADAPTIVE](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_ADAPTIVE:kotlin.Int) Track change reason for adaptive changes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_CHANGE_REASON_INITIAL](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_INITIAL:kotlin.Int) Track change reason for initial state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_CHANGE_REASON_MANUAL](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_MANUAL:kotlin.Int) Track change reason for manual changes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_CHANGE_REASON_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_OTHER:kotlin.Int) Other track change reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_CHANGE_REASON_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_UNKNOWN:kotlin.Int) Unknown track change reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_STATE_OFF](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_STATE_OFF:kotlin.Int) The track is off. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_STATE_ON](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_STATE_ON:kotlin.Int) The track is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_TYPE_AUDIO](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_AUDIO:kotlin.Int) Audio track. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_TYPE_TEXT](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_TEXT:kotlin.Int) Text track. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACK_TYPE_VIDEO](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_VIDEO:kotlin.Int) Video track. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAudioSampleRate](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getAudioSampleRate())`()` Gets audio sample rate. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBitrate](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getBitrate())`()` Gets bitrate. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelCount](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getChannelCount())`()` Gets channel count. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getCodecName](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getCodecName())`()` Gets codec name. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getContainerMimeType](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getContainerMimeType())`()` Gets container MIME type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getHeight())`()` Gets video height. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getLanguage](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getLanguage())`()` Gets language code. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getLanguageRegion](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getLanguageRegion())`()` Gets language region code. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getMetricsBundle](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getMetricsBundle())`()` Gets metrics-related information that is not supported by dedicated methods. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSampleMimeType](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getSampleMimeType())`()` Gets the MIME type of the video/audio/text samples. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeSinceCreatedMillis](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getTimeSinceCreatedMillis())`()` Gets timestamp since the creation of the log session in milliseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrackChangeReason](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getTrackChangeReason())`()` Gets track change reason. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrackState](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getTrackState())`()` Gets track state. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrackType](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getTrackType())`()` Gets the track type. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVideoFrameRate](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getVideoFrameRate())`()` Gets video frame rate. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#getWidth())`()` Gets video width. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TrackChangeEvent](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TRACK_CHANGE_REASON_ADAPTIVE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_CHANGE_REASON_ADAPTIVE: Int
```

Track change reason for adaptive changes. 

 Value: 4

### TRACK_CHANGE_REASON_INITIAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_CHANGE_REASON_INITIAL: Int
```

Track change reason for initial state. 

 Value: 2

### TRACK_CHANGE_REASON_MANUAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_CHANGE_REASON_MANUAL: Int
```

Track change reason for manual changes. 

 Value: 3

### TRACK_CHANGE_REASON_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_CHANGE_REASON_OTHER: Int
```

Other track change reason. 

 Value: 1

### TRACK_CHANGE_REASON_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_CHANGE_REASON_UNKNOWN: Int
```

Unknown track change reason. 

 Value: 0

### TRACK_STATE_OFF

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_STATE_OFF: Int
```

The track is off. 

 Value: 0

### TRACK_STATE_ON

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_STATE_ON: Int
```

The track is on. 

 Value: 1

### TRACK_TYPE_AUDIO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_TYPE_AUDIO: Int
```

Audio track. 

 Value: 0

### TRACK_TYPE_TEXT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_TYPE_TEXT: Int
```

Text track. 

 Value: 2

### TRACK_TYPE_VIDEO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACK_TYPE_VIDEO: Int
```

Video track. 

 Value: 1

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

### getAudioSampleRate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioSampleRate(): Int
```

Gets audio sample rate.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the sample rate, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

### getBitrate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBitrate(): Int
```

Gets bitrate.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the bitrate, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

### getChannelCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelCount(): Int
```

Gets channel count.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the channel count, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

### getCodecName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecName(): String?
```

Gets codec name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getContainerMimeType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContainerMimeType(): String?
```

Gets container MIME type.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getHeight

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

Gets video height.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the video height, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

### getLanguage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLanguage(): String?
```

Gets language code.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a two-letter ISO 639-1 language code. This value may be`null`. |

### getLanguageRegion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLanguageRegion(): String?
```

Gets language region code.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | an IETF BCP 47 optional language region subtag based on a two-letter country code. This value may be`null`. |

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

### getSampleMimeType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleMimeType(): String?
```

Gets the MIME type of the video/audio/text samples.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getTimeSinceCreatedMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeSinceCreatedMillis(): Long
```

Gets timestamp since the creation of the log session in milliseconds.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the timestamp since the creation in milliseconds, or -1 if unknown. Value is -1 or greater |

**See Also**

- [android.media.metrics.LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)
- [android.media.metrics.PlaybackSession](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession)
- [android.media.metrics.RecordingSession](https://developer.android.com/reference/kotlin/android/media/metrics/RecordingSession) 

### getTrackChangeReason

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrackChangeReason(): Int
```

Gets track change reason.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.TrackChangeEvent#TRACK_CHANGE_REASON_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_UNKNOWN:kotlin.Int), [android.media.metrics.TrackChangeEvent#TRACK_CHANGE_REASON_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_OTHER:kotlin.Int), [android.media.metrics.TrackChangeEvent#TRACK_CHANGE_REASON_INITIAL](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_INITIAL:kotlin.Int), [android.media.metrics.TrackChangeEvent#TRACK_CHANGE_REASON_MANUAL](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_MANUAL:kotlin.Int), or [android.media.metrics.TrackChangeEvent#TRACK_CHANGE_REASON_ADAPTIVE](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_CHANGE_REASON_ADAPTIVE:kotlin.Int) |

### getTrackState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrackState(): Int
```

Gets track state.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.TrackChangeEvent#TRACK_STATE_OFF](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_STATE_OFF:kotlin.Int), or [android.media.metrics.TrackChangeEvent#TRACK_STATE_ON](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_STATE_ON:kotlin.Int) |

### getTrackType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrackType(): Int
```

Gets the track type.

The track type must be one of [TRACK_TYPE_AUDIO](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_AUDIO:kotlin.Int), [TRACK_TYPE_VIDEO](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_VIDEO:kotlin.Int), [TRACK_TYPE_TEXT](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_TEXT:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.TrackChangeEvent#TRACK_TYPE_AUDIO](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_AUDIO:kotlin.Int), [android.media.metrics.TrackChangeEvent#TRACK_TYPE_VIDEO](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_VIDEO:kotlin.Int), or [android.media.metrics.TrackChangeEvent#TRACK_TYPE_TEXT](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent#TRACK_TYPE_TEXT:kotlin.Int) |

### getVideoFrameRate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVideoFrameRate(): Float
```

Gets video frame rate.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the video frame rate, or -1 if unknown. Value is between -1.0f and [java.lang.Float#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Float.html#MAX_VALUE:kotlin.Float) inclusive |

### getWidth

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

Gets video width.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the video width, or -1 if unknown. Value is between -1 and [java.lang.Integer#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int) inclusive |

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
static val CREATOR: Parcelable.Creator<TrackChangeEvent!>
```
