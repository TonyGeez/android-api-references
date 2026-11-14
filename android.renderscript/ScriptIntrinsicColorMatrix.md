# ScriptIntrinsicColorMatrix

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicColorMatrix

Kotlin| [Java](ScriptIntrinsicColorMatrix.md) 
| --- | --- |

```
class ScriptIntrinsicColorMatrix : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicColorMatrix](ScriptIntrinsicColorMatrix.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for applying a color matrix to allocations. If the element type is [Element.DataType.UNSIGNED_8](../android/renderscript/Element.DataType.md), it is converted to [Element.DataType.FLOAT_32](../android/renderscript/Element.DataType.md) and normalized from (0-255) to (0-1). If the incoming vector size is less than four, a [Element.F32_4](Element.md))is created by filling the missing vector channels with zero. This value is then multiplied by the 4x4 color matrix as performed by rsMatrixMultiply(), adding a [Element.F32_4](Element.md)), and then writing it to the output [Allocation](Allocation.md). If the ouptut type is unsigned, the value is normalized from (0-1) to (0-255) and converted. If the output vector size is less than four, the unused channels are discarded. Supported elements types are [Element.U8](Element.md)), [android.renderscript.Element#U8_2](Element.md)), [Element.U8_3](Element.md)), [Element.U8_4](Element.md)), [Element.F32](Element.md)), [Element.F32_2](Element.md)), [android.renderscript.Element#F32_3](Element.md)), and [Element.F32_4](Element.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicColorMatrix](ScriptIntrinsicColorMatrix.md)! | [create](ScriptIntrinsicColorMatrix.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Create an intrinsic for applying a color matrix to an allocation. |
| static [ScriptIntrinsicColorMatrix](ScriptIntrinsicColorMatrix.md)! | [create](ScriptIntrinsicColorMatrix.md))`(`rs:` ` [RenderScript](RenderScript.md)!`, `e:` ` [Element](Element.md)!`)` Create an intrinsic for applying a color matrix to an allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicColorMatrix.md))`(`ain:` ` [Allocation](Allocation.md)!`, `aout:` ` [Allocation](Allocation.md)!`)` Invoke the kernel and apply the matrix to each cell of input [Allocation](Allocation.md) and copy to the output [Allocation](Allocation.md). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicColorMatrix.md))`(`ain:` ` [Allocation](Allocation.md)!`, `aout:` ` [Allocation](Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Invoke the kernel and apply the matrix to each cell of input [Allocation](Allocation.md) and copy to the output [Allocation](Allocation.md). |
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelID](ScriptIntrinsicColorMatrix.md))`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdd](ScriptIntrinsicColorMatrix.md))`(`f:` ` [Float4](Float4.md)!`)` Set the value to be added after the color matrix has been applied. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdd](ScriptIntrinsicColorMatrix.md))`(`r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `g:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the value to be added after the color matrix has been applied. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorMatrix](ScriptIntrinsicColorMatrix.md))`(`m:` ` [Matrix3f](Matrix3f.md)!`)` Set the color matrix which will be applied to each cell of the image. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorMatrix](ScriptIntrinsicColorMatrix.md))`(`m:` ` [Matrix4f](Matrix4f.md)!`)` Set the color matrix which will be applied to each cell of the image. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGreyscale](ScriptIntrinsicColorMatrix.md))`()` Set a color matrix to convert from RGB to luminance. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRGBtoYUV](ScriptIntrinsicColorMatrix.md))`()` Set the matrix to convert from RGB to YUV with a direct copy of the 4th channel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setYUVtoRGB](ScriptIntrinsicColorMatrix.md))`()` Set the matrix to convert from YUV to RGB with a direct copy of the 4th channel. |
| --- | --- |

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
| `rs` | [RenderScript](RenderScript.md)!:The RenderScript context |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [ScriptIntrinsicColorMatrix](ScriptIntrinsicColorMatrix.md)! | ScriptIntrinsicColorMatrix |

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
| `rs` | [RenderScript](RenderScript.md)!:The RenderScript context |
| `e` | [Element](Element.md)!:Element type for inputs and outputs, As of API 19, this parameter is ignored. The Element type check is performed in the kernel launch. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [ScriptIntrinsicColorMatrix](ScriptIntrinsicColorMatrix.md)! | ScriptIntrinsicColorMatrix |

### forEach

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Invoke the kernel and apply the matrix to each cell of input [Allocation](Allocation.md) and copy to the output [Allocation](Allocation.md). If the vector size of the input is less than four, the remaining components are treated as zero for the matrix multiply. If the output vector size is less than four, the unused vector components are discarded.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](Allocation.md)!:Input allocation |
| `aout` | [Allocation](Allocation.md)!:Output allocation |

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

Invoke the kernel and apply the matrix to each cell of input [Allocation](Allocation.md) and copy to the output [Allocation](Allocation.md). If the vector size of the input is less than four, the remaining components are treated as zero for the matrix multiply. If the output vector size is less than four, the unused vector components are discarded.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](Allocation.md)!:Input allocation |
| `aout` | [Allocation](Allocation.md)!:Output allocation |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### getKernelID

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKernelID(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for this intrinsic kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

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
| `f` | [Float4](Float4.md)!:The float4 value to be added. |

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
| --- | --- |
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
| `m` | [Matrix3f](Matrix3f.md)!:The 3x3 matrix to set. |

### setColorMatrix

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setColorMatrix(m: Matrix4f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the color matrix which will be applied to each cell of the image.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `m` | [Matrix4f](Matrix4f.md)!:The 4x4 matrix to set. |

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
