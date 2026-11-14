# ImageReader.OnImageAvailableListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnImageAvailableListener

Kotlin| [Java](https://developer.android.com/reference/android/media/ImageReader.OnImageAvailableListener "View this page in Java") 

```
interface OnImageAvailableListener
```

| [android.media.ImageReader.OnImageAvailableListener](https://developer.android.com/reference/kotlin/android/media/ImageReader.OnImageAvailableListener#) |

Callback interface for being notified that a new image is available.

The onImageAvailable is called per image basis, that is, callback fires for every new frame available from ImageReader.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onImageAvailable](https://developer.android.com/reference/kotlin/android/media/ImageReader.OnImageAvailableListener#onImageAvailable(android.media.ImageReader))`(`reader:` ` [ImageReader](https://developer.android.com/reference/kotlin/android/media/ImageReader)!`)` Callback that is called when a new image is available from ImageReader. |

## Public methods

### onImageAvailable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onImageAvailable(reader: ImageReader!): Unit
```

Callback that is called when a new image is available from ImageReader.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `reader` | [ImageReader](https://developer.android.com/reference/kotlin/android/media/ImageReader)!:the ImageReader the callback is associated with. |

**See Also**

- [android.media.ImageReader](https://developer.android.com/reference/kotlin/android/media/ImageReader)
- [android.media.Image](https://developer.android.com/reference/kotlin/android/media/Image)
