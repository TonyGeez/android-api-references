# ETC1Util

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ETC1Util

Kotlin| [Java](https://developer.android.com/reference/android/opengl/ETC1Util "View this page in Java") 
| --- | --- |

```
open class ETC1Util
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.ETC1Util](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util#) |

Utility methods for using ETC1 compressed textures.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture) A utility class encapsulating a compressed ETC1 texture. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------|---|
| [ETC1Util](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util#ETC1Util())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ETC1Util.ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture)! | [compressTexture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util#compressTexture(java.nio.Buffer,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`input:` ` [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pixelSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Helper function that compresses an image into an ETC1Texture. |
| openstatic [ETC1Util.ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture)! | [createTexture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util#createTexture(java.io.InputStream))`(`input:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Create a new ETC1Texture from an input stream containing a PKM formatted compressed texture. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isETC1Supported](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util#isETC1Supported())`()` Check if ETC1 texture compression is supported by the active OpenGL ES context. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadTexture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util#loadTexture(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.opengl.ETC1Util.ETC1Texture))`(`target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `border:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallbackFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallbackType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `texture:` ` [ETC1Util.ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture)!`)` Convenience method to load an ETC1 texture whether or not the active OpenGL context supports the ETC1 texture compression format. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadTexture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util#loadTexture(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.io.InputStream))`(`target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `border:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallbackFormat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallbackType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `input:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Convenience method to load an ETC1 texture whether or not the active OpenGL context supports the ETC1 texture compression format. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeTexture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util#writeTexture(android.opengl.ETC1Util.ETC1Texture,%20java.io.OutputStream))`(`texture:` ` [ETC1Util.ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture)!`, `output:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Helper function that writes an ETC1Texture to an output stream formatted as a PKM file. |
| --- | --- |

## Public constructors

### ETC1Util

```
ETC1Util()
```

## Public methods

### compressTexture

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun compressTexture(
    input: Buffer!, 
    width: Int, 
    height: Int, 
    pixelSize: Int, 
    stride: Int
): ETC1Util.ETC1Texture!
```

Helper function that compresses an image into an ETC1Texture.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)!:a native order direct buffer containing the image data |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the width of the image in pixels |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the height of the image in pixels |
| --- | --- |
| `pixelSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size of a pixel in bytes (2 or 3) |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the width of a line of the image in bytes |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------|
| [ETC1Util.ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture)! | the ETC1 texture. |

### createTexture

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createTexture(input: InputStream!): ETC1Util.ETC1Texture!
```

Create a new ETC1Texture from an input stream containing a PKM formatted compressed texture.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:an input stream containing a PKM formatted compressed texture. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [ETC1Util.ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture)! | an ETC1Texture read from the input stream. |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### isETC1Supported

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isETC1Supported(): Boolean
```

Check if ETC1 texture compression is supported by the active OpenGL ES context.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the active OpenGL ES context supports ETC1 texture compression. |

### loadTexture

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun loadTexture(
    target: Int, 
    level: Int, 
    border: Int, 
    fallbackFormat: Int, 
    fallbackType: Int, 
    texture: ETC1Util.ETC1Texture!
): Unit
```

Convenience method to load an ETC1 texture whether or not the active OpenGL context supports the ETC1 texture compression format.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the texture target. |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the texture level |
| `border` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the border size. Typically 0. |
| --- | --- |
| `fallbackFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the format to use if ETC1 texture compression is not supported. Must be GL_RGB. |
| `fallbackType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type to use if ETC1 texture compression is not supported. Can be either GL_UNSIGNED_SHORT_5_6_5, which implies 16-bits-per-pixel, or GL_UNSIGNED_BYTE, which implies 24-bits-per-pixel. |
| `texture` | [ETC1Util.ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture)!:the ETC1 to load. |
| --- | --- |

### loadTexture

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun loadTexture(
    target: Int, 
    level: Int, 
    border: Int, 
    fallbackFormat: Int, 
    fallbackType: Int, 
    input: InputStream!
): Unit
```

Convenience method to load an ETC1 texture whether or not the active OpenGL context supports the ETC1 texture compression format.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the texture target. |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the texture level |
| `border` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the border size. Typically 0. |
| --- | --- |
| `fallbackFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the format to use if ETC1 texture compression is not supported. Must be GL_RGB. |
| `fallbackType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type to use if ETC1 texture compression is not supported. Can be either GL_UNSIGNED_SHORT_5_6_5, which implies 16-bits-per-pixel, or GL_UNSIGNED_BYTE, which implies 24-bits-per-pixel. |
| `input` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the input stream containing an ETC1 texture in PKM format. |
| --- | --- |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### writeTexture

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeTexture(
    texture: ETC1Util.ETC1Texture!, 
    output: OutputStream!
): Unit
```

Helper function that writes an ETC1Texture to an output stream formatted as a PKM file.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `texture` | [ETC1Util.ETC1Texture](https://developer.android.com/reference/kotlin/android/opengl/ETC1Util.ETC1Texture)!:the input texture. |
| `output` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the stream to write the formatted texture data to. |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |
