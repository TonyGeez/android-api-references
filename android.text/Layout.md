# Layout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Layout

Kotlin | [Java](https://developer.android.com/reference/android/text/Layout "View this page in Java") 
| --- | --- |

```
abstract class Layout
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.Layout](https://developer.android.com/reference/kotlin/android/text/Layout#) |

| Known Direct Subclasses [BoringLayout](https://developer.android.com/reference/kotlin/android/text/BoringLayout), [DynamicLayout](https://developer.android.com/reference/kotlin/android/text/DynamicLayout), [StaticLayout](https://developer.android.com/reference/kotlin/android/text/StaticLayout) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [BoringLayout](https://developer.android.com/reference/kotlin/android/text/BoringLayout) | A BoringLayout is a very simple Layout implementation for text that fits on a single line and is all left-to-right characters. | | [DynamicLayout](https://developer.android.com/reference/kotlin/android/text/DynamicLayout) | DynamicLayout is a text layout that updates itself as the text is edited. | | [StaticLayout](https://developer.android.com/reference/kotlin/android/text/StaticLayout) | StaticLayout is a Layout for text that will not be edited after it is laid out. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A base class that manages text layout in visual elements on the screen.

For text that will be edited, use a [DynamicLayout](https://developer.android.com/reference/kotlin/android/text/DynamicLayout), which will be updated as the text changes. For text that will not change, use a [StaticLayout](https://developer.android.com/reference/kotlin/android/text/StaticLayout).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Alignment](https://developer.android.com/reference/kotlin/android/text/Layout.Alignment) <br /> |
| | [Builder](https://developer.android.com/reference/kotlin/android/text/Layout.Builder) A builder class for Layout object. |
| open | [Directions](https://developer.android.com/reference/kotlin/android/text/Layout.Directions) Stores information about bidirectional (left-to-right or right-to-left) text within the layout of a line. |
| --- | --- |
| abstract | [TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy) Strategy for determining whether a text segment is inside a rectangle area. |

| Constants ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_BALANCED](https://developer.android.com/reference/kotlin/android/text/Layout#BREAK_STRATEGY_BALANCED:kotlin.Int) Value for break strategy indicating balanced line breaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_HIGH_QUALITY](https://developer.android.com/reference/kotlin/android/text/Layout#BREAK_STRATEGY_HIGH_QUALITY:kotlin.Int) Value for break strategy indicating high quality line breaking, including automatic hyphenation and doing whole-paragraph optimization of line breaks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BREAK_STRATEGY_SIMPLE](https://developer.android.com/reference/kotlin/android/text/Layout#BREAK_STRATEGY_SIMPLE:kotlin.Int) Value for break strategy indicating simple line breaking. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [DEFAULT_LINESPACING_ADDITION](https://developer.android.com/reference/kotlin/android/text/Layout#DEFAULT_LINESPACING_ADDITION:kotlin.Float) <br /> |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [DEFAULT_LINESPACING_MULTIPLIER](https://developer.android.com/reference/kotlin/android/text/Layout#DEFAULT_LINESPACING_MULTIPLIER:kotlin.Float) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIR_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/text/Layout#DIR_LEFT_TO_RIGHT:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIR_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/text/Layout#DIR_RIGHT_TO_LEFT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_FULL](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_FULL:kotlin.Int) Value for hyphenation frequency indicating the full amount of automatic hyphenation, typical in typography. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_FULL_FAST](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_FULL_FAST:kotlin.Int) Value for hyphenation frequency indicating the full amount of automatic hyphenation with using faster algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NONE](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NONE:kotlin.Int) Value for hyphenation frequency indicating no automatic hyphenation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NORMAL](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NORMAL:kotlin.Int) Value for hyphenation frequency indicating a light amount of automatic hyphenation, which is a conservative default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_FREQUENCY_NORMAL_FAST](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NORMAL_FAST:kotlin.Int) Value for hyphenation frequency indicating a light amount of automatic hyphenation with using faster algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_INTER_CHARACTER](https://developer.android.com/reference/kotlin/android/text/Layout#JUSTIFICATION_MODE_INTER_CHARACTER:kotlin.Int) Value for justification mode indicating the text is justified by stretching letter spacing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_INTER_WORD](https://developer.android.com/reference/kotlin/android/text/Layout#JUSTIFICATION_MODE_INTER_WORD:kotlin.Int) Value for justification mode indicating the text is justified by stretching word spacing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUSTIFICATION_MODE_NONE](https://developer.android.com/reference/kotlin/android/text/Layout#JUSTIFICATION_MODE_NONE:kotlin.Int) Value for justification mode indicating no justification. |
| --- | --- |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Layout](https://developer.android.com/reference/kotlin/android/text/Layout#Layout(kotlin.CharSequence,%20android.text.TextPaint,%20kotlin.Int,%20android.text.Layout.Alignment,%20kotlin.Float,%20kotlin.Float))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `paint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `align:` ` [Layout.Alignment](https://developer.android.com/reference/kotlin/android/text/Layout.Alignment)!`, `spacingMult:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `spacingAdd:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Subclasses of Layout use this constructor to set the display text, width, and other standard properties. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) | [computeDrawingBoundingBox](https://developer.android.com/reference/kotlin/android/text/Layout#computeDrawingBoundingBox())`()` Get an actual bounding box that draws text content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas))`(`c:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`)` Draw this Layout on the specified Canvas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`, `selectionHighlight:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`, `selectionHighlightPaint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!`, `cursorOffsetVertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Draw this Layout on the specified canvas, with the highlight path drawn between the background and the text. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`, `highlightPaths:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!>?`, `highlightPaints:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!>?`, `selectionPath:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)?`, `selectionPaint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)?`, `cursorOffsetVertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Draw this layout on the specified canvas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBackground](https://developer.android.com/reference/kotlin/android/text/Layout#drawBackground(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`)` Draw background of this layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawText](https://developer.android.com/reference/kotlin/android/text/Layout#drawText(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`)` Draw text part of this layout. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillCharacterBounds](https://developer.android.com/reference/kotlin/android/text/Layout#fillCharacterBounds(kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `boundsStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the characters' bounds in the given range. |
| [Layout.Alignment](https://developer.android.com/reference/kotlin/android/text/Layout.Alignment) | [getAlignment](https://developer.android.com/reference/kotlin/android/text/Layout#getAlignment())`()` Returns the alignment used for creating this layout in pixels. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBottomPadding](https://developer.android.com/reference/kotlin/android/text/Layout#getBottomPadding())`()` Returns the number of extra pixels of descent padding in the bottom line of the Layout. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBreakStrategy](https://developer.android.com/reference/kotlin/android/text/Layout#getBreakStrategy())`()` Return the break strategy used for creating this layout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCursorPath](https://developer.android.com/reference/kotlin/android/text/Layout#getCursorPath(kotlin.Int,%20android.graphics.Path,%20kotlin.CharSequence))`(`point:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`, `editingBuffer:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Fills in the specified Path with a representation of a cursor at the specified offset. |
| open static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDesiredWidth](https://developer.android.com/reference/kotlin/android/text/Layout#getDesiredWidth(kotlin.CharSequence,%20android.text.TextPaint))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `paint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint)!`)` Return how wide a layout must be in order to display the specified text with one line per paragraph. |
| --- | --- |
| open static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDesiredWidth](https://developer.android.com/reference/kotlin/android/text/Layout#getDesiredWidth(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.text.TextPaint))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint)!`)` Return how wide a layout must be in order to display the specified text slice with one line per paragraph. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsisCount](https://developer.android.com/reference/kotlin/android/text/Layout#getEllipsisCount(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the number of characters to be ellipsized away, or 0 if no ellipsis is to take place. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsisStart](https://developer.android.com/reference/kotlin/android/text/Layout#getEllipsisStart(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the offset of the first character to be ellipsized away, relative to the start of the line. |
| --- | --- |
| [TextUtils.TruncateAt](https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt)? | [getEllipsize](https://developer.android.com/reference/kotlin/android/text/Layout#getEllipsize())`()` Return the ellipsize option used for creating this layout. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEllipsizedWidth](https://developer.android.com/reference/kotlin/android/text/Layout#getEllipsizedWidth())`()` Return the width to which this layout is ellipsized. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/text/Layout#getHeight())`()` Return the total height of this layout. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHyphenationFrequency](https://developer.android.com/reference/kotlin/android/text/Layout#getHyphenationFrequency())`()` Return the hyphenation frequency used for creating this layout. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJustificationMode](https://developer.android.com/reference/kotlin/android/text/Layout#getJustificationMode())`()` Return the justification mode used for creating this layout. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getLeftIndents](https://developer.android.com/reference/kotlin/android/text/Layout#getLeftIndents())`()` Return a copy of the left indents used for this layout. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineAscent](https://developer.android.com/reference/kotlin/android/text/Layout#getLineAscent(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the ascent of the text on the specified line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBaseline](https://developer.android.com/reference/kotlin/android/text/Layout#getLineBaseline(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the vertical position of the baseline of the specified line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBottom](https://developer.android.com/reference/kotlin/android/text/Layout#getLineBottom(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the vertical position of the bottom of the specified line. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBottom](https://developer.android.com/reference/kotlin/android/text/Layout#getLineBottom(kotlin.Int,%20kotlin.Boolean))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `includeLineSpacing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return the vertical position of the bottom of the specified line. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBounds](https://developer.android.com/reference/kotlin/android/text/Layout#getLineBounds(kotlin.Int,%20android.graphics.Rect))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` Return the baseline for the specified line (0...getLineCount() - 1) If bounds is not null, return the top, left, right, bottom extents of the specified line in it. |
| open [LineBreakConfig](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#) | [getLineBreakConfig](https://developer.android.com/reference/kotlin/android/text/Layout#getLineBreakConfig())`()` Gets the [LineBreakConfig](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#) used for creating this layout. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLineContainsTab](https://developer.android.com/reference/kotlin/android/text/Layout#getLineContainsTab(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns whether the specified line contains one or more characters that need to be handled specially, like tabs. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineCount](https://developer.android.com/reference/kotlin/android/text/Layout#getLineCount())`()` Return the number of lines of text in this layout. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineDescent](https://developer.android.com/reference/kotlin/android/text/Layout#getLineDescent(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the descent of the specified line(0...getLineCount() - 1). |
| --- | --- |
| abstract [Layout.Directions](https://developer.android.com/reference/kotlin/android/text/Layout.Directions)! | [getLineDirections](https://developer.android.com/reference/kotlin/android/text/Layout#getLineDirections(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the directional run information for the specified line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineEnd](https://developer.android.com/reference/kotlin/android/text/Layout#getLineEnd(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the text offset after the last character on the specified line. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineForOffset](https://developer.android.com/reference/kotlin/android/text/Layout#getLineForOffset(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the line number on which the specified text offset appears. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineForVertical](https://developer.android.com/reference/kotlin/android/text/Layout#getLineForVertical(kotlin.Int))`(`vertical:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the line number corresponding to the specified vertical position. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineLeft](https://developer.android.com/reference/kotlin/android/text/Layout#getLineLeft(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the leftmost position that should be exposed for horizontal scrolling on the specified line. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineLetterSpacingUnitCount](https://developer.android.com/reference/kotlin/android/text/Layout#getLineLetterSpacingUnitCount(kotlin.Int,%20kotlin.Boolean))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `includeTrailingWhitespace:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the number of letter spacing unit in the line. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineMax](https://developer.android.com/reference/kotlin/android/text/Layout#getLineMax(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the unsigned horizontal extent of the specified line, including leading margin indent, but excluding trailing whitespace. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineRight](https://developer.android.com/reference/kotlin/android/text/Layout#getLineRight(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the rightmost position that should be exposed for horizontal scrolling on the specified line. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineSpacingAmount](https://developer.android.com/reference/kotlin/android/text/Layout#getLineSpacingAmount())`()` Returns the amount added to the line height. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineSpacingMultiplier](https://developer.android.com/reference/kotlin/android/text/Layout#getLineSpacingMultiplier())`()` Returns the multiplier applied to the line height. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineStart](https://developer.android.com/reference/kotlin/android/text/Layout#getLineStart(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the text offset of the beginning of the specified line ( 0...getLineCount()). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineTop](https://developer.android.com/reference/kotlin/android/text/Layout#getLineTop(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the vertical position of the top of the specified line (0...getLineCount()). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineVisibleEnd](https://developer.android.com/reference/kotlin/android/text/Layout#getLineVisibleEnd(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the text offset after the last visible character (so whitespace is not counted) on the specified line. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLineWidth](https://developer.android.com/reference/kotlin/android/text/Layout#getLineWidth(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the unsigned horizontal extent of the specified line, including leading margin indent and trailing whitespace. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxLines](https://developer.android.com/reference/kotlin/android/text/Layout#getMaxLines())`()` Return the maximum lines allowed used for creating this layout. |
| --- | --- |
| open [Paint.FontMetrics](https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics.html#)? | [getMinimumFontMetrics](https://developer.android.com/reference/kotlin/android/text/Layout#getMinimumFontMetrics())`()` Get the minimum font metrics used for line spacing. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetForHorizontal](https://developer.android.com/reference/kotlin/android/text/Layout#getOffsetForHorizontal(kotlin.Int,%20kotlin.Float))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `horiz:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Get the character offset on the specified line whose position is closest to the specified horizontal position. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetToLeftOf](https://developer.android.com/reference/kotlin/android/text/Layout#getOffsetToLeftOf(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetToRightOf](https://developer.android.com/reference/kotlin/android/text/Layout#getOffsetToRightOf(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint) | [getPaint](https://developer.android.com/reference/kotlin/android/text/Layout#getPaint())`()` Return the paint used for creating this layout. |
| [Layout.Alignment](https://developer.android.com/reference/kotlin/android/text/Layout.Alignment)! | [getParagraphAlignment](https://developer.android.com/reference/kotlin/android/text/Layout#getParagraphAlignment(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the alignment of the specified paragraph, taking into account markup attached to it. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphDirection](https://developer.android.com/reference/kotlin/android/text/Layout#getParagraphDirection(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the primary directionality of the paragraph containing the specified line, either 1 for left-to-right lines, or -1 for right-to-left lines (see [DIR_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/text/Layout#DIR_LEFT_TO_RIGHT:kotlin.Int), [DIR_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/text/Layout#DIR_RIGHT_TO_LEFT:kotlin.Int)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphLeft](https://developer.android.com/reference/kotlin/android/text/Layout#getParagraphLeft(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the left edge of the specified paragraph, inset by left margins. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphRight](https://developer.android.com/reference/kotlin/android/text/Layout#getParagraphRight(kotlin.Int))`(`line:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the right edge of the specified paragraph, inset by right margins. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPrimaryHorizontal](https://developer.android.com/reference/kotlin/android/text/Layout#getPrimaryHorizontal(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the primary horizontal position for the specified text offset. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getRangeForRect](https://developer.android.com/reference/kotlin/android/text/Layout#getRangeForRect(android.graphics.RectF,%20android.text.SegmentFinder,%20android.text.Layout.TextInclusionStrategy))`(`area:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)`, `segmentFinder:` ` [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder)`, `inclusionStrategy:` ` [Layout.TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy)`)` Finds the range of text which is inside the specified rectangle area. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getRightIndents](https://developer.android.com/reference/kotlin/android/text/Layout#getRightIndents())`()` Return a copy of the right indents used for this layout. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSecondaryHorizontal](https://developer.android.com/reference/kotlin/android/text/Layout#getSecondaryHorizontal(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the secondary horizontal position for the specified text offset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSelectionPath](https://developer.android.com/reference/kotlin/android/text/Layout#getSelectionPath(kotlin.Int,%20kotlin.Int,%20android.graphics.Path))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Fills in the specified Path with a representation of a highlight between the specified offsets. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShiftDrawingOffsetForStartOverhang](https://developer.android.com/reference/kotlin/android/text/Layout#getShiftDrawingOffsetForStartOverhang())`()` Returns true if shifting drawing offset for start overhang. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpacingAdd](https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingAdd())`()` Returns the amount added to the line height. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSpacingMultiplier](https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingMultiplier())`()` Returns the multiplier applied to the line height. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getText](https://developer.android.com/reference/kotlin/android/text/Layout#getText())`()` Return the text used for creating this layout. |
| --- | --- |
| [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic) | [getTextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/Layout#getTextDirectionHeuristic())`()` Returns the text direction heuristic used for creating this layout. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTopPadding](https://developer.android.com/reference/kotlin/android/text/Layout#getTopPadding())`()` Returns the (negative) number of extra pixels of ascent padding in the top line of the Layout. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseBoundsForWidth](https://developer.android.com/reference/kotlin/android/text/Layout#getUseBoundsForWidth())`()` Returns true if using bounding box as a width, false for using advance as a width. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/text/Layout#getWidth())`()` Return the width used for creating this layout in pixels. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [increaseWidthTo](https://developer.android.com/reference/kotlin/android/text/Layout#increaseWidthTo(kotlin.Int))`(`wid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increase the width of this layout to the specified width. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFallbackLineSpacingEnabled](https://developer.android.com/reference/kotlin/android/text/Layout#isFallbackLineSpacingEnabled())`()` Return true if the fallback line space is enabled in this Layout. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFontPaddingIncluded](https://developer.android.com/reference/kotlin/android/text/Layout#isFontPaddingIncluded())`()` Returns true if this layout is created with increased line height. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRtlCharAt](https://developer.android.com/reference/kotlin/android/text/Layout#isRtlCharAt(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the character at offset is right to left (RTL). |

| Protected methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpanned](https://developer.android.com/reference/kotlin/android/text/Layout#isSpanned())`()` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Layout.TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy) | [INCLUSION_STRATEGY_ANY_OVERLAP](https://developer.android.com/reference/kotlin/android/text/Layout#INCLUSION_STRATEGY_ANY_OVERLAP:android.text.Layout.TextInclusionStrategy) Strategy which considers a text segment to be inside a rectangle area if the segment bounds intersect the rectangle. |
| static [Layout.TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy) | [INCLUSION_STRATEGY_CONTAINS_ALL](https://developer.android.com/reference/kotlin/android/text/Layout#INCLUSION_STRATEGY_CONTAINS_ALL:android.text.Layout.TextInclusionStrategy) Strategy which considers a text segment to be inside a rectangle area if the segment bounds are completely contained within the rectangle. |
| static [Layout.TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy) | [INCLUSION_STRATEGY_CONTAINS_CENTER](https://developer.android.com/reference/kotlin/android/text/Layout#INCLUSION_STRATEGY_CONTAINS_CENTER:android.text.Layout.TextInclusionStrategy) Strategy which considers a text segment to be inside a rectangle area if the center of the segment bounds is inside the rectangle. |
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
| `paint` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint)!: the default paint for the layout. Styles can override various attributes of the paint. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the wrapping width for the text. |
| --- | --- |
| `align` | [Layout.Alignment](https://developer.android.com/reference/kotlin/android/text/Layout.Alignment)!: whether to left, right, or center the text. Styles can override the alignment. |
| `spacingMult` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): factor by which to scale the font size to get the default line spacing |
| `spacingAdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): amount to add to the default line spacing |
| --- | --- |

## Public methods

### computeDrawingBoundingBox

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeDrawingBoundingBox(): RectF
```

Get an actual bounding box that draws text content. Note that the [RectF.top](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#top:kotlin.Float) and [RectF.bottom](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#bottom:kotlin.Float) may be different from the [Layout.getLineTop(int)](https://developer.android.com/reference/kotlin/android/text/Layout#getLineTop(kotlin.Int)) of the first line and [Layout.getLineBottom(int)](https://developer.android.com/reference/kotlin/android/text/Layout#getLineBottom(kotlin.Int)) of the last line. The line top and line bottom are calculated based on yMin/yMax or ascent/descent value of font file. On the other hand, the drawing bounding boxes are calculated based on actual glyphs used there.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------------------|
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) | bounding rectangle This value cannot be `null`. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(c: Canvas!): Unit
```

Draw this Layout on the specified Canvas. This API draws background first, then draws text on top of it. 
**See Also**

- [#draw(Canvas, List, List, Path, Paint, int)](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int)) 

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
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!: the canvas |
| `selectionHighlight` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!: the path of the selection highlight or cursor; can be null |
| `selectionHighlightPaint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!: the paint for the selection highlight |
| --- | --- |
| `cursorOffsetVertical` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount to temporarily translate the canvas while rendering the highlight |

**See Also**

- [#draw(Canvas, List, List, Path, Paint, int)](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int)) 

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
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): the canvas This value cannot be `null`. |
| `highlightPaths` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!\>?: the path of the highlights. The highlightPaths and highlightPaints must have the same length and aligned in the same order. For example, the paint of the n-th of the highlightPaths should be stored at the n-th of highlightPaints. This value may be `null`. |
| `highlightPaints` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!\>?: the paints for the highlights. The highlightPaths and highlightPaints must have the same length and aligned in the same order. For example, the paint of the n-th of the highlightPaths should be stored at the n-th of highlightPaints. This value may be `null`. |
| --- | --- |
| `selectionPath` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)?: the selection or cursor path This value may be `null`. |
| `selectionPaint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)?: the paint for the selection or cursor. This value may be `null`. |
| `cursorOffsetVertical` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount to temporarily translate the canvas while rendering the highlight |
| --- | --- |

**See Also**

- [#drawBackground(Canvas)](https://developer.android.com/reference/kotlin/android/text/Layout#drawBackground(android.graphics.Canvas))
- [#drawText(Canvas)](https://developer.android.com/reference/kotlin/android/text/Layout#drawText(android.graphics.Canvas)) 

### drawBackground

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawBackground(canvas: Canvas): Unit
```

Draw background of this layout. Different from [draw(android.graphics.Canvas,java.util.List,java.util.List,android.graphics.Path,android.graphics.Paint,int)](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int)) API, this API only draws background, not drawing text, highlights or selections. The background here is drawn by [LineBackgroundSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan) attached to the text.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): the canvas This value cannot be `null`. |

**See Also**

- [#draw(Canvas, List, List, Path, Paint, int)](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int))
- [#drawText(Canvas)](https://developer.android.com/reference/kotlin/android/text/Layout#drawText(android.graphics.Canvas)) 

### drawText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawText(canvas: Canvas): Unit
```

Draw text part of this layout. Different from [draw(android.graphics.Canvas,java.util.List,java.util.List,android.graphics.Path,android.graphics.Paint,int)](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int)) API, this API only draws text part, not drawing highlights, selections, or backgrounds.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): the canvas This value cannot be `null`. |

**See Also**

- [#draw(Canvas, List, List, Path, Paint, int)](https://developer.android.com/reference/kotlin/android/text/Layout#draw(android.graphics.Canvas,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.graphics.Path,%20android.graphics.Paint,%20kotlin.Int))
- [#drawBackground(Canvas)](https://developer.android.com/reference/kotlin/android/text/Layout#drawBackground(android.graphics.Canvas)) 

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
| [Layout.Alignment](https://developer.android.com/reference/kotlin/android/text/Layout.Alignment) | the alignment used for creating this layout. This value cannot be `null`. |

**See Also**

- [android.text.StaticLayout.Builder#setAlignment(Alignment)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setAlignment(android.text.Layout.Alignment)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the break strategy used for creating this layout. Value is [android.graphics.text.LineBreaker#BREAK_STRATEGY_SIMPLE](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.html#BREAK_STRATEGY_SIMPLE:kotlin.Int), [android.graphics.text.LineBreaker#BREAK_STRATEGY_HIGH_QUALITY](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.html#BREAK_STRATEGY_HIGH_QUALITY:kotlin.Int), or [android.graphics.text.LineBreaker#BREAK_STRATEGY_BALANCED](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.html#BREAK_STRATEGY_BALANCED:kotlin.Int) |

**See Also**

- [android.text.Layout.Builder#setBreakStrategy(int)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setBreakStrategy(kotlin.Int))
- [android.text.StaticLayout.Builder#setBreakStrategy(int)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setBreakStrategy(kotlin.Int)) 

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

As of O, Uses [TextDirectionHeuristics.FIRSTSTRONG_LTR](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#FIRSTSTRONG_LTR:android.text.TextDirectionHeuristic) as the default text direction heuristics. In the earlier versions uses [TextDirectionHeuristics.LTR](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#LTR:android.text.TextDirectionHeuristic) as the default. 

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

As of O, Uses [TextDirectionHeuristics.FIRSTSTRONG_LTR](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#FIRSTSTRONG_LTR:android.text.TextDirectionHeuristic) as the default text direction heuristics. In the earlier versions uses [TextDirectionHeuristics.LTR](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics#LTR:android.text.TextDirectionHeuristic) as the default. 

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
| [TextUtils.TruncateAt](https://developer.android.com/reference/kotlin/android/text/TextUtils.TruncateAt)? | The ellipsize option used for creating this layout, or null if no ellipsize option was selected. |

**See Also**

- [android.text.Layout.Builder#setEllipsize(TextUtils.TruncateAt)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setEllipsize(android.text.TextUtils.TruncateAt))
- [android.text.StaticLayout.Builder#setEllipsize(TextUtils.TruncateAt)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setEllipsize(android.text.TextUtils.TruncateAt))
- [android.text.Layout.Builder#setEllipsizedWidth(int)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setEllipsizedWidth(kotlin.Int))
- [android.text.StaticLayout.Builder#setEllipsizedWidth(int)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setEllipsizedWidth(kotlin.Int))
- [android.text.Layout#getEllipsizedWidth()](https://developer.android.com/reference/kotlin/android/text/Layout#getEllipsizedWidth()) 

### getEllipsizedWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEllipsizedWidth(): Int
```

Return the width to which this layout is ellipsized. If no ellipsize is applied, the same amount of [getWidth](https://developer.android.com/reference/kotlin/android/text/Layout#getWidth()) is returned.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of ellipsized width in pixels. Value is 0 or greater |

**See Also**

- [android.text.StaticLayout.Builder#setEllipsizedWidth(int)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setEllipsizedWidth(kotlin.Int))
- [android.text.StaticLayout.Builder#setEllipsize(TextUtils.TruncateAt)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setEllipsize(android.text.TextUtils.TruncateAt)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hyphenation frequency used for creating this layout. Value is [android.text.Layout#HYPHENATION_FREQUENCY_NORMAL](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NORMAL:kotlin.Int), [android.text.Layout#HYPHENATION_FREQUENCY_NORMAL_FAST](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NORMAL_FAST:kotlin.Int), [android.text.Layout#HYPHENATION_FREQUENCY_FULL](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_FULL:kotlin.Int), [android.text.Layout#HYPHENATION_FREQUENCY_FULL_FAST](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_FULL_FAST:kotlin.Int), or [android.text.Layout#HYPHENATION_FREQUENCY_NONE](https://developer.android.com/reference/kotlin/android/text/Layout#HYPHENATION_FREQUENCY_NONE:kotlin.Int) |

**See Also**

- [android.text.Layout.Builder#setHyphenationFrequency(int)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setHyphenationFrequency(kotlin.Int))
- [android.text.StaticLayout.Builder#setHyphenationFrequency(int)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setHyphenationFrequency(kotlin.Int)) 

### getJustificationMode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getJustificationMode(): Int
```

Return the justification mode used for creating this layout.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the justification mode used for creating this layout. Value is [android.graphics.text.LineBreaker#JUSTIFICATION_MODE_NONE](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.html#JUSTIFICATION_MODE_NONE:kotlin.Int), [android.graphics.text.LineBreaker#JUSTIFICATION_MODE_INTER_WORD](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.html#JUSTIFICATION_MODE_INTER_WORD:kotlin.Int), or [android.graphics.text.LineBreaker#JUSTIFICATION_MODE_INTER_CHARACTER](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.html#JUSTIFICATION_MODE_INTER_CHARACTER:kotlin.Int) |

**See Also**

- [android.text.Layout.Builder#setJustificationMode(int)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setJustificationMode(kotlin.Int))
- [android.text.StaticLayout.Builder#setJustificationMode(int)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setJustificationMode(kotlin.Int)) 

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
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: Optional. If not null, it returns the extent of the line |

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Y-coordinate of the baseline |

### getLineBreakConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineBreakConfig(): LineBreakConfig
```

Gets the [LineBreakConfig](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#) used for creating this layout. Do not modify the returned object.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [LineBreakConfig](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#) | The line break config used for creating this layout. This value cannot be `null`. |

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

This API returns a number of letters that is a target of letter spacing. The letter spacing won't be added to the middle of the characters that are needed to be treated as a single, e.g., ligatured or conjunct form. Note that this value is different from the number of\] grapheme clusters that is calculated by [BreakIterator.getCharacterInstance(Locale)](https://developer.android.com/reference/kotlin/java/text/BreakIterator.html#getCharacterInstance(java.util.Locale)). For example, if the "fi" is ligatured, the ligatured form is treated as single uni and letter spacing is not added, but it has two separate grapheme cluster.

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

- [android.text.Layout.Builder#setLineSpacingAmount(float)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setLineSpacingAmount(kotlin.Float))
- [android.text.StaticLayout.Builder#setLineSpacing(float, float)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setLineSpacing(kotlin.Float,%20kotlin.Float))
- [android.text.Layout#getSpacingAdd()](https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingAdd()) 

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

- [android.text.Layout.Builder#setLineSpacingMultiplier(float)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setLineSpacingMultiplier(kotlin.Float))
- [android.text.StaticLayout.Builder#setLineSpacing(float, float)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setLineSpacing(kotlin.Float,%20kotlin.Float))
- [android.text.Layout#getSpacingMultiplier()](https://developer.android.com/reference/kotlin/android/text/Layout#getSpacingMultiplier()) 

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

Return the maximum lines allowed used for creating this layout. Note that this is not an actual line count of this layout. Use [getLineCount()](https://developer.android.com/reference/kotlin/android/text/Layout#getLineCount()) for getting the actual line count of this layout.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum lines allowed used for creating this layout. Value is 1 or greater |

**See Also**

- [android.text.Layout.Builder#setMaxLines(int)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setMaxLines(kotlin.Int))
- [android.text.StaticLayout.Builder#setMaxLines(int)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setMaxLines(kotlin.Int)) 

### getMinimumFontMetrics

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumFontMetrics(): Paint.FontMetrics?
```

Get the minimum font metrics used for line spacing.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Paint.FontMetrics](https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics.html#)? | a minimum font metrics. `null` for using the value obtained by [Paint.getFontMetricsForLocale(Paint.FontMetrics)](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetricsForLocale(android.graphics.Paint.FontMetrics)) |

**See Also**

- [android.widget.TextView#setMinimumFontMetrics(Paint.FontMetrics)](https://developer.android.com/reference/kotlin/android/widget/TextView.html#setMinimumFontMetrics(android.graphics.Paint.FontMetrics))
- [android.widget.TextView#getMinimumFontMetrics()](https://developer.android.com/reference/kotlin/android/widget/TextView.html#getMinimumFontMetrics())
- [android.text.Layout.Builder#setMinimumFontMetrics(Paint.FontMetrics)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setMinimumFontMetrics(android.graphics.Paint.FontMetrics))
- [android.text.StaticLayout.Builder#setMinimumFontMetrics(Paint.FontMetrics)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setMinimumFontMetrics(android.graphics.Paint.FontMetrics))
- [android.text.DynamicLayout.Builder#setMinimumFontMetrics(Paint.FontMetrics)](https://developer.android.com/reference/kotlin/android/text/DynamicLayout.Builder#setMinimumFontMetrics(android.graphics.Paint.FontMetrics)) 

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
| [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint) | the paint used for creating this layout. This value cannot be `null`. |

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

Returns the primary directionality of the paragraph containing the specified line, either 1 for left-to-right lines, or -1 for right-to-left lines (see [DIR_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/text/Layout#DIR_LEFT_TO_RIGHT:kotlin.Int), [DIR_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/text/Layout#DIR_RIGHT_TO_LEFT:kotlin.Int)). 

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

A text segment is considered to be inside the area according to the provided [TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy). If a text segment spans multiple lines or multiple directional runs (e.g. a hyphenated word), the text segment is divided into pieces at the line and run breaks, then the text segment is considered to be inside the area if any of its pieces are inside the area.

The returned range may also include text segments which are not inside the specified area, if those text segments are in between text segments which are inside the area. For example, the returned range may be "segment1 segment2 segment3" if "segment1" and "segment3" are inside the area and "segment2" is not.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `area` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#): area for which the text range will be found This value cannot be `null`. |
| `segmentFinder` | [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder): SegmentFinder for determining the ranges of text to be considered as a text segment This value cannot be `null`. |
| `inclusionStrategy` | [Layout.TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy): strategy for determining whether a text segment is inside the specified area This value cannot be `null`. |
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

- [android.widget.TextView#setShiftDrawingOffsetForStartOverhang(boolean)](https://developer.android.com/reference/kotlin/android/widget/TextView.html#setShiftDrawingOffsetForStartOverhang(kotlin.Boolean))
- [android.widget.TextView#getShiftDrawingOffsetForStartOverhang()](https://developer.android.com/reference/kotlin/android/widget/TextView.html#getShiftDrawingOffsetForStartOverhang())
- [android.text.StaticLayout.Builder#setShiftDrawingOffsetForStartOverhang(boolean)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setShiftDrawingOffsetForStartOverhang(kotlin.Boolean))
- [android.text.DynamicLayout.Builder#setShiftDrawingOffsetForStartOverhang(boolean)](https://developer.android.com/reference/kotlin/android/text/DynamicLayout.Builder#setShiftDrawingOffsetForStartOverhang(kotlin.Boolean)) 

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

- [android.text.StaticLayout.Builder#setLineSpacing(float, float)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setLineSpacing(kotlin.Float,%20kotlin.Float)) 

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

- [android.text.StaticLayout.Builder#setLineSpacing(float, float)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setLineSpacing(kotlin.Float,%20kotlin.Float)) 

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
| [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic) | the text direction heuristic used for creating this layout This value cannot be `null`. |

**See Also**

- [android.text.Layout.Builder#setTextDirectionHeuristic(TextDirectionHeuristic)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setTextDirectionHeuristic(android.text.TextDirectionHeuristic))
- [android.text.StaticLayout.Builder#setTextDirection(TextDirectionHeuristic)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setTextDirection(android.text.TextDirectionHeuristic)) 

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

- [android.widget.TextView#setUseBoundsForWidth(boolean)](https://developer.android.com/reference/kotlin/android/widget/TextView.html#setUseBoundsForWidth(kotlin.Boolean))
- [android.widget.TextView#getUseBoundsForWidth()](https://developer.android.com/reference/kotlin/android/widget/TextView.html#getUseBoundsForWidth())
- [android.text.StaticLayout.Builder#setUseBoundsForWidth(boolean)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setUseBoundsForWidth(kotlin.Boolean))
- [android.text.DynamicLayout.Builder#setUseBoundsForWidth(boolean)](https://developer.android.com/reference/kotlin/android/text/DynamicLayout.Builder#setUseBoundsForWidth(kotlin.Boolean)) 

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

- [android.text.StaticLayout.Builder#setUseLineSpacingFromFallbacks(boolean)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setUseLineSpacingFromFallbacks(kotlin.Boolean)) 

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

- [android.text.Layout.Builder#setFontPaddingIncluded(boolean)](https://developer.android.com/reference/kotlin/android/text/Layout.Builder#setFontPaddingIncluded(kotlin.Boolean))
- [android.text.StaticLayout.Builder#setIncludePad(boolean)](https://developer.android.com/reference/kotlin/android/text/StaticLayout.Builder#setIncludePad(kotlin.Boolean)) 

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
