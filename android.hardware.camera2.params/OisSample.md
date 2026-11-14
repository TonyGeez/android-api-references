# OisSample

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OisSample

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/params/OisSample "View this page in Java") 

```
class OisSample
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.params.OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#) |

Immutable class to store an [optical image stabilization sample](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#STATISTICS_OIS_SAMPLES:android.hardware.camera2.CaptureResult.Key).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#OisSample(kotlin.Long,%20kotlin.Float,%20kotlin.Float))`(`timestamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `xShift:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yShift:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Create a new [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#). |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#) is equal to another [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestamp](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#getTimestamp())`()` Get the timestamp in nanoseconds. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getXshift](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#getXshift())`()` Get the shift in x direction. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getYshift](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#getYshift())`()` Get the shift in y direction. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#hashCode())`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#toString())`()` Return the OisSample as a string representation. |

## Public constructors

### OisSample

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OisSample(
    timestamp: Long, 
    xShift: Float, 
    yShift: Float)
```

Create a new [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#).

[OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#) contains the timestamp and the amount of shifts in x and y direction, in pixels, of the OIS sample.

A positive value for a shift in x direction is a shift from left to right in active array coordinate system. For example, if the optical center is`(1000, 500)`in active array coordinates, a shift of`(3, 0)`puts the new optical center at`(1003, 500)`.

A positive value for a shift in y direction is a shift from top to bottom in active array coordinate system. For example, if the optical center is`(1000, 500)`in active array coordinates, a shift of`(0, 5)`puts the new optical center at`(1000, 505)`.

xShift and yShift must be finite; NaN and infinity is not allowed.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `timestamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):timestamp of the OIS sample. |
| `xShift` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):shift of the OIS sample in x direction. |
| `yShift` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):shift of the OIS sample in y direction. |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if xShift or yShift is not finite |

## Public methods

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#) is equal to another [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#).

Two samples are only equal if and only if each of the OIS information is equal.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getTimestamp

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestamp(): Long
```

Get the timestamp in nanoseconds.

The timestamps are in the same timebase as and comparable to [android.sensor.timestamp](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key).

| Return ||
|------------------------------------------------------------------------------|----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a long value (guaranteed to be finite) |

### getXshift

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getXshift(): Float
```

Get the shift in x direction.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a floating point value (guaranteed to be finite) |

### getYshift

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getYshift(): Float
```

Get the shift in y direction.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a floating point value (guaranteed to be finite) |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return the OisSample as a string representation.

`"OisSample{timestamp:%l, shift_x:%f, shift_y:%f}"`represents the OIS sample's timestamp, shift in x direction, and shift in y direction.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample#) |
