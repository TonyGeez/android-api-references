# Image

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Image

Kotlin| [Java](Image.md) 
| --- | --- |

```
abstract class Image : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.Image](Image.md) |

A single complete image buffer to use with a media source such as a [MediaCodec](MediaCodec.md) or a [CameraDevice](../android.hardware.camera2/CameraDevice.md).

This class allows for efficient direct application access to the pixel data of the Image through one or more [ByteBuffers](../java.nio/ByteBuffer.md). Each buffer is encapsulated in a [Plane](../android/media/Image.Plane.md) that describes the layout of the pixel data in that plane. Due to this direct access, and unlike the [Bitmap](../android.graphics/Bitmap.md) class, Images are not directly usable as UI resources.

Since Images are often directly produced or consumed by hardware components, they are a limited resource shared across the system, and should be closed as soon as they are no longer needed.

For example, when using the [ImageReader](ImageReader.md) class to read out Images from various media sources, not closing old Image objects will prevent the availability of new Images once [the maximum outstanding image count](ImageReader.md))is reached. When this happens, the function acquiring new Images will typically throw an [IllegalStateException](../java.lang/IllegalStateException.md).

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| abstract | [Plane](../android/media/Image.Plane.md) A single color plane of image data. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](Image.md))`()` Free up this frame for reuse. |
| open [Rect](../android.graphics/Rect.md)! | [getCropRect](Image.md))`()` Get the crop rectangle associated with this frame. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataSpace](Image.md))`()` Get the dataspace associated with this frame. |
| --- | --- |
| open [SyncFence](../android.hardware/SyncFence.md) | [getFence](Image.md))`()` Get the SyncFence object associated with this frame. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFormat](Image.md))`()` Get the format for this image. |
| open [HardwareBuffer](../android.hardware/HardwareBuffer.md)? | [getHardwareBuffer](Image.md))`()` Get the [HardwareBuffer](../android.hardware/HardwareBuffer.md) handle of the input image intended for GPU and/or hardware access. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](Image.md))`()` The height of the image in pixels. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Image.Plane](../android/media/Image.Plane.md)!\>! | [getPlanes](Image.md))`()` Get the array of pixel planes for this Image. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestamp](Image.md))`()` Get the timestamp associated with this frame. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](Image.md))`()` The width of the image in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCropRect](Image.md))`(`cropRect:` ` [Rect](../android.graphics/Rect.md)!`)` Set the crop rectangle associated with this frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSpace](Image.md))`(`dataSpace:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the dataspace associated with this frame. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFence](Image.md))`(`fence:` ` [SyncFence](../android.hardware/SyncFence.md)`)` Set the fence file descriptor with this frame. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](Image.md))`(`timestamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Set the timestamp associated with this frame. |

## Public methods

### close

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Free up this frame for reuse.

After calling this method, calling any methods on this`Image`will result in an [IllegalStateException](../java.lang/IllegalStateException.md), and attempting to read from or write to [ByteBuffers](../java.nio/ByteBuffer.md) returned by an earlier [Plane.getBuffer](../android/media/Image.Plane.md))call will have undefined behavior. If the image was obtained from [ImageWriter](ImageWriter.md) via [ImageWriter.dequeueInputImage()](ImageWriter.md)), after calling this method, any image data filled by the application will be lost and the image will be returned to [ImageWriter](ImageWriter.md) for reuse. Images given to [queueInputImage()](ImageWriter.md))are automatically closed.

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.hardware.DataSpace#DATASPACE_DEPTH](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DYNAMIC_DEPTH](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_HEIF](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_HEIF_ULTRAHDR](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_JPEG_R](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_UNKNOWN](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SCRGB_LINEAR](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SRGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SCRGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DISPLAY_P3](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020_HLG](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020_PQ](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_ADOBE_RGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_JFIF](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT601_625](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT601_525](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT709](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DCI_P3](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SRGB_LINEAR](../android.hardware/DataSpace.md), and android.hardware.DataSpace.DATASPACE_DISPLAY_BT2020 |

### getFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFence(): SyncFence
```

Get the SyncFence object associated with this frame.

This function returns an invalid SyncFence after [getPlanes()](Image.md))on the image dequeued from [ImageWriter](ImageWriter.md) via [ImageWriter.dequeueInputImage()](ImageWriter.md)).

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [SyncFence](../android.hardware/SyncFence.md) | The SyncFence for this frame. This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------|
| `java.io.IOException` | if there is an error when a SyncFence object returns. |

**See Also**

- [android.hardware.SyncFence](../android.hardware/SyncFence.md) 

### getFormat

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFormat(): Int
```

Get the format for this image. This format determines the number of ByteBuffers needed to represent the image, and the general layout of the pixel data in each ByteBuffer.

The format is one of the values from [ImageFormat](../android.graphics/ImageFormat.md), [PixelFormat](../android.graphics/PixelFormat.md), or [HardwareBuffer](../android.hardware/HardwareBuffer.md). The mapping between the formats and the planes is as follows (any formats not listed will have 1 plane):

| Format | Plane count | Layout details |
|------------------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [JPEG](../android.graphics/ImageFormat.md) | 1 | Compressed data, so row and pixel strides are 0. To uncompress, use android.graphics.BitmapFactory#decodeByteArray. |
| [YUV_420_888](../android.graphics/ImageFormat.md) | 3 | A luminance plane followed by the Cb and Cr chroma planes. The chroma planes have half the width and height of the luminance plane (4:2:0 subsampling). Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| [YUV_422_888](../android.graphics/ImageFormat.md) | 3 | A luminance plane followed by the Cb and Cr chroma planes. The chroma planes have half the width and the full height of the luminance plane (4:2:2 subsampling). Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| --- | --- | --- |
| [YUV_444_888](../android.graphics/ImageFormat.md) | 3 | A luminance plane followed by the Cb and Cr chroma planes. The chroma planes have the same width and height as that of the luminance plane (4:4:4 subsampling). Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| [FLEX_RGB_888](../android.graphics/ImageFormat.md) | 3 | A R (red) plane followed by the G (green) and B (blue) planes. All planes have the same widths and heights. Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| [FLEX_RGBA_8888](../android.graphics/ImageFormat.md) | 4 | A R (red) plane followed by the G (green), B (blue), and A (alpha) planes. All planes have the same widths and heights. Each pixel sample in each plane has 8 bits. Each plane has its own row stride and pixel stride. |
| --- | --- | --- |
| [RAW_SENSOR](../android.graphics/ImageFormat.md) | 1 | A single plane of raw sensor image data, with 16 bits per color sample. The details of the layout need to be queried from the source of the raw sensor data, such as [CameraDevice](../android.hardware.camera2/CameraDevice.md). |
| [RAW_PRIVATE](../android.graphics/ImageFormat.md) | 1 | A single plane of raw sensor image data of private layout. The details of the layout is implementation specific. Row stride and pixel stride are undefined for this format. Calling [Plane.getRowStride()](../android/media/Image.Plane.md))or [Plane.getPixelStride()](../android/media/Image.Plane.md))on RAW_PRIVATE image will cause UnSupportedOperationException being thrown. |
| [HEIC](../android.graphics/ImageFormat.md) | 1 | Compressed data, so row and pixel strides are 0. To uncompress, use android.graphics.BitmapFactory#decodeByteArray. |
| --- | --- | --- |
| [YCBCR_P010](../android.graphics/ImageFormat.md) | 3 | P010 is a 4:2:0 YCbCr semiplanar format comprised of a WxH Y plane followed by a Wx(H/2) Cb and Cr planes. Each sample is represented by a 16-bit little-endian value, with the lower 6 bits set to zero. Since this is guaranteed to be a semi-planar format, the Cb plane can also be treated as an interleaved Cb/Cr plane. |
| [YCBCR_P210](../android.graphics/ImageFormat.md) | 3 | P210 is a 4:2:2 YCbCr semiplanar format comprised of a WxH Y plane followed by a WxH Cb and Cr planes. Each sample is represented by a 16-bit little-endian value, with the lower 6 bits set to zero. Since this is guaranteed to be a semi-planar format, the Cb plane can also be treated as an interleaved Cb/Cr plane. |

**See Also**

- [android.graphics.ImageFormat](../android.graphics/ImageFormat.md)
- [android.graphics.PixelFormat](../android.graphics/PixelFormat.md)
- [android.hardware.HardwareBuffer](../android.hardware/HardwareBuffer.md) 

### getHardwareBuffer

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHardwareBuffer(): HardwareBuffer?
```

Get the [HardwareBuffer](../android.hardware/HardwareBuffer.md) handle of the input image intended for GPU and/or hardware access.

The returned [HardwareBuffer](../android.hardware/HardwareBuffer.md) shall not be used after [Image.close()](Image.md))has been called.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HardwareBuffer](../android.hardware/HardwareBuffer.md)? | the HardwareBuffer associated with this Image or null if this Image doesn't support this feature. (Unsupported use cases include Image instances obtained through [MediaCodec](MediaCodec.md), and on versions prior to Android P, [ImageWriter](ImageWriter.md)). |

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

Get the array of pixel planes for this Image. The number of planes is determined by the format of the Image. The application will get an empty array if the image format is [PRIVATE](../android.graphics/ImageFormat.md), because the image pixel data is not directly accessible. The application can check the image format by calling [Image.getFormat()](Image.md)). 

### getTimestamp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTimestamp(): Long
```

Get the timestamp associated with this frame.

The timestamp is measured in nanoseconds, and is normally monotonically increasing. The timestamps for the images from different sources may have different timebases therefore may not be comparable. The specific meaning and timebase of the timestamp depend on the source providing images. See [Camera](../android.hardware/Camera.md), [CameraDevice](../android.hardware.camera2/CameraDevice.md), [MediaPlayer](MediaPlayer.md) and [MediaCodec](MediaCodec.md) for more details. 

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

If dataspace for an image is not set, dataspace value depends on [android.view.Surface](../android.view/Surface.md) that is provided in the [ImageWriter](ImageWriter.md) constructor.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSpace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The Dataspace to be set for this image Value is either`0`or a combination of [android.hardware.DataSpace#DATASPACE_DEPTH](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DYNAMIC_DEPTH](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_HEIF](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_HEIF_ULTRAHDR](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_JPEG_R](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_UNKNOWN](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SCRGB_LINEAR](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SRGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SCRGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DISPLAY_P3](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020_HLG](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020_PQ](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_ADOBE_RGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_JFIF](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT601_625](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT601_525](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT709](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DCI_P3](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SRGB_LINEAR](../android.hardware/DataSpace.md), and android.hardware.DataSpace.DATASPACE_DISPLAY_BT2020 |

### setFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFence(fence: SyncFence): Unit
```

Set the fence file descriptor with this frame.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fence` | [SyncFence](../android.hardware/SyncFence.md):The fence file descriptor to be set for this frame. This value cannot be`null`. |

| Exceptions ||
|-----------------------|------------------------------------------------|
| `java.io.IOException` | if there is an error when setting a SyncFence. |

**See Also**

- [android.hardware.SyncFence](../android.hardware/SyncFence.md) 

### setTimestamp

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTimestamp(timestamp: Long): Unit
```

Set the timestamp associated with this frame.

The timestamp is measured in nanoseconds, and is normally monotonically increasing. The timestamps for the images from different sources may have different timebases therefore may not be comparable. The specific meaning and timebase of the timestamp depend on the source providing images. See [Camera](../android.hardware/Camera.md), [CameraDevice](../android.hardware.camera2/CameraDevice.md), [MediaPlayer](MediaPlayer.md) and [MediaCodec](MediaCodec.md) for more details.

For images dequeued from [ImageWriter](ImageWriter.md) via [ImageWriter.dequeueInputImage()](ImageWriter.md)), it's up to the application to set the timestamps correctly before sending them back to the [ImageWriter](ImageWriter.md), or the timestamp will be generated automatically when [queueInputImage()](ImageWriter.md))is called.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `timestamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The timestamp to be set for this image. |
