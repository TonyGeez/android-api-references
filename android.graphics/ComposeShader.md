# ComposeShader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComposeShader

Kotlin| [Java](https://developer.android.com/reference/android/graphics/ComposeShader "View this page in Java") 

```
open class ComposeShader : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader) ||
| | ↳ | [android.graphics.ComposeShader](https://developer.android.com/reference/kotlin/android/graphics/ComposeShader#) |

A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Xfermode) subclass.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ComposeShader](https://developer.android.com/reference/kotlin/android/graphics/ComposeShader#ComposeShader(android.graphics.Shader,%20android.graphics.Shader,%20android.graphics.BlendMode))`(`shaderA:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`, `shaderB:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`, `blendMode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode)`)` Create a new compose shader, given shaders A, B, and a combining PorterDuff mode. |
| [ComposeShader](https://developer.android.com/reference/kotlin/android/graphics/ComposeShader#ComposeShader(android.graphics.Shader,%20android.graphics.Shader,%20android.graphics.PorterDuff.Mode))`(`shaderA:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`, `shaderB:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`, `mode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode)`)` Create a new compose shader, given shaders A, B, and a combining PorterDuff mode. |
| [ComposeShader](https://developer.android.com/reference/kotlin/android/graphics/ComposeShader#ComposeShader(android.graphics.Shader,%20android.graphics.Shader,%20android.graphics.Xfermode))`(`shaderA:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`, `shaderB:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`, `mode:` ` [Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Xfermode)`)` Create a new compose shader, given shaders A, B, and a combining mode. |

| Inherited functions ||
|---|---|
| From class [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](https://developer.android.com/reference/kotlin/android/graphics/Shader#getLocalMatrix(android.graphics.Matrix))`(`localM:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)`)` <br /> Return true if the shader has a non-identity local matrix. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](https://developer.android.com/reference/kotlin/android/graphics/Shader#setLocalMatrix(android.graphics.Matrix))`(`localM:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?`)` <br /> Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

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
| `shaderA` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
| `blendMode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode):The blend mode that combines the colors from the two shaders. This value cannot be`null`. |

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
| `shaderA` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
| `mode` | [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode):The PorterDuff mode that combines the colors from the two shaders. This value cannot be`null`. |

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
| `shaderA` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):The colors from this shader are seen as the "dst" by the mode This value cannot be`null`. |
| `shaderB` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):The colors from this shader are seen as the "src" by the mode This value cannot be`null`. |
| `mode` | [Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Xfermode):The mode that combines the colors from the two shaders. If mode is null, then SRC_OVER is assumed. |
