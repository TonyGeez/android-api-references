Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Sensor

```
class Sensor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.Sensor](../android/hardware/Sensor.md) |

Class representing a sensor. Use `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getSensorList(kotlin.Int)` to get the list of available sensors. For more information about Android sensors, read the [Motion Sensors guide](../guide/topics/sensors/sensors_motion.md).

<br />

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_CONTINUOUS:kotlin.Int` Events are reported at a constant rate which is set by the rate parameter of `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#registerListener(android.hardware.SensorEventListener,%20android.hardware.Sensor,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_ONE_SHOT:kotlin.Int` Events are reported in one-shot mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_ON_CHANGE:kotlin.Int` Events are reported only when the value changes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_SPECIAL_TRIGGER:kotlin.Int` Events are reported as described in the description of the sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_ACCELEROMETER:kotlin.String` A constant string describing an accelerometer sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_ACCELEROMETER_LIMITED_AXES:kotlin.String` A constant string describing a limited axes accelerometer sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED:kotlin.String` A constant string describing an uncalibrated limited axes accelerometer sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_ACCELEROMETER_UNCALIBRATED:kotlin.String` A constant string describing an uncalibrated accelerometer sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_AMBIENT_TEMPERATURE:kotlin.String` A constant string describing an ambient temperature sensor type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_GAME_ROTATION_VECTOR:kotlin.String` A constant string describing an uncalibrated rotation vector sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_GEOMAGNETIC_ROTATION_VECTOR:kotlin.String` A constant string describing a geo-magnetic rotation vector. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_GRAVITY:kotlin.String` A constant string describing a gravity sensor type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_GYROSCOPE:kotlin.String` A constant string describing a gyroscope sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_GYROSCOPE_LIMITED_AXES:kotlin.String` A constant string describing a limited axes gyroscope sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_GYROSCOPE_LIMITED_AXES_UNCALIBRATED:kotlin.String` A constant string describing an uncalibrated limited axes gyroscope sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_GYROSCOPE_UNCALIBRATED:kotlin.String` A constant string describing an uncalibrated gyroscope sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_HEADING:kotlin.String` A constant string describing a heading sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_HEAD_TRACKER:kotlin.String` A constant string describing a head tracker sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_HEART_BEAT:kotlin.String` A constant string describing a heart beat sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_HEART_RATE:kotlin.String` A constant string describing a heart rate monitor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_HINGE_ANGLE:kotlin.String` A constant string describing a hinge angle sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_LIGHT:kotlin.String` A constant string describing a light sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_LINEAR_ACCELERATION:kotlin.String` A constant string describing a linear acceleration sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_LOW_LATENCY_OFFBODY_DETECT:kotlin.String` A constant string describing a low-latency offbody detector sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_MAGNETIC_FIELD:kotlin.String` A constant string describing a magnetic field sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_MAGNETIC_FIELD_UNCALIBRATED:kotlin.String` A constant string describing an uncalibrated magnetic field sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_MOTION_DETECT:kotlin.String` A constant string describing a motion detection sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_ORIENTATION:kotlin.String` A constant string describing an orientation sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_POSE_6DOF:kotlin.String` A constant string describing a pose sensor with 6 degrees of freedom. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_PRESSURE:kotlin.String` A constant string describing a pressure sensor type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_PROXIMITY:kotlin.String` A constant string describing a proximity sensor type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_RELATIVE_HUMIDITY:kotlin.String` A constant string describing a relative humidity sensor type |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_ROTATION_VECTOR:kotlin.String` A constant string describing a rotation vector sensor type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_SIGNIFICANT_MOTION:kotlin.String` A constant string describing a significant motion trigger sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_STATIONARY_DETECT:kotlin.String` A constant string describing a stationary detection sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_STEP_COUNTER:kotlin.String` A constant string describing a step counter sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_STEP_DETECTOR:kotlin.String` A constant string describing a step detector sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_TEMPERATURE:kotlin.String` A constant string describing a temperature sensor type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ACCELEROMETER:kotlin.Int` A constant describing an accelerometer sensor type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ACCELEROMETER_LIMITED_AXES:kotlin.Int` A constant describing a limited axes accelerometer sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED:kotlin.Int` A constant describing an uncalibrated limited axes accelerometer sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ACCELEROMETER_UNCALIBRATED:kotlin.Int` A constant describing an uncalibrated accelerometer sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ALL:kotlin.Int` A constant describing all sensor types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_AMBIENT_TEMPERATURE:kotlin.Int` A constant describing an ambient temperature sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_DEVICE_PRIVATE_BASE:kotlin.Int` The lowest sensor type vendor defined sensors can use. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GAME_ROTATION_VECTOR:kotlin.Int` A constant describing an uncalibrated rotation vector sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GEOMAGNETIC_ROTATION_VECTOR:kotlin.Int` A constant describing a geo-magnetic rotation vector. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GRAVITY:kotlin.Int` A constant describing a gravity sensor type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE:kotlin.Int` A constant describing a gyroscope sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE_LIMITED_AXES:kotlin.Int` A constant describing a limited axes gyroscope sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE_LIMITED_AXES_UNCALIBRATED:kotlin.Int` A constant describing an uncalibrated limited axes gyroscope sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE_UNCALIBRATED:kotlin.Int` A constant describing an uncalibrated gyroscope sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HEADING:kotlin.Int` A constant string describing a heading sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HEAD_TRACKER:kotlin.Int` A constant describing a head tracker sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HEART_BEAT:kotlin.Int` A constant describing a heart beat sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HEART_RATE:kotlin.Int` A constant describing a heart rate monitor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HINGE_ANGLE:kotlin.Int` A constant describing a hinge angle sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_LIGHT:kotlin.Int` A constant describing a light sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_LINEAR_ACCELERATION:kotlin.Int` A constant describing a linear acceleration sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_LOW_LATENCY_OFFBODY_DETECT:kotlin.Int` A constant describing a low latency off-body detect sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_MAGNETIC_FIELD:kotlin.Int` A constant describing a magnetic field sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_MAGNETIC_FIELD_UNCALIBRATED:kotlin.Int` A constant describing an uncalibrated magnetic field sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_MOTION_DETECT:kotlin.Int` A constant describing a motion detect sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ORIENTATION:kotlin.Int` A constant describing an orientation sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_POSE_6DOF:kotlin.Int` A constant describing a pose sensor with 6 degrees of freedom. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_PRESSURE:kotlin.Int` A constant describing a pressure sensor type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_PROXIMITY:kotlin.Int` A constant describing a proximity sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_RELATIVE_HUMIDITY:kotlin.Int` A constant describing a relative humidity sensor type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ROTATION_VECTOR:kotlin.Int` A constant describing a rotation vector sensor type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_SIGNIFICANT_MOTION:kotlin.Int` A constant describing a significant motion trigger sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_STATIONARY_DETECT:kotlin.Int` A constant describing a stationary detect sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_STEP_COUNTER:kotlin.Int` A constant describing a step counter sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_STEP_DETECTOR:kotlin.Int` A constant describing a step detector sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_TEMPERATURE:kotlin.Int` A constant describing a temperature sensor type |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getFifoMaxEventCount()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getFifoReservedEventCount()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getHighestDirectReportRateLevel()()` Get the highest supported direct report mode rate level of the sensor. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getId()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getMaxDelay()()` This value is defined only for continuous and on-change sensors. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getMaximumRange()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getMinDelay()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getName()()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getPower()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getReportingMode()()` Each sensor has exactly one reporting mode associated with it. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getResolution()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getStringType()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getType()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getVendor()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#getVersion()()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#isAdditionalInfoSupported()()` Returns true if the sensor supports sensor additional information API |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#isDirectChannelTypeSupported(kotlin.Int)(sharedMemType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Test if a sensor supports a specified direct channel type. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#isDynamicSensor()()` Returns true if the sensor is a dynamic sensor. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#isWakeUpSensor()()` Returns true if the sensor is a wake-up sensor. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/Sensor#toString()()` Returns a string representation of the object. |

## Constants

### REPORTING_MODE_CONTINUOUS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REPORTING_MODE_CONTINUOUS: Int
```

Events are reported at a constant rate which is set by the rate parameter of `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#registerListener(android.hardware.SensorEventListener,%20android.hardware.Sensor,%20kotlin.Int)`. Note: If other applications are requesting a higher rate, the sensor data might be delivered at faster rates than requested.

 Value: 0

### REPORTING_MODE_ONE_SHOT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REPORTING_MODE_ONE_SHOT: Int
```

Events are reported in one-shot mode. Upon detection of an event, the sensor deactivates itself and then sends a single event. Sensors of this reporting mode must be registered to using `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#requestTriggerSensor(android.hardware.TriggerEventListener,%20android.hardware.Sensor)`.

 Value: 2

### REPORTING_MODE_ON_CHANGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REPORTING_MODE_ON_CHANGE: Int
```

Events are reported only when the value changes. Event delivery rate can be limited by setting appropriate value for rate parameter of `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#registerListener(android.hardware.SensorEventListener,%20android.hardware.Sensor,%20kotlin.Int)` Note: If other applications are requesting a higher rate, the sensor data might be delivered at faster rates than requested.

 Value: 1

### REPORTING_MODE_SPECIAL_TRIGGER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REPORTING_MODE_SPECIAL_TRIGGER: Int
```

Events are reported as described in the description of the sensor. The rate passed to registerListener might not have an impact on the rate of event delivery. See the sensor definition for more information on when and how frequently the events are reported. For example, step detectors report events when a step is detected.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#registerListener(android.hardware.SensorEventListener,%20android.hardware.Sensor,%20kotlin.Int,%20kotlin.Int)`

### STRING_TYPE_ACCELEROMETER

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_ACCELEROMETER: String
```

A constant string describing an accelerometer sensor type.

 Value: "android.sensor.accelerometer"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ACCELEROMETER:kotlin.Int`

### STRING_TYPE_ACCELEROMETER_LIMITED_AXES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_ACCELEROMETER_LIMITED_AXES: String
```

A constant string describing a limited axes accelerometer sensor.

 Value: "android.sensor.accelerometer_limited_axes"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ACCELEROMETER_LIMITED_AXES:kotlin.Int`

### STRING_TYPE_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED: String
```

A constant string describing an uncalibrated limited axes accelerometer sensor.

 Value: "android.sensor.accelerometer_limited_axes_uncalibrated"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED:kotlin.Int`

### STRING_TYPE_ACCELEROMETER_UNCALIBRATED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_ACCELEROMETER_UNCALIBRATED: String
```

A constant string describing an uncalibrated accelerometer sensor.

 Value: "android.sensor.accelerometer_uncalibrated"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ACCELEROMETER_UNCALIBRATED:kotlin.Int`

### STRING_TYPE_AMBIENT_TEMPERATURE

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_AMBIENT_TEMPERATURE: String
```

A constant string describing an ambient temperature sensor type.

 Value: "android.sensor.ambient_temperature"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_AMBIENT_TEMPERATURE:kotlin.Int`

### STRING_TYPE_GAME_ROTATION_VECTOR

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_GAME_ROTATION_VECTOR: String
```

A constant string describing an uncalibrated rotation vector sensor type.

 Value: "android.sensor.game_rotation_vector"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GAME_ROTATION_VECTOR:kotlin.Int`

### STRING_TYPE_GEOMAGNETIC_ROTATION_VECTOR

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_GEOMAGNETIC_ROTATION_VECTOR: String
```

A constant string describing a geo-magnetic rotation vector.

 Value: "android.sensor.geomagnetic_rotation_vector"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GEOMAGNETIC_ROTATION_VECTOR:kotlin.Int`

### STRING_TYPE_GRAVITY

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_GRAVITY: String
```

A constant string describing a gravity sensor type.

 Value: "android.sensor.gravity"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GRAVITY:kotlin.Int`

### STRING_TYPE_GYROSCOPE

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_GYROSCOPE: String
```

A constant string describing a gyroscope sensor type.

 Value: "android.sensor.gyroscope"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE:kotlin.Int`

### STRING_TYPE_GYROSCOPE_LIMITED_AXES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_GYROSCOPE_LIMITED_AXES: String
```

A constant string describing a limited axes gyroscope sensor.

 Value: "android.sensor.gyroscope_limited_axes"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE_LIMITED_AXES:kotlin.Int`

### STRING_TYPE_GYROSCOPE_LIMITED_AXES_UNCALIBRATED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_GYROSCOPE_LIMITED_AXES_UNCALIBRATED: String
```

A constant string describing an uncalibrated limited axes gyroscope sensor.

 Value: "android.sensor.gyroscope_limited_axes_uncalibrated"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE_LIMITED_AXES_UNCALIBRATED:kotlin.Int`

### STRING_TYPE_GYROSCOPE_UNCALIBRATED

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_GYROSCOPE_UNCALIBRATED: String
```

A constant string describing an uncalibrated gyroscope sensor type.

 Value: "android.sensor.gyroscope_uncalibrated"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE_UNCALIBRATED:kotlin.Int`

### STRING_TYPE_HEADING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_HEADING: String
```

A constant string describing a heading sensor.

 Value: "android.sensor.heading"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HEADING:kotlin.Int`

### STRING_TYPE_HEAD_TRACKER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_HEAD_TRACKER: String
```

A constant string describing a head tracker sensor. Note that this sensor type is typically not available for apps to use. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: "android.sensor.head_tracker"

### STRING_TYPE_HEART_BEAT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_HEART_BEAT: String
```

A constant string describing a heart beat sensor.

 Value: "android.sensor.heart_beat"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HEART_BEAT:kotlin.Int`

### STRING_TYPE_HEART_RATE

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_HEART_RATE: String
```

A constant string describing a heart rate monitor.

 Value: "android.sensor.heart_rate"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HEART_RATE:kotlin.Int`

### STRING_TYPE_HINGE_ANGLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_HINGE_ANGLE: String
```

A constant string describing a hinge angle sensor.

 Value: "android.sensor.hinge_angle"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_HINGE_ANGLE:kotlin.Int`

### STRING_TYPE_LIGHT

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_LIGHT: String
```

A constant string describing a light sensor type.

 Value: "android.sensor.light"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_LIGHT:kotlin.Int`

### STRING_TYPE_LINEAR_ACCELERATION

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_LINEAR_ACCELERATION: String
```

A constant string describing a linear acceleration sensor type.

 Value: "android.sensor.linear_acceleration"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_LINEAR_ACCELERATION:kotlin.Int`

### STRING_TYPE_LOW_LATENCY_OFFBODY_DETECT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_LOW_LATENCY_OFFBODY_DETECT: String
```

A constant string describing a low-latency offbody detector sensor.

 Value: "android.sensor.low_latency_offbody_detect"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_LOW_LATENCY_OFFBODY_DETECT:kotlin.Int`

### STRING_TYPE_MAGNETIC_FIELD

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_MAGNETIC_FIELD: String
```

A constant string describing a magnetic field sensor type.

 Value: "android.sensor.magnetic_field"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_MAGNETIC_FIELD:kotlin.Int`

### STRING_TYPE_MAGNETIC_FIELD_UNCALIBRATED

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_MAGNETIC_FIELD_UNCALIBRATED: String
```

A constant string describing an uncalibrated magnetic field sensor type.

 Value: "android.sensor.magnetic_field_uncalibrated"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_MAGNETIC_FIELD_UNCALIBRATED:kotlin.Int`

### STRING_TYPE_MOTION_DETECT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_MOTION_DETECT: String
```

A constant string describing a motion detection sensor.

 Value: "android.sensor.motion_detect"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_MOTION_DETECT:kotlin.Int`

### STRING_TYPE_ORIENTATION

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_ORIENTATION: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getOrientation(kotlin.FloatArray,%20kotlin.FloatArray)` instead.*

A constant string describing an orientation sensor type.

 Value: "android.sensor.orientation"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ORIENTATION:kotlin.Int`

### STRING_TYPE_POSE_6DOF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_POSE_6DOF: String
```

A constant string describing a pose sensor with 6 degrees of freedom.

 Value: "android.sensor.pose_6dof"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_POSE_6DOF:kotlin.Int`

### STRING_TYPE_PRESSURE

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_PRESSURE: String
```

A constant string describing a pressure sensor type.

 Value: "android.sensor.pressure"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_PRESSURE:kotlin.Int`

### STRING_TYPE_PROXIMITY

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_PROXIMITY: String
```

A constant string describing a proximity sensor type.

 Value: "android.sensor.proximity"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_PROXIMITY:kotlin.Int`

### STRING_TYPE_RELATIVE_HUMIDITY

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_RELATIVE_HUMIDITY: String
```

A constant string describing a relative humidity sensor type

 Value: "android.sensor.relative_humidity"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_RELATIVE_HUMIDITY:kotlin.Int`

### STRING_TYPE_ROTATION_VECTOR

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_ROTATION_VECTOR: String
```

A constant string describing a rotation vector sensor type.

 Value: "android.sensor.rotation_vector"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ROTATION_VECTOR:kotlin.Int`

### STRING_TYPE_SIGNIFICANT_MOTION

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_SIGNIFICANT_MOTION: String
```

A constant string describing a significant motion trigger sensor.

 Value: "android.sensor.significant_motion"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_SIGNIFICANT_MOTION:kotlin.Int`

### STRING_TYPE_STATIONARY_DETECT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_STATIONARY_DETECT: String
```

A constant string describing a stationary detection sensor.

 Value: "android.sensor.stationary_detect"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_STATIONARY_DETECT:kotlin.Int`

### STRING_TYPE_STEP_COUNTER

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_STEP_COUNTER: String
```

A constant string describing a step counter sensor.

 Value: "android.sensor.step_counter"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_STEP_COUNTER:kotlin.Int`

### STRING_TYPE_STEP_DETECTOR

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_STEP_DETECTOR: String
```

A constant string describing a step detector sensor.

 Value: "android.sensor.step_detector"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_STEP_DETECTOR:kotlin.Int`

### STRING_TYPE_TEMPERATURE

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRING_TYPE_TEMPERATURE: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/hardware/Sensor#STRING_TYPE_AMBIENT_TEMPERATURE:kotlin.String` instead.*

A constant string describing a temperature sensor type

 Value: "android.sensor.temperature"

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_TEMPERATURE:kotlin.Int`

### TYPE_ACCELEROMETER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ACCELEROMETER: Int
```

A constant describing an accelerometer sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 1

### TYPE_ACCELEROMETER_LIMITED_AXES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ACCELEROMETER_LIMITED_AXES: Int
```

A constant describing a limited axes accelerometer sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 38

### TYPE_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED: Int
```

A constant describing an uncalibrated limited axes accelerometer sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 40

### TYPE_ACCELEROMETER_UNCALIBRATED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ACCELEROMETER_UNCALIBRATED: Int
```

A constant describing an uncalibrated accelerometer sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 35

### TYPE_ALL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ALL: Int
```

A constant describing all sensor types.

 Value: -1

### TYPE_AMBIENT_TEMPERATURE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_AMBIENT_TEMPERATURE: Int
```

A constant describing an ambient temperature sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 13

### TYPE_DEVICE_PRIVATE_BASE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DEVICE_PRIVATE_BASE: Int
```

The lowest sensor type vendor defined sensors can use. All vendor sensor types are greater than or equal to this constant.

 Value: 65536

### TYPE_GAME_ROTATION_VECTOR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_GAME_ROTATION_VECTOR: Int
```

A constant describing an uncalibrated rotation vector sensor type.

Identical to `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ROTATION_VECTOR:kotlin.Int` except that it doesn't use the geomagnetic field. Therefore the Y axis doesn't point north, but instead to some other reference, that reference is allowed to drift by the same order of magnitude as the gyroscope drift around the Z axis.

In the ideal case, a phone rotated and returning to the same real-world orientation should report the same game rotation vector (without using the earth's geomagnetic field). However, the orientation may drift somewhat over time.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 15

### TYPE_GEOMAGNETIC_ROTATION_VECTOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_GEOMAGNETIC_ROTATION_VECTOR: Int
```

A constant describing a geo-magnetic rotation vector.

Similar to `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ROTATION_VECTOR:kotlin.Int`, but using a magnetometer instead of using a gyroscope. This sensor uses lower power than the other rotation vectors, because it doesn't use the gyroscope. However, it is more noisy and will work best outdoors.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 20

### TYPE_GRAVITY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_GRAVITY: Int
```

A constant describing a gravity sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 9

### TYPE_GYROSCOPE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_GYROSCOPE: Int
```

A constant describing a gyroscope sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 4

### TYPE_GYROSCOPE_LIMITED_AXES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_GYROSCOPE_LIMITED_AXES: Int
```

A constant describing a limited axes gyroscope sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 39

### TYPE_GYROSCOPE_LIMITED_AXES_UNCALIBRATED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_GYROSCOPE_LIMITED_AXES_UNCALIBRATED: Int
```

A constant describing an uncalibrated limited axes gyroscope sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 41

### TYPE_GYROSCOPE_UNCALIBRATED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_GYROSCOPE_UNCALIBRATED: Int
```

A constant describing an uncalibrated gyroscope sensor type.

Similar to `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_GYROSCOPE:kotlin.Int` but no gyro-drift compensation has been performed to adjust the given sensor values. However, such gyro-drift bias values are returned to you separately in the result `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` so you may use them for custom calibrations.

Factory calibration and temperature compensation is still applied to the rate of rotation (angular speeds).

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 16

### TYPE_HEADING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HEADING: Int
```

A constant string describing a heading sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 42

### TYPE_HEAD_TRACKER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HEAD_TRACKER: Int
```

A constant describing a head tracker sensor. Note that this sensor type is typically not available for apps to use. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 37

### TYPE_HEART_BEAT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HEART_BEAT: Int
```

A constant describing a heart beat sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 31

### TYPE_HEART_RATE

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HEART_RATE: Int
```

A constant describing a heart rate monitor.

The reported value is the heart rate in beats per minute.

The reported accuracy represents the status of the monitor during the reading. See the `SENSOR_STATUS_*` constants in `https://developer.android.com/reference/kotlin/android/hardware/SensorManager` for more details on accuracy/status values. In particular, when the accuracy is `SENSOR_STATUS_UNRELIABLE` or `SENSOR_STATUS_NO_CONTACT`, the heart rate value should be discarded.

This sensor requires permission `android.permission.BODY_SENSORS` for SDK \< 36 and `android.permission.health.READ_HEART_RATE` for SDK \>= 36. The sensor will be returned by `SensorManager.getSensorList` and `SensorManager.getDefaultSensor`, but the application must hold this permission in order to successfully register a listener and receive data.

 Value: 21

### TYPE_HINGE_ANGLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HINGE_ANGLE: Int
```

A constant describing a hinge angle sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 36

### TYPE_LIGHT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_LIGHT: Int
```

A constant describing a light sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 5

### TYPE_LINEAR_ACCELERATION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_LINEAR_ACCELERATION: Int
```

A constant describing a linear acceleration sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 10

### TYPE_LOW_LATENCY_OFFBODY_DETECT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_LOW_LATENCY_OFFBODY_DETECT: Int
```

A constant describing a low latency off-body detect sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 34

### TYPE_MAGNETIC_FIELD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MAGNETIC_FIELD: Int
```

A constant describing a magnetic field sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 2

### TYPE_MAGNETIC_FIELD_UNCALIBRATED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MAGNETIC_FIELD_UNCALIBRATED: Int
```

A constant describing an uncalibrated magnetic field sensor type.

Similar to `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_MAGNETIC_FIELD:kotlin.Int` but the hard iron calibration (device calibration due to distortions that arise from magnetized iron, steel or permanent magnets on the device) is not considered in the given sensor values. However, such hard iron bias values are returned to you separately in the result `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` so you may use them for custom calibrations.

Also, no periodic calibration is performed (i.e. there are no discontinuities in the data stream while using this sensor) and assumptions that the magnetic field is due to the Earth's poles is avoided, but factory calibration and temperature compensation have been performed.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 14

### TYPE_MOTION_DETECT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MOTION_DETECT: Int
```

A constant describing a motion detect sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 30

### TYPE_ORIENTATION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ORIENTATION: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getOrientation(kotlin.FloatArray,%20kotlin.FloatArray)` instead.*

A constant describing an orientation sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 3

### TYPE_POSE_6DOF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_POSE_6DOF: Int
```

A constant describing a pose sensor with 6 degrees of freedom. Similar to `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_ROTATION_VECTOR:kotlin.Int`, with additional delta translation from an arbitrary reference point. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details. Can use camera, depth sensor etc to compute output value. This is expected to be a high power sensor and expected only to be used when the screen is on. Expected to be more accurate than the rotation vector alone.

 Value: 28

### TYPE_PRESSURE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PRESSURE: Int
```

A constant describing a pressure sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 6

### TYPE_PROXIMITY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PROXIMITY: Int
```

A constant describing a proximity sensor type. This is a wake up sensor.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#isWakeUpSensor()`

### TYPE_RELATIVE_HUMIDITY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_RELATIVE_HUMIDITY: Int
```

A constant describing a relative humidity sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 12

### TYPE_ROTATION_VECTOR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ROTATION_VECTOR: Int
```

A constant describing a rotation vector sensor type.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 11

### TYPE_SIGNIFICANT_MOTION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SIGNIFICANT_MOTION: Int
```

A constant describing a significant motion trigger sensor.

It triggers when an event occurs and then automatically disables itself. The sensor continues to operate while the device is asleep and will automatically wake the device to notify when significant motion is detected. The application does not need to hold any wake locks for this sensor to trigger. This is a wake up sensor.

See `https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent` for more details.

 Value: 17

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#isWakeUpSensor()`

### TYPE_STATIONARY_DETECT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_STATIONARY_DETECT: Int
```

A constant describing a stationary detect sensor. See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 29

### TYPE_STEP_COUNTER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_STEP_COUNTER: Int
```

A constant describing a step counter sensor.

A sensor of this type returns the number of steps taken by the user since the last reboot while activated. The value is returned as a float (with the fractional part set to zero) and is reset to zero only on a system reboot. The timestamp of the event is set to the time when the last step for that event was taken. This sensor is implemented in hardware and is expected to be low power. If you want to continuously track the number of steps over a long period of time, do NOT unregister for this sensor, so that it keeps counting steps in the background even when the AP is in suspend mode and report the aggregate count when the AP is awake. Application needs to stay registered for this sensor because step counter does not count steps if it is not activated. This sensor is ideal for fitness tracking applications. It is defined as an `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_ON_CHANGE:kotlin.Int` sensor.

This sensor requires permission `android.permission.ACTIVITY_RECOGNITION`.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 19

### TYPE_STEP_DETECTOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_STEP_DETECTOR: Int
```

A constant describing a step detector sensor.

A sensor of this type triggers an event each time a step is taken by the user. The only allowed value to return is 1.0 and an event is generated for each step. Like with any other event, the timestamp indicates when the event (here the step) occurred, this corresponds to when the foot hit the ground, generating a high variation in acceleration. This sensor is only for detecting every individual step as soon as it is taken, for example to perform dead reckoning. If you only need aggregate number of steps taken over a period of time, register for `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_STEP_COUNTER:kotlin.Int` instead. It is defined as a `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_SPECIAL_TRIGGER:kotlin.Int` sensor.

This sensor requires permission `android.permission.ACTIVITY_RECOGNITION`.

See `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray` for more details.

 Value: 18

### TYPE_TEMPERATURE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_TEMPERATURE: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_AMBIENT_TEMPERATURE:kotlin.Int` instead.*

A constant describing a temperature sensor type

 Value: 7

## Public methods

### getFifoMaxEventCount

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFifoMaxEventCount(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Maximum number of events of this sensor that could be batched. If this value is zero it indicates that batch mode is not supported for this sensor. If other applications registered to batched sensors, the actual number of events that can be batched might be smaller because the hardware FiFo will be partially used to batch the other sensors. |

### getFifoReservedEventCount

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFifoReservedEventCount(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Number of events reserved for this sensor in the batch mode FIFO. This gives a guarantee on the minimum number of events that can be batched. |

### getHighestDirectReportRateLevel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighestDirectReportRateLevel(): Int
```

Get the highest supported direct report mode rate level of the sensor.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Highest direct report rate level of this sensor. Note that if the app does not have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#HIGH_SAMPLING_RATE_SENSORS:kotlin.String` permission, the highest direct report rate level is `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_NORMAL:kotlin.Int`. If the sensor does not support direct report mode, this returns `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_STOP:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_STOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_FAST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_VERY_FAST:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_STOP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_NORMAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#RATE_VERY_FAST:kotlin.Int`

### getId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The sensor id that will be unique for the same app unless the device is factory reset. Return value of 0 means this sensor does not support this function; return value of -1 means this sensor can be uniquely identified in system by combination of its type and name. |

### getMaxDelay

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxDelay(): Int
```

This value is defined only for continuous and on-change sensors. It is the delay between two sensor events corresponding to the lowest frequency that this sensor supports. When lower frequencies are requested through registerListener() the events will be generated at this frequency instead. It can be used to estimate when the batch FIFO may be full. Older devices may set this value to zero. Ignore this value in case it is negative or zero.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The max delay for this sensor in microseconds. |

### getMaximumRange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaximumRange(): Float
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | maximum range of the sensor in the sensor's unit. |

### getMinDelay

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinDelay(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum delay allowed between two events in microseconds or zero if this sensor only returns a value when the data it's measuring changes. Note that if the app does not have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#HIGH_SAMPLING_RATE_SENSORS:kotlin.String` permission, the minimum delay is capped at 5000 microseconds (200 Hz). |

### getName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String!
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | name string of the sensor. The name is guaranteed to be unique for a particular sensor type. |

### getPower

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPower(): Float
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the power in mA used by this sensor while in use |

### getReportingMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReportingMode(): Int
```

Each sensor has exactly one reporting mode associated with it. This method returns the reporting mode constant for this sensor type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Reporting mode for the input sensor, one of REPORTING_MODE_\* constants. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_CONTINUOUS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_ON_CHANGE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_ONE_SHOT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/Sensor#REPORTING_MODE_SPECIAL_TRIGGER:kotlin.Int`

### getResolution

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResolution(): Float
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | resolution of the sensor in the sensor's unit. |

### getStringType

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStringType(): String!
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The type of this sensor as a string. |

### getType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | generic type of this sensor. |

### getVendor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVendor(): String!
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | vendor string of this sensor. |

### getVersion

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVersion(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | version of the sensor's module. |

### isAdditionalInfoSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAdditionalInfoSupported(): Boolean
```

Returns true if the sensor supports sensor additional information API

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the sensor supports sensor additional information API |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo`

### isDirectChannelTypeSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDirectChannelTypeSupported(sharedMemType: Int): Boolean
```

Test if a sensor supports a specified direct channel type.

| Parameters ||
|---|---|
| `sharedMemType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of shared memory used by direct channel. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#TYPE_MEMORY_FILE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#TYPE_HARDWARE_BUFFER:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified shared memory type is supported. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#TYPE_MEMORY_FILE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel#TYPE_HARDWARE_BUFFER:kotlin.Int`

### isDynamicSensor

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDynamicSensor(): Boolean
```

Returns true if the sensor is a dynamic sensor.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the sensor is a dynamic sensor (sensor added at runtime). |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/SensorManager.DynamicSensorCallback`

### isWakeUpSensor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isWakeUpSensor(): Boolean
```

Returns true if the sensor is a wake-up sensor.

**Application Processor Power modes**

Application Processor(AP), is the processor on which applications run. When no wake lock is held and the user is not interacting with the device, this processor can enter a "Suspend" mode, reducing the power consumption by 10 times or more.

**Non-wake-up sensors**

Non-wake-up sensors are sensors that do not wake the AP out of suspend to report data. While the AP is in suspend mode, the sensors continue to function and generate events, which are put in a hardware FIFO. The events in the FIFO are delivered to the application when the AP wakes up. If the FIFO was too small to store all events generated while the AP was in suspend mode, the older events are lost: the oldest data is dropped to accommodate the newer data. In the extreme case where the FIFO is non-existent `maxFifoEventCount() == 0`, all events generated while the AP was in suspend mode are lost. Applications using non-wake-up sensors should usually:

- Either unregister from the sensors when they do not need them, usually in the activity's `onPause` method. This is the most common case.
- Or realize that the sensors are consuming some power while the AP is in suspend mode and that even then, some events might be lost.

<br />

**Wake-up sensors**

In opposition to non-wake-up sensors, wake-up sensors ensure that their data is delivered independently of the state of the AP. While the AP is awake, the wake-up sensors behave like non-wake-up-sensors. When the AP is asleep, wake-up sensors wake up the AP to deliver events. That is, the AP will wake up and the sensor will deliver the events before the maximum reporting latency is elapsed or the hardware FIFO gets full. See `https://developer.android.com/reference/kotlin/android/hardware/SensorManager#registerListener(android.hardware.SensorEventListener,%20android.hardware.Sensor,%20kotlin.Int,%20kotlin.Int)` for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this is a wake-up sensor, `false` otherwise. |

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
