# AccessibilityManager.AccessibilityStateChangeListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityStateChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener "View this page in Java") 

```
interface AccessibilityStateChangeListener
```

| [android.view.accessibility.AccessibilityManager.AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener#) |

Listener for the system accessibility state. To listen for changes to the accessibility state on the device, implement this interface and register it with the system by calling #addAccessibilityStateChangeListener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccessibilityStateChanged](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener#onAccessibilityStateChanged(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the accessibility enabled state changes. |

## Public methods

### onAccessibilityStateChanged

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccessibilityStateChanged(enabled: Boolean): Unit
```

Called when the accessibility enabled state changes.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether accessibility is enabled. |
