# ImageWriter.OnImageReleasedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnImageReleasedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/ImageWriter.OnImageReleasedListener "View this page in Java") 

```
interface OnImageReleasedListener
```

| [android.media.ImageWriter.OnImageReleasedListener](https://developer.android.com/reference/kotlin/android/media/ImageWriter.OnImageReleasedListener#) |

ImageWriter callback interface, used to to asynchronously notify the application of various ImageWriter events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onImageReleased](https://developer.android.com/reference/kotlin/android/media/ImageWriter.OnImageReleasedListener#onImageReleased(android.media.ImageWriter))`(`writer:` ` [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter)!`)` Callback that is called when an input Image is released back to ImageWriter after the data consumption. |

## Public methods

### onImageReleased

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onImageReleased(writer: ImageWriter!): Unit
```

Callback that is called when an input Image is released back to ImageWriter after the data consumption.

The client can use this callback to be notified that an input Image has been consumed and released by the downstream consumer. More specifically, this callback will be fired for below cases:
- The application dequeues an input Image via the [dequeueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter#dequeueInputImage())method, uses it, and then queues it back to this ImageWriter via the [queueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image))method. After the downstream consumer uses and releases this image to this ImageWriter, this callback will be fired. This image will be available to be dequeued after this callback.
- The application obtains an Image from some other component (e.g. an [ImageReader](https://developer.android.com/reference/kotlin/android/media/ImageReader)), uses it, and then queues it to this ImageWriter via [queueInputImage()](https://developer.android.com/reference/kotlin/android/media/ImageWriter#queueInputImage(android.media.Image)). After the downstream consumer uses and releases this image to this ImageWriter, this callback will be fired.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `writer` | [ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter)!:the ImageWriter the callback is associated with. |

**See Also**

- [android.media.ImageWriter](https://developer.android.com/reference/kotlin/android/media/ImageWriter)
- [android.media.Image](https://developer.android.com/reference/kotlin/android/media/Image)
