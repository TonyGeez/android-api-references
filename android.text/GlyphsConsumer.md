# TextShaper.GlyphsConsumer

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GlyphsConsumer

Kotlin| [Java](../android/text/TextShaper.GlyphsConsumer.md) 
| --- | --- |

```
interface GlyphsConsumer
```

| [android.text.TextShaper.GlyphsConsumer](../android/text/TextShaper.GlyphsConsumer.md) |

A consumer interface for accepting text shape result.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](../android/text/TextShaper.GlyphsConsumer.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `glyphs:` ` [PositionedGlyphs](../android.graphics.text/PositionedGlyphs.md)`, `paint:` ` [TextPaint](TextPaint.md)`)` Accept text shape result. |

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

Accept text shape result. The implementation must not keep reference of paint since it will be mutated for the subsequent styles. Also, for saving heap size, keep only necessary members in the [TextPaint](TextPaint.md) instead of copying [TextPaint](TextPaint.md) object.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start index of the shaped text. Value is 0 or greater |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The length of the shaped text. Value is 0 or greater |
| `glyphs` | [PositionedGlyphs](../android.graphics.text/PositionedGlyphs.md):The shape result. This value cannot be`null`. |
| --- | --- |
| `paint` | [TextPaint](TextPaint.md):The paint to be used for drawing. This value cannot be`null`. |
