# ScriptIntrinsicResize

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicResize

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/ScriptIntrinsicResize "View this page in Java") 
| --- | --- |

```
class ScriptIntrinsicResize : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicResize](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for performing a resize of a 2D allocation.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicResize](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#create(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Supported elements types are [Element.U8](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8(android.renderscript.RenderScript)), [android.renderscript.Element#U8_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_2(android.renderscript.RenderScript)), [Element.U8_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_3(android.renderscript.RenderScript)), [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript)) [Element.F32](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32(android.renderscript.RenderScript)), [Element.F32_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_2(android.renderscript.RenderScript)), [android.renderscript.Element#F32_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_3(android.renderscript.RenderScript)), [Element.F32_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_4(android.renderscript.RenderScript)) |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach_bicubic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#forEach_bicubic(android.renderscript.Allocation))`(`aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Resize copy the input allocation to the output specified. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach_bicubic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#forEach_bicubic(android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Resize copy the input allocation to the output specified. |
| --- | --- |
| [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID)! | [getFieldID_Input](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#getFieldID_Input())`()` Get a FieldID for the input field of this intrinsic. |
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelID_bicubic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#getKernelID_bicubic())`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#setInput(android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Set the input of the resize. |
| --- | --- |

## Public methods

### create

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(rs: RenderScript!): ScriptIntrinsicResize!
```

**Deprecated:** *Deprecated in Java.*

Supported elements types are [Element.U8](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8(android.renderscript.RenderScript)), [android.renderscript.Element#U8_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_2(android.renderscript.RenderScript)), [Element.U8_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_3(android.renderscript.RenderScript)), [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript)) [Element.F32](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32(android.renderscript.RenderScript)), [Element.F32_2](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_2(android.renderscript.RenderScript)), [android.renderscript.Element#F32_3](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_3(android.renderscript.RenderScript)), [Element.F32_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#F32_4(android.renderscript.RenderScript))

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------|
| [ScriptIntrinsicResize](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize#)! | ScriptIntrinsicResize |

### forEach_bicubic

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach_bicubic(aout: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Resize copy the input allocation to the output specified. The Allocation is rescaled if necessary using bi-cubic interpolation.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation. Element type must match current input. Must not be same as input. |

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
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation. Element type must match current input. |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

### getFieldID_Input

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFieldID_Input(): Script.FieldID!
```

**Deprecated:** *Deprecated in Java.*

Get a FieldID for the input field of this intrinsic.

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------------------|
| [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID)! | Script.FieldID The FieldID object. |

### getKernelID_bicubic

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKernelID_bicubic(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for this intrinsic kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### setInput

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the input of the resize. Must match the element type supplied during create.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The input allocation. |
