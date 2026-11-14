# ImageDecoder.OnHeaderDecodedListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnHeaderDecodedListener

Kotlin| [Java](../android/graphics/ImageDecoder.OnHeaderDecodedListener.md) 
| --- | --- |

```
interface OnHeaderDecodedListener
```

| [android.graphics.ImageDecoder.OnHeaderDecodedListener](../android/graphics/ImageDecoder.OnHeaderDecodedListener.md) |

Interface for changing the default settings of a decode.

Supply an instance to [decodeDrawable](ImageDecoder.md))or [decodeBitmap](ImageDecoder.md)), which will call [onHeaderDecoded](../android/graphics/ImageDecoder.OnHeaderDecodedListener.md))(in the same thread) once the size is known. The implementation of [onHeaderDecoded](../android/graphics/ImageDecoder.OnHeaderDecodedListener.md))can then change the decode settings as desired.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHeaderDecoded](../android/graphics/ImageDecoder.OnHeaderDecodedListener.md))`(`decoder:` ` [ImageDecoder](ImageDecoder.md)`, `info:` ` [ImageDecoder.ImageInfo](../android/graphics/ImageDecoder.ImageInfo.md)`, `source:` ` [ImageDecoder.Source](../android/graphics/ImageDecoder.Source.md)`)` Called by [ImageDecoder](ImageDecoder.md) when the header has been decoded and the image size is known. |

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

Called by [ImageDecoder](ImageDecoder.md) when the header has been decoded and the image size is known.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `decoder` | [ImageDecoder](ImageDecoder.md):the object performing the decode, for changing its default settings. This value cannot be`null`. |
| `info` | [ImageDecoder.ImageInfo](../android/graphics/ImageDecoder.ImageInfo.md):information about the encoded image. This value cannot be`null`. |
| `source` | [ImageDecoder.Source](../android/graphics/ImageDecoder.Source.md):object that created`decoder`. This value cannot be`null`. |
| --- | --- |
