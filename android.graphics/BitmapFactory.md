Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BitmapFactory

Kotlin | [Java](BitmapFactory.md)
| --- | --- |

```
open class BitmapFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.BitmapFactory](BitmapFactory.md) |

Creates Bitmap objects from various sources, including files, streams, and byte-arrays.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options` <br /> |

| Public constructors ||
|---|---|
| BitmapFactory <br /> |

| Public methods ||
|---|---|
| open static [Bitmap](Bitmap.md)! | decodeByteArray Decode an immutable bitmap from the specified byte array. |
| open static [Bitmap](Bitmap.md)! | decodeByteArray Decode an immutable bitmap from the specified byte array. |
| open static [Bitmap](Bitmap.md)! | decodeFile Decode a file path into a bitmap. |
| --- | --- |
| open static [Bitmap](Bitmap.md)! | decodeFile Decode a file path into a bitmap. |
| open static [Bitmap](Bitmap.md)! | decodeFileDescriptor Decode a bitmap from the file descriptor. |
| open static [Bitmap](Bitmap.md)! | decodeFileDescriptor Decode a bitmap from the file descriptor. |
| --- | --- |
| open static [Bitmap](Bitmap.md)! | decodeResource Synonym for decodeResource with null Options. |
| open static [Bitmap](Bitmap.md)! | decodeResource Synonym for opening the given resource and calling decodeResourceStream. |
| open static [Bitmap](Bitmap.md)? | decodeResourceStream Decode a new Bitmap from an InputStream. |
| --- | --- |
| open static [Bitmap](Bitmap.md)! | decodeStream Decode an input stream into a bitmap. |
| open static [Bitmap](Bitmap.md)? | decodeStream Decode an input stream into a bitmap. |

## Public constructors

### BitmapFactory

```
BitmapFactory()
```

## Public methods

### decodeByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeByteArray(
    data: ByteArray!, 
    offset: Int, 
    length: Int
): Bitmap!
```

Decode an immutable bitmap from the specified byte array.

| Parameters ||
|---|---|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: byte array of compressed image data |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): offset into imageData for where the decoder should begin parsing. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes, beginning at offset, to parse |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | The decoded bitmap, or null if the image could not be decoded. |

### decodeByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeByteArray(
    data: ByteArray!, 
    offset: Int, 
    length: Int, 
    opts: BitmapFactory.Options!
): Bitmap!
```

Decode an immutable bitmap from the specified byte array.

| Parameters ||
|---|---|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: byte array of compressed image data |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): offset into imageData for where the decoder should begin parsing. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes, beginning at offset, to parse |
| --- | --- |
| `opts` | [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)!: null-ok; Options that control downsampling and whether the image should be completely decoded, or just is size returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | The decoded bitmap, or null if the image data could not be decoded, or, if opts is non-null, if opts requested only the size be returned (in opts.outWidth and opts.outHeight) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPreferredConfig:android.graphics.Bitmap.Config` is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inMutable:kotlin.Boolean` is set, if the specified color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, or if the specified color space's transfer function is not an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters` |

### decodeFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeFile(pathName: String!): Bitmap!
```

Decode a file path into a bitmap. If the specified file name is null, or cannot be decoded into a bitmap, the function returns null.

| Parameters ||
|---|---|
| `pathName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: complete path name for the file to be decoded. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | the resulting decoded bitmap, or null if it could not be decoded. |

### decodeFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeFile(
    pathName: String!, 
    opts: BitmapFactory.Options!
): Bitmap!
```

Decode a file path into a bitmap. If the specified file name is null, or cannot be decoded into a bitmap, the function returns null.

| Parameters ||
|---|---|
| `pathName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: complete path name for the file to be decoded. |
| `opts` | [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)!: null-ok; Options that control downsampling and whether the image should be completely decoded, or just is size returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | The decoded bitmap, or null if the image data could not be decoded, or, if opts is non-null, if opts requested only the size be returned (in opts.outWidth and opts.outHeight) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPreferredConfig:android.graphics.Bitmap.Config` is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inMutable:kotlin.Boolean` is set, if the specified color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, or if the specified color space's transfer function is not an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters` |

### decodeFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeFileDescriptor(fd: FileDescriptor!): Bitmap!
```

Decode a bitmap from the file descriptor. If the bitmap cannot be decoded return null. The position within the descriptor will not be changed when this returns, so the descriptor can be used again as is.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)!: The file descriptor containing the bitmap data to decode |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | the decoded bitmap, or null |

### decodeFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeFileDescriptor(
    fd: FileDescriptor!, 
    outPadding: Rect!, 
    opts: BitmapFactory.Options!
): Bitmap!
```

Decode a bitmap from the file descriptor. If the bitmap cannot be decoded return null. The position within the descriptor will not be changed when this returns, so the descriptor can be used again as-is.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)!: The file descriptor containing the bitmap data to decode |
| `outPadding` | [Rect](Rect.md)!: If not null, return the padding rect for the bitmap if it exists, otherwise set padding to \[-1,-1,-1,-1\]. If no bitmap is returned (null) then padding is unchanged. |
| `opts` | [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)!: null-ok; Options that control downsampling and whether the image should be completely decoded, or just its size returned. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | the decoded bitmap, or null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPreferredConfig:android.graphics.Bitmap.Config` is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inMutable:kotlin.Boolean` is set, if the specified color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, or if the specified color space's transfer function is not an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters` |

### decodeResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeResource(
    res: Resources!, 
    id: Int
): Bitmap!
```

Synonym for decodeResource with null Options.

| Parameters ||
|---|---|
| `res` | [Resources](../android.content.res/Resources.md)!: The resources object containing the image data |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource id of the image data |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | The decoded bitmap, or null if the image could not be decoded. |

### decodeResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeResource(
    res: Resources!, 
    id: Int, 
    opts: BitmapFactory.Options!
): Bitmap!
```

Synonym for opening the given resource and calling decodeResourceStream.

| Parameters ||
|---|---|
| `res` | [Resources](../android.content.res/Resources.md)!: The resources object containing the image data |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource id of the image data |
| `opts` | [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)!: null-ok; Options that control downsampling and whether the image should be completely decoded, or just is size returned. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | The decoded bitmap, or null if the image data could not be decoded, or, if opts is non-null, if opts requested only the size be returned (in opts.outWidth and opts.outHeight) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPreferredConfig:android.graphics.Bitmap.Config` is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inMutable:kotlin.Boolean` is set, if the specified color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, or if the specified color space's transfer function is not an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters` |

### decodeResourceStream

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeResourceStream(
    res: Resources?, 
    value: TypedValue?, 
    is: InputStream?, 
    pad: Rect?, 
    opts: BitmapFactory.Options?
): Bitmap?
```

Decode a new Bitmap from an InputStream. This InputStream was obtained from resources, which we pass to be able to scale the bitmap accordingly.

| Parameters ||
|---|---|
| `res` | [Resources](../android.content.res/Resources.md)?: This value may be `null`. |
| `value` | [TypedValue](../android.util/TypedValue.md)?: This value may be `null`. |
| `is` | [InputStream](../java.io/InputStream.md)?: This value may be `null`. |
| --- | --- |
| `pad` | [Rect](Rect.md)?: This value may be `null`. |
| `opts` | [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?: This value may be `null`. |

| Return ||
|---|---|
| Bitmap | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPreferredConfig:android.graphics.Bitmap.Config` is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inMutable:kotlin.Boolean` is set, if the specified color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, or if the specified color space's transfer function is not an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters` |

### decodeStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeStream(is: InputStream!): Bitmap!
```

Decode an input stream into a bitmap. If the input stream is null, or cannot be used to decode a bitmap, the function returns null. The stream's position will be where ever it was after the encoded data was read.

| Parameters ||
|---|---|
| `is` | [InputStream](../java.io/InputStream.md)!: The input stream that holds the raw data to be decoded into a bitmap. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap!` | The decoded bitmap, or null if the image data could not be decoded. |

### decodeStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun decodeStream(
    is: InputStream?, 
    outPadding: Rect?, 
    opts: BitmapFactory.Options?
): Bitmap?
```

Decode an input stream into a bitmap. If the input stream is null, or cannot be used to decode a bitmap, the function returns null. The stream's position will be where ever it was after the encoded data was read.

| Parameters ||
|---|---|
| `is` | [InputStream](../java.io/InputStream.md)?: The input stream that holds the raw data to be decoded into a bitmap. This value may be `null`. |
| `outPadding` | [Rect](Rect.md)?: If not null, return the padding rect for the bitmap if it exists, otherwise set padding to \[-1,-1,-1,-1\]. If no bitmap is returned (null) then padding is unchanged. |
| `opts` | [BitmapFactory.Options](../android/graphics/BitmapFactory.Options.md)?: null-ok; Options that control downsampling and whether the image should be completely decoded, or just is size returned. |
| --- | --- |

| Return ||
|---|---|
| Bitmap | The decoded bitmap, or null if the image data could not be decoded, or, if opts is non-null, if opts requested only the size be returned (in opts.outWidth and opts.outHeight) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPreferredConfig:android.graphics.Bitmap.Config` is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inMutable:kotlin.Boolean` is set, if the specified color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, or if the specified color space's transfer function is not an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters` Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, if markSupported returns true, `is.mark(1024)` would be called. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, this is no longer the case. |
