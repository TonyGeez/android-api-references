# AccessibilityManager.AccessibilityServicesStateChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityServicesStateChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener "View this page in Java") 
| --- | --- |

```
interface AccessibilityServicesStateChangeListener
```

| [android.view.accessibility.AccessibilityManager.AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener#) |

Listener for changes to the state of accessibility services.

This refers to changes to [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#), including:

- Whenever a service is enabled or disabled, or its info has been set or removed.
- Whenever a metadata attribute of any running service's info changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccessibilityServicesStateChanged](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener#onAccessibilityServicesStateChanged(android.view.accessibility.AccessibilityManager))`(`manager:` ` [AccessibilityManager](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager)`)` Called when the state of accessibility services changes. |

## Public methods

### onAccessibilityServicesStateChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccessibilityServicesStateChanged(manager: AccessibilityManager): Unit
```

Called when the state of accessibility services changes.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `manager` | [AccessibilityManager](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager):The manager that is calling back This value cannot be`null`. |
