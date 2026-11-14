# ScrollCaptureSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScrollCaptureSession

Kotlin| [Java](../android/view/ScrollCaptureSession.md) 
| --- | --- |

```
open class ScrollCaptureSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ScrollCaptureSession](../android/view/ScrollCaptureSession.md) |

A session represents the scope of interaction between a [ScrollCaptureCallback](../android/view/ScrollCaptureCallback.md) and the system during an active scroll capture operation.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ScrollCaptureSession](../android/view/ScrollCaptureSession.md))`(`surface:` ` [Surface](../android/view/Surface.md)`, `scrollBounds:` ` [Rect](../android/graphics/Rect.md)`, `positionInWindow:` ` [Point](../android/graphics/Point.md)`)` Constructs a new session instance. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Point](../android/graphics/Point.md) | [getPositionInWindow](../android/view/ScrollCaptureSession.md))`()` Returns the offset of`scroll bounds`within the window. |
| open [Rect](../android/graphics/Rect.md) | [getScrollBounds](../android/view/ScrollCaptureSession.md))`()` Returns the`scroll bounds`, as provided by [ScrollCaptureCallback.onScrollCaptureSearch](../android/view/ScrollCaptureCallback.md)). |
| open [Surface](../android/view/Surface.md) | [getSurface](../android/view/ScrollCaptureSession.md))`()` Returns a [BufferQueue](https://source.android.com/devices/graphics/arch-bq-gralloc) in the form of a [Surface](../android/view/Surface.md) for transfer of image buffers. |
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
| `surface` | [Surface](../android/view/Surface.md):the surface to consume generated images This value cannot be`null`. |
| `scrollBounds` | [Rect](../android/graphics/Rect.md):the bounds of the capture area within the containing view This value cannot be`null`. |
| `positionInWindow` | [Point](../android/graphics/Point.md):the offset of scrollBounds within the window This value cannot be`null`. |
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
| [Point](../android/graphics/Point.md) | the area of scrolling content within the containing view This value cannot be`null`. |

### getScrollBounds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScrollBounds(): Rect
```

Returns the`scroll bounds`, as provided by [ScrollCaptureCallback.onScrollCaptureSearch](../android/view/ScrollCaptureCallback.md)).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Rect](../android/graphics/Rect.md) | the area of scrolling content within the containing view This value cannot be`null`. |

### getSurface

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSurface(): Surface
```

Returns a [BufferQueue](https://source.android.com/devices/graphics/arch-bq-gralloc) in the form of a [Surface](../android/view/Surface.md) for transfer of image buffers.

The surface is guaranteed to remain [valid](../android/view/Surface.md))until the session [ends](../android/view/ScrollCaptureCallback.md)).

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Surface](../android/view/Surface.md) | the surface for transferring image buffers This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|--------------------------------|
| `java.lang.IllegalStateException` | if the session has been closed |
