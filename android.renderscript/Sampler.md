# Sampler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Sampler

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/Sampler "View this page in Java") 
| --- | --- |

```
open class Sampler : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||
| | ↳ | [android.renderscript.Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Sampler object that defines how Allocations can be read as textures within a kernel. Samplers are used in conjunction with the`rsSample`runtime function to return values from normalized coordinates. Any Allocation used with a Sampler must have been created with [android.renderscript.Allocation#USAGE_GRAPHICS_TEXTURE](https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_TEXTURE:kotlin.Int); using a Sampler on an [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) that was not created with [android.renderscript.Allocation#USAGE_GRAPHICS_TEXTURE](https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_TEXTURE:kotlin.Int) is undefined.

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Builder) Builder for creating non-standard samplers. |
| | [Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value) <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [CLAMP_LINEAR](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#CLAMP_LINEAR(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with min and mag set to linear and wrap modes set to clamp. |
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [CLAMP_LINEAR_MIP_LINEAR](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#CLAMP_LINEAR_MIP_LINEAR(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with mag set to linear, min linear mipmap linear, and wrap modes set to clamp. |
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [CLAMP_NEAREST](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#CLAMP_NEAREST(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with min and mag set to nearest and wrap modes set to clamp. |
| --- | --- |
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [MIRRORED_REPEAT_LINEAR](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#MIRRORED_REPEAT_LINEAR(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with min and mag set to linear and wrap modes set to mirrored repeat. |
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [MIRRORED_REPEAT_LINEAR_MIP_LINEAR](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#MIRRORED_REPEAT_LINEAR_MIP_LINEAR(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with min and mag set to linear and wrap modes set to mirrored repeat. |
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [MIRRORED_REPEAT_NEAREST](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#MIRRORED_REPEAT_NEAREST(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with min and mag set to nearest and wrap modes set to mirrored repeat. |
| --- | --- |
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [WRAP_LINEAR](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#WRAP_LINEAR(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with min and mag set to linear and wrap modes set to wrap. |
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [WRAP_LINEAR_MIP_LINEAR](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#WRAP_LINEAR_MIP_LINEAR(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with mag set to linear, min linear mipmap linear, and wrap modes set to wrap. |
| openstatic [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | [WRAP_NEAREST](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#WRAP_NEAREST(android.renderscript.RenderScript))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`)` Retrieve a sampler with min and mag set to nearest and wrap modes set to wrap. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAnisotropy](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#getAnisotropy())`()` <br /> |
| open [Sampler.Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value)! | [getMagnification](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#getMagnification())`()` <br /> |
| open [Sampler.Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value)! | [getMinification](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#getMinification())`()` <br /> |
| --- | --- |
| open [Sampler.Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value)! | [getWrapS](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#getWrapS())`()` <br /> |
| open [Sampler.Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value)! | [getWrapT](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#getWrapT())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#destroy())`()` <br /> Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#finalize())`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#getName())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#hashCode())`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#setName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

## Public methods

### CLAMP_LINEAR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun CLAMP_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to linear and wrap modes set to clamp.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### CLAMP_LINEAR_MIP_LINEAR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun CLAMP_LINEAR_MIP_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with mag set to linear, min linear mipmap linear, and wrap modes set to clamp.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### CLAMP_NEAREST

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun CLAMP_NEAREST(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to nearest and wrap modes set to clamp.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### MIRRORED_REPEAT_LINEAR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun MIRRORED_REPEAT_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to linear and wrap modes set to mirrored repeat.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### MIRRORED_REPEAT_LINEAR_MIP_LINEAR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun MIRRORED_REPEAT_LINEAR_MIP_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to linear and wrap modes set to mirrored repeat.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### MIRRORED_REPEAT_NEAREST

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun MIRRORED_REPEAT_NEAREST(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to nearest and wrap modes set to mirrored repeat.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### WRAP_LINEAR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun WRAP_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to linear and wrap modes set to wrap.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### WRAP_LINEAR_MIP_LINEAR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun WRAP_LINEAR_MIP_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with mag set to linear, min linear mipmap linear, and wrap modes set to wrap.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### WRAP_NEAREST

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun WRAP_NEAREST(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to nearest and wrap modes set to wrap.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](https://developer.android.com/reference/kotlin/android/renderscript/Sampler#)! | Sampler |

### getAnisotropy

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnisotropy(): Float
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|--------------------------------------------------------------------------------|------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | anisotropy setting for the sampler |

### getMagnification

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMagnification(): Sampler.Value!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------|
| [Sampler.Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value)! | magnification setting for the sampler |

### getMinification

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinification(): Sampler.Value!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------|--------------------------------------|
| [Sampler.Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value)! | minification setting for the sampler |

### getWrapS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWrapS(): Sampler.Value!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------|
| [Sampler.Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value)! | S wrapping mode for the sampler |

### getWrapT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWrapT(): Sampler.Value!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------|
| [Sampler.Value](https://developer.android.com/reference/kotlin/android/renderscript/Sampler.Value)! | T wrapping mode for the sampler |
