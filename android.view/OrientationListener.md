# OrientationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OrientationListener

Kotlin| [Java](../android/view/OrientationListener.md) 
| --- | --- |

```
abstract class OrientationListener : SensorListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.OrientationListener](../android/view/OrientationListener.md) |

| **This class was deprecated in API level 3.**
|
| use [android.view.OrientationEventListener](../android/view/OrientationEventListener.md) instead. This class internally uses the OrientationEventListener.

Helper class for receiving notifications from the SensorManager when the orientation of the device has changed.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_UNKNOWN](../android/view/OrientationListener.md) Returned from onOrientationChanged when the device orientation cannot be determined (typically when the device is in a close to flat position). |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OrientationListener](../android/view/OrientationListener.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Creates a new OrientationListener. |
| [OrientationListener](../android/view/OrientationListener.md))`(`context:` ` [Context](../android/content/Context.md)!`, `rate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new OrientationListener. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disable](../android/view/OrientationListener.md))`()` Disables the OrientationListener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enable](../android/view/OrientationListener.md))`()` Enables the OrientationListener so it will monitor the sensor and call [onOrientationChanged](../android/view/OrientationListener.md))when the device orientation changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](../android/view/OrientationListener.md))`(`sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOrientationChanged](../android/view/OrientationListener.md))`(`orientation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Look at [android.view.OrientationEventListener#onOrientationChanged](../android/view/OrientationEventListener.md))for method description and usage |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](../android/view/OrientationListener.md))`(`sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` <br /> |

## Constants

### ORIENTATION_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_UNKNOWN: Int
```

**Deprecated:** *Deprecated in Java.*

Returned from onOrientationChanged when the device orientation cannot be determined (typically when the device is in a close to flat position). 

 Value: -1

**See Also**

- [#onOrientationChanged](../android/view/OrientationListener.md))

## Public constructors

### OrientationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OrientationListener(context: Context!)
```

Creates a new OrientationListener.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:for the OrientationListener. |

### OrientationListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OrientationListener(
    context: Context!, 
    rate: Int)
```

Creates a new OrientationListener.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:for the OrientationListener. |
| `rate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):at which sensor events are processed (see also [SensorManager](../android/hardware/SensorManager.md)). Use the default value of [SENSOR_DELAY_NORMAL](../android/hardware/SensorManager.md) for simple screen orientation change detection. |

## Public methods

### disable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun disable(): Unit
```

**Deprecated:** *Deprecated in Java.*

Disables the OrientationListener. 

### enable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enable(): Unit
```

**Deprecated:** *Deprecated in Java.*

Enables the OrientationListener so it will monitor the sensor and call [onOrientationChanged](../android/view/OrientationListener.md))when the device orientation changes. 

### onAccuracyChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAccuracyChanged(
    sensor: Int, 
    accuracy: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `sensor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the sensor being monitored |
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new accuracy of this sensor. |

### onOrientationChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOrientationChanged(orientation: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Look at [android.view.OrientationEventListener#onOrientationChanged](../android/view/OrientationEventListener.md))for method description and usage

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------|
| `orientation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new orientation of the device. |

**See Also**

- [#ORIENTATION_UNKNOWN](../android/view/OrientationListener.md) 

### onSensorChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSensorChanged(
    sensor: Int, 
    values: FloatArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the sensor being monitored |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The new values for the sensor. |
