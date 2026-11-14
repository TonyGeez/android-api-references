# SensorListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorListener

Kotlin| [Java](../android/hardware/SensorListener.md) 
| --- | --- |

```
interface SensorListener
```

| [android.hardware.SensorListener](../android/hardware/SensorListener.md) |

| Known Direct Subclasses [OrientationListener](../android/view/OrientationListener.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [OrientationListener](../android/view/OrientationListener.md) | Helper class for receiving notifications from the SensorManager when the orientation of the device has changed. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 3.**
|
| Use [SensorEventListener](../android/hardware/SensorEventListener.md) instead.

Used for receiving notifications from the SensorManager when sensor values have changed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](../android/hardware/SensorListener.md))`(`sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the accuracy of a sensor has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](../android/hardware/SensorListener.md))`(`sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Called when sensor values have changed. |

## Public methods

### onAccuracyChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccuracyChanged(
    sensor: Int, 
    accuracy: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the accuracy of a sensor has changed. See [SensorManager](../android/hardware/SensorManager.md) for details.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `sensor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the sensor being monitored |
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new accuracy of this sensor. |

### onSensorChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSensorChanged(
    sensor: Int, 
    values: FloatArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when sensor values have changed. The length and contents of the values array vary depending on which sensor is being monitored. See [SensorManager](../android/hardware/SensorManager.md) for details on possible sensor types.

Definition of the coordinate system used below.

<br />

The X axis refers to the screen's horizontal axis (the small edge in portrait mode, the long edge in landscape mode) and points to the right.

The Y axis refers to the screen's vertical axis and points towards the top of the screen (the origin is in the lower-left corner).

The Z axis points toward the sky when the device is lying on its back on a table.

**IMPORTANT NOTE:** The axis**are swapped**when the device's screen orientation changes. To access the unswapped values, use indices 3, 4 and 5 in values\[\].

[SENSOR_ORIENTATION](../android/hardware/SensorManager.md), [SENSOR_ORIENTATION_RAW](../android/hardware/SensorManager.md):

All values are angles in degrees.

values\[0\]: Azimuth, rotation around the Z axis (0\<=azimuth\<360). 0 = North, 90 = East, 180 = South, 270 = West

values\[1\]: Pitch, rotation around X axis (-180\<=pitch\<=180), with positive values when the z-axis moves toward the y-axis.

values\[2\]: Roll, rotation around Y axis (-90\<=roll\<=90), with positive values when the z-axis moves toward the x-axis.

Note that this definition of yaw, pitch and roll is different from the traditional definition used in aviation where the X axis is along the long side of the plane (tail to nose).

[SENSOR_ACCELEROMETER](../android/hardware/SensorManager.md):

All values are in SI units (m/s\^2) and measure contact forces.

values\[0\]: force applied by the device on the x-axis

values\[1\]: force applied by the device on the y-axis

values\[2\]: force applied by the device on the z-axis

Examples:
- When the device is pushed on its left side toward the right, the x acceleration value is negative (the device applies a reaction force to the push toward the left)
- When the device lies flat on a table, the acceleration value is [-STANDARD_GRAVITY](../android/hardware/SensorManager.md), which correspond to the force the device applies on the table in reaction to gravity.
- [SENSOR_MAGNETIC_FIELD](../android/hardware/SensorManager.md):
- All values are in micro-Tesla (uT) and measure the ambient magnetic field in the X, Y and -Z axis.
- **Note:**the magnetic field's Z axis is inverted.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the sensor being monitored |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The new values for the sensor. |
