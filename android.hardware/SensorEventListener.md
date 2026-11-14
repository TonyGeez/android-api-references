# SensorEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorEventListener

Kotlin| [Java](../android/hardware/SensorEventListener.md) 
| --- | --- |

```
interface SensorEventListener
```

| [android.hardware.SensorEventListener](../android/hardware/SensorEventListener.md) |

| Known Direct Subclasses [SensorEventListener2](../android/hardware/SensorEventListener2.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [SensorEventListener2](../android/hardware/SensorEventListener2.md) | Used for receiving a notification when a flush() has been successfully completed. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SensorEventCallback](../android/hardware/SensorEventCallback.md) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [SensorEventCallback](../android/hardware/SensorEventCallback.md) | Used for receiving sensor additional information frames. | |
| --- | --- | --- | --- | --- | --- | --- |

Used for receiving notifications from the SensorManager when there is new sensor data.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](../android/hardware/SensorEventListener.md))`(`sensor:` ` [Sensor](../android/hardware/Sensor.md)!`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the accuracy of the registered sensor has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](../android/hardware/SensorEventListener.md))`(`event:` ` [SensorEvent](../android/hardware/SensorEvent.md)!`)` Called when there is a new sensor event. |

## Public methods

### onAccuracyChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccuracyChanged(
    sensor: Sensor!, 
    accuracy: Int
): Unit
```

Called when the accuracy of the registered sensor has changed. Unlike onSensorChanged(), this is only called when this accuracy value changes.

See the SENSOR_STATUS_\* constants in [SensorManager](../android/hardware/SensorManager.md) for details.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new accuracy of this sensor, one of`SensorManager.SENSOR_STATUS_*` |

### onSensorChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSensorChanged(event: SensorEvent!): Unit
```

Called when there is a new sensor event. Note that "on changed" is somewhat of a misnomer, as this will also be called if we have a new reading from a sensor with the exact same sensor values (but a newer timestamp).

See [SensorManager](../android/hardware/SensorManager.md) for details on possible sensor types.

See also [SensorEvent](../android/hardware/SensorEvent.md).

**NOTE:** The application doesn't own the [event](../android/hardware/SensorEvent.md) object passed as a parameter and therefore cannot hold on to it. The object may be part of an internal pool and may be reused by the framework.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SensorEvent](../android/hardware/SensorEvent.md)!:the [SensorEvent](../android/hardware/SensorEvent.md). |
