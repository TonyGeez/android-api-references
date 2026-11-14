# SessionConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SessionConfiguration

Kotlin| [Java](../android/hardware/camera2/params/SessionConfiguration.md) 
| --- | --- |

```
class SessionConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md) |

A helper class that aggregates all supported arguments for capture session initialization.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_HIGH_SPEED](../android/hardware/camera2/params/SessionConfiguration.md) A high speed session type that can only contain instances of [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_REGULAR](../android/hardware/camera2/params/SessionConfiguration.md) A regular session type containing instances of [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md) running at regular non high speed FPS ranges and optionally [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md) for reprocessable sessions. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md))`(`sessionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outputs:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md)!>`)` Create a new [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md) with sessionType and output configurations. |
| [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md))`(`sessionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outputs:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md)!>`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `cb:` ` [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md)`)` Create a new [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md). |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorSpace](../android/hardware/camera2/params/SessionConfiguration.md))`()` Clear the color space, such that the default color space will be used. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/hardware/camera2/params/SessionConfiguration.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/hardware/camera2/params/SessionConfiguration.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md) is equal to another [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md). |
| --- | --- |
| [ColorSpace](../android/graphics/ColorSpace.md)? | [getColorSpace](../android/hardware/camera2/params/SessionConfiguration.md))`()` Return the current color space. |
| [Executor](../java/util/concurrent/Executor.md)! | [getExecutor](../android/hardware/camera2/params/SessionConfiguration.md))`()` Retrieve the [java.util.concurrent.Executor](../java/util/concurrent/Executor.md) for the capture session. |
| [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md)! | [getInputConfiguration](../android/hardware/camera2/params/SessionConfiguration.md))`()` Retrieve the [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md). |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md)!\>! | [getOutputConfigurations](../android/hardware/camera2/params/SessionConfiguration.md))`()` Retrieve the [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md) list for the capture session. |
| [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)! | [getSessionParameters](../android/hardware/camera2/params/SessionConfiguration.md))`()` Retrieve the session wide camera parameters (see [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSessionType](../android/hardware/camera2/params/SessionConfiguration.md))`()` Retrieve the type of the capture session. |
| --- | --- |
| [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md)! | [getStateCallback](../android/hardware/camera2/params/SessionConfiguration.md))`()` Retrieve the [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md) for the capture session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/hardware/camera2/params/SessionConfiguration.md))`()` Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorSpace](../android/hardware/camera2/params/SessionConfiguration.md))`(`colorSpace:` ` [ColorSpace.Named](../android/graphics/ColorSpace.Named.md)`)` Set a specific device-supported color space. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputConfiguration](../android/hardware/camera2/params/SessionConfiguration.md))`(`input:` ` [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md)`)` Sets the [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md) for a reprocessable session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSessionParameters](../android/hardware/camera2/params/SessionConfiguration.md))`(`params:` ` [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)!`)` Sets the session wide camera parameters (see [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStateCallback](../android/hardware/camera2/params/SessionConfiguration.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `cb:` ` [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md)`)` Set the state callback and executor. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/hardware/camera2/params/SessionConfiguration.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md)!\> | [CREATOR](../android/hardware/camera2/params/SessionConfiguration.md) <br /> |

## Constants

### SESSION_HIGH_SPEED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_HIGH_SPEED: Int
```

A high speed session type that can only contain instances of [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md). The outputs can run using high speed FPS ranges. Calls to [setInputConfiguration](../android/hardware/camera2/params/SessionConfiguration.md))are not supported.

When using this type, the CameraCaptureSession returned by [android.hardware.camera2.CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md) can be cast to a [android.hardware.camera2.CameraConstrainedHighSpeedCaptureSession](../android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.md) to access the extra methods for constrained high speed recording. 

 Value: 1

**See Also**

- [android.hardware.camera2.CameraDevice#createConstrainedHighSpeedCaptureSession](../android/hardware/camera2/CameraDevice.md)) 

### SESSION_REGULAR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_REGULAR: Int
```

A regular session type containing instances of [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md) running at regular non high speed FPS ranges and optionally [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md) for reprocessable sessions. 

 Value: 0

**See Also**

- [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](../android/hardware/camera2/CameraDevice.md))
- [android.hardware.camera2.CameraDevice#createReprocessableCaptureSession](../android/hardware/camera2/CameraDevice.md))

## Public constructors

### SessionConfiguration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SessionConfiguration(
    sessionType: Int, 
    outputs: MutableList<OutputConfiguration!>)
```

Create a new [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md) with sessionType and output configurations.

The SessionConfiguration objects created by this constructor can be used by [CameraDeviceSetup.isSessionConfigurationSupported](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md))and [android.hardware.camera2.CameraDevice.CameraDeviceSetup#getSessionCharacteristics](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md))to query a camera device's feature combination support and session specific characteristics. For the SessionConfiguration object to be used to create a capture session, [setStateCallback](../android/hardware/camera2/params/SessionConfiguration.md))must be called to specify the state callback function, and any incomplete OutputConfigurations must be completed via [OutputConfiguration.addSurface](../android/hardware/camera2/params/OutputConfiguration.md))or [OutputConfiguration.setSurfacesForMultiResolutionOutput](../android/hardware/camera2/params/OutputConfiguration.md))as appropriate.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The session type. Value is [android.hardware.camera2.params.SessionConfiguration#SESSION_REGULAR](../android/hardware/camera2/params/SessionConfiguration.md), or [android.hardware.camera2.params.SessionConfiguration#SESSION_HIGH_SPEED](../android/hardware/camera2/params/SessionConfiguration.md) |
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md)!\>:A list of output configurations for the capture session. This value cannot be`null`. |

**See Also**

- [#SESSION_REGULAR](../android/hardware/camera2/params/SessionConfiguration.md)
- [#SESSION_HIGH_SPEED](../android/hardware/camera2/params/SessionConfiguration.md)
- [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](../android/hardware/camera2/CameraDevice.md))
- [android.hardware.camera2.CameraDevice.CameraDeviceSetup#isSessionConfigurationSupported](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md))
- [android.hardware.camera2.CameraDevice.CameraDeviceSetup#getSessionCharacteristics](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md)) 

### SessionConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SessionConfiguration(
    sessionType: Int, 
    outputs: MutableList<OutputConfiguration!>, 
    executor: Executor, 
    cb: CameraCaptureSession.StateCallback)
```

Create a new [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The session type. Value is [android.hardware.camera2.params.SessionConfiguration#SESSION_REGULAR](../android/hardware/camera2/params/SessionConfiguration.md), or [android.hardware.camera2.params.SessionConfiguration#SESSION_HIGH_SPEED](../android/hardware/camera2/params/SessionConfiguration.md) |
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md)!\>:A list of output configurations for the capture session. This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):The executor which should be used to invoke the callback. In general it is recommended that camera operations are not done on the main (UI) thread. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `cb` | [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md):A state callback interface implementation. This value cannot be`null`. |

**See Also**

- [#SESSION_REGULAR](../android/hardware/camera2/params/SessionConfiguration.md)
- [#SESSION_HIGH_SPEED](../android/hardware/camera2/params/SessionConfiguration.md)
- [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](../android/hardware/camera2/CameraDevice.md))

## Public methods

### clearColorSpace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearColorSpace(): Unit
```

Clear the color space, such that the default color space will be used. 

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md) is equal to another [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md).

Two output session configurations are only equal if and only if the underlying input configuration, output configurations, and session type are equal.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getColorSpace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getColorSpace(): ColorSpace?
```

Return the current color space.

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ColorSpace](../android/graphics/ColorSpace.md)? | the currently set color space This value may be`null`. |

### getExecutor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExecutor(): Executor!
```

Retrieve the [java.util.concurrent.Executor](../java/util/concurrent/Executor.md) for the capture session.

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Executor](../java/util/concurrent/Executor.md)! | The Executor on which the callback will be invoked. |

### getInputConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputConfiguration(): InputConfiguration!
```

Retrieve the [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md)! | The capture session input configuration. |

### getOutputConfigurations

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputConfigurations(): MutableList<OutputConfiguration!>!
```

Retrieve the [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md) list for the capture session.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md)!>! | A list of output configurations for the capture session. |

### getSessionParameters

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionParameters(): CaptureRequest!
```

Retrieve the session wide camera parameters (see [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)).

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)! | A capture request that includes the initial values for any available session wide capture keys. |

### getSessionType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionType(): Int
```

Retrieve the type of the capture session.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The capture session type. Value is [android.hardware.camera2.params.SessionConfiguration#SESSION_REGULAR](../android/hardware/camera2/params/SessionConfiguration.md), or [android.hardware.camera2.params.SessionConfiguration#SESSION_HIGH_SPEED](../android/hardware/camera2/params/SessionConfiguration.md) |

### getStateCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStateCallback(): CameraCaptureSession.StateCallback!
```

Retrieve the [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md) for the capture session.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md)! | A state callback interface implementation. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### setColorSpace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setColorSpace(colorSpace: ColorSpace.Named): Unit
```

Set a specific device-supported color space.

Clients can choose from any profile advertised as supported in [CameraCharacteristics.REQUEST_AVAILABLE_COLOR_SPACE_PROFILES](../android/hardware/camera2/CameraCharacteristics.md) queried using [ColorSpaceProfiles.getSupportedColorSpaces](../android/hardware/camera2/params/ColorSpaceProfiles.md)). When set, the colorSpace will override the default color spaces of the output targets, or the color space implied by the dataSpace passed into an [ImageReader](../android/media/ImageReader.md)'s constructor.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `colorSpace` | [ColorSpace.Named](../android/graphics/ColorSpace.Named.md):This value cannot be`null`. |

### setInputConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInputConfiguration(input: InputConfiguration): Unit
```

Sets the [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md) for a reprocessable session. Input configuration are not supported for [SESSION_HIGH_SPEED](../android/hardware/camera2/params/SessionConfiguration.md).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md):Input configuration. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | In case it is called for [SESSION_HIGH_SPEED](../android/hardware/camera2/params/SessionConfiguration.md) type session configuration. |

### setSessionParameters

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSessionParameters(params: CaptureRequest!): Unit
```

Sets the session wide camera parameters (see [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)). This argument can be set for every supported session type and will be passed to the camera device as part of the capture session initialization. Session parameters are a subset of the available capture request parameters (see [CameraCharacteristics.getAvailableSessionKeys](../android/hardware/camera2/CameraCharacteristics.md))) and their application can introduce internal camera delays. To improve camera performance it is suggested to change them sparingly within the lifetime of the capture session and to pass their initial values as part of this method.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)!:A capture request that includes the initial values for any available session wide capture keys. Tags (see [CaptureRequest.Builder.setTag](../android/hardware/camera2/CaptureRequest.Builder.md))) and output targets (see [CaptureRequest.Builder.addTarget](../android/hardware/camera2/CaptureRequest.Builder.md))) are ignored if set. Parameter values not part of [CameraCharacteristics.getAvailableSessionKeys](../android/hardware/camera2/CameraCharacteristics.md))will also be ignored. It is recommended to build the session parameters using the same template type as the initial capture request, so that the session and initial request parameters match as much as possible. |

### setStateCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setStateCallback(
    executor: Executor, 
    cb: CameraCaptureSession.StateCallback
): Unit
```

Set the state callback and executor.

This function must be called for the SessionConfiguration object created via [SessionConfiguration(int, List<OutputConfiguration>)](../android/hardware/camera2/params/SessionConfiguration.md))before it's used to create a capture session.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):The executor which should be used to invoke the callback. In general it is recommended that camera operations are not done on the main (UI) thread. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `cb` | [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md):A state callback interface implementation. This value cannot be`null`. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SessionConfiguration!>
```
