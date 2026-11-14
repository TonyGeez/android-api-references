# HardwareRenderer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HardwareRenderer

Kotlin| [Java](../android/graphics/HardwareRenderer.md) 
| --- | --- |

```
open class HardwareRenderer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.HardwareRenderer](../android/graphics/HardwareRenderer.md) |

Creates an instance of a hardware-accelerated renderer. This is used to render a scene built from [RenderNode](../android/graphics/RenderNode.md)'s to an output [android.view.Surface](../android/view/Surface.md). There can be as many HardwareRenderer instances as desired.

### Resources \& lifecycle

All HardwareRenderer instances share a common render thread. The render thread contains the GPU context \& resources necessary to do GPU-accelerated rendering. As such, the first HardwareRenderer created comes with the cost of also creating the associated GPU contexts, however each incremental HardwareRenderer thereafter is fairly cheap. The expected usage is to have a HardwareRenderer instance for every active [Surface](../android/view/Surface.md). For example when an Activity shows a Dialog the system internally will use 2 hardware renderers, both of which may be drawing at the same time.

NOTE: Due to the shared, cooperative nature of the render thread it is critical that any [Surface](../android/view/Surface.md) used must have a prompt, reliable consuming side. System-provided consumers such as [android.view.SurfaceView](../android/view/SurfaceView.md), [android.view.Window#takeSurface(SurfaceHolder.Callback2)](../android/view/Window.md)), or [android.view.TextureView](../android/view/TextureView.md) all fit this requirement. However if custom consumers are used such as when using [SurfaceTexture](../android/graphics/SurfaceTexture.md) or [android.media.ImageReader](../android/media/ImageReader.md) it is the app's responsibility to ensure that they consume updates promptly and rapidly. Failure to do so will cause the render thread to stall on that surface, blocking all HardwareRenderer instances.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [FrameRenderRequest](../android/graphics/HardwareRenderer.FrameRenderRequest.md) Sets the parameters that can be used to control a render request for a [HardwareRenderer](../android/graphics/HardwareRenderer.md). |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_CONTEXT_IS_STOPPED](../android/graphics/HardwareRenderer.md) The hardware renderer has been set to a "stopped" state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_FRAME_DROPPED](../android/graphics/HardwareRenderer.md) The content was synced but the renderer has declined to produce a frame in this vsync interval. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_LOST_SURFACE_REWARD_IF_FOUND](../android/graphics/HardwareRenderer.md) The hardware renderer no longer has a valid [android.view.Surface](../android/view/Surface.md) to render to. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_OK](../android/graphics/HardwareRenderer.md) Nothing interesting to report. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_REDRAW_REQUESTED](../android/graphics/HardwareRenderer.md) The renderer is requesting a redraw. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HardwareRenderer](../android/graphics/HardwareRenderer.md))`()` Creates a new instance of a HardwareRenderer. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearContent](../android/graphics/HardwareRenderer.md))`()` Destroys all the display lists associated with the current rendering content. |
| open [HardwareRenderer.FrameRenderRequest](../android/graphics/HardwareRenderer.FrameRenderRequest.md) | [createRenderRequest](../android/graphics/HardwareRenderer.md))`()` Returns a [FrameRenderRequest](../android/graphics/HardwareRenderer.FrameRenderRequest.md) that can be used to render a new frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](../android/graphics/HardwareRenderer.md))`()` Destroys the rendering context of this HardwareRenderer. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDrawingEnabled](../android/graphics/HardwareRenderer.md))`()` Returns true if HardwareRender will produce output. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpaque](../android/graphics/HardwareRenderer.md))`()` Whether or not the renderer is set to be opaque. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyFramePending](../android/graphics/HardwareRenderer.md))`()` Notifies the hardware renderer that a call to [FrameRenderRequest.syncAndDraw()](../android/graphics/HardwareRenderer.FrameRenderRequest.md))will be coming soon. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentRoot](../android/graphics/HardwareRenderer.md))`(`content:` ` [RenderNode](../android/graphics/RenderNode.md)?`)` Sets the content root to render. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDrawingEnabled](../android/graphics/HardwareRenderer.md))`(`drawingEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Toggles whether or not HardwareRenderer will produce drawing output globally in the current process. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLightSourceAlpha](../android/graphics/HardwareRenderer.md))`(`ambientShadowAlpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `spotShadowAlpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Configures the ambient \& spot shadow alphas. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLightSourceGeometry](../android/graphics/HardwareRenderer.md))`(`lightX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the center of the light source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](../android/graphics/HardwareRenderer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets a name for this renderer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](../android/graphics/HardwareRenderer.md))`(`opaque:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Change the HardwareRenderer's opacity. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSurface](../android/graphics/HardwareRenderer.md))`(`surface:` ` [Surface](../android/view/Surface.md)?`)` The surface to render into. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/graphics/HardwareRenderer.md))`()` Resumes rendering into the surface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](../android/graphics/HardwareRenderer.md))`()` Hard stops rendering into the surface. |
| --- | --- |

## Constants

### SYNC_CONTEXT_IS_STOPPED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_CONTEXT_IS_STOPPED: Int
```

The hardware renderer has been set to a "stopped" state. If this is returned then the rendering content has been synced, however a frame was not produced. 

 Value: 4

### SYNC_FRAME_DROPPED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_FRAME_DROPPED: Int
```

The content was synced but the renderer has declined to produce a frame in this vsync interval. This can happen if a frame was already drawn in this vsync or if the renderer is outrunning the frame consumer. The renderer will internally re-schedule itself to render a frame in the next vsync signal, so the caller does not need to do anything in response to this signal. 

 Value: 8

### SYNC_LOST_SURFACE_REWARD_IF_FOUND

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_LOST_SURFACE_REWARD_IF_FOUND: Int
```

The hardware renderer no longer has a valid [android.view.Surface](../android/view/Surface.md) to render to. This can happen if [Surface.release()](../android/view/Surface.md))was called. The user should no longer attempt to call syncAndDraw until a new surface has been provided by calling setSurface.

Spoiler: the reward is GPU-accelerated drawing, better find that Surface! 

 Value: 2

### SYNC_OK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_OK: Int
```

Nothing interesting to report. Sync \& draw kicked off 

 Value: 0

### SYNC_REDRAW_REQUESTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_REDRAW_REQUESTED: Int
```

The renderer is requesting a redraw. This can occur if there's an animation that's running in the RenderNode tree and the hardware renderer is unable to self-animate.

If this is returned from syncAndDraw the expectation is that syncAndDraw will be called again on the next vsync signal. 

 Value: 1

## Public constructors

### HardwareRenderer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HardwareRenderer()
```

Creates a new instance of a HardwareRenderer. The HardwareRenderer will default to opaque with no light source configured.

## Public methods

### clearContent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearContent(): Unit
```

Destroys all the display lists associated with the current rendering content. This includes releasing a reference to the current content root RenderNode. It will therefore be necessary to call [setContentRoot(android.graphics.RenderNode)](../android/graphics/HardwareRenderer.md))in order to resume rendering after calling this, along with re-recording the display lists for the RenderNode tree.

It is recommended, but not necessary, to use this in combination with lifecycle events such as [Activity.onStop()](../android/app/Activity.md))and [Activity.onStart()](../android/app/Activity.md))or in response to [android.content.ComponentCallbacks2#onTrimMemory(int)](../android/content/ComponentCallbacks2.md))signals such as [android.content.ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN](../android/content/ComponentCallbacks2.md) See also [stop()](../android/graphics/HardwareRenderer.md)). 

### createRenderRequest

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createRenderRequest(): HardwareRenderer.FrameRenderRequest
```

Returns a [FrameRenderRequest](../android/graphics/HardwareRenderer.FrameRenderRequest.md) that can be used to render a new frame. This is used to synchronize the RenderNode content provided by [setContentRoot(android.graphics.RenderNode)](../android/graphics/HardwareRenderer.md))with the RenderThread and then renders a single frame to the Surface set with [setSurface(android.view.Surface)](../android/graphics/HardwareRenderer.md)).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HardwareRenderer.FrameRenderRequest](../android/graphics/HardwareRenderer.FrameRenderRequest.md) | An instance of [FrameRenderRequest](../android/graphics/HardwareRenderer.FrameRenderRequest.md). The instance may be reused for every frame, so the caller should not hold onto it for longer than a single render request. This value cannot be`null`. |

### destroy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun destroy(): Unit
```

Destroys the rendering context of this HardwareRenderer. This destroys the resources associated with this renderer and releases the currently set [Surface](../android/view/Surface.md). This must be called when this HardwareRenderer is no longer needed.

The renderer may be restored from this state by setting a new [Surface](../android/view/Surface.md), setting new rendering content with [setContentRoot(android.graphics.RenderNode)](../android/graphics/HardwareRenderer.md)), and resuming rendering by issuing a new [FrameRenderRequest](../android/graphics/HardwareRenderer.FrameRenderRequest.md).

It is recommended to call this in response to callbacks such as [android.view.SurfaceHolder.Callback#surfaceDestroyed(SurfaceHolder)](../android/view/SurfaceHolder.Callback.md)).

Note that if there are any outstanding frame commit callbacks they may never being invoked if the frame was deferred to a later vsync. 

### isDrawingEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isDrawingEnabled(): Boolean
```

Returns true if HardwareRender will produce output. This value is global to the process and affects all uses of HardwareRenderer, including those created by the system such as those used by the View tree when using hardware accelerated rendering. Default is true in all production environments, but may be false in testing-focused emulators or if [setDrawingEnabled(boolean)](../android/graphics/HardwareRenderer.md))is used. 

### isOpaque

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpaque(): Boolean
```

Whether or not the renderer is set to be opaque. See [setOpaque(boolean)](../android/graphics/HardwareRenderer.md))

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the renderer is opaque, false otherwise |

### notifyFramePending

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyFramePending(): Unit
```

Notifies the hardware renderer that a call to [FrameRenderRequest.syncAndDraw()](../android/graphics/HardwareRenderer.FrameRenderRequest.md))will be coming soon. This is used to help schedule when RenderThread-driven animations will happen as the renderer wants to avoid producing more than one frame per vsync signal. 

### setContentRoot

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentRoot(content: RenderNode?): Unit
```

Sets the content root to render. It is not necessary to call this whenever the content recording changes. Any mutations to the RenderNode content, or any of the RenderNode's contained within the content node, will be applied whenever a new [FrameRenderRequest](../android/graphics/HardwareRenderer.FrameRenderRequest.md) is issued via [createRenderRequest()](../android/graphics/HardwareRenderer.md))and [FrameRenderRequest.syncAndDraw()](../android/graphics/HardwareRenderer.FrameRenderRequest.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `content` | [RenderNode](../android/graphics/RenderNode.md)?:The content to set as the root RenderNode. If null the content root is removed and the renderer will draw nothing. |

### setDrawingEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDrawingEnabled(drawingEnabled: Boolean): Unit
```

Toggles whether or not HardwareRenderer will produce drawing output globally in the current process. This applies to all HardwareRenderer instances, including those created by the platform such as those used by the system for hardware accelerated View rendering. The capability to disable drawing output is intended for test environments, primarily headless ones. By setting this to false, tests that launch activities or interact with Views can be quicker with less RAM usage by skipping the final step of View drawing. All View lifecycle events will occur as normal, only the final step of rendering on the GPU to the display will be skipped. This can be toggled on and off at will, so screenshot tests can also run in this same environment by toggling drawing back on and forcing a frame to be drawn such as by calling view#invalidate(). Once drawn and the screenshot captured, this can then be turned back off. 

### setLightSourceAlpha

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLightSourceAlpha(
    ambientShadowAlpha: Float, 
    spotShadowAlpha: Float
): Unit
```

Configures the ambient \& spot shadow alphas. This is the alpha used when the shadow has max alpha, and ramps down from the values provided to zero.

These values are typically provided by the current theme, see [android.R.attr#spotShadowAlpha](../android/R.attr.md) and [android.R.attr#ambientShadowAlpha](../android/R.attr.md).

This must be set at least once along with [setLightSourceGeometry(float,float,float,float)](../android/graphics/HardwareRenderer.md))before shadows will work.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ambientShadowAlpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha for the ambient shadow. If unsure, a reasonable default is 0.039f. Value is between 0.0f and 1.0f inclusive |
| `spotShadowAlpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha for the spot shadow. If unsure, a reasonable default is 0.19f. Value is between 0.0f and 1.0f inclusive |

### setLightSourceGeometry

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLightSourceGeometry(
    lightX: Float, 
    lightY: Float, 
    lightZ: Float, 
    lightRadius: Float
): Unit
```

Sets the center of the light source. The light source point controls the directionality and shape of shadows rendered by RenderNode Z \& elevation.

The platform's recommendation is to set lightX to 'displayWidth / 2f - windowLeft', set lightY to 0 - windowTop, lightZ set to 600dp, and lightRadius to 800dp.

The light source should be setup both as part of initial configuration, and whenever the window moves to ensure the light source stays anchored in display space instead of in window space.

This must be set at least once along with [setLightSourceAlpha(float,float)](../android/graphics/HardwareRenderer.md))before shadows will work.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lightX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X position of the light source |
| `lightY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y position of the light source |
| `lightZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Z position of the light source. Must be \>= 0. |
| --- | --- |
| `lightRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The radius of the light source. Smaller radius will have sharper edges, larger radius will have softer shadows. |

### setName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setName(name: String): Unit
```

Sets a name for this renderer. This is used to identify this renderer instance when reporting debug information such as the per-window frame time metrics reported by 'adb shell dumpsys gfxinfo \[package\] framestats'

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The debug name to use for this HardwareRenderer instance This value cannot be`null`. |

### setOpaque

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOpaque(opaque: Boolean): Unit
```

Change the HardwareRenderer's opacity. Will take effect on the next frame produced.

If the renderer is set to opaque it is the app's responsibility to ensure that the content renders to every pixel of the Surface, otherwise corruption may result. Note that this includes ensuring that the first draw of any given pixel does not attempt to blend against the destination. If this is false then the hardware renderer will clear to transparent at the start of every frame.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `opaque` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the content rendered is opaque, false if the renderer should clear to transparent before rendering |

### setSurface

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSurface(surface: Surface?): Unit
```

The surface to render into. The surface is assumed to be associated with the display and as such is still driven by vsync signals such as those from [android.view.Choreographer](../android/view/Choreographer.md) and that it has a native refresh rate matching that of the display's (typically 60hz).

NOTE: Due to the shared, cooperative nature of the render thread it is critical that any [Surface](../android/view/Surface.md) used must have a prompt, reliable consuming side. System-provided consumers such as [android.view.SurfaceView](../android/view/SurfaceView.md), [android.view.Window#takeSurface(SurfaceHolder.Callback2)](../android/view/Window.md)), or [android.view.TextureView](../android/view/TextureView.md) all fit this requirement. However if custom consumers are used such as when using [SurfaceTexture](../android/graphics/SurfaceTexture.md) or [android.media.ImageReader](../android/media/ImageReader.md) it is the app's responsibility to ensure that they consume updates promptly and rapidly. Failure to do so will cause the render thread to stall on that surface, blocking all HardwareRenderer instances.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [Surface](../android/view/Surface.md)?:The surface to render into. If null then rendering will be stopped. If non-null then [Surface.isValid()](../android/view/Surface.md))must be true. |

### start

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Resumes rendering into the surface. Any pending rendering requests will produce a new frame at the next vsync signal.

This is useful in combination with lifecycle events such as [Activity.onStart()](../android/app/Activity.md)). See [stop()](../android/graphics/HardwareRenderer.md))for stopping rendering. 

### stop

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Hard stops rendering into the surface. If the renderer is stopped it will block any attempt to render. Calls to [FrameRenderRequest.syncAndDraw()](../android/graphics/HardwareRenderer.FrameRenderRequest.md))will still sync over the latest rendering content, however they will not render and instead [SYNC_CONTEXT_IS_STOPPED](../android/graphics/HardwareRenderer.md) will be returned.

This is useful in combination with lifecycle events such as [Activity.onStop()](../android/app/Activity.md)). See [start()](../android/graphics/HardwareRenderer.md))for resuming rendering.
