# LineHeightSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LineHeightSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/LineHeightSpan "View this page in Java") 

```
interface LineHeightSpan : ParagraphStyle, WrapTogetherSpan
```

| [android.text.style.LineHeightSpan](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan#) |

| Known Direct Subclasses [DrawableMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan), [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan), [LineHeightSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan.Standard), [LineHeightSpan.WithDensity](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan.WithDensity) |----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DrawableMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan) | A span which adds a drawable and a padding to the paragraph it's attached to. | | [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan) | Paragraph affecting span, that draws a bitmap at the beginning of a text. | | [LineHeightSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan.Standard) | Default implementation of the [LineHeightSpan](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan#), which changes the line height of the attached paragraph. | | [LineHeightSpan.WithDensity](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan.WithDensity) | The classes that affect the line height of paragraph with respect to density, should implement this interface. | |

The classes that affect the line height of paragraph should implement this interface.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Standard](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan.Standard) Default implementation of the [LineHeightSpan](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan#), which changes the line height of the attached paragraph. |
| abstract | [WithDensity](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan.WithDensity) The classes that affect the line height of paragraph with respect to density, should implement this interface. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [chooseHeight](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan#chooseHeight(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint.FontMetricsInt))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `spanstartv:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lineHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fm:` ` [Paint.FontMetricsInt](https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#)!`)` Classes that implement this should define how the height is being calculated. |

## Public methods

### chooseHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun chooseHeight(
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    spanstartv: Int, 
    lineHeight: Int, 
    fm: Paint.FontMetricsInt!
): Unit
```

Classes that implement this should define how the height is being calculated.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the line |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end of the line |
| `spanstartv` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the span |
| `lineHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the line height |
| `fm` | [Paint.FontMetricsInt](https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#)!:font metrics of the paint, in integers |
