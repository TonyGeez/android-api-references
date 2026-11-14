# AudioTimestamp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioTimestamp

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioTimestamp "View this page in Java") 
| --- | --- |

```
class AudioTimestamp : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioTimestamp](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#) |

Structure that groups a position in frame units relative to an assumed audio stream, together with the estimated time when that frame enters or leaves the audio processing pipeline on that device. This can be used to coordinate events and interactions with the external environment.

The time is based on the implementation's best effort, using whatever knowledge is available to the system, but cannot account for any delay unknown to the implementation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEBASE_BOOTTIME](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_BOOTTIME:kotlin.Int) Clock monotonic including suspend time or its equivalent on the system, in the same units and timebase as [android.os.SystemClock#elapsedRealtimeNanos](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEBASE_MONOTONIC](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_MONOTONIC:kotlin.Int) Clock monotonic or its equivalent on the system, in the same units and timebase as [java.lang.System#nanoTime](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime()). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [AudioTimestamp](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#AudioTimestamp())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#describeContents())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AudioTimestamp](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#CREATOR:android.os.Parcelable.Creator) Creates an instance from a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [framePosition](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#framePosition:kotlin.Long) Position in frames relative to start of an assumed audio stream. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nanoTime](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#nanoTime:kotlin.Long) Time associated with the frame in the audio pipeline. |
| --- | --- |

## Constants

### TIMEBASE_BOOTTIME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMEBASE_BOOTTIME: Int
```

Clock monotonic including suspend time or its equivalent on the system, in the same units and timebase as [android.os.SystemClock#elapsedRealtimeNanos](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()). 

 Value: 1

### TIMEBASE_MONOTONIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMEBASE_MONOTONIC: Int
```

Clock monotonic or its equivalent on the system, in the same units and timebase as [java.lang.System#nanoTime](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime()). 

 Value: 0

## Public constructors

### AudioTimestamp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AudioTimestamp()
```

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AudioTimestamp!>
```

Creates an instance from a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). 

### framePosition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var framePosition: Long
```

Position in frames relative to start of an assumed audio stream.

When obtained through [AudioRecord.getTimestamp(AudioTimestamp, int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getTimestamp(android.media.AudioTimestamp,%20kotlin.Int)), all 64 bits of position are valid.

When obtained through [AudioTrack.getTimestamp(AudioTimestamp)](https://developer.android.com/reference/kotlin/android/media/AudioTrack#getTimestamp(android.media.AudioTimestamp)), the low-order 32 bits of position is in wrapping frame units similar to [AudioTrack.getPlaybackHeadPosition()](https://developer.android.com/reference/kotlin/android/media/AudioTrack#getPlaybackHeadPosition()). 

### nanoTime

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var nanoTime: Long
```

Time associated with the frame in the audio pipeline.

When obtained through [AudioRecord.getTimestamp(AudioTimestamp, int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getTimestamp(android.media.AudioTimestamp,%20kotlin.Int)), this is the estimated time in nanoseconds when the frame referred to by [framePosition](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#framePosition:kotlin.Long) was captured. The timebase is either [TIMEBASE_MONOTONIC](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_MONOTONIC:kotlin.Int) or [TIMEBASE_BOOTTIME](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_BOOTTIME:kotlin.Int), depending on the timebase parameter used in [AudioRecord.getTimestamp(AudioTimestamp, int)](https://developer.android.com/reference/kotlin/android/media/AudioRecord#getTimestamp(android.media.AudioTimestamp,%20kotlin.Int)).

When obtained through [AudioTrack.getTimestamp(AudioTimestamp)](https://developer.android.com/reference/kotlin/android/media/AudioTrack#getTimestamp(android.media.AudioTimestamp)), this is the estimated time when the frame was presented or is committed to be presented, with a timebase of [TIMEBASE_MONOTONIC](https://developer.android.com/reference/kotlin/android/media/AudioTimestamp#TIMEBASE_MONOTONIC:kotlin.Int).
