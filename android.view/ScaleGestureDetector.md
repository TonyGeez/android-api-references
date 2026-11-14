Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScaleGestureDetector

Kotlin | [Java](ScaleGestureDetector.md)
| --- | --- |

```
open class ScaleGestureDetector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ScaleGestureDetector](ScaleGestureDetector.md) |

Detects scaling transformation gestures using the supplied MotionEvents. The `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` callback will notify users when a particular gesture event has occurred. This class should only be used with MotionEvents reported via touch. To use this class:

- Create an instance of the `ScaleGestureDetector` for your View
- In the onTouchEvent method ensure you call onTouchEvent. The methods defined in your callback will be executed when the events occur.

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` The listener for receiving notifications when gestures occur. |
| open | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.SimpleOnScaleGestureListener` A convenience class to extend when you only want to listen for a subset of scaling-related events. |

| Public constructors ||
|---|---|
| ScaleGestureDetector Creates a ScaleGestureDetector with the supplied listener. |
| ScaleGestureDetector Creates a ScaleGestureDetector with the supplied listener. |

| Public methods ||
|---|---|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getCurrentSpan Return the average distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getCurrentSpanX Return the average X distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getCurrentSpanY Return the average Y distance between each of the pointers forming the gesture in progress through the focal point. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getEventTime Return the event time of the current event being processed. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getFocusX Get the X coordinate of the current gesture's focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getFocusY Get the Y coordinate of the current gesture's focal point. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getPreviousSpan Return the previous average distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getPreviousSpanX Return the previous average X distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getPreviousSpanY Return the previous average Y distance between each of the pointers forming the gesture in progress through the focal point. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getScaleFactor Return the scaling factor from the previous scale event to the current event. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getTimeDelta Return the time difference in milliseconds between the previous accepted scaling event and the current scaling event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isInProgress Returns `true` if a scale gesture is in progress. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isQuickScaleEnabled Return whether the quick scale gesture, in which the user performs a double tap followed by a swipe, should perform scaling. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isStylusScaleEnabled Return whether the stylus scale gesture, in which the user uses a stylus and presses the button, should perform scaling. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onTouchEvent Accepts MotionEvents and dispatches events to a `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` when appropriate. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setQuickScaleEnabled Set whether the associated `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` should receive onScale callbacks when the user performs a doubleTap followed by a swipe. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStylusScaleEnabled Sets whether the associated `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` should receive onScale callbacks when the user uses a stylus and presses the button. |

## Public constructors

### ScaleGestureDetector

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ScaleGestureDetector(
    context: Context, 
    listener: ScaleGestureDetector.OnScaleGestureListener)
```

Creates a ScaleGestureDetector with the supplied listener. You may only use this constructor from a `https://developer.android.com/reference/kotlin/android/os/Looper.html#` thread.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the application's context. This value cannot be `null`. |
| `listener` | [ScaleGestureDetector.OnScaleGestureListener](../android/view/ScaleGestureDetector.OnScaleGestureListener.md): the listener invoked for all the callbacks, this must not be null. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `listener` is null. |

### ScaleGestureDetector

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ScaleGestureDetector(
    context: Context, 
    listener: ScaleGestureDetector.OnScaleGestureListener, 
    handler: Handler?)
```

Creates a ScaleGestureDetector with the supplied listener.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the application's context. This value cannot be `null`. |
| `listener` | [ScaleGestureDetector.OnScaleGestureListener](../android/view/ScaleGestureDetector.OnScaleGestureListener.md): the listener invoked for all the callbacks, this must not be null. |
| `handler` | [Handler](../android.os/Handler.md)?: the handler to use for running deferred listener events. This value may be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `listener` is null. |

**See Also**

- Handler

## Public methods

### getCurrentSpan

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentSpan(): Float
```

Return the average distance between each of the pointers forming the gesture in progress through the focal point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Distance between pointers in pixels. |

### getCurrentSpanX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentSpanX(): Float
```

Return the average X distance between each of the pointers forming the gesture in progress through the focal point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Distance between pointers in pixels. |

### getCurrentSpanY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentSpanY(): Float
```

Return the average Y distance between each of the pointers forming the gesture in progress through the focal point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Distance between pointers in pixels. |

### getEventTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEventTime(): Long
```

Return the event time of the current event being processed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Current event time in milliseconds. |

### getFocusX

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFocusX(): Float
```

Get the X coordinate of the current gesture's focal point. If a gesture is in progress, the focal point is between each of the pointers forming the gesture. If isInProgress would return false, the result of this function is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | X coordinate of the focal point in pixels. |

### getFocusY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFocusY(): Float
```

Get the Y coordinate of the current gesture's focal point. If a gesture is in progress, the focal point is between each of the pointers forming the gesture. If isInProgress would return false, the result of this function is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Y coordinate of the focal point in pixels. |

### getPreviousSpan

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreviousSpan(): Float
```

Return the previous average distance between each of the pointers forming the gesture in progress through the focal point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Previous distance between pointers in pixels. |

### getPreviousSpanX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreviousSpanX(): Float
```

Return the previous average X distance between each of the pointers forming the gesture in progress through the focal point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Previous distance between pointers in pixels. |

### getPreviousSpanY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreviousSpanY(): Float
```

Return the previous average Y distance between each of the pointers forming the gesture in progress through the focal point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Previous distance between pointers in pixels. |

### getScaleFactor

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScaleFactor(): Float
```

Return the scaling factor from the previous scale event to the current event. This value is defined as (getCurrentSpan / getPreviousSpan).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The current scaling factor. |

### getTimeDelta

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeDelta(): Long
```

Return the time difference in milliseconds between the previous accepted scaling event and the current scaling event.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Time difference since the last scaling event in milliseconds. |

### isInProgress

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInProgress(): Boolean
```

Returns `true` if a scale gesture is in progress.

### isQuickScaleEnabled

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isQuickScaleEnabled(): Boolean
```

Return whether the quick scale gesture, in which the user performs a double tap followed by a swipe, should perform scaling.
**See Also**

- setQuickScaleEnabled

### isStylusScaleEnabled

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStylusScaleEnabled(): Boolean
```

Return whether the stylus scale gesture, in which the user uses a stylus and presses the button, should perform scaling.
**See Also**

- setStylusScaleEnabled

### onTouchEvent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTouchEvent(event: MotionEvent): Boolean
```

Accepts MotionEvents and dispatches events to a `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` when appropriate.

Applications should pass a complete and consistent event stream to this method. A complete and consistent event stream involves all MotionEvents from the initial ACTION_DOWN to the final ACTION_UP or ACTION_CANCEL.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md): The event to process. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the event was processed and the detector wants to receive the rest of the MotionEvents in this event stream. |

### setQuickScaleEnabled

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setQuickScaleEnabled(scales: Boolean): Unit
```

Set whether the associated `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` should receive onScale callbacks when the user performs a doubleTap followed by a swipe. Note that this is enabled by default if the app targets API 19 and newer.

| Parameters ||
|---|---|
| `scales` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable quick scaling, false to disable |

### setStylusScaleEnabled

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStylusScaleEnabled(scales: Boolean): Unit
```

Sets whether the associated `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` should receive onScale callbacks when the user uses a stylus and presses the button. Note that this is enabled by default if the app targets API 23 and newer.

| Parameters ||
|---|---|
| `scales` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable stylus scaling, false to disable. |
