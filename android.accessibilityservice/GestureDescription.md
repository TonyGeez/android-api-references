# GestureDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureDescription

Kotlin| [Java](https://developer.android.com/reference/android/accessibilityservice/GestureDescription "View this page in Java") 
| --- | --- |

```
class GestureDescription
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.GestureDescription](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription#) |

Accessibility services with the [android.R.styleable#AccessibilityService_canPerformGestures](https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canPerformGestures:kotlin.Int) property can dispatch gestures. This class describes those gestures. Gestures are made up of one or more strokes. Gestures are immutable once built and will be dispatched to the specified display.

Spatial dimensions throughout are in screen pixels. Time is measured in milliseconds.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription.Builder) Builder for a`GestureDescription` |
| | [StrokeDescription](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription.StrokeDescription) Immutable description of stroke that can be part of a gesture. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisplayId](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription#getDisplayId())`()` Returns the ID of the display this gesture is sent on, for use with [android.hardware.display.DisplayManager#getDisplay(int)](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMaxGestureDuration](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription#getMaxGestureDuration())`()` Get the upper limit on a gesture's duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxStrokeCount](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription#getMaxStrokeCount())`()` Get the upper limit for the number of strokes a gesture may contain. |
| --- | --- |
| [GestureDescription.StrokeDescription](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription.StrokeDescription)! | [getStroke](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription#getStroke(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read a stroke from the gesture |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrokeCount](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription#getStrokeCount())`()` Get the number of stroke in the gesture. |

## Public methods

### getDisplayId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayId(): Int
```

Returns the ID of the display this gesture is sent on, for use with [android.hardware.display.DisplayManager#getDisplay(int)](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)).

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The logical display id. |

### getMaxGestureDuration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMaxGestureDuration(): Long
```

Get the upper limit on a gesture's duration.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The maximum duration in milliseconds. |

### getMaxStrokeCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMaxStrokeCount(): Int
```

Get the upper limit for the number of strokes a gesture may contain.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The maximum number of strokes. |

### getStroke

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStroke(index: Int): GestureDescription.StrokeDescription!
```

Read a stroke from the gesture

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the stroke Value is 0 or greater |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [GestureDescription.StrokeDescription](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription.StrokeDescription)! | A description of the stroke. |

### getStrokeCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStrokeCount(): Int
```

Get the number of stroke in the gesture.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of strokes in this gesture |
