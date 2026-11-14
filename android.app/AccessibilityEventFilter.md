# UiAutomation.AccessibilityEventFilter

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityEventFilter

Kotlin| [Java](../android/app/UiAutomation.AccessibilityEventFilter.md) 
| --- | --- |

```
interface AccessibilityEventFilter
```

| [android.app.UiAutomation.AccessibilityEventFilter](../android/app/UiAutomation.AccessibilityEventFilter.md) |

Listener for filtering accessibility events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [accept](../android/app/UiAutomation.AccessibilityEventFilter.md))`(`event:` ` [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!`)` Callback for determining whether an event is accepted or it is filtered out. |

## Public methods

### accept

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(event: AccessibilityEvent!): Boolean
```

Callback for determining whether an event is accepted or it is filtered out.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!:The event to process. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event is accepted, false to filter it out. |
