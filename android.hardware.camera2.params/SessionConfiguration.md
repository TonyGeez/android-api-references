# SessionConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SessionConfiguration

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/params/SessionConfiguration "View this page in Java") 
| --- | --- |

```
class SessionConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#) |

A helper class that aggregates all supported arguments for capture session initialization.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_HIGH_SPEED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int) A high speed session type that can only contain instances of [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_REGULAR](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_REGULAR:kotlin.Int) A regular session type containing instances of [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration) running at regular non high speed FPS ranges and optionally [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration) for reprocessable sessions. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SessionConfiguration(kotlin.Int,%20kotlin.collections.MutableList))`(`sessionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outputs:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!>`)` Create a new [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#) with sessionType and output configurations. |
| [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SessionConfiguration(kotlin.Int,%20kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraCaptureSession.StateCallback))`(`sessionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outputs:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!>`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `cb:` ` [CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#)`)` Create a new [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#). |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearColorSpace](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#clearColorSpace())`()` Clear the color space, such that the default color space will be used. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#) is equal to another [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#). |
| --- | --- |
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.html#)? | [getColorSpace](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#getColorSpace())`()` Return the current color space. |
| [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)! | [getExecutor](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#getExecutor())`()` Retrieve the [java.util.concurrent.Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) for the capture session. |
| [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration)! | [getInputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#getInputConfiguration())`()` Retrieve the [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration). |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!\>! | [getOutputConfigurations](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#getOutputConfigurations())`()` Retrieve the [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration) list for the capture session. |
| [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)! | [getSessionParameters](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#getSessionParameters())`()` Retrieve the session wide camera parameters (see [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSessionType](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#getSessionType())`()` Retrieve the type of the capture session. |
| --- | --- |
| [CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#)! | [getStateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#getStateCallback())`()` Retrieve the [CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#) for the capture session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#hashCode())`()` Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColorSpace](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named))`(`colorSpace:` ` [ColorSpace.Named](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#)`)` Set a specific device-supported color space. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setInputConfiguration(android.hardware.camera2.params.InputConfiguration))`(`input:` ` [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration)`)` Sets the [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration) for a reprocessable session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSessionParameters](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest))`(`params:` ` [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)!`)` Sets the session wide camera parameters (see [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setStateCallback(java.util.concurrent.Executor,%20android.hardware.camera2.CameraCaptureSession.StateCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `cb:` ` [CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#)`)` Set the state callback and executor. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### SESSION_HIGH_SPEED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_HIGH_SPEED: Int
```

A high speed session type that can only contain instances of [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration). The outputs can run using high speed FPS ranges. Calls to [setInputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setInputConfiguration(android.hardware.camera2.params.InputConfiguration))are not supported.

When using this type, the CameraCaptureSession returned by [android.hardware.camera2.CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#) can be cast to a [android.hardware.camera2.CameraConstrainedHighSpeedCaptureSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.html#) to access the extra methods for constrained high speed recording. 

 Value: 1

**See Also**

- [android.hardware.camera2.CameraDevice#createConstrainedHighSpeedCaptureSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)) 

### SESSION_REGULAR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_REGULAR: Int
```

A regular session type containing instances of [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration) running at regular non high speed FPS ranges and optionally [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration) for reprocessable sessions. 

 Value: 0

**See Also**

- [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration))
- [android.hardware.camera2.CameraDevice#createReprocessableCaptureSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler))

## Public constructors

### SessionConfiguration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SessionConfiguration(
    sessionType: Int, 
    outputs: MutableList<OutputConfiguration!>)
```

Create a new [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#) with sessionType and output configurations.

The SessionConfiguration objects created by this constructor can be used by [CameraDeviceSetup.isSessionConfigurationSupported](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup.html#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration))and [android.hardware.camera2.CameraDevice.CameraDeviceSetup#getSessionCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup.html#getSessionCharacteristics(android.hardware.camera2.params.SessionConfiguration))to query a camera device's feature combination support and session specific characteristics. For the SessionConfiguration object to be used to create a capture session, [setStateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setStateCallback(java.util.concurrent.Executor,%20android.hardware.camera2.CameraCaptureSession.StateCallback))must be called to specify the state callback function, and any incomplete OutputConfigurations must be completed via [OutputConfiguration.addSurface](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#addSurface(android.view.Surface))or [OutputConfiguration.setSurfacesForMultiResolutionOutput](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setSurfacesForMultiResolutionOutput(kotlin.collections.MutableCollection,%20android.hardware.camera2.MultiResolutionImageReader))as appropriate.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The session type. Value is [android.hardware.camera2.params.SessionConfiguration#SESSION_REGULAR](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_REGULAR:kotlin.Int), or [android.hardware.camera2.params.SessionConfiguration#SESSION_HIGH_SPEED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int) |
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!\>:A list of output configurations for the capture session. This value cannot be`null`. |

**See Also**

- [#SESSION_REGULAR](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_REGULAR:kotlin.Int)
- [#SESSION_HIGH_SPEED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int)
- [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration))
- [android.hardware.camera2.CameraDevice.CameraDeviceSetup#isSessionConfigurationSupported](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup.html#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration))
- [android.hardware.camera2.CameraDevice.CameraDeviceSetup#getSessionCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup.html#getSessionCharacteristics(android.hardware.camera2.params.SessionConfiguration)) 

### SessionConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SessionConfiguration(
    sessionType: Int, 
    outputs: MutableList<OutputConfiguration!>, 
    executor: Executor, 
    cb: CameraCaptureSession.StateCallback)
```

Create a new [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The session type. Value is [android.hardware.camera2.params.SessionConfiguration#SESSION_REGULAR](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_REGULAR:kotlin.Int), or [android.hardware.camera2.params.SessionConfiguration#SESSION_HIGH_SPEED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int) |
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!\>:A list of output configurations for the capture session. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor which should be used to invoke the callback. In general it is recommended that camera operations are not done on the main (UI) thread. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| --- | --- |
| `cb` | [CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#):A state callback interface implementation. This value cannot be`null`. |

**See Also**

- [#SESSION_REGULAR](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_REGULAR:kotlin.Int)
- [#SESSION_HIGH_SPEED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int)
- [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration))

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#) is equal to another [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#).

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
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.html#)? | the currently set color space This value may be`null`. |

### getExecutor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExecutor(): Executor!
```

Retrieve the [java.util.concurrent.Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) for the capture session.

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)! | The Executor on which the callback will be invoked. |

### getInputConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputConfiguration(): InputConfiguration!
```

Retrieve the [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration)! | The capture session input configuration. |

### getOutputConfigurations

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputConfigurations(): MutableList<OutputConfiguration!>!
```

Retrieve the [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration) list for the capture session.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!>! | A list of output configurations for the capture session. |

### getSessionParameters

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionParameters(): CaptureRequest!
```

Retrieve the session wide camera parameters (see [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)).

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)! | A capture request that includes the initial values for any available session wide capture keys. |

### getSessionType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionType(): Int
```

Retrieve the type of the capture session.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The capture session type. Value is [android.hardware.camera2.params.SessionConfiguration#SESSION_REGULAR](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_REGULAR:kotlin.Int), or [android.hardware.camera2.params.SessionConfiguration#SESSION_HIGH_SPEED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int) |

### getStateCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStateCallback(): CameraCaptureSession.StateCallback!
```

Retrieve the [CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#) for the capture session.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#)! | A state callback interface implementation. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setColorSpace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setColorSpace(colorSpace: ColorSpace.Named): Unit
```

Set a specific device-supported color space.

Clients can choose from any profile advertised as supported in [CameraCharacteristics.REQUEST_AVAILABLE_COLOR_SPACE_PROFILES](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#REQUEST_AVAILABLE_COLOR_SPACE_PROFILES:android.hardware.camera2.CameraCharacteristics.Key) queried using [ColorSpaceProfiles.getSupportedColorSpaces](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpaces(kotlin.Int)). When set, the colorSpace will override the default color spaces of the output targets, or the color space implied by the dataSpace passed into an [ImageReader](https://developer.android.com/reference/kotlin/android/media/ImageReader.html#)'s constructor.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `colorSpace` | [ColorSpace.Named](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#):This value cannot be`null`. |

### setInputConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInputConfiguration(input: InputConfiguration): Unit
```

Sets the [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration) for a reprocessable session. Input configuration are not supported for [SESSION_HIGH_SPEED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration):Input configuration. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | In case it is called for [SESSION_HIGH_SPEED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int) type session configuration. |

### setSessionParameters

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSessionParameters(params: CaptureRequest!): Unit
```

Sets the session wide camera parameters (see [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)). This argument can be set for every supported session type and will be passed to the camera device as part of the capture session initialization. Session parameters are a subset of the available capture request parameters (see [CameraCharacteristics.getAvailableSessionKeys](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#getAvailableSessionKeys())) and their application can introduce internal camera delays. To improve camera performance it is suggested to change them sparingly within the lifetime of the capture session and to pass their initial values as part of this method.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)!:A capture request that includes the initial values for any available session wide capture keys. Tags (see [CaptureRequest.Builder.setTag](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder.html#setTag(kotlin.Any))) and output targets (see [CaptureRequest.Builder.addTarget](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder.html#addTarget(android.view.Surface))) are ignored if set. Parameter values not part of [CameraCharacteristics.getAvailableSessionKeys](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#getAvailableSessionKeys())will also be ignored. It is recommended to build the session parameters using the same template type as the initial capture request, so that the session and initial request parameters match as much as possible. |

### setStateCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setStateCallback(
    executor: Executor, 
    cb: CameraCaptureSession.StateCallback
): Unit
```

Set the state callback and executor.

This function must be called for the SessionConfiguration object created via [SessionConfiguration(int, List<OutputConfiguration>)](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SessionConfiguration(kotlin.Int,%20kotlin.collections.MutableList))before it's used to create a capture session.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor which should be used to invoke the callback. In general it is recommended that camera operations are not done on the main (UI) thread. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `cb` | [CameraCaptureSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback.html#):A state callback interface implementation. This value cannot be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SessionConfiguration!>
```
