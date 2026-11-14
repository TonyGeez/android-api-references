Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScaleGestureDetector

Kotlin | [Java](https://developer.android.com/reference/android/view/ScaleGestureDetector "View this page in Java")

```
open class ScaleGestureDetector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.ScaleGestureDetector](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#) |

Detects scaling transformation gestures using the supplied `https://developer.android.com/reference/kotlin/android/view/MotionEvent`s. The `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` callback will notify users when a particular gesture event has occurred. This class should only be used with `https://developer.android.com/reference/kotlin/android/view/MotionEvent`s reported via touch. To use this class:

- Create an instance of the `ScaleGestureDetector` for your `https://developer.android.com/reference/kotlin/android/view/View`
- In the `https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent)` method ensure you call `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#onTouchEvent(android.view.MotionEvent)`. The methods defined in your callback will be executed when the events occur.

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` The listener for receiving notifications when gestures occur. |
| open | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.SimpleOnScaleGestureListener` A convenience class to extend when you only want to listen for a subset of scaling-related events. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#ScaleGestureDetector(android.content.Context,%20android.view.ScaleGestureDetector.OnScaleGestureListener)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, listener: https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener)` Creates a ScaleGestureDetector with the supplied listener. |
| `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#ScaleGestureDetector(android.content.Context,%20android.view.ScaleGestureDetector.OnScaleGestureListener,%20android.os.Handler)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, listener: https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Creates a ScaleGestureDetector with the supplied listener. |

| Public methods ||
|---|---|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getCurrentSpan()()` Return the average distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getCurrentSpanX()()` Return the average X distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getCurrentSpanY()()` Return the average Y distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getEventTime()()` Return the event time of the current event being processed. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getFocusX()()` Get the X coordinate of the current gesture's focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getFocusY()()` Get the Y coordinate of the current gesture's focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getPreviousSpan()()` Return the previous average distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getPreviousSpanX()()` Return the previous average X distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getPreviousSpanY()()` Return the previous average Y distance between each of the pointers forming the gesture in progress through the focal point. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getScaleFactor()()` Return the scaling factor from the previous scale event to the current event. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getTimeDelta()()` Return the time difference in milliseconds between the previous accepted scaling event and the current scaling event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#isInProgress()()` Returns `true` if a scale gesture is in progress. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#isQuickScaleEnabled()()` Return whether the quick scale gesture, in which the user performs a double tap followed by a swipe, should perform scaling. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#isStylusScaleEnabled()()` Return whether the stylus scale gesture, in which the user uses a stylus and presses the button, should perform scaling. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#onTouchEvent(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent)` Accepts MotionEvents and dispatches events to a `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` when appropriate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#setQuickScaleEnabled(kotlin.Boolean)(scales: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether the associated `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` should receive onScale callbacks when the user performs a doubleTap followed by a swipe. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#setStylusScaleEnabled(kotlin.Boolean)(scales: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the associated `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` should receive onScale callbacks when the user uses a stylus and presses the button. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the application's context. This value cannot be `null`. |
| `listener` | [ScaleGestureDetector.OnScaleGestureListener](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener): the listener invoked for all the callbacks, this must not be null. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the application's context. This value cannot be `null`. |
| `listener` | [ScaleGestureDetector.OnScaleGestureListener](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener): the listener invoked for all the callbacks, this must not be null. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: the handler to use for running deferred listener events. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `listener` is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Handler.html#Handler()`

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

Get the X coordinate of the current gesture's focal point. If a gesture is in progress, the focal point is between each of the pointers forming the gesture. If `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#isInProgress()` would return false, the result of this function is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | X coordinate of the focal point in pixels. |

### getFocusY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFocusY(): Float
```

Get the Y coordinate of the current gesture's focal point. If a gesture is in progress, the focal point is between each of the pointers forming the gesture. If `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#isInProgress()` would return false, the result of this function is undefined.

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

Return the scaling factor from the previous scale event to the current event. This value is defined as (`https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getCurrentSpan()` / `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getPreviousSpan()`).

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

- `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#setQuickScaleEnabled(kotlin.Boolean)`

### isStylusScaleEnabled

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStylusScaleEnabled(): Boolean
```

Return whether the stylus scale gesture, in which the user uses a stylus and presses the button, should perform scaling.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#setStylusScaleEnabled(kotlin.Boolean)`

### onTouchEvent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTouchEvent(event: MotionEvent): Boolean
```

Accepts MotionEvents and dispatches events to a `https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener` when appropriate.

Applications should pass a complete and consistent event stream to this method. A complete and consistent event stream involves all MotionEvents from the initial ACTION_DOWN to the final ACTION_UP or ACTION_CANCEL.

| Parameters ||
|---|---|
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent): The event to process. This value cannot be `null`. |

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
