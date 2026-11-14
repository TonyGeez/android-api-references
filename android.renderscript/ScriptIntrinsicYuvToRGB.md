# ScriptIntrinsicYuvToRGB

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicYuvToRGB

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/ScriptIntrinsicYuvToRGB "View this page in Java") 
| --- | --- |

```
class ScriptIntrinsicYuvToRGB : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicYuvToRGB](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for converting an Android YUV buffer to RGB. The input allocation should be supplied in a supported YUV format as a YUV element Allocation. The output is RGBA; the alpha channel will be set to 255.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicYuvToRGB](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB#create(android.renderscript.RenderScript,%20android.renderscript.Element))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`)` Create an intrinsic for converting YUV to RGB. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB#forEach(android.renderscript.Allocation))`(`aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Convert the image to RGB. |
| [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID)! | [getFieldID_Input](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB#getFieldID_Input())`()` Get a FieldID for the input field of this intrinsic. |
| --- | --- |
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelID](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB#getKernelID())`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB#setInput(android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Set the input yuv allocation, must be [Element.U8](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8(android.renderscript.RenderScript)). |

## Public methods

### create

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    rs: RenderScript!, 
    e: Element!
): ScriptIntrinsicYuvToRGB!
```

**Deprecated:** *Deprecated in Java.*

Create an intrinsic for converting YUV to RGB. Supported elements types are [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript))

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:Element type for output |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [ScriptIntrinsicYuvToRGB](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB#)! | ScriptIntrinsicYuvToRGB |

### forEach

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(aout: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Convert the image to RGB.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation. Must match creation element type. |

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

### setInput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the input yuv allocation, must be [Element.U8](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8(android.renderscript.RenderScript)).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The input allocation. |
