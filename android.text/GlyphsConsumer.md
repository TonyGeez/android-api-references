# TextShaper.GlyphsConsumer

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GlyphsConsumer

Kotlin| [Java](https://developer.android.com/reference/android/text/TextShaper.GlyphsConsumer "View this page in Java") 
| --- | --- |

```
interface GlyphsConsumer
```

| [android.text.TextShaper.GlyphsConsumer](https://developer.android.com/reference/kotlin/android/text/TextShaper.GlyphsConsumer#) |

A consumer interface for accepting text shape result.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/android/text/TextShaper.GlyphsConsumer#accept(kotlin.Int,%20kotlin.Int,%20android.graphics.text.PositionedGlyphs,%20android.text.TextPaint))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `glyphs:` ` [PositionedGlyphs](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs.html#)`, `paint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint)`)` Accept text shape result. |

## Public methods

### accept

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(
    start: Int, 
    count: Int, 
    glyphs: PositionedGlyphs, 
    paint: TextPaint
): Unit
```

Accept text shape result. The implementation must not keep reference of paint since it will be mutated for the subsequent styles. Also, for saving heap size, keep only necessary members in the [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint) instead of copying [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint) object.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start index of the shaped text. Value is 0 or greater |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the shaped text. Value is 0 or greater |
| `glyphs` | [PositionedGlyphs](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs.html#):The shape result. This value cannot be`null`. |
| --- | --- |
| `paint` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint):The paint to be used for drawing. This value cannot be`null`. |
