# Script

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Script

Kotlin| [Java](../android/renderscript/Script.md) 
| --- | --- |

```
open class Script : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](../android/renderscript/BaseObj.md) ||
| | ↳ | [android.renderscript.Script](../android/renderscript/Script.md) |

| Known Direct Subclasses [ScriptC](../android/renderscript/ScriptC.md), [ScriptIntrinsic](../android/renderscript/ScriptIntrinsic.md) |--------------------------------------------------------------------------------------------------------|----------------------------------------------| | [ScriptC](../android/renderscript/ScriptC.md) | The superclass for all user-defined scripts. | | [ScriptIntrinsic](../android/renderscript/ScriptIntrinsic.md) | Base class for all Intrinsic scripts. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ScriptIntrinsic3DLUT](../android/renderscript/ScriptIntrinsic3DLUT.md), [ScriptIntrinsicBLAS](../android/renderscript/ScriptIntrinsicBLAS.md), [ScriptIntrinsicBlend](../android/renderscript/ScriptIntrinsicBlend.md), [ScriptIntrinsicBlur](../android/renderscript/ScriptIntrinsicBlur.md), [ScriptIntrinsicColorMatrix](../android/renderscript/ScriptIntrinsicColorMatrix.md), [ScriptIntrinsicConvolve3x3](../android/renderscript/ScriptIntrinsicConvolve3x3.md), [ScriptIntrinsicConvolve5x5](../android/renderscript/ScriptIntrinsicConvolve5x5.md), [ScriptIntrinsicHistogram](../android/renderscript/ScriptIntrinsicHistogram.md), [ScriptIntrinsicLUT](../android/renderscript/ScriptIntrinsicLUT.md), [ScriptIntrinsicResize](../android/renderscript/ScriptIntrinsicResize.md), [ScriptIntrinsicYuvToRGB](../android/renderscript/ScriptIntrinsicYuvToRGB.md) |------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ScriptIntrinsic3DLUT](../android/renderscript/ScriptIntrinsic3DLUT.md) | Intrinsic for converting RGB to RGBA by using a 3D lookup table. | | [ScriptIntrinsicBLAS](../android/renderscript/ScriptIntrinsicBLAS.md) | ScriptIntrinsicBLAS class provides high performance RenderScript APIs to BLAS. | | [ScriptIntrinsicBlend](../android/renderscript/ScriptIntrinsicBlend.md) | Intrinsic kernels for blending two [android.renderscript.Allocation](../android/renderscript/Allocation.md) objects. | | [ScriptIntrinsicBlur](../android/renderscript/ScriptIntrinsicBlur.md) | Intrinsic Gausian blur filter. | | [ScriptIntrinsicColorMatrix](../android/renderscript/ScriptIntrinsicColorMatrix.md) | Intrinsic for applying a color matrix to allocations. | | [ScriptIntrinsicConvolve3x3](../android/renderscript/ScriptIntrinsicConvolve3x3.md) | Intrinsic for applying a 3x3 convolve to an allocation. | | [ScriptIntrinsicConvolve5x5](../android/renderscript/ScriptIntrinsicConvolve5x5.md) | Intrinsic for applying a 5x5 convolve to an allocation. | | [ScriptIntrinsicHistogram](../android/renderscript/ScriptIntrinsicHistogram.md) | Intrinsic Histogram filter. | | [ScriptIntrinsicLUT](../android/renderscript/ScriptIntrinsicLUT.md) | Intrinsic for applying a per-channel lookup table. | | [ScriptIntrinsicResize](../android/renderscript/ScriptIntrinsicResize.md) | Intrinsic for performing a resize of a 2D allocation. | | [ScriptIntrinsicYuvToRGB](../android/renderscript/ScriptIntrinsicYuvToRGB.md) | Intrinsic for converting an Android YUV buffer to RGB. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

The parent class for all executable scripts. This should not be used by applications.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/renderscript/Script.Builder.md) Only intended for use by generated reflected code. |
| open | [FieldBase](../android/renderscript/Script.FieldBase.md) Only intended for use by generated reflected code. |
| | [FieldID](../android/renderscript/Script.FieldID.md) FieldID is an identifier for a Script + exported field pair. |
| --- | --- |
| | [InvokeID](../android/renderscript/Script.InvokeID.md) InvokeID is an identifier for an invoke function. |
| | [KernelID](../android/renderscript/Script.KernelID.md) KernelID is an identifier for a Script + root function pair. |
| | [LaunchOptions](../android/renderscript/Script.LaunchOptions.md) Class for specifying the specifics about how a kernel will be launched. |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindAllocation](../android/renderscript/Script.md))`(`va:` ` [Allocation](../android/renderscript/Allocation.md)!`, `slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Only intended for use by generated reflected code. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getVarB](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getVarD](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVarF](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVarI](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getVarJ](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getVarV](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [FieldPacker](../android/renderscript/FieldPacker.md)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeZone](../android/renderscript/Script.md))`(`timeZone:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `o:` ` [BaseObj](../android/renderscript/BaseObj.md)!`)` Only intended for use by generated reflected code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [FieldPacker](../android/renderscript/FieldPacker.md)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [FieldPacker](../android/renderscript/FieldPacker.md)!`, `e:` ` [Element](../android/renderscript/Element.md)!`, `dims:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Only intended for use by generated reflected code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Only intended for use by generated reflected code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVar](../android/renderscript/Script.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Only intended for use by generated reflected code. |

| Protected methods ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Script.FieldID](../android/renderscript/Script.FieldID.md)! | [createFieldID](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `e:` ` [Element](../android/renderscript/Element.md)!`)` Only to be used by generated reflected classes. |
| open [Script.InvokeID](../android/renderscript/Script.InvokeID.md)! | [createInvokeID](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Only to be used by generated reflected classes. |
| open [Script.KernelID](../android/renderscript/Script.KernelID.md)! | [createKernelID](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sig:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ein:` ` [Element](../android/renderscript/Element.md)!`, `eout:` ` [Element](../android/renderscript/Element.md)!`)` Only to be used by generated reflected classes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `v:` ` [FieldPacker](../android/renderscript/FieldPacker.md)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ain:` ` [Allocation](../android/renderscript/Allocation.md)!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `v:` ` [FieldPacker](../android/renderscript/FieldPacker.md)!`, `sc:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Allocation](../android/renderscript/Allocation.md)!>!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `v:` ` [FieldPacker](../android/renderscript/FieldPacker.md)!`)` Only intended for use by generated reflected code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Allocation](../android/renderscript/Allocation.md)!>!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `v:` ` [FieldPacker](../android/renderscript/FieldPacker.md)!`, `sc:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invoke](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Only intended for use by generated reflected code. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invoke](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [FieldPacker](../android/renderscript/FieldPacker.md)!`)` Only intended for use by generated reflected code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reduce](../android/renderscript/Script.md))`(`slot:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Allocation](../android/renderscript/Allocation.md)!>!`, `aout:` ` [Allocation](../android/renderscript/Allocation.md)!`, `sc:` ` [Script.LaunchOptions](../android/renderscript/Script.LaunchOptions.md)!`)` Only intended for use by generated reflected code. |

| Inherited functions ||
|---|---|
| From class [BaseObj](../android/renderscript/BaseObj.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](../android/renderscript/BaseObj.md))`()` <br /> Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/renderscript/BaseObj.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/renderscript/BaseObj.md))`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/renderscript/BaseObj.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/renderscript/BaseObj.md))`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](../android/renderscript/BaseObj.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

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
