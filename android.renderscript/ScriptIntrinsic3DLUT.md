# ScriptIntrinsic3DLUT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsic3DLUT

Kotlin| [Java](ScriptIntrinsic3DLUT.md) 
| --- | --- |

```
class ScriptIntrinsic3DLUT : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsic3DLUT](ScriptIntrinsic3DLUT.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for converting RGB to RGBA by using a 3D lookup table. The incoming r,g,b values are use as normalized x,y,z coordinates into a 3D allocation. The 8 nearest values are sampled and linearly interpolated. The result is placed in the output.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsic3DLUT](ScriptIntrinsic3DLUT.md)! | [create](ScriptIntrinsic3DLUT.md))`(`rs:` ` [RenderScript](RenderScript.md)!`, `e:` ` [Element](Element.md)!`)` Supported elements types are [Element.U8_4](Element.md))The defaults tables are identity. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsic3DLUT.md))`(`ain:` ` [Allocation](Allocation.md)!`, `aout:` ` [Allocation](Allocation.md)!`)` Invoke the kernel and apply the lookup to each cell of ain and copy to aout. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsic3DLUT.md))`(`ain:` ` [Allocation](Allocation.md)!`, `aout:` ` [Allocation](Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Invoke the kernel and apply the lookup to each cell of ain and copy to aout. |
| --- | --- |
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelID](ScriptIntrinsic3DLUT.md))`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLUT](ScriptIntrinsic3DLUT.md))`(`lut:` ` [Allocation](Allocation.md)!`)` Sets the [android.renderscript.Allocation](Allocation.md) to be used as the lookup table. |

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

Supported elements types are [Element.U8_4](Element.md))The defaults tables are identity.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:The RenderScript context |
| `e` | [Element](Element.md)!:Element type for intputs and outputs |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------|
| [ScriptIntrinsic3DLUT](ScriptIntrinsic3DLUT.md)! | ScriptIntrinsic3DLUT |

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
| `ain` | [Allocation](Allocation.md)!:Input allocation |
| `aout` | [Allocation](Allocation.md)!:Output allocation |

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
| `ain` | [Allocation](Allocation.md)!:Input allocation |
| `aout` | [Allocation](Allocation.md)!:Output allocation |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:Launch options for kernel |
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
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### setLUT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLUT(lut: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [android.renderscript.Allocation](Allocation.md) to be used as the lookup table. The lookup table must use the same [android.renderscript.Element](Element.md) as the intrinsic.
