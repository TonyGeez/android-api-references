# Type

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Type

Kotlin| [Java](../android/renderscript/Type.md) 
| --- | --- |

```
open class Type : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](../android/renderscript/BaseObj.md) ||
| | ↳ | [android.renderscript.Type](../android/renderscript/Type.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

A Type describes the [android.renderscript.Element](../android/renderscript/Element.md) and dimensions used for an or a parallel operation. Types are created through .

A Type always includes an [android.renderscript.Element](../android/renderscript/Element.md) and an X dimension. A Type may be multidimensional, up to three dimensions. A nonzero value in the Y or Z dimensions indicates that the dimension is present. Note that a Type with only a given X dimension and a Type with the same X dimension but Y = 1 are not equivalent.

A Type also supports inclusion of level of detail (LOD) or cube map faces. LOD and cube map faces are booleans to indicate present or not present.

A Type also supports YUV format information to support an [android.renderscript.Allocation](../android/renderscript/Allocation.md) in a YUV format. The YUV formats supported are [android.graphics.ImageFormat#YV12](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#NV21](../android/graphics/ImageFormat.md), and [android.graphics.ImageFormat#YUV_420_888](../android/graphics/ImageFormat.md)
|
| ### Developer Guides
|
| For more information about creating an application that uses RenderScript, read the [RenderScript](https://developer.android.com/guide/topics/renderscript/index.html) developer guide.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/renderscript/Type.Builder.md) Builder class for Type. |
| | [CubemapFace](../android/renderscript/Type.CubemapFace.md) <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Type](../android/renderscript/Type.md)! | [createX](../android/renderscript/Type.md))`(`rs:` ` [RenderScript](../android/renderscript/RenderScript.md)!`, `e:` ` [Element](../android/renderscript/Element.md)!`, `dimX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Utility function for creating basic 1D types. |
| openstatic [Type](../android/renderscript/Type.md)! | [createXY](../android/renderscript/Type.md))`(`rs:` ` [RenderScript](../android/renderscript/RenderScript.md)!`, `e:` ` [Element](../android/renderscript/Element.md)!`, `dimX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dimY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Utility function for creating basic 2D types. |
| openstatic [Type](../android/renderscript/Type.md)! | [createXYZ](../android/renderscript/Type.md))`(`rs:` ` [RenderScript](../android/renderscript/RenderScript.md)!`, `e:` ` [Element](../android/renderscript/Element.md)!`, `dimX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dimY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dimZ:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Utility function for creating basic 3D types. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](../android/renderscript/Type.md))`()` Return the total number of accessable cells in the Type. |
| open [Element](../android/renderscript/Element.md)! | [getElement](../android/renderscript/Type.md))`()` Return the element associated with this Type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getX](../android/renderscript/Type.md))`()` Return the value of the X dimension. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getY](../android/renderscript/Type.md))`()` Return the value of the Y dimension or 0 for a 1D allocation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYuv](../android/renderscript/Type.md))`()` Get the YUV format |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getZ](../android/renderscript/Type.md))`()` Return the value of the Z dimension or 0 for a 1D or 2D allocation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFaces](../android/renderscript/Type.md))`()` Return if the Type is a cube map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMipmaps](../android/renderscript/Type.md))`()` Return if the Type has a mipmap chain. |

| Inherited functions ||
|---|---|
| From class [BaseObj](../android/renderscript/BaseObj.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](../android/renderscript/BaseObj.md))`()` <br /> Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/renderscript/BaseObj.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/renderscript/BaseObj.md))`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/renderscript/BaseObj.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/renderscript/BaseObj.md))`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](../android/renderscript/BaseObj.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

## Public methods

### createX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createX(
    rs: RenderScript!, 
    e: Element!, 
    dimX: Int
): Type!
```

**Deprecated:** *Deprecated in Java.*

Utility function for creating basic 1D types. The type is created without mipmaps enabled.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](../android/renderscript/RenderScript.md)!:The RenderScript context |
| `e` | [Element](../android/renderscript/Element.md)!:The Element for the Type |
| `dimX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The X dimension, must be \> 0 |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------|
| [Type](../android/renderscript/Type.md)! | Type |

### createXY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createXY(
    rs: RenderScript!, 
    e: Element!, 
    dimX: Int, 
    dimY: Int
): Type!
```

**Deprecated:** *Deprecated in Java.*

Utility function for creating basic 2D types. The type is created without mipmaps or cubemaps.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](../android/renderscript/RenderScript.md)!:The RenderScript context |
| `e` | [Element](../android/renderscript/Element.md)!:The Element for the Type |
| `dimX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The X dimension, must be \> 0 |
| --- | --- |
| `dimY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The Y dimension, must be \> 0 |

| Return ||
|------------------------------------------------------------------------------------|------|
| [Type](../android/renderscript/Type.md)! | Type |

### createXYZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createXYZ(
    rs: RenderScript!, 
    e: Element!, 
    dimX: Int, 
    dimY: Int, 
    dimZ: Int
): Type!
```

**Deprecated:** *Deprecated in Java.*

Utility function for creating basic 3D types. The type is created without mipmaps.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](../android/renderscript/RenderScript.md)!:The RenderScript context |
| `e` | [Element](../android/renderscript/Element.md)!:The Element for the Type |
| `dimX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The X dimension, must be \> 0 |
| --- | --- |
| `dimY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The Y dimension, must be \> 0 |
| `dimZ` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The Z dimension, must be \> 0 |

| Return ||
|------------------------------------------------------------------------------------|------|
| [Type](../android/renderscript/Type.md)! | Type |

### getCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCount(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the total number of accessable cells in the Type.

| Return ||
|----------------------------------------------------------------------------|-----|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int |

### getElement

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getElement(): Element!
```

**Deprecated:** *Deprecated in Java.*

Return the element associated with this Type.

| Return ||
|-----------------------------------------------------------------------------------------|---------|
| [Element](../android/renderscript/Element.md)! | Element |

### getX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getX(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the value of the X dimension.

| Return ||
|----------------------------------------------------------------------------|-----|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int |

### getY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getY(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the value of the Y dimension or 0 for a 1D allocation.

| Return ||
|----------------------------------------------------------------------------|-----|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int |

### getYuv

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYuv(): Int
```

**Deprecated:** *Deprecated in Java.*

Get the YUV format

| Return ||
|----------------------------------------------------------------------------|-----|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int |

### getZ

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getZ(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the value of the Z dimension or 0 for a 1D or 2D allocation.

| Return ||
|----------------------------------------------------------------------------|-----|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int |

### hasFaces

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasFaces(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return if the Type is a cube map.

| Return ||
|------------------------------------------------------------------------------------|---------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean |

### hasMipmaps

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMipmaps(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return if the Type has a mipmap chain.

| Return ||
|------------------------------------------------------------------------------------|---------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean |
