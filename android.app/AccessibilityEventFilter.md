# UiAutomation.AccessibilityEventFilter

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityEventFilter

Kotlin| [Java](https://developer.android.com/reference/android/app/UiAutomation.AccessibilityEventFilter "View this page in Java") 

```
interface AccessibilityEventFilter
```

| [android.app.UiAutomation.AccessibilityEventFilter](https://developer.android.com/reference/kotlin/android/app/UiAutomation.AccessibilityEventFilter#) |

Listener for filtering accessibility events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [accept](https://developer.android.com/reference/kotlin/android/app/UiAutomation.AccessibilityEventFilter#accept(android.view.accessibility.AccessibilityEvent))`(`event:` ` [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#)!`)` Callback for determining whether an event is accepted or it is filtered out. |

## Public methods

### accept

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(event: AccessibilityEvent!): Boolean
```

Callback for determining whether an event is accepted or it is filtered out.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#)!:The event to process. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event is accepted, false to filter it out. |
