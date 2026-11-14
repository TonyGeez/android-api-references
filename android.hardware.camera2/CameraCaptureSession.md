Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraCaptureSession

```
abstract class CameraCaptureSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.CameraCaptureSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#) |

| Known Direct Subclasses [CameraConstrainedHighSpeedCaptureSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession), [CameraOfflineSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession) |---|---| | [CameraConstrainedHighSpeedCaptureSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession) | A constrained high speed capture session for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice`, used for capturing high speed images from the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice` for high speed video recording use case. | | [CameraOfflineSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession) | A camera capture session that was switched to offline mode via successful call to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#switchToOffline(kotlin.collections.MutableCollection,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraOfflineSession.CameraOfflineSessionCallback)`. | |

A configured capture session for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice`, used for capturing images from the camera or reprocessing images captured from the camera in the same session previously.

A CameraCaptureSession is created by providing a set of target output surfaces to android.hardware.camera2.CameraDevice#createCaptureSession, or by providing an `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration` and a set of target output surfaces to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` for a reprocessable capture session. Once created, the session is active until a new session is created by the camera device, or the camera device is closed.

All capture sessions can be used for capturing images from the camera but only reprocessable capture sessions can reprocess images captured from the camera in the same session previously.

Creating a session is an expensive operation and can take several hundred milliseconds, since it requires configuring the camera device's internal pipelines and allocating memory buffers for sending images to the desired targets. Therefore the setup is done asynchronously, and android.hardware.camera2.CameraDevice#createCaptureSession and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` will send the ready-to-use CameraCaptureSession to the provided listener's `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onConfigured(android.hardware.camera2.CameraCaptureSession)` callback. If configuration cannot be completed, then the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onConfigureFailed(android.hardware.camera2.CameraCaptureSession)` is called, and the session will not become active.

If a new session is created by the camera device, then the previous session is closed, and its associated `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onClosed(android.hardware.camera2.CameraCaptureSession)` callback will be invoked. All of the session methods will throw an IllegalStateException if called once the session is closed.

A closed session clears any repeating requests (as if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()` had been called), but will still complete all of its in-progress capture requests as normal, before a newly created session takes over and reconfigures the camera device.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback` A callback object for tracking the progress of a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` submitted to the camera device. |
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback` A callback object for receiving updates about the state of a camera capture session. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#CameraCaptureSession()()` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()()` Discard all captures currently pending and in-progress as fast as possible. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)(request: https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Submit a request for an image to be captured by the camera device. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)(requests: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest!>, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Submit a list of requests to be captured in sequence as a burst. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurstRequests(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback)(requests: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback)` Submit a list of requests to be captured in sequence as a burst. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureSingleRequest(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback)(request: https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback)` Submit a request for an image to be captured by the camera device. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#close()()` Close this capture session asynchronously. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#finalizeOutputConfigurations(kotlin.collections.MutableList)(outputConfigs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration!>!)` Finalize the output configurations that now have their deferred and/or extra Surfaces included. |
| abstract [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#getDevice()()` Get the camera device that this session is created for. |
| abstract [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#getInputSurface()()` Get the input Surface associated with a reprocessable capture session. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#isReprocessable()()` Return if the application can submit reprocess capture requests with this camera capture session. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)(surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#)` Pre-allocate all buffers for an output Surface. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)(requests: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest!>, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Request endlessly repeating capture of a sequence of images by this capture session. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurstRequests(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback)(requests: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback)` Request endlessly repeating capture of a sequence of images by this capture session. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)(request: https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Request endlessly repeating capture of images by this capture session. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setSingleRepeatingRequest(android.hardware.camera2.CaptureRequest,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback)(request: https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback)` Request endlessly repeating capture of images by this capture session. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()()` Cancel any ongoing repeating capture set by either `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#supportsOfflineProcessing(android.view.Surface)(surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#)` Query whether a given Surface is able to support offline mode. |
| open [CameraOfflineSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession)? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#switchToOffline(kotlin.collections.MutableCollection,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraOfflineSession.CameraOfflineSessionCallback)(offlineSurfaces: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/view/Surface.html#!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession.CameraOfflineSessionCallback)` Switch the current capture session and a given set of registered camera surfaces to offline processing mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#updateOutputConfiguration(android.hardware.camera2.params.OutputConfiguration)(config: https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration!)` Update `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` after configuration finalization see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#finalizeOutputConfigurations(kotlin.collections.MutableList)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#updateOutputConfigurations(kotlin.collections.MutableList)(configurations: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration!>)` Update the output configurations for this camera session. |

## Public constructors

### CameraCaptureSession

```
CameraCaptureSession()
```

## Public methods

### abortCaptures

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun abortCaptures(): Unit
```

Discard all captures currently pending and in-progress as fast as possible.

The camera device will discard all of its current work as fast as possible. Some in-flight captures may complete successfully and call `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureCompleted(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.TotalCaptureResult)`, while others will trigger their `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureFailed(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CaptureFailure)` callbacks. If a repeating request or a repeating burst is set, it will be cleared.

This method is the fastest way to switch the camera device to a new session with android.hardware.camera2.CameraDevice#createCaptureSession or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`, at the cost of discarding in-progress work. It must be called before the new session is created. Once all pending requests are either completed or thrown away, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onReady(android.hardware.camera2.CameraCaptureSession)` callback will be called, if the session has not been closed. Otherwise, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onClosed(android.hardware.camera2.CameraCaptureSession)` callback will be fired when a new session is created by the camera device.

Cancelling will introduce at least a brief pause in the stream of data from the camera device, since once the camera device is emptied, the first new request has to make it through the entire camera pipeline before new output buffers are produced.

This means that using `abortCaptures()` to simply remove pending requests is not recommended; it's best used for quickly switching output configurations, or for cancelling long in-progress requests (such as a multi-second capture).

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`

### capture

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun capture(
    request: CaptureRequest, 
    listener: CameraCaptureSession.CaptureCallback?, 
    handler: Handler?
): Int
```

Submit a request for an image to be captured by the camera device.

The request defines all the parameters for capturing the single image, including sensor, lens, flash, and post-processing settings.

Each request will produce one `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult` and produce new frames for one or more target Surfaces, set with the CaptureRequest builder's `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface)` method. The target surfaces (set with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface)`) must be a subset of the surfaces provided when this capture session was created.

Multiple regular and reprocess requests can be in progress at once. If there are only regular requests or reprocess requests in progress, they are processed in first-in, first-out order. If there are both regular and reprocess requests in progress, regular requests are processed in first-in, first-out order and reprocess requests are processed in first-in, first-out order, respectively. However, the processing order of a regular request and a reprocess request in progress is not specified. In other words, a regular request will always be processed before regular requests that are submitted later. A reprocess request will always be processed before reprocess requests that are submitted later. However, a regular request may not be processed before reprocess requests that are submitted later.

Requests submitted through this method have higher priority than those submitted through `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, and will be processed as soon as the current repeat/repeatBurst processing completes.

All capture sessions can be used for capturing images from the camera but only capture sessions created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` can submit reprocess capture requests. Submitting a reprocess request to a regular capture session will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

Submitting a request that targets Surfaces with an unsupported dynamic range combination will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `request` | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest): the settings for this capture. This value cannot be `null`. |
| `listener` | [CameraCaptureSession.CaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback)?: The callback object to notify once this request has been processed. If null, no metadata will be produced for this capture, although image data will still be produced. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: the handler on which the listener should be invoked, or `null` to use the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int A unique capture sequence ID used by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the request targets no Surfaces or Surfaces that are not configured as outputs for this session; or the request targets a set of Surfaces that cannot be submitted simultaneously in a reprocessable capture session; or a reprocess capture request is submitted in a non-reprocessable capture session; or the reprocess capture request was created with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` from a different session; or the capture targets a Surface in the middle of being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)`; or the handler is null, the listener is not null, and the calling thread has no looper; or the request targets Surfaces with an unsupported dynamic range combination |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`

### captureBurst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun captureBurst(
    requests: MutableList<CaptureRequest!>, 
    listener: CameraCaptureSession.CaptureCallback?, 
    handler: Handler?
): Int
```

Submit a list of requests to be captured in sequence as a burst. The burst will be captured in the minimum amount of time possible, and will not be interleaved with requests submitted by other capture or repeat calls.

Regular and reprocess requests can be mixed together in a single burst. Regular requests will be captured in order and reprocess requests will be processed in order, respectively. However, the processing order between a regular request and a reprocess request is not specified. Each capture produces one `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult` and image buffers for one or more target `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. The target surfaces (set with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface)`) must be a subset of the surfaces provided when this capture session was created.

The main difference between this method and simply calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` repeatedly is that this method guarantees that no other requests will be interspersed with the burst.

All capture sessions can be used for capturing images from the camera but only capture sessions created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` can submit reprocess capture requests. Submitting a reprocess request to a regular capture session will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

Submitting a request that targets Surfaces with an unsupported dynamic range combination will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `requests` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest)!\>: the list of settings for this burst capture. This value cannot be `null`. |
| `listener` | [CameraCaptureSession.CaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback)?: The callback object to notify each time one of the requests in the burst has been processed. If null, no metadata will be produced for any requests in this burst, although image data will still be produced. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: the handler on which the listener should be invoked, or `null` to use the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int A unique capture sequence ID used by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | If the requests target no Surfaces, or the requests target Surfaces not currently configured as outputs; or one of the requests targets a set of Surfaces that cannot be submitted simultaneously in a reprocessable capture session; or a reprocess capture request is submitted in a non-reprocessable capture session; or one of the reprocess capture requests was created with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` from a different session; or one of the captures targets a Surface in the middle of being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)`; or if the handler is null, the listener is not null, and the calling thread has no looper; or the request targets Surfaces with an unsupported dynamic range combination. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`

### captureBurstRequests

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun captureBurstRequests(
    requests: MutableList<CaptureRequest!>, 
    executor: Executor, 
    listener: CameraCaptureSession.CaptureCallback
): Int
```

Submit a list of requests to be captured in sequence as a burst. The burst will be captured in the minimum amount of time possible, and will not be interleaved with requests submitted by other capture or repeat calls.

The behavior of this method matches that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, except that it uses `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` as an argument instead of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

| Parameters ||
|---|---|
| `requests` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest)!\>: the list of settings for this burst capture. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor which will be used for invoking the listener. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [CameraCaptureSession.CaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback): The callback object to notify each time one of the requests in the burst has been processed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int A unique capture sequence ID used by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | If the requests target no Surfaces, or the requests target Surfaces not currently configured as outputs; or one of the requests targets a set of Surfaces that cannot be submitted simultaneously in a reprocessable capture session; or a reprocess capture request is submitted in a non-reprocessable capture session; or one of the reprocess capture requests was created with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` from a different session; or one of the captures targets a Surface in the middle of being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)`; or if the executor is null; or if the listener is null; or the request targets Surfaces with an unsupported dynamic range combination. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`

### captureSingleRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun captureSingleRequest(
    request: CaptureRequest, 
    executor: Executor, 
    listener: CameraCaptureSession.CaptureCallback
): Int
```

Submit a request for an image to be captured by the camera device.

The behavior of this method matches that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, except that it uses `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` as an argument instead of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

| Parameters ||
|---|---|
| `request` | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest): the settings for this capture. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor which will be used for invoking the listener. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [CameraCaptureSession.CaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback): The callback object to notify once this request has been processed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int A unique capture sequence ID used by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the request targets no Surfaces or Surfaces that are not configured as outputs for this session; or the request targets a set of Surfaces that cannot be submitted simultaneously in a reprocessable capture session; or a reprocess capture request is submitted in a non-reprocessable capture session; or the reprocess capture request was created with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` from a different session; or the capture targets a Surface in the middle of being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)`; or the executor is null, or the listener is not null; or the request targets Surfaces with an unsupported dynamic range combination; |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`

### close

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun close(): Unit
```

Close this capture session asynchronously.

Closing a session frees up the target output Surfaces of the session for reuse with either a new session, or to other APIs that can draw to Surfaces.

Note that for common usage scenarios like creating a new session or closing the camera device, it is faster to call respective APIs directly (see below for more details) without calling into this method. This API is only useful when application wants to unconfigure the camera but keep the device open for later use.

Creating a new capture session with android.hardware.camera2.CameraDevice#createCaptureSession will close any existing capture session automatically, and call the older session listener's `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onClosed(android.hardware.camera2.CameraCaptureSession)` callback. Using android.hardware.camera2.CameraDevice#createCaptureSession directly without closing is the recommended approach for quickly switching to a new session, since unchanged target outputs can be reused more efficiently.

Closing the device with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#close()` directly without calling this API is also recommended for quickly closing the camera.

Once a session is closed, all methods on it will throw an IllegalStateException, and any repeating requests or bursts are stopped (as if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()` was called). However, any in-progress capture requests submitted to the session will be completed as normal; once all captures have completed and the session has been torn down, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onClosed(android.hardware.camera2.CameraCaptureSession)` will be called.

Closing a session is idempotent; closing more than once has no effect.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### finalizeOutputConfigurations

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun finalizeOutputConfigurations(outputConfigs: MutableList<OutputConfiguration!>!): Unit
```

Finalize the output configurations that now have their deferred and/or extra Surfaces included.

For camera use cases where a preview and other output configurations need to be configured, it can take some time for the preview Surface to be ready. For example, if the preview Surface is obtained from `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`, the SurfaceView will only be ready after the UI layout is done, potentially delaying camera startup.

To speed up camera startup time, the application can configure the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#` with the eventual preview size (via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#OutputConfiguration(android.util.Size,%20java.lang.Class)`), and defer the preview output configuration until the Surface is ready. After the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#` is created successfully with this deferred output and other normal outputs, the application can start submitting requests as long as they do not include deferred output Surfaces. Once a deferred Surface is ready, the application can add the Surface to the deferred output configuration with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#addSurface(android.view.Surface)` method, and then update the deferred output configuration via this method, before it can submit capture requests with this output target.

This function can also be called in case where multiple surfaces share the same OutputConfiguration, and one of the surfaces becomes available after the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#` is created. In that case, the application must first create the OutputConfiguration with the available Surface, then enable further surface sharing via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#enableSurfaceSharing()`, before creating the CameraCaptureSession. After the CameraCaptureSession is created, and once the extra Surface becomes available, the application must then call `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#addSurface(android.view.Surface)` before finalizing the configuration with this method.

If the provided OutputConfigurations are unchanged from session creation, this function call has no effect. This function must only be called once for a particular output configuration.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` deferred Surfaces can be dynamically updated by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#updateOutputConfigurations(kotlin.collections.MutableList)`. Using deferred surface updates, clients will no longer be limited to finalizing surfaces a single time and will be enabled to switch to and from deferred surface state at any time.

The output Surfaces included by this list of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` can be used as `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` targets as soon as this call returns.

This method is not supported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int`-level devices.

| Parameters ||
|---|---|
| `outputConfigs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!\>!: a list of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` that have had `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#addSurface(android.view.Surface)` invoked with a valid output Surface after `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSessionByOutputConfigurations(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error. |
| `java.lang.IllegalArgumentException` | for invalid output configurations, including ones where the source of the Surface is no longer valid or the Surface is from a unsupported source. Or if one of the output configuration was already finished with an included surface in a prior call. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created, or the camera device has been closed. |

### getDevice

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDevice(): CameraDevice
```

Get the camera device that this session is created for.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice` | This value cannot be `null`. |

### getInputSurface

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInputSurface(): Surface?
```

Get the input Surface associated with a reprocessable capture session.

Each reprocessable capture session has an input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` where the reprocess capture requests get the input images from, rather than the camera device. The application can create a `https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#` with this input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` and use it to provide input images for reprocess capture requests. When the reprocessable capture session is closed, the input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` is abandoned and becomes invalid.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Surface.html#?` | The `https://developer.android.com/reference/kotlin/android/view/Surface.html#` where reprocessing capture requests get the input images from. If this is not a reprocess capture session, `null` will be returned. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#`
- `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#`

### isReprocessable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isReprocessable(): Boolean
```

Return if the application can submit reprocess capture requests with this camera capture session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the application can submit reprocess capture requests with this camera capture session. `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`

### prepare

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun prepare(surface: Surface): Unit
```

Pre-allocate all buffers for an output Surface.

Normally, the image buffers for a given output Surface are allocated on-demand, to minimize startup latency and memory overhead.

However, in some cases, it may be desirable for the buffers to be allocated before any requests targeting the Surface are actually submitted to the device. Large buffers may take some time to allocate, which can result in delays in submitting requests until sufficient buffers are allocated to reach steady-state behavior. Such delays can cause bursts to take longer than desired, or cause skips or stutters in preview output.

The prepare() method can be used to perform this preallocation. It may only be called for a given output Surface before that Surface is used as a target for a request. The number of buffers allocated is the sum of the count needed by the consumer providing the output Surface, and the maximum number needed by the camera device to fill its pipeline. Since this may be a larger number than what is actually required for steady-state operation, using prepare may result in higher memory consumption than the normal on-demand behavior results in. Prepare() will also delay the time to first output to a given Surface, in exchange for smoother frame rate once the allocation is complete.

For example, an application that creates an android.media.ImageReader#newInstance with a maxImages argument of 10, but only uses 3 simultaneous Images at once would normally only cause those 3 images to be allocated (plus what is needed by the camera device for smooth operation). But using prepare() on the ImageReader Surface will result in all 10 Images being allocated. So applications using this method should take care to request only the number of buffers actually necessary for their application.

If the same output Surface is used in consecutive sessions (without closing the first session explicitly), then its already-allocated buffers are carried over, and if it was used as a target of a capture request in the first session, prepare cannot be called on it in the second session.

Once allocation is complete, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onSurfacePrepared(android.hardware.camera2.CameraCaptureSession,%20android.view.Surface)` will be invoked with the Surface provided to this method. Between the prepare call and the onSurfacePrepared call, the Surface provided to prepare must not be used as a target of a CaptureRequest submitted to this session.

Note that if 2 surfaces share the same stream via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#enableSurfaceSharing()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#addSurface(android.view.Surface)`, prepare() only needs to be called on one surface, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onSurfacePrepared(android.hardware.camera2.CameraCaptureSession,%20android.view.Surface)` will be triggered for both surfaces.

`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int` devices cannot pre-allocate output buffers; for those devices, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onSurfacePrepared(android.hardware.camera2.CameraCaptureSession,%20android.view.Surface)` will be immediately called, and no preallocation is done.

| Parameters ||
|---|---|
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#): the output Surface for which buffers should be pre-allocated. Must be one of the output Surfaces used to create this session. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the Surface is invalid, not part of this Session, or has already been used as a target of a CaptureRequest in this session or immediately prior sessions. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onSurfacePrepared(android.hardware.camera2.CameraCaptureSession,%20android.view.Surface)`

### setRepeatingBurst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setRepeatingBurst(
    requests: MutableList<CaptureRequest!>, 
    listener: CameraCaptureSession.CaptureCallback?, 
    handler: Handler?
): Int
```

Request endlessly repeating capture of a sequence of images by this capture session.

With this method, the camera device will continually capture images, cycling through the settings in the provided list of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest`, at the maximum rate possible.

If a request is submitted through `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, the current repetition of the request list will be completed before the higher-priority request is handled. This guarantees that the application always receives a complete repeat burst captured in minimal time, instead of bursts interleaved with higher-priority captures, or incomplete captures.

Repeating burst requests are a simple way for an application to maintain a preview or other continuous stream of frames where each request is different in a predictable way, without having to continually submit requests through `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`.

To stop the repeating capture, call `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()`. Any ongoing burst will still be completed, however. Calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()` will also clear the request.

Calling this method will replace a previously-set repeating request or burst set up by this method or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, although any in-progress burst will be completed before the new repeat burst will be used.

This method does not support reprocess capture requests because each reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` must be created from the `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` that matches the input image to be reprocessed. This is either the `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` of capture that is sent for reprocessing, or one of the `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` of a set of captures, when data from the whole set is combined by the application into a single reprocess input image. The request must be capturing images from the camera. If a reprocess capture request is submitted, this method will throw IllegalArgumentException.

Submitting a request that targets Surfaces with an unsupported dynamic range combination will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `requests` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest)!\>: the list of requests to cycle through indefinitely. This value cannot be `null`. |
| `listener` | [CameraCaptureSession.CaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback)?: The callback object to notify each time one of the requests in the repeating bursts has finished processing. If null, no metadata will be produced for this stream of requests, although image data will still be produced. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: the handler on which the listener should be invoked, or `null` to use the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int A unique capture sequence ID used by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | If the requests reference no Surfaces or reference Surfaces not currently configured as outputs; or one of the requests is a reprocess capture request; or one of the captures targets a Surface in the middle of being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)`; or the handler is null, the listener is not null, and the calling thread has no looper; or no requests were passed in; or the request targets Surfaces with an unsupported dynamic range combination. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`

### setRepeatingBurstRequests

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRepeatingBurstRequests(
    requests: MutableList<CaptureRequest!>, 
    executor: Executor, 
    listener: CameraCaptureSession.CaptureCallback
): Int
```

Request endlessly repeating capture of a sequence of images by this capture session.

The behavior of this method matches that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, except that it uses `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` as an argument instead of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

| Parameters ||
|---|---|
| `requests` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest)!\>: the list of requests to cycle through indefinitely. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor which will be used for invoking the listener. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [CameraCaptureSession.CaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback): The callback object to notify each time one of the requests in the repeating bursts has finished processing. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int A unique capture sequence ID used by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | If the requests reference no Surfaces or reference Surfaces not currently configured as outputs; or one of the requests is a reprocess capture request; or one of the captures targets a Surface in the middle of being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)`; or the executor is null; or the listener is null; or the request targets Surfaces with an unsupported dynamic range combination. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`

### setRepeatingRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setRepeatingRequest(
    request: CaptureRequest, 
    listener: CameraCaptureSession.CaptureCallback?, 
    handler: Handler?
): Int
```

Request endlessly repeating capture of images by this capture session.

With this method, the camera device will continually capture images using the settings in the provided `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest`, at the maximum rate possible.

Repeating requests are a simple way for an application to maintain a preview or other continuous stream of frames, without having to continually submit identical requests through `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`.

Repeat requests have lower priority than those submitted through `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, so if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` is called when a repeating request is active, the capture request will be processed before any further repeating requests are processed.

To stop the repeating capture, call `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()`. Calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()` will also clear the request.

Calling this method will replace any earlier repeating request or burst set up by this method or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, although any in-progress burst will be completed before the new repeat request will be used.

This method does not support reprocess capture requests because each reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` must be created from the `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` that matches the input image to be reprocessed. This is either the `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` of capture that is sent for reprocessing, or one of the `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult` of a set of captures, when data from the whole set is combined by the application into a single reprocess input image. The request must be capturing images from the camera. If a reprocess capture request is submitted, this method will throw IllegalArgumentException.

Submitting a request that targets Surfaces with an unsupported dynamic range combination will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `request` | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest): the request to repeat indefinitely. This value cannot be `null`. |
| `listener` | [CameraCaptureSession.CaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback)?: The callback object to notify every time the request finishes processing. If null, no metadata will be produced for this stream of requests, although image data will still be produced. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?: the handler on which the listener should be invoked, or `null` to use the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int A unique capture sequence ID used by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | If the request references no Surfaces or references Surfaces that are not currently configured as outputs; or the request is a reprocess capture request; or the capture targets a Surface in the middle of being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)`; or the handler is null, the listener is not null, and the calling thread has no looper; or no requests were passed in; or the request targets Surfaces with an unsupported dynamic range combination. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`

### setSingleRepeatingRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSingleRepeatingRequest(
    request: CaptureRequest, 
    executor: Executor, 
    listener: CameraCaptureSession.CaptureCallback
): Int
```

Request endlessly repeating capture of images by this capture session.

The behavior of this method matches that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, except that it uses `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` as an argument instead of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

| Parameters ||
|---|---|
| `request` | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest): the request to repeat indefinitely. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the executor which will be used for invoking the listener. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [CameraCaptureSession.CaptureCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback): The callback object to notify every time the request finishes processing. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int A unique capture sequence ID used by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | If the request references no Surfaces or references Surfaces that are not currently configured as outputs; or the request is a reprocess capture request; or the capture targets a Surface in the middle of being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#prepare(android.view.Surface)`; or the executor is null; or the listener is null; or the request targets Surfaces with an unsupported dynamic range combination. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#stopRepeating()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`

### stopRepeating

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun stopRepeating(): Unit
```

Cancel any ongoing repeating capture set by either `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`. Has no effect on requests submitted through `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`.

Any currently in-flight captures will still complete, as will any burst that is mid-capture. To ensure that the device has finished processing all of its capture requests and is in ready state, wait for the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onReady(android.hardware.camera2.CameraCaptureSession)` callback after calling this method.

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onReady(android.hardware.camera2.CameraCaptureSession)`

### supportsOfflineProcessing

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun supportsOfflineProcessing(surface: Surface): Boolean
```

Query whether a given Surface is able to support offline mode.

Surfaces that support offline mode can be passed as arguments to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#switchToOffline(kotlin.collections.MutableCollection,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraOfflineSession.CameraOfflineSessionCallback)`.

| Parameters ||
|---|---|
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#): An input/output surface that was used to create this session or the result of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#getInputSurface()`. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the surface can support offline mode and can be passed as argument to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#switchToOffline(kotlin.collections.MutableCollection,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraOfflineSession.CameraOfflineSessionCallback)`. `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if an attempt was made to pass a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` that was not registered with this capture session. |
| `java.lang.UnsupportedOperationException` | if an attempt was made to call this method using unsupported camera capture session like `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#switchToOffline(kotlin.collections.MutableCollection,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraOfflineSession.CameraOfflineSessionCallback)`

### switchToOffline

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun switchToOffline(
    offlineSurfaces: MutableCollection<Surface!>, 
    executor: Executor, 
    listener: CameraOfflineSession.CameraOfflineSessionCallback
): CameraOfflineSession?
```

Switch the current capture session and a given set of registered camera surfaces to offline processing mode.

Devices support this method will report `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING:kotlin.Int` capability in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`. When this method is supported, applications can use it to improve the latency of closing camera or recreating capture session without losing the in progress capture request outputs.

Offline processing mode and the corresponding `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession` differ from a regular online camera capture session in several ways. Successful offline switches will close the currently active camera capture session. Camera clients are also allowed to call `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#close()` while offline processing of selected capture requests is still in progress. Such side effects free device close is only possible when the offline session moves to the ready state. Once this happens, closing the camera device will not affect the pending offline requests and they must complete as normal.

Offline processing mode switches may need several hundred milliseconds to complete as the underlying camera implementation must abort all currently active repeating requests as well as all other pending requests not specified by the client. Additionally the switch will be blocked until all requests that continue processing within the offline session acquire their initial input frame from camera sensor. The call to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#switchToOffline(kotlin.collections.MutableCollection,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraOfflineSession.CameraOfflineSessionCallback)` itself is not blocking and will only trigger the offline switch sequence. Clients will be notified via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession.CameraOfflineSessionCallback#onReady(android.hardware.camera2.CameraOfflineSession)` once the entire sequence is complete.

Please note that after a successful call to this method the currently active capture session will no longer be valid and clients will begin receiving capture callbacks with a corresponding `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession` passed as a session argument.

| Parameters ||
|---|---|
| `offlineSurfaces` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)!\>: Client-specified collection of input/output camera registered surfaces that need to be switched to offline mode along with their pending capture requests. Do note that not all camera registered surfaces can be switched to offline mode. Offline processing support for individual surfaces can be queried using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#supportsOfflineProcessing(android.view.Surface)`. Additionally offline mode switches are not available for shared surfaces `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#enableSurfaceSharing()` and surfaces as part of a surface group. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor which will be used for invoking the offline callback listener. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [CameraOfflineSession.CameraOfflineSessionCallback](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession.CameraOfflineSessionCallback): The callback object to notify for offline session events. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession?` | camera offline session which in case of successful offline switch will move in ready state after clients receive `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession.CameraOfflineSessionCallback#onReady(android.hardware.camera2.CameraOfflineSession)`. In case the offline switch was not successful clients will receive respective `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession.CameraOfflineSessionCallback#onSwitchFailed(android.hardware.camera2.CameraOfflineSession)` notification. This value may be `null`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error. |
| `java.lang.IllegalArgumentException` | if an attempt was made to pass a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` that was not registered with this capture session or a shared surface `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#enableSurfaceSharing()` or surface as part of a surface group. The current capture session will remain valid and active in case of this exception. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession.CameraOfflineSessionCallback`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#supportsOfflineProcessing(android.view.Surface)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING:kotlin.Int`

### updateOutputConfiguration

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateOutputConfiguration(config: OutputConfiguration!): Unit
```

Update `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` after configuration finalization see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#finalizeOutputConfigurations(kotlin.collections.MutableList)`.

Any `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` that has been modified via calls to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#addSurface(android.view.Surface)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#removeSurface(android.view.Surface)` must be updated. After the update call returns without throwing exceptions any newly added surfaces can be referenced in subsequent capture requests.

Surfaces that get removed must not be part of any active repeating or single/burst request or have any pending results. Consider updating any repeating requests first via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` and then wait for the last frame number when the sequence completes `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)` before calling updateOutputConfiguration to remove a previously active Surface.

Surfaces that get added must not be part of any other registered `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration`.

| Parameters ||
|---|---|
| `config` | [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!: Modified output configuration. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error. |
| `java.lang.IllegalArgumentException` | if an attempt was made to add a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` already in use by another buffer-producing API, such as MediaCodec or a different camera device or `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration`; or new surfaces are not compatible (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#enableSurfaceSharing()`); or a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` that was removed from the modified `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` still has pending requests. |
| `java.lang.IllegalStateException` | if this session is no longer active, either because the session was explicitly closed, a new session has been created or the camera device has been closed. |

### updateOutputConfigurations

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateOutputConfigurations(configurations: MutableList<OutputConfiguration!>): Unit
```

Update the output configurations for this camera session.

This method allows for updating the surfaces associated with the currently configured output `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration`. It is used to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#addSurface(android.view.Surface)` `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#makeDeferredAndRemoveSurfaces()` surfaces with active surface instances or to swap surfaces for seamless transitions between use cases without re-initializing the entire camera session.

The number of provided configurations must match the number of currently configured outputs. Each provided `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` must correspond to an already existing output configuration passed previously to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`. The `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` is identified by its properties (size, format, etc.), but can have a new surface associated with it (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#addSurface(android.view.Surface)`) or be marked as deferred (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#makeDeferredAndRemoveSurfaces()`).

This method is not for adding or removing new `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration`.

Any active requests that target replaced surfaces will be stopped by this call. When a surface with active capture requests is replaced, the framework will keep track of the old surface to ensure that any in-flight buffers can return successfully before the connection is terminated.

| Parameters ||
|---|---|
| `configurations` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration)!\>: A list of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` objects with the updated surface information. The size of this list must be equal to the number of currently configured outputs. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device has encountered a fatal error, or if the update operation fails. |
| `java.lang.IllegalArgumentException` | if the list of configurations is invalid (e.g., wrong size, or contains an unknown configuration). |
