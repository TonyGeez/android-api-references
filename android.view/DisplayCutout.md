# DisplayCutout

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayCutout

Kotlin| [Java](DisplayCutout.md) 
| --- | --- |

```
class DisplayCutout
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.DisplayCutout](DisplayCutout.md) |

Represents the area of the display that is not functional for displaying content.

`DisplayCutout`is immutable.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/DisplayCutout.Builder.md) A Builder class to construct a DisplayCutout instance. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DisplayCutout](DisplayCutout.md))`(`safeInsets:` ` [Insets](../android.graphics/Insets.md)`, `boundLeft:` ` [Rect](../android.graphics/Rect.md)?`, `boundTop:` ` [Rect](../android.graphics/Rect.md)?`, `boundRight:` ` [Rect](../android.graphics/Rect.md)?`, `boundBottom:` ` [Rect](../android.graphics/Rect.md)?`)` Creates a DisplayCutout instance. |
| [DisplayCutout](DisplayCutout.md))`(`safeInsets:` ` [Insets](../android.graphics/Insets.md)`, `boundLeft:` ` [Rect](../android.graphics/Rect.md)?`, `boundTop:` ` [Rect](../android.graphics/Rect.md)?`, `boundRight:` ` [Rect](../android.graphics/Rect.md)?`, `boundBottom:` ` [Rect](../android.graphics/Rect.md)?`, `waterfallInsets:` ` [Insets](../android.graphics/Insets.md)`)` Creates a DisplayCutout instance. |
| [DisplayCutout](DisplayCutout.md))`(`safeInsets:` ` [Rect](../android.graphics/Rect.md)?`, `boundingRects:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Rect](../android.graphics/Rect.md)!>?`)` Creates a DisplayCutout instance. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](DisplayCutout.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Rect](../android.graphics/Rect.md) | [getBoundingRectBottom](DisplayCutout.md))`()` Returns a bounding rectangle for a non-functional area on the display which is located on the bottom of the screen. |
| [Rect](../android.graphics/Rect.md) | [getBoundingRectLeft](DisplayCutout.md))`()` Returns a bounding rectangle for a non-functional area on the display which is located on the left of the screen. |
| --- | --- |
| [Rect](../android.graphics/Rect.md) | [getBoundingRectRight](DisplayCutout.md))`()` Returns a bounding rectangle for a non-functional area on the display which is located on the right of the screen. |
| [Rect](../android.graphics/Rect.md) | [getBoundingRectTop](DisplayCutout.md))`()` Returns a bounding rectangle for a non-functional area on the display which is located on the top of the screen. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android.graphics/Rect.md)!\> | [getBoundingRects](DisplayCutout.md))`()` Returns a list of`Rect`s, each of which is the bounding rectangle for a non-functional area on the display. |
| --- | --- |
| [Path](../android.graphics/Path.md)? | [getCutoutPath](DisplayCutout.md))`()` Returns a [Path](../android.graphics/Path.md) that contains the cutout paths of all sides on the display. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSafeInsetBottom](DisplayCutout.md))`()` Returns the inset from the bottom which avoids the display cutout in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSafeInsetLeft](DisplayCutout.md))`()` Returns the inset from the left which avoids the display cutout in pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSafeInsetRight](DisplayCutout.md))`()` Returns the inset from the right which avoids the display cutout in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSafeInsetTop](DisplayCutout.md))`()` Returns the inset from the top which avoids the display cutout in pixels. |
| [Insets](../android.graphics/Insets.md) | [getWaterfallInsets](DisplayCutout.md))`()` Returns the insets representing the curved areas of a waterfall display. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](DisplayCutout.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](DisplayCutout.md))`()` <br /> |

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

Note that this is only useful for tests. For production code, developers should always use a [DisplayCutout](DisplayCutout.md) obtained from the system.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `safeInsets` | [Insets](../android.graphics/Insets.md):the insets from each edge which avoid the display cutout as returned by [getSafeInsetTop()](DisplayCutout.md))etc. This value cannot be`null`. |
| `boundLeft` | [Rect](../android.graphics/Rect.md)?:the left bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `boundTop` | [Rect](../android.graphics/Rect.md)?:the top bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| --- | --- |
| `boundRight` | [Rect](../android.graphics/Rect.md)?:the right bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `boundBottom` | [Rect](../android.graphics/Rect.md)?:the bottom bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |

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

Note that this is only useful for tests. For production code, developers should always use a [DisplayCutout](DisplayCutout.md) obtained from the system.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `safeInsets` | [Insets](../android.graphics/Insets.md):the insets from each edge which avoid the display cutout as returned by [getSafeInsetTop()](DisplayCutout.md))etc. This value cannot be`null`. |
| `boundLeft` | [Rect](../android.graphics/Rect.md)?:the left bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `boundTop` | [Rect](../android.graphics/Rect.md)?:the top bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| --- | --- |
| `boundRight` | [Rect](../android.graphics/Rect.md)?:the right bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `boundBottom` | [Rect](../android.graphics/Rect.md)?:the bottom bounding rect of the display cutout in pixels. If null is passed, it's treated as an empty rectangle (0,0)-(0,0). |
| `waterfallInsets` | [Insets](../android.graphics/Insets.md):the insets for the curved areas in waterfall display. This value cannot be`null`. |
| --- | --- |

### DisplayCutout

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DisplayCutout(
    safeInsets: Rect?, 
    boundingRects: MutableList<Rect!>?)
```

**Deprecated:** *Use [DisplayCutout.DisplayCutout(Insets, Rect, Rect, Rect, Rect)](DisplayCutout.md))instead.*

Creates a DisplayCutout instance.

Note that this is only useful for tests. For production code, developers should always use a [DisplayCutout](DisplayCutout.md) obtained from the system.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `safeInsets` | [Rect](../android.graphics/Rect.md)?:the insets from each edge which avoid the display cutout as returned by [getSafeInsetTop()](DisplayCutout.md))etc. This value may be`null`. |
| `boundingRects` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Rect](../android.graphics/Rect.md)!\>?:the bounding rects of the display cutouts as returned by [getBoundingRects()](DisplayCutout.md))()}. This value may be`null`. |

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
| [Rect](../android.graphics/Rect.md) | bounding rectangle in pixels. In case of no bounding rectangle, an empty rectangle is returned. This value cannot be`null`. |

### getBoundingRectLeft

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRectLeft(): Rect
```

Returns a bounding rectangle for a non-functional area on the display which is located on the left of the screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Rect](../android.graphics/Rect.md) | bounding rectangle in pixels. In case of no bounding rectangle, an empty rectangle is returned. This value cannot be`null`. |

### getBoundingRectRight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRectRight(): Rect
```

Returns a bounding rectangle for a non-functional area on the display which is located on the right of the screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Rect](../android.graphics/Rect.md) | bounding rectangle in pixels. In case of no bounding rectangle, an empty rectangle is returned. This value cannot be`null`. |

### getBoundingRectTop

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRectTop(): Rect
```

Returns a bounding rectangle for a non-functional area on the display which is located on the top of the screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Rect](../android.graphics/Rect.md) | bounding rectangle in pixels. In case of no bounding rectangle, an empty rectangle is returned. This value cannot be`null`. |

### getBoundingRects

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoundingRects(): MutableList<Rect!>
```

Returns a list of`Rect`s, each of which is the bounding rectangle for a non-functional area on the display. There will be at most one non-functional area per edge of the device.

Note that there is no bounding rectangle for waterfall cutout since it just represents the curved areas of the display but not the non-functional areas.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Rect](../android.graphics/Rect.md)!> | a list of bounding`Rect`s, one for each display cutout area. No empty Rect is returned. This value cannot be`null`. |

### getCutoutPath

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCutoutPath(): Path?
```

Returns a [Path](../android.graphics/Path.md) that contains the cutout paths of all sides on the display. To get a cutout path for one specific side, apps can intersect the [Path](../android.graphics/Path.md) with the [Rect](../android.graphics/Rect.md) obtained from [getBoundingRectLeft()](DisplayCutout.md)), [getBoundingRectTop()](DisplayCutout.md)), [getBoundingRectRight()](DisplayCutout.md))or [getBoundingRectBottom()](DisplayCutout.md)).

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Path](../android.graphics/Path.md)? | a [Path](../android.graphics/Path.md) contains all the cutout paths based on display coordinate. Returns null if there is no cutout on the display. |

### getSafeInsetBottom

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSafeInsetBottom(): Int
```

Returns the inset from the bottom which avoids the display cutout in pixels. 
**See Also**

- [android.view.WindowInsets.Type#displayCutout()](../android/view/WindowInsets.Type.md)) 

### getSafeInsetLeft

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSafeInsetLeft(): Int
```

Returns the inset from the left which avoids the display cutout in pixels. 
**See Also**

- [android.view.WindowInsets.Type#displayCutout()](../android/view/WindowInsets.Type.md)) 

### getSafeInsetRight

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSafeInsetRight(): Int
```

Returns the inset from the right which avoids the display cutout in pixels. 
**See Also**

- [android.view.WindowInsets.Type#displayCutout()](../android/view/WindowInsets.Type.md)) 

### getSafeInsetTop

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSafeInsetTop(): Int
```

Returns the inset from the top which avoids the display cutout in pixels. 
**See Also**

- [android.view.WindowInsets.Type#displayCutout()](../android/view/WindowInsets.Type.md)) 

### getWaterfallInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWaterfallInsets(): Insets
```

Returns the insets representing the curved areas of a waterfall display. A waterfall display has curved areas along the edges of the screen. Apps should be careful when showing UI and handling touch input in those insets because the curve may impair legibility and can frequently lead to unintended touch inputs.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Insets](../android.graphics/Insets.md) | the insets for the curved areas of a waterfall display in pixels or`Insets.NONE`if there are no curved areas or they don't overlap with the window. This value cannot be`null`. |

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
