# UiAutomation.OnAccessibilityEventListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAccessibilityEventListener

Kotlin| [Java](../android/app/UiAutomation.OnAccessibilityEventListener.md) 
| --- | --- |

```
interface OnAccessibilityEventListener
```

| [android.app.UiAutomation.OnAccessibilityEventListener](../android/app/UiAutomation.OnAccessibilityEventListener.md) |

Listener for observing the [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) stream.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccessibilityEvent](../android/app/UiAutomation.OnAccessibilityEventListener.md))`(`event:` ` [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!`)` Callback for receiving an [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md). |

## Public methods

### onAccessibilityEvent

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccessibilityEvent(event: AccessibilityEvent!): Unit
```

Callback for receiving an [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md).

**Note:** This method is**NOT**executed on the main test thread. The client is responsible for proper synchronization.

**Note:**It is responsibility of the client to recycle the received events to minimize object creation.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!:The received event. |
