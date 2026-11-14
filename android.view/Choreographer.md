# Choreographer

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Choreographer

Kotlin| [Java](https://developer.android.com/reference/android/view/Choreographer "View this page in Java") 
| --- | --- |

```
class Choreographer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.Choreographer](https://developer.android.com/reference/kotlin/android/view/Choreographer#) |

Coordinates the timing of animations, input and drawing.

The choreographer receives timing pulses (such as vertical synchronization) from the display subsystem then schedules work to occur as part of rendering the next display frame.

Applications typically interact with the choreographer indirectly using higher level abstractions in the animation framework or the view hierarchy. Here are some examples of things you can do using the higher-level APIs.

- To post an animation to be processed on a regular time basis synchronized with display frame rendering, use [android.animation.ValueAnimator#start](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.html#start()).
- To post a [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#) to be invoked once at the beginning of the next display frame, use [View.postOnAnimation](https://developer.android.com/reference/kotlin/android/view/View#postOnAnimation(java.lang.Runnable)).
- To post a [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#) to be invoked once at the beginning of the next display frame after a delay, use [View.postOnAnimationDelayed](https://developer.android.com/reference/kotlin/android/view/View#postOnAnimationDelayed(java.lang.Runnable,%20kotlin.Long)).
- To post a call to [View.invalidate()](https://developer.android.com/reference/kotlin/android/view/View#invalidate())to occur once at the beginning of the next display frame, use [View.postInvalidateOnAnimation()](https://developer.android.com/reference/kotlin/android/view/View#postInvalidateOnAnimation())or [View.postInvalidateOnAnimation(int, int, int, int)](https://developer.android.com/reference/kotlin/android/view/View#postInvalidateOnAnimation(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)).
- To ensure that the contents of a [View](https://developer.android.com/reference/kotlin/android/view/View) scroll smoothly and are drawn in sync with display frame rendering, do nothing. This already happens automatically. [View.onDraw](https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas))will be called at the appropriate time.

However, there are a few cases where you might want to use the functions of the choreographer directly in your application. Here are some examples.

- If your application does its rendering in a different thread, possibly using GL, or does not use the animation framework or view hierarchy at all and you want to ensure that it is appropriately synchronized with the display, then use [Choreographer.postFrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#postFrameCallback(android.view.Choreographer.FrameCallback)).
- ... and that's about it.

Each [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) thread has its own choreographer. Other threads can post callbacks to run on the choreographer but they will run on the [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) to which the choreographer belongs.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback) Implement this interface to receive a callback when a new display frame is being rendered. |
| | [FrameData](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameData) The payload for [VsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback) which includes frame information such as when the frame started being rendered, and multiple possible frame timelines and their information including deadline and expected present time. |
| | [FrameTimeline](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameTimeline) Holds data that describes one possible VSync frame event to render at. |
| --- | --- |
| abstract | [VsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback) Implement this interface to receive a callback to start the next frame. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Choreographer](https://developer.android.com/reference/kotlin/android/view/Choreographer#)! | [getInstance](https://developer.android.com/reference/kotlin/android/view/Choreographer#getInstance())`()` Gets the choreographer for the calling thread. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postFrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#postFrameCallback(android.view.Choreographer.FrameCallback))`(`callback:` ` [Choreographer.FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback)!`)` Posts a frame callback to run on the next frame. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postFrameCallbackDelayed](https://developer.android.com/reference/kotlin/android/view/Choreographer#postFrameCallbackDelayed(android.view.Choreographer.FrameCallback,%20kotlin.Long))`(`callback:` ` [Choreographer.FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback)!`, `delayMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Posts a frame callback to run on the next frame after the specified delay. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postVsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#postVsyncCallback(android.view.Choreographer.VsyncCallback))`(`callback:` ` [Choreographer.VsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback)`)` Posts a vsync callback to run on the next frame. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeFrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#removeFrameCallback(android.view.Choreographer.FrameCallback))`(`callback:` ` [Choreographer.FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback)!`)` Removes a previously posted frame callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeVsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#removeVsyncCallback(android.view.Choreographer.VsyncCallback))`(`callback:` ` [Choreographer.VsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback)?`)` Removes a previously posted vsync callback. |
| --- | --- |

## Public methods

### getInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): Choreographer!
```

Gets the choreographer for the calling thread. Must be called from a thread that already has a [android.os.Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) associated with it.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------|
| [Choreographer](https://developer.android.com/reference/kotlin/android/view/Choreographer#)! | The choreographer for this thread. |

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
| `callback` | [Choreographer.FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback)!:The frame callback to run during the next frame. |

**See Also**

- [#postFrameCallbackDelayed](https://developer.android.com/reference/kotlin/android/view/Choreographer#postFrameCallbackDelayed(android.view.Choreographer.FrameCallback,%20kotlin.Long))
- [#removeFrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#removeFrameCallback(android.view.Choreographer.FrameCallback)) 

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
| `callback` | [Choreographer.FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback)!:The frame callback to run during the next frame. |
| `delayMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The delay time in milliseconds. |

**See Also**

- [#postFrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#postFrameCallback(android.view.Choreographer.FrameCallback))
- [#removeFrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#removeFrameCallback(android.view.Choreographer.FrameCallback)) 

### postVsyncCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun postVsyncCallback(callback: Choreographer.VsyncCallback): Unit
```

Posts a vsync callback to run on the next frame.

The callback runs once then is automatically removed.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Choreographer.VsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback):The vsync callback to run during the next frame. This value cannot be`null`. |

**See Also**

- [#removeVsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#removeVsyncCallback(android.view.Choreographer.VsyncCallback)) 

### removeFrameCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeFrameCallback(callback: Choreographer.FrameCallback!): Unit
```

Removes a previously posted frame callback.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Choreographer.FrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.FrameCallback)!:The frame callback to remove. |

**See Also**

- [#postFrameCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#postFrameCallback(android.view.Choreographer.FrameCallback))
- [#postFrameCallbackDelayed](https://developer.android.com/reference/kotlin/android/view/Choreographer#postFrameCallbackDelayed(android.view.Choreographer.FrameCallback,%20kotlin.Long)) 

### removeVsyncCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeVsyncCallback(callback: Choreographer.VsyncCallback?): Unit
```

Removes a previously posted vsync callback.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Choreographer.VsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer.VsyncCallback)?:The vsync callback to remove. This value may be`null`. |

**See Also**

- [#postVsyncCallback](https://developer.android.com/reference/kotlin/android/view/Choreographer#postVsyncCallback(android.view.Choreographer.VsyncCallback))
