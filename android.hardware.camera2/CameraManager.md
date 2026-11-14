# CameraManager

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraManager

Kotlin | [Java](https://developer.android.com/reference/android/hardware/camera2/CameraManager "View this page in Java") 
| --- | --- |

```
class CameraManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.CameraManager](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#) |

A system service manager for detecting, characterizing, and connecting to [CameraDevices](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice).

For more details about communicating with camera devices, read the Camera developer guide or the [camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) package documentation.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback) A callback for camera devices becoming available or unavailable to open. |
| abstract | [TorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback) A callback for camera flash torch modes becoming unavailable, disabled, or enabled. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics) | [getCameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query the capabilities of a camera device. |
| [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) | [getCameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraDeviceSetup(kotlin.String))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) object for the given `cameraId`, which provides limited access to CameraDevice setup and query functionality without requiring an #openCamera call. |
| [CameraExtensionCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics) | [getCameraExtensionCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraExtensionCharacteristics(kotlin.String))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query the camera extension capabilities of a camera device. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList())`()` Return the list of currently connected camera devices by identifier, including cameras that may be in use by other camera API clients. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | [getConcurrentCameraIds](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getConcurrentCameraIds())`()` Return the set of combinations of currently connected camera device identifiers, which support configuring camera device sessions concurrently. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTorchStrengthLevel](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getTorchStrengthLevel(kotlin.String))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the brightness level of the flash unit associated with the cameraId. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCameraDeviceSetupSupported](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#isCameraDeviceSetupSupported(kotlin.String))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Checks a Camera Device's characteristics to ensure that a [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) instance can be constructed for a given `cameraId`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConcurrentSessionConfigurationSupported](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#isConcurrentSessionConfigurationSupported(kotlin.collections.MutableMap))`(`cameraIdAndSessionConfig:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration)!>`)` Checks whether the provided set of camera devices and their corresponding [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration) can be configured concurrently. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openCamera](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#openCamera(kotlin.String,%20android.hardware.camera2.CameraDevice.StateCallback,%20android.os.Handler))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `callback:` ` [CameraDevice.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Open a connection to a camera with the given ID. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openCamera](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#openCamera(kotlin.String,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraDevice.StateCallback))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [CameraDevice.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback)`)` Open a connection to a camera with the given ID. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#registerAvailabilityCallback(android.hardware.camera2.CameraManager.AvailabilityCallback,%20android.os.Handler))`(`callback:` ` [CameraManager.AvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Register a callback to be notified about camera device availability. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#registerAvailabilityCallback(java.util.concurrent.Executor,%20android.hardware.camera2.CameraManager.AvailabilityCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [CameraManager.AvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback)`)` Register a callback to be notified about camera device availability. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerTorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#registerTorchCallback(android.hardware.camera2.CameraManager.TorchCallback,%20android.os.Handler))`(`callback:` ` [CameraManager.TorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Register a callback to be notified about torch mode status. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerTorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#registerTorchCallback(java.util.concurrent.Executor,%20android.hardware.camera2.CameraManager.TorchCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [CameraManager.TorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback)`)` Register a callback to be notified about torch mode status. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTorchMode](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#setTorchMode(kotlin.String,%20kotlin.Boolean))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the flash unit's torch mode of the camera of the given ID without opening the camera device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [turnOnTorchWithStrengthLevel](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#turnOnTorchWithStrengthLevel(kotlin.String,%20kotlin.Int))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `torchStrength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the brightness level of the flashlight associated with the given cameraId in torch mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#unregisterAvailabilityCallback(android.hardware.camera2.CameraManager.AvailabilityCallback))`(`callback:` ` [CameraManager.AvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback)`)` Remove a previously-added callback; the callback will no longer receive connection and disconnection callbacks. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterTorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#unregisterTorchCallback(android.hardware.camera2.CameraManager.TorchCallback))`(`callback:` ` [CameraManager.TorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback)`)` Remove a previously-added callback; the callback will no longer receive torch mode status callbacks. |
| --- | --- |

## Public methods

### getCameraCharacteristics

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCameraCharacteristics(cameraId: String): CameraCharacteristics
```

Query the capabilities of a camera device. These capabilities are immutable for a given camera.

From API level 29, this function can also be used to query the capabilities of physical cameras that can only be used as part of logical multi-camera. These cameras cannot be opened directly via #openCamera

Also starting with API level 29, while most basic camera information is still available even without the CAMERA permission, some values are not available to apps that do not hold that permission. The keys not available are listed by [CameraCharacteristics.getKeysNeedingPermission](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getKeysNeedingPermission()).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The id of the camera device to query. This could be either a standalone camera ID which can be directly opened by #openCamera, or a physical camera ID that can only used as part of a logical multi-camera. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [CameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics) | The properties of the given camera This value cannot be `null`. |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the cameraId does not match any known camera device. |
| `android.hardware.camera2.CameraAccessException` | if the camera device has been disconnected. |

**See Also**

- [#getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList())
- [android.app.admin.DevicePolicyManager#setCameraDisabled](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setCameraDisabled(android.content.ComponentName,%20kotlin.Boolean)) 

### getCameraDeviceSetup

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCameraDeviceSetup(cameraId: String): CameraDevice.CameraDeviceSetup
```

Returns a [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) object for the given `cameraId`, which provides limited access to CameraDevice setup and query functionality without requiring an #openCamera call. The [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) can later be obtained either by calling #openCamera, or [CameraDevice.CameraDeviceSetup.openCamera](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#openCamera(java.util.concurrent.Executor,%20android.hardware.camera2.CameraDevice.StateCallback)).

Support for [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) for a given `cameraId` must be checked with [isCameraDeviceSetupSupported](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#isCameraDeviceSetupSupported(kotlin.String)). If `isCameraDeviceSetupSupported` returns `false` for a `cameraId`, this method will throw an [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#)

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device for which [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) object must be constructed. This identifier must be present in [getCameraIdList()](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()) This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) | [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) object corresponding to the provided `cameraId` This value cannot be `null`. |

| Exceptions ||
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If `cameraId` is null, or if `cameraId` does not match any device in [getCameraIdList()](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()). |
| `android.hardware.camera2.CameraAccessException` | if the camera device is not accessible |
| `java.lang.UnsupportedOperationException` | if [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) instance cannot be constructed for the given `cameraId`, i.e. [isCameraDeviceSetupSupported](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#isCameraDeviceSetupSupported(kotlin.String)) returns false. |
| --- | --- |

**See Also**

- [android.hardware.camera2.CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup)
- <https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()> 

### getCameraExtensionCharacteristics

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCameraExtensionCharacteristics(cameraId: String): CameraExtensionCharacteristics
```

Query the camera extension capabilities of a camera device.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The id of the camera device to query. This must be a standalone camera ID which can be directly opened by #openCamera. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [CameraExtensionCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics) | The properties of the given camera This value cannot be `null`. |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the cameraId does not match any known camera device. |
| `android.hardware.camera2.CameraAccessException` | if the camera device has been disconnected. |

**See Also**

- [android.hardware.camera2.CameraExtensionCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics)
- [android.hardware.camera2.CameraDevice#createExtensionSession(ExtensionSessionConfiguration)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createExtensionSession(android.hardware.camera2.params.ExtensionSessionConfiguration))
- [android.hardware.camera2.CameraExtensionSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession) 

### getCameraIdList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCameraIdList(): Array<String!>
```

Return the list of currently connected camera devices by identifier, including cameras that may be in use by other camera API clients.

Non-removable cameras use integers starting at 0 for their identifiers, while removable cameras have a unique identifier for each individual device, even if they are the same model.

This list doesn't contain physical cameras that can only be used as part of a logical multi-camera device.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The list of currently connected camera devices. This value cannot be `null`. |

### getConcurrentCameraIds

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConcurrentCameraIds(): MutableSet<MutableSet<String!>!>
```

Return the set of combinations of currently connected camera device identifiers, which support configuring camera device sessions concurrently.

The devices in these combinations can be concurrently configured by the same client camera application. Using these camera devices concurrently by two different applications is not guaranteed to be supported, however.

For concurrent operation, in chronological order :

- Applications must first close any open cameras that have sessions configured, using [CameraDevice.close](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#close()).
- All camera devices intended to be operated concurrently, must be opened using #openCamera, before configuring sessions on any of the camera devices.

<br />

Each device in a combination, is guaranteed to support stream combinations which may be obtained by querying [getCameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)) for the key [android.hardware.camera2.CameraCharacteristics#SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key).

For concurrent operation, if a camera device has a non null zoom ratio range as specified by [android.hardware.camera2.CameraCharacteristics#CONTROL_ZOOM_RATIO_RANGE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_ZOOM_RATIO_RANGE:android.hardware.camera2.CameraCharacteristics.Key), its complete zoom ratio range may not apply. Applications can use [android.hardware.camera2.CaptureRequest#CONTROL_ZOOM_RATIO](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key) \>=1 and \<= [android.hardware.camera2.CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM:android.hardware.camera2.CameraCharacteristics.Key) during concurrent operation.

The set of combinations may include camera devices that may be in use by other camera API clients.

Concurrent camera extension sessions [CameraExtensionSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession) are not currently supported.

The set of combinations doesn't contain physical cameras that can only be used as part of a logical multi-camera device.

If a new camera id becomes available through [AvailabilityCallback.onCameraUnavailable(String)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onCameraUnavailable(kotlin.String)), clients can call this method to check if new combinations of camera ids which can stream concurrently are available.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!> | The set of combinations of currently connected camera devices, that may have sessions configured concurrently. The set of combinations will be empty if no such combinations are supported by the camera subsystem. |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera device has been disconnected. |

### getTorchStrengthLevel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTorchStrengthLevel(cameraId: String): Int
```

Returns the brightness level of the flash unit associated with the cameraId.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device that the flash unit belongs to. This value cannot be `null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The brightness level of the flash unit associated with cameraId. When the torch is turned OFF, the strength level will reset to a default level [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key). In this case the return value will be [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key) rather than 0. |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if it failed to access the flash unit. |
| `java.lang.IllegalArgumentException` | if cameraId was null, cameraId doesn't match any currently or previously available camera device, or the camera device doesn't have a flash unit. |

### isCameraDeviceSetupSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCameraDeviceSetupSupported(cameraId: String): Boolean
```

Checks a Camera Device's characteristics to ensure that a [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) instance can be constructed for a given `cameraId`. If this method returns false for a `cameraId`, calling [getCameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraDeviceSetup(kotlin.String)) for that `cameraId` will throw an [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#).

[CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) is supported for all devices that report [CameraCharacteristics.INFO_SESSION_CONFIGURATION_QUERY_VERSION](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SESSION_CONFIGURATION_QUERY_VERSION:android.hardware.camera2.CameraCharacteristics.Key) \> [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device for which [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) support is being queried. This identifier must be present in [getCameraIdList()](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()). This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if [CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup) object can be constructed for the provided `cameraId`; `false` otherwise. |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If `cameraId` is null, or if `cameraId` does not match any device in [getCameraIdList()](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()). |
| `android.hardware.camera2.CameraAccessException` | if the camera device is not accessible |

**See Also**

- [android.hardware.camera2.CameraCharacteristics#INFO_SESSION_CONFIGURATION_QUERY_VERSION](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SESSION_CONFIGURATION_QUERY_VERSION:android.hardware.camera2.CameraCharacteristics.Key)
- [android.hardware.camera2.CameraDevice.CameraDeviceSetup](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup)
- [#getCameraDeviceSetup(String)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraDeviceSetup(kotlin.String))
- <https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()> 

### isConcurrentSessionConfigurationSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConcurrentSessionConfigurationSupported(cameraIdAndSessionConfig: MutableMap<String!, SessionConfiguration!>): Boolean
```

Checks whether the provided set of camera devices and their corresponding [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration) can be configured concurrently.

This method performs a runtime check of the given [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration) and camera id combinations. The result confirms whether or not the passed session configurations can be successfully used to create camera capture sessions concurrently, on the given camera devices using [CameraDevice.createCaptureSession(SessionConfiguration)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)).

The method can be called at any point before, during and after active capture sessions. It will not impact normal camera behavior in any way and must complete significantly faster than creating a regular or constrained capture session.

Although this method is faster than creating a new capture session, it is not intended to be used for exploring the entire space of supported concurrent stream combinations. The available mandatory concurrent stream combinations may be obtained by querying [getCameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)) for the key [android.hardware.camera2.CameraCharacteristics#SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key).

Note that session parameters will be ignored and calls to [SessionConfiguration.setSessionParameters](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest)) are not required.

Requires [android.Manifest.permission#CAMERA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String)

| Parameters ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraIdAndSessionConfig` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration)!\>: This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the given combination of session configurations and corresponding camera ids are concurrently supported by the camera sub-system, `false` otherwise OR if the set of camera devices provided is not a subset of those returned by [getConcurrentCameraIds](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getConcurrentCameraIds()). |

| Exceptions ||
|--------------------------------------------------|--------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if one of the camera devices queried is no longer connected. |

### openCamera

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openCamera(
    cameraId: String, 
    callback: CameraDevice.StateCallback, 
    handler: Handler?
): Unit
```

Open a connection to a camera with the given ID.

Use [getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()) to get the list of available camera devices. Note that even if an id is listed, open may fail if the device is disconnected between the calls to [getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()) and #openCamera, or if a higher-priority camera API client begins using the camera device.

As of API level 23, devices for which the [AvailabilityCallback.onCameraUnavailable(String)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onCameraUnavailable(kotlin.String)) callback has been called due to the device being in use by a lower-priority, background camera API client can still potentially be opened by calling this method when the calling camera API client has a higher priority than the current camera API client using this device. In general, if the top, foreground activity is running within your application process, your process will be given the highest priority when accessing the camera, and this method will succeed even if the camera device is in use by another camera API client. Any lower-priority application that loses control of the camera in this way will receive an [android.hardware.camera2.CameraDevice.StateCallback#onDisconnected](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onDisconnected(android.hardware.camera2.CameraDevice)) callback. Opening the same camera ID twice in the same application will similarly cause the [android.hardware.camera2.CameraDevice.StateCallback#onDisconnected](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onDisconnected(android.hardware.camera2.CameraDevice)) callback being fired for the [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) from the first open call and all ongoing tasks being dropped.

Once the camera is successfully opened, [CameraDevice.StateCallback.onOpened](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onOpened(android.hardware.camera2.CameraDevice)) will be invoked with the newly opened [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice). The camera device can then be set up for operation by calling android.hardware.camera2.CameraDevice#createCaptureSession and android.hardware.camera2.CameraDevice#createCaptureRequest

Before API level 30, when the application tries to open multiple [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) of different IDs and the device does not support opening such combination, either the #openCamera will fail and throw a [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException) or one or more of already opened [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) will be disconnected and receive [android.hardware.camera2.CameraDevice.StateCallback#onDisconnected](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onDisconnected(android.hardware.camera2.CameraDevice)) callback. Which behavior will happen depends on the device implementation and can vary on different devices. Starting in API level 30, if the device does not support the combination of cameras being opened, it is guaranteed the #openCamera call will fail and none of existing [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) will be disconnected.

If the camera becomes disconnected during initialization after this function call returns, [CameraDevice.StateCallback.onDisconnected](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onDisconnected(android.hardware.camera2.CameraDevice)) with a [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) in the disconnected state (and [CameraDevice.StateCallback.onOpened](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onOpened(android.hardware.camera2.CameraDevice)) will be skipped).

If opening the camera device fails, then the device callback's [onError](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onError(android.hardware.camera2.CameraDevice,%20kotlin.Int)) method will be called, and subsequent calls on the camera device will throw a [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException).

Requires [android.Manifest.permission#CAMERA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device to open This value cannot be `null`. |
| `callback` | [CameraDevice.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback): The callback which is invoked once the camera is opened This value cannot be `null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: The handler on which the callback should be invoked, or `null` to use the current thread's [looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#). |
| --- | --- |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera is disabled by device policy, has been disconnected, is being used by a higher-priority camera API client, or the device has reached its maximal resource and cannot open this camera device. |
| `java.lang.IllegalArgumentException` | if cameraId or the callback was null, or the cameraId does not match any currently or previously available camera device returned by [getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()). |
| `java.lang.SecurityException` | if the application does not have permission to access the camera |
| --- | --- |

**See Also**

- [#getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList())
- [android.app.admin.DevicePolicyManager#setCameraDisabled](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setCameraDisabled(android.content.ComponentName,%20kotlin.Boolean)) 

### openCamera

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openCamera(
    cameraId: String, 
    executor: Executor, 
    callback: CameraDevice.StateCallback
): Unit
```

Open a connection to a camera with the given ID.

The behavior of this method matches that of [openCamera(java.lang.String,android.hardware.camera2.CameraDevice.StateCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#openCamera(kotlin.String,%20android.hardware.camera2.CameraDevice.StateCallback,%20android.os.Handler)), except that it uses [java.util.concurrent.Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) as an argument instead of [android.os.Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#).

Do note that typically callbacks are expected to be dispatched by the executor in a single thread. If the executor uses two or more threads to dispatch callbacks, then clients must ensure correct synchronization and must also be able to handle potentially different ordering of the incoming callbacks.

Requires [android.Manifest.permission#CAMERA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device to open This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor which will be used when invoking the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [CameraDevice.StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback): The callback which is invoked once the camera is opened This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera is disabled by device policy, has been disconnected, or is being used by a higher-priority camera API client. |
| `java.lang.IllegalArgumentException` | if cameraId, the callback or the executor was null, or the cameraId does not match any currently or previously available camera device. |
| `java.lang.SecurityException` | if the application does not have permission to access the camera |
| --- | --- |

**See Also**

- [#getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList())
- [android.app.admin.DevicePolicyManager#setCameraDisabled](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setCameraDisabled(android.content.ComponentName,%20kotlin.Boolean)) 

### registerAvailabilityCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerAvailabilityCallback(
    callback: CameraManager.AvailabilityCallback, 
    handler: Handler?
): Unit
```

Register a callback to be notified about camera device availability.

Registering the same callback again will replace the handler with the new one provided.

The first time a callback is registered, it is immediately called with the availability status of all currently known camera devices.

[AvailabilityCallback.onCameraUnavailable(String)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onCameraUnavailable(kotlin.String)) will be called whenever a camera device is opened by any camera API client. As of API level 23, other camera API clients may still be able to open such a camera device, evicting the existing client if they have higher priority than the existing client of a camera device. See open() for more details.

Since this callback will be registered with the camera service, remember to unregister it once it is no longer needed; otherwise the callback will continue to receive events indefinitely and it may prevent other resources from being released. Specifically, the callbacks will be invoked independently of the general activity lifecycle and independently of the state of individual CameraManager instances.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [CameraManager.AvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback): the new callback to send camera availability notices to This value cannot be `null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: The handler on which the callback should be invoked, or `null` to use the current thread's [looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#). |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the handler is `null` but the current thread has no looper. |

### registerAvailabilityCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerAvailabilityCallback(
    executor: Executor, 
    callback: CameraManager.AvailabilityCallback
): Unit
```

Register a callback to be notified about camera device availability.

The behavior of this method matches that of [registerAvailabilityCallback(android.hardware.camera2.CameraManager.AvailabilityCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#registerAvailabilityCallback(android.hardware.camera2.CameraManager.AvailabilityCallback,%20android.os.Handler)), except that it uses [java.util.concurrent.Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) as an argument instead of [android.os.Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#).

Note: If the order between some availability callbacks matters, the implementation of the executor should handle those callbacks in the same thread to maintain the callbacks' order. Some examples are:

- [AvailabilityCallback.onCameraAvailable](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onCameraAvailable(kotlin.String)) and [AvailabilityCallback.onCameraUnavailable](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onCameraUnavailable(kotlin.String)) of the same camera ID.
- [AvailabilityCallback.onCameraAvailable](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onCameraAvailable(kotlin.String)) or [AvailabilityCallback.onCameraUnavailable](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onCameraUnavailable(kotlin.String)) of a logical multi-camera, and [android.hardware.camera2.CameraManager.AvailabilityCallback#onPhysicalCameraUnavailable](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onPhysicalCameraUnavailable(kotlin.String,%20kotlin.String)) or [AvailabilityCallback.onPhysicalCameraAvailable](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onPhysicalCameraAvailable(kotlin.String,%20kotlin.String)) of its physical cameras.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor which will be used to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [CameraManager.AvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback): the new callback to send camera availability notices to This value cannot be `null`. |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the executor is `null`. |

### registerTorchCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerTorchCallback(
    callback: CameraManager.TorchCallback, 
    handler: Handler?
): Unit
```

Register a callback to be notified about torch mode status.

Registering the same callback again will replace the handler with the new one provided.

The first time a callback is registered, it is immediately called with the torch mode status of all currently known camera devices with a flash unit.

Since this callback will be registered with the camera service, remember to unregister it once it is no longer needed; otherwise the callback will continue to receive events indefinitely and it may prevent other resources from being released. Specifically, the callbacks will be invoked independently of the general activity lifecycle and independently of the state of individual CameraManager instances.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [CameraManager.TorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback): The new callback to send torch mode status to This value cannot be `null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: The handler on which the callback should be invoked, or `null` to use the current thread's [looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#). |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the handler is `null` but the current thread has no looper. |

### registerTorchCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerTorchCallback(
    executor: Executor, 
    callback: CameraManager.TorchCallback
): Unit
```

Register a callback to be notified about torch mode status.

The behavior of this method matches that of [registerTorchCallback(android.hardware.camera2.CameraManager.TorchCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#registerTorchCallback(android.hardware.camera2.CameraManager.TorchCallback,%20android.os.Handler)), except that it uses [java.util.concurrent.Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) as an argument instead of [android.os.Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor which will be used to invoke the callback This value cannot be `null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [CameraManager.TorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback): The new callback to send torch mode status to This value cannot be `null`. |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the executor is `null`. |

### setTorchMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTorchMode(
    cameraId: String, 
    enabled: Boolean
): Unit
```

Set the flash unit's torch mode of the camera of the given ID without opening the camera device.

Use [getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()) to get the list of available camera devices and use [getCameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)) to check whether the camera device has a flash unit. Note that even if a camera device has a flash unit, turning on the torch mode may fail if the camera device or other camera resources needed to turn on the torch mode are in use.

If [setTorchMode](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#setTorchMode(kotlin.String,%20kotlin.Boolean)) is called to turn on or off the torch mode successfully, [CameraManager.TorchCallback.onTorchModeChanged](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback#onTorchModeChanged(kotlin.String,%20kotlin.Boolean)) will be invoked. However, even if turning on the torch mode is successful, the application does not have the exclusive ownership of the flash unit or the camera device. The torch mode will be turned off and becomes unavailable when the camera device that the flash unit belongs to becomes unavailable or when other camera resources to keep the torch on become unavailable ( [CameraManager.TorchCallback.onTorchModeUnavailable](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback#onTorchModeUnavailable(kotlin.String)) will be invoked). Also, other applications are free to call [setTorchMode](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#setTorchMode(kotlin.String,%20kotlin.Boolean)) to turn off the torch mode ( [CameraManager.TorchCallback.onTorchModeChanged](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback#onTorchModeChanged(kotlin.String,%20kotlin.Boolean)) will be invoked). If the latest application that turned on the torch mode exits, the torch mode will be turned off.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device that the flash unit belongs to. This value cannot be `null`. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The desired state of the torch mode for the target camera device. Set to `true` to turn on the torch mode. Set to `false` to turn off the torch mode. |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if it failed to access the flash unit. [CameraAccessException.CAMERA_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_IN_USE:kotlin.Int) will be thrown if the camera device is in use. [CameraAccessException.MAX_CAMERAS_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#MAX_CAMERAS_IN_USE:kotlin.Int) will be thrown if other camera resources needed to turn on the torch mode are in use. [CameraAccessException.CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int) will be thrown if camera service is not available. |
| `java.lang.IllegalArgumentException` | if cameraId was null, cameraId doesn't match any currently or previously available camera device, or the camera device doesn't have a flash unit. |

### turnOnTorchWithStrengthLevel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun turnOnTorchWithStrengthLevel(
    cameraId: String, 
    torchStrength: Int
): Unit
```

Set the brightness level of the flashlight associated with the given cameraId in torch mode. If the torch is OFF and torchStrength is \>= 1, torch will turn ON with the strength level specified in torchStrength.

Use [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL:android.hardware.camera2.CameraCharacteristics.Key) to check whether the camera device supports flash unit strength control or not. If this value is greater than 1, applications can call this API to control the flashlight brightness level.

If [turnOnTorchWithStrengthLevel](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#turnOnTorchWithStrengthLevel(kotlin.String,%20kotlin.Int)) is called to change the brightness level of the flash unit [CameraManager.TorchCallback.onTorchStrengthLevelChanged](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback#onTorchStrengthLevelChanged(kotlin.String,%20kotlin.Int)) will be invoked. If the new desired strength level is same as previously set level, then this callback will not be invoked. If the torch is OFF and [turnOnTorchWithStrengthLevel](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#turnOnTorchWithStrengthLevel(kotlin.String,%20kotlin.Int)) is called with level \>= 1, the torch will be turned ON with that brightness level. In this case [CameraManager.TorchCallback.onTorchModeChanged](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback#onTorchModeChanged(kotlin.String,%20kotlin.Boolean)) will also be invoked.

When the torch is turned OFF via [setTorchMode](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#setTorchMode(kotlin.String,%20kotlin.Boolean)), the flashlight brightness level will reset to default value [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key) In this case the [CameraManager.TorchCallback.onTorchStrengthLevelChanged](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback#onTorchStrengthLevelChanged(kotlin.String,%20kotlin.Int)) will not be invoked.

If torch is enabled via [setTorchMode](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#setTorchMode(kotlin.String,%20kotlin.Boolean)) after calling [turnOnTorchWithStrengthLevel](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#turnOnTorchWithStrengthLevel(kotlin.String,%20kotlin.Int)) with level N then the flash unit will have the brightness level N. Since multiple applications are free to call [setTorchMode](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#setTorchMode(kotlin.String,%20kotlin.Boolean)), when the latest application that turned ON the torch mode exits, the torch mode will be turned OFF and in this case the brightness level will reset to default level.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device that the flash unit belongs to. This value cannot be `null`. |
| `torchStrength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired brightness level to be set for the flash unit in the range 1 to [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL:android.hardware.camera2.CameraCharacteristics.Key). |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if it failed to access the flash unit. [CameraAccessException.CAMERA_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_IN_USE:kotlin.Int) will be thrown if the camera device is in use. [CameraAccessException.MAX_CAMERAS_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#MAX_CAMERAS_IN_USE:kotlin.Int) will be thrown if other camera resources needed to turn on the torch mode are in use. [CameraAccessException.CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int) will be thrown if camera service is not available. |
| `java.lang.IllegalArgumentException` | if cameraId was null, cameraId doesn't match any currently or previously available camera device, the camera device doesn't have a flash unit or if torchStrength is not within the range i.e. is greater than the maximum level [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL:android.hardware.camera2.CameraCharacteristics.Key) or \<= 0. |

### unregisterAvailabilityCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterAvailabilityCallback(callback: CameraManager.AvailabilityCallback): Unit
```

Remove a previously-added callback; the callback will no longer receive connection and disconnection callbacks.

Removing a callback that isn't registered has no effect.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [CameraManager.AvailabilityCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback): The callback to remove from the notification list This value cannot be `null`. |

### unregisterTorchCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterTorchCallback(callback: CameraManager.TorchCallback): Unit
```

Remove a previously-added callback; the callback will no longer receive torch mode status callbacks.

Removing a callback that isn't registered has no effect.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [CameraManager.TorchCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.TorchCallback): The callback to remove from the notification list This value cannot be `null`. |
