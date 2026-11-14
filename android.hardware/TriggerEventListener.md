# TriggerEventListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TriggerEventListener

Kotlin| [Java](../android/hardware/TriggerEventListener.md) 
| --- | --- |

```
abstract class TriggerEventListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.TriggerEventListener](../android/hardware/TriggerEventListener.md) |

This class is the listener used to handle Trigger Sensors. Trigger Sensors are sensors that trigger an event and are automatically disabled. [Sensor.TYPE_SIGNIFICANT_MOTION](../android/hardware/Sensor.md) is one such example.

[SensorManager](../android/hardware/SensorManager.md) lets you access the device's [sensors](../android/hardware/Sensor.md). Get an instance of [SensorManager](../android/hardware/SensorManager.md) by calling [Context.getSystemService()](../android/content/Context.md))with the argument [android.content.Context#SENSOR_SERVICE](../android/content/Context.md).

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
| [TriggerEventListener](../android/hardware/TriggerEventListener.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrigger](../android/hardware/TriggerEventListener.md))`(`event:` ` [TriggerEvent](../android/hardware/TriggerEvent.md)!`)` The method that will be called when the sensor is triggered. |

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
| `event` | [TriggerEvent](../android/hardware/TriggerEvent.md)!:The details of the event. |
