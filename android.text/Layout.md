# Layout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Layout

Kotlin | [Java](../android/text/Layout.md) 
| --- | --- |

```
abstract class Layout
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.Layout](../android/text/Layout.md) |

| Known Direct Subclasses [BoringLayout](../android/text/BoringLayout.md), [DynamicLayout](../android/text/DynamicLayout.md), [StaticLayout](../android/text/StaticLayout.md) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [BoringLayout](../android/text/BoringLayout.md) | A BoringLayout is a very simple Layout implementation for text that fits on a single line and is all left-to-right characters. | | [DynamicLayout](../android/text/DynamicLayout.md) | DynamicLayout is a text layout that updates itself as the text is edited. | | [StaticLayout](../android/text/StaticLayout.md) | StaticLayout is a Layout for text that will not be edited after it is laid out. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A base class that manages text layout in visual elements on the screen.

For text that will be edited, use a [DynamicLayout](../android/text/DynamicLayout.md), which will be updated as the text changes. For text that will not change, use a [StaticLayout](../android/text/StaticLayout.md).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Alignment](../android/text/Layout.Alignment.md) <br /> |
| | [Builder](../android/text/Layout.Builder.md) A builder class for Layout object. |
| open | [Directions](../android/text/Layout.Directions.md) Stores information about bidirectional (left-to-right or right-to-left) text within the layout of a line. |
| --- | --- |
| abstract | [TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) Strategy for determining whether a text segment is inside a rectangle area. |

| Constants ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_BALANCED](../android/text/Layout.md) Value for break strategy indicating balanced line breaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_HIGH_QUALITY](../android/text/Layout.md) Value for break strategy indicating high quality line breaking, including automatic hyphenation and doing whole-paragraph optimization of line breaks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_SIMPLE](../android/text/Layout.md) Value for break strategy indicating simple line breaking. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [DEFAULT_LINESPACING_ADDITION](../android/text/Layout.md) <br /> |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [DEFAULT_LINESPACING_MULTIPLIER](../android/text/Layout.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIR_LEFT_TO_RIGHT](../android/text/Layout.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIR_RIGHT_TO_LEFT](../android/text/Layout.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_FULL](../android/text/Layout.md) Value for hyphenation frequency indicating the full amount of automatic hyphenation, typical in typography. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_FULL_FAST](../android/text/Layout.md) Value for hyphenation frequency indicating the full amount of automatic hyphenation with using faster algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NONE](../android/text/Layout.md) Value for hyphenation frequency indicating no automatic hyphenation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NORMAL](../android/text/Layout.md) Value for hyphenation frequency indicating a light amount of automatic hyphenation, which is a conservative default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NORMAL_FAST](../android/text/Layout.md) Value for hyphenation frequency indicating a light amount of automatic hyphenation with using faster algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_INTER_CHARACTER](../android/text/Layout.md) Value for justification mode indicating the text is justified by stretching letter spacing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_INTER_WORD](../android/text/Layout.md) Value for justification mode indicating the text is justified by stretching word spacing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_NONE](../android/text/Layout.md) Value for justification mode indicating no justification. |
| --- | --- |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Layout](../android/text/Layout.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `paint:` ` [TextPaint](../android/text/TextPaint.md)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `align:` ` [Layout.Alignment](../android/text/Layout.Alignment.md)!`, `spacingMult:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `spacingAdd:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Subclasses of Layout use this constructor to set the display text, width, and other standard properties. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RectF](../android/graphics/RectF.md) | [computeDrawingBoundingBox](../android/text/Layout.md))`()` Get an actual bounding box that draws text content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/text/Layout.md))`(`c:` ` [Canvas](../android/graphics/Canvas.md)!`)` Draw this Layout on the specified Canvas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/text/Layout.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)!`, `selectionHighlight:` ` [Path](../android/graphics/Path.md)!`, `selectionHighlightPaint:` ` [Paint](../android/graphics/Paint.md)!`, `cursorOffsetVertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Draw this Layout on the specified canvas, with the highlight path drawn between the background and the text. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/text/Layout.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)`, `highlightPaths:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Path](../android/graphics/Path.md)!>?`, `highlightPaints:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Paint](../android/graphics/Paint.md)!>?`, `selectionPath:` ` [Path](../android/graphics/Path.md)?`, `selectionPaint:` ` [Paint](../android/graphics/Paint.md)?`, `cursorOffsetVertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Draw this layout on the specified canvas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBackground](../android/text/Layout.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)`)` Draw background of this layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawText](../android/text/Layout.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)`)` Draw text part of this layout. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillCharacterBounds](../android/text/Layout.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `boundsStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the characters' bounds in the given range. |
| [Layout.Alignment](../android/text/Layout.Alignment.md) | [getAlignment](../android/text/Layout.md))`()` Returns the alignment used for creating this layout in pixels. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBottomPadding](../android/text/Layout.md))`()` Returns the number of extra pixels of descent padding in the bottom line of the Layout. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBreakStrategy](../android/text/Layout.md))`()` Return the break strategy used for creating this layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCursorPath](../android/text/Layout.md))`(`point:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Path](../android/graphics/Path.md)!`, `editingBuffer:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Fills in the specified Path with a representation of a cursor at the specified offset. |
| open static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDesiredWidth](../android/text/Layout.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `paint:` ` [TextPaint](../android/text/TextPaint.md)!`)` Return how wide a layout must be in order to display the specified text with one line per paragraph. |
| --- | --- |
| open static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDesiredWidth](../android/text/Layout.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paint:` ` [TextPaint](../android/text/TextPaint.md)!`)` Return how wide a layout must be in order to display the specified text slice with one line per paragraph. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsisCount](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the number of characters to be ellipsized away, or 0 if no ellipsis is to take place. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsisStart](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the offset of the first character to be ellipsized away, relative to the start of the line. |
| --- | --- |
| [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)? | [getEllipsize](../android/text/Layout.md))`()` Return the ellipsize option used for creating this layout. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsizedWidth](../android/text/Layout.md))`()` Return the width to which this layout is ellipsized. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](../android/text/Layout.md))`()` Return the total height of this layout. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHyphenationFrequency](../android/text/Layout.md))`()` Return the hyphenation frequency used for creating this layout. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJustificationMode](../android/text/Layout.md))`()` Return the justification mode used for creating this layout. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getLeftIndents](../android/text/Layout.md))`()` Return a copy of the left indents used for this layout. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineAscent](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the ascent of the text on the specified line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBaseline](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the vertical position of the baseline of the specified line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBottom](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the vertical position of the bottom of the specified line. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBottom](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `includeLineSpacing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return the vertical position of the bottom of the specified line. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBounds](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [Rect](../android/graphics/Rect.md)!`)` Return the baseline for the specified line (0...getLineCount() - 1) If bounds is not null, return the top, left, right, bottom extents of the specified line in it. |
| open [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) | [getLineBreakConfig](../android/text/Layout.md))`()` Gets the [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) used for creating this layout. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLineContainsTab](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns whether the specified line contains one or more characters that need to be handled specially, like tabs. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineCount](../android/text/Layout.md))`()` Return the number of lines of text in this layout. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineDescent](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the descent of the specified line(0...getLineCount() - 1). |
| --- | --- |
| abstract [Layout.Directions](../android/text/Layout.Directions.md)! | [getLineDirections](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the directional run information for the specified line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineEnd](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the text offset after the last character on the specified line. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineForOffset](../android/text/Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the line number on which the specified text offset appears. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineForVertical](../android/text/Layout.md))`(`vertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the line number corresponding to the specified vertical position. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineLeft](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the leftmost position that should be exposed for horizontal scrolling on the specified line. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineLetterSpacingUnitCount](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `includeTrailingWhitespace:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the number of letter spacing unit in the line. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineMax](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the unsigned horizontal extent of the specified line, including leading margin indent, but excluding trailing whitespace. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineRight](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the rightmost position that should be exposed for horizontal scrolling on the specified line. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineSpacingAmount](../android/text/Layout.md))`()` Returns the amount added to the line height. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineSpacingMultiplier](../android/text/Layout.md))`()` Returns the multiplier applied to the line height. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineStart](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the text offset of the beginning of the specified line ( 0...getLineCount()). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineTop](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the vertical position of the top of the specified line (0...getLineCount()). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineVisibleEnd](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the text offset after the last visible character (so whitespace is not counted) on the specified line. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineWidth](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the unsigned horizontal extent of the specified line, including leading margin indent and trailing whitespace. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxLines](../android/text/Layout.md))`()` Return the maximum lines allowed used for creating this layout. |
| --- | --- |
| open [Paint.FontMetrics](../android/graphics/Paint.FontMetrics.md)? | [getMinimumFontMetrics](../android/text/Layout.md))`()` Get the minimum font metrics used for line spacing. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetForHorizontal](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `horiz:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Get the character offset on the specified line whose position is closest to the specified horizontal position. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetToLeftOf](../android/text/Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetToRightOf](../android/text/Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [TextPaint](../android/text/TextPaint.md) | [getPaint](../android/text/Layout.md))`()` Return the paint used for creating this layout. |
| [Layout.Alignment](../android/text/Layout.Alignment.md)! | [getParagraphAlignment](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the alignment of the specified paragraph, taking into account markup attached to it. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphDirection](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the primary directionality of the paragraph containing the specified line, either 1 for left-to-right lines, or -1 for right-to-left lines (see [DIR_LEFT_TO_RIGHT](../android/text/Layout.md), [DIR_RIGHT_TO_LEFT](../android/text/Layout.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphLeft](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the left edge of the specified paragraph, inset by left margins. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphRight](../android/text/Layout.md))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the right edge of the specified paragraph, inset by right margins. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPrimaryHorizontal](../android/text/Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the primary horizontal position for the specified text offset. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getRangeForRect](../android/text/Layout.md))`(`area:` ` [RectF](../android/graphics/RectF.md)`, `segmentFinder:` ` [SegmentFinder](../android/text/SegmentFinder.md)`, `inclusionStrategy:` ` [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md)`)` Finds the range of text which is inside the specified rectangle area. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getRightIndents](../android/text/Layout.md))`()` Return a copy of the right indents used for this layout. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSecondaryHorizontal](../android/text/Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the secondary horizontal position for the specified text offset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSelectionPath](../android/text/Layout.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Path](../android/graphics/Path.md)!`)` Fills in the specified Path with a representation of a highlight between the specified offsets. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShiftDrawingOffsetForStartOverhang](../android/text/Layout.md))`()` Returns true if shifting drawing offset for start overhang. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpacingAdd](../android/text/Layout.md))`()` Returns the amount added to the line height. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpacingMultiplier](../android/text/Layout.md))`()` Returns the multiplier applied to the line height. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getText](../android/text/Layout.md))`()` Return the text used for creating this layout. |
| --- | --- |
| [TextDirectionHeuristic](../android/text/TextDirectionHeuristic.md) | [getTextDirectionHeuristic](../android/text/Layout.md))`()` Returns the text direction heuristic used for creating this layout. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTopPadding](../android/text/Layout.md))`()` Returns the (negative) number of extra pixels of ascent padding in the top line of the Layout. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseBoundsForWidth](../android/text/Layout.md))`()` Returns true if using bounding box as a width, false for using advance as a width. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](../android/text/Layout.md))`()` Return the width used for creating this layout in pixels. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [increaseWidthTo](../android/text/Layout.md))`(`wid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increase the width of this layout to the specified width. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFallbackLineSpacingEnabled](../android/text/Layout.md))`()` Return true if the fallback line space is enabled in this Layout. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFontPaddingIncluded](../android/text/Layout.md))`()` Returns true if this layout is created with increased line height. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRtlCharAt](../android/text/Layout.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the character at offset is right to left (RTL). |

| Protected methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpanned](../android/text/Layout.md))`()` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) | [INCLUSION_STRATEGY_ANY_OVERLAP](../android/text/Layout.md) Strategy which considers a text segment to be inside a rectangle area if the segment bounds intersect the rectangle. |
| static [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) | [INCLUSION_STRATEGY_CONTAINS_ALL](../android/text/Layout.md) Strategy which considers a text segment to be inside a rectangle area if the segment bounds are completely contained within the rectangle. |
| static [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) | [INCLUSION_STRATEGY_CONTAINS_CENTER](../android/text/Layout.md) Strategy which considers a text segment to be inside a rectangle area if the center of the segment bounds is inside the rectangle. |
| --- | --- |

## Constants

### BREAK_STRATEGY_BALANCED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BREAK_STRATEGY_BALANCED: Int
```

Value for break strategy indicating balanced line breaking. The breaks are chosen to make all lines as close to the same length as possible, including automatic hyphenation. 

 Value: 2

### BREAK_STRATEGY_HIGH_QUALITY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BREAK_STRATEGY_HIGH_QUALITY: Int
```

Value for break strategy indicating high quality line breaking, including automatic hyphenation and doing whole-paragraph optimization of line breaks. 

 Value: 1

### BREAK_STRATEGY_SIMPLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BREAK_STRATEGY_SIMPLE: Int
```

Value for break strategy indicating simple line breaking. Automatic hyphens are not added (though soft hyphens are respected), and modifying text generally doesn't affect the layout before it (which yields a more consistent user experience when editing), but layout may not be the highest quality. 

 Value: 0

### DEFAULT_LINESPACING_ADDITION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_LINESPACING_ADDITION: Float
```  

 Value: 0.0f

### DEFAULT_LINESPACING_MULTIPLIER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_LINESPACING_MULTIPLIER: Float
```  

 Value: 1.0f

### DIR_LEFT_TO_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIR_LEFT_TO_RIGHT: Int
```  

 Value: 1

### DIR_RIGHT_TO_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIR_RIGHT_TO_LEFT: Int
```  

 Value: -1

### HYPHENATION_FREQUENCY_FULL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHENATION_FREQUENCY_FULL: Int
```

Value for hyphenation frequency indicating the full amount of automatic hyphenation, typical in typography. Useful for running text and where it's important to put the maximum amount of text in a screen with limited space. 

 Value: 2

### HYPHENATION_FREQUENCY_FULL_FAST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHENATION_FREQUENCY_FULL_FAST: Int
```

Value for hyphenation frequency indicating the full amount of automatic hyphenation with using faster algorithm. This option is useful for running text and where it's important to put the maximum amount of text in a screen with limited space. To make text rendering faster with hyphenation, this algorithm ignores some hyphen character related typographic features, e.g. kerning. 

 Value: 4

### HYPHENATION_FREQUENCY_NONE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHENATION_FREQUENCY_NONE: Int
```

Value for hyphenation frequency indicating no automatic hyphenation. Useful for backward compatibility, and for cases where the automatic hyphenation algorithm results in incorrect hyphenation. Mid-word breaks may still happen when a word is wider than the layout and there is otherwise no valid break. Soft hyphens are ignored and will not be used as suggestions for potential line breaks. 

 Value: 0

### HYPHENATION_FREQUENCY_NORMAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHENATION_FREQUENCY_NORMAL: Int
```

Value for hyphenation frequency indicating a light amount of automatic hyphenation, which is a conservative default. Useful for informal cases, such as short sentences or chat messages. 

 Value: 1

### HYPHENATION_FREQUENCY_NORMAL_FAST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHENATION_FREQUENCY_NORMAL_FAST: Int
```

Value for hyphenation frequency indicating a light amount of automatic hyphenation with using faster algorithm. This option is useful for informal cases, such as short sentences or chat messages. To make text rendering faster with hyphenation, this algorithm ignores some hyphen character related typographic features, e.g. kerning. 

 Value: 3

### JUSTIFICATION_MODE_INTER_CHARACTER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION_MODE_INTER_CHARACTER: Int
```

Value for justification mode indicating the text is justified by stretching letter spacing. 

 Value: 2

### JUSTIFICATION_MODE_INTER_WORD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION_MODE_INTER_WORD: Int
```

Value for justification mode indicating the text is justified by stretching word spacing. 

 Value: 1

### JUSTIFICATION_MODE_NONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION_MODE_NONE: Int
```

Value for justification mode indicating no justification. 

 Value: 0

## Protected constructors

### Layout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Layout(
    text: CharSequence!, 
    paint: TextPaint!, 
    width: Int, 
    align: Layout.Alignment!, 
    spacingMult: Float, 
    spacingAdd: Float)
```

Subclasses of Layout use this constructor to set the display text, width, and other standard properties.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to render |
| `paint` | [TextPaint](../android/text/TextPaint.md)!: the default paint for the layout. Styles can override various attributes of the paint. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text. |
| --- | --- |
| `align` | [Layout.Alignment](../android/text/Layout.Alignment.md)!: whether to left, right, or center the text. Styles can override the alignment. |
| `spacingMult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): factor by which to scale the font size to get the default line spacing |
| `spacingAdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): amount to add to the default line spacing |
| --- | --- |

## Public methods

### computeDrawingBoundingBox

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeDrawingBoundingBox(): RectF
```

Get an actual bounding box that draws text content. Note that the [RectF.top](../android/graphics/RectF.md) and [RectF.bottom](../android/graphics/RectF.md) may be different from the [Layout.getLineTop(int)](../android/text/Layout.md)) of the first line and [Layout.getLineBottom(int)](../android/text/Layout.md)) of the last line. The line top and line bottom are calculated based on yMin/yMax or ascent/descent value of font file. On the other hand, the drawing bounding boxes are calculated based on actual glyphs used there.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------------------|
| [RectF](../android/graphics/RectF.md) | bounding rectangle This value cannot be `null`. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(c: Canvas!): Unit
```

Draw this Layout on the specified Canvas. This API draws background first, then draws text on top of it. 
**See Also**

- [#draw(Canvas, List, List, Path, Paint, int)](../android/text/Layout.md)) 

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    selectionHighlight: Path!, 
    selectionHighlightPaint: Paint!, 
    cursorOffsetVertical: Int
): Unit
```

Draw this Layout on the specified canvas, with the highlight path drawn between the background and the text.

| Parameters ||
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md)!: the canvas |
| `selectionHighlight` | [Path](../android/graphics/Path.md)!: the path of the selection highlight or cursor; can be null |
| `selectionHighlightPaint` | [Paint](../android/graphics/Paint.md)!: the paint for the selection highlight |
| --- | --- |
| `cursorOffsetVertical` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount to temporarily translate the canvas while rendering the highlight |

**See Also**

- [#draw(Canvas, List, List, Path, Paint, int)](../android/text/Layout.md)) 

### draw

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas, 
    highlightPaths: MutableList<Path!>?, 
    highlightPaints: MutableList<Paint!>?, 
    selectionPath: Path?, 
    selectionPaint: Paint?, 
    cursorOffsetVertical: Int
): Unit
```

Draw this layout on the specified canvas. This API draws background first, then draws highlight paths on top of it, then draws selection or cursor, then finally draws text on top of it.

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md): the canvas This value cannot be `null`. |
| `highlightPaths` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Path](../android/graphics/Path.md)!\>?: the path of the highlights. The highlightPaths and highlightPaints must have the same length and aligned in the same order. For example, the paint of the n-th of the highlightPaths should be stored at the n-th of highlightPaints. This value may be `null`. |
| `highlightPaints` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Paint](../android/graphics/Paint.md)!\>?: the paints for the highlights. The highlightPaths and highlightPaints must have the same length and aligned in the same order. For example, the paint of the n-th of the highlightPaths should be stored at the n-th of highlightPaints. This value may be `null`. |
| --- | --- |
| `selectionPath` | [Path](../android/graphics/Path.md)?: the selection or cursor path This value may be `null`. |
| `selectionPaint` | [Paint](../android/graphics/Paint.md)?: the paint for the selection or cursor. This value may be `null`. |
| `cursorOffsetVertical` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount to temporarily translate the canvas while rendering the highlight |
| --- | --- |

**See Also**

- [#drawBackground(Canvas)](../android/text/Layout.md))
- [#drawText(Canvas)](../android/text/Layout.md)) 

### drawBackground

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBackground(canvas: Canvas): Unit
```

Draw background of this layout. Different from [draw(android.graphics.Canvas,java.util.List,java.util.List,android.graphics.Path,android.graphics.Paint,int)](../android/text/Layout.md)) API, this API only draws background, not drawing text, highlights or selections. The background here is drawn by [LineBackgroundSpan](../android/text/style/LineBackgroundSpan.md) attached to the text.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md): the canvas This value cannot be `null`. |

**See Also**

- [#draw(Canvas, List, List, Path, Paint, int)](../android/text/Layout.md))
- [#drawText(Canvas)](../android/text/Layout.md)) 

### drawText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawText(canvas: Canvas): Unit
```

Draw text part of this layout. Different from [draw(android.graphics.Canvas,java.util.List,java.util.List,android.graphics.Path,android.graphics.Paint,int)](../android/text/Layout.md)) API, this API only draws text part, not drawing highlights, selections, or backgrounds.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md): the canvas This value cannot be `null`. |

**See Also**

- [#draw(Canvas, List, List, Path, Paint, int)](../android/text/Layout.md))
- [#drawBackground(Canvas)](../android/text/Layout.md)) 

### fillCharacterBounds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fillCharacterBounds(
    start: Int, 
    end: Int, 
    bounds: FloatArray, 
    boundsStart: Int
): Unit
```

Return the characters' bounds in the given range. The `bounds` array will be filled starting from `boundsStart` (inclusive). The coordinates are in local text layout.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start index to compute the character bounds, inclusive. Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end index to compute the character bounds, exclusive. Value is 0 or greater |
| `bounds` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to fill in the character bounds. The array is divided into segments of four where each index in that segment represents left, top, right and bottom of the character. This value cannot be `null`. |
| --- | --- |
| `boundsStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the inclusive start index in the array to start filling in the values from. Value is 0 or greater |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the range defined by `start` and `end` exceeds the range of the text, or `bounds` doesn't have enough space to store the result. |
| `java.lang.IllegalArgumentException` | if `bounds` is null. |

### getAlignment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlignment(): Layout.Alignment
```

Returns the alignment used for creating this layout in pixels.

| Return ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Layout.Alignment](../android/text/Layout.Alignment.md) | the alignment used for creating this layout. This value cannot be `null`. |

**See Also**

- [android.text.StaticLayout.Builder#setAlignment(Alignment)](../android/text/StaticLayout.Builder.md)) 

### getBottomPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBottomPadding(): Int
```

Returns the number of extra pixels of descent padding in the bottom line of the Layout. 

### getBreakStrategy

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBreakStrategy(): Int
```

Return the break strategy used for creating this layout.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the break strategy used for creating this layout. Value is [android.graphics.text.LineBreaker#BREAK_STRATEGY_SIMPLE](../android/graphics/text/LineBreaker.md), [android.graphics.text.LineBreaker#BREAK_STRATEGY_HIGH_QUALITY](../android/graphics/text/LineBreaker.md), or [android.graphics.text.LineBreaker#BREAK_STRATEGY_BALANCED](../android/graphics/text/LineBreaker.md) |

**See Also**

- [android.text.Layout.Builder#setBreakStrategy(int)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setBreakStrategy(int)](../android/text/StaticLayout.Builder.md)) 

### getCursorPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCursorPath(
    point: Int, 
    dest: Path!, 
    editingBuffer: CharSequence!
): Unit
```

Fills in the specified Path with a representation of a cursor at the specified offset. This will often be a vertical line but can be multiple discontinuous lines in text with multiple directionalities. 

### getDesiredWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDesiredWidth(
    source: CharSequence!, 
    paint: TextPaint!
): Float
```

Return how wide a layout must be in order to display the specified text with one line per paragraph.

As of O, Uses [TextDirectionHeuristics.FIRSTSTRONG_LTR](../android/text/TextDirectionHeuristics.md) as the default text direction heuristics. In the earlier versions uses [TextDirectionHeuristics.LTR](../android/text/TextDirectionHeuristics.md) as the default. 

### getDesiredWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDesiredWidth(
    source: CharSequence!, 
    start: Int, 
    end: Int, 
    paint: TextPaint!
): Float
```

Return how wide a layout must be in order to display the specified text slice with one line per paragraph.

As of O, Uses [TextDirectionHeuristics.FIRSTSTRONG_LTR](../android/text/TextDirectionHeuristics.md) as the default text direction heuristics. In the earlier versions uses [TextDirectionHeuristics.LTR](../android/text/TextDirectionHeuristics.md) as the default. 

### getEllipsisCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEllipsisCount(line: Int): Int
```

Returns the number of characters to be ellipsized away, or 0 if no ellipsis is to take place. 

### getEllipsisStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEllipsisStart(line: Int): Int
```

Return the offset of the first character to be ellipsized away, relative to the start of the line. (So 0 if the beginning of the line is ellipsized, not getLineStart().) 

### getEllipsize

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEllipsize(): TextUtils.TruncateAt?
```

Return the ellipsize option used for creating this layout. May return null if no ellipsize option was selected.

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [TextUtils.TruncateAt](../android/text/TextUtils.TruncateAt.md)? | The ellipsize option used for creating this layout, or null if no ellipsize option was selected. |

**See Also**

- [android.text.Layout.Builder#setEllipsize(TextUtils.TruncateAt)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setEllipsize(TextUtils.TruncateAt)](../android/text/StaticLayout.Builder.md))
- [android.text.Layout.Builder#setEllipsizedWidth(int)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setEllipsizedWidth(int)](../android/text/StaticLayout.Builder.md))
- [android.text.Layout#getEllipsizedWidth()](../android/text/Layout.md)) 

### getEllipsizedWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEllipsizedWidth(): Int
```

Return the width to which this layout is ellipsized. If no ellipsize is applied, the same amount of [getWidth](../android/text/Layout.md)) is returned.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of ellipsized width in pixels. Value is 0 or greater |

**See Also**

- [android.text.StaticLayout.Builder#setEllipsizedWidth(int)](../android/text/StaticLayout.Builder.md))
- [android.text.StaticLayout.Builder#setEllipsize(TextUtils.TruncateAt)](../android/text/StaticLayout.Builder.md)) 

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

Return the total height of this layout. 

### getHyphenationFrequency

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHyphenationFrequency(): Int
```

Return the hyphenation frequency used for creating this layout.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hyphenation frequency used for creating this layout. Value is [android.text.Layout#HYPHENATION_FREQUENCY_NORMAL](../android/text/Layout.md), [android.text.Layout#HYPHENATION_FREQUENCY_NORMAL_FAST](../android/text/Layout.md), [android.text.Layout#HYPHENATION_FREQUENCY_FULL](../android/text/Layout.md), [android.text.Layout#HYPHENATION_FREQUENCY_FULL_FAST](../android/text/Layout.md), or [android.text.Layout#HYPHENATION_FREQUENCY_NONE](../android/text/Layout.md) |

**See Also**

- [android.text.Layout.Builder#setHyphenationFrequency(int)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setHyphenationFrequency(int)](../android/text/StaticLayout.Builder.md)) 

### getJustificationMode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getJustificationMode(): Int
```

Return the justification mode used for creating this layout.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the justification mode used for creating this layout. Value is [android.graphics.text.LineBreaker#JUSTIFICATION_MODE_NONE](../android/graphics/text/LineBreaker.md), [android.graphics.text.LineBreaker#JUSTIFICATION_MODE_INTER_WORD](../android/graphics/text/LineBreaker.md), or [android.graphics.text.LineBreaker#JUSTIFICATION_MODE_INTER_CHARACTER](../android/graphics/text/LineBreaker.md) |

**See Also**

- [android.text.Layout.Builder#setJustificationMode(int)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setJustificationMode(int)](../android/text/StaticLayout.Builder.md)) 

### getLeftIndents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLeftIndents(): IntArray?
```

Return a copy of the left indents used for this layout. May return null if no left indentation is applied.

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | the array of left indents in pixels. |

**See Also**

- [android.text.Layout.Builder#setLeftIndents(int[])](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setLeftIndents(kotlin.IntArray))
- [android.text.Layout.Builder#setRightIndents(int[])](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setRightIndents(kotlin.IntArray))
- [android.text.StaticLayout.Builder#setIndents(int[], int[])](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setIndents(kotlin.IntArray,%20kotlin.IntArray)) 

### getLineAscent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineAscent(line: Int): Int
```

Get the ascent of the text on the specified line. The return value is negative to match the Paint.ascent() convention. 

### getLineBaseline

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineBaseline(line: Int): Int
```

Return the vertical position of the baseline of the specified line. 

### getLineBottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineBottom(line: Int): Int
```

Return the vertical position of the bottom of the specified line. 

### getLineBottom

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineBottom(
    line: Int, 
    includeLineSpacing: Boolean
): Int
```

Return the vertical position of the bottom of the specified line.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------|
| `line` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the line |
| `includeLineSpacing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to include the line spacing |

### getLineBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineBounds(
    line: Int, 
    bounds: Rect!
): Int
```

Return the baseline for the specified line (0...getLineCount() - 1) If bounds is not null, return the top, left, right, bottom extents of the specified line in it.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `line` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): which line to examine (0..getLineCount() - 1) |
| `bounds` | [Rect](../android/graphics/Rect.md)!: Optional. If not null, it returns the extent of the line |

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Y-coordinate of the baseline |

### getLineBreakConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineBreakConfig(): LineBreakConfig
```

Gets the [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) used for creating this layout. Do not modify the returned object.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) | The line break config used for creating this layout. This value cannot be `null`. |

### getLineContainsTab

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineContainsTab(line: Int): Boolean
```

Returns whether the specified line contains one or more characters that need to be handled specially, like tabs. 

### getLineCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineCount(): Int
```

Return the number of lines of text in this layout. 

### getLineDescent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineDescent(line: Int): Int
```

Return the descent of the specified line(0...getLineCount() - 1). 

### getLineDirections

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineDirections(line: Int): Layout.Directions!
```

Returns the directional run information for the specified line. The array alternates counts of characters in left-to-right and right-to-left segments of the line.

NOTE: this is inadequate to support bidirectional text, and will change. 

### getLineEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineEnd(line: Int): Int
```

Return the text offset after the last character on the specified line. 

### getLineForOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineForOffset(offset: Int): Int
```

Get the line number on which the specified text offset appears. If you ask for a position before 0, you get 0; if you ask for a position beyond the end of the text, you get the last line. 

### getLineForVertical

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineForVertical(vertical: Int): Int
```

Get the line number corresponding to the specified vertical position. If you ask for a position above 0, you get 0; if you ask for a position below the bottom of the text, you get the last line. 

### getLineLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineLeft(line: Int): Float
```

Get the leftmost position that should be exposed for horizontal scrolling on the specified line. 

### getLineLetterSpacingUnitCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineLetterSpacingUnitCount(
    line: Int, 
    includeTrailingWhitespace: Boolean
): Int
```

Returns the number of letter spacing unit in the line.

This API returns a number of letters that is a target of letter spacing. The letter spacing won't be added to the middle of the characters that are needed to be treated as a single, e.g., ligatured or conjunct form. Note that this value is different from the number of\] grapheme clusters that is calculated by [BreakIterator.getCharacterInstance(Locale)](../java/text/BreakIterator.md)). For example, if the "fi" is ligatured, the ligatured form is treated as single uni and letter spacing is not added, but it has two separate grapheme cluster.

This value is used for calculating the letter spacing amount for the justification because the letter spacing is applied between clusters. For example, if extra `W` pixels needed to be filled by letter spacing, the amount of letter spacing to be applied is `W`/(letter spacing unit count - 1) px.

| Parameters ||
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `line` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the line Value is 0 or greater |
| `includeTrailingWhitespace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to include trailing whitespace |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of cluster count in the line. Value is 0 or greater |

### getLineMax

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineMax(line: Int): Float
```

Gets the unsigned horizontal extent of the specified line, including leading margin indent, but excluding trailing whitespace. 

### getLineRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineRight(line: Int): Float
```

Get the rightmost position that should be exposed for horizontal scrolling on the specified line. 

### getLineSpacingAmount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineSpacingAmount(): Float
```

Returns the amount added to the line height.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the line height additional amount. |

**See Also**

- [android.text.Layout.Builder#setLineSpacingAmount(float)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setLineSpacing(float, float)](../android/text/StaticLayout.Builder.md))
- [android.text.Layout#getSpacingAdd()](../android/text/Layout.md)) 

### getLineSpacingMultiplier

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineSpacingMultiplier(): Float
```

Returns the multiplier applied to the line height.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the line height multiplier. |

**See Also**

- [android.text.Layout.Builder#setLineSpacingMultiplier(float)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setLineSpacing(float, float)](../android/text/StaticLayout.Builder.md))
- [android.text.Layout#getSpacingMultiplier()](../android/text/Layout.md)) 

### getLineStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineStart(line: Int): Int
```

Return the text offset of the beginning of the specified line ( 0...getLineCount()). If the specified line is equal to the line count, returns the length of the text. 

### getLineTop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineTop(line: Int): Int
```

Return the vertical position of the top of the specified line (0...getLineCount()). If the specified line is equal to the line count, returns the bottom of the last line. 

### getLineVisibleEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineVisibleEnd(line: Int): Int
```

Return the text offset after the last visible character (so whitespace is not counted) on the specified line. 

### getLineWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineWidth(line: Int): Float
```

Gets the unsigned horizontal extent of the specified line, including leading margin indent and trailing whitespace. 

### getMaxLines

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxLines(): Int
```

Return the maximum lines allowed used for creating this layout. Note that this is not an actual line count of this layout. Use [getLineCount()](../android/text/Layout.md)) for getting the actual line count of this layout.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum lines allowed used for creating this layout. Value is 1 or greater |

**See Also**

- [android.text.Layout.Builder#setMaxLines(int)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setMaxLines(int)](../android/text/StaticLayout.Builder.md)) 

### getMinimumFontMetrics

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumFontMetrics(): Paint.FontMetrics?
```

Get the minimum font metrics used for line spacing.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Paint.FontMetrics](../android/graphics/Paint.FontMetrics.md)? | a minimum font metrics. `null` for using the value obtained by [Paint.getFontMetricsForLocale(Paint.FontMetrics)](../android/graphics/Paint.md)) |

**See Also**

- [android.widget.TextView#setMinimumFontMetrics(Paint.FontMetrics)](../android/widget/TextView.md))
- [android.widget.TextView#getMinimumFontMetrics()](../android/widget/TextView.md))
- [android.text.Layout.Builder#setMinimumFontMetrics(Paint.FontMetrics)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setMinimumFontMetrics(Paint.FontMetrics)](../android/text/StaticLayout.Builder.md))
- [android.text.DynamicLayout.Builder#setMinimumFontMetrics(Paint.FontMetrics)](../android/text/DynamicLayout.Builder.md)) 

### getOffsetForHorizontal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOffsetForHorizontal(
    line: Int, 
    horiz: Float
): Int
```

Get the character offset on the specified line whose position is closest to the specified horizontal position. 

### getOffsetToLeftOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOffsetToLeftOf(offset: Int): Int
```  

### getOffsetToRightOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOffsetToRightOf(offset: Int): Int
```  

### getPaint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPaint(): TextPaint
```

Return the paint used for creating this layout. Do not modify the returned paint object. This paint object will still be used for drawing/measuring text.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [TextPaint](../android/text/TextPaint.md) | the paint used for creating this layout. This value cannot be `null`. |

### getParagraphAlignment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParagraphAlignment(line: Int): Layout.Alignment!
```

Get the alignment of the specified paragraph, taking into account markup attached to it. 

### getParagraphDirection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParagraphDirection(line: Int): Int
```

Returns the primary directionality of the paragraph containing the specified line, either 1 for left-to-right lines, or -1 for right-to-left lines (see [DIR_LEFT_TO_RIGHT](../android/text/Layout.md), [DIR_RIGHT_TO_LEFT](../android/text/Layout.md)). 

### getParagraphLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParagraphLeft(line: Int): Int
```

Get the left edge of the specified paragraph, inset by left margins. 

### getParagraphRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParagraphRight(line: Int): Int
```

Get the right edge of the specified paragraph, inset by right margins. 

### getPrimaryHorizontal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryHorizontal(offset: Int): Float
```

Get the primary horizontal position for the specified text offset. This is the location where a new character would be inserted in the paragraph's primary direction. 

### getRangeForRect

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRangeForRect(
    area: RectF, 
    segmentFinder: SegmentFinder, 
    inclusionStrategy: Layout.TextInclusionStrategy
): IntArray?
```

Finds the range of text which is inside the specified rectangle area. The start of the range is the start of the first text segment inside the area, and the end of the range is the end of the last text segment inside the area.

A text segment is considered to be inside the area according to the provided [TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md). If a text segment spans multiple lines or multiple directional runs (e.g. a hyphenated word), the text segment is divided into pieces at the line and run breaks, then the text segment is considered to be inside the area if any of its pieces are inside the area.

The returned range may also include text segments which are not inside the specified area, if those text segments are in between text segments which are inside the area. For example, the returned range may be "segment1 segment2 segment3" if "segment1" and "segment3" are inside the area and "segment2" is not.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `area` | [RectF](../android/graphics/RectF.md): area for which the text range will be found This value cannot be `null`. |
| `segmentFinder` | [SegmentFinder](../android/text/SegmentFinder.md): SegmentFinder for determining the ranges of text to be considered as a text segment This value cannot be `null`. |
| `inclusionStrategy` | [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md): strategy for determining whether a text segment is inside the specified area This value cannot be `null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | int array of size 2 containing the start (inclusive) and end (exclusive) character offsets of the text range, or null if there are no text segments inside the area |

### getRightIndents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRightIndents(): IntArray?
```

Return a copy of the right indents used for this layout. May return null if no right indentation is applied.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | the array of right indents in pixels. |

**See Also**

- [android.text.Layout.Builder#setLeftIndents(int[])](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setLeftIndents(kotlin.IntArray))
- [android.text.Layout.Builder#setRightIndents(int[])](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setRightIndents(kotlin.IntArray))
- [android.text.StaticLayout.Builder#setIndents(int[], int[])](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setIndents(kotlin.IntArray,%20kotlin.IntArray)) 

### getSecondaryHorizontal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSecondaryHorizontal(offset: Int): Float
```

Get the secondary horizontal position for the specified text offset. This is the location where a new character would be inserted in the direction other than the paragraph's primary direction. 

### getSelectionPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectionPath(
    start: Int, 
    end: Int, 
    dest: Path!
): Unit
```

Fills in the specified Path with a representation of a highlight between the specified offsets. This will often be a rectangle or a potentially discontinuous set of rectangles. If the start and end are the same, the returned path is empty. 

### getShiftDrawingOffsetForStartOverhang

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShiftDrawingOffsetForStartOverhang(): Boolean
```

Returns true if shifting drawing offset for start overhang.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if shifting drawing offset for start overhang. |

**See Also**

- [android.widget.TextView#setShiftDrawingOffsetForStartOverhang(boolean)](../android/widget/TextView.md))
- [android.widget.TextView#getShiftDrawingOffsetForStartOverhang()](../android/widget/TextView.md))
- [android.text.StaticLayout.Builder#setShiftDrawingOffsetForStartOverhang(boolean)](../android/text/StaticLayout.Builder.md))
- [android.text.DynamicLayout.Builder#setShiftDrawingOffsetForStartOverhang(boolean)](../android/text/DynamicLayout.Builder.md)) 

### getSpacingAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSpacingAdd(): Float
```

Returns the amount added to the line height.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the line height additional amount. |

**See Also**

- [android.text.StaticLayout.Builder#setLineSpacing(float, float)](../android/text/StaticLayout.Builder.md)) 

### getSpacingMultiplier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSpacingMultiplier(): Float
```

Returns the multiplier applied to the line height.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the line height multiplier. |

**See Also**

- [android.text.StaticLayout.Builder#setLineSpacing(float, float)](../android/text/StaticLayout.Builder.md)) 

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getText(): CharSequence
```

Return the text used for creating this layout.

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the text used for creating this layout. This value cannot be `null`. |

### getTextDirectionHeuristic

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTextDirectionHeuristic(): TextDirectionHeuristic
```

Returns the text direction heuristic used for creating this layout.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [TextDirectionHeuristic](../android/text/TextDirectionHeuristic.md) | the text direction heuristic used for creating this layout This value cannot be `null`. |

**See Also**

- [android.text.Layout.Builder#setTextDirectionHeuristic(TextDirectionHeuristic)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setTextDirection(TextDirectionHeuristic)](../android/text/StaticLayout.Builder.md)) 

### getTopPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTopPadding(): Int
```

Returns the (negative) number of extra pixels of ascent padding in the top line of the Layout. 

### getUseBoundsForWidth

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUseBoundsForWidth(): Boolean
```

Returns true if using bounding box as a width, false for using advance as a width.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if using bounding box for width, false if using advance for width. |

**See Also**

- [android.widget.TextView#setUseBoundsForWidth(boolean)](../android/widget/TextView.md))
- [android.widget.TextView#getUseBoundsForWidth()](../android/widget/TextView.md))
- [android.text.StaticLayout.Builder#setUseBoundsForWidth(boolean)](../android/text/StaticLayout.Builder.md))
- [android.text.DynamicLayout.Builder#setUseBoundsForWidth(boolean)](../android/text/DynamicLayout.Builder.md)) 

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

Return the width used for creating this layout in pixels.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the width used for creating this layout in pixels. Value is 0 or greater |

### increaseWidthTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun increaseWidthTo(wid: Int): Unit
```

Increase the width of this layout to the specified width. Be careful to use this only when you know it is appropriate--- it does not cause the text to reflow to use the full new width. 

### isFallbackLineSpacingEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFallbackLineSpacingEnabled(): Boolean
```

Return true if the fallback line space is enabled in this Layout.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the fallback line space is enabled. Otherwise, returns false. |

**See Also**

- [android.text.StaticLayout.Builder#setUseLineSpacingFromFallbacks(boolean)](../android/text/StaticLayout.Builder.md)) 

### isFontPaddingIncluded

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFontPaddingIncluded(): Boolean
```

Returns true if this layout is created with increased line height.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the layout is created with increased line height. |

**See Also**

- [android.text.Layout.Builder#setFontPaddingIncluded(boolean)](../android/text/Layout.Builder.md))
- [android.text.StaticLayout.Builder#setIncludePad(boolean)](../android/text/StaticLayout.Builder.md)) 

### isRtlCharAt

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRtlCharAt(offset: Int): Boolean
```

Returns true if the character at offset is right to left (RTL).

| Parameters ||
|----------|----------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the character is RTL, false if it is LTR |

## Protected methods

### isSpanned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun isSpanned(): Boolean
```

## Properties

### INCLUSION_STRATEGY_ANY_OVERLAP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INCLUSION_STRATEGY_ANY_OVERLAP: Layout.TextInclusionStrategy
```

Strategy which considers a text segment to be inside a rectangle area if the segment bounds intersect the rectangle. 

### INCLUSION_STRATEGY_CONTAINS_ALL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INCLUSION_STRATEGY_CONTAINS_ALL: Layout.TextInclusionStrategy
```

Strategy which considers a text segment to be inside a rectangle area if the segment bounds are completely contained within the rectangle. 

### INCLUSION_STRATEGY_CONTAINS_CENTER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INCLUSION_STRATEGY_CONTAINS_CENTER: Layout.TextInclusionStrategy
```

Strategy which considers a text segment to be inside a rectangle area if the center of the segment bounds is inside the rectangle.
