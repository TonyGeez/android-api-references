# Shader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Shader

Kotlin| [Java](../android/graphics/Shader.md) 
| --- | --- |

```
open class Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Shader](../android/graphics/Shader.md) |

| Known Direct Subclasses [BitmapShader](../android/graphics/BitmapShader.md), [ComposeShader](../android/graphics/ComposeShader.md), [LinearGradient](../android/graphics/LinearGradient.md), [RadialGradient](../android/graphics/RadialGradient.md), [RuntimeShader](../android/graphics/RuntimeShader.md), [SweepGradient](../android/graphics/SweepGradient.md) |--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BitmapShader](../android/graphics/BitmapShader.md) | Shader used to draw a bitmap as a texture. | | [ComposeShader](../android/graphics/ComposeShader.md) | A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](../android/graphics/Xfermode.md) subclass. | | [LinearGradient](../android/graphics/LinearGradient.md) | <br /> | | [RadialGradient](../android/graphics/RadialGradient.md) | <br /> | | [RuntimeShader](../android/graphics/RuntimeShader.md) | A [RuntimeShader](../android/graphics/RuntimeShader.md) calculates a per-pixel color based on the output of a user defined Android Graphics Shading Language (AGSL) function. | | [SweepGradient](../android/graphics/SweepGradient.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Shader is the base class for objects that return horizontal spans of colors during drawing. A subclass of Shader is installed in a Paint calling paint.setShader(shader). After that any object (other than a bitmap) that is drawn with that paint will get its color(s) from the shader.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------|
| | [TileMode](../android/graphics/Shader.TileMode.md) <br /> |

| Public constructors ||
|------------------------------------------------------------------------------------------------------|---|
| [Shader](../android/graphics/Shader.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](../android/graphics/Shader.md))`(`localM:` ` [Matrix](../android/graphics/Matrix.md)`)` Return true if the shader has a non-identity local matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](../android/graphics/Shader.md))`(`localM:` ` [Matrix](../android/graphics/Matrix.md)?`)` Set the shader's local matrix. |

## Public constructors

### Shader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Shader()
```

**Deprecated:** *Use subclass constructors directly instead.*

## Public methods

### getLocalMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalMatrix(localM: Matrix): Boolean
```

Return true if the shader has a non-identity local matrix.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localM` | [Matrix](../android/graphics/Matrix.md):Set to the local matrix of the shader, if the shader's matrix is non-null. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the shader has a non-identity local matrix |

### setLocalMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocalMatrix(localM: Matrix?): Unit
```

Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `localM` | [Matrix](../android/graphics/Matrix.md)?:The shader's new local matrix, or null to specify identity |
