Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MultiResolutionImageReader

```
open class MultiResolutionImageReader : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.MultiResolutionImageReader](https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#) |

The MultiResolutionImageReader class wraps a group of `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` with the same format and different sizes, source camera Id, or camera sensor modes.

The main use case of this class is for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int` or an ultra high resolution sensor camera to output variable-size images. For a logical multi-camera which implements optical zoom, different physical cameras may have different maximum resolutions. As a result, when the camera device switches between physical cameras depending on zoom ratio, the maximum resolution for a particular format may change. For an ultra high resolution sensor camera, the camera device may deem it better or worse to run in maximum resolution mode / default mode depending on lighting conditions. So the application may choose to let the camera device decide on its behalf.

MultiResolutionImageReader should be used for a camera device only if the camera device supports multi-resolution output stream by advertising the specified output format in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`.

To acquire images from the MultiResolutionImageReader, the application must use the `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` object passed by `https://developer.android.com/reference/kotlin/android/media/ImageReader.OnImageAvailableListener.html#onImageAvailable(android.media.ImageReader)` callback to call `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#acquireNextImage()` or `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#acquireLatestImage()`. The application must not use the `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` passed by an `https://developer.android.com/reference/kotlin/android/media/ImageReader.OnImageAvailableListener.html#onImageAvailable(android.media.ImageReader)` callback to acquire future images because future images may originate from a different `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` contained within the `MultiResolutionImageReader`.

Note that by default, for a MultiResolutionImageReader, each capture request produces only one output buffer from one internal reader. Some devices also support producing from multiple readers for a single CaptureRequest (for example, by running multiple sensors at the same time). Support for this can be queried by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#isConcurrentReadersSupported(kotlin.Int)` and enabled by using `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.Builder#setConcurrentOutputsEnabled(kotlin.Boolean)`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#` objects. |
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.OnActiveOutputSurfacesListener` Callback interface for being notified of the surfaces used for the capture. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#MultiResolutionImageReader(kotlin.collections.MutableCollection,%20kotlin.Int,%20kotlin.Int)(streams: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo!>, format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxImages: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new multi-resolution reader based on a group of camera stream properties returned by a camera device. |
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#MultiResolutionImageReader(kotlin.collections.MutableCollection,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long)(streams: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo!>, format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxImages: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, usage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Create a new multi-resolution reader based on a group of camera stream properties returned by a camera device, and the desired format, maximum buffer capacity and consumer usage flag. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#close()()` Closes this resource, relinquishing any underlying resources. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#flush()()` Flush pending images from all internal ImageReaders |
| open [MultiResolutionImageReader.OnActiveOutputSurfacesListener](https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.OnActiveOutputSurfacesListener)? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#getOnActiveOutputSurfacesListener()()` Get the `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.OnActiveOutputSurfacesListener` currently registered for this MultiResolutionImageReader. |
| --- | --- |
| open [MultiResolutionStreamInfo](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#getStreamInfoForImageReader(android.media.ImageReader)(reader: https://developer.android.com/reference/kotlin/android/media/ImageReader.html#)` Get the MultiResolutionStreamInfo describing the ImageReader an image originates from |
| open [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#getSurface()()` Get the surface that is used as a target for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#setOnActiveOutputSurfacesListener(java.util.concurrent.Executor,%20android.hardware.camera2.MultiResolutionImageReader.OnActiveOutputSurfacesListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.OnActiveOutputSurfacesListener)` Register a listener to be notified of active output surfaces for a concurrency-enabled MultiResolutionImageReader. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#setOnImageAvailableListener(android.media.ImageReader.OnImageAvailableListener,%20java.util.concurrent.Executor)(listener: https://developer.android.com/reference/kotlin/android/media/ImageReader.OnImageAvailableListener.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?)` Set onImageAvailableListener callback. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public constructors

### MultiResolutionImageReader

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MultiResolutionImageReader(
    streams: MutableCollection<MultiResolutionStreamInfo!>, 
    format: Int, 
    maxImages: Int)
```

Create a new multi-resolution reader based on a group of camera stream properties returned by a camera device.

This constructor is the equivalent of `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#MultiResolutionImageReader(kotlin.collections.MutableCollection,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long)` without specifying `usage`.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#MultiResolutionImageReader(kotlin.collections.MutableCollection,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long)` for full details.

| Parameters ||
|---|---|
| `streams` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MultiResolutionStreamInfo](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo)!\>: The group of multi-resolution stream info. This value cannot be `null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the Image that this multi-resolution reader will produce. |
| `maxImages` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of images the user will want to access simultaneously. Value is 1 or greater |
| --- | --- |

### MultiResolutionImageReader

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MultiResolutionImageReader(
    streams: MutableCollection<MultiResolutionStreamInfo!>, 
    format: Int, 
    maxImages: Int, 
    usage: Long)
```

Create a new multi-resolution reader based on a group of camera stream properties returned by a camera device, and the desired format, maximum buffer capacity and consumer usage flag.

The valid size and formats depend on the camera characteristics. `MultiResolutionImageReader` for an image format is supported by the camera device if the format is in the supported multi-resolution output stream formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#getOutputFormats()`. If the image format is supported, the `MultiResolutionImageReader` object can be created with the `streams` objects returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#getOutputInfo(kotlin.Int)`.

The `maxImages` parameter determines the maximum number of `https://developer.android.com/reference/kotlin/android/media/Image.html#` objects that can be acquired from each of the `ImageReader` within the `MultiResolutionImageReader`. However, requesting more buffers will use up more memory, so it is important to use only the minimum number necessary. The application is strongly recommended to acquire no more than `maxImages` images from all of the internal ImageReader objects combined. By keeping track of the number of acquired images for the MultiResolutionImageReader, the application doesn't need to do the bookkeeping for each internal ImageReader returned from `https://developer.android.com/reference/kotlin/android/media/ImageReader.OnImageAvailableListener.html#onImageAvailable(android.media.ImageReader)` callback.

Unlike the normal ImageReader, the MultiResolutionImageReader has a more complex configuration sequence. Instead of passing the same surface to OutputConfiguration and CaptureRequest, the android.hardware.camera2.params.OutputConfiguration#createInstancesForMultiResolutionOutput call needs to be used to create the OutputConfigurations for session creation, and then `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader#getSurface()` is used to get `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface)`.

| Parameters ||
|---|---|
| `streams` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MultiResolutionStreamInfo](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo)!\>: The group of multi-resolution stream info, which is used to create a multi-resolution reader containing a number of ImageReader objects. Each ImageReader object represents a multi-resolution stream in the group. This value cannot be `null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the Image that this multi-resolution reader will produce. This must be one of the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` constants. Note that not all formats are supported, like ImageFormat.NV21. The supported multi-resolution reader format can be queried by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#getOutputFormats()`. |
| `maxImages` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of images the user will want to access simultaneously. This should be as small as possible to limit memory use. Once maxImages images are obtained by the user from any given internal ImageReader, one of them has to be released before a new Image will become available for access through the ImageReader's `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#acquireLatestImage()` or `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#acquireNextImage()`. Must be greater than 0. Value is 1 or greater |
| --- | --- |
| `usage` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The intended usage of the images produced by the internal ImageReader. See the usages on `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` for a list of valid usage bits. See also `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#isSupported(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long)` for checking if a combination is supported. If it's not supported this will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_COLOR_OUTPUT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_COMPOSER_OVERLAY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_PROTECTED_CONTENT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_DATA_BUFFER:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_SENSOR_DIRECT_DATA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_CUBE_MAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_MIPMAP_COMPLETE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_FRONT_BUFFER:kotlin.Long` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Image.html#`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap`

## Public methods

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes this resource, relinquishing any underlying resources. This method is invoked automatically on objects managed by the `try`-with-resources statement.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### flush

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flush(): Unit
```

Flush pending images from all internal ImageReaders

Acquire and close pending images from all internal ImageReaders. This has the same effect as calling acquireLatestImage() on all internal ImageReaders, and closing all latest images.

### getOnActiveOutputSurfacesListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOnActiveOutputSurfacesListener(): MultiResolutionImageReader.OnActiveOutputSurfacesListener?
```

Get the `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.OnActiveOutputSurfacesListener` currently registered for this MultiResolutionImageReader.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.OnActiveOutputSurfacesListener?` | The listener, or `null` if no listener is currently registered. |

### getStreamInfoForImageReader

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStreamInfoForImageReader(reader: ImageReader): MultiResolutionStreamInfo
```

Get the MultiResolutionStreamInfo describing the ImageReader an image originates from

An image from a `MultiResolutionImageReader` is produced from one of the underlying `ImageReader`s. This function returns the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo` to describe the property for that `ImageReader`, such as width, height, and physical camera Id.

| Parameters ||
|---|---|
| `reader` | [ImageReader](https://developer.android.com/reference/kotlin/android/media/ImageReader.html#): An internal ImageReader within `MultiResolutionImageReader`. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo` | The stream info describing the internal `ImageReader`. This value cannot be `null`. |

### getSurface

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSurface(): Surface
```

Get the surface that is used as a target for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest`

The application must use the surface returned by this function as a target for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest`. The camera device makes the decision on which internal `ImageReader` will receive the output image.

Please note that holding on to the Surface objects returned by this method is not enough to keep their parent MultiResolutionImageReaders from being reclaimed. In that sense, a Surface acts like a `https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference.html#` to the MultiResolutionImageReader that provides it.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Surface.html#` | a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` to use as the target for a capture request. This value cannot be `null`. |

### setOnActiveOutputSurfacesListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnActiveOutputSurfacesListener(
    executor: Executor, 
    listener: MultiResolutionImageReader.OnActiveOutputSurfacesListener
): Unit
```

Register a listener to be notified of active output surfaces for a concurrency-enabled MultiResolutionImageReader.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.OnActiveOutputSurfacesListener#onActiveOutputSurfaces(kotlin.collections.MutableList,%20kotlin.Long,%20kotlin.Long)` for more details.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor which will be used to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [MultiResolutionImageReader.OnActiveOutputSurfacesListener](https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.OnActiveOutputSurfacesListener): The listener that will be run. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the executor or listener is null. |
| `java.lang.IllegalStateException` | If the MultiResolutionImageReader is created without enabling concurrency. |

### setOnImageAvailableListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnImageAvailableListener(
    listener: ImageReader.OnImageAvailableListener?, 
    executor: Executor?
): Unit
```

Set onImageAvailableListener callback.

This function sets the onImageAvailableListener for all the internal `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` objects.

For a multi-resolution ImageReader, the timestamps of images acquired in onImageAvailable callback from different internal ImageReaders may become out-of-order due to the asynchronous callbacks between the different resolution image queues.

| Parameters ||
|---|---|
| `listener` | [ImageReader.OnImageAvailableListener](https://developer.android.com/reference/kotlin/android/media/ImageReader.OnImageAvailableListener.html#)?: The listener that will be run. This value may be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)?: The executor which will be used when invoking the callback. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |

## Protected methods

### finalize

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
