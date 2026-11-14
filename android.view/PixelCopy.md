# PixelCopy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PixelCopy

Kotlin| [Java](../android/view/PixelCopy.md) 
| --- | --- |

```
class PixelCopy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.PixelCopy](../android/view/PixelCopy.md) |

Provides a mechanisms to issue pixel copy requests to allow for copy operations from [Surface](../android/view/Surface.md) to [Bitmap](../android/graphics/Bitmap.md)

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md) Listener for observing the completion of a PixelCopy request. |
| | [Request](../android/view/PixelCopy.Request.md) Represents a PixelCopy request. |
| | [Result](../android/view/PixelCopy.Result.md) Contains the result of a PixelCopy request |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DESTINATION_INVALID](../android/view/PixelCopy.md) The destination isn't a valid copy target. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SOURCE_INVALID](../android/view/PixelCopy.md) It is not possible to copy from the source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SOURCE_NO_DATA](../android/view/PixelCopy.md) The source has nothing to copy from. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TIMEOUT](../android/view/PixelCopy.md) A timeout occurred while trying to acquire a buffer from the source to copy from. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](../android/view/PixelCopy.md) The pixel copy request failed with an unknown error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](../android/view/PixelCopy.md) The pixel copy request succeeded |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](../android/view/PixelCopy.md))`(`request:` ` [PixelCopy.Request](../android/view/PixelCopy.Request.md)`, `callbackExecutor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [Consumer](../java/util/function/Consumer.md)< [PixelCopy.Result](../android/view/PixelCopy.Result.md)!>`)` Executes the pixel copy request |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](../android/view/PixelCopy.md))`(`source:` ` [Surface](../android/view/Surface.md)`, `dest:` ` [Bitmap](../android/graphics/Bitmap.md)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md)`, `listenerThread:` ` [Handler](../android/os/Handler.md)`)` Requests a copy of the pixels from a [Surface](../android/view/Surface.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](../android/view/PixelCopy.md))`(`source:` ` [Surface](../android/view/Surface.md)`, `srcRect:` ` [Rect](../android/graphics/Rect.md)?`, `dest:` ` [Bitmap](../android/graphics/Bitmap.md)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md)`, `listenerThread:` ` [Handler](../android/os/Handler.md)`)` Requests a copy of the pixels at the provided [Rect](../android/graphics/Rect.md) from a [Surface](../android/view/Surface.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](../android/view/PixelCopy.md))`(`source:` ` [SurfaceView](../android/view/SurfaceView.md)`, `dest:` ` [Bitmap](../android/graphics/Bitmap.md)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md)`, `listenerThread:` ` [Handler](../android/os/Handler.md)`)` Requests for the display content of a [SurfaceView](../android/view/SurfaceView.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](../android/view/PixelCopy.md))`(`source:` ` [SurfaceView](../android/view/SurfaceView.md)`, `srcRect:` ` [Rect](../android/graphics/Rect.md)?`, `dest:` ` [Bitmap](../android/graphics/Bitmap.md)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md)`, `listenerThread:` ` [Handler](../android/os/Handler.md)`)` Requests for the display content of a [SurfaceView](../android/view/SurfaceView.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](../android/view/PixelCopy.md))`(`source:` ` [Window](../android/view/Window.md)`, `dest:` ` [Bitmap](../android/graphics/Bitmap.md)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md)`, `listenerThread:` ` [Handler](../android/os/Handler.md)`)` Requests a copy of the pixels from a [Window](../android/view/Window.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](../android/view/PixelCopy.md))`(`source:` ` [Window](../android/view/Window.md)`, `srcRect:` ` [Rect](../android/graphics/Rect.md)?`, `dest:` ` [Bitmap](../android/graphics/Bitmap.md)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md)`, `listenerThread:` ` [Handler](../android/os/Handler.md)`)` Requests a copy of the pixels at the provided [Rect](../android/graphics/Rect.md) from a [Window](../android/view/Window.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). |

## Constants

### ERROR_DESTINATION_INVALID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DESTINATION_INVALID: Int
```

The destination isn't a valid copy target. If the destination is a bitmap this can occur if the bitmap is too large for the hardware to copy to. It can also occur if the destination has been destroyed. 

 Value: 5

### ERROR_SOURCE_INVALID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SOURCE_INVALID: Int
```

It is not possible to copy from the source. This can happen if the source is hardware-protected or destroyed. 

 Value: 4

### ERROR_SOURCE_NO_DATA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SOURCE_NO_DATA: Int
```

The source has nothing to copy from. When the source is a [Surface](../android/view/Surface.md) this means that no buffers have been queued yet. Wait for the source to produce a frame and try again. 

 Value: 3

### ERROR_TIMEOUT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TIMEOUT: Int
```

A timeout occurred while trying to acquire a buffer from the source to copy from. 

 Value: 2

### ERROR_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN: Int
```

The pixel copy request failed with an unknown error. 

 Value: 1

### SUCCESS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUCCESS: Int
```

The pixel copy request succeeded 

 Value: 0

## Public methods

### request

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun request(
    request: PixelCopy.Request, 
    callbackExecutor: Executor, 
    listener: Consumer<PixelCopy.Result!>
): Unit
```

Executes the pixel copy request

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [PixelCopy.Request](../android/view/PixelCopy.Request.md):The request to execute This value cannot be`null`. |
| `callbackExecutor` | [Executor](../java/util/concurrent/Executor.md):The executor to run the callback on This value cannot be`null`. |
| `listener` | [Consumer](../java/util/function/Consumer.md)\< [PixelCopy.Result](../android/view/PixelCopy.Result.md)!\>:The callback for when the copy request is completed This value cannot be`null`. |
| --- | --- |

### request

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun request(
    source: Surface, 
    dest: Bitmap, 
    listener: PixelCopy.OnPixelCopyFinishedListener, 
    listenerThread: Handler
): Unit
```

Requests a copy of the pixels from a [Surface](../android/view/Surface.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). The contents of the source will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](../android/graphics/Bitmap.Config.md). The most recently queued buffer in the Surface will be used as the source of the copy.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Surface](../android/view/Surface.md):The source from which to copy This value cannot be`null`. |
| `dest` | [Bitmap](../android/graphics/Bitmap.md):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md):Callback for when the pixel copy request completes This value cannot be`null`. |
| --- | --- |
| `listenerThread` | [Handler](../android/os/Handler.md):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

### request

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun request(
    source: Surface, 
    srcRect: Rect?, 
    dest: Bitmap, 
    listener: PixelCopy.OnPixelCopyFinishedListener, 
    listenerThread: Handler
): Unit
```

Requests a copy of the pixels at the provided [Rect](../android/graphics/Rect.md) from a [Surface](../android/view/Surface.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). The contents of the source rect will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](../android/graphics/Bitmap.Config.md). The most recently queued buffer in the Surface will be used as the source of the copy.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Surface](../android/view/Surface.md):The source from which to copy This value cannot be`null`. |
| `srcRect` | [Rect](../android/graphics/Rect.md)?:The area of the source to copy from. If this is null the copy area will be the entire surface. The rect will be clamped to the bounds of the Surface. |
| `dest` | [Bitmap](../android/graphics/Bitmap.md):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| --- | --- |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](../android/os/Handler.md):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

### request

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun request(
    source: SurfaceView, 
    dest: Bitmap, 
    listener: PixelCopy.OnPixelCopyFinishedListener, 
    listenerThread: Handler
): Unit
```

Requests for the display content of a [SurfaceView](../android/view/SurfaceView.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). The contents of the source will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](../android/graphics/Bitmap.Config.md). The most recently queued buffer in the SurfaceView's Surface will be used as the source of the copy.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [SurfaceView](../android/view/SurfaceView.md):The source from which to copy This value cannot be`null`. |
| `dest` | [Bitmap](../android/graphics/Bitmap.md):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md):Callback for when the pixel copy request completes This value cannot be`null`. |
| --- | --- |
| `listenerThread` | [Handler](../android/os/Handler.md):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

### request

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun request(
    source: SurfaceView, 
    srcRect: Rect?, 
    dest: Bitmap, 
    listener: PixelCopy.OnPixelCopyFinishedListener, 
    listenerThread: Handler
): Unit
```

Requests for the display content of a [SurfaceView](../android/view/SurfaceView.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). The contents of the source will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](../android/graphics/Bitmap.Config.md). The most recently queued buffer in the SurfaceView's Surface will be used as the source of the copy.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [SurfaceView](../android/view/SurfaceView.md):The source from which to copy This value cannot be`null`. |
| `srcRect` | [Rect](../android/graphics/Rect.md)?:The area of the source to copy from. If this is null the copy area will be the entire surface. The rect will be clamped to the bounds of the Surface. |
| `dest` | [Bitmap](../android/graphics/Bitmap.md):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| --- | --- |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](../android/os/Handler.md):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

### request

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun request(
    source: Window, 
    dest: Bitmap, 
    listener: PixelCopy.OnPixelCopyFinishedListener, 
    listenerThread: Handler
): Unit
```

Requests a copy of the pixels from a [Window](../android/view/Window.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). The contents of the source will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](../android/graphics/Bitmap.Config.md). The most recently queued buffer in the Window's Surface will be used as the source of the copy. Note: This is limited to being able to copy from Window's with a non-null DecorView. If [Window.peekDecorView()](../android/view/Window.md))is null this throws an [IllegalArgumentException](../java/lang/IllegalArgumentException.md). It will similarly throw an exception if the DecorView has not yet acquired a backing surface. It is recommended that [OnDrawListener](../android/view/ViewTreeObserver.OnDrawListener.md) is used to ensure that at least one draw has happened before trying to copy from the window, otherwise either an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) will be thrown or an error will be returned to the [OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Window](../android/view/Window.md):The source from which to copy This value cannot be`null`. |
| `dest` | [Bitmap](../android/graphics/Bitmap.md):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md):Callback for when the pixel copy request completes This value cannot be`null`. |
| --- | --- |
| `listenerThread` | [Handler](../android/os/Handler.md):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

### request

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun request(
    source: Window, 
    srcRect: Rect?, 
    dest: Bitmap, 
    listener: PixelCopy.OnPixelCopyFinishedListener, 
    listenerThread: Handler
): Unit
```

Requests a copy of the pixels at the provided [Rect](../android/graphics/Rect.md) from a [Window](../android/view/Window.md) to be copied into a provided [Bitmap](../android/graphics/Bitmap.md). The contents of the source rect will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](../android/graphics/Bitmap.Config.md). The most recently queued buffer in the Window's Surface will be used as the source of the copy. Note: This is limited to being able to copy from Window's with a non-null DecorView. If [Window.peekDecorView()](../android/view/Window.md))is null this throws an [IllegalArgumentException](../java/lang/IllegalArgumentException.md). It will similarly throw an exception if the DecorView has not yet acquired a backing surface. It is recommended that [OnDrawListener](../android/view/ViewTreeObserver.OnDrawListener.md) is used to ensure that at least one draw has happened before trying to copy from the window, otherwise either an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) will be thrown or an error will be returned to the [OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md).

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Window](../android/view/Window.md):The source from which to copy This value cannot be`null`. |
| `srcRect` | [Rect](../android/graphics/Rect.md)?:The area of the source to copy from. If this is null the copy area will be the entire surface. The rect will be clamped to the bounds of the Surface. |
| `dest` | [Bitmap](../android/graphics/Bitmap.md):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| --- | --- |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](../android/view/PixelCopy.OnPixelCopyFinishedListener.md):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](../android/os/Handler.md):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |
