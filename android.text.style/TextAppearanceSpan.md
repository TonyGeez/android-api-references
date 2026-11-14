# TextAppearanceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextAppearanceSpan

Kotlin| [Java](TextAppearanceSpan.md) 
| --- | --- |

```
open class TextAppearanceSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](CharacterStyle.md) |||
| | ↳ | [android.text.style.MetricAffectingSpan](MetricAffectingSpan.md) ||
| | | ↳ | [android.text.style.TextAppearanceSpan](TextAppearanceSpan.md) |
| --- | --- | --- | --- |

Sets the text appearance using the given [TextAppearance](../android/R.styleable.md) attributes. By default [TextAppearanceSpan](TextAppearanceSpan.md) only changes the specified attributes in XML. [textColorHighlight](../android/R.styleable.md), [textColorHint](../android/R.styleable.md), [textAllCaps](../android/R.styleable.md) and [fallbackLineSpacing](../android/R.styleable.md) are not supported by [TextAppearanceSpan](TextAppearanceSpan.md). {@see android.widget.TextView#setTextAppearance(int)}

## Summary

| XML attributes ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [`android:elegantTextHeight`](TextAppearanceSpan.md) | Elegant text height, especially for less compacted complex script text. |
| [`android:fontFamily`](TextAppearanceSpan.md) | Font family (named by string or as a font resource reference) for the text. |
| [`android:fontFeatureSettings`](TextAppearanceSpan.md) | Font feature settings. |
| --- | --- |
| [`android:fontVariationSettings`](TextAppearanceSpan.md) | Font variation settings. |
| [`android:letterSpacing`](TextAppearanceSpan.md) | Text letter-spacing. |
| [`android:shadowColor`](TextAppearanceSpan.md) | Place a blurred shadow of text underneath the text, drawn with the specified color. |
| --- | --- |
| [`android:shadowDx`](TextAppearanceSpan.md) | Horizontal offset of the text shadow. |
| [`android:shadowDy`](TextAppearanceSpan.md) | Vertical offset of the text shadow. |
| [`android:shadowRadius`](TextAppearanceSpan.md) | Blur radius of the text shadow. |
| --- | --- |
| [`android:textColor`](TextAppearanceSpan.md) | Text color. |
| [`android:textColorLink`](TextAppearanceSpan.md) | Color of the links. |
| [`android:textFontWeight`](TextAppearanceSpan.md) | Weight for the font used in the TextView. |
| --- | --- |
| [`android:textSize`](TextAppearanceSpan.md) | Size of the text. |
| [`android:textStyle`](TextAppearanceSpan.md) | Style (normal, bold, italic, bold|italic) for the text. |
| [`android:typeface`](TextAppearanceSpan.md) | Typeface (normal, sans, serif, monospace) for the text. |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextAppearanceSpan](TextAppearanceSpan.md))`(`context:` ` [Context](../android.content/Context.md)!`, `appearance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Uses the specified TextAppearance resource to determine the text appearance. |
| [TextAppearanceSpan](TextAppearanceSpan.md))`(`context:` ` [Context](../android.content/Context.md)!`, `appearance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colorList:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Uses the specified TextAppearance resource to determine the text appearance, and the specified text color resource to determine the color. |
| [TextAppearanceSpan](TextAppearanceSpan.md))`(`src:` ` [Parcel](../android.os/Parcel.md)!`)` <br /> |
| [TextAppearanceSpan](TextAppearanceSpan.md))`(`family:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color:` ` [ColorStateList](../android.content.res/ColorStateList.md)!`, `linkColor:` ` [ColorStateList](../android.content.res/ColorStateList.md)!`)` Makes text be drawn with the specified typeface, size, style, and colors. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](TextAppearanceSpan.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFamily](TextAppearanceSpan.md))`()` Returns the typeface family specified by this span, or`null`if it does not specify one. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFontFeatureSettings](TextAppearanceSpan.md))`()` Returns the font feature settings specified by this span, or`null`if it does not specify one. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFontVariationSettings](TextAppearanceSpan.md))`()` Returns the font variation settings specified by this span, or`null`if it does not specify one. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLetterSpacing](TextAppearanceSpan.md))`()` Returns the value of letter spacing to be added in em unit. |
| open [ColorStateList](../android.content.res/ColorStateList.md)! | [getLinkTextColor](TextAppearanceSpan.md))`()` Returns the link color specified by this span, or`null`if it does not specify one. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getShadowColor](TextAppearanceSpan.md))`()` Returns the color of the text shadow specified by this span, or`0`if it does not specify one. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getShadowDx](TextAppearanceSpan.md))`()` Returns the horizontal offset of the text shadow specified by this span, or`0.0f`if it does not specify one. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getShadowDy](TextAppearanceSpan.md))`()` Returns the vertical offset of the text shadow specified by this span, or`0.0f`if it does not specify one. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getShadowRadius](TextAppearanceSpan.md))`()` Returns the blur radius of the text shadow specified by this span, or`0.0f`if it does not specify one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](TextAppearanceSpan.md))`()` <br /> |
| open [ColorStateList](../android.content.res/ColorStateList.md)! | [getTextColor](TextAppearanceSpan.md))`()` Returns the text color specified by this span, or`null`if it does not specify one. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextFontWeight](TextAppearanceSpan.md))`()` Returns the text font weight specified by this span, or`FontStyle.FONT_WEIGHT_UNSPECIFIED`if it does not specify one. |
| open [LocaleList](../android.os/LocaleList.md)? | [getTextLocales](TextAppearanceSpan.md))`()` Returns the [android.os.LocaleList](../android.os/LocaleList.md) specified by this span, or`null`if it does not specify one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextSize](TextAppearanceSpan.md))`()` Returns the text size specified by this span, or`-1`if it does not specify one. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextStyle](TextAppearanceSpan.md))`()` Returns the text style specified by this span, or`0`if it does not specify one. |
| open [Typeface](../android.graphics/Typeface.md)? | [getTypeface](TextAppearanceSpan.md))`()` Returns the typeface specified by this span, or`null`if it does not specify one. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isElegantTextHeight](TextAppearanceSpan.md))`()` Returns the value of elegant height metrics flag specified by this span, or`false`if it does not specify one. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](TextAppearanceSpan.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](TextAppearanceSpan.md))`(`ds:` ` [TextPaint](../android.text/TextPaint.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](TextAppearanceSpan.md))`(`ds:` ` [TextPaint](../android.text/TextPaint.md)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](TextAppearanceSpan.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MetricAffectingSpan](MetricAffectingSpan.md) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](MetricAffectingSpan.md)! | [getUnderlying](MetricAffectingSpan.md))`()` <br /> Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](CharacterStyle.md)), returns the underlying MetricAffectingSpan. <br /> | ||
| From class [CharacterStyle](CharacterStyle.md) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](CharacterStyle.md))`(`tp:` ` [TextPaint](../android.text/TextPaint.md)!`)` <br /> | | [CharacterStyle](CharacterStyle.md)! | [wrap](CharacterStyle.md))`(`cs:` ` [CharacterStyle](CharacterStyle.md)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## XML attributes

### android:elegantTextHeight

```
android:elegantTextHeight
```
Elegant text height, especially for less compacted complex script text.

May be a boolean value, such as "`true`" or "`false`". 

### android:fontFamily

```
android:fontFamily
```
Font family (named by string or as a font resource reference) for the text.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:fontFeatureSettings

```
android:fontFeatureSettings
```
Font feature settings.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:fontVariationSettings

```
android:fontVariationSettings
```
Font variation settings.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:letterSpacing

```
android:letterSpacing
```
Text letter-spacing.

May be a floating point value, such as "`1.2`". 

### android:shadowColor

```
android:shadowColor
```
Place a blurred shadow of text underneath the text, drawn with the specified color. The text shadow produced does not interact with properties on View that are responsible for real time shadows, [elevation](../android/R.styleable.md) and [translationZ](../android/R.styleable.md).

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:shadowDx

```
android:shadowDx
```
Horizontal offset of the text shadow.

May be a floating point value, such as "`1.2`". 

### android:shadowDy

```
android:shadowDy
```
Vertical offset of the text shadow.

May be a floating point value, such as "`1.2`". 

### android:shadowRadius

```
android:shadowRadius
```
Blur radius of the text shadow.

May be a floating point value, such as "`1.2`". 

### android:textColor

```
android:textColor
```
Text color.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:textColorLink

```
android:textColorLink
```
Color of the links.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

May be a color value, in the form of "*rgb*", "*argb*", "*rrggbb*", or "*aarrggbb*". 

### android:textFontWeight

```
android:textFontWeight
```
Weight for the font used in the TextView.

May be an integer value, such as "`100`". 

### android:textSize

```
android:textSize
```
Size of the text. Recommended dimension type for text is "sp" for scaled-pixels (example: 15sp).

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:textStyle

```
android:textStyle
```
Style (normal, bold, italic, bold|italic) for the text.
| --- | --- |

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|----------|-------|-------------|
| bold | 1 | |
| italic | 2 | |
| normal | 0 | |
| --- | --- | --- |

### android:typeface

```
android:typeface
```
Typeface (normal, sans, serif, monospace) for the text.

Must be one of the following constant values.

| Constant | Value | Description |
|-----------|-------|-------------|
| monospace | 3 | |
| normal | 0 | |
| sans | 1 | |
| --- | --- | --- |
| serif | 2 | |

## Public constructors

### TextAppearanceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextAppearanceSpan(
    context: Context!, 
    appearance: Int)
```

Uses the specified TextAppearance resource to determine the text appearance. The`appearance`should be, for example,`android.R.style.TextAppearance_Small`. 

### TextAppearanceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextAppearanceSpan(
    context: Context!, 
    appearance: Int, 
    colorList: Int)
```

Uses the specified TextAppearance resource to determine the text appearance, and the specified text color resource to determine the color. The`appearance`should be, for example,`android.R.style.TextAppearance_Small`, and the`colorList`should be, for example,`android.R.styleable.Theme_textColorPrimary`. 

### TextAppearanceSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextAppearanceSpan(src: Parcel!)
```  

### TextAppearanceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextAppearanceSpan(
    family: String!, 
    style: Int, 
    size: Int, 
    color: ColorStateList!, 
    linkColor: ColorStateList!)
```

Makes text be drawn with the specified typeface, size, style, and colors.

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFamily(): String!
```

Returns the typeface family specified by this span, or`null`if it does not specify one. 

### getFontFeatureSettings

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFontFeatureSettings(): String?
```

Returns the font feature settings specified by this span, or`null`if it does not specify one. 

### getFontVariationSettings

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFontVariationSettings(): String?
```

Returns the font variation settings specified by this span, or`null`if it does not specify one. 

### getLetterSpacing

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLetterSpacing(): Float
```

Returns the value of letter spacing to be added in em unit.

| Return ||
|--------------------------------------------------------------------------------|-------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a letter spacing amount |

### getLinkTextColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLinkTextColor(): ColorStateList!
```

Returns the link color specified by this span, or`null`if it does not specify one. 

### getShadowColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShadowColor(): Int
```

Returns the color of the text shadow specified by this span, or`0`if it does not specify one. 

### getShadowDx

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShadowDx(): Float
```

Returns the horizontal offset of the text shadow specified by this span, or`0.0f`if it does not specify one. 

### getShadowDy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShadowDy(): Float
```

Returns the vertical offset of the text shadow specified by this span, or`0.0f`if it does not specify one. 

### getShadowRadius

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShadowRadius(): Float
```

Returns the blur radius of the text shadow specified by this span, or`0.0f`if it does not specify one. 

### getSpanTypeId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanTypeId(): Int
```  

### getTextColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextColor(): ColorStateList!
```

Returns the text color specified by this span, or`null`if it does not specify one. 

### getTextFontWeight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextFontWeight(): Int
```

Returns the text font weight specified by this span, or`FontStyle.FONT_WEIGHT_UNSPECIFIED`if it does not specify one. 

### getTextLocales

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextLocales(): LocaleList?
```

Returns the [android.os.LocaleList](../android.os/LocaleList.md) specified by this span, or`null`if it does not specify one. 

### getTextSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextSize(): Int
```

Returns the text size specified by this span, or`-1`if it does not specify one. 

### getTextStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextStyle(): Int
```

Returns the text style specified by this span, or`0`if it does not specify one. 

### getTypeface

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTypeface(): Typeface?
```

Returns the typeface specified by this span, or`null`if it does not specify one. 

### isElegantTextHeight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isElegantTextHeight(): Boolean
```

Returns the value of elegant height metrics flag specified by this span, or`false`if it does not specify one. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### updateDrawState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateDrawState(ds: TextPaint!): Unit
```  

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateMeasureState(ds: TextPaint): Unit
```

| Parameters ||
|-------------|-----------------------------------------------------------------|
| `textPaint` | the paint used for drawing the text This value cannot be`null`. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
