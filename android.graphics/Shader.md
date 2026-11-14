# Shader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Shader

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Shader "View this page in Java") 

```
open class Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader#) |

| Known Direct Subclasses [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader), [ComposeShader](https://developer.android.com/reference/kotlin/android/graphics/ComposeShader), [LinearGradient](https://developer.android.com/reference/kotlin/android/graphics/LinearGradient), [RadialGradient](https://developer.android.com/reference/kotlin/android/graphics/RadialGradient), [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader), [SweepGradient](https://developer.android.com/reference/kotlin/android/graphics/SweepGradient) |--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader) | Shader used to draw a bitmap as a texture. | | [ComposeShader](https://developer.android.com/reference/kotlin/android/graphics/ComposeShader) | A subclass of shader that returns the composition of two other shaders, combined by an [android.graphics.Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Xfermode) subclass. | | [LinearGradient](https://developer.android.com/reference/kotlin/android/graphics/LinearGradient) | <br /> | | [RadialGradient](https://developer.android.com/reference/kotlin/android/graphics/RadialGradient) | <br /> | | [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader) | A [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader) calculates a per-pixel color based on the output of a user defined Android Graphics Shading Language (AGSL) function. | | [SweepGradient](https://developer.android.com/reference/kotlin/android/graphics/SweepGradient) | <br /> | |

Shader is the base class for objects that return horizontal spans of colors during drawing. A subclass of Shader is installed in a Paint calling paint.setShader(shader). After that any object (other than a bitmap) that is drawn with that paint will get its color(s) from the shader.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------|
| | [TileMode](https://developer.android.com/reference/kotlin/android/graphics/Shader.TileMode) <br /> |

| Public constructors ||
|------------------------------------------------------------------------------------------------------|---|
| [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader#Shader())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](https://developer.android.com/reference/kotlin/android/graphics/Shader#getLocalMatrix(android.graphics.Matrix))`(`localM:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)`)` Return true if the shader has a non-identity local matrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](https://developer.android.com/reference/kotlin/android/graphics/Shader#setLocalMatrix(android.graphics.Matrix))`(`localM:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?`)` Set the shader's local matrix. |

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
| `localM` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix):Set to the local matrix of the shader, if the shader's matrix is non-null. |

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
| `localM` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?:The shader's new local matrix, or null to specify identity |
