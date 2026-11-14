Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BoringLayout

Kotlin | [Java](BoringLayout.md)
| --- | --- |

```
open class BoringLayout : Layout, TextUtils.EllipsizeCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.Layout](Layout.md) ||
| | ↳ | [android.text.BoringLayout](BoringLayout.md) |

A BoringLayout is a very simple Layout implementation for text that fits on a single line and is all left-to-right characters. You will probably never want to make one of these yourself; if you do, be sure to call #isBoring first to make sure the text meets the criteria.

This class is used by widgets to control text layout. You should not need to use this class directly unless you are implementing your own widget or custom display object, in which case you are encouraged to use a Layout instead of calling `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#drawText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20android.graphics.Paint)` directly.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics` <br /> |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/Layout` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#BREAK_STRATEGY_BALANCED:kotlin.Int` Value for break strategy indicating balanced line breaking. The breaks are chosen to make all lines as close to the same length as possible, including automatic hyphenation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#BREAK_STRATEGY_HIGH_QUALITY:kotlin.Int` Value for break strategy indicating high quality line breaking, including automatic hyphenation and doing whole-paragraph optimization of line breaks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#BREAK_STRATEGY_SIMPLE:kotlin.Int` Value for break strategy indicating simple line breaking. Automatic hyphens are not added (though soft hyphens are respected), and modifying text generally doesn't affect the layout before it (which yields a more consistent user experience when editing), but layout may not be the highest quality. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#DEFAULT_LINESPACING_ADDITION:kotlin.Float` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#DEFAULT_LINESPACING_MULTIPLIER:kotlin.Float` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#DIR_LEFT_TO_RIGHT:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#DIR_RIGHT_TO_LEFT:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_FULL:kotlin.Int` Value for hyphenation frequency indicating the full amount of automatic hyphenation, typical in typography. Useful for running text and where it's important to put the maximum amount of text in a screen with limited space. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_FULL_FAST:kotlin.Int` Value for hyphenation frequency indicating the full amount of automatic hyphenation with using faster algorithm. This option is useful for running text and where it's important to put the maximum amount of text in a screen with limited space. To make text rendering faster with hyphenation, this algorithm ignores some hyphen character related typographic features, e.g. kerning. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NONE:kotlin.Int` Value for hyphenation frequency indicating no automatic hyphenation. Useful for backward compatibility, and for cases where the automatic hyphenation algorithm results in incorrect hyphenation. Mid-word breaks may still happen when a word is wider than the layout and there is otherwise no valid break. Soft hyphens are ignored and will not be used as suggestions for potential line breaks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NORMAL:kotlin.Int` Value for hyphenation frequency indicating a light amount of automatic hyphenation, which is a conservative default. Useful for informal cases, such as short sentences or chat messages. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NORMAL_FAST:kotlin.Int` Value for hyphenation frequency indicating a light amount of automatic hyphenation with using faster algorithm. This option is useful for informal cases, such as short sentences or chat messages. To make text rendering faster with hyphenation, this algorithm ignores some hyphen character related typographic features, e.g. kerning. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#JUSTIFICATION_MODE_INTER_CHARACTER:kotlin.Int` Value for justification mode indicating the text is justified by stretching letter spacing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#JUSTIFICATION_MODE_INTER_WORD:kotlin.Int` Value for justification mode indicating the text is justified by stretching word spacing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#JUSTIFICATION_MODE_NONE:kotlin.Int` Value for justification mode indicating no justification. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/BoringLayout#BoringLayout(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20kotlin.Float,%20kotlin.Float,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!, outerwidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment!, spacingMult: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, spacingAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/android/text/BoringLayout#BoringLayout(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20kotlin.Float,%20kotlin.Float,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean,%20android.text.TextUtils.TruncateAt,%20kotlin.Int)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!, outerWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment!, spacingMult: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, spacingAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, ellipsize: https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt!, ellipsizedWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/android/text/BoringLayout#BoringLayout(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20kotlin.Float,%20kotlin.Float,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean,%20android.text.TextUtils.TruncateAt,%20kotlin.Int,%20kotlin.Boolean)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint, outerWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment, spacingMult: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, spacingAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, ellipsize: https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt?, ellipsizedWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, useFallbackLineSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |

| Public methods ||
|---|---|
| open [RectF](../android.graphics/RectF.md) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#computeDrawingBoundingBox()()` Get an actual bounding box that draws text content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#draw(android.graphics.Canvas,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int)(c: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#!, highlight: https://developer.android.com/reference/kotlin/android/graphics/Path.html#!, highlightpaint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#!, cursorOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Draw this Layout on the specified canvas, with the highlight path drawn between the background and the text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#ellipsized(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback for the ellipsizer to report what region it ellipsized. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getBottomPadding()()` Returns the number of extra pixels of descent padding in the bottom line of the Layout. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getEllipsisCount(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the number of characters to be ellipsized away, or 0 if no ellipsis is to take place. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getEllipsisStart(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the offset of the first character to be ellipsized away, relative to the start of the line. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getEllipsizedWidth()()` Return the width to which this layout is ellipsized. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getHeight()()` Return the total height of this layout. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getLineContainsTab(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether the specified line contains one or more characters that need to be handled specially, like tabs. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getLineCount()()` Return the number of lines of text in this layout. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getLineDescent(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the descent of the specified line(0...getLineCount() - 1). |
| [Layout.Directions](../android/text/Layout.Directions.md)! | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getLineDirections(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the directional run information for the specified line. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getLineMax(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the unsigned horizontal extent of the specified line, including leading margin indent, but excluding trailing whitespace. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getLineStart(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the text offset of the beginning of the specified line ( 0...getLineCount()). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getLineTop(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the vertical position of the top of the specified line (0...getLineCount()). |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getLineWidth(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the unsigned horizontal extent of the specified line, including leading margin indent and trailing whitespace. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getParagraphDirection(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the primary directionality of the paragraph containing the specified line, either 1 for left-to-right lines, or -1 for right-to-left lines (see `https://developer.android.com/reference/kotlin/android/text/Layout#DIR_LEFT_TO_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/Layout#DIR_RIGHT_TO_LEFT:kotlin.Int`). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#getTopPadding()()` Returns the (negative) number of extra pixels of ascent padding in the top line of the Layout. |
| --- | --- |
| open static [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)! | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#isBoring(kotlin.CharSequence,%20android.text.TextPaint)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!)` Determine and compute metrics if given text can be handled by BoringLayout. |
| open static [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)! | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#isBoring(kotlin.CharSequence,%20android.text.TextPaint,%20android.text.BoringLayout.Metrics)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!)` Determine and compute metrics if given text can be handled by BoringLayout. |
| open static [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)? | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#isBoring(kotlin.CharSequence,%20android.text.TextPaint,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean,%20android.text.BoringLayout.Metrics)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint, textDir: https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic, useFallbackLineSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics?)` Returns null if not boring; the width, ascent, and descent in the provided Metrics object (or a new one if the provided one was null) if boring. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#isFallbackLineSpacingEnabled()()` Return true if the fallback line space is enabled in this Layout. |
| open static [BoringLayout](BoringLayout.md) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#make(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean,%20android.text.TextUtils.TruncateAt,%20kotlin.Int,%20kotlin.Boolean)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint, outerWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, ellipsize: https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt?, ellipsizedWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, useFallbackLineSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Utility function to construct a BoringLayout instance. |
| open static [BoringLayout](BoringLayout.md)! | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#make(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20kotlin.Float,%20kotlin.Float,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!, outerWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment!, spacingMult: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, spacingAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Utility function to construct a BoringLayout instance. |
| --- | --- |
| open static [BoringLayout](BoringLayout.md)! | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#make(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20kotlin.Float,%20kotlin.Float,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean,%20android.text.TextUtils.TruncateAt,%20kotlin.Int)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!, outerWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment!, spacingmult: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, spacingadd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, ellipsize: https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt!, ellipsizedWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Utility function to construct a BoringLayout instance. |
| open [BoringLayout](BoringLayout.md) | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#replaceOrMake(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean,%20android.text.TextUtils.TruncateAt,%20kotlin.Int,%20kotlin.Boolean)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint, outerWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, ellipsize: https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt?, ellipsizedWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, useFallbackLineSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a BoringLayout for the specified text, potentially reusing this one if it is already suitable. |
| open [BoringLayout](BoringLayout.md)! | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#replaceOrMake(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20kotlin.Float,%20kotlin.Float,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!, outerwidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment!, spacingMult: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, spacingAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a BoringLayout for the specified text, potentially reusing this one if it is already suitable. |
| --- | --- |
| open [BoringLayout](BoringLayout.md)! | `https://developer.android.com/reference/kotlin/android/text/BoringLayout#replaceOrMake(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20kotlin.Float,%20kotlin.Float,%20android.text.BoringLayout.Metrics,%20kotlin.Boolean,%20android.text.TextUtils.TruncateAt,%20kotlin.Int)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!, outerWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, align: https://developer.android.com/reference/kotlin/android/text/Layout.Alignment!, spacingMult: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, spacingAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, metrics: https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!, includePad: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, ellipsize: https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt!, ellipsizedWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a BoringLayout for the specified text, potentially reusing this one if it is already suitable. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/Layout` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas)(c: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#!)` Draw this Layout on the specified Canvas. This API draws background first, then draws text on top of it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#, highlightPaths: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Path.html#!>?, highlightPaints: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/Paint.html#!>?, selectionPath: https://developer.android.com/reference/kotlin/android/graphics/Path.html#?, selectionPaint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#?, cursorOffsetVertical: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Draw this layout on the specified canvas. This API draws background first, then draws highlight paths on top of it, then draws selection or cursor, then finally draws text on top of it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#drawBackground(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)` Draw background of this layout. Different from `https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int)` API, this API only draws background, not drawing text, highlights or selections. The background here is drawn by `https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan` attached to the text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#drawText(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)` Draw text part of this layout. Different from `https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int)` API, this API only draws text part, not drawing highlights, selections, or backgrounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#fillCharacterBounds(kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bounds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html, boundsStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the characters' bounds in the given range. The `bounds` array will be filled starting from `boundsStart` (inclusive). The coordinates are in local text layout. <br /> | | `https://developer.android.com/reference/kotlin/android/text/Layout.Alignment` | `https://developer.android.com/reference/kotlin/android/text/Layout#getAlignment()()` Returns the alignment used for creating this layout in pixels. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getBreakStrategy()()` Return the break strategy used for creating this layout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getCursorPath(kotlin.Int,%20android.graphics.Path,%20kotlin.CharSequence)(point: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dest: https://developer.android.com/reference/kotlin/android/graphics/Path.html#!, editingBuffer: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Fills in the specified Path with a representation of a cursor at the specified offset. This will often be a vertical line but can be multiple discontinuous lines in text with multiple directionalities. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getDesiredWidth(kotlin.CharSequence,%20android.text.TextPaint)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!)` Return how wide a layout must be in order to display the specified text with one line per paragraph. As of O, Uses `https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#FIRSTSTRONG_LTR:android.text.TextDirectionHeuristic` as the default text direction heuristics. In the earlier versions uses `https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#LTR:android.text.TextDirectionHeuristic` as the default. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getDesiredWidth(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.text.TextPaint)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, paint: https://developer.android.com/reference/kotlin/android/text/TextPaint!)` Return how wide a layout must be in order to display the specified text slice with one line per paragraph. As of O, Uses `https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#FIRSTSTRONG_LTR:android.text.TextDirectionHeuristic` as the default text direction heuristics. In the earlier versions uses `https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#LTR:android.text.TextDirectionHeuristic` as the default. <br /> | | `https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt?` | `https://developer.android.com/reference/kotlin/android/text/Layout#getEllipsize()()` Return the ellipsize option used for creating this layout. May return null if no ellipsize option was selected. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getHyphenationFrequency()()` Return the hyphenation frequency used for creating this layout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getJustificationMode()()` Return the justification mode used for creating this layout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLeftIndents()()` Return a copy of the left indents used for this layout. May return null if no left indentation is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineAscent(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the ascent of the text on the specified line. The return value is negative to match the Paint.ascent() convention. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineBaseline(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the vertical position of the baseline of the specified line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineBottom(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the vertical position of the bottom of the specified line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineBottom(kotlin.Int,%20kotlin.Boolean)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, includeLineSpacing: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Return the vertical position of the bottom of the specified line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineBounds(kotlin.Int,%20android.graphics.Rect)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Return the baseline for the specified line (0...getLineCount() - 1) If bounds is not null, return the top, left, right, bottom extents of the specified line in it. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineBreakConfig()()` Gets the `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#` used for creating this layout. Do not modify the returned object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineEnd(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the text offset after the last character on the specified line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineForOffset(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the line number on which the specified text offset appears. If you ask for a position before 0, you get 0; if you ask for a position beyond the end of the text, you get the last line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineForVertical(kotlin.Int)(vertical: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the line number corresponding to the specified vertical position. If you ask for a position above 0, you get 0; if you ask for a position below the bottom of the text, you get the last line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineLeft(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the leftmost position that should be exposed for horizontal scrolling on the specified line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineLetterSpacingUnitCount(kotlin.Int,%20kotlin.Boolean)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, includeTrailingWhitespace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the number of letter spacing unit in the line. This API returns a number of letters that is a target of letter spacing. The letter spacing won't be added to the middle of the characters that are needed to be treated as a single, e.g., ligatured or conjunct form. Note that this value is different from the number of\] grapheme clusters that is calculated by `https://developer.android.com/reference/kotlin/java/text/BreakIterator.html#getCharacterInstance(java.util.Locale)`. For example, if the "fi" is ligatured, the ligatured form is treated as single uni and letter spacing is not added, but it has two separate grapheme cluster. This value is used for calculating the letter spacing amount for the justification because the letter spacing is applied between clusters. For example, if extra `W` pixels needed to be filled by letter spacing, the amount of letter spacing to be applied is `W`/(letter spacing unit count - 1) px. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineRight(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the rightmost position that should be exposed for horizontal scrolling on the specified line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineSpacingAmount()()` Returns the amount added to the line height. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineSpacingMultiplier()()` Returns the multiplier applied to the line height. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getLineVisibleEnd(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the text offset after the last visible character (so whitespace is not counted) on the specified line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getMaxLines()()` Return the maximum lines allowed used for creating this layout. Note that this is not an actual line count of this layout. Use `https://developer.android.com/reference/kotlin/android/text/Layout#getLineCount()` for getting the actual line count of this layout. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics.html#?` | `https://developer.android.com/reference/kotlin/android/text/Layout#getMinimumFontMetrics()()` Get the minimum font metrics used for line spacing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getOffsetForHorizontal(kotlin.Int,%20kotlin.Float)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, horiz: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Get the character offset on the specified line whose position is closest to the specified horizontal position. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getOffsetToLeftOf(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getOffsetToRightOf(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://developer.android.com/reference/kotlin/android/text/TextPaint` | `https://developer.android.com/reference/kotlin/android/text/Layout#getPaint()()` Return the paint used for creating this layout. Do not modify the returned paint object. This paint object will still be used for drawing/measuring text. <br /> | | `https://developer.android.com/reference/kotlin/android/text/Layout.Alignment!` | `https://developer.android.com/reference/kotlin/android/text/Layout#getParagraphAlignment(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the alignment of the specified paragraph, taking into account markup attached to it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getParagraphLeft(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the left edge of the specified paragraph, inset by left margins. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getParagraphRight(kotlin.Int)(line: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the right edge of the specified paragraph, inset by right margins. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getPrimaryHorizontal(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the primary horizontal position for the specified text offset. This is the location where a new character would be inserted in the paragraph's primary direction. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | `https://developer.android.com/reference/kotlin/android/text/Layout#getRangeForRect(android.graphics.RectF,%20android.text.SegmentFinder,%20android.text.Layout.TextInclusionStrategy)(area: https://developer.android.com/reference/kotlin/android/graphics/RectF.html#, segmentFinder: https://developer.android.com/reference/kotlin/android/text/SegmentFinder, inclusionStrategy: https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy)` Finds the range of text which is inside the specified rectangle area. The start of the range is the start of the first text segment inside the area, and the end of the range is the end of the last text segment inside the area. A text segment is considered to be inside the area according to the provided `https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy`. If a text segment spans multiple lines or multiple directional runs (e.g. a hyphenated word), the text segment is divided into pieces at the line and run breaks, then the text segment is considered to be inside the area if any of its pieces are inside the area. The returned range may also include text segments which are not inside the specified area, if those text segments are in between text segments which are inside the area. For example, the returned range may be "segment1 segment2 segment3" if "segment1" and "segment3" are inside the area and "segment2" is not. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | `https://developer.android.com/reference/kotlin/android/text/Layout#getRightIndents()()` Return a copy of the right indents used for this layout. May return null if no right indentation is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getSecondaryHorizontal(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the secondary horizontal position for the specified text offset. This is the location where a new character would be inserted in the direction other than the paragraph's primary direction. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getSelectionPath(kotlin.Int,%20kotlin.Int,%20android.graphics.Path)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dest: https://developer.android.com/reference/kotlin/android/graphics/Path.html#!)` Fills in the specified Path with a representation of a highlight between the specified offsets. This will often be a rectangle or a potentially discontinuous set of rectangles. If the start and end are the same, the returned path is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getShiftDrawingOffsetForStartOverhang()()` Returns true if shifting drawing offset for start overhang. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingAdd()()` Returns the amount added to the line height. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingMultiplier()()` Returns the multiplier applied to the line height. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getText()()` Return the text used for creating this layout. <br /> | | `https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic` | `https://developer.android.com/reference/kotlin/android/text/Layout#getTextDirectionHeuristic()()` Returns the text direction heuristic used for creating this layout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getUseBoundsForWidth()()` Returns true if using bounding box as a width, false for using advance as a width. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#getWidth()()` Return the width used for creating this layout in pixels. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#increaseWidthTo(kotlin.Int)(wid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Increase the width of this layout to the specified width. Be careful to use this only when you know it is appropriate--- it does not cause the text to reflow to use the full new width. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#isFontPaddingIncluded()()` Returns true if this layout is created with increased line height. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#isRtlCharAt(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the character at offset is right to left (RTL). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/Layout#isSpanned()()` <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/Layout` |---|---| | `https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy` | `https://developer.android.com/reference/kotlin/android/text/Layout#INCLUSION_STRATEGY_ANY_OVERLAP:android.text.Layout.TextInclusionStrategy` Strategy which considers a text segment to be inside a rectangle area if the segment bounds intersect the rectangle. <br /> | | `https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy` | `https://developer.android.com/reference/kotlin/android/text/Layout#INCLUSION_STRATEGY_CONTAINS_ALL:android.text.Layout.TextInclusionStrategy` Strategy which considers a text segment to be inside a rectangle area if the segment bounds are completely contained within the rectangle. <br /> | | `https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy` | `https://developer.android.com/reference/kotlin/android/text/Layout#INCLUSION_STRATEGY_CONTAINS_CENTER:android.text.Layout.TextInclusionStrategy` Strategy which considers a text segment to be inside a rectangle area if the center of the segment bounds is inside the rectangle. <br /> | ||

## Public constructors

### BoringLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BoringLayout(
    source: CharSequence!, 
    paint: TextPaint!, 
    outerwidth: Int, 
    align: Layout.Alignment!, 
    spacingMult: Float, 
    spacingAdd: Float, 
    metrics: BoringLayout.Metrics!, 
    includePad: Boolean)
```

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to render |
| `paint` | [TextPaint](TextPaint.md)!: the default paint for the layout |
| `outerwidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md)!: whether to left, right, or center the text |
| `spacingMult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| `spacingAdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| --- | --- |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)!: `Metrics` instance that contains information about FontMetrics and line width |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |

### BoringLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BoringLayout(
    source: CharSequence!, 
    paint: TextPaint!, 
    outerWidth: Int, 
    align: Layout.Alignment!, 
    spacingMult: Float, 
    spacingAdd: Float, 
    metrics: BoringLayout.Metrics!, 
    includePad: Boolean, 
    ellipsize: TextUtils.TruncateAt!, 
    ellipsizedWidth: Int)
```

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to render |
| `paint` | [TextPaint](TextPaint.md)!: the default paint for the layout |
| `outerWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md)!: whether to left, right, or center the text |
| `spacingMult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| `spacingAdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| --- | --- |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)!: `Metrics` instance that contains information about FontMetrics and line width |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |
| `ellipsize` | [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)!: whether to ellipsize the text if width of the text is longer than the requested `outerWidth` |
| --- | --- |
| `ellipsizedWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width to which this Layout is ellipsizing. If `ellipsize` is `null`, or is `https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt` this value is not used, `outerWidth` is used instead |

### BoringLayout

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BoringLayout(
    source: CharSequence, 
    paint: TextPaint, 
    outerWidth: Int, 
    align: Layout.Alignment, 
    spacingMult: Float, 
    spacingAdd: Float, 
    metrics: BoringLayout.Metrics, 
    includePad: Boolean, 
    ellipsize: TextUtils.TruncateAt?, 
    ellipsizedWidth: Int, 
    useFallbackLineSpacing: Boolean)
```

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the text to render. This value cannot be `null`. |
| `paint` | [TextPaint](TextPaint.md): the default paint for the layout. This value cannot be `null`. |
| `outerWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text. Value is 0 or greater |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md): whether to left, right, or center the text. This value cannot be `null`. |
| `spacingMult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| `spacingAdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| --- | --- |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md): `Metrics` instance that contains information about FontMetrics and line width. This value cannot be `null`. |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |
| `ellipsize` | [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)?: whether to ellipsize the text if width of the text is longer than the requested `outerWidth`. null if ellipsis is not applied. |
| --- | --- |
| `ellipsizedWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width to which this Layout is ellipsizing. If `ellipsize` is `null`, or is `https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt` this value is not used, `outerWidth` is used instead. Value is 0 or greater |
| `useFallbackLineSpacing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True for adjusting the line spacing based on fallback fonts. False for keeping the first font's line height. If some glyphs requires larger vertical spaces, by passing true to this argument, the layout increase the line height to fit all glyphs. |

## Public methods

### computeDrawingBoundingBox

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeDrawingBoundingBox(): RectF
```

Get an actual bounding box that draws text content. Note that the `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#top:kotlin.Float` and `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#bottom:kotlin.Float` may be different from the `https://developer.android.com/reference/kotlin/android/text/Layout#getLineTop(kotlin.Int)` of the first line and `https://developer.android.com/reference/kotlin/android/text/Layout#getLineBottom(kotlin.Int)` of the last line. The line top and line bottom are calculated based on yMin/yMax or ascent/descent value of font file. On the other hand, the drawing bounding boxes are calculated based on actual glyphs used there.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` | This value cannot be `null`. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun draw(
    c: Canvas!, 
    highlight: Path!, 
    highlightpaint: Paint!, 
    cursorOffset: Int
): Unit
```

Draw this Layout on the specified canvas, with the highlight path drawn between the background and the text.

| Parameters ||
|---|---|
| `canvas` | the canvas |
| `selectionHighlight` | the path of the selection highlight or cursor; can be null |
| `selectionHighlightPaint` | the paint for the selection highlight |
| --- | --- |
| `cursorOffsetVertical` | the amount to temporarily translate the canvas while rendering the highlight |

### ellipsized

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ellipsized(
    start: Int, 
    end: Int
): Unit
```

Callback for the ellipsizer to report what region it ellipsized.

### getBottomPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBottomPadding(): Int
```

Returns the number of extra pixels of descent padding in the bottom line of the Layout.

### getEllipsisCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEllipsisCount(line: Int): Int
```

Returns the number of characters to be ellipsized away, or 0 if no ellipsis is to take place.

### getEllipsisStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEllipsisStart(line: Int): Int
```

Return the offset of the first character to be ellipsized away, relative to the start of the line. (So 0 if the beginning of the line is ellipsized, not getLineStart().)

### getEllipsizedWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEllipsizedWidth(): Int
```

Return the width to which this layout is ellipsized. If no ellipsize is applied, the same amount of `https://developer.android.com/reference/kotlin/android/text/Layout#getWidth()` is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the amount of ellipsized width in pixels. Value is 0 or greater |

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHeight(): Int
```

Return the total height of this layout.

### getLineContainsTab

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLineContainsTab(line: Int): Boolean
```

Returns whether the specified line contains one or more characters that need to be handled specially, like tabs.

### getLineCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLineCount(): Int
```

Return the number of lines of text in this layout.

### getLineDescent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLineDescent(line: Int): Int
```

Return the descent of the specified line(0...getLineCount() - 1).

### getLineDirections

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLineDirections(line: Int): Layout.Directions!
```

Returns the directional run information for the specified line. The array alternates counts of characters in left-to-right and right-to-left segments of the line.

NOTE: this is inadequate to support bidirectional text, and will change.

### getLineMax

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLineMax(line: Int): Float
```

Gets the unsigned horizontal extent of the specified line, including leading margin indent, but excluding trailing whitespace.

### getLineStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLineStart(line: Int): Int
```

Return the text offset of the beginning of the specified line ( 0...getLineCount()). If the specified line is equal to the line count, returns the length of the text.

### getLineTop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLineTop(line: Int): Int
```

Return the vertical position of the top of the specified line (0...getLineCount()). If the specified line is equal to the line count, returns the bottom of the last line.

### getLineWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLineWidth(line: Int): Float
```

Gets the unsigned horizontal extent of the specified line, including leading margin indent and trailing whitespace.

### getParagraphDirection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParagraphDirection(line: Int): Int
```

Returns the primary directionality of the paragraph containing the specified line, either 1 for left-to-right lines, or -1 for right-to-left lines (see `https://developer.android.com/reference/kotlin/android/text/Layout#DIR_LEFT_TO_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/Layout#DIR_RIGHT_TO_LEFT:kotlin.Int`).

### getTopPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTopPadding(): Int
```

Returns the (negative) number of extra pixels of ascent padding in the top line of the Layout.

### isBoring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isBoring(
    text: CharSequence!, 
    paint: TextPaint!
): BoringLayout.Metrics!
```

Determine and compute metrics if given text can be handled by BoringLayout.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: a text |
| `paint` | [TextPaint](TextPaint.md)!: a paint |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!` | layout metric for the given text. null if given text is unable to be handled by BoringLayout. |

### isBoring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isBoring(
    text: CharSequence!, 
    paint: TextPaint!, 
    metrics: BoringLayout.Metrics!
): BoringLayout.Metrics!
```

Determine and compute metrics if given text can be handled by BoringLayout.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: a text |
| `paint` | [TextPaint](TextPaint.md)!: a paint |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)!: a metrics object to be recycled. If null is passed, this function creat new object. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics!` | layout metric for the given text. If metrics is not null, this method fills values to given metrics object instead of allocating new metrics object. null if given text is unable to be handled by BoringLayout. |

### isBoring

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isBoring(
    text: CharSequence, 
    paint: TextPaint, 
    textDir: TextDirectionHeuristic, 
    useFallbackLineSpacing: Boolean, 
    metrics: BoringLayout.Metrics?
): BoringLayout.Metrics?
```

Returns null if not boring; the width, ascent, and descent in the provided Metrics object (or a new one if the provided one was null) if boring.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): a text to be calculated text layout. This value cannot be `null`. |
| `paint` | [TextPaint](TextPaint.md): a paint object used for styling. This value cannot be `null`. |
| `textDir` | [TextDirectionHeuristic](TextDirectionHeuristic.md): a text direction. This value cannot be `null`. |
| --- | --- |
| `useFallbackLineSpacing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True for adjusting the line spacing based on fallback fonts. False for keeping the first font's line height. If some glyphs requires larger vertical spaces, by passing true to this argument, the layout increase the line height to fit all glyphs. |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)?: the out metrics. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/BoringLayout.Metrics?` | metrics on success. null if text cannot be rendered by BoringLayout. |

### isFallbackLineSpacingEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFallbackLineSpacingEnabled(): Boolean
```

Return true if the fallback line space is enabled in this Layout.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the fallback line space is enabled. Otherwise, returns false. |

### make

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun make(
    source: CharSequence, 
    paint: TextPaint, 
    outerWidth: Int, 
    align: Layout.Alignment, 
    metrics: BoringLayout.Metrics, 
    includePad: Boolean, 
    ellipsize: TextUtils.TruncateAt?, 
    ellipsizedWidth: Int, 
    useFallbackLineSpacing: Boolean
): BoringLayout
```

Utility function to construct a BoringLayout instance. The spacing multiplier and additional amount spacing are not used by BoringLayout. `https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingMultiplier()` will return 1.0 and `https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingAdd()` will return 0.0.

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the text to render. This value cannot be `null`. |
| `paint` | [TextPaint](TextPaint.md): the default paint for the layout. This value cannot be `null`. |
| `outerWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text. Value is 0 or greater |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md): whether to left, right, or center the text. This value cannot be `null`. |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md): `Metrics` instance that contains information about FontMetrics and line width. This value cannot be `null`. |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |
| --- | --- |
| `ellipsize` | [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)?: whether to ellipsize the text if width of the text is longer than the requested width. null if ellipsis is not applied. |
| `ellipsizedWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width to which this Layout is ellipsizing. If `ellipsize` is `null`, or is `https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt` this value is not used, `outerWidth` is used instead. Value is 0 or greater |
| `useFallbackLineSpacing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True for adjusting the line spacing based on fallback fonts. False for keeping the first font's line height. If some glyphs requires larger vertical spaces, by passing true to this argument, the layout increase the line height to fit all glyphs. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/BoringLayout#` | This value cannot be `null`. |

### make

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun make(
    source: CharSequence!, 
    paint: TextPaint!, 
    outerWidth: Int, 
    align: Layout.Alignment!, 
    spacingMult: Float, 
    spacingAdd: Float, 
    metrics: BoringLayout.Metrics!, 
    includePad: Boolean
): BoringLayout!
```

Utility function to construct a BoringLayout instance.

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to render |
| `paint` | [TextPaint](TextPaint.md)!: the default paint for the layout |
| `outerWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md)!: whether to left, right, or center the text |
| `spacingMult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| `spacingAdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| --- | --- |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)!: `Metrics` instance that contains information about FontMetrics and line width |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |

### make

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun make(
    source: CharSequence!, 
    paint: TextPaint!, 
    outerWidth: Int, 
    align: Layout.Alignment!, 
    spacingmult: Float, 
    spacingadd: Float, 
    metrics: BoringLayout.Metrics!, 
    includePad: Boolean, 
    ellipsize: TextUtils.TruncateAt!, 
    ellipsizedWidth: Int
): BoringLayout!
```

Utility function to construct a BoringLayout instance.

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to render |
| `paint` | [TextPaint](TextPaint.md)!: the default paint for the layout |
| `outerWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md)!: whether to left, right, or center the text |
| `spacingmult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| `spacingadd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| --- | --- |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)!: `Metrics` instance that contains information about FontMetrics and line width |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |
| `ellipsize` | [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)!: whether to ellipsize the text if width of the text is longer than the requested width |
| --- | --- |
| `ellipsizedWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width to which this Layout is ellipsizing. If `ellipsize` is `null`, or is `https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt` this value is not used, `outerWidth` is used instead |

### replaceOrMake

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceOrMake(
    source: CharSequence, 
    paint: TextPaint, 
    outerWidth: Int, 
    align: Layout.Alignment, 
    metrics: BoringLayout.Metrics, 
    includePad: Boolean, 
    ellipsize: TextUtils.TruncateAt?, 
    ellipsizedWidth: Int, 
    useFallbackLineSpacing: Boolean
): BoringLayout
```

Returns a BoringLayout for the specified text, potentially reusing this one if it is already suitable. The caller must make sure that no one is still using this Layout. The spacing multiplier and additional amount spacing are not used by BoringLayout. `https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingMultiplier()` will return 1.0 and `https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingAdd()` will return 0.0.

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the text to render. This value cannot be `null`. |
| `paint` | [TextPaint](TextPaint.md): the default paint for the layout. This value cannot be `null`. |
| `outerWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text. Value is 0 or greater |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md): whether to left, right, or center the text. This value cannot be `null`. |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md): `Metrics` instance that contains information about FontMetrics and line width. This value cannot be `null`. |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |
| --- | --- |
| `ellipsize` | [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)?: whether to ellipsize the text if width of the text is longer than the requested width. null if ellipsis not applied. |
| `ellipsizedWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width to which this Layout is ellipsizing. If `ellipsize` is `null`, or is `https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt` this value is not used, `outerWidth` is used instead. Value is 0 or greater |
| `useFallbackLineSpacing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True for adjusting the line spacing based on fallback fonts. False for keeping the first font's line height. If some glyphs requires larger vertical spaces, by passing true to this argument, the layout increase the line height to fit all glyphs. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/BoringLayout#` | This value cannot be `null`. |

### replaceOrMake

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceOrMake(
    source: CharSequence!, 
    paint: TextPaint!, 
    outerwidth: Int, 
    align: Layout.Alignment!, 
    spacingMult: Float, 
    spacingAdd: Float, 
    metrics: BoringLayout.Metrics!, 
    includePad: Boolean
): BoringLayout!
```

Returns a BoringLayout for the specified text, potentially reusing this one if it is already suitable. The caller must make sure that no one is still using this Layout.

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to render |
| `paint` | [TextPaint](TextPaint.md)!: the default paint for the layout |
| `outerwidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md)!: whether to left, right, or center the text |
| `spacingMult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| `spacingAdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| --- | --- |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)!: `Metrics` instance that contains information about FontMetrics and line width |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |

### replaceOrMake

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceOrMake(
    source: CharSequence!, 
    paint: TextPaint!, 
    outerWidth: Int, 
    align: Layout.Alignment!, 
    spacingMult: Float, 
    spacingAdd: Float, 
    metrics: BoringLayout.Metrics!, 
    includePad: Boolean, 
    ellipsize: TextUtils.TruncateAt!, 
    ellipsizedWidth: Int
): BoringLayout!
```

Returns a BoringLayout for the specified text, potentially reusing this one if it is already suitable. The caller must make sure that no one is still using this Layout.

| Parameters ||
|---|---|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to render |
| `paint` | [TextPaint](TextPaint.md)!: the default paint for the layout |
| `outerWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md)!: whether to left, right, or center the text |
| `spacingMult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| `spacingAdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): this value is no longer used by BoringLayout |
| --- | --- |
| `metrics` | [BoringLayout.Metrics](../android/text/BoringLayout.Metrics.md)!: `Metrics` instance that contains information about FontMetrics and line width |
| `includePad` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set whether to include extra space beyond font ascent and descent which is needed to avoid clipping in some scripts |
| `ellipsize` | [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)!: whether to ellipsize the text if width of the text is longer than the requested width |
| --- | --- |
| `ellipsizedWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width to which this Layout is ellipsizing. If `ellipsize` is `null`, or is `https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt` this value is not used, `outerWidth` is used instead |
