# UiAutomation.OnAccessibilityEventListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAccessibilityEventListener

Kotlin| [Java](https://developer.android.com/reference/android/app/UiAutomation.OnAccessibilityEventListener "View this page in Java") 
| --- | --- |

```
interface OnAccessibilityEventListener
```

| [android.app.UiAutomation.OnAccessibilityEventListener](https://developer.android.com/reference/kotlin/android/app/UiAutomation.OnAccessibilityEventListener#) |

Listener for observing the [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#) stream.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAccessibilityEvent](https://developer.android.com/reference/kotlin/android/app/UiAutomation.OnAccessibilityEventListener#onAccessibilityEvent(android.view.accessibility.AccessibilityEvent))`(`event:` ` [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#)!`)` Callback for receiving an [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#). |

## Public methods

### onAccessibilityEvent

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAccessibilityEvent(event: AccessibilityEvent!): Unit
```

Callback for receiving an [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#).

**Note:** This method is**NOT**executed on the main test thread. The client is responsible for proper synchronization.

**Note:**It is responsibility of the client to recycle the received events to minimize object creation.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#)!:The received event. |
