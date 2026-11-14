# ScriptIntrinsicYuvToRGB

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicYuvToRGB

Kotlin| [Java](../android/renderscript/ScriptIntrinsicYuvToRGB.md) 
| --- | --- |

```
class ScriptIntrinsicYuvToRGB : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](../android/renderscript/BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](../android/renderscript/Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](../android/renderscript/ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicYuvToRGB](../android/renderscript/ScriptIntrinsicYuvToRGB.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for converting an Android YUV buffer to RGB. The input allocation should be supplied in a supported YUV format as a YUV element Allocation. The output is RGBA; the alpha channel will be set to 255.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicYuvToRGB](../android/renderscript/ScriptIntrinsicYuvToRGB.md)! | [create](../android/renderscript/ScriptIntrinsicYuvToRGB.md))`(`rs:` ` [RenderScript](../android/renderscript/RenderScript.md)!`, `e:` ` [Element](../android/renderscript/Element.md)!`)` Create an intrinsic for converting YUV to RGB. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../android/renderscript/ScriptIntrinsicYuvToRGB.md))`(`aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Convert the image to RGB. |
| [Script.FieldID](../android/renderscript/Script.FieldID.md)! | [getFieldID_Input](../android/renderscript/ScriptIntrinsicYuvToRGB.md))`()` Get a FieldID for the input field of this intrinsic. |
| --- | --- |
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelID](../android/renderscript/ScriptIntrinsicYuvToRGB.md))`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](../android/renderscript/ScriptIntrinsicYuvToRGB.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Set the input yuv allocation, must be [Element.U8](../android/renderscript/Element.md)). |

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

Create an intrinsic for converting YUV to RGB. Supported elements types are [Element.U8_4](../android/renderscript/Element.md))

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](../android/renderscript/RenderScript.md)!:The RenderScript context |
| `e` | [Element](../android/renderscript/Element.md)!:Element type for output |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [ScriptIntrinsicYuvToRGB](../android/renderscript/ScriptIntrinsicYuvToRGB.md)! | ScriptIntrinsicYuvToRGB |

### forEach

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(aout: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Convert the image to RGB.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:Output allocation. Must match creation element type. |

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

### setInput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the input yuv allocation, must be [Element.U8](../android/renderscript/Element.md)).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The input allocation. |
