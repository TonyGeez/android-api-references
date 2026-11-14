Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExtensionSessionConfiguration

```
class ExtensionSessionConfiguration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.ExtensionSessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#) |

A class that aggregates all supported arguments for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.html#` initialization.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#ExtensionSessionConfiguration(kotlin.Int,%20kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.StateCallback)(extension: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, outputs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StateCallback.html#)` Create a new ExtensionSessionConfiguration |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#clearColorSpace()()` Clear the color space, such that the default color space will be used. |
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.html#)? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#getColorSpace()()` Return the current color space. |
| [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#getExecutor()()` Retrieve the Executor for the CameraExtensionSession instance. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#getExtension()()` Retrieve the extension type. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#getOutputConfigurations()()` Retrieve the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` list for the capture session. |
| [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#getPostviewOutputConfiguration()()` Get the postview for still capture output configuration. |
| --- | --- |
| [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#getSessionWideParams()()` Retrieve the session wide camera parameters (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#`). |
| [CameraExtensionSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StateCallback.html#) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#getStateCallback()()` Retrieve the CameraCaptureSession. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)(colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#)` Set a specific device-supported color space. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#setPostviewOutputConfiguration(android.hardware.camera2.params.OutputConfiguration)(postviewOutput: https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration?)` Set the postview for still capture output configuration. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration#setSessionWideParams(android.hardware.camera2.CaptureRequest)(sessionCaptureParams: https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#)` Sets the session wide camera parameters (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#`). |

## Public constructors

### ExtensionSessionConfiguration

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ExtensionSessionConfiguration(
    extension: Int, 
    outputs: MutableList<OutputConfiguration!>, 
    executor: Executor, 
    listener: CameraExtensionSession.StateCallback)
```

Create a new ExtensionSessionConfiguration

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): to be used for processing. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_NIGHT:kotlin.Int` |
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!\>: a list of output configurations for the capture session. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor which will be used for invoking the callbacks. This value cannot be `null`. |
| --- | --- |
| `listener` | [CameraExtensionSession.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StateCallback.html#): callbacks to be invoked when the state of the CameraExtensionSession changes. This value cannot be `null`. |

## Public methods

### clearColorSpace

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearColorSpace(): Unit
```

Clear the color space, such that the default color space will be used.

### getColorSpace

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColorSpace(): ColorSpace?
```

Return the current color space.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.html#?` | the currently set color space, or null if not set |

### getExecutor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExecutor(): Executor
```

Retrieve the Executor for the CameraExtensionSession instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` | The Executor on which the callback will be invoked. This value cannot be `null`. |

### getExtension

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtension(): Int
```

Retrieve the extension type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#EXTENSION_NIGHT:kotlin.Int` |

### getOutputConfigurations

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputConfigurations(): MutableList<OutputConfiguration!>
```

Retrieve the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` list for the capture session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration!>` | A list of output configurations for the capture session. This value cannot be `null`. |

### getPostviewOutputConfiguration

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPostviewOutputConfiguration(): OutputConfiguration?
```

Get the postview for still capture output configuration.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration?` | output configuration for postview. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#isPostviewAvailable(kotlin.Int)`

### getSessionWideParams

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSessionWideParams(): CaptureRequest?
```

Retrieve the session wide camera parameters (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#`).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#?` | A capture request that includes the initial values for any available session wide capture keys. This value may be `null`. |

### getStateCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStateCallback(): CameraExtensionSession.StateCallback
```

Retrieve the CameraCaptureSession.StateCallback listener.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StateCallback.html#` | A state callback interface implementation. This value cannot be `null`. |

### setColorSpace

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setColorSpace(colorSpace: ColorSpace.Named): Unit
```

Set a specific device-supported color space.

Clients can choose from any profile advertised as supported in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#REQUEST_AVAILABLE_COLOR_SPACE_PROFILES:android.hardware.camera2.CameraCharacteristics.Key` queried using `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpaces(kotlin.Int)`. When set, the colorSpace will override the default color spaces of the output targets, or the color space implied by the dataSpace passed into an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#`'s constructor.

| Parameters ||
|---|---|
| `colorSpace` | [ColorSpace.Named](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#): This value cannot be `null`. |

### setPostviewOutputConfiguration

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPostviewOutputConfiguration(postviewOutput: OutputConfiguration?): Unit
```

Set the postview for still capture output configuration.

| Parameters ||
|---|---|
| `postviewOutput` | [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)?: output configuration for postview. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics.html#isPostviewAvailable(kotlin.Int)`

### setSessionWideParams

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSessionWideParams(sessionCaptureParams: CaptureRequest): Unit
```

Sets the session wide camera parameters (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#`). This argument can be set for every supported session type and will be passed to the camera device as part of the capture session initialization. Session parameters are a subset of the available capture request parameters (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#getAvailableSessionKeys()`) and their application can introduce internal camera delays. To improve camera performance it is suggested to change them sparingly within the lifetime of the capture session and to pass their initial values as part of this method.

| Parameters ||
|---|---|
| `sessionCaptureParams` | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#): A capture request that includes the initial values for any available session wide capture keys. Tags (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder.html#setTag(kotlin.Any)`) and output targets (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder.html#addTarget(android.view.Surface)`) are ignored if set. Parameter values not part of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#getAvailableSessionKeys()` will also be ignored. It is recommended to build the session parameters using the same template type as the initial capture request, so that the session and initial request parameters match as much as possible. This value cannot be `null`. |
