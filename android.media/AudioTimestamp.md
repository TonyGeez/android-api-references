# AudioTimestamp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioTimestamp

Kotlin| [Java](../android/media/AudioTimestamp.md) 
| --- | --- |

```
class AudioTimestamp : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioTimestamp](../android/media/AudioTimestamp.md) |

Structure that groups a position in frame units relative to an assumed audio stream, together with the estimated time when that frame enters or leaves the audio processing pipeline on that device. This can be used to coordinate events and interactions with the external environment.

The time is based on the implementation's best effort, using whatever knowledge is available to the system, but cannot account for any delay unknown to the implementation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEBASE_BOOTTIME](../android/media/AudioTimestamp.md) Clock monotonic including suspend time or its equivalent on the system, in the same units and timebase as [android.os.SystemClock#elapsedRealtimeNanos](../android/os/SystemClock.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEBASE_MONOTONIC](../android/media/AudioTimestamp.md) Clock monotonic or its equivalent on the system, in the same units and timebase as [java.lang.System#nanoTime](../java/lang/System.md)). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [AudioTimestamp](../android/media/AudioTimestamp.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/AudioTimestamp.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/media/AudioTimestamp.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/AudioTimestamp.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AudioTimestamp](../android/media/AudioTimestamp.md)!\> | [CREATOR](../android/media/AudioTimestamp.md) Creates an instance from a [Parcel](../android/os/Parcel.md). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [framePosition](../android/media/AudioTimestamp.md) Position in frames relative to start of an assumed audio stream. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nanoTime](../android/media/AudioTimestamp.md) Time associated with the frame in the audio pipeline. |
| --- | --- |

## Constants

### TIMEBASE_BOOTTIME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMEBASE_BOOTTIME: Int
```

Clock monotonic including suspend time or its equivalent on the system, in the same units and timebase as [android.os.SystemClock#elapsedRealtimeNanos](../android/os/SystemClock.md)). 

 Value: 1

### TIMEBASE_MONOTONIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMEBASE_MONOTONIC: Int
```

Clock monotonic or its equivalent on the system, in the same units and timebase as [java.lang.System#nanoTime](../java/lang/System.md)). 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AudioTimestamp!>
```

Creates an instance from a [Parcel](../android/os/Parcel.md). 

### framePosition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var framePosition: Long
```

Position in frames relative to start of an assumed audio stream.

When obtained through [AudioRecord.getTimestamp(AudioTimestamp, int)](../android/media/AudioRecord.md)), all 64 bits of position are valid.

When obtained through [AudioTrack.getTimestamp(AudioTimestamp)](../android/media/AudioTrack.md)), the low-order 32 bits of position is in wrapping frame units similar to [AudioTrack.getPlaybackHeadPosition()](../android/media/AudioTrack.md)). 

### nanoTime

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var nanoTime: Long
```

Time associated with the frame in the audio pipeline.

When obtained through [AudioRecord.getTimestamp(AudioTimestamp, int)](../android/media/AudioRecord.md)), this is the estimated time in nanoseconds when the frame referred to by [framePosition](../android/media/AudioTimestamp.md) was captured. The timebase is either [TIMEBASE_MONOTONIC](../android/media/AudioTimestamp.md) or [TIMEBASE_BOOTTIME](../android/media/AudioTimestamp.md), depending on the timebase parameter used in [AudioRecord.getTimestamp(AudioTimestamp, int)](../android/media/AudioRecord.md)).

When obtained through [AudioTrack.getTimestamp(AudioTimestamp)](../android/media/AudioTrack.md)), this is the estimated time when the frame was presented or is committed to be presented, with a timebase of [TIMEBASE_MONOTONIC](../android/media/AudioTimestamp.md).
