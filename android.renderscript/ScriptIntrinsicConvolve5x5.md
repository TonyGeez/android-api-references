# ScriptIntrinsicConvolve5x5

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicConvolve5x5

Kotlin| [Java](ScriptIntrinsicConvolve5x5.md) 
| --- | --- |

```
class ScriptIntrinsicConvolve5x5 : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicConvolve5x5](ScriptIntrinsicConvolve5x5.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for applying a 5x5 convolve to an allocation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicConvolve5x5](ScriptIntrinsicConvolve5x5.md)! | [create](ScriptIntrinsicConvolve5x5.md))`(`rs:` ` [RenderScript](RenderScript.md)!`, `e:` ` [Element](Element.md)!`)` Supported elements types are [Element.U8](Element.md)), [android.renderscript.Element#U8_2](Element.md)), [Element.U8_3](Element.md)), [Element.U8_4](Element.md)), [Element.F32](Element.md)), [Element.F32_2](Element.md)), [android.renderscript.Element#F32_3](Element.md)), and [Element.F32_4](Element.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicConvolve5x5.md))`(`aout:` ` [Allocation](Allocation.md)!`)` Apply the filter to the input and save to the specified allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicConvolve5x5.md))`(`aout:` ` [Allocation](Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Apply the filter to the input and save to the specified allocation. |
| --- | --- |
| [Script.FieldID](../android/renderscript/Script.FieldID.md)! | [getFieldID_Input](ScriptIntrinsicConvolve5x5.md))`()` Get a FieldID for the input field of this intrinsic. |
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelID](ScriptIntrinsicConvolve5x5.md))`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCoefficients](ScriptIntrinsicConvolve5x5.md))`(`v:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Set the coefficients for the convolve. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](ScriptIntrinsicConvolve5x5.md))`(`ain:` ` [Allocation](Allocation.md)!`)` Set the input of the 5x5 convolve. |

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

Supported elements types are [Element.U8](Element.md)), [android.renderscript.Element#U8_2](Element.md)), [Element.U8_3](Element.md)), [Element.U8_4](Element.md)), [Element.F32](Element.md)), [Element.F32_2](Element.md)), [android.renderscript.Element#F32_3](Element.md)), and [Element.F32_4](Element.md)).

The default coefficients are:` `

` [ 0, 0, 0, 0, 0 ] `

` [ 0, 0, 0, 0, 0 ] `

` [ 0, 0, 1, 0, 0 ] `

` [ 0, 0, 0, 0, 0 ] `

` [ 0, 0, 0, 0, 0 ] `

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:The RenderScript context |
| `e` | [Element](Element.md)!:Element type for intputs and outputs |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [ScriptIntrinsicConvolve5x5](ScriptIntrinsicConvolve5x5.md)! | ScriptIntrinsicConvolve5x5 |

### forEach

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(aout: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Apply the filter to the input and save to the specified allocation.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](Allocation.md)!:Output allocation. Must match creation element type. |

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
| `aout` | [Allocation](Allocation.md)!:Output allocation. Must match creation element type. |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |

### getFieldID_Input

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFieldID_Input(): Script.FieldID!
```

**Deprecated:** *Deprecated in Java.*

Get a FieldID for the input field of this intrinsic.

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------------------|
| [Script.FieldID](../android/renderscript/Script.FieldID.md)! | Script.FieldID The FieldID object. |

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
| `ain` | [Allocation](Allocation.md)!:The input allocation. |
