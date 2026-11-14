# View.OnCapturedPointerListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCapturedPointerListener

Kotlin| [Java](../android/view/View.OnCapturedPointerListener.md) 
| --- | --- |

```
interface OnCapturedPointerListener
```

| [android.view.View.OnCapturedPointerListener](../android/view/View.OnCapturedPointerListener.md) |

Interface definition for a callback to be invoked when a captured pointer event is being dispatched this view. The callback will be invoked before the event is given to the view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCapturedPointer](../android/view/View.OnCapturedPointerListener.md))`(`view:` ` [View](../android/view/View.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` Called when a captured pointer event is dispatched to a view. |

## Public methods

### onCapturedPointer

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCapturedPointer(
    view: View!, 
    event: MotionEvent!
): Boolean
```

Called when a captured pointer event is dispatched to a view.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The view this event has been dispatched to. |
| `event` | [MotionEvent](../android/view/MotionEvent.md)!:The captured event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener has consumed the event, false otherwise. |
