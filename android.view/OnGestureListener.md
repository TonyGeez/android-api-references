# GestureDetector.OnGestureListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGestureListener

Kotlin| [Java](../android/view/GestureDetector.OnGestureListener.md) 
| --- | --- |

```
interface OnGestureListener
```

| [android.view.GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) |

| Known Direct Subclasses [Gallery](../android/widget/Gallery.md), [GestureDetector.SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [Gallery](../android/widget/Gallery.md) | A view that shows items in a center-locked, horizontally scrolling list. | | [GestureDetector.SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md) | A convenience class to extend when you only want to listen for a subset of all the gestures. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The listener that is used to notify when gestures occur. If you want to listen for all the different gestures then implement this interface. If you only want to listen for a subset it might be easier to extend [SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onDown](../android/view/GestureDetector.OnGestureListener.md))`(`e:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Notified when a tap occurs with the down [MotionEvent](../android/view/MotionEvent.md) that triggered it. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onFling](../android/view/GestureDetector.OnGestureListener.md))`(`e1:` ` [MotionEvent](../android/view/MotionEvent.md)?`, `e2:` ` [MotionEvent](../android/view/MotionEvent.md)`, `velocityX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `velocityY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Notified of a fling event when it occurs with the initial on down [MotionEvent](../android/view/MotionEvent.md) and the matching up [MotionEvent](../android/view/MotionEvent.md). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLongPress](../android/view/GestureDetector.OnGestureListener.md))`(`e:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Notified when a long press occurs with the initial on down [MotionEvent](../android/view/MotionEvent.md) that trigged it. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onScroll](../android/view/GestureDetector.OnGestureListener.md))`(`e1:` ` [MotionEvent](../android/view/MotionEvent.md)?`, `e2:` ` [MotionEvent](../android/view/MotionEvent.md)`, `distanceX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `distanceY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Notified when a scroll occurs with the initial on down [MotionEvent](../android/view/MotionEvent.md) and the current move [MotionEvent](../android/view/MotionEvent.md). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onShowPress](../android/view/GestureDetector.OnGestureListener.md))`(`e:` ` [MotionEvent](../android/view/MotionEvent.md)`)` The user has performed a down [MotionEvent](../android/view/MotionEvent.md) and not performed a move or up yet. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onSingleTapUp](../android/view/GestureDetector.OnGestureListener.md))`(`e:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Notified when a tap occurs with the up [MotionEvent](../android/view/MotionEvent.md) that triggered it. |
| --- | --- |

## Public methods

### onDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDown(e: MotionEvent): Boolean
```

Notified when a tap occurs with the down [MotionEvent](../android/view/MotionEvent.md) that triggered it. This will be triggered immediately for every down event. All other events should be preceded by this.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](../android/view/MotionEvent.md):The down motion event. This value cannot be`null`. |

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

Notified of a fling event when it occurs with the initial on down [MotionEvent](../android/view/MotionEvent.md) and the matching up [MotionEvent](../android/view/MotionEvent.md). The calculated velocity is supplied along the x and y axis in pixels per second.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e1` | [MotionEvent](../android/view/MotionEvent.md)?:The first down motion event that started the fling. A`null`event indicates an incomplete event stream or error state. |
| `e2` | [MotionEvent](../android/view/MotionEvent.md):The move motion event that triggered the current onFling. This value cannot be`null`. |
| `velocityX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The velocity of this fling measured in pixels per second along the x axis. |
| --- | --- |
| `velocityY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The velocity of this fling measured in pixels per second along the y axis. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |

### onLongPress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLongPress(e: MotionEvent): Unit
```

Notified when a long press occurs with the initial on down [MotionEvent](../android/view/MotionEvent.md) that trigged it.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](../android/view/MotionEvent.md):The initial on down motion event that started the longpress. This value cannot be`null`. |

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

Notified when a scroll occurs with the initial on down [MotionEvent](../android/view/MotionEvent.md) and the current move [MotionEvent](../android/view/MotionEvent.md). The distance in x and y is also supplied for convenience.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e1` | [MotionEvent](../android/view/MotionEvent.md)?:The first down motion event that started the scrolling. A`null`event indicates an incomplete event stream or error state. |
| `e2` | [MotionEvent](../android/view/MotionEvent.md):The move motion event that triggered the current onScroll. This value cannot be`null`. |
| `distanceX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance along the X axis that has been scrolled since the last call to onScroll. This is NOT the distance between`e1`and`e2`. |
| --- | --- |
| `distanceY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance along the Y axis that has been scrolled since the last call to onScroll. This is NOT the distance between`e1`and`e2`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |

### onShowPress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onShowPress(e: MotionEvent): Unit
```

The user has performed a down [MotionEvent](../android/view/MotionEvent.md) and not performed a move or up yet. This event is commonly used to provide visual feedback to the user to let them know that their action has been recognized i.e. highlight an element.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](../android/view/MotionEvent.md):The down motion event This value cannot be`null`. |

### onSingleTapUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSingleTapUp(e: MotionEvent): Boolean
```

Notified when a tap occurs with the up [MotionEvent](../android/view/MotionEvent.md) that triggered it.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [MotionEvent](../android/view/MotionEvent.md):The up motion event that completed the first tap This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event is consumed, else false |
