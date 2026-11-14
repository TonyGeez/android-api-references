# ImageReader.OnImageAvailableListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnImageAvailableListener

Kotlin| [Java](../android/media/ImageReader.OnImageAvailableListener.md) 
| --- | --- |

```
interface OnImageAvailableListener
```

| [android.media.ImageReader.OnImageAvailableListener](../android/media/ImageReader.OnImageAvailableListener.md) |

Callback interface for being notified that a new image is available.

The onImageAvailable is called per image basis, that is, callback fires for every new frame available from ImageReader.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onImageAvailable](../android/media/ImageReader.OnImageAvailableListener.md))`(`reader:` ` [ImageReader](ImageReader.md)!`)` Callback that is called when a new image is available from ImageReader. |

## Public methods

### onImageAvailable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onImageAvailable(reader: ImageReader!): Unit
```

Callback that is called when a new image is available from ImageReader.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `reader` | [ImageReader](ImageReader.md)!:the ImageReader the callback is associated with. |

**See Also**

- [android.media.ImageReader](ImageReader.md)
- [android.media.Image](Image.md)
