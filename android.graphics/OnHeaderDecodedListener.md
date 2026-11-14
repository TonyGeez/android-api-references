# ImageDecoder.OnHeaderDecodedListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnHeaderDecodedListener

Kotlin| [Java](https://developer.android.com/reference/android/graphics/ImageDecoder.OnHeaderDecodedListener "View this page in Java") 

```
interface OnHeaderDecodedListener
```

| [android.graphics.ImageDecoder.OnHeaderDecodedListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#) |

Interface for changing the default settings of a decode.

Supply an instance to [decodeDrawable](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeDrawable(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener))or [decodeBitmap](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#decodeBitmap(android.graphics.ImageDecoder.Source,%20android.graphics.ImageDecoder.OnHeaderDecodedListener)), which will call [onHeaderDecoded](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source))(in the same thread) once the size is known. The implementation of [onHeaderDecoded](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source))can then change the decode settings as desired.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHeaderDecoded](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnHeaderDecodedListener#onHeaderDecoded(android.graphics.ImageDecoder,%20android.graphics.ImageDecoder.ImageInfo,%20android.graphics.ImageDecoder.Source))`(`decoder:` ` [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder)`, `info:` ` [ImageDecoder.ImageInfo](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.ImageInfo)`, `source:` ` [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source)`)` Called by [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder) when the header has been decoded and the image size is known. |

## Public methods

### onHeaderDecoded

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onHeaderDecoded(
    decoder: ImageDecoder, 
    info: ImageDecoder.ImageInfo, 
    source: ImageDecoder.Source
): Unit
```

Called by [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder) when the header has been decoded and the image size is known.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `decoder` | [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder):the object performing the decode, for changing its default settings. This value cannot be`null`. |
| `info` | [ImageDecoder.ImageInfo](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.ImageInfo):information about the encoded image. This value cannot be`null`. |
| `source` | [ImageDecoder.Source](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.Source):object that created`decoder`. This value cannot be`null`. |
