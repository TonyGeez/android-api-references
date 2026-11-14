# ScriptIntrinsicColorMatrix

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicColorMatrix

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/ScriptIntrinsicColorMatrix "View this page in Java") 

```
class ScriptIntrinsicColorMatrix : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) ||
| | | | ↳ | [android.renderscript.ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for applying a color matrix to allocations. If the element type is [Element.DataType.UNSIGNED_8](https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType), it is converted to [Element.DataType.FLOAT_32](https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType) and normalized from (0-255) to (0-1). If the incoming vector size is less than four, a [Element.F32_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_4(android.renderscript.RenderScript))is created by filling the missing vector channels with zero. This value is then multiplied by the 4x4 color matrix as performed by rsMatrixMultiply(), adding a [Element.F32_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_4(android.renderscript.RenderScript)), and then writing it to the output [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation). If the ouptut type is unsigned, the value is normalized from (0-1) to (0-255) and converted. If the output vector size is less than four, the unused channels are discarded. Supported elements types are [Element.U8](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8(android.renderscript.RenderScript)), [android.renderscript.Element#U8_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_2(android.renderscript.RenderScript)), [Element.U8_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_3(android.renderscript.RenderScript)), [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript)), [Element.F32](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32(android.renderscript.RenderScript)), [Element.F32_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_2(android.renderscript.RenderScript)), [android.renderscript.Element#F32_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_3(android.renderscript.RenderScript)), and [Element.F32_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_4(android.renderscript.RenderScript)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#create(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Create an intrinsic for applying a color matrix to an allocation. |
| static [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#create(android.renderscript.RenderScript,%20android.renderscript.Element))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`)` Create an intrinsic for applying a color matrix to an allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#forEach(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Invoke the kernel and apply the matrix to each cell of input [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) and copy to the output [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#forEach(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Invoke the kernel and apply the matrix to each cell of input [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) and copy to the output [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation). |
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelID](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#getKernelID())`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdd](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#setAdd(android.renderscript.Float4))`(`f:` ` [Float4](https://developer.android.com/reference/kotlin/android/renderscript/Float4)!`)` Set the value to be added after the color matrix has been applied. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdd](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#setAdd(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `g:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the value to be added after the color matrix has been applied. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#setColorMatrix(android.renderscript.Matrix3f))`(`m:` ` [Matrix3f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix3f)!`)` Set the color matrix which will be applied to each cell of the image. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#setColorMatrix(android.renderscript.Matrix4f))`(`m:` ` [Matrix4f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix4f)!`)` Set the color matrix which will be applied to each cell of the image. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGreyscale](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#setGreyscale())`()` Set a color matrix to convert from RGB to luminance. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRGBtoYUV](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#setRGBtoYUV())`()` Set the matrix to convert from RGB to YUV with a direct copy of the 4th channel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setYUVtoRGB](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#setYUVtoRGB())`()` Set the matrix to convert from YUV to RGB with a direct copy of the 4th channel. |

## Public methods

### create

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(rs: RenderScript!): ScriptIntrinsicColorMatrix!
```

**Deprecated:** *Deprecated in Java.*

Create an intrinsic for applying a color matrix to an allocation.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#)! | ScriptIntrinsicColorMatrix |

### create

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    rs: RenderScript!, 
    e: Element!
): ScriptIntrinsicColorMatrix!
```

**Deprecated:** *Use the single argument version as Element is now ignored.*

Create an intrinsic for applying a color matrix to an allocation.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:Element type for inputs and outputs, As of API 19, this parameter is ignored. The Element type check is performed in the kernel launch. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix#)! | ScriptIntrinsicColorMatrix |

### forEach

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Invoke the kernel and apply the matrix to each cell of input [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) and copy to the output [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation). If the vector size of the input is less than four, the remaining components are treated as zero for the matrix multiply. If the output vector size is less than four, the unused vector components are discarded.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Input allocation |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation |

### forEach

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Invoke the kernel and apply the matrix to each cell of input [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) and copy to the output [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation). If the vector size of the input is less than four, the remaining components are treated as zero for the matrix multiply. If the output vector size is less than four, the unused vector components are discarded.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Input allocation |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

### getKernelID

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKernelID(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for this intrinsic kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### setAdd

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAdd(f: Float4!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the value to be added after the color matrix has been applied. The default value is {0, 0, 0, 0}

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `f` | [Float4](https://developer.android.com/reference/kotlin/android/renderscript/Float4)!:The float4 value to be added. |

### setAdd

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAdd(
    r: Float, 
    g: Float, 
    b: Float, 
    a: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the value to be added after the color matrix has been applied. The default value is {0, 0, 0, 0}

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red add value. |
| `g` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green add value. |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue add value. |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha add value. |

### setColorMatrix

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setColorMatrix(m: Matrix3f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the color matrix which will be applied to each cell of the image. This will set the alpha channel to be a copy.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `m` | [Matrix3f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix3f)!:The 3x3 matrix to set. |

### setColorMatrix

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setColorMatrix(m: Matrix4f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the color matrix which will be applied to each cell of the image.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `m` | [Matrix4f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix4f)!:The 4x4 matrix to set. |

### setGreyscale

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setGreyscale(): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a color matrix to convert from RGB to luminance. The alpha channel will be a copy. 

### setRGBtoYUV

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRGBtoYUV(): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the matrix to convert from RGB to YUV with a direct copy of the 4th channel. 

### setYUVtoRGB

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setYUVtoRGB(): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the matrix to convert from YUV to RGB with a direct copy of the 4th channel.
