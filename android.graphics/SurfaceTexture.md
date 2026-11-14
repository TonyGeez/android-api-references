# SurfaceTexture

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceTexture

Kotlin| [Java](SurfaceTexture.md) 
| --- | --- |

```
open class SurfaceTexture
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.SurfaceTexture](SurfaceTexture.md) |

Captures frames from an image stream as an OpenGL ES texture.

The image stream may come from either camera preview or video decode. A [android.view.Surface](../android.view/Surface.md) created from a SurfaceTexture can be used as an output destination for the [android.hardware.camera2](../android.hardware.camera2/_package.md), [android.media.MediaCodec](../android.media/MediaCodec.md), [android.media.MediaPlayer](../android.media/MediaPlayer.md), and [android.renderscript.Allocation](../android.renderscript/Allocation.md) APIs. When [updateTexImage](SurfaceTexture.md))is called, the contents of the texture object specified when the SurfaceTexture was created are updated to contain the most recent image from the image stream. This may cause some frames of the stream to be skipped.

A SurfaceTexture may also be used in place of a SurfaceHolder when specifying the output destination of the older [android.hardware.Camera](../android.hardware/Camera.md) API. Doing so will cause all the frames from the image stream to be sent to the SurfaceTexture object rather than to the device's display.

A typical pattern is to use SurfaceTexture to render frames to a [TextureView](../android.view/TextureView.md); however, a TextureView is not*required*for using the texture object. The texture object may be used as part of an OpenGL ES shader.

When sampling from the texture one should first transform the texture coordinates using the matrix queried via[getTransformMatrix(float[])](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture#getTransformMatrix(kotlin.FloatArray)). The transform matrix may change each time [updateTexImage](SurfaceTexture.md))is called, so it should be re-queried each time the texture image is updated. This matrix transforms traditional 2D OpenGL ES texture coordinate column vectors of the form (s, t, 0, 1) where s and t are on the inclusive interval \[0, 1\] to the proper sampling location in the streamed texture. This transform compensates for any properties of the image stream source that cause it to appear different from a traditional OpenGL ES texture. For example, sampling from the bottom left corner of the image can be accomplished by transforming the column vector (0, 0, 0, 1) using the queried matrix, while sampling from the top right corner of the image can be done by transforming (1, 1, 0, 1).

The texture object uses the GL_TEXTURE_EXTERNAL_OES texture target, which is defined by the [GL_OES_EGL_image_external](http://www.khronos.org/registry/gles/extensions/OES/OES_EGL_image_external.txt) OpenGL ES extension. This limits how the texture may be used. Each time the texture is bound it must be bound to the GL_TEXTURE_EXTERNAL_OES target rather than the GL_TEXTURE_2D target. Additionally, any OpenGL ES 2.0 shader that samples from the texture must declare its use of this extension using, for example, an "#extension GL_OES_EGL_image_external : require" directive. Such shaders must also access the texture using the samplerExternalOES GLSL sampler type.

SurfaceTexture objects may be created on any thread. [updateTexImage](SurfaceTexture.md))may only be called on the thread with the OpenGL ES context that contains the texture object. The frame-available callback is called on an arbitrary thread, so unless special care is taken [updateTexImage](SurfaceTexture.md))should not be called directly from the callback.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnFrameAvailableListener](../android/graphics/SurfaceTexture.OnFrameAvailableListener.md) Callback interface for being notified that a new stream frame is available. |
| open | [OutOfResourcesException](../android/graphics/SurfaceTexture.OutOfResourcesException.md) Exception thrown when a SurfaceTexture couldn't be created or resized. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SurfaceTexture](SurfaceTexture.md))`(`singleBufferMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Construct a new SurfaceTexture to stream images to a given OpenGL texture. |
| [SurfaceTexture](SurfaceTexture.md))`(`texName:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a new SurfaceTexture to stream images to a given OpenGL texture. |
| [SurfaceTexture](SurfaceTexture.md))`(`texName:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `singleBufferMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Construct a new SurfaceTexture to stream images to a given OpenGL texture. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachToGLContext](SurfaceTexture.md))`(`texName:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attach the SurfaceTexture to the OpenGL ES context that is current on the calling thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [detachFromGLContext](SurfaceTexture.md))`()` Detach the SurfaceTexture from the OpenGL ES context that owns the OpenGL ES texture object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataSpace](SurfaceTexture.md))`()` Retrieve the dataspace associated with the texture image set by the most recent call to [updateTexImage](SurfaceTexture.md)). |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestamp](SurfaceTexture.md))`()` Retrieve the timestamp associated with the texture image set by the most recent call to [updateTexImage](SurfaceTexture.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getTransformMatrix](SurfaceTexture.md))`(`mtx:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Retrieve the 4x4 texture coordinate transform matrix associated with the texture image set by the most recent call to [updateTexImage](SurfaceTexture.md)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReleased](SurfaceTexture.md))`()` Returns`true`if the SurfaceTexture was released. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](SurfaceTexture.md))`()` `release()`frees all the buffers and puts the SurfaceTexture into the 'abandoned' state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseTexImage](SurfaceTexture.md))`()` Releases the texture content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultBufferSize](SurfaceTexture.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the default size of the image buffers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnFrameAvailableListener](SurfaceTexture.md))`(`listener:` ` [SurfaceTexture.OnFrameAvailableListener](../android/graphics/SurfaceTexture.OnFrameAvailableListener.md)?`)` Register a callback to be invoked when a new image frame becomes available to the SurfaceTexture. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnFrameAvailableListener](SurfaceTexture.md))`(`listener:` ` [SurfaceTexture.OnFrameAvailableListener](../android/graphics/SurfaceTexture.OnFrameAvailableListener.md)?`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Register a callback to be invoked when a new image frame becomes available to the SurfaceTexture. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTexImage](SurfaceTexture.md))`()` Update the texture image to the most recent frame from the image stream. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](SurfaceTexture.md))`()` <br /> |

## Public constructors

### SurfaceTexture

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SurfaceTexture(singleBufferMode: Boolean)
```

Construct a new SurfaceTexture to stream images to a given OpenGL texture.

In single buffered mode the application is responsible for serializing access to the image content buffer. Each time the image content is to be updated, the [releaseTexImage()](SurfaceTexture.md))method must be called before the image content producer takes ownership of the buffer. For example, when producing image content with the NDK ANativeWindow_lock and ANativeWindow_unlockAndPost functions, [releaseTexImage()](SurfaceTexture.md))must be called before each ANativeWindow_lock, or that call will fail. When producing image content with OpenGL ES, [releaseTexImage()](SurfaceTexture.md))must be called before the first OpenGL ES function call each frame.

Unlike [SurfaceTexture(int,boolean)](SurfaceTexture.md)), which takes an OpenGL texture object name, this constructor creates the SurfaceTexture in detached mode. A texture name must be passed in using [attachToGLContext](SurfaceTexture.md))before calling [releaseTexImage()](SurfaceTexture.md))and producing image content using OpenGL ES.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `singleBufferMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the SurfaceTexture will be in single buffered mode. |

| Exceptions ||
|------------------------------------------------|------------------------------------------|
| `android.view.Surface.OutOfResourcesException` | If the SurfaceTexture cannot be created. |

### SurfaceTexture

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SurfaceTexture(texName: Int)
```

Construct a new SurfaceTexture to stream images to a given OpenGL texture.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `texName` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the OpenGL texture object name (e.g. generated via glGenTextures) |

| Exceptions ||
|------------------------------------------------|------------------------------------------|
| `android.view.Surface.OutOfResourcesException` | If the SurfaceTexture cannot be created. |

### SurfaceTexture

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SurfaceTexture(
    texName: Int, 
    singleBufferMode: Boolean)
```

Construct a new SurfaceTexture to stream images to a given OpenGL texture.

In single buffered mode the application is responsible for serializing access to the image content buffer. Each time the image content is to be updated, the [releaseTexImage()](SurfaceTexture.md))method must be called before the image content producer takes ownership of the buffer. For example, when producing image content with the NDK ANativeWindow_lock and ANativeWindow_unlockAndPost functions, [releaseTexImage()](SurfaceTexture.md))must be called before each ANativeWindow_lock, or that call will fail. When producing image content with OpenGL ES, [releaseTexImage()](SurfaceTexture.md))must be called before the first OpenGL ES function call each frame.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `texName` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the OpenGL texture object name (e.g. generated via glGenTextures) |
| `singleBufferMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the SurfaceTexture will be in single buffered mode. |

| Exceptions ||
|------------------------------------------------|------------------------------------------|
| `android.view.Surface.OutOfResourcesException` | If the SurfaceTexture cannot be created. |

## Public methods

### attachToGLContext

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attachToGLContext(texName: Int): Unit
```

Attach the SurfaceTexture to the OpenGL ES context that is current on the calling thread. A new OpenGL ES texture object is created and populated with the SurfaceTexture image frame that was current at the time of the last call to [detachFromGLContext](SurfaceTexture.md)). This new texture is bound to the`GL_TEXTURE_EXTERNAL_OES`texture target.

This can be used to access the SurfaceTexture image contents from multiple OpenGL ES contexts. Note, however, that the image contents are only accessible from one OpenGL ES context at a time.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `texName` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The name of the OpenGL ES texture that will be created. This texture name must be unused in the OpenGL ES context that is current on the calling thread. |

### detachFromGLContext

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun detachFromGLContext(): Unit
```

Detach the SurfaceTexture from the OpenGL ES context that owns the OpenGL ES texture object. This call must be made with the OpenGL ES context current on the calling thread. The OpenGL ES texture object will be deleted as a result of this call. After calling this method all calls to [updateTexImage](SurfaceTexture.md))will throw an [java.lang.IllegalStateException](../java.lang/IllegalStateException.md) until a successful call to [attachToGLContext](SurfaceTexture.md))is made.

This can be used to access the SurfaceTexture image contents from multiple OpenGL ES contexts. Note, however, that the image contents are only accessible from one OpenGL ES context at a time. 

### getDataSpace

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataSpace(): Int
```

Retrieve the dataspace associated with the texture image set by the most recent call to [updateTexImage](SurfaceTexture.md)).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.hardware.DataSpace#DATASPACE_DEPTH](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DYNAMIC_DEPTH](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_HEIF](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_HEIF_ULTRAHDR](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_JPEG_R](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_UNKNOWN](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SCRGB_LINEAR](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SRGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SCRGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DISPLAY_P3](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020_HLG](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020_PQ](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_ADOBE_RGB](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_JFIF](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT601_625](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT601_525](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT709](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DCI_P3](../android.hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SRGB_LINEAR](../android.hardware/DataSpace.md), and android.hardware.DataSpace.DATASPACE_DISPLAY_BT2020 |

### getTimestamp

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimestamp(): Long
```

Retrieve the timestamp associated with the texture image set by the most recent call to [updateTexImage](SurfaceTexture.md)).

This timestamp is in nanoseconds, and is normally monotonically increasing. The timestamp should be unaffected by time-of-day adjustments. The specific meaning and zero point of the timestamp depends on the source providing images to the SurfaceTexture. Unless otherwise specified by the image source, timestamps cannot generally be compared across SurfaceTexture instances, or across multiple program invocations. It is mostly useful for determining time offsets between subsequent frames.

For camera sources, timestamps should be strictly monotonic. Timestamps from MediaPlayer sources may be reset when the playback position is set. For EGL and Vulkan producers, the timestamp is the desired present time set with the`EGL_ANDROID_presentation_time`or`VK_GOOGLE_display_timing`extensions. 

### getTransformMatrix

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransformMatrix(mtx: FloatArray!): Unit
```

Retrieve the 4x4 texture coordinate transform matrix associated with the texture image set by the most recent call to [updateTexImage](SurfaceTexture.md)).

This transform matrix maps 2D homogeneous texture coordinates of the form (s, t, 0, 1) with s and t in the inclusive range \[0, 1\] to the texture coordinate that should be used to sample that location from the texture. Sampling the texture outside of the range of this transform is undefined.

The matrix is stored in column-major order so that it may be passed directly to OpenGL ES via the`glLoadMatrixf`or`glUniformMatrix4fv`functions.

If the underlying buffer has a crop associated with it, the transformation will also include a slight scale to cut off a 1-texel border around the edge of the crop. This ensures that when the texture is bilinear sampled that no texels outside of the buffer's valid region are accessed by the GPU, avoiding any sampling artifacts when scaling.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mtx` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the array into which the 4x4 matrix will be stored. The array must have exactly 16 elements. |

### isReleased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReleased(): Boolean
```

Returns`true`if the SurfaceTexture was released. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture#release()> 

### release

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

`release()`frees all the buffers and puts the SurfaceTexture into the 'abandoned' state. Once put in this state the SurfaceTexture can never leave it. When in the 'abandoned' state, all methods of the`IGraphicBufferProducer`interface will fail with the`NO_INIT`error.

Note that while calling this method causes all the buffers to be freed from the perspective of the SurfaceTexture, if there are additional references on the buffers (e.g. if a buffer is referenced by a client or by OpenGL ES as a texture) then those buffer will remain allocated.

Always call this method when you are done with SurfaceTexture. Failing to do so may delay resource deallocation for a significant amount of time. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture#isReleased()> 

### releaseTexImage

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun releaseTexImage(): Unit
```

Releases the texture content. This is needed in single buffered mode to allow the image content producer to take ownership of the image buffer.

For more information see [SurfaceTexture(int,boolean)](SurfaceTexture.md)). 

### setDefaultBufferSize

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDefaultBufferSize(
    width: Int, 
    height: Int
): Unit
```

Set the default size of the image buffers. The image producer may override the buffer size, in which case the producer-set buffer size will be used, not the default size set by this method. Both video and camera based image producers do override the size. This method may be used to set the image size when producing images with [android.graphics.Canvas](Canvas.md)(via [android.view.Surface#lockCanvas](../android.view/Surface.md))), or OpenGL ES (via an EGLSurface).

The new default buffer size will take effect the next time the image producer requests a buffer to fill. For [android.graphics.Canvas](Canvas.md) this will be the next time [android.view.Surface#lockCanvas](../android.view/Surface.md))is called. For OpenGL ES, the EGLSurface should be destroyed (via eglDestroySurface), made not-current (via eglMakeCurrent), and then recreated (via`eglCreateWindowSurface`) to ensure that the new default size has taken effect.

The width and height parameters must be no greater than the minimum of`GL_MAX_VIEWPORT_DIMS`and`GL_MAX_TEXTURE_SIZE`(see javax.microedition.khronos.opengles.GL10#glGetIntegerv). An error due to invalid dimensions might not be reported until updateTexImage() is called. 

### setOnFrameAvailableListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnFrameAvailableListener(listener: SurfaceTexture.OnFrameAvailableListener?): Unit
```

Register a callback to be invoked when a new image frame becomes available to the SurfaceTexture.

The callback may be called on an arbitrary thread, so it is not safe to call [updateTexImage](SurfaceTexture.md))without first binding the OpenGL ES context to the thread invoking the callback.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SurfaceTexture.OnFrameAvailableListener](../android/graphics/SurfaceTexture.OnFrameAvailableListener.md)?:The listener to use, or null to remove the listener. |

### setOnFrameAvailableListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnFrameAvailableListener(
    listener: SurfaceTexture.OnFrameAvailableListener?, 
    handler: Handler?
): Unit
```

Register a callback to be invoked when a new image frame becomes available to the SurfaceTexture.

If a handler is specified, the callback will be invoked on that handler's thread. If no handler is specified, then the callback may be called on an arbitrary thread, so it is not safe to call [updateTexImage](SurfaceTexture.md))without first binding the OpenGL ES context to the thread invoking the callback.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SurfaceTexture.OnFrameAvailableListener](../android/graphics/SurfaceTexture.OnFrameAvailableListener.md)?:The listener to use, or null to remove the listener. |
| `handler` | [Handler](../android.os/Handler.md)?:The handler on which the listener should be invoked, or null to use an arbitrary thread. |

### updateTexImage

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateTexImage(): Unit
```

Update the texture image to the most recent frame from the image stream. This may only be called while the OpenGL ES context that owns the texture is current on the calling thread. It will implicitly bind its texture to the`GL_TEXTURE_EXTERNAL_OES`texture target.

## Protected methods

### finalize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
