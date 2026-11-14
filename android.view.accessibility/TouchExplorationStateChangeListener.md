# AccessibilityManager.TouchExplorationStateChangeListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TouchExplorationStateChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener "View this page in Java") 
| --- | --- |

```
interface TouchExplorationStateChangeListener
```

| [android.view.accessibility.AccessibilityManager.TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener#) |

Listener for the system touch exploration state. To listen for changes to the touch exploration state on the device, implement this interface and register it with the system by calling #addTouchExplorationStateChangeListener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTouchExplorationStateChanged](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener#onTouchExplorationStateChanged(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the touch exploration enabled state changes. |

## Public methods

### onTouchExplorationStateChanged

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTouchExplorationStateChanged(enabled: Boolean): Unit
```

Called when the touch exploration enabled state changes.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether touch exploration is enabled. |
