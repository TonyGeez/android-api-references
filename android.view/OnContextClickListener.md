# GestureDetector.OnContextClickListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnContextClickListener

Kotlin| [Java](https://developer.android.com/reference/android/view/GestureDetector.OnContextClickListener "View this page in Java") 
| --- | --- |

```
interface OnContextClickListener
```

| [android.view.GestureDetector.OnContextClickListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener#) |

| Known Direct Subclasses [GestureDetector.SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [GestureDetector.SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener) | A convenience class to extend when you only want to listen for a subset of all the gestures. | |
| --- | --- | --- | --- | --- | --- | --- |

The listener that is used to notify when a context click occurs. When listening for a context click ensure that you call [onGenericMotionEvent(android.view.MotionEvent)](https://developer.android.com/reference/kotlin/android/view/GestureDetector#onGenericMotionEvent(android.view.MotionEvent))in [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onContextClick](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener#onContextClick(android.view.MotionEvent))`(`e:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Notified when a context click occurs. |

## Public methods

### onContextClick

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onContextClick(e: MotionEvent): Boolean
```

Notified when a context click occurs.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The motion event that occurred during the context click. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |
