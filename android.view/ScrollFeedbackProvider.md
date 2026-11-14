# ScrollFeedbackProvider

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScrollFeedbackProvider

Kotlin| [Java](https://developer.android.com/reference/android/view/ScrollFeedbackProvider "View this page in Java") 
| --- | --- |

```
interface ScrollFeedbackProvider
```

| [android.view.ScrollFeedbackProvider](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#) |

Provides feedback to the user for scroll events on a [View](https://developer.android.com/reference/kotlin/android/view/View). The type of feedback provided to the user may depend on the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) that generated the scroll events.

An example of the type of feedback that this interface may provide is haptic feedback (that is, tactile feedback that provide the user physical feedback for their scroll).

The interface provides methods for the client to report different scroll events. The client should report all scroll events that they want to be considered for scroll feedback using the respective methods. The interface will process these events and provide scroll feedback based on its specific feedback implementation.

### Obtaining the correct arguments for methods in this interface

Methods in this interface rely on the provision of valid [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) ID and source, as well as the [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) axis that generated a specific scroll event. The [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) represented by the provided ID must have a [InputDevice.MotionRange](https://developer.android.com/reference/kotlin/android/view/InputDevice.MotionRange) with the provided source and axis. See below for more details on obtaining the right arguments for your method call.

- **inputDeviceId** : should always be the ID of the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) that generated the scroll event. If calling this method in response to a [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent), use the device ID that is reported by the event, which can be obtained using [MotionEvent.getDeviceId()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getDeviceId()). Otherwise, use a valid ID that is obtained from [InputDevice.getId()](https://developer.android.com/reference/kotlin/android/view/InputDevice#getId()), or from an [android.hardware.input.InputManager](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.html#) instance ([android.hardware.input.InputManager#getInputDeviceIds()](https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.html#getInputDeviceIds())gives all the valid input device IDs).
- **source** : should always be the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) source that generated the scroll event. Use [MotionEvent.getSource()](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSource())if calling this method in response to a [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent). Otherwise, use a valid source for the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice). You can use [InputDevice.getMotionRanges()](https://developer.android.com/reference/kotlin/android/view/InputDevice#getMotionRanges())to get all the [InputDevice.MotionRange](https://developer.android.com/reference/kotlin/android/view/InputDevice.MotionRange) s for the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice), from which you can derive all the valid sources for the device.
- **axis** : should always be the axis whose axis value produced the scroll event. A [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) may report data for multiple axes, and each axis may have multiple data points for different pointers. Use the axis whose movement produced the specific scroll event. The motion value for an axis can be obtained using [MotionEvent.getAxisValue(int)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#getAxisValue(kotlin.Int)). You can use [InputDevice.getMotionRanges()](https://developer.android.com/reference/kotlin/android/view/InputDevice#getMotionRanges())to get all the [InputDevice.MotionRange](https://developer.android.com/reference/kotlin/android/view/InputDevice.MotionRange) s for the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice), from which you can derive all the valid axes for the device.

**Note** that not all valid input device source and motion axis inputs are necessarily supported for scroll feedback; the implementation may choose to provide no feedback for some valid input device source and motion axis arguments.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ScrollFeedbackProvider](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#) | [createProvider](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#createProvider(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`)` Creates a [ScrollFeedbackProvider](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#) implementation for this device. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollLimit](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#onScrollLimit(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`inputDeviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isStart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Call this when the view has reached the scroll limit. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollProgress](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#onScrollProgress(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`inputDeviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `deltaInPixels:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Call this when the view has scrolled. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSnapToItem](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#onSnapToItem(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`inputDeviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Call this when the view has snapped to an item. |

## Public methods

### createProvider

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createProvider(view: View): ScrollFeedbackProvider
```

Creates a [ScrollFeedbackProvider](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#) implementation for this device.

Use a feedback provider created by this method, unless you intend to use your custom scroll feedback providing logic. This allows your use cases to generate scroll feedback that is consistent with the rest of the use cases on the device.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View):the [View](https://developer.android.com/reference/kotlin/android/view/View) for which to provide scroll feedback. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ScrollFeedbackProvider](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#) | the default [ScrollFeedbackProvider](https://developer.android.com/reference/kotlin/android/view/ScrollFeedbackProvider#) implementation for the device. This value cannot be`null`. |

### onScrollLimit

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollLimit(
    inputDeviceId: Int, 
    source: Int, 
    axis: Int, 
    isStart: Boolean
): Unit
```

Call this when the view has reached the scroll limit.

Note that a feedback may not be provided on every call to this method. This interface, for instance, may provide feedback on every \`N\`th scroll limit event. For the interface to properly provide feedback when needed, call this method for each scroll limit event that you want to be accounted to scroll limit feedback.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputDeviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID of the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) that caused scrolling to hit limit. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input source of the motion that caused scrolling to hit the limit. |
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the axis of`event`that caused scrolling to hit the limit. |
| --- | --- |
| `isStart` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if scrolling hit limit at the start of the scrolling list, and`false`if the scrolling hit limit at the end of the scrolling list.*start* and*end*in this context are not geometrical references. Instead, they refer to the start and end of a scrolling experience. As such, "start" for some views may be at the bottom of a scrolling list, while it may be at the top of scrolling list for others.** |

### onScrollProgress

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollProgress(
    inputDeviceId: Int, 
    source: Int, 
    axis: Int, 
    deltaInPixels: Int
): Unit
```

Call this when the view has scrolled.

Different axes have different ways to map their raw axis values to pixels for scrolling. When calling this method, use the scroll values in pixels by which the view was scrolled; do not use the raw axis values. That is, use whatever value is passed to one of View's scrolling methods (example: [View.scrollBy(int, int)](https://developer.android.com/reference/kotlin/android/view/View#scrollBy(kotlin.Int,%20kotlin.Int))). For example, for vertical scrolling on [MotionEvent.AXIS_SCROLL](https://developer.android.com/reference/kotlin/android/view/MotionEvent#AXIS_SCROLL:kotlin.Int), convert the raw axis value to the equivalent pixels by using [ViewConfiguration.getScaledVerticalScrollFactor()](https://developer.android.com/reference/kotlin/android/view/ViewConfiguration#getScaledVerticalScrollFactor()), and use that value for this method call.

Note that a feedback may not be provided on every call to this method. This interface, for instance, may provide feedback for every \`x\` pixels scrolled. For the interface to properly track scroll progress and provide feedback when needed, call this method for each scroll event that you want to be accounted to scroll feedback.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputDeviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID of the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) that caused scroll progress. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input source of the motion that caused scroll progress. |
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the axis of`event`that caused scroll progress. |
| --- | --- |
| `deltaInPixels` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of scroll progress, in pixels. |

### onSnapToItem

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSnapToItem(
    inputDeviceId: Int, 
    source: Int, 
    axis: Int
): Unit
```

Call this when the view has snapped to an item.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputDeviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID of the [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice) that generated the motion triggering the snap. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input source of the motion causing the snap. |
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the axis of`event`that caused the item to snap. |
| --- | --- |
