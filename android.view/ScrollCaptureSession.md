# ScrollCaptureSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScrollCaptureSession

Kotlin| [Java](https://developer.android.com/reference/android/view/ScrollCaptureSession "View this page in Java") 
| --- | --- |

```
open class ScrollCaptureSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ScrollCaptureSession](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureSession#) |

A session represents the scope of interaction between a [ScrollCaptureCallback](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback) and the system during an active scroll capture operation.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ScrollCaptureSession](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureSession#ScrollCaptureSession(android.view.Surface,%20android.graphics.Rect,%20android.graphics.Point))`(`surface:` ` [Surface](https://developer.android.com/reference/kotlin/android/view/Surface)`, `scrollBounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`, `positionInWindow:` ` [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)`)` Constructs a new session instance. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) | [getPositionInWindow](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureSession#getPositionInWindow())`()` Returns the offset of`scroll bounds`within the window. |
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getScrollBounds](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureSession#getScrollBounds())`()` Returns the`scroll bounds`, as provided by [ScrollCaptureCallback.onScrollCaptureSearch](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback#onScrollCaptureSearch(android.os.CancellationSignal,%20java.util.function.Consumer)). |
| open [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) | [getSurface](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureSession#getSurface())`()` Returns a [BufferQueue](https://source.android.com/devices/graphics/arch-bq-gralloc) in the form of a [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) for transfer of image buffers. |
| --- | --- |

## Public constructors

### ScrollCaptureSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScrollCaptureSession(
    surface: Surface, 
    scrollBounds: Rect, 
    positionInWindow: Point)
```

Constructs a new session instance.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface):the surface to consume generated images This value cannot be`null`. |
| `scrollBounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):the bounds of the capture area within the containing view This value cannot be`null`. |
| `positionInWindow` | [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#):the offset of scrollBounds within the window This value cannot be`null`. |
| --- | --- |

## Public methods

### getPositionInWindow

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPositionInWindow(): Point
```

Returns the offset of`scroll bounds`within the window.

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) | the area of scrolling content within the containing view This value cannot be`null`. |

### getScrollBounds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScrollBounds(): Rect
```

Returns the`scroll bounds`, as provided by [ScrollCaptureCallback.onScrollCaptureSearch](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback#onScrollCaptureSearch(android.os.CancellationSignal,%20java.util.function.Consumer)).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | the area of scrolling content within the containing view This value cannot be`null`. |

### getSurface

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSurface(): Surface
```

Returns a [BufferQueue](https://source.android.com/devices/graphics/arch-bq-gralloc) in the form of a [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) for transfer of image buffers.

The surface is guaranteed to remain [valid](https://developer.android.com/reference/kotlin/android/view/Surface#isValid())until the session [ends](https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback#onScrollCaptureEnd(java.lang.Runnable)).

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Surface](https://developer.android.com/reference/kotlin/android/view/Surface) | the surface for transferring image buffers This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|--------------------------------|
| `java.lang.IllegalStateException` | if the session has been closed |
