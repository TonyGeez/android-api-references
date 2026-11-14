# UiModeManager.ContrastChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContrastChangeListener

Kotlin| [Java](../android/app/UiModeManager.ContrastChangeListener.md) 
| --- | --- |

```
interface ContrastChangeListener
```

| [android.app.UiModeManager.ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md) |

Listener for the UI contrast. To listen for changes to the UI contrast on the device, implement this interface and register it with the system by calling [addContrastChangeListener](UiModeManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContrastChanged](../android/app/UiModeManager.ContrastChangeListener.md))`(`contrast:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Called when the color contrast enabled state changes. |

## Public methods

### onContrastChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onContrastChanged(contrast: Float): Unit
```

Called when the color contrast enabled state changes.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `contrast` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The color contrast as in [getContrast](UiModeManager.md))Value is between -1.0f and 1.0f inclusive |
