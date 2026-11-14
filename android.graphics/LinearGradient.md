# LinearGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinearGradient

Kotlin| [Java](LinearGradient.md) 
| --- | --- |

```
open class LinearGradient : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Shader](Shader.md) ||
| | ↳ | [android.graphics.LinearGradient](LinearGradient.md) |

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinearGradient](LinearGradient.md))`(`x0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `color0:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tile:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a linear gradient along a line. |
| [LinearGradient](LinearGradient.md))`(`x0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`, `positions:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`, `tile:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a linear gradient along a line. |
| [LinearGradient](LinearGradient.md))`(`x0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `color0:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `color1:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `tile:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a linear gradient along a line. |
| [LinearGradient](LinearGradient.md))`(`x0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y0:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colors:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)`, `positions:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`, `tile:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a linear gradient along a line. |

| Inherited functions ||
|---|---|
| From class [Shader](Shader.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](Shader.md))`(`localM:` ` [Matrix](Matrix.md)`)` <br /> Return true if the shader has a non-identity local matrix. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](Shader.md))`(`localM:` ` [Matrix](Matrix.md)?`)` <br /> Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

## Public constructors

### LinearGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinearGradient(
    x0: Float, 
    y0: Float, 
    x1: Float, 
    y1: Float, 
    color0: Int, 
    color1: Int, 
    tile: Shader.TileMode)
```

Create a shader that draws a linear gradient along a line.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate for the start of the gradient line |
| `y0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate for the start of the gradient line |
| `x1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate for the end of the gradient line |
| --- | --- |
| `y1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate for the end of the gradient line |
| `color0` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sRGB color at the start of the gradient line. |
| `color1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sRGB color at the end of the gradient line. |
| --- | --- |
| `tile` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |

### LinearGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinearGradient(
    x0: Float, 
    y0: Float, 
    x1: Float, 
    y1: Float, 
    colors: IntArray, 
    positions: FloatArray?, 
    tile: Shader.TileMode)
```

Create a shader that draws a linear gradient along a line.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate for the start of the gradient line |
| `y0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate for the start of the gradient line |
| `x1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate for the end of the gradient line |
| --- | --- |
| `y1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate for the end of the gradient line |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):The sRGB colors to be distributed along the gradient line This value cannot be`null`. |
| `positions` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:May be null. The relative positions \[0..1\] of each corresponding color in the colors array. If this is null, the colors are distributed evenly along the gradient line. |
| --- | --- |
| `tile` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |

### LinearGradient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinearGradient(
    x0: Float, 
    y0: Float, 
    x1: Float, 
    y1: Float, 
    color0: Long, 
    color1: Long, 
    tile: Shader.TileMode)
```

Create a shader that draws a linear gradient along a line.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate for the start of the gradient line |
| `y0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate for the start of the gradient line |
| `x1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate for the end of the gradient line |
| --- | --- |
| `y1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate for the end of the gradient line |
| `color0` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color at the start of the gradient line. |
| `color1` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color at the end of the gradient line. |
| --- | --- |
| `tile` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the colors do not share the same [ColorSpace](ColorSpace.md) or do not use a valid one. |

### LinearGradient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinearGradient(
    x0: Float, 
    y0: Float, 
    x1: Float, 
    y1: Float, 
    colors: LongArray, 
    positions: FloatArray?, 
    tile: Shader.TileMode)
```

Create a shader that draws a linear gradient along a line.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate for the start of the gradient line |
| `y0` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate for the start of the gradient line |
| `x1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate for the end of the gradient line |
| --- | --- |
| `y1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate for the end of the gradient line |
| `colors` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html):The colors to be distributed along the gradient line This value cannot be`null`. |
| `positions` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:May be null. The relative positions \[0..1\] of each corresponding color in the colors array. If this is null, the colors are distributed evenly along the gradient line. |
| --- | --- |
| `tile` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if there are less than two colors, the colors do not share the same [ColorSpace](ColorSpace.md) or do not use a valid one, or`positions`is not`null`and has a different length from`colors`. |
