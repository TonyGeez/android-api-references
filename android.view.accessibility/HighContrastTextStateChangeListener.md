# AccessibilityManager.HighContrastTextStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HighContrastTextStateChangeListener

Kotlin| [Java](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md) 
| --- | --- |

```
interface HighContrastTextStateChangeListener
```

| [android.view.accessibility.AccessibilityManager.HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md) |

Listener for the system high contrast text state. To listen for changes to the high contrast text state on the device, implement this interface and register it with the system by calling [addHighContrastTextStateChangeListener](AccessibilityManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHighContrastTextStateChanged](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the high contrast text enabled state changes. |

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
