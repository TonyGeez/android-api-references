# View.OnGenericMotionListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGenericMotionListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnGenericMotionListener "View this page in Java") 

```
interface OnGenericMotionListener
```

| [android.view.View.OnGenericMotionListener](https://developer.android.com/reference/kotlin/android/view/View.OnGenericMotionListener#) |

Interface definition for a callback to be invoked when a generic motion event is dispatched to this view. The callback will be invoked before the generic motion event is given to the view.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotion](https://developer.android.com/reference/kotlin/android/view/View.OnGenericMotionListener#onGenericMotion(android.view.View,%20android.view.MotionEvent))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!`)` Called when a generic motion event is dispatched to a view. |

## Public methods

### onGenericMotion

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGenericMotion(
    v: View!, 
    event: MotionEvent!
): Boolean
```

Called when a generic motion event is dispatched to a view. This allows listeners to get a chance to respond before the target view.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view the generic motion event has been dispatched to. |
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)!:The MotionEvent object containing full information about the event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener has consumed the event, false otherwise. |
