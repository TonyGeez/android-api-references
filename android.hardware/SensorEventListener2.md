# SensorEventListener2

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorEventListener2

Kotlin| [Java](SensorEventListener2.md) 
| --- | --- |

```
interface SensorEventListener2 : SensorEventListener
```

| [android.hardware.SensorEventListener2](SensorEventListener2.md) |

| Known Direct Subclasses [SensorEventCallback](SensorEventCallback.md) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [SensorEventCallback](SensorEventCallback.md) | Used for receiving sensor additional information frames. | |
| --- | --- | --- | --- | --- | --- | --- |

Used for receiving a notification when a flush() has been successfully completed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFlushCompleted](SensorEventListener2.md))`(`sensor:` ` [Sensor](Sensor.md)!`)` Called after flush() is completed. |

| Inherited functions ||
|---|---|
| From class [SensorEventListener](SensorEventListener.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](SensorEventListener.md))`(`sensor:` ` [Sensor](Sensor.md)!`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when the accuracy of the registered sensor has changed. Unlike onSensorChanged(), this is only called when this accuracy value changes. See the SENSOR_STATUS_\* constants in [SensorManager](SensorManager.md) for details. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](SensorEventListener.md))`(`event:` ` [SensorEvent](SensorEvent.md)!`)` <br /> Called when there is a new sensor event. Note that "on changed" is somewhat of a misnomer, as this will also be called if we have a new reading from a sensor with the exact same sensor values (but a newer timestamp). See [SensorManager](SensorManager.md) for details on possible sensor types. See also [SensorEvent](SensorEvent.md). **NOTE:** The application doesn't own the [event](SensorEvent.md) object passed as a parameter and therefore cannot hold on to it. The object may be part of an internal pool and may be reused by the framework. <br /> | ||

## Public methods

### onFlushCompleted

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFlushCompleted(sensor: Sensor!): Unit
```

Called after flush() is completed. All the events in the batch at the point when the flush was called have been delivered to the applications registered for those sensor events. In [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md), applications may receive flush complete events even if some other application has called flush() on the same sensor. Starting with [android.os.Build.VERSION_CODES#LOLLIPOP](../android/os/Build.VERSION_CODES.md), flush Complete events are sent ONLY to the application that has explicitly called flush(). If the hardware FIFO is flushed due to some other application calling flush(), flush complete event is not delivered to this application.

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Sensor](Sensor.md)!:The [Sensor](Sensor.md) on which flush was called. |

**See Also**

- [android.hardware.SensorManager#flush(SensorEventListener)](SensorManager.md))
