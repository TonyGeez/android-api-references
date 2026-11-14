# SweepGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SweepGradient

Kotlin| [Java](../android/graphics/SweepGradient.md) 
| --- | --- |

```
open class SweepGradient : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Shader](../android/graphics/Shader.md) ||
| | ↳ | [android.graphics.SweepGradient](../android/graphics/SweepGradient.md) |

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SweepGradient](../android/graphics/SweepGradient.md))`(`cx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `color0:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` A Shader that draws a sweep gradient around a center point. |
| [SweepGradient](../android/graphics/SweepGradient.md))`(`cx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`, `positions:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`)` A Shader that draws a sweep gradient around a center point. |
| [SweepGradient](../android/graphics/SweepGradient.md))`(`cx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `color0:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `color1:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` A Shader that draws a sweep gradient around a center point. |
| [SweepGradient](../android/graphics/SweepGradient.md))`(`cx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colors:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)`, `positions:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`)` A Shader that draws a sweep gradient around a center point. |

| Inherited functions ||
|---|---|
| From class [Shader](../android/graphics/Shader.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](../android/graphics/Shader.md))`(`localM:` ` [Matrix](../android/graphics/Matrix.md)`)` <br /> Return true if the shader has a non-identity local matrix. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](../android/graphics/Shader.md))`(`localM:` ` [Matrix](../android/graphics/Matrix.md)?`)` <br /> Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

## Public constructors

### SweepGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SweepGradient(
    cx: Float, 
    cy: Float, 
    color0: Int, 
    color1: Int)
```

A Shader that draws a sweep gradient around a center point.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `cx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center |
| `cy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center |
| `color0` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sRGB color to use at the start of the sweep |
| --- | --- |
| `color1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sRGB color to use at the end of the sweep |

### SweepGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SweepGradient(
    cx: Float, 
    cy: Float, 
    colors: IntArray, 
    positions: FloatArray?)
```

A Shader that draws a sweep gradient around a center point.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center |
| `cy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):The sRGB colors to be distributed between around the center. There must be at least 2 colors in the array. This value cannot be`null`. |
| --- | --- |
| `positions` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:May be NULL. The relative position of each corresponding color in the colors array, beginning with 0 and ending with 1.0. If the values are not monotonic, the drawing may produce unexpected results. If positions is NULL, then the colors are automatically spaced evenly. This value may be`null`. |

### SweepGradient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SweepGradient(
    cx: Float, 
    cy: Float, 
    color0: Long, 
    color1: Long)
```

A Shader that draws a sweep gradient around a center point.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------|
| `cx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center |
| `cy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center |
| `color0` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color to use at the start of the sweep |
| --- | --- |
| `color1` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color to use at the end of the sweep |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the colors do not share the same [ColorSpace](../android/graphics/ColorSpace.md) or do not use a valid one. |

### SweepGradient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SweepGradient(
    cx: Float, 
    cy: Float, 
    colors: LongArray, 
    positions: FloatArray?)
```

A Shader that draws a sweep gradient around a center point.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center |
| `cy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center |
| `colors` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html):The colors to be distributed between around the center. There must be at least 2 colors in the array. This value cannot be`null`. |
| --- | --- |
| `positions` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:May be NULL. The relative position of each corresponding color in the colors array, beginning with 0 and ending with 1.0. If the values are not monotonic, the drawing may produce unexpected results. If positions is NULL, then the colors are automatically spaced evenly. This value may be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if there are less than two colors, the colors do not share the same [ColorSpace](../android/graphics/ColorSpace.md) or do not use a valid one, or`positions`is not`null`and has a different length from`colors`. |
