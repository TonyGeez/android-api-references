# YuvImage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# YuvImage

Kotlin| [Java](YuvImage.md) 
| --- | --- |

```
open class YuvImage
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.YuvImage](YuvImage.md) |

YuvImage contains YUV data and provides a method that compresses a region of the YUV data to a Jpeg. The YUV data should be provided as a single byte array irrespective of the number of image planes in it. Currently only ImageFormat.NV21 and ImageFormat.YUY2 are supported. To compress a rectangle region in the YUV data, users have to specify the region by left, top, width and height.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [YuvImage](YuvImage.md))`(`yuv:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `strides:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Construct an YuvImage. |
| [YuvImage](YuvImage.md))`(`yuv:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `strides:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`, `colorSpace:` ` [ColorSpace](ColorSpace.md)`)` Construct an YuvImage. |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compressToJpeg](YuvImage.md))`(`rectangle:` ` [Rect](Rect.md)!`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stream:` ` [OutputStream](../java.io/OutputStream.md)!`)` Compress a rectangle region in the YuvImage to a jpeg. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compressToJpegR](YuvImage.md))`(`sdr:` ` [YuvImage](YuvImage.md)`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stream:` ` [OutputStream](../java.io/OutputStream.md)`)` Compress the HDR image into JPEG/R format. |
| open [ColorSpace](ColorSpace.md) | [getColorSpace](YuvImage.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](YuvImage.md))`()` <br /> |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getStrides](YuvImage.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](YuvImage.md))`()` <br /> |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getYuvData](YuvImage.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYuvFormat](YuvImage.md))`()` <br /> |

## Public constructors

### YuvImage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
YuvImage(
    yuv: ByteArray!, 
    format: Int, 
    width: Int, 
    height: Int, 
    strides: IntArray!)
```

Construct an YuvImage. Use SRGB for as default [ColorSpace](ColorSpace.md).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `yuv` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The YUV data. In the case of more than one image plane, all the planes must be concatenated into a single byte array. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The YUV data format as defined in [ImageFormat](ImageFormat.md). |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the YuvImage. |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height of the YuvImage. |
| `strides` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:(Optional) Row bytes of each image plane. If yuv contains padding, the stride of each image must be provided. If strides is null, the method assumes no padding and derives the row bytes by format and width itself. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if format is not support; width or height \<= 0; or yuv is null. |

### YuvImage

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
YuvImage(
    yuv: ByteArray, 
    format: Int, 
    width: Int, 
    height: Int, 
    strides: IntArray?, 
    colorSpace: ColorSpace)
```

Construct an YuvImage.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `yuv` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):The YUV data. In the case of more than one image plane, all the planes must be concatenated into a single byte array. This value cannot be`null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The YUV data format as defined in [ImageFormat](ImageFormat.md). |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the YuvImage. |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height of the YuvImage. |
| `strides` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?:(Optional) Row bytes of each image plane. If yuv contains padding, the stride of each image must be provided. If strides is null, the method assumes no padding and derives the row bytes by format and width itself. |
| `colorSpace` | [ColorSpace](ColorSpace.md):The YUV image color space as defined in [ColorSpace](ColorSpace.md). If the parameter is null, SRGB will be set as the default value. |
| --- | --- |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if format is not support; width or height \<= 0; or yuv is null. |

## Public methods

### compressToJpeg

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compressToJpeg(
    rectangle: Rect!, 
    quality: Int, 
    stream: OutputStream!
): Boolean
```

Compress a rectangle region in the YuvImage to a jpeg. For image format, only ImageFormat.NV21 and ImageFormat.YUY2 are supported. For color space, only SRGB is supported.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rectangle` | [Rect](Rect.md)!:The rectangle region to be compressed. The medthod checks if rectangle is inside the image. Also, the method modifies rectangle if the chroma pixels in it are not matched with the luma pixels in it. |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Hint to the compressor, 0-100. 0 meaning compress for small size, 100 meaning compress for max quality. |
| `stream` | [OutputStream](../java.io/OutputStream.md)!:OutputStream to write the compressed data. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the compression is successful. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if rectangle is invalid; color space or image format is not supported; quality is not within \[0, 100\]; or stream is null. |

### compressToJpegR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compressToJpegR(
    sdr: YuvImage, 
    quality: Int, 
    stream: OutputStream
): Boolean
```

Compress the HDR image into JPEG/R format. Sample usage: hdr_image.compressToJpegR(sdr_image, 90, stream); For the SDR image, only YUV_420_888 image format is supported, and the following color spaces are supported: ColorSpace.Named.SRGB, ColorSpace.Named.DISPLAY_P3 For the HDR image, only YCBCR_P010 image format is supported, and the following color spaces are supported: ColorSpace.Named.BT2020_HLG, ColorSpace.Named.BT2020_PQ

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sdr` | [YuvImage](YuvImage.md):The SDR image, only ImageFormat.YUV_420_888 is supported. This value cannot be`null`. |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Hint to the compressor, 0-100. 0 meaning compress for small size, 100 meaning compress for max quality. |
| `stream` | [OutputStream](../java.io/OutputStream.md):OutputStream to write the compressed data. This value cannot be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the compression is successful. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if input images are invalid; quality is not within \[0, 100\]; or stream is null. |

### getColorSpace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorSpace(): ColorSpace
```

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [ColorSpace](ColorSpace.md) | the color space of the image. This value cannot be`null`. |

### getHeight

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the height of the image. |

### getStrides

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStrides(): IntArray!
```

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | the number of row bytes in each image plane. |

### getWidth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the width of the image. |

### getYuvData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYuvData(): ByteArray!
```

| Return ||
|------------------------------------------------------------------------------------------|---------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the YUV data. |

### getYuvFormat

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYuvFormat(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the YUV format as defined in [ImageFormat](ImageFormat.md). |
