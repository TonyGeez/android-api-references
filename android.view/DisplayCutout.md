# DisplayCutout

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayCutout

Kotlin| [Java](https://developer.android.com/reference/android/view/DisplayCutout "View this page in Java") 
| --- | --- |

```
class DisplayCutout
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#) |

Represents the area of the display that is not functional for displaying content.

`DisplayCutout`is immutable.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/DisplayCutout.Builder) A Builder class to construct a DisplayCutout instance. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#DisplayCutout(android.graphics.Insets,%20android.graphics.Rect,%20android.graphics.Rect,%20android.graphics.Rect,%20android.graphics.Rect))`(`safeInsets:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#)`, `boundLeft:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `boundTop:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `boundRight:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `boundBottom:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`)` Creates a DisplayCutout instance. |
| [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#DisplayCutout(android.graphics.Insets,%20android.graphics.Rect,%20android.graphics.Rect,%20android.graphics.Rect,%20android.graphics.Rect,%20android.graphics.Insets))`(`safeInsets:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#)`, `boundLeft:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `boundTop:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `boundRight:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `boundBottom:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `waterfallInsets:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#)`)` Creates a DisplayCutout instance. |
| [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#DisplayCutout(android.graphics.Rect,%20kotlin.collections.MutableList))`(`safeInsets:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?`, `boundingRects:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!>?`)` Creates a DisplayCutout instance. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBoundingRectBottom](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRectBottom())`()` Returns a bounding rectangle for a non-functional area on the display which is located on the bottom of the screen. |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBoundingRectLeft](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRectLeft())`()` Returns a bounding rectangle for a non-functional area on the display which is located on the left of the screen. |
| --- | --- |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBoundingRectRight](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRectRight())`()` Returns a bounding rectangle for a non-functional area on the display which is located on the right of the screen. |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBoundingRectTop](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRectTop())`()` Returns a bounding rectangle for a non-functional area on the display which is located on the top of the screen. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\> | [getBoundingRects](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRects())`()` Returns a list of`Rect`s, each of which is the bounding rectangle for a non-functional area on the display. |
| --- | --- |
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)? | [getCutoutPath](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getCutoutPath())`()` Returns a [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#) that contains the cutout paths of all sides on the display. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSafeInsetBottom](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getSafeInsetBottom())`()` Returns the inset from the bottom which avoids the display cutout in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSafeInsetLeft](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getSafeInsetLeft())`()` Returns the inset from the left which avoids the display cutout in pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSafeInsetRight](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getSafeInsetRight())`()` Returns the inset from the right which avoids the display cutout in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSafeInsetTop](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getSafeInsetTop())`()` Returns the inset from the top which avoids the display cutout in pixels. |
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getWaterfallInsets](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getWaterfallInsets())`()` Returns the insets representing the curved areas of a waterfall display. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#toString())`()` <br /> |

## Public constructors

### DisplayCutout

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DisplayCutout(
    safeInsets: Insets, 
    boundLeft: Rect?, 
    boundTop: Rect?, 
    boundRight: Rect?, 
    boundBottom: Rect?)
```

Creates a DisplayCutout instance.

Note that this is only useful for tests. For production code, developers should always use a [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#) obtained from the system.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `safeInsets` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#):the insets from each edge which avoid the display cutout as returned by [getSafeInsetTop()](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getSafeInsetTop())etc. This value cannot be`null`. |
| `boundLeft` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the left bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `boundTop` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the top bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| --- | --- |
| `boundRight` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the right bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `boundBottom` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the bottom bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |

### DisplayCutout

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DisplayCutout(
    safeInsets: Insets, 
    boundLeft: Rect?, 
    boundTop: Rect?, 
    boundRight: Rect?, 
    boundBottom: Rect?, 
    waterfallInsets: Insets)
```

Creates a DisplayCutout instance.

Note that this is only useful for tests. For production code, developers should always use a [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#) obtained from the system.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `safeInsets` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#):the insets from each edge which avoid the display cutout as returned by [getSafeInsetTop()](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getSafeInsetTop())etc. This value cannot be`null`. |
| `boundLeft` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the left bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `boundTop` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the top bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| --- | --- |
| `boundRight` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the right bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `boundBottom` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the bottom bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `waterfallInsets` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#):the insets for the curved areas in waterfall display. This value cannot be`null`. |
| --- | --- |

### DisplayCutout

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DisplayCutout(
    safeInsets: Rect?, 
    boundingRects: MutableList<Rect!>?)
```

**Deprecated:** *Use [DisplayCutout.DisplayCutout(Insets, Rect, Rect, Rect, Rect)](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#DisplayCutout(android.graphics.Insets,%20android.graphics.Rect,%20android.graphics.Rect,%20android.graphics.Rect,%20android.graphics.Rect))instead.*

Creates a DisplayCutout instance.

Note that this is only useful for tests. For production code, developers should always use a [DisplayCutout](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#) obtained from the system.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `safeInsets` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?:the insets from each edge which avoid the display cutout as returned by [getSafeInsetTop()](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getSafeInsetTop())etc. This value may be`null`. |
| `boundingRects` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\>?:the bounding rects of the display cutouts as returned by [getBoundingRects()](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRects())()}. This value may be`null`. |

## Public methods

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getBoundingRectBottom

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRectBottom(): Rect
```

Returns a bounding rectangle for a non-functional area on the display which is located on the bottom of the screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | bounding rectangle in pixels. In case of no bounding rectangle, an empty rectangle is returned. This value cannot be`null`. |

### getBoundingRectLeft

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRectLeft(): Rect
```

Returns a bounding rectangle for a non-functional area on the display which is located on the left of the screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | bounding rectangle in pixels. In case of no bounding rectangle, an empty rectangle is returned. This value cannot be`null`. |

### getBoundingRectRight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRectRight(): Rect
```

Returns a bounding rectangle for a non-functional area on the display which is located on the right of the screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | bounding rectangle in pixels. In case of no bounding rectangle, an empty rectangle is returned. This value cannot be`null`. |

### getBoundingRectTop

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRectTop(): Rect
```

Returns a bounding rectangle for a non-functional area on the display which is located on the top of the screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | bounding rectangle in pixels. In case of no bounding rectangle, an empty rectangle is returned. This value cannot be`null`. |

### getBoundingRects

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRects(): MutableList<Rect!>
```

Returns a list of`Rect`s, each of which is the bounding rectangle for a non-functional area on the display. There will be at most one non-functional area per edge of the device.

Note that there is no bounding rectangle for waterfall cutout since it just represents the curved areas of the display but not the non-functional areas.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!> | a list of bounding`Rect`s, one for each display cutout area. No empty Rect is returned. This value cannot be`null`. |

### getCutoutPath

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCutoutPath(): Path?
```

Returns a [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#) that contains the cutout paths of all sides on the display. To get a cutout path for one specific side, apps can intersect the [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#) with the [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) obtained from [getBoundingRectLeft()](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRectLeft()), [getBoundingRectTop()](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRectTop()), [getBoundingRectRight()](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRectRight())or [getBoundingRectBottom()](https://developer.android.com/reference/kotlin/android/view/DisplayCutout#getBoundingRectBottom()).

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)? | a [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#) contains all the cutout paths based on display coordinate. Returns null if there is no cutout on the display. |

### getSafeInsetBottom

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSafeInsetBottom(): Int
```

Returns the inset from the bottom which avoids the display cutout in pixels. 
**See Also**

- [android.view.WindowInsets.Type#displayCutout()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#displayCutout()) 

### getSafeInsetLeft

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSafeInsetLeft(): Int
```

Returns the inset from the left which avoids the display cutout in pixels. 
**See Also**

- [android.view.WindowInsets.Type#displayCutout()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#displayCutout()) 

### getSafeInsetRight

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSafeInsetRight(): Int
```

Returns the inset from the right which avoids the display cutout in pixels. 
**See Also**

- [android.view.WindowInsets.Type#displayCutout()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#displayCutout()) 

### getSafeInsetTop

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSafeInsetTop(): Int
```

Returns the inset from the top which avoids the display cutout in pixels. 
**See Also**

- [android.view.WindowInsets.Type#displayCutout()](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type#displayCutout()) 

### getWaterfallInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWaterfallInsets(): Insets
```

Returns the insets representing the curved areas of a waterfall display. A waterfall display has curved areas along the edges of the screen. Apps should be careful when showing UI and handling touch input in those insets because the curve may impair legibility and can frequently lead to unintended touch inputs.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | the insets for the curved areas of a waterfall display in pixels or`Insets.NONE`if there are no curved areas or they don't overlap with the window. This value cannot be`null`. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
