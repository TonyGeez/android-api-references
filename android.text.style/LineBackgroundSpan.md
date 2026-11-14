# LineBackgroundSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LineBackgroundSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/LineBackgroundSpan "View this page in Java") 
| --- | --- |

```
interface LineBackgroundSpan : ParagraphStyle
```

| [android.text.style.LineBackgroundSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan#) |

| Known Direct Subclasses [LineBackgroundSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan.Standard) |------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [LineBackgroundSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan.Standard) | Default implementation of the [LineBackgroundSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan#), which changes the background color of the lines to which the span is attached. | |
| --- | --- | --- | --- | --- | --- | --- |

Used to change the background of lines where the span is attached to.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Standard](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan.Standard) Default implementation of the [LineBackgroundSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan#), which changes the background color of the lines to which the span is attached. |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawBackground](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan#drawBackground(android.graphics.Canvas,%20android.graphics.Paint,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)`, `left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `baseline:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Draw the background on the canvas. |

## Public methods

### drawBackground

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun drawBackground(
    canvas: Canvas, 
    paint: Paint, 
    left: Int, 
    right: Int, 
    top: Int, 
    baseline: Int, 
    bottom: Int, 
    text: CharSequence, 
    start: Int, 
    end: Int, 
    lineNumber: Int
): Unit
```

Draw the background on the canvas.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#):canvas on which the span should be rendered This value cannot be`null`. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#):paint used to draw text, which should be left unchanged on exit This value cannot be`null`. |
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):left position of the line relative to input canvas, in pixels The units of this value are pixels. |
| --- | --- |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):right position of the line relative to input canvas, in pixels The units of this value are pixels. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):top position of the line relative to input canvas, in pixels The units of this value are pixels. |
| `baseline` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):baseline of the text relative to input canvas, in pixels The units of this value are pixels. |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):bottom position of the line relative to input canvas, in pixels The units of this value are pixels. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):current text This value cannot be`null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):start character index of the line |
| --- | --- |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):end character index of the line |
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):line number in the current text layout |
