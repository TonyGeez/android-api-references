# WindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsets

Kotlin| [Java](https://developer.android.com/reference/android/view/WindowInsets "View this page in Java") 
| --- | --- |

```
class WindowInsets
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) |

Describes a set of insets for window content.

WindowInsets are immutable and may be expanded to include more inset types in the future. To adjust insets, use one of the supplied clone methods to obtain a new WindowInsets instance with the adjusted properties.

Note: Before [P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int), WindowInsets instances were only immutable during a single layout pass (i.e. would return the same values between [View.onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets))and [View.onLayout](https://developer.android.com/reference/kotlin/android/view/View#onLayout(kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)), but could return other values otherwise). Starting with [P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int), WindowInsets are always immutable and implement equality.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Builder) Builder for WindowInsets. |
| | [Side](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Side) Class that defines different sides for insets. |
| | [Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) Class that defines different types of sources causing window insets. |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#WindowInsets(android.view.WindowInsets))`(`src:` ` [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#)!`)` Construct a new WindowInsets, copying all values from a source WindowInsets. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | [consumeDisplayCutout](https://developer.android.com/reference/kotlin/android/view/WindowInsets#consumeDisplayCutout())`()` Returns a copy of this WindowInsets with the cutout fully consumed. |
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | [consumeStableInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#consumeStableInsets())`()` Returns a copy of this WindowInsets with the stable insets fully consumed. |
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | [consumeSystemWindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#consumeSystemWindowInsets())`()` Returns a copy of this WindowInsets with the system window insets fully consumed. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/view/WindowInsets#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\> | [getBoundingRects](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getBoundingRects(kotlin.Int))`(`typeMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a list of [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) s, each of which is the bounding rectangle for an area that is being partially or fully obscured inside the window. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\> | [getBoundingRectsIgnoringVisibility](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getBoundingRectsIgnoringVisibility(kotlin.Int))`(`typeMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a list of [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) s, each of which is the bounding rectangle for an area that can be partially or fully obscured inside the window, regardless of whether that type is currently visible or not. |
| --- | --- |
| [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout)? | [getDisplayCutout](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getDisplayCutout())`()` Returns the display cutout if there is one. |
| [DisplayShape](https://developer.android.com/reference/kotlin/android/view/DisplayShape)? | [getDisplayShape](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getDisplayShape())`()` Returns the display shape in the coordinate space of the window. |
| [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#) | [getFrame](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getFrame())`()` Returns the assumed size of the window, relative to which the [getInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))and [getBoundingRects](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getBoundingRects(kotlin.Int))have been calculated. |
| --- | --- |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))`(`typeMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the insets of a specific set of windows causing insets, denoted by the`typeMask`bit mask of [Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s. |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getInsetsIgnoringVisibility](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsetsIgnoringVisibility(kotlin.Int))`(`typeMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the insets a specific set of windows can cause, denoted by the`typeMask`bit mask of [Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s, regardless of whether that type is currently visible or not. |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getMandatorySystemGestureInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getMandatorySystemGestureInsets())`()` Returns the mandatory system gesture insets. |
| --- | --- |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)? | [getPrivacyIndicatorBounds](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getPrivacyIndicatorBounds())`()` Returns the [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) of the maximum bounds of the system privacy indicator, for the current orientation, in relative coordinates, or null if the bounds have not been loaded yet. |
| [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner)? | [getRoundedCorner](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getRoundedCorner(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner) of the given position if there is one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStableInsetBottom](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getStableInsetBottom())`()` Returns the bottom stable inset in pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStableInsetLeft](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getStableInsetLeft())`()` Returns the left stable inset in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStableInsetRight](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getStableInsetRight())`()` Returns the right stable inset in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStableInsetTop](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getStableInsetTop())`()` Returns the top stable inset in pixels. |
| --- | --- |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getStableInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getStableInsets())`()` Returns the stable insets in pixels. |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getSystemGestureInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemGestureInsets())`()` Returns the system gesture insets. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemWindowInsetBottom](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsetBottom())`()` Returns the bottom system window inset in pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemWindowInsetLeft](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsetLeft())`()` Returns the left system window inset in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemWindowInsetRight](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsetRight())`()` Returns the right system window inset in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemWindowInsetTop](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsetTop())`()` Returns the top system window inset in pixels. |
| --- | --- |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getSystemWindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsets())`()` Returns the system window insets in pixels. |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getTappableElementInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getTappableElementInsets())`()` Returns the tappable element insets. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#hasInsets())`()` Returns true if this WindowInsets has any nonzero insets. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#hasStableInsets())`()` Returns true if this WindowInsets has nonzero stable insets. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSystemWindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#hasSystemWindowInsets())`()` Returns true if this WindowInsets has nonzero system window insets. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/view/WindowInsets#hashCode())`()` <br /> |
| --- | --- |
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | [inset](https://developer.android.com/reference/kotlin/android/view/WindowInsets#inset(android.graphics.Insets))`(`insets:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#)`)` Returns a copy of this instance inset in the given directions. |
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | [inset](https://developer.android.com/reference/kotlin/android/view/WindowInsets#inset(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this instance inset in the given directions. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConsumed](https://developer.android.com/reference/kotlin/android/view/WindowInsets#isConsumed())`()` Check if these insets have been fully consumed. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRound](https://developer.android.com/reference/kotlin/android/view/WindowInsets#isRound())`()` Returns true if the associated window has a round shape. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/view/WindowInsets#isVisible(kotlin.Int))`(`typeMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns whether a set of windows that may cause insets is currently visible on screen, regardless of whether it actually overlaps with this window. |
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | [replaceSystemWindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#replaceSystemWindowInsets(android.graphics.Rect))`(`systemWindowInsets:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` Returns a copy of this WindowInsets with selected system window insets replaced with new values. |
| --- | --- |
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | [replaceSystemWindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#replaceSystemWindowInsets(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this WindowInsets with selected system window insets replaced with new values. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/WindowInsets#toString())`()` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | [CONSUMED](https://developer.android.com/reference/kotlin/android/view/WindowInsets#CONSUMED:android.view.WindowInsets) A [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) instance for which [isConsumed()](https://developer.android.com/reference/kotlin/android/view/WindowInsets#isConsumed())returns`true`. |

## Public constructors

### WindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WindowInsets(src: WindowInsets!)
```

Construct a new WindowInsets, copying all values from a source WindowInsets.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `src` | [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#)!:Source to copy insets from |

## Public methods

### consumeDisplayCutout

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun consumeDisplayCutout(): WindowInsets
```

**Deprecated:** *Consuming of different parts individually of a [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) instance is deprecated, since [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) contains many different insets. Use [CONSUMED](https://developer.android.com/reference/kotlin/android/view/WindowInsets#CONSUMED:android.view.WindowInsets) instead to stop dispatching insets.*

Returns a copy of this WindowInsets with the cutout fully consumed.

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | A modified copy of this WindowInsets This value cannot be`null`. |

### consumeStableInsets

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun consumeStableInsets(): WindowInsets
```

**Deprecated:** *Consuming of different parts individually of a [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) instance is deprecated, since [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) contains many different insets. Use [CONSUMED](https://developer.android.com/reference/kotlin/android/view/WindowInsets#CONSUMED:android.view.WindowInsets) instead to stop dispatching insets. On [R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), this method has no effect.*

Returns a copy of this WindowInsets with the stable insets fully consumed.

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | A modified copy of this WindowInsets This value cannot be`null`. |

### consumeSystemWindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun consumeSystemWindowInsets(): WindowInsets
```

**Deprecated:** *Consuming of different parts individually of a [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) instance is deprecated, since [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) contains many different insets. Use [CONSUMED](https://developer.android.com/reference/kotlin/android/view/WindowInsets#CONSUMED:android.view.WindowInsets) instead to stop dispatching insets.*

Returns a copy of this WindowInsets with the system window insets fully consumed.

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | A modified copy of this WindowInsets This value cannot be`null`. |

### equals

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getBoundingRects

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRects(typeMask: Int): MutableList<Rect!>
```

Returns a list of [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) s, each of which is the bounding rectangle for an area that is being partially or fully obscured inside the window.

May be used with or instead of [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) for finer avoidance of regions that may be partially obscuring the window but may be smaller than those provided by [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int)).

The [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) s returned are always cropped to the bounds of the window frame and their coordinate values are relative to the [getFrame()](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getFrame()), regardless of the window's position on screen.

If inset by [inset(android.graphics.Insets)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#inset(android.graphics.Insets)), bounding rects that intersect with the provided insets will be resized to only include the intersection with the remaining frame. Bounding rects may be completely removed if they no longer intersect with the new instance.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the insets type for which to obtain the bounding rectangles Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!> | the bounding rectangles This value cannot be`null`. |

### getBoundingRectsIgnoringVisibility

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRectsIgnoringVisibility(typeMask: Int): MutableList<Rect!>
```

Returns a list of [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) s, each of which is the bounding rectangle for an area that can be partially or fully obscured inside the window, regardless of whether that type is currently visible or not.

The bounding rects represent areas of a window that**may** be partially or fully obscured by the`type`. This value does not change based on the visibility state of those elements. For example, if the status bar is normally shown, but temporarily hidden, the bounding rects returned here will provide the rects associated with the status bar being shown.

May be used with or instead of [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) for finer avoidance of regions that may be partially obscuring the window but may be smaller than those provided by [getInsetsIgnoringVisibility(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsetsIgnoringVisibility(kotlin.Int)).

The [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) s returned are always cropped to the bounds of the window frame and their coordinate values are relative to the [getFrame()](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getFrame()), regardless of the window's position on screen.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the insets type for which to obtain the bounding rectangles Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!> | the bounding rectangles This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the caller tries to query [Type.ime()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#ime()). Bounding rects are not available if the IME isn't visible as the height of the IME is dynamic depending on the [EditorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo) of the currently focused view, as well as the UI state of the IME. |

### getDisplayCutout

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayCutout(): DisplayCutout?
```

Returns the display cutout if there is one.

Note: the display cutout will already be [consumed](https://developer.android.com/reference/kotlin/android/view/WindowInsets#consumeDisplayCutout())during dispatch to [View.onApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets)), unless the window has requested a [WindowManager.LayoutParams.layoutInDisplayCutoutMode](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#layoutInDisplayCutoutMode:kotlin.Int) other than [never](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#LAYOUT_IN_DISPLAY_CUTOUT_MODE_NEVER:kotlin.Int) or [default](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams#LAYOUT_IN_DISPLAY_CUTOUT_MODE_DEFAULT:kotlin.Int).

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------|
| [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout)? | the display cutout or null if there is none |

**See Also**

- [android.view.DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout) 

### getDisplayShape

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayShape(): DisplayShape?
```

Returns the display shape in the coordinate space of the window.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------|
| [DisplayShape](https://developer.android.com/reference/kotlin/android/view/DisplayShape)? | the display shape This value may be`null`. |

**See Also**

- [android.view.DisplayShape](https://developer.android.com/reference/kotlin/android/view/DisplayShape) 

### getFrame

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrame(): Size
```

Returns the assumed size of the window, relative to which the [getInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))and [getBoundingRects](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getBoundingRects(kotlin.Int))have been calculated.

May be used with [getBoundingRects](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getBoundingRects(kotlin.Int))to better understand their position within the window, such as the area between the edge of a bounding rect and the edge of the window.

Note: the size may not match the actual size of the window, which is determined during the layout pass - as [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) are dispatched before layout.

Caution: using this value in determining the actual window size may make the result of layout passes unstable and should be avoided.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#) | the assumed size of the window during the inset calculation This value cannot be`null`. |

### getInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInsets(typeMask: Int): Insets
```

Returns the insets of a specific set of windows causing insets, denoted by the`typeMask`bit mask of [Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Bit mask of [Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s to query the insets for. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | The insets. This value cannot be`null`. |

### getInsetsIgnoringVisibility

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInsetsIgnoringVisibility(typeMask: Int): Insets
```

Returns the insets a specific set of windows can cause, denoted by the`typeMask`bit mask of [Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s, regardless of whether that type is currently visible or not.

The insets represents the area of a a window that that**may** be partially or fully obscured by the system window identified by`type`. This value does not change based on the visibility state of those elements. For example, if the status bar is normally shown, but temporarily hidden, the inset returned here will still provide the inset associated with the status bar being shown.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Bit mask of [Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s to query the insets for. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | The insets. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the caller tries to query [Type.ime()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#ime()). Insets are not available if the IME isn't visible as the height of the IME is dynamic depending on the [EditorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo) of the currently focused view, as well as the UI state of the IME. |

### getMandatorySystemGestureInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMandatorySystemGestureInsets(): Insets
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.mandatorySystemGestures()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#mandatorySystemGestures())instead.*

Returns the mandatory system gesture insets.

The mandatory system gesture insets represent the area of a window where mandatory system gestures have priority and may consume some or all touch input, e.g. due to the a system bar occupying it, or it being reserved for touch-only gestures.

In contrast to [regular system gestures](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemGestureInsets()),**mandatory** system gestures cannot be overridden by [View.setSystemGestureExclusionRects](https://developer.android.com/reference/kotlin/android/view/View#setSystemGestureExclusionRects(kotlin.collections.MutableList)).

Simple taps are guaranteed to reach the window even within the system gesture insets, as long as they are outside the [system window insets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getTappableElementInsets()).

When [View.SYSTEM_UI_FLAG_LAYOUT_STABLE](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int) is requested, an inset will be returned even when the system gestures are inactive due to [View.SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int) or [View.SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int).

This inset is consumed together with the [system window insets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsets())by [consumeSystemWindowInsets()](https://developer.android.com/reference/kotlin/android/view/WindowInsets#consumeSystemWindowInsets()).

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | This value cannot be`null`. |

**See Also**

- [#getSystemGestureInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemGestureInsets()) 

### getPrivacyIndicatorBounds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrivacyIndicatorBounds(): Rect?
```

Returns the [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) of the maximum bounds of the system privacy indicator, for the current orientation, in relative coordinates, or null if the bounds have not been loaded yet.

The privacy indicator bounds are determined by SystemUI, and subsequently loaded once the StatusBar window has been created and attached. The bounds for all rotations are calculated and loaded at once, and this value is only expected to ever change on display or font scale changes. As long as there is a StatusBar window, this value should not be expected to be null.

The privacy indicator shows over apps when an app uses the microphone or camera permissions, while an app is in immersive mode.

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)? | A rectangle representing the maximum bounds of the indicator |

### getRoundedCorner

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoundedCorner(position: Int): RoundedCorner?
```

Returns the [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner) of the given position if there is one.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the rounded corner on the display. The value should be one of the following: [RoundedCorner.POSITION_TOP_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_LEFT:kotlin.Int), [RoundedCorner.POSITION_TOP_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_RIGHT:kotlin.Int), [RoundedCorner.POSITION_BOTTOM_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_RIGHT:kotlin.Int), [RoundedCorner.POSITION_BOTTOM_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_LEFT:kotlin.Int). Value is [android.view.RoundedCorner#POSITION_TOP_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_LEFT:kotlin.Int), [android.view.RoundedCorner#POSITION_TOP_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_RIGHT:kotlin.Int), [android.view.RoundedCorner#POSITION_BOTTOM_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_RIGHT:kotlin.Int), or [android.view.RoundedCorner#POSITION_BOTTOM_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_LEFT:kotlin.Int) |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner)? | the rounded corner of the given position. Returns`null`if there is none or the rounded corner area is not inside the application's bounds. |

### getStableInsetBottom

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStableInsetBottom(): Int
```

**Deprecated:** *Use [getInsetsIgnoringVisibility(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsetsIgnoringVisibility(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the bottom stable inset in pixels.

The stable inset represents the area of a full-screen window that**may**be partially or fully obscured by the system UI elements. This value does not change based on the visibility state of those elements; for example, if the status bar is normally shown, but temporarily hidden, the stable inset will still provide the inset associated with the status bar being shown.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bottom stable inset |

### getStableInsetLeft

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStableInsetLeft(): Int
```

**Deprecated:** *Use [getInsetsIgnoringVisibility(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsetsIgnoringVisibility(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the left stable inset in pixels.

The stable inset represents the area of a full-screen window that**may**be partially or fully obscured by the system UI elements. This value does not change based on the visibility state of those elements; for example, if the status bar is normally shown, but temporarily hidden, the stable inset will still provide the inset associated with the status bar being shown.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The left stable inset |

### getStableInsetRight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStableInsetRight(): Int
```

**Deprecated:** *Use [getInsetsIgnoringVisibility(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsetsIgnoringVisibility(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the right stable inset in pixels.

The stable inset represents the area of a full-screen window that**may**be partially or fully obscured by the system UI elements. This value does not change based on the visibility state of those elements; for example, if the status bar is normally shown, but temporarily hidden, the stable inset will still provide the inset associated with the status bar being shown.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The right stable inset |

### getStableInsetTop

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStableInsetTop(): Int
```

**Deprecated:** *Use [getInsetsIgnoringVisibility(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsetsIgnoringVisibility(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the top stable inset in pixels.

The stable inset represents the area of a full-screen window that**may**be partially or fully obscured by the system UI elements. This value does not change based on the visibility state of those elements; for example, if the status bar is normally shown, but temporarily hidden, the stable inset will still provide the inset associated with the status bar being shown.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The top stable inset |

### getStableInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStableInsets(): Insets
```

**Deprecated:** *Use [getInsetsIgnoringVisibility(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsetsIgnoringVisibility(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the stable insets in pixels.

The stable inset represents the area of a full-screen window that**may**be partially or fully obscured by the system UI elements. This value does not change based on the visibility state of those elements; for example, if the status bar is normally shown, but temporarily hidden, the stable inset will still provide the inset associated with the status bar being shown.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | The stable insets This value cannot be`null`. |

### getSystemGestureInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemGestureInsets(): Insets
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.systemGestures()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemGestures())instead.*

Returns the system gesture insets.

The system gesture insets represent the area of a window where system gestures have priority and may consume some or all touch input, e.g. due to the a system bar occupying it, or it being reserved for touch-only gestures.

An app can declare priority over system gestures with [View.setSystemGestureExclusionRects](https://developer.android.com/reference/kotlin/android/view/View#setSystemGestureExclusionRects(kotlin.collections.MutableList))outside of the [mandatory system gesture insets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getMandatorySystemGestureInsets()).

Note: the system will put a limit of`200dp`on the vertical extent of the exclusions it takes into account. The limit does not apply while the navigation bar is [stickily](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_IMMERSIVE_STICKY:kotlin.Int) hidden, nor to the [input method](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#) and [home activity](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_HOME:kotlin.String).

Simple taps are guaranteed to reach the window even within the system gesture insets, as long as they are outside the [system window insets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getTappableElementInsets()).

When [View.SYSTEM_UI_FLAG_LAYOUT_STABLE](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int) is requested, an inset will be returned even when the system gestures are inactive due to [View.SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int) or [View.SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int).

This inset is consumed together with the [system window insets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsets())by [consumeSystemWindowInsets()](https://developer.android.com/reference/kotlin/android/view/WindowInsets#consumeSystemWindowInsets()).

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | This value cannot be`null`. |

**See Also**

- [#getMandatorySystemGestureInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getMandatorySystemGestureInsets()) 

### getSystemWindowInsetBottom

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemWindowInsetBottom(): Int
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the bottom system window inset in pixels.

The system window inset represents the area of a full-screen window that is partially or fully obscured by the status bar, navigation bar, IME or other system windows.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bottom system window inset |

### getSystemWindowInsetLeft

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemWindowInsetLeft(): Int
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the left system window inset in pixels.

The system window inset represents the area of a full-screen window that is partially or fully obscured by the status bar, navigation bar, IME or other system windows.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The left system window inset |

### getSystemWindowInsetRight

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemWindowInsetRight(): Int
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the right system window inset in pixels.

The system window inset represents the area of a full-screen window that is partially or fully obscured by the status bar, navigation bar, IME or other system windows.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The right system window inset |

### getSystemWindowInsetTop

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemWindowInsetTop(): Int
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns the top system window inset in pixels.

The system window inset represents the area of a full-screen window that is partially or fully obscured by the status bar, navigation bar, IME or other system windows.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The top system window inset |

### getSystemWindowInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemWindowInsets(): Insets
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())*

Returns the system window insets in pixels.

The system window inset represents the area of a full-screen window that is partially or fully obscured by the status bar, navigation bar, IME or other system windows.

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | The system window insets This value cannot be`null`. |

### getTappableElementInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTappableElementInsets(): Insets
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.tappableElement()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#tappableElement())instead.*

Returns the tappable element insets.

The tappable element insets represent how much tappable elements**must at least**be inset to remain both tappable and visually unobstructed by persistent system windows.

This may be smaller than [getSystemWindowInsets()](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsets())if the system window is largely transparent and lets through simple taps (but not necessarily more complex gestures).

Note that generally, tappable elements**should** be aligned with the [system window insets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsets())instead to avoid overlapping with the system bars.

When [View.SYSTEM_UI_FLAG_LAYOUT_STABLE](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_STABLE:kotlin.Int) is requested, an inset will be returned even when the area covered by the inset would be tappable due to [View.SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN:kotlin.Int) or [View.SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LAYOUT_HIDE_NAVIGATION:kotlin.Int).

This inset is consumed together with the [system window insets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getSystemWindowInsets())by [consumeSystemWindowInsets()](https://developer.android.com/reference/kotlin/android/view/WindowInsets#consumeSystemWindowInsets()).

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | This value cannot be`null`. |

### hasInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasInsets(): Boolean
```

Returns true if this WindowInsets has any nonzero insets.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any inset values are nonzero |

### hasStableInsets

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasStableInsets(): Boolean
```

**Deprecated:** *Use [getInsetsIgnoringVisibility(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsetsIgnoringVisibility(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns true if this WindowInsets has nonzero stable insets.

The stable inset represents the area of a full-screen window that**may**be partially or fully obscured by the system UI elements. This value does not change based on the visibility state of those elements; for example, if the status bar is normally shown, but temporarily hidden, the stable inset will still provide the inset associated with the status bar being shown.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any of the stable inset values are nonzero |

### hasSystemWindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSystemWindowInsets(): Boolean
```

**Deprecated:** *Use [getInsets(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getInsets(kotlin.Int))with [Type.systemBars()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#systemBars())instead.*

Returns true if this WindowInsets has nonzero system window insets.

The system window inset represents the area of a full-screen window that is partially or fully obscured by the status bar, navigation bar, IME or other system windows.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any of the system window inset values are nonzero |

### hashCode

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### inset

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun inset(insets: Insets): WindowInsets
```

Returns a copy of this instance inset in the given directions.

This is intended for dispatching insets to areas of the window that are smaller than the current area.

Example: 

```kotlin
childView.dispatchApplyWindowInsets(insets.inset(childMargins));
  
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `insets` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#):the amount of insets to remove from all sides. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | This value cannot be`null`. |

**See Also**

- [#inset(int, int, int, int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#inset(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### inset

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun inset(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): WindowInsets
```

Returns a copy of this instance inset in the given directions.

This is intended for dispatching insets to areas of the window that are smaller than the current area.

Example: 

```kotlin
childView.dispatchApplyWindowInsets(insets.inset(
          childMarginLeft, childMarginTop, childMarginBottom, childMarginRight));
  
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of insets to remove from the left. Must be non-negative. Value is 0 or greater |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of insets to remove from the top. Must be non-negative. Value is 0 or greater |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of insets to remove from the right. Must be non-negative. Value is 0 or greater |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of insets to remove from the bottom. Must be non-negative. Value is 0 or greater |

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | the inset insets This value cannot be`null`. |

**See Also**

- [#inset(Insets)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#inset(android.graphics.Insets)) 

### isConsumed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConsumed(): Boolean
```

Check if these insets have been fully consumed.

Insets are considered "consumed" if the applicable`consume*`methods have been called such that all insets have been set to zero. This affects propagation of insets through the view hierarchy; insets that have not been fully consumed will continue to propagate down to child views.

The result of this method is equivalent to the return value of [View.fitSystemWindows(android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/view/View#fitSystemWindows(android.graphics.Rect)).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the insets have been fully consumed. |

### isRound

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRound(): Boolean
```

Returns true if the associated window has a round shape.

A round window's left, top, right and bottom edges reach all the way to the associated edges of the window but the corners may not be visible. Views responding to round insets should take care to not lay out critical elements within the corners where they may not be accessible.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the window is round |

### isVisible

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVisible(typeMask: Int): Boolean
```

Returns whether a set of windows that may cause insets is currently visible on screen, regardless of whether it actually overlaps with this window.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Bit mask of [Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s to query visibility status. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if all windows included in`typeMask`are currently visible on screen. |

### replaceSystemWindowInsets

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replaceSystemWindowInsets(systemWindowInsets: Rect!): WindowInsets
```

**Deprecated:** *use`Builder#Builder(WindowInsets)`with [Builder.setSystemWindowInsets(Insets)](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Builder#setSystemWindowInsets(android.graphics.Insets))instead.*

Returns a copy of this WindowInsets with selected system window insets replaced with new values.

Note: If the system window insets are already consumed, this method will return them unchanged on [Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) and later. Prior to [Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int), the new values were applied regardless of whether they were consumed, and this method returns invalid non-zero consumed insets.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `systemWindowInsets` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:New system window insets. Each field is the inset in pixels for that edge |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | A modified copy of this WindowInsets This value cannot be`null`. |

### replaceSystemWindowInsets

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replaceSystemWindowInsets(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): WindowInsets
```

**Deprecated:** *use`Builder#Builder(WindowInsets)`with [Builder.setSystemWindowInsets(Insets)](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Builder#setSystemWindowInsets(android.graphics.Insets))instead.*

Returns a copy of this WindowInsets with selected system window insets replaced with new values.

Note: If the system window insets are already consumed, this method will return them unchanged on [Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) and later. Prior to [Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int), the new values were applied regardless of whether they were consumed, and this method returns invalid non-zero consumed insets.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):New left inset in pixels |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):New top inset in pixels |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):New right inset in pixels |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):New bottom inset in pixels |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) | A modified copy of this WindowInsets This value cannot be`null`. |

### toString

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### CONSUMED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONSUMED: WindowInsets
```

A [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets#) instance for which [isConsumed()](https://developer.android.com/reference/kotlin/android/view/WindowInsets#isConsumed())returns`true`.

This can be used during insets dispatch in the view hierarchy by returning this value from [View.onApplyWindowInsets(WindowInsets)](https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets))or [OnApplyWindowInsetsListener.onApplyWindowInsets(View, WindowInsets)](https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener#onApplyWindowInsets(android.view.View,%20android.view.WindowInsets))to stop dispatch the insets to its children to avoid traversing the entire view hierarchy.

The application should return this instance once it has taken care of all insets on a certain level in the view hierarchy, and doesn't need to dispatch to its children anymore for better performance. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/view/WindowInsets#isConsumed()>
