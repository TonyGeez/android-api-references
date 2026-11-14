# TouchInteractionController.Callback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](../android/accessibilityservice/TouchInteractionController.Callback.md) 
| --- | --- |

```
interface Callback
```

| [android.accessibilityservice.TouchInteractionController.Callback](../android/accessibilityservice/TouchInteractionController.Callback.md) |

callbacks allow services to receive motion events and state change updates.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMotionEvent](../android/accessibilityservice/TouchInteractionController.Callback.md))`(`event:` ` [MotionEvent](../android.view/MotionEvent.md)`)` Called when the framework has sent a motion event to the service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStateChanged](../android/accessibilityservice/TouchInteractionController.Callback.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the state of motion event dispatch for this display has changed. |

## Public methods

### onMotionEvent

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMotionEvent(event: MotionEvent): Unit
```

Called when the framework has sent a motion event to the service.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](../android.view/MotionEvent.md):the event being passed to the service. This value cannot be`null`. |

### onStateChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStateChanged(state: Int): Unit
```

Called when the state of motion event dispatch for this display has changed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new state of motion event dispatch. Value is [android.accessibilityservice.TouchInteractionController#STATE_CLEAR](TouchInteractionController.md), [android.accessibilityservice.TouchInteractionController#STATE_TOUCH_INTERACTING](TouchInteractionController.md), [android.accessibilityservice.TouchInteractionController#STATE_TOUCH_EXPLORING](TouchInteractionController.md), [android.accessibilityservice.TouchInteractionController#STATE_DRAGGING](TouchInteractionController.md), or [android.accessibilityservice.TouchInteractionController#STATE_DELEGATING](TouchInteractionController.md) |

**See Also**

- [android.accessibilityservice.TouchInteractionController#STATE_CLEAR](TouchInteractionController.md)
- [android.accessibilityservice.TouchInteractionController#STATE_DELEGATING](TouchInteractionController.md)
- [android.accessibilityservice.TouchInteractionController#STATE_DRAGGING](TouchInteractionController.md)
- [android.accessibilityservice.TouchInteractionController#STATE_TOUCH_EXPLORING](TouchInteractionController.md)
