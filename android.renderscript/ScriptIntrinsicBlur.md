# ScriptIntrinsicBlur

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicBlur

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/ScriptIntrinsicBlur "View this page in Java") 
| --- | --- |

```
class ScriptIntrinsicBlur : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicBlur](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic Gausian blur filter. Applies a gaussian blur of the specified radius to all elements of an allocation.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicBlur](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#create(android.renderscript.RenderScript,%20android.renderscript.Element))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`)` Create an intrinsic for applying a blur to an allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#forEach(android.renderscript.Allocation))`(`aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Apply the filter to the input and save to the specified allocation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#forEach(android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Apply the filter to the input and save to the specified allocation. |
| --- | --- |
| [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID)! | [getFieldID_Input](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#getFieldID_Input())`()` Get a FieldID for the input field of this intrinsic. |
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelID](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#getKernelID())`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#setInput(android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Set the input of the blur. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRadius](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#setRadius(kotlin.Float))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the radius of the Blur. |

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

Create an intrinsic for applying a blur to an allocation. The default radius is 5.0. Supported elements types are [Element.U8](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8(android.renderscript.RenderScript)), [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript)).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:Element type for inputs and outputs |

| Return ||
|------------------------------------------------------------------------------------------------------------------|---------------------|
| [ScriptIntrinsicBlur](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur#)! | ScriptIntrinsicBlur |

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

### setInput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(ain: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the input of the blur. Must match the element type supplied during create.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The input allocation |

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
