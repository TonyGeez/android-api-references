# SensorEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorEventListener

Kotlin| [Java](SensorEventListener.md) 
| --- | --- |

```
interface SensorEventListener
```

| [android.hardware.SensorEventListener](SensorEventListener.md) |

| Known Direct Subclasses [SensorEventListener2](SensorEventListener2.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [SensorEventListener2](SensorEventListener2.md) | Used for receiving a notification when a flush() has been successfully completed. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SensorEventCallback](SensorEventCallback.md) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [SensorEventCallback](SensorEventCallback.md) | Used for receiving sensor additional information frames. | |
| --- | --- | --- | --- | --- | --- | --- |

Used for receiving notifications from the SensorManager when there is new sensor data.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](SensorEventListener.md))`(`sensor:` ` [Sensor](Sensor.md)!`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the accuracy of the registered sensor has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](SensorEventListener.md))`(`event:` ` [SensorEvent](SensorEvent.md)!`)` Called when there is a new sensor event. |

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

See the SENSOR_STATUS_\* constants in [SensorManager](SensorManager.md) for details.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new accuracy of this sensor, one of`SensorManager.SENSOR_STATUS_*` |

### onSensorChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSensorChanged(event: SensorEvent!): Unit
```

Called when there is a new sensor event. Note that "on changed" is somewhat of a misnomer, as this will also be called if we have a new reading from a sensor with the exact same sensor values (but a newer timestamp).

See [SensorManager](SensorManager.md) for details on possible sensor types.

See also [SensorEvent](SensorEvent.md).

**NOTE:** The application doesn't own the [event](SensorEvent.md) object passed as a parameter and therefore cannot hold on to it. The object may be part of an internal pool and may be reused by the framework.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SensorEvent](SensorEvent.md)!:the [SensorEvent](SensorEvent.md). |
