# CameraManager

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraManager

Kotlin | [Java](CameraManager.md) 
| --- | --- |

```
class CameraManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.CameraManager](CameraManager.md) |

A system service manager for detecting, characterizing, and connecting to [CameraDevices](CameraDevice.md).

For more details about communicating with camera devices, read the Camera developer guide or the [camera2](_package.md) package documentation.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AvailabilityCallback](../android/hardware/camera2/CameraManager.AvailabilityCallback.md) A callback for camera devices becoming available or unavailable to open. |
| abstract | [TorchCallback](../android/hardware/camera2/CameraManager.TorchCallback.md) A callback for camera flash torch modes becoming unavailable, disabled, or enabled. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CameraCharacteristics](CameraCharacteristics.md) | [getCameraCharacteristics](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query the capabilities of a camera device. |
| [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) | [getCameraDeviceSetup](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) object for the given `cameraId`, which provides limited access to CameraDevice setup and query functionality without requiring an #openCamera call. |
| [CameraExtensionCharacteristics](CameraExtensionCharacteristics.md) | [getCameraExtensionCharacteristics](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query the camera extension capabilities of a camera device. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getCameraIdList](CameraManager.md))`()` Return the list of currently connected camera devices by identifier, including cameras that may be in use by other camera API clients. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | [getConcurrentCameraIds](CameraManager.md))`()` Return the set of combinations of currently connected camera device identifiers, which support configuring camera device sessions concurrently. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTorchStrengthLevel](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the brightness level of the flash unit associated with the cameraId. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCameraDeviceSetupSupported](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Checks a Camera Device's characteristics to ensure that a [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) instance can be constructed for a given `cameraId`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConcurrentSessionConfigurationSupported](CameraManager.md))`(`cameraIdAndSessionConfig:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [SessionConfiguration](../android.hardware.camera2.params/SessionConfiguration.md)!>`)` Checks whether the provided set of camera devices and their corresponding [SessionConfiguration](../android.hardware.camera2.params/SessionConfiguration.md) can be configured concurrently. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openCamera](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `callback:` ` [CameraDevice.StateCallback](../android/hardware/camera2/CameraDevice.StateCallback.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Open a connection to a camera with the given ID. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openCamera](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [CameraDevice.StateCallback](../android/hardware/camera2/CameraDevice.StateCallback.md)`)` Open a connection to a camera with the given ID. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAvailabilityCallback](CameraManager.md))`(`callback:` ` [CameraManager.AvailabilityCallback](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Register a callback to be notified about camera device availability. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAvailabilityCallback](CameraManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [CameraManager.AvailabilityCallback](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)`)` Register a callback to be notified about camera device availability. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerTorchCallback](CameraManager.md))`(`callback:` ` [CameraManager.TorchCallback](../android/hardware/camera2/CameraManager.TorchCallback.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Register a callback to be notified about torch mode status. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerTorchCallback](CameraManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [CameraManager.TorchCallback](../android/hardware/camera2/CameraManager.TorchCallback.md)`)` Register a callback to be notified about torch mode status. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTorchMode](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the flash unit's torch mode of the camera of the given ID without opening the camera device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [turnOnTorchWithStrengthLevel](CameraManager.md))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `torchStrength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the brightness level of the flashlight associated with the given cameraId in torch mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAvailabilityCallback](CameraManager.md))`(`callback:` ` [CameraManager.AvailabilityCallback](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)`)` Remove a previously-added callback; the callback will no longer receive connection and disconnection callbacks. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterTorchCallback](CameraManager.md))`(`callback:` ` [CameraManager.TorchCallback](../android/hardware/camera2/CameraManager.TorchCallback.md)`)` Remove a previously-added callback; the callback will no longer receive torch mode status callbacks. |
| --- | --- |

## Public methods

### getCameraCharacteristics

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCameraCharacteristics(cameraId: String): CameraCharacteristics
```

Query the capabilities of a camera device. These capabilities are immutable for a given camera.

From API level 29, this function can also be used to query the capabilities of physical cameras that can only be used as part of logical multi-camera. These cameras cannot be opened directly via #openCamera

Also starting with API level 29, while most basic camera information is still available even without the CAMERA permission, some values are not available to apps that do not hold that permission. The keys not available are listed by [CameraCharacteristics.getKeysNeedingPermission](CameraCharacteristics.md)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The id of the camera device to query. This could be either a standalone camera ID which can be directly opened by #openCamera, or a physical camera ID that can only used as part of a logical multi-camera. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [CameraCharacteristics](CameraCharacteristics.md) | The properties of the given camera This value cannot be `null`. |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the cameraId does not match any known camera device. |
| `android.hardware.camera2.CameraAccessException` | if the camera device has been disconnected. |

**See Also**

- [#getCameraIdList](CameraManager.md))
- [android.app.admin.DevicePolicyManager#setCameraDisabled](../android.app.admin/DevicePolicyManager.md)) 

### getCameraDeviceSetup

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCameraDeviceSetup(cameraId: String): CameraDevice.CameraDeviceSetup
```

Returns a [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) object for the given `cameraId`, which provides limited access to CameraDevice setup and query functionality without requiring an #openCamera call. The [CameraDevice](CameraDevice.md) can later be obtained either by calling #openCamera, or [CameraDevice.CameraDeviceSetup.openCamera](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md)).

Support for [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) for a given `cameraId` must be checked with [isCameraDeviceSetupSupported](CameraManager.md)). If `isCameraDeviceSetupSupported` returns `false` for a `cameraId`, this method will throw an [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md)

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device for which [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) object must be constructed. This identifier must be present in [getCameraIdList()](CameraManager.md)) This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) | [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) object corresponding to the provided `cameraId` This value cannot be `null`. |

| Exceptions ||
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If `cameraId` is null, or if `cameraId` does not match any device in [getCameraIdList()](CameraManager.md)). |
| `android.hardware.camera2.CameraAccessException` | if the camera device is not accessible |
| `java.lang.UnsupportedOperationException` | if [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) instance cannot be constructed for the given `cameraId`, i.e. [isCameraDeviceSetupSupported](CameraManager.md)) returns false. |
| --- | --- |

**See Also**

- [android.hardware.camera2.CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md)
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
| [CameraExtensionCharacteristics](CameraExtensionCharacteristics.md) | The properties of the given camera This value cannot be `null`. |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the cameraId does not match any known camera device. |
| `android.hardware.camera2.CameraAccessException` | if the camera device has been disconnected. |

**See Also**

- [android.hardware.camera2.CameraExtensionCharacteristics](CameraExtensionCharacteristics.md)
- [android.hardware.camera2.CameraDevice#createExtensionSession(ExtensionSessionConfiguration)](CameraDevice.md))
- [android.hardware.camera2.CameraExtensionSession](CameraExtensionSession.md) 

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

- Applications must first close any open cameras that have sessions configured, using [CameraDevice.close](CameraDevice.md)).
- All camera devices intended to be operated concurrently, must be opened using #openCamera, before configuring sessions on any of the camera devices.

<br />

Each device in a combination, is guaranteed to support stream combinations which may be obtained by querying [getCameraCharacteristics](CameraManager.md)) for the key [android.hardware.camera2.CameraCharacteristics#SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS](CameraCharacteristics.md).

For concurrent operation, if a camera device has a non null zoom ratio range as specified by [android.hardware.camera2.CameraCharacteristics#CONTROL_ZOOM_RATIO_RANGE](CameraCharacteristics.md), its complete zoom ratio range may not apply. Applications can use [android.hardware.camera2.CaptureRequest#CONTROL_ZOOM_RATIO](CaptureRequest.md) \>=1 and \<= [android.hardware.camera2.CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM](CameraCharacteristics.md) during concurrent operation.

The set of combinations may include camera devices that may be in use by other camera API clients.

Concurrent camera extension sessions [CameraExtensionSession](CameraExtensionSession.md) are not currently supported.

The set of combinations doesn't contain physical cameras that can only be used as part of a logical multi-camera device.

If a new camera id becomes available through [AvailabilityCallback.onCameraUnavailable(String)](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)), clients can call this method to check if new combinations of camera ids which can stream concurrently are available.

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The brightness level of the flash unit associated with cameraId. When the torch is turned OFF, the strength level will reset to a default level [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL](CameraCharacteristics.md). In this case the return value will be [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL](CameraCharacteristics.md) rather than 0. |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if it failed to access the flash unit. |
| `java.lang.IllegalArgumentException` | if cameraId was null, cameraId doesn't match any currently or previously available camera device, or the camera device doesn't have a flash unit. |

### isCameraDeviceSetupSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCameraDeviceSetupSupported(cameraId: String): Boolean
```

Checks a Camera Device's characteristics to ensure that a [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) instance can be constructed for a given `cameraId`. If this method returns false for a `cameraId`, calling [getCameraDeviceSetup](CameraManager.md)) for that `cameraId` will throw an [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md).

[CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) is supported for all devices that report [CameraCharacteristics.INFO_SESSION_CONFIGURATION_QUERY_VERSION](CameraCharacteristics.md) \> [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device for which [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) support is being queried. This identifier must be present in [getCameraIdList()](CameraManager.md)). This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if [CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md) object can be constructed for the provided `cameraId`; `false` otherwise. |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If `cameraId` is null, or if `cameraId` does not match any device in [getCameraIdList()](CameraManager.md)). |
| `android.hardware.camera2.CameraAccessException` | if the camera device is not accessible |

**See Also**

- [android.hardware.camera2.CameraCharacteristics#INFO_SESSION_CONFIGURATION_QUERY_VERSION](CameraCharacteristics.md)
- [android.hardware.camera2.CameraDevice.CameraDeviceSetup](../android/hardware/camera2/CameraDevice.CameraDeviceSetup.md)
- [#getCameraDeviceSetup(String)](CameraManager.md))
- <https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()> 

### isConcurrentSessionConfigurationSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConcurrentSessionConfigurationSupported(cameraIdAndSessionConfig: MutableMap<String!, SessionConfiguration!>): Boolean
```

Checks whether the provided set of camera devices and their corresponding [SessionConfiguration](../android.hardware.camera2.params/SessionConfiguration.md) can be configured concurrently.

This method performs a runtime check of the given [SessionConfiguration](../android.hardware.camera2.params/SessionConfiguration.md) and camera id combinations. The result confirms whether or not the passed session configurations can be successfully used to create camera capture sessions concurrently, on the given camera devices using [CameraDevice.createCaptureSession(SessionConfiguration)](CameraDevice.md)).

The method can be called at any point before, during and after active capture sessions. It will not impact normal camera behavior in any way and must complete significantly faster than creating a regular or constrained capture session.

Although this method is faster than creating a new capture session, it is not intended to be used for exploring the entire space of supported concurrent stream combinations. The available mandatory concurrent stream combinations may be obtained by querying [getCameraCharacteristics](CameraManager.md)) for the key [android.hardware.camera2.CameraCharacteristics#SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS](CameraCharacteristics.md).

Note that session parameters will be ignored and calls to [SessionConfiguration.setSessionParameters](../android.hardware.camera2.params/SessionConfiguration.md)) are not required.

Requires [android.Manifest.permission#CAMERA](../android/Manifest.permission.md)

| Parameters ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraIdAndSessionConfig` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [SessionConfiguration](../android.hardware.camera2.params/SessionConfiguration.md)!\>: This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the given combination of session configurations and corresponding camera ids are concurrently supported by the camera sub-system, `false` otherwise OR if the set of camera devices provided is not a subset of those returned by [getConcurrentCameraIds](CameraManager.md)). |

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

Use [getCameraIdList](CameraManager.md)) to get the list of available camera devices. Note that even if an id is listed, open may fail if the device is disconnected between the calls to [getCameraIdList](CameraManager.md)) and #openCamera, or if a higher-priority camera API client begins using the camera device.

As of API level 23, devices for which the [AvailabilityCallback.onCameraUnavailable(String)](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)) callback has been called due to the device being in use by a lower-priority, background camera API client can still potentially be opened by calling this method when the calling camera API client has a higher priority than the current camera API client using this device. In general, if the top, foreground activity is running within your application process, your process will be given the highest priority when accessing the camera, and this method will succeed even if the camera device is in use by another camera API client. Any lower-priority application that loses control of the camera in this way will receive an [android.hardware.camera2.CameraDevice.StateCallback#onDisconnected](../android/hardware/camera2/CameraDevice.StateCallback.md)) callback. Opening the same camera ID twice in the same application will similarly cause the [android.hardware.camera2.CameraDevice.StateCallback#onDisconnected](../android/hardware/camera2/CameraDevice.StateCallback.md)) callback being fired for the [CameraDevice](CameraDevice.md) from the first open call and all ongoing tasks being dropped.

Once the camera is successfully opened, [CameraDevice.StateCallback.onOpened](../android/hardware/camera2/CameraDevice.StateCallback.md)) will be invoked with the newly opened [CameraDevice](CameraDevice.md). The camera device can then be set up for operation by calling android.hardware.camera2.CameraDevice#createCaptureSession and android.hardware.camera2.CameraDevice#createCaptureRequest

Before API level 30, when the application tries to open multiple [CameraDevice](CameraDevice.md) of different IDs and the device does not support opening such combination, either the #openCamera will fail and throw a [CameraAccessException](CameraAccessException.md) or one or more of already opened [CameraDevice](CameraDevice.md) will be disconnected and receive [android.hardware.camera2.CameraDevice.StateCallback#onDisconnected](../android/hardware/camera2/CameraDevice.StateCallback.md)) callback. Which behavior will happen depends on the device implementation and can vary on different devices. Starting in API level 30, if the device does not support the combination of cameras being opened, it is guaranteed the #openCamera call will fail and none of existing [CameraDevice](CameraDevice.md) will be disconnected.

If the camera becomes disconnected during initialization after this function call returns, [CameraDevice.StateCallback.onDisconnected](../android/hardware/camera2/CameraDevice.StateCallback.md)) with a [CameraDevice](CameraDevice.md) in the disconnected state (and [CameraDevice.StateCallback.onOpened](../android/hardware/camera2/CameraDevice.StateCallback.md)) will be skipped).

If opening the camera device fails, then the device callback's [onError](../android/hardware/camera2/CameraDevice.StateCallback.md)) method will be called, and subsequent calls on the camera device will throw a [CameraAccessException](CameraAccessException.md).

Requires [android.Manifest.permission#CAMERA](../android/Manifest.permission.md)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device to open This value cannot be `null`. |
| `callback` | [CameraDevice.StateCallback](../android/hardware/camera2/CameraDevice.StateCallback.md): The callback which is invoked once the camera is opened This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: The handler on which the callback should be invoked, or `null` to use the current thread's [looper](../android.os/Looper.md). |
| --- | --- |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera is disabled by device policy, has been disconnected, is being used by a higher-priority camera API client, or the device has reached its maximal resource and cannot open this camera device. |
| `java.lang.IllegalArgumentException` | if cameraId or the callback was null, or the cameraId does not match any currently or previously available camera device returned by [getCameraIdList](CameraManager.md)). |
| `java.lang.SecurityException` | if the application does not have permission to access the camera |
| --- | --- |

**See Also**

- [#getCameraIdList](CameraManager.md))
- [android.app.admin.DevicePolicyManager#setCameraDisabled](../android.app.admin/DevicePolicyManager.md)) 

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

The behavior of this method matches that of [openCamera(java.lang.String,android.hardware.camera2.CameraDevice.StateCallback,android.os.Handler)](CameraManager.md)), except that it uses [java.util.concurrent.Executor](../java.util.concurrent/Executor.md) as an argument instead of [android.os.Handler](../android.os/Handler.md).

Do note that typically callbacks are expected to be dispatched by the executor in a single thread. If the executor uses two or more threads to dispatch callbacks, then clients must ensure correct synchronization and must also be able to handle potentially different ordering of the incoming callbacks.

Requires [android.Manifest.permission#CAMERA](../android/Manifest.permission.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device to open This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor which will be used when invoking the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [CameraDevice.StateCallback](../android/hardware/camera2/CameraDevice.StateCallback.md): The callback which is invoked once the camera is opened This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera is disabled by device policy, has been disconnected, or is being used by a higher-priority camera API client. |
| `java.lang.IllegalArgumentException` | if cameraId, the callback or the executor was null, or the cameraId does not match any currently or previously available camera device. |
| `java.lang.SecurityException` | if the application does not have permission to access the camera |
| --- | --- |

**See Also**

- [#getCameraIdList](CameraManager.md))
- [android.app.admin.DevicePolicyManager#setCameraDisabled](../android.app.admin/DevicePolicyManager.md)) 

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

[AvailabilityCallback.onCameraUnavailable(String)](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)) will be called whenever a camera device is opened by any camera API client. As of API level 23, other camera API clients may still be able to open such a camera device, evicting the existing client if they have higher priority than the existing client of a camera device. See open() for more details.

Since this callback will be registered with the camera service, remember to unregister it once it is no longer needed; otherwise the callback will continue to receive events indefinitely and it may prevent other resources from being released. Specifically, the callbacks will be invoked independently of the general activity lifecycle and independently of the state of individual CameraManager instances.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [CameraManager.AvailabilityCallback](../android/hardware/camera2/CameraManager.AvailabilityCallback.md): the new callback to send camera availability notices to This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: The handler on which the callback should be invoked, or `null` to use the current thread's [looper](../android.os/Looper.md). |

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

The behavior of this method matches that of [registerAvailabilityCallback(android.hardware.camera2.CameraManager.AvailabilityCallback,android.os.Handler)](CameraManager.md)), except that it uses [java.util.concurrent.Executor](../java.util.concurrent/Executor.md) as an argument instead of [android.os.Handler](../android.os/Handler.md).

Note: If the order between some availability callbacks matters, the implementation of the executor should handle those callbacks in the same thread to maintain the callbacks' order. Some examples are:

- [AvailabilityCallback.onCameraAvailable](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)) and [AvailabilityCallback.onCameraUnavailable](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)) of the same camera ID.
- [AvailabilityCallback.onCameraAvailable](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)) or [AvailabilityCallback.onCameraUnavailable](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)) of a logical multi-camera, and [android.hardware.camera2.CameraManager.AvailabilityCallback#onPhysicalCameraUnavailable](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)) or [AvailabilityCallback.onPhysicalCameraAvailable](../android/hardware/camera2/CameraManager.AvailabilityCallback.md)) of its physical cameras.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor which will be used to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [CameraManager.AvailabilityCallback](../android/hardware/camera2/CameraManager.AvailabilityCallback.md): the new callback to send camera availability notices to This value cannot be `null`. |

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
| `callback` | [CameraManager.TorchCallback](../android/hardware/camera2/CameraManager.TorchCallback.md): The new callback to send torch mode status to This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: The handler on which the callback should be invoked, or `null` to use the current thread's [looper](../android.os/Looper.md). |

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

The behavior of this method matches that of [registerTorchCallback(android.hardware.camera2.CameraManager.TorchCallback,android.os.Handler)](CameraManager.md)), except that it uses [java.util.concurrent.Executor](../java.util.concurrent/Executor.md) as an argument instead of [android.os.Handler](../android.os/Handler.md).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor which will be used to invoke the callback This value cannot be `null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [CameraManager.TorchCallback](../android/hardware/camera2/CameraManager.TorchCallback.md): The new callback to send torch mode status to This value cannot be `null`. |

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

Use [getCameraIdList](CameraManager.md)) to get the list of available camera devices and use [getCameraCharacteristics](CameraManager.md)) to check whether the camera device has a flash unit. Note that even if a camera device has a flash unit, turning on the torch mode may fail if the camera device or other camera resources needed to turn on the torch mode are in use.

If [setTorchMode](CameraManager.md)) is called to turn on or off the torch mode successfully, [CameraManager.TorchCallback.onTorchModeChanged](../android/hardware/camera2/CameraManager.TorchCallback.md)) will be invoked. However, even if turning on the torch mode is successful, the application does not have the exclusive ownership of the flash unit or the camera device. The torch mode will be turned off and becomes unavailable when the camera device that the flash unit belongs to becomes unavailable or when other camera resources to keep the torch on become unavailable ( [CameraManager.TorchCallback.onTorchModeUnavailable](../android/hardware/camera2/CameraManager.TorchCallback.md)) will be invoked). Also, other applications are free to call [setTorchMode](CameraManager.md)) to turn off the torch mode ( [CameraManager.TorchCallback.onTorchModeChanged](../android/hardware/camera2/CameraManager.TorchCallback.md)) will be invoked). If the latest application that turned on the torch mode exits, the torch mode will be turned off.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device that the flash unit belongs to. This value cannot be `null`. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The desired state of the torch mode for the target camera device. Set to `true` to turn on the torch mode. Set to `false` to turn off the torch mode. |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if it failed to access the flash unit. [CameraAccessException.CAMERA_IN_USE](CameraAccessException.md) will be thrown if the camera device is in use. [CameraAccessException.MAX_CAMERAS_IN_USE](CameraAccessException.md) will be thrown if other camera resources needed to turn on the torch mode are in use. [CameraAccessException.CAMERA_DISCONNECTED](CameraAccessException.md) will be thrown if camera service is not available. |
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

Use [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL](CameraCharacteristics.md) to check whether the camera device supports flash unit strength control or not. If this value is greater than 1, applications can call this API to control the flashlight brightness level.

If [turnOnTorchWithStrengthLevel](CameraManager.md)) is called to change the brightness level of the flash unit [CameraManager.TorchCallback.onTorchStrengthLevelChanged](../android/hardware/camera2/CameraManager.TorchCallback.md)) will be invoked. If the new desired strength level is same as previously set level, then this callback will not be invoked. If the torch is OFF and [turnOnTorchWithStrengthLevel](CameraManager.md)) is called with level \>= 1, the torch will be turned ON with that brightness level. In this case [CameraManager.TorchCallback.onTorchModeChanged](../android/hardware/camera2/CameraManager.TorchCallback.md)) will also be invoked.

When the torch is turned OFF via [setTorchMode](CameraManager.md)), the flashlight brightness level will reset to default value [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL](CameraCharacteristics.md) In this case the [CameraManager.TorchCallback.onTorchStrengthLevelChanged](../android/hardware/camera2/CameraManager.TorchCallback.md)) will not be invoked.

If torch is enabled via [setTorchMode](CameraManager.md)) after calling [turnOnTorchWithStrengthLevel](CameraManager.md)) with level N then the flash unit will have the brightness level N. Since multiple applications are free to call [setTorchMode](CameraManager.md)), when the latest application that turned ON the torch mode exits, the torch mode will be turned OFF and in this case the brightness level will reset to default level.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier of the camera device that the flash unit belongs to. This value cannot be `null`. |
| `torchStrength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired brightness level to be set for the flash unit in the range 1 to [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL](CameraCharacteristics.md). |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if it failed to access the flash unit. [CameraAccessException.CAMERA_IN_USE](CameraAccessException.md) will be thrown if the camera device is in use. [CameraAccessException.MAX_CAMERAS_IN_USE](CameraAccessException.md) will be thrown if other camera resources needed to turn on the torch mode are in use. [CameraAccessException.CAMERA_DISCONNECTED](CameraAccessException.md) will be thrown if camera service is not available. |
| `java.lang.IllegalArgumentException` | if cameraId was null, cameraId doesn't match any currently or previously available camera device, the camera device doesn't have a flash unit or if torchStrength is not within the range i.e. is greater than the maximum level [android.hardware.camera2.CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL](CameraCharacteristics.md) or \<= 0. |

### unregisterAvailabilityCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterAvailabilityCallback(callback: CameraManager.AvailabilityCallback): Unit
```

Remove a previously-added callback; the callback will no longer receive connection and disconnection callbacks.

Removing a callback that isn't registered has no effect.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [CameraManager.AvailabilityCallback](../android/hardware/camera2/CameraManager.AvailabilityCallback.md): The callback to remove from the notification list This value cannot be `null`. |

### unregisterTorchCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterTorchCallback(callback: CameraManager.TorchCallback): Unit
```

Remove a previously-added callback; the callback will no longer receive torch mode status callbacks.

Removing a callback that isn't registered has no effect.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [CameraManager.TorchCallback](../android/hardware/camera2/CameraManager.TorchCallback.md): The callback to remove from the notification list This value cannot be `null`. |
