# ScriptIntrinsicBlend

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptIntrinsicBlend

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/ScriptIntrinsicBlend "View this page in Java") 

```
open class ScriptIntrinsicBlend : ScriptIntrinsic
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) |||
| | | ↳ | [android.renderscript.ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) ||
| | | | ↳ | [android.renderscript.ScriptIntrinsicBlend](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Intrinsic kernels for blending two [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) objects.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ScriptIntrinsicBlend](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#create(android.renderscript.RenderScript,%20android.renderscript.Element))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`)` Supported elements types are [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript)) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachAdd](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachAdd(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = min(src + dst, 1.0) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachAdd](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachAdd(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = min(src + dst, 1.0) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachClear](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachClear(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = {0, 0, 0, 0} |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachClear](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachClear(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = {0, 0, 0, 0} |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDst](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDst(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = dst This is a NOP. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDst](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDst(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = dst This is a NOP. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstAtop](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDstAtop(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` dst = dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstAtop](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDstAtop(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` dst = dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstIn](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDstIn(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = dst \* src. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstIn](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDstIn(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = dst \* src. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstOut](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDstOut(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = dst \* (1.0 - src.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstOut](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDstOut(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = dst \* (1.0 - src.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstOver](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDstOver(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = dst + src \* (1.0 - dst.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachDstOver](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachDstOver(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = dst + src \* (1.0 - dst.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachMultiply](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachMultiply(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = src \* dst |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachMultiply](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachMultiply(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = src \* dst |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrc](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrc(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = src |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrc](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrc(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = src |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcAtop](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrcAtop(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcAtop](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrcAtop(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcIn](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrcIn(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = src \* dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcIn](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrcIn(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = src \* dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcOut](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrcOut(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = src \* (1.0 - dst.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcOut](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrcOut(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = src \* (1.0 - dst.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcOver](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrcOver(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = src + dst \* (1.0 - src.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSrcOver](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSrcOver(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = src + dst \* (1.0 - src.a) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSubtract](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSubtract(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = max(dst - src, 0.0) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachSubtract](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachSubtract(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = max(dst - src, 0.0) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachXor](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachXor(android.renderscript.Allocation,%20android.renderscript.Allocation))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets dst = {src. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachXor](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#forEachXor(android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `opt:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Sets dst = {src. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDAdd](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDAdd())`()` Get a KernelID for the Add kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDClear](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDClear())`()` Get a KernelID for the Clear kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDDst](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDDst())`()` Get a KernelID for the Dst kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDDstAtop](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDDstAtop())`()` Get a KernelID for the DstAtop kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDDstIn](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDDstIn())`()` Get a KernelID for the DstIn kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDDstOut](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDDstOut())`()` Get a KernelID for the DstOut kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDDstOver](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDDstOver())`()` Get a KernelID for the DstOver kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDMultiply](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDMultiply())`()` Get a KernelID for the Multiply kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDSrc](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDSrc())`()` Get a KernelID for the Src kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDSrcAtop](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDSrcAtop())`()` Get a KernelID for the SrcAtop kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDSrcIn](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDSrcIn())`()` Get a KernelID for the SrcIn kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDSrcOut](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDSrcOut())`()` Get a KernelID for the SrcOut kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDSrcOver](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDSrcOver())`()` Get a KernelID for the SrcOver kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDSubtract](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDSubtract())`()` Get a KernelID for the Subtract kernel. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [getKernelIDXor](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#getKernelIDXor())`()` Get a KernelID for the Xor kernel. |

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

Supported elements types are [Element.U8_4](https://developer.android.com/reference/kotlin/android/renderscript/Element#U8_4(android.renderscript.RenderScript))

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:Element type for inputs and outputs |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------|
| [ScriptIntrinsicBlend](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend#)! | ScriptIntrinsicBlend |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |

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
| `ain` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The source buffer |
| `aout` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The destination buffer |
| `opt` | [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!:LaunchOptions for clipping |

### getKernelIDAdd

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDAdd(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Add kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDClear

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDClear(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Clear kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDDst

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDst(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Dst kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDDstAtop

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDstAtop(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the DstAtop kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDDstIn

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDstIn(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the DstIn kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDDstOut

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDstOut(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the DstOut kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDDstOver

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDDstOver(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the DstOver kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDMultiply

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDMultiply(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Multiply kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDSrc

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrc(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Src kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDSrcAtop

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrcAtop(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the SrcAtop kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDSrcIn

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrcIn(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the SrcIn kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDSrcOut

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrcOut(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the SrcOut kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDSrcOver

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSrcOver(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the SrcOver kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDSubtract

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDSubtract(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Subtract kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |

### getKernelIDXor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKernelIDXor(): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Get a KernelID for the Xor kernel.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | Script.KernelID The KernelID object. |
