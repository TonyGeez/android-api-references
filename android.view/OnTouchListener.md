# View.OnTouchListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTouchListener

Kotlin| [Java](../android/view/View.OnTouchListener.md) 
| --- | --- |

```
interface OnTouchListener
```

| [android.view.View.OnTouchListener](../android/view/View.OnTouchListener.md) |

| Known Direct Subclasses [ZoomButtonsController](../android/widget/ZoomButtonsController.md) |--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ZoomButtonsController](../android/widget/ZoomButtonsController.md) | The [ZoomButtonsController](../android/widget/ZoomButtonsController.md) handles showing and hiding the zoom controls and positioning it relative to an owner view. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when a touch event is dispatched to this view. The callback will be invoked before the touch event is given to the view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouch](../android/view/View.OnTouchListener.md))`(`v:` ` [View](../android/view/View.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` Called when a touch event is dispatched to a view. |

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
| `v` | [View](../android/view/View.md)!:The view the touch event has been dispatched to. |
| `event` | [MotionEvent](../android/view/MotionEvent.md)!:The MotionEvent object containing full information about the event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener has consumed the event, false otherwise. |
