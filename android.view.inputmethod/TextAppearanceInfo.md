Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextAppearanceInfo

Kotlin | [Java](../android/view/inputmethod/TextAppearanceInfo.md)
| --- | --- |

```
class TextAppearanceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.TextAppearanceInfo](../android/view/inputmethod/TextAppearanceInfo.md) |

Information about text appearance in an editor, passed through `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo` for use by `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo.Builder` Builder for `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getFontFeatureSettings()()` Returns the font feature settings. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getFontVariationSettings()()` Returns the font variation settings. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getHighlightTextColor()()` Returns the color of the text selection highlight. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getHintTextColor()()` Returns the current color of the hint text. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getLetterSpacing()()` Returns the text letter-spacing, which determines the spacing between characters. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getLineBreakStyle()()` Returns the line-break strategies for text wrapping. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getLineBreakWordStyle()()` Returns the line-break word strategies for text wrapping. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getLinkTextColor()()` Returns the text color used to paint the links in the editor. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getShadowColor()()` Returns the color of the text shadow. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getShadowDx()()` Returns the horizontal offset (in pixels) of the text shadow. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getShadowDy()()` Returns the vertical offset (in pixels) of the text shadow. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getShadowRadius()()` Returns the blur radius (in pixels) of the text shadow. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getSystemFontFamilyName()()` Returns the font family name if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` of the text is created from a system font family. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getTextColor()()` Returns the current text color of the editor. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getTextFontWeight()()` Returns the weight of the text, or `FontStyle#FONT_WEIGHT_UNSPECIFIED` when no `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` is specified. |
| [LocaleList](../android/os/LocaleList.md) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getTextLocales()()` Returns the `https://developer.android.com/reference/kotlin/android/os/LocaleList.html#` of the text. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getTextScaleX()()` Returns the extent by which text should be stretched horizontally. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getTextSize()()` Returns the text size (in pixels) for current editor. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#getTextStyle()()` Returns the style (normal, bold, italic, bold|italic) of the text. |
| --- | --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#isAllCaps()()` Returns whether the transformation method applied to the current editor is set to all caps. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#isElegantTextHeight()()` Returns `true` if the elegant height metrics flag is set. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#isFallbackLineSpacing()()` Returns whether to expand linespacing based on fallback fonts. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TextAppearanceInfo](../android/view/inputmethod/TextAppearanceInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getFontFeatureSettings

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFontFeatureSettings(): String?
```

Returns the font feature settings. Returns null if not specified.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontFeatureSettings()`

### getFontVariationSettings

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFontVariationSettings(): String?
```

Returns the font variation settings. Returns null if no variation is specified.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontVariationSettings()`

### getHighlightTextColor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighlightTextColor(): Int
```

Returns the color of the text selection highlight.
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#getHighlightColor()`

### getHintTextColor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHintTextColor(): Int
```

Returns the current color of the hint text.
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#getCurrentHintTextColor()`

### getLetterSpacing

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLetterSpacing(): Float
```

Returns the text letter-spacing, which determines the spacing between characters. The value is in 'EM' units. Normally, this value is 0.0.

### getLineBreakStyle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLineBreakStyle(): Int
```

Returns the line-break strategies for text wrapping.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_STYLE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_STYLE_LOOSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_STYLE_NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_STYLE_STRICT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_STYLE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_STYLE_NO_BREAK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_STYLE_AUTO:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#setLineBreakStyle(kotlin.Int)`

### getLineBreakWordStyle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLineBreakWordStyle(): Int
```

Returns the line-break word strategies for text wrapping.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_WORD_STYLE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_WORD_STYLE_PHRASE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_WORD_STYLE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#LINE_BREAK_WORD_STYLE_AUTO:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#setLineBreakWordStyle(kotlin.Int)`

### getLinkTextColor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLinkTextColor(): Int
```

Returns the text color used to paint the links in the editor.
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#getLinkTextColors()`

### getShadowColor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShadowColor(): Int
```

Returns the color of the text shadow.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`

### getShadowDx

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShadowDx(): Float
```

Returns the horizontal offset (in pixels) of the text shadow. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`

### getShadowDy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShadowDy(): Float
```

Returns the vertical offset (in pixels) of the text shadow. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`

### getShadowRadius

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getShadowRadius(): Float
```

Returns the blur radius (in pixels) of the text shadow. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`

### getSystemFontFamilyName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSystemFontFamilyName(): String?
```

Returns the font family name if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` of the text is created from a system font family. Returns null if no `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` is specified, or it is not created from a system font family.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#getSystemFontFamilyName()`

### getTextColor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextColor(): Int
```

Returns the current text color of the editor.
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#getCurrentTextColor()`

### getTextFontWeight

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextFontWeight(): Int
```

Returns the weight of the text, or `FontStyle#FONT_WEIGHT_UNSPECIFIED` when no `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` is specified.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between `https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle.html#FONT_WEIGHT_UNSPECIFIED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle.html#FONT_WEIGHT_MAX:kotlin.Int` inclusive |

### getTextLocales

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextLocales(): LocaleList
```

Returns the `https://developer.android.com/reference/kotlin/android/os/LocaleList.html#` of the text.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/LocaleList.html#` | This value cannot be `null`. |

### getTextScaleX

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextScaleX(): Float
```

Returns the extent by which text should be stretched horizontally. Returns 1.0 if not specified.

### getTextSize

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextSize(): Float
```

Returns the text size (in pixels) for current editor. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The units of this value are pixels. |

### getTextStyle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextStyle(): Int
```

Returns the style (normal, bold, italic, bold|italic) of the text. Returns `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#NORMAL:kotlin.Int` when no `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` is specified.
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#BOLD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#ITALIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#BOLD_ITALIC:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#`

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isAllCaps

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAllCaps(): Boolean
```

Returns whether the transformation method applied to the current editor is set to all caps.
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#setAllCaps(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#setTransformationMethod(android.text.method.TransformationMethod)`

### isElegantTextHeight

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isElegantTextHeight(): Boolean
```

Returns `true` if the elegant height metrics flag is set. This setting selects font variants that have not been compacted to fit Latin-based vertical metrics, and also increases top and bottom bounds to provide more space.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isElegantTextHeight()`

### isFallbackLineSpacing

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFallbackLineSpacing(): Boolean
```

Returns whether to expand linespacing based on fallback fonts.
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#setFallbackLineSpacing(kotlin.Boolean)`

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TextAppearanceInfo!>
```
