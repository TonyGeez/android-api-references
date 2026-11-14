# Script

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Script

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/Script "View this page in Java") 

```
open class Script : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script#) |

| Known Direct Subclasses [ScriptC](https://developer.android.com/reference/kotlin/android/renderscript/ScriptC), [ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) |--------------------------------------------------------------------------------------------------------|----------------------------------------------| | [ScriptC](https://developer.android.com/reference/kotlin/android/renderscript/ScriptC) | The superclass for all user-defined scripts. | | [ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) | Base class for all Intrinsic scripts. | |

| Known Indirect Subclasses [ScriptIntrinsic3DLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT), [ScriptIntrinsicBLAS](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS), [ScriptIntrinsicBlend](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend), [ScriptIntrinsicBlur](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur), [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix), [ScriptIntrinsicConvolve3x3](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve3x3), [ScriptIntrinsicConvolve5x5](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5), [ScriptIntrinsicHistogram](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicHistogram), [ScriptIntrinsicLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicLUT), [ScriptIntrinsicResize](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize), [ScriptIntrinsicYuvToRGB](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB) |------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ScriptIntrinsic3DLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT) | Intrinsic for converting RGB to RGBA by using a 3D lookup table. | | [ScriptIntrinsicBLAS](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS) | ScriptIntrinsicBLAS class provides high performance RenderScript APIs to BLAS. | | [ScriptIntrinsicBlend](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend) | Intrinsic kernels for blending two [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) objects. | | [ScriptIntrinsicBlur](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur) | Intrinsic Gausian blur filter. | | [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix) | Intrinsic for applying a color matrix to allocations. | | [ScriptIntrinsicConvolve3x3](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve3x3) | Intrinsic for applying a 3x3 convolve to an allocation. | | [ScriptIntrinsicConvolve5x5](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5) | Intrinsic for applying a 5x5 convolve to an allocation. | | [ScriptIntrinsicHistogram](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicHistogram) | Intrinsic Histogram filter. | | [ScriptIntrinsicLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicLUT) | Intrinsic for applying a per-channel lookup table. | | [ScriptIntrinsicResize](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize) | Intrinsic for performing a resize of a 2D allocation. | | [ScriptIntrinsicYuvToRGB](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB) | Intrinsic for converting an Android YUV buffer to RGB. | |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

The parent class for all executable scripts. This should not be used by applications.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](https://developer.android.com/reference/kotlin/android/renderscript/Script.Builder) Only intended for use by generated reflected code. |
| open | [FieldBase](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldBase) Only intended for use by generated reflected code. |
| | [FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID) FieldID is an identifier for a Script + exported field pair. |
| | [InvokeID](https://developer.android.com/reference/kotlin/android/renderscript/Script.InvokeID) InvokeID is an identifier for an invoke function. |
| | [KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID) KernelID is an identifier for a Script + root function pair. |
| | [LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions) Class for specifying the specifics about how a kernel will be launched. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindAllocation](https://developer.android.com/reference/kotlin/android/renderscript/Script#bindAllocation(android.renderscript.Allocation,%20kotlin.Int))`(`va:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Only intended for use by generated reflected code. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getVarB](https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarB(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getVarD](https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarD(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVarF](https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarF(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVarI](https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarI(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getVarJ](https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarJ(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getVarV](https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarV(kotlin.Int,%20android.renderscript.FieldPacker))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeZone](https://developer.android.com/reference/kotlin/android/renderscript/Script#setTimeZone(kotlin.String))`(`timeZone:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20android.renderscript.BaseObj))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `o:` ` [BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20android.renderscript.FieldPacker))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20android.renderscript.FieldPacker,%20android.renderscript.Element,%20kotlin.IntArray))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`, `dims:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Boolean))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Double))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Float))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Long))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Only intended for use by generated reflected code. |

| Protected methods ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID)! | [createFieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script#createFieldID(kotlin.Int,%20android.renderscript.Element))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`)` Only to be used by generated reflected classes. |
| open [Script.InvokeID](https://developer.android.com/reference/kotlin/android/renderscript/Script.InvokeID)! | [createInvokeID](https://developer.android.com/reference/kotlin/android/renderscript/Script#createInvokeID(kotlin.Int))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Only to be used by generated reflected classes. |
| open [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)! | [createKernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script#createKernelID(kotlin.Int,%20kotlin.Int,%20android.renderscript.Element,%20android.renderscript.Element))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sig:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ein:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`, `eout:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`)` Only to be used by generated reflected classes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/Script#forEach(kotlin.Int,%20android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.FieldPacker))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `v:` ` [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/Script#forEach(kotlin.Int,%20android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.FieldPacker,%20android.renderscript.Script.LaunchOptions))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ain:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `v:` ` [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker)!`, `sc:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/Script#forEach(kotlin.Int,%20kotlin.Array,%20android.renderscript.Allocation,%20android.renderscript.FieldPacker))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!>!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `v:` ` [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/android/renderscript/Script#forEach(kotlin.Int,%20kotlin.Array,%20android.renderscript.Allocation,%20android.renderscript.FieldPacker,%20android.renderscript.Script.LaunchOptions))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!>!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `v:` ` [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker)!`, `sc:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invoke](https://developer.android.com/reference/kotlin/android/renderscript/Script#invoke(kotlin.Int))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invoke](https://developer.android.com/reference/kotlin/android/renderscript/Script#invoke(kotlin.Int,%20android.renderscript.FieldPacker))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [FieldPacker](https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reduce](https://developer.android.com/reference/kotlin/android/renderscript/Script#reduce(kotlin.Int,%20kotlin.Array,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!>!`, `aout:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`, `sc:` ` [Script.LaunchOptions](https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions)!`)` Only intended for use by generated reflected code. |

| Inherited functions ||
|---|---|
| From class [BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#destroy())`()` <br /> Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#finalize())`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#getName())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#hashCode())`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#setName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

## Public methods

### bindAllocation

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindAllocation(
    va: Allocation!, 
    slot: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### getVarB

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVarB(index: Int): Boolean
```

**Deprecated:** *Deprecated in Java.* 

### getVarD

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVarD(index: Int): Double
```

**Deprecated:** *Deprecated in Java.* 

### getVarF

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVarF(index: Int): Float
```

**Deprecated:** *Deprecated in Java.* 

### getVarI

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVarI(index: Int): Int
```

**Deprecated:** *Deprecated in Java.* 

### getVarJ

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVarJ(index: Int): Long
```

**Deprecated:** *Deprecated in Java.* 

### getVarV

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVarV(
    index: Int, 
    v: FieldPacker!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### setTimeZone

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTimeZone(timeZone: String!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setVar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVar(
    index: Int, 
    o: BaseObj!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### setVar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVar(
    index: Int, 
    v: FieldPacker!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### setVar

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVar(
    index: Int, 
    v: FieldPacker!, 
    e: Element!, 
    dims: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### setVar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVar(
    index: Int, 
    v: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### setVar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVar(
    index: Int, 
    v: Double
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### setVar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVar(
    index: Int, 
    v: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### setVar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVar(
    index: Int, 
    v: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### setVar

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVar(
    index: Int, 
    v: Long
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code.

## Protected methods

### createFieldID

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun createFieldID(
    slot: Int, 
    e: Element!
): Script.FieldID!
```

**Deprecated:** *Deprecated in Java.*

Only to be used by generated reflected classes. 

### createInvokeID

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun createInvokeID(slot: Int): Script.InvokeID!
```

**Deprecated:** *Deprecated in Java.*

Only to be used by generated reflected classes. 

### createKernelID

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun createKernelID(
    slot: Int, 
    sig: Int, 
    ein: Element!, 
    eout: Element!
): Script.KernelID!
```

**Deprecated:** *Deprecated in Java.*

Only to be used by generated reflected classes. 

### forEach

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun forEach(
    slot: Int, 
    ain: Allocation!, 
    aout: Allocation!, 
    v: FieldPacker!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### forEach

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun forEach(
    slot: Int, 
    ain: Allocation!, 
    aout: Allocation!, 
    v: FieldPacker!, 
    sc: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### forEach

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun forEach(
    slot: Int, 
    ains: Array<Allocation!>!, 
    aout: Allocation!, 
    v: FieldPacker!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### forEach

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun forEach(
    slot: Int, 
    ains: Array<Allocation!>!, 
    aout: Allocation!, 
    v: FieldPacker!, 
    sc: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### invoke

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun invoke(slot: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### invoke

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun invoke(
    slot: Int, 
    v: FieldPacker!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. 

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun reduce(
    slot: Int, 
    ains: Array<Allocation!>!, 
    aout: Allocation!, 
    sc: Script.LaunchOptions!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Only intended for use by generated reflected code. (General reduction)
