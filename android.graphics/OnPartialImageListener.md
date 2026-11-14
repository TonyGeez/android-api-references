# ImageDecoder.OnPartialImageListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPartialImageListener

Kotlin| [Java](../android/graphics/ImageDecoder.OnPartialImageListener.md) 
| --- | --- |

```
interface OnPartialImageListener
```

| [android.graphics.ImageDecoder.OnPartialImageListener](../android/graphics/ImageDecoder.OnPartialImageListener.md) |

Interface for inspecting a [DecodeException](../android/graphics/ImageDecoder.DecodeException.md) and potentially preventing it from being thrown.

If an instance is passed to [setOnPartialImageListener](ImageDecoder.md)), a [DecodeException](../android/graphics/ImageDecoder.DecodeException.md) that would otherwise have been thrown can be inspected inside [onPartialImage](../android/graphics/ImageDecoder.OnPartialImageListener.md)). If [onPartialImage](../android/graphics/ImageDecoder.OnPartialImageListener.md))returns`true`, a partial image will be created.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPartialImage](../android/graphics/ImageDecoder.OnPartialImageListener.md))`(`exception:` ` [ImageDecoder.DecodeException](../android/graphics/ImageDecoder.DecodeException.md)`)` Called by [ImageDecoder](ImageDecoder.md) when there is only a partial image to display. |

## Public methods

### onPartialImage

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPartialImage(exception: ImageDecoder.DecodeException): Boolean
```

Called by [ImageDecoder](ImageDecoder.md) when there is only a partial image to display.

If decoding is interrupted after having decoded a partial image, this method will be called. The implementation can inspect the [DecodeException](../android/graphics/ImageDecoder.DecodeException.md) and optionally finish the rest of the decode creation process to create a partial [Drawable](../android.graphics.drawable/Drawable.md) or [Bitmap](Bitmap.md).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [ImageDecoder.DecodeException](../android/graphics/ImageDecoder.DecodeException.md):exception containing information about the decode interruption. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`to create and return a [Drawable](../android.graphics.drawable/Drawable.md) or [Bitmap](Bitmap.md) with partial data.`false`(which is the default) to abort the decode and throw`e`. Any undecoded lines in the image will be blank. |
