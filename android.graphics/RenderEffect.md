Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderEffect

Kotlin | [Java](RenderEffect.md)
| --- | --- |

```
class RenderEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.RenderEffect](RenderEffect.md) |

Intermediate rendering step used to render drawing commands with a corresponding visual effect. A RenderEffect can be configured on a RenderNode through setRenderEffect and will be applied when drawn through drawRenderNode. Additionally a RenderEffect can be applied to a View's backing RenderNode through setRenderEffect

## Summary

| Public methods ||
|---|---|
| static [RenderEffect](RenderEffect.md) | createBitmapEffect Create a RenderEffect that renders the contents of the input Bitmap. |
| static [RenderEffect](RenderEffect.md) | createBitmapEffect Create a RenderEffect that renders the contents of the input Bitmap. |
| static [RenderEffect](RenderEffect.md) | createBlendModeEffect Create a RenderEffect that is a composition of 2 other RenderEffect instances combined by the specified BlendMode |
| --- | --- |
| static [RenderEffect](RenderEffect.md) | createBlurEffect Create a RenderEffect that blurs the contents of the optional input RenderEffect with the specified radius along the x and y axis. |
| static [RenderEffect](RenderEffect.md) | createBlurEffect Create a RenderEffect that blurs the contents of the RenderNode that this RenderEffect is installed on with the specified radius along the x and y axis. |
| static [RenderEffect](RenderEffect.md) | createChainEffect Create a RenderEffect that composes 'inner' with 'outer', such that the results of 'inner' are treated as the source bitmap passed to 'outer', i. |
| --- | --- |
| static [RenderEffect](RenderEffect.md) | createColorFilterEffect Create a RenderEffect that applies the color filter to the contents of the RenderNode that this RenderEffect is installed on |
| static [RenderEffect](RenderEffect.md) | createColorFilterEffect Create a RenderEffect that applies the color filter to the provided RenderEffect |
| static [RenderEffect](RenderEffect.md) | createOffsetEffect Create a RenderEffect instance that will offset the drawing content by the provided x and y offset. |
| --- | --- |
| static [RenderEffect](RenderEffect.md) | createOffsetEffect Create a RenderEffect instance with the provided x and y offset |
| static [RenderEffect](RenderEffect.md) | createRuntimeShaderEffect Create a RenderEffect that executes the provided RuntimeShader and passes the contents of the RenderNode that this RenderEffect is installed on as an input to the shader. |
| static [RenderEffect](RenderEffect.md) | createShaderEffect Create a RenderEffect that renders the contents of the input Shader. |
| --- | --- |

## Public methods

### createBitmapEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmapEffect(bitmap: Bitmap): RenderEffect
```

Create a RenderEffect that renders the contents of the input Bitmap. This is useful to create an input for other RenderEffect types such as createBlurEffect or createColorFilterEffect

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](Bitmap.md): The source bitmap to be rendered by the created RenderEffect This value cannot be `null`. |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createBitmapEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmapEffect(
    bitmap: Bitmap, 
    src: Rect?, 
    dst: Rect
): RenderEffect
```

Create a RenderEffect that renders the contents of the input Bitmap. This is useful to create an input for other RenderEffect types such as createBlurEffect or createColorFilterEffect

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](Bitmap.md): The source bitmap to be rendered by the created RenderEffect This value cannot be `null`. |
| `src` | [Rect](Rect.md)?: Optional subset of the bitmap to be part of the rendered output. If null is provided, the entire bitmap bounds are used. |
| `dst` | [Rect](Rect.md): Bounds of the destination which the bitmap is translated and scaled to be drawn into within the bounds of the RenderNode this RenderEffect is installed on. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createBlendModeEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBlendModeEffect(
    dst: RenderEffect, 
    src: RenderEffect, 
    blendMode: BlendMode
): RenderEffect
```

Create a RenderEffect that is a composition of 2 other RenderEffect instances combined by the specified BlendMode

| Parameters ||
|---|---|
| `dst` | [RenderEffect](RenderEffect.md): The Dst pixels used in blending. This value cannot be `null`. |
| `src` | [RenderEffect](RenderEffect.md): The Src pixels used in blending. This value cannot be `null`. |
| `blendMode` | [BlendMode](BlendMode.md): The BlendMode to be used to combine colors from the two RenderEffects. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

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

Create a RenderEffect that blurs the contents of the optional input RenderEffect with the specified radius along the x and y axis. If no input RenderEffect is provided then all drawing commands issued with a RenderNode that this RenderEffect is installed in will be blurred

| Parameters ||
|---|---|
| `radiusX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Radius of blur along the X axis |
| `radiusY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Radius of blur along the Y axis |
| `inputEffect` | [RenderEffect](RenderEffect.md): Input RenderEffect that provides the content to be blurred, can be null to indicate that the drawing commands on the RenderNode are to be blurred instead of the input RenderEffect |
| --- | --- |
| `edgeTreatment` | [Shader.TileMode](../android/graphics/Shader.TileMode.md): Policy for how to blur content near edges of the blur kernel. This value cannot be `null`. |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createBlurEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBlurEffect(
    radiusX: Float, 
    radiusY: Float, 
    edgeTreatment: Shader.TileMode
): RenderEffect
```

Create a RenderEffect that blurs the contents of the RenderNode that this RenderEffect is installed on with the specified radius along the x and y axis.

| Parameters ||
|---|---|
| `radiusX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Radius of blur along the X axis |
| `radiusY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Radius of blur along the Y axis |
| `edgeTreatment` | [Shader.TileMode](../android/graphics/Shader.TileMode.md): Policy for how to blur content near edges of the blur kernel. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createChainEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createChainEffect(
    outer: RenderEffect, 
    inner: RenderEffect
): RenderEffect
```

Create a RenderEffect that composes 'inner' with 'outer', such that the results of 'inner' are treated as the source bitmap passed to 'outer', i.e.

```kotlin
<code>result = outer(inner(source))
  </code>
```
Consumers should favor explicit chaining of RenderEffect instances at creation time rather than using chain effect. Chain effects are useful for situations where the input or output are provided from elsewhere and the input or output RenderEffect need to be changed.

<br />

| Parameters ||
|---|---|
| `outer` | [RenderEffect](RenderEffect.md): RenderEffect that consumes the output of `inner` as its input. This value cannot be `null`. |
| `inner` | [RenderEffect](RenderEffect.md): RenderEffect that is consumed as input by `outer` This value cannot be `null`. |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createColorFilterEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createColorFilterEffect(colorFilter: ColorFilter): RenderEffect
```

Create a RenderEffect that applies the color filter to the contents of the RenderNode that this RenderEffect is installed on

| Parameters ||
|---|---|
| `colorFilter` | [ColorFilter](ColorFilter.md): ColorFilter applied to the content in the input RenderEffect. This value cannot be `null`. |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createColorFilterEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createColorFilterEffect(
    colorFilter: ColorFilter, 
    renderEffect: RenderEffect
): RenderEffect
```

Create a RenderEffect that applies the color filter to the provided RenderEffect

| Parameters ||
|---|---|
| `colorFilter` | [ColorFilter](ColorFilter.md): ColorFilter applied to the content in the input RenderEffect. This value cannot be `null`. |
| `renderEffect` | [RenderEffect](RenderEffect.md): Source to be transformed by the specified ColorFilter This value cannot be `null`. |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createOffsetEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createOffsetEffect(
    offsetX: Float, 
    offsetY: Float
): RenderEffect
```

Create a RenderEffect instance that will offset the drawing content by the provided x and y offset.

| Parameters ||
|---|---|
| `offsetX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): offset along the x axis in pixels |
| `offsetY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): offset along the y axis in pixels |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createOffsetEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createOffsetEffect(
    offsetX: Float, 
    offsetY: Float, 
    input: RenderEffect
): RenderEffect
```

Create a RenderEffect instance with the provided x and y offset

| Parameters ||
|---|---|
| `offsetX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): offset along the x axis in pixels |
| `offsetY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): offset along the y axis in pixels |
| `input` | [RenderEffect](RenderEffect.md): target RenderEffect used to render in the offset coordinates. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createRuntimeShaderEffect

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createRuntimeShaderEffect(
    shader: RuntimeShader, 
    uniformShaderName: String
): RenderEffect
```

Create a RenderEffect that executes the provided RuntimeShader and passes the contents of the RenderNode that this RenderEffect is installed on as an input to the shader.

| Parameters ||
|---|---|
| `shader` | [RuntimeShader](RuntimeShader.md): the runtime shader that will bind the inputShaderName to the RenderEffect input. This value cannot be `null`. |
| `uniformShaderName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the uniform name defined in the RuntimeShader's program to which the contents of the RenderNode will be bound. This value cannot be `null`. |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |

### createShaderEffect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createShaderEffect(shader: Shader): RenderEffect
```

Create a RenderEffect that renders the contents of the input Shader. This is useful to create an input for other RenderEffect types such as createBlurEffect createBlurEffect or createColorFilterEffect.

| Parameters ||
|---|---|
| `shader` | [Shader](Shader.md): This value cannot be `null`. |

| Return ||
|---|---|
| RenderEffect | This value cannot be `null`. |
