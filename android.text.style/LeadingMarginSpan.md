# LeadingMarginSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LeadingMarginSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/LeadingMarginSpan "View this page in Java") 

```
interface LeadingMarginSpan : ParagraphStyle
```

| [android.text.style.LeadingMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan#) |

| Known Direct Subclasses [BulletSpan](https://developer.android.com/reference/kotlin/android/text/style/BulletSpan), [DrawableMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan), [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan), [LeadingMarginSpan.LeadingMarginSpan2](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan.LeadingMarginSpan2), [LeadingMarginSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan.Standard), [QuoteSpan](https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan) |------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BulletSpan](https://developer.android.com/reference/kotlin/android/text/style/BulletSpan) | A span which styles paragraphs as bullet points (respecting layout direction). | | [DrawableMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan) | A span which adds a drawable and a padding to the paragraph it's attached to. | | [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan) | Paragraph affecting span, that draws a bitmap at the beginning of a text. | | [LeadingMarginSpan.LeadingMarginSpan2](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan.LeadingMarginSpan2) | An extended version of [LeadingMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan#), which allows the implementor to specify the number of lines of the paragraph to which this object is attached that the "first line of paragraph" margin width will be applied to. | | [LeadingMarginSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan.Standard) | The standard implementation of LeadingMarginSpan, which adjusts the margin but does not do any rendering. | | [QuoteSpan](https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan) | A span which styles paragraphs by adding a vertical stripe at the beginning of the text (respecting layout direction). | |

A paragraph style affecting the leading margin. There can be multiple leading margin spans on a single paragraph; they will be rendered in order, each adding its margin to the ones before it. The leading margin is on the right for lines in a right-to-left paragraph.

LeadingMarginSpans should be attached from the first character to the last character of a single paragraph.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [LeadingMarginSpan2](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan.LeadingMarginSpan2) An extended version of [LeadingMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan#), which allows the implementor to specify the number of lines of the paragraph to which this object is attached that the "first line of paragraph" margin width will be applied to. |
| open | [Standard](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan.Standard) The standard implementation of LeadingMarginSpan, which adjusts the margin but does not do any rendering. |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawLeadingMargin](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan#drawLeadingMargin(android.graphics.Canvas,%20android.graphics.Paint,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.text.Layout))`(`c:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`, `p:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dir:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `baseline:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `first:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `layout:` ` [Layout](https://developer.android.com/reference/kotlin/android/text/Layout.html#)!`)` Renders the leading margin. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLeadingMargin](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan#getLeadingMargin(kotlin.Boolean))`(`first:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the amount by which to adjust the leading margin. |

## Public methods

### drawLeadingMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun drawLeadingMargin(
    c: Canvas!, 
    p: Paint!, 
    x: Int, 
    dir: Int, 
    top: Int, 
    baseline: Int, 
    bottom: Int, 
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    first: Boolean, 
    layout: Layout!
): Unit
```

Renders the leading margin. This is called before the margin has been adjusted by the value returned by [getLeadingMargin(boolean)](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan#getLeadingMargin(kotlin.Boolean)).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!:the canvas |
| `p` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!:the paint. The this should be left unchanged on exit. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current position of the margin |
| `dir` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the base direction of the paragraph; if negative, the margin is to the right of the text, otherwise it is to the left. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the top of the line |
| `baseline` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the baseline of the line |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the bottom of the line |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the line |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end of the line |
| `first` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this is the first line of its paragraph |
| `layout` | [Layout](https://developer.android.com/reference/kotlin/android/text/Layout.html#)!:the layout containing this line |

### getLeadingMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLeadingMargin(first: Boolean): Int
```

Returns the amount by which to adjust the leading margin. Positive values move away from the leading edge of the paragraph, negative values move towards it.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `first` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the request is for the first line of a paragraph, false for subsequent lines |

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offset for the margin. |
