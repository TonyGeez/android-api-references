# ScriptIntrinsicResize

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicResize

Kotlin| [Java](../android/renderscript/ScriptIntrinsicResize.md) 
| --- | --- |

```
class ScriptIntrinsicResize : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](../android/renderscript/BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](../android/renderscript/Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](../android/renderscript/ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicResize](../android/renderscript/ScriptIntrinsicResize.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for performing a resize of a 2D allocation.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicResize](../android/renderscript/ScriptIntrinsicResize.md)! | [create](../android/renderscript/ScriptIntrinsicResize.md))`(`rs:` ` [RenderScript](../android/renderscript/RenderScript.md)!`)` Supported elements types are [Element.U8](../android/renderscript/Element.md)), [android.renderscript.Element#U8_2](../android/renderscript/Element.md)), [Element.U8_3](../android/renderscript/Element.md)), [Element.U8_4](../android/renderscript/Element.md)) [Element.F32](../android/renderscript/Element.md)), [Element.F32_2](../android/renderscript/Element.md)), [android.renderscript.Element#F32_3](../android/renderscript/Element.md)), [Element.F32_4](../android/renderscript/Element.md)) |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach_bicubic](../android/renderscript/ScriptIntrinsicResize.md))`(`aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Resize copy the input allocation to the output specified. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach_bicubic](../android/renderscript/ScriptIntrinsicResize.md))`(`aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Resize copy the input allocation to the output specified. |
| --- | --- |
| [Script.FieldID](../android/renderscript/Script.FieldID.md)! | [getFieldID_Input](../android/renderscript/ScriptIntrinsicResize.md))`()` Get a FieldID for the input field of this intrinsic. |
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelID_bicubic](../android/renderscript/ScriptIntrinsicResize.md))`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](../android/renderscript/ScriptIntrinsicResize.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Set the input of the resize. |
| --- | --- |

## Public methods

### create

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(rs: RenderScript!): ScriptIntrinsicResize!
```

**Deprecated:** *Deprecated in Java.*

Supported elements types are [Element.U8](../android/renderscript/Element.md)), [android.renderscript.Element#U8_2](../android/renderscript/Element.md)), [Element.U8_3](../android/renderscript/Element.md)), [Element.U8_4](../android/renderscript/Element.md)) [Element.F32](../android/renderscript/Element.md)), [Element.F32_2](../android/renderscript/Element.md)), [android.renderscript.Element#F32_3](../android/renderscript/Element.md)), [Element.F32_4](../android/renderscript/Element.md))

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](../android/renderscript/RenderScript.md)!:The RenderScript context |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------|
| [ScriptIntrinsicResize](../android/renderscript/ScriptIntrinsicResize.md)! | ScriptIntrinsicResize |

### forEach_bicubic

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach_bicubic(aout: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Resize copy the input allocation to the output specified. The Allocation is rescaled if necessary using bi-cubic interpolation.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:Output allocation. Element type must match current input. Must not be same as input. |

### forEach_bicubic

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach_bicubic(
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Resize copy the input allocation to the output specified. The Allocation is rescaled if necessary using bi-cubic interpolation.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:Output allocation. Element type must match current input. |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |

### getFieldID_Input

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFieldID_Input(): Script.FieldID!
```

**Deprecated:** *Deprecated in Java.*

Get a FieldID for the input field of this intrinsic.

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------------------|
| [Script.FieldID](../android/renderscript/Script.FieldID.md)! | Script.FieldID The FieldID object. |

### getKernelID_bicubic

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKernelID_bicubic(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for this intrinsic kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### setInput

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the input of the resize. Must match the element type supplied during create.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The input allocation. |
