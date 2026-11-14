# TextRunShaper

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextRunShaper

Kotlin| [Java](https://developer.android.com/reference/android/graphics/text/TextRunShaper "View this page in Java") 

```
open class TextRunShaper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.text.TextRunShaper](https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper#) |

Provides conversion from a text into glyph array. Text shaping is a preprocess for drawing text into canvas with glyphs. The glyph is a most primitive unit of the text drawing, consist of glyph identifier in the font file and its position and style. You can draw the shape result to Canvas by calling Canvas#drawGlyphs. For most of the use cases, [android.text.TextShaper](https://developer.android.com/reference/kotlin/android/text/TextShaper.html#) will provide text shaping functionalities needed. [TextRunShaper](https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper#) is a lower level API that is used by [android.text.TextShaper](https://developer.android.com/reference/kotlin/android/text/TextShaper.html#).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [PositionedGlyphs](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs) | [shapeTextRun](https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper#shapeTextRun(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `isRtl:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)`)` Shape non-styled text. |
| openstatic [PositionedGlyphs](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs) | [shapeTextRun](https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper#shapeTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `contextCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yOffset:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `isRtl:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)`)` Shape non-styled text. |

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
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a start index of context used for shaping in the buffer. |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a length of context used for shaping in the buffer. |
| `xOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):an additional amount of x offset of the result glyphs. |
| `yOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):an additional amount of y offset of the result glyphs. |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this text is shaped for RTL direction, false otherwise. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#):a paint used for shaping text. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [PositionedGlyphs](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs) | a shape result. This value cannot be`null`. |

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
| `contextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a start index of context used for shaping in the buffer. |
| `contextCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a length of context used for shaping in the buffer. |
| `xOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):an additional amount of x offset of the result glyphs. |
| `yOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):an additional amount of y offset of the result glyphs. |
| `isRtl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this text is shaped for RTL direction, false otherwise. |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#):a paint used for shaping text. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [PositionedGlyphs](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs) | a shape result This value cannot be`null`. |
