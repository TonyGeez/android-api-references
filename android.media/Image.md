# Image

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Image

Kotlin| [Java](https://developer.android.com/reference/android/media/Image "View this page in Java") 

```
abstract class Image : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.Image](https://developer.android.com/reference/kotlin/android/media/Image#) |

A single complete image buffer to use with a media source such as a [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) or a [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#).

This class allows for efficient direct application access to the pixel data of the Image through one or more [ByteBuffers](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#). Each buffer is encapsulated in a [Plane](https://developer.android.com/reference/kotlin/android/media/Image.Plane) that describes the layout of the pixel data in that plane. Due to this direct access, and unlike the [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) class, Images are not directly usable as UI resources.

Since Images are often directly produced or consumed by hardware components, they are a limited resource shared across the system, and should be closed as soon as they are no longer needed.

For example, when using the [ImageReader](https://developer.android.com/reference/kotlin/android/media/ImageReader) class to read out Images from various media sources, not closing old Image objects will prevent the availability of new Images once [the maximum outstanding image count](https://developer.android.com/reference/kotlin/android/media/ImageReader#getMaxImages())is reached. When this happens, the function acquiring new Images will typically throw an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| abstract | [Plane](https://developer.android.com/reference/kotlin/android/media/Image.Plane) A single color plane of image data. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/media/Image#close())`()` Free up this frame for reuse. |
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | [getCropRect](https://developer.android.com/reference/kotlin/android/media/Image#getCropRect())`()` Get the crop rectangle associated with this frame. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataSpace](https://developer.android.com/reference/kotlin/android/media/Image#getDataSpace())`()` Get the dataspace associated with this frame. |
| open [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#) | [getFence](https://developer.android.com/reference/kotlin/android/media/Image#getFence())`()` Get the SyncFence object associated with this frame. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFormat](https://developer.android.com/reference/kotlin/android/media/Image#getFormat())`()` Get the format for this image. |
| open [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#)? | [getHardwareBuffer](https://developer.android.com/reference/kotlin/android/media/Image#getHardwareBuffer())`()` Get the [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) handle of the input image intended for GPU and/or hardware access. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/media/Image#getHeight())`()` The height of the image in pixels. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Image.Plane](https://developer.android.com/reference/kotlin/android/media/Image.Plane)!\>! | [getPlanes](https://developer.android.com/reference/kotlin/android/media/Image#getPlanes())`()` Get the array of pixel planes for this Image. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestamp](https://developer.android.com/reference/kotlin/android/media/Image#getTimestamp())`()` Get the timestamp associated with this frame. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/media/Image#getWidth())`()` The width of the image in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCropRect](https://developer.android.com/reference/kotlin/android/media/Image#setCropRect(android.graphics.Rect))`(`cropRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` Set the crop rectangle associated with this frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSpace](https://developer.android.com/reference/kotlin/android/media/Image#setDataSpace(kotlin.Int))`(`dataSpace:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the dataspace associated with this frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFence](https://developer.android.com/reference/kotlin/android/media/Image#setFence(android.hardware.SyncFence))`(`fence:` ` [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#)`)` Set the fence file descriptor with this frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](https://developer.android.com/reference/kotlin/android/media/Image#setTimestamp(kotlin.Long))`(`timestamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Set the timestamp associated with this frame. |

## Public methods

### close

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Free up this frame for reuse.

After calling this method, calling any methods on this`Image`will result in an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#), and attempting to read from or write to [ByteBuffers](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#) returned by an earlier [Plane.getBuffer](https://developer.android.com/reference/kotlin/android/media/Image.Plane#getBuffer())call will have undefined behavior. If the image was obtained from [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter) via [ImageWriter.dequeueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()), after calling this method, any image data filled by the application will be lost and the image will be returned to [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter) for reuse. Images given to [queueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image))are automatically closed.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### getCropRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCropRect(): Rect!
```

Get the crop rectangle associated with this frame.

The crop rectangle specifies the region of valid pixels in the image, using coordinates in the largest-resolution plane. 

### getDataSpace

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataSpace(): Int
```

Get the dataspace associated with this frame.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.hardware.DataSpace#DATASPACE_DEPTH](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DEPTH:kotlin.Int), [android.hardware.DataSpace#DATASPACE_DYNAMIC_DEPTH](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DYNAMIC_DEPTH:kotlin.Int), [android.hardware.DataSpace#DATASPACE_HEIF](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_HEIF:kotlin.Int), [android.hardware.DataSpace#DATASPACE_HEIF_ULTRAHDR](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_HEIF_ULTRAHDR:kotlin.Int), [android.hardware.DataSpace#DATASPACE_JPEG_R](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JPEG_R:kotlin.Int), [android.hardware.DataSpace#DATASPACE_UNKNOWN](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_UNKNOWN:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SCRGB_LINEAR](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB_LINEAR:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SRGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SCRGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_DISPLAY_P3](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DISPLAY_P3:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020_HLG](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_HLG:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020_PQ](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_PQ:kotlin.Int), [android.hardware.DataSpace#DATASPACE_ADOBE_RGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_ADOBE_RGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_JFIF](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JFIF:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT601_625](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_625:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT601_525](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_525:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT709](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT709:kotlin.Int), [android.hardware.DataSpace#DATASPACE_DCI_P3](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DCI_P3:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SRGB_LINEAR](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB_LINEAR:kotlin.Int), and android.hardware.DataSpace.DATASPACE_DISPLAY_BT2020 |

### getFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFence(): SyncFence
```

Get the SyncFence object associated with this frame.

This function returns an invalid SyncFence after [getPlanes()](https://developer.android.com/reference/kotlin/android/media/Image#getPlanes())on the image dequeued from [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter) via [ImageWriter.dequeueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()).

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#) | The SyncFence for this frame. This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------|
| `java.io.IOException` | if there is an error when a SyncFence object returns. |

**See Also**

- [android.hardware.SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#) 

### getFormat

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFormat(): Int
```

Get the format for this image. This format determines the number of ByteBuffers needed to represent the image, and the general layout of the pixel data in each ByteBuffer.

The format is one of the values from [ImageFormat](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#), [PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#), or [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#). The mapping between the formats and the planes is as follows (any formats not listed will have 1 plane):

| Format | Plane count | Layout details |
|------------------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [JPEG](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int) | 1 | Compressed data, so row and pixel strides are 0. To uncompress, use android.graphics.BitmapFactory#decodeByteArray. |
| [YUV_420_888](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int) | 3 | A luminance plane followed by the Cb and Cr chroma planes. The chroma planes have half the width and height of the luminance plane (4:2:0 subsampling). Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| [YUV_422_888](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int) | 3 | A luminance plane followed by the Cb and Cr chroma planes. The chroma planes have half the width and the full height of the luminance plane (4:2:2 subsampling). Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| [YUV_444_888](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int) | 3 | A luminance plane followed by the Cb and Cr chroma planes. The chroma planes have the same width and height as that of the luminance plane (4:4:4 subsampling). Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| [FLEX_RGB_888](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int) | 3 | A R (red) plane followed by the G (green) and B (blue) planes. All planes have the same widths and heights. Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| [FLEX_RGBA_8888](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int) | 4 | A R (red) plane followed by the G (green), B (blue), and A (alpha) planes. All planes have the same widths and heights. Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| [RAW_SENSOR](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int) | 1 | A single plane of raw sensor image data, with 16 bits per color sample. The details of the layout need to be queried from the source of the raw sensor data, such as [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#). |
| [RAW_PRIVATE](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int) | 1 | A single plane of raw sensor image data of private layout. The details of the layout is implementation specific. Row stride and pixel stride are undefined for this format. Calling [Plane.getRowStride()](https://developer.android.com/reference/kotlin/android/media/Image.Plane#getRowStride())or [Plane.getPixelStride()](https://developer.android.com/reference/kotlin/android/media/Image.Plane#getPixelStride())on RAW_PRIVATE image will cause UnSupportedOperationException being thrown. |
| [HEIC](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int) | 1 | Compressed data, so row and pixel strides are 0. To uncompress, use android.graphics.BitmapFactory#decodeByteArray. |
| [YCBCR_P010](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int) | 3 | P010 is a 4:2:0 YCbCr semiplanar format comprised of a WxH Y plane followed by a Wx(H/2) Cb and Cr planes. Each sample is represented by a 16-bit little-endian value, with the lower 6 bits set to zero. Since this is guaranteed to be a semi-planar format, the Cb plane can also be treated as an interleaved Cb/Cr plane. |
| [YCBCR_P210](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int) | 3 | P210 is a 4:2:2 YCbCr semiplanar format comprised of a WxH Y plane followed by a WxH Cb and Cr planes. Each sample is represented by a 16-bit little-endian value, with the lower 6 bits set to zero. Since this is guaranteed to be a semi-planar format, the Cb plane can also be treated as an interleaved Cb/Cr plane. |

**See Also**

- [android.graphics.ImageFormat](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#)
- [android.graphics.PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#)
- [android.hardware.HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) 

### getHardwareBuffer

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHardwareBuffer(): HardwareBuffer?
```

Get the [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) handle of the input image intended for GPU and/or hardware access.

The returned [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) shall not be used after [Image.close()](https://developer.android.com/reference/kotlin/android/media/Image#close())has been called.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#)? | the HardwareBuffer associated with this Image or null if this Image doesn't support this feature. (Unsupported use cases include Image instances obtained through [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec), and on versions prior to Android P, [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter)). |

### getHeight

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHeight(): Int
```

The height of the image in pixels. For formats where some color channels are subsampled, this is the height of the largest-resolution plane. 

### getPlanes

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPlanes(): Array<Image.Plane!>!
```

Get the array of pixel planes for this Image. The number of planes is determined by the format of the Image. The application will get an empty array if the image format is [PRIVATE](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int), because the image pixel data is not directly accessible. The application can check the image format by calling [Image.getFormat()](https://developer.android.com/reference/kotlin/android/media/Image#getFormat()). 

### getTimestamp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTimestamp(): Long
```

Get the timestamp associated with this frame.

The timestamp is measured in nanoseconds, and is normally monotonically increasing. The timestamps for the images from different sources may have different timebases therefore may not be comparable. The specific meaning and timebase of the timestamp depend on the source providing images. See [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera.html#), [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#), [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer) and [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) for more details. 

### getWidth

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getWidth(): Int
```

The width of the image in pixels. For formats where some color channels are subsampled, this is the width of the largest-resolution plane. 

### setCropRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCropRect(cropRect: Rect!): Unit
```

Set the crop rectangle associated with this frame.

The crop rectangle specifies the region of valid pixels in the image, using coordinates in the largest-resolution plane. 

### setDataSpace

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSpace(dataSpace: Int): Unit
```

Set the dataspace associated with this frame.

If dataspace for an image is not set, dataspace value depends on [android.view.Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#) that is provided in the [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter) constructor.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSpace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The Dataspace to be set for this image Value is either`0`or a combination of [android.hardware.DataSpace#DATASPACE_DEPTH](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DEPTH:kotlin.Int), [android.hardware.DataSpace#DATASPACE_DYNAMIC_DEPTH](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DYNAMIC_DEPTH:kotlin.Int), [android.hardware.DataSpace#DATASPACE_HEIF](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_HEIF:kotlin.Int), [android.hardware.DataSpace#DATASPACE_HEIF_ULTRAHDR](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_HEIF_ULTRAHDR:kotlin.Int), [android.hardware.DataSpace#DATASPACE_JPEG_R](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JPEG_R:kotlin.Int), [android.hardware.DataSpace#DATASPACE_UNKNOWN](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_UNKNOWN:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SCRGB_LINEAR](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB_LINEAR:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SRGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SCRGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_DISPLAY_P3](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DISPLAY_P3:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020_HLG](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_HLG:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020_PQ](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_PQ:kotlin.Int), [android.hardware.DataSpace#DATASPACE_ADOBE_RGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_ADOBE_RGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_JFIF](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JFIF:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT601_625](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_625:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT601_525](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_525:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT709](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT709:kotlin.Int), [android.hardware.DataSpace#DATASPACE_DCI_P3](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DCI_P3:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SRGB_LINEAR](https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB_LINEAR:kotlin.Int), and android.hardware.DataSpace.DATASPACE_DISPLAY_BT2020 |

### setFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFence(fence: SyncFence): Unit
```

Set the fence file descriptor with this frame.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fence` | [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#):The fence file descriptor to be set for this frame. This value cannot be`null`. |

| Exceptions ||
|-----------------------|------------------------------------------------|
| `java.io.IOException` | if there is an error when setting a SyncFence. |

**See Also**

- [android.hardware.SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#) 

### setTimestamp

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTimestamp(timestamp: Long): Unit
```

Set the timestamp associated with this frame.

The timestamp is measured in nanoseconds, and is normally monotonically increasing. The timestamps for the images from different sources may have different timebases therefore may not be comparable. The specific meaning and timebase of the timestamp depend on the source providing images. See [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera.html#), [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#), [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer) and [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) for more details.

For images dequeued from [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter) via [ImageWriter.dequeueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage()), it's up to the application to set the timestamps correctly before sending them back to the [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter), or the timestamp will be generated automatically when [queueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image))is called.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `timestamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The timestamp to be set for this image. |
