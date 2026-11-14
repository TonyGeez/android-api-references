# BitmapRegionDecoder

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BitmapRegionDecoder

Kotlin| [Java](BitmapRegionDecoder.md) 
| --- | --- |

```
class BitmapRegionDecoder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.BitmapRegionDecoder](BitmapRegionDecoder.md) |

BitmapRegionDecoder can be used to decode a rectangle region from an image. BitmapRegionDecoder is particularly useful when an original image is large and you only need parts of the image.

To create a BitmapRegionDecoder, call newInstance(...). Given a BitmapRegionDecoder, users can call decodeRegion() repeatedly to get a decoded Bitmap of the specified region.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](Bitmap.md)! | [decodeRegion](BitmapRegionDecoder.md))`(`rect:` ` [Rect](Rect.md)!`, `options:` ` [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)!`)` Decodes a rectangle region in the image specified by rect. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](BitmapRegionDecoder.md))`()` Returns the original image's height |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](BitmapRegionDecoder.md))`()` Returns the original image's width |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecycled](BitmapRegionDecoder.md))`()` Returns true if this region decoder has been recycled. |
| static [BitmapRegionDecoder](BitmapRegionDecoder.md) | [newInstance](BitmapRegionDecoder.md))`(`pfd:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`)` Create a BitmapRegionDecoder from the file descriptor. |
| static [BitmapRegionDecoder](BitmapRegionDecoder.md) | [newInstance](BitmapRegionDecoder.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a BitmapRegionDecoder from the specified byte array. |
| --- | --- |
| static [BitmapRegionDecoder](BitmapRegionDecoder.md) | [newInstance](BitmapRegionDecoder.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isShareable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a BitmapRegionDecoder from the specified byte array. |
| static [BitmapRegionDecoder](BitmapRegionDecoder.md) | [newInstance](BitmapRegionDecoder.md))`(`fd:` ` [FileDescriptor](../java.io/FileDescriptor.md)`, `isShareable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a BitmapRegionDecoder from the file descriptor. |
| static [BitmapRegionDecoder](BitmapRegionDecoder.md)? | [newInstance](BitmapRegionDecoder.md))`(`is:` ` [InputStream](../java.io/InputStream.md)`)` Create a BitmapRegionDecoder from an input stream. |
| --- | --- |
| static [BitmapRegionDecoder](BitmapRegionDecoder.md)? | [newInstance](BitmapRegionDecoder.md))`(`is:` ` [InputStream](../java.io/InputStream.md)`, `isShareable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a BitmapRegionDecoder from an input stream. |
| static [BitmapRegionDecoder](BitmapRegionDecoder.md) | [newInstance](BitmapRegionDecoder.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a BitmapRegionDecoder from a file path. |
| static [BitmapRegionDecoder](BitmapRegionDecoder.md) | [newInstance](BitmapRegionDecoder.md))`(`pathName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `isShareable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a BitmapRegionDecoder from a file path. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](BitmapRegionDecoder.md))`()` Frees up the memory associated with this region decoder, and mark the region decoder as "dead", meaning it will throw an exception if decodeRegion(), getWidth() or getHeight() is called. |

| Protected methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](BitmapRegionDecoder.md))`()` <br /> |

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
| `rect` | [Rect](Rect.md)!:The rectangle that specified the region to be decode. |
| `options` | [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)!:null-ok; Options that control downsampling. inPurgeable is not supported. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Bitmap](Bitmap.md)! | The decoded bitmap, or null if the image data could not be decoded. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if [BitmapFactory.Options.inPreferredConfig](../android/graphics/BitmapFactory.Options.md) is [android.graphics.Bitmap.Config#HARDWARE](../android/graphics/Bitmap.Config.md) and [BitmapFactory.Options.inMutable](../android/graphics/BitmapFactory.Options.md) is set, if the specified color space is not [RGB](../android/graphics/ColorSpace.Model.md), or if the specified color space's transfer function is not an [ICC parametric curve](../android/graphics/ColorSpace.Rgb.TransferParameters.md) |

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
| `pfd` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):The parcel file descriptor containing the data to decode This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](BitmapRegionDecoder.md) | This value cannot be`null`. |

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
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](BitmapRegionDecoder.md) | This value cannot be`null`. |

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
| --- | --- |
| `isShareable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):This field has been ignored since [Build.VERSION_CODES.GINGERBREAD](../android/os/Build.VERSION_CODES.md). |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](BitmapRegionDecoder.md) | This value cannot be`null`. |

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

**Deprecated:** *In favor of [newInstance(android.os.ParcelFileDescriptor)](BitmapRegionDecoder.md))*

Create a BitmapRegionDecoder from the file descriptor. The position within the descriptor will not be changed when this returns, so the descriptor can be used again as is. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md):The file descriptor containing the data to decode This value cannot be`null`. |
| `isShareable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):This field has been ignored since [Build.VERSION_CODES.KITKAT](../android/os/Build.VERSION_CODES.md). |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](BitmapRegionDecoder.md) | This value cannot be`null`. |

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
| `is` | [InputStream](../java.io/InputStream.md):The input stream that holds the raw data to be decoded into a BitmapRegionDecoder. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [BitmapRegionDecoder](BitmapRegionDecoder.md)? | A new BitmapRegionDecoder, or`null`if`is`is`null`. |

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

**Deprecated:** *In favor of [newInstance(java.io.InputStream)](BitmapRegionDecoder.md))*

*Prior to [Build.VERSION_CODES.KITKAT](../android/os/Build.VERSION_CODES.md), if [is.markSupported()](../java.io/InputStream.md))returns true,`is.mark(1024)`would be called. As of [Build.VERSION_CODES.KITKAT](../android/os/Build.VERSION_CODES.md), this is no longer the case.*

<br />

Create a BitmapRegionDecoder from an input stream. The stream's position will be where ever it was after the encoded data was read. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](../java.io/InputStream.md):The input stream that holds the raw data to be decoded into a BitmapRegionDecoder. This value cannot be`null`. |
| `isShareable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):This field has always been ignored. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [BitmapRegionDecoder](BitmapRegionDecoder.md)? | A new BitmapRegionDecoder, or`null`if`is`is`null`. |

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
| [BitmapRegionDecoder](BitmapRegionDecoder.md) | This value cannot be`null`. |

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

**Deprecated:** *In favor of [newInstance(java.lang.String)](BitmapRegionDecoder.md))*

Create a BitmapRegionDecoder from a file path. Currently only the JPEG, PNG, WebP and HEIF formats are supported.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pathName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):complete path name for the file to be decoded. This value cannot be`null`. |
| `isShareable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):This field has always been ignored. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [BitmapRegionDecoder](BitmapRegionDecoder.md) | This value cannot be`null`. |

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
