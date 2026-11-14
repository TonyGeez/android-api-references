# ETC1

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ETC1

Kotlin| [Java](https://developer.android.com/reference/android/opengl/ETC1 "View this page in Java") 

```
open class ETC1
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.opengl.ETC1](https://developer.android.com/reference/kotlin/android/opengl/ETC1#) |

Methods for encoding and decoding ETC1 textures.

The standard for the ETC1 texture format can be found at http://www.khronos.org/registry/gles/extensions/OES/OES_compressed_ETC1_RGB8_texture.txt

The PKM file format is of a 16-byte header that describes the image bounds followed by the encoded ETC1 texture data.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DECODED_BLOCK_SIZE](https://developer.android.com/reference/kotlin/android/opengl/ETC1#DECODED_BLOCK_SIZE:kotlin.Int) Size in bytes of a decoded block. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENCODED_BLOCK_SIZE](https://developer.android.com/reference/kotlin/android/opengl/ETC1#ENCODED_BLOCK_SIZE:kotlin.Int) Size in bytes of an encoded block. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ETC1_RGB8_OES](https://developer.android.com/reference/kotlin/android/opengl/ETC1#ETC1_RGB8_OES:kotlin.Int) Accepted by the internalformat parameter of glCompressedTexImage2D. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ETC_PKM_HEADER_SIZE](https://developer.android.com/reference/kotlin/android/opengl/ETC1#ETC_PKM_HEADER_SIZE:kotlin.Int) Size of a PKM file header, in bytes. |

| Public constructors ||
|----------------------------------------------------------------------------------------------|---|
| [ETC1](https://developer.android.com/reference/kotlin/android/opengl/ETC1#ETC1())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [decodeBlock](https://developer.android.com/reference/kotlin/android/opengl/ETC1#decodeBlock(java.nio.Buffer,%20java.nio.Buffer))`(`in:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`, `out:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`)` Decode a block of pixels. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [decodeImage](https://developer.android.com/reference/kotlin/android/opengl/ETC1#decodeImage(java.nio.Buffer,%20java.nio.Buffer,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`in:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`, `out:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pixelSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Decode an entire image. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [encodeBlock](https://developer.android.com/reference/kotlin/android/opengl/ETC1#encodeBlock(java.nio.Buffer,%20kotlin.Int,%20java.nio.Buffer))`(`in:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`, `validPixelMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `out:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`)` Encode a block of pixels. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [encodeImage](https://developer.android.com/reference/kotlin/android/opengl/ETC1#encodeImage(java.nio.Buffer,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.nio.Buffer))`(`in:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pixelSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `out:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`)` Encode an entire image. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [formatHeader](https://developer.android.com/reference/kotlin/android/opengl/ETC1#formatHeader(java.nio.Buffer,%20kotlin.Int,%20kotlin.Int))`(`header:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Format a PKM header |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEncodedDataSize](https://developer.android.com/reference/kotlin/android/opengl/ETC1#getEncodedDataSize(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the size of the encoded image data (does not include size of PKM header). |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/opengl/ETC1#getHeight(java.nio.Buffer))`(`header:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`)` Read the image height from a PKM header |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/opengl/ETC1#getWidth(java.nio.Buffer))`(`header:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`)` Read the image width from a PKM header |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/android/opengl/ETC1#isValid(java.nio.Buffer))`(`header:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`)` Check if a PKM header is correctly formatted. |

## Constants

### DECODED_BLOCK_SIZE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DECODED_BLOCK_SIZE: Int
```

Size in bytes of a decoded block. 

 Value: 48

### ENCODED_BLOCK_SIZE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENCODED_BLOCK_SIZE: Int
```

Size in bytes of an encoded block. 

 Value: 8

### ETC1_RGB8_OES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ETC1_RGB8_OES: Int
```

Accepted by the internalformat parameter of glCompressedTexImage2D. 

 Value: 36196

### ETC_PKM_HEADER_SIZE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ETC_PKM_HEADER_SIZE: Int
```

Size of a PKM file header, in bytes. 

 Value: 16

## Public constructors

### ETC1

```
ETC1()
```

## Public methods

### decodeBlock

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decodeBlock(
    in: Buffer!, 
    out: Buffer!
): Unit
```

Decode a block of pixels.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:a native order direct buffer of size ENCODED_BLOCK_SIZE that contains the ETC1 compressed version of the data. |
| `out` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:a native order direct buffer of size DECODED_BLOCK_SIZE that will receive the decoded data. The data represents a 4 x 4 square of 3-byte pixels in form R, G, B. Byte (3 \* (x + 4 \* y) is the R value of pixel (x, y). |

### decodeImage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun decodeImage(
    in: Buffer!, 
    out: Buffer!, 
    width: Int, 
    height: Int, 
    pixelSize: Int, 
    stride: Int
): Unit
```

Decode an entire image.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:native order direct buffer of the encoded data. |
| `out` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:native order direct buffer of the image data. Will be written such that pixel (x,y) is at pIn + pixelSize \* x + stride \* y. Must be large enough to store entire image. |
| `pixelSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):must be 2 or 3. 2 is an GL_UNSIGNED_SHORT_5_6_5 image, 3 is a GL_BYTE RGB image. |

### encodeBlock

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun encodeBlock(
    in: Buffer!, 
    validPixelMask: Int, 
    out: Buffer!
): Unit
```

Encode a block of pixels.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:a native order direct buffer of size DECODED_BLOCK_SIZE that represent a 4 x 4 square of 3-byte pixels in form R, G, B. Byte (3 \* (x + 4 \* y) is the R value of pixel (x, y). |
| `validPixelMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is a 16-bit mask where bit (1 \<\< (x + y \* 4)) indicates whether the corresponding (x,y) pixel is valid. Invalid pixel color values are ignored when compressing. |
| `out` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:a native order direct buffer of size ENCODED_BLOCK_SIZE that receives the ETC1 compressed version of the data. |

### encodeImage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun encodeImage(
    in: Buffer!, 
    width: Int, 
    height: Int, 
    pixelSize: Int, 
    stride: Int, 
    out: Buffer!
): Unit
```

Encode an entire image.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:a native order direct buffer of the image data. Formatted such that pixel (x,y) is at pIn + pixelSize \* x + stride \* y; |
| `out` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:a native order direct buffer of the encoded data. Must be large enough to store entire encoded image. |
| `pixelSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):must be 2 or 3. 2 is an GL_UNSIGNED_SHORT_5_6_5 image, 3 is a GL_BYTE RGB image. |

### formatHeader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatHeader(
    header: Buffer!, 
    width: Int, 
    height: Int
): Unit
```

Format a PKM header

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `header` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:native order direct buffer of the header. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the width of the image in pixels. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the height of the image in pixels. |

### getEncodedDataSize

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getEncodedDataSize(
    width: Int, 
    height: Int
): Int
```

Return the size of the encoded image data (does not include size of PKM header). 

### getHeight

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getHeight(header: Buffer!): Int
```

Read the image height from a PKM header

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `header` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:native order direct buffer of the header. |

### getWidth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getWidth(header: Buffer!): Int
```

Read the image width from a PKM header

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `header` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:native order direct buffer of the header. |

### isValid

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isValid(header: Buffer!): Boolean
```

Check if a PKM header is correctly formatted.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `header` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:native order direct buffer of the header. |
