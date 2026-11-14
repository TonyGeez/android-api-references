# ComposeShader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComposeShader

Kotlin| [Java](../android/graphics/ComposeShader.md) 
| --- | --- |

```
open class ComposeShader : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Shader](../android/graphics/Shader.md) ||
| | ↳ | [android.graphics.ComposeShader](../android/graphics/ComposeShader.md) |

A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](../android/graphics/Xfermode.md) subclass.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ComposeShader](../android/graphics/ComposeShader.md))`(`shaderA:` ` [Shader](../android/graphics/Shader.md)`, `shaderB:` ` [Shader](../android/graphics/Shader.md)`, `blendMode:` ` [BlendMode](../android/graphics/BlendMode.md)`)` Create a new compose shader, given shaders A, B, and a combining PorterDuff mode. |
| [ComposeShader](../android/graphics/ComposeShader.md))`(`shaderA:` ` [Shader](../android/graphics/Shader.md)`, `shaderB:` ` [Shader](../android/graphics/Shader.md)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` Create a new compose shader, given shaders A, B, and a combining PorterDuff mode. |
| [ComposeShader](../android/graphics/ComposeShader.md))`(`shaderA:` ` [Shader](../android/graphics/Shader.md)`, `shaderB:` ` [Shader](../android/graphics/Shader.md)`, `mode:` ` [Xfermode](../android/graphics/Xfermode.md)`)` Create a new compose shader, given shaders A, B, and a combining mode. |

| Inherited functions ||
|---|---|
| From class [Shader](../android/graphics/Shader.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](../android/graphics/Shader.md))`(`localM:` ` [Matrix](../android/graphics/Matrix.md)`)` <br /> Return true if the shader has a non-identity local matrix. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](../android/graphics/Shader.md))`(`localM:` ` [Matrix](../android/graphics/Matrix.md)?`)` <br /> Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

## Public constructors

### ComposeShader

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComposeShader(
    shaderA: Shader, 
    shaderB: Shader, 
    blendMode: BlendMode)
```

Create a new compose shader, given shaders A, B, and a combining PorterDuff mode. When the mode is applied, it will be given the result from shader A as its "dst", and the result from shader B as its "src".

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shaderA` | [Shader](../android/graphics/Shader.md):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](../android/graphics/Shader.md):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
| `blendMode` | [BlendMode](../android/graphics/BlendMode.md):The blend mode that combines the colors from the two shaders. This value cannot be`null`. |
| --- | --- |

### ComposeShader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComposeShader(
    shaderA: Shader, 
    shaderB: Shader, 
    mode: PorterDuff.Mode)
```

Create a new compose shader, given shaders A, B, and a combining PorterDuff mode. When the mode is applied, it will be given the result from shader A as its "dst", and the result from shader B as its "src".

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shaderA` | [Shader](../android/graphics/Shader.md):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](../android/graphics/Shader.md):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
| `mode` | [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md):The PorterDuff mode that combines the colors from the two shaders. This value cannot be`null`. |
| --- | --- |

### ComposeShader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComposeShader(
    shaderA: Shader, 
    shaderB: Shader, 
    mode: Xfermode)
```

Create a new compose shader, given shaders A, B, and a combining mode. When the mode is applied, it will be given the result from shader A as its "dst", and the result from shader B as its "src".

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shaderA` | [Shader](../android/graphics/Shader.md):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](../android/graphics/Shader.md):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
| `mode` | [Xfermode](../android/graphics/Xfermode.md):The mode that combines the colors from the two shaders. If mode is null, then SRC_OVER is assumed. |
| --- | --- |
