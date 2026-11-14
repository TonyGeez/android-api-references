# ScriptIntrinsicBlur

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicBlur

Kotlin| [Java](ScriptIntrinsicBlur.md) 
| --- | --- |

```
class ScriptIntrinsicBlur : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicBlur](ScriptIntrinsicBlur.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic Gausian blur filter. Applies a gaussian blur of the specified radius to all elements of an allocation.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicBlur](ScriptIntrinsicBlur.md)! | [create](ScriptIntrinsicBlur.md))`(`rs:` ` [RenderScript](RenderScript.md)!`, `e:` ` [Element](Element.md)!`)` Create an intrinsic for applying a blur to an allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicBlur.md))`(`aout:` ` [Allocation](Allocation.md)!`)` Apply the filter to the input and save to the specified allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicBlur.md))`(`aout:` ` [Allocation](Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Apply the filter to the input and save to the specified allocation. |
| --- | --- |
| [Script.FieldID](../android/renderscript/Script.FieldID.md)! | [getFieldID_Input](ScriptIntrinsicBlur.md))`()` Get a FieldID for the input field of this intrinsic. |
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelID](ScriptIntrinsicBlur.md))`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](ScriptIntrinsicBlur.md))`(`ain:` ` [Allocation](Allocation.md)!`)` Set the input of the blur. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRadius](ScriptIntrinsicBlur.md))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the radius of the Blur. |

## Public methods

### create

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    rs: RenderScript!, 
    e: Element!
): ScriptIntrinsicBlur!
```

**Deprecated:** *Deprecated in Java.*

Create an intrinsic for applying a blur to an allocation. The default radius is 5.0. Supported elements types are [Element.U8](Element.md)), [Element.U8_4](Element.md)).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:The RenderScript context |
| `e` | [Element](Element.md)!:Element type for inputs and outputs |

| Return ||
|------------------------------------------------------------------------------------------------------------------|---------------------|
| [ScriptIntrinsicBlur](ScriptIntrinsicBlur.md)! | ScriptIntrinsicBlur |

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

### setInput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the input of the blur. Must match the element type supplied during create.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](Allocation.md)!:The input allocation |

### setRadius

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRadius(radius: Float): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the radius of the Blur. Supported range 0 \< radius \<= 25

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The radius of the blur |
