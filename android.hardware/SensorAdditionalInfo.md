# SensorAdditionalInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorAdditionalInfo

Kotlin | [Java](https://developer.android.com/reference/android/hardware/SensorAdditionalInfo "View this page in Java") 

```
open class SensorAdditionalInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.SensorAdditionalInfo](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#) |

This class represents a [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor) additional information frame, which is reported through listener callback [onSensorAdditionalInfo](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback#onSensorAdditionalInfo(android.hardware.SensorAdditionalInfo)).

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FRAME_BEGIN](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#TYPE_FRAME_BEGIN:kotlin.Int) Mark the beginning of a set of additional info frames. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FRAME_END](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#TYPE_FRAME_END:kotlin.Int) Mark the end of a set of additional info frames. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INTERNAL_TEMPERATURE](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#TYPE_INTERNAL_TEMPERATURE:kotlin.Int) Internal temperature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SAMPLING](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#TYPE_SAMPLING:kotlin.Int) Sampling parameter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SENSOR_PLACEMENT](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#TYPE_SENSOR_PLACEMENT:kotlin.Int) Sensor placement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNTRACKED_DELAY](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#TYPE_UNTRACKED_DELAY:kotlin.Int) Untracked delay. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VEC3_CALIBRATION](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#TYPE_VEC3_CALIBRATION:kotlin.Int) Vector calibration parameter. |

| Properties ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [floatValues](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#floatValues:kotlin.FloatArray) Additional info payload data represented in float values. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [intValues](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#intValues:kotlin.IntArray) Additional info payload data represented in int values. |
| [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor)! | [sensor](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#sensor:android.hardware.Sensor) The sensor that generated this event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [serial](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#serial:kotlin.Int) Sequence number of frame for a certain type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [type](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo#type:kotlin.Int) Type of this additional info frame. |

## Constants

### TYPE_FRAME_BEGIN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FRAME_BEGIN: Int
```

Mark the beginning of a set of additional info frames. 

 Value: 0

### TYPE_FRAME_END

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FRAME_END: Int
```

Mark the end of a set of additional info frames. 

 Value: 1

### TYPE_INTERNAL_TEMPERATURE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INTERNAL_TEMPERATURE: Int
```

Internal temperature. Sensor hardware device internal temperature. Payload: floatValues\[0\]: internal temperature in Celsius. 

 Value: 65537

### TYPE_SAMPLING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SAMPLING: Int
```

Sampling parameter. Describes the raw sample period and estimated jitter of sample time in terms of standard deviation. Payload: floatValues\[0\]: raw sample period in seconds. floatValues\[1\]: standard deviation of sampling period. 

 Value: 65540

### TYPE_SENSOR_PLACEMENT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SENSOR_PLACEMENT: Int
```

Sensor placement. Provides the orientation and location of the sensor element in terms of the Android coordinate system. This data is given as a 3x4 matrix consisting of a 3x3 rotation matrix (R) concatenated with a 3x1 location vector (t). The rotation matrix provides the orientation of the Android device coordinate frame relative to the local coordinate frame of the sensor. Note that assuming the axes conventions of the sensor are the same as Android, this is the inverse of the matrix applied to raw samples read from the sensor to convert them into the Android representation. The location vector represents the translation from the origin of the Android sensor coordinate system to the geometric center of the sensor, specified in millimeters (mm).

**Payload** : `floatValues[0..11]`: 3x4 matrix in row major order \[R; t\]

**Example** : This raw buffer: `{0, 1, 0, 0, -1, 0, 0, 10, 0, 0, 1, -2.5}` 
Corresponds to this 3x4 matrix:

| Orientation ||| Location |
| 0 | 1 | 0 | 0 |
| -1 | 0 | 0 | 10 |
| 0 | 0 | 1 | -2.5 |

The sensor is oriented such that:

- The device X axis corresponds to the sensor's local -Y axis
- The device Y axis corresponds to the sensor's local X axis
- The device Z axis and sensor's local Z axis are equivalent

In other words, if viewing the origin of the Android coordinate system from the positive Z direction, the device coordinate frame is to be rotated 90° counter-clockwise about the Z axis to align with the sensor's local coordinate frame. Equivalently, a vector in the Android coordinate frame may be multiplied with R to rotate it 90° clockwise (270° counter-clockwise), yielding its representation in the sensor's coordinate frame. Relative to the origin of the Android coordinate system, the physical center of the sensor is located 10mm in the positive Y direction, and 2.5mm in the negative Z direction.

<br />

 Value: 65539

### TYPE_UNTRACKED_DELAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNTRACKED_DELAY: Int
```

Untracked delay. Delays that are introduced by data processing, such as filtering, which is not taken into account by sensor timestamps. Payload: floatValues\[0\]: delay estimation in seconds floatValues\[1\]: delay estimation standard deviation 

 Value: 65536

### TYPE_VEC3_CALIBRATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VEC3_CALIBRATION: Int
```

Vector calibration parameter. Calibration applied to a sensor with 3 elements vector output, such as accelerometer, gyro, etc. Payload: floatValues\[0..11\]: First 3 rows of a homogeneous matrix in row major order that captures any linear transformation, including rotation, scaling, shear, shift. 

 Value: 65538

## Properties

### floatValues

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val floatValues: FloatArray!
```

Additional info payload data represented in float values. Depending on the type of information, this may be null. 

### intValues

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val intValues: IntArray!
```

Additional info payload data represented in int values. Depending on the type of information, this may be null. 

### sensor

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val sensor: Sensor!
```

The sensor that generated this event. See [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) for details. 

### serial

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val serial: Int
```

Sequence number of frame for a certain type. 

### type

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val type: Int
```

Type of this additional info frame.
