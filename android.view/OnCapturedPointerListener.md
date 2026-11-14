# View.OnCapturedPointerListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCapturedPointerListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnCapturedPointerListener "View this page in Java") 
| --- | --- |

```
interface OnCapturedPointerListener
```

| [android.view.View.OnCapturedPointerListener](https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener#) |

Interface definition for a callback to be invoked when a captured pointer event is being dispatched this view. The callback will be invoked before the event is given to the view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCapturedPointer](https://developer.android.com/reference/kotlin/android/view/View.OnCapturedPointerListener#onCapturedPointer(android.view.View,%20android.view.MotionEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!`)` Called when a captured pointer event is dispatched to a view. |

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
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view this event has been dispatched to. |
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!:The captured event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener has consumed the event, false otherwise. |
