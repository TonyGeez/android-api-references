# AccessibilityManager.AccessibilityServicesStateChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityServicesStateChangeListener

Kotlin| [Java](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md) 
| --- | --- |

```
interface AccessibilityServicesStateChangeListener
```

| [android.view.accessibility.AccessibilityManager.AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md) |

Listener for changes to the state of accessibility services.

This refers to changes to [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md), including:

- Whenever a service is enabled or disabled, or its info has been set or removed.
- Whenever a metadata attribute of any running service's info changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccessibilityServicesStateChanged](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md))`(`manager:` ` [AccessibilityManager](AccessibilityManager.md)`)` Called when the state of accessibility services changes. |

## Public methods

### onAccessibilityServicesStateChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccessibilityServicesStateChanged(manager: AccessibilityManager): Unit
```

Called when the state of accessibility services changes.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `manager` | [AccessibilityManager](AccessibilityManager.md):The manager that is calling back This value cannot be`null`. |
