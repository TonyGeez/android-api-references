# DeviceStateSensorOrientationMap

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceStateSensorOrientationMap

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/params/DeviceStateSensorOrientationMap "View this page in Java") 

```
class DeviceStateSensorOrientationMap
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.params.DeviceStateSensorOrientationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap#) |

Immutable class that maps the device fold state to sensor orientation.

Some [logical](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int) cameras on foldables can include physical sensors with different sensor orientation values. As a result, the values of the logical camera device can potentially change depending on the device fold state.

The device fold state to sensor orientation map will contain information about the respective logical camera sensor orientation given a device state. Clients can query the mapping for all possible supported folded states.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap.Builder) Builds a DeviceStateSensorOrientationMap object. |

| Constants ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [FOLDED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap#FOLDED:kotlin.Long) The device is folded. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [NORMAL](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap#NORMAL:kotlin.Long) The device is in its normal physical configuration. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this DeviceStateSensorOrientationMap is equal to another DeviceStateSensorOrientationMap. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSensorOrientation](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap#getSensorOrientation(kotlin.Long))`(`deviceState:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Return the logical camera sensor orientation given a specific device fold state. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap#hashCode())`()` Returns a hash code value for the object. |

## Constants

### FOLDED

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOLDED: Long
```

The device is folded. If not set, the device is unfolded or does not support folding. The exact point when this status change happens during the folding operation is device-specific. 

 Value: 4L

### NORMAL

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NORMAL: Long
```

The device is in its normal physical configuration. This is the default if the device does not support multiple different states. 

 Value: 0L

## Public methods

### equals

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this DeviceStateSensorOrientationMap is equal to another DeviceStateSensorOrientationMap.

Two device state orientation maps are equal if and only if all of their elements are [equal](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)).

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getSensorOrientation

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSensorOrientation(deviceState: Long): Int
```

Return the logical camera sensor orientation given a specific device fold state.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceState` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Device fold state Value is [android.hardware.camera2.params.DeviceStateSensorOrientationMap#NORMAL](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap#NORMAL:kotlin.Long), or [android.hardware.camera2.params.DeviceStateSensorOrientationMap#FOLDED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap#FOLDED:kotlin.Long) |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Valid [android.hardware.camera2.CameraCharacteristics#SENSOR_ORIENTATION](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key) for any supported device fold state |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if the given device state is invalid |

### hashCode

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
