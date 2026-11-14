Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScrollCaptureTarget

Kotlin | [Java](../android/view/ScrollCaptureTarget.md)
| --- | --- |

```
class ScrollCaptureTarget
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ScrollCaptureTarget](../android/view/ScrollCaptureTarget.md) |

A target collects the set of contextual information for a ScrollCaptureHandler discovered during a `https://developer.android.com/reference/kotlin/android/view/View#dispatchScrollCaptureSearch(android.graphics.Rect,%20android.graphics.Point,%20java.util.function.Consumer)`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#ScrollCaptureTarget(android.view.View,%20android.graphics.Rect,%20android.graphics.Point,%20android.view.ScrollCaptureCallback)(scrollTarget: https://developer.android.com/reference/kotlin/android/view/View, localVisibleRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#, positionInWindow: https://developer.android.com/reference/kotlin/android/graphics/Point.html#, callback: https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback)` <br /> |

| Public methods ||
|---|---|
| [ScrollCaptureCallback](../android/view/ScrollCaptureCallback.md) | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#getCallback()()` <br /> |
| [View](../android/view/View.md) | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#getContainingView()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#getHint()()` <br /> |
| --- | --- |
| [Rect](../android/graphics/Rect.md) | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#getLocalVisibleRect()()` Returns the visible bounds of the containing view. |
| [Point](../android/graphics/Point.md) | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#getPositionInWindow()()` <br /> |
| [Rect](../android/graphics/Rect.md)? | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#getScrollBounds()()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#setScrollBounds(android.graphics.Rect)(scrollBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?)` Sets the scroll bounds rect to the intersection of provided rect and the current bounds of the `containing view`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureTarget#updatePositionInWindow()()` Refresh the local visible bounds and its offset within the window, based on the current state of the `containing view`. |
| --- | --- |

## Public constructors

### ScrollCaptureTarget

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ScrollCaptureTarget(
    scrollTarget: View, 
    localVisibleRect: Rect, 
    positionInWindow: Point, 
    callback: ScrollCaptureCallback)
```

| Parameters ||
|---|---|
| `scrollTarget` | [View](../android/view/View.md): This value cannot be `null`. |
| `localVisibleRect` | [Rect](../android/graphics/Rect.md): This value cannot be `null`. |
| `positionInWindow` | [Point](../android/graphics/Point.md): This value cannot be `null`. |
| --- | --- |
| `callback` | [ScrollCaptureCallback](../android/view/ScrollCaptureCallback.md): This value cannot be `null`. |

## Public methods

### getCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallback(): ScrollCaptureCallback
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback` | the `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback` for this target. This value cannot be `null`. |

### getContainingView

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContainingView(): View
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View` | the `containing view` for this `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback` This value cannot be `null`. |

### getHint

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHint(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hint that the `containing view` had during the scroll capture search. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_INCLUDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View#SCROLL_CAPTURE_HINT_EXCLUDE_DESCENDANTS:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View#getScrollCaptureHint()`

### getLocalVisibleRect

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocalVisibleRect(): Rect
```

Returns the visible bounds of the containing view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | the visible bounds of the `containing view` in view-local coordinates. This value cannot be `null`. |

### getPositionInWindow

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPositionInWindow(): Point
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Point.html#` | the position of the visible bounds of the containing view within the window. This value cannot be `null`. |

### getScrollBounds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScrollBounds(): Rect?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?` | the `scroll bounds` for this `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback` This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ScrollCaptureCallback#onScrollCaptureSearch(android.os.CancellationSignal,%20java.util.function.Consumer)`

### setScrollBounds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setScrollBounds(scrollBounds: Rect?): Unit
```

Sets the scroll bounds rect to the intersection of provided rect and the current bounds of the `containing view`.

| Parameters ||
|---|---|
| `scrollBounds` | [Rect](../android/graphics/Rect.md)?: This value may be `null`. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### updatePositionInWindow

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updatePositionInWindow(): Unit
```

Refresh the local visible bounds and its offset within the window, based on the current state of the `containing view`. 
This method must be called on the thread that originally created this UI element. This is typically the [main thread](../android/os/Looper.md)) of your app.
