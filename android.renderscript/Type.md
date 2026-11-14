# Type

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Type

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/Type "View this page in Java") 
| --- | --- |

```
open class Type : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||
| | ↳ | [android.renderscript.Type](https://developer.android.com/reference/kotlin/android/renderscript/Type#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

A Type describes the [android.renderscript.Element](https://developer.android.com/reference/kotlin/android/renderscript/Element) and dimensions used for an or a parallel operation. Types are created through .

A Type always includes an [android.renderscript.Element](https://developer.android.com/reference/kotlin/android/renderscript/Element) and an X dimension. A Type may be multidimensional, up to three dimensions. A nonzero value in the Y or Z dimensions indicates that the dimension is present. Note that a Type with only a given X dimension and a Type with the same X dimension but Y = 1 are not equivalent.

A Type also supports inclusion of level of detail (LOD) or cube map faces. LOD and cube map faces are booleans to indicate present or not present.

A Type also supports YUV format information to support an [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation) in a YUV format. The YUV formats supported are [android.graphics.ImageFormat#YV12](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int), [android.graphics.ImageFormat#NV21](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int), and [android.graphics.ImageFormat#YUV_420_888](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int)
|
| ### Developer Guides
|
| For more information about creating an application that uses RenderScript, read the [RenderScript](https://developer.android.com/guide/topics/renderscript/index.html) developer guide.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------|
| open | [Builder](https://developer.android.com/reference/kotlin/android/renderscript/Type.Builder) Builder class for Type. |
| | [CubemapFace](https://developer.android.com/reference/kotlin/android/renderscript/Type.CubemapFace) <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type#)! | [createX](https://developer.android.com/reference/kotlin/android/renderscript/Type#createX(android.renderscript.RenderScript,%20android.renderscript.Element,%20kotlin.Int))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`, `dimX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Utility function for creating basic 1D types. |
| openstatic [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type#)! | [createXY](https://developer.android.com/reference/kotlin/android/renderscript/Type#createXY(android.renderscript.RenderScript,%20android.renderscript.Element,%20kotlin.Int,%20kotlin.Int))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`, `dimX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dimY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Utility function for creating basic 2D types. |
| openstatic [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type#)! | [createXYZ](https://developer.android.com/reference/kotlin/android/renderscript/Type#createXYZ(android.renderscript.RenderScript,%20android.renderscript.Element,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`rs:` ` [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!`, `e:` ` [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!`, `dimX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dimY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dimZ:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Utility function for creating basic 3D types. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/renderscript/Type#getCount())`()` Return the total number of accessable cells in the Type. |
| open [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)! | [getElement](https://developer.android.com/reference/kotlin/android/renderscript/Type#getElement())`()` Return the element associated with this Type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getX](https://developer.android.com/reference/kotlin/android/renderscript/Type#getX())`()` Return the value of the X dimension. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getY](https://developer.android.com/reference/kotlin/android/renderscript/Type#getY())`()` Return the value of the Y dimension or 0 for a 1D allocation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYuv](https://developer.android.com/reference/kotlin/android/renderscript/Type#getYuv())`()` Get the YUV format |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getZ](https://developer.android.com/reference/kotlin/android/renderscript/Type#getZ())`()` Return the value of the Z dimension or 0 for a 1D or 2D allocation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFaces](https://developer.android.com/reference/kotlin/android/renderscript/Type#hasFaces())`()` Return if the Type is a cube map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMipmaps](https://developer.android.com/reference/kotlin/android/renderscript/Type#hasMipmaps())`()` Return if the Type has a mipmap chain. |

| Inherited functions ||
|---|---|
| From class [BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#destroy())`()` <br /> Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#finalize())`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#getName())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#hashCode())`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#setName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

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
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:The Element for the Type |
| `dimX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The X dimension, must be \> 0 |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------|
| [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type#)! | Type |

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
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:The Element for the Type |
| `dimX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The X dimension, must be \> 0 |
| --- | --- |
| `dimY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The Y dimension, must be \> 0 |

| Return ||
|------------------------------------------------------------------------------------|------|
| [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type#)! | Type |

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
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!:The RenderScript context |
| `e` | [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)!:The Element for the Type |
| `dimX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The X dimension, must be \> 0 |
| --- | --- |
| `dimY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The Y dimension, must be \> 0 |
| `dimZ` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The Z dimension, must be \> 0 |

| Return ||
|------------------------------------------------------------------------------------|------|
| [Type](https://developer.android.com/reference/kotlin/android/renderscript/Type#)! | Type |

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
| [Element](https://developer.android.com/reference/kotlin/android/renderscript/Element)! | Element |

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
