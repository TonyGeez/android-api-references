# ScaleGestureDetector.OnScaleGestureListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnScaleGestureListener

Kotlin| [Java](../android/view/ScaleGestureDetector.OnScaleGestureListener.md) 
| --- | --- |

```
interface OnScaleGestureListener
```

| [android.view.ScaleGestureDetector.OnScaleGestureListener](../android/view/ScaleGestureDetector.OnScaleGestureListener.md) |

| Known Direct Subclasses [ScaleGestureDetector.SimpleOnScaleGestureListener](../android/view/ScaleGestureDetector.SimpleOnScaleGestureListener.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------| | [ScaleGestureDetector.SimpleOnScaleGestureListener](../android/view/ScaleGestureDetector.SimpleOnScaleGestureListener.md) | A convenience class to extend when you only want to listen for a subset of scaling-related events. | |
| --- | --- | --- | --- | --- | --- | --- |

The listener for receiving notifications when gestures occur. If you want to listen for all the different gestures then implement this interface. If you only want to listen for a subset it might be easier to extend [SimpleOnScaleGestureListener](../android/view/ScaleGestureDetector.SimpleOnScaleGestureListener.md). An application will receive events in the following order:

- One [OnScaleGestureListener.onScaleBegin(ScaleGestureDetector)](../android/view/ScaleGestureDetector.OnScaleGestureListener.md))
- Zero or more [OnScaleGestureListener.onScale(ScaleGestureDetector)](../android/view/ScaleGestureDetector.OnScaleGestureListener.md))
- One [OnScaleGestureListener.onScaleEnd(ScaleGestureDetector)](../android/view/ScaleGestureDetector.OnScaleGestureListener.md))

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onScale](../android/view/ScaleGestureDetector.OnScaleGestureListener.md))`(`detector:` ` [ScaleGestureDetector](../android/view/ScaleGestureDetector.md)`)` Responds to scaling events for a gesture in progress. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onScaleBegin](../android/view/ScaleGestureDetector.OnScaleGestureListener.md))`(`detector:` ` [ScaleGestureDetector](../android/view/ScaleGestureDetector.md)`)` Responds to the beginning of a scaling gesture. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScaleEnd](../android/view/ScaleGestureDetector.OnScaleGestureListener.md))`(`detector:` ` [ScaleGestureDetector](../android/view/ScaleGestureDetector.md)`)` Responds to the end of a scale gesture. |
| --- | --- |

## Public methods

### onScale

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScale(detector: ScaleGestureDetector): Boolean
```

Responds to scaling events for a gesture in progress. Reported by pointer motion.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `detector` | [ScaleGestureDetector](../android/view/ScaleGestureDetector.md):The detector reporting the event - use this to retrieve extended info about event state. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether or not the detector should consider this event as handled. If an event was not handled, the detector will continue to accumulate movement until an event is handled. This can be useful if an application, for example, only wants to update scaling factors if the change is greater than 0.01. |

### onScaleBegin

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScaleBegin(detector: ScaleGestureDetector): Boolean
```

Responds to the beginning of a scaling gesture. Reported by new pointers going down.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `detector` | [ScaleGestureDetector](../android/view/ScaleGestureDetector.md):The detector reporting the event - use this to retrieve extended info about event state. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether or not the detector should continue recognizing this gesture. For example, if a gesture is beginning with a focal point outside of a region where it makes sense, onScaleBegin() may return false to ignore the rest of the gesture. |

### onScaleEnd

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScaleEnd(detector: ScaleGestureDetector): Unit
```

Responds to the end of a scale gesture. Reported by existing pointers going up. Once a scale has ended, [ScaleGestureDetector.getFocusX()](../android/view/ScaleGestureDetector.md))and [ScaleGestureDetector.getFocusY()](../android/view/ScaleGestureDetector.md))will return focal point of the pointers remaining on the screen.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `detector` | [ScaleGestureDetector](../android/view/ScaleGestureDetector.md):The detector reporting the event - use this to retrieve extended info about event state. This value cannot be`null`. |
