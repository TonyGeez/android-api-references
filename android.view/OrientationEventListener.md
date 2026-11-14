# OrientationEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OrientationEventListener

Kotlin| [Java](../android/view/OrientationEventListener.md) 
| --- | --- |

```
abstract class OrientationEventListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.OrientationEventListener](../android/view/OrientationEventListener.md) |

Helper class for receiving notifications from the SensorManager when the orientation of the device has changed.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_UNKNOWN](../android/view/OrientationEventListener.md) Returned from onOrientationChanged when the device orientation cannot be determined (typically when the device is in a close to flat position). |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OrientationEventListener](../android/view/OrientationEventListener.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Creates a new OrientationEventListener. |
| [OrientationEventListener](../android/view/OrientationEventListener.md))`(`context:` ` [Context](../android/content/Context.md)!`, `rate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new OrientationEventListener. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canDetectOrientation](../android/view/OrientationEventListener.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disable](../android/view/OrientationEventListener.md))`()` Disables the OrientationEventListener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enable](../android/view/OrientationEventListener.md))`()` Enables the OrientationEventListener so it will monitor the sensor and call [onOrientationChanged](../android/view/OrientationEventListener.md))when the device orientation changes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOrientationChanged](../android/view/OrientationEventListener.md))`(`orientation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the orientation of the device has changed. |

## Constants

### ORIENTATION_UNKNOWN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_UNKNOWN: Int
```

Returned from onOrientationChanged when the device orientation cannot be determined (typically when the device is in a close to flat position). 

 Value: -1

**See Also**

- [#onOrientationChanged](../android/view/OrientationEventListener.md))

## Public constructors

### OrientationEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OrientationEventListener(context: Context!)
```

Creates a new OrientationEventListener.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:for the OrientationEventListener. |

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
| `context` | [Context](../android/content/Context.md)!:for the OrientationEventListener. |
| `rate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):at which sensor events are processed (see also [SensorManager](../android/hardware/SensorManager.md)). Use the default value of [SENSOR_DELAY_NORMAL](../android/hardware/SensorManager.md) for simple screen orientation change detection. |

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

Enables the OrientationEventListener so it will monitor the sensor and call [onOrientationChanged](../android/view/OrientationEventListener.md))when the device orientation changes. 

### onOrientationChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onOrientationChanged(orientation: Int): Unit
```

Called when the orientation of the device has changed. orientation parameter is in degrees, ranging from 0 to 359. orientation is 0 degrees when the device is oriented in its natural position, 90 degrees when its left side is at the top, 180 degrees when it is upside down, and 270 degrees when its right side is to the top. [ORIENTATION_UNKNOWN](../android/view/OrientationEventListener.md) is returned when the device is close to flat and the orientation cannot be determined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------|
| `orientation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new orientation of the device. |

**See Also**

- [#ORIENTATION_UNKNOWN](../android/view/OrientationEventListener.md)
