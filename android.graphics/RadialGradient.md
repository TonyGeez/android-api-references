# RadialGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RadialGradient

Kotlin| [Java](RadialGradient.md) 
| --- | --- |

```
open class RadialGradient : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Shader](Shader.md) ||
| | ↳ | [android.graphics.RadialGradient](RadialGradient.md) |

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RadialGradient](RadialGradient.md))`(`startX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colors:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)`, `stops:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`, `tileMode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a radial gradient given the start and end points as well as starting and ending radii. |
| [RadialGradient](RadialGradient.md))`(`centerX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edgeColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tileMode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a radial gradient given the center and radius. |
| [RadialGradient](RadialGradient.md))`(`centerX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colors:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`, `stops:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`, `tileMode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a radial gradient given the center and radius. |
| [RadialGradient](RadialGradient.md))`(`centerX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerColor:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `edgeColor:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `tileMode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a radial gradient given the center and radius. |
| [RadialGradient](RadialGradient.md))`(`centerX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colors:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)`, `stops:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`, `tileMode:` ` [Shader.TileMode](../android/graphics/Shader.TileMode.md)`)` Create a shader that draws a radial gradient given the center and radius. |

| Inherited functions ||
|---|---|
| From class [Shader](Shader.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](Shader.md))`(`localM:` ` [Matrix](Matrix.md)`)` <br /> Return true if the shader has a non-identity local matrix. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](Shader.md))`(`localM:` ` [Matrix](Matrix.md)?`)` <br /> Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

## Public constructors

### RadialGradient

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RadialGradient(
    startX: Float, 
    startY: Float, 
    startRadius: Float, 
    endX: Float, 
    endY: Float, 
    endRadius: Float, 
    colors: LongArray, 
    stops: FloatArray?, 
    tileMode: Shader.TileMode)
```

Create a shader that draws a radial gradient given the start and end points as well as starting and ending radii. The starting point is often referred to as the focal center and represents the starting circle of the radial gradient.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center of the starting circle of the radial gradient, often referred to as the focal point. |
| `startY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center of the starting circle of the radial gradient, often referred to as the focal point. |
| `startRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The radius of the starting circle of the radial gradient, often referred to as the focal radius. Must be greater than or equal to zero. Value is 0.0f or greater |
| --- | --- |
| `endX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center of the radius for the end circle of the radial gradient |
| `endY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center of the radius for the end circle of the radial gradient |
| `endRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The radius of the ending circle for this gradient. This must be strictly greater than zero. A radius value equal to zero is not allowed. Value is 0.0f or greater |
| --- | --- |
| `colors` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html):The colors to be distributed between the center and edge of the circle This value cannot be`null`. |
| `stops` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:May be`null`. Valid values are between`0.0f`and`1.0f`. The relative position of each corresponding color in the colors array. If`null`, colors are distributed evenly between the center and edge of the circle. |
| `tileMode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | In one of the following circumstances: - There are less than two colors - The colors do not share the same [ColorSpace](ColorSpace.md) - The colors do not use a valid [ColorSpace](ColorSpace.md) - The`stops`parameter is not`null`and has a different length from`colors`. - The`startRadius`is negative - The`endRadius`is less than or equal to zero |

### RadialGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RadialGradient(
    centerX: Float, 
    centerY: Float, 
    radius: Float, 
    centerColor: Int, 
    edgeColor: Int, 
    tileMode: Shader.TileMode)
```

Create a shader that draws a radial gradient given the center and radius.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `centerX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center of the radius |
| `centerY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center of the radius |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Must be positive. The radius of the circle for this gradient |
| --- | --- |
| `centerColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sRGB color at the center of the circle. |
| `edgeColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sRGB color at the edge of the circle. |
| `tileMode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |
| --- | --- |

### RadialGradient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RadialGradient(
    centerX: Float, 
    centerY: Float, 
    radius: Float, 
    colors: IntArray, 
    stops: FloatArray?, 
    tileMode: Shader.TileMode)
```

Create a shader that draws a radial gradient given the center and radius.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `centerX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center of the radius |
| `centerY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center of the radius |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Must be positive. The radius of the circle for this gradient. |
| --- | --- |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):The sRGB colors to be distributed between the center and edge of the circle This value cannot be`null`. |
| `stops` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:May be`null`. Valid values are between`0.0f`and`1.0f`. The relative position of each corresponding color in the colors array. If`null`, colors are distributed evenly between the center and edge of the circle. |
| `tileMode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |
| --- | --- |

### RadialGradient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RadialGradient(
    centerX: Float, 
    centerY: Float, 
    radius: Float, 
    centerColor: Long, 
    edgeColor: Long, 
    tileMode: Shader.TileMode)
```

Create a shader that draws a radial gradient given the center and radius.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `centerX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center of the radius |
| `centerY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center of the radius |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Must be positive. The radius of the circle for this gradient |
| --- | --- |
| `centerColor` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color at the center of the circle. |
| `edgeColor` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color at the edge of the circle. |
| `tileMode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the colors do not share the same [ColorSpace](ColorSpace.md) or do not use a valid one. |

### RadialGradient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RadialGradient(
    centerX: Float, 
    centerY: Float, 
    radius: Float, 
    colors: LongArray, 
    stops: FloatArray?, 
    tileMode: Shader.TileMode)
```

Create a shader that draws a radial gradient given the center and radius.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `centerX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x-coordinate of the center of the radius |
| `centerY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y-coordinate of the center of the radius |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Must be positive. The radius of the circle for this gradient. |
| --- | --- |
| `colors` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html):The colors to be distributed between the center and edge of the circle This value cannot be`null`. |
| `stops` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:May be`null`. Valid values are between`0.0f`and`1.0f`. The relative position of each corresponding color in the colors array. If`null`, colors are distributed evenly between the center and edge of the circle. |
| `tileMode` | [Shader.TileMode](../android/graphics/Shader.TileMode.md):The Shader tiling mode This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if there are less than two colors, the colors do not share the same [ColorSpace](ColorSpace.md) or do not use a valid one, or`stops`is not`null`and has a different length from`colors`. |
