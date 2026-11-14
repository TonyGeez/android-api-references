# PixelCopy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PixelCopy

Kotlin| [Java](https://developer.android.com/reference/android/view/PixelCopy "View this page in Java") 

```
class PixelCopy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.PixelCopy](https://developer.android.com/reference/kotlin/android/view/PixelCopy#) |

Provides a mechanisms to issue pixel copy requests to allow for copy operations from [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) to [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener) Listener for observing the completion of a PixelCopy request. |
| | [Request](https://developer.android.com/reference/kotlin/android/view/PixelCopy.Request) Represents a PixelCopy request. |
| | [Result](https://developer.android.com/reference/kotlin/android/view/PixelCopy.Result) Contains the result of a PixelCopy request |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DESTINATION_INVALID](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_DESTINATION_INVALID:kotlin.Int) The destination isn't a valid copy target. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SOURCE_INVALID](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_SOURCE_INVALID:kotlin.Int) It is not possible to copy from the source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SOURCE_NO_DATA](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_SOURCE_NO_DATA:kotlin.Int) The source has nothing to copy from. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TIMEOUT](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_TIMEOUT:kotlin.Int) A timeout occurred while trying to acquire a buffer from the source to copy from. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/PixelCopy#ERROR_UNKNOWN:kotlin.Int) The pixel copy request failed with an unknown error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/view/PixelCopy#SUCCESS:kotlin.Int) The pixel copy request succeeded |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](https://developer.android.com/reference/kotlin/android/view/PixelCopy#request(android.view.PixelCopy.Request,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`request:` ` [PixelCopy.Request](https://developer.android.com/reference/kotlin/android/view/PixelCopy.Request)`, `callbackExecutor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [PixelCopy.Result](https://developer.android.com/reference/kotlin/android/view/PixelCopy.Result)!>`)` Executes the pixel copy request |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](https://developer.android.com/reference/kotlin/android/view/PixelCopy#request(android.view.Surface,%20android.graphics.Bitmap,%20android.view.PixelCopy.OnPixelCopyFinishedListener,%20android.os.Handler))`(`source:` ` [Surface](https://developer.android.com/reference/kotlin/android/view/Surface)`, `dest:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener)`, `listenerThread:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)`)` Requests a copy of the pixels from a [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](https://developer.android.com/reference/kotlin/android/view/PixelCopy#request(android.view.Surface,%20android.graphics.Rect,%20android.graphics.Bitmap,%20android.view.PixelCopy.OnPixelCopyFinishedListener,%20android.os.Handler))`(`source:` ` [Surface](https://developer.android.com/reference/kotlin/android/view/Surface)`, `srcRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `dest:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener)`, `listenerThread:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)`)` Requests a copy of the pixels at the provided [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) from a [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](https://developer.android.com/reference/kotlin/android/view/PixelCopy#request(android.view.SurfaceView,%20android.graphics.Bitmap,%20android.view.PixelCopy.OnPixelCopyFinishedListener,%20android.os.Handler))`(`source:` ` [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView)`, `dest:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener)`, `listenerThread:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)`)` Requests for the display content of a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](https://developer.android.com/reference/kotlin/android/view/PixelCopy#request(android.view.SurfaceView,%20android.graphics.Rect,%20android.graphics.Bitmap,%20android.view.PixelCopy.OnPixelCopyFinishedListener,%20android.os.Handler))`(`source:` ` [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView)`, `srcRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `dest:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener)`, `listenerThread:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)`)` Requests for the display content of a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](https://developer.android.com/reference/kotlin/android/view/PixelCopy#request(android.view.Window,%20android.graphics.Bitmap,%20android.view.PixelCopy.OnPixelCopyFinishedListener,%20android.os.Handler))`(`source:` ` [Window](https://developer.android.com/reference/kotlin/android/view/Window)`, `dest:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener)`, `listenerThread:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)`)` Requests a copy of the pixels from a [Window](https://developer.android.com/reference/kotlin/android/view/Window) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](https://developer.android.com/reference/kotlin/android/view/PixelCopy#request(android.view.Window,%20android.graphics.Rect,%20android.graphics.Bitmap,%20android.view.PixelCopy.OnPixelCopyFinishedListener,%20android.os.Handler))`(`source:` ` [Window](https://developer.android.com/reference/kotlin/android/view/Window)`, `srcRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `dest:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`, `listener:` ` [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener)`, `listenerThread:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)`)` Requests a copy of the pixels at the provided [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) from a [Window](https://developer.android.com/reference/kotlin/android/view/Window) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |

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

The source has nothing to copy from. When the source is a [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) this means that no buffers have been queued yet. Wait for the source to produce a frame and try again. 

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
| `request` | [PixelCopy.Request](https://developer.android.com/reference/kotlin/android/view/PixelCopy.Request):The request to execute This value cannot be`null`. |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor to run the callback on This value cannot be`null`. |
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [PixelCopy.Result](https://developer.android.com/reference/kotlin/android/view/PixelCopy.Result)!\>:The callback for when the copy request is completed This value cannot be`null`. |

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

Requests a copy of the pixels from a [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). The contents of the source will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#). The most recently queued buffer in the Surface will be used as the source of the copy.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface):The source from which to copy This value cannot be`null`. |
| `dest` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

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

Requests a copy of the pixels at the provided [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) from a [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). The contents of the source rect will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#). The most recently queued buffer in the Surface will be used as the source of the copy.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface):The source from which to copy This value cannot be`null`. |
| `srcRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:The area of the source to copy from. If this is null the copy area will be the entire surface. The rect will be clamped to the bounds of the Surface. |
| `dest` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

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

Requests for the display content of a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). The contents of the source will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#). The most recently queued buffer in the SurfaceView's Surface will be used as the source of the copy.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView):The source from which to copy This value cannot be`null`. |
| `dest` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

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

Requests for the display content of a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). The contents of the source will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#). The most recently queued buffer in the SurfaceView's Surface will be used as the source of the copy.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView):The source from which to copy This value cannot be`null`. |
| `srcRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:The area of the source to copy from. If this is null the copy area will be the entire surface. The rect will be clamped to the bounds of the Surface. |
| `dest` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

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

Requests a copy of the pixels from a [Window](https://developer.android.com/reference/kotlin/android/view/Window) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). The contents of the source will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#). The most recently queued buffer in the Window's Surface will be used as the source of the copy. Note: This is limited to being able to copy from Window's with a non-null DecorView. If [Window.peekDecorView()](https://developer.android.com/reference/kotlin/android/view/Window#peekDecorView())is null this throws an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#). It will similarly throw an exception if the DecorView has not yet acquired a backing surface. It is recommended that [OnDrawListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnDrawListener) is used to ensure that at least one draw has happened before trying to copy from the window, otherwise either an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) will be thrown or an error will be returned to the [OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Window](https://developer.android.com/reference/kotlin/android/view/Window):The source from which to copy This value cannot be`null`. |
| `dest` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |

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

Requests a copy of the pixels at the provided [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) from a [Window](https://developer.android.com/reference/kotlin/android/view/Window) to be copied into a provided [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). The contents of the source rect will be scaled to fit exactly inside the bitmap. The pixel format of the source buffer will be converted, as part of the copy, to fit the bitmap's [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#). The most recently queued buffer in the Window's Surface will be used as the source of the copy. Note: This is limited to being able to copy from Window's with a non-null DecorView. If [Window.peekDecorView()](https://developer.android.com/reference/kotlin/android/view/Window#peekDecorView())is null this throws an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#). It will similarly throw an exception if the DecorView has not yet acquired a backing surface. It is recommended that [OnDrawListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnDrawListener) is used to ensure that at least one draw has happened before trying to copy from the window, otherwise either an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) will be thrown or an error will be returned to the [OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener).

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Window](https://developer.android.com/reference/kotlin/android/view/Window):The source from which to copy This value cannot be`null`. |
| `srcRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:The area of the source to copy from. If this is null the copy area will be the entire surface. The rect will be clamped to the bounds of the Surface. |
| `dest` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):The destination of the copy. The source will be scaled to match the width, height, and format of this bitmap. This value cannot be`null`. |
| `listener` | [PixelCopy.OnPixelCopyFinishedListener](https://developer.android.com/reference/kotlin/android/view/PixelCopy.OnPixelCopyFinishedListener):Callback for when the pixel copy request completes This value cannot be`null`. |
| `listenerThread` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#):The callback will be invoked on this Handler when the copy is finished. This value cannot be`null`. |
