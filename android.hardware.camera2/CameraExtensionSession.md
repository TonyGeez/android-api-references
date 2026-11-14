# CameraExtensionSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraExtensionSession

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/CameraExtensionSession "View this page in Java") 

```
abstract class CameraExtensionSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.CameraExtensionSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#) |

A camera capture session that enables access to device-specific camera extensions, which often use multi-frame bursts and sophisticated post-process algorithms for image capture.

The capture session will be returned after a successful call to [CameraDevice.createExtensionSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createExtensionSession(android.hardware.camera2.params.ExtensionSessionConfiguration))as part of the argument in the registered state callback [StateCallback.onConfigured](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StateCallback#onConfigured(android.hardware.camera2.CameraExtensionSession))method.

Note that CameraExtensionSession is currently limited to a maximum of two output surfaces for continuous repeating and multi-frame processing respectively. Some features such as capture settings will not be supported as the device-specific Extension is allowed to override all capture parameters.

Information about support for specific device-specific extensions can be queried from [CameraExtensionCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ExtensionCaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback) A callback object for tracking the progress of a [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) submitted to the camera device. |
| abstract | [StateCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StateCallback) A callback object for receiving updates about the state of a camera extension session. |
| | [StillCaptureLatency](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StillCaptureLatency) Realtime calculated still [capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#capture(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback))latency. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#capture(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback))`(`request:` ` [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [CameraExtensionSession.ExtensionCaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback)`)` Submit a request for device-specific processing using input from the camera device, to produce a single high-quality output result. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#close())`()` Close this capture session asynchronously. |
| open [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) | [getDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#getDevice())`()` Get the camera device that this session is created for. |
| open [CameraExtensionSession.StillCaptureLatency](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StillCaptureLatency)? | [getRealtimeStillCaptureLatency](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#getRealtimeStillCaptureLatency())`()` Return the realtime still [capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#capture(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback))latency. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setRepeatingRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback))`(`request:` ` [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [CameraExtensionSession.ExtensionCaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback)`)` Request endlessly repeating device-specific extension processing of camera images. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopRepeating](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#stopRepeating())`()` Cancel any ongoing repeating capture set by [setRepeatingRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback)). |

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

Note that single capture requests currently do not support client parameters except for controls advertised in [CameraExtensionCharacteristics.getAvailableCaptureRequestKeys](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#getAvailableCaptureRequestKeys(kotlin.Int)). The rest of the settings included in the request will be entirely overridden by the device-specific extension.

If [CameraExtensionCharacteristics.isPostviewAvailable](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#isPostviewAvailable(kotlin.Int))returns false, the [CaptureRequest.Builder.addTarget](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface))will support only one ImageFormat.YUV_420_888 or ImageFormat.JPEG target surface. [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) arguments that include further targets will cause IllegalArgumentException to be thrown. If postview is available, [CaptureRequest.Builder.addTarget](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface))will support up to two ImageFormat.YUV_420_888 or ImageFormat.JPEG target surfaces for the still capture and postview. IllegalArgumentException will be thrown if a postview target is added without a still capture target, if more than two target surfaces are added, or if the surface formats for postview and capture are not equivalent.

Starting with Android [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int) single capture requests will also support the preview [android.graphics.ImageFormat#PRIVATE](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int) target surface. These can typically be used for enabling AF/AE triggers. Do note, that single capture requests referencing both output surfaces remain unsupported.

Each request will produce one new frame for one target Surface, set with the CaptureRequest builder's [CaptureRequest.Builder.addTarget](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface))method.

Multiple requests can be in progress at once. Requests are processed in first-in, first-out order.

Requests submitted through this method have higher priority than those submitted through [setRepeatingRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback)), and will be processed as soon as the current repeat processing completes.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest):the settings for this capture This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor which will be used for invoking the listener. This value cannot be`null`. |
| `listener` | [CameraExtensionSession.ExtensionCaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback):The callback object to notify once this request has been processed. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int A unique capture sequence ID used by [ExtensionCaptureCallback.onCaptureSequenceCompleted](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraExtensionSession,%20kotlin.Int)). |

| Exceptions ||
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |
| `java.lang.IllegalArgumentException` | if the request targets no Surfaces or Surfaces that are not configured as outputs for this session; or the request targets a set of Surfaces that cannot be submitted simultaneously. |

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Close this capture session asynchronously.

Closing a session frees up the target output Surfaces of the session for reuse with either a new session, or to other APIs that can draw to Surfaces.

Note that creating a new capture session with android.hardware.camera2.CameraDevice#createCaptureSession or [android.hardware.camera2.CameraDevice#createExtensionSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createExtensionSession(android.hardware.camera2.params.ExtensionSessionConfiguration))will close any existing capture session automatically, and call the older session listener's [StateCallback.onClosed](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StateCallback#onClosed(android.hardware.camera2.CameraExtensionSession))callback. Using android.hardware.camera2.CameraDevice#createCaptureSession or [android.hardware.camera2.CameraDevice#createExtensionSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createExtensionSession(android.hardware.camera2.params.ExtensionSessionConfiguration))directly without closing is the recommended approach for quickly switching to a new session, since unchanged target outputs can be reused more efficiently.

Once a session is closed, all methods on it will throw an IllegalStateException, and any repeating requests are stopped (as if [stopRepeating()](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#stopRepeating())was called).

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
| [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) | This value cannot be`null`. |

### getRealtimeStillCaptureLatency

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRealtimeStillCaptureLatency(): CameraExtensionSession.StillCaptureLatency?
```

Return the realtime still [capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#capture(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback))latency.

The estimations will take into account the current environment conditions, the camera state and will include the time spent processing the multi-frame capture request along with any additional time for encoding of the processed buffer if necessary.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [CameraExtensionSession.StillCaptureLatency](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.StillCaptureLatency)? | The realtime still capture latency, or`null`if the estimation is not supported. |

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

Note that repeating capture requests currently do not support client parameters except for controls advertised in [CameraExtensionCharacteristics.getAvailableCaptureRequestKeys](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#getAvailableCaptureRequestKeys(kotlin.Int)). The rest of the settings included in the request will be entirely overridden by the device-specific extension.

The [CaptureRequest.Builder.addTarget](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface))supports only one target surface. [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) arguments that include further targets will cause IllegalArgumentException to be thrown.

Repeating requests are a simple way for an application to maintain a preview or other continuous stream of frames.

Repeat requests have lower priority than those submitted through [capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#capture(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback)), so if [capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#capture(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback))is called when a repeating request is active, the capture request will be processed before any further repeating requests are processed.

To stop the repeating capture, call [stopRepeating](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#stopRepeating()).

Calling this method will replace any earlier repeating request.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest):the request to repeat indefinitely This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor which will be used for invoking the listener. This value cannot be`null`. |
| `listener` | [CameraExtensionSession.ExtensionCaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback):The callback object to notify every time the request finishes processing. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int A unique capture sequence ID used by [ExtensionCaptureCallback.onCaptureSequenceCompleted](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.ExtensionCaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraExtensionSession,%20kotlin.Int)). |

| Exceptions ||
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |
| `java.lang.IllegalArgumentException` | If the request references no Surfaces or references Surfaces that are not currently configured as outputs. |

**See Also**

- [#capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#capture(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback)) 

### stopRepeating

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopRepeating(): Unit
```

Cancel any ongoing repeating capture set by [setRepeatingRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback)). Has no effect on requests submitted through [capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#capture(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback)).

Any currently in-flight captures will still complete.

| Exceptions ||
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- [#setRepeatingRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraExtensionSession.ExtensionCaptureCallback))
