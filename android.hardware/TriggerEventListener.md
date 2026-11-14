# TriggerEventListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TriggerEventListener

Kotlin| [Java](https://developer.android.com/reference/android/hardware/TriggerEventListener "View this page in Java") 

```
abstract class TriggerEventListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.TriggerEventListener](https://developer.android.com/reference/kotlin/android/hardware/TriggerEventListener#) |

This class is the listener used to handle Trigger Sensors. Trigger Sensors are sensors that trigger an event and are automatically disabled. [Sensor.TYPE_SIGNIFICANT_MOTION](https://developer.android.com/reference/kotlin/android/hardware/Sensor#TYPE_SIGNIFICANT_MOTION:kotlin.Int) is one such example.

[SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) lets you access the device's [sensors](https://developer.android.com/reference/kotlin/android/hardware/Sensor). Get an instance of [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) by calling [Context.getSystemService()](https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String))with the argument [android.content.Context#SENSOR_SERVICE](https://developer.android.com/reference/kotlin/android/content/Context.html#SENSOR_SERVICE:kotlin.String).

Here's an example setup for a TriggerEventListener: 

```kotlin
class TriggerListener extends TriggerEventListener {
      public void onTrigger(TriggerEvent event) {
           // Do Work.
 
      // As it is a one shot sensor, it will be canceled automatically.
      // SensorManager.requestTriggerSensor(this, mSigMotion); needs to
      // be called again, if needed.
      }
  }
  public class SensorActivity extends Activity {
      private final SensorManager mSensorManager;
      private final Sensor mSigMotion;
      private final TriggerEventListener mListener = new TriggerEventListener();
 
      public SensorActivity() {
          mSensorManager = (SensorManager)getSystemService(SENSOR_SERVICE);
          mSigMotion = mSensorManager.getDefaultSensor(Sensor.TYPE_SIGNIFICANT_MOTION);
      }
 
      protected void onResume() {
          super.onResume();
          mSensorManager.requestTriggerSensor(mListener, mSigMotion);
      }
 
      protected void onPause() {
          super.onPause();
          // Call disable to ensure that the trigger request has been canceled.
          mSensorManager.cancelTriggerSensor(mListener, mSigMotion);
      }
 
  }
  
```

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TriggerEventListener](https://developer.android.com/reference/kotlin/android/hardware/TriggerEventListener#TriggerEventListener())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrigger](https://developer.android.com/reference/kotlin/android/hardware/TriggerEventListener#onTrigger(android.hardware.TriggerEvent))`(`event:` ` [TriggerEvent](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent)!`)` The method that will be called when the sensor is triggered. |

## Public constructors

### TriggerEventListener

```
TriggerEventListener()
```

## Public methods

### onTrigger

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTrigger(event: TriggerEvent!): Unit
```

The method that will be called when the sensor is triggered. Override this method in your implementation of this class.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `event` | [TriggerEvent](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent)!:The details of the event. |
