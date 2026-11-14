# OrientationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OrientationListener

Kotlin| [Java](https://developer.android.com/reference/android/view/OrientationListener "View this page in Java") 
| --- | --- |

```
abstract class OrientationListener : SensorListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.OrientationListener](https://developer.android.com/reference/kotlin/android/view/OrientationListener#) |

| **This class was deprecated in API level 3.**
|
| use [android.view.OrientationEventListener](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener) instead. This class internally uses the OrientationEventListener.

Helper class for receiving notifications from the SensorManager when the orientation of the device has changed.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/OrientationListener#ORIENTATION_UNKNOWN:kotlin.Int) Returned from onOrientationChanged when the device orientation cannot be determined (typically when the device is in a close to flat position). |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OrientationListener](https://developer.android.com/reference/kotlin/android/view/OrientationListener#OrientationListener(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Creates a new OrientationListener. |
| [OrientationListener](https://developer.android.com/reference/kotlin/android/view/OrientationListener#OrientationListener(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `rate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new OrientationListener. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disable](https://developer.android.com/reference/kotlin/android/view/OrientationListener#disable())`()` Disables the OrientationListener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enable](https://developer.android.com/reference/kotlin/android/view/OrientationListener#enable())`()` Enables the OrientationListener so it will monitor the sensor and call [onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationListener#onOrientationChanged(kotlin.Int))when the device orientation changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccuracyChanged](https://developer.android.com/reference/kotlin/android/view/OrientationListener#onAccuracyChanged(kotlin.Int,%20kotlin.Int))`(`sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationListener#onOrientationChanged(kotlin.Int))`(`orientation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Look at [android.view.OrientationEventListener#onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#onOrientationChanged(kotlin.Int))for method description and usage |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSensorChanged](https://developer.android.com/reference/kotlin/android/view/OrientationListener#onSensorChanged(kotlin.Int,%20kotlin.FloatArray))`(`sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` <br /> |

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

- [#onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationListener#onOrientationChanged(kotlin.Int))

## Public constructors

### OrientationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OrientationListener(context: Context!)
```

Creates a new OrientationListener.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:for the OrientationListener. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:for the OrientationListener. |
| `rate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):at which sensor events are processed (see also [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#)). Use the default value of [SENSOR_DELAY_NORMAL](https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#SENSOR_DELAY_NORMAL:kotlin.Int) for simple screen orientation change detection. |

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

Enables the OrientationListener so it will monitor the sensor and call [onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationListener#onOrientationChanged(kotlin.Int))when the device orientation changes. 

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

Look at [android.view.OrientationEventListener#onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#onOrientationChanged(kotlin.Int))for method description and usage

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------|
| `orientation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new orientation of the device. |

**See Also**

- [#ORIENTATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/OrientationListener#ORIENTATION_UNKNOWN:kotlin.Int) 

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
