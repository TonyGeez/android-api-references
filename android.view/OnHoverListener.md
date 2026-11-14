# View.OnHoverListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnHoverListener

Kotlin| [Java](../android/view/View.OnHoverListener.md) 
| --- | --- |

```
interface OnHoverListener
```

| [android.view.View.OnHoverListener](../android/view/View.OnHoverListener.md) |

Interface definition for a callback to be invoked when a hover event is dispatched to this view. The callback will be invoked before the hover event is given to the view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onHover](../android/view/View.OnHoverListener.md))`(`v:` ` [View](View.md)!`, `event:` ` [MotionEvent](MotionEvent.md)!`)` Called when a hover event is dispatched to a view. |

## Public methods

### onHover

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onHover(
    v: View!, 
    event: MotionEvent!
): Boolean
```

Called when a hover event is dispatched to a view. This allows listeners to get a chance to respond before the target view.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](View.md)!:The view the hover event has been dispatched to. |
| `event` | [MotionEvent](MotionEvent.md)!:The MotionEvent object containing full information about the event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener has consumed the event, false otherwise. |
