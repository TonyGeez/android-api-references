# Sampler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Sampler

Kotlin| [Java](Sampler.md) 
| --- | --- |

```
open class Sampler : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||
| | ↳ | [android.renderscript.Sampler](Sampler.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Sampler object that defines how Allocations can be read as textures within a kernel. Samplers are used in conjunction with the`rsSample`runtime function to return values from normalized coordinates. Any Allocation used with a Sampler must have been created with [android.renderscript.Allocation#USAGE_GRAPHICS_TEXTURE](Allocation.md); using a Sampler on an [android.renderscript.Allocation](Allocation.md) that was not created with [android.renderscript.Allocation#USAGE_GRAPHICS_TEXTURE](Allocation.md) is undefined.

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/renderscript/Sampler.Builder.md) Builder for creating non-standard samplers. |
| | [Value](../android/renderscript/Sampler.Value.md) <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Sampler](Sampler.md)! | [CLAMP_LINEAR](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with min and mag set to linear and wrap modes set to clamp. |
| openstatic [Sampler](Sampler.md)! | [CLAMP_LINEAR_MIP_LINEAR](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with mag set to linear, min linear mipmap linear, and wrap modes set to clamp. |
| openstatic [Sampler](Sampler.md)! | [CLAMP_NEAREST](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with min and mag set to nearest and wrap modes set to clamp. |
| --- | --- |
| openstatic [Sampler](Sampler.md)! | [MIRRORED_REPEAT_LINEAR](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with min and mag set to linear and wrap modes set to mirrored repeat. |
| openstatic [Sampler](Sampler.md)! | [MIRRORED_REPEAT_LINEAR_MIP_LINEAR](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with min and mag set to linear and wrap modes set to mirrored repeat. |
| openstatic [Sampler](Sampler.md)! | [MIRRORED_REPEAT_NEAREST](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with min and mag set to nearest and wrap modes set to mirrored repeat. |
| --- | --- |
| openstatic [Sampler](Sampler.md)! | [WRAP_LINEAR](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with min and mag set to linear and wrap modes set to wrap. |
| openstatic [Sampler](Sampler.md)! | [WRAP_LINEAR_MIP_LINEAR](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with mag set to linear, min linear mipmap linear, and wrap modes set to wrap. |
| openstatic [Sampler](Sampler.md)! | [WRAP_NEAREST](Sampler.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Retrieve a sampler with min and mag set to nearest and wrap modes set to wrap. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAnisotropy](Sampler.md))`()` <br /> |
| open [Sampler.Value](../android/renderscript/Sampler.Value.md)! | [getMagnification](Sampler.md))`()` <br /> |
| open [Sampler.Value](../android/renderscript/Sampler.Value.md)! | [getMinification](Sampler.md))`()` <br /> |
| --- | --- |
| open [Sampler.Value](../android/renderscript/Sampler.Value.md)! | [getWrapS](Sampler.md))`()` <br /> |
| open [Sampler.Value](../android/renderscript/Sampler.Value.md)! | [getWrapT](Sampler.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [BaseObj](BaseObj.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](BaseObj.md))`()` <br /> Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](BaseObj.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](BaseObj.md))`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](BaseObj.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](BaseObj.md))`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](BaseObj.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

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
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

### CLAMP_LINEAR_MIP_LINEAR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun CLAMP_LINEAR_MIP_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with mag set to linear, min linear mipmap linear, and wrap modes set to clamp.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

### CLAMP_NEAREST

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun CLAMP_NEAREST(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to nearest and wrap modes set to clamp.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

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
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

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
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

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
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

### WRAP_LINEAR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun WRAP_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to linear and wrap modes set to wrap.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

### WRAP_LINEAR_MIP_LINEAR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun WRAP_LINEAR_MIP_LINEAR(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with mag set to linear, min linear mipmap linear, and wrap modes set to wrap.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

### WRAP_NEAREST

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun WRAP_NEAREST(rs: RenderScript!): Sampler!
```

**Deprecated:** *Deprecated in Java.*

Retrieve a sampler with min and mag set to nearest and wrap modes set to wrap.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:Context to which the sampler will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Sampler](Sampler.md)! | Sampler |

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
| [Sampler.Value](../android/renderscript/Sampler.Value.md)! | magnification setting for the sampler |

### getMinification

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinification(): Sampler.Value!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------|--------------------------------------|
| [Sampler.Value](../android/renderscript/Sampler.Value.md)! | minification setting for the sampler |

### getWrapS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWrapS(): Sampler.Value!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------|
| [Sampler.Value](../android/renderscript/Sampler.Value.md)! | S wrapping mode for the sampler |

### getWrapT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWrapT(): Sampler.Value!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------|
| [Sampler.Value](../android/renderscript/Sampler.Value.md)! | T wrapping mode for the sampler |
