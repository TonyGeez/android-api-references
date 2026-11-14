# Capability

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Capability

Kotlin| [Java](../android/hardware/camera2/params/Capability.md) 
| --- | --- |

```
class Capability
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.Capability](../android/hardware/camera2/params/Capability.md) |

Immutable class to store the camera capability, its corresponding maximum streaming dimension and zoom range.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Capability](../android/hardware/camera2/params/Capability.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxStreamingSize:` ` [Size](../android/util/Size.md)`, `zoomRatioRange:` ` [Range](../android/util/Range.md)< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>`)` Create a new Capability object. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/hardware/camera2/params/Capability.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compare two Capability objects to see if they are equal. |
| [Size](../android/util/Size.md) | [getMaxStreamingSize](../android/hardware/camera2/params/Capability.md))`()` Return the maximum streaming dimension of this capability. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](../android/hardware/camera2/params/Capability.md))`()` Return the supported mode for this capability. |
| --- | --- |
| [Range](../android/util/Range.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | [getZoomRatioRange](../android/hardware/camera2/params/Capability.md))`()` Return the zoom ratio range of this capability. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/hardware/camera2/params/Capability.md))`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/hardware/camera2/params/Capability.md))`()` Return the Capability as a string representation`"(mode:%d, maxStreamingSize:%d x %d, zoomRatio: %f-%f)"`. |
| --- | --- |

## Public constructors

### Capability

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Capability(
    mode: Int, 
    maxStreamingSize: Size, 
    zoomRatioRange: Range<Float!>)
```

Create a new Capability object.

The mode argument can be any integer value. maxStreamingWidth and maxStreamingHeight must be non-negative, while minZoomRatio and maxZoomRatio must be strictly positive.

This constructor is public to allow for easier application testing by creating custom object instances. It's not necessary to construct these objects during normal use of the camera API.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):supported mode for a camera capability. |
| `maxStreamingSize` | [Size](../android/util/Size.md):The maximum streaming size for this mode This value cannot be`null`. |
| `zoomRatioRange` | [Range](../android/util/Range.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>:the minimum/maximum zoom ratio this mode supports This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the arguments are not valid |

## Public methods

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compare two Capability objects to see if they are equal.

| Parameters ||
|-------|---------------------------|
| `obj` | Another Capability object |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the mode, max size and zoom ratio range are equal,`false`otherwise |

### getMaxStreamingSize

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxStreamingSize(): Size
```

Return the maximum streaming dimension of this capability.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Size](../android/util/Size.md) | a new [Size](../android/util/Size.md) with non-negative width and height This value cannot be`null`. |

### getMode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMode(): Int
```

Return the supported mode for this capability.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | One of supported modes for the capability. For example, for available extended scene modes, this will be one of [CameraMetadata.CONTROL_EXTENDED_SCENE_MODE_DISABLED](../android/hardware/camera2/CameraMetadata.md), [CameraMetadata.CONTROL_EXTENDED_SCENE_MODE_BOKEH_STILL_CAPTURE](../android/hardware/camera2/CameraMetadata.md), and [CameraMetadata.CONTROL_EXTENDED_SCENE_MODE_BOKEH_CONTINUOUS](../android/hardware/camera2/CameraMetadata.md). |

### getZoomRatioRange

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZoomRatioRange(): Range<Float!>
```

Return the zoom ratio range of this capability.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Range](../android/util/Range.md)< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!> | The supported zoom ratio range supported by this capability This value cannot be`null`. |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java/util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return the Capability as a string representation`"(mode:%d, maxStreamingSize:%d x %d, zoomRatio: %f-%f)"`.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of the capability and max streaming size. |
