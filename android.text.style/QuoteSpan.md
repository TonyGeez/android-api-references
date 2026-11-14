Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# QuoteSpan

```
open class QuoteSpan : LeadingMarginSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.QuoteSpan](../android/text/style/QuoteSpan.md) |

A span which styles paragraphs by adding a vertical stripe at the beginning of the text (respecting layout direction).

A `QuoteSpan` must be attached from the first character to the last character of a single paragraph, otherwise the span will not be displayed.

`QuoteSpans` allow configuring the following elements:

- **color** - the vertical stripe color. By default, the stripe color is 0xff0000ff
- **gap width** - the distance, in pixels, between the stripe and the paragraph. Default value is 2px.
- **stripe width** - the width, in pixels, of the stripe. Default value is 2px.

For example, a `QuoteSpan` using the default values can be constructed like this:

```kotlin
<code>SpannableString string = new SpannableString("Text with quote span on a long line");
 string.setSpan(new QuoteSpan(), 0, string.length(), Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
`QuoteSpan` constructed with default values.

To construct a `QuoteSpan` with a green stripe, of 20px in width and a gap width of 40px:

```kotlin
<code>SpannableString string = new SpannableString("Text with quote span on a long line");
 string.setSpan(new QuoteSpan(Color.GREEN, 20, 40), 0, string.length(),
 Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
Customized `QuoteSpan`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#STANDARD_COLOR:kotlin.Int` Default color for the quote stripe. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#STANDARD_GAP_WIDTH_PX:kotlin.Int` Default gap width in pixels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#STANDARD_STRIPE_WIDTH_PX:kotlin.Int` Default stripe width in pixels. |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#QuoteSpan()()` Creates a `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#` with the default values. |
| `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#QuoteSpan(android.os.Parcel)(src: https://developer.android.com/reference/kotlin/android/os/Parcel.html#)` Create a `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#` from a parcel. |
| `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#QuoteSpan(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#` based on a color. |
| `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#QuoteSpan(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, stripeWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, gapWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#` based on a color, a stripe width and the width of the gap between the stripe and the text. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#drawLeadingMargin(android.graphics.Canvas,%20android.graphics.Paint,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.text.Layout)(c: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#, p: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dir: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, baseline: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, first: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, layout: https://developer.android.com/reference/kotlin/android/text/Layout.html#)` Renders the leading margin. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#getColor()()` Get the color of the quote stripe. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#getGapWidth()()` Get the width of the gap between the stripe and the text. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#getLeadingMargin(kotlin.Boolean)(first: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the amount by which to adjust the leading margin. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#getSpanTypeId()()` Return a special type identifier for this span class. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#getStripeWidth()()` Get the width of the quote stripe. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

## Constants

### STANDARD_COLOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_COLOR: Int
```

Default color for the quote stripe.

 Value: -16776961

### STANDARD_GAP_WIDTH_PX

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_GAP_WIDTH_PX: Int
```

Default gap width in pixels.

 Value: 2

### STANDARD_STRIPE_WIDTH_PX

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_STRIPE_WIDTH_PX: Int
```

Default stripe width in pixels.

 Value: 2

## Public constructors

### QuoteSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
QuoteSpan()
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#` with the default values.

### QuoteSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
QuoteSpan(src: Parcel)
```

Create a `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#` from a parcel.

| Parameters ||
|---|---|
| `src` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |

### QuoteSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
QuoteSpan(color: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#` based on a color.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the color of the quote stripe. |

### QuoteSpan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
QuoteSpan(
    color: Int, 
    stripeWidth: Int, 
    gapWidth: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan#` based on a color, a stripe width and the width of the gap between the stripe and the text.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the color of the quote stripe. |
| `stripeWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width of the stripe. Value is 0 or greater |
| `gapWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width of the gap between the stripe and the text. Value is 0 or greater |
| --- | --- |

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

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

### getColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColor(): Int
```

Get the color of the quote stripe.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the color of the quote stripe. |

### getGapWidth

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGapWidth(): Int
```

Get the width of the gap between the stripe and the text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the width of the gap between the stripe and the text. |

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

### getSpanTypeId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSpanTypeId(): Int
```

Return a special type identifier for this span class.

### getStripeWidth

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStripeWidth(): Int
```

Get the width of the quote stripe.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the width of the quote stripe. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
