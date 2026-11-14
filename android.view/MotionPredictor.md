Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MotionPredictor

Kotlin | [Java](MotionPredictor.md)
| --- | --- |

```
class MotionPredictor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.MotionPredictor](MotionPredictor.md) |

Calculate motion predictions. Feed motion events to this class in order to generate predicted future events. The prediction functionality may not be available on all devices: check if a specific source is supported on a given input device using `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#isPredictionAvailable(kotlin.Int,%20kotlin.Int)`. Send all of the events that were received from the system to `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#record(android.view.MotionEvent)` to generate complete, accurate predictions from `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#predict(kotlin.Long)`. When processing the returned predictions, make sure to consider all of the android.view.MotionEvent#getHistoricalAxisValue.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#MotionPredictor(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Create a new MotionPredictor for the provided `https://developer.android.com/reference/kotlin/android/content/Context.html#`. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#isPredictionAvailable(kotlin.Int,%20kotlin.Int)(deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Check whether a device supports motion predictions for a given source type. |
| [MotionEvent](MotionEvent.md)? | `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#predict(kotlin.Long)(predictionTimeNanos: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Get a predicted event for the gesture that has been provided to `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#record(android.view.MotionEvent)`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#record(android.view.MotionEvent)(event: https://developer.android.com/reference/kotlin/android/view/MotionEvent)` Record a movement so that in the future, a prediction for the current gesture can be generated. |
| --- | --- |

## Public constructors

### MotionPredictor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MotionPredictor(context: Context)
```

Create a new MotionPredictor for the provided `https://developer.android.com/reference/kotlin/android/content/Context.html#`.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The context for the predictions. This value cannot be `null`. |

## Public methods

### isPredictionAvailable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPredictionAvailable(
    deviceId: Int, 
    source: Int
): Boolean
```

Check whether a device supports motion predictions for a given source type.

| Parameters ||
|---|---|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The input device id. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The source of input events. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the current device supports predictions, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/MotionEvent#getDeviceId()`
- `https://developer.android.com/reference/kotlin/android/view/MotionEvent#getSource()`

### predict

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun predict(predictionTimeNanos: Long): MotionEvent?
```

Get a predicted event for the gesture that has been provided to `https://developer.android.com/reference/kotlin/android/view/MotionPredictor#record(android.view.MotionEvent)`. Predictions may not reach the requested timestamp if the confidence in the prediction results is low.

| Parameters ||
|---|---|
| `predictionTimeNanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time that the prediction should target, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base, but in nanoseconds. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/MotionEvent?` | The predicted motion event, or \`null\` if predictions are not supported, or not possible for the current gesture. Be sure to check the historical data in addition to the latest (android.view.MotionEvent#getX, android.view.MotionEvent#getY) coordinates for smooth prediction curves. |

### record

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun record(event: MotionEvent): Unit
```

Record a movement so that in the future, a prediction for the current gesture can be generated. Only gestures from one input device at a time should be provided to an instance of MotionPredictor.

| Parameters ||
|---|---|
| `event` | [MotionEvent](MotionEvent.md): The received event. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if an inconsistent MotionEvent stream is sent. |
