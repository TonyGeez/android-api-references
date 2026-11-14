# GestureDetector.OnDoubleTapListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDoubleTapListener

Kotlin| [Java](../android/view/GestureDetector.OnDoubleTapListener.md) 
| --- | --- |

```
interface OnDoubleTapListener
```

| [android.view.GestureDetector.OnDoubleTapListener](../android/view/GestureDetector.OnDoubleTapListener.md) |

| Known Direct Subclasses [GestureDetector.SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [GestureDetector.SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md) | A convenience class to extend when you only want to listen for a subset of all the gestures. | |
| --- | --- | --- | --- | --- | --- | --- |

The listener that is used to notify when a double-tap or a confirmed single-tap occur.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onDoubleTap](../android/view/GestureDetector.OnDoubleTapListener.md))`(`e:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Notified when a double-tap occurs. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onDoubleTapEvent](../android/view/GestureDetector.OnDoubleTapListener.md))`(`e:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Notified when an event within a double-tap gesture occurs, including the down, move, and up events. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSingleTapConfirmed](../android/view/GestureDetector.OnDoubleTapListener.md))`(`e:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Notified when a single-tap occurs. |
| --- | --- |

## Public methods

### onDoubleTap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDoubleTap(e: MotionEvent): Boolean
```

Notified when a double-tap occurs. Triggered on the down event of second tap.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](../android/view/MotionEvent.md):The down motion event of the first tap of the double-tap. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |

### onDoubleTapEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDoubleTapEvent(e: MotionEvent): Boolean
```

Notified when an event within a double-tap gesture occurs, including the down, move, and up events.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](../android/view/MotionEvent.md):The motion event that occurred during the double-tap gesture. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |

### onSingleTapConfirmed

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSingleTapConfirmed(e: MotionEvent): Boolean
```

Notified when a single-tap occurs.

Unlike [OnGestureListener.onSingleTapUp(MotionEvent)](../android/view/GestureDetector.OnGestureListener.md)), this will only be called after the detector is confident that the user's first tap is not followed by a second tap leading to a double-tap gesture.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](../android/view/MotionEvent.md):The down motion event of the single-tap. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |
