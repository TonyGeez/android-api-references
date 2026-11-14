# SyncFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncFence

Kotlin| [Java](https://developer.android.com/reference/android/hardware/SyncFence "View this page in Java") 

```
class SyncFence : AutoCloseable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#) |

A SyncFence represents a synchronization primitive which signals when hardware units have completed work on a particular resource. They initially start in an unsignaled state and make a one-time transition to either a signaled or error state. SyncFences are created by various device APIs in response to submitting tasks to the device. They cannot be created nor signaled by userspace. As a result, this means that a SyncFence will make always make forward progress.

SyncFence's generally come in one of two varieties. "Presentation fences" refer to a SyncFence when the writing to a buffer has finished. "Release fences" then refer to when the reading from a buffer has finished.

For example, a GPU rendering to a framebuffer may generate a synchronization fence, e.g., an EGLSync or VkFence, which signals when rendering has completed. Once the fence signals, then the backing storage for the framebuffer may be safely read from, such as for display or for media encoding. This would be referred to as a "presentation fence."

Similarly when using an [android.media.ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#) it is possible that an [android.media.Image](https://developer.android.com/reference/kotlin/android/media/Image.html#) returned by [ImageWriter.dequeueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#dequeueInputImage())may already have a [fence](https://developer.android.com/reference/kotlin/android/media/Image.html#getFence())set on it. This would be what is referred to as either a "release fence" or an "acqurie fence" and indicates the fence that the writer must wait on before writing to the underlying buffer. In the case of ImageWriter this is done automatically when eg [Image.getPlanes()](https://developer.android.com/reference/kotlin/android/media/Image.html#getPlanes())is called, however when using [Image.getHardwareBuffer()](https://developer.android.com/reference/kotlin/android/media/Image.html#getHardwareBuffer())it is the caller's responsibility to ensure the release fence has signaled before writing to the buffer.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [SIGNAL_TIME_INVALID](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#SIGNAL_TIME_INVALID:kotlin.Long) An invalid signal time. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [SIGNAL_TIME_PENDING](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#SIGNAL_TIME_PENDING:kotlin.Long) A pending signal time. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#SyncFence(android.hardware.SyncFence))`(`other:` ` [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#)`)` Creates a copy of the SyncFence from an existing one. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [await](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#await(java.time.Duration))`(`timeout:` ` [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)`)` Waits for a SyncFence to signal for up to the timeout duration. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitForever](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#awaitForever())`()` Waits forever for a SyncFence to signal. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#close())`()` Close the SyncFence. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#describeContents())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSignalTime](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#getSignalTime())`()` Returns the time in nanoseconds that the fence signaled in the CLOCK_MONOTONIC time domain. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#isValid())`()` Checks if the SyncFile object is valid. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object into a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### SIGNAL_TIME_INVALID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_TIME_INVALID: Long
```

An invalid signal time. Represents either the signal time for a SyncFence that isn't valid (that is, [isValid()](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#isValid())is false), or if an error occurred while attempting to retrieve the signal time. 

 Value: -1L

### SIGNAL_TIME_PENDING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_TIME_PENDING: Long
```

A pending signal time. This is equivalent to the max value of a long, representing an infinitely far point in the future. 

 Value: 9223372036854775807L

## Public constructors

### SyncFence

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SyncFence(other: SyncFence)
```

Creates a copy of the SyncFence from an existing one. Both fences must be closed() independently.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `other` | [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#):This value cannot be`null`. |

## Public methods

### await

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun await(timeout: Duration): Boolean
```

Waits for a SyncFence to signal for up to the timeout duration. An invalid SyncFence, that is if [isValid()](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#isValid())is false, is treated equivalently to a SyncFence that has already signaled. That is, wait() will immediately return true.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#):The timeout duration. If the duration is negative, then this waits forever. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the fence signaled or isn't valid, false otherwise. |

### awaitForever

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun awaitForever(): Boolean
```

Waits forever for a SyncFence to signal. An invalid SyncFence, that is if [isValid()](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#isValid())is false, is treated equivalently to a SyncFence that has already signaled. That is, wait() will immediately return true.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the fence signaled or isn't valid, false otherwise. |

### close

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Close the SyncFence. This implementation closes the underlying OS resources allocated this stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getSignalTime

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignalTime(): Long
```

Returns the time in nanoseconds that the fence signaled in the CLOCK_MONOTONIC time domain. This corresponds to [System.nanoTime()](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime())but may also be compared to [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())after adjusting for milliseconds vs. nanoseconds. If the fence isn't valid, that is if [isValid()](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#isValid())is false, then this returns [SIGNAL_TIME_INVALID](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#SIGNAL_TIME_INVALID:kotlin.Long). Similarly, if an error occurs while trying to access the signal time, then [SIGNAL_TIME_INVALID](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#SIGNAL_TIME_INVALID:kotlin.Long) is also returned. If the fence hasn't yet signaled, then [SIGNAL_TIME_PENDING](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#SIGNAL_TIME_PENDING:kotlin.Long) is returned.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The time the fence signaled, [SIGNAL_TIME_INVALID](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#SIGNAL_TIME_INVALID:kotlin.Long) if there's an error, or [SIGNAL_TIME_PENDING](https://developer.android.com/reference/kotlin/android/hardware/SyncFence#SIGNAL_TIME_PENDING:kotlin.Long) if the fence hasn't signaled yet. |

### isValid

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isValid(): Boolean
```

Checks if the SyncFile object is valid.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file descriptor represents a valid, open file;`false`otherwise. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object into a Parcel.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be`0`or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SyncFence!>
```
