# ScriptIntrinsicLUT

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicLUT

Kotlin| [Java](ScriptIntrinsicLUT.md) 
| --- | --- |

```
class ScriptIntrinsicLUT : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicLUT](ScriptIntrinsicLUT.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic for applying a per-channel lookup table. Each channel of the input has an independant lookup table. The tables are 256 entries in size and can cover the full value range of [Element.U8_4](Element.md)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ScriptIntrinsicLUT](ScriptIntrinsicLUT.md)! | [create](ScriptIntrinsicLUT.md))`(`rs:` ` [RenderScript](RenderScript.md)!`, `e:` ` [Element](Element.md)!`)` Supported elements types are [Element.U8_4](Element.md))The defaults tables are identity. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](ScriptIntrinsicLUT.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicLUT.md))`(`ain:` ` [Allocation](Allocation.md)!`, `aout:` ` [Allocation](Allocation.md)!`)` Invoke the kernel and apply the lookup to each cell of ain and copy to aout. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ScriptIntrinsicLUT.md))`(`ain:` ` [Allocation](Allocation.md)!`, `aout:` ` [Allocation](Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Invoke the kernel and apply the lookup to each cell of ain and copy to aout. |
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelID](ScriptIntrinsicLUT.md))`()` Get a KernelID for this intrinsic kernel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](ScriptIntrinsicLUT.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an entry in the alpha channel lookup table |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlue](ScriptIntrinsicLUT.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an entry in the blue channel lookup table |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGreen](ScriptIntrinsicLUT.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an entry in the green channel lookup table |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRed](ScriptIntrinsicLUT.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an entry in the red channel lookup table |
| --- | --- |

## Public methods

### create

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    rs: RenderScript!, 
    e: Element!
): ScriptIntrinsicLUT!
```

**Deprecated:** *Deprecated in Java.*

Supported elements types are [Element.U8_4](Element.md))The defaults tables are identity.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:The RenderScript context |
| `e` | [Element](Element.md)!:Element type for intputs and outputs |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------|
| [ScriptIntrinsicLUT](ScriptIntrinsicLUT.md)! | ScriptIntrinsicLUT |

### destroy

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun destroy(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### forEach

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](Allocation.md)!:Input allocation |
| `aout` | [Allocation](Allocation.md)!:Output allocation |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:Options for clipping |
| --- | --- |

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

### setAlpha

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAlpha(
    index: Int, 
    value: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set an entry in the alpha channel lookup table

| Parameters ||
|---------|------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0-255 |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0-255 |

### setBlue

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setBlue(
    index: Int, 
    value: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set an entry in the blue channel lookup table

| Parameters ||
|---------|------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0-255 |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0-255 |

### setGreen

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setGreen(
    index: Int, 
    value: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set an entry in the green channel lookup table

| Parameters ||
|---------|------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0-255 |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0-255 |

### setRed

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRed(
    index: Int, 
    value: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set an entry in the red channel lookup table

| Parameters ||
|---------|------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0-255 |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Must be 0-255 |
