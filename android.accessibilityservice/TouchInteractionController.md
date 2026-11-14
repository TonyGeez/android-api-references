Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TouchInteractionController

Kotlin | [Java](../android/accessibilityservice/TouchInteractionController.md)
| --- | --- |

```
class TouchInteractionController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.TouchInteractionController](../android/accessibilityservice/TouchInteractionController.md) |

This class allows a service to handle touch exploration and the detection of specialized accessibility gestures. The service receives motion events and can match those motion events against the gestures it supports. The service can also request the framework enter three other states of operation for the duration of this interaction. Upon entering any of these states the framework will take over and the service will not receive motion events until the start of a new interaction. The states are as follows:

- The service can tell the framework that this interaction is touch exploration. The user is trying to explore the screen rather than manipulate it. The framework will then convert the motion events to hover events to support touch exploration.
- The service can tell the framework that this interaction is a dragging interaction where two fingers are used to execute a one-finger gesture such as scrolling the screen. The service must specify which of the two fingers should be passed through to rest of the input pipeline.
- Finally, the service can request that the framework delegate this interaction, meaning pass it through to the rest of the input pipeline as-is.

When `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled, this controller will receive all motion events received by the framework for the specified display when not touch-exploring or delegating. If the service classifies this interaction as touch exploration or delegating the framework will stop sending motion events to the service for the duration of this interaction. If the service classifies this interaction as a dragging interaction the framework will send motion events to the service to allow the service to determine if the interaction still qualifies as dragging or if it has become a delegating interaction. If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is disabled this controller will not receive any motion events because touch interactions are being passed through to the input pipeline unaltered. Note that `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` requires setting `https://developer.android.com/reference/kotlin/android/R.attr.html#canRequestTouchExplorationMode:kotlin.Int` as well.

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController.Callback` callbacks allow services to receive motion events and state change updates. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_CLEAR:kotlin.Int` The state where the user is not touching the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_DELEGATING:kotlin.Int` The user is performing a gesture which is being passed through to the input pipeline as-is. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_DRAGGING:kotlin.Int` The state where the user is dragging with two fingers. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_TOUCH_EXPLORING:kotlin.Int` The state where the user is explicitly exploring the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_TOUCH_INTERACTING:kotlin.Int` The state where the user is touching the screen and the service is receiving motion events. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#getDisplayId()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#getMaxPointerCount()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#getState()()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#performClick()()` If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added, this function tells the framework to perform a click. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#performLongClickAndStartDrag()()` If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added, this function tells the framework to perform a long click. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#registerCallback(java.util.concurrent.Executor,%20android.accessibilityservice.TouchInteractionController.Callback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController.Callback)` Adds the specified callback to the list of callbacks. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#requestDelegating()()` If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added, this function tells the framework to initiate a delegating interaction. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#requestDragging(kotlin.Int)(pointerId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added, this function tells the framework to initiate a dragging interaction using the specified pointer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#requestTouchExploration()()` If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added for this display this function tells the framework to initiate touch exploration. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#stateToString(kotlin.Int)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a string representation of the specified state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#unregisterAllCallbacks()()` Removes all callbacks and returns control of touch interactions to the framework. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#unregisterCallback(android.accessibilityservice.TouchInteractionController.Callback)(callback: https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController.Callback)` Unregisters the specified callback. |
| --- | --- |

## Constants

### STATE_CLEAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_CLEAR: Int
```

The state where the user is not touching the screen.

 Value: 0

### STATE_DELEGATING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_DELEGATING: Int
```

The user is performing a gesture which is being passed through to the input pipeline as-is. The service is not receiving motion events.

 Value: 4

### STATE_DRAGGING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_DRAGGING: Int
```

The state where the user is dragging with two fingers. The service is not receiving motion events. The selected finger is being dispatched to the rest of the input pipeline to execute the drag.

 Value: 3

### STATE_TOUCH_EXPLORING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TOUCH_EXPLORING: Int
```

The state where the user is explicitly exploring the screen. The service is not receiving motion events.

 Value: 2

### STATE_TOUCH_INTERACTING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TOUCH_INTERACTING: Int
```

The state where the user is touching the screen and the service is receiving motion events.

 Value: 1

## Public methods

### getDisplayId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayId(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the display id associated with this controller. |

### getMaxPointerCount

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxPointerCount(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum number of pointers that this display will accept. |

### getState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getState(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current state of this controller. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_CLEAR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_DELEGATING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_DRAGGING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController#STATE_TOUCH_EXPLORING:kotlin.Int`

### performClick

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun performClick(): Unit
```

If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added, this function tells the framework to perform a click. The framework will first try to perform AccessibilityNodeInfo.AccessibilityAction#ACTION_CLICK on the item with accessibility focus. If that fails, the framework will simulate a click using motion events on the last location to have accessibility focus.

### performLongClickAndStartDrag

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun performLongClickAndStartDrag(): Unit
```

If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added, this function tells the framework to perform a long click. The framework will simulate a long click using motion events on the last location with accessibility focus and will delegate any movements to the rest of the input pipeline. This allows a user to double-tap and hold to trigger a drag and then execute that drag by moving their finger.

### registerCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerCallback(
    executor: Executor?, 
    callback: TouchInteractionController.Callback
): Unit
```

Adds the specified callback to the list of callbacks. The callback will run using on the specified `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`', or on the service's main thread if the Executor is `null`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: the executor for this callback, or `null` to execute on the service's main thread |
| `callback` | [TouchInteractionController.Callback](../android/accessibilityservice/TouchInteractionController.Callback.md): the callback to add, must be non-null |

### requestDelegating

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestDelegating(): Unit
```

If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added, this function tells the framework to initiate a delegating interaction. Motion events will be passed through as-is to the rest of the input pipeline for the duration of this interaction.

### requestDragging

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestDragging(pointerId: Int): Unit
```

If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added, this function tells the framework to initiate a dragging interaction using the specified pointer. The pointer's movements will be passed through to the rest of the input pipeline. Dragging is often used to perform two-finger scrolling.

| Parameters ||
|---|---|
| `pointerId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the pointer to be passed through to the rest of the input pipeline. If the pointer id is valid but not actually present on the screen it will be ignored. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pointer id is outside of the allowed range. |

### requestTouchExploration

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestTouchExploration(): Unit
```

If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled and at least one callback has been added for this display this function tells the framework to initiate touch exploration. Touch exploration will continue for the duration of this interaction.

### stateToString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stateToString(state: Int): String
```

Returns a string representation of the specified state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### unregisterAllCallbacks

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterAllCallbacks(): Unit
```

Removes all callbacks and returns control of touch interactions to the framework.

### unregisterCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterCallback(callback: TouchInteractionController.Callback): Boolean
```

Unregisters the specified callback.

| Parameters ||
|---|---|
| `callback` | [TouchInteractionController.Callback](../android/accessibilityservice/TouchInteractionController.Callback.md): the callback to remove, must be non-null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the callback was removed, `false` otherwise |
