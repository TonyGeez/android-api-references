# Shader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Shader

Kotlin| [Java](Shader.md) 
| --- | --- |

```
open class Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Shader](Shader.md) |

| Known Direct Subclasses [BitmapShader](BitmapShader.md), [ComposeShader](ComposeShader.md), [LinearGradient](LinearGradient.md), [RadialGradient](RadialGradient.md), [RuntimeShader](RuntimeShader.md), [SweepGradient](SweepGradient.md) |--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BitmapShader](BitmapShader.md) | Shader used to draw a bitmap as a texture. | | [ComposeShader](ComposeShader.md) | A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](Xfermode.md) subclass. | | [LinearGradient](LinearGradient.md) | <br /> | | [RadialGradient](RadialGradient.md) | <br /> | | [RuntimeShader](RuntimeShader.md) | A [RuntimeShader](RuntimeShader.md) calculates a per-pixel color based on the output of a user defined Android Graphics Shading Language (AGSL) function. | | [SweepGradient](SweepGradient.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Shader is the base class for objects that return horizontal spans of colors during drawing. A subclass of Shader is installed in a Paint calling paint.setShader(shader). After that any object (other than a bitmap) that is drawn with that paint will get its color(s) from the shader.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------|
| | [TileMode](../android/graphics/Shader.TileMode.md) <br /> |

| Public constructors ||
|------------------------------------------------------------------------------------------------------|---|
| [Shader](Shader.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](Shader.md))`(`localM:` ` [Matrix](Matrix.md)`)` Return true if the shader has a non-identity local matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](Shader.md))`(`localM:` ` [Matrix](Matrix.md)?`)` Set the shader's local matrix. |

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
| `localM` | [Matrix](Matrix.md):Set to the local matrix of the shader, if the shader's matrix is non-null. |

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
| `localM` | [Matrix](Matrix.md)?:The shader's new local matrix, or null to specify identity |
