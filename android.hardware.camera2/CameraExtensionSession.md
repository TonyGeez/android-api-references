# CameraExtensionSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraExtensionSession

Kotlin| [Java](../android/hardware/camera2/CameraExtensionSession.md) 
| --- | --- |

```
abstract class CameraExtensionSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.CameraExtensionSession](../android/hardware/camera2/CameraExtensionSession.md) |

A camera capture session that enables access to device-specific camera extensions, which often use multi-frame bursts and sophisticated post-process algorithms for image capture.

The capture session will be returned after a successful call to [CameraDevice.createExtensionSession](../android/hardware/camera2/CameraDevice.md))as part of the argument in the registered state callback [StateCallback.onConfigured](../android/hardware/camera2/CameraExtensionSession.StateCallback.md))method.

Note that CameraExtensionSession is currently limited to a maximum of two output surfaces for continuous repeating and multi-frame processing respectively. Some features such as capture settings will not be supported as the device-specific Extension is allowed to override all capture parameters.

Information about support for specific device-specific extensions can be queried from [CameraExtensionCharacteristics](../android/hardware/camera2/CameraExtensionCharacteristics.md).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ExtensionCaptureCallback](../android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback.md) A callback object for tracking the progress of a [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) submitted to the camera device. |
| abstract | [StateCallback](../android/hardware/camera2/CameraExtensionSession.StateCallback.md) A callback object for receiving updates about the state of a camera extension session. |
| | [StillCaptureLatency](../android/hardware/camera2/CameraExtensionSession.StillCaptureLatency.md) Realtime calculated still [capture](../android/hardware/camera2/CameraExtensionSession.md))latency. |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capture](../android/hardware/camera2/CameraExtensionSession.md))`(`request:` ` [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [CameraExtensionSession.ExtensionCaptureCallback](../android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback.md)`)` Submit a request for device-specific processing using input from the camera device, to produce a single high-quality output result. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/hardware/camera2/CameraExtensionSession.md))`()` Close this capture session asynchronously. |
| open [CameraDevice](../android/hardware/camera2/CameraDevice.md) | [getDevice](../android/hardware/camera2/CameraExtensionSession.md))`()` Get the camera device that this session is created for. |
| --- | --- |
| open [CameraExtensionSession.StillCaptureLatency](../android/hardware/camera2/CameraExtensionSession.StillCaptureLatency.md)? | [getRealtimeStillCaptureLatency](../android/hardware/camera2/CameraExtensionSession.md))`()` Return the realtime still [capture](../android/hardware/camera2/CameraExtensionSession.md))latency. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setRepeatingRequest](../android/hardware/camera2/CameraExtensionSession.md))`(`request:` ` [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [CameraExtensionSession.ExtensionCaptureCallback](../android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback.md)`)` Request endlessly repeating device-specific extension processing of camera images. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopRepeating](../android/hardware/camera2/CameraExtensionSession.md))`()` Cancel any ongoing repeating capture set by [setRepeatingRequest](../android/hardware/camera2/CameraExtensionSession.md)). |
| --- | --- |

## Public methods

### capture

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun capture(
    request: CaptureRequest, 
    executor: Executor, 
    listener: CameraExtensionSession.ExtensionCaptureCallback
): Int
```

Submit a request for device-specific processing using input from the camera device, to produce a single high-quality output result.

Note that single capture requests currently do not support client parameters except for controls advertised in [CameraExtensionCharacteristics.getAvailableCaptureRequestKeys](../android/hardware/camera2/CameraExtensionCharacteristics.md)). The rest of the settings included in the request will be entirely overridden by the device-specific extension.

If [CameraExtensionCharacteristics.isPostviewAvailable](../android/hardware/camera2/CameraExtensionCharacteristics.md))returns false, the [CaptureRequest.Builder.addTarget](../android/hardware/camera2/CaptureRequest.Builder.md))will support only one ImageFormat.YUV_420_888 or ImageFormat.JPEG target surface. [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) arguments that include further targets will cause IllegalArgumentException to be thrown. If postview is available, [CaptureRequest.Builder.addTarget](../android/hardware/camera2/CaptureRequest.Builder.md))will support up to two ImageFormat.YUV_420_888 or ImageFormat.JPEG target surfaces for the still capture and postview. IllegalArgumentException will be thrown if a postview target is added without a still capture target, if more than two target surfaces are added, or if the surface formats for postview and capture are not equivalent.

Starting with Android [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md) single capture requests will also support the preview [android.graphics.ImageFormat#PRIVATE](../android/graphics/ImageFormat.md) target surface. These can typically be used for enabling AF/AE triggers. Do note, that single capture requests referencing both output surfaces remain unsupported.

Each request will produce one new frame for one target Surface, set with the CaptureRequest builder's [CaptureRequest.Builder.addTarget](../android/hardware/camera2/CaptureRequest.Builder.md))method.

Multiple requests can be in progress at once. Requests are processed in first-in, first-out order.

Requests submitted through this method have higher priority than those submitted through [setRepeatingRequest](../android/hardware/camera2/CameraExtensionSession.md)), and will be processed as soon as the current repeat processing completes.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [CaptureRequest](../android/hardware/camera2/CaptureRequest.md):the settings for this capture This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor which will be used for invoking the listener. This value cannot be`null`. |
| `listener` | [CameraExtensionSession.ExtensionCaptureCallback](../android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback.md):The callback object to notify once this request has been processed. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int A unique capture sequence ID used by [ExtensionCaptureCallback.onCaptureSequenceCompleted](../android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback.md)). |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |
| `java.lang.IllegalArgumentException` | if the request targets no Surfaces or Surfaces that are not configured as outputs for this session; or the request targets a set of Surfaces that cannot be submitted simultaneously. |
| --- | --- |

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Close this capture session asynchronously.

Closing a session frees up the target output Surfaces of the session for reuse with either a new session, or to other APIs that can draw to Surfaces.

Note that creating a new capture session with android.hardware.camera2.CameraDevice#createCaptureSession or [android.hardware.camera2.CameraDevice#createExtensionSession](../android/hardware/camera2/CameraDevice.md))will close any existing capture session automatically, and call the older session listener's [StateCallback.onClosed](../android/hardware/camera2/CameraExtensionSession.StateCallback.md))callback. Using android.hardware.camera2.CameraDevice#createCaptureSession or [android.hardware.camera2.CameraDevice#createExtensionSession](../android/hardware/camera2/CameraDevice.md))directly without closing is the recommended approach for quickly switching to a new session, since unchanged target outputs can be reused more efficiently.

Once a session is closed, all methods on it will throw an IllegalStateException, and any repeating requests are stopped (as if [stopRepeating()](../android/hardware/camera2/CameraExtensionSession.md))was called).

Closing a session is idempotent; closing more than once has no effect.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### getDevice

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDevice(): CameraDevice
```

Get the camera device that this session is created for.

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------|
| [CameraDevice](../android/hardware/camera2/CameraDevice.md) | This value cannot be`null`. |

### getRealtimeStillCaptureLatency

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRealtimeStillCaptureLatency(): CameraExtensionSession.StillCaptureLatency?
```

Return the realtime still [capture](../android/hardware/camera2/CameraExtensionSession.md))latency.

The estimations will take into account the current environment conditions, the camera state and will include the time spent processing the multi-frame capture request along with any additional time for encoding of the processed buffer if necessary.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [CameraExtensionSession.StillCaptureLatency](../android/hardware/camera2/CameraExtensionSession.StillCaptureLatency.md)? | The realtime still capture latency, or`null`if the estimation is not supported. |

### setRepeatingRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRepeatingRequest(
    request: CaptureRequest, 
    executor: Executor, 
    listener: CameraExtensionSession.ExtensionCaptureCallback
): Int
```

Request endlessly repeating device-specific extension processing of camera images.

With this method, the camera device will continually capture images and process them using the device-specific extension at the maximum rate possible.

Note that repeating capture requests currently do not support client parameters except for controls advertised in [CameraExtensionCharacteristics.getAvailableCaptureRequestKeys](../android/hardware/camera2/CameraExtensionCharacteristics.md)). The rest of the settings included in the request will be entirely overridden by the device-specific extension.

The [CaptureRequest.Builder.addTarget](../android/hardware/camera2/CaptureRequest.Builder.md))supports only one target surface. [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) arguments that include further targets will cause IllegalArgumentException to be thrown.

Repeating requests are a simple way for an application to maintain a preview or other continuous stream of frames.

Repeat requests have lower priority than those submitted through [capture](../android/hardware/camera2/CameraExtensionSession.md)), so if [capture](../android/hardware/camera2/CameraExtensionSession.md))is called when a repeating request is active, the capture request will be processed before any further repeating requests are processed.

To stop the repeating capture, call [stopRepeating](../android/hardware/camera2/CameraExtensionSession.md)).

Calling this method will replace any earlier repeating request.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [CaptureRequest](../android/hardware/camera2/CaptureRequest.md):the request to repeat indefinitely This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor which will be used for invoking the listener. This value cannot be`null`. |
| `listener` | [CameraExtensionSession.ExtensionCaptureCallback](../android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback.md):The callback object to notify every time the request finishes processing. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int A unique capture sequence ID used by [ExtensionCaptureCallback.onCaptureSequenceCompleted](../android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback.md)). |

| Exceptions ||
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |
| `java.lang.IllegalArgumentException` | If the request references no Surfaces or references Surfaces that are not currently configured as outputs. |
| --- | --- |

**See Also**

- [#capture](../android/hardware/camera2/CameraExtensionSession.md)) 

### stopRepeating

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopRepeating(): Unit
```

Cancel any ongoing repeating capture set by [setRepeatingRequest](../android/hardware/camera2/CameraExtensionSession.md)). Has no effect on requests submitted through [capture](../android/hardware/camera2/CameraExtensionSession.md)).

Any currently in-flight captures will still complete.

| Exceptions ||
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- [#setRepeatingRequest](../android/hardware/camera2/CameraExtensionSession.md))
