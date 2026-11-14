Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImageWriter

```
open class ImageWriter : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.ImageWriter](ImageWriter.md) |

The ImageWriter class allows an application to produce Image data into a `https://developer.android.com/reference/kotlin/android/view/Surface.html#`, and have it be consumed by another component like `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`.

Several Android API classes can provide input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` objects for ImageWriter to produce data into, including `https://developer.android.com/reference/kotlin/android/media/MediaCodec` (encoder), `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.html#` (reprocessing input), `https://developer.android.com/reference/kotlin/android/media/ImageReader`, etc.

The input Image data is encapsulated in `https://developer.android.com/reference/kotlin/android/media/Image` objects. To produce Image data into a destination `https://developer.android.com/reference/kotlin/android/view/Surface.html#`, the application can get an input Image via `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()` then write Image data into it. Multiple such `https://developer.android.com/reference/kotlin/android/media/Image` objects can be dequeued at the same time and queued back in any order, up to the number specified by the `maxImages` constructor parameter.

If the application already has an Image from `https://developer.android.com/reference/kotlin/android/media/ImageReader`, the application can directly queue this Image into the ImageWriter (via `https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)`), potentially with zero buffer copies. This even works if the image format of the ImageWriter is `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`, and prior to Android P is the only way to enqueue images into such an ImageWriter. Starting in Android P private images may also be accessed through their hardware buffers (when available) through the `https://developer.android.com/reference/kotlin/android/media/Image#getHardwareBuffer()` method. Attempting to access the planes of a private image, will return an empty array.

Once new input Images are queued into an ImageWriter, it's up to the downstream components (e.g. `https://developer.android.com/reference/kotlin/android/media/ImageReader` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`) to consume the Images. If the downstream components cannot consume the Images at least as fast as the ImageWriter production rate, the `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()` call will eventually block and the application will have to drop input frames.

If the consumer component that provided the input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` abandons the `https://developer.android.com/reference/kotlin/android/view/Surface.html#`, `https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)` or `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()` an `https://developer.android.com/reference/kotlin/android/media/Image` will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/ImageWriter.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/media/ImageWriter#` objects. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/ImageWriter.OnImageReleasedListener` ImageWriter callback interface, used to to asynchronously notify the application of various ImageWriter events. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#close()()` Free up all the resources associated with this ImageWriter. |
| open [Image](Image.md)! | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()()` Dequeue the next available input Image for the application to produce data into. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getDataSpace()()` Get the ImageWriter dataspace. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getFormat()()` Get the ImageWriter format. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getHardwareBufferFormat()()` Get the ImageWriter hardwareBuffer format. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getHeight()()` The height of `https://developer.android.com/reference/kotlin/android/media/Image`, in pixels. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getMaxImages()()` Maximum number of Images that can be dequeued from the ImageWriter simultaneously (for example, with `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()`). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getUsage()()` Get the ImageWriter usage flag. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getWidth()()` The width of `https://developer.android.com/reference/kotlin/android/media/Image`, in pixels. |
| --- | --- |
| open static [ImageWriter](ImageWriter.md) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#newInstance(android.view.Surface,%20kotlin.Int)(surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#, maxImages: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new ImageWriter. |
| open static [ImageWriter](ImageWriter.md) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#newInstance(android.view.Surface,%20kotlin.Int,%20kotlin.Int)(surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#, maxImages: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new ImageWriter with given number of max Images and format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)(image: https://developer.android.com/reference/kotlin/android/media/Image!)` Queue an input `https://developer.android.com/reference/kotlin/android/media/Image` back to ImageWriter for the downstream consumer to access. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#setOnImageReleasedListener(android.media.ImageWriter.OnImageReleasedListener,%20android.os.Handler)(listener: https://developer.android.com/reference/kotlin/android/media/ImageWriter.OnImageReleasedListener!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Register a listener to be invoked when an input Image is returned to the ImageWriter. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/ImageWriter#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public methods

### close

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Free up all the resources associated with this ImageWriter.

After calling this method, this ImageWriter cannot be used. Calling any methods on this ImageWriter and Images previously provided by `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()` will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`, and attempting to write into `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` returned by an earlier `https://developer.android.com/reference/kotlin/android/media/Image.Plane#getBuffer()` call will have undefined behavior.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### dequeueInputImage

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dequeueInputImage(): Image!
```

Dequeue the next available input Image for the application to produce data into.

This method requests a new input Image from ImageWriter. The application owns this Image after this call. Once the application fills the Image data, it is expected to return this Image back to ImageWriter for downstream consumer components (e.g. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`) to consume. The Image can be returned to ImageWriter via `https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)` or `https://developer.android.com/reference/kotlin/android/media/Image#close()`.

This call will block if all available input images have been queued by the application and the downstream consumer has not yet consumed any. When an Image is consumed by the downstream consumer and released, an `https://developer.android.com/reference/kotlin/android/media/ImageWriter.OnImageReleasedListener#onImageReleased(android.media.ImageWriter)` callback will be fired, which indicates that there is one input Image available. For non- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` formats ( `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getFormat()` != `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`), it is recommended to dequeue the next Image only after this callback is fired, in the steady state.

If the format of ImageWriter is `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` ( `https://developer.android.com/reference/kotlin/android/media/ImageWriter#getFormat()` == `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`), the image buffer is accessible to the application only through the hardware buffer obtained through `https://developer.android.com/reference/kotlin/android/media/Image#getHardwareBuffer()`. (On Android versions prior to P, dequeueing private buffers will cause an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` to be thrown). Alternatively, the application can acquire images from some other component (e.g. an `https://developer.android.com/reference/kotlin/android/media/ImageReader`), and queue them directly to this ImageWriter via the `https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)` method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/Image!` | The next available input Image from this ImageWriter. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `maxImages` Images are currently dequeued, or the input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` has been abandoned by the consumer component that provided the `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. Prior to Android P, throws if the ImageWriter format is `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)`
- `https://developer.android.com/reference/kotlin/android/media/Image#close()`

### getDataSpace

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDataSpace(): Int
```

Get the ImageWriter dataspace.

Use this function if the ImageWriter instance is created by builder pattern `ImageWriter.Builder` and `https://developer.android.com/reference/kotlin/android/media/ImageWriter.Builder#setDataSpace(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The ImageWriter dataspace. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DEPTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DYNAMIC_DEPTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_HEIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_HEIF_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JPEG_R:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DISPLAY_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_HLG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_PQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_ADOBE_RGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JFIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DISPLAY_BT2020:kotlin.Int` |

### getFormat

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFormat(): Int
```

Get the ImageWriter format.

This format may be different than the Image format returned by `https://developer.android.com/reference/kotlin/android/media/Image#getFormat()`. However, if the ImageWriter format is `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`, calling `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()` will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The ImageWriter format. |

### getHardwareBufferFormat

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHardwareBufferFormat(): Int
```

Get the ImageWriter hardwareBuffer format.

Use this function if the ImageWriter instance is created by builder pattern `ImageWriter.Builder` and using `https://developer.android.com/reference/kotlin/android/media/ImageWriter.Builder#setHardwareBufferFormat(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/media/ImageWriter.Builder#setDataSpace(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The ImageWriter hardwareBuffer format. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_FP16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_1010102:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#BLOB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#YCBCR_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#D_16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#D_24:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#DS_24UI8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#D_FP32:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#DS_FP32UI8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#S_UI8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#R_8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#R_16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RG_1616:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_10101010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#R_12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#R_14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RG_1212:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RG_1414:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_12121212:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_14141414:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#BGRA_1010102:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#BGRX_1010102:kotlin.Int` |

### getHeight

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHeight(): Int
```

The height of `https://developer.android.com/reference/kotlin/android/media/Image`, in pixels.

If `https://developer.android.com/reference/kotlin/android/media/ImageWriter.Builder#setWidthAndHeight(kotlin.Int,%20kotlin.Int)` is not called, the default height of the Image depends on the Surface provided by customer end-point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the expected height of an Image. |

### getMaxImages

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxImages(): Int
```

Maximum number of Images that can be dequeued from the ImageWriter simultaneously (for example, with `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()`).

An Image is considered dequeued after it's returned by `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()` from ImageWriter, and until the Image is sent back to ImageWriter via `https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)`, or `https://developer.android.com/reference/kotlin/android/media/Image#close()`.

Attempting to dequeue more than `maxImages` concurrently will result in the `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()` function throwing an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Maximum number of Images that can be dequeued from this ImageWriter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()`
- `https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)`
- `https://developer.android.com/reference/kotlin/android/media/Image#close()`

### getUsage

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUsage(): Long
```

Get the ImageWriter usage flag.

It is not recommended to use this function if `https://developer.android.com/reference/kotlin/android/media/ImageWriter.Builder#setUsage(kotlin.Long)` is not called. Invalid usage value will be returned if so.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The ImageWriter usage flag. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_COLOR_OUTPUT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_COMPOSER_OVERLAY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_PROTECTED_CONTENT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_DATA_BUFFER:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_SENSOR_DIRECT_DATA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_CUBE_MAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_MIPMAP_COMPLETE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_FRONT_BUFFER:kotlin.Long` |

### getWidth

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWidth(): Int
```

The width of `https://developer.android.com/reference/kotlin/android/media/Image`, in pixels.

If `https://developer.android.com/reference/kotlin/android/media/ImageWriter.Builder#setWidthAndHeight(kotlin.Int,%20kotlin.Int)` is not called, the default width of the Image depends on the Surface provided by customer end-point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the expected actual width of an Image. |

### newInstance

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(
    surface: Surface, 
    maxImages: Int
): ImageWriter
```

Create a new ImageWriter.

The `maxImages` parameter determines the maximum number of `https://developer.android.com/reference/kotlin/android/media/Image` objects that can be be dequeued from the `ImageWriter` simultaneously. Requesting more buffers will use up more memory, so it is important to use only the minimum number necessary.

The input Image size and format depend on the Surface that is provided by the downstream consumer end-point.

| Parameters ||
|---|---|
| `surface` | [Surface](../android.view/Surface.md): The destination Surface this writer produces Image data into. This value cannot be `null`. |
| `maxImages` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of Images the user will want to access simultaneously for producing Image data. This should be as small as possible to limit memory use. Once maxImages Images are dequeued by the user, one of them has to be queued back before a new Image can be dequeued for access via `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()`. Value is 1 or greater |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/ImageWriter#` | a new ImageWriter instance. This value cannot be `null`. |

### newInstance

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(
    surface: Surface, 
    maxImages: Int, 
    format: Int
): ImageWriter
```

Create a new ImageWriter with given number of max Images and format.

The `maxImages` parameter determines the maximum number of `https://developer.android.com/reference/kotlin/android/media/Image` objects that can be be dequeued from the `ImageWriter` simultaneously. Requesting more buffers will use up more memory, so it is important to use only the minimum number necessary.

The format specifies the image format of this ImageWriter. The format from the `surface` will be overridden with this format. For example, if the surface is obtained from a `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#`, the default format may be `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int`. If the application creates an ImageWriter with this surface and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`, this ImageWriter will be able to operate with `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` Images.

Note that the consumer end-point may or may not be able to support Images with different format, for such case, the application should only use this method if the consumer is able to consume such images.

The input Image size depends on the Surface that is provided by the downstream consumer end-point.

| Parameters ||
|---|---|
| `surface` | [Surface](../android.view/Surface.md): The destination Surface this writer produces Image data into. This value cannot be `null`. |
| `maxImages` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of Images the user will want to access simultaneously for producing Image data. This should be as small as possible to limit memory use. Once maxImages Images are dequeued by the user, one of them has to be queued back before a new Image can be dequeued for access via `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()`. Value is 1 or greater |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of this ImageWriter. It can be any valid format specified by `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/ImageWriter#` | a new ImageWriter instance. This value cannot be `null`. |

### queueInputImage

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queueInputImage(image: Image!): Unit
```

Queue an input `https://developer.android.com/reference/kotlin/android/media/Image` back to ImageWriter for the downstream consumer to access.

The input `https://developer.android.com/reference/kotlin/android/media/Image` could be from ImageReader (acquired via `https://developer.android.com/reference/kotlin/android/media/ImageReader#acquireNextImage()` or `https://developer.android.com/reference/kotlin/android/media/ImageReader#acquireLatestImage()`), or from this ImageWriter (acquired via `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()`). In the former case, the Image data will be moved to this ImageWriter. Note that the Image properties (size, format, strides, etc.) must be the same as the properties of the images dequeued from this ImageWriter. In the latter case, the application has filled the input image with data. This method then passes the filled buffer to the downstream consumer. In both cases, it's up to the caller to ensure that the Image timestamp (in nanoseconds) is correctly set, as the downstream component may want to use it to indicate the Image data capture time.

After this method is called and the downstream consumer consumes and releases the Image, an `https://developer.android.com/reference/kotlin/android/media/ImageWriter.OnImageReleasedListener#onImageReleased(android.media.ImageWriter)` callback will fire. The application can use this callback to avoid sending Images faster than the downstream consumer processing rate in steady state.

Passing in an Image from some other component (e.g. an `https://developer.android.com/reference/kotlin/android/media/ImageReader`) requires a free input Image from this ImageWriter as the destination. In this case, this call will block, as `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()` does, if there are no free Images available. To avoid blocking, the application should ensure that there is at least one free Image available in this ImageWriter before calling this method.

After this call, the input Image is no longer valid for further access, as if the Image is `https://developer.android.com/reference/kotlin/android/media/Image#close()`. Attempting to access the `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` returned by an earlier `https://developer.android.com/reference/kotlin/android/media/Image.Plane#getBuffer()` call will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

| Parameters ||
|---|---|
| `image` | [Image](Image.md)!: The Image to be queued back to ImageWriter for future consumption. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the image was already queued previously, or the image was aborted previously, or the input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` has been abandoned by the consumer component that provided the `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()`

### setOnImageReleasedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnImageReleasedListener(
    listener: ImageWriter.OnImageReleasedListener!, 
    handler: Handler!
): Unit
```

Register a listener to be invoked when an input Image is returned to the ImageWriter.

| Parameters ||
|---|---|
| `listener` | [ImageWriter.OnImageReleasedListener](../android/media/ImageWriter.OnImageReleasedListener.md)!: The listener that will be run. |
| `handler` | [Handler](../android.os/Handler.md)!: The handler on which the listener should be invoked, or null if the listener should be invoked on the calling thread's looper. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If no handler specified and the calling thread has no looper. |

## Protected methods

### finalize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
