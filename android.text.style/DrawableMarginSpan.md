Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrawableMarginSpan

Kotlin | [Java](../android/text/style/DrawableMarginSpan.md)
| --- | --- |

```
open class DrawableMarginSpan : LeadingMarginSpan, LineHeightSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.DrawableMarginSpan](../android/text/style/DrawableMarginSpan.md) |

A span which adds a drawable and a padding to the paragraph it's attached to.

If the height of the drawable is bigger than the height of the line it's attached to then the line height is increased to fit the drawable. `DrawableMarginSpan` allows setting a padding between the drawable and the text. The default value is 0. The span must be set from the beginning of the text, otherwise either the span won't be rendered or it will be rendered incorrectly.

For example, a drawable and a padding of 20px can be added like this:

```kotlin
<code>SpannableString string = new SpannableString("Text with a drawable.");
  string.setSpan(new DrawableMarginSpan(drawable, 20), 0, string.length(),
  Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
Text with a drawable and a padding.

<br />

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#DrawableMarginSpan(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#` from a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`. |
| `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#DrawableMarginSpan(android.graphics.drawable.Drawable,%20kotlin.Int)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#, pad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#` from a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` and a padding, in pixels. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#chooseHeight(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint.FontMetricsInt)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, istartv: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fm: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#)` Classes that implement this should define how the height is being calculated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#drawLeadingMargin(android.graphics.Canvas,%20android.graphics.Paint,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.text.Layout)(c: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#, p: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dir: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, baseline: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, first: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, layout: https://developer.android.com/reference/kotlin/android/text/Layout.html#)` Renders the leading margin. |
| open [Drawable](../android/graphics/drawable/Drawable.md) | `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#getDrawable()()` Returns the drawable used. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#getLeadingMargin(kotlin.Boolean)(first: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the amount by which to adjust the leading margin. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#getPadding()()` Returns a distance between the drawable and text in pixel. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#toString()()` Returns a string representation of the object. |
| --- | --- |

## Public constructors

### DrawableMarginSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DrawableMarginSpan(drawable: Drawable)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#` from a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`. The pad width will be 0.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android/graphics/drawable/Drawable.md): the drawable to be added. This value cannot be `null`. |

### DrawableMarginSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DrawableMarginSpan(
    drawable: Drawable, 
    pad: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan#` from a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` and a padding, in pixels.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android/graphics/drawable/Drawable.md): the drawable to be added. This value cannot be `null`. |
| `pad` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the distance between the drawable and the text |

## Public methods

### chooseHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun chooseHeight(
    text: CharSequence, 
    start: Int, 
    end: Int, 
    istartv: Int, 
    v: Int, 
    fm: Paint.FontMetricsInt
): Unit
```

Classes that implement this should define how the height is being calculated.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the line |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end of the line |
| --- | --- |
| `spanstartv` | the start of the span |
| `lineHeight` | the line height |
| `fm` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md): This value cannot be `null`. |
| --- | --- |

### drawLeadingMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun drawLeadingMargin(
    c: Canvas, 
    p: Paint, 
    x: Int, 
    dir: Int, 
    top: Int, 
    baseline: Int, 
    bottom: Int, 
    text: CharSequence, 
    start: Int, 
    end: Int, 
    first: Boolean, 
    layout: Layout
): Unit
```

Renders the leading margin. This is called before the margin has been adjusted by the value returned by `https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan#getLeadingMargin(kotlin.Boolean)`.

| Parameters ||
|---|---|
| `c` | [Canvas](../android/graphics/Canvas.md): This value cannot be `null`. |
| `p` | [Paint](../android/graphics/Paint.md): This value cannot be `null`. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the current position of the margin |
| --- | --- |
| `dir` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the base direction of the paragraph; if negative, the margin is to the right of the text, otherwise it is to the left. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the top of the line |
| `baseline` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the baseline of the line |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bottom of the line |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the line |
| --- | --- |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end of the line |
| `first` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if this is the first line of its paragraph |
| `layout` | [Layout](../android/text/Layout.md): This value cannot be `null`. |
| --- | --- |

### getDrawable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(): Drawable
```

Returns the drawable used.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | a drawable. This value cannot be `null`. |

### getLeadingMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLeadingMargin(first: Boolean): Int
```

Returns the amount by which to adjust the leading margin. Positive values move away from the leading edge of the paragraph, negative values move towards it.

| Parameters ||
|---|---|
| `first` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the request is for the first line of a paragraph, false for subsequent lines |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset for the margin. |

### getPadding

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPadding(): Int
```

Returns a distance between the drawable and text in pixel. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a distance pixel from the text. The units of this value are pixels. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
