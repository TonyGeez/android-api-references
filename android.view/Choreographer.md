# Choreographer

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Choreographer

Kotlin| [Java](Choreographer.md) 
| --- | --- |

```
class Choreographer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.Choreographer](Choreographer.md) |

Coordinates the timing of animations, input and drawing.

The choreographer receives timing pulses (such as vertical synchronization) from the display subsystem then schedules work to occur as part of rendering the next display frame.

Applications typically interact with the choreographer indirectly using higher level abstractions in the animation framework or the view hierarchy. Here are some examples of things you can do using the higher-level APIs.

- To post an animation to be processed on a regular time basis synchronized with display frame rendering, use [android.animation.ValueAnimator#start](../android.animation/ValueAnimator.md)).
- To post a [Runnable](../java.lang/Runnable.md) to be invoked once at the beginning of the next display frame, use [View.postOnAnimation](View.md)).
- To post a [Runnable](../java.lang/Runnable.md) to be invoked once at the beginning of the next display frame after a delay, use [View.postOnAnimationDelayed](View.md)).
- To post a call to [View.invalidate()](View.md))to occur once at the beginning of the next display frame, use [View.postInvalidateOnAnimation()](View.md))or [View.postInvalidateOnAnimation(int, int, int, int)](View.md)).
- To ensure that the contents of a [View](View.md) scroll smoothly and are drawn in sync with display frame rendering, do nothing. This already happens automatically. [View.onDraw](View.md))will be called at the appropriate time.

However, there are a few cases where you might want to use the functions of the choreographer directly in your application. Here are some examples.

- If your application does its rendering in a different thread, possibly using GL, or does not use the animation framework or view hierarchy at all and you want to ensure that it is appropriately synchronized with the display, then use [Choreographer.postFrameCallback](Choreographer.md)).
- ... and that's about it.

Each [Looper](../android.os/Looper.md) thread has its own choreographer. Other threads can post callbacks to run on the choreographer but they will run on the [Looper](../android.os/Looper.md) to which the choreographer belongs.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [FrameCallback](../android/view/Choreographer.FrameCallback.md) Implement this interface to receive a callback when a new display frame is being rendered. |
| | [FrameData](../android/view/Choreographer.FrameData.md) The payload for [VsyncCallback](../android/view/Choreographer.VsyncCallback.md) which includes frame information such as when the frame started being rendered, and multiple possible frame timelines and their information including deadline and expected present time. |
| | [FrameTimeline](../android/view/Choreographer.FrameTimeline.md) Holds data that describes one possible VSync frame event to render at. |
| --- | --- |
| abstract | [VsyncCallback](../android/view/Choreographer.VsyncCallback.md) Implement this interface to receive a callback to start the next frame. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Choreographer](Choreographer.md)! | [getInstance](Choreographer.md))`()` Gets the choreographer for the calling thread. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postFrameCallback](Choreographer.md))`(`callback:` ` [Choreographer.FrameCallback](../android/view/Choreographer.FrameCallback.md)!`)` Posts a frame callback to run on the next frame. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postFrameCallbackDelayed](Choreographer.md))`(`callback:` ` [Choreographer.FrameCallback](../android/view/Choreographer.FrameCallback.md)!`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Posts a frame callback to run on the next frame after the specified delay. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postVsyncCallback](Choreographer.md))`(`callback:` ` [Choreographer.VsyncCallback](../android/view/Choreographer.VsyncCallback.md)`)` Posts a vsync callback to run on the next frame. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeFrameCallback](Choreographer.md))`(`callback:` ` [Choreographer.FrameCallback](../android/view/Choreographer.FrameCallback.md)!`)` Removes a previously posted frame callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeVsyncCallback](Choreographer.md))`(`callback:` ` [Choreographer.VsyncCallback](../android/view/Choreographer.VsyncCallback.md)?`)` Removes a previously posted vsync callback. |
| --- | --- |

## Public methods

### getInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): Choreographer!
```

Gets the choreographer for the calling thread. Must be called from a thread that already has a [android.os.Looper](../android.os/Looper.md) associated with it.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------|
| [Choreographer](Choreographer.md)! | The choreographer for this thread. |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if the thread does not have a looper. |

### postFrameCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun postFrameCallback(callback: Choreographer.FrameCallback!): Unit
```

Posts a frame callback to run on the next frame.

The callback runs once then is automatically removed.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Choreographer.FrameCallback](../android/view/Choreographer.FrameCallback.md)!:The frame callback to run during the next frame. |

**See Also**

- [#postFrameCallbackDelayed](Choreographer.md))
- [#removeFrameCallback](Choreographer.md)) 

### postFrameCallbackDelayed

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun postFrameCallbackDelayed(
    callback: Choreographer.FrameCallback!, 
    delayMillis: Long
): Unit
```

Posts a frame callback to run on the next frame after the specified delay.

The callback runs once then is automatically removed.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Choreographer.FrameCallback](../android/view/Choreographer.FrameCallback.md)!:The frame callback to run during the next frame. |
| `delayMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The delay time in milliseconds. |

**See Also**

- [#postFrameCallback](Choreographer.md))
- [#removeFrameCallback](Choreographer.md)) 

### postVsyncCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun postVsyncCallback(callback: Choreographer.VsyncCallback): Unit
```

Posts a vsync callback to run on the next frame.

The callback runs once then is automatically removed.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Choreographer.VsyncCallback](../android/view/Choreographer.VsyncCallback.md):The vsync callback to run during the next frame. This value cannot be`null`. |

**See Also**

- [#removeVsyncCallback](Choreographer.md)) 

### removeFrameCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeFrameCallback(callback: Choreographer.FrameCallback!): Unit
```

Removes a previously posted frame callback.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Choreographer.FrameCallback](../android/view/Choreographer.FrameCallback.md)!:The frame callback to remove. |

**See Also**

- [#postFrameCallback](Choreographer.md))
- [#postFrameCallbackDelayed](Choreographer.md)) 

### removeVsyncCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeVsyncCallback(callback: Choreographer.VsyncCallback?): Unit
```

Removes a previously posted vsync callback.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Choreographer.VsyncCallback](../android/view/Choreographer.VsyncCallback.md)?:The vsync callback to remove. This value may be`null`. |

**See Also**

- [#postVsyncCallback](Choreographer.md))
