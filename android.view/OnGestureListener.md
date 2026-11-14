# GestureDetector.OnGestureListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGestureListener

Kotlin| [Java](https://developer.android.com/reference/android/view/GestureDetector.OnGestureListener "View this page in Java") 

```
interface OnGestureListener
```

| [android.view.GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener#) |

| Known Direct Subclasses [Gallery](https://developer.android.com/reference/kotlin/android/widget/Gallery.html#), [GestureDetector.SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [Gallery](https://developer.android.com/reference/kotlin/android/widget/Gallery.html#) | A view that shows items in a center-locked, horizontally scrolling list. | | [GestureDetector.SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener) | A convenience class to extend when you only want to listen for a subset of all the gestures. | |

The listener that is used to notify when gestures occur. If you want to listen for all the different gestures then implement this interface. If you only want to listen for a subset it might be easier to extend [SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onDown](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener#onDown(android.view.MotionEvent))`(`e:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Notified when a tap occurs with the down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) that triggered it. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onFling](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener#onFling(android.view.MotionEvent,%20android.view.MotionEvent,%20kotlin.Float,%20kotlin.Float))`(`e1:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)?`, `e2:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`, `velocityX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `velocityY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Notified of a fling event when it occurs with the initial on down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) and the matching up [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLongPress](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener#onLongPress(android.view.MotionEvent))`(`e:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Notified when a long press occurs with the initial on down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) that trigged it. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onScroll](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener#onScroll(android.view.MotionEvent,%20android.view.MotionEvent,%20kotlin.Float,%20kotlin.Float))`(`e1:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)?`, `e2:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`, `distanceX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `distanceY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Notified when a scroll occurs with the initial on down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) and the current move [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onShowPress](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener#onShowPress(android.view.MotionEvent))`(`e:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` The user has performed a down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) and not performed a move or up yet. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSingleTapUp](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener#onSingleTapUp(android.view.MotionEvent))`(`e:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Notified when a tap occurs with the up [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) that triggered it. |

## Public methods

### onDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDown(e: MotionEvent): Boolean
```

Notified when a tap occurs with the down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) that triggered it. This will be triggered immediately for every down event. All other events should be preceded by this.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The down motion event. This value cannot be`null`. |

### onFling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFling(
    e1: MotionEvent?, 
    e2: MotionEvent, 
    velocityX: Float, 
    velocityY: Float
): Boolean
```

Notified of a fling event when it occurs with the initial on down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) and the matching up [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent). The calculated velocity is supplied along the x and y axis in pixels per second.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e1` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)?:The first down motion event that started the fling. A`null`event indicates an incomplete event stream or error state. |
| `e2` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The move motion event that triggered the current onFling. This value cannot be`null`. |
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The velocity of this fling measured in pixels per second along the x axis. |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The velocity of this fling measured in pixels per second along the y axis. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |

### onLongPress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLongPress(e: MotionEvent): Unit
```

Notified when a long press occurs with the initial on down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) that trigged it.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The initial on down motion event that started the longpress. This value cannot be`null`. |

### onScroll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScroll(
    e1: MotionEvent?, 
    e2: MotionEvent, 
    distanceX: Float, 
    distanceY: Float
): Boolean
```

Notified when a scroll occurs with the initial on down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) and the current move [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent). The distance in x and y is also supplied for convenience.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e1` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)?:The first down motion event that started the scrolling. A`null`event indicates an incomplete event stream or error state. |
| `e2` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The move motion event that triggered the current onScroll. This value cannot be`null`. |
| `distanceX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance along the X axis that has been scrolled since the last call to onScroll. This is NOT the distance between`e1`and`e2`. |
| `distanceY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance along the Y axis that has been scrolled since the last call to onScroll. This is NOT the distance between`e1`and`e2`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |

### onShowPress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onShowPress(e: MotionEvent): Unit
```

The user has performed a down [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) and not performed a move or up yet. This event is commonly used to provide visual feedback to the user to let them know that their action has been recognized i.e. highlight an element.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The down motion event This value cannot be`null`. |

### onSingleTapUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSingleTapUp(e: MotionEvent): Boolean
```

Notified when a tap occurs with the up [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) that triggered it.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The up motion event that completed the first tap This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |
