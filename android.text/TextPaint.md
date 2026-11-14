Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextPaint

```
open class TextPaint : Paint
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#) ||
| | ↳ | [android.text.TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint#) |

TextPaint is an extension of Paint that leaves room for some extra data used during text measuring and drawing.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#ANTI_ALIAS_FLAG:kotlin.Int`

Paint flag that enables antialiasing when drawing.

Enabling this flag will cause all draw operations that support antialiasing to use it.

Notable draw operations that do **not** support antialiasing include:

- `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#drawBitmapMesh(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int,%20android.graphics.Paint)`
- android.graphics.Canvas#drawPatch
- `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#drawVertices(android.graphics.Canvas.VertexMode,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.ShortArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#CURSOR_AFTER:kotlin.Int`

Option for getTextRunCursor. Compute the valid cursor after offset or the limit of the context, whichever is less.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#CURSOR_AT:kotlin.Int`

Option for getTextRunCursor. Return offset if the cursor at offset is valid, or -1 if it isn't.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#CURSOR_AT_OR_AFTER:kotlin.Int`

Option for getTextRunCursor. Compute the valid cursor at or after the offset or the limit of the context, whichever is less.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#CURSOR_AT_OR_BEFORE:kotlin.Int`

Option for getTextRunCursor. Compute the valid cursor at or before offset or the start of the context, whichever is greater.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#CURSOR_BEFORE:kotlin.Int`

Option for getTextRunCursor. Compute the valid cursor before offset or the start of the context, whichever is greater.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#DEV_KERN_TEXT_FLAG:kotlin.Int`

Legacy Paint flag, no longer used.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#DITHER_FLAG:kotlin.Int`

Paint flag that enables dithering when blitting.

Enabling this flag applies a dither to any blit operation where the target's colour space is more constrained than the source.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#EMBEDDED_BITMAP_TEXT_FLAG:kotlin.Int`

Paint flag that enables the use of bitmap fonts when drawing text.

Disabling this flag will prevent text draw operations from using embedded bitmap strikes in fonts, causing fonts with both scalable outlines and bitmap strikes to draw only the scalable outlines, and fonts with only bitmap strikes to not draw at all.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_INSERT_ARMENIAN_HYPHEN:kotlin.Int`

An integer representing the end of the line has Armentian hyphen (U+058A).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int`

An integer representing the end of the line has normal hyphen character (U+002D).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_INSERT_MAQAF:kotlin.Int`

An integer representing the end of the line has maqaf (Hebrew hyphen, U+05BE).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_INSERT_UCAS_HYPHEN:kotlin.Int`

An integer representing the end of the line has Canadian Syllabics hyphen (U+1400).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_INSERT_ZWJ_AND_HYPHEN:kotlin.Int`

An integer representing the end of the line has Zero-Width-Joiner (U+200D) followed by normal hyphen character (U+002D).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_NO_EDIT:kotlin.Int`

An integer representing the end of the line has no modification for hyphenation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_REPLACE_WITH_HYPHEN:kotlin.Int`

An integer representing the character at the end of the line is replaced with hyphen character (U+002D).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#FAKE_BOLD_TEXT_FLAG:kotlin.Int`

Paint flag that applies a synthetic bolding effect to drawn text.

Enabling this flag will cause text draw operations to apply a simulated bold effect when drawing a `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` that is not already bold.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#FILTER_BITMAP_FLAG:kotlin.Int`

Paint flag that enables bilinear sampling on scaled bitmaps.

If cleared, scaled bitmaps will be drawn with nearest neighbor sampling, likely resulting in artifacts. This should generally be on when drawing bitmaps, unless performance-bound (rendering to software canvas) or preferring pixelation artifacts to blurriness when scaling significantly.

If bitmaps are scaled for device density at creation time (as resource bitmaps often are) the filtering will already have been done.

On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` and below, hardware accelerated drawing always uses bilinear sampling on scaled bitmaps, regardless of this flag. On devices running `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and above, this flag defaults to being set on a new `Paint`. It can be cleared with `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFlags(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFilterBitmap(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#HINTING_OFF:kotlin.Int`

Font hinter option that disables font hinting.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#HINTING_ON:kotlin.Int`

Font hinter option that enables font hinting.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#LINEAR_TEXT_FLAG:kotlin.Int`

Paint flag that enables smooth linear scaling of text.

Enabling this flag does not actually scale text, but rather adjusts text draw operations to deal gracefully with smooth adjustment of scale. When this flag is enabled, font hinting is disabled to prevent shape deformation between scale factors, and glyph caching is disabled due to the large number of glyph images that will be generated.

`https://developer.android.com/reference/kotlin/android/graphics/Paint.html#SUBPIXEL_TEXT_FLAG:kotlin.Int` should be used in conjunction with this flag to prevent glyph positions from snapping to whole pixel values as scale factor is adjusted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#START_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int`

An integer representing the starting of the line has normal hyphen character (U+002D).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#START_HYPHEN_EDIT_INSERT_ZWJ:kotlin.Int`

An integer representing the starting of the line has Zero-Width-Joiner (U+200D).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#START_HYPHEN_EDIT_NO_EDIT:kotlin.Int`

An integer representing the starting of the line has no modification for hyphenation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#STRIKE_THRU_TEXT_FLAG:kotlin.Int`

Paint flag that applies a strike-through decoration to drawn text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#SUBPIXEL_TEXT_FLAG:kotlin.Int`

Paint flag that enables subpixel positioning of text.

Enabling this flag causes glyph advances to be computed with subpixel accuracy.

This can be used with `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#LINEAR_TEXT_FLAG:kotlin.Int` to prevent text from jittering during smooth scale transitions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int`

A text run flag that indicates the run is located the visually most left segment of the line.

This flag is used for telling the underlying text layout engine that the text is located at the most left of the line. This flag is used for controlling the amount letter spacing added. If the text is in the middle of the line, the text layout engine assigns additional letter spacing to the both side of each letter. On the other hand, the letter spacing should not be added to the visually most left and right of the line. By setting this flag, text layout engine calculates the layout as it is located at the most visually left of the line and doesn't add letter spacing to the left of this run.

Note that the caller must resolve BiDi runs and reorder them visually and set this flag only if the target run is located visually most left position. This left does not always mean the beginning of the text.

If the run covers entire line, caller should set `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` as well.

Note that this flag is only effective for run based APIs. For example, this flag works for `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#drawTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint)` and `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getRunCharacterAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)`. However, this doesn't work for `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#drawText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#measureText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)`. The non-run based APIs works as both `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` are specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int`

A text run flag that indicates the run is located the visually most right segment of the line.

This flag is used for telling the underlying text layout engine that the text is located at the most right of the line. This flag is used for controlling the amount letter spacing added. If the text is in the middle of the line, the text layout engine assigns additional letter spacing to the both side of each letter. On the other hand, the letter spacing should not be added to the visually most left and right of the line. By setting this flag, text layout engine calculates the layout as it is located at the most visually left of the line and doesn't add letter spacing to the left of this run.

Note that the caller must resolve BiDi runs and reorder them visually and set this flag only if the target run is located visually most right position. This right does not always mean the end of the text.

If the run covers entire line, caller should set `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` as well.

Note that this flag is only effective for run based APIs. For example, this flag works for `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#drawTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint)` and `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getRunCharacterAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)`. However, this doesn't work for `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#drawText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint)` or `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#measureText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)`. The non-run based APIs works as both `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#TEXT_RUN_FLAG_LEFT_EDGE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#TEXT_RUN_FLAG_RIGHT_EDGE:kotlin.Int` are specified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#UNDERLINE_TEXT_FLAG:kotlin.Int`

Paint flag that applies an underline decoration to drawn text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#VERTICAL_TEXT_FLAG:kotlin.Int`

A flat that controls text to be written in vertical orientation

This flag is used for telling the underlying text layout engine that the text is for vertical direction. By enabling this flag, text measurement, drawing and shaping APIs works for vertical text layout. For example, `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#drawText(kotlin.String,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint)` draws text from top to bottom. `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#measureText(kotlin.String)` returns vertical advances instead of horizontal advances. `https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper.html#` shapes text vertically and report glyph IDs for vertical layout.

Do not set this flag for making `https://developer.android.com/reference/kotlin/android/text/Layout`. The `https://developer.android.com/reference/kotlin/android/text/Layout` class and its subclasses are designed for horizontal text only and does not work for vertical text.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/TextPaint#TextPaint()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/text/TextPaint#TextPaint(android.graphics.Paint)(p: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/text/TextPaint#TextPaint(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Public methods ||
|---|---|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/text/TextPaint#getUnderlineThickness()()` Returns the thickness of the underline in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/TextPaint#set(android.text.TextPaint)(tp: https://developer.android.com/reference/kotlin/android/text/TextPaint#!)` Copy the fields from tp into this TextPaint, including the fields inherited from Paint. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#ascent()()`

Return the distance above (negative) the baseline (ascent) based on the current typeface and text size.

Note that this is the ascent of the main typeface, and actual text rendered may need a larger ascent because fallback fonts may get used in rendering the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#breakText(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, measuredWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)`

Measure the text, stopping early if the measured width exceeds maxWidth. Return the number of chars that were measured, and if measuredWidth is not null, return in it the actual width measured.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#breakText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, measureForwards: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, measuredWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)`

Measure the text, stopping early if the measured width exceeds maxWidth. Return the number of chars that were measured, and if measuredWidth is not null, return in it the actual width measured.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#breakText(kotlin.String,%20kotlin.Boolean,%20kotlin.Float,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, measureForwards: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, measuredWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)`

Measure the text, stopping early if the measured width exceeds maxWidth. Return the number of chars that were measured, and if measuredWidth is not null, return in it the actual width measured.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#clearShadowLayer()()`

Clear the shadow layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#descent()()`

Return the distance below (positive) the baseline (descent) based on the current typeface and text size.

Note that this is the descent of the main typeface, and actual text rendered may need a larger descent because fallback fonts may get used in rendering the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#equalsForTextMeasurement(android.graphics.Paint)(other: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)`

Returns true of the passed `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#` will have the same effect on text measurement

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getAlpha()()`

Helper to getColor() that just returns the color's alpha value. This is the same as calling getColor() \>\>\> 24. It always returns a value between 0 (completely transparent) and 255 (completely opaque).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getBlendMode()()`

Get the paint's blend mode object. Will return null if there is a Xfermode applied that cannot be represented by a blend mode (i.e. a custom `RuntimeXfermode`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getColor()()`

Return the paint's color in sRGB. Note that the color is a 32bit value containing alpha as well as r,g,b. This 32bit value is not premultiplied, meaning that its alpha can be any value, regardless of the values of r,g,b. See the Color class for more details.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getColorFilter()()`

Get the paint's colorfilter (maybe be null).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getColorLong()()`

Return the paint's color. Note that the color is a long with an encoded `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.html#` as well as alpha and r,g,b. These values are not premultiplied, meaning that alpha can be any value, regardless of the values of r,g,b. See the `https://developer.android.com/reference/kotlin/android/graphics/Color.html#` class for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getEndHyphenEdit()()`

Get the current value of end hyphen edit. The default value is 0 which is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_NO_EDIT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFillPath(android.graphics.Path,%20android.graphics.Path)(src: https://developer.android.com/reference/kotlin/android/graphics/Path.html#!, dst: https://developer.android.com/reference/kotlin/android/graphics/Path.html#!)`

Applies any/all effects (patheffect, stroking) to src, returning the result in dst. The result is that drawing src with this paint will be the same as drawing dst with a default paint (at least from the geometric perspective).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFlags()()`

Return the paint's flags. Use the Flag enum to test flag values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontFeatureSettings()()`

Returns the font feature settings. The format is the same as the CSS font-feature-settings attribute: <https://www.w3.org/TR/css-fonts-3/#font-feature-settings-prop>

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetrics()()`

Allocates a new FontMetrics object, and then calls getFontMetrics(fm) with it, returning the object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetrics(android.graphics.Paint.FontMetrics)(metrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics.html#!)`

Return the font's recommended interline spacing, given the Paint's settings for typeface, textSize, etc. If metrics is not null, return the fontmetric values in it.

Note that these are the values for the main typeface, and actual text rendered may need a larger set of values because fallback fonts may get used in rendering the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetricsForLocale(android.graphics.Paint.FontMetrics)(metrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics.html#)`

Get the font metrics used for the locale Obtain the metrics of the font that is used for the specified locale by `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextLocales(android.os.LocaleList)`. If multiple locales are specified, the minimum ascent and maximum descent will be set. This API is useful for determining the default line height of the empty text field, e.g. `https://developer.android.com/reference/kotlin/android/widget/EditText.html#`. Note, if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` is created from the custom font files, its metrics are reserved, i.e. the ascent will be the custom font's ascent or smaller, the descent will be the custom font's descent or larger. Note, if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` is a system fallback, e.g. `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#SERIF:android.graphics.Typeface`, the default font's metrics are reserved, i.e. the ascent will be the serif font's ascent or smaller, the descent will be the serif font's descent or larger.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetricsInt()()`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetricsInt(android.graphics.Paint.FontMetricsInt)(fmi: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#!)`

Return the font's interline spacing, given the Paint's settings for typeface, textSize, etc. If metrics is not null, return the fontmetric values in it. Note: all values have been converted to integers from floats, in such a way has to make the answers useful for both spacing and clipping. If you want more control over the rounding, call getFontMetrics().

Note that these are the values for the main typeface, and actual text rendered may need a larger set of values because fallback fonts may get used in rendering the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetricsInt(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.graphics.Paint.FontMetricsInt)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, outMetrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#)`

Returns the font metrics value for the given text. If the text is rendered with multiple font files, this function returns the large ascent and descent that are enough for drawing all font files. The context range is used for shaping context. Some script, e.g. Arabic or Devanagari, changes letter shape based on its location or surrounding characters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetricsInt(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.graphics.Paint.FontMetricsInt)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, outMetrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#)`

Returns the font metrics value for the given text. If the text is rendered with multiple font files, this function returns the large ascent and descent that are enough for drawing all font files. The context range is used for shaping context. Some script, e.g. Arabic or Devanagari, changes letter shape based on its location or surrounding characters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetricsIntForLocale(android.graphics.Paint.FontMetricsInt)(metrics: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#)`

Get the font metrics used for the locale Obtain the metrics of the font that is used for the specified locale by `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextLocales(android.os.LocaleList)`. If multiple locales are specified, the minimum ascent and maximum descent will be set. This API is useful for determining the default line height of the empty text field, e.g. `https://developer.android.com/reference/kotlin/android/widget/EditText.html#`. Note, if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` is created from the custom font files, its metrics are reserved, i.e. the ascent will be the custom font's ascent or smaller, the descent will be the custom font's descent or larger. Note, if the `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` is a system fallback, e.g. `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#SERIF:android.graphics.Typeface`, the default font's metrics are reserved, i.e. the ascent will be the serif font's ascent or smaller, the descent will be the serif font's descent or larger.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontSpacing()()`

Return the recommend line spacing based on the current typeface and text size.

Note that this is the value for the main typeface, and actual text rendered may need a larger value because fallback fonts may get used in rendering the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontVariationOverride()()`

Gets the current font variation override value.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontVariationSettings()()`

Returns the font variation settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getHinting()()`

Return the paint's hinting mode. Returns either `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#HINTING_OFF:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#HINTING_ON:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getLetterSpacing()()`

Return the paint's letter-spacing for text. The default value is 0.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/MaskFilter.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getMaskFilter()()`

Get the paint's maskfilter object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getOffsetForAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, advance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Get the character offset within the string whose position is closest to the specified horizontal position.

The returned value is generally the value of `offset` for which #getRunAdvance yields a result most closely approximating `advance`, and which is also on a grapheme cluster boundary. As such, it is the preferred method for positioning a cursor in response to a touch or pointer event. The grapheme cluster boundaries are based on [Unicode Standard Annex #29](http://unicode.org/reports/tr29/) but with some tailoring for better user experience.

Note that `advance` is a (generally positive) width measurement relative to the start of the run. Thus, for RTL runs it the distance from the point to the right edge.

All indices are relative to the start of `text`. Further, `0 <= contextStart <= start <= end <= contextEnd <= text.length` must hold on entry, and `start <= result <= end` will hold on return.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getOffsetForAdvance(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, advance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

<br />

`https://developer.android.com/reference/kotlin/android/graphics/PathEffect.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getPathEffect()()`

Get the paint's patheffect object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getRunAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Measure cursor position within a run of text.

The run of text includes the characters from `start` to `end` in the text. In addition, the range `contextStart` to `contextEnd` is used as context for the purpose of complex text shaping, such as Arabic text potentially shaped differently based on the text next to it.

All text outside the range `contextStart..contextEnd` is ignored. The text between `start` and `end` will be laid out to be measured.

The returned width measurement is the advance from `start` to `offset`. It is generally a positive value, no matter the direction of the run. If `offset == end`, the return value is simply the width of the whole run from `start` to `end`.

Ligatures are formed for characters in the range `start..end` (but not for `start..contextStart` or `end..contextEnd`). If `offset` points to a character in the middle of such a formed ligature, but at a grapheme cluster boundary, the return value will also reflect an advance in the middle of the ligature. See #getOffsetForAdvance for more discussion of grapheme cluster boundaries.

The direction of the run is explicitly specified by `isRtl`. Thus, this method is suitable only for runs of a single direction.

All indices are relative to the start of `text`. Further, `0 <= contextStart <= start <= offset <= end <= contextEnd <= text.length` must hold on entry.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getRunAdvance(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getRunCharacterAdvance(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, advances: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?, advancesIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Measure the advance of each character within a run of text and also return the cursor position within the run.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getRunCharacterAdvance(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, advances: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?, advancesIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Shader.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getShader()()`

Get the paint's shader object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getShadowLayerColor()()`

Returns the color of the shadow layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getShadowLayerColorLong()()`

Returns the color of the shadow layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getShadowLayerDx()()`

Returns the x offset of the shadow layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getShadowLayerDy()()`

Returns the y offset of the shadow layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getShadowLayerRadius()()`

Returns the blur radius of the shadow layer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getStartHyphenEdit()()`

Get the current value of start hyphen edit. The default value is 0 which is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#START_HYPHEN_EDIT_NO_EDIT:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getStrikeThruPosition()()`

Distance from top of the strike-through line to the baseline in pixels. The result is negative for positions that are above the baseline. This method returns where the strike-through line should be drawn independent of if the `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#STRIKE_THRU_TEXT_FLAG:kotlin.Int` bit is set. 
The units of this value are pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getStrikeThruThickness()()`

Returns the thickness of the strike-through line in pixels. 
The units of this value are pixels.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Paint.Cap.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getStrokeCap()()`

Return the paint's Cap, controlling how the start and end of stroked lines and paths are treated.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Paint.Join.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getStrokeJoin()()`

Return the paint's stroke join type.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getStrokeMiter()()`

Return the paint's stroke miter value. Used to control the behavior of miter joins when the joins angle is sharp.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getStrokeWidth()()`

Return the width for stroking.

<br />

A value of 0 strokes in hairline mode. Hairlines always draws a single pixel independent of the canvas's matrix.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Paint.Style.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getStyle()()`

Return the paint's style, used for controlling how primitives' geometries are interpreted (except for drawBitmap, which always assumes FILL_STYLE).

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Paint.Align.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextAlign()()`

Return the paint's Align value for drawing text. This controls how the text is positioned relative to its origin. LEFT align means that all of the text will be drawn to the right of its origin (i.e. the origin specifies the LEFT edge of the text) and so on.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextBounds(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Rect)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Return in bounds (allocated by the caller) the smallest rectangle that encloses all of the characters, with an implied origin at (0,0).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextBounds(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Rect)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`

Retrieve the text boundary box and store to bounds. Return in bounds (allocated by the caller) the smallest rectangle that encloses all of the characters, with an implied origin at (0,0). Note that styles are ignored even if you pass `https://developer.android.com/reference/kotlin/android/text/Spanned` instance. Use `https://developer.android.com/reference/kotlin/android/text/StaticLayout` for measuring bounds of `https://developer.android.com/reference/kotlin/android/text/Spanned`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextBounds(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Rect)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)`

Retrieve the text boundary box and store to bounds. Return in bounds (allocated by the caller) the smallest rectangle that encloses all of the characters, with an implied origin at (0,0).

<br />

`https://developer.android.com/reference/kotlin/java/util/Locale.html#` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextLocale()()`

Get the text's primary Locale. Note that this is not all of the locale-related information Paint has. Use `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextLocales()` to get the complete list.

<br />

`https://developer.android.com/reference/kotlin/android/os/LocaleList.html#` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextLocales()()`

Get the text locale list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextPath(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, path: https://developer.android.com/reference/kotlin/android/graphics/Path.html#!)`

Return the path (outline) for the specified text. Note: just like Canvas.drawText, this will respect the Align setting in the paint.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextPath(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Path)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, path: https://developer.android.com/reference/kotlin/android/graphics/Path.html#!)`

Return the path (outline) for the specified text. Note: just like Canvas.drawText, this will respect the Align setting in the paint.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextRunAdvances(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.FloatArray,%20kotlin.Int)(chars: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, advances: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html?, advancesIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve the character advances of the text. Returns the total advance width for the characters in the run from `index` for `count` of chars, and if `advances` is not null, the advance assigned to each of these characters (java chars).

The trailing surrogate in a valid surrogate pair is assigned an advance of 0. Thus the number of returned advances is always equal to count, not to the number of unicode codepoints represented by the run.

In the case of conjuncts or combining marks, the total advance is assigned to the first logical character, and the following characters are assigned an advance of 0.

This generates the sum of the advances of glyphs for characters in a reordered cluster as the width of the first logical character in the cluster, and 0 for the widths of all other characters in the cluster. In effect, such clusters are treated like conjuncts.

The shaping bounds limit the amount of context available outside start and end that can be used for shaping analysis. These bounds typically reflect changes in bidi level or font metrics across which shaping does not occur.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextRunCursor(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, cursorOpt: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns the next cursor position in the run. This avoids placing the cursor between surrogates, between characters that form conjuncts, between base characters and combining marks, or within a reordering cluster.

ContextStart and offset are relative to the start of text. The context is the shaping context for cursor movement, generally the bounds of the metric span enclosing the cursor in the direction of movement.

If cursorOpt is `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#CURSOR_AT:kotlin.Int` and the offset is not a valid cursor position, this returns -1. Otherwise this will never return a value before contextStart or after contextStart + contextLength.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextRunCursor(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, contextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, contextEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isRtl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, cursorOpt: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns the next cursor position in the run. This avoids placing the cursor between surrogates, between characters that form conjuncts, between base characters and combining marks, or within a reordering cluster.

ContextStart, contextEnd, and offset are relative to the start of text. The context is the shaping context for cursor movement, generally the bounds of the metric span enclosing the cursor in the direction of movement.

If cursorOpt is `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#CURSOR_AT:kotlin.Int` and the offset is not a valid cursor position, this returns -1. Otherwise this will never return a value before contextStart or after contextEnd.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextScaleX()()`

Return the paint's horizontal scale factor for text. The default value is 1.0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextSize()()`

Return the paint's text size.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextSkewX()()`

Return the paint's horizontal skew factor for text. The default value is 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextWidths(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, widths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)`

Return the advance widths for the characters in the string.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextWidths(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, widths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)`

Return the advance widths for the characters in the string.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextWidths(kotlin.String,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, widths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)`

Return the advance widths for the characters in the string.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTextWidths(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, widths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html!)`

Return the advance widths for the characters in the string.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getTypeface()()`

Get the paint's typeface object.

<br />

The typeface object identifies which font to use when drawing or measuring text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getUnderlinePosition()()`

Returns the distance from top of the underline to the baseline in pixels. The result is positive for positions that are below the baseline. This method returns where the underline should be drawn independent of if the `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#UNDERLINE_TEXT_FLAG:kotlin.Int` bit is set. 
The units of this value are pixels.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getWordSpacing()()`

Return the paint's extra word-spacing for text. The default value is 0. 
The units of this value are pixels.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Xfermode.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getXfermode()()`

Get the paint's transfer mode object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#hasGlyph(kotlin.String)(string: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Determine whether the typeface set on the paint has a glyph supporting the string. The simplest case is when the string contains a single character, in which this method determines whether the font has the character. In the case of multiple characters, the method returns true if there is a single glyph representing the ligature. For example, if the input is a pair of regional indicator symbols, determine whether there is an emoji flag for the pair.

Finally, if the string contains a variation selector, the method only returns true if the fonts contains a glyph specific to that variation.

Checking is done on the entire fallback chain, not just the immediate font referenced.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isAntiAlias()()`

Helper for getFlags(), returning true if ANTI_ALIAS_FLAG bit is set AntiAliasing smooths out the edges of what is being drawn, but is has no impact on the interior of the shape. See setDither() and setFilterBitmap() to affect how colors are treated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isDither()()`

Helper for getFlags(), returning true if DITHER_FLAG bit is set Dithering affects how colors that are higher precision than the device are down-sampled. No dithering is generally faster, but higher precision colors are just truncated down (e.g. 8888 -\> 565). Dithering tries to distribute the error inherent in this process, to reduce the visual artifacts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isElegantTextHeight()()`

Get the elegant metrics flag. Note: For applications target API 35 or later, this function returns true by default. For applications target API 36 or later, the function call will be ignored and the elegant text height is always enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isFakeBoldText()()`

Helper for getFlags(), returning true if FAKE_BOLD_TEXT_FLAG bit is set

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isFilterBitmap()()`

Whether or not the bitmap filter is activated. Filtering affects the sampling of bitmaps when they are transformed. Filtering does not affect how the colors in the bitmap are converted into device pixels. That is dependent on dithering and xfermodes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isLinearText()()`

Helper for getFlags(), returning true if LINEAR_TEXT_FLAG bit is set

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isStrikeThruText()()`

Helper for getFlags(), returning true if STRIKE_THRU_TEXT_FLAG bit is set

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isSubpixelText()()`

Helper for getFlags(), returning true if SUBPIXEL_TEXT_FLAG bit is set

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#isUnderlineText()()`

Helper for getFlags(), returning true if UNDERLINE_TEXT_FLAG bit is set

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#measureText(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return the width of the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#measureText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return the width of the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#measureText(kotlin.String)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Return the width of the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#measureText(kotlin.String,%20kotlin.Int,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return the width of the text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#reset()()`

Restores the paint to its default settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#set(android.graphics.Paint)(src: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#!)`

Copy the fields from src into this paint. This is equivalent to calling get() on all of the src fields, and calling the corresponding set() methods on this.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setARGB(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, g: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Helper to setColor(), that takes a,r,g,b and constructs the color int

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setAlpha(kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Helper to setColor(), that only assigns the color's alpha value, leaving its r,g,b values unchanged. Results are undefined if the alpha value is outside of the range \[0..255\]

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setAntiAlias(kotlin.Boolean)(aa: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Helper for setFlags(), setting or clearing the ANTI_ALIAS_FLAG bit AntiAliasing smooths out the edges of what is being drawn, but is has no impact on the interior of the shape. See setDither() and setFilterBitmap() to affect how colors are treated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setBlendMode(android.graphics.BlendMode)(blendmode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#?)`

Set or clear the blend mode. A blend mode defines how source pixels (generated by a drawing command) are composited with the destination pixels (content of the render target).

<br />

Pass null to clear any previous blend mode.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setColor(kotlin.Int)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the paint's color. Note that the color is an int containing alpha as well as r,g,b. This 32bit value is not premultiplied, meaning that its alpha can be any value, regardless of the values of r,g,b. See the Color class for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setColor(kotlin.Long)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Set the paint's color with a `ColorLong`. Note that the color is a long with an encoded `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.html#` as well as alpha and r,g,b. These values are not premultiplied, meaning that alpha can be any value, regardless of the values of r,g,b. See the `https://developer.android.com/reference/kotlin/android/graphics/Color.html#` class for more details.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setColorFilter(android.graphics.ColorFilter)(filter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#!)`

Set or clear the paint's colorfilter, returning the parameter.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setDither(kotlin.Boolean)(dither: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Helper for setFlags(), setting or clearing the DITHER_FLAG bit Dithering affects how colors that are higher precision than the device are down-sampled. No dithering is generally faster, but higher precision colors are just truncated down (e.g. 8888 -\> 565). Dithering tries to distribute the error inherent in this process, to reduce the visual artifacts.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setElegantTextHeight(kotlin.Boolean)(elegant: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set the paint's elegant height metrics flag. This setting selects font variants that have not been compacted to fit Latin-based vertical metrics, and also increases top and bottom bounds to provide more space.

Note: For applications target API 35 or later, the default value will be true by default. For applications target API 36 or later, the function call will be ignored and the elegant text height is always enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setEndHyphenEdit(kotlin.Int)(endHyphen: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set a end hyphen edit on the paint. By setting end hyphen edit, the measurement and drawing is performed with modifying hyphenation at the end of line. For example, by passing `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` like as follows, HYPHEN(U+2010) character is appended at the end of line.

```kotlin
<code>
    Paint paint = new Paint();
    paint.setEndHyphenEdit(Paint.END_HYPHEN_EDIT_INSERT_HYPHEN);
    paint.measureText("abc", 0, 3);  // Returns the width of "abc-"
    Canvas.drawText("abc", 0, 3, 0f, 0f, paint);  // Draws "abc-"
  </code>
```
The default value is 0 which is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#END_HYPHEN_EDIT_NO_EDIT:kotlin.Int`.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFakeBoldText(kotlin.Boolean)(fakeBoldText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Helper for setFlags(), setting or clearing the FAKE_BOLD_TEXT_FLAG bit

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFilterBitmap(kotlin.Boolean)(filter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Helper for setFlags(), setting or clearing the FILTER_BITMAP_FLAG bit. Filtering affects the sampling of bitmaps when they are transformed. Filtering does not affect how the colors in the bitmap are converted into device pixels. That is dependent on dithering and xfermodes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFlags(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the paint's flags. Use the Flag enum to specific flag values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFontFeatureSettings(kotlin.String)(settings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Set font feature settings. The format is the same as the CSS font-feature-settings attribute: <https://www.w3.org/TR/css-fonts-3/#font-feature-settings-prop>

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFontVariationOverride(kotlin.String)(fontVariationOverride: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)`

Sets TrueType or OpenType font variation settings for overriding. The settings string is constructed from multiple pairs of axis tag and style values. The axis tag must contain four ASCII characters and must be wrapped with single quotes (U+0027) or double quotes (U+0022). Axis strings that are longer or shorter than four characters, or contain characters outside of U+0020..U+007E are invalid. If invalid font variation settings is provided, this method does nothing and returning false with printing error message to the logcat. Different from `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFontVariationSettings(kotlin.String)`, this overrides the font variation settings which is already assigned to the font instance. For example, if the underlying font is configured as `'wght' 500, 'ital' 1`, and if the override is specified as ``'wght' 700, `wdth` 150``, then the effective font variation setting is `` `wght' 700, 'ital' 1, 'wdth' 150 ``. The \`wght\` value is updated by override, 'ital' value is preserved because no overrides, and \`wdth\` value is added by override. If the font variation override is empty or null, nothing overrides and original font variation settings assigned to the font instance is used as it is.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setFontVariationSettings(kotlin.String)(fontVariationSettings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

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

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setHinting(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set the paint's hinting mode. May be either `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#HINTING_OFF:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#HINTING_ON:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setLetterSpacing(kotlin.Float)(letterSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the paint's letter-spacing for text. The default value is 0. The value is in 'EM' units. Typical values for slight expansion will be around 0.05. Negative values tighten text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setLinearText(kotlin.Boolean)(linearText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Helper for setFlags(), setting or clearing the LINEAR_TEXT_FLAG bit

<br />

`https://developer.android.com/reference/kotlin/android/graphics/MaskFilter.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setMaskFilter(android.graphics.MaskFilter)(maskfilter: https://developer.android.com/reference/kotlin/android/graphics/MaskFilter.html#!)`

Set or clear the maskfilter object.

<br />

Pass null to clear any previous maskfilter. As a convenience, the parameter passed is also returned.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/PathEffect.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setPathEffect(android.graphics.PathEffect)(effect: https://developer.android.com/reference/kotlin/android/graphics/PathEffect.html#!)`

Set or clear the patheffect object.

<br />

Pass null to clear any previous patheffect. As a convenience, the parameter passed is also returned.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Shader.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setShader(android.graphics.Shader)(shader: https://developer.android.com/reference/kotlin/android/graphics/Shader.html#!)`

Set or clear the shader object.

<br />

Pass null to clear any previous shader. As a convenience, the parameter passed is also returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)(radius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, shadowColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

This draws a shadow layer below the main layer, with the specified offset and color, and blur radius. If radius is 0, then the shadow layer is removed.

Can be used to create a blurred shadow underneath text. Support for use with other drawing operations is constrained to the software rendering pipeline.

The alpha of the shadow will be the paint's alpha if the shadow color is opaque, or the alpha from the shadow color if not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setShadowLayer(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Long)(radius: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dx: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, dy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, shadowColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

This draws a shadow layer below the main layer, with the specified offset and color, and blur radius. If radius is 0, then the shadow layer is removed.

Can be used to create a blurred shadow underneath text. Support for use with other drawing operations is constrained to the software rendering pipeline.

The alpha of the shadow will be the paint's alpha if the shadow color is opaque, or the alpha from the shadow color if not.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setStartHyphenEdit(kotlin.Int)(startHyphen: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Set a start hyphen edit on the paint. By setting start hyphen edit, the measurement and drawing is performed with modifying hyphenation at the start of line. For example, by passing `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#START_HYPHEN_EDIT_INSERT_HYPHEN:kotlin.Int` like as follows, HYPHEN(U+2010) character is appended at the start of line.

```kotlin
<code>
    Paint paint = new Paint();
    paint.setStartHyphenEdit(Paint.START_HYPHEN_EDIT_INSERT_HYPHEN);
    paint.measureText("abc", 0, 3);  // Returns the width of "-abc"
    Canvas.drawText("abc", 0, 3, 0f, 0f, paint);  // Draws "-abc"
  </code>
```
The default value is 0 which is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#START_HYPHEN_EDIT_NO_EDIT:kotlin.Int`.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setStrikeThruText(kotlin.Boolean)(strikeThruText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Helper for setFlags(), setting or clearing the STRIKE_THRU_TEXT_FLAG bit

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setStrokeCap(android.graphics.Paint.Cap)(cap: https://developer.android.com/reference/kotlin/android/graphics/Paint.Cap.html#!)`

Set the paint's Cap.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setStrokeJoin(android.graphics.Paint.Join)(join: https://developer.android.com/reference/kotlin/android/graphics/Paint.Join.html#!)`

Set the paint's Join.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setStrokeMiter(kotlin.Float)(miter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the paint's stroke miter value. This is used to control the behavior of miter joins when the joins angle is sharp. This value must be \>= 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setStrokeWidth(kotlin.Float)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the width for stroking. Pass 0 to stroke in hairline mode. Hairlines always draws a single pixel independent of the canvas's matrix.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setStyle(android.graphics.Paint.Style)(style: https://developer.android.com/reference/kotlin/android/graphics/Paint.Style.html#!)`

Set the paint's style, used for controlling how primitives' geometries are interpreted (except for drawBitmap, which always assumes Fill).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setSubpixelText(kotlin.Boolean)(subpixelText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Helper for setFlags(), setting or clearing the SUBPIXEL_TEXT_FLAG bit

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextAlign(android.graphics.Paint.Align)(align: https://developer.android.com/reference/kotlin/android/graphics/Paint.Align.html#!)`

Set the paint's text alignment. This controls how the text is positioned relative to its origin. LEFT align means that all of the text will be drawn to the right of its origin (i.e. the origin specifies the LEFT edge of the text) and so on.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextLocale(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#)`

Set the text locale list to a one-member list consisting of just the locale. See `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextLocales(android.os.LocaleList)` for how the locale list affects the way the text is drawn for some languages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextLocales(android.os.LocaleList)(locales: https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)`

Set the text locale list. The text locale list affects how the text is drawn for some languages. For example, if the locale list contains `https://developer.android.com/reference/kotlin/java/util/Locale.html#CHINESE:java.util.Locale` or `https://developer.android.com/reference/kotlin/java/util/Locale.html#CHINA:java.util.Locale`, then the text renderer will prefer to draw text using a Chinese font. Likewise, if the locale list contains `https://developer.android.com/reference/kotlin/java/util/Locale.html#JAPANESE:java.util.Locale` or `https://developer.android.com/reference/kotlin/java/util/Locale.html#JAPAN:java.util.Locale`, then the text renderer will prefer to draw text using a Japanese font. If the locale list contains both, the order those locales appear in the list is considered for deciding the font. This distinction is important because Chinese and Japanese text both use many of the same Unicode code points but their appearance is subtly different for each language. By default, the text locale list is initialized to a one-member list just containing the system locales. This assumes that the text to be rendered will most likely be in the user's preferred language. If the actual language or languages of the text is/are known, then they can be provided to the text renderer using this method. The text renderer may attempt to guess the language script based on the contents of the text to be drawn independent of the text locale here. Specifying the text locales just helps it do a better job in certain ambiguous cases.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextScaleX(kotlin.Float)(scaleX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the paint's horizontal scale factor for text. The default value is 1.0. Values \> 1.0 will stretch the text wider. Values \< 1.0 will stretch the text narrower.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextSize(kotlin.Float)(textSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the paint's text size. This value must be \> 0

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTextSkewX(kotlin.Float)(skewX: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the paint's horizontal skew factor for text. The default value is 0. For approximating oblique text, use values around -0.25.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setTypeface(android.graphics.Typeface)(typeface: https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#!)`

Set or clear the typeface object.

<br />

Pass null to clear any previous typeface. As a convenience, the parameter passed is also returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setUnderlineText(kotlin.Boolean)(underlineText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Helper for setFlags(), setting or clearing the UNDERLINE_TEXT_FLAG bit

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setWordSpacing(kotlin.Float)(wordSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`

Set the paint's extra word-spacing for text. Increases the white space width between words with the given amount of pixels. The default value is 0.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/Xfermode.html#!` `https://developer.android.com/reference/kotlin/android/graphics/Paint.html#setXfermode(android.graphics.Xfermode)(xfermode: https://developer.android.com/reference/kotlin/android/graphics/Xfermode.html#!)`

Set or clear the transfer mode object. A transfer mode defines how source pixels (generate by a drawing command) are composited with the destination pixels (content of the render target).

<br />

Pass null to clear any previous transfer mode. As a convenience, the parameter passed is also returned.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/PorterDuffXfermode.html#` is the most common transfer mode.

<br />

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/TextPaint#baselineShift:kotlin.Int` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/TextPaint#bgColor:kotlin.Int` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/text/TextPaint#density:kotlin.Float` <br /> |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/text/TextPaint#drawableState:kotlin.IntArray` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/TextPaint#linkColor:kotlin.Int` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/TextPaint#underlineColor:kotlin.Int` Special value 0 means no custom underline |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/text/TextPaint#underlineThickness:kotlin.Float` Thickness of the underline, in pixels. |

## Public constructors

### TextPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TextPaint()
```

### TextPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TextPaint(p: Paint!)
```

### TextPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TextPaint(flags: Int)
```

## Public methods

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

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(tp: TextPaint!): Unit
```

Copy the fields from tp into this TextPaint, including the fields inherited from Paint.

## Properties

### baselineShift

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var baselineShift: Int
```

### bgColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var bgColor: Int
```

### density

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var density: Float
```

### drawableState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var drawableState: IntArray!
```

### linkColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var linkColor: Int
```

### underlineColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var underlineColor: Int
```

Special value 0 means no custom underline

### underlineThickness

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var underlineThickness: Float
```

Thickness of the underline, in pixels. 
The units of this value are pixels.
