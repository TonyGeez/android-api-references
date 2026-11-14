# View.OnHoverListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnHoverListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnHoverListener "View this page in Java") 
| --- | --- |

```
interface OnHoverListener
```

| [android.view.View.OnHoverListener](https://developer.android.com/reference/kotlin/android/view/View.OnHoverListener#) |

Interface definition for a callback to be invoked when a hover event is dispatched to this view. The callback will be invoked before the hover event is given to the view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onHover](https://developer.android.com/reference/kotlin/android/view/View.OnHoverListener#onHover(android.view.View,%20android.view.MotionEvent))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!`)` Called when a hover event is dispatched to a view. |

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
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view the hover event has been dispatched to. |
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!:The MotionEvent object containing full information about the event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener has consumed the event, false otherwise. |
