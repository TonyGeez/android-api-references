# BaseObj

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseObj

Kotlin| [Java](../android/renderscript/BaseObj.md) 
| --- | --- |

```
open class BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.renderscript.BaseObj](../android/renderscript/BaseObj.md) |

| Known Direct Subclasses [Allocation](../android/renderscript/Allocation.md), [Element](../android/renderscript/Element.md), [Sampler](../android/renderscript/Sampler.md), [Script](../android/renderscript/Script.md), [Script.FieldID](../android/renderscript/Script.FieldID.md), [Script.InvokeID](../android/renderscript/Script.InvokeID.md), [Script.KernelID](../android/renderscript/Script.KernelID.md), [ScriptGroup](../android/renderscript/ScriptGroup.md), [ScriptGroup.Closure](../android/renderscript/ScriptGroup.Closure.md), [Type](../android/renderscript/Type.md) |----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Allocation](../android/renderscript/Allocation.md) | This class provides the primary method through which data is passed to and from RenderScript kernels. | | [Element](../android/renderscript/Element.md) | An Element represents one item within an . | | [Sampler](../android/renderscript/Sampler.md) | Sampler object that defines how Allocations can be read as textures within a kernel. | | [Script](../android/renderscript/Script.md) | The parent class for all executable scripts. | | [Script.FieldID](../android/renderscript/Script.FieldID.md) | FieldID is an identifier for a Script + exported field pair. | | [Script.InvokeID](../android/renderscript/Script.InvokeID.md) | InvokeID is an identifier for an invoke function. | | [Script.KernelID](../android/renderscript/Script.KernelID.md) | KernelID is an identifier for a Script + root function pair. | | [ScriptGroup](../android/renderscript/ScriptGroup.md) | A group of kernels that are executed together with one execution call as if they were a single kernel | | [ScriptGroup.Closure](../android/renderscript/ScriptGroup.Closure.md) | An opaque class for closures | | [Type](../android/renderscript/Type.md) | A Type describes the [android.renderscript.Element](../android/renderscript/Element.md) and dimensions used for an or a parallel operation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AllocationAdapter](../android/renderscript/AllocationAdapter.md), [ScriptC](../android/renderscript/ScriptC.md), [ScriptIntrinsic](../android/renderscript/ScriptIntrinsic.md), [ScriptIntrinsic3DLUT](../android/renderscript/ScriptIntrinsic3DLUT.md), [ScriptIntrinsicBLAS](../android/renderscript/ScriptIntrinsicBLAS.md), [ScriptIntrinsicBlend](../android/renderscript/ScriptIntrinsicBlend.md), [ScriptIntrinsicBlur](../android/renderscript/ScriptIntrinsicBlur.md), [ScriptIntrinsicColorMatrix](../android/renderscript/ScriptIntrinsicColorMatrix.md), [ScriptIntrinsicConvolve3x3](../android/renderscript/ScriptIntrinsicConvolve3x3.md), [ScriptIntrinsicConvolve5x5](../android/renderscript/ScriptIntrinsicConvolve5x5.md), [ScriptIntrinsicHistogram](../android/renderscript/ScriptIntrinsicHistogram.md), [ScriptIntrinsicLUT](../android/renderscript/ScriptIntrinsicLUT.md), and 2 others. |------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AllocationAdapter](../android/renderscript/AllocationAdapter.md) | Only intended for use by generated reflected code. | | [ScriptC](../android/renderscript/ScriptC.md) | The superclass for all user-defined scripts. | | [ScriptIntrinsic](../android/renderscript/ScriptIntrinsic.md) | Base class for all Intrinsic scripts. | | [ScriptIntrinsic3DLUT](../android/renderscript/ScriptIntrinsic3DLUT.md) | Intrinsic for converting RGB to RGBA by using a 3D lookup table. | | [ScriptIntrinsicBLAS](../android/renderscript/ScriptIntrinsicBLAS.md) | ScriptIntrinsicBLAS class provides high performance RenderScript APIs to BLAS. | | [ScriptIntrinsicBlend](../android/renderscript/ScriptIntrinsicBlend.md) | Intrinsic kernels for blending two [android.renderscript.Allocation](../android/renderscript/Allocation.md) objects. | | [ScriptIntrinsicBlur](../android/renderscript/ScriptIntrinsicBlur.md) | Intrinsic Gausian blur filter. | | [ScriptIntrinsicColorMatrix](../android/renderscript/ScriptIntrinsicColorMatrix.md) | Intrinsic for applying a color matrix to allocations. | | [ScriptIntrinsicConvolve3x3](../android/renderscript/ScriptIntrinsicConvolve3x3.md) | Intrinsic for applying a 3x3 convolve to an allocation. | | [ScriptIntrinsicConvolve5x5](../android/renderscript/ScriptIntrinsicConvolve5x5.md) | Intrinsic for applying a 5x5 convolve to an allocation. | | [ScriptIntrinsicHistogram](../android/renderscript/ScriptIntrinsicHistogram.md) | Intrinsic Histogram filter. | | [ScriptIntrinsicLUT](../android/renderscript/ScriptIntrinsicLUT.md) | Intrinsic for applying a per-channel lookup table. | | [ScriptIntrinsicResize](../android/renderscript/ScriptIntrinsicResize.md) | Intrinsic for performing a resize of a 2D allocation. | | [ScriptIntrinsicYuvToRGB](../android/renderscript/ScriptIntrinsicYuvToRGB.md) | Intrinsic for converting an Android YUV buffer to RGB. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

BaseObj is the base class for all RenderScript objects owned by a RS context. It is responsible for lifetime management and resource tracking. This class should not be used by a user application.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](../android/renderscript/BaseObj.md))`()` Frees any native resources associated with this object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/renderscript/BaseObj.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compare the current BaseObj with another BaseObj for equality. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/renderscript/BaseObj.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/renderscript/BaseObj.md))`()` Calculates the hash code value for a BaseObj. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](../android/renderscript/BaseObj.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` setName assigns a name to an object. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/renderscript/BaseObj.md))`()` <br /> |

## Public methods

### destroy

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun destroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. 

### equals

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Compare the current BaseObj with another BaseObj for equality.

| Parameters ||
|-------|------------------------------------|
| `obj` | The object to check equality with. |

| Return ||
|------------------------------------------------------------------------------------|---------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean |

### getName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | name of the renderscript object |

### hashCode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Calculates the hash code value for a BaseObj.

| Return ||
|----------------------------------------------------------------------------|-----|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int |

### setName

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setName(name: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

setName assigns a name to an object. This object can later be looked up by this name.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name to assign to the object. |

## Protected methods

### finalize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
