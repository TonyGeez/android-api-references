# ComposeShader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComposeShader

Kotlin| [Java](ComposeShader.md) 
| --- | --- |

```
open class ComposeShader : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Shader](Shader.md) ||
| | ↳ | [android.graphics.ComposeShader](ComposeShader.md) |

A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](Xfermode.md) subclass.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ComposeShader](ComposeShader.md))`(`shaderA:` ` [Shader](Shader.md)`, `shaderB:` ` [Shader](Shader.md)`, `blendMode:` ` [BlendMode](BlendMode.md)`)` Create a new compose shader, given shaders A, B, and a combining PorterDuff mode. |
| [ComposeShader](ComposeShader.md))`(`shaderA:` ` [Shader](Shader.md)`, `shaderB:` ` [Shader](Shader.md)`, `mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` Create a new compose shader, given shaders A, B, and a combining PorterDuff mode. |
| [ComposeShader](ComposeShader.md))`(`shaderA:` ` [Shader](Shader.md)`, `shaderB:` ` [Shader](Shader.md)`, `mode:` ` [Xfermode](Xfermode.md)`)` Create a new compose shader, given shaders A, B, and a combining mode. |

| Inherited functions ||
|---|---|
| From class [Shader](Shader.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](Shader.md))`(`localM:` ` [Matrix](Matrix.md)`)` <br /> Return true if the shader has a non-identity local matrix. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](Shader.md))`(`localM:` ` [Matrix](Matrix.md)?`)` <br /> Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

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
| `shaderA` | [Shader](Shader.md):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](Shader.md):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
| `blendMode` | [BlendMode](BlendMode.md):The blend mode that combines the colors from the two shaders. This value cannot be`null`. |
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
| `shaderA` | [Shader](Shader.md):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](Shader.md):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
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
| `shaderA` | [Shader](Shader.md):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](Shader.md):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
| `mode` | [Xfermode](Xfermode.md):The mode that combines the colors from the two shaders. If mode is null, then SRC_OVER is assumed. |
| --- | --- |
