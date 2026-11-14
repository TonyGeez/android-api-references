# OrientationEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OrientationEventListener

Kotlin| [Java](https://developer.android.com/reference/android/view/OrientationEventListener "View this page in Java") 
| --- | --- |

```
abstract class OrientationEventListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.OrientationEventListener](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#) |

Helper class for receiving notifications from the SensorManager when the orientation of the device has changed.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#ORIENTATION_UNKNOWN:kotlin.Int) Returned from onOrientationChanged when the device orientation cannot be determined (typically when the device is in a close to flat position). |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OrientationEventListener](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#OrientationEventListener(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Creates a new OrientationEventListener. |
| [OrientationEventListener](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#OrientationEventListener(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `rate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new OrientationEventListener. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canDetectOrientation](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#canDetectOrientation())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disable](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#disable())`()` Disables the OrientationEventListener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enable](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#enable())`()` Enables the OrientationEventListener so it will monitor the sensor and call [onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#onOrientationChanged(kotlin.Int))when the device orientation changes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#onOrientationChanged(kotlin.Int))`(`orientation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the orientation of the device has changed. |

## Constants

### ORIENTATION_UNKNOWN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_UNKNOWN: Int
```

Returned from onOrientationChanged when the device orientation cannot be determined (typically when the device is in a close to flat position). 

 Value: -1

**See Also**

- [#onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#onOrientationChanged(kotlin.Int))

## Public constructors

### OrientationEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OrientationEventListener(context: Context!)
```

Creates a new OrientationEventListener.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:for the OrientationEventListener. |

### OrientationEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OrientationEventListener(
    context: Context!, 
    rate: Int)
```

Creates a new OrientationEventListener.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:for the OrientationEventListener. |
| `rate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):at which sensor events are processed (see also [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#)). Use the default value of [SENSOR_DELAY_NORMAL](https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#SENSOR_DELAY_NORMAL:kotlin.Int) for simple screen orientation change detection. |

## Public methods

### canDetectOrientation

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canDetectOrientation(): Boolean
```  

### disable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun disable(): Unit
```

Disables the OrientationEventListener. 

### enable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enable(): Unit
```

Enables the OrientationEventListener so it will monitor the sensor and call [onOrientationChanged](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#onOrientationChanged(kotlin.Int))when the device orientation changes. 

### onOrientationChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOrientationChanged(orientation: Int): Unit
```

Called when the orientation of the device has changed. orientation parameter is in degrees, ranging from 0 to 359. orientation is 0 degrees when the device is oriented in its natural position, 90 degrees when its left side is at the top, 180 degrees when it is upside down, and 270 degrees when its right side is to the top. [ORIENTATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#ORIENTATION_UNKNOWN:kotlin.Int) is returned when the device is close to flat and the orientation cannot be determined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------|
| `orientation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new orientation of the device. |

**See Also**

- [#ORIENTATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/OrientationEventListener#ORIENTATION_UNKNOWN:kotlin.Int)
