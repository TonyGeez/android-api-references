# BitmapRegionDecoder

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BitmapRegionDecoder

Kotlin| [Java](https://developer.android.com/reference/android/graphics/BitmapRegionDecoder "View this page in Java") 

```
class BitmapRegionDecoder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) |

BitmapRegionDecoder can be used to decode a rectangle region from an image. BitmapRegionDecoder is particularly useful when an original image is large and you only need parts of the image.

To create a BitmapRegionDecoder, call newInstance(...). Given a BitmapRegionDecoder, users can call decodeRegion() repeatedly to get a decoded Bitmap of the specified region.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)! | [decodeRegion](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#decodeRegion(android.graphics.Rect,%20android.graphics.BitmapFactory.Options))`(`rect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!`, `options:` ` [BitmapFactory.Options](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options)!`)` Decodes a rectangle region in the image specified by rect. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#getHeight())`()` Returns the original image's height |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#getWidth())`()` Returns the original image's width |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecycled](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#isRecycled())`()` Returns true if this region decoder has been recycled. |
| static [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | [newInstance](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(android.os.ParcelFileDescriptor))`(`pfd:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`)` Create a BitmapRegionDecoder from the file descriptor. |
| static [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | [newInstance](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a BitmapRegionDecoder from the specified byte array. |
| static [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | [newInstance](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isShareable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a BitmapRegionDecoder from the specified byte array. |
| static [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | [newInstance](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(java.io.FileDescriptor,%20kotlin.Boolean))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`, `isShareable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a BitmapRegionDecoder from the file descriptor. |
| static [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#)? | [newInstance](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(java.io.InputStream))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)`)` Create a BitmapRegionDecoder from an input stream. |
| static [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#)? | [newInstance](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(java.io.InputStream,%20kotlin.Boolean))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)`, `isShareable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a BitmapRegionDecoder from an input stream. |
| static [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | [newInstance](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(kotlin.String))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a BitmapRegionDecoder from a file path. |
| static [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | [newInstance](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(kotlin.String,%20kotlin.Boolean))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `isShareable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a BitmapRegionDecoder from a file path. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#recycle())`()` Frees up the memory associated with this region decoder, and mark the region decoder as "dead", meaning it will throw an exception if decodeRegion(), getWidth() or getHeight() is called. |

| Protected methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#finalize())`()` <br /> |

## Public methods

### decodeRegion

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun decodeRegion(
    rect: Rect!, 
    options: BitmapFactory.Options!
): Bitmap!
```

Decodes a rectangle region in the image specified by rect.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!:The rectangle that specified the region to be decode. |
| `options` | [BitmapFactory.Options](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options)!:null-ok; Options that control downsampling. inPurgeable is not supported. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap)! | The decoded bitmap, or null if the image data could not be decoded. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if [BitmapFactory.Options.inPreferredConfig](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPreferredConfig:android.graphics.Bitmap.Config) is [android.graphics.Bitmap.Config#HARDWARE](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config) and [BitmapFactory.Options.inMutable](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inMutable:kotlin.Boolean) is set, if the specified color space is not [RGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model), or if the specified color space's transfer function is not an [ICC parametric curve](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters) |

### getHeight

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

Returns the original image's height 

### getWidth

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

Returns the original image's width 

### isRecycled

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRecycled(): Boolean
```

Returns true if this region decoder has been recycled. If so, then it is an error to try use its method.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the region decoder has been recycled |

### newInstance

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(pfd: ParcelFileDescriptor): BitmapRegionDecoder
```

Create a BitmapRegionDecoder from the file descriptor. The position within the descriptor will not be changed when this returns, so the descriptor can be used again as is. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pfd` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):The parcel file descriptor containing the data to decode This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if the image format is not supported or can not be decoded. |

### newInstance

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(
    data: ByteArray, 
    offset: Int, 
    length: Int
): BitmapRegionDecoder
```

Create a BitmapRegionDecoder from the specified byte array. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):byte array of compressed image data. This value cannot be`null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into data for where the decoder should begin parsing. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes, beginning at offset, to parse |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if the image format is not supported or can not be decoded. |

### newInstance

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(
    data: ByteArray, 
    offset: Int, 
    length: Int, 
    isShareable: Boolean
): BitmapRegionDecoder
```

**Deprecated:** *In favor of[newInstance(byte[],int,int)](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))*

Create a BitmapRegionDecoder from the specified byte array. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):byte array of compressed image data. This value cannot be`null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into data for where the decoder should begin parsing. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes, beginning at offset, to parse |
| `isShareable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):This field has been ignored since [Build.VERSION_CODES.GINGERBREAD](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#GINGERBREAD:kotlin.Int). |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if the image format is not supported or can not be decoded. |

### newInstance

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(
    fd: FileDescriptor, 
    isShareable: Boolean
): BitmapRegionDecoder
```

**Deprecated:** *In favor of [newInstance(android.os.ParcelFileDescriptor)](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(android.os.ParcelFileDescriptor))*

Create a BitmapRegionDecoder from the file descriptor. The position within the descriptor will not be changed when this returns, so the descriptor can be used again as is. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):The file descriptor containing the data to decode This value cannot be`null`. |
| `isShareable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):This field has been ignored since [Build.VERSION_CODES.KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int). |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if the image format is not supported or can not be decoded. |

### newInstance

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(is: InputStream): BitmapRegionDecoder?
```

Create a BitmapRegionDecoder from an input stream. The stream's position will be where ever it was after the encoded data was read. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#):The input stream that holds the raw data to be decoded into a BitmapRegionDecoder. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#)? | A new BitmapRegionDecoder, or`null`if`is`is`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if the image format is not supported or can not be decoded. |

### newInstance

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(
    is: InputStream, 
    isShareable: Boolean
): BitmapRegionDecoder?
```

**Deprecated:** *In favor of [newInstance(java.io.InputStream)](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(java.io.InputStream))*

*Prior to [Build.VERSION_CODES.KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int), if [is.markSupported()](https://developer.android.com/reference/kotlin/java/io/InputStream.html#markSupported())returns true,`is.mark(1024)`would be called. As of [Build.VERSION_CODES.KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int), this is no longer the case.*

<br />

Create a BitmapRegionDecoder from an input stream. The stream's position will be where ever it was after the encoded data was read. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#):The input stream that holds the raw data to be decoded into a BitmapRegionDecoder. This value cannot be`null`. |
| `isShareable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):This field has always been ignored. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#)? | A new BitmapRegionDecoder, or`null`if`is`is`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if the image format is not supported or can not be decoded. |

### newInstance

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(pathName: String): BitmapRegionDecoder
```

Create a BitmapRegionDecoder from a file path. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pathName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):complete path name for the file to be decoded. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if the image format is not supported or can not be decoded. |

### newInstance

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(
    pathName: String, 
    isShareable: Boolean
): BitmapRegionDecoder
```

**Deprecated:** *In favor of [newInstance(java.lang.String)](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#newInstance(kotlin.String))*

Create a BitmapRegionDecoder from a file path. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pathName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):complete path name for the file to be decoded. This value cannot be`null`. |
| `isShareable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):This field has always been ignored. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if the image format is not supported or can not be decoded. |

### recycle

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun recycle(): Unit
```

Frees up the memory associated with this region decoder, and mark the region decoder as "dead", meaning it will throw an exception if decodeRegion(), getWidth() or getHeight() is called.

This operation cannot be reversed, so it should only be called if you are sure there are no further uses for the region decoder. This is an advanced call, and normally need not be called, since the normal GC process will free up this memory when there are no more references to this region decoder.

## Protected methods

### finalize

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
