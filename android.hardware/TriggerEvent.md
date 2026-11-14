# TriggerEvent

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TriggerEvent

Kotlin| [Java](https://developer.android.com/reference/android/hardware/TriggerEvent "View this page in Java") 
| --- | --- |

```
class TriggerEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.TriggerEvent](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent#) |

This class represents a Trigger Event - the event associated with a Trigger Sensor. When the sensor detects a trigger event condition, such as significant motion in the case of the [Sensor.TYPE_SIGNIFICANT_MOTION](https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_SIGNIFICANT_MOTION:kotlin.Int), the [TriggerEventListener](https://developer.android.com/reference/kotlin/android/hardware/TriggerEventListener) is called with the TriggerEvent. The sensor is automatically canceled after the trigger.

This class holds information such as the value of the sensor when the trigger happened, the timestamp along with detailed information regarding the Sensor itself.

## Summary

| Properties ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)! | [sensor](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent#sensor:android.hardware.Sensor) The sensor that generated this event. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [timestamp](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent#timestamp:kotlin.Long) The time in nanosecond at which the event happened |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [values](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent#values:kotlin.FloatArray) The length and contents of the [values](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent#values:kotlin.FloatArray) array depends on which [sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor) type is being monitored (see also [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent) for a definition of the coordinate system used). |
| --- | --- |

## Properties

### sensor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var sensor: Sensor!
```

The sensor that generated this event. See [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) for details. 

### timestamp

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var timestamp: Long
```

The time in nanosecond at which the event happened 

### values

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val values: FloatArray!
```

The length and contents of the [values](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent#values:kotlin.FloatArray) array depends on which [sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor) type is being monitored (see also [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent) for a definition of the coordinate system used).

#### [Sensor.TYPE_SIGNIFICANT_MOTION](https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_SIGNIFICANT_MOTION:kotlin.Int)

The value field is of length 1. value\[0\] = 1.0 when the sensor triggers. 1.0 is the only allowed value.
