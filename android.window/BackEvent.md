# BackEvent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackEvent

Kotlin | [Java](https://developer.android.com/reference/android/window/BackEvent "View this page in Java") 
| --- | --- |

```
class BackEvent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.window.BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent#) |

Object used to report back gesture progress. Holds information about the touch event, swipe direction and the animation progress that predictive back animations should seek to.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDGE_LEFT](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_LEFT:kotlin.Int) Indicates that the edge swipe starts from the left edge of the screen |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDGE_NONE](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_NONE:kotlin.Int) Indicates that the back event was not triggered by an edge swipe back gesture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDGE_RIGHT](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_RIGHT:kotlin.Int) Indicates that the edge swipe starts from the right edge of the screen |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent#BackEvent(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int))`(`touchX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `touchY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `progress:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `swipeEdge:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent#) instance with a frame time of 0. |
| [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent#BackEvent(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.Long))`(`touchX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `touchY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `progress:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `swipeEdge:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `frameTimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent#) instance. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/window/BackEvent#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFrameTimeMillis](https://developer.android.com/reference/kotlin/android/window/BackEvent#getFrameTimeMillis())`()` Returns the frameTime of the BackEvent in milliseconds. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getProgress](https://developer.android.com/reference/kotlin/android/window/BackEvent#getProgress())`()` Returns a value between 0 and 1 on how far along the back gesture is. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSwipeEdge](https://developer.android.com/reference/kotlin/android/window/BackEvent#getSwipeEdge())`()` Returns the screen edge that the swipe starts from. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getTouchX](https://developer.android.com/reference/kotlin/android/window/BackEvent#getTouchX())`()` Returns the absolute X location of the touch point, or NaN if the event is from a button press. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getTouchY](https://developer.android.com/reference/kotlin/android/window/BackEvent#getTouchY())`()` Returns the absolute Y location of the touch point, or NaN if the event is from a button press. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/window/BackEvent#toString())`()` <br /> |

## Constants

### EDGE_LEFT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDGE_LEFT: Int
```

Indicates that the edge swipe starts from the left edge of the screen 

 Value: 0

### EDGE_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDGE_NONE: Int
```

Indicates that the back event was not triggered by an edge swipe back gesture. This applies to cases like using the back button in 3-button navigation or pressing a hardware back button. 

 Value: 2

### EDGE_RIGHT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDGE_RIGHT: Int
```

Indicates that the edge swipe starts from the right edge of the screen 

 Value: 1

## Public constructors

### BackEvent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BackEvent(
    touchX: Float, 
    touchY: Float, 
    progress: Float, 
    swipeEdge: Int)
```

Creates a new [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent#) instance with a frame time of 0.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `touchX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Absolute X location of the touch point of this event. |
| `touchY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Absolute Y location of the touch point of this event. |
| `progress` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Value between 0 and 1 on how far along the back gesture is. |
| --- | --- |
| `swipeEdge` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Indicates which edge the swipe starts from. Value is [android.window.BackEvent#EDGE_LEFT](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_LEFT:kotlin.Int), [android.window.BackEvent#EDGE_RIGHT](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_RIGHT:kotlin.Int), or [android.window.BackEvent#EDGE_NONE](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_NONE:kotlin.Int) |

### BackEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BackEvent(
    touchX: Float, 
    touchY: Float, 
    progress: Float, 
    swipeEdge: Int, 
    frameTimeMillis: Long)
```

Creates a new [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent#) instance.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `touchX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Absolute X location of the touch point of this event. |
| `touchY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Absolute Y location of the touch point of this event. |
| `progress` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Value between 0 and 1 on how far along the back gesture is. |
| --- | --- |
| `swipeEdge` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Indicates which edge the swipe starts from. Value is [android.window.BackEvent#EDGE_LEFT](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_LEFT:kotlin.Int), [android.window.BackEvent#EDGE_RIGHT](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_RIGHT:kotlin.Int), or [android.window.BackEvent#EDGE_NONE](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_NONE:kotlin.Int) |
| `frameTimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): frame time of the back event. |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getFrameTimeMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrameTimeMillis(): Long
```

Returns the frameTime of the BackEvent in milliseconds. Useful for calculating velocity. 

### getProgress

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProgress(): Float
```

Returns a value between 0 and 1 on how far along the back gesture is. This value is driven by the horizontal location of the touch point, and should be used as the fraction to seek the predictive back animation with. Specifically,

1. The progress is 0 when the touch is at the starting edge of the screen (left or right), and animation should seek to its start state.
2. The progress is approximately 1 when the touch is at the opposite side of the screen, and animation should seek to its end state. Exact end value may vary depending on screen size.

- After the gesture finishes in cancel state, this method keeps getting invoked until the progress value animates back to 0. In-between locations are linearly interpolated based on horizontal distance from the starting edge and smooth clamped to 1 when the distance exceeds a system-wide threshold.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is between 0.0f and 1.0f inclusive |

### getSwipeEdge

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSwipeEdge(): Int
```

Returns the screen edge that the swipe starts from.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.window.BackEvent#EDGE_LEFT](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_LEFT:kotlin.Int), [android.window.BackEvent#EDGE_RIGHT](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_RIGHT:kotlin.Int), or [android.window.BackEvent#EDGE_NONE](https://developer.android.com/reference/kotlin/android/window/BackEvent#EDGE_NONE:kotlin.Int) |

### getTouchX

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTouchX(): Float
```

Returns the absolute X location of the touch point, or NaN if the event is from a button press. 

### getTouchY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTouchY(): Float
```

Returns the absolute Y location of the touch point, or NaN if the event is from a button press. 

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
