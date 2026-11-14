# TouchInteractionController.Callback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](https://developer.android.com/reference/android/accessibilityservice/TouchInteractionController.Callback "View this page in Java") 

```
interface Callback
```

| [android.accessibilityservice.TouchInteractionController.Callback](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController.Callback#) |

callbacks allow services to receive motion events and state change updates.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMotionEvent](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController.Callback#onMotionEvent(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)`)` Called when the framework has sent a motion event to the service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStateChanged](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController.Callback#onStateChanged(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the state of motion event dispatch for this display has changed. |

## Public methods

### onMotionEvent

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMotionEvent(event: MotionEvent): Unit
```

Called when the framework has sent a motion event to the service.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#):the event being passed to the service. This value cannot be`null`. |

### onStateChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStateChanged(state: Int): Unit
```

Called when the state of motion event dispatch for this display has changed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new state of motion event dispatch. Value is [android.accessibilityservice.TouchInteractionController#STATE_CLEAR](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_CLEAR:kotlin.Int), [android.accessibilityservice.TouchInteractionController#STATE_TOUCH_INTERACTING](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_TOUCH_INTERACTING:kotlin.Int), [android.accessibilityservice.TouchInteractionController#STATE_TOUCH_EXPLORING](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_TOUCH_EXPLORING:kotlin.Int), [android.accessibilityservice.TouchInteractionController#STATE_DRAGGING](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_DRAGGING:kotlin.Int), or [android.accessibilityservice.TouchInteractionController#STATE_DELEGATING](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_DELEGATING:kotlin.Int) |

**See Also**

- [android.accessibilityservice.TouchInteractionController#STATE_CLEAR](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_CLEAR:kotlin.Int)
- [android.accessibilityservice.TouchInteractionController#STATE_DELEGATING](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_DELEGATING:kotlin.Int)
- [android.accessibilityservice.TouchInteractionController#STATE_DRAGGING](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_DRAGGING:kotlin.Int)
- [android.accessibilityservice.TouchInteractionController#STATE_TOUCH_EXPLORING](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_TOUCH_EXPLORING:kotlin.Int)
