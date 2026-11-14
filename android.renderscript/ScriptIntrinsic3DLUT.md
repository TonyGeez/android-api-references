# ScriptIntrinsic3DLUT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsic3DLUT

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/ScriptIntrinsic3DLUT "View this page in Java") 
| --- | --- |

```
class ScriptIntrinsic3DLUT : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsic3DLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for converting RGB to RGBA by using a 3D lookup table. The incoming r,g,b values are use as normalized x,y,z coordinates into a 3D allocation. The 8 nearest values are sampled and linearly interpolated. The result is placed in the output.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsic3DLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT#create(android.renderscript.RenderScript,%20android.renderscript.Element))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`)` Supported elements types are [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript))The defaults tables are identity. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT#forEach(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Invoke the kernel and apply the lookup to each cell of ain and copy to aout. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT#forEach(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Invoke the kernel and apply the lookup to each cell of ain and copy to aout. |
| --- | --- |
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelID](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT#getKernelID())`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT#setLUT(android.renderscript.Allocation))`(`lut:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets the [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) to be used as the lookup table. |

## Public methods

### create

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    rs: RenderScript!, 
    e: Element!
): ScriptIntrinsic3DLUT!
```

**Deprecated:** *Deprecated in Java.*

Supported elements types are [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript))The defaults tables are identity.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:Element type for intputs and outputs |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------|
| [ScriptIntrinsic3DLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT#)! | ScriptIntrinsic3DLUT |

### forEach

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Invoke the kernel and apply the lookup to each cell of ain and copy to aout.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Input allocation |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation |

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

Invoke the kernel and apply the lookup to each cell of ain and copy to aout.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Input allocation |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:Output allocation |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:Launch options for kernel |
| --- | --- |

### getKernelID

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKernelID(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for this intrinsic kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### setLUT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLUT(lut: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) to be used as the lookup table. The lookup table must use the same [android.renderscript.Element](https://developer.android.com/reference/kotlin/android/renderscript/Element) as the intrinsic.
