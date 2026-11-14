# ImageDecoder.OnPartialImageListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPartialImageListener

Kotlin| [Java](https://developer.android.com/reference/android/graphics/ImageDecoder.OnPartialImageListener "View this page in Java") 
| --- | --- |

```
interface OnPartialImageListener
```

| [android.graphics.ImageDecoder.OnPartialImageListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener#) |

Interface for inspecting a [DecodeException](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException) and potentially preventing it from being thrown.

If an instance is passed to [setOnPartialImageListener](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder#setOnPartialImageListener(android.graphics.ImageDecoder.OnPartialImageListener)), a [DecodeException](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException) that would otherwise have been thrown can be inspected inside [onPartialImage](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener#onPartialImage(android.graphics.ImageDecoder.DecodeException)). If [onPartialImage](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener#onPartialImage(android.graphics.ImageDecoder.DecodeException))returns`true`, a partial image will be created.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPartialImage](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.OnPartialImageListener#onPartialImage(android.graphics.ImageDecoder.DecodeException))`(`exception:` ` [ImageDecoder.DecodeException](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException)`)` Called by [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder) when there is only a partial image to display. |

## Public methods

### onPartialImage

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPartialImage(exception: ImageDecoder.DecodeException): Boolean
```

Called by [ImageDecoder](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder) when there is only a partial image to display.

If decoding is interrupted after having decoded a partial image, this method will be called. The implementation can inspect the [DecodeException](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException) and optionally finish the rest of the decode creation process to create a partial [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) or [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [ImageDecoder.DecodeException](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException):exception containing information about the decode interruption. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`to create and return a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) or [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap) with partial data.`false`(which is the default) to abort the decode and throw`e`. Any undecoded lines in the image will be blank. |
