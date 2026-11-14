Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BulletSpan

```
open class BulletSpan : LeadingMarginSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.BulletSpan](BulletSpan.md) |

A span which styles paragraphs as bullet points (respecting layout direction).

BulletSpans must be attached from the first character to the last character of a single paragraph, otherwise the bullet point will not be displayed but the first paragraph encountered will have a leading margin.

BulletSpans allow configuring the following elements:

- **gap width** - the distance, in pixels, between the bullet point and the paragraph. Default value is 2px.
- **color** - the bullet point color. By default, the bullet point color is 0 - no color, so it uses the TextView's text color.
- **bullet radius** - the radius, in pixels, of the bullet point. Default value is 4px.

For example, a BulletSpan using the default values can be constructed like this:

```kotlin
<code>SpannableString string = new SpannableString("Text with\nBullet point");
 string.setSpan(new BulletSpan(), 10, 22, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
BulletSpan constructed with default values.

To construct a BulletSpan with a gap width of 40px, green bullet point and bullet radius of 20px:

```kotlin
<code>SpannableString string = new SpannableString("Text with\nBullet point");
 string.setSpan(new BulletSpan(40, color, 20), 10, 22, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
Customized BulletSpan.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#STANDARD_GAP_WIDTH:kotlin.Int` <br /> |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#BulletSpan()()` Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` with the default values. |
| `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#BulletSpan(android.os.Parcel)(src: https://developer.android.com/reference/kotlin/android/os/Parcel.html#)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` from a parcel. |
| `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#BulletSpan(kotlin.Int)(gapWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` based on a gap width |
| `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#BulletSpan(kotlin.Int,%20kotlin.Int)(gapWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` based on a gap width and a color integer. |
| `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#BulletSpan(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(gapWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bulletRadius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` based on a gap width and a color integer. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#drawLeadingMargin(android.graphics.Canvas,%20android.graphics.Paint,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.text.Layout)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#, paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dir: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, baseline: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, first: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, layout: https://developer.android.com/reference/kotlin/android/text/Layout.html#?)` Renders the leading margin. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#getBulletRadius()()` Get the radius, in pixels, of the bullet point. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#getColor()()` Get the bullet point color. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#getGapWidth()()` Get the distance, in pixels, between the bullet point and the paragraph. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#getLeadingMargin(kotlin.Boolean)(first: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the amount by which to adjust the leading margin. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#getSpanTypeId()()` Return a special type identifier for this span class. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

## Constants

### STANDARD_GAP_WIDTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_GAP_WIDTH: Int
```

 Value: 2

## Public constructors

### BulletSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BulletSpan()
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` with the default values.

### BulletSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BulletSpan(src: Parcel)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` from a parcel.

| Parameters ||
|---|---|
| `src` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |

### BulletSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BulletSpan(gapWidth: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` based on a gap width

| Parameters ||
|---|---|
| `gapWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the distance, in pixels, between the bullet point and the paragraph. |

### BulletSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BulletSpan(
    gapWidth: Int, 
    color: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` based on a gap width and a color integer.

| Parameters ||
|---|---|
| `gapWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the distance, in pixels, between the bullet point and the paragraph. |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bullet point color, as a color integer |

**See Also**

### BulletSpan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BulletSpan(
    gapWidth: Int, 
    color: Int, 
    bulletRadius: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/BulletSpan#` based on a gap width and a color integer.

| Parameters ||
|---|---|
| `gapWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the distance, in pixels, between the bullet point and the paragraph. |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bullet point color, as a color integer. |
| `bulletRadius` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radius of the bullet point, in pixels. Value is 0 or greater |
| --- | --- |

**See Also**

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
    canvas: Canvas, 
    paint: Paint, 
    x: Int, 
    dir: Int, 
    top: Int, 
    baseline: Int, 
    bottom: Int, 
    text: CharSequence, 
    start: Int, 
    end: Int, 
    first: Boolean, 
    layout: Layout?
): Unit
```

Renders the leading margin. This is called before the margin has been adjusted by the value returned by `https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan#getLeadingMargin(kotlin.Boolean)`.

| Parameters ||
|---|---|
| `c` | the canvas |
| `p` | the paint. The this should be left unchanged on exit. |
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
| `layout` | [Layout](../android.text/Layout.md)?: This value may be `null`. |
| --- | --- |
| `canvas` | [Canvas](../android.graphics/Canvas.md): This value cannot be `null`. |
| `paint` | [Paint](../android.graphics/Paint.md): This value cannot be `null`. |

### getBulletRadius

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBulletRadius(): Int
```

Get the radius, in pixels, of the bullet point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the radius, in pixels, of the bullet point. |

### getColor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColor(): Int
```

Get the bullet point color.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the bullet point color |

### getGapWidth

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGapWidth(): Int
```

Get the distance, in pixels, between the bullet point and the paragraph.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the distance, in pixels, between the bullet point and the paragraph. |

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
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
