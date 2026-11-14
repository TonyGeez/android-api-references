Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewTreeObserver

```
class ViewTreeObserver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ViewTreeObserver](ViewTreeObserver.md) |

A view tree observer is used to register listeners that can be notified of global changes in the view tree. Such global events include, but are not limited to, layout of the whole tree, beginning of the drawing pass, touch mode change.... A ViewTreeObserver should never be instantiated by applications as it is provided by the views hierarchy. Refer to getViewTreeObserver for more information.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnDrawListener` Interface definition for a callback to be invoked when the view tree is about to be drawn. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnGlobalFocusChangeListener` Interface definition for a callback to be invoked when the focus state within the view tree changes. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnGlobalLayoutListener` Interface definition for a callback to be invoked when the global layout state or the visibility of views within the view tree changes. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnPreDrawListener` Interface definition for a callback to be invoked when the view tree is about to be drawn. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnScrollChangedListener` Interface definition for a callback to be invoked when something in the view tree has been scrolled. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnTouchModeChangeListener` Interface definition for a callback to be invoked when the touch mode changes. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowAttachListener` Interface definition for a callback to be invoked when the view hierarchy is attached to and detached from its window. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowFocusChangeListener` Interface definition for a callback to be invoked when the view hierarchy's window focus state changes. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowVisibilityChangeListener` Interface definition for a callback to be invoked when the view hierarchy's window visibility changes. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.WindowInsetsAnimationListener` Interface definition for a callback to be invoked when window insets animations prepare or end. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnDrawListener Register a callback to be invoked when the view tree is about to be drawn. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnGlobalFocusChangeListener <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnGlobalLayoutListener Register a callback to be invoked when the global layout state or the visibility of views within the view tree changes |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnPreDrawListener Register a callback to be invoked when the view tree is about to be drawn |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnScrollChangedListener Register a callback to be invoked when a view has been scrolled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnSystemGestureExclusionRectsChangedListener Add a listener to be notified when the tree's *transformed* gesture exclusion rects change. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnTouchModeChangeListener Register a callback to be invoked when the invoked when the touch mode changes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnWindowAttachListener Register a callback to be invoked when the view hierarchy is attached to a window. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnWindowFocusChangeListener Register a callback to be invoked when the window focus state within the view tree changes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnWindowVisibilityChangeListener Register a callback to be invoked when the window visibility changes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addWindowInsetsAnimationListener Register a callback to be invoked when window insets animations start or end. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchOnDraw Notifies registered listeners that the drawing pass is about to start. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchOnGlobalLayout Notifies registered listeners that a global layout happened. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | dispatchOnPreDraw Notifies registered listeners that the drawing pass is about to start. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchOnScrollChanged Notifies registered listeners that something has scrolled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAlive Indicates whether this ViewTreeObserver is alive. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerFrameCommitCallback Adds a frame commit callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeGlobalOnLayoutListener Remove a previously installed global layout callback |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnDrawListener Remove a previously installed pre-draw callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnGlobalFocusChangeListener Remove a previously installed focus change callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnGlobalLayoutListener Remove a previously installed global layout callback |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnPreDrawListener Remove a previously installed pre-draw callback |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnScrollChangedListener Remove a previously installed scroll-changed callback |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnSystemGestureExclusionRectsChangedListener Unsubscribe the given listener from gesture exclusion rect changes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnTouchModeChangeListener Remove a previously installed touch mode change callback |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnWindowAttachListener Remove a previously installed window attach callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnWindowFocusChangeListener Remove a previously installed window focus change callback. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnWindowVisibilityChangeListener Remove a previously installed window visibility callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeWindowInsetsAnimationListener Remove a previously installed window insets animation callback. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | unregisterFrameCommitCallback Attempts to remove the given callback from the list of pending frame complete callbacks. |
| --- | --- |

## Public methods

### addOnDrawListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnDrawListener(listener: ViewTreeObserver.OnDrawListener!): Unit
```

Register a callback to be invoked when the view tree is about to be drawn.

**Note:** this method **cannot** be invoked from onDraw.

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.OnDrawListener](../android/view/ViewTreeObserver.OnDrawListener.md)!: The callback to add |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### addOnGlobalFocusChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnGlobalFocusChangeListener(listener: ViewTreeObserver.OnGlobalFocusChangeListener!): Unit
```

### addOnGlobalLayoutListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnGlobalLayoutListener(listener: ViewTreeObserver.OnGlobalLayoutListener!): Unit
```

Register a callback to be invoked when the global layout state or the visibility of views within the view tree changes

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.OnGlobalLayoutListener](../android/view/ViewTreeObserver.OnGlobalLayoutListener.md)!: The callback to add |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### addOnPreDrawListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnPreDrawListener(listener: ViewTreeObserver.OnPreDrawListener!): Unit
```

Register a callback to be invoked when the view tree is about to be drawn

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.OnPreDrawListener](../android/view/ViewTreeObserver.OnPreDrawListener.md)!: The callback to add |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### addOnScrollChangedListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnScrollChangedListener(listener: ViewTreeObserver.OnScrollChangedListener!): Unit
```

Register a callback to be invoked when a view has been scrolled.

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.OnScrollChangedListener](../android/view/ViewTreeObserver.OnScrollChangedListener.md)!: The callback to add |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### addOnSystemGestureExclusionRectsChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnSystemGestureExclusionRectsChangedListener(listener: Consumer<MutableList<Rect!>!>): Unit
```

Add a listener to be notified when the tree's *transformed* gesture exclusion rects change. This could be the result of an animation or other layout change, or a view calling setSystemGestureExclusionRects.

| Parameters ||
|---|---|
| `listener` | [Consumer](../java.util.function/Consumer.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android.graphics/Rect.md)!\>!\>: listener to add. This value cannot be `null`. |

**See Also**

- setSystemGestureExclusionRects

### addOnTouchModeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnTouchModeChangeListener(listener: ViewTreeObserver.OnTouchModeChangeListener!): Unit
```

Register a callback to be invoked when the invoked when the touch mode changes.

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.OnTouchModeChangeListener](../android/view/ViewTreeObserver.OnTouchModeChangeListener.md)!: The callback to add |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### addOnWindowAttachListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnWindowAttachListener(listener: ViewTreeObserver.OnWindowAttachListener!): Unit
```

Register a callback to be invoked when the view hierarchy is attached to a window.

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.OnWindowAttachListener](../android/view/ViewTreeObserver.OnWindowAttachListener.md)!: The callback to add |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### addOnWindowFocusChangeListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnWindowFocusChangeListener(listener: ViewTreeObserver.OnWindowFocusChangeListener!): Unit
```

Register a callback to be invoked when the window focus state within the view tree changes.

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.OnWindowFocusChangeListener](../android/view/ViewTreeObserver.OnWindowFocusChangeListener.md)!: The callback to add |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### addOnWindowVisibilityChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnWindowVisibilityChangeListener(listener: ViewTreeObserver.OnWindowVisibilityChangeListener): Unit
```

Register a callback to be invoked when the window visibility changes.

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.OnWindowVisibilityChangeListener](../android/view/ViewTreeObserver.OnWindowVisibilityChangeListener.md): The callback to add. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### addWindowInsetsAnimationListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addWindowInsetsAnimationListener(listener: ViewTreeObserver.WindowInsetsAnimationListener): Unit
```

Register a callback to be invoked when window insets animations start or end.

| Parameters ||
|---|---|
| `listener` | [ViewTreeObserver.WindowInsetsAnimationListener](../android/view/ViewTreeObserver.WindowInsetsAnimationListener.md): The callback to add. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### dispatchOnDraw

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchOnDraw(): Unit
```

Notifies registered listeners that the drawing pass is about to start.

### dispatchOnGlobalLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchOnGlobalLayout(): Unit
```

Notifies registered listeners that a global layout happened. This can be called manually if you are forcing a layout on a View or a hierarchy of Views that are not attached to a Window or in the GONE state.

### dispatchOnPreDraw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchOnPreDraw(): Boolean
```

Notifies registered listeners that the drawing pass is about to start. If a listener returns true, then the drawing pass is canceled and rescheduled. This can be called manually if you are forcing the drawing on a View or a hierarchy of Views that are not attached to a Window or in the GONE state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the current draw should be canceled and rescheduled, false otherwise. |

### dispatchOnScrollChanged

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dispatchOnScrollChanged(): Unit
```

Notifies registered listeners that something has scrolled.

### isAlive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAlive(): Boolean
```

Indicates whether this ViewTreeObserver is alive. When an observer is not alive, any call to a method (except this one) will throw an exception. If an application keeps a long-lived reference to this ViewTreeObserver, it should always check for the result of this method before calling any other method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this object is alive and be used, false otherwise. |

### registerFrameCommitCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerFrameCommitCallback(callback: Runnable): Unit
```

Adds a frame commit callback. This callback will be invoked when the current rendering content has been rendered into a frame and submitted to the swap chain. The frame may not currently be visible on the display when this is invoked, but it has been submitted. This callback is useful in combination with PixelCopy to capture the current rendered content of the UI reliably. Note: Only works with hardware rendering. Does nothing otherwise.

| Parameters ||
|---|---|
| `callback` | [Runnable](../java.lang/Runnable.md): The callback to invoke when the frame is committed. This value cannot be `null`. |

### removeGlobalOnLayoutListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeGlobalOnLayoutListener(victim: ViewTreeObserver.OnGlobalLayoutListener!): Unit
```

**Deprecated:** *Use #removeOnGlobalLayoutListener instead*

Remove a previously installed global layout callback

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnGlobalLayoutListener](../android/view/ViewTreeObserver.OnGlobalLayoutListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnGlobalLayoutListener

### removeOnDrawListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnDrawListener(victim: ViewTreeObserver.OnDrawListener!): Unit
```

Remove a previously installed pre-draw callback.

**Note:** this method **cannot** be invoked from onDraw.

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnDrawListener](../android/view/ViewTreeObserver.OnDrawListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnDrawListener

### removeOnGlobalFocusChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnGlobalFocusChangeListener(victim: ViewTreeObserver.OnGlobalFocusChangeListener!): Unit
```

Remove a previously installed focus change callback.

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnGlobalFocusChangeListener](../android/view/ViewTreeObserver.OnGlobalFocusChangeListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnGlobalFocusChangeListener

### removeOnGlobalLayoutListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnGlobalLayoutListener(victim: ViewTreeObserver.OnGlobalLayoutListener!): Unit
```

Remove a previously installed global layout callback

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnGlobalLayoutListener](../android/view/ViewTreeObserver.OnGlobalLayoutListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnGlobalLayoutListener

### removeOnPreDrawListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnPreDrawListener(victim: ViewTreeObserver.OnPreDrawListener!): Unit
```

Remove a previously installed pre-draw callback

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnPreDrawListener](../android/view/ViewTreeObserver.OnPreDrawListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnPreDrawListener

### removeOnScrollChangedListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnScrollChangedListener(victim: ViewTreeObserver.OnScrollChangedListener!): Unit
```

Remove a previously installed scroll-changed callback

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnScrollChangedListener](../android/view/ViewTreeObserver.OnScrollChangedListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnScrollChangedListener

### removeOnSystemGestureExclusionRectsChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnSystemGestureExclusionRectsChangedListener(listener: Consumer<MutableList<Rect!>!>): Unit
```

Unsubscribe the given listener from gesture exclusion rect changes.

| Parameters ||
|---|---|
| `listener` | [Consumer](../java.util.function/Consumer.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android.graphics/Rect.md)!\>!\>: This value cannot be `null`. |

**See Also**

- addOnSystemGestureExclusionRectsChangedListener
- setSystemGestureExclusionRects

### removeOnTouchModeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnTouchModeChangeListener(victim: ViewTreeObserver.OnTouchModeChangeListener!): Unit
```

Remove a previously installed touch mode change callback

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnTouchModeChangeListener](../android/view/ViewTreeObserver.OnTouchModeChangeListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnTouchModeChangeListener

### removeOnWindowAttachListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnWindowAttachListener(victim: ViewTreeObserver.OnWindowAttachListener!): Unit
```

Remove a previously installed window attach callback.

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnWindowAttachListener](../android/view/ViewTreeObserver.OnWindowAttachListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnWindowAttachListener

### removeOnWindowFocusChangeListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnWindowFocusChangeListener(victim: ViewTreeObserver.OnWindowFocusChangeListener!): Unit
```

Remove a previously installed window focus change callback.

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnWindowFocusChangeListener](../android/view/ViewTreeObserver.OnWindowFocusChangeListener.md)!: The callback to remove |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnWindowFocusChangeListener

### removeOnWindowVisibilityChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnWindowVisibilityChangeListener(victim: ViewTreeObserver.OnWindowVisibilityChangeListener): Unit
```

Remove a previously installed window visibility callback.

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.OnWindowVisibilityChangeListener](../android/view/ViewTreeObserver.OnWindowVisibilityChangeListener.md): The callback to remove. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

**See Also**

- addOnWindowVisibilityChangeListener

### removeWindowInsetsAnimationListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeWindowInsetsAnimationListener(victim: ViewTreeObserver.WindowInsetsAnimationListener): Unit
```

Remove a previously installed window insets animation callback.

| Parameters ||
|---|---|
| `victim` | [ViewTreeObserver.WindowInsetsAnimationListener](../android/view/ViewTreeObserver.WindowInsetsAnimationListener.md): The callback to remove. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If isAlive returns false |

### unregisterFrameCommitCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterFrameCommitCallback(callback: Runnable): Boolean
```

Attempts to remove the given callback from the list of pending frame complete callbacks.

| Parameters ||
|---|---|
| `callback` | [Runnable](../java.lang/Runnable.md): The callback to remove. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether or not the callback was removed. If this returns true the callback will not be invoked. If false is returned then the callback was either never added or may already be pending execution and was unable to be removed |
