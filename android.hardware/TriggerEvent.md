# TriggerEvent

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TriggerEvent

Kotlin| [Java](TriggerEvent.md) 
| --- | --- |

```
class TriggerEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.TriggerEvent](TriggerEvent.md) |

This class represents a Trigger Event - the event associated with a Trigger Sensor. When the sensor detects a trigger event condition, such as significant motion in the case of the [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md), the [TriggerEventListener](TriggerEventListener.md) is called with the TriggerEvent. The sensor is automatically canceled after the trigger.

This class holds information such as the value of the sensor when the trigger happened, the timestamp along with detailed information regarding the Sensor itself.

## Summary

| Properties ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sensor](Sensor.md)! | [sensor](TriggerEvent.md) The sensor that generated this event. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [timestamp](TriggerEvent.md) The time in nanosecond at which the event happened |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [values](TriggerEvent.md) The length and contents of the [values](TriggerEvent.md) array depends on which [sensor](Sensor.md) type is being monitored (see also [SensorEvent](SensorEvent.md) for a definition of the coordinate system used). |
| --- | --- |

## Properties

### sensor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var sensor: Sensor!
```

The sensor that generated this event. See [SensorManager](SensorManager.md) for details. 

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

The length and contents of the [values](TriggerEvent.md) array depends on which [sensor](Sensor.md) type is being monitored (see also [SensorEvent](SensorEvent.md) for a definition of the coordinate system used).

#### [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md)

The value field is of length 1. value\[0\] = 1.0 when the sensor triggers. 1.0 is the only allowed value.
