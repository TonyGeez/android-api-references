# HardwareBufferRenderer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HardwareBufferRenderer

Kotlin| [Java](HardwareBufferRenderer.md) 
| --- | --- |

```
open class HardwareBufferRenderer : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.HardwareBufferRenderer](HardwareBufferRenderer.md) |

Creates an instance of a hardware-accelerated renderer. This is used to render a scene built from [RenderNode](RenderNode.md) s to an output [HardwareBuffer](../android.hardware/HardwareBuffer.md). There can be as many HardwareBufferRenderer instances as desired.

### Resources \& lifecycle

All HardwareBufferRenderer and [HardwareRenderer](HardwareRenderer.md) instances share a common render thread. Therefore HardwareBufferRenderer will share common resources and GPU utilization with hardware accelerated rendering initiated by the UI thread of an application. The render thread contains the GPU context \& resources necessary to do GPU-accelerated rendering. As such, the first HardwareBufferRenderer created comes with the cost of also creating the associated GPU contexts, however each incremental HardwareBufferRenderer thereafter is fairly cheap. The expected usage is to have a HardwareBufferRenderer instance for every active [HardwareBuffer](../android.hardware/HardwareBuffer.md).
This is useful in situations where a scene built with [RenderNode](RenderNode.md) s can be consumed directly by the system compositor through [SurfaceControl.Transaction.setBuffer(SurfaceControl, HardwareBuffer)](../android/view/SurfaceControl.Transaction.md)). HardwareBufferRenderer will never clear contents before each draw invocation so previous contents in the [HardwareBuffer](../android.hardware/HardwareBuffer.md) target will be preserved across renders.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [RenderRequest](../android/graphics/HardwareBufferRenderer.RenderRequest.md) Sets the parameters that can be used to control a render request for a [HardwareBufferRenderer](HardwareBufferRenderer.md). |
| | [RenderResult](../android/graphics/HardwareBufferRenderer.RenderResult.md) Class that contains data regarding the result of the render request. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HardwareBufferRenderer](HardwareBufferRenderer.md))`(`buffer:` ` [HardwareBuffer](../android.hardware/HardwareBuffer.md)`)` Creates a new instance of [HardwareBufferRenderer](HardwareBufferRenderer.md) with the provided [HardwareBuffer](../android.hardware/HardwareBuffer.md) as the output of the rendered scene. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](HardwareBufferRenderer.md))`()` Releases the resources associated with this [HardwareBufferRenderer](HardwareBufferRenderer.md) instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](HardwareBufferRenderer.md))`()` Returns if the [HardwareBufferRenderer](HardwareBufferRenderer.md) has already been closed. |
| open [HardwareBufferRenderer.RenderRequest](../android/graphics/HardwareBufferRenderer.RenderRequest.md) | [obtainRenderRequest](HardwareBufferRenderer.md))`()` Returns a [RenderRequest](../android/graphics/HardwareBufferRenderer.RenderRequest.md) that can be used to render into the provided [HardwareBuffer](../android.hardware/HardwareBuffer.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentRoot](HardwareBufferRenderer.md))`(`content:` ` [RenderNode](RenderNode.md)?`)` Sets the content root to render. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLightSourceAlpha](HardwareBufferRenderer.md))`(`ambientShadowAlpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `spotShadowAlpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Configures the ambient \& spot shadow alphas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLightSourceGeometry](HardwareBufferRenderer.md))`(`lightX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `lightRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the center of the light source. |
| --- | --- |

## Public constructors

### HardwareBufferRenderer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HardwareBufferRenderer(buffer: HardwareBuffer)
```

Creates a new instance of [HardwareBufferRenderer](HardwareBufferRenderer.md) with the provided [HardwareBuffer](../android.hardware/HardwareBuffer.md) as the output of the rendered scene.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [HardwareBuffer](../android.hardware/HardwareBuffer.md):This value cannot be`null`. |

## Public methods

### close

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Releases the resources associated with this [HardwareBufferRenderer](HardwareBufferRenderer.md) instance. \*\*Note\*\* this does not call [HardwareBuffer.close()](../android.hardware/HardwareBuffer.md))on the provided [HardwareBuffer](../android.hardware/HardwareBuffer.md) instance

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### isClosed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClosed(): Boolean
```

Returns if the [HardwareBufferRenderer](HardwareBufferRenderer.md) has already been closed. That is [HardwareBufferRenderer.close()](HardwareBufferRenderer.md))has been invoked.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the [HardwareBufferRenderer](HardwareBufferRenderer.md) has been closed, false otherwise. |

### obtainRenderRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun obtainRenderRequest(): HardwareBufferRenderer.RenderRequest
```

Returns a [RenderRequest](../android/graphics/HardwareBufferRenderer.RenderRequest.md) that can be used to render into the provided [HardwareBuffer](../android.hardware/HardwareBuffer.md). This is used to synchronize the RenderNode content provided by [setContentRoot(android.graphics.RenderNode)](HardwareBufferRenderer.md)).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HardwareBufferRenderer.RenderRequest](../android/graphics/HardwareBufferRenderer.RenderRequest.md) | An instance of [RenderRequest](../android/graphics/HardwareBufferRenderer.RenderRequest.md). The instance may be reused for every frame, so the caller should not hold onto it for longer than a single render request. This value cannot be`null`. |

### setContentRoot

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentRoot(content: RenderNode?): Unit
```

Sets the content root to render. It is not necessary to call this whenever the content recording changes. Any mutations to the RenderNode content, or any of the RenderNodes contained within the content node, will be applied whenever a new [RenderRequest](../android/graphics/HardwareBufferRenderer.RenderRequest.md) is issued via [obtainRenderRequest()](HardwareBufferRenderer.md))and [RenderRequest.draw(Executor,](../android/graphics/HardwareBufferRenderer.RenderRequest.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `content` | [RenderNode](RenderNode.md)?:The content to set as the root RenderNode. If null the content root is removed and the renderer will draw nothing. |

### setLightSourceAlpha

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLightSourceAlpha(
    ambientShadowAlpha: Float, 
    spotShadowAlpha: Float
): Unit
```

Configures the ambient \& spot shadow alphas. This is the alpha used when the shadow has max alpha, and ramps down from the values provided to zero.

These values are typically provided by the current theme, see [android.R.attr#spotShadowAlpha](../android/R.attr.md) and [android.R.attr#ambientShadowAlpha](../android/R.attr.md).

This must be set at least once along with [setLightSourceGeometry(float,float,float,float)](HardwareBufferRenderer.md))before shadows will work.

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

This must be set at least once along with [setLightSourceAlpha(float,float)](HardwareBufferRenderer.md))before shadows will work.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lightX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X position of the light source. If unsure, a reasonable default is 'displayWidth / 2f - windowLeft'. |
| `lightY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y position of the light source. If unsure, a reasonable default is '0 - windowTop' |
| `lightZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Z position of the light source. Must be \>= 0. If unsure, a reasonable default is 600dp. Value is 0.0f or greater |
| --- | --- |
| `lightRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The radius of the light source. Smaller radius will have sharper edges, larger radius will have softer shadows. If unsure, a reasonable default is 800 dp. Value is 0.0f or greater |
