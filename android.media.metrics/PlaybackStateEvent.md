# PlaybackStateEvent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlaybackStateEvent

Kotlin| [Java](https://developer.android.com/reference/android/media/metrics/PlaybackStateEvent "View this page in Java") 
| --- | --- |

```
class PlaybackStateEvent : Event, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.metrics.Event](https://developer.android.com/reference/kotlin/android/media/metrics/Event) ||
| | ↳ | [android.media.metrics.PlaybackStateEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#) |

Playback state event.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent.Builder) A builder for [PlaybackStateEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#) |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ABANDONED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_ABANDONED:kotlin.Int) Playback is abandoned before reaching the end of the media. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_BUFFERING:kotlin.Int) Playback is buffering to resume active playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ENDED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_ENDED:kotlin.Int) Playback has reached the end of the media. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_FAILED:kotlin.Int) Playback is stopped due a fatal error and can be retried. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_INTERRUPTED_BY_AD](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_INTERRUPTED_BY_AD:kotlin.Int) Playback is interrupted by an ad. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_JOINING_BACKGROUND](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_JOINING_BACKGROUND:kotlin.Int) Playback is buffering in the background for initial playback start |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_JOINING_FOREGROUND](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_JOINING_FOREGROUND:kotlin.Int) Playback is buffering in the foreground for initial playback start |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_NOT_STARTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_NOT_STARTED:kotlin.Int) Playback has not started (initial state) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PAUSED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_PAUSED:kotlin.Int) Playback is paused but ready to play |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PAUSED_BUFFERING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_PAUSED_BUFFERING:kotlin.Int) Playback is buffering while paused. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_PLAYING:kotlin.Int) Playback is actively playing |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SEEKING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_SEEKING:kotlin.Int) Playback is handling a seek. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_STOPPED:kotlin.Int) Playback is stopped and can be restarted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SUPPRESSED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_SUPPRESSED:kotlin.Int) Playback is suppressed (e.g. due to audio focus loss). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SUPPRESSED_BUFFERING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_SUPPRESSED_BUFFERING:kotlin.Int) Playback is suppressed (e.g. due to audio focus loss) while buffering to resume a playback. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getMetricsBundle](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#getMetricsBundle())`()` Gets metrics-related information that is not supported by dedicated methods. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#getState())`()` Gets playback state. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeSinceCreatedMillis](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#getTimeSinceCreatedMillis())`()` Gets time since the corresponding playback session is created in millisecond. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#hashCode())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PlaybackStateEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### STATE_ABANDONED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ABANDONED: Int
```

Playback is abandoned before reaching the end of the media. 

 Value: 15

### STATE_BUFFERING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_BUFFERING: Int
```

Playback is buffering to resume active playback. 

 Value: 6

### STATE_ENDED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ENDED: Int
```

Playback has reached the end of the media. 

 Value: 11

### STATE_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_FAILED: Int
```

Playback is stopped due a fatal error and can be retried. 

 Value: 13

### STATE_INTERRUPTED_BY_AD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_INTERRUPTED_BY_AD: Int
```

Playback is interrupted by an ad. 

 Value: 14

### STATE_JOINING_BACKGROUND

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_JOINING_BACKGROUND: Int
```

Playback is buffering in the background for initial playback start 

 Value: 1

### STATE_JOINING_FOREGROUND

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_JOINING_FOREGROUND: Int
```

Playback is buffering in the foreground for initial playback start 

 Value: 2

### STATE_NOT_STARTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_NOT_STARTED: Int
```

Playback has not started (initial state) 

 Value: 0

### STATE_PAUSED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_PAUSED: Int
```

Playback is paused but ready to play 

 Value: 4

### STATE_PAUSED_BUFFERING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_PAUSED_BUFFERING: Int
```

Playback is buffering while paused. 

 Value: 7

### STATE_PLAYING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_PLAYING: Int
```

Playback is actively playing 

 Value: 3

### STATE_SEEKING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SEEKING: Int
```

Playback is handling a seek. 

 Value: 5

### STATE_STOPPED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_STOPPED: Int
```

Playback is stopped and can be restarted. 

 Value: 12

### STATE_SUPPRESSED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SUPPRESSED: Int
```

Playback is suppressed (e.g. due to audio focus loss). 

 Value: 9

### STATE_SUPPRESSED_BUFFERING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SUPPRESSED_BUFFERING: Int
```

Playback is suppressed (e.g. due to audio focus loss) while buffering to resume a playback. 

 Value: 10

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

### getState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

Gets playback state.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.PlaybackStateEvent#STATE_NOT_STARTED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_NOT_STARTED:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_JOINING_BACKGROUND](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_JOINING_BACKGROUND:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_JOINING_FOREGROUND](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_JOINING_FOREGROUND:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_PLAYING:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_PAUSED:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_SEEKING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_SEEKING:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_BUFFERING:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_PAUSED_BUFFERING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_PAUSED_BUFFERING:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_SUPPRESSED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_SUPPRESSED:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_SUPPRESSED_BUFFERING](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_SUPPRESSED_BUFFERING:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_ENDED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_ENDED:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_STOPPED:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_FAILED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_FAILED:kotlin.Int), [android.media.metrics.PlaybackStateEvent#STATE_INTERRUPTED_BY_AD](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_INTERRUPTED_BY_AD:kotlin.Int), or [android.media.metrics.PlaybackStateEvent#STATE_ABANDONED](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent#STATE_ABANDONED:kotlin.Int) |

### getTimeSinceCreatedMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeSinceCreatedMillis(): Long
```

Gets time since the corresponding playback session is created in millisecond.

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
static val CREATOR: Parcelable.Creator<PlaybackStateEvent!>
```
