# MeshSpecification

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MeshSpecification

Kotlin| [Java](https://developer.android.com/reference/android/graphics/MeshSpecification "View this page in Java") 

```
open class MeshSpecification
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) |

Class responsible for holding specifications for [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh) creations. This class generates a [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) via the[MeshSpecification.make(Attribute[], int, Varying[], String, String)](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#make(kotlin.Array,%20kotlin.Int,%20kotlin.Array,%20kotlin.String,%20kotlin.String))method, where multiple parameters to set up the mesh are supplied, including attributes, vertex stride, [Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying), and vertex/fragment shaders. There are also additional methods to provide an optional [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) as well as an alpha type. For example a vertex shader that leverages a [Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying) may look like the following: 

```kotlin
Varyings main(const Attributes attributes) {
              Varyings varyings;
              varyings.position = attributes.position;
              return varyings;
         }
  
```
The corresponding fragment shader that may consume the varying look like the following: 

```kotlin
float2 main(const Varyings varyings, out float4 color) {
              color = vec4(1.0, 0.0, 0.0, 1.0);
              return varyings.position;
       }
  
```
The color returned from this fragment shader is blended with the other parameters that are configured on the Paint object (ex. [Paint.setBlendMode(BlendMode)](https://developer.android.com/reference/kotlin/android/graphics/Paint#setBlendMode(android.graphics.BlendMode))used to draw the mesh. The position returned in the fragment shader can be consumed by any following fragment shaders in the shader chain. See https://developer.android.com/develop/ui/views/graphics/agsl for more information regarding Android Graphics Shader Language. Note that there are several limitations on various mesh specifications: 1. The max amount of attributes allowed is 8. 2. The offset alignment length is 4 bytes. 2. The max stride length is 1024. 3. The max amount of varyings is 6. These should be kept in mind when generating a mesh specification, as exceeding them will lead to errors.

<br />

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute) Data class to represent a single attribute in a shader. |
| open | [Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying) Data class to represent a single varying variable. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA_TYPE_OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_OPAQUE:kotlin.Int) Pixel is opaque. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA_TYPE_PREMULTIPLIED](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_PREMULTIPLIED:kotlin.Int) Pixel components are premultiplied by alpha. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_UNKNOWN:kotlin.Int) uninitialized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA_TYPE_UNPREMULTIPLIED](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_UNPREMULTIPLIED:kotlin.Int) Pixel components are independent of alpha. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#TYPE_FLOAT:kotlin.Int) Represents one float. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT2](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#TYPE_FLOAT2:kotlin.Int) Represents two floats. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT3](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#TYPE_FLOAT3:kotlin.Int) Represents three floats. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT4](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#TYPE_FLOAT4:kotlin.Int) Represents four floats. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UBYTE4](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#TYPE_UBYTE4:kotlin.Int) Represents four bytes. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) | [make](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#make(kotlin.Array,%20kotlin.Int,%20kotlin.Array,%20kotlin.String,%20kotlin.String))`(`attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute)!>`, `vertexStride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `varyings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying)!>`, `vertexShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fragmentShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object for use within [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh). |
| openstatic [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) | [make](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#make(kotlin.Array,%20kotlin.Int,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20android.graphics.ColorSpace))`(`attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute)!>`, `vertexStride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `varyings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying)!>`, `vertexShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fragmentShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Creates a [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object. |
| openstatic [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) | [make](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#make(kotlin.Array,%20kotlin.Int,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20android.graphics.ColorSpace,%20kotlin.Int))`(`attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute)!>`, `vertexStride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `varyings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying)!>`, `vertexShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fragmentShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`, `alphaType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object. |

## Constants

### ALPHA_TYPE_OPAQUE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALPHA_TYPE_OPAQUE: Int
```

Pixel is opaque. 

 Value: 1

### ALPHA_TYPE_PREMULTIPLIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALPHA_TYPE_PREMULTIPLIED: Int
```

Pixel components are premultiplied by alpha. 

 Value: 2

### ALPHA_TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALPHA_TYPE_UNKNOWN: Int
```

uninitialized. 

 Value: 0

### ALPHA_TYPE_UNPREMULTIPLIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALPHA_TYPE_UNPREMULTIPLIED: Int
```

Pixel components are independent of alpha. 

 Value: 3

### TYPE_FLOAT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FLOAT: Int
```

Represents one float. Its equivalent shader type is float. 

 Value: 0

### TYPE_FLOAT2

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FLOAT2: Int
```

Represents two floats. Its equivalent shader type is float2. 

 Value: 1

### TYPE_FLOAT3

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FLOAT3: Int
```

Represents three floats. Its equivalent shader type is float3. 

 Value: 2

### TYPE_FLOAT4

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FLOAT4: Int
```

Represents four floats. Its equivalent shader type is float4. 

 Value: 3

### TYPE_UBYTE4

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UBYTE4: Int
```

Represents four bytes. Its equivalent shader type is half4. 

 Value: 4

## Public methods

### make

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun make(
    attributes: Array<MeshSpecification.Attribute!>, 
    vertexStride: Int, 
    varyings: Array<MeshSpecification.Varying!>, 
    vertexShader: String, 
    fragmentShader: String
): MeshSpecification
```

Creates a [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object for use within [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh). This uses a default color space of [ColorSpace.Named.SRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) and alphaType of [ALPHA_TYPE_PREMULTIPLIED](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_PREMULTIPLIED:kotlin.Int).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute)!\>:list of attributes represented by [Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute). Can hold a max of 8. This value cannot be`null`. |
| `vertexStride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):length of vertex stride in bytes. This should be the size of a single vertex' attributes. Max of 1024 is accepted. Value is between 1 and 1024 inclusive |
| `varyings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying)!\>:List of varyings represented by [Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying). Can hold a max of 6. Note that \`position\` is provided by default, does not need to be provided in the list, and does not count towards the 6 varyings allowed. This value cannot be`null`. |
| `vertexShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):vertex shader to be supplied to the mesh. Ensure that the position varying is set within the shader to get proper results. See [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) for an example vertex shader implementation This value cannot be`null`. |
| `fragmentShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):fragment shader to be supplied to the mesh. See [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) for an example fragment shader implementation This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) | [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object for use when creating [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh) This value cannot be`null`. |

### make

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun make(
    attributes: Array<MeshSpecification.Attribute!>, 
    vertexStride: Int, 
    varyings: Array<MeshSpecification.Varying!>, 
    vertexShader: String, 
    fragmentShader: String, 
    colorSpace: ColorSpace
): MeshSpecification
```

Creates a [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object. This uses a default alphaType of [ALPHA_TYPE_PREMULTIPLIED](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_PREMULTIPLIED:kotlin.Int).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute)!\>:list of attributes represented by [Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute). Can hold a max of 8. This value cannot be`null`. |
| `vertexStride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):length of vertex stride in bytes. This should be the size of a single vertex' attributes. Max of 1024 is accepted. Value is between 1 and 1024 inclusive |
| `varyings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying)!\>:List of varyings represented by [Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying). Can hold a max of 6. Note that \`position\` is provided by default, does not need to be provided in the list, and does not count towards the 6 varyings allowed. This value cannot be`null`. |
| `vertexShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):vertex shader to be supplied to the mesh. Ensure that the position varying is set within the shader to get proper results. See [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) for an example vertex shader implementation This value cannot be`null`. |
| `fragmentShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):fragment shader to be supplied to the mesh. See [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) for an example fragment shader implementation This value cannot be`null`. |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace): [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) to tell what color space to work in. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) | [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object for use when creating [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh) This value cannot be`null`. |

### make

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun make(
    attributes: Array<MeshSpecification.Attribute!>, 
    vertexStride: Int, 
    varyings: Array<MeshSpecification.Varying!>, 
    vertexShader: String, 
    fragmentShader: String, 
    colorSpace: ColorSpace, 
    alphaType: Int
): MeshSpecification
```

Creates a [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute)!\>:list of attributes represented by [Attribute](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Attribute). Can hold a max of 8. This value cannot be`null`. |
| `vertexStride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):length of vertex stride in bytes. This should be the size of a single vertex' attributes. Max of 1024 is accepted. Value is between 1 and 1024 inclusive |
| `varyings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying)!\>:List of varyings represented by [Varying](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification.Varying). Can hold a max of 6. Note that \`position\` is provided by default, does not need to be provided in the list, and does not count towards the 6 varyings allowed. This value cannot be`null`. |
| `vertexShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):vertex shader to be supplied to the mesh. Ensure that the position varying is set within the shader to get proper results. See [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) for an example vertex shader implementation This value cannot be`null`. |
| `fragmentShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):fragment shader to be supplied to the mesh. See [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) for an example fragment shader implementation This value cannot be`null`. |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace): [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) to tell what color space to work in. This value cannot be`null`. |
| `alphaType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Describes how to interpret the alpha component for a pixel. Must be one of [MeshSpecification.ALPHA_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_UNKNOWN:kotlin.Int), [MeshSpecification.ALPHA_TYPE_OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_OPAQUE:kotlin.Int), [MeshSpecification.ALPHA_TYPE_PREMULTIPLIED](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_PREMULTIPLIED:kotlin.Int), or [MeshSpecification.ALPHA_TYPE_UNPREMULTIPLIED](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_UNPREMULTIPLIED:kotlin.Int) Value is [android.graphics.MeshSpecification#ALPHA_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_UNKNOWN:kotlin.Int), [android.graphics.MeshSpecification#ALPHA_TYPE_OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_OPAQUE:kotlin.Int), [android.graphics.MeshSpecification#ALPHA_TYPE_PREMULTIPLIED](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_PREMULTIPLIED:kotlin.Int), or [android.graphics.MeshSpecification#ALPHA_TYPE_UNPREMULTIPLIED](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#ALPHA_TYPE_UNPREMULTIPLIED:kotlin.Int) |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) | [MeshSpecification](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#) object for use when creating [Mesh](https://developer.android.com/reference/kotlin/android/graphics/Mesh) This value cannot be`null`. |
