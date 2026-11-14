# AccessibilityManager.HighContrastTextStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HighContrastTextStateChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener "View this page in Java") 
| --- | --- |

```
interface HighContrastTextStateChangeListener
```

| [android.view.accessibility.AccessibilityManager.HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener#) |

Listener for the system high contrast text state. To listen for changes to the high contrast text state on the device, implement this interface and register it with the system by calling [addHighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addHighContrastTextStateChangeListener(java.util.concurrent.Executor,%20android.view.accessibility.AccessibilityManager.HighContrastTextStateChangeListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHighContrastTextStateChanged](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener#onHighContrastTextStateChanged(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the high contrast text enabled state changes. |

## Public methods

### onHighContrastTextStateChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onHighContrastTextStateChanged(enabled: Boolean): Unit
```

Called when the high contrast text enabled state changes.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether high contrast text is enabled. |
