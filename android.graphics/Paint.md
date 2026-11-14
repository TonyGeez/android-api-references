Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Paint

Kotlin | [Java](Paint.md)
| --- | --- |

```
open class Paint
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Paint](Paint.md) |

| Known Direct Subclasses [TextPaint](../android.text/TextPaint.md) |---|---| | [TextPaint](../android.text/TextPaint.md) | TextPaint is an extension of Paint that leaves room for some extra data used during text measuring and drawing. | |
| --- | --- | --- | --- | --- | --- | --- |

The Paint class holds the style and color information about how to draw geometries, text and bitmaps.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/graphics/Paint.Align` Align specifies how drawText aligns its text relative to the \[x,y\] coordinates. |
| | `https://developer.android.com/reference/kotlin/android/graphics/Paint.Cap` The Cap specifies the treatment for the beginning and ending of stroked lines and paths. |
| open | `https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics` Class that describes the various metrics for a font at a given text size. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt` Convenience method for callers that want to have FontMetrics values as integers. |
| | `https://developer.android.com/reference/kotlin/android/graphics/Paint.Join` The Join specifies the treatment where lines and curve segments join on a stroked path. |
| | `https://developer.android.com/reference/kotlin/android/graphics/Paint.Style` The Style specifies if the primitive being drawn is filled, stroked, or both (in the same color). |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int` Paint flag that enables antialiasing when drawing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AFTER:kotlin.Int` Option for getTextRunCursor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT:kotlin.Int` Option for getTextRunCursor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT_OR_AFTER:kotlin.Int` Option for getTextRunCursor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT_OR_BEFORE:kotlin.Int` Option for getTextRunCursor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_BEFORE:kotlin.Int` Option for getTextRunCursor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#DEV_KERN_TEXT_FLAG:kotlin.Int` Legacy Paint flag, no longer used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#DITHER_FLAG:kotlin.Int` Paint flag that enables dithering when blitting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#EMBEDDED_BITMAP_TEXT_FLAG:kotlin.Int` Paint flag that enables the use of bitmap fonts when drawing text. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_ARMENIAN_HYPHEN:kotlin.Int` An integer representing the end of the line has Armentian hyphen (U+058A). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` An integer representing the end of the line has normal hyphen character (U+002D). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_MAQAF:kotlin.Int` An integer representing the end of the line has maqaf (Hebrew hyphen, U+05BE). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_UCAS_HYPHEN:kotlin.Int` An integer representing the end of the line has Canadian Syllabics hyphen (U+1400). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_ZWJ_AND_HYPHEN:kotlin.Int` An integer representing the end of the line has Zero-Width-Joiner (U+200D) followed by normal hyphen character (U+002D). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_NO_EDIT:kotlin.Int` An integer representing the end of the line has no modification for hyphenation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_REPLACE_WITH_HYPHEN:kotlin.Int` An integer representing the character at the end of the line is replaced with hyphen character (U+002D). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#FAKE_BOLD_TEXT_FLAG:kotlin.Int` Paint flag that applies a synthetic bolding effect to drawn text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#FILTER_BITMAP_FLAG:kotlin.Int` Paint flag that enables bilinear sampling on scaled bitmaps. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#HINTING_OFF:kotlin.Int` Font hinter option that disables font hinting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#HINTING_ON:kotlin.Int` Font hinter option that enables font hinting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#LINEAR_TEXT_FLAG:kotlin.Int` Paint flag that enables smooth linear scaling of text. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` An integer representing the starting of the line has normal hyphen character (U+002D). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_INSERT_ZWJ:kotlin.Int` An integer representing the starting of the line has Zero-Width-Joiner (U+200D). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_NO_EDIT:kotlin.Int` An integer representing the starting of the line has no modification for hyphenation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#STRIKE_THRU_TEXT_FLAG:kotlin.Int` Paint flag that applies a strike-through decoration to drawn text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#SUBPIXEL_TEXT_FLAG:kotlin.Int` Paint flag that enables subpixel positioning of text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` A text run flag that indicates the run is located the visually most left segment of the line. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` A text run flag that indicates the run is located the visually most right segment of the line. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#UNDERLINE_TEXT_FLAG:kotlin.Int` Paint flag that applies an underline decoration to drawn text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#VERTICAL_TEXT_FLAG:kotlin.Int` A flat that controls text to be written in vertical orientation |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint()()` Create a new paint with default settings. |
| `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(android.graphics.Paint)(paint: https://developer.android.com/reference/kotlin/android/graphics/Paint#!)` Create a new paint, initialized with the attributes in the specified paint parameter. |
| `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new paint with the specified flags. |

| Public methods ||
|---|---|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#ascent()()` Return the distance above (negative) the baseline (ascent) based on the current typeface and text size. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#breakText(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, measuredWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)` Measure the text, stopping early if the measured width exceeds maxWidth. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#breakText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, measureForwards: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, measuredWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)` Measure the text, stopping early if the measured width exceeds maxWidth. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#breakText(kotlin.String,%20kotlin.Boolean,%20kotlin.Float,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, measureForwards: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, measuredWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)` Measure the text, stopping early if the measured width exceeds maxWidth. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#clearShadowLayer()()` Clear the shadow layer. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#descent()()` Return the distance below (positive) the baseline (descent) based on the current typeface and text size. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#equalsForTextMeasurement(android.graphics.Paint)(other: https://developer.android.com/reference/kotlin/android/graphics/Paint#)` Returns true of the passed `https://developer.android.com/reference/kotlin/android/graphics/Paint#` will have the same effect on text measurement |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getAlpha()()` Helper to getColor() that just returns the color's alpha value. |
| open [BlendMode](BlendMode.md)? | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getBlendMode()()` Get the paint's blend mode object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getColor()()` Return the paint's color in sRGB. |
| open [ColorFilter](ColorFilter.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getColorFilter()()` Get the paint's colorfilter (maybe be null). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getColorLong()()` Return the paint's color. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getEndHyphenEdit()()` Get the current value of end hyphen edit. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFillPath(android.graphics.Path,%20android.graphics.Path)(src: https://developer.android.com/reference/kotlin/android/graphics/Path!, dst: https://developer.android.com/reference/kotlin/android/graphics/Path!)` Applies any/all effects (patheffect, stroking) to src, returning the result in dst. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFlags()()` Return the paint's flags. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontFeatureSettings()()` Returns the font feature settings. |
| open [Paint.FontMetrics](../android/graphics/Paint.FontMetrics.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontMetrics()()` Allocates a new FontMetrics object, and then calls getFontMetrics(fm) with it, returning the object. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontMetrics(android.graphics.Paint.FontMetrics)(metrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics!)` Return the font's recommended interline spacing, given the Paint's settings for typeface, textSize, etc. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontMetricsForLocale(android.graphics.Paint.FontMetrics)(metrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics)` Get the font metrics used for the locale Obtain the metrics of the font that is used for the specified locale by `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextLocales(android.os.LocaleList)`. |
| open [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontMetricsInt()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontMetricsInt(android.graphics.Paint.FontMetricsInt)(fmi: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt!)` Return the font's interline spacing, given the Paint's settings for typeface, textSize, etc. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontMetricsInt(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.graphics.Paint.FontMetricsInt)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, outMetrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt)` Returns the font metrics value for the given text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontMetricsInt(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.graphics.Paint.FontMetricsInt)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, outMetrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt)` Returns the font metrics value for the given text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontMetricsIntForLocale(android.graphics.Paint.FontMetricsInt)(metrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt)` Get the font metrics used for the locale Obtain the metrics of the font that is used for the specified locale by `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextLocales(android.os.LocaleList)`. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontSpacing()()` Return the recommend line spacing based on the current typeface and text size. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontVariationOverride()()` Gets the current font variation override value. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontVariationSettings()()` Returns the font variation settings. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getHinting()()` Return the paint's hinting mode. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getLetterSpacing()()` Return the paint's letter-spacing for text. |
| open [MaskFilter](MaskFilter.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getMaskFilter()()` Get the paint's maskfilter object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getOffsetForAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, advance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Get the character offset within the string whose position is closest to the specified horizontal position. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getOffsetForAdvance(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, advance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` <br /> |
| open [PathEffect](PathEffect.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getPathEffect()()` Get the paint's patheffect object. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Measure cursor position within a run of text. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunAdvance(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunCharacterAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, advances: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?, advancesIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Measure the advance of each character within a run of text and also return the cursor position within the run. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunCharacterAdvance(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, advances: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?, advancesIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Shader](Shader.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getShader()()` Get the paint's shader object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getShadowLayerColor()()` Returns the color of the shadow layer. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getShadowLayerColorLong()()` Returns the color of the shadow layer. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getShadowLayerDx()()` Returns the x offset of the shadow layer. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getShadowLayerDy()()` Returns the y offset of the shadow layer. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getShadowLayerRadius()()` Returns the blur radius of the shadow layer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStartHyphenEdit()()` Get the current value of start hyphen edit. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrikeThruPosition()()` Distance from top of the strike-through line to the baseline in pixels. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrikeThruThickness()()` Returns the thickness of the strike-through line in pixels. |
| open [Paint.Cap](../android/graphics/Paint.Cap.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrokeCap()()` Return the paint's Cap, controlling how the start and end of stroked lines and paths are treated. |
| open [Paint.Join](../android/graphics/Paint.Join.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrokeJoin()()` Return the paint's stroke join type. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrokeMiter()()` Return the paint's stroke miter value. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrokeWidth()()` Return the width for stroking. |
| open [Paint.Style](../android/graphics/Paint.Style.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStyle()()` Return the paint's style, used for controlling how primitives' geometries are interpreted (except for drawBitmap, which always assumes FILL_STYLE). |
| --- | --- |
| open [Paint.Align](../android/graphics/Paint.Align.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextAlign()()` Return the paint's Align value for drawing text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextBounds(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Rect)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect!)` Return in bounds (allocated by the caller) the smallest rectangle that encloses all of the characters, with an implied origin at (0,0). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextBounds(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Rect)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect)` Retrieve the text boundary box and store to bounds. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextBounds(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Rect)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect!)` Retrieve the text boundary box and store to bounds. |
| open [Locale](../java.util/Locale.md) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextLocale()()` Get the text's primary Locale. |
| open [LocaleList](../android.os/LocaleList.md) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextLocales()()` Get the text locale list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextPath(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, path: https://developer.android.com/reference/kotlin/android/graphics/Path!)` Return the path (outline) for the specified text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextPath(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, path: https://developer.android.com/reference/kotlin/android/graphics/Path!)` Return the path (outline) for the specified text. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextRunAdvances(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.FloatArray,%20kotlin.Int)(chars: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, advances: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?, advancesIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve the character advances of the text. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextRunCursor(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, cursorOpt: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the next cursor position in the run. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextRunCursor(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, cursorOpt: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the next cursor position in the run. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextScaleX()()` Return the paint's horizontal scale factor for text. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextSize()()` Return the paint's text size. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextSkewX()()` Return the paint's horizontal skew factor for text. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextWidths(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, widths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)` Return the advance widths for the characters in the string. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextWidths(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, widths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)` Return the advance widths for the characters in the string. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextWidths(kotlin.String,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, widths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)` Return the advance widths for the characters in the string. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextWidths(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, widths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)` Return the advance widths for the characters in the string. |
| --- | --- |
| open [Typeface](Typeface.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTypeface()()` Get the paint's typeface object. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getUnderlinePosition()()` Returns the distance from top of the underline to the baseline in pixels. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getUnderlineThickness()()` Returns the thickness of the underline in pixels. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getWordSpacing()()` Return the paint's extra word-spacing for text. |
| open [Xfermode](Xfermode.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#getXfermode()()` Get the paint's transfer mode object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#hasGlyph(kotlin.String)(string: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Determine whether the typeface set on the paint has a glyph supporting the string. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isAntiAlias()()` Helper for getFlags(), returning true if ANTI_ALIAS_FLAG bit is set AntiAliasing smooths out the edges of what is being drawn, but is has no impact on the interior of the shape. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isDither()()` Helper for getFlags(), returning true if DITHER_FLAG bit is set Dithering affects how colors that are higher precision than the device are down-sampled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isElegantTextHeight()()` Get the elegant metrics flag. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isFakeBoldText()()` Helper for getFlags(), returning true if FAKE_BOLD_TEXT_FLAG bit is set |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isFilterBitmap()()` Whether or not the bitmap filter is activated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isLinearText()()` Helper for getFlags(), returning true if LINEAR_TEXT_FLAG bit is set |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isStrikeThruText()()` Helper for getFlags(), returning true if STRIKE_THRU_TEXT_FLAG bit is set |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isSubpixelText()()` Helper for getFlags(), returning true if SUBPIXEL_TEXT_FLAG bit is set |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#isUnderlineText()()` Helper for getFlags(), returning true if UNDERLINE_TEXT_FLAG bit is set |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#measureText(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the width of the text. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#measureText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the width of the text. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#measureText(kotlin.String)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return the width of the text. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#measureText(kotlin.String,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the width of the text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#reset()()` Restores the paint to its default settings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#set(android.graphics.Paint)(src: https://developer.android.com/reference/kotlin/android/graphics/Paint#!)` Copy the fields from src into this paint. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setARGB(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, g: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Helper to setColor(), that takes a,r,g,b and constructs the color int |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setAlpha(kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Helper to setColor(), that only assigns the color's alpha value, leaving its r,g,b values unchanged. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setAntiAlias(kotlin.Boolean)(aa: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Helper for setFlags(), setting or clearing the ANTI_ALIAS_FLAG bit AntiAliasing smooths out the edges of what is being drawn, but is has no impact on the interior of the shape. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setBlendMode(android.graphics.BlendMode)(blendmode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode?)` Set or clear the blend mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the paint's color. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setColor(kotlin.Long)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Set the paint's color with a `ColorLong`. |
| --- | --- |
| open [ColorFilter](ColorFilter.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setColorFilter(android.graphics.ColorFilter)(filter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter!)` Set or clear the paint's colorfilter, returning the parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setDither(kotlin.Boolean)(dither: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Helper for setFlags(), setting or clearing the DITHER_FLAG bit Dithering affects how colors that are higher precision than the device are down-sampled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setElegantTextHeight(kotlin.Boolean)(elegant: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set the paint's elegant height metrics flag. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setEndHyphenEdit(kotlin.Int)(endHyphen: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set a end hyphen edit on the paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFakeBoldText(kotlin.Boolean)(fakeBoldText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Helper for setFlags(), setting or clearing the FAKE_BOLD_TEXT_FLAG bit |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFilterBitmap(kotlin.Boolean)(filter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Helper for setFlags(), setting or clearing the FILTER_BITMAP_FLAG bit. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the paint's flags. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFontFeatureSettings(kotlin.String)(settings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set font feature settings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFontVariationOverride(kotlin.String)(fontVariationOverride: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Sets TrueType or OpenType font variation settings for overriding. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFontVariationSettings(kotlin.String)(fontVariationSettings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets TrueType or OpenType font variation settings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setHinting(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the paint's hinting mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setLetterSpacing(kotlin.Float)(letterSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the paint's letter-spacing for text. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setLinearText(kotlin.Boolean)(linearText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Helper for setFlags(), setting or clearing the LINEAR_TEXT_FLAG bit |
| open [MaskFilter](MaskFilter.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setMaskFilter(android.graphics.MaskFilter)(maskfilter: https://developer.android.com/reference/kotlin/android/graphics/MaskFilter!)` Set or clear the maskfilter object. |
| open [PathEffect](PathEffect.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setPathEffect(android.graphics.PathEffect)(effect: https://developer.android.com/reference/kotlin/android/graphics/PathEffect!)` Set or clear the patheffect object. |
| --- | --- |
| open [Shader](Shader.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShader(android.graphics.Shader)(shader: https://developer.android.com/reference/kotlin/android/graphics/Shader!)` Set or clear the shader object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)(radius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, shadowColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This draws a shadow layer below the main layer, with the specified offset and color, and blur radius. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Long)(radius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, shadowColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` This draws a shadow layer below the main layer, with the specified offset and color, and blur radius. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStartHyphenEdit(kotlin.Int)(startHyphen: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set a start hyphen edit on the paint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStrikeThruText(kotlin.Boolean)(strikeThruText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Helper for setFlags(), setting or clearing the STRIKE_THRU_TEXT_FLAG bit |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStrokeCap(android.graphics.Paint.Cap)(cap: https://developer.android.com/reference/kotlin/android/graphics/Paint.Cap!)` Set the paint's Cap. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStrokeJoin(android.graphics.Paint.Join)(join: https://developer.android.com/reference/kotlin/android/graphics/Paint.Join!)` Set the paint's Join. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStrokeMiter(kotlin.Float)(miter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the paint's stroke miter value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStrokeWidth(kotlin.Float)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the width for stroking. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStyle(android.graphics.Paint.Style)(style: https://developer.android.com/reference/kotlin/android/graphics/Paint.Style!)` Set the paint's style, used for controlling how primitives' geometries are interpreted (except for drawBitmap, which always assumes Fill). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setSubpixelText(kotlin.Boolean)(subpixelText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Helper for setFlags(), setting or clearing the SUBPIXEL_TEXT_FLAG bit |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextAlign(android.graphics.Paint.Align)(align: https://developer.android.com/reference/kotlin/android/graphics/Paint.Align!)` Set the paint's text alignment. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextLocale(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#)` Set the text locale list to a one-member list consisting of just the locale. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextLocales(android.os.LocaleList)(locales: https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)` Set the text locale list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextScaleX(kotlin.Float)(scaleX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the paint's horizontal scale factor for text. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextSize(kotlin.Float)(textSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the paint's text size. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextSkewX(kotlin.Float)(skewX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the paint's horizontal skew factor for text. |
| open [Typeface](Typeface.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTypeface(android.graphics.Typeface)(typeface: https://developer.android.com/reference/kotlin/android/graphics/Typeface!)` Set or clear the typeface object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setUnderlineText(kotlin.Boolean)(underlineText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Helper for setFlags(), setting or clearing the UNDERLINE_TEXT_FLAG bit |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setWordSpacing(kotlin.Float)(wordSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the paint's extra word-spacing for text. |
| open [Xfermode](Xfermode.md)! | `https://developer.android.com/reference/kotlin/android/graphics/Paint#setXfermode(android.graphics.Xfermode)(xfermode: https://developer.android.com/reference/kotlin/android/graphics/Xfermode!)` Set or clear the transfer mode object. |
| --- | --- |

## Constants

### ANTI_ALIAS_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANTI_ALIAS_FLAG: Int
```

Paint flag that enables antialiasing when drawing.

Enabling this flag will cause all draw operations that support antialiasing to use it.

Notable draw operations that do **not** support antialiasing include:

- `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawBitmapMesh(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int,%20android.graphics.Paint)`
- android.graphics.Canvas#drawPatch
- `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawVertices(android.graphics.Canvas.VertexMode,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.ShortArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint)`

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### CURSOR_AFTER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_AFTER: Int
```

Option for getTextRunCursor. Compute the valid cursor after offset or the limit of the context, whichever is less.

 Value: 0

### CURSOR_AT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_AT: Int
```

Option for getTextRunCursor. Return offset if the cursor at offset is valid, or -1 if it isn't.

 Value: 4

### CURSOR_AT_OR_AFTER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_AT_OR_AFTER: Int
```

Option for getTextRunCursor. Compute the valid cursor at or after the offset or the limit of the context, whichever is less.

 Value: 1

### CURSOR_AT_OR_BEFORE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_AT_OR_BEFORE: Int
```

Option for getTextRunCursor. Compute the valid cursor at or before offset or the start of the context, whichever is greater.

 Value: 3

### CURSOR_BEFORE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURSOR_BEFORE: Int
```

Option for getTextRunCursor. Compute the valid cursor before offset or the start of the context, whichever is greater.

 Value: 2

### DEV_KERN_TEXT_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEV_KERN_TEXT_FLAG: Int
```

Legacy Paint flag, no longer used.

 Value: 256

### DITHER_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DITHER_FLAG: Int
```

Paint flag that enables dithering when blitting.

Enabling this flag applies a dither to any blit operation where the target's colour space is more constrained than the source.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### EMBEDDED_BITMAP_TEXT_FLAG

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMBEDDED_BITMAP_TEXT_FLAG: Int
```

Paint flag that enables the use of bitmap fonts when drawing text.

Disabling this flag will prevent text draw operations from using embedded bitmap strikes in fonts, causing fonts with both scalable outlines and bitmap strikes to draw only the scalable outlines, and fonts with only bitmap strikes to not draw at all.

 Value: 1024

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### END_HYPHEN_EDIT_INSERT_ARMENIAN_HYPHEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val END_HYPHEN_EDIT_INSERT_ARMENIAN_HYPHEN: Int
```

An integer representing the end of the line has Armentian hyphen (U+058A).

 Value: 3

### END_HYPHEN_EDIT_INSERT_HYPHEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val END_HYPHEN_EDIT_INSERT_HYPHEN: Int
```

An integer representing the end of the line has normal hyphen character (U+002D).

 Value: 2

### END_HYPHEN_EDIT_INSERT_MAQAF

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val END_HYPHEN_EDIT_INSERT_MAQAF: Int
```

An integer representing the end of the line has maqaf (Hebrew hyphen, U+05BE).

 Value: 4

### END_HYPHEN_EDIT_INSERT_UCAS_HYPHEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val END_HYPHEN_EDIT_INSERT_UCAS_HYPHEN: Int
```

An integer representing the end of the line has Canadian Syllabics hyphen (U+1400).

 Value: 5

### END_HYPHEN_EDIT_INSERT_ZWJ_AND_HYPHEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val END_HYPHEN_EDIT_INSERT_ZWJ_AND_HYPHEN: Int
```

An integer representing the end of the line has Zero-Width-Joiner (U+200D) followed by normal hyphen character (U+002D).

 Value: 6

### END_HYPHEN_EDIT_NO_EDIT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val END_HYPHEN_EDIT_NO_EDIT: Int
```

An integer representing the end of the line has no modification for hyphenation.

 Value: 0

### END_HYPHEN_EDIT_REPLACE_WITH_HYPHEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val END_HYPHEN_EDIT_REPLACE_WITH_HYPHEN: Int
```

An integer representing the character at the end of the line is replaced with hyphen character (U+002D).

 Value: 1

### FAKE_BOLD_TEXT_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FAKE_BOLD_TEXT_FLAG: Int
```

Paint flag that applies a synthetic bolding effect to drawn text.

Enabling this flag will cause text draw operations to apply a simulated bold effect when drawing a `https://developer.android.com/reference/kotlin/android/graphics/Typeface` that is not already bold.

 Value: 32

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### FILTER_BITMAP_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FILTER_BITMAP_FLAG: Int
```

Paint flag that enables bilinear sampling on scaled bitmaps.

If cleared, scaled bitmaps will be drawn with nearest neighbor sampling, likely resulting in artifacts. This should generally be on when drawing bitmaps, unless performance-bound (rendering to software canvas) or preferring pixelation artifacts to blurriness when scaling significantly.

If bitmaps are scaled for device density at creation time (as resource bitmaps often are) the filtering will already have been done.

On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and below, hardware accelerated drawing always uses bilinear sampling on scaled bitmaps, regardless of this flag. On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and above, this flag defaults to being set on a new `Paint`. It can be cleared with `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFilterBitmap(kotlin.Boolean)`.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### HINTING_OFF

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINTING_OFF: Int
```

Font hinter option that disables font hinting.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setHinting(kotlin.Int)`

### HINTING_ON

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINTING_ON: Int
```

Font hinter option that enables font hinting.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setHinting(kotlin.Int)`

### LINEAR_TEXT_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LINEAR_TEXT_FLAG: Int
```

Paint flag that enables smooth linear scaling of text.

Enabling this flag does not actually scale text, but rather adjusts text draw operations to deal gracefully with smooth adjustment of scale. When this flag is enabled, font hinting is disabled to prevent shape deformation between scale factors, and glyph caching is disabled due to the large number of glyph images that will be generated.

`https://developer.android.com/reference/kotlin/android/graphics/Paint#SUBPIXEL_TEXT_FLAG:kotlin.Int` should be used in conjunction with this flag to prevent glyph positions from snapping to whole pixel values as scale factor is adjusted.

 Value: 64

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### START_HYPHEN_EDIT_INSERT_HYPHEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_HYPHEN_EDIT_INSERT_HYPHEN: Int
```

An integer representing the starting of the line has normal hyphen character (U+002D).

 Value: 1

### START_HYPHEN_EDIT_INSERT_ZWJ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_HYPHEN_EDIT_INSERT_ZWJ: Int
```

An integer representing the starting of the line has Zero-Width-Joiner (U+200D).

 Value: 2

### START_HYPHEN_EDIT_NO_EDIT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_HYPHEN_EDIT_NO_EDIT: Int
```

An integer representing the starting of the line has no modification for hyphenation.

 Value: 0

### STRIKE_THRU_TEXT_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRIKE_THRU_TEXT_FLAG: Int
```

Paint flag that applies a strike-through decoration to drawn text.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### SUBPIXEL_TEXT_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBPIXEL_TEXT_FLAG: Int
```

Paint flag that enables subpixel positioning of text.

Enabling this flag causes glyph advances to be computed with subpixel accuracy.

This can be used with `https://developer.android.com/reference/kotlin/android/graphics/Paint#LINEAR_TEXT_FLAG:kotlin.Int` to prevent text from jittering during smooth scale transitions.

 Value: 128

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### TEXT_RUN_FLAG_LEFT_EDGE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_RUN_FLAG_LEFT_EDGE: Int
```

A text run flag that indicates the run is located the visually most left segment of the line.

This flag is used for telling the underlying text layout engine that the text is located at the most left of the line. This flag is used for controlling the amount letter spacing added. If the text is in the middle of the line, the text layout engine assigns additional letter spacing to the both side of each letter. On the other hand, the letter spacing should not be added to the visually most left and right of the line. By setting this flag, text layout engine calculates the layout as it is located at the most visually left of the line and doesn't add letter spacing to the left of this run.

Note that the caller must resolve BiDi runs and reorder them visually and set this flag only if the target run is located visually most left position. This left does not always mean the beginning of the text.

If the run covers entire line, caller should set `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` as well.

Note that this flag is only effective for run based APIs. For example, this flag works for `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint)` and `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunCharacterAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)`. However, this doesn't work for `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint#measureText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)`. The non-run based APIs works as both `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` are specified.

 Value: 8192

### TEXT_RUN_FLAG_RIGHT_EDGE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEXT_RUN_FLAG_RIGHT_EDGE: Int
```

A text run flag that indicates the run is located the visually most right segment of the line.

This flag is used for telling the underlying text layout engine that the text is located at the most right of the line. This flag is used for controlling the amount letter spacing added. If the text is in the middle of the line, the text layout engine assigns additional letter spacing to the both side of each letter. On the other hand, the letter spacing should not be added to the visually most left and right of the line. By setting this flag, text layout engine calculates the layout as it is located at the most visually left of the line and doesn't add letter spacing to the left of this run.

Note that the caller must resolve BiDi runs and reorder them visually and set this flag only if the target run is located visually most right position. This right does not always mean the end of the text.

If the run covers entire line, caller should set `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` as well.

Note that this flag is only effective for run based APIs. For example, this flag works for `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint)` and `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunCharacterAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)`. However, this doesn't work for `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint#measureText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)`. The non-run based APIs works as both `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` are specified.

 Value: 16384

### UNDERLINE_TEXT_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNDERLINE_TEXT_FLAG: Int
```

Paint flag that applies an underline decoration to drawn text.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#Paint(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)`

### VERTICAL_TEXT_FLAG

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERTICAL_TEXT_FLAG: Int
```

A flat that controls text to be written in vertical orientation

This flag is used for telling the underlying text layout engine that the text is for vertical direction. By enabling this flag, text measurement, drawing and shaping APIs works for vertical text layout. For example, `https://developer.android.com/reference/kotlin/android/graphics/Canvas#drawText(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint)` draws text from top to bottom. `https://developer.android.com/reference/kotlin/android/graphics/Paint#measureText(kotlin.String)` returns vertical advances instead of horizontal advances. `https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper` shapes text vertically and report glyph IDs for vertical layout.

Do not set this flag for making `https://developer.android.com/reference/kotlin/android/text/Layout.html#`. The `https://developer.android.com/reference/kotlin/android/text/Layout.html#` class and its subclasses are designed for horizontal text only and does not work for vertical text.

 Value: 4096

## Public constructors

### Paint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Paint()
```

Create a new paint with default settings.

On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and below, hardware accelerated drawing always acts as if `https://developer.android.com/reference/kotlin/android/graphics/Paint#FILTER_BITMAP_FLAG:kotlin.Int` is set. On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and above, `FILTER_BITMAP_FLAG` is set by this constructor, and it can be cleared with `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFilterBitmap(kotlin.Boolean)`. On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` and above, `ANTI_ALIAS_FLAG` is set by this constructor, and it can be cleared with `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint#setAntiAlias(kotlin.Boolean)`.

### Paint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Paint(paint: Paint!)
```

Create a new paint, initialized with the attributes in the specified paint parameter.

| Parameters ||
|---|---|
| `paint` | [Paint](Paint.md)!: Existing paint used to initialized the attributes of the new paint. |

### Paint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Paint(flags: Int)
```

Create a new paint with the specified flags. Use setFlags() to change these after the paint is created.

On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and below, hardware accelerated drawing always acts as if `https://developer.android.com/reference/kotlin/android/graphics/Paint#FILTER_BITMAP_FLAG:kotlin.Int` is set. On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and above, `FILTER_BITMAP_FLAG` is always set by this constructor, regardless of the value of `flags`. It can be cleared with `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFlags(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFilterBitmap(kotlin.Boolean)`.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): initial flag bits, as if they were passed via setFlags(). |

## Public methods

### ascent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ascent(): Float
```

Return the distance above (negative) the baseline (ascent) based on the current typeface and text size.

Note that this is the ascent of the main typeface, and actual text rendered may need a larger ascent because fallback fonts may get used in rendering the text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the distance above (negative) the baseline (ascent) based on the current typeface and text size. |

### breakText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun breakText(
    text: CharArray!, 
    index: Int, 
    count: Int, 
    maxWidth: Float, 
    measuredWidth: FloatArray!
): Int
```

Measure the text, stopping early if the measured width exceeds maxWidth. Return the number of chars that were measured, and if measuredWidth is not null, return in it the actual width measured.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The text to measure. Cannot be null. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset into text to begin measuring at |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of maximum number of entries to measure. If count is negative, then the characters are measured in reverse order. |
| --- | --- |
| `maxWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The maximum width to accumulate. |
| `measuredWidth` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: Optional. If not null, returns the actual width measured. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of chars that were measured. Will always be \<= abs(count). |

### breakText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun breakText(
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    measureForwards: Boolean, 
    maxWidth: Float, 
    measuredWidth: FloatArray!
): Int
```

Measure the text, stopping early if the measured width exceeds maxWidth. Return the number of chars that were measured, and if measuredWidth is not null, return in it the actual width measured.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset into text to begin measuring at |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The end of the text slice to measure. |
| --- | --- |
| `measureForwards` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, measure forwards, starting at start. Otherwise, measure backwards, starting with end. |
| `maxWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The maximum width to accumulate. |
| `measuredWidth` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: Optional. If not null, returns the actual width measured. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of chars that were measured. Will always be \<= abs(end - start). |

### breakText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun breakText(
    text: String!, 
    measureForwards: Boolean, 
    maxWidth: Float, 
    measuredWidth: FloatArray!
): Int
```

Measure the text, stopping early if the measured width exceeds maxWidth. Return the number of chars that were measured, and if measuredWidth is not null, return in it the actual width measured.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text to measure. Cannot be null. |
| `measureForwards` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, measure forwards, starting with the first character in the string. Otherwise, measure backwards, starting with the last character in the string. |
| `maxWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The maximum width to accumulate. |
| --- | --- |
| `measuredWidth` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: Optional. If not null, returns the actual width measured. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of chars that were measured. Will always be \<= abs(count). |

### clearShadowLayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearShadowLayer(): Unit
```

Clear the shadow layer.

### descent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun descent(): Float
```

Return the distance below (positive) the baseline (descent) based on the current typeface and text size.

Note that this is the descent of the main typeface, and actual text rendered may need a larger descent because fallback fonts may get used in rendering the text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the distance below (positive) the baseline (descent) based on the current typeface and text size. |

### equalsForTextMeasurement

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equalsForTextMeasurement(other: Paint): Boolean
```

Returns true of the passed `https://developer.android.com/reference/kotlin/android/graphics/Paint#` will have the same effect on text measurement

| Parameters ||
|---|---|
| `other` | [Paint](Paint.md): A `https://developer.android.com/reference/kotlin/android/graphics/Paint#` object. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the other `https://developer.android.com/reference/kotlin/android/graphics/Paint#` has the same effect on text measurement. |

### getAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlpha(): Int
```

Helper to getColor() that just returns the color's alpha value. This is the same as calling getColor() \>\>\> 24. It always returns a value between 0 (completely transparent) and 255 (completely opaque).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the alpha component of the paint's color. |

### getBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBlendMode(): BlendMode?
```

Get the paint's blend mode object. Will return null if there is a Xfermode applied that cannot be represented by a blend mode (i.e. a custom `RuntimeXfermode`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/BlendMode?` | the paint's blend mode (or null) |

### getColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColor(): Int
```

Return the paint's color in sRGB. Note that the color is a 32bit value containing alpha as well as r,g,b. This 32bit value is not premultiplied, meaning that its alpha can be any value, regardless of the values of r,g,b. See the Color class for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the paint's color (and alpha). |

### getColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColorFilter(): ColorFilter!
```

Get the paint's colorfilter (maybe be null).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorFilter!` | the paint's colorfilter (maybe be null) |

### getColorLong

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColorLong(): Long
```

Return the paint's color. Note that the color is a long with an encoded `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace` as well as alpha and r,g,b. These values are not premultiplied, meaning that alpha can be any value, regardless of the values of r,g,b. See the `https://developer.android.com/reference/kotlin/android/graphics/Color` class for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the paint's color, alpha, and `ColorSpace` encoded as a `ColorLong` |

### getEndHyphenEdit

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEndHyphenEdit(): Int
```

Get the current value of end hyphen edit. The default value is 0 which is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_NO_EDIT:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current starting hyphen edit value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_NO_EDIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_REPLACE_WITH_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_ARMENIAN_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_MAQAF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_UCAS_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_ZWJ_AND_HYPHEN:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStartHyphenEdit(kotlin.Int)`

### getFillPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFillPath(
    src: Path!, 
    dst: Path!
): Boolean
```

Applies any/all effects (patheffect, stroking) to src, returning the result in dst. The result is that drawing src with this paint will be the same as drawing dst with a default paint (at least from the geometric perspective).

| Parameters ||
|---|---|
| `src` | [Path](Path.md)!: input path |
| `dst` | [Path](Path.md)!: output path (may be the same as src) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the path should be filled, or false if it should be drawn with a hairline (width == 0) |

### getFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFlags(): Int
```

Return the paint's flags. Use the Flag enum to test flag values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the paint's flags (see enums ending in _Flag for bit masks). Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#FILTER_BITMAP_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#DITHER_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#UNDERLINE_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#STRIKE_THRU_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#FAKE_BOLD_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#LINEAR_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#SUBPIXEL_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#EMBEDDED_BITMAP_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` |

### getFontFeatureSettings

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontFeatureSettings(): String!
```

Returns the font feature settings. The format is the same as the CSS font-feature-settings attribute: <https://www.w3.org/TR/css-fonts-3/#font-feature-settings-prop>

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the paint's currently set font feature settings. Default is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFontFeatureSettings(kotlin.String)`

### getFontMetrics

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontMetrics(): Paint.FontMetrics!
```

Allocates a new FontMetrics object, and then calls getFontMetrics(fm) with it, returning the object.

### getFontMetrics

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontMetrics(metrics: Paint.FontMetrics!): Float
```

Return the font's recommended interline spacing, given the Paint's settings for typeface, textSize, etc. If metrics is not null, return the fontmetric values in it.

Note that these are the values for the main typeface, and actual text rendered may need a larger set of values because fallback fonts may get used in rendering the text.

| Parameters ||
|---|---|
| `metrics` | [Paint.FontMetrics](../android/graphics/Paint.FontMetrics.md)!: If this object is not null, its fields are filled with the appropriate values given the paint's text attributes. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the font's recommended interline spacing. |

### getFontMetricsForLocale

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontMetricsForLocale(metrics: Paint.FontMetrics): Unit
```

Get the font metrics used for the locale Obtain the metrics of the font that is used for the specified locale by `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextLocales(android.os.LocaleList)`. If multiple locales are specified, the minimum ascent and maximum descent will be set. This API is useful for determining the default line height of the empty text field, e.g. `https://developer.android.com/reference/kotlin/android/widget/EditText.html#`. Note, if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface` is created from the custom font files, its metrics are reserved, i.e. the ascent will be the custom font's ascent or smaller, the descent will be the custom font's descent or larger. Note, if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface` is a system fallback, e.g. `https://developer.android.com/reference/kotlin/android/graphics/Typeface#SERIF:android.graphics.Typeface`, the default font's metrics are reserved, i.e. the ascent will be the serif font's ascent or smaller, the descent will be the serif font's descent or larger.

| Parameters ||
|---|---|
| `metrics` | [Paint.FontMetrics](../android/graphics/Paint.FontMetrics.md): an output parameter. All members will be set by calling this function. This value cannot be `null`. |

### getFontMetricsInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontMetricsInt(): Paint.FontMetricsInt!
```

### getFontMetricsInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontMetricsInt(fmi: Paint.FontMetricsInt!): Int
```

Return the font's interline spacing, given the Paint's settings for typeface, textSize, etc. If metrics is not null, return the fontmetric values in it. Note: all values have been converted to integers from floats, in such a way has to make the answers useful for both spacing and clipping. If you want more control over the rounding, call getFontMetrics().

Note that these are the values for the main typeface, and actual text rendered may need a larger set of values because fallback fonts may get used in rendering the text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the font's interline spacing. |

### getFontMetricsInt

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontMetricsInt(
    text: CharArray, 
    start: Int, 
    count: Int, 
    contextStart: Int, 
    contextCount: Int, 
    isRtl: Boolean, 
    outMetrics: Paint.FontMetricsInt
): Unit
```

Returns the font metrics value for the given text. If the text is rendered with multiple font files, this function returns the large ascent and descent that are enough for drawing all font files. The context range is used for shaping context. Some script, e.g. Arabic or Devanagari, changes letter shape based on its location or surrounding characters.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): a text to be measured. This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a starting offset in the text. Value is 0 or greater |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a length of the text to be measured. Value is 0 or greater |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a context starting offset in the text. Value is 0 or greater |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a length of the context to be used. Value is 0 or greater |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if measuring on RTL context, otherwise false. |
| --- | --- |
| `outMetrics` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md): the output font metrics. This value cannot be `null`. |

### getFontMetricsInt

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontMetricsInt(
    text: CharSequence, 
    start: Int, 
    count: Int, 
    contextStart: Int, 
    contextCount: Int, 
    isRtl: Boolean, 
    outMetrics: Paint.FontMetricsInt
): Unit
```

Returns the font metrics value for the given text. If the text is rendered with multiple font files, this function returns the large ascent and descent that are enough for drawing all font files. The context range is used for shaping context. Some script, e.g. Arabic or Devanagari, changes letter shape based on its location or surrounding characters.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): a text to be measured. This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a starting offset in the text. Value is 0 or greater |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a length of the text to be measured. Value is 0 or greater |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a context starting offset in the text. Value is 0 or greater |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a length of the context to be used. Value is 0 or greater |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if measuring on RTL context, otherwise false. |
| --- | --- |
| `outMetrics` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md): the output font metrics. This value cannot be `null`. |

### getFontMetricsIntForLocale

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontMetricsIntForLocale(metrics: Paint.FontMetricsInt): Unit
```

Get the font metrics used for the locale Obtain the metrics of the font that is used for the specified locale by `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextLocales(android.os.LocaleList)`. If multiple locales are specified, the minimum ascent and maximum descent will be set. This API is useful for determining the default line height of the empty text field, e.g. `https://developer.android.com/reference/kotlin/android/widget/EditText.html#`. Note, if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface` is created from the custom font files, its metrics are reserved, i.e. the ascent will be the custom font's ascent or smaller, the descent will be the custom font's descent or larger. Note, if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface` is a system fallback, e.g. `https://developer.android.com/reference/kotlin/android/graphics/Typeface#SERIF:android.graphics.Typeface`, the default font's metrics are reserved, i.e. the ascent will be the serif font's ascent or smaller, the descent will be the serif font's descent or larger.

| Parameters ||
|---|---|
| `metrics` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md): an output parameter. All members will be set by calling this function. This value cannot be `null`. |

### getFontSpacing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontSpacing(): Float
```

Return the recommend line spacing based on the current typeface and text size.

Note that this is the value for the main typeface, and actual text rendered may need a larger value because fallback fonts may get used in rendering the text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | recommend line spacing based on the current typeface and text size. |

### getFontVariationOverride

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontVariationOverride(): String?
```

Gets the current font variation override value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | a current font variation override value. This value may be `null`. |

### getFontVariationSettings

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFontVariationSettings(): String!
```

Returns the font variation settings.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the paint's currently set font variation settings. Default is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFontVariationSettings(kotlin.String)`

### getHinting

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHinting(): Int
```

Return the paint's hinting mode. Returns either `https://developer.android.com/reference/kotlin/android/graphics/Paint#HINTING_OFF:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/graphics/Paint#HINTING_ON:kotlin.Int`.

### getLetterSpacing

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLetterSpacing(): Float
```

Return the paint's letter-spacing for text. The default value is 0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the paint's letter-spacing for drawing text. |

### getMaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaskFilter(): MaskFilter!
```

Get the paint's maskfilter object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/MaskFilter!` | the paint's maskfilter (or null) |

### getOffsetForAdvance

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOffsetForAdvance(
    text: CharArray!, 
    start: Int, 
    end: Int, 
    contextStart: Int, 
    contextEnd: Int, 
    isRtl: Boolean, 
    advance: Float
): Int
```

Get the character offset within the string whose position is closest to the specified horizontal position.

The returned value is generally the value of `offset` for which #getRunAdvance yields a result most closely approximating `advance`, and which is also on a grapheme cluster boundary. As such, it is the preferred method for positioning a cursor in response to a touch or pointer event. The grapheme cluster boundaries are based on [Unicode Standard Annex #29](http://unicode.org/reports/tr29/) but with some tailoring for better user experience.

Note that `advance` is a (generally positive) width measurement relative to the start of the run. Thus, for RTL runs it the distance from the point to the right edge.

All indices are relative to the start of `text`. Further, `0 <= contextStart <= start <= end <= contextEnd <= text.length` must hold on entry, and `start <= result <= end` will hold on return.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the range to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the range to measure |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the range to measure |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| --- | --- |
| `advance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): width relative to start of run |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of offset |

### getOffsetForAdvance

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOffsetForAdvance(
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    contextStart: Int, 
    contextEnd: Int, 
    isRtl: Boolean, 
    advance: Float
): Int
```

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the range to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the range to measure |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the range to measure |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| --- | --- |
| `advance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): width relative to start of run |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of offset |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getOffsetForAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float)`

### getPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPathEffect(): PathEffect!
```

Get the paint's patheffect object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/PathEffect!` | the paint's patheffect (or null) |

### getRunAdvance

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRunAdvance(
    text: CharArray!, 
    start: Int, 
    end: Int, 
    contextStart: Int, 
    contextEnd: Int, 
    isRtl: Boolean, 
    offset: Int
): Float
```

Measure cursor position within a run of text.

The run of text includes the characters from `start` to `end` in the text. In addition, the range `contextStart` to `contextEnd` is used as context for the purpose of complex text shaping, such as Arabic text potentially shaped differently based on the text next to it.

All text outside the range `contextStart..contextEnd` is ignored. The text between `start` and `end` will be laid out to be measured.

The returned width measurement is the advance from `start` to `offset`. It is generally a positive value, no matter the direction of the run. If `offset == end`, the return value is simply the width of the whole run from `start` to `end`.

Ligatures are formed for characters in the range `start..end` (but not for `start..contextStart` or `end..contextEnd`). If `offset` points to a character in the middle of such a formed ligature, but at a grapheme cluster boundary, the return value will also reflect an advance in the middle of the ligature. See #getOffsetForAdvance for more discussion of grapheme cluster boundaries.

The direction of the run is explicitly specified by `isRtl`. Thus, this method is suitable only for runs of a single direction.

All indices are relative to the start of `text`. Further, `0 <= contextStart <= start <= offset <= end <= contextEnd <= text.length` must hold on entry.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the range to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the range to measure |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the shaping context |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| --- | --- |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of caret position |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | width measurement between start and offset |

### getRunAdvance

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRunAdvance(
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    contextStart: Int, 
    contextEnd: Int, 
    isRtl: Boolean, 
    offset: Int
): Float
```

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the range to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the range to measure |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the shaping context |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| --- | --- |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of caret position |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | width measurement between start and offset |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int)`

### getRunCharacterAdvance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRunCharacterAdvance(
    text: CharArray, 
    start: Int, 
    end: Int, 
    contextStart: Int, 
    contextEnd: Int, 
    isRtl: Boolean, 
    offset: Int, 
    advances: FloatArray?, 
    advancesIndex: Int
): Float
```

Measure the advance of each character within a run of text and also return the cursor position within the run.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start index of the range to measure, inclusive |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end index of the range to measure, exclusive |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start index of the shaping context, inclusive |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end index of the shaping context, exclusive |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| --- | --- |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of caret position |
| `advances` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: the array that receives the computed character advances. This value may be `null`. |
| `advancesIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start index from which the advances array is filled |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | width measurement between start and offset |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if a) contextStart or contextEnd is out of array's range or contextStart is larger than contextEnd, b) start or end is not within the range \[contextStart, contextEnd), or start is larger than end, c) offset is not within the range \[start, end), d) advances.length - advanceIndex is smaller than the length of the run, which equals to end - start. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int)`

### getRunCharacterAdvance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRunCharacterAdvance(
    text: CharSequence, 
    start: Int, 
    end: Int, 
    contextStart: Int, 
    contextEnd: Int, 
    isRtl: Boolean, 
    offset: Int, 
    advances: FloatArray?, 
    advancesIndex: Int
): Float
```

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the range to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the range to measure |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the start of the shaping context |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index + 1 of the end of the shaping context |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| --- | --- |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of caret position |
| `advances` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: the array that receives the computed character advances. This value may be `null`. |
| `advancesIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start index from which the advances array is filled |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | width measurement between start and offset |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if a) contextStart or contextEnd is out of array's range or contextStart is larger than contextEnd, b) start or end is not within the range \[contextStart, contextEnd), or end is larger than start, c) offset is not within the range \[start, end), d) advances.length - advanceIndex is smaller than the run length, which equals to end - start. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getRunCharacterAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)`

### getShader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShader(): Shader!
```

Get the paint's shader object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Shader!` | the paint's shader (or null) |

### getShadowLayerColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShadowLayerColor(): Int
```

Returns the color of the shadow layer.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Long)`

### getShadowLayerColorLong

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShadowLayerColorLong(): Long
```

Returns the color of the shadow layer.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the shadow layer's color encoded as a `ColorLong`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Long)`
- `https://developer.android.com/reference/kotlin/android/graphics/Color`

### getShadowLayerDx

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShadowLayerDx(): Float
```

Returns the x offset of the shadow layer.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Long)`

### getShadowLayerDy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShadowLayerDy(): Float
```

Returns the y offset of the shadow layer.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Long)`

### getShadowLayerRadius

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShadowLayerRadius(): Float
```

Returns the blur radius of the shadow layer.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Long)`

### getStartHyphenEdit

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStartHyphenEdit(): Int
```

Get the current value of start hyphen edit. The default value is 0 which is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_NO_EDIT:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current starting hyphen edit value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_NO_EDIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_INSERT_ZWJ:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStartHyphenEdit(kotlin.Int)`

### getStrikeThruPosition

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStrikeThruPosition(): Float
```

Distance from top of the strike-through line to the baseline in pixels. The result is negative for positions that are above the baseline. This method returns where the strike-through line should be drawn independent of if the `https://developer.android.com/reference/kotlin/android/graphics/Paint#STRIKE_THRU_TEXT_FLAG:kotlin.Int` bit is set. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the position of the strike-through line in pixels. The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrikeThruThickness()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStrikeThruText(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#isStrikeThruText()`

### getStrikeThruThickness

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStrikeThruThickness(): Float
```

Returns the thickness of the strike-through line in pixels. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the position of the strike-through line in pixels. The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrikeThruPosition()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStrikeThruText(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#isStrikeThruText()`

### getStrokeCap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStrokeCap(): Paint.Cap!
```

Return the paint's Cap, controlling how the start and end of stroked lines and paths are treated.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Paint.Cap!` | the line cap style for the paint, used whenever the paint's style is Stroke or StrokeAndFill. |

### getStrokeJoin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStrokeJoin(): Paint.Join!
```

Return the paint's stroke join type.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Paint.Join!` | the paint's Join. |

### getStrokeMiter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStrokeMiter(): Float
```

Return the paint's stroke miter value. Used to control the behavior of miter joins when the joins angle is sharp.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the paint's miter limit, used whenever the paint's style is Stroke or StrokeAndFill. |

### getStrokeWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStrokeWidth(): Float
```

Return the width for stroking.

<br />

A value of 0 strokes in hairline mode. Hairlines always draws a single pixel independent of the canvas's matrix.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the paint's stroke width, used whenever the paint's style is Stroke or StrokeAndFill. |

### getStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStyle(): Paint.Style!
```

Return the paint's style, used for controlling how primitives' geometries are interpreted (except for drawBitmap, which always assumes FILL_STYLE).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Paint.Style!` | the paint's style setting (Fill, Stroke, StrokeAndFill) |

### getTextAlign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextAlign(): Paint.Align!
```

Return the paint's Align value for drawing text. This controls how the text is positioned relative to its origin. LEFT align means that all of the text will be drawn to the right of its origin (i.e. the origin specifies the LEFT edge of the text) and so on.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Paint.Align!` | the paint's Align value for drawing text. |

### getTextBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextBounds(
    text: CharArray!, 
    index: Int, 
    count: Int, 
    bounds: Rect!
): Unit
```

Return in bounds (allocated by the caller) the smallest rectangle that encloses all of the characters, with an implied origin at (0,0).

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: array of chars to measure and return their unioned bounds |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the first char in the array to measure |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of chars, beginning at index, to measure |
| --- | --- |
| `bounds` | [Rect](Rect.md)!: returns the unioned bounds of all the text. Must be allocated by the caller |

### getTextBounds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextBounds(
    text: CharSequence, 
    start: Int, 
    end: Int, 
    bounds: Rect
): Unit
```

Retrieve the text boundary box and store to bounds. Return in bounds (allocated by the caller) the smallest rectangle that encloses all of the characters, with an implied origin at (0,0). Note that styles are ignored even if you pass `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` instance. Use `https://developer.android.com/reference/kotlin/android/text/StaticLayout.html#` for measuring bounds of `https://developer.android.com/reference/kotlin/android/text/Spanned.html#`.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): text to measure and return its bounds. This value cannot be `null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the first char in the text to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): 1 past the last char in the text to measure |
| --- | --- |
| `bounds` | [Rect](Rect.md): returns the unioned bounds of all the text. Must be allocated by the caller. This value cannot be `null`. |

### getTextBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextBounds(
    text: String!, 
    start: Int, 
    end: Int, 
    bounds: Rect!
): Unit
```

Retrieve the text boundary box and store to bounds. Return in bounds (allocated by the caller) the smallest rectangle that encloses all of the characters, with an implied origin at (0,0).

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: string to measure and return its bounds |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the first char in the string to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): 1 past the last char in the string to measure |
| --- | --- |
| `bounds` | [Rect](Rect.md)!: returns the unioned bounds of all the text. Must be allocated by the caller |

### getTextLocale

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextLocale(): Locale
```

Get the text's primary Locale. Note that this is not all of the locale-related information Paint has. Use `https://developer.android.com/reference/kotlin/android/graphics/Paint#getTextLocales()` to get the complete list.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale.html#` | the paint's primary Locale used for drawing text, never null. |

### getTextLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextLocales(): LocaleList
```

Get the text locale list.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/LocaleList.html#` | the paint's LocaleList used for drawing text, never null or empty. |

### getTextPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextPath(
    text: CharArray!, 
    index: Int, 
    count: Int, 
    x: Float, 
    y: Float, 
    path: Path!
): Unit
```

Return the path (outline) for the specified text. Note: just like Canvas.drawText, this will respect the Align setting in the paint.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the text to retrieve the path from |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first character in text |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of characters starting with index |
| --- | --- |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the x coordinate of the text's origin |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the y coordinate of the text's origin |
| `path` | [Path](Path.md)!: the path to receive the data describing the text. Must be allocated by the caller |
| --- | --- |

### getTextPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextPath(
    text: String!, 
    start: Int, 
    end: Int, 
    x: Float, 
    y: Float, 
    path: Path!
): Unit
```

Return the path (outline) for the specified text. Note: just like Canvas.drawText, this will respect the Align setting in the paint.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text to retrieve the path from |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first character in the text |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): 1 past the last character in the text |
| --- | --- |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the x coordinate of the text's origin |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the y coordinate of the text's origin |
| `path` | [Path](Path.md)!: the path to receive the data describing the text. Must be allocated by the caller |
| --- | --- |

### getTextRunAdvances

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextRunAdvances(
    chars: CharArray, 
    index: Int, 
    count: Int, 
    contextIndex: Int, 
    contextCount: Int, 
    isRtl: Boolean, 
    advances: FloatArray?, 
    advancesIndex: Int
): Float
```

Retrieve the character advances of the text. Returns the total advance width for the characters in the run from `index` for `count` of chars, and if `advances` is not null, the advance assigned to each of these characters (java chars).

The trailing surrogate in a valid surrogate pair is assigned an advance of 0. Thus the number of returned advances is always equal to count, not to the number of unicode codepoints represented by the run.

In the case of conjuncts or combining marks, the total advance is assigned to the first logical character, and the following characters are assigned an advance of 0.

This generates the sum of the advances of glyphs for characters in a reordered cluster as the width of the first logical character in the cluster, and 0 for the widths of all other characters in the cluster. In effect, such clusters are treated like conjuncts.

The shaping bounds limit the amount of context available outside start and end that can be used for shaping analysis. These bounds typically reflect changes in bidi level or font metrics across which shaping does not occur.

| Parameters ||
|---|---|
| `chars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the text to measure. This value cannot be `null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first character to measure. Value is 0 or greater |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of characters to measure. Value is 0 or greater |
| --- | --- |
| `contextIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first character to use for shaping context. Context must cover the measureing target. Value is 0 or greater |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of character to use for shaping context. Context must cover the measureing target. Value is 0 or greater |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the run is in RTL direction |
| --- | --- |
| `advances` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: array to receive the advances, must have room for all advances. This can be null if only total advance is needed |
| `advancesIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position in advances at which to put the advance corresponding to the character at start. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the total advance in pixels |

### getTextRunCursor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextRunCursor(
    text: CharArray, 
    contextStart: Int, 
    contextLength: Int, 
    isRtl: Boolean, 
    offset: Int, 
    cursorOpt: Int
): Int
```

Returns the next cursor position in the run. This avoids placing the cursor between surrogates, between characters that form conjuncts, between base characters and combining marks, or within a reordering cluster.

ContextStart and offset are relative to the start of text. The context is the shaping context for cursor movement, generally the bounds of the metric span enclosing the cursor in the direction of movement.

If cursorOpt is `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT:kotlin.Int` and the offset is not a valid cursor position, this returns -1. Otherwise this will never return a value before contextStart or after contextStart + contextLength.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the text. This value cannot be `null`. |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the context. Value is 0 or greater |
| `contextLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the context. Value is 0 or greater |
| --- | --- |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the paragraph context is RTL, otherwise false |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cursor position to move from. Value is 0 or greater |
| `cursorOpt` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): how to move the cursor. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AFTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT_OR_AFTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_BEFORE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT_OR_BEFORE:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset of the next position, or -1 |

### getTextRunCursor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextRunCursor(
    text: CharSequence, 
    contextStart: Int, 
    contextEnd: Int, 
    isRtl: Boolean, 
    offset: Int, 
    cursorOpt: Int
): Int
```

Returns the next cursor position in the run. This avoids placing the cursor between surrogates, between characters that form conjuncts, between base characters and combining marks, or within a reordering cluster.

ContextStart, contextEnd, and offset are relative to the start of text. The context is the shaping context for cursor movement, generally the bounds of the metric span enclosing the cursor in the direction of movement.

If cursorOpt is `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT:kotlin.Int` and the offset is not a valid cursor position, this returns -1. Otherwise this will never return a value before contextStart or after contextEnd.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the text. This value cannot be `null`. |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start of the context. Value is 0 or greater |
| `contextEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end of the context. Value is 0 or greater |
| --- | --- |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the paragraph context is RTL, otherwise false |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cursor position to move from. Value is 0 or greater |
| `cursorOpt` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): how to move the cursor. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AFTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT_OR_AFTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_BEFORE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#CURSOR_AT_OR_BEFORE:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset of the next position, or -1 |

### getTextScaleX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextScaleX(): Float
```

Return the paint's horizontal scale factor for text. The default value is 1.0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the paint's scale factor in X for drawing/measuring text |

### getTextSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextSize(): Float
```

Return the paint's text size.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the paint's text size in pixel units. |

### getTextSkewX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextSkewX(): Float
```

Return the paint's horizontal skew factor for text. The default value is 0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the paint's skew factor in X for drawing text. |

### getTextWidths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextWidths(
    text: CharArray!, 
    index: Int, 
    count: Int, 
    widths: FloatArray!
): Int
```

Return the advance widths for the characters in the string.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The text to measure. Cannot be null. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first char to to measure |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of chars starting with index to measure |
| --- | --- |
| `widths` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: array to receive the advance widths of the characters. Must be at least a large as count. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the actual number of widths returned. |

### getTextWidths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextWidths(
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    widths: FloatArray!
): Int
```

Return the advance widths for the characters in the string.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first char to to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The end of the text slice to measure |
| --- | --- |
| `widths` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: array to receive the advance widths of the characters. Must be at least a large as (end - start). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the actual number of widths returned. |

### getTextWidths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextWidths(
    text: String!, 
    widths: FloatArray!
): Int
```

Return the advance widths for the characters in the string.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text to measure |
| `widths` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: array to receive the advance widths of the characters. Must be at least a large as the text. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of code units in the specified text. |

### getTextWidths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextWidths(
    text: String!, 
    start: Int, 
    end: Int, 
    widths: FloatArray!
): Int
```

Return the advance widths for the characters in the string.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first char to to measure |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The end of the text slice to measure |
| --- | --- |
| `widths` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: array to receive the advance widths of the characters. Must be at least a large as the text. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of code units in the specified text. |

### getTypeface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTypeface(): Typeface!
```

Get the paint's typeface object.

<br />

The typeface object identifies which font to use when drawing or measuring text.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Typeface!` | the paint's typeface (or null) |

### getUnderlinePosition

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUnderlinePosition(): Float
```

Returns the distance from top of the underline to the baseline in pixels. The result is positive for positions that are below the baseline. This method returns where the underline should be drawn independent of if the `https://developer.android.com/reference/kotlin/android/graphics/Paint#UNDERLINE_TEXT_FLAG:kotlin.Int` bit is set. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the position of the underline in pixels. The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#isUnderlineText()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getUnderlineThickness()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setUnderlineText(kotlin.Boolean)`

### getUnderlineThickness

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUnderlineThickness(): Float
```

Returns the thickness of the underline in pixels. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the thickness of the underline in pixels. The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#isUnderlineText()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getUnderlinePosition()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setUnderlineText(kotlin.Boolean)`

### getWordSpacing

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWordSpacing(): Float
```

Return the paint's extra word-spacing for text. The default value is 0. 
The units of this value are pixels.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the paint's extra word-spacing for drawing text in pixels. The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setWordSpacing(kotlin.Float)`

### getXfermode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getXfermode(): Xfermode!
```

Get the paint's transfer mode object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Xfermode!` | the paint's transfer mode (or null) |

### hasGlyph

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasGlyph(string: String!): Boolean
```

Determine whether the typeface set on the paint has a glyph supporting the string. The simplest case is when the string contains a single character, in which this method determines whether the font has the character. In the case of multiple characters, the method returns true if there is a single glyph representing the ligature. For example, if the input is a pair of regional indicator symbols, determine whether there is an emoji flag for the pair.

Finally, if the string contains a variation selector, the method only returns true if the fonts contains a glyph specific to that variation.

Checking is done on the entire fallback chain, not just the immediate font referenced.

| Parameters ||
|---|---|
| `string` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string to test whether there is glyph support |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the typeface has a glyph for the string |

### isAntiAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAntiAlias(): Boolean
```

Helper for getFlags(), returning true if ANTI_ALIAS_FLAG bit is set AntiAliasing smooths out the edges of what is being drawn, but is has no impact on the interior of the shape. See setDither() and setFilterBitmap() to affect how colors are treated.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the antialias bit is set in the paint's flags. |

### isDither

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDither(): Boolean
```

Helper for getFlags(), returning true if DITHER_FLAG bit is set Dithering affects how colors that are higher precision than the device are down-sampled. No dithering is generally faster, but higher precision colors are just truncated down (e.g. 8888 -\> 565). Dithering tries to distribute the error inherent in this process, to reduce the visual artifacts.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the dithering bit is set in the paint's flags. |

### isElegantTextHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isElegantTextHeight(): Boolean
```

**Deprecated:** *The underlying UI fonts are deprecated and will be removed from the system image. Applications supporting scripts with large vertical metrics should adapt their UI by using fonts designed with corresponding vertical metrics.*

Get the elegant metrics flag. Note: For applications target API 35 or later, this function returns true by default. For applications target API 36 or later, the function call will be ignored and the elegant text height is always enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if elegant metrics are enabled for text drawing. |

### isFakeBoldText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFakeBoldText(): Boolean
```

Helper for getFlags(), returning true if FAKE_BOLD_TEXT_FLAG bit is set

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the fakeBoldText bit is set in the paint's flags. |

### isFilterBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFilterBitmap(): Boolean
```

Whether or not the bitmap filter is activated. Filtering affects the sampling of bitmaps when they are transformed. Filtering does not affect how the colors in the bitmap are converted into device pixels. That is dependent on dithering and xfermodes.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFilterBitmap(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#FILTER_BITMAP_FLAG:kotlin.Int`

### isLinearText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLinearText(): Boolean
```

Helper for getFlags(), returning true if LINEAR_TEXT_FLAG bit is set

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the lineartext bit is set in the paint's flags |

### isStrikeThruText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isStrikeThruText(): Boolean
```

Helper for getFlags(), returning true if STRIKE_THRU_TEXT_FLAG bit is set

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the `https://developer.android.com/reference/kotlin/android/graphics/Paint#STRIKE_THRU_TEXT_FLAG:kotlin.Int` bit is set in the paint's flags. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrikeThruPosition()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrikeThruThickness()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setStrikeThruText(kotlin.Boolean)`

### isSubpixelText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSubpixelText(): Boolean
```

Helper for getFlags(), returning true if SUBPIXEL_TEXT_FLAG bit is set

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the subpixel bit is set in the paint's flags |

### isUnderlineText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUnderlineText(): Boolean
```

Helper for getFlags(), returning true if UNDERLINE_TEXT_FLAG bit is set

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the underlineText bit is set in the paint's flags. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getUnderlinePosition()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getUnderlineThickness()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setUnderlineText(kotlin.Boolean)`

### measureText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun measureText(
    text: CharArray!, 
    index: Int, 
    count: Int
): Float
```

Return the width of the text.

| Parameters ||
|---|---|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The text to measure. Cannot be null. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character to start measuring |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): THe number of characters to measure, beginning with start |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The width of the text |

### measureText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun measureText(
    text: CharSequence!, 
    start: Int, 
    end: Int
): Float
```

Return the width of the text.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text to measure |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character to start measuring |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): 1 beyond the index of the last character to measure |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The width of the text |

### measureText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun measureText(text: String!): Float
```

Return the width of the text.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text to measure. Cannot be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The width of the text |

### measureText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun measureText(
    text: String!, 
    start: Int, 
    end: Int
): Float
```

Return the width of the text.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text to measure. Cannot be null. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character to start measuring |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): 1 beyond the index of the last character to measure |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The width of the text |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Restores the paint to its default settings.

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(src: Paint!): Unit
```

Copy the fields from src into this paint. This is equivalent to calling get() on all of the src fields, and calling the corresponding set() methods on this.

### setARGB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setARGB(
    a: Int, 
    r: Int, 
    g: Int, 
    b: Int
): Unit
```

Helper to setColor(), that takes a,r,g,b and constructs the color int

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new alpha component (0..255) of the paint's color. |
| `r` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new red component (0..255) of the paint's color. |
| `g` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new green component (0..255) of the paint's color. |
| --- | --- |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new blue component (0..255) of the paint's color. |

### setAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAlpha(a: Int): Unit
```

Helper to setColor(), that only assigns the color's alpha value, leaving its r,g,b values unchanged. Results are undefined if the alpha value is outside of the range \[0..255\]

| Parameters ||
|---|---|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): set the alpha component \[0..255\] of the paint's color. |

### setAntiAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAntiAlias(aa: Boolean): Unit
```

Helper for setFlags(), setting or clearing the ANTI_ALIAS_FLAG bit AntiAliasing smooths out the edges of what is being drawn, but is has no impact on the interior of the shape. See setDither() and setFilterBitmap() to affect how colors are treated.

| Parameters ||
|---|---|
| `aa` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the antialias bit in the flags, false to clear it |

### setBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBlendMode(blendmode: BlendMode?): Unit
```

Set or clear the blend mode. A blend mode defines how source pixels (generated by a drawing command) are composited with the destination pixels (content of the render target).

<br />

Pass null to clear any previous blend mode.

<br />

| Parameters ||
|---|---|
| `blendmode` | [BlendMode](BlendMode.md)?: May be null. The blend mode to be installed in the paint |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/BlendMode`

### setColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColor(color: Int): Unit
```

Set the paint's color. Note that the color is an int containing alpha as well as r,g,b. This 32bit value is not premultiplied, meaning that its alpha can be any value, regardless of the values of r,g,b. See the Color class for more details.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new color (including alpha) to set in the paint. |

### setColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColor(color: Long): Unit
```

Set the paint's color with a `ColorLong`. Note that the color is a long with an encoded `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace` as well as alpha and r,g,b. These values are not premultiplied, meaning that alpha can be any value, regardless of the values of r,g,b. See the `https://developer.android.com/reference/kotlin/android/graphics/Color` class for more details.

| Parameters ||
|---|---|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The new color (including alpha and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace`) to set in the paint. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the color space encoded in the `ColorLong` is invalid or unknown. |

### setColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorFilter(filter: ColorFilter!): ColorFilter!
```

Set or clear the paint's colorfilter, returning the parameter.

| Parameters ||
|---|---|
| `filter` | [ColorFilter](ColorFilter.md)!: May be null. The new filter to be installed in the paint |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorFilter!` | filter |

### setDither

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDither(dither: Boolean): Unit
```

Helper for setFlags(), setting or clearing the DITHER_FLAG bit Dithering affects how colors that are higher precision than the device are down-sampled. No dithering is generally faster, but higher precision colors are just truncated down (e.g. 8888 -\> 565). Dithering tries to distribute the error inherent in this process, to reduce the visual artifacts.

| Parameters ||
|---|---|
| `dither` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the dithering bit in flags, false to clear it |

### setElegantTextHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setElegantTextHeight(elegant: Boolean): Unit
```

**Deprecated:** *This API will be no-op at some point in the future. The underlying UI fonts is deprecated and will be removed from the system image. Applications supporting scripts with large vertical metrics should adapt their UI by using fonts designed with corresponding vertical metrics.*

Set the paint's elegant height metrics flag. This setting selects font variants that have not been compacted to fit Latin-based vertical metrics, and also increases top and bottom bounds to provide more space.

Note: For applications target API 35 or later, the default value will be true by default. For applications target API 36 or later, the function call will be ignored and the elegant text height is always enabled.

| Parameters ||
|---|---|
| `elegant` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set the paint's elegant metrics flag for drawing text. |

### setEndHyphenEdit

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEndHyphenEdit(endHyphen: Int): Unit
```

Set a end hyphen edit on the paint. By setting end hyphen edit, the measurement and drawing is performed with modifying hyphenation at the end of line. For example, by passing `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` like as follows, HYPHEN(U+2010) character is appended at the end of line.

```kotlin
<code>
    Paint paint = new Paint();
    paint.setEndHyphenEdit(Paint.END_HYPHEN_EDIT_INSERT_HYPHEN);
    paint.measureText("abc", 0, 3);  // Returns the width of "abc-"
    Canvas.drawText("abc", 0, 3, 0f, 0f, paint);  // Draws "abc-"
  </code>
```
The default value is 0 which is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_NO_EDIT:kotlin.Int`.

<br />

| Parameters ||
|---|---|
| `endHyphen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a end hyphen edit value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_NO_EDIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_REPLACE_WITH_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_ARMENIAN_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_MAQAF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_UCAS_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#END_HYPHEN_EDIT_INSERT_ZWJ_AND_HYPHEN:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getEndHyphenEdit()`

### setFakeBoldText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFakeBoldText(fakeBoldText: Boolean): Unit
```

Helper for setFlags(), setting or clearing the FAKE_BOLD_TEXT_FLAG bit

| Parameters ||
|---|---|
| `fakeBoldText` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the fakeBoldText bit in the paint's flags, false to clear it. |

### setFilterBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFilterBitmap(filter: Boolean): Unit
```

Helper for setFlags(), setting or clearing the FILTER_BITMAP_FLAG bit. Filtering affects the sampling of bitmaps when they are transformed. Filtering does not affect how the colors in the bitmap are converted into device pixels. That is dependent on dithering and xfermodes.

| Parameters ||
|---|---|
| `filter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the FILTER_BITMAP_FLAG bit in the paint's flags, false to clear it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#FILTER_BITMAP_FLAG:kotlin.Int`

### setFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFlags(flags: Int): Unit
```

Set the paint's flags. Use the Flag enum to specific flag values.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new flag bits for the paint. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Paint#ANTI_ALIAS_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#FILTER_BITMAP_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#DITHER_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#UNDERLINE_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#STRIKE_THRU_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#FAKE_BOLD_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#LINEAR_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#SUBPIXEL_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#EMBEDDED_BITMAP_TEXT_FLAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` |

### setFontFeatureSettings

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFontFeatureSettings(settings: String!): Unit
```

Set font feature settings. The format is the same as the CSS font-feature-settings attribute: <https://www.w3.org/TR/css-fonts-3/#font-feature-settings-prop>

| Parameters ||
|---|---|
| `settings` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the font feature settings string to use, may be null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontFeatureSettings()`

### setFontVariationOverride

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFontVariationOverride(fontVariationOverride: String?): Unit
```

Sets TrueType or OpenType font variation settings for overriding. The settings string is constructed from multiple pairs of axis tag and style values. The axis tag must contain four ASCII characters and must be wrapped with single quotes (U+0027) or double quotes (U+0022). Axis strings that are longer or shorter than four characters, or contain characters outside of U+0020..U+007E are invalid. If invalid font variation settings is provided, this method does nothing and returning false with printing error message to the logcat. Different from `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFontVariationSettings(kotlin.String)`, this overrides the font variation settings which is already assigned to the font instance. For example, if the underlying font is configured as `'wght' 500, 'ital' 1`, and if the override is specified as ``'wght' 700, `wdth` 150``, then the effective font variation setting is `` `wght' 700, 'ital' 1, 'wdth' 150 ``. The \`wght\` value is updated by override, 'ital' value is preserved because no overrides, and \`wdth\` value is added by override. If the font variation override is empty or null, nothing overrides and original font variation settings assigned to the font instance is used as it is.

| Parameters ||
|---|---|
| `fontVariationOverride` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: font variation override. You can pass null or empty string for clearing font variation override. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If given string is not a valid font variation settings format |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontVariationSettings()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#setFontVariationSettings(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontVariationOverride()`
- `https://developer.android.com/reference/kotlin/android/graphics/fonts/FontVariationAxis`

### setFontVariationSettings

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFontVariationSettings(fontVariationSettings: String!): Boolean
```

Sets TrueType or OpenType font variation settings. The settings string is constructed from multiple pairs of axis tag and style values. The axis tag must contain four ASCII characters and must be wrapped with single quotes (U+0027) or double quotes (U+0022). Axis strings that are longer or shorter than four characters, or contain characters outside of U+0020..U+007E are invalid. If a specified axis name is not defined in the font, the settings will be ignored. Examples,

- Set font width to 150.

  ```kotlin
  <code>
      Paint paint = new Paint();
      paint.setFontVariationSettings("'wdth' 150");
    </code>
  ```
- Set the font slant to 20 degrees and ask for italic style.

  ```kotlin
  <code>
      Paint paint = new Paint();
      paint.setFontVariationSettings("'slnt' 20, 'ital' 1");
    </code>
  ```

<br />

| Parameters ||
|---|---|
| `fontVariationSettings` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: font variation settings. You can pass null or empty string as no variation settings. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given settings is effective to at least one font file underlying this typeface. This function also returns true for empty settings string. Otherwise returns false |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If given string is not a valid font variation settings format |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getFontVariationSettings()`
- `https://developer.android.com/reference/kotlin/android/graphics/fonts/FontVariationAxis`

### setHinting

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHinting(mode: Int): Unit
```

Set the paint's hinting mode. May be either `https://developer.android.com/reference/kotlin/android/graphics/Paint#HINTING_OFF:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/graphics/Paint#HINTING_ON:kotlin.Int`.

### setLetterSpacing

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLetterSpacing(letterSpacing: Float): Unit
```

Set the paint's letter-spacing for text. The default value is 0. The value is in 'EM' units. Typical values for slight expansion will be around 0.05. Negative values tighten text.

| Parameters ||
|---|---|
| `letterSpacing` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): set the paint's letter-spacing for drawing text. |

### setLinearText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLinearText(linearText: Boolean): Unit
```

Helper for setFlags(), setting or clearing the LINEAR_TEXT_FLAG bit

| Parameters ||
|---|---|
| `linearText` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the linearText bit in the paint's flags, false to clear it. |

### setMaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaskFilter(maskfilter: MaskFilter!): MaskFilter!
```

Set or clear the maskfilter object.

<br />

Pass null to clear any previous maskfilter. As a convenience, the parameter passed is also returned.

| Parameters ||
|---|---|
| `maskfilter` | [MaskFilter](MaskFilter.md)!: May be null. The maskfilter to be installed in the paint |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/MaskFilter!` | maskfilter |

### setPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPathEffect(effect: PathEffect!): PathEffect!
```

Set or clear the patheffect object.

<br />

Pass null to clear any previous patheffect. As a convenience, the parameter passed is also returned.

| Parameters ||
|---|---|
| `effect` | [PathEffect](PathEffect.md)!: May be null. The patheffect to be installed in the paint |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/PathEffect!` | effect |

### setShader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShader(shader: Shader!): Shader!
```

Set or clear the shader object.

<br />

Pass null to clear any previous shader. As a convenience, the parameter passed is also returned.

| Parameters ||
|---|---|
| `shader` | [Shader](Shader.md)!: May be null. the new shader to be installed in the paint |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Shader!` | shader |

### setShadowLayer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShadowLayer(
    radius: Float, 
    dx: Float, 
    dy: Float, 
    shadowColor: Int
): Unit
```

This draws a shadow layer below the main layer, with the specified offset and color, and blur radius. If radius is 0, then the shadow layer is removed.

Can be used to create a blurred shadow underneath text. Support for use with other drawing operations is constrained to the software rendering pipeline.

The alpha of the shadow will be the paint's alpha if the shadow color is opaque, or the alpha from the shadow color if not.

### setShadowLayer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShadowLayer(
    radius: Float, 
    dx: Float, 
    dy: Float, 
    shadowColor: Long
): Unit
```

This draws a shadow layer below the main layer, with the specified offset and color, and blur radius. If radius is 0, then the shadow layer is removed.

Can be used to create a blurred shadow underneath text. Support for use with other drawing operations is constrained to the software rendering pipeline.

The alpha of the shadow will be the paint's alpha if the shadow color is opaque, or the alpha from the shadow color if not.

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the color space encoded in the `ColorLong` is invalid or unknown. |

### setStartHyphenEdit

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStartHyphenEdit(startHyphen: Int): Unit
```

Set a start hyphen edit on the paint. By setting start hyphen edit, the measurement and drawing is performed with modifying hyphenation at the start of line. For example, by passing `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` like as follows, HYPHEN(U+2010) character is appended at the start of line.

```kotlin
<code>
    Paint paint = new Paint();
    paint.setStartHyphenEdit(Paint.START_HYPHEN_EDIT_INSERT_HYPHEN);
    paint.measureText("abc", 0, 3);  // Returns the width of "-abc"
    Canvas.drawText("abc", 0, 3, 0f, 0f, paint);  // Draws "-abc"
  </code>
```
The default value is 0 which is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_NO_EDIT:kotlin.Int`.

<br />

| Parameters ||
|---|---|
| `startHyphen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a start hyphen edit value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_NO_EDIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Paint#START_HYPHEN_EDIT_INSERT_ZWJ:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStartHyphenEdit()`

### setStrikeThruText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStrikeThruText(strikeThruText: Boolean): Unit
```

Helper for setFlags(), setting or clearing the STRIKE_THRU_TEXT_FLAG bit

| Parameters ||
|---|---|
| `strikeThruText` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the strikeThruText bit in the paint's flags, false to clear it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrikeThruPosition()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getStrikeThruThickness()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#isStrikeThruText()`

### setStrokeCap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStrokeCap(cap: Paint.Cap!): Unit
```

Set the paint's Cap.

| Parameters ||
|---|---|
| `cap` | [Paint.Cap](../android/graphics/Paint.Cap.md)!: set the paint's line cap style, used whenever the paint's style is Stroke or StrokeAndFill. |

### setStrokeJoin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStrokeJoin(join: Paint.Join!): Unit
```

Set the paint's Join.

| Parameters ||
|---|---|
| `join` | [Paint.Join](../android/graphics/Paint.Join.md)!: set the paint's Join, used whenever the paint's style is Stroke or StrokeAndFill. |

### setStrokeMiter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStrokeMiter(miter: Float): Unit
```

Set the paint's stroke miter value. This is used to control the behavior of miter joins when the joins angle is sharp. This value must be \>= 0.

| Parameters ||
|---|---|
| `miter` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): set the miter limit on the paint, used whenever the paint's style is Stroke or StrokeAndFill. |

### setStrokeWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStrokeWidth(width: Float): Unit
```

Set the width for stroking. Pass 0 to stroke in hairline mode. Hairlines always draws a single pixel independent of the canvas's matrix.

| Parameters ||
|---|---|
| `width` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): set the paint's stroke width, used whenever the paint's style is Stroke or StrokeAndFill. |

### setStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStyle(style: Paint.Style!): Unit
```

Set the paint's style, used for controlling how primitives' geometries are interpreted (except for drawBitmap, which always assumes Fill).

| Parameters ||
|---|---|
| `style` | [Paint.Style](../android/graphics/Paint.Style.md)!: The new style to set in the paint |

### setSubpixelText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubpixelText(subpixelText: Boolean): Unit
```

Helper for setFlags(), setting or clearing the SUBPIXEL_TEXT_FLAG bit

| Parameters ||
|---|---|
| `subpixelText` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the subpixelText bit in the paint's flags, false to clear it. |

### setTextAlign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextAlign(align: Paint.Align!): Unit
```

Set the paint's text alignment. This controls how the text is positioned relative to its origin. LEFT align means that all of the text will be drawn to the right of its origin (i.e. the origin specifies the LEFT edge of the text) and so on.

| Parameters ||
|---|---|
| `align` | [Paint.Align](../android/graphics/Paint.Align.md)!: set the paint's Align value for drawing text. |

### setTextLocale

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextLocale(locale: Locale): Unit
```

Set the text locale list to a one-member list consisting of just the locale. See `https://developer.android.com/reference/kotlin/android/graphics/Paint#setTextLocales(android.os.LocaleList)` for how the locale list affects the way the text is drawn for some languages.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md): the paint's locale value for drawing text, must not be null. |

### setTextLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextLocales(locales: LocaleList): Unit
```

Set the text locale list. The text locale list affects how the text is drawn for some languages. For example, if the locale list contains `https://developer.android.com/reference/kotlin/java/util/Locale.html#CHINESE:java.util.Locale` or `https://developer.android.com/reference/kotlin/java/util/Locale.html#CHINA:java.util.Locale`, then the text renderer will prefer to draw text using a Chinese font. Likewise, if the locale list contains `https://developer.android.com/reference/kotlin/java/util/Locale.html#JAPANESE:java.util.Locale` or `https://developer.android.com/reference/kotlin/java/util/Locale.html#JAPAN:java.util.Locale`, then the text renderer will prefer to draw text using a Japanese font. If the locale list contains both, the order those locales appear in the list is considered for deciding the font. This distinction is important because Chinese and Japanese text both use many of the same Unicode code points but their appearance is subtly different for each language. By default, the text locale list is initialized to a one-member list just containing the system locales. This assumes that the text to be rendered will most likely be in the user's preferred language. If the actual language or languages of the text is/are known, then they can be provided to the text renderer using this method. The text renderer may attempt to guess the language script based on the contents of the text to be drawn independent of the text locale here. Specifying the text locales just helps it do a better job in certain ambiguous cases.

| Parameters ||
|---|---|
| `locales` | [LocaleList](../android.os/LocaleList.md): the paint's locale list for drawing text, must not be null or empty. |

### setTextScaleX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextScaleX(scaleX: Float): Unit
```

Set the paint's horizontal scale factor for text. The default value is 1.0. Values \> 1.0 will stretch the text wider. Values \< 1.0 will stretch the text narrower.

| Parameters ||
|---|---|
| `scaleX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): set the paint's scale in X for drawing/measuring text. |

### setTextSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextSize(textSize: Float): Unit
```

Set the paint's text size. This value must be \> 0

| Parameters ||
|---|---|
| `textSize` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): set the paint's text size in pixel units. |

### setTextSkewX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextSkewX(skewX: Float): Unit
```

Set the paint's horizontal skew factor for text. The default value is 0. For approximating oblique text, use values around -0.25.

| Parameters ||
|---|---|
| `skewX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): set the paint's skew factor in X for drawing text. |

### setTypeface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTypeface(typeface: Typeface!): Typeface!
```

Set or clear the typeface object.

<br />

Pass null to clear any previous typeface. As a convenience, the parameter passed is also returned.

| Parameters ||
|---|---|
| `typeface` | [Typeface](Typeface.md)!: May be null. The typeface to be installed in the paint |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Typeface!` | typeface |

### setUnderlineText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUnderlineText(underlineText: Boolean): Unit
```

Helper for setFlags(), setting or clearing the UNDERLINE_TEXT_FLAG bit

| Parameters ||
|---|---|
| `underlineText` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the underlineText bit in the paint's flags, false to clear it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#isUnderlineText()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getUnderlinePosition()`
- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getUnderlineThickness()`

### setWordSpacing

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWordSpacing(wordSpacing: Float): Unit
```

Set the paint's extra word-spacing for text. Increases the white space width between words with the given amount of pixels. The default value is 0.

| Parameters ||
|---|---|
| `wordSpacing` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): set the paint's extra word-spacing for drawing text in pixels. The units of this value are pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Paint#getWordSpacing()`

### setXfermode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setXfermode(xfermode: Xfermode!): Xfermode!
```

Set or clear the transfer mode object. A transfer mode defines how source pixels (generate by a drawing command) are composited with the destination pixels (content of the render target).

<br />

Pass null to clear any previous transfer mode. As a convenience, the parameter passed is also returned.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/PorterDuffXfermode` is the most common transfer mode.

| Parameters ||
|---|---|
| `xfermode` | [Xfermode](Xfermode.md)!: May be null. The xfermode to be installed in the paint |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Xfermode!` | xfermode |
