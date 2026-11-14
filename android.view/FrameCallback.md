# Choreographer.FrameCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FrameCallback

Kotlin| [Java](https://developer.android.com/reference/android/view/Choreographer.FrameCallback "View this page in Java") 

```
interface FrameCallback
```

| [android.view.Choreographer.FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback#) |

Implement this interface to receive a callback when a new display frame is being rendered. The callback is invoked on the [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) thread to which the [Choreographer](https://developer.android.com/reference/kotlin/android/view/Choreographer) is attached.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doFrame](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback#doFrame(kotlin.Long))`(`frameTimeNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Called when a new display frame is being rendered. |

## Public methods

### doFrame

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun doFrame(frameTimeNanos: Long): Unit
```

Called when a new display frame is being rendered.

This method provides the time in nanoseconds when the frame started being rendered. The frame time provides a stable time base for synchronizing animations and drawing. It should be used instead of [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())or [System.nanoTime()](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime())for animations and drawing in the UI. Using the frame time helps to reduce inter-frame jitter because the frame time is fixed at the time the frame was scheduled to start, regardless of when the animations or drawing callback actually runs. All callbacks that run as part of rendering a frame will observe the same frame time so using the frame time also helps to synchronize effects that are performed by different callbacks.

Please note that the framework already takes care to process animations and drawing using the frame time as a stable time base. Most applications should not need to use the frame time information directly.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameTimeNanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time in nanoseconds when the frame started being rendered, in the [System.nanoTime()](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime())timebase. Divide this value by`1000000`to convert it to the [SystemClock.uptimeMillis()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base. |
