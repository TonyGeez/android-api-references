# SensorEventCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorEventCallback

Kotlin| [Java](../android/hardware/SensorEventCallback.md) 
| --- | --- |

```
abstract class SensorEventCallback : SensorEventListener2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.SensorEventCallback](../android/hardware/SensorEventCallback.md) |

Used for receiving sensor additional information frames.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SensorEventCallback](../android/hardware/SensorEventCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](../android/hardware/SensorEventCallback.md))`(`sensor:` ` [Sensor](../android/hardware/Sensor.md)!`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the accuracy of the registered sensor has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFlushCompleted](../android/hardware/SensorEventCallback.md))`(`sensor:` ` [Sensor](../android/hardware/Sensor.md)!`)` Called after flush() is completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorAdditionalInfo](../android/hardware/SensorEventCallback.md))`(`info:` ` [SensorAdditionalInfo](../android/hardware/SensorAdditionalInfo.md)!`)` Called when a sensor additional information frame is available. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](../android/hardware/SensorEventCallback.md))`(`event:` ` [SensorEvent](../android/hardware/SensorEvent.md)!`)` Called when sensor values have changed. |

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

- [android.hardware.SensorEventListener#onAccuracyChanged(Sensor, int)](../android/hardware/SensorEventListener.md)) 

### onFlushCompleted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFlushCompleted(sensor: Sensor!): Unit
```

Called after flush() is completed.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Sensor](../android/hardware/Sensor.md)!:The [Sensor](../android/hardware/Sensor.md) on which flush was called. |

**See Also**

- [android.hardware.SensorEventListener2#onFlushCompleted(Sensor)](../android/hardware/SensorEventListener2.md)) 

### onSensorAdditionalInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSensorAdditionalInfo(info: SensorAdditionalInfo!): Unit
```

Called when a sensor additional information frame is available.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [SensorAdditionalInfo](../android/hardware/SensorAdditionalInfo.md)!:A [SensorAdditionalInfo](../android/hardware/SensorAdditionalInfo.md) frame reported from sensor hardware. |

### onSensorChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSensorChanged(event: SensorEvent!): Unit
```

Called when sensor values have changed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SensorEvent](../android/hardware/SensorEvent.md)!:the [SensorEvent](../android/hardware/SensorEvent.md). |

**See Also**

- [android.hardware.SensorEventListener#onSensorChanged(SensorEvent)](../android/hardware/SensorEventListener.md))
