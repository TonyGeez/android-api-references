# ImageWriter.OnImageReleasedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnImageReleasedListener

Kotlin| [Java](../android/media/ImageWriter.OnImageReleasedListener.md) 
| --- | --- |

```
interface OnImageReleasedListener
```

| [android.media.ImageWriter.OnImageReleasedListener](../android/media/ImageWriter.OnImageReleasedListener.md) |

ImageWriter callback interface, used to to asynchronously notify the application of various ImageWriter events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onImageReleased](../android/media/ImageWriter.OnImageReleasedListener.md))`(`writer:` ` [ImageWriter](ImageWriter.md)!`)` Callback that is called when an input Image is released back to ImageWriter after the data consumption. |

## Public methods

### onImageReleased

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onImageReleased(writer: ImageWriter!): Unit
```

Callback that is called when an input Image is released back to ImageWriter after the data consumption.

The client can use this callback to be notified that an input Image has been consumed and released by the downstream consumer. More specifically, this callback will be fired for below cases:
- The application dequeues an input Image via the [dequeueInputImage()](ImageWriter.md))method, uses it, and then queues it back to this ImageWriter via the [queueInputImage()](ImageWriter.md))method. After the downstream consumer uses and releases this image to this ImageWriter, this callback will be fired. This image will be available to be dequeued after this callback.
- The application obtains an Image from some other component (e.g. an [ImageReader](ImageReader.md)), uses it, and then queues it to this ImageWriter via [queueInputImage()](ImageWriter.md)). After the downstream consumer uses and releases this image to this ImageWriter, this callback will be fired.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `writer` | [ImageWriter](ImageWriter.md)!:the ImageWriter the callback is associated with. |

**See Also**

- [android.media.ImageWriter](ImageWriter.md)
- [android.media.Image](Image.md)
