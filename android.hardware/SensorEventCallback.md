# SensorEventCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorEventCallback

Kotlin| [Java](https://developer.android.com/reference/android/hardware/SensorEventCallback "View this page in Java") 
| --- | --- |

```
abstract class SensorEventCallback : SensorEventListener2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.SensorEventCallback](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback#) |

Used for receiving sensor additional information frames.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SensorEventCallback](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback#SensorEventCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback#onAccuracyChanged(android.hardware.Sensor,%20kotlin.Int))`(`sensor:` ` [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)!`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the accuracy of the registered sensor has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFlushCompleted](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback#onFlushCompleted(android.hardware.Sensor))`(`sensor:` ` [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)!`)` Called after flush() is completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorAdditionalInfo](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback#onSensorAdditionalInfo(android.hardware.SensorAdditionalInfo))`(`info:` ` [SensorAdditionalInfo](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo)!`)` Called when a sensor additional information frame is available. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback#onSensorChanged(android.hardware.SensorEvent))`(`event:` ` [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent)!`)` Called when sensor values have changed. |

## Public constructors

### SensorEventCallback

```
SensorEventCallback()
```

## Public methods

### onAccuracyChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAccuracyChanged(
    sensor: Sensor!, 
    accuracy: Int
): Unit
```

Called when the accuracy of the registered sensor has changed.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new accuracy of this sensor, one of`SensorManager.SENSOR_STATUS_*` |

**See Also**

- [android.hardware.SensorEventListener#onAccuracyChanged(Sensor, int)](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener#onAccuracyChanged(android.hardware.Sensor,%20kotlin.Int)) 

### onFlushCompleted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFlushCompleted(sensor: Sensor!): Unit
```

Called after flush() is completed.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)!:The [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor) on which flush was called. |

**See Also**

- [android.hardware.SensorEventListener2#onFlushCompleted(Sensor)](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener2#onFlushCompleted(android.hardware.Sensor)) 

### onSensorAdditionalInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSensorAdditionalInfo(info: SensorAdditionalInfo!): Unit
```

Called when a sensor additional information frame is available.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [SensorAdditionalInfo](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo)!:A [SensorAdditionalInfo](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo) frame reported from sensor hardware. |

### onSensorChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSensorChanged(event: SensorEvent!): Unit
```

Called when sensor values have changed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent)!:the [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent). |

**See Also**

- [android.hardware.SensorEventListener#onSensorChanged(SensorEvent)](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener#onSensorChanged(android.hardware.SensorEvent))
