# BaseObj

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseObj

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/BaseObj "View this page in Java") 

```
open class BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#) |

| Known Direct Subclasses [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation), [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element), [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler), [Script](https://developer.android.com/reference/kotlin/android/renderscript/Script), [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID), [Script.InvokeID](https://developer.android.com/reference/kotlin/android/renderscript/Script.InvokeID), [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID), [ScriptGroup](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup), [ScriptGroup.Closure](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Closure), [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type) |----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) | This class provides the primary method through which data is passed to and from RenderScript kernels. | | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element) | An Element represents one item within an . | | [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler) | Sampler object that defines how Allocations can be read as textures within a kernel. | | [Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) | The parent class for all executable scripts. | | [Script.FieldID](https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID) | FieldID is an identifier for a Script + exported field pair. | | [Script.InvokeID](https://developer.android.com/reference/kotlin/android/renderscript/Script.InvokeID) | InvokeID is an identifier for an invoke function. | | [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID) | KernelID is an identifier for a Script + root function pair. | | [ScriptGroup](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup) | A group of kernels that are executed together with one execution call as if they were a single kernel | | [ScriptGroup.Closure](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Closure) | An opaque class for closures | | [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type) | A Type describes the [android.renderscript.Element](https://developer.android.com/reference/kotlin/android/renderscript/Element) and dimensions used for an or a parallel operation. | |

| Known Indirect Subclasses [AllocationAdapter](https://developer.android.com/reference/kotlin/android/renderscript/AllocationAdapter), [ScriptC](https://developer.android.com/reference/kotlin/android/renderscript/ScriptC), [ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic), [ScriptIntrinsic3DLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT), [ScriptIntrinsicBLAS](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS), [ScriptIntrinsicBlend](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend), [ScriptIntrinsicBlur](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur), [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix), [ScriptIntrinsicConvolve3x3](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve3x3), [ScriptIntrinsicConvolve5x5](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5), [ScriptIntrinsicHistogram](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicHistogram), [ScriptIntrinsicLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicLUT), and 2 others. |------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AllocationAdapter](https://developer.android.com/reference/kotlin/android/renderscript/AllocationAdapter) | Only intended for use by generated reflected code. | | [ScriptC](https://developer.android.com/reference/kotlin/android/renderscript/ScriptC) | The superclass for all user-defined scripts. | | [ScriptIntrinsic](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic) | Base class for all Intrinsic scripts. | | [ScriptIntrinsic3DLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsic3DLUT) | Intrinsic for converting RGB to RGBA by using a 3D lookup table. | | [ScriptIntrinsicBLAS](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBLAS) | ScriptIntrinsicBLAS class provides high performance RenderScript APIs to BLAS. | | [ScriptIntrinsicBlend](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlend) | Intrinsic kernels for blending two [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) objects. | | [ScriptIntrinsicBlur](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicBlur) | Intrinsic Gausian blur filter. | | [ScriptIntrinsicColorMatrix](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicColorMatrix) | Intrinsic for applying a color matrix to allocations. | | [ScriptIntrinsicConvolve3x3](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve3x3) | Intrinsic for applying a 3x3 convolve to an allocation. | | [ScriptIntrinsicConvolve5x5](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicConvolve5x5) | Intrinsic for applying a 5x5 convolve to an allocation. | | [ScriptIntrinsicHistogram](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicHistogram) | Intrinsic Histogram filter. | | [ScriptIntrinsicLUT](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicLUT) | Intrinsic for applying a per-channel lookup table. | | [ScriptIntrinsicResize](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicResize) | Intrinsic for performing a resize of a 2D allocation. | | [ScriptIntrinsicYuvToRGB](https://developer.android.com/reference/kotlin/android/renderscript/ScriptIntrinsicYuvToRGB) | Intrinsic for converting an Android YUV buffer to RGB. | |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

BaseObj is the base class for all RenderScript objects owned by a RS context. It is responsible for lifetime management and resource tracking. This class should not be used by a user application.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#destroy())`()` Frees any native resources associated with this object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compare the current BaseObj with another BaseObj for equality. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#getName())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#hashCode())`()` Calculates the hash code value for a BaseObj. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#setName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` setName assigns a name to an object. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#finalize())`()` <br /> |

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
