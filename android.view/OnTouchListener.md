# View.OnTouchListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTouchListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnTouchListener "View this page in Java") 
| --- | --- |

```
interface OnTouchListener
```

| [android.view.View.OnTouchListener](https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener#) |

| Known Direct Subclasses [ZoomButtonsController](https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.html#) |--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ZoomButtonsController](https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.html#) | The [ZoomButtonsController](https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.html#) handles showing and hiding the zoom controls and positioning it relative to an owner view. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when a touch event is dispatched to this view. The callback will be invoked before the touch event is given to the view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouch](https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener#onTouch(android.view.View,%20android.view.MotionEvent))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!`)` Called when a touch event is dispatched to a view. |

## Public methods

### onTouch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTouch(
    v: View!, 
    event: MotionEvent!
): Boolean
```

Called when a touch event is dispatched to a view. This allows listeners to get a chance to respond before the target view.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view the touch event has been dispatched to. |
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!:The MotionEvent object containing full information about the event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener has consumed the event, false otherwise. |
