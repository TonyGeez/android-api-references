# TextAppearanceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextAppearanceSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/TextAppearanceSpan "View this page in Java") 
| --- | --- |

```
open class TextAppearanceSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |||
| | ↳ | [android.text.style.MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) ||
| | | ↳ | [android.text.style.TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#) |
| --- | --- | --- | --- |

Sets the text appearance using the given [TextAppearance](https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance:kotlin.IntArray) attributes. By default [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#) only changes the specified attributes in XML. [textColorHighlight](https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance_textColorHighlight:kotlin.Int), [textColorHint](https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance_textColorHint:kotlin.Int), [textAllCaps](https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance_textAllCaps:kotlin.Int) and [fallbackLineSpacing](https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance_fallbackLineSpacing:kotlin.Int) are not supported by [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#). {@see android.widget.TextView#setTextAppearance(int)}

## Summary

| XML attributes ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [`android:elegantTextHeight`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Elegant text height, especially for less compacted complex script text. |
| [`android:fontFamily`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Font family (named by string or as a font resource reference) for the text. |
| [`android:fontFeatureSettings`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Font feature settings. |
| --- | --- |
| [`android:fontVariationSettings`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Font variation settings. |
| [`android:letterSpacing`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Text letter-spacing. |
| [`android:shadowColor`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Place a blurred shadow of text underneath the text, drawn with the specified color. |
| --- | --- |
| [`android:shadowDx`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Horizontal offset of the text shadow. |
| [`android:shadowDy`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Vertical offset of the text shadow. |
| [`android:shadowRadius`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Blur radius of the text shadow. |
| --- | --- |
| [`android:textColor`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Text color. |
| [`android:textColorLink`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Color of the links. |
| [`android:textFontWeight`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Weight for the font used in the TextView. |
| --- | --- |
| [`android:textSize`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Size of the text. |
| [`android:textStyle`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Style (normal, bold, italic, bold|italic) for the text. |
| [`android:typeface`](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#attr_TextAppearanceSpan) | Typeface (normal, sans, serif, monospace) for the text. |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#TextAppearanceSpan(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `appearance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Uses the specified TextAppearance resource to determine the text appearance. |
| [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#TextAppearanceSpan(android.content.Context,%20kotlin.Int,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `appearance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colorList:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Uses the specified TextAppearance resource to determine the text appearance, and the specified text color resource to determine the color. |
| [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#TextAppearanceSpan(android.os.Parcel))`(`src:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#TextAppearanceSpan(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20android.content.res.ColorStateList,%20android.content.res.ColorStateList))`(`family:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)!`, `linkColor:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)!`)` Makes text be drawn with the specified typeface, size, style, and colors. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#describeContents())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFamily](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getFamily())`()` Returns the typeface family specified by this span, or`null`if it does not specify one. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFontFeatureSettings](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getFontFeatureSettings())`()` Returns the font feature settings specified by this span, or`null`if it does not specify one. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFontVariationSettings](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getFontVariationSettings())`()` Returns the font variation settings specified by this span, or`null`if it does not specify one. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLetterSpacing](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getLetterSpacing())`()` Returns the value of letter spacing to be added in em unit. |
| open [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)! | [getLinkTextColor](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getLinkTextColor())`()` Returns the link color specified by this span, or`null`if it does not specify one. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getShadowColor](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getShadowColor())`()` Returns the color of the text shadow specified by this span, or`0`if it does not specify one. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getShadowDx](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getShadowDx())`()` Returns the horizontal offset of the text shadow specified by this span, or`0.0f`if it does not specify one. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getShadowDy](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getShadowDy())`()` Returns the vertical offset of the text shadow specified by this span, or`0.0f`if it does not specify one. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getShadowRadius](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getShadowRadius())`()` Returns the blur radius of the text shadow specified by this span, or`0.0f`if it does not specify one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getSpanTypeId())`()` <br /> |
| open [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)! | [getTextColor](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getTextColor())`()` Returns the text color specified by this span, or`null`if it does not specify one. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextFontWeight](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getTextFontWeight())`()` Returns the text font weight specified by this span, or`FontStyle.FONT_WEIGHT_UNSPECIFIED`if it does not specify one. |
| open [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)? | [getTextLocales](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getTextLocales())`()` Returns the [android.os.LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) specified by this span, or`null`if it does not specify one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextSize](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getTextSize())`()` Returns the text size specified by this span, or`-1`if it does not specify one. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextStyle](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getTextStyle())`()` Returns the text style specified by this span, or`0`if it does not specify one. |
| open [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#)? | [getTypeface](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#getTypeface())`()` Returns the typeface specified by this span, or`null`if it does not specify one. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isElegantTextHeight](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#isElegantTextHeight())`()` Returns the value of elegant height metrics flag specified by this span, or`false`if it does not specify one. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#updateDrawState(android.text.TextPaint))`(`ds:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#updateMeasureState(android.text.TextPaint))`(`ds:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying())`()` <br /> Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying MetricAffectingSpan. <br /> | ||
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint))`(`tp:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

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
Place a blurred shadow of text underneath the text, drawn with the specified color. The text shadow produced does not interact with properties on View that are responsible for real time shadows, [elevation](https://developer.android.com/reference/kotlin/android/R.styleable.html#View_elevation:kotlin.Int) and [translationZ](https://developer.android.com/reference/kotlin/android/R.styleable.html#View_translationZ:kotlin.Int).

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Returns the [android.os.LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) specified by this span, or`null`if it does not specify one. 

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
