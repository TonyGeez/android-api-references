# GestureDetector.OnDoubleTapListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDoubleTapListener

Kotlin| [Java](https://developer.android.com/reference/android/view/GestureDetector.OnDoubleTapListener "View this page in Java") 
| --- | --- |

```
interface OnDoubleTapListener
```

| [android.view.GestureDetector.OnDoubleTapListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener#) |

| Known Direct Subclasses [GestureDetector.SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [GestureDetector.SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener) | A convenience class to extend when you only want to listen for a subset of all the gestures. | |
| --- | --- | --- | --- | --- | --- | --- |

The listener that is used to notify when a double-tap or a confirmed single-tap occur.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onDoubleTap](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener#onDoubleTap(android.view.MotionEvent))`(`e:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Notified when a double-tap occurs. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onDoubleTapEvent](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener#onDoubleTapEvent(android.view.MotionEvent))`(`e:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Notified when an event within a double-tap gesture occurs, including the down, move, and up events. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSingleTapConfirmed](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener#onSingleTapConfirmed(android.view.MotionEvent))`(`e:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Notified when a single-tap occurs. |
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
| `e` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The down motion event of the first tap of the double-tap. This value cannot be`null`. |

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
| `e` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The motion event that occurred during the double-tap gesture. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |

### onSingleTapConfirmed

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSingleTapConfirmed(e: MotionEvent): Boolean
```

Notified when a single-tap occurs.

Unlike [OnGestureListener.onSingleTapUp(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener#onSingleTapUp(android.view.MotionEvent)), this will only be called after the detector is confident that the user's first tap is not followed by a second tap leading to a double-tap gesture.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The down motion event of the single-tap. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |
