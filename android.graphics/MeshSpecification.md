# MeshSpecification

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MeshSpecification

Kotlin| [Java](MeshSpecification.md) 
| --- | --- |

```
open class MeshSpecification
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.MeshSpecification](MeshSpecification.md) |

Class responsible for holding specifications for [Mesh](Mesh.md) creations. This class generates a [MeshSpecification](MeshSpecification.md) via the[MeshSpecification.make(Attribute[], int, Varying[], String, String)](https://developer.android.com/reference/kotlin/android/graphics/MeshSpecification#make(kotlin.Array,%20kotlin.Int,%20kotlin.Array,%20kotlin.String,%20kotlin.String))method, where multiple parameters to set up the mesh are supplied, including attributes, vertex stride, [Varying](../android/graphics/MeshSpecification.Varying.md), and vertex/fragment shaders. There are also additional methods to provide an optional [ColorSpace](ColorSpace.md) as well as an alpha type. For example a vertex shader that leverages a [Varying](../android/graphics/MeshSpecification.Varying.md) may look like the following: 

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
The color returned from this fragment shader is blended with the other parameters that are configured on the Paint object (ex. [Paint.setBlendMode(BlendMode)](Paint.md))used to draw the mesh. The position returned in the fragment shader can be consumed by any following fragment shaders in the shader chain. See https://developer.android.com/develop/ui/views/graphics/agsl for more information regarding Android Graphics Shader Language. Note that there are several limitations on various mesh specifications: 1. The max amount of attributes allowed is 8. 2. The offset alignment length is 4 bytes. 2. The max stride length is 1024. 3. The max amount of varyings is 6. These should be kept in mind when generating a mesh specification, as exceeding them will lead to errors.

<br />

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Attribute](../android/graphics/MeshSpecification.Attribute.md) Data class to represent a single attribute in a shader. |
| open | [Varying](../android/graphics/MeshSpecification.Varying.md) Data class to represent a single varying variable. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA_TYPE_OPAQUE](MeshSpecification.md) Pixel is opaque. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA_TYPE_PREMULTIPLIED](MeshSpecification.md) Pixel components are premultiplied by alpha. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA_TYPE_UNKNOWN](MeshSpecification.md) uninitialized. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA_TYPE_UNPREMULTIPLIED](MeshSpecification.md) Pixel components are independent of alpha. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT](MeshSpecification.md) Represents one float. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT2](MeshSpecification.md) Represents two floats. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT3](MeshSpecification.md) Represents three floats. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT4](MeshSpecification.md) Represents four floats. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UBYTE4](MeshSpecification.md) Represents four bytes. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [MeshSpecification](MeshSpecification.md) | [make](MeshSpecification.md))`(`attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Attribute](../android/graphics/MeshSpecification.Attribute.md)!>`, `vertexStride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `varyings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Varying](../android/graphics/MeshSpecification.Varying.md)!>`, `vertexShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fragmentShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a [MeshSpecification](MeshSpecification.md) object for use within [Mesh](Mesh.md). |
| openstatic [MeshSpecification](MeshSpecification.md) | [make](MeshSpecification.md))`(`attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Attribute](../android/graphics/MeshSpecification.Attribute.md)!>`, `vertexStride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `varyings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Varying](../android/graphics/MeshSpecification.Varying.md)!>`, `vertexShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fragmentShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `colorSpace:` ` [ColorSpace](ColorSpace.md)`)` Creates a [MeshSpecification](MeshSpecification.md) object. |
| openstatic [MeshSpecification](MeshSpecification.md) | [make](MeshSpecification.md))`(`attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Attribute](../android/graphics/MeshSpecification.Attribute.md)!>`, `vertexStride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `varyings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MeshSpecification.Varying](../android/graphics/MeshSpecification.Varying.md)!>`, `vertexShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fragmentShader:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `colorSpace:` ` [ColorSpace](ColorSpace.md)`, `alphaType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a [MeshSpecification](MeshSpecification.md) object. |
| --- | --- |

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

Creates a [MeshSpecification](MeshSpecification.md) object for use within [Mesh](Mesh.md). This uses a default color space of [ColorSpace.Named.SRGB](../android/graphics/ColorSpace.Named.md) and alphaType of [ALPHA_TYPE_PREMULTIPLIED](MeshSpecification.md).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Attribute](../android/graphics/MeshSpecification.Attribute.md)!\>:list of attributes represented by [Attribute](../android/graphics/MeshSpecification.Attribute.md). Can hold a max of 8. This value cannot be`null`. |
| `vertexStride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):length of vertex stride in bytes. This should be the size of a single vertex' attributes. Max of 1024 is accepted. Value is between 1 and 1024 inclusive |
| `varyings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Varying](../android/graphics/MeshSpecification.Varying.md)!\>:List of varyings represented by [Varying](../android/graphics/MeshSpecification.Varying.md). Can hold a max of 6. Note that \`position\` is provided by default, does not need to be provided in the list, and does not count towards the 6 varyings allowed. This value cannot be`null`. |
| --- | --- |
| `vertexShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):vertex shader to be supplied to the mesh. Ensure that the position varying is set within the shader to get proper results. See [MeshSpecification](MeshSpecification.md) for an example vertex shader implementation This value cannot be`null`. |
| `fragmentShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):fragment shader to be supplied to the mesh. See [MeshSpecification](MeshSpecification.md) for an example fragment shader implementation This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MeshSpecification](MeshSpecification.md) | [MeshSpecification](MeshSpecification.md) object for use when creating [Mesh](Mesh.md) This value cannot be`null`. |

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

Creates a [MeshSpecification](MeshSpecification.md) object. This uses a default alphaType of [ALPHA_TYPE_PREMULTIPLIED](MeshSpecification.md).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Attribute](../android/graphics/MeshSpecification.Attribute.md)!\>:list of attributes represented by [Attribute](../android/graphics/MeshSpecification.Attribute.md). Can hold a max of 8. This value cannot be`null`. |
| `vertexStride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):length of vertex stride in bytes. This should be the size of a single vertex' attributes. Max of 1024 is accepted. Value is between 1 and 1024 inclusive |
| `varyings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Varying](../android/graphics/MeshSpecification.Varying.md)!\>:List of varyings represented by [Varying](../android/graphics/MeshSpecification.Varying.md). Can hold a max of 6. Note that \`position\` is provided by default, does not need to be provided in the list, and does not count towards the 6 varyings allowed. This value cannot be`null`. |
| --- | --- |
| `vertexShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):vertex shader to be supplied to the mesh. Ensure that the position varying is set within the shader to get proper results. See [MeshSpecification](MeshSpecification.md) for an example vertex shader implementation This value cannot be`null`. |
| `fragmentShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):fragment shader to be supplied to the mesh. See [MeshSpecification](MeshSpecification.md) for an example fragment shader implementation This value cannot be`null`. |
| `colorSpace` | [ColorSpace](ColorSpace.md): [ColorSpace](ColorSpace.md) to tell what color space to work in. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MeshSpecification](MeshSpecification.md) | [MeshSpecification](MeshSpecification.md) object for use when creating [Mesh](Mesh.md) This value cannot be`null`. |

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

Creates a [MeshSpecification](MeshSpecification.md) object.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Attribute](../android/graphics/MeshSpecification.Attribute.md)!\>:list of attributes represented by [Attribute](../android/graphics/MeshSpecification.Attribute.md). Can hold a max of 8. This value cannot be`null`. |
| `vertexStride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):length of vertex stride in bytes. This should be the size of a single vertex' attributes. Max of 1024 is accepted. Value is between 1 and 1024 inclusive |
| `varyings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeshSpecification.Varying](../android/graphics/MeshSpecification.Varying.md)!\>:List of varyings represented by [Varying](../android/graphics/MeshSpecification.Varying.md). Can hold a max of 6. Note that \`position\` is provided by default, does not need to be provided in the list, and does not count towards the 6 varyings allowed. This value cannot be`null`. |
| --- | --- |
| `vertexShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):vertex shader to be supplied to the mesh. Ensure that the position varying is set within the shader to get proper results. See [MeshSpecification](MeshSpecification.md) for an example vertex shader implementation This value cannot be`null`. |
| `fragmentShader` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):fragment shader to be supplied to the mesh. See [MeshSpecification](MeshSpecification.md) for an example fragment shader implementation This value cannot be`null`. |
| `colorSpace` | [ColorSpace](ColorSpace.md): [ColorSpace](ColorSpace.md) to tell what color space to work in. This value cannot be`null`. |
| --- | --- |
| `alphaType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Describes how to interpret the alpha component for a pixel. Must be one of [MeshSpecification.ALPHA_TYPE_UNKNOWN](MeshSpecification.md), [MeshSpecification.ALPHA_TYPE_OPAQUE](MeshSpecification.md), [MeshSpecification.ALPHA_TYPE_PREMULTIPLIED](MeshSpecification.md), or [MeshSpecification.ALPHA_TYPE_UNPREMULTIPLIED](MeshSpecification.md) Value is [android.graphics.MeshSpecification#ALPHA_TYPE_UNKNOWN](MeshSpecification.md), [android.graphics.MeshSpecification#ALPHA_TYPE_OPAQUE](MeshSpecification.md), [android.graphics.MeshSpecification#ALPHA_TYPE_PREMULTIPLIED](MeshSpecification.md), or [android.graphics.MeshSpecification#ALPHA_TYPE_UNPREMULTIPLIED](MeshSpecification.md) |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MeshSpecification](MeshSpecification.md) | [MeshSpecification](MeshSpecification.md) object for use when creating [Mesh](Mesh.md) This value cannot be`null`. |
