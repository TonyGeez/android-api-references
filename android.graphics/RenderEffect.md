Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderEffect

Kotlin | [Java](../android/graphics/RenderEffect.md)
| --- | --- |

```
class RenderEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.RenderEffect](../android/graphics/RenderEffect.md) |

Intermediate rendering step used to render drawing commands with a corresponding visual effect. A `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` can be configured on a `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` through `https://developer.android.com/reference/kotlin/android/graphics/RenderNode#setRenderEffect(android.graphics.RenderEffect)` and will be applied when drawn through `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawRenderNode(android.graphics.RenderNode)`. Additionally a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` can be applied to a View's backing RenderNode through `https://developer.android.com/reference/kotlin/android/view/View.html#setRenderEffect(android.graphics.RenderEffect)`

## Summary

| Public methods ||
|---|---|
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBitmapEffect(android.graphics.Bitmap)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that renders the contents of the input `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBitmapEffect(android.graphics.Bitmap,%20android.graphics.Rect,%20android.graphics.Rect)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap, src: https://developer.android.com/reference/kotlin/android/graphics/Rect?, dst: https://developer.android.com/reference/kotlin/android/graphics/Rect)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that renders the contents of the input `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlendModeEffect(android.graphics.RenderEffect,%20android.graphics.RenderEffect,%20android.graphics.BlendMode)(dst: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#, src: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#, blendMode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that is a composition of 2 other `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` instances combined by the specified `https://developer.android.com/reference/kotlin/android/graphics/BlendMode` |
| --- | --- |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)(radiusX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, radiusY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, inputEffect: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#, edgeTreatment: https://developer.android.com/reference/kotlin/android/graphics/Shader.TileMode)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that blurs the contents of the optional input RenderEffect with the specified radius along the x and y axis. |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.Shader.TileMode)(radiusX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, radiusY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, edgeTreatment: https://developer.android.com/reference/kotlin/android/graphics/Shader.TileMode)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that blurs the contents of the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` that this RenderEffect is installed on with the specified radius along the x and y axis. |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createChainEffect(android.graphics.RenderEffect,%20android.graphics.RenderEffect)(outer: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#, inner: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that composes 'inner' with 'outer', such that the results of 'inner' are treated as the source bitmap passed to 'outer', i. |
| --- | --- |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createColorFilterEffect(android.graphics.ColorFilter)(colorFilter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that applies the color filter to the contents of the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` that this RenderEffect is installed on |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createColorFilterEffect(android.graphics.ColorFilter,%20android.graphics.RenderEffect)(colorFilter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter, renderEffect: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that applies the color filter to the provided RenderEffect |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createOffsetEffect(kotlin.Float,%20kotlin.Float)(offsetX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, offsetY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` instance that will offset the drawing content by the provided x and y offset. |
| --- | --- |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createOffsetEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect)(offsetX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, offsetY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, input: https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` instance with the provided x and y offset |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createRuntimeShaderEffect(android.graphics.RuntimeShader,%20kotlin.String)(shader: https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader, uniformShaderName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that executes the provided `https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader` and passes the contents of the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` that this RenderEffect is installed on as an input to the shader. |
| static [RenderEffect](../android/graphics/RenderEffect.md) | `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createShaderEffect(android.graphics.Shader)(shader: https://developer.android.com/reference/kotlin/android/graphics/Shader)` Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that renders the contents of the input `https://developer.android.com/reference/kotlin/android/graphics/Shader`. |
| --- | --- |

## Public methods

### createBitmapEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmapEffect(bitmap: Bitmap): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that renders the contents of the input `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. This is useful to create an input for other `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` types such as `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)` or `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createColorFilterEffect(android.graphics.ColorFilter,%20android.graphics.RenderEffect)`

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](../android/graphics/Bitmap.md): The source bitmap to be rendered by the created `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createBitmapEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmapEffect(
    bitmap: Bitmap, 
    src: Rect?, 
    dst: Rect
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that renders the contents of the input `https://developer.android.com/reference/kotlin/android/graphics/Bitmap`. This is useful to create an input for other `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` types such as `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)` or `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createColorFilterEffect(android.graphics.ColorFilter,%20android.graphics.RenderEffect)`

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](../android/graphics/Bitmap.md): The source bitmap to be rendered by the created `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` This value cannot be `null`. |
| `src` | [Rect](../android/graphics/Rect.md)?: Optional subset of the bitmap to be part of the rendered output. If null is provided, the entire bitmap bounds are used. |
| `dst` | [Rect](../android/graphics/Rect.md): Bounds of the destination which the bitmap is translated and scaled to be drawn into within the bounds of the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` this RenderEffect is installed on. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createBlendModeEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBlendModeEffect(
    dst: RenderEffect, 
    src: RenderEffect, 
    blendMode: BlendMode
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that is a composition of 2 other `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` instances combined by the specified `https://developer.android.com/reference/kotlin/android/graphics/BlendMode`

| Parameters ||
|---|---|
| `dst` | [RenderEffect](../android/graphics/RenderEffect.md): The Dst pixels used in blending. This value cannot be `null`. |
| `src` | [RenderEffect](../android/graphics/RenderEffect.md): The Src pixels used in blending. This value cannot be `null`. |
| `blendMode` | [BlendMode](../android/graphics/BlendMode.md): The `https://developer.android.com/reference/kotlin/android/graphics/BlendMode` to be used to combine colors from the two `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#`s. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createBlurEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBlurEffect(
    radiusX: Float, 
    radiusY: Float, 
    inputEffect: RenderEffect, 
    edgeTreatment: Shader.TileMode
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that blurs the contents of the optional input RenderEffect with the specified radius along the x and y axis. If no input RenderEffect is provided then all drawing commands issued with a `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` that this RenderEffect is installed in will be blurred

| Parameters ||
|---|---|
| `radiusX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Radius of blur along the X axis |
| `radiusY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Radius of blur along the Y axis |
| `inputEffect` | [RenderEffect](../android/graphics/RenderEffect.md): Input RenderEffect that provides the content to be blurred, can be null to indicate that the drawing commands on the RenderNode are to be blurred instead of the input RenderEffect |
| --- | --- |
| `edgeTreatment` | [Shader.TileMode](../android/graphics/Shader.TileMode.md): Policy for how to blur content near edges of the blur kernel. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createBlurEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBlurEffect(
    radiusX: Float, 
    radiusY: Float, 
    edgeTreatment: Shader.TileMode
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that blurs the contents of the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` that this RenderEffect is installed on with the specified radius along the x and y axis.

| Parameters ||
|---|---|
| `radiusX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Radius of blur along the X axis |
| `radiusY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Radius of blur along the Y axis |
| `edgeTreatment` | [Shader.TileMode](../android/graphics/Shader.TileMode.md): Policy for how to blur content near edges of the blur kernel. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createChainEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createChainEffect(
    outer: RenderEffect, 
    inner: RenderEffect
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that composes 'inner' with 'outer', such that the results of 'inner' are treated as the source bitmap passed to 'outer', i.e.

```kotlin
<code>result = outer(inner(source))
  </code>
```
Consumers should favor explicit chaining of `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` instances at creation time rather than using chain effect. Chain effects are useful for situations where the input or output are provided from elsewhere and the input or output `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` need to be changed.

<br />

| Parameters ||
|---|---|
| `outer` | [RenderEffect](../android/graphics/RenderEffect.md): `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that consumes the output of `inner` as its input. This value cannot be `null`. |
| `inner` | [RenderEffect](../android/graphics/RenderEffect.md): `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that is consumed as input by `outer` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createColorFilterEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createColorFilterEffect(colorFilter: ColorFilter): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that applies the color filter to the contents of the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` that this RenderEffect is installed on

| Parameters ||
|---|---|
| `colorFilter` | [ColorFilter](../android/graphics/ColorFilter.md): ColorFilter applied to the content in the input RenderEffect. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createColorFilterEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createColorFilterEffect(
    colorFilter: ColorFilter, 
    renderEffect: RenderEffect
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that applies the color filter to the provided RenderEffect

| Parameters ||
|---|---|
| `colorFilter` | [ColorFilter](../android/graphics/ColorFilter.md): ColorFilter applied to the content in the input RenderEffect. This value cannot be `null`. |
| `renderEffect` | [RenderEffect](../android/graphics/RenderEffect.md): Source to be transformed by the specified `https://developer.android.com/reference/kotlin/android/graphics/ColorFilter` This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createOffsetEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createOffsetEffect(
    offsetX: Float, 
    offsetY: Float
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` instance that will offset the drawing content by the provided x and y offset.

| Parameters ||
|---|---|
| `offsetX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): offset along the x axis in pixels |
| `offsetY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): offset along the y axis in pixels |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createOffsetEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createOffsetEffect(
    offsetX: Float, 
    offsetY: Float, 
    input: RenderEffect
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` instance with the provided x and y offset

| Parameters ||
|---|---|
| `offsetX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): offset along the x axis in pixels |
| `offsetY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): offset along the y axis in pixels |
| `input` | [RenderEffect](../android/graphics/RenderEffect.md): target RenderEffect used to render in the offset coordinates. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createRuntimeShaderEffect

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createRuntimeShaderEffect(
    shader: RuntimeShader, 
    uniformShaderName: String
): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that executes the provided `https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader` and passes the contents of the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode` that this RenderEffect is installed on as an input to the shader.

| Parameters ||
|---|---|
| `shader` | [RuntimeShader](../android/graphics/RuntimeShader.md): the runtime shader that will bind the inputShaderName to the RenderEffect input. This value cannot be `null`. |
| `uniformShaderName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the uniform name defined in the RuntimeShader's program to which the contents of the RenderNode will be bound. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |

### createShaderEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createShaderEffect(shader: Shader): RenderEffect
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` that renders the contents of the input `https://developer.android.com/reference/kotlin/android/graphics/Shader`. This is useful to create an input for other `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` types such as `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)` `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createBlurEffect(kotlin.Float,%20kotlin.Float,%20android.graphics.RenderEffect,%20android.graphics.Shader.TileMode)` or `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#createColorFilterEffect(android.graphics.ColorFilter,%20android.graphics.RenderEffect)`.

| Parameters ||
|---|---|
| `shader` | [Shader](../android/graphics/Shader.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RenderEffect#` | This value cannot be `null`. |
