# ScrollCaptureCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScrollCaptureCallback

Kotlin| [Java](ScrollCaptureCallback.md) 
| --- | --- |

```
interface ScrollCaptureCallback
```

| [android.view.ScrollCaptureCallback](ScrollCaptureCallback.md) |

A ScrollCaptureCallback is responsible for providing rendered snapshots of scrolling content for the scroll capture system. A single callback is responsible for providing support to a single scrolling UI element. At request time, the system will select the best candidate from among all callbacks registered within the window.

A callback is assigned to a View using [View.setScrollCaptureCallback](View.md)), or to the window as [Window.registerScrollCaptureCallback](Window.md)). The point where the callback is registered defines the frame of reference for the bounds measurements used.

**Terminology**

Containing View
: The view on which this callback is attached, or the root view of the window if the callback is assigned directly to a window.

Scroll Bounds
: A rectangle which describes an area within the containing view where scrolling content appears. This may be the entire view or any rectangle within. This defines a frame of reference for requests as well as the width and maximum height of a single request.

Scroll Delta
: The distance the scroll position has moved since capture started. Implementations are responsible for tracking changes in vertical scroll position during capture. This is required to map the capture area to the correct location, given the current scroll position.

Capture Area
: A rectangle which describes the area to capture, relative to scroll bounds. The vertical position remains relative to the starting scroll position and any movement since ("Scroll Delta") should be subtracted to locate the correct local position, and scrolled into view as necessary.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollCaptureEnd](ScrollCaptureCallback.md))`(`onReady:` ` [Runnable](../java.lang/Runnable.md)`)` Signals that capture has ended. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollCaptureImageRequest](ScrollCaptureCallback.md))`(`session:` ` [ScrollCaptureSession](ScrollCaptureSession.md)`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)`, `captureArea:` ` [Rect](../android.graphics/Rect.md)`, `onComplete:` ` [Consumer](../java.util.function/Consumer.md)< [Rect](../android.graphics/Rect.md)!>`)` An image capture has been requested from the scrolling content. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollCaptureSearch](ScrollCaptureCallback.md))`(`signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)`, `onReady:` ` [Consumer](../java.util.function/Consumer.md)< [Rect](../android.graphics/Rect.md)!>`)` The system is searching for the appropriate scrolling container to capture and would like to know the size and position of scrolling content handled by this callback. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScrollCaptureStart](ScrollCaptureCallback.md))`(`session:` ` [ScrollCaptureSession](ScrollCaptureSession.md)`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)`, `onReady:` ` [Runnable](../java.lang/Runnable.md)`)` Scroll Capture has selected this callback to provide the scrolling image content. |

## Public methods

### onScrollCaptureEnd

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollCaptureEnd(onReady: Runnable): Unit
```

Signals that capture has ended. Implementations should release any temporary resources or references to objects in use during the capture. Any resources obtained from the session are now invalid and attempts to use them after this point may throw an exception.

The window should be returned to its original state when capture started. At a minimum, the content should be scrolled to its original position.

[onReady.run](../java.lang/Runnable.md))should be called as soon as possible after the window is ready for normal interactive use. After the callback (or after a timeout, if not called) the screenshot tool will be dismissed and the window may become visible to the user at any time.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onReady` | [Runnable](../java.lang/Runnable.md):a callback to inform the system that the application has completed any cleanup and is ready to become visible This value cannot be`null`. |

### onScrollCaptureImageRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollCaptureImageRequest(
    session: ScrollCaptureSession, 
    signal: CancellationSignal, 
    captureArea: Rect, 
    onComplete: Consumer<Rect!>
): Unit
```

An image capture has been requested from the scrolling content.

The requested rectangle describes an area inside the target view, relative to`scrollBounds`. The content may be offscreen, above or below the current visible portion of the target view. To handle the request, render the available portion of this rectangle to a buffer and return it via the Surface available from [android.view.ScrollCaptureSession#getSurface()](ScrollCaptureSession.md)).

Note: Implementations are only required to render the requested content, and may do so into off-screen buffers without scrolling if they are able.

The resulting available portion of the request must be computed as a portion of`captureArea`, and sent to signal the operation is complete, using [onComplete.accept](../java.util.function/Consumer.md)). If the requested rectangle is partially or fully out of bounds the resulting portion should be returned. If no portion is available (outside of available content), then skip sending any buffer and report an empty Rect as result.

This request may be cancelled via the provided [CancellationSignal](../android.os/CancellationSignal.md). When this happens, any future call to [onComplete.accept](../java.util.function/Consumer.md))will be ignored until the next request.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [ScrollCaptureSession](ScrollCaptureSession.md):the current session, resources provided by it are valid for use until the [session ends](ScrollCaptureCallback.md))This value cannot be`null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md):signal to cancel the operation in progress This value cannot be`null`. |
| `captureArea` | [Rect](../android.graphics/Rect.md):the area to capture, a rectangle within`scrollBounds`This value cannot be`null`. |
| --- | --- |
| `onComplete` | [Consumer](../java.util.function/Consumer.md)\< [Rect](../android.graphics/Rect.md)!\>:a consumer for the captured area This value cannot be`null`. |

### onScrollCaptureSearch

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollCaptureSearch(
    signal: CancellationSignal, 
    onReady: Consumer<Rect!>
): Unit
```

The system is searching for the appropriate scrolling container to capture and would like to know the size and position of scrolling content handled by this callback.

To determine scroll bounds, an implementation should inset the visible bounds of the containing view to cover only the area where scrolling content may be positioned. This should cover only the content which tracks with scrolling movement.

Return the updated rectangle to [onReady.accept](../java.util.function/Consumer.md)). If for any reason the scrolling content is not available to capture, a empty rectangle may be returned which will exclude this view from consideration.

This request may be cancelled via the provided [CancellationSignal](../android.os/CancellationSignal.md). When this happens, any future call to [onReady.accept](../java.util.function/Consumer.md))will have no effect and this content will be omitted from the search results.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md):signal to cancel the operation in progress This value cannot be`null`. |
| `onReady` | [Consumer](../java.util.function/Consumer.md)\< [Rect](../android.graphics/Rect.md)!\>:consumer for the updated rectangle This value cannot be`null`. |

### onScrollCaptureStart

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScrollCaptureStart(
    session: ScrollCaptureSession, 
    signal: CancellationSignal, 
    onReady: Runnable
): Unit
```

Scroll Capture has selected this callback to provide the scrolling image content.

[onReady.run](../java.lang/Runnable.md))should be called when ready to begin handling image requests.

This request may be cancelled via the provided [CancellationSignal](../android.os/CancellationSignal.md). When this happens, any future call to [onReady.run](../java.lang/Runnable.md))will have no effect and provided session will not be activated.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [ScrollCaptureSession](ScrollCaptureSession.md):the current session, resources provided by it are valid for use until the [session ends](ScrollCaptureCallback.md))This value cannot be`null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md):signal to cancel the operation in progress This value cannot be`null`. |
| `onReady` | [Runnable](../java.lang/Runnable.md):signal used to report completion of the request This value cannot be`null`. |
| --- | --- |
