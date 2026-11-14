Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImageReader

```
open class ImageReader : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.ImageReader](ImageReader.md) |

The ImageReader class allows direct application access to image data rendered into a `https://developer.android.com/reference/kotlin/android/view/Surface.html#`

Several Android media API classes accept Surface objects as targets to render to, including MediaPlayer, MediaCodec, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`, ImageWriter and `https://developer.android.com/reference/kotlin/android/renderscript/Allocation.html#`. The image sizes and formats that can be used with each source vary, and should be checked in the documentation for the specific API.

The image data is encapsulated in Image objects, and multiple such objects can be accessed at the same time, up to the number specified by the `maxImages` constructor parameter. New images sent to an ImageReader through its `https://developer.android.com/reference/kotlin/android/view/Surface.html#` are queued until accessed through the acquireLatestImage or acquireNextImage call. Due to memory limits, an image source will eventually stall or drop Images in trying to render to the Surface if the ImageReader does not obtain and release Images at a rate equal to the production rate.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/ImageReader.Builder` Builder class for ImageReader objects. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/ImageReader.OnImageAvailableListener` Callback interface for being notified that a new image is available. |

| Public methods ||
|---|---|
| open [Image](Image.md)! | acquireLatestImage Acquire the latest Image from the ImageReader's queue, dropping older Image. |
| open [Image](Image.md)! | acquireNextImage Acquire the next Image from the ImageReader's queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Free up all the resources associated with this ImageReader. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | discardFreeBuffers Discard any free buffers owned by this ImageReader. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDataSpace The default dataspace of Image. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHardwareBufferFormat The default `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` format of Image. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHeight The default height of Image, in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getImageFormat The default `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` of Image. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaxImages Maximum number of images that can be acquired from the ImageReader by any time (for example, with acquireNextImage). |
| --- | --- |
| open [Surface](../android.view/Surface.md)! | getSurface Get a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` that can be used to produce Image for this `ImageReader`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getUsage The usage flag of images that can be produced by the ImageReader. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWidth The default width of Image, in pixels. |
| --- | --- |
| open static [ImageReader](ImageReader.md) | newInstance Create a new reader for images of the desired size and format. |
| open static [ImageReader](ImageReader.md) | newInstance Create a new reader for images of the desired size, format and consumer usage flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOnImageAvailableListener Register a listener to be invoked when a new image becomes available from the ImageReader. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public methods

### acquireLatestImage

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acquireLatestImage(): Image!
```

Acquire the latest Image from the ImageReader's queue, dropping older Image. Returns `null` if no new image is available.

This operation will acquire all the images possible from the ImageReader, but close all images that aren't the latest. This function is recommended to use over acquireNextImage for most use-cases, as it's more suited for real-time processing.

Note that getMaxImages should be at least 2 for acquireLatestImage to be any different than acquireNextImage - discarding all-but-the-newest Image requires temporarily acquiring two Image at once. Or more generally, calling acquireLatestImage with less than two images of margin, that is `(maxImages - currentAcquiredImages < 2)` will not discard as expected.

This operation will fail by throwing an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` if `maxImages` have been acquired with acquireLatestImage or acquireNextImage. In particular a sequence of acquireLatestImage calls greater than getMaxImages without calling close in-between will exhaust the underlying queue. At such a time, `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` will be thrown until more images are released with close.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/Image!` | latest frame of image data, or `null` if no image data is available. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if too many images are currently acquired |
| `java.lang.UnsupportedOperationException` | Until API level 36 if the format of acquired image is different than format of the ImageReader. (If format is `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` or API level is 37 or later, the exception is not thrown and an image is acquired.) |

### acquireNextImage

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acquireNextImage(): Image!
```

Acquire the next Image from the ImageReader's queue. Returns `null` if no new image is available.

*Warning:* Consider using acquireLatestImage instead, as it will automatically release older images, and allow slower-running processing routines to catch up to the newest frame. Usage of acquireNextImage is recommended for batch/background processing. Incorrectly using this function can cause images to appear with an ever-increasing delay, followed by a complete stall where no new images seem to appear.

This operation will fail by throwing an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` if `maxImages` have been acquired with acquireNextImage or acquireLatestImage. In particular a sequence of acquireNextImage or acquireLatestImage calls greater than getMaxImages without calling close in-between will exhaust the underlying queue. At such a time, `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` will be thrown until more images are released with close.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/Image!` | a new frame of image data, or `null` if no image data is available. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `maxImages` images are currently acquired |
| `java.lang.UnsupportedOperationException` | Until API level 36 if the format of acquired image is different than format of the ImageReader. (If format is `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` or API level is 37 or later, the exception is not thrown and an image is acquired.) |

**See Also**

- acquireLatestImage

### close

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Free up all the resources associated with this ImageReader.

After calling this method, this ImageReader can not be used. Calling any methods on this ImageReader and Images previously provided by acquireNextImage or acquireLatestImage will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`, and attempting to read from `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` returned by an earlier getBuffer call will have undefined behavior.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### discardFreeBuffers

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun discardFreeBuffers(): Unit
```

Discard any free buffers owned by this ImageReader.

Generally, the ImageReader caches buffers for reuse once they have been allocated, for best performance. However, sometimes it may be important to release all the cached, unused buffers to save on memory.

Calling this method will discard all free cached buffers. This does not include any buffers associated with Images acquired from the ImageReader, any filled buffers waiting to be acquired, and any buffers currently in use by the source rendering buffers into the ImageReader's Surface.

The ImageReader continues to be usable after this call, but may need to reallocate buffers when more buffers are needed for rendering.

### getDataSpace

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDataSpace(): Int
```

The default dataspace of Image.

Use this function if the ImageReader instance is created by builder pattern `ImageReader.Builder` and setDefaultDataSpace.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the expected dataspace of an Image. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DEPTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DYNAMIC_DEPTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_HEIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_HEIF_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JPEG_R:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DISPLAY_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_HLG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_PQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_ADOBE_RGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JFIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DISPLAY_BT2020:kotlin.Int` |

### getHardwareBufferFormat

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHardwareBufferFormat(): Int
```

The default `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` format of Image.

Use this function if the ImageReader instance is created by builder pattern `ImageReader.Builder` and using setDefaultHardwareBufferFormat and setDefaultDataSpace.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the expected `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` format of an Image. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_FP16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_1010102:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#BLOB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#YCBCR_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#D_16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#D_24:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#DS_24UI8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#D_FP32:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#DS_FP32UI8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#S_UI8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#R_8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#R_16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RG_1616:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_10101010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#R_12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#R_14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RG_1212:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RG_1414:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_12121212:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#RGBA_14141414:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#BGRA_1010102:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#BGRX_1010102:kotlin.Int` |

### getHeight

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHeight(): Int
```

The default height of Image, in pixels.

The height may be overridden by the producer sending buffers to this ImageReader's Surface. If so, the actual height of the images can be found using getHeight.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the expected height of an Image |

### getImageFormat

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getImageFormat(): Int
```

The default `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` of Image.

Some color formats may be overridden by the producer sending buffers to this ImageReader's Surface if the default color format allows. ImageReader guarantees that all Image acquired from ImageReader (for example, with acquireNextImage) will have a "compatible" format to what was specified in #newInstance. As of now, each format is only compatible to itself. The actual format of the images can be found using getFormat.

Use this function if the ImageReader instance is created by factory method `newInstance` function or by builder pattern `ImageReader.Builder` and using setImageFormat.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the expected format of an Image |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`

### getMaxImages

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxImages(): Int
```

Maximum number of images that can be acquired from the ImageReader by any time (for example, with acquireNextImage).

An image is considered acquired after it's returned by a function from ImageReader, and until the Image is close to release the image back to the ImageReader.

Attempting to acquire more than `maxImages` concurrently will result in the acquire function throwing a `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. Furthermore, while the max number of images have been acquired by the ImageReader user, the producer enqueueing additional images may stall until at least one image has been released.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Maximum number of images for this ImageReader. |

**See Also**

- close

### getSurface

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSurface(): Surface!
```

Get a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` that can be used to produce Image for this `ImageReader`.

Until valid image data is rendered into this `https://developer.android.com/reference/kotlin/android/view/Surface.html#`, the acquireNextImage method will return `null`. Only one source can be producing data into this Surface at the same time, although the same `https://developer.android.com/reference/kotlin/android/view/Surface.html#` can be reused with a different API once the first source is disconnected from the `https://developer.android.com/reference/kotlin/android/view/Surface.html#`.

Please note that holding on to the Surface object returned by this method is not enough to keep its parent ImageReader from being reclaimed. In that sense, a Surface acts like a `https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference.html#` to the ImageReader that provides it.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Surface.html#!` | A `https://developer.android.com/reference/kotlin/android/view/Surface.html#` to use for a drawing target for various APIs. |

### getUsage

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUsage(): Long
```

The usage flag of images that can be produced by the ImageReader.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The usage flag of the images for this ImageReader. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_COLOR_OUTPUT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_COMPOSER_OVERLAY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_PROTECTED_CONTENT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_DATA_BUFFER:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_SENSOR_DIRECT_DATA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_CUBE_MAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_MIPMAP_COMPLETE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_FRONT_BUFFER:kotlin.Long` |

### getWidth

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWidth(): Int
```

The default width of Image, in pixels.

The width may be overridden by the producer sending buffers to this ImageReader's Surface. If so, the actual width of the images can be found using getWidth.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the expected width of an Image |

### newInstance

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(
    width: Int, 
    height: Int, 
    format: Int, 
    maxImages: Int
): ImageReader
```

Create a new reader for images of the desired size and format.

The `maxImages` parameter determines the maximum number of Image objects that can be be acquired from the `ImageReader` simultaneously. Requesting more buffers will use up more memory, so it is important to use only the minimum number necessary for the use case.

The valid sizes and formats depend on the source of the image data.

If the `format` is `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`, the created ImageReader will produce images that are not directly accessible by the application. The application can still acquire images from this ImageReader, and send them to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#` for reprocessing via ImageWriter interface. However, the getPlanes will return an empty array for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format images. The application can check if an existing reader's format by calling getImageFormat.

`https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format ImageReader are more efficient to use when application access to image data is not necessary, compared to ImageReaders using other format such as `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int`.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The default width in pixels of the Images that this reader will produce. Value is 1 or greater |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The default height in pixels of the Images that this reader will produce. Value is 1 or greater |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the Image that this reader will produce. This must be one of the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` constants. Note that not all formats are supported, like ImageFormat.NV21. |
| --- | --- |
| `maxImages` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of images the user will want to access simultaneously. This should be as small as possible to limit memory use. Once maxImages Images are obtained by the user, one of them has to be released before a new Image will become available for access through acquireLatestImage or acquireNextImage. Must be greater than 0. Value is 1 or greater |

| Return ||
|---|---|
| ImageReader | This value cannot be `null`. |

**See Also**

- Image

### newInstance

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(
    width: Int, 
    height: Int, 
    format: Int, 
    maxImages: Int, 
    usage: Long
): ImageReader
```

Create a new reader for images of the desired size, format and consumer usage flag.

The `maxImages` parameter determines the maximum number of Image objects that can be be acquired from the `ImageReader` simultaneously. Requesting more buffers will use up more memory, so it is important to use only the minimum number necessary for the use case.

The valid sizes and formats depend on the source of the image data.

The format and usage flag combination describes how the buffer will be used by consumer end-points. For example, if the application intends to send the images to MediaCodec or MediaRecorder for hardware video encoding, the format and usage flag combination needs to be `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long`. When an ImageReader object is created with a valid size and such format/usage flag combination, the application can send the Image to an ImageWriter that is created with the input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` provided by the MediaCodec or MediaRecorder.

If the `format` is `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`, the created ImageReader will produce images that are not directly accessible by the application. The application can still acquire images from this ImageReader, and send them to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#` for reprocessing, or to the MediaCodec / MediaRecorder for hardware video encoding via ImageWriter interface. However, the getPlanes will return an empty array for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format images. The application can check if an existing reader's format by calling getImageFormat.

`https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format ImageReader are more efficient to use when application access to image data is not necessary, compared to ImageReaders using other format such as `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int`.

Note that not all format and usage flag combinations are supported by the ImageReader. Below are the supported combinations by the ImageReader (assuming the consumer end-points support the such image consumption, e.g., hardware video encoding).

| Format | Compatible usage flags |
|---|---|
| non-`https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` formats defined by `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` | `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_RARELY:kotlin.Long` or `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` or `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long`, or combined |

Using other combinations may result in `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. Additionally, specifying `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_RARELY:kotlin.Long` or `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_OFTEN:kotlin.Long` and writing to the ImageReader's buffers might break assumptions made by some producers, and should be used with caution.

<br />

If the ImageReader is used as an output target for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`, and if the usage flag contains `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long`, the timestamps of the Image produced by the ImageReader won't be in the same timebase as elapsedRealtimeNanos, even if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key` is `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_INFO_TIMESTAMP_SOURCE_REALTIME:kotlin.Int`. Instead, the timestamps will be roughly in the same timebase as in uptimeMillis, so that A/V synchronization could work for video recording. In this case, the timestamps from the ImageReader with `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` usage flag may not be directly comparable with timestamps of other streams or capture result metadata.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The default width in pixels of the Images that this reader will produce. Value is 1 or greater |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The default height in pixels of the Images that this reader will produce. Value is 1 or greater |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the Image that this reader will produce. This must be one of the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` constants. Note that not all formats are supported, like ImageFormat.NV21. |
| --- | --- |
| `maxImages` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of images the user will want to access simultaneously. This should be as small as possible to limit memory use. Once maxImages Images are obtained by the user, one of them has to be released before a new Image will become available for access through acquireLatestImage or acquireNextImage. Must be greater than 0. Value is 1 or greater |
| `usage` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The intended usage of the images produced by this ImageReader. See the usages on `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` for a list of valid usage bits. See also isSupported for checking if a combination is supported. If it's not supported this will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_COLOR_OUTPUT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_COMPOSER_OVERLAY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_PROTECTED_CONTENT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_DATA_BUFFER:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_SENSOR_DIRECT_DATA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_CUBE_MAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_MIPMAP_COMPLETE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_FRONT_BUFFER:kotlin.Long` |

| Return ||
|---|---|
| ImageReader | This value cannot be `null`. |

**See Also**

- Image
- `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#`

### setOnImageAvailableListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnImageAvailableListener(
    listener: ImageReader.OnImageAvailableListener!, 
    handler: Handler!
): Unit
```

Register a listener to be invoked when a new image becomes available from the ImageReader.

| Parameters ||
|---|---|
| `listener` | [ImageReader.OnImageAvailableListener](../android/media/ImageReader.OnImageAvailableListener.md)!: The listener that will be run. |
| `handler` | [Handler](../android.os/Handler.md)!: The handler on which the listener should be invoked, or null if the listener should be invoked on the calling thread's looper. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If no handler specified and the calling thread has no looper. |

## Protected methods

### finalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
