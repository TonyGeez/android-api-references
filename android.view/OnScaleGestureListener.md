# ScaleGestureDetector.OnScaleGestureListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnScaleGestureListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ScaleGestureDetector.OnScaleGestureListener "View this page in Java") 
| --- | --- |

```
interface OnScaleGestureListener
```

| [android.view.ScaleGestureDetector.OnScaleGestureListener](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener#) |

| Known Direct Subclasses [ScaleGestureDetector.SimpleOnScaleGestureListener](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.SimpleOnScaleGestureListener) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------| | [ScaleGestureDetector.SimpleOnScaleGestureListener](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.SimpleOnScaleGestureListener) | A convenience class to extend when you only want to listen for a subset of scaling-related events. | |
| --- | --- | --- | --- | --- | --- | --- |

The listener for receiving notifications when gestures occur. If you want to listen for all the different gestures then implement this interface. If you only want to listen for a subset it might be easier to extend [SimpleOnScaleGestureListener](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.SimpleOnScaleGestureListener). An application will receive events in the following order:

- One [OnScaleGestureListener.onScaleBegin(ScaleGestureDetector)](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener#onScaleBegin(android.view.ScaleGestureDetector))
- Zero or more [OnScaleGestureListener.onScale(ScaleGestureDetector)](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener#onScale(android.view.ScaleGestureDetector))
- One [OnScaleGestureListener.onScaleEnd(ScaleGestureDetector)](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener#onScaleEnd(android.view.ScaleGestureDetector))

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onScale](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener#onScale(android.view.ScaleGestureDetector))`(`detector:` ` [ScaleGestureDetector](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector)`)` Responds to scaling events for a gesture in progress. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onScaleBegin](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener#onScaleBegin(android.view.ScaleGestureDetector))`(`detector:` ` [ScaleGestureDetector](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector)`)` Responds to the beginning of a scaling gesture. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScaleEnd](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector.OnScaleGestureListener#onScaleEnd(android.view.ScaleGestureDetector))`(`detector:` ` [ScaleGestureDetector](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector)`)` Responds to the end of a scale gesture. |
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
| `detector` | [ScaleGestureDetector](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector):The detector reporting the event - use this to retrieve extended info about event state. This value cannot be`null`. |

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
| `detector` | [ScaleGestureDetector](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector):The detector reporting the event - use this to retrieve extended info about event state. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether or not the detector should continue recognizing this gesture. For example, if a gesture is beginning with a focal point outside of a region where it makes sense, onScaleBegin() may return false to ignore the rest of the gesture. |

### onScaleEnd

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScaleEnd(detector: ScaleGestureDetector): Unit
```

Responds to the end of a scale gesture. Reported by existing pointers going up. Once a scale has ended, [ScaleGestureDetector.getFocusX()](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getFocusX())and [ScaleGestureDetector.getFocusY()](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector#getFocusY())will return focal point of the pointers remaining on the screen.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `detector` | [ScaleGestureDetector](https://developer.android.com/reference/kotlin/android/view/ScaleGestureDetector):The detector reporting the event - use this to retrieve extended info about event state. This value cannot be`null`. |
