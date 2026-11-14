# Element

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Element

Kotlin| [Java](Element.md) 
| --- | --- |

```
open class Element : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||
| | ↳ | [android.renderscript.Element](Element.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

An Element represents one item within an . An Element is roughly equivalent to a C type in a RenderScript kernel. Elements may be basic or complex. Some basic elements are

- A single float value (equivalent to a float in a kernel)
- A four-element float vector (equivalent to a float4 in a kernel)
- An unsigned 32-bit integer (equivalent to an unsigned int in a kernel)
- A single signed 8-bit integer (equivalent to a char in a kernel)

A complex element is roughly equivalent to a C struct and contains a number of basic or complex Elements. From Java code, a complex element contains a list of sub-elements and names that represents a particular data structure. Structs used in RS scripts are available to Java code by using the`ScriptField_structname`class that is reflected from a particular script.

Basic Elements are comprised of a and a . The DataType encodes C type information of an Element, while the DataKind encodes how that Element should be interpreted by a [android.renderscript.Sampler](Sampler.md). Note that objects with DataKind [android.renderscript.Element.DataKind#USER](../android/renderscript/Element.DataKind.md) cannot be used as input for a [android.renderscript.Sampler](Sampler.md). In general, objects that are intended for use with a [android.renderscript.Sampler](Sampler.md) should use bitmap-derived Elements such as [android.renderscript.Element#RGBA_8888](Element.md))or android.renderscript#Element.A_8.
|
| ### Developer Guides
|
| For more information about creating an application that uses RenderScript, read the [RenderScript](https://developer.android.com/guide/topics/renderscript/index.html) developer guide.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/renderscript/Element.Builder.md) Builder class for producing complex elements with matching field and name pairs. |
| | [DataKind](../android/renderscript/Element.DataKind.md) The special interpretation of the data if required. |
| | [DataType](../android/renderscript/Element.DataType.md) DataType represents the basic type information for a basic element. |
| --- | --- |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Element](Element.md)! | [ALLOCATION](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [A_8](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [BOOLEAN](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Utility function for returning an Element containing a single Boolean. |
| --- | --- |
| openstatic [Element](Element.md)! | [ELEMENT](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [F16](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [F16_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [F16_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [F16_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [F32](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [F32_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [F32_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [F32_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [F64](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [F64_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [F64_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [F64_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [FONT](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I16](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [I16_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I16_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I16_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [I32](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I32_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I32_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [I32_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I64](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I64_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [I64_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I64_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I8](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Utility function for returning an Element containing a single SIGNED_8. |
| --- | --- |
| openstatic [Element](Element.md)! | [I8_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I8_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [I8_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [MATRIX4X4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [MATRIX_2X2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [MATRIX_3X3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [MATRIX_4X4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [MESH](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [PROGRAM_FRAGMENT](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [PROGRAM_RASTER](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [PROGRAM_STORE](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [PROGRAM_VERTEX](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [RGBA_4444](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [RGBA_5551](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [RGBA_8888](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [RGB_565](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [RGB_888](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [SAMPLER](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [SCRIPT](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [TYPE](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U16](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [U16_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U16_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U16_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [U32](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U32_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U32_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [U32_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U64](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U64_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [U64_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U64_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U8](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` Utility function for returning an Element containing a single UNSIGNED_8. |
| --- | --- |
| openstatic [Element](Element.md)! | [U8_2](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U8_3](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [U8_4](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| --- | --- |
| openstatic [Element](Element.md)! | [YUV](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`)` <br /> |
| openstatic [Element](Element.md)! | [createPixel](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`, `dt:` ` [Element.DataType](../android/renderscript/Element.DataType.md)!`, `dk:` ` [Element.DataKind](../android/renderscript/Element.DataKind.md)!`)` Create a new pixel Element type. |
| openstatic [Element](Element.md)! | [createVector](Element.md))`(`rs:` ` [RenderScript](RenderScript.md)!`, `dt:` ` [Element.DataType](../android/renderscript/Element.DataType.md)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a custom vector element of the specified DataType and vector size. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBytesSize](Element.md))`()` <br /> |
| open [Element.DataKind](../android/renderscript/Element.DataKind.md)! | [getDataKind](Element.md))`()` <br /> |
| open [Element.DataType](../android/renderscript/Element.DataType.md)! | [getDataType](Element.md))`()` <br /> |
| --- | --- |
| open [Element](Element.md)! | [getSubElement](Element.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` For complex elements, this function will return the sub-element at index |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubElementArraySize](Element.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` For complex elements, some sub-elements could be statically sized arrays. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubElementCount](Element.md))`()` Elements could be simple, such as an int or a float, or a structure with multiple sub elements, such as a collection of floats, float2, float4. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubElementName](Element.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` For complex elements, this function will return the sub-element name at index |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubElementOffsetBytes](Element.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This function specifies the location of a sub-element within the element |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVectorSize](Element.md))`()` Returns the number of vector components. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCompatible](Element.md))`(`e:` ` [Element](Element.md)!`)` Check if the current Element is compatible with another Element. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isComplex](Element.md))`()` Return if a element is too complex for use as a data source for a Mesh or a Program. |

| Inherited functions ||
|---|---|
| From class [BaseObj](BaseObj.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](BaseObj.md))`()` <br /> Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](BaseObj.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](BaseObj.md))`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](BaseObj.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](BaseObj.md))`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](BaseObj.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

## Public methods

### ALLOCATION

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ALLOCATION(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### A_8

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun A_8(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### BOOLEAN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun BOOLEAN(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.*

Utility function for returning an Element containing a single Boolean.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:Context to which the element will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Element](Element.md)! | Element |

### ELEMENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ELEMENT(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F16

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F16(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F16_2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F16_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F16_3

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F16_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F16_4

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F16_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F32

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F32(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F32_2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F32_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F32_3

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F32_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F32_4

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F32_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F64

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F64(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F64_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F64_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F64_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F64_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### F64_4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun F64_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### FONT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun FONT(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I16

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I16(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I16_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I16_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I16_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I16_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I16_4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I16_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I32

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I32(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I32_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I32_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I32_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I32_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I32_4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I32_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I64

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I64(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I64_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I64_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I64_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I64_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I64_4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I64_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I8

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I8(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.*

Utility function for returning an Element containing a single SIGNED_8.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:Context to which the element will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Element](Element.md)! | Element |

### I8_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I8_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I8_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I8_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### I8_4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun I8_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### MATRIX4X4

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun MATRIX4X4(rs: RenderScript!): Element!
```

**Deprecated:** *use MATRIX_4X4* 

### MATRIX_2X2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun MATRIX_2X2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### MATRIX_3X3

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun MATRIX_3X3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### MATRIX_4X4

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun MATRIX_4X4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### MESH

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun MESH(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### PROGRAM_FRAGMENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun PROGRAM_FRAGMENT(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### PROGRAM_RASTER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun PROGRAM_RASTER(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### PROGRAM_STORE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun PROGRAM_STORE(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### PROGRAM_VERTEX

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun PROGRAM_VERTEX(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### RGBA_4444

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun RGBA_4444(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### RGBA_5551

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun RGBA_5551(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### RGBA_8888

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun RGBA_8888(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### RGB_565

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun RGB_565(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### RGB_888

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun RGB_888(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### SAMPLER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun SAMPLER(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### SCRIPT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun SCRIPT(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### TYPE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun TYPE(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U16

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U16(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U16_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U16_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U16_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U16_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U16_4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U16_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U32

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U32(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U32_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U32_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U32_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U32_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U32_4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U32_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U64

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U64(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U64_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U64_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U64_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U64_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U64_4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U64_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U8

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U8(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.*

Utility function for returning an Element containing a single UNSIGNED_8.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:Context to which the element will belong. |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Element](Element.md)! | Element |

### U8_2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U8_2(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U8_3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U8_3(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### U8_4

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun U8_4(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### YUV

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun YUV(rs: RenderScript!): Element!
```

**Deprecated:** *Deprecated in Java.* 

### createPixel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createPixel(
    rs: RenderScript!, 
    dt: Element.DataType!, 
    dk: Element.DataKind!
): Element!
```

**Deprecated:** *Deprecated in Java.*

Create a new pixel Element type. A matching DataType and DataKind must be provided. The DataType and DataKind must contain the same number of components. Vector size will be set to 1.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:The context associated with the new Element. |
| `dt` | [Element.DataType](../android/renderscript/Element.DataType.md)!:The DataType for the new element. |
| `dk` | [Element.DataKind](../android/renderscript/Element.DataKind.md)!:The DataKind to specify the mapping of each component in the DataType. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Element](Element.md)! | Element |

### createVector

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createVector(
    rs: RenderScript!, 
    dt: Element.DataType!, 
    size: Int
): Element!
```

**Deprecated:** *Deprecated in Java.*

Create a custom vector element of the specified DataType and vector size. DataKind will be set to USER. Only primitive types (FLOAT_32, FLOAT_64, SIGNED_8, SIGNED_16, SIGNED_32, SIGNED_64, UNSIGNED_8, UNSIGNED_16, UNSIGNED_32, UNSIGNED_64, BOOLEAN) are supported.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `rs` | [RenderScript](RenderScript.md)!:The context associated with the new Element. |
| `dt` | [Element.DataType](../android/renderscript/Element.DataType.md)!:The DataType for the new Element. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Vector size for the new Element. Range 2-4 inclusive supported. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|---------|
| [Element](Element.md)! | Element |

### getBytesSize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBytesSize(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | element size in bytes |

### getDataKind

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataKind(): Element.DataKind!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------|
| [Element.DataKind](../android/renderscript/Element.DataKind.md)! | element data kind |

### getDataType

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataType(): Element.DataType!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------|
| [Element.DataType](../android/renderscript/Element.DataType.md)! | element data type |

### getSubElement

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubElement(index: Int): Element!
```

**Deprecated:** *Deprecated in Java.*

For complex elements, this function will return the sub-element at index

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the sub-element to return |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------|
| [Element](Element.md)! | sub-element in this element at given index |

### getSubElementArraySize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubElementArraySize(index: Int): Int
```

**Deprecated:** *Deprecated in Java.*

For complex elements, some sub-elements could be statically sized arrays. This function will return the array size for sub-element at index

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the sub-element |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | array size of sub-element in this element at given index |

### getSubElementCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubElementCount(): Int
```

**Deprecated:** *Deprecated in Java.*

Elements could be simple, such as an int or a float, or a structure with multiple sub elements, such as a collection of floats, float2, float4. This function returns zero for simple elements or the number of sub-elements otherwise.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of sub-elements in this element |

### getSubElementName

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubElementName(index: Int): String!
```

**Deprecated:** *Deprecated in Java.*

For complex elements, this function will return the sub-element name at index

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the sub-element |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | sub-element in this element at given index |

### getSubElementOffsetBytes

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubElementOffsetBytes(index: Int): Int
```

**Deprecated:** *Deprecated in Java.*

This function specifies the location of a sub-element within the element

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the sub-element |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | offset in bytes of sub-element in this element at given index |

### getVectorSize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVectorSize(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the number of vector components. 2 for float2, 4 for float4, etc.

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | element vector size |

### isCompatible

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCompatible(e: Element!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Check if the current Element is compatible with another Element. Primitive Elements are compatible if they share the same underlying size and type (i.e. U8 is compatible with A_8). User-defined Elements must be equal in order to be compatible. This requires strict name equivalence for all sub-Elements (in addition to structural equivalence).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Element](Element.md)!:The Element to check compatibility with. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean true if the Elements are compatible, otherwise false. |

### isComplex

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isComplex(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return if a element is too complex for use as a data source for a Mesh or a Program.

| Return ||
|------------------------------------------------------------------------------------|---------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean |
