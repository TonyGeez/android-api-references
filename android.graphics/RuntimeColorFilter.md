Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RuntimeColorFilter

Kotlin | [Java](https://developer.android.com/reference/android/graphics/RuntimeColorFilter "View this page in Java")

```
open class RuntimeColorFilter : ColorFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter) ||
| | ↳ | [android.graphics.RuntimeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#) |

A `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#` calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function.

This AGSL function takes in an input color to be operated on. This color is in sRGB and the \* output is also interpreted as sRGB. The AGSL function signature expects a single input \* of color (packed as a half4 or float4 or vec4).

```kotlin
vec4 main(half4 in_color);
  
```

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#RuntimeColorFilter(kotlin.String)(agsl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Creates a new RuntimeColorFilter. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setColorUniform(kotlin.String,%20android.graphics.Color)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, color: https://developer.android.com/reference/kotlin/android/graphics/Color)` Sets the uniform color value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setColorUniform(kotlin.String,%20kotlin.Int)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the uniform color value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setColorUniform(kotlin.String,%20kotlin.Long)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the uniform color value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setFloatUniform(kotlin.String,%20kotlin.Float)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, value2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, value2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, value3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, value2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, value3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, value4: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setFloatUniform(kotlin.String,%20kotlin.FloatArray)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, values: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setInputColorFilter(kotlin.String,%20android.graphics.ColorFilter)(filterName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, colorFilter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter)` Assigns the uniform color filter to the provided color filter parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setInputShader(kotlin.String,%20android.graphics.Shader)(shaderName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, shader: https://developer.android.com/reference/kotlin/android/graphics/Shader)` Assigns the uniform shader to the provided shader parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setInputXfermode(kotlin.String,%20android.graphics.RuntimeXfermode)(xfermodeName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, xfermode: https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode)` Assigns the uniform xfermode to the provided xfermode parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setIntUniform(kotlin.String,%20kotlin.Int)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value3: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value4: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the uniform value corresponding to this color filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter#setIntUniform(kotlin.String,%20kotlin.IntArray)(uniformName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, values: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Sets the uniform value corresponding to this color filter. |

## Public constructors

### RuntimeColorFilter

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RuntimeColorFilter(agsl: String)
```

Creates a new RuntimeColorFilter.

| Parameters ||
|---|---|
| `agsl` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The text of AGSL color filter program to run. This value cannot be `null`. |

## Public methods

### setColorUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorUniform(
    uniformName: String, 
    color: Color
): Unit
```

Sets the uniform color value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the color uniform declared in the AGSL program. This value cannot be `null`. |
| `color` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color): the provided sRGB color. This value cannot be `null`. |

### setColorUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorUniform(
    uniformName: String, 
    color: Int
): Unit
```

Sets the uniform color value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the color uniform declared in the AGSL program. This value cannot be `null`. |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the provided sRGB color |

### setColorUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorUniform(
    uniformName: String, 
    color: Long
): Unit
```

Sets the uniform color value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the color uniform declared in the AGSL program. This value cannot be `null`. |
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the provided sRGB color |

### setFloatUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloatUniform(
    uniformName: String, 
    value: Float
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than a float or float\[1\] then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |

### setFloatUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than a vec2 or float\[2\] then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |

### setFloatUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float, 
    value3: Float
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than a vec3 or float\[3\] then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |

### setFloatUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float, 
    value3: Float, 
    value4: Float
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than a vec4 or float\[4\] then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |

### setFloatUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFloatUniform(
    uniformName: String, 
    values: FloatArray
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than a float (for N=1), vecN, or float\[N\] where N is the length of the values param then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): This value cannot be `null`. |

### setInputColorFilter

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInputColorFilter(
    filterName: String, 
    colorFilter: ColorFilter
): Unit
```

Assigns the uniform color filter to the provided color filter parameter. If the shader program does not have a uniform color filter with that name then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `filterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |
| `colorFilter` | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter): filter passed into the AGSL program for sampling. This value cannot be `null`. |

### setInputShader

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInputShader(
    shaderName: String, 
    shader: Shader
): Unit
```

Assigns the uniform shader to the provided shader parameter. If the shader program does not have a uniform shader with that name then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `shaderName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |
| `shader` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader): shader passed into the AGSL program for sampling. This value cannot be `null`. |

### setInputXfermode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInputXfermode(
    xfermodeName: String, 
    xfermode: RuntimeXfermode
): Unit
```

Assigns the uniform xfermode to the provided xfermode parameter. If the shader program does not have a uniform xfermode with that name then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `xfermodeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |
| `xfermode` | [RuntimeXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode): filter passed into the AGSL program for sampling. This value cannot be `null`. |

### setIntUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntUniform(
    uniformName: String, 
    value: Int
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than an int or int\[1\] then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |

### setIntUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than an ivec2 or int\[2\] then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |

### setIntUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int, 
    value3: Int
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than an ivec3 or int\[3\] then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |

### setIntUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int, 
    value3: Int, 
    value4: Int
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than an ivec4 or int\[4\] then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |

### setIntUniform

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntUniform(
    uniformName: String, 
    values: IntArray
): Unit
```

Sets the uniform value corresponding to this color filter. If the effect does not have a uniform with that name or if the uniform is declared with a type other than an int (for N=1), ivecN, or int\[N\] where N is the length of the values param then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name matching the uniform declared in the AGSL program. This value cannot be `null`. |
| `values` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |
