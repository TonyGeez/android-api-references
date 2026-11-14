# HardwareBufferRenderer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HardwareBufferRenderer

Kotlin| [Java](https://developer.android.com/reference/android/graphics/HardwareBufferRenderer "View this page in Java") 
| --- | --- |

```
open class HardwareBufferRenderer : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#) |

Creates an instance of a hardware-accelerated renderer. This is used to render a scene built from [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode) s to an output [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#). There can be as many HardwareBufferRenderer instances as desired.

### Resources \& lifecycle

All HardwareBufferRenderer and [HardwareRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareRenderer) instances share a common render thread. Therefore HardwareBufferRenderer will share common resources and GPU utilization with hardware accelerated rendering initiated by the UI thread of an application. The render thread contains the GPU context \& resources necessary to do GPU-accelerated rendering. As such, the first HardwareBufferRenderer created comes with the cost of also creating the associated GPU contexts, however each incremental HardwareBufferRenderer thereafter is fairly cheap. The expected usage is to have a HardwareBufferRenderer instance for every active [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#).
This is useful in situations where a scene built with [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode) s can be consumed directly by the system compositor through [SurfaceControl.Transaction.setBuffer(SurfaceControl, HardwareBuffer)](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction.html#setBuffer(android.view.SurfaceControl,%20android.hardware.HardwareBuffer)). HardwareBufferRenderer will never clear contents before each draw invocation so previous contents in the [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) target will be preserved across renders.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [RenderRequest](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderRequest) Sets the parameters that can be used to control a render request for a [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#). |
| | [RenderResult](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderResult) Class that contains data regarding the result of the render request. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#HardwareBufferRenderer(android.hardware.HardwareBuffer))`(`buffer:` ` [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#)`)` Creates a new instance of [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#) with the provided [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) as the output of the rendered scene. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#close())`()` Releases the resources associated with this [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#) instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#isClosed())`()` Returns if the [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#) has already been closed. |
| open [HardwareBufferRenderer.RenderRequest](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderRequest) | [obtainRenderRequest](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#obtainRenderRequest())`()` Returns a [RenderRequest](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderRequest) that can be used to render into the provided [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentRoot](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#setContentRoot(android.graphics.RenderNode))`(`content:` ` [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode)?`)` Sets the content root to render. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLightSourceAlpha](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#setLightSourceAlpha(kotlin.Float,%20kotlin.Float))`(`ambientShadowAlpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `spotShadowAlpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Configures the ambient \& spot shadow alphas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLightSourceGeometry](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#setLightSourceGeometry(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`lightX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the center of the light source. |
| --- | --- |

## Public constructors

### HardwareBufferRenderer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HardwareBufferRenderer(buffer: HardwareBuffer)
```

Creates a new instance of [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#) with the provided [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) as the output of the rendered scene.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#):This value cannot be`null`. |

## Public methods

### close

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Releases the resources associated with this [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#) instance. \*\*Note\*\* this does not call [HardwareBuffer.close()](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#close())on the provided [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) instance

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### isClosed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClosed(): Boolean
```

Returns if the [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#) has already been closed. That is [HardwareBufferRenderer.close()](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#close())has been invoked.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the [HardwareBufferRenderer](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#) has been closed, false otherwise. |

### obtainRenderRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun obtainRenderRequest(): HardwareBufferRenderer.RenderRequest
```

Returns a [RenderRequest](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderRequest) that can be used to render into the provided [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#). This is used to synchronize the RenderNode content provided by [setContentRoot(android.graphics.RenderNode)](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#setContentRoot(android.graphics.RenderNode)).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HardwareBufferRenderer.RenderRequest](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderRequest) | An instance of [RenderRequest](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderRequest). The instance may be reused for every frame, so the caller should not hold onto it for longer than a single render request. This value cannot be`null`. |

### setContentRoot

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentRoot(content: RenderNode?): Unit
```

Sets the content root to render. It is not necessary to call this whenever the content recording changes. Any mutations to the RenderNode content, or any of the RenderNodes contained within the content node, will be applied whenever a new [RenderRequest](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderRequest) is issued via [obtainRenderRequest()](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#obtainRenderRequest())and [RenderRequest.draw(Executor,](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer.RenderRequest#draw(java.util.concurrent.Executor,%20java.util.function.Consumer)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `content` | [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode)?:The content to set as the root RenderNode. If null the content root is removed and the renderer will draw nothing. |

### setLightSourceAlpha

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLightSourceAlpha(
    ambientShadowAlpha: Float, 
    spotShadowAlpha: Float
): Unit
```

Configures the ambient \& spot shadow alphas. This is the alpha used when the shadow has max alpha, and ramps down from the values provided to zero.

These values are typically provided by the current theme, see [android.R.attr#spotShadowAlpha](https://developer.android.com/reference/kotlin/android/R.attr.html#spotShadowAlpha:kotlin.Int) and [android.R.attr#ambientShadowAlpha](https://developer.android.com/reference/kotlin/android/R.attr.html#ambientShadowAlpha:kotlin.Int).

This must be set at least once along with [setLightSourceGeometry(float,float,float,float)](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#setLightSourceGeometry(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))before shadows will work.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ambientShadowAlpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha for the ambient shadow. If unsure, a reasonable default is 0.039f. Value is between 0.0f and 1.0f inclusive |
| `spotShadowAlpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha for the spot shadow. If unsure, a reasonable default is 0.19f. Value is between 0.0f and 1.0f inclusive |

### setLightSourceGeometry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLightSourceGeometry(
    lightX: Float, 
    lightY: Float, 
    lightZ: Float, 
    lightRadius: Float
): Unit
```

Sets the center of the light source. The light source point controls the directionality and shape of shadows rendered by RenderNode Z \& elevation.

The light source should be setup both as part of initial configuration, and whenever the window moves to ensure the light source stays anchored in display space instead of in window space.

This must be set at least once along with [setLightSourceAlpha(float,float)](https://developer.android.com/reference/kotlin/android/graphics/HardwareBufferRenderer#setLightSourceAlpha(kotlin.Float,%20kotlin.Float))before shadows will work.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lightX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X position of the light source. If unsure, a reasonable default is 'displayWidth / 2f - windowLeft'. |
| `lightY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y position of the light source. If unsure, a reasonable default is '0 - windowTop' |
| `lightZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Z position of the light source. Must be \>= 0. If unsure, a reasonable default is 600dp. Value is 0.0f or greater |
| --- | --- |
| `lightRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The radius of the light source. Smaller radius will have sharper edges, larger radius will have softer shadows. If unsure, a reasonable default is 800 dp. Value is 0.0f or greater |
