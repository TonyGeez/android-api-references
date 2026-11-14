# GestureDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureDescription

Kotlin| [Java](GestureDescription.md) 
| --- | --- |

```
class GestureDescription
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.GestureDescription](GestureDescription.md) |

Accessibility services with the [android.R.styleable#AccessibilityService_canPerformGestures](../android/R.styleable.md) property can dispatch gestures. This class describes those gestures. Gestures are made up of one or more strokes. Gestures are immutable once built and will be dispatched to the specified display.

Spatial dimensions throughout are in screen pixels. Time is measured in milliseconds.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/accessibilityservice/GestureDescription.Builder.md) Builder for a`GestureDescription` |
| | [StrokeDescription](../android/accessibilityservice/GestureDescription.StrokeDescription.md) Immutable description of stroke that can be part of a gesture. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisplayId](GestureDescription.md))`()` Returns the ID of the display this gesture is sent on, for use with [android.hardware.display.DisplayManager#getDisplay(int)](../android.hardware.display/DisplayManager.md)). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMaxGestureDuration](GestureDescription.md))`()` Get the upper limit on a gesture's duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxStrokeCount](GestureDescription.md))`()` Get the upper limit for the number of strokes a gesture may contain. |
| --- | --- |
| [GestureDescription.StrokeDescription](../android/accessibilityservice/GestureDescription.StrokeDescription.md)! | [getStroke](GestureDescription.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read a stroke from the gesture |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrokeCount](GestureDescription.md))`()` Get the number of stroke in the gesture. |

## Public methods

### getDisplayId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayId(): Int
```

Returns the ID of the display this gesture is sent on, for use with [android.hardware.display.DisplayManager#getDisplay(int)](../android.hardware.display/DisplayManager.md)).

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
| [GestureDescription.StrokeDescription](../android/accessibilityservice/GestureDescription.StrokeDescription.md)! | A description of the stroke. |

### getStrokeCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStrokeCount(): Int
```

Get the number of stroke in the gesture.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of strokes in this gesture |
