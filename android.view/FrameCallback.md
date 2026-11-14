# Choreographer.FrameCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FrameCallback

Kotlin| [Java](../android/view/Choreographer.FrameCallback.md) 
| --- | --- |

```
interface FrameCallback
```

| [android.view.Choreographer.FrameCallback](../android/view/Choreographer.FrameCallback.md) |

Implement this interface to receive a callback when a new display frame is being rendered. The callback is invoked on the [Looper](../android/os/Looper.md) thread to which the [Choreographer](../android/view/Choreographer.md) is attached.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doFrame](../android/view/Choreographer.FrameCallback.md))`(`frameTimeNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Called when a new display frame is being rendered. |

## Public methods

### doFrame

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun doFrame(frameTimeNanos: Long): Unit
```

Called when a new display frame is being rendered.

This method provides the time in nanoseconds when the frame started being rendered. The frame time provides a stable time base for synchronizing animations and drawing. It should be used instead of [SystemClock.uptimeMillis()](../android/os/SystemClock.md))or [System.nanoTime()](../java/lang/System.md))for animations and drawing in the UI. Using the frame time helps to reduce inter-frame jitter because the frame time is fixed at the time the frame was scheduled to start, regardless of when the animations or drawing callback actually runs. All callbacks that run as part of rendering a frame will observe the same frame time so using the frame time also helps to synchronize effects that are performed by different callbacks.

Please note that the framework already takes care to process animations and drawing using the frame time as a stable time base. Most applications should not need to use the frame time information directly.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameTimeNanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time in nanoseconds when the frame started being rendered, in the [System.nanoTime()](../java/lang/System.md))timebase. Divide this value by`1000000`to convert it to the [SystemClock.uptimeMillis()](../android/os/SystemClock.md))time base. |
