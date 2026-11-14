# MediaTimestamp

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaTimestamp

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaTimestamp "View this page in Java") 

```
class MediaTimestamp
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaTimestamp](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#) |

An immutable object that represents the linear correlation between the media time and the system time. It contains the media clock rate, together with the media timestamp of an anchor frame and the system time when that frame was presented or is committed to be presented.

The phrase "present" means that audio/video produced on device is detectable by an external observer off device. The time is based on the implementation's best effort, using whatever knowledge is available to the system, but cannot account for any delay unknown to the implementation. The anchor frame could be any frame, including a just-rendered frame, or even a theoretical or in-between frame, based on the source of the MediaTimestamp. When the anchor frame is a just-rendered one, the media time stands for current position of the playback or recording.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaTimestamp](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#MediaTimestamp(kotlin.Long,%20kotlin.Long,%20kotlin.Float))`(`mediaTimeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `nanoTimeNs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `clockRate:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAnchorMediaTimeUs](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#getAnchorMediaTimeUs())`()` Get the media time of the anchor in microseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAnchorSystemNanoTime](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#getAnchorSystemNanoTime())`()` Get the [system time](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime())corresponding to the media time in nanoseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAnchorSytemNanoTime](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#getAnchorSytemNanoTime())`()` Get the [system time](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime())corresponding to the media time in nanoseconds. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMediaClockRate](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#getMediaClockRate())`()` Get the rate of the media clock in relation to the system time. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#toString())`()` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MediaTimestamp](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#)! | [TIMESTAMP_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#TIMESTAMP_UNKNOWN:android.media.MediaTimestamp) An unknown media timestamp value |

## Public constructors

### MediaTimestamp

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaTimestamp(
    mediaTimeUs: Long, 
    nanoTimeNs: Long, 
    clockRate: Float)
```

Constructor.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaTimeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the media time of the anchor in microseconds |
| `nanoTimeNs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the [system time](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime())corresponding to the media time in nanoseconds. |
| `clockRate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the rate of the media clock in relation to the system time. Value is between 0.0f and [java.lang.Float#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Float.html#MAX_VALUE:kotlin.Float) inclusive |

## Public methods

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAnchorMediaTimeUs

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAnchorMediaTimeUs(): Long
```

Get the media time of the anchor in microseconds. 

### getAnchorSystemNanoTime

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAnchorSystemNanoTime(): Long
```

Get the [system time](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime())corresponding to the media time in nanoseconds. 

### getAnchorSytemNanoTime

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAnchorSytemNanoTime(): Long
```

**Deprecated:** *use [getAnchorSystemNanoTime](https://developer.android.com/reference/kotlin/android/media/MediaTimestamp#getAnchorSystemNanoTime())instead.*

Get the [system time](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime())corresponding to the media time in nanoseconds. 

### getMediaClockRate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaClockRate(): Float
```

Get the rate of the media clock in relation to the system time.

It is 1.0 if media clock advances in sync with the system clock; greater than 1.0 if media clock is faster than the system clock; less than 1.0 if media clock is slower than the system clock.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is between 0.0f and [java.lang.Float#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Float.html#MAX_VALUE:kotlin.Float) inclusive |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### TIMESTAMP_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMESTAMP_UNKNOWN: MediaTimestamp!
```

An unknown media timestamp value
