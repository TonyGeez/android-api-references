# ScriptIntrinsicConvolve5x5

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicConvolve5x5

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/ScriptIntrinsicConvolve5x5 "View this page in Java") 

```
class ScriptIntrinsicConvolve5x5 : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) ||
| | | | ↳ | [android.renderscript.ScriptIntrinsicConvolve5x5](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for applying a 5x5 convolve to an allocation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicConvolve5x5](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#create(android.renderscript.RenderScript,%20android.renderscript.Element))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`)` Supported elements types are [Element.U8](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8(android.renderscript.RenderScript)), [android.renderscript.Element#U8_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_2(android.renderscript.RenderScript)), [Element.U8_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_3(android.renderscript.RenderScript)), [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript)), [Element.F32](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32(android.renderscript.RenderScript)), [Element.F32_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_2(android.renderscript.RenderScript)), [android.renderscript.Element#F32_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_3(android.renderscript.RenderScript)), and [Element.F32_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_4(android.renderscript.RenderScript)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#forEach(android.renderscript.Allocation))`(`aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Apply the filter to the input and save to the specified allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#forEach(android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Apply the filter to the input and save to the specified allocation. |
| [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID)! | [getFieldID_Input](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#getFieldID_Input())`()` Get a FieldID for the input field of this intrinsic. |
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelID](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#getKernelID())`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCoefficients](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#setCoefficients(kotlin.FloatArray))`(`v:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Set the coefficients for the convolve. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#setInput(android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Set the input of the 5x5 convolve. |

## Public methods

### create

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    rs: RenderScript!, 
    e: Element!
): ScriptIntrinsicConvolve5x5!
```

**Deprecated:** *Deprecated in Java.*

Supported elements types are [Element.U8](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8(android.renderscript.RenderScript)), [android.renderscript.Element#U8_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_2(android.renderscript.RenderScript)), [Element.U8_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_3(android.renderscript.RenderScript)), [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript)), [Element.F32](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32(android.renderscript.RenderScript)), [Element.F32_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_2(android.renderscript.RenderScript)), [android.renderscript.Element#F32_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_3(android.renderscript.RenderScript)), and [Element.F32_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_4(android.renderscript.RenderScript)).

The default coefficients are:` `

` [ 0, 0, 0, 0, 0 ] `

` [ 0, 0, 0, 0, 0 ] `

` [ 0, 0, 1, 0, 0 ] `

` [ 0, 0, 0, 0, 0 ] `

` [ 0, 0, 0, 0, 0 ] `

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:Element type for intputs and outputs |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [ScriptIntrinsicConvolve5x5](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5#)! | ScriptIntrinsicConvolve5x5 |

### forEach

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(aout: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Apply the filter to the input and save to the specified allocation.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation. Must match creation element type. |

### forEach

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Apply the filter to the input and save to the specified allocation.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation. Must match creation element type. |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

### getFieldID_Input

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFieldID_Input(): Script.FieldID!
```

**Deprecated:** *Deprecated in Java.*

Get a FieldID for the input field of this intrinsic.

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------------------|
| [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID)! | Script.FieldID The FieldID object. |

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

### setCoefficients

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCoefficients(v: FloatArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the coefficients for the convolve.

The convolve layout is:` `

` [ 0, 1, 2, 3, 4 ] `

` [ 5, 6, 7, 8, 9 ] `

` [ 10, 11, 12, 13, 14 ] `

` [ 15, 16, 17, 18, 19 ] `

` [ 20, 21, 22, 23, 24 ] `

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------|
| `v` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of coefficients to set |

### setInput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the input of the 5x5 convolve. Must match the element type supplied during create.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The input allocation. |
