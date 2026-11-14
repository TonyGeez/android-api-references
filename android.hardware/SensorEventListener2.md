# SensorEventListener2

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorEventListener2

Kotlin| [Java](https://developer.android.com/reference/android/hardware/SensorEventListener2 "View this page in Java") 

```
interface SensorEventListener2 : SensorEventListener
```

| [android.hardware.SensorEventListener2](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener2#) |

| Known Direct Subclasses [SensorEventCallback](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [SensorEventCallback](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback) | Used for receiving sensor additional information frames. | |

Used for receiving a notification when a flush() has been successfully completed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFlushCompleted](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener2#onFlushCompleted(android.hardware.Sensor))`(`sensor:` ` [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)!`)` Called after flush() is completed. |

| Inherited functions ||
|---|---|
| From class [SensorEventListener](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener#onAccuracyChanged(android.hardware.Sensor,%20kotlin.Int))`(`sensor:` ` [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)!`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the accuracy of the registered sensor has changed. Unlike onSensorChanged(), this is only called when this accuracy value changes. See the SENSOR_STATUS_\* constants in [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) for details. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener#onSensorChanged(android.hardware.SensorEvent))`(`event:` ` [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent)!`)` <br /> Called when there is a new sensor event. Note that "on changed" is somewhat of a misnomer, as this will also be called if we have a new reading from a sensor with the exact same sensor values (but a newer timestamp). See [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) for details on possible sensor types. See also [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent). **NOTE:** The application doesn't own the [event](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent) object passed as a parameter and therefore cannot hold on to it. The object may be part of an internal pool and may be reused by the framework. <br /> | ||

## Public methods

### onFlushCompleted

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFlushCompleted(sensor: Sensor!): Unit
```

Called after flush() is completed. All the events in the batch at the point when the flush was called have been delivered to the applications registered for those sensor events. In [android.os.Build.VERSION_CODES#KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int), applications may receive flush complete events even if some other application has called flush() on the same sensor. Starting with [android.os.Build.VERSION_CODES#LOLLIPOP](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int), flush Complete events are sent ONLY to the application that has explicitly called flush(). If the hardware FIFO is flushed due to some other application calling flush(), flush complete event is not delivered to this application.

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)!:The [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor) on which flush was called. |

**See Also**

- [android.hardware.SensorManager#flush(SensorEventListener)](https://developer.android.com/reference/kotlin/android/hardware/SensorManager#flush(android.hardware.SensorEventListener))
