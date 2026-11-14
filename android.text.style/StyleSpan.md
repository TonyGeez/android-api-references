Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StyleSpan

```
open class StyleSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |||
| | ↳ | [android.text.style.MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) ||
| | | ↳ | [android.text.style.StyleSpan](https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#) |

Span that allows setting the style of the text it's attached to. Possible styles are: `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#BOLD:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#ITALIC:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#BOLD_ITALIC:kotlin.Int`.

Note that styles are cumulative -- if both bold and italic are set in separate spans, or if the base style is bold and a span calls for italic, you get bold italic. You can't turn off a style from the base style.

For example, the `StyleSpan` can be used like this:

```kotlin
SpannableString string = new SpannableString("Bold and italic text");
  string.setSpan(new StyleSpan(Typeface.BOLD), 0, 4, Spannable.SPAN_EXCLUSIVE_EXCLUSIVE);
  string.setSpan(new StyleSpan(Typeface.ITALIC), 9, 15, Spannable.SPAN_EXCLUSIVE_EXCLUSIVE);
  
```
Text styled bold and italic with the `StyleSpan`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#StyleSpan(android.os.Parcel)(src: https://developer.android.com/reference/kotlin/android/os/Parcel.html#)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#` from a parcel. |
| `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#StyleSpan(kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#` from a style. |
| `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#StyleSpan(kotlin.Int,%20kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fontWeightAdjustment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#` from a style and font weight adjustment. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#getFontWeightAdjustment()()` Returns the font weight adjustment specified by this span. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#getSpanTypeId()()` Return a special type identifier for this span class. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#getStyle()()` Returns the style constant defined in `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#updateDrawState(android.text.TextPaint)(ds: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#updateMeasureState(android.text.TextPaint)(paint: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)` Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan` |---|---| | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan!` | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying()()` Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)`, returns the underlying MetricAffectingSpan. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint)(tp: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)` <br /> | | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!` | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)(cs: https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!)` A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### StyleSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StyleSpan(src: Parcel)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#` from a parcel.

| Parameters ||
|---|---|
| `src` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): the parcel. This value cannot be `null`. |

### StyleSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StyleSpan(style: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#` from a style.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An integer constant describing the style for this span. Examples include bold, italic, and normal. Values are constants defined in `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#`. |

### StyleSpan

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StyleSpan(
    style: Int, 
    fontWeightAdjustment: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/StyleSpan#` from a style and font weight adjustment.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An integer constant describing the style for this span. Examples include bold, italic, and normal. Values are constants defined in `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#BOLD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#ITALIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#BOLD_ITALIC:kotlin.Int` |
| `fontWeightAdjustment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An integer describing the adjustment to be made to the font weight. This is added to the value of the current weight returned by `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#getWeight()`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#fontWeightAdjustment:kotlin.Int`

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

### getFontWeightAdjustment

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontWeightAdjustment(): Int
```

Returns the font weight adjustment specified by this span.

This can be `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#FONT_WEIGHT_ADJUSTMENT_UNDEFINED:kotlin.Int`. This is added to the value of the current weight returned by `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#getWeight()`.

### getSpanTypeId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSpanTypeId(): Int
```

Return a special type identifier for this span class.

### getStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStyle(): Int
```

Returns the style constant defined in `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#`.

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### updateDrawState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateDrawState(ds: TextPaint!): Unit
```

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateMeasureState(paint: TextPaint): Unit
```

Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters.

| Parameters ||
|---|---|
| `textPaint` | the paint used for drawing the text. This value cannot be `null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
