# RuntimeShader

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RuntimeShader

Kotlin| [Java](https://developer.android.com/reference/android/graphics/RuntimeShader "View this page in Java") 
| --- | --- |

```
open class RuntimeShader : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader) ||
| | ↳ | [android.graphics.RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#) |

A [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#) calculates a per-pixel color based on the output of a user defined Android Graphics Shading Language (AGSL) function.

### Android Graphics Shading Language

The AGSL syntax is very similar to OpenGL ES Shading Language, but there are some important differences that are highlighted here. Most of these differences are summed up in one basic fact:**With GPU shading languages, you are programming a stage of the GPU pipeline. With AGSL, you are programming a stage of the [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) or [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode) drawing pipeline.**

In particular, a GLSL fragment shader controls the entire behavior of the GPU between the rasterizer and the blending hardware. That shader does all of the work to compute a color, and the color it generates is exactly what is fed to the blending stage of the pipeline.

In contrast, AGSL functions exist as part of a larger pipeline. When you issue a [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) drawing operation, Android (generally) assembles a single GPU fragment shader to do all of the required work. This shader typically includes several pieces. For example, it might include:

- Evaluating whether a pixel falls inside or outside of the shape being drawn (or on the border, where it might apply antialiasing).
- Evaluating whether a pixel falls inside or outside of the clipping region (again, with possible antialiasing logic for border pixels).
- Logic for the [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader), [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter), and [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode) on the [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint).
- Color space conversion code, as part of Android's color management.

A [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#), like other [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader) types, effectively contributes a function to the GPU's fragment shader.

### AGSL Shader Execution

Just like a GLSL shader, an AGSL shader begins execution in a main function. Unlike GLSL, the function receives as an input parameter the position of the pixel within the [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) or [RenderNode](https://developer.android.com/reference/kotlin/android/graphics/RenderNode) coordinate space (similar to gl_fragCoord) and returns the color to be shaded as a vec4 (similar to out vec4 color or gl_FragColor in GLSL). 

```kotlin
vec4 main(vec2 canvas_coordinates);
  
```

AGSL and GLSL use different coordinate spaces by default. In GLSL, the fragment coordinate (fragCoord) is relative to the lower left. AGSL matches the screen coordinate system of the Android [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) which has its origin as the upper left corner. This means that the coordinates provided as a parameter in the main function are local to the canvas with the exception of any [Shader.getLocalMatrix(Matrix)](https://developer.android.com/reference/kotlin/android/graphics/Shader#getLocalMatrix(android.graphics.Matrix))transformations applied to this shader. Additionally, if the shader is invoked by another using [setInputShader(java.lang.String,android.graphics.Shader)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setInputShader(kotlin.String,%20android.graphics.Shader)), then that parent shader may modify the input coordinates arbitrarily.

### AGSL and Color Spaces

Android Graphics and by extension [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#) are color managed. The working [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) for an AGSL shader is defined to be the color space of the destination, which in most cases is determined by [Window.setColorMode(int)](https://developer.android.com/reference/kotlin/android/view/Window.html#setColorMode(kotlin.Int)).

When authoring an AGSL shader, you won't know what the working color space is. For many effects, this is fine because by default color inputs are automatically converted into the working color space. For certain effects, it may be important to do some math in a fixed, known color space. A common example is lighting - to get physically accurate lighting, math should be done in a linear color space. To help with this, AGSL provides two intrinsic functions that convert colors between the working color space and the [ColorSpace.Named.LINEAR_EXTENDED_SRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space: 

```kotlin
vec3 toLinearSrgb(vec3 color);
  vec3 fromLinearSrgb(vec3 color);
```

### AGSL and Premultiplied Alpha

When dealing with transparent colors, there are two (common) possible representations: straight (unassociated) alpha and premultiplied (associated) alpha. In ASGL the color returned by the main function is expected to be premultiplied. AGSL's use of premultiplied alpha implies:

- If your AGSL shader will return transparent colors, be sure to multiply the RGB by A. The resulting color should be \[R\*A, G\*A, B\*A, A\], not \[R, G, B, A\].
- For more complex shaders, you must understand which of your colors are premultiplied vs. straight. Many operations don't make sense if you mix both kinds of color together.

### Uniforms

AGSL, like GLSL, exposes the concept of uniforms. An AGSL uniform is defined as a read-only, global variable that is accessible by the AGSL code and is initialized by a number of setter methods on [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#). AGSL exposes two primitive uniform data types (float, int) and two specialized types (colors, shaders) that are outlined below.

#### Primitive Uniforms

There are two primitive uniform types supported by AGSL, float and int. For these types and uniforms representing a grouping of these types, like arrays and matrices, there are corresponding [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#) methods to initialize them.

| Java Type | AGSL Type | Method |
|---------------------|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Floats | float | [RuntimeShader.setFloatUniform(String, float)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float)) |
| Floats | vec2 | [RuntimeShader.setFloatUniform(String, float, float)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float)) |
| Floats | vec3 | [RuntimeShader.setFloatUniform(String, float, float, float)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)) |
| --- | --- | --- |
| Floats | vec4 | [RuntimeShader.setFloatUniform(String, float, float, float, float)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)) |
| Integers | int | [RuntimeShader.setIntUniform(String, int)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.Int)) |
| Integers | ivec2 | [RuntimeShader.setIntUniform(String, int, int)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int)) |
| --- | --- | --- |
| Integers | ivec3 | [RuntimeShader.setIntUniform(String, int, int, int)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) |
| Integers | ivec4 | [RuntimeShader.setIntUniform(String, int, int, int, int)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) |
| Matrices and Arrays | mat2, mat3, and mat4, and float\[\] | [RuntimeShader.setFloatUniform(String, float[])](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.FloatArray)) |
| --- | --- | --- |
| Matrices and Arrays | int\[\] | [RuntimeShader.setIntUniform(String, int[])](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.IntArray)) |

For example, a simple AGSL shader making use of a float uniform to modulate the transparency of the output color would look like:

<br />

```kotlin
uniform float alpha;
  vec4 main(vec2 canvas_coordinates) {
      vec3 red = vec3(1.0, 0.0, 0.0);
      return vec4(red * alpha, alpha);
  }
```

After creating a [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#) with that program the uniform can then be initialized and updated per frame by calling [RuntimeShader.setFloatUniform(String, float)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float))with the value of alpha. The value of a primitive uniform defaults to 0 if it is declared in the AGSL shader but not initialized.

#### Color Uniforms

AGSL doesn't know if uniform variables contain colors, it won't automatically convert them to the working colorspace of the shader at runtime. However, you can label your vec4 uniform with the "layout(color)" qualifier which lets Android know that the uniform will be used as a color. Doing so allows AGSL to transform the uniform value to the working color space. In AGSL, declare the uniform like this: 

```kotlin
layout(color) uniform vec4 inputColorA;
  layout(color) uniform vec4 inputColorB;
  vec4 main(vec2 canvas_coordinates) {
      // blend the two colors together and return the resulting color
      return mix(inputColorA, inputColorB, 0.5);
  }
```

After creating a [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#) with that program the uniforms can then be initialized and updated per frame by calling [RuntimeShader.setColorUniform(String, int)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setColorUniform(kotlin.String,%20kotlin.Int)), [RuntimeShader.setColorUniform(String, long)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setColorUniform(kotlin.String,%20kotlin.Long)), or [RuntimeShader.setColorUniform(String, Color)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setColorUniform(kotlin.String,%20android.graphics.Color))with the desired colors. The value of a color uniform is undefined if it is declared in the AGSL shader but not initialized.

#### Shader Uniforms

In GLSL, a fragment shader can sample a texture. For AGSL instead of sampling textures you can sample from any [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader), which includes but is not limited to [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader). To make it clear that you are operating on an [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader) object there is no "sample" method. Instead, the shader uniform has an "eval()" method. This distinction enables AGSL shaders to sample from existing bitmap and gradient shaders as well as other [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#) objects. In AGSL, declare the uniform like this: 

```kotlin
uniform shader myShader;
  vec4 main(vec2 canvas_coordinates) {
      // swap the red and blue color channels when sampling from myShader
      return myShader.eval(canvas_coordinates).bgra;
  }
```

After creating a [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#) with that program the shader uniform can then be initialized and updated per frame by calling [RuntimeShader.setInputShader(String, Shader)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setInputShader(kotlin.String,%20android.graphics.Shader))with the desired shader. The value of a shader uniform is undefined if it is declared in the AGSL shader but not initialized.

Although most [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader) s contain colors that should be color managed, some contain data that isn't actually colors. This includes bitmaps storing normals, material properties (e.g. roughness), heightmaps, or any other purely mathematical data that happens to be stored in a bitmap. When using these kinds of shaders in AGSL, you probably want to initialize them with [setInputBuffer(java.lang.String,android.graphics.BitmapShader)](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setInputBuffer(kotlin.String,%20android.graphics.BitmapShader)). Shaders initialized this way work much like a regular [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader)(including filtering and tiling), with a few major differences:

- No color space transformation is applied (the color space of the bitmap is ignored).
- Bitmaps that return false for [Bitmap.isPremultiplied()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isPremultiplied())are not automatically premultiplied.

In addition, when sampling from a [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader) be aware that the shader does not use normalized coordinates (like a texture in GLSL). It uses (0, 0) in the upper-left corner, and (width, height) in the bottom-right corner. Normally, this is exactly what you want. If you're evaluating the shader with coordinates based on the ones passed to your AGSL program, the scale is correct. However, if you want to adjust those coordinates (to do some kind of re-mapping of the bitmap), remember that the coordinates are local to the canvas.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RuntimeShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#RuntimeShader(kotlin.String))`(`shader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a new RuntimeShader. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setColorUniform(kotlin.String,%20android.graphics.Color))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `color:` ` [Color](https://developer.android.com/reference/kotlin/android/graphics/Color)`)` Sets the uniform color value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setColorUniform(kotlin.String,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform color value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setColorUniform(kotlin.String,%20kotlin.Long))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the uniform color value corresponding to this shader. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the uniform value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value2:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the uniform value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value2:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value3:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the uniform value corresponding to this shader. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value2:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value3:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value4:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the uniform value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setFloatUniform(kotlin.String,%20kotlin.FloatArray))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`)` Sets the uniform value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputBuffer](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setInputBuffer(kotlin.String,%20android.graphics.BitmapShader))`(`shaderName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `shader:` ` [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader)`)` Assigns the uniform shader to the provided shader parameter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputColorFilter](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setInputColorFilter(kotlin.String,%20android.graphics.ColorFilter))`(`filterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `colorFilter:` ` [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter)`)` Assigns the uniform color filter to the provided color filter parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputShader](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setInputShader(kotlin.String,%20android.graphics.Shader))`(`shaderName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `shader:` ` [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader)`)` Assigns the uniform shader to the provided shader parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setInputXfermode(kotlin.String,%20android.graphics.RuntimeXfermode))`(`xfermodeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `xfermode:` ` [RuntimeXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode)`)` Assigns the uniform xfermode to the provided xfermode parameter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value3:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform value corresponding to this shader. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value3:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value4:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform value corresponding to this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/RuntimeShader#setIntUniform(kotlin.String,%20kotlin.IntArray))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `values:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Sets the uniform value corresponding to this shader. |

| Inherited functions ||
|---|---|
| From class [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLocalMatrix](https://developer.android.com/reference/kotlin/android/graphics/Shader#getLocalMatrix(android.graphics.Matrix))`(`localM:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)`)` <br /> Return true if the shader has a non-identity local matrix. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalMatrix](https://developer.android.com/reference/kotlin/android/graphics/Shader#setLocalMatrix(android.graphics.Matrix))`(`localM:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?`)` <br /> Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

## Public constructors

### RuntimeShader

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RuntimeShader(shader: String)
```

Creates a new RuntimeShader.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The text of AGSL shader program to run. This value cannot be`null`. |

## Public methods

### setColorUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorUniform(
    uniformName: String, 
    color: Color
): Unit
```

Sets the uniform color value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the color uniform declared in the AGSL shader program This value cannot be`null`. |
| `color` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color):the provided sRGB color will be transformed into the shader program's output colorspace and will be available as a vec4 uniform in the program. This value cannot be`null`. |

### setColorUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorUniform(
    uniformName: String, 
    color: Int
): Unit
```

Sets the uniform color value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the color uniform declared in the AGSL shader program This value cannot be`null`. |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the provided sRGB color will be transformed into the shader program's output colorspace and will be available as a vec4 uniform in the program. |

### setColorUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorUniform(
    uniformName: String, 
    color: Long
): Unit
```

Sets the uniform color value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the color uniform declared in the AGSL shader program This value cannot be`null`. |
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the provided sRGB color will be transformed into the shader program's output colorspace and will be available as a vec4 uniform in the program. |

### setFloatUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    value: Float
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than a float or float\[1\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |

### setFloatUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec2 or float\[2\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |

### setFloatUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float, 
    value3: Float
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec3 or float\[3\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |

### setFloatUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float, 
    value3: Float, 
    value4: Float
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec4 or float\[4\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |

### setFloatUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    values: FloatArray
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than a float (for N=1), vecN, or float\[N\] where N is the length of the values param then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):This value cannot be`null`. |

### setInputBuffer

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInputBuffer(
    shaderName: String, 
    shader: BitmapShader
): Unit
```

Assigns the uniform shader to the provided shader parameter. If the shader program does not have a uniform shader with that name then an IllegalArgumentException is thrown. Unlike setInputShader this method returns samples directly from the bitmap's buffer. This means that there will be no transformation of the sampled pixels, such as colorspace conversion or alpha premultiplication.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------|
| `shaderName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `shader` | [BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader):This value cannot be`null`. |

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
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL program This value cannot be`null`. |
| `colorFilter` | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter):filter passed into the AGSL program for sampling This value cannot be`null`. |

### setInputShader

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInputShader(
    shaderName: String, 
    shader: Shader
): Unit
```

Assigns the uniform shader to the provided shader parameter. If the shader program does not have a uniform shader with that name then an IllegalArgumentException is thrown.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shaderName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |
| `shader` | [Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader):shader passed into the AGSL shader program for sampling This value cannot be`null`. |

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
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `xfermodeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL program This value cannot be`null`. |
| `xfermode` | [RuntimeXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode):filter passed into the AGSL program for sampling This value cannot be`null`. |

### setIntUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    value: Int
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than an int or int\[1\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |

### setIntUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than ivec2 or int\[2\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |

### setIntUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int, 
    value3: Int
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than ivec3 or int\[3\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |

### setIntUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int, 
    value3: Int, 
    value4: Int
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than ivec4 or int\[4\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |

### setIntUniform

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    values: IntArray
): Unit
```

Sets the uniform value corresponding to this shader. If the shader does not have a uniform with that name or if the uniform is declared with a type other than an int (for N=1), ivecN, or int\[N\] where N is the length of the values param then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the uniform declared in the AGSL shader program This value cannot be`null`. |
| `values` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):This value cannot be`null`. |
