# LensIntrinsicsSample

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LensIntrinsicsSample

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/params/LensIntrinsicsSample "View this page in Java") 
| --- | --- |

```
class LensIntrinsicsSample
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#) |

Immutable class to store an [lens intrinsics intra-frame sample](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#STATISTICS_LENS_INTRINSICS_SAMPLES:android.hardware.camera2.CaptureResult.Key).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#LensIntrinsicsSample(kotlin.Long,%20kotlin.FloatArray))`(`timestampNs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `lensIntrinsics:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`)` Create a new [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#). |

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#) is equal to another [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#). |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getLensIntrinsics](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#getLensIntrinsics())`()` Get the lens [intrinsics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CaptureResult.Key) calibration |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampNanos](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#getTimestampNanos())`()` Get the timestamp in nanoseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#hashCode())`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#toString())`()` Return the LensIntrinsicsSample as a string representation. |

## Public constructors

### LensIntrinsicsSample

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LensIntrinsicsSample(
    timestampNs: Long, 
    lensIntrinsics: FloatArray)
```

Create a new [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#).

[LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#) contains the timestamp and the [CaptureResult.LENS_INTRINSIC_CALIBRATION](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CaptureResult.Key) sample.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timestampNs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):timestamp in nanoseconds of the lens intrinsics sample. This uses the same time basis as [CaptureResult.SENSOR_TIMESTAMP](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key). |
| `lensIntrinsics` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):the lens [intrinsic](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CaptureResult.Key) calibration for the sample. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | if lensIntrinsics length is different from 5 |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#) is equal to another [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#).

Two samples are only equal if and only if each of the lens intrinsics are equal.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getLensIntrinsics

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLensIntrinsics(): FloatArray
```

Get the lens [intrinsics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CaptureResult.Key) calibration

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | a floating point value (guaranteed to be finite) This value cannot be`null`. |

**See Also**

- [android.hardware.camera2.CaptureResult#LENS_INTRINSIC_CALIBRATION](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CaptureResult.Key) 

### getTimestampNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestampNanos(): Long
```

Get the timestamp in nanoseconds.

The timestamps are in the same time basis as and comparable to [android.sensor.timestamp](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key).

| Return ||
|------------------------------------------------------------------------------|----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a long value (guaranteed to be finite) |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return the LensIntrinsicsSample as a string representation.

`"LensIntrinsicsSample{timestamp:%l, sample:%s}"`represents the LensIntrinsics sample's timestamp, and calibration data.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample#) |
