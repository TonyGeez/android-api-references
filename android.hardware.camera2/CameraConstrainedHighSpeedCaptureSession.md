Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraConstrainedHighSpeedCaptureSession

```
abstract class CameraConstrainedHighSpeedCaptureSession : CameraCaptureSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.hardware.camera2.CameraCaptureSession](CameraCaptureSession.md) ||
| | ↳ | [android.hardware.camera2.CameraConstrainedHighSpeedCaptureSession](CameraConstrainedHighSpeedCaptureSession.md) |

A constrained high speed capture session for a CameraDevice, used for capturing high speed images from the CameraDevice for high speed video recording use case.

A CameraConstrainedHighSpeedCaptureSession is created by providing a session configuration to android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration) with a type of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int`. The CameraCaptureSession returned from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback` can then be cast to a CameraConstrainedHighSpeedCaptureSession. Once created, the session is active until a new session is created by the camera device, or the camera device is closed.

An active high speed capture session is a specialized capture session that is only targeted at high speed video recording (\>=120fps) use case if the camera device supports high speed video capability (i.e., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int`). It only accepts request lists created via createHighSpeedRequestList, and the request list can only be submitted to this session via captureBurst, or setRepeatingBurst. See createCaptureSession for more details of the limitations.

Creating a session is an expensive operation and can take several hundred milliseconds, since it requires configuring the camera device's internal pipelines and allocating memory buffers for sending images to the desired targets. Therefore the setup is done asynchronously, and createConstrainedHighSpeedCaptureSession will send the ready-to-use CameraCaptureSession to the provided listener's onConfigured callback. If configuration cannot be completed, then the onConfigureFailed is called, and the session will not become active.

If a new session is created by the camera device, then the previous session is closed, and its associated onClosed callback will be invoked. All of the session methods will throw an IllegalStateException if called once the session is closed.

A closed session clears any repeating requests (as if stopRepeating had been called), but will still complete all of its in-progress capture requests as normal, before a newly created session takes over and reconfigures the camera device.

## Summary

| Public constructors ||
|---|---|
| CameraConstrainedHighSpeedCaptureSession <br /> |

| Public methods ||
|---|---|
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest](CaptureRequest.md)!\> | createHighSpeedRequestList Create a unmodifiable list of requests that is suitable for constrained high speed capture session streaming. |

Inherited functions From class CameraCaptureSession `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` abortCaptures

<br />

Discard all captures currently pending and in-progress as fast as possible.

The camera device will discard all of its current work as fast as possible. Some in-flight captures may complete successfully and call onCaptureCompleted, while others will trigger their onCaptureFailed callbacks. If a repeating request or a repeating burst is set, it will be cleared.

This method is the fastest way to switch the camera device to a new session with android.hardware.camera2.CameraDevice#createCaptureSession or createReprocessableCaptureSession, at the cost of discarding in-progress work. It must be called before the new session is created. Once all pending requests are either completed or thrown away, the onReady callback will be called, if the session has not been closed. Otherwise, the onClosed callback will be fired when a new session is created by the camera device.

Cancelling will introduce at least a brief pause in the stream of data from the camera device, since once the camera device is emptied, the first new request has to make it through the entire camera pipeline before new output buffers are produced.

This means that using `abortCaptures()` to simply remove pending requests is not recommended; it's best used for quickly switching output configurations, or for cancelling long in-progress requests (such as a multi-second capture).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` capture

<br />

Submit a request for an image to be captured by the camera device.

The request defines all the parameters for capturing the single image, including sensor, lens, flash, and post-processing settings.

Each request will produce one CaptureResult and produce new frames for one or more target Surfaces, set with the CaptureRequest builder's addTarget method. The target surfaces (set with addTarget) must be a subset of the surfaces provided when this capture session was created.

Multiple regular and reprocess requests can be in progress at once. If there are only regular requests or reprocess requests in progress, they are processed in first-in, first-out order. If there are both regular and reprocess requests in progress, regular requests are processed in first-in, first-out order and reprocess requests are processed in first-in, first-out order, respectively. However, the processing order of a regular request and a reprocess request in progress is not specified. In other words, a regular request will always be processed before regular requests that are submitted later. A reprocess request will always be processed before reprocess requests that are submitted later. However, a regular request may not be processed before reprocess requests that are submitted later.

<br />

Requests submitted through this method have higher priority than those submitted through setRepeatingRequest or setRepeatingBurst, and will be processed as soon as the current repeat/repeatBurst processing completes.

All capture sessions can be used for capturing images from the camera but only capture sessions created by createReprocessableCaptureSession can submit reprocess capture requests. Submitting a reprocess request to a regular capture session will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

Submitting a request that targets Surfaces with an unsupported dynamic range combination will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` captureBurst

<br />

Submit a list of requests to be captured in sequence as a burst. The burst will be captured in the minimum amount of time possible, and will not be interleaved with requests submitted by other capture or repeat calls.

Regular and reprocess requests can be mixed together in a single burst. Regular requests will be captured in order and reprocess requests will be processed in order, respectively. However, the processing order between a regular request and a reprocess request is not specified. Each capture produces one CaptureResult and image buffers for one or more target `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. The target surfaces (set with addTarget) must be a subset of the surfaces provided when this capture session was created.

The main difference between this method and simply calling capture repeatedly is that this method guarantees that no other requests will be interspersed with the burst.

All capture sessions can be used for capturing images from the camera but only capture sessions created by createReprocessableCaptureSession can submit reprocess capture requests. Submitting a reprocess request to a regular capture session will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

Submitting a request that targets Surfaces with an unsupported dynamic range combination will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` captureBurstRequests

<br />

Submit a list of requests to be captured in sequence as a burst. The burst will be captured in the minimum amount of time possible, and will not be interleaved with requests submitted by other capture or repeat calls.

The behavior of this method matches that of captureBurst, except that it uses `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` as an argument instead of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` captureSingleRequest

<br />

Submit a request for an image to be captured by the camera device.

The behavior of this method matches that of capture, except that it uses `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` as an argument instead of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` close

<br />

Close this capture session asynchronously.

Closing a session frees up the target output Surfaces of the session for reuse with either a new session, or to other APIs that can draw to Surfaces.

Note that for common usage scenarios like creating a new session or closing the camera device, it is faster to call respective APIs directly (see below for more details) without calling into this method. This API is only useful when application wants to unconfigure the camera but keep the device open for later use.

Creating a new capture session with android.hardware.camera2.CameraDevice#createCaptureSession will close any existing capture session automatically, and call the older session listener's onClosed callback. Using android.hardware.camera2.CameraDevice#createCaptureSession directly without closing is the recommended approach for quickly switching to a new session, since unchanged target outputs can be reused more efficiently.

Closing the device with close directly without calling this API is also recommended for quickly closing the camera.

Once a session is closed, all methods on it will throw an IllegalStateException, and any repeating requests or bursts are stopped (as if stopRepeating was called). However, any in-progress capture requests submitted to the session will be completed as normal; once all captures have completed and the session has been torn down, onClosed will be called.

Closing a session is idempotent; closing more than once has no effect.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` finalizeOutputConfigurations

<br />

Finalize the output configurations that now have their deferred and/or extra Surfaces included.

For camera use cases where a preview and other output configurations need to be configured, it can take some time for the preview Surface to be ready. For example, if the preview Surface is obtained from `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`, the SurfaceView will only be ready after the UI layout is done, potentially delaying camera startup.

To speed up camera startup time, the application can configure the CameraCaptureSession with the eventual preview size (via OutputConfiguration), and defer the preview output configuration until the Surface is ready. After the CameraCaptureSession is created successfully with this deferred output and other normal outputs, the application can start submitting requests as long as they do not include deferred output Surfaces. Once a deferred Surface is ready, the application can add the Surface to the deferred output configuration with the addSurface method, and then update the deferred output configuration via this method, before it can submit capture requests with this output target.

This function can also be called in case where multiple surfaces share the same OutputConfiguration, and one of the surfaces becomes available after the CameraCaptureSession is created. In that case, the application must first create the OutputConfiguration with the available Surface, then enable further surface sharing via enableSurfaceSharing, before creating the CameraCaptureSession. After the CameraCaptureSession is created, and once the extra Surface becomes available, the application must then call addSurface before finalizing the configuration with this method.

If the provided OutputConfigurations are unchanged from session creation, this function call has no effect. This function must only be called once for a particular output configuration.

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` deferred Surfaces can be dynamically updated by calling updateOutputConfigurations. Using deferred surface updates, clients will no longer be limited to finalizing surfaces a single time and will be enabled to switch to and from deferred surface state at any time.

The output Surfaces included by this list of OutputConfiguration can be used as CaptureRequest targets as soon as this call returns.

This method is not supported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int`-level devices.

<br />

CameraDevice getDevice

<br />

Get the camera device that this session is created for.

<br />

`https://developer.android.com/reference/kotlin/android/view/Surface.html#?` getInputSurface

<br />

Get the input Surface associated with a reprocessable capture session.

Each reprocessable capture session has an input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` where the reprocess capture requests get the input images from, rather than the camera device. The application can create a `https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#` with this input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` and use it to provide input images for reprocess capture requests. When the reprocessable capture session is closed, the input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` is abandoned and becomes invalid.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isReprocessable

<br />

Return if the application can submit reprocess capture requests with this camera capture session.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` prepare

<br />

Pre-allocate all buffers for an output Surface.

Normally, the image buffers for a given output Surface are allocated on-demand, to minimize startup latency and memory overhead.

However, in some cases, it may be desirable for the buffers to be allocated before any requests targeting the Surface are actually submitted to the device. Large buffers may take some time to allocate, which can result in delays in submitting requests until sufficient buffers are allocated to reach steady-state behavior. Such delays can cause bursts to take longer than desired, or cause skips or stutters in preview output.

The prepare() method can be used to perform this preallocation. It may only be called for a given output Surface before that Surface is used as a target for a request. The number of buffers allocated is the sum of the count needed by the consumer providing the output Surface, and the maximum number needed by the camera device to fill its pipeline. Since this may be a larger number than what is actually required for steady-state operation, using prepare may result in higher memory consumption than the normal on-demand behavior results in. Prepare() will also delay the time to first output to a given Surface, in exchange for smoother frame rate once the allocation is complete.

For example, an application that creates an android.media.ImageReader#newInstance with a maxImages argument of 10, but only uses 3 simultaneous Images at once would normally only cause those 3 images to be allocated (plus what is needed by the camera device for smooth operation). But using prepare() on the ImageReader Surface will result in all 10 Images being allocated. So applications using this method should take care to request only the number of buffers actually necessary for their application.

If the same output Surface is used in consecutive sessions (without closing the first session explicitly), then its already-allocated buffers are carried over, and if it was used as a target of a capture request in the first session, prepare cannot be called on it in the second session.

Once allocation is complete, onSurfacePrepared will be invoked with the Surface provided to this method. Between the prepare call and the onSurfacePrepared call, the Surface provided to prepare must not be used as a target of a CaptureRequest submitted to this session.

Note that if 2 surfaces share the same stream via enableSurfaceSharing and addSurface, prepare() only needs to be called on one surface, and onSurfacePrepared will be triggered for both surfaces.

`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int` devices cannot pre-allocate output buffers; for those devices, onSurfacePrepared will be immediately called, and no preallocation is done.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` setRepeatingBurst

<br />

Request endlessly repeating capture of a sequence of images by this capture session.

With this method, the camera device will continually capture images, cycling through the settings in the provided list of CaptureRequest, at the maximum rate possible.

If a request is submitted through capture or captureBurst, the current repetition of the request list will be completed before the higher-priority request is handled. This guarantees that the application always receives a complete repeat burst captured in minimal time, instead of bursts interleaved with higher-priority captures, or incomplete captures.

Repeating burst requests are a simple way for an application to maintain a preview or other continuous stream of frames where each request is different in a predictable way, without having to continually submit requests through captureBurst.

To stop the repeating capture, call stopRepeating. Any ongoing burst will still be completed, however. Calling abortCaptures will also clear the request.

Calling this method will replace a previously-set repeating request or burst set up by this method or setRepeatingRequest, although any in-progress burst will be completed before the new repeat burst will be used.

This method does not support reprocess capture requests because each reprocess CaptureRequest must be created from the TotalCaptureResult that matches the input image to be reprocessed. This is either the TotalCaptureResult of capture that is sent for reprocessing, or one of the TotalCaptureResult of a set of captures, when data from the whole set is combined by the application into a single reprocess input image. The request must be capturing images from the camera. If a reprocess capture request is submitted, this method will throw IllegalArgumentException.

Submitting a request that targets Surfaces with an unsupported dynamic range combination will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` setRepeatingBurstRequests

<br />

Request endlessly repeating capture of a sequence of images by this capture session.

The behavior of this method matches that of setRepeatingBurst, except that it uses `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` as an argument instead of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` setRepeatingRequest

<br />

Request endlessly repeating capture of images by this capture session.

With this method, the camera device will continually capture images using the settings in the provided CaptureRequest, at the maximum rate possible.

Repeating requests are a simple way for an application to maintain a preview or other continuous stream of frames, without having to continually submit identical requests through capture.

Repeat requests have lower priority than those submitted through capture or captureBurst, so if capture is called when a repeating request is active, the capture request will be processed before any further repeating requests are processed.

<br />

To stop the repeating capture, call stopRepeating. Calling abortCaptures will also clear the request.

Calling this method will replace any earlier repeating request or burst set up by this method or setRepeatingBurst, although any in-progress burst will be completed before the new repeat request will be used.

This method does not support reprocess capture requests because each reprocess CaptureRequest must be created from the TotalCaptureResult that matches the input image to be reprocessed. This is either the TotalCaptureResult of capture that is sent for reprocessing, or one of the TotalCaptureResult of a set of captures, when data from the whole set is combined by the application into a single reprocess input image. The request must be capturing images from the camera. If a reprocess capture request is submitted, this method will throw IllegalArgumentException.

Submitting a request that targets Surfaces with an unsupported dynamic range combination will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` setSingleRepeatingRequest

<br />

Request endlessly repeating capture of images by this capture session.

The behavior of this method matches that of setRepeatingRequest, except that it uses `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` as an argument instead of `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` stopRepeating

<br />

Cancel any ongoing repeating capture set by either setRepeatingRequest or setRepeatingBurst. Has no effect on requests submitted through capture or captureBurst.

Any currently in-flight captures will still complete, as will any burst that is mid-capture. To ensure that the device has finished processing all of its capture requests and is in ready state, wait for the onReady callback after calling this method.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` supportsOfflineProcessing

<br />

Query whether a given Surface is able to support offline mode.

Surfaces that support offline mode can be passed as arguments to switchToOffline.

<br />

CameraOfflineSession switchToOffline

<br />

Switch the current capture session and a given set of registered camera surfaces to offline processing mode.

Devices support this method will report `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING:kotlin.Int` capability in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`. When this method is supported, applications can use it to improve the latency of closing camera or recreating capture session without losing the in progress capture request outputs.

Offline processing mode and the corresponding CameraOfflineSession differ from a regular online camera capture session in several ways. Successful offline switches will close the currently active camera capture session. Camera clients are also allowed to call close while offline processing of selected capture requests is still in progress. Such side effects free device close is only possible when the offline session moves to the ready state. Once this happens, closing the camera device will not affect the pending offline requests and they must complete as normal.

Offline processing mode switches may need several hundred milliseconds to complete as the underlying camera implementation must abort all currently active repeating requests as well as all other pending requests not specified by the client. Additionally the switch will be blocked until all requests that continue processing within the offline session acquire their initial input frame from camera sensor. The call to switchToOffline itself is not blocking and will only trigger the offline switch sequence. Clients will be notified via onReady once the entire sequence is complete.

Please note that after a successful call to this method the currently active capture session will no longer be valid and clients will begin receiving capture callbacks with a corresponding CameraOfflineSession passed as a session argument.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` updateOutputConfiguration

<br />

Update OutputConfiguration after configuration finalization see finalizeOutputConfigurations.

Any OutputConfiguration that has been modified via calls to addSurface or removeSurface must be updated. After the update call returns without throwing exceptions any newly added surfaces can be referenced in subsequent capture requests.

Surfaces that get removed must not be part of any active repeating or single/burst request or have any pending results. Consider updating any repeating requests first via setRepeatingRequest or setRepeatingBurst and then wait for the last frame number when the sequence completes onCaptureSequenceCompleted before calling updateOutputConfiguration to remove a previously active Surface.

Surfaces that get added must not be part of any other registered OutputConfiguration.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` updateOutputConfigurations

<br />

Update the output configurations for this camera session.

This method allows for updating the surfaces associated with the currently configured output OutputConfiguration. It is used to addSurface makeDeferredAndRemoveSurfaces surfaces with active surface instances or to swap surfaces for seamless transitions between use cases without re-initializing the entire camera session.

The number of provided configurations must match the number of currently configured outputs. Each provided OutputConfiguration must correspond to an already existing output configuration passed previously to createCaptureSession. The OutputConfiguration is identified by its properties (size, format, etc.), but can have a new surface associated with it (see addSurface) or be marked as deferred (see makeDeferredAndRemoveSurfaces).

This method is not for adding or removing new OutputConfiguration.

Any active requests that target replaced surfaces will be stopped by this call. When a surface with active capture requests is replaced, the framework will keep track of the old surface to ensure that any in-flight buffers can return successfully before the connection is terminated.

<br />

## Public constructors

### CameraConstrainedHighSpeedCaptureSession

```
CameraConstrainedHighSpeedCaptureSession()
```

## Public methods

### createHighSpeedRequestList

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createHighSpeedRequestList(request: CaptureRequest): MutableList<CaptureRequest!>
```

Create a unmodifiable list of requests that is suitable for constrained high speed capture session streaming.

High speed video streaming creates significant performance pressure on the camera device, so to achieve efficient high speed streaming, the camera device may have to aggregate multiple frames together. This means requests must be sent in batched groups, with all requests sharing the same settings. This method takes the list of output target Surfaces (subject to the output Surface requirements specified by the constrained high speed session) and a CaptureRequest, and generates a request list that has the same controls for each request. The input CaptureRequest must contain the target output Surfaces and target high speed FPS range that is one of the getHighSpeedVideoFpsRangesFor for the Surface size.

If both preview and recording Surfaces are specified in the `request`, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` in the input CaptureRequest must be a fixed frame rate FPS range, where the getLower == getUpper. The created request list will contain a interleaved request pattern such that the preview output FPS is at least 30fps, the recording output FPS is getUpper of the requested FPS range. The application can submit this request list directly to an active high speed capture session to achieve high speed video recording. When only preview or recording Surface is specified, this method will return a list of request that have the same controls and output targets for all requests.

Submitting a request list created by this method to a normal capture session will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the high speed `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` is not supported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`.

| Parameters ||
|---|---|
| `request` | [CaptureRequest](CaptureRequest.md): The high speed capture request that will be used to generate the high speed request list. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest!>` | A unmodifiable CaptureRequest list that is suitable for constrained high speed capture. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the set of output Surfaces in the request do not meet the high speed video capability requirements, or the camera device doesn't support high speed video capability, or the request doesn't meet the high speed video capability requirements, or the request doesn't contain the required controls for high speed capture. |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |

**See Also**

- createConstrainedHighSpeedCaptureSession
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`
- getHighSpeedVideoSizes
- getHighSpeedVideoFpsRangesFor
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int`
