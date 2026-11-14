# DynamicLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DynamicLayout

Kotlin| [Java](DynamicLayout.md) 
| --- | --- |

```
open class DynamicLayout : Layout
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.Layout](Layout.md) ||
| | ↳ | [android.text.DynamicLayout](DynamicLayout.md) |

DynamicLayout is a text layout that updates itself as the text is edited.

This is used by widgets to control text layout. You should not need to use this class directly unless you are implementing your own widget or custom display object, or need to call [Canvas.drawText()](../android.graphics/Canvas.md))directly.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/text/DynamicLayout.Builder.md) Builder for dynamic layouts. |

| Inherited constants ||
|---|---|
| From class [Layout](Layout.md) |--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_BALANCED](Layout.md) <br /> Value for break strategy indicating balanced line breaking. The breaks are chosen to make all lines as close to the same length as possible, including automatic hyphenation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_HIGH_QUALITY](Layout.md) <br /> Value for break strategy indicating high quality line breaking, including automatic hyphenation and doing whole-paragraph optimization of line breaks. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_SIMPLE](Layout.md) <br /> Value for break strategy indicating simple line breaking. Automatic hyphens are not added (though soft hyphens are respected), and modifying text generally doesn't affect the layout before it (which yields a more consistent user experience when editing), but layout may not be the highest quality. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [DEFAULT_LINESPACING_ADDITION](Layout.md) <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [DEFAULT_LINESPACING_MULTIPLIER](Layout.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIR_LEFT_TO_RIGHT](Layout.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIR_RIGHT_TO_LEFT](Layout.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_FULL](Layout.md) <br /> Value for hyphenation frequency indicating the full amount of automatic hyphenation, typical in typography. Useful for running text and where it's important to put the maximum amount of text in a screen with limited space. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_FULL_FAST](Layout.md) <br /> Value for hyphenation frequency indicating the full amount of automatic hyphenation with using faster algorithm. This option is useful for running text and where it's important to put the maximum amount of text in a screen with limited space. To make text rendering faster with hyphenation, this algorithm ignores some hyphen character related typographic features, e.g. kerning. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NONE](Layout.md) <br /> Value for hyphenation frequency indicating no automatic hyphenation. Useful for backward compatibility, and for cases where the automatic hyphenation algorithm results in incorrect hyphenation. Mid-word breaks may still happen when a word is wider than the layout and there is otherwise no valid break. Soft hyphens are ignored and will not be used as suggestions for potential line breaks. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NORMAL](Layout.md) <br /> Value for hyphenation frequency indicating a light amount of automatic hyphenation, which is a conservative default. Useful for informal cases, such as short sentences or chat messages. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NORMAL_FAST](Layout.md) <br /> Value for hyphenation frequency indicating a light amount of automatic hyphenation with using faster algorithm. This option is useful for informal cases, such as short sentences or chat messages. To make text rendering faster with hyphenation, this algorithm ignores some hyphen character related typographic features, e.g. kerning. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_INTER_CHARACTER](Layout.md) <br /> Value for justification mode indicating the text is justified by stretching letter spacing. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_INTER_WORD](Layout.md) <br /> Value for justification mode indicating the text is justified by stretching word spacing. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_NONE](Layout.md) <br /> Value for justification mode indicating no justification. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DynamicLayout](DynamicLayout.md))`(`base:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `paint:` ` [TextPaint](TextPaint.md)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `align:` ` [Layout.Alignment](../android/text/Layout.Alignment.md)`, `spacingmult:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `spacingadd:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `includepad:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| [DynamicLayout](DynamicLayout.md))`(`base:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `display:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `paint:` ` [TextPaint](TextPaint.md)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `align:` ` [Layout.Alignment](../android/text/Layout.Alignment.md)`, `spacingmult:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `spacingadd:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `includepad:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| [DynamicLayout](DynamicLayout.md))`(`base:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `display:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `paint:` ` [TextPaint](TextPaint.md)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `align:` ` [Layout.Alignment](../android/text/Layout.Alignment.md)`, `spacingmult:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `spacingadd:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `includepad:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `ellipsize:` ` [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)?`, `ellipsizedWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBottomPadding](DynamicLayout.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsisCount](DynamicLayout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsisStart](DynamicLayout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsizedWidth](DynamicLayout.md))`()` <br /> |
| open [LineBreakConfig](../android.graphics.text/LineBreakConfig.md) | [getLineBreakConfig](DynamicLayout.md))`()` Gets the [LineBreakConfig](../android.graphics.text/LineBreakConfig.md) used in this DynamicLayout. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLineContainsTab](DynamicLayout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineCount](DynamicLayout.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineDescent](DynamicLayout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Layout.Directions](../android/text/Layout.Directions.md)! | [getLineDirections](DynamicLayout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineStart](DynamicLayout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineTop](DynamicLayout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphDirection](DynamicLayout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTopPadding](DynamicLayout.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Layout](Layout.md) |---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RectF](../android.graphics/RectF.md) | [computeDrawingBoundingBox](Layout.md))`()` <br /> Get an actual bounding box that draws text content. Note that the [RectF.top](../android.graphics/RectF.md) and [RectF.bottom](../android.graphics/RectF.md) may be different from the [Layout.getLineTop(int)](Layout.md))of the first line and [Layout.getLineBottom(int)](Layout.md))of the last line. The line top and line bottom are calculated based on yMin/yMax or ascent/descent value of font file. On the other hand, the drawing bounding boxes are calculated based on actual glyphs used there. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](Layout.md))`(`c:` ` [Canvas](../android.graphics/Canvas.md)!`)` <br /> Draw this Layout on the specified Canvas. This API draws background first, then draws text on top of it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](Layout.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)!`, `selectionHighlight:` ` [Path](../android.graphics/Path.md)!`, `selectionHighlightPaint:` ` [Paint](../android.graphics/Paint.md)!`, `cursorOffsetVertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Draw this Layout on the specified canvas, with the highlight path drawn between the background and the text. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](Layout.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`, `highlightPaths:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Path](../android.graphics/Path.md)!>?`, `highlightPaints:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Paint](../android.graphics/Paint.md)!>?`, `selectionPath:` ` [Path](../android.graphics/Path.md)?`, `selectionPaint:` ` [Paint](../android.graphics/Paint.md)?`, `cursorOffsetVertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Draw this layout on the specified canvas. This API draws background first, then draws highlight paths on top of it, then draws selection or cursor, then finally draws text on top of it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBackground](Layout.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` <br /> Draw background of this layout. Different from [draw(android.graphics.Canvas,java.util.List,java.util.List,android.graphics.Path,android.graphics.Paint,int)](Layout.md))API, this API only draws background, not drawing text, highlights or selections. The background here is drawn by [LineBackgroundSpan](../android.text.style/LineBackgroundSpan.md) attached to the text. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawText](Layout.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)`)` <br /> Draw text part of this layout. Different from [draw(android.graphics.Canvas,java.util.List,java.util.List,android.graphics.Path,android.graphics.Paint,int)](Layout.md))API, this API only draws text part, not drawing highlights, selections, or backgrounds. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillCharacterBounds](Layout.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `boundsStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the characters' bounds in the given range. The`bounds`array will be filled starting from`boundsStart`(inclusive). The coordinates are in local text layout. <br /> | | [Layout.Alignment](../android/text/Layout.Alignment.md) | [getAlignment](Layout.md))`()` <br /> Returns the alignment used for creating this layout in pixels. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBreakStrategy](Layout.md))`()` <br /> Return the break strategy used for creating this layout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCursorPath](Layout.md))`(`point:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Path](../android.graphics/Path.md)!`, `editingBuffer:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Fills in the specified Path with a representation of a cursor at the specified offset. This will often be a vertical line but can be multiple discontinuous lines in text with multiple directionalities. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDesiredWidth](Layout.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `paint:` ` [TextPaint](TextPaint.md)!`)` <br /> Return how wide a layout must be in order to display the specified text with one line per paragraph. As of O, Uses [TextDirectionHeuristics.FIRSTSTRONG_LTR](TextDirectionHeuristics.md) as the default text direction heuristics. In the earlier versions uses [TextDirectionHeuristics.LTR](TextDirectionHeuristics.md) as the default. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDesiredWidth](Layout.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paint:` ` [TextPaint](TextPaint.md)!`)` <br /> Return how wide a layout must be in order to display the specified text slice with one line per paragraph. As of O, Uses [TextDirectionHeuristics.FIRSTSTRONG_LTR](TextDirectionHeuristics.md) as the default text direction heuristics. In the earlier versions uses [TextDirectionHeuristics.LTR](TextDirectionHeuristics.md) as the default. <br /> | | [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)? | [getEllipsize](Layout.md))`()` <br /> Return the ellipsize option used for creating this layout. May return null if no ellipsize option was selected. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](Layout.md))`()` <br /> Return the total height of this layout. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHyphenationFrequency](Layout.md))`()` <br /> Return the hyphenation frequency used for creating this layout. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJustificationMode](Layout.md))`()` <br /> Return the justification mode used for creating this layout. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getLeftIndents](Layout.md))`()` <br /> Return a copy of the left indents used for this layout. May return null if no left indentation is applied. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineAscent](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the ascent of the text on the specified line. The return value is negative to match the Paint.ascent() convention. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBaseline](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the vertical position of the baseline of the specified line. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBottom](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the vertical position of the bottom of the specified line. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBottom](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `includeLineSpacing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Return the vertical position of the bottom of the specified line. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBounds](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [Rect](../android.graphics/Rect.md)!`)` <br /> Return the baseline for the specified line (0...getLineCount() - 1) If bounds is not null, return the top, left, right, bottom extents of the specified line in it. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineEnd](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the text offset after the last character on the specified line. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineForOffset](Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the line number on which the specified text offset appears. If you ask for a position before 0, you get 0; if you ask for a position beyond the end of the text, you get the last line. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineForVertical](Layout.md))`(`vertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the line number corresponding to the specified vertical position. If you ask for a position above 0, you get 0; if you ask for a position below the bottom of the text, you get the last line. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineLeft](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the leftmost position that should be exposed for horizontal scrolling on the specified line. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineLetterSpacingUnitCount](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `includeTrailingWhitespace:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Returns the number of letter spacing unit in the line. This API returns a number of letters that is a target of letter spacing. The letter spacing won't be added to the middle of the characters that are needed to be treated as a single, e.g., ligatured or conjunct form. Note that this value is different from the number of\] grapheme clusters that is calculated by [BreakIterator.getCharacterInstance(Locale)](../java.text/BreakIterator.md)). For example, if the "fi" is ligatured, the ligatured form is treated as single uni and letter spacing is not added, but it has two separate grapheme cluster. This value is used for calculating the letter spacing amount for the justification because the letter spacing is applied between clusters. For example, if extra`W`pixels needed to be filled by letter spacing, the amount of letter spacing to be applied is`W`/(letter spacing unit count - 1) px. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineMax](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the unsigned horizontal extent of the specified line, including leading margin indent, but excluding trailing whitespace. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineRight](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the rightmost position that should be exposed for horizontal scrolling on the specified line. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineSpacingAmount](Layout.md))`()` <br /> Returns the amount added to the line height. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineSpacingMultiplier](Layout.md))`()` <br /> Returns the multiplier applied to the line height. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineVisibleEnd](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the text offset after the last visible character (so whitespace is not counted) on the specified line. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineWidth](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the unsigned horizontal extent of the specified line, including leading margin indent and trailing whitespace. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxLines](Layout.md))`()` <br /> Return the maximum lines allowed used for creating this layout. Note that this is not an actual line count of this layout. Use [getLineCount()](Layout.md))for getting the actual line count of this layout. <br /> | | [Paint.FontMetrics](../android/graphics/Paint.FontMetrics.md)? | [getMinimumFontMetrics](Layout.md))`()` <br /> Get the minimum font metrics used for line spacing. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetForHorizontal](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `horiz:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Get the character offset on the specified line whose position is closest to the specified horizontal position. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetToLeftOf](Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetToRightOf](Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [TextPaint](TextPaint.md) | [getPaint](Layout.md))`()` <br /> Return the paint used for creating this layout. Do not modify the returned paint object. This paint object will still be used for drawing/measuring text. <br /> | | [Layout.Alignment](../android/text/Layout.Alignment.md)! | [getParagraphAlignment](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the alignment of the specified paragraph, taking into account markup attached to it. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphLeft](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the left edge of the specified paragraph, inset by left margins. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphRight](Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the right edge of the specified paragraph, inset by right margins. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPrimaryHorizontal](Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the primary horizontal position for the specified text offset. This is the location where a new character would be inserted in the paragraph's primary direction. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getRangeForRect](Layout.md))`(`area:` ` [RectF](../android.graphics/RectF.md)`, `segmentFinder:` ` [SegmentFinder](SegmentFinder.md)`, `inclusionStrategy:` ` [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md)`)` <br /> Finds the range of text which is inside the specified rectangle area. The start of the range is the start of the first text segment inside the area, and the end of the range is the end of the last text segment inside the area. A text segment is considered to be inside the area according to the provided [TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md). If a text segment spans multiple lines or multiple directional runs (e.g. a hyphenated word), the text segment is divided into pieces at the line and run breaks, then the text segment is considered to be inside the area if any of its pieces are inside the area. The returned range may also include text segments which are not inside the specified area, if those text segments are in between text segments which are inside the area. For example, the returned range may be "segment1 segment2 segment3" if "segment1" and "segment3" are inside the area and "segment2" is not. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getRightIndents](Layout.md))`()` <br /> Return a copy of the right indents used for this layout. May return null if no right indentation is applied. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSecondaryHorizontal](Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the secondary horizontal position for the specified text offset. This is the location where a new character would be inserted in the direction other than the paragraph's primary direction. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSelectionPath](Layout.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Path](../android.graphics/Path.md)!`)` <br /> Fills in the specified Path with a representation of a highlight between the specified offsets. This will often be a rectangle or a potentially discontinuous set of rectangles. If the start and end are the same, the returned path is empty. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShiftDrawingOffsetForStartOverhang](Layout.md))`()` <br /> Returns true if shifting drawing offset for start overhang. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpacingAdd](Layout.md))`()` <br /> Returns the amount added to the line height. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpacingMultiplier](Layout.md))`()` <br /> Returns the multiplier applied to the line height. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getText](Layout.md))`()` <br /> Return the text used for creating this layout. <br /> | | [TextDirectionHeuristic](TextDirectionHeuristic.md) | [getTextDirectionHeuristic](Layout.md))`()` <br /> Returns the text direction heuristic used for creating this layout. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseBoundsForWidth](Layout.md))`()` <br /> Returns true if using bounding box as a width, false for using advance as a width. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](Layout.md))`()` <br /> Return the width used for creating this layout in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [increaseWidthTo](Layout.md))`(`wid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Increase the width of this layout to the specified width. Be careful to use this only when you know it is appropriate--- it does not cause the text to reflow to use the full new width. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFallbackLineSpacingEnabled](Layout.md))`()` <br /> Return true if the fallback line space is enabled in this Layout. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFontPaddingIncluded](Layout.md))`()` <br /> Returns true if this layout is created with increased line height. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRtlCharAt](Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns true if the character at offset is right to left (RTL). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpanned](Layout.md))`()` <br /> | ||

| Inherited properties ||
|---|---|
| From class [Layout](Layout.md) |--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) | [INCLUSION_STRATEGY_ANY_OVERLAP](Layout.md) <br /> Strategy which considers a text segment to be inside a rectangle area if the segment bounds intersect the rectangle. <br /> | | [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) | [INCLUSION_STRATEGY_CONTAINS_ALL](Layout.md) <br /> Strategy which considers a text segment to be inside a rectangle area if the segment bounds are completely contained within the rectangle. <br /> | | [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) | [INCLUSION_STRATEGY_CONTAINS_CENTER](Layout.md) <br /> Strategy which considers a text segment to be inside a rectangle area if the center of the segment bounds is inside the rectangle. <br /> | ||

## Public constructors

### DynamicLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DynamicLayout(
    base: CharSequence, 
    paint: TextPaint, 
    width: Int, 
    align: Layout.Alignment, 
    spacingmult: Float, 
    spacingadd: Float, 
    includepad: Boolean)
```

**Deprecated:** *Use [Builder](../android/text/DynamicLayout.Builder.md) instead.*

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| `base` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):This value cannot be`null`. |
| `paint` | [TextPaint](TextPaint.md):This value cannot be`null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md):This value cannot be`null`. |
| `spacingmult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Value is 0.0f or greater |

### DynamicLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DynamicLayout(
    base: CharSequence, 
    display: CharSequence, 
    paint: TextPaint, 
    width: Int, 
    align: Layout.Alignment, 
    spacingmult: Float, 
    spacingadd: Float, 
    includepad: Boolean)
```

**Deprecated:** *Use [Builder](../android/text/DynamicLayout.Builder.md) instead.*

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| `base` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):This value cannot be`null`. |
| `display` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):This value cannot be`null`. |
| `paint` | [TextPaint](TextPaint.md):This value cannot be`null`. |
| --- | --- |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md):This value cannot be`null`. |
| `spacingmult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Value is 0.0f or greater |
| --- | --- |

### DynamicLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DynamicLayout(
    base: CharSequence, 
    display: CharSequence, 
    paint: TextPaint, 
    width: Int, 
    align: Layout.Alignment, 
    spacingmult: Float, 
    spacingadd: Float, 
    includepad: Boolean, 
    ellipsize: TextUtils.TruncateAt?, 
    ellipsizedWidth: Int)
```

**Deprecated:** *Use [Builder](../android/text/DynamicLayout.Builder.md) instead.*

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `base` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):This value cannot be`null`. |
| `display` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):This value cannot be`null`. |
| `paint` | [TextPaint](TextPaint.md):This value cannot be`null`. |
| --- | --- |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md):This value cannot be`null`. |
| `spacingmult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Value is 0.0f or greater |
| --- | --- |
| `ellipsize` | [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)?:This value may be`null`. |
| `ellipsizedWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

## Public methods

### getBottomPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBottomPadding(): Int
```  

### getEllipsisCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEllipsisCount(line: Int): Int
```  

### getEllipsisStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEllipsisStart(line: Int): Int
```  

### getEllipsizedWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEllipsizedWidth(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of ellipsized width in pixels. Value is 0 or greater |

### getLineBreakConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineBreakConfig(): LineBreakConfig
```

Gets the [LineBreakConfig](../android.graphics.text/LineBreakConfig.md) used in this DynamicLayout. Use this only to consult the LineBreakConfig's properties and not to change them.

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [LineBreakConfig](../android.graphics.text/LineBreakConfig.md) | The line break config in this DynamicLayout. This value cannot be`null`. |

### getLineContainsTab

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineContainsTab(line: Int): Boolean
```  

### getLineCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineCount(): Int
```  

### getLineDescent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineDescent(line: Int): Int
```  

### getLineDirections

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineDirections(line: Int): Layout.Directions!
```  

### getLineStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineStart(line: Int): Int
```  

### getLineTop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineTop(line: Int): Int
```  

### getParagraphDirection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParagraphDirection(line: Int): Int
```  

### getTopPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTopPadding(): Int
```
