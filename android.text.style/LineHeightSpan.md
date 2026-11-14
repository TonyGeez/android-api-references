# LineHeightSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LineHeightSpan

Kotlin| [Java](LineHeightSpan.md) 
| --- | --- |

```
interface LineHeightSpan : ParagraphStyle, WrapTogetherSpan
```

| [android.text.style.LineHeightSpan](LineHeightSpan.md) |

| Known Direct Subclasses [DrawableMarginSpan](DrawableMarginSpan.md), [IconMarginSpan](IconMarginSpan.md), [LineHeightSpan.Standard](../android/text/style/LineHeightSpan.Standard.md), [LineHeightSpan.WithDensity](../android/text/style/LineHeightSpan.WithDensity.md) |----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DrawableMarginSpan](DrawableMarginSpan.md) | A span which adds a drawable and a padding to the paragraph it's attached to. | | [IconMarginSpan](IconMarginSpan.md) | Paragraph affecting span, that draws a bitmap at the beginning of a text. | | [LineHeightSpan.Standard](../android/text/style/LineHeightSpan.Standard.md) | Default implementation of the [LineHeightSpan](LineHeightSpan.md), which changes the line height of the attached paragraph. | | [LineHeightSpan.WithDensity](../android/text/style/LineHeightSpan.WithDensity.md) | The classes that affect the line height of paragraph with respect to density, should implement this interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The classes that affect the line height of paragraph should implement this interface.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Standard](../android/text/style/LineHeightSpan.Standard.md) Default implementation of the [LineHeightSpan](LineHeightSpan.md), which changes the line height of the attached paragraph. |
| abstract | [WithDensity](../android/text/style/LineHeightSpan.WithDensity.md) The classes that affect the line height of paragraph with respect to density, should implement this interface. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [chooseHeight](LineHeightSpan.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `spanstartv:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lineHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fm:` ` [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md)!`)` Classes that implement this should define how the height is being calculated. |

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
| --- | --- |
| `spanstartv` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the span |
| `lineHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the line height |
| `fm` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md)!:font metrics of the paint, in integers |
| --- | --- |
