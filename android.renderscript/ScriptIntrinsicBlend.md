# ScriptIntrinsicBlend

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicBlend

Kotlin| [Java](../android/renderscript/ScriptIntrinsicBlend.md) 
| --- | --- |

```
open class ScriptIntrinsicBlend : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](../android/renderscript/BaseObj.md) ||||
| | ↳ | [android.renderscript.Script](../android/renderscript/Script.md) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](../android/renderscript/ScriptIntrinsic.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.renderscript.ScriptIntrinsicBlend](../android/renderscript/ScriptIntrinsicBlend.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic kernels for blending two [android.renderscript.Allocation](../android/renderscript/Allocation.md) objects.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ScriptIntrinsicBlend](../android/renderscript/ScriptIntrinsicBlend.md)! | [create](../android/renderscript/ScriptIntrinsicBlend.md))`(`rs:` ` [RenderScript](../android/renderscript/RenderScript.md)!`, `e:` ` [Element](../android/renderscript/Element.md)!`)` Supported elements types are [Element.U8_4](../android/renderscript/Element.md)) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachAdd](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = min(src + dst, 1.0) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachAdd](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = min(src + dst, 1.0) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachClear](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = {0, 0, 0, 0} |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachClear](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = {0, 0, 0, 0} |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDst](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = dst This is a NOP. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDst](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = dst This is a NOP. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstAtop](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` dst = dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstAtop](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` dst = dst. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstIn](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = dst \* src. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstIn](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = dst \* src. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstOut](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = dst \* (1.0 - src.a) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstOut](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = dst \* (1.0 - src.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstOver](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = dst + src \* (1.0 - dst.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstOver](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = dst + src \* (1.0 - dst.a) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachMultiply](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = src \* dst |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachMultiply](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = src \* dst |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrc](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = src |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrc](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = src |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcAtop](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcAtop](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` dst. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcIn](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = src \* dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcIn](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = src \* dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcOut](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = src \* (1.0 - dst.a) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcOut](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = src \* (1.0 - dst.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcOver](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = src + dst \* (1.0 - src.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcOver](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = src + dst \* (1.0 - src.a) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSubtract](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = max(dst - src, 0.0) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSubtract](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = max(dst - src, 0.0) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachXor](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`)` Sets dst = {src. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachXor](../android/renderscript/ScriptIntrinsicBlend.md))`(`ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `opt:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Sets dst = {src. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDAdd](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the Add kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDClear](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the Clear kernel. |
| --- | --- |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDDst](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the Dst kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDDstAtop](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the DstAtop kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDDstIn](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the DstIn kernel. |
| --- | --- |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDDstOut](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the DstOut kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDDstOver](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the DstOver kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDMultiply](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the Multiply kernel. |
| --- | --- |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDSrc](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the Src kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDSrcAtop](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the SrcAtop kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDSrcIn](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the SrcIn kernel. |
| --- | --- |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDSrcOut](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the SrcOut kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDSrcOver](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the SrcOver kernel. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDSubtract](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the Subtract kernel. |
| --- | --- |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [getKernelIDXor](../android/renderscript/ScriptIntrinsicBlend.md))`()` Get a KernelID for the Xor kernel. |

## Public methods

### create

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    rs: RenderScript!, 
    e: Element!
): ScriptIntrinsicBlend!
```

**Deprecated:** *Deprecated in Java.*

Supported elements types are [Element.U8_4](../android/renderscript/Element.md))

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](../android/renderscript/RenderScript.md)!:The RenderScript context |
| `e` | [Element](../android/renderscript/Element.md)!:Element type for inputs and outputs |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------|
| [ScriptIntrinsicBlend](../android/renderscript/ScriptIntrinsicBlend.md)! | ScriptIntrinsicBlend |

### forEachAdd

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachAdd(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = min(src + dst, 1.0)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachAdd

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachAdd(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = min(src + dst, 1.0)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachClear

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachClear(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = {0, 0, 0, 0}

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachClear

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachClear(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = {0, 0, 0, 0}

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachDst

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDst(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = dst This is a NOP.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachDst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDst(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = dst This is a NOP.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachDstAtop

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDstAtop(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

dst = dst.rgb \* src.a + (1.0 - dst.a) \* src.rgb dst.a = src.a Note: Before API 23, the alpha channel was not correctly set. Please use with caution when targeting older APIs.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachDstAtop

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDstAtop(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

dst = dst.rgb \* src.a + (1.0 - dst.a) \* src.rgb dst.a = src.a Note: Before API 23, the alpha channel was not correctly set. Please use with caution when targeting older APIs.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachDstIn

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDstIn(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = dst \* src.a

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachDstIn

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDstIn(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = dst \* src.a

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachDstOut

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDstOut(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = dst \* (1.0 - src.a)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachDstOut

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDstOut(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = dst \* (1.0 - src.a)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachDstOver

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDstOver(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = dst + src \* (1.0 - dst.a)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachDstOver

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachDstOver(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = dst + src \* (1.0 - dst.a)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachMultiply

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachMultiply(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src \* dst

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachMultiply

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachMultiply(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src \* dst

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachSrc

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrc(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachSrc

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrc(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachSrcAtop

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrcAtop(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

dst.rgb = src.rgb \* dst.a + (1.0 - src.a) \* dst.rgb dst.a = dst.a

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachSrcAtop

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrcAtop(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

dst.rgb = src.rgb \* dst.a + (1.0 - src.a) \* dst.rgb dst.a = dst.a

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachSrcIn

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrcIn(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src \* dst.a

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachSrcIn

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrcIn(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src \* dst.a

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachSrcOut

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrcOut(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src \* (1.0 - dst.a)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachSrcOut

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrcOut(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src \* (1.0 - dst.a)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachSrcOver

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrcOver(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src + dst \* (1.0 - src.a)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachSrcOver

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSrcOver(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = src + dst \* (1.0 - src.a)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachSubtract

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSubtract(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = max(dst - src, 0.0)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachSubtract

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachSubtract(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = max(dst - src, 0.0)

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### forEachXor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachXor(
    ain: Allocation!, 
    aout: Allocation!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = {src.r \^ dst.r, src.g \^ dst.g, src.b \^ dst.b, src.a \^ dst.a}

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |

### forEachXor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachXor(
    ain: Allocation!, 
    aout: Allocation!, 
    opt: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets dst = {src.r \^ dst.r, src.g \^ dst.g, src.b \^ dst.b, src.a \^ dst.a}**Note:**this is NOT the Porter/Duff XOR mode; this is a bitwise xor.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ain` | [Allocation](../android/renderscript/Allocation.md)!:The source buffer |
| `aout` | [Allocation](../android/renderscript/Allocation.md)!:The destination buffer |
| `opt` | [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!:LaunchOptions for clipping |
| --- | --- |

### getKernelIDAdd

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDAdd(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Add kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDClear

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDClear(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Clear kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDDst

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDst(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Dst kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDDstAtop

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDstAtop(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the DstAtop kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDDstIn

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDstIn(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the DstIn kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDDstOut

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDstOut(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the DstOut kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDDstOver

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDstOver(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the DstOver kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDMultiply

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDMultiply(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Multiply kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDSrc

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrc(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Src kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDSrcAtop

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrcAtop(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the SrcAtop kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDSrcIn

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrcIn(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the SrcIn kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDSrcOut

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrcOut(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the SrcOut kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDSrcOver

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrcOver(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the SrcOver kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDSubtract

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSubtract(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Subtract kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |

### getKernelIDXor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDXor(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Xor kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](../android/renderscript/Script.KernelID.md)! | Script.KernelID The KernelID object. |
