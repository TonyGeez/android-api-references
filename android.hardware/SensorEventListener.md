# SensorEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorEventListener

Kotlin| [Java](https://developer.android.com/reference/android/hardware/SensorEventListener "View this page in Java") 
| --- | --- |

```
interface SensorEventListener
```

| [android.hardware.SensorEventListener](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener#) |

| Known Direct Subclasses [SensorEventListener2](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener2) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [SensorEventListener2](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener2) | Used for receiving a notification when a flush() has been successfully completed. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SensorEventCallback](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [SensorEventCallback](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback) | Used for receiving sensor additional information frames. | |
| --- | --- | --- | --- | --- | --- | --- |

Used for receiving notifications from the SensorManager when there is new sensor data.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener#onAccuracyChanged(android.hardware.Sensor,%20kotlin.Int))`(`sensor:` ` [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)!`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the accuracy of the registered sensor has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener#onSensorChanged(android.hardware.SensorEvent))`(`event:` ` [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent)!`)` Called when there is a new sensor event. |

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

See the SENSOR_STATUS_\* constants in [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) for details.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new accuracy of this sensor, one of`SensorManager.SENSOR_STATUS_*` |

### onSensorChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSensorChanged(event: SensorEvent!): Unit
```

Called when there is a new sensor event. Note that "on changed" is somewhat of a misnomer, as this will also be called if we have a new reading from a sensor with the exact same sensor values (but a newer timestamp).

See [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) for details on possible sensor types.

See also [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent).

**NOTE:** The application doesn't own the [event](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent) object passed as a parameter and therefore cannot hold on to it. The object may be part of an internal pool and may be reused by the framework.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent)!:the [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent). |
