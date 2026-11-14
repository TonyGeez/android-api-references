# UiModeManager.ContrastChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContrastChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/app/UiModeManager.ContrastChangeListener "View this page in Java") 
| --- | --- |

```
interface ContrastChangeListener
```

| [android.app.UiModeManager.ContrastChangeListener](https://developer.android.com/reference/kotlin/android/app/UiModeManager.ContrastChangeListener#) |

Listener for the UI contrast. To listen for changes to the UI contrast on the device, implement this interface and register it with the system by calling [addContrastChangeListener](https://developer.android.com/reference/kotlin/android/app/UiModeManager#addContrastChangeListener(java.util.concurrent.Executor,%20android.app.UiModeManager.ContrastChangeListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onContrastChanged](https://developer.android.com/reference/kotlin/android/app/UiModeManager.ContrastChangeListener#onContrastChanged(kotlin.Float))`(`contrast:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Called when the color contrast enabled state changes. |

## Public methods

### onContrastChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onContrastChanged(contrast: Float): Unit
```

Called when the color contrast enabled state changes.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `contrast` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The color contrast as in [getContrast](https://developer.android.com/reference/kotlin/android/app/UiModeManager#getContrast())Value is between -1.0f and 1.0f inclusive |
