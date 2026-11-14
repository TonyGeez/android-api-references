# TextRunShaper

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextRunShaper

Kotlin| [Java](../android/graphics/text/TextRunShaper.md) 
| --- | --- |

```
open class TextRunShaper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.text.TextRunShaper](../android/graphics/text/TextRunShaper.md) |

Provides conversion from a text into glyph array. Text shaping is a preprocess for drawing text into canvas with glyphs. The glyph is a most primitive unit of the text drawing, consist of glyph identifier in the font file and its position and style. You can draw the shape result to Canvas by calling Canvas#drawGlyphs. For most of the use cases, [android.text.TextShaper](../android/text/TextShaper.md) will provide text shaping functionalities needed. [TextRunShaper](../android/graphics/text/TextRunShaper.md) is a lower level API that is used by [android.text.TextShaper](../android/text/TextShaper.md).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [PositionedGlyphs](../android/graphics/text/PositionedGlyphs.md) | [shapeTextRun](../android/graphics/text/TextRunShaper.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `isRtl:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](../android/graphics/Paint.md)`)` Shape non-styled text. |
| openstatic [PositionedGlyphs](../android/graphics/text/PositionedGlyphs.md) | [shapeTextRun](../android/graphics/text/TextRunShaper.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `isRtl:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](../android/graphics/Paint.md)`)` Shape non-styled text. |

## Public methods

### shapeTextRun

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun shapeTextRun(
    text: CharArray, 
    start: Int, 
    count: Int, 
    contextStart: Int, 
    contextCount: Int, 
    xOffset: Float, 
    yOffset: Float, 
    isRtl: Boolean, 
    paint: Paint
): PositionedGlyphs
```

Shape non-styled text. This function shapes the text of the given range under the context of given context range. Some script, e.g. Arabic or Devanagari, changes letter shape based on its location or surrounding characters.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html):a text buffer to be shaped This value cannot be`null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a start index of shaping target in the buffer. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a length of shaping target in the buffer. |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a start index of context used for shaping in the buffer. |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a length of context used for shaping in the buffer. |
| `xOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):an additional amount of x offset of the result glyphs. |
| --- | --- |
| `yOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):an additional amount of y offset of the result glyphs. |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this text is shaped for RTL direction, false otherwise. |
| `paint` | [Paint](../android/graphics/Paint.md):a paint used for shaping text. This value cannot be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [PositionedGlyphs](../android/graphics/text/PositionedGlyphs.md) | a shape result. This value cannot be`null`. |

### shapeTextRun

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun shapeTextRun(
    text: CharSequence, 
    start: Int, 
    count: Int, 
    contextStart: Int, 
    contextCount: Int, 
    xOffset: Float, 
    yOffset: Float, 
    isRtl: Boolean, 
    paint: Paint
): PositionedGlyphs
```

Shape non-styled text. This function shapes the text of the given range under the context of given context range. Some script, e.g. Arabic or Devanagari, changes letter shape based on its location or surrounding characters.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):a text buffer to be shaped. Any styled spans stored in this text are ignored. This value cannot be`null`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a start index of shaping target in the buffer. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a length of shaping target in the buffer. |
| --- | --- |
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a start index of context used for shaping in the buffer. |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a length of context used for shaping in the buffer. |
| `xOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):an additional amount of x offset of the result glyphs. |
| --- | --- |
| `yOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):an additional amount of y offset of the result glyphs. |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this text is shaped for RTL direction, false otherwise. |
| `paint` | [Paint](../android/graphics/Paint.md):a paint used for shaping text. This value cannot be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [PositionedGlyphs](../android/graphics/text/PositionedGlyphs.md) | a shape result This value cannot be`null`. |
