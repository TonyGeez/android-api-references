# Mesh

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Mesh

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Mesh "View this page in Java") 

```
open class Mesh
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh#) |

Class representing a mesh object. This class represents a Mesh object that can optionally be indexed. A [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification) is required along with various attributes for detailing the mesh object, including a mode, vertex buffer, optional index buffer, and bounds for the mesh. Once generated, a mesh object can be drawn through [Canvas.drawMesh(Mesh, BlendMode, Paint)](https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawMesh(android.graphics.Mesh,%20android.graphics.BlendMode,%20android.graphics.Paint))

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIANGLES](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLES:kotlin.Int) The mesh will be drawn with triangles without utilizing shared vertices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIANGLE_STRIP](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLE_STRIP:kotlin.Int) The mesh will be drawn with triangles utilizing shared vertices. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh#Mesh(android.graphics.MeshSpecification,%20kotlin.Int,%20java.nio.Buffer,%20kotlin.Int,%20android.graphics.RectF))`(`meshSpec:` ` [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification)`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vertexBuffer:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)`, `vertexCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`)` Constructor for a non-indexed Mesh. |
| [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh#Mesh(android.graphics.MeshSpecification,%20kotlin.Int,%20java.nio.Buffer,%20kotlin.Int,%20java.nio.ShortBuffer,%20android.graphics.RectF))`(`meshSpec:` ` [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification)`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vertexBuffer:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)`, `vertexCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `indexBuffer:` ` [ShortBuffer](https://developer.android.com/reference/kotlin/java/nio/ShortBuffer.html#)`, `bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)`)` Constructor for an indexed Mesh. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setColorUniform(kotlin.String,%20android.graphics.Color))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `color:` ` [Color](https://developer.android.com/reference/kotlin/android/graphics/Color)`)` Sets the uniform color value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setColorUniform(kotlin.String,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform color value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setColorUniform(kotlin.String,%20kotlin.Long))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the uniform color value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setFloatUniform(kotlin.String,%20kotlin.Float))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value2:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value2:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value3:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setFloatUniform(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value2:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value3:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value4:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setFloatUniform(kotlin.String,%20kotlin.FloatArray))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setIntUniform(kotlin.String,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value3:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setIntUniform(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value1:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value2:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value3:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value4:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntUniform](https://developer.android.com/reference/kotlin/android/graphics/Mesh#setIntUniform(kotlin.String,%20kotlin.IntArray))`(`uniformName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `values:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Sets the uniform value corresponding to the shader assigned to the mesh. |

## Constants

### TRIANGLES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRIANGLES: Int
```

The mesh will be drawn with triangles without utilizing shared vertices. 

 Value: 0

### TRIANGLE_STRIP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRIANGLE_STRIP: Int
```

The mesh will be drawn with triangles utilizing shared vertices. 

 Value: 1

## Public constructors

### Mesh

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Mesh(
    meshSpec: MeshSpecification, 
    mode: Int, 
    vertexBuffer: Buffer, 
    vertexCount: Int, 
    bounds: RectF)
```

Constructor for a non-indexed Mesh.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `meshSpec` | [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification): [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification) used when generating the mesh. This value cannot be`null`. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Determines what mode to draw the mesh in. Must be one of [Mesh.TRIANGLES](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLES:kotlin.Int) or [Mesh.TRIANGLE_STRIP](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLE_STRIP:kotlin.Int) Value is [android.graphics.Mesh#TRIANGLES](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLES:kotlin.Int), or [android.graphics.Mesh#TRIANGLE_STRIP](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLE_STRIP:kotlin.Int) |
| `vertexBuffer` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#):vertex buffer representing through [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#). This provides the data for all attributes provided within the meshSpec for every vertex. That is, a vertex buffer should be (attributes size \* number of vertices) in length to be valid. Note that currently implementation will have a CPU backed buffer generated. This value cannot be`null`. |
| `vertexCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of vertices represented in the vertexBuffer and mesh. |
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):bounds of the mesh object. This value cannot be`null`. |

### Mesh

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Mesh(
    meshSpec: MeshSpecification, 
    mode: Int, 
    vertexBuffer: Buffer, 
    vertexCount: Int, 
    indexBuffer: ShortBuffer, 
    bounds: RectF)
```

Constructor for an indexed Mesh.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `meshSpec` | [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification): [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification) used when generating the mesh. This value cannot be`null`. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Determines what mode to draw the mesh in. Must be one of [Mesh.TRIANGLES](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLES:kotlin.Int) or [Mesh.TRIANGLE_STRIP](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLE_STRIP:kotlin.Int) Value is [android.graphics.Mesh#TRIANGLES](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLES:kotlin.Int), or [android.graphics.Mesh#TRIANGLE_STRIP](https://developer.android.com/reference/kotlin/android/graphics/Mesh#TRIANGLE_STRIP:kotlin.Int) |
| `vertexBuffer` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#):vertex buffer representing through [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#). This provides the data for all attributes provided within the meshSpec for every vertex. That is, a vertex buffer should be (attributes size \* number of vertices) in length to be valid. Note that currently implementation will have a CPU backed buffer generated. This value cannot be`null`. |
| `vertexCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of vertices represented in the vertexBuffer and mesh. |
| `indexBuffer` | [ShortBuffer](https://developer.android.com/reference/kotlin/java/nio/ShortBuffer.html#):index buffer representing through [ShortBuffer](https://developer.android.com/reference/kotlin/java/nio/ShortBuffer.html#). Indices are required to be 16 bits, so ShortBuffer is necessary. Note that currently implementation will have a CPU backed buffer generated. This value cannot be`null`. |
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF):bounds of the mesh object. This value cannot be`null`. |

## Public methods

### setColorUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorUniform(
    uniformName: String, 
    color: Color
): Unit
```

Sets the uniform color value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentExcepton is thrown.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the color uniform declared in the shader program. This value cannot be`null`. |
| `color` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color):the provided sRGB color will be converted into the shader program's output colorspace and will be made available as a vec4 uniform in the program. This value cannot be`null`. |

### setColorUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorUniform(
    uniformName: String, 
    color: Int
): Unit
```

Sets the uniform color value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentExcepton is thrown.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the color uniform declared in the shader program. This value cannot be`null`. |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the provided sRGB color will be converted into the shader program's output colorspace and be available as a vec4 uniform in the program. |

### setColorUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColorUniform(
    uniformName: String, 
    color: Long
): Unit
```

Sets the uniform color value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than vec3 or vec4 and corresponding layout(color) annotation then an IllegalArgumentExcepton is thrown.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the color uniform declared in the shader program. This value cannot be`null`. |
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the provided sRGB color will be converted into the shader program's output colorspace and be available as a vec4 uniform in the program. |

### setFloatUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    value: Float
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than a float or float\[1\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the float uniform declared in the shader program. This value cannot be`null`. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):float value corresponding to the float uniform with the given name. |

### setFloatUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than a vec2 or float\[2\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the float uniform declared in the shader program. This value cannot be`null`. |
| `value1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):first float value corresponding to the float uniform with the given name. |
| `value2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):second float value corresponding to the float uniform with the given name. |

### setFloatUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float, 
    value3: Float
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than a vec3 or float\[3\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the float uniform declared in the shader program. This value cannot be`null`. |
| `value1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):first float value corresponding to the float uniform with the given name. |
| `value2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):second float value corresponding to the float uniform with the given name. |
| `value3` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):third float value corresponding to the float unifiform with the given name. |

### setFloatUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    value1: Float, 
    value2: Float, 
    value3: Float, 
    value4: Float
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than a vec4 or float\[4\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the float uniform declared in the shader program. This value cannot be`null`. |
| `value1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):first float value corresponding to the float uniform with the given name. |
| `value2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):second float value corresponding to the float uniform with the given name. |
| `value3` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):third float value corresponding to the float uniform with the given name. |
| `value4` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):fourth float value corresponding to the float uniform with the given name. |

### setFloatUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatUniform(
    uniformName: String, 
    values: FloatArray
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than a float (for N=1), vecN, or float\[N\], where N is the length of the values param, then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the float uniform declared in the shader program. This value cannot be`null`. |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):float value corresponding to the vec4 float uniform with the given name. This value cannot be`null`. |

### setIntUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    value: Int
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than int or int\[1\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the int uniform declared in the shader program. This value cannot be`null`. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):value corresponding to the int uniform with the given name. |

### setIntUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than ivec2 or int\[2\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the int uniform declared in the shader program. This value cannot be`null`. |
| `value1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):first value corresponding to the int uniform with the given name. |
| `value2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):second value corresponding to the int uniform with the given name. |

### setIntUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int, 
    value3: Int
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than ivec3 or int\[3\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the int uniform declared in the shader program. This value cannot be`null`. |
| `value1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):first value corresponding to the int uniform with the given name. |
| `value2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):second value corresponding to the int uniform with the given name. |
| `value3` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):third value corresponding to the int uniform with the given name. |

### setIntUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    value1: Int, 
    value2: Int, 
    value3: Int, 
    value4: Int
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than ivec4 or int\[4\] then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the int uniform declared in the shader program. This value cannot be`null`. |
| `value1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):first value corresponding to the int uniform with the given name. |
| `value2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):second value corresponding to the int uniform with the given name. |
| `value3` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):third value corresponding to the int uniform with the given name. |
| `value4` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):fourth value corresponding to the int uniform with the given name. |

### setIntUniform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntUniform(
    uniformName: String, 
    values: IntArray
): Unit
```

Sets the uniform value corresponding to the shader assigned to the mesh. If the shader does not have a uniform with that name or if the uniform is declared with a type other than an int (for N=1), ivecN, or int\[N\], where N is the length of the values param, then an IllegalArgumentException is thrown.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniformName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name matching the int uniform declared in the shader program. This value cannot be`null`. |
| `values` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):int values corresponding to the vec4 int uniform with the given name. This value cannot be`null`. |
