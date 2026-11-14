# SensorManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorManager

Kotlin| [Java](SensorManager.md) 
| --- | --- |

```
abstract class SensorManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.SensorManager](SensorManager.md) |

SensorManager lets you access the device's [sensors](Sensor.md).

Always make sure to disable sensors you don't need, especially when your activity is paused. Failing to do so can drain the battery in just a few hours. Note that the system will*not*disable sensors automatically when the screen turns off.

Note: Don't use this mechanism with a Trigger Sensor, have a look at [TriggerEventListener](TriggerEventListener.md). [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md) is an example of a trigger sensor.

In order to access sensor data at high sampling rates (i.e. greater than 200 Hz for [SensorEventListener](SensorEventListener.md) and greater than [SensorDirectChannel.RATE_NORMAL](SensorDirectChannel.md) for [SensorDirectChannel](SensorDirectChannel.md)), apps must declare the [android.Manifest.permission#HIGH_SAMPLING_RATE_SENSORS](../android/Manifest.permission.md) permission in their AndroidManifest.xml file. 

```kotlin
public class SensorActivity extends Activity implements SensorEventListener {
      private final SensorManager mSensorManager;
      private final Sensor mAccelerometer;
 
      public SensorActivity() {
          mSensorManager = (SensorManager)getSystemService(SENSOR_SERVICE);
          mAccelerometer = mSensorManager.getDefaultSensor(Sensor.TYPE_ACCELEROMETER);
      }
 
      protected void onResume() {
          super.onResume();
          mSensorManager.registerListener(this, mAccelerometer, SensorManager.SENSOR_DELAY_NORMAL);
      }
 
      protected void onPause() {
          super.onPause();
          mSensorManager.unregisterListener(this);
      }
 
      public void onAccuracyChanged(Sensor sensor, int accuracy) {
      }
 
      public void onSensorChanged(SensorEvent event) {
      }
  }
  
```

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) Used for receiving notifications from the SensorManager when dynamic sensors are connected or disconnected. |

| Constants ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_MINUS_X](SensorManager.md) see [remapCoordinateSystem](SensorManager.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_MINUS_Y](SensorManager.md) see [remapCoordinateSystem](SensorManager.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_MINUS_Z](SensorManager.md) see [remapCoordinateSystem](SensorManager.md)) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_X](SensorManager.md) see [remapCoordinateSystem](SensorManager.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_Y](SensorManager.md) see [remapCoordinateSystem](SensorManager.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_Z](SensorManager.md) see [remapCoordinateSystem](SensorManager.md)) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_X](SensorManager.md) Index of the X value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_Y](SensorManager.md) Index of the Y value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_Z](SensorManager.md) Index of the Z value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_DEATH_STAR_I](SensorManager.md) Gravity (estimate) on the first Death Star in Empire units (m/s\^2) |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_EARTH](SensorManager.md) Earth's gravity in SI units (m/s\^2) |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_JUPITER](SensorManager.md) Jupiter's gravity in SI units (m/s\^2) |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_MARS](SensorManager.md) Mars' gravity in SI units (m/s\^2) |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_MERCURY](SensorManager.md) Mercury's gravity in SI units (m/s\^2) |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_MOON](SensorManager.md) The Moon's gravity in SI units (m/s\^2) |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_NEPTUNE](SensorManager.md) Neptune's gravity in SI units (m/s\^2) |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_PLUTO](SensorManager.md) Pluto's gravity in SI units (m/s\^2) |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_SATURN](SensorManager.md) Saturn's gravity in SI units (m/s\^2) |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_SUN](SensorManager.md) Sun's gravity in SI units (m/s\^2) |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_THE_ISLAND](SensorManager.md) Gravity on the island |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_URANUS](SensorManager.md) Uranus' gravity in SI units (m/s\^2) |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [GRAVITY_VENUS](SensorManager.md) Venus' gravity in SI units (m/s\^2) |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LIGHT_CLOUDY](SensorManager.md) luminance under a cloudy sky in lux |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LIGHT_FULLMOON](SensorManager.md) luminance at night with full moon in lux |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LIGHT_NO_MOON](SensorManager.md) luminance at night with no moon in lux |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LIGHT_OVERCAST](SensorManager.md) luminance under an overcast sky in lux |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LIGHT_SHADE](SensorManager.md) luminance in shade in lux |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LIGHT_SUNLIGHT](SensorManager.md) luminance of sunlight in lux |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LIGHT_SUNLIGHT_MAX](SensorManager.md) Maximum luminance of sunlight in lux |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LIGHT_SUNRISE](SensorManager.md) luminance at sunrise in lux |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [MAGNETIC_FIELD_EARTH_MAX](SensorManager.md) Maximum magnetic field on Earth's surface |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [MAGNETIC_FIELD_EARTH_MIN](SensorManager.md) Minimum magnetic field on Earth's surface |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [PRESSURE_STANDARD_ATMOSPHERE](SensorManager.md) Standard atmosphere, or average sea-level pressure in hPa (millibar) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RAW_DATA_INDEX](SensorManager.md) Offset to the untransformed values in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RAW_DATA_X](SensorManager.md) Index of the untransformed X value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RAW_DATA_Y](SensorManager.md) Index of the untransformed Y value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RAW_DATA_Z](SensorManager.md) Index of the untransformed Z value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_ACCELEROMETER](SensorManager.md) A constant describing an accelerometer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_ALL](SensorManager.md) A constant that includes all sensors |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_DELAY_FASTEST](SensorManager.md) get sensor data as fast as possible |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_DELAY_GAME](SensorManager.md) rate suitable for games |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_DELAY_NORMAL](SensorManager.md) rate (default) suitable for screen orientation changes |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_DELAY_UI](SensorManager.md) rate suitable for the user interface |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_LIGHT](SensorManager.md) A constant describing an ambient light sensor See [SensorListener](SensorListener.md) for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_MAGNETIC_FIELD](SensorManager.md) A constant describing a magnetic sensor See [SensorListener](SensorListener.md) for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_MAX](SensorManager.md) Largest sensor ID |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_MIN](SensorManager.md) Smallest sensor ID |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_ORIENTATION](SensorManager.md) A constant describing an orientation sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_ORIENTATION_RAW](SensorManager.md) A constant describing an orientation sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_PROXIMITY](SensorManager.md) A constant describing a proximity sensor See [SensorListener](SensorListener.md) for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_STATUS_ACCURACY_HIGH](SensorManager.md) This sensor is reporting data with maximum accuracy |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_STATUS_ACCURACY_LOW](SensorManager.md) This sensor is reporting data with low accuracy, calibration with the environment is needed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_STATUS_ACCURACY_MEDIUM](SensorManager.md) This sensor is reporting data with an average level of accuracy, calibration with the environment may improve the readings |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_STATUS_NO_CONTACT](SensorManager.md) The values returned by this sensor cannot be trusted because the sensor had no contact with what it was measuring (for example, the heart rate monitor is not in contact with the user). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_STATUS_UNRELIABLE](SensorManager.md) The values returned by this sensor cannot be trusted, calibration is needed or the environment doesn't allow readings |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_TEMPERATURE](SensorManager.md) A constant describing a temperature sensor See [SensorListener](SensorListener.md) for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SENSOR_TRICORDER](SensorManager.md) A constant describing a Tricorder See [SensorListener](SensorListener.md) for more details. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [STANDARD_GRAVITY](SensorManager.md) Standard gravity (g) on Earth. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancelTriggerSensor](SensorManager.md))`(`listener:` ` [TriggerEventListener](TriggerEventListener.md)!`, `sensor:` ` [Sensor](Sensor.md)!`)` Cancels receiving trigger events for a trigger sensor. |
| open [SensorDirectChannel](SensorDirectChannel.md)! | [createDirectChannel](SensorManager.md))`(`mem:` ` [HardwareBuffer](HardwareBuffer.md)!`)` Create a sensor direct channel backed by shared memory wrapped in HardwareBuffer object. |
| open [SensorDirectChannel](SensorDirectChannel.md)! | [createDirectChannel](SensorManager.md))`(`mem:` ` [MemoryFile](../android.os/MemoryFile.md)!`)` Create a sensor direct channel backed by shared memory wrapped in MemoryFile object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [flush](SensorManager.md))`(`listener:` ` [SensorEventListener](SensorEventListener.md)!`)` Flushes the FIFO of all the sensors registered for this listener. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAltitude](SensorManager.md))`(`p0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `p:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Computes the Altitude in meters from the atmospheric pressure and the pressure at sea level. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getAngleChange](SensorManager.md))`(`angleChange:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `R:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `prevR:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Helper function to compute the angle change between two rotation matrices. |
| --- | --- |
| open [Sensor](Sensor.md)? | [getDefaultSensor](SensorManager.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Use this method to get the default sensor for a given type. |
| open [Sensor](Sensor.md)? | [getDefaultSensor](SensorManager.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `wakeUp:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return a Sensor with the given type and wakeUp properties. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Sensor](Sensor.md)!\>! | [getDynamicSensorList](SensorManager.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Use this method to get a list of available dynamic sensors of a certain type. |
| --- | --- |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInclination](SensorManager.md))`(`I:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Computes the geomagnetic inclination angle in radians from the inclination matrix**I** returned by [getRotationMatrix](SensorManager.md)). |
| openstatic [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [getOrientation](SensorManager.md))`(`R:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Computes the device's orientation based on the rotation matrix. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getQuaternionFromVector](SensorManager.md))`(`Q:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `rv:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Helper function to convert a rotation vector to a normalized quaternion. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRotationMatrix](SensorManager.md))`(`R:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `I:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `gravity:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `geomagnetic:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Computes the inclination matrix**I** as well as the rotation matrix**R**transforming a vector from the device coordinate system to the world's coordinate system which is defined as a direct orthonormal basis, where: |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRotationMatrixFromVector](SensorManager.md))`(`R:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `rotationVector:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Helper function to convert a rotation vector to a rotation matrix. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Sensor](Sensor.md)!\>! | [getSensorList](SensorManager.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Use this method to get the list of available sensors of a certain type. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSensors](SensorManager.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDynamicSensorDiscoverySupported](SensorManager.md))`()` Tell if dynamic sensor discovery feature is supported by system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDynamicSensorCallback](SensorManager.md))`(`callback:` ` [SensorManager.DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md)!`)` Add a [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) to receive dynamic sensor connection callbacks. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDynamicSensorCallback](SensorManager.md))`(`callback:` ` [SensorManager.DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Add a [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) to receive dynamic sensor connection callbacks. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerListener](SensorManager.md))`(`listener:` ` [SensorEventListener](SensorEventListener.md)!`, `sensor:` ` [Sensor](Sensor.md)!`, `samplingPeriodUs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers a [SensorEventListener](SensorEventListener.md) for the given sensor at the given sampling frequency. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerListener](SensorManager.md))`(`listener:` ` [SensorEventListener](SensorEventListener.md)!`, `sensor:` ` [Sensor](Sensor.md)!`, `samplingPeriodUs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Registers a [SensorEventListener](SensorEventListener.md) for the given sensor. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerListener](SensorManager.md))`(`listener:` ` [SensorEventListener](SensorEventListener.md)!`, `sensor:` ` [Sensor](Sensor.md)!`, `samplingPeriodUs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxReportLatencyUs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers a [SensorEventListener](SensorEventListener.md) for the given sensor at the given sampling frequency and the given maximum reporting latency. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerListener](SensorManager.md))`(`listener:` ` [SensorEventListener](SensorEventListener.md)!`, `sensor:` ` [Sensor](Sensor.md)!`, `samplingPeriodUs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxReportLatencyUs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Registers a [SensorEventListener](SensorEventListener.md) for the given sensor at the given sampling frequency and the given maximum reporting latency. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerListener](SensorManager.md))`(`listener:` ` [SensorListener](SensorListener.md)!`, `sensors:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers a listener for given sensors. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerListener](SensorManager.md))`(`listener:` ` [SensorListener](SensorListener.md)!`, `sensors:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers a SensorListener for given sensors. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remapCoordinateSystem](SensorManager.md))`(`inR:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `X:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `Y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outR:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Rotates the supplied rotation matrix so it is expressed in a different coordinate system. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requestTriggerSensor](SensorManager.md))`(`listener:` ` [TriggerEventListener](TriggerEventListener.md)!`, `sensor:` ` [Sensor](Sensor.md)!`)` Requests receiving trigger events for a trigger sensor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDynamicSensorCallback](SensorManager.md))`(`callback:` ` [SensorManager.DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md)!`)` Remove a [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) to stop sending dynamic sensor connection events to that callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterListener](SensorManager.md))`(`listener:` ` [SensorEventListener](SensorEventListener.md)!`)` Unregisters a listener for all sensors. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterListener](SensorManager.md))`(`listener:` ` [SensorEventListener](SensorEventListener.md)!`, `sensor:` ` [Sensor](Sensor.md)!`)` Unregisters a listener for the sensors with which it is registered. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterListener](SensorManager.md))`(`listener:` ` [SensorListener](SensorListener.md)!`)` Unregisters a listener for all sensors. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterListener](SensorManager.md))`(`listener:` ` [SensorListener](SensorListener.md)!`, `sensors:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Unregisters a listener for the sensors with which it is registered. |

## Constants

### AXIS_MINUS_X

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_MINUS_X: Int
```

see [remapCoordinateSystem](SensorManager.md)) 

 Value: 129

### AXIS_MINUS_Y

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_MINUS_Y: Int
```

see [remapCoordinateSystem](SensorManager.md)) 

 Value: 130

### AXIS_MINUS_Z

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_MINUS_Z: Int
```

see [remapCoordinateSystem](SensorManager.md)) 

 Value: 131

### AXIS_X

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_X: Int
```

see [remapCoordinateSystem](SensorManager.md)) 

 Value: 1

### AXIS_Y

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_Y: Int
```

see [remapCoordinateSystem](SensorManager.md)) 

 Value: 2

### AXIS_Z

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_Z: Int
```

see [remapCoordinateSystem](SensorManager.md)) 

 Value: 3

### DATA_X

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_X: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Index of the X value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) 

 Value: 0

### DATA_Y

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_Y: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Index of the Y value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) 

 Value: 1

### DATA_Z

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_Z: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Index of the Z value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) 

 Value: 2

### GRAVITY_DEATH_STAR_I

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_DEATH_STAR_I: Float
```

Gravity (estimate) on the first Death Star in Empire units (m/s\^2) 

 Value: 3.5303614E-7f

### GRAVITY_EARTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_EARTH: Float
```

Earth's gravity in SI units (m/s\^2) 

 Value: 9.80665f

### GRAVITY_JUPITER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_JUPITER: Float
```

Jupiter's gravity in SI units (m/s\^2) 

 Value: 23.12f

### GRAVITY_MARS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_MARS: Float
```

Mars' gravity in SI units (m/s\^2) 

 Value: 3.71f

### GRAVITY_MERCURY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_MERCURY: Float
```

Mercury's gravity in SI units (m/s\^2) 

 Value: 3.7f

### GRAVITY_MOON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_MOON: Float
```

The Moon's gravity in SI units (m/s\^2) 

 Value: 1.6f

### GRAVITY_NEPTUNE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_NEPTUNE: Float
```

Neptune's gravity in SI units (m/s\^2) 

 Value: 11.0f

### GRAVITY_PLUTO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_PLUTO: Float
```

Pluto's gravity in SI units (m/s\^2) 

 Value: 0.6f

### GRAVITY_SATURN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_SATURN: Float
```

Saturn's gravity in SI units (m/s\^2) 

 Value: 8.96f

### GRAVITY_SUN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_SUN: Float
```

Sun's gravity in SI units (m/s\^2) 

 Value: 275.0f

### GRAVITY_THE_ISLAND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_THE_ISLAND: Float
```

Gravity on the island 

 Value: 4.815162f

### GRAVITY_URANUS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_URANUS: Float
```

Uranus' gravity in SI units (m/s\^2) 

 Value: 8.69f

### GRAVITY_VENUS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAVITY_VENUS: Float
```

Venus' gravity in SI units (m/s\^2) 

 Value: 8.87f

### LIGHT_CLOUDY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_CLOUDY: Float
```

luminance under a cloudy sky in lux 

 Value: 100.0f

### LIGHT_FULLMOON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_FULLMOON: Float
```

luminance at night with full moon in lux 

 Value: 0.25f

### LIGHT_NO_MOON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_NO_MOON: Float
```

luminance at night with no moon in lux 

 Value: 0.001f

### LIGHT_OVERCAST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_OVERCAST: Float
```

luminance under an overcast sky in lux 

 Value: 10000.0f

### LIGHT_SHADE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_SHADE: Float
```

luminance in shade in lux 

 Value: 20000.0f

### LIGHT_SUNLIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_SUNLIGHT: Float
```

luminance of sunlight in lux 

 Value: 110000.0f

### LIGHT_SUNLIGHT_MAX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_SUNLIGHT_MAX: Float
```

Maximum luminance of sunlight in lux 

 Value: 120000.0f

### LIGHT_SUNRISE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGHT_SUNRISE: Float
```

luminance at sunrise in lux 

 Value: 400.0f

### MAGNETIC_FIELD_EARTH_MAX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAGNETIC_FIELD_EARTH_MAX: Float
```

Maximum magnetic field on Earth's surface 

 Value: 60.0f

### MAGNETIC_FIELD_EARTH_MIN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAGNETIC_FIELD_EARTH_MIN: Float
```

Minimum magnetic field on Earth's surface 

 Value: 30.0f

### PRESSURE_STANDARD_ATMOSPHERE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESSURE_STANDARD_ATMOSPHERE: Float
```

Standard atmosphere, or average sea-level pressure in hPa (millibar) 

 Value: 1013.25f

### RAW_DATA_INDEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_DATA_INDEX: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Offset to the untransformed values in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) 

 Value: 3

### RAW_DATA_X

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_DATA_X: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Index of the untransformed X value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) 

 Value: 3

### RAW_DATA_Y

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_DATA_Y: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Index of the untransformed Y value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) 

 Value: 4

### RAW_DATA_Z

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_DATA_Z: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Index of the untransformed Z value in the array returned by [android.hardware.SensorListener#onSensorChanged](SensorListener.md)) 

 Value: 5

### SENSOR_ACCELEROMETER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_ACCELEROMETER: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant describing an accelerometer. See [SensorListener](SensorListener.md) for more details. 

 Value: 2

### SENSOR_ALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_ALL: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant that includes all sensors 

 Value: 127

### SENSOR_DELAY_FASTEST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_DELAY_FASTEST: Int
```

get sensor data as fast as possible 

 Value: 0

### SENSOR_DELAY_GAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_DELAY_GAME: Int
```

rate suitable for games 

 Value: 1

### SENSOR_DELAY_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_DELAY_NORMAL: Int
```

rate (default) suitable for screen orientation changes 

 Value: 3

### SENSOR_DELAY_UI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_DELAY_UI: Int
```

rate suitable for the user interface 

 Value: 2

### SENSOR_LIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_LIGHT: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant describing an ambient light sensor See [SensorListener](SensorListener.md) for more details. 

 Value: 16

### SENSOR_MAGNETIC_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_MAGNETIC_FIELD: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant describing a magnetic sensor See [SensorListener](SensorListener.md) for more details. 

 Value: 8

### SENSOR_MAX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_MAX: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Largest sensor ID 

 Value: 64

### SENSOR_MIN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_MIN: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

Smallest sensor ID 

 Value: 1

### SENSOR_ORIENTATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_ORIENTATION: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant describing an orientation sensor. See [SensorListener](SensorListener.md) for more details. 

 Value: 1

### SENSOR_ORIENTATION_RAW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_ORIENTATION_RAW: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant describing an orientation sensor. See [SensorListener](SensorListener.md) for more details. 

 Value: 128

### SENSOR_PROXIMITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_PROXIMITY: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant describing a proximity sensor See [SensorListener](SensorListener.md) for more details. 

 Value: 32

### SENSOR_STATUS_ACCURACY_HIGH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_STATUS_ACCURACY_HIGH: Int
```

This sensor is reporting data with maximum accuracy 

 Value: 3

### SENSOR_STATUS_ACCURACY_LOW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_STATUS_ACCURACY_LOW: Int
```

This sensor is reporting data with low accuracy, calibration with the environment is needed 

 Value: 1

### SENSOR_STATUS_ACCURACY_MEDIUM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_STATUS_ACCURACY_MEDIUM: Int
```

This sensor is reporting data with an average level of accuracy, calibration with the environment may improve the readings 

 Value: 2

### SENSOR_STATUS_NO_CONTACT

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_STATUS_NO_CONTACT: Int
```

The values returned by this sensor cannot be trusted because the sensor had no contact with what it was measuring (for example, the heart rate monitor is not in contact with the user). 

 Value: -1

### SENSOR_STATUS_UNRELIABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_STATUS_UNRELIABLE: Int
```

The values returned by this sensor cannot be trusted, calibration is needed or the environment doesn't allow readings 

 Value: 0

### SENSOR_TEMPERATURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_TEMPERATURE: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant describing a temperature sensor See [SensorListener](SensorListener.md) for more details. 

 Value: 4

### SENSOR_TRICORDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSOR_TRICORDER: Int
```

**Deprecated:** *use [Sensor](Sensor.md) instead.*

A constant describing a Tricorder See [SensorListener](SensorListener.md) for more details. 

 Value: 64

### STANDARD_GRAVITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARD_GRAVITY: Float
```

Standard gravity (g) on Earth. This value is equivalent to 1G 

 Value: 9.80665f

## Public methods

### cancelTriggerSensor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancelTriggerSensor(
    listener: TriggerEventListener!, 
    sensor: Sensor!
): Boolean
```

Cancels receiving trigger events for a trigger sensor.

Note that a Trigger sensor will be auto disabled if [TriggerEventListener.onTrigger(TriggerEvent)](TriggerEventListener.md))has triggered. This method is provided in case the user wants to explicitly cancel the request to receive trigger events.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [TriggerEventListener](TriggerEventListener.md)!:The listener on which the [TriggerEventListener.onTrigger(TriggerEvent)](TriggerEventListener.md))is delivered.It should be the same as the one used in [requestTriggerSensor(android.hardware.TriggerEventListener,android.hardware.Sensor)](SensorManager.md)) |
| `sensor` | [Sensor](Sensor.md)!:The sensor for which the trigger request should be canceled. If null, it cancels receiving trigger for all sensors associated with the listener. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if successfully canceled. |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | when sensor is a trigger sensor. |

### createDirectChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createDirectChannel(mem: HardwareBuffer!): SensorDirectChannel!
```

Create a sensor direct channel backed by shared memory wrapped in HardwareBuffer object. The resulting channel can be used for delivering sensor events to native code, other processes, GPU/DSP or other co-processors without CPU intervention. This is the recommended for high performance sensor applications that use high sensor rates (e.g. greater than 200Hz) and cares about sensor event latency. Use the returned [android.hardware.SensorDirectChannel](SensorDirectChannel.md) object to configure direct report of sensor events. After use, call android.hardware.SensorDirectChannel#close() to free up resource in sensor system associated with the direct channel.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mem` | [HardwareBuffer](HardwareBuffer.md)!:A [android.hardware.HardwareBuffer](HardwareBuffer.md) shared memory object. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [SensorDirectChannel](SensorDirectChannel.md)! | A [android.hardware.SensorDirectChannel](SensorDirectChannel.md) object. |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | when mem is null. |
| `UncheckedIOException` | if not able to create channel. |

**See Also**

### createDirectChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createDirectChannel(mem: MemoryFile!): SensorDirectChannel!
```

Create a sensor direct channel backed by shared memory wrapped in MemoryFile object. The resulting channel can be used for delivering sensor events to native code, other processes, GPU/DSP or other co-processors without CPU intervention. This is the recommended for high performance sensor applications that use high sensor rates (e.g. greater than 200Hz) and cares about sensor event latency. Use the returned [android.hardware.SensorDirectChannel](SensorDirectChannel.md) object to configure direct report of sensor events. After use, call android.hardware.SensorDirectChannel#close() to free up resource in sensor system associated with the direct channel.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mem` | [MemoryFile](../android.os/MemoryFile.md)!:A [android.os.MemoryFile](../android.os/MemoryFile.md) shared memory object. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [SensorDirectChannel](SensorDirectChannel.md)! | A [android.hardware.SensorDirectChannel](SensorDirectChannel.md) object. |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | when mem is null. |
| `UncheckedIOException` | if not able to create channel. |

**See Also**

### flush

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(listener: SensorEventListener!): Boolean
```

Flushes the FIFO of all the sensors registered for this listener. If there are events in the FIFO of the sensor, they are returned as if the maxReportLatency of the FIFO has expired. Events are returned in the usual way through the SensorEventListener. This call doesn't affect the maxReportLatency for this sensor. This call is asynchronous and returns immediately. [onFlushCompleted](SensorEventListener2.md))is called after all the events in the batch at the time of calling this method have been delivered successfully. If the hardware doesn't support flush, it still returns true and a trivial flush complete event is sent after the current event for all the clients registered for this sensor.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorEventListener](SensorEventListener.md)!:A [SensorEventListener](SensorEventListener.md) object which was previously used in a registerListener call. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the flush is initiated successfully on all the sensors registered for this listener, false if no sensor is previously registered for this listener or flush on one of the sensors fails. |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | when listener is null. |

**See Also**

- [#registerListener(SensorEventListener, Sensor, int, int)](SensorManager.md)) 

### getAltitude

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAltitude(
    p0: Float, 
    p: Float
): Float
```

Computes the Altitude in meters from the atmospheric pressure and the pressure at sea level.

Typically the atmospheric pressure is read from a [Sensor.TYPE_PRESSURE](Sensor.md) sensor. The pressure at sea level must be known, usually it can be retrieved from airport databases in the vicinity. If unknown, you can use [PRESSURE_STANDARD_ATMOSPHERE](SensorManager.md) as an approximation, but absolute altitudes won't be accurate.

To calculate altitude differences, you must calculate the difference between the altitudes at both points. If you don't know the altitude as sea level, you can use [PRESSURE_STANDARD_ATMOSPHERE](SensorManager.md) instead, which will give good results considering the range of pressure typically involved.

` float altitude_difference = getAltitude(SensorManager.PRESSURE_STANDARD_ATMOSPHERE, pressure_at_point2) - getAltitude(SensorManager.PRESSURE_STANDARD_ATMOSPHERE, pressure_at_point1); `

<br />

| Parameters ||
|------|------------------------------------------------------------------------------------------------------|
| `p0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):pressure at sea level |
| `p` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):atmospheric pressure |

| Return ||
|--------------------------------------------------------------------------------|--------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Altitude in meters |

### getAngleChange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAngleChange(
    angleChange: FloatArray!, 
    R: FloatArray!, 
    prevR: FloatArray!
): Unit
```

Helper function to compute the angle change between two rotation matrices. Given a current rotation matrix (R) and a previous rotation matrix (prevR) computes the intrinsic rotation around the z, x, and y axes which transforms prevR to R. outputs a 3 element vector containing the z, x, and y angle change at indexes 0, 1, and 2 respectively.

Each input matrix is either as a 3x3 or 4x4 row-major matrix depending on the length of the passed array:

If the array length is 9, then the array elements represent this matrix 

```kotlin
/  R[ 0]   R[ 1]   R[ 2]   \
    |  R[ 3]   R[ 4]   R[ 5]   |
    \  R[ 6]   R[ 7]   R[ 8]   /
 
```

If the array length is 16, then the array elements represent this matrix 

```kotlin
/  R[ 0]   R[ 1]   R[ 2]   R[ 3]  \
    |  R[ 4]   R[ 5]   R[ 6]   R[ 7]  |
    |  R[ 8]   R[ 9]   R[10]   R[11]  |
    \  R[12]   R[13]   R[14]   R[15]  /
 
```
See [getOrientation](SensorManager.md))for more detailed definition of the output.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `R` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:current rotation matrix |
| `prevR` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:previous rotation matrix |
| `angleChange` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:an an array of floats (z, x, and y) in which the angle change (in radians) is stored |
| --- | --- |

### getDefaultSensor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultSensor(type: Int): Sensor?
```

Use this method to get the default sensor for a given type. Note that the returned sensor could be a composite sensor, and its data could be averaged or filtered. If you need to access the raw sensors use [getSensorList](SensorManager.md)).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of sensors requested |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Sensor](Sensor.md)? | the default sensor matching the requested type if one exists and the application has the necessary permissions, or null otherwise. |

**See Also**

- [#getSensorList(int)](SensorManager.md))
- [android.hardware.Sensor](Sensor.md) 

### getDefaultSensor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultSensor(
    type: Int, 
    wakeUp: Boolean
): Sensor?
```

Return a Sensor with the given type and wakeUp properties. If multiple sensors of this type exist, any one of them may be returned.

For example,

- getDefaultSensor([Sensor.TYPE_ACCELEROMETER](Sensor.md), true) returns a wake-up accelerometer sensor if it exists.
- getDefaultSensor([Sensor.TYPE_PROXIMITY](Sensor.md), false) returns a non wake-up proximity sensor if it exists.
- getDefaultSensor([Sensor.TYPE_PROXIMITY](Sensor.md), true) returns a wake-up proximity sensor which is the same as the Sensor returned by [getDefaultSensor(int)](SensorManager.md)).

<br />

Note: Sensors like [Sensor.TYPE_PROXIMITY](Sensor.md) and [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md) are declared as wake-up sensors by default.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):type of sensor requested |
| `wakeUp` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):flag to indicate whether the Sensor is a wake-up or non wake-up sensor. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sensor](Sensor.md)? | the default sensor matching the requested type and wakeUp properties if one exists and the application has the necessary permissions, or null otherwise. |

**See Also**

- [android.hardware.Sensor#isWakeUpSensor()](Sensor.md)) 

### getDynamicSensorList

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDynamicSensorList(type: Int): MutableList<Sensor!>!
```

Use this method to get a list of available dynamic sensors of a certain type. Make multiple calls to get sensors of different types or use [Sensor.TYPE_ALL](Sensor.md) to get all dynamic sensors.

NOTE: Both wake-up and non wake-up sensors matching the given type are returned. Check [Sensor.isWakeUpSensor()](Sensor.md))to know the wake-up properties of the returned [Sensor](Sensor.md).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of sensors requested |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Sensor](Sensor.md)!>! | a list of dynamic sensors matching the requested type. |

**See Also**

- [android.hardware.Sensor](Sensor.md) 

### getInclination

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInclination(I: FloatArray!): Float
```

Computes the geomagnetic inclination angle in radians from the inclination matrix**I** returned by [getRotationMatrix](SensorManager.md)).

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `I` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:inclination matrix see [getRotationMatrix](SensorManager.md)). |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The geomagnetic inclination angle in radians. |

**See Also**

- [#getRotationMatrix(float[], float[], float[], float[])](https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getRotationMatrix(kotlin.FloatArray,%20kotlin.FloatArray,%20kotlin.FloatArray,%20kotlin.FloatArray))
- [#getOrientation(float[], float[])](https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getOrientation(kotlin.FloatArray,%20kotlin.FloatArray))
- [android.hardware.GeomagneticField](GeomagneticField.md) 

### getOrientation

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getOrientation(
    R: FloatArray!, 
    values: FloatArray!
): FloatArray!
```

Computes the device's orientation based on the rotation matrix.

When it returns, the array values are as follows:

- values\[0\]:*Azimuth*, angle of rotation about the -z axis. This value represents the angle between the device's y axis and the magnetic north pole. When facing north, this angle is 0, when facing south, this angle is π. Likewise, when facing east, this angle is π/2, and when facing west, this angle is -π/2. The range of values is -π to π.
- values\[1\]:*Pitch*, angle of rotation about the -x axis. This value represents the angle between a plane parallel to the device's screen and a plane parallel to the ground. Assuming that the bottom edge of the device faces the user and that the screen is face-up, tilting the top edge of the device toward the ground creates a positive pitch angle. The range of values is -π/2 to π/2.
- values\[2\]:*Roll*, angle of rotation about the y axis. This value represents the angle between a plane perpendicular to the device's screen and a plane perpendicular to the ground. Assuming that the bottom edge of the device faces the user and that the screen is face-up, tilting the right edge of the device toward the ground creates a positive roll angle. The range of values is -π to π.

Applying these three rotations in the azimuth, pitch, roll order transforms an identity matrix to the rotation matrix passed into this method. Also, note that all three orientation angles are expressed in**radians**.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `R` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:rotation matrix see [getRotationMatrix](SensorManager.md)). |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:an array of 3 floats to hold the result. |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | The array values passed as argument. |

**See Also**

- [#getRotationMatrix(float[], float[], float[], float[])](https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getRotationMatrix(kotlin.FloatArray,%20kotlin.FloatArray,%20kotlin.FloatArray,%20kotlin.FloatArray))
- [android.hardware.GeomagneticField](GeomagneticField.md) 

### getQuaternionFromVector

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getQuaternionFromVector(
    Q: FloatArray!, 
    rv: FloatArray!
): Unit
```

Helper function to convert a rotation vector to a normalized quaternion. Given a rotation vector (presumably from a ROTATION_VECTOR sensor), returns a normalized quaternion in the array Q. The quaternion is stored as \[w, x, y, z\]

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rv` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the rotation vector to convert |
| `Q` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:an array of floats in which to store the computed quaternion |

### getRotationMatrix

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRotationMatrix(
    R: FloatArray!, 
    I: FloatArray!, 
    gravity: FloatArray!, 
    geomagnetic: FloatArray!
): Boolean
```

Computes the inclination matrix**I** as well as the rotation matrix**R**transforming a vector from the device coordinate system to the world's coordinate system which is defined as a direct orthonormal basis, where:

- X is defined as the vector product**Y.Z**(It is tangential to the ground at the device's current location and roughly points East).
- Y is tangential to the ground at the device's current location and points towards the magnetic North Pole.
- Z points towards the sky and is perpendicular to the ground.

<br />

<br />

<br />

By definition:

\[0 0 g\] =**R** \***gravity**(g = magnitude of gravity)

\[0 m 0\] =**I** \***R** \***geomagnetic**(m = magnitude of geomagnetic field)

**R**is the identity matrix when the device is aligned with the world's coordinate system, that is, when the device's X axis points toward East, the Y axis points to the North Pole and the device is facing the sky.

**I** is a rotation matrix transforming the geomagnetic vector into the same coordinate space as gravity (the world's coordinate space).**I** is a simple rotation around the X axis. The inclination angle in radians can be computed with [getInclination](SensorManager.md)).

Each matrix is returned either as a 3x3 or 4x4 row-major matrix depending on the length of the passed array:

If the array length is 16: 

```kotlin
/  M[ 0]   M[ 1]   M[ 2]   M[ 3]  \
    |  M[ 4]   M[ 5]   M[ 6]   M[ 7]  |
    |  M[ 8]   M[ 9]   M[10]   M[11]  |
    \  M[12]   M[13]   M[14]   M[15]  /
 
```
This matrix is ready to be used by OpenGL ES's[glLoadMatrixf(float[], int)](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL10.html#glLoadMatrixf(kotlin.FloatArray,%20kotlin.Int)).

Note that because OpenGL matrices are column-major matrices you must transpose the matrix before using it. However, since the matrix is a rotation matrix, its transpose is also its inverse, conveniently, it is often the inverse of the rotation that is needed for rendering; it can therefore be used with OpenGL ES directly.

Also note that the returned matrices always have this form: 

```kotlin
/  M[ 0]   M[ 1]   M[ 2]   0  \
    |  M[ 4]   M[ 5]   M[ 6]   0  |
    |  M[ 8]   M[ 9]   M[10]   0  |
    \      0       0       0   1  /
 
```

If the array length is 9: 

```kotlin
/  M[ 0]   M[ 1]   M[ 2]  \
    |  M[ 3]   M[ 4]   M[ 5]  |
    \  M[ 6]   M[ 7]   M[ 8]  /
 
```

The inverse of each matrix can be computed easily by taking its transpose.

The matrices returned by this function are meaningful only when the device is not free-falling and it is not close to the magnetic north. If the device is accelerating, or placed into a strong magnetic field, the returned matrices may be inaccurate.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `R` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:is an array of 9 floats holding the rotation matrix**R** when this function returns. R can be null. <br /> |
| `I` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:is an array of 9 floats holding the rotation matrix**I** when this function returns. I can be null. <br /> |
| `gravity` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:is an array of 3 floats containing the gravity vector expressed in the device's coordinate. You can simply use the [values](SensorEvent.md) returned by a [SensorEvent](SensorEvent.md) of a [Sensor](Sensor.md) of type [TYPE_ACCELEROMETER](Sensor.md). <br /> |
| --- | --- |
| `geomagnetic` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:is an array of 3 floats containing the geomagnetic vector expressed in the device's coordinate. You can simply use the [values](SensorEvent.md) returned by a [SensorEvent](SensorEvent.md) of a [Sensor](Sensor.md) of type [TYPE_MAGNETIC_FIELD](Sensor.md). |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`on success,`false`on failure (for instance, if the device is in free fall). Free fall is defined as condition when the magnitude of the gravity is less than 1/10 of the nominal value. On failure the output matrices are not modified. |

**See Also**

- [#getInclination(float[])](https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getInclination(kotlin.FloatArray))
- [#getOrientation(float[], float[])](https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getOrientation(kotlin.FloatArray,%20kotlin.FloatArray))
- [#remapCoordinateSystem(float[], int, int, float[])](https://developer.android.com/reference/kotlin/android/hardware/SensorManager#remapCoordinateSystem(kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray)) 

### getRotationMatrixFromVector

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRotationMatrixFromVector(
    R: FloatArray!, 
    rotationVector: FloatArray!
): Unit
```

Helper function to convert a rotation vector to a rotation matrix. Given a rotation vector (presumably from a ROTATION_VECTOR sensor), returns a 9 or 16 element rotation matrix in the array R. R must have length 9 or 16. If R.length == 9, the following matrix is returned: 

```kotlin
/  R[ 0]   R[ 1]   R[ 2]   \
    |  R[ 3]   R[ 4]   R[ 5]   |
    \  R[ 6]   R[ 7]   R[ 8]   /
 
```
If R.length == 16, the following matrix is returned: 

```kotlin
/  R[ 0]   R[ 1]   R[ 2]   0  \
    |  R[ 4]   R[ 5]   R[ 6]   0  |
    |  R[ 8]   R[ 9]   R[10]   0  |
    \  0       0       0       1  /
 
```

<br />

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `rotationVector` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the rotation vector to convert |
| `R` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:an array of floats in which to store the rotation matrix |

### getSensorList

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSensorList(type: Int): MutableList<Sensor!>!
```

Use this method to get the list of available sensors of a certain type. Make multiple calls to get sensors of different types or use [Sensor.TYPE_ALL](Sensor.md) to get all the sensors. Note that the [android.hardware.Sensor#getName()](Sensor.md))is expected to yield a value that is unique across any sensors that return the same value for [android.hardware.Sensor#getType()](Sensor.md)).

NOTE: Both wake-up and non wake-up sensors matching the given type are returned. Check [Sensor.isWakeUpSensor()](Sensor.md))to know the wake-up properties of the returned [Sensor](Sensor.md).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of sensors requested |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Sensor](Sensor.md)!>! | a list of sensors matching the asked type. |

**See Also**

- [#getDefaultSensor(int)](SensorManager.md))
- [android.hardware.Sensor](Sensor.md) 

### getSensors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSensors(): Int
```

**Deprecated:** *This method is deprecated, use [SensorManager.getSensorList(int)](SensorManager.md))instead*

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | available sensors. |

### isDynamicSensorDiscoverySupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDynamicSensorDiscoverySupported(): Boolean
```

Tell if dynamic sensor discovery feature is supported by system.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if dynamic sensor discovery is supported,`false`otherwise. |

### registerDynamicSensorCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerDynamicSensorCallback(callback: SensorManager.DynamicSensorCallback!): Unit
```

Add a [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) to receive dynamic sensor connection callbacks. Repeat registration with the already registered callback object will have no additional effect.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [SensorManager.DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md)!:An object that implements the [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) interface for receiving callbacks. |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | when callback is null. |

**See Also**

- [#registerDynamicSensorCallback(DynamicSensorCallback, Handler)](SensorManager.md)) 

### registerDynamicSensorCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerDynamicSensorCallback(
    callback: SensorManager.DynamicSensorCallback!, 
    handler: Handler!
): Unit
```

Add a [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) to receive dynamic sensor connection callbacks. Repeat registration with the already registered callback object will have no additional effect.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [SensorManager.DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md)!:An object that implements the [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) interface for receiving callbacks. |
| `handler` | [Handler](../android.os/Handler.md)!:The [Handler](../android.os/Handler.md) the will be delivered to. |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | when callback is null. |

### registerListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerListener(
    listener: SensorEventListener!, 
    sensor: Sensor!, 
    samplingPeriodUs: Int
): Boolean
```

Registers a [SensorEventListener](SensorEventListener.md) for the given sensor at the given sampling frequency.

The events will be delivered to the provided`SensorEventListener`as soon as they are available. To reduce the power consumption, applications can use [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int,int)](SensorManager.md))instead and specify a positive non-zero maximum reporting latency.

In the case of non-wake-up sensors, the events are only delivered while the Application Processor (AP) is not in suspend mode. See [Sensor.isWakeUpSensor()](Sensor.md))for more details. To ensure delivery of events from non-wake-up sensors even when the screen is OFF, the application registering to the sensor must hold a partial wake-lock to keep the AP awake, otherwise some events might be lost while the AP is asleep. Note that although events might be lost while the AP is asleep, the sensor will still consume power if it is not explicitly deactivated by the application. Applications must unregister their`SensorEventListener`s in their activity's`onPause()`method to avoid consuming power while the device is inactive. See [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int,int)](SensorManager.md))for more details on hardware FIFO (queueing) capabilities and when some sensor events might be lost.

In the case of wake-up sensors, each event generated by the sensor will cause the AP to wake-up, ensuring that each event can be delivered. Because of this, registering to a wake-up sensor has very significant power implications. Call [Sensor.isWakeUpSensor()](Sensor.md))to check whether a sensor is a wake-up sensor. See [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int,int)](SensorManager.md))for information on how to reduce the power impact of registering to wake-up sensors.

Note: Don't use this method with one-shot trigger sensors such as [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md). Use [requestTriggerSensor(android.hardware.TriggerEventListener,android.hardware.Sensor)](SensorManager.md))instead. Use [Sensor.getReportingMode()](Sensor.md))to obtain the reporting mode of a given sensor.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorEventListener](SensorEventListener.md)!:A [SensorEventListener](SensorEventListener.md) object. |
| `sensor` | [Sensor](Sensor.md)!:The [Sensor](Sensor.md) to register to. |
| `samplingPeriodUs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The rate [sensor events](SensorEvent.md) are delivered at. This is only a hint to the system. Events may be received faster or slower than the specified rate. Usually events are received faster. The value must be one of [SENSOR_DELAY_NORMAL](SensorManager.md), [SENSOR_DELAY_UI](SensorManager.md), [SENSOR_DELAY_GAME](SensorManager.md), or [SENSOR_DELAY_FASTEST](SensorManager.md) or, the desired delay between events in microseconds. Specifying the delay in microseconds only works from Android 2.3 (API level 9) onwards. For earlier releases, you must use one of the`SENSOR_DELAY_*`constants. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the sensor is supported and successfully enabled. |

**See Also**

- [#registerListener(SensorEventListener, Sensor, int, Handler)](SensorManager.md))
- [#unregisterListener(SensorEventListener)](SensorManager.md))
- [#unregisterListener(SensorEventListener, Sensor)](SensorManager.md)) 

### registerListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerListener(
    listener: SensorEventListener!, 
    sensor: Sensor!, 
    samplingPeriodUs: Int, 
    handler: Handler!
): Boolean
```

Registers a [SensorEventListener](SensorEventListener.md) for the given sensor. Events are delivered in continuous mode as soon as they are available. To reduce the power consumption, applications can use [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int,int)](SensorManager.md))instead and specify a positive non-zero maximum reporting latency.

<br />

Note: Don't use this method with a one shot trigger sensor such as [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md). Use [requestTriggerSensor(android.hardware.TriggerEventListener,android.hardware.Sensor)](SensorManager.md))instead.

<br />

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorEventListener](SensorEventListener.md)!:A [SensorEventListener](SensorEventListener.md) object. |
| `sensor` | [Sensor](Sensor.md)!:The [Sensor](Sensor.md) to register to. |
| `samplingPeriodUs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The rate [sensor events](SensorEvent.md) are delivered at. This is only a hint to the system. Events may be received faster or slower than the specified rate. Usually events are received faster. The value must be one of [SENSOR_DELAY_NORMAL](SensorManager.md), [SENSOR_DELAY_UI](SensorManager.md), [SENSOR_DELAY_GAME](SensorManager.md), or [SENSOR_DELAY_FASTEST](SensorManager.md) or, the desired delay between events in microseconds. Specifying the delay in microseconds only works from Android 2.3 (API level 9) onwards. For earlier releases, you must use one of the`SENSOR_DELAY_*`constants. |
| --- | --- |
| `handler` | [Handler](../android.os/Handler.md)!:The [Handler](../android.os/Handler.md) the [sensor events](SensorEvent.md) will be delivered to. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the sensor is supported and successfully enabled. |

**See Also**

- [#registerListener(SensorEventListener, Sensor, int)](SensorManager.md))
- [#unregisterListener(SensorEventListener)](SensorManager.md))
- [#unregisterListener(SensorEventListener, Sensor)](SensorManager.md)) 

### registerListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerListener(
    listener: SensorEventListener!, 
    sensor: Sensor!, 
    samplingPeriodUs: Int, 
    maxReportLatencyUs: Int
): Boolean
```

Registers a [SensorEventListener](SensorEventListener.md) for the given sensor at the given sampling frequency and the given maximum reporting latency.

This function is similar to [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int)](SensorManager.md))but it allows events to stay temporarily in the hardware FIFO (queue) before being delivered. The events can be stored in the hardware FIFO up to`maxReportLatencyUs`microseconds. Once one of the events in the FIFO needs to be reported, all of the events in the FIFO are reported sequentially. This means that some events will be reported before the maximum reporting latency has elapsed.

When`maxReportLatencyUs`is 0, the call is equivalent to a call to [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int)](SensorManager.md)), as it requires the events to be delivered as soon as possible.

When`sensor.maxFifoEventCount()`is 0, the sensor does not use a FIFO, so the call will also be equivalent to [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int)](SensorManager.md)).

Setting`maxReportLatencyUs`to a positive value allows to reduce the number of interrupts the AP (Application Processor) receives, hence reducing power consumption, as the AP can switch to a lower power state while the sensor is capturing the data. This is especially important when registering to wake-up sensors, for which each interrupt causes the AP to wake up if it was in suspend mode. See [Sensor.isWakeUpSensor()](Sensor.md))for more information on wake-up sensors.

<br />

Note: Don't use this method with one-shot trigger sensors such as [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md). Use [requestTriggerSensor(android.hardware.TriggerEventListener,android.hardware.Sensor)](SensorManager.md))instead.

<br />

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorEventListener](SensorEventListener.md)!:A [SensorEventListener](SensorEventListener.md) object that will receive the sensor events. If the application is interested in receiving flush complete notifications, it should register with [SensorEventListener2](SensorEventListener.md) instead. |
| `sensor` | [Sensor](Sensor.md)!:The [Sensor](Sensor.md) to register to. |
| `samplingPeriodUs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired delay between two consecutive events in microseconds. This is only a hint to the system. Events may be received faster or slower than the specified rate. Usually events are received faster. Can be one of [SENSOR_DELAY_NORMAL](SensorManager.md), [SENSOR_DELAY_UI](SensorManager.md), [SENSOR_DELAY_GAME](SensorManager.md), [SENSOR_DELAY_FASTEST](SensorManager.md) or the delay in microseconds. |
| --- | --- |
| `maxReportLatencyUs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum time in microseconds that events can be delayed before being reported to the application. A large value allows reducing the power consumption associated with the sensor. If maxReportLatencyUs is set to zero, events are delivered as soon as they are available, which is equivalent to calling [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int)](SensorManager.md)). |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the sensor is supported and successfully enabled. |

**See Also**

- [#registerListener(SensorEventListener, Sensor, int)](SensorManager.md))
- [#unregisterListener(SensorEventListener)](SensorManager.md))
- [#flush(SensorEventListener)](SensorManager.md)) 

### registerListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerListener(
    listener: SensorEventListener!, 
    sensor: Sensor!, 
    samplingPeriodUs: Int, 
    maxReportLatencyUs: Int, 
    handler: Handler!
): Boolean
```

Registers a [SensorEventListener](SensorEventListener.md) for the given sensor at the given sampling frequency and the given maximum reporting latency.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorEventListener](SensorEventListener.md)!:A [SensorEventListener](SensorEventListener.md) object that will receive the sensor events. If the application is interested in receiving flush complete notifications, it should register with [SensorEventListener2](SensorEventListener.md) instead. |
| `sensor` | [Sensor](Sensor.md)!:The [Sensor](Sensor.md) to register to. |
| `samplingPeriodUs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired delay between two consecutive events in microseconds. This is only a hint to the system. Events may be received faster or slower than the specified rate. Usually events are received faster. Can be one of [SENSOR_DELAY_NORMAL](SensorManager.md), [SENSOR_DELAY_UI](SensorManager.md), [SENSOR_DELAY_GAME](SensorManager.md), [SENSOR_DELAY_FASTEST](SensorManager.md) or the delay in microseconds. |
| --- | --- |
| `maxReportLatencyUs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum time in microseconds that events can be delayed before being reported to the application. A large value allows reducing the power consumption associated with the sensor. If maxReportLatencyUs is set to zero, events are delivered as soon as they are available, which is equivalent to calling [registerListener(android.hardware.SensorEventListener,android.hardware.Sensor,int)](SensorManager.md)). |
| `handler` | [Handler](../android.os/Handler.md)!:The [Handler](../android.os/Handler.md) the [sensor events](SensorEvent.md) will be delivered to. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the sensor is supported and successfully enabled. |

**See Also**

- [#registerListener(SensorEventListener, Sensor, int, int)](SensorManager.md)) 

### registerListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerListener(
    listener: SensorListener!, 
    sensors: Int
): Boolean
```

**Deprecated:** *This method is deprecated, use [SensorManager.registerListener(SensorEventListener, Sensor, int)](SensorManager.md))instead.*

Registers a listener for given sensors.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorListener](SensorListener.md)!:sensor listener object |
| `sensors` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit masks of the sensors to register to |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the sensor is supported and successfully enabled |

### registerListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerListener(
    listener: SensorListener!, 
    sensors: Int, 
    rate: Int
): Boolean
```

**Deprecated:** *This method is deprecated, use [SensorManager.registerListener(SensorEventListener, Sensor, int)](SensorManager.md))instead.*

Registers a SensorListener for given sensors.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorListener](SensorListener.md)!:sensor listener object |
| `sensors` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit masks of the sensors to register to |
| `rate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):rate of events. This is only a hint to the system. events may be received faster or slower than the specified rate. Usually events are received faster. The value must be one of [SENSOR_DELAY_NORMAL](SensorManager.md), [SENSOR_DELAY_UI](SensorManager.md), [SENSOR_DELAY_GAME](SensorManager.md), or [SENSOR_DELAY_FASTEST](SensorManager.md). |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the sensor is supported and successfully enabled |

### remapCoordinateSystem

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun remapCoordinateSystem(
    inR: FloatArray!, 
    X: Int, 
    Y: Int, 
    outR: FloatArray!
): Boolean
```

Rotates the supplied rotation matrix so it is expressed in a different coordinate system. This is typically used when an application needs to compute the three orientation angles of the device (see [getOrientation](SensorManager.md))) in a different coordinate system.

When the rotation matrix is used for drawing (for instance with OpenGL ES), it usually**doesn't need** to be transformed by this function, unless the screen is physically rotated, in which case you can use [Display.getRotation()](../android.view/Display.md))to retrieve the current rotation of the screen. Note that because the user is generally free to rotate their screen, you often should consider the rotation in deciding the parameters to use here.

Examples:

<br />

- Using the camera (Y axis along the camera's axis) for an augmented reality application where the rotation angles are needed:
`remapCoordinateSystem(inR, AXIS_X, AXIS_Z, outR);`
- Using the device as a mechanical compass when rotation is [Surface.ROTATION_90](../android.view/Surface.md):
`remapCoordinateSystem(inR, AXIS_Y, AXIS_MINUS_X, outR);`Beware of the above example. This call is needed only to account for a rotation from its natural orientation when calculating the rotation angles (see [getOrientation](SensorManager.md))). If the rotation matrix is also used for rendering, it may not need to be transformed, for instance if your [Activity](../android.app/Activity.md) is running in landscape mode.

Since the resulting coordinate system is orthonormal, only two axes need to be specified.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inR` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the rotation matrix to be transformed. Usually it is the matrix returned by [getRotationMatrix](SensorManager.md)). |
| `X` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):defines the axis of the new coordinate system that coincide with the X axis of the original coordinate system. |
| `Y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):defines the axis of the new coordinate system that coincide with the Y axis of the original coordinate system. |
| --- | --- |
| `outR` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the transformed rotation matrix. inR and outR should not be the same array. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`on success.`false`if the input parameters are incorrect, for instance if X and Y define the same axis. Or if inR and outR don't have the same length. |

**See Also**

- [#getRotationMatrix(float[], float[], float[], float[])](https://developer.android.com/reference/kotlin/android/hardware/SensorManager#getRotationMatrix(kotlin.FloatArray,%20kotlin.FloatArray,%20kotlin.FloatArray,%20kotlin.FloatArray)) 

### requestTriggerSensor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestTriggerSensor(
    listener: TriggerEventListener!, 
    sensor: Sensor!
): Boolean
```

Requests receiving trigger events for a trigger sensor.

When the sensor detects a trigger event condition, such as significant motion in the case of the [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md), the provided trigger listener will be invoked once and then its request to receive trigger events will be canceled. To continue receiving trigger events, the application must request to receive trigger events again.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [TriggerEventListener](TriggerEventListener.md)!:The listener on which the [TriggerEventListener.onTrigger(TriggerEvent)](TriggerEventListener.md))will be delivered. |
| `sensor` | [Sensor](Sensor.md)!:The sensor to be enabled. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the sensor was successfully enabled. |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | when sensor is null or not a trigger sensor. |

### unregisterDynamicSensorCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterDynamicSensorCallback(callback: SensorManager.DynamicSensorCallback!): Unit
```

Remove a [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) to stop sending dynamic sensor connection events to that callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [SensorManager.DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md)!:An object that implements the [DynamicSensorCallback](../android/hardware/SensorManager.DynamicSensorCallback.md) interface for receiving callbacks. |

### unregisterListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterListener(listener: SensorEventListener!): Unit
```

Unregisters a listener for all sensors.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorEventListener](SensorEventListener.md)!:a SensorListener object |

**See Also**

- [#unregisterListener(SensorEventListener, Sensor)](SensorManager.md))
- [#registerListener(SensorEventListener, Sensor, int)](SensorManager.md)) 

### unregisterListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterListener(
    listener: SensorEventListener!, 
    sensor: Sensor!
): Unit
```

Unregisters a listener for the sensors with which it is registered.

Note: Don't use this method with a one shot trigger sensor such as [Sensor.TYPE_SIGNIFICANT_MOTION](Sensor.md). Use [cancelTriggerSensor(android.hardware.TriggerEventListener,android.hardware.Sensor)](SensorManager.md))instead.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorEventListener](SensorEventListener.md)!:a SensorEventListener object |
| `sensor` | [Sensor](Sensor.md)!:the sensor to unregister from |

**See Also**

- [#unregisterListener(SensorEventListener)](SensorManager.md))
- [#registerListener(SensorEventListener, Sensor, int)](SensorManager.md)) 

### unregisterListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterListener(listener: SensorListener!): Unit
```

**Deprecated:** *This method is deprecated, use [SensorManager.unregisterListener(SensorEventListener)](SensorManager.md))instead.*

Unregisters a listener for all sensors.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorListener](SensorListener.md)!:a SensorListener object |

### unregisterListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterListener(
    listener: SensorListener!, 
    sensors: Int
): Unit
```

**Deprecated:** *This method is deprecated, use [SensorManager.unregisterListener(SensorEventListener, Sensor)](SensorManager.md))instead.*

Unregisters a listener for the sensors with which it is registered.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SensorListener](SensorListener.md)!:a SensorListener object |
| `sensors` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit masks of the sensors to unregister from |
