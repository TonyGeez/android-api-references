Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReplacementSpan

Kotlin | [Java](ReplacementSpan.md)
| --- | --- |

```
abstract class ReplacementSpan : MetricAffectingSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](CharacterStyle.md) |||
| | ↳ | [android.text.style.MetricAffectingSpan](MetricAffectingSpan.md) ||
| | | ↳ | [android.text.style.ReplacementSpan](ReplacementSpan.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [DynamicDrawableSpan](DynamicDrawableSpan.md) |---|---| | [DynamicDrawableSpan](DynamicDrawableSpan.md) | Span that replaces the text it's attached to with a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` that can be aligned with the bottom or with the baseline of the surrounding text. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ImageSpan](ImageSpan.md) |---|---| | [ImageSpan](ImageSpan.md) | Span that replaces the text it's attached to with a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` that can be aligned with the bottom or with the baseline of the surrounding text. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#ReplacementSpan()()` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#draw(android.graphics.Canvas,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)` Draws the span into the canvas. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#getContentDescription()()` Gets a brief description of this ReplacementSpan for use in accessibility support. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#getSize(android.graphics.Paint,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint.FontMetricsInt)(paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fm: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#?)` Returns the width of the span. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#setContentDescription(kotlin.CharSequence)(contentDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the specific content description into ReplacementSpan. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#updateDrawState(android.text.TextPaint)(ds: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)` This method does nothing, since ReplacementSpans are drawn explicitly instead of affecting Paint properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#updateMeasureState(android.text.TextPaint)(p: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)` This method does nothing, since ReplacementSpans are measured explicitly instead of affecting Paint properties. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan` |---|---| | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan!` | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying()()` Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)`, returns the underlying MetricAffectingSpan. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint)(tp: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)` <br /> | | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!` | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)(cs: https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!)` A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### ReplacementSpan

```
ReplacementSpan()
```

## Public methods

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun draw(
    canvas: Canvas, 
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    x: Float, 
    top: Int, 
    y: Int, 
    bottom: Int, 
    paint: Paint
): Unit
```

Draws the span into the canvas.

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md): Canvas into which the span should be rendered. This value cannot be `null`. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Current text. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Start character index for span. Value is 0 or greater |
| --- | --- |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): End character index for span. Value is 0 or greater |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Edge of the replacement closest to the leading margin. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Top of the line. |
| --- | --- |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Baseline. |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bottom of the line. |
| `paint` | [Paint](../android.graphics/Paint.md): Paint instance. This value cannot be `null`. |
| --- | --- |

### getContentDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContentDescription(): CharSequence?
```

Gets a brief description of this ReplacementSpan for use in accessibility support.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The content description. This value may be `null`. |

### getSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSize(
    paint: Paint, 
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    fm: Paint.FontMetricsInt?
): Int
```

Returns the width of the span. Extending classes can set the height of the span by updating attributes of `https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#`. If the span covers the whole text, and the height is not set, `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#draw(android.graphics.Canvas,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint)` will not be called for the span.

| Parameters ||
|---|---|
| `paint` | [Paint](../android.graphics/Paint.md): Paint instance. This value cannot be `null`. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Current text. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Start character index for span. Value is 0 or greater |
| --- | --- |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): End character index for span. Value is 0 or greater |
| `fm` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md)?: Font metrics, can be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Width of the span. |

### setContentDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContentDescription(contentDescription: CharSequence?): Unit
```

Sets the specific content description into ReplacementSpan. ReplacementSpans are shared with accessibility services, but only the content description is available from them.

| Parameters ||
|---|---|
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: content description. The default value is null. |

### updateDrawState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateDrawState(ds: TextPaint!): Unit
```

This method does nothing, since ReplacementSpans are drawn explicitly instead of affecting Paint properties.

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateMeasureState(p: TextPaint): Unit
```

This method does nothing, since ReplacementSpans are measured explicitly instead of affecting Paint properties.

| Parameters ||
|---|---|
| `textPaint` | the paint used for drawing the text. This value cannot be `null`. |
