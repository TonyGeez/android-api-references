# Equalizer.OnParameterChangeListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnParameterChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/media/audiofx/Equalizer.OnParameterChangeListener "View this page in Java") 

```
interface OnParameterChangeListener
```

| [android.media.audiofx.Equalizer.OnParameterChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer.OnParameterChangeListener#) |

The OnParameterChangeListener interface defines a method called by the Equalizer when a parameter value has changed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onParameterChange](https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer.OnParameterChangeListener#onParameterChange(android.media.audiofx.Equalizer,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`effect:` ` [Equalizer](https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `param1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `param2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Method called when a parameter value has changed. |

## Public methods

### onParameterChange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onParameterChange(
    effect: Equalizer!, 
    status: Int, 
    param1: Int, 
    param2: Int, 
    value: Int
): Unit
```

Method called when a parameter value has changed. The method is called only if the parameter was changed by another application having the control of the same Equalizer engine.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [Equalizer](https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer)!:the Equalizer on which the interface is registered. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):status of the set parameter operation. |
| `param1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):ID of the modified parameter. See [PARAM_BAND_LEVEL](https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_BAND_LEVEL:kotlin.Int)... |
| `param2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):additional parameter qualifier (e.g the band for band level parameter). |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new parameter value. |
