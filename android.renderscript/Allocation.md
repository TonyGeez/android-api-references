Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Allocation

Kotlin | [Java](Allocation.md)
| --- | --- |

```
open class Allocation : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||
| | ↳ | [android.renderscript.Allocation](Allocation.md) |

| Known Direct Subclasses [AllocationAdapter](AllocationAdapter.md) |---|---| | [AllocationAdapter](AllocationAdapter.md) | Only intended for use by generated reflected code. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

This class provides the primary method through which data is passed to and from RenderScript kernels. An Allocation provides the backing store for a given Type.

An Allocation also contains a set of usage flags that denote how the Allocation could be used. For example, an Allocation may have usage flags specifying that it can be used from a script as well as input to a Sampler. A developer must synchronize across these different usages using syncAll in order to ensure that different users of the Allocation have a consistent view of memory. For example, in the case where an Allocation is used as the output of one kernel and as Sampler input in a later kernel, a developer must call syncAll prior to launching the second kernel to ensure correctness.

An Allocation can be populated with the #copyFrom routines. For more complex Element types, the #copyFromUnchecked methods can be used to copy from byte arrays or similar constructs.
|
| ### Developer Guides
|
| For more information about creating an application that uses RenderScript, read the [RenderScript](https://developer.android.com/guide/topics/renderscript/index.html) developer guide.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation.MipmapControl` Controls mipmap behavior when using the bitmap creation and update functions. |
| abstract | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation.OnBufferAvailableListener` Interface to handle notification when new buffers are available via `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_INPUT:kotlin.Int`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_CONSTANTS:kotlin.Int` The Allocation will be used as the source of shader constants by one or more programs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_RENDER_TARGET:kotlin.Int` The Allocation will be used as a target for offscreen rendering This was deprecated in API level 16. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_TEXTURE:kotlin.Int` The Allocation will be used as a texture source by one or more graphics programs. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_VERTEX:kotlin.Int` The Allocation will be used as a graphics mesh. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_INPUT:kotlin.Int` The Allocation will be used as a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` consumer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_OUTPUT:kotlin.Int` The Allocation will be used as a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` producer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_SCRIPT:kotlin.Int` The Allocation will be bound to and accessed by scripts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_SHARED:kotlin.Int` The Allocation's backing store will be inherited from another object (usually a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`); copying to or from the original source Bitmap will cause a synchronization rather than a full copy. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFrom Copy part of an Allocation into this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFrom Copy an array into a 1D region of this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFrom Copy an array into a 1D region of this Allocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFrom Copy an array into a 1D region of this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFrom Copy an array into a 1D region of this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFrom Copy an array into a 1D region of this Allocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFromUnchecked Copy an array into a 1D region of this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFromUnchecked Copy an array into a 1D region of this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFromUnchecked Copy an array into a 1D region of this Allocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFromUnchecked Copy an array into a 1D region of this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeFromUnchecked Copy an array into a 1D region of this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeTo Copy a 1D region of this Allocation into an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeTo Copy a 1D region of this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeTo Copy a 1D region of this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeTo Copy a 1D region of this Allocation into an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeTo Copy a 1D region of this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeToUnchecked Copy a 1D region of this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeToUnchecked Copy a 1D region of this Allocation into an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeToUnchecked Copy a 1D region of this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeToUnchecked Copy a 1D region of this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy1DRangeToUnchecked Copy a 1D region of this Allocation into an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeFrom Copy a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` into an Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeFrom Copy a rectangular region from an Allocation into a rectangular region in this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeFrom Copy from an array into a rectangular region in this Allocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeFrom Copy from an array into a rectangular region in this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeFrom Copy from an array into a rectangular region in this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeFrom Copy from an array into a rectangular region in this Allocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeFrom Copy from an array into a rectangular region in this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeTo Copy from a rectangular region in this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeTo Copy from a rectangular region in this Allocation into an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeTo Copy from a rectangular region in this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeTo Copy from a rectangular region in this Allocation into an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy2DRangeTo Copy from a rectangular region in this Allocation into an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy3DRangeFrom Copy a rectangular region into the allocation from another allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy3DRangeFrom Copy from an array into a 3D region in this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copy3DRangeTo <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom Copy into an Allocation from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom Copy an Allocation from an Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom Copy an array of RS objects to the Allocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom Copy into this Allocation from an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom Copy into this Allocation from an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom Copy into this Allocation from an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom Copy into this Allocation from an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom Copy into this Allocation from an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFromUnchecked Copy into this Allocation from an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFromUnchecked Copy into this Allocation from an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFromUnchecked Copy into this Allocation from an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFromUnchecked Copy into this Allocation from an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFromUnchecked Copy into this Allocation from an array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyTo Copy from the Allocation into a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyTo Copy from the Allocation into a byte array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyTo Copy from the Allocation into a float array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyTo Copy from the Allocation into a int array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyTo Copy from the Allocation into an array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyTo Copy from the Allocation into a short array. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Allocation](Allocation.md)!\>! | createAllocations Creates a new Allocation Array with the given Type, and usage flags. |
| open static [Allocation](Allocation.md)! | createCubemapFromBitmap Creates a non-mipmapped cubemap Allocation for use as a graphics texture from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` containing the horizontal list of cube faces. |
| --- | --- |
| open static [Allocation](Allocation.md)! | createCubemapFromBitmap Creates a cubemap Allocation from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` containing the horizontal list of cube faces. |
| open static [Allocation](Allocation.md)! | createCubemapFromCubeFaces Creates a non-mipmapped cubemap Allocation for use as a sampler input from 6 `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` objects containing the cube faces. |
| open static [Allocation](Allocation.md)! | createCubemapFromCubeFaces Creates a cubemap Allocation from 6 `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` objects containing the cube faces. |
| --- | --- |
| open static [Allocation](Allocation.md)! | createFromBitmap Creates an Allocation from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`. |
| open static [Allocation](Allocation.md)! | createFromBitmap Creates an Allocation from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`. |
| open static [Allocation](Allocation.md)! | createFromBitmapResource Creates a non-mipmapped Allocation to use as a graphics texture from the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` referenced by resource ID. |
| --- | --- |
| open static [Allocation](Allocation.md)! | createFromBitmapResource Creates an Allocation from the Bitmap referenced by resource ID. |
| open static [Allocation](Allocation.md)! | createFromString Creates an Allocation containing string data encoded in UTF-8 format. |
| open static [Allocation](Allocation.md)! | createSized Creates an Allocation with a specified number of given elements |
| --- | --- |
| open static [Allocation](Allocation.md)! | createSized Creates an Allocation with a specified number of given elements |
| open static [Allocation](Allocation.md)! | createTyped Creates an Allocation for use by scripts with a given Type and no mipmaps |
| open static [Allocation](Allocation.md)! | createTyped Creates a new Allocation with the given Type, mipmap flag, and usage flags. |
| --- | --- |
| open static [Allocation](Allocation.md)! | createTyped Creates an Allocation with the size specified by the type and no mipmaps generated by default |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | destroy For USAGE_IO_OUTPUT, destroy() implies setSurface(null). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | generateMipmaps Generate a mipmap chain. |
| --- | --- |
| open [ByteBuffer](../java.nio/ByteBuffer.md)! | getByteBuffer Gets or creates a ByteBuffer that contains the raw data of the current Allocation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBytesSize Get the size of the Allocation in bytes. |
| open [Element](Element.md)! | getElement Get the Element of the Type of the Allocation. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getStride Gets the stride of the Allocation. |
| open [Surface](../android.view/Surface.md)! | getSurface Returns the handle to a raw buffer that is being managed by the screen compositor. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getTimeStamp Get the timestamp for the most recent buffer held by this Allocation. |
| --- | --- |
| open [Type](Type.md)! | getType Get the Type of the Allocation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getUsage Get the usage flags of the Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ioReceive Receive the latest input into the Allocation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | ioSend Send a buffer to the output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | resize Resize a 1D allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAutoPadding Specifies the mapping between the Allocation's cells and an array's elements when data is copied from the Allocation to the array, or vice-versa. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFromFieldPacker This is only intended to be used by auto-generated code reflected from the RenderScript script files and should not be used by developers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFromFieldPacker This is only intended to be used by auto-generated code reflected from the RenderScript script files and should not be used by developers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFromFieldPacker This is only intended to be used by auto-generated code reflected from the RenderScript script files and should not be used by developers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnBufferAvailableListener Set a notification handler for `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_INPUT:kotlin.Int`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSurface Associate a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` with this Allocation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | syncAll Propagate changes from one usage of the Allocation to the other usages of the Allocation. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

| Inherited functions ||
|---|---|
| From class BaseObj |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | equals Compare the current BaseObj with another BaseObj for equality. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getName <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | hashCode Calculates the hash code value for a BaseObj. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setName setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

## Constants

### USAGE_GRAPHICS_CONSTANTS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_GRAPHICS_CONSTANTS: Int
```

**Deprecated:** *Deprecated in Java.*

The Allocation will be used as the source of shader constants by one or more programs. This was deprecated in API level 16.

 Value: 8

### USAGE_GRAPHICS_RENDER_TARGET

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_GRAPHICS_RENDER_TARGET: Int
```

**Deprecated:** *Deprecated in Java.*

The Allocation will be used as a target for offscreen rendering This was deprecated in API level 16.

 Value: 16

### USAGE_GRAPHICS_TEXTURE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_GRAPHICS_TEXTURE: Int
```

**Deprecated:** *Deprecated in Java.*

The Allocation will be used as a texture source by one or more graphics programs.

 Value: 2

### USAGE_GRAPHICS_VERTEX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_GRAPHICS_VERTEX: Int
```

**Deprecated:** *Deprecated in Java.*

The Allocation will be used as a graphics mesh. This was deprecated in API level 16.

 Value: 4

### USAGE_IO_INPUT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_IO_INPUT: Int
```

**Deprecated:** *Deprecated in Java.*

The Allocation will be used as a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` consumer. This usage will cause the Allocation to be created as read-only.

 Value: 32

### USAGE_IO_OUTPUT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_IO_OUTPUT: Int
```

**Deprecated:** *Deprecated in Java.*

The Allocation will be used as a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` producer. The dimensions and format of the `https://developer.android.com/reference/kotlin/android/view/Surface.html#` will be forced to those of the Allocation.

 Value: 64

### USAGE_SCRIPT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_SCRIPT: Int
```

**Deprecated:** *Deprecated in Java.*

The Allocation will be bound to and accessed by scripts.

 Value: 1

### USAGE_SHARED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_SHARED: Int
```

**Deprecated:** *Deprecated in Java.*

The Allocation's backing store will be inherited from another object (usually a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`); copying to or from the original source Bitmap will cause a synchronization rather than a full copy. syncAll may also be used to synchronize the Allocation and the source Bitmap.

This is set by default for allocations created with #createFromBitmap in API version 18 and higher.

 Value: 128

## Public methods

### copy1DRangeFrom

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFrom(
    off: Int, 
    count: Int, 
    data: Allocation!, 
    dataOff: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy part of an Allocation into this Allocation.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `data` | [Allocation](Allocation.md)!: the source data allocation. |
| --- | --- |
| `dataOff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): off The offset of the first element in data to be copied. |

### copy1DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFrom(
    off: Int, 
    count: Int, 
    d: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This variant is type checked and will generate exceptions if the Allocation's Element is not an 8 bit integer nor a vector of 8 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFrom(
    off: Int, 
    count: Int, 
    d: FloatArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 32 bit float nor a vector of 32 bit floats `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: the source array. |
| --- | --- |

### copy1DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFrom(
    off: Int, 
    count: Int, 
    d: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This variant is type checked and will generate exceptions if the Allocation's Element is not an 32 bit integer nor a vector of 32 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeFrom

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFrom(
    off: Int, 
    count: Int, 
    array: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This variant is type checked and will generate exceptions if the Allocation's Element does not match the component type of the array passed in.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The source array. |
| --- | --- |

### copy1DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFrom(
    off: Int, 
    count: Int, 
    d: ShortArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This variant is type checked and will generate exceptions if the Allocation's Element is not an 16 bit integer nor a vector of 16 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeFromUnchecked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFromUnchecked(
    off: Int, 
    count: Int, 
    d: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeFromUnchecked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFromUnchecked(
    off: Int, 
    count: Int, 
    d: FloatArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeFromUnchecked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFromUnchecked(
    off: Int, 
    count: Int, 
    d: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeFromUnchecked

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFromUnchecked(
    off: Int, 
    count: Int, 
    array: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The source array |
| --- | --- |

### copy1DRangeFromUnchecked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeFromUnchecked(
    off: Int, 
    count: Int, 
    d: ShortArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array into a 1D region of this Allocation. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeTo(
    off: Int, 
    count: Int, 
    d: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither an 8 bit integer nor a vector of 8 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeTo(
    off: Int, 
    count: Int, 
    d: FloatArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 32 bit float nor a vector of 32 bit floats `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: the source array. |
| --- | --- |

### copy1DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeTo(
    off: Int, 
    count: Int, 
    d: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 32 bit integer nor a vector of 32 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeTo(
    off: Int, 
    count: Int, 
    array: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This method is type checked and will generate exceptions if the Allocation's Element does not match the component type of the array passed in.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The source array. |
| --- | --- |

### copy1DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeTo(
    off: Int, 
    count: Int, 
    d: ShortArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 16 bit integer nor a vector of 16 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeToUnchecked

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeToUnchecked(
    off: Int, 
    count: Int, 
    d: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeToUnchecked

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeToUnchecked(
    off: Int, 
    count: Int, 
    d: FloatArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeToUnchecked

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeToUnchecked(
    off: Int, 
    count: Int, 
    d: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: the source array |
| --- | --- |

### copy1DRangeToUnchecked

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeToUnchecked(
    off: Int, 
    count: Int, 
    array: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The dest array |
| --- | --- |

### copy1DRangeToUnchecked

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy1DRangeToUnchecked(
    off: Int, 
    count: Int, 
    d: ShortArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a 1D region of this Allocation into an array. This method does not guarantee that the Allocation is compatible with the input buffer.

The size of the region is: count \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset of the first element to be copied. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of elements to be copied. |
| `d` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: the source array |
| --- | --- |

### copy2DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    data: Bitmap!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` into an Allocation. The height and width of the update will use the height and width of the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to update in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to update in this Allocation |
| `data` | [Bitmap](../android.graphics/Bitmap.md)!: the Bitmap to be copied |
| --- | --- |

### copy2DRangeFrom

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: Allocation!, 
    dataXoff: Int, 
    dataYoff: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a rectangular region from an Allocation into a rectangular region in this Allocation.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to update. |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to update. |
| `data` | [Allocation](Allocation.md)!: source Allocation. |
| `dataXoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset in source Allocation |
| --- | --- |
| `dataYoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset in source Allocation |

### copy2DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from an array into a rectangular region in this Allocation. The array is assumed to be tightly packed. This variant is type checked and will generate exceptions if the Allocation's Element is not an 8 bit integer nor a vector of 8 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to update in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to update in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to update |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to update |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: to be placed into the Allocation |

### copy2DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: FloatArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from an array into a rectangular region in this Allocation. The array is assumed to be tightly packed. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 32 bit float nor a vector of 32 bit floats `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to update in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to update in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to update |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to update |
| `data` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: to be placed into the Allocation |

### copy2DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from an array into a rectangular region in this Allocation. The array is assumed to be tightly packed. This variant is type checked and will generate exceptions if the Allocation's Element is not a 32 bit integer nor a vector of 32 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to update in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to update in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to update |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to update |
| `data` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: to be placed into the Allocation |

### copy2DRangeFrom

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    array: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from an array into a rectangular region in this Allocation. The array is assumed to be tightly packed. This variant is type checked and will generate exceptions if the Allocation's Element does not match the input data type.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to update in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to update in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to update |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to update |
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Data to be placed into the Allocation |

### copy2DRangeFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: ShortArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from an array into a rectangular region in this Allocation. The array is assumed to be tightly packed. This variant is type checked and will generate exceptions if the Allocation's Element is not a 16 bit integer nor a vector of 16 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to update in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to update in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to update |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to update |
| `data` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: to be placed into the Allocation |

### copy2DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeTo(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from a rectangular region in this Allocation into an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither an 8 bit integer nor a vector of 8 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to copy in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to copy in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to copy |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to copy |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Dest Array to be copied into |

### copy2DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeTo(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: FloatArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from a rectangular region in this Allocation into an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 32 bit float nor a vector of 32 bit floats `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to copy in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to copy in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to copy |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to copy |
| `data` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: Dest Array to be copied into |

### copy2DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeTo(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from a rectangular region in this Allocation into an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 32 bit integer nor a vector of 32 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to copy in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to copy in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to copy |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to copy |
| `data` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Dest Array to be copied into |

### copy2DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeTo(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    array: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from a rectangular region in this Allocation into an array. This method is type checked and will generate exceptions if the Allocation's Element does not match the component type of the array passed in.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to copy in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to copy in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to copy |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to copy |
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Dest Array to be copied into |

### copy2DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy2DRangeTo(
    xoff: Int, 
    yoff: Int, 
    w: Int, 
    h: Int, 
    data: ShortArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from a rectangular region in this Allocation into an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 16 bit integer nor a vector of 16 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

The size of the region is: w \* h \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to copy in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to copy in this Allocation |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to copy |
| --- | --- |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to copy |
| `data` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: Dest Array to be copied into |

### copy3DRangeFrom

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy3DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    zoff: Int, 
    w: Int, 
    h: Int, 
    d: Int, 
    data: Allocation!, 
    dataXoff: Int, 
    dataYoff: Int, 
    dataZoff: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy a rectangular region into the allocation from another allocation.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to update in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to update in this Allocation |
| `zoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Z offset of the region to update in this Allocation |
| --- | --- |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to update. |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to update. |
| `d` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Depth of the region to update. |
| --- | --- |
| `data` | [Allocation](Allocation.md)!: source allocation. |
| `dataXoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region in the source Allocation |
| `dataYoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region in the source Allocation |
| --- | --- |
| `dataZoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Z offset of the region in the source Allocation |

### copy3DRangeFrom

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy3DRangeFrom(
    xoff: Int, 
    yoff: Int, 
    zoff: Int, 
    w: Int, 
    h: Int, 
    d: Int, 
    array: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from an array into a 3D region in this Allocation. The array is assumed to be tightly packed. This variant is type checked and will generate exceptions if the Allocation's Element does not match the input data type.

The size of the region is: w \* h \* d \* getElement.getBytesSize.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the region.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the region. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the region. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): X offset of the region to update in this Allocation |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Y offset of the region to update in this Allocation |
| `zoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Z offset of the region to update in this Allocation |
| --- | --- |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the region to update |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the region to update |
| `d` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Depth of the region to update |
| --- | --- |
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: to be placed into the allocation |

### copy3DRangeTo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copy3DRangeTo(
    xoff: Int, 
    yoff: Int, 
    zoff: Int, 
    w: Int, 
    h: Int, 
    d: Int, 
    array: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

### copyFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFrom(b: Bitmap!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into an Allocation from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`. The height, width, and format of the bitmap must match the existing allocation.

If the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` is the same as the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` used to create the Allocation with #createFromBitmap and `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_SHARED:kotlin.Int` is set on the Allocation, this will synchronize the Allocation with the latest data from the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`, potentially avoiding the actual copy.

| Parameters ||
|---|---|
| `b` | [Bitmap](../android.graphics/Bitmap.md)!: the source bitmap |

### copyFrom

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFrom(a: Allocation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an Allocation from an Allocation. The types of both allocations must be identical.

| Parameters ||
|---|---|
| `a` | [Allocation](Allocation.md)!: the source allocation |

### copyFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFrom(d: Array<BaseObj!>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy an array of RS objects to the Allocation.

| Parameters ||
|---|---|
| `d` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [BaseObj](BaseObj.md)!\>!: Source array. |

### copyFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFrom(d: ByteArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This variant is type checked and will generate exceptions if the Allocation's Element is not an 8 bit integer nor a vector of 8 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the source array |

### copyFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFrom(d: FloatArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 32 bit float nor a vector of 32 bit floats `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: the source array |

### copyFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFrom(d: IntArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This variant is type checked and will generate exceptions if the Allocation's Element is not a 32 bit integer nor a vector of 32 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: the source array |

### copyFrom

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFrom(array: Any!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This variant is type checked and will generate exceptions if the Allocation's Element does not match the array's primitive type.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The source array |

### copyFrom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFrom(d: ShortArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This variant is type checked and will generate exceptions if the Allocation's Element is not a 16 bit integer nor a vector of 16 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: the source array |

### copyFromUnchecked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFromUnchecked(d: ByteArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This method does not guarantee that the Allocation is compatible with the input buffer; it copies memory without reinterpretation.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the source array |

### copyFromUnchecked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFromUnchecked(d: FloatArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This method does not guarantee that the Allocation is compatible with the input buffer; it copies memory without reinterpretation.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: the source array |

### copyFromUnchecked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFromUnchecked(d: IntArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This method does not guarantee that the Allocation is compatible with the input buffer; it copies memory without reinterpretation.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: the source array |

### copyFromUnchecked

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFromUnchecked(array: Any!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This method does not guarantee that the Allocation is compatible with the input buffer; it copies memory without reinterpretation.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The source array |

### copyFromUnchecked

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyFromUnchecked(d: ShortArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy into this Allocation from an array. This method does not guarantee that the Allocation is compatible with the input buffer; it copies memory without reinterpretation.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells must be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: the source array |

### copyTo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyTo(b: Bitmap!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from the Allocation into a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`. The bitmap must match the dimensions of the Allocation.

| Parameters ||
|---|---|
| `b` | [Bitmap](../android.graphics/Bitmap.md)!: The bitmap to be set from the Allocation. |

### copyTo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyTo(d: ByteArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from the Allocation into a byte array. This variant is type checked and will generate exceptions if the Allocation's Element is neither an 8 bit integer nor a vector of 8 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells will be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The array to be set from the Allocation. |

### copyTo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyTo(d: FloatArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from the Allocation into a float array. This variant is type checked and will generate exceptions if the Allocation's Element is neither a 32 bit float nor a vector of 32 bit floats `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells will be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: The array to be set from the Allocation. |

### copyTo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyTo(d: IntArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from the Allocation into a int array. This variant is type checked and will generate exceptions if the Allocation's Element is not a 32 bit integer nor a vector of 32 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells will be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The array to be set from the Allocation. |

### copyTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyTo(array: Any!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from the Allocation into an array. The method is type checked and will generate exceptions if the Allocation's Element does not match the input data type.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells will be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The array to be set from the Allocation. |

### copyTo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun copyTo(d: ShortArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy from the Allocation into a short array. This variant is type checked and will generate exceptions if the Allocation's Element is not a 16 bit integer nor a vector of 16 bit integers `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`.

If the Allocation does not have Vec3 Elements, then the size of the array in bytes must be at least the size of the Allocation getBytesSize.

If the Allocation has Vec3 Elements and setAutoPadding is disabled, then the size of the array in bytes must be at least the size of the Allocation getBytesSize. The padding bytes for the cells will be part of the array.

If the Allocation has Vec3 Elements and setAutoPadding is enabled, then the size of the array in bytes must be at least 3/4 the size of the Allocation getBytesSize. The padding bytes for the cells must not be part of the array.

| Parameters ||
|---|---|
| `d` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!: The array to be set from the Allocation. |

### createAllocations

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createAllocations(
    rs: RenderScript!, 
    t: Type!, 
    usage: Int, 
    numAlloc: Int
): Array<Allocation!>!
```

**Deprecated:** *Deprecated in Java.*

Creates a new Allocation Array with the given Type, and usage flags. Note: If the input allocation is of usage: USAGE_IO_INPUT, the created Allocation will be sharing the same BufferQueue.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: RenderScript context |
| `t` | [Type](Type.md)!: RenderScript type describing data layout |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the Allocation is utilized |
| --- | --- |
| `numAlloc` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of Allocations in the array. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!>!` | Allocation\[\] |

### createCubemapFromBitmap

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createCubemapFromBitmap(
    rs: RenderScript!, 
    b: Bitmap!
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates a non-mipmapped cubemap Allocation for use as a graphics texture from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` containing the horizontal list of cube faces. Each face must be a square, have the same size as all other faces, and have a width that is a power of 2.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `b` | [Bitmap](../android.graphics/Bitmap.md)!: bitmap with cubemap faces layed out in the following format: right, left, top, bottom, front, back |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | allocation containing cubemap data |

### createCubemapFromBitmap

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createCubemapFromBitmap(
    rs: RenderScript!, 
    b: Bitmap!, 
    mips: Allocation.MipmapControl!, 
    usage: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates a cubemap Allocation from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` containing the horizontal list of cube faces. Each face must be a square, have the same size as all other faces, and have a width that is a power of 2.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `b` | [Bitmap](../android.graphics/Bitmap.md)!: Bitmap with cubemap faces layed out in the following format: right, left, top, bottom, front, back |
| `mips` | [Allocation.MipmapControl](../android/renderscript/Allocation.MipmapControl.md)!: specifies desired mipmap behaviour for the cubemap |
| --- | --- |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the cubemap is utilized |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | allocation containing cubemap data |

### createCubemapFromCubeFaces

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createCubemapFromCubeFaces(
    rs: RenderScript!, 
    xpos: Bitmap!, 
    xneg: Bitmap!, 
    ypos: Bitmap!, 
    yneg: Bitmap!, 
    zpos: Bitmap!, 
    zneg: Bitmap!
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates a non-mipmapped cubemap Allocation for use as a sampler input from 6 `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` objects containing the cube faces. Each face must be a square, have the same size as all other faces, and have a width that is a power of 2.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `xpos` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the positive x direction |
| `xneg` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the negative x direction |
| --- | --- |
| `ypos` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the positive y direction |
| `yneg` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the negative y direction |
| `zpos` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the positive z direction |
| --- | --- |
| `zneg` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the negative z direction |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | allocation containing cubemap data |

### createCubemapFromCubeFaces

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createCubemapFromCubeFaces(
    rs: RenderScript!, 
    xpos: Bitmap!, 
    xneg: Bitmap!, 
    ypos: Bitmap!, 
    yneg: Bitmap!, 
    zpos: Bitmap!, 
    zneg: Bitmap!, 
    mips: Allocation.MipmapControl!, 
    usage: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates a cubemap Allocation from 6 `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` objects containing the cube faces. Each face must be a square, have the same size as all other faces, and have a width that is a power of 2.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `xpos` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the positive x direction |
| `xneg` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the negative x direction |
| --- | --- |
| `ypos` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the positive y direction |
| `yneg` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the negative y direction |
| `zpos` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the positive z direction |
| --- | --- |
| `zneg` | [Bitmap](../android.graphics/Bitmap.md)!: cubemap face in the negative z direction |
| `mips` | [Allocation.MipmapControl](../android/renderscript/Allocation.MipmapControl.md)!: specifies desired mipmap behaviour for the cubemap |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the cubemap is utilized |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | allocation containing cubemap data |

### createFromBitmap

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromBitmap(
    rs: RenderScript!, 
    b: Bitmap!
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates an Allocation from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`.

With target API version 18 or greater, this Allocation will be created with `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_SHARED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_SCRIPT:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_TEXTURE:kotlin.Int`. With target API version 17 or lower, this Allocation will be created with `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_TEXTURE:kotlin.Int`.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `b` | [Bitmap](../android.graphics/Bitmap.md)!: bitmap source for the allocation data |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | Allocation containing bitmap data |

### createFromBitmap

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromBitmap(
    rs: RenderScript!, 
    b: Bitmap!, 
    mips: Allocation.MipmapControl!, 
    usage: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates an Allocation from a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `b` | [Bitmap](../android.graphics/Bitmap.md)!: Bitmap source for the allocation data |
| `mips` | [Allocation.MipmapControl](../android/renderscript/Allocation.MipmapControl.md)!: specifies desired mipmap behaviour for the allocation |
| --- | --- |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the allocation is utilized |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | Allocation containing bitmap data |

### createFromBitmapResource

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromBitmapResource(
    rs: RenderScript!, 
    res: Resources!, 
    id: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates a non-mipmapped Allocation to use as a graphics texture from the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` referenced by resource ID.

With target API version 18 or greater, this allocation will be created with `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_SCRIPT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_TEXTURE:kotlin.Int`. With target API version 17 or lower, this allocation will be created with `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_GRAPHICS_TEXTURE:kotlin.Int`.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `res` | [Resources](../android.content.res/Resources.md)!: application resources |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource id to load the data from |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | Allocation containing resource data |

### createFromBitmapResource

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromBitmapResource(
    rs: RenderScript!, 
    res: Resources!, 
    id: Int, 
    mips: Allocation.MipmapControl!, 
    usage: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates an Allocation from the Bitmap referenced by resource ID.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `res` | [Resources](../android.content.res/Resources.md)!: application resources |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource id to load the data from |
| --- | --- |
| `mips` | [Allocation.MipmapControl](../android/renderscript/Allocation.MipmapControl.md)!: specifies desired mipmap behaviour for the allocation |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the allocation is utilized |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | Allocation containing resource data |

### createFromString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createFromString(
    rs: RenderScript!, 
    str: String!, 
    usage: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates an Allocation containing string data encoded in UTF-8 format.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: string to create the allocation from |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the allocaiton is utilized |
| --- | --- |

### createSized

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createSized(
    rs: RenderScript!, 
    e: Element!, 
    count: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates an Allocation with a specified number of given elements

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the Allocation will belong. |
| `e` | [Element](Element.md)!: Element to use in the Allocation |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of Elements in the Allocation |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | allocation |

### createSized

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createSized(
    rs: RenderScript!, 
    e: Element!, 
    count: Int, 
    usage: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates an Allocation with a specified number of given elements

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the Allocation will belong. |
| `e` | [Element](Element.md)!: Element to use in the Allocation |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of Elements in the Allocation |
| --- | --- |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the Allocation is utilized |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | allocation |

### createTyped

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createTyped(
    rs: RenderScript!, 
    type: Type!
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates an Allocation for use by scripts with a given Type and no mipmaps

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the Allocation will belong. |
| `type` | [Type](Type.md)!: RenderScript Type describing data layout |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | allocation |

### createTyped

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createTyped(
    rs: RenderScript!, 
    type: Type!, 
    mips: Allocation.MipmapControl!, 
    usage: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates a new Allocation with the given Type, mipmap flag, and usage flags.

| Parameters ||
|---|---|
| `type` | [Type](Type.md)!: RenderScript type describing data layout |
| `mips` | [Allocation.MipmapControl](../android/renderscript/Allocation.MipmapControl.md)!: specifies desired mipmap behaviour for the allocation |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the Allocation is utilized |
| --- | --- |

### createTyped

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createTyped(
    rs: RenderScript!, 
    type: Type!, 
    usage: Int
): Allocation!
```

**Deprecated:** *Deprecated in Java.*

Creates an Allocation with the size specified by the type and no mipmaps generated by default

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: Context to which the allocation will belong. |
| `type` | [Type](Type.md)!: renderscript type describing data layout |
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field specifying how the allocation is utilized |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#!` | allocation |

### destroy

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun destroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

For USAGE_IO_OUTPUT, destroy() implies setSurface(null).

### generateMipmaps

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun generateMipmaps(): Unit
```

**Deprecated:** *Deprecated in Java.*

Generate a mipmap chain. This is only valid if the Type of the Allocation includes mipmaps.

This function will generate a complete set of mipmaps from the top level LOD and place them into the script memory space.

If the Allocation is also using other memory spaces, a call to syncAll is required.

### getByteBuffer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getByteBuffer(): ByteBuffer!
```

**Deprecated:** *Deprecated in Java.*

Gets or creates a ByteBuffer that contains the raw data of the current Allocation.

If the Allocation is created with USAGE_IO_INPUT, the returned ByteBuffer would contain the up-to-date data as READ ONLY. For a 2D or 3D Allocation, the raw data maybe padded so that each row of the Allocation has certain alignment. The size of each row including padding, called stride, can be queried using the getStride method. Note: Operating on the ByteBuffer of a destroyed Allocation will triger errors.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!` | ByteBuffer The ByteBuffer associated with raw data pointer of the Allocation. |

### getBytesSize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBytesSize(): Int
```

**Deprecated:** *Deprecated in Java.*

Get the size of the Allocation in bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | size of the Allocation in bytes. |

### getElement

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getElement(): Element!
```

**Deprecated:** *Deprecated in Java.*

Get the Element of the Type of the Allocation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Element!` | Element |

### getStride

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStride(): Long
```

**Deprecated:** *Deprecated in Java.*

Gets the stride of the Allocation. For a 2D or 3D Allocation, the raw data maybe padded so that each row of the Allocation has certain alignment. The size of each row including such padding is called stride.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the stride. For 1D Allocation, the stride will be the number of bytes of this Allocation. For 2D and 3D Allocations, the stride will be the stride in X dimension measuring in bytes. |

### getSurface

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSurface(): Surface!
```

**Deprecated:** *Deprecated in Java.*

Returns the handle to a raw buffer that is being managed by the screen compositor. This operation is only valid for Allocations with `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_INPUT:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Surface.html#!` | Surface object associated with allocation |

### getTimeStamp

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeStamp(): Long
```

**Deprecated:** *Deprecated in Java.*

Get the timestamp for the most recent buffer held by this Allocation. The timestamp is guaranteed to be unique and monotonically increasing. Default value: -1. The timestamp will be updated after each ioReceive call. It can be used to identify the images by comparing the unique timestamps when used with `https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary.html` APIs. Example steps: 1. Save `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult.html#` when the capture is completed. 2. Get the timestamp after ioReceive call. 3. Comparing totalCaptureResult.get(CaptureResult.SENSOR_TIMESTAMP) with alloc.getTimeStamp().

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | long Timestamp associated with the buffer held by the Allocation. |

### getType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(): Type!
```

**Deprecated:** *Deprecated in Java.*

Get the Type of the Allocation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/Type!` | Type |

### getUsage

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUsage(): Int
```

**Deprecated:** *Deprecated in Java.*

Get the usage flags of the Allocation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | usage this Allocation's set of the USAGE_\* flags OR'd together |

### ioReceive

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ioReceive(): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive the latest input into the Allocation. This operation is only valid if `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_INPUT:kotlin.Int` is set on the Allocation.

### ioSend

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ioSend(): Unit
```

**Deprecated:** *Deprecated in Java.*

Send a buffer to the output stream. The contents of the Allocation will be undefined after this operation. This operation is only valid if `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_OUTPUT:kotlin.Int` is set on the Allocation.

### resize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resize(dimX: Int): Unit
```

**Deprecated:** *RenderScript objects should be immutable once created. The replacement is to create a new allocation and copy the contents. This function will throw an exception if API 21 or higher is used.*

Resize a 1D allocation. The contents of the allocation are preserved. If new elements are allocated objects are created with null contents and the new region is otherwise undefined.

If the new region is smaller the references of any objects outside the new region will be released.

A new type will be created with the new dimension.

| Parameters ||
|---|---|
| `dimX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new size of the allocation. |

### setAutoPadding

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutoPadding(useAutoPadding: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Specifies the mapping between the Allocation's cells and an array's elements when data is copied from the Allocation to the array, or vice-versa. Only applies to an Allocation whose Element is a vector of length 3 (such as U8_3 or RGB_888). Enabling this feature may make copying data from the Allocation to an array or vice-versa less efficient.

Vec3 Element cells are stored in an Allocation as Vec4 Element cells with the same `https://developer.android.com/reference/kotlin/android/renderscript/Element.DataType`, with the fourth vector component treated as padding. When this feature is enabled, only the data components, i.e. the first 3 vector components of each cell, will be mapped between the array and the Allocation. When disabled, explicit mapping of the padding components is required, as described in the following example.

For example, when copying an integer array to an Allocation of two I32_3 cells using copyFrom:

When disabled: The array must have at least 8 integers, with the first 4 integers copied to the first cell of the Allocation, and the next 4 integers copied to the second cell. The 4th and 8th integers are mapped as the padding components.

When enabled: The array just needs to have at least 6 integers, with the first 3 integers copied to the the first cell as data components, and the next 3 copied to the second cell. There is no mapping for the padding components.

Similarly, when copying a byte array to an Allocation of two I32_3 cells, using copyFromUnchecked:

When disabled: The array must have at least 32 bytes, with the first 16 bytes copied to the first cell of the Allocation, and the next 16 bytes copied to the second cell. The 13th-16th and 29th-32nd bytes are mapped as padding components.

When enabled: The array just needs to have at least 24 bytes, with the first 12 bytes copied to the first cell of the Allocation, and the next 12 bytes copied to the second cell. There is no mapping for the padding components.

Similar to copying data to an Allocation from an array, when copying data from an Allocation to an array, the padding components for Vec3 Element cells will not be copied/mapped to the array if AutoPadding is enabled.

Default: Disabled.

| Parameters ||
|---|---|
| `useAutoPadding` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True: enable AutoPadding; False: disable AutoPadding |

### setFromFieldPacker

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFromFieldPacker(
    xoff: Int, 
    fp: FieldPacker!
): Unit
```

**Deprecated:** *Deprecated in Java.*

This is only intended to be used by auto-generated code reflected from the RenderScript script files and should not be used by developers.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `fp` | [FieldPacker](FieldPacker.md)!: |

### setFromFieldPacker

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFromFieldPacker(
    xoff: Int, 
    component_number: Int, 
    fp: FieldPacker!
): Unit
```

**Deprecated:** *Deprecated in Java.*

This is only intended to be used by auto-generated code reflected from the RenderScript script files and should not be used by developers.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `component_number` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `fp` | [FieldPacker](FieldPacker.md)!: |
| --- | --- |

### setFromFieldPacker

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFromFieldPacker(
    xoff: Int, 
    yoff: Int, 
    zoff: Int, 
    component_number: Int, 
    fp: FieldPacker!
): Unit
```

**Deprecated:** *Deprecated in Java.*

This is only intended to be used by auto-generated code reflected from the RenderScript script files and should not be used by developers.

| Parameters ||
|---|---|
| `xoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `yoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `zoff` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |
| `component_number` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `fp` | [FieldPacker](FieldPacker.md)!: |

### setOnBufferAvailableListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnBufferAvailableListener(callback: Allocation.OnBufferAvailableListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a notification handler for `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_INPUT:kotlin.Int`.

| Parameters ||
|---|---|
| `callback` | [Allocation.OnBufferAvailableListener](../android/renderscript/Allocation.OnBufferAvailableListener.md)!: instance of the OnBufferAvailableListener class to be called when buffer arrive. |

### setSurface

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSurface(sur: Surface!): Unit
```

**Deprecated:** *Deprecated in Java.*

Associate a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` with this Allocation. This operation is only valid for Allocations with `https://developer.android.com/reference/kotlin/android/renderscript/Allocation#USAGE_IO_OUTPUT:kotlin.Int`.

| Parameters ||
|---|---|
| `sur` | [Surface](../android.view/Surface.md)!: Surface to associate with allocation |

### syncAll

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun syncAll(srcLocation: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Propagate changes from one usage of the Allocation to the other usages of the Allocation.

## Protected methods

### finalize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
