# GestureDetector.OnContextClickListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnContextClickListener

Kotlin| [Java](../android/view/GestureDetector.OnContextClickListener.md) 
| --- | --- |

```
interface OnContextClickListener
```

| [android.view.GestureDetector.OnContextClickListener](../android/view/GestureDetector.OnContextClickListener.md) |

| Known Direct Subclasses [GestureDetector.SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [GestureDetector.SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md) | A convenience class to extend when you only want to listen for a subset of all the gestures. | |
| --- | --- | --- | --- | --- | --- | --- |

The listener that is used to notify when a context click occurs. When listening for a context click ensure that you call [onGenericMotionEvent(android.view.MotionEvent)](GestureDetector.md))in [View.onGenericMotionEvent(MotionEvent)](View.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onContextClick](../android/view/GestureDetector.OnContextClickListener.md))`(`e:` ` [MotionEvent](MotionEvent.md)`)` Notified when a context click occurs. |

## Public methods

### onContextClick

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onContextClick(e: MotionEvent): Boolean
```

Notified when a context click occurs.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](MotionEvent.md):The motion event that occurred during the context click. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |
