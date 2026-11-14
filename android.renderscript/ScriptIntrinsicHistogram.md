# ScriptIntrinsicHistogram

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicHistogram

Kotlin| [Java](ScriptIntrinsicHistogram.md) 
| --- | --- |

```
class ScriptIntrinsicHistogram : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicHistogram](ScriptIntrinsicHistogram.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic Histogram filter.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicHistogram](ScriptIntrinsicHistogram.md)! | [create](ScriptIntrinsicHistogram.md))`(`rs:` ` [RenderScript](RenderScript.md)!`, `e:` ` [Element](Element.md)!`)` Create an intrinsic for calculating the histogram of an uchar or uchar4 image. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicHistogram.md))`(`ain:` ` [Allocation](Allocation.md)!`)` Process an input buffer and place the histogram into the output allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicHistogram.md))`(`ain:` ` [Allocation](Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Process an input buffer and place the histogram into the output allocation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach_Dot](ScriptIntrinsicHistogram.md))`(`ain:` ` [Allocation](Allocation.md)!`)` Process an input buffer and place the histogram into the output allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach_Dot](ScriptIntrinsicHistogram.md))`(`ain:` ` [Allocation](Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Process an input buffer and place the histogram into the output allocation. |
| [Script.FieldID](../android/renderscript/Script.FieldID.md)! | [getFieldID_Input](ScriptIntrinsicHistogram.md))`()` Get a FieldID for the input field of this intrinsic. |
| --- | --- |
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelID_Separate](ScriptIntrinsicHistogram.md))`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDotCoefficients](ScriptIntrinsicHistogram.md))`(`r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `g:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the coefficients used for the RGBA to Luminocity calculation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutput](ScriptIntrinsicHistogram.md))`(`aout:` ` [Allocation](Allocation.md)!`)` Set the output of the histogram. |
| --- | --- |

## Public methods

### create

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    rs: RenderScript!, 
    e: Element!
): ScriptIntrinsicHistogram!
```

**Deprecated:** *Deprecated in Java.*

Create an intrinsic for calculating the histogram of an uchar or uchar4 image. Supported elements types are [Element.U8_4](Element.md)), [Element.U8_3](Element.md)), [Element.U8_2](Element.md)), [Element.U8](Element.md))

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:The RenderScript context |
| `e` | [Element](Element.md)!:Element type for inputs |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [ScriptIntrinsicHistogram](ScriptIntrinsicHistogram.md)! | ScriptIntrinsicHistogram |

### forEach

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Process an input buffer and place the histogram into the output allocation. The output allocation may be a narrower vector size than the input. In this case the vector size of the output is used to determine how many of the input channels are used in the computation. This is useful if you have an RGBA input buffer but only want the histogram for RGB. 1D and 2D input allocations are supported.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](Allocation.md)!:The input image |

### forEach

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(
    ain: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Process an input buffer and place the histogram into the output allocation. The output allocation may be a narrower vector size than the input. In this case the vector size of the output is used to determine how many of the input channels are used in the computation. This is useful if you have an RGBA input buffer but only want the histogram for RGB. 1D and 2D input allocations are supported.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](Allocation.md)!:The input image |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |

### forEach_Dot

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach_Dot(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Process an input buffer and place the histogram into the output allocation. The dot product of the input channel and the coefficients from 'setDotCoefficients' are used to calculate the output values. 1D and 2D input allocations are supported.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](Allocation.md)!:The input image |

### forEach_Dot

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach_Dot(
    ain: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Process an input buffer and place the histogram into the output allocation. The dot product of the input channel and the coefficients from 'setDotCoefficients' are used to calculate the output values. 1D and 2D input allocations are supported.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](Allocation.md)!:The input image |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |

### getFieldID_Input

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFieldID_Input(): Script.FieldID!
```

**Deprecated:** *Deprecated in Java.*

Get a FieldID for the input field of this intrinsic.

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------------------|
| [Script.FieldID](../android/renderscript/Script.FieldID.md)! | Script.FieldID The FieldID object. |

### getKernelID_Separate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKernelID_Separate(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for this intrinsic kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### setDotCoefficients

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDotCoefficients(
    r: Float, 
    g: Float, 
    b: Float, 
    a: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the coefficients used for the RGBA to Luminocity calculation. The default is {0.299f, 0.587f, 0.114f, 0.f}. Coefficients must be \>= 0 and sum to 1.0 or less.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Red coefficient |
| `g` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Green coefficient |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Blue coefficient |
| --- | --- |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Alpha coefficient |

### setOutput

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOutput(aout: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the output of the histogram. 32 bit integer types are supported.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](Allocation.md)!:The output allocation |
