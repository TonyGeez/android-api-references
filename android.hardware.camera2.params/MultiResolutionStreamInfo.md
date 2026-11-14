# MultiResolutionStreamInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MultiResolutionStreamInfo

Kotlin| [Java](../android/hardware/camera2/params/MultiResolutionStreamInfo.md) 
| --- | --- |

```
open class MultiResolutionStreamInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md) |

A utility class describing the properties of one stream of fixed-size image buffers backing a multi-resolution image stream.

A group of [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md) are used to describe the properties of a multi-resolution image stream for a particular format. The [android.hardware.camera2.MultiResolutionImageReader](../android/hardware/camera2/MultiResolutionImageReader.md) class represents a multi-resolution output stream, and is constructed using a group of [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md). A group of [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md) can also be used to create a multi-resolution reprocessable camera capture session. See [android.hardware.camera2.params.InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md) for details.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md))`(`streamWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `streamHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `physicalCameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a new [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md). |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/hardware/camera2/params/MultiResolutionStreamInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md) is equal to another [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](../android/hardware/camera2/params/MultiResolutionStreamInfo.md))`()` The height of this particular image buffer stream in pixels. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPhysicalCameraId](../android/hardware/camera2/params/MultiResolutionStreamInfo.md))`()` The physical camera Id of this particular image buffer stream. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](../android/hardware/camera2/params/MultiResolutionStreamInfo.md))`()` The width of this particular image buffer stream in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/hardware/camera2/params/MultiResolutionStreamInfo.md))`()` Returns a hash code value for the object. |

## Public constructors

### MultiResolutionStreamInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MultiResolutionStreamInfo(
    streamWidth: Int, 
    streamHeight: Int, 
    physicalCameraId: String)
```

Create a new [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md).

This class creates a [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md) using image width, image height, and the physical camera Id images originate from.

Normally applications do not need to create these directly. Use [android.hardware.camera2.params.MultiResolutionStreamConfigurationMap#getOutputInfo](../android/hardware/camera2/params/MultiResolutionStreamConfigurationMap.md))or [android.hardware.camera2.params.MultiResolutionStreamConfigurationMap#getInputInfo](../android/hardware/camera2/params/MultiResolutionStreamConfigurationMap.md))to obtain them for a particular format instead.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `streamWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width in pixels of the camera stream Value is 1 or greater |
| `streamHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height in pixels of the camera stream Value is 1 or greater |
| `physicalCameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The physical camera Id the camera stream is associated with This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the streamWidth or streamHeight is invalid (either zero or negative). |

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Check if this [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md) is equal to another [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md).

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getHeight

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

The height of this particular image buffer stream in pixels.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 1 or greater |

### getPhysicalCameraId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPhysicalCameraId(): String
```

The physical camera Id of this particular image buffer stream.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getWidth

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

The width of this particular image buffer stream in pixels.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 1 or greater |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java/util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
