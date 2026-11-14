# ImageFormat

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImageFormat

Kotlin| [Java](../android/graphics/ImageFormat.md) 
| --- | --- |

```
open class ImageFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.ImageFormat](../android/graphics/ImageFormat.md) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEPTH16](../android/graphics/ImageFormat.md) Android dense depth image format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEPTH_JPEG](../android/graphics/ImageFormat.md) Depth augmented compressed JPEG format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEPTH_POINT_CLOUD](../android/graphics/ImageFormat.md) Android sparse depth point cloud format. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLEX_RGBA_8888](../android/graphics/ImageFormat.md) Multi-plane Android RGBA format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLEX_RGB_888](../android/graphics/ImageFormat.md) Multi-plane Android RGB format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEIC](../android/graphics/ImageFormat.md) Compressed HEIC format. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEIC_ULTRAHDR](../android/graphics/ImageFormat.md) High Efficiency Image File Format (HEIF) with embedded HDR gain map |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JPEG](../android/graphics/ImageFormat.md) Compressed JPEG format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JPEG_R](../android/graphics/ImageFormat.md) Compressed JPEG format that includes an embedded recovery map. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NV16](../android/graphics/ImageFormat.md) YCbCr format, used for video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NV21](../android/graphics/ImageFormat.md) YCrCb format used for images, which uses the NV21 encoding format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIVATE](../android/graphics/ImageFormat.md) Android private opaque image format. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RAW10](../android/graphics/ImageFormat.md) Android 10-bit raw format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RAW12](../android/graphics/ImageFormat.md) Android 12-bit raw format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RAW_PRIVATE](../android/graphics/ImageFormat.md) Private raw camera sensor image format, a single channel image with implementation dependent pixel layout. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RAW_SENSOR](../android/graphics/ImageFormat.md) General raw camera sensor image format, usually representing a single-channel Bayer-mosaic image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_565](../android/graphics/ImageFormat.md) RGB format used for pictures encoded as RGB_565. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN](../android/graphics/ImageFormat.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [Y8](../android/graphics/ImageFormat.md) Android Y8 format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCBCR_P010](../android/graphics/ImageFormat.md) Android YUV P010 format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCBCR_P210](../android/graphics/ImageFormat.md) Android YUV P210 format. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YUV_420_888](../android/graphics/ImageFormat.md) Multi-plane Android YUV 420 format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YUV_422_888](../android/graphics/ImageFormat.md) Multi-plane Android YUV 422 format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YUV_444_888](../android/graphics/ImageFormat.md) Multi-plane Android YUV 444 format |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YUY2](../android/graphics/ImageFormat.md) YCbCr format used for images, which uses YUYV (YUY2) encoding format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YV12](../android/graphics/ImageFormat.md) Android YUV format. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [ImageFormat](../android/graphics/ImageFormat.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBitsPerPixel](../android/graphics/ImageFormat.md))`(`format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Use this function to retrieve the number of bits per pixel of an ImageFormat. |

## Constants

### DEPTH16

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEPTH16: Int
```

Android dense depth image format.

Each pixel is 16 bits, representing a depth ranging measurement from a depth camera or similar sensor. The 16-bit sample consists of a confidence value and the actual ranging measurement.

The confidence value is an estimate of correctness for this sample. It is encoded in the 3 most significant bits of the sample, with a value of 0 representing 100% confidence, a value of 1 representing 0% confidence, a value of 2 representing 1/7, a value of 3 representing 2/7, and so on.

As an example, the following sample extracts the range and confidence from the first pixel of a DEPTH16-format [android.media.Image](../android/media/Image.md), and converts the confidence to a floating-point value between 0 and 1.f inclusive, with 1.f representing maximum confidence: 

```kotlin
ShortBuffer shortDepthBuffer = img.getPlanes()[0].getBuffer().asShortBuffer();
     short depthSample = shortDepthBuffer.get()
     short depthRange = (short) (depthSample & 0x1FFF);
     short depthConfidence = (short) ((depthSample >> 13) & 0x7);
     float depthPercentage = depthConfidence == 0 ? 1.f : (depthConfidence - 1) / 7.f;
  
```

<br />

This format assumes

- an even width
- an even height
- a horizontal stride multiple of 16 pixels

<br />

```kotlin
y_size = stride * height 
```
When produced by a camera, the units for the range are millimeters. 

 Value: 1144402265

### DEPTH_JPEG

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEPTH_JPEG: Int
```

Depth augmented compressed JPEG format.

JPEG compressed main image along with XMP embedded depth metadata following ISO 16684-1:2011(E). 

 Value: 1768253795

### DEPTH_POINT_CLOUD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEPTH_POINT_CLOUD: Int
```

Android sparse depth point cloud format.

A variable-length list of 3D points plus a confidence value, with each point represented by four floats; first the X, Y, Z position coordinates, and then the confidence value.

The number of points is`(size of the buffer in bytes) / 16`.

The coordinate system and units of the position values depend on the source of the point cloud data. The confidence value is between 0.f and 1.f, inclusive, with 0 representing 0% confidence and 1.f representing 100% confidence in the measured position values.

As an example, the following code extracts the first depth point in a DEPTH_POINT_CLOUD format [android.media.Image](../android/media/Image.md): 

```kotlin
FloatBuffer floatDepthBuffer = img.getPlanes()[0].getBuffer().asFloatBuffer();
     float x = floatDepthBuffer.get();
     float y = floatDepthBuffer.get();
     float z = floatDepthBuffer.get();
     float confidence = floatDepthBuffer.get();
  
```
For camera devices that support the [DEPTH_OUTPUT](../android/hardware/camera2/CameraMetadata.md) capability, DEPTH_POINT_CLOUD coordinates have units of meters, and the coordinate system is defined by the camera's pose transforms: [android.hardware.camera2.CameraCharacteristics#LENS_POSE_TRANSLATION](../android/hardware/camera2/CameraCharacteristics.md) and [android.hardware.camera2.CameraCharacteristics#LENS_POSE_ROTATION](../android/hardware/camera2/CameraCharacteristics.md). That means the origin is the optical center of the camera device, and the positive Z axis points along the camera's optical axis, toward the scene. 

 Value: 257

### FLEX_RGBA_8888

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLEX_RGBA_8888: Int
```

Multi-plane Android RGBA format

This format is a generic RGBA format, capable of describing most RGBA formats, with 8 bits per color sample.

Images in this format are always represented by four separate buffers of data, one for each color plane. Additional information always accompanies the buffers, describing the row stride and the pixel stride for each plane.

The order of planes in the array returned by [Image#getPlanes()](../android/media/Image.md))is guaranteed such that plane #0 is always R (red), plane #1 is always G (green), plane #2 is always B (blue), and plane #3 is always A (alpha). This format may represent pre-multiplied or non-premultiplied alpha.

All four planes are guaranteed to have the same row strides and pixel strides.

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.media.MediaCodec](../android/media/MediaCodec.md) through [android.media.MediaCodec#getOutputImage](../android/media/MediaCodec.md))object. 

 Value: 42

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.MediaCodec](../android/media/MediaCodec.md) 

### FLEX_RGB_888

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLEX_RGB_888: Int
```

Multi-plane Android RGB format

This format is a generic RGB format, capable of describing most RGB formats, with 8 bits per color sample.

Images in this format are always represented by three separate buffers of data, one for each color plane. Additional information always accompanies the buffers, describing the row stride and the pixel stride for each plane.

The order of planes in the array returned by [Image#getPlanes()](../android/media/Image.md))is guaranteed such that plane #0 is always R (red), plane #1 is always G (green), and plane #2 is always B (blue).

All three planes are guaranteed to have the same row strides and pixel strides.

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.media.MediaCodec](../android/media/MediaCodec.md) through [android.media.MediaCodec#getOutputImage](../android/media/MediaCodec.md))object. 

 Value: 41

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.MediaCodec](../android/media/MediaCodec.md) 

### HEIC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEIC: Int
```

Compressed HEIC format.

This format defines the HEIC brand of High Efficiency Image File Format as described in ISO/IEC 23008-12. 

 Value: 1212500294

### HEIC_ULTRAHDR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEIC_ULTRAHDR: Int
```

High Efficiency Image File Format (HEIF) with embedded HDR gain map

This format defines the HEIC brand of High Efficiency Image File Format as described in ISO/IEC 23008-12:2024 with HDR gain map according to ISO/CD 21496‐1. 

 Value: 4102

### JPEG

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JPEG: Int
```

Compressed JPEG format.

This format is always supported as an output format for the [android.hardware.camera2](../android/hardware/camera2/_package.md) API, and as a picture format for the older [android.hardware.Camera](../android/hardware/Camera.md) API 

 Value: 256

### JPEG_R

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JPEG_R: Int
```

Compressed JPEG format that includes an embedded recovery map.

JPEG compressed main image along with embedded recovery map following the [Ultra HDR Image format specification](https://developer.android.com/guide/topics/media/hdr-image-format). 

 Value: 4101

### NV16

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NV16: Int
```

YCbCr format, used for video.

For the [android.hardware.camera2](../android/hardware/camera2/_package.md) API, the [YUV_420_888](../android/graphics/ImageFormat.md) format is recommended for YUV output instead.

Whether this format is supported by the old camera API can be determined by [android.hardware.Camera.Parameters#getSupportedPreviewFormats()](../android/hardware/Camera.Parameters.md)). 

 Value: 16

### NV21

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NV21: Int
```

YCrCb format used for images, which uses the NV21 encoding format.

This is the default format for [android.hardware.Camera](../android/hardware/Camera.md) preview images, when not otherwise set with [android.hardware.Camera.Parameters#setPreviewFormat(int)](../android/hardware/Camera.Parameters.md)).

For the [android.hardware.camera2](../android/hardware/camera2/_package.md) API, the [YUV_420_888](../android/graphics/ImageFormat.md) format is recommended for YUV output instead. 

 Value: 17

### PRIVATE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIVATE: Int
```

Android private opaque image format.

The choices of the actual format and pixel data layout are entirely up to the device-specific and framework internal implementations, and may vary depending on use cases even for the same device. The buffers of this format can be produced by components like [ImageWriter](../android/media/ImageWriter.md), and interpreted correctly by consumers like [CameraDevice](../android/hardware/camera2/CameraDevice.md) based on the device/framework private information. However, these buffers are not directly accessible to the application.

When an [Image](../android/media/Image.md) of this format is obtained from an [ImageReader](../android/media/ImageReader.md) or [ImageWriter](../android/media/ImageWriter.md), the [getPlanes()](../android/media/Image.md))method will return an empty [Plane](../android/media/Image.Plane.md) array.

If a buffer of this format is to be used as an OpenGL ES texture, the framework will assume that sampling the texture will always return an alpha value of 1.0 (i.e. the buffer contains only opaque pixel values). 

 Value: 34

### RAW10

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW10: Int
```

Android 10-bit raw format

This is a single-plane, 10-bit per pixel, densely packed (in each row), unprocessed format, usually representing raw Bayer-pattern images coming from an image sensor.

In an image buffer with this format, starting from the first pixel of each row, each 4 consecutive pixels are packed into 5 bytes (40 bits). Each one of the first 4 bytes contains the top 8 bits of each pixel, The fifth byte contains the 2 least significant bits of the 4 pixels, the exact layout data for each 4 consecutive pixels is illustrated below (`Pi[j]`stands for the jth bit of the ith pixel):

| | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Byte 0: | P0\[9\] | P0\[8\] | P0\[7\] | P0\[6\] | P0\[5\] | P0\[4\] | P0\[3\] | P0\[2\] |
| Byte 1: | P1\[9\] | P1\[8\] | P1\[7\] | P1\[6\] | P1\[5\] | P1\[4\] | P1\[3\] | P1\[2\] |
| Byte 2: | P2\[9\] | P2\[8\] | P2\[7\] | P2\[6\] | P2\[5\] | P2\[4\] | P2\[3\] | P2\[2\] |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Byte 3: | P3\[9\] | P3\[8\] | P3\[7\] | P3\[6\] | P3\[5\] | P3\[4\] | P3\[3\] | P3\[2\] |
| Byte 4: | P3\[1\] | P3\[0\] | P2\[1\] | P2\[0\] | P1\[1\] | P1\[0\] | P0\[1\] | P0\[0\] |

This format assumes

- a width multiple of 4 pixels
- an even height

<br />

```kotlin
size = row stride * height
```
where the row stride is in*bytes* , not pixels.

Since this is a densely packed format, the pixel stride is always 0. The application must use the pixel data layout defined in above table to access each row data. When row stride is equal to`width * (10 / 8)`, there will be no padding bytes at the end of each row, the entire image data is densely packed. When stride is larger than`width * (10 / 8)`, padding bytes will be present at the end of each row.

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md)(if supported) through a [android.media.ImageReader](../android/media/ImageReader.md) object. The [Image#getPlanes()](../android/media/Image.md))will return a single plane containing the pixel data. The pixel stride is always 0 in [android.media.Image.Plane#getPixelStride()](../android/media/Image.Plane.md)), and the [android.media.Image.Plane#getRowStride()](../android/media/Image.Plane.md))describes the vertical neighboring pixel distance (in bytes) between adjacent rows. 

 Value: 37

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.ImageReader](../android/media/ImageReader.md)
- [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) 

### RAW12

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW12: Int
```

Android 12-bit raw format

This is a single-plane, 12-bit per pixel, densely packed (in each row), unprocessed format, usually representing raw Bayer-pattern images coming from an image sensor.

In an image buffer with this format, starting from the first pixel of each row, each two consecutive pixels are packed into 3 bytes (24 bits). The first and second byte contains the top 8 bits of first and second pixel. The third byte contains the 4 least significant bits of the two pixels, the exact layout data for each two consecutive pixels is illustrated below (Pi\[j\] stands for the jth bit of the ith pixel):

| | bit 7 | bit 6 | bit 5 | bit 4 | bit 3 | bit 2 | bit 1 | bit 0 |
|---------|----------|----------|----------|----------|----------|----------|----------|----------|
| Byte 0: | P0\[11\] | P0\[10\] | P0\[ 9\] | P0\[ 8\] | P0\[ 7\] | P0\[ 6\] | P0\[ 5\] | P0\[ 4\] |
| Byte 1: | P1\[11\] | P1\[10\] | P1\[ 9\] | P1\[ 8\] | P1\[ 7\] | P1\[ 6\] | P1\[ 5\] | P1\[ 4\] |
| Byte 2: | P1\[ 3\] | P1\[ 2\] | P1\[ 1\] | P1\[ 0\] | P0\[ 3\] | P0\[ 2\] | P0\[ 1\] | P0\[ 0\] |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

This format assumes

- a width multiple of 4 pixels
- an even height

<br />

```kotlin
size = row stride * height
```
where the row stride is in*bytes* , not pixels.

Since this is a densely packed format, the pixel stride is always 0. The application must use the pixel data layout defined in above table to access each row data. When row stride is equal to`width * (12 / 8)`, there will be no padding bytes at the end of each row, the entire image data is densely packed. When stride is larger than`width * (12 / 8)`, padding bytes will be present at the end of each row.

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md)(if supported) through a [android.media.ImageReader](../android/media/ImageReader.md) object. The [Image#getPlanes()](../android/media/Image.md))will return a single plane containing the pixel data. The pixel stride is always 0 in [android.media.Image.Plane#getPixelStride()](../android/media/Image.Plane.md)), and the [android.media.Image.Plane#getRowStride()](../android/media/Image.Plane.md))describes the vertical neighboring pixel distance (in bytes) between adjacent rows. 

 Value: 38

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.ImageReader](../android/media/ImageReader.md)
- [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) 

### RAW_PRIVATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_PRIVATE: Int
```

Private raw camera sensor image format, a single channel image with implementation dependent pixel layout.

RAW_PRIVATE is a format for unprocessed raw image buffers coming from an image sensor. The actual structure of buffers of this format is implementation-dependent. 

 Value: 36

### RAW_SENSOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_SENSOR: Int
```

General raw camera sensor image format, usually representing a single-channel Bayer-mosaic image. Each pixel color sample is stored with 16 bits of precision.

The layout of the color mosaic, the maximum and minimum encoding values of the raw pixel data, the color space of the image, and all other needed information to interpret a raw sensor image must be queried from the [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) which produced the image. 

 Value: 32

### RGB_565

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGB_565: Int
```

RGB format used for pictures encoded as RGB_565. See [android.hardware.Camera.Parameters#setPictureFormat(int)](../android/hardware/Camera.Parameters.md)). 

 Value: 4

### UNKNOWN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN: Int
```  

 Value: 0

### Y8

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val Y8: Int
```

Android Y8 format.

Y8 is a YUV planar format comprised of a WxH Y plane only, with each pixel being represented by 8 bits. It is equivalent to just the Y plane from [YV12](../android/graphics/ImageFormat.md) format.

This format assumes

- an even width
- an even height
- a horizontal stride multiple of 16 pixels

<br />

```kotlin
size = stride * height 
```

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md)(if supported) through a [android.media.ImageReader](../android/media/ImageReader.md) object. The [Image#getPlanes()](../android/media/Image.md))will return a single plane containing the pixel data. The pixel stride is always 1 in [android.media.Image.Plane#getPixelStride()](../android/media/Image.Plane.md)), and the [android.media.Image.Plane#getRowStride()](../android/media/Image.Plane.md))describes the vertical neighboring pixel distance (in bytes) between adjacent rows. 

 Value: 538982489

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.ImageReader](../android/media/ImageReader.md)
- [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) 

### YCBCR_P010

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCBCR_P010: Int
```

Android YUV P010 format.
P010 is a 10-bit 4:2:0 YCbCr semiplanar format comprised of a WxH Y plane followed by a Wx(H/2) CbCr plane. Each sample is represented by a 16-bit little-endian value, with the lower 6 bits set to zero.

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) through a [android.media.ImageReader](../android/media/ImageReader.md) object if this format is supported by [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md). 

 Value: 54

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.ImageReader](../android/media/ImageReader.md)
- [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) 

### YCBCR_P210

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCBCR_P210: Int
```

Android YUV P210 format.
P210 is a 10-bit 4:2:2 YCbCr semiplanar format comprised of a WxH Y plane followed by a WxH CbCr plane. Each sample is represented by a 16-bit little-endian value, with the lower 6 bits set to zero.

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) through a [android.media.ImageReader](../android/media/ImageReader.md) object if this format is supported by [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md). 

 Value: 60

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.ImageReader](../android/media/ImageReader.md)
- [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) 

### YUV_420_888

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YUV_420_888: Int
```

Multi-plane Android YUV 420 format

This format is a generic YCbCr format, capable of describing any 4:2:0 chroma-subsampled planar or semiplanar buffer (but not fully interleaved), with 8 bits per color sample.

Images in this format are always represented by three separate buffers of data, one for each color plane. Additional information always accompanies the buffers, describing the row stride and the pixel stride for each plane.

The order of planes in the array returned by [Image#getPlanes()](../android/media/Image.md))is guaranteed such that plane #0 is always Y, plane #1 is always U (Cb), and plane #2 is always V (Cr).

The Y-plane is guaranteed not to be interleaved with the U/V planes (in particular, pixel stride is always 1 in [yPlane.getPixelStride()](../android/media/Image.Plane.md))).

The U/V planes are guaranteed to have the same row stride and pixel stride (in particular, [uPlane.getRowStride()](../android/media/Image.Plane.md))== [vPlane.getRowStride()](../android/media/Image.Plane.md))and [uPlane.getPixelStride()](../android/media/Image.Plane.md))== [vPlane.getPixelStride()](../android/media/Image.Plane.md)); ).

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) through a [android.media.ImageReader](../android/media/ImageReader.md) object. 

 Value: 35

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.ImageReader](../android/media/ImageReader.md)
- [android.hardware.camera2.CameraDevice](../android/hardware/camera2/CameraDevice.md) 

### YUV_422_888

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YUV_422_888: Int
```

Multi-plane Android YUV 422 format

This format is a generic YCbCr format, capable of describing any 4:2:2 chroma-subsampled (planar, semiplanar or interleaved) format, with 8 bits per color sample.

Images in this format are always represented by three separate buffers of data, one for each color plane. Additional information always accompanies the buffers, describing the row stride and the pixel stride for each plane.

The order of planes in the array returned by [Image#getPlanes()](../android/media/Image.md))is guaranteed such that plane #0 is always Y, plane #1 is always U (Cb), and plane #2 is always V (Cr).

In contrast to the [YUV_420_888](../android/graphics/ImageFormat.md) format, the Y-plane may have a pixel stride greater than 1 in [yPlane.getPixelStride()](../android/media/Image.Plane.md)).

The U/V planes are guaranteed to have the same row stride and pixel stride (in particular, [uPlane.getRowStride()](../android/media/Image.Plane.md))== [vPlane.getRowStride()](../android/media/Image.Plane.md))and [uPlane.getPixelStride()](../android/media/Image.Plane.md))== [vPlane.getPixelStride()](../android/media/Image.Plane.md)); ).

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.media.MediaCodec](../android/media/MediaCodec.md) through [android.media.MediaCodec#getOutputImage](../android/media/MediaCodec.md))object. 

 Value: 39

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.MediaCodec](../android/media/MediaCodec.md) 

### YUV_444_888

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YUV_444_888: Int
```

Multi-plane Android YUV 444 format

This format is a generic YCbCr format, capable of describing any 4:4:4 (planar, semiplanar or interleaved) format, with 8 bits per color sample.

Images in this format are always represented by three separate buffers of data, one for each color plane. Additional information always accompanies the buffers, describing the row stride and the pixel stride for each plane.

The order of planes in the array returned by [Image#getPlanes()](../android/media/Image.md))is guaranteed such that plane #0 is always Y, plane #1 is always U (Cb), and plane #2 is always V (Cr).

In contrast to the [YUV_420_888](../android/graphics/ImageFormat.md) format, the Y-plane may have a pixel stride greater than 1 in [yPlane.getPixelStride()](../android/media/Image.Plane.md)).

The U/V planes are guaranteed to have the same row stride and pixel stride (in particular, [uPlane.getRowStride()](../android/media/Image.Plane.md))== [vPlane.getRowStride()](../android/media/Image.Plane.md))and [uPlane.getPixelStride()](../android/media/Image.Plane.md))== [vPlane.getPixelStride()](../android/media/Image.Plane.md)); ).

For example, the [android.media.Image](../android/media/Image.md) object can provide data in this format from a [android.media.MediaCodec](../android/media/MediaCodec.md) through [android.media.MediaCodec#getOutputImage](../android/media/MediaCodec.md))object. 

 Value: 40

**See Also**

- [android.media.Image](../android/media/Image.md)
- [android.media.MediaCodec](../android/media/MediaCodec.md) 

### YUY2

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YUY2: Int
```

YCbCr format used for images, which uses YUYV (YUY2) encoding format.

For the [android.hardware.camera2](../android/hardware/camera2/_package.md) API, the [YUV_420_888](../android/graphics/ImageFormat.md) format is recommended for YUV output instead.

This is an alternative format for [android.hardware.Camera](../android/hardware/Camera.md) preview images. Whether this format is supported by the camera hardware can be determined by [android.hardware.Camera.Parameters#getSupportedPreviewFormats()](../android/hardware/Camera.Parameters.md)). 

 Value: 20

### YV12

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YV12: Int
```

Android YUV format.

This format is exposed to software decoders and applications.

YV12 is a 4:2:0 YCrCb planar format comprised of a WxH Y plane followed by (W/2) x (H/2) Cr and Cb planes.

This format assumes

- an even width
- an even height
- a horizontal stride multiple of 16 pixels
- a vertical stride equal to the height

<br />

```kotlin
y_size = stride * height
  c_stride = ALIGN(stride/2, 16)
  c_size = c_stride * height/2
  size = y_size + c_size * 2
  cr_offset = y_size
  cb_offset = y_size + c_size
```

For the [android.hardware.camera2](../android/hardware/camera2/_package.md) API, the [YUV_420_888](../android/graphics/ImageFormat.md) format is recommended for YUV output instead.

For the older camera API, this format is guaranteed to be supported for [android.hardware.Camera](../android/hardware/Camera.md) preview images since API level 12; for earlier API versions, check [android.hardware.Camera.Parameters#getSupportedPreviewFormats()](../android/hardware/Camera.Parameters.md)).

Note that for camera preview callback use (see [android.hardware.Camera#setPreviewCallback](../android/hardware/Camera.md))), the stride value is the smallest possible; that is, it is equal to: 

```kotlin
stride = ALIGN(width, 16)
```  

 Value: 842094169

**See Also**

- [android.hardware.Camera.Parameters#setPreviewCallback](../android/hardware/Camera.md))
- [android.hardware.Camera.Parameters#setPreviewFormat](../android/hardware/Camera.Parameters.md))
- [android.hardware.Camera.Parameters#getSupportedPreviewFormats](../android/hardware/Camera.Parameters.md))

## Public constructors

### ImageFormat

```
ImageFormat()
```

## Public methods

### getBitsPerPixel

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getBitsPerPixel(format: Int): Int
```

Use this function to retrieve the number of bits per pixel of an ImageFormat.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.graphics.ImageFormat#UNKNOWN](../android/graphics/ImageFormat.md), [android.graphics.PixelFormat#RGBA_8888](../android/graphics/PixelFormat.md), [android.graphics.PixelFormat#RGBX_8888](../android/graphics/PixelFormat.md), [android.graphics.PixelFormat#RGB_888](../android/graphics/PixelFormat.md), [android.graphics.ImageFormat#RGB_565](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#YV12](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#Y8](../android/graphics/ImageFormat.md), android.graphics.ImageFormat.Y16, [android.graphics.ImageFormat#YCBCR_P010](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#YCBCR_P210](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#NV16](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#NV21](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#YUY2](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#JPEG](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#DEPTH_JPEG](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#YUV_420_888](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#YUV_422_888](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#YUV_444_888](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#FLEX_RGB_888](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#FLEX_RGBA_8888](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#RAW_SENSOR](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#RAW_PRIVATE](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#RAW10](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#RAW12](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#DEPTH16](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#DEPTH_POINT_CLOUD](../android/graphics/ImageFormat.md), android.graphics.ImageFormat.RAW_DEPTH, android.graphics.ImageFormat.RAW_DEPTH10, [android.graphics.ImageFormat#PRIVATE](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#HEIC](../android/graphics/ImageFormat.md), [android.graphics.ImageFormat#HEIC_ULTRAHDR](../android/graphics/ImageFormat.md), or [android.graphics.ImageFormat#JPEG_R](../android/graphics/ImageFormat.md) |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bits per pixel of the given format or -1 if the format doesn't exist or is not supported. |
