# PositionedGlyphs

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PositionedGlyphs

Kotlin| [Java](https://developer.android.com/reference/android/graphics/text/PositionedGlyphs "View this page in Java") 
| --- | --- |

```
class PositionedGlyphs
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.text.PositionedGlyphs](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#) |

Text shaping result object for single style text. You can get text shaping result by[TextRunShaper.shapeTextRun(char[], int, int, int, int, float, float, boolean, Paint)](https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper#shapeTextRun(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint))and [TextRunShaper.shapeTextRun(CharSequence, int, int, int, int, float, float, boolean,](https://developer.android.com/reference/kotlin/android/graphics/text/TextRunShaper#shapeTextRun(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float,%20kotlin.Boolean,%20android.graphics.Paint)).

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [NO_OVERRIDE](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#NO_OVERRIDE:kotlin.Float) A special value returned by [getWeightOverride(int)](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getWeightOverride(kotlin.Int))and [getItalicOverride(int)](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getItalicOverride(kotlin.Int))that indicates no font variation setting is overridden. |

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAdvance](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getAdvance())`()` Returns the total amount of advance consumed by this positioned glyphs. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAscent](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getAscent())`()` Effective ascent value of this positioned glyphs. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDescent](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getDescent())`()` Effective descent value of this positioned glyphs. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFakeBold](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getFakeBold(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the fake bold option used for drawing, otherwise false. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFakeItalic](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getFakeItalic(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the fake italic option used for drawing, otherwise false. |
| --- | --- |
| [Font](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font.html#) | [getFont](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getFont(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the font object used for drawing the glyph at the given index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlyphId](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getGlyphId(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the glyph ID used for drawing the glyph at the given index. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGlyphX](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getGlyphX(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the x coordinate of the glyph position at the given index. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGlyphY](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getGlyphY(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the y coordinate of the glyph position at the given index. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getItalicOverride](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getItalicOverride(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns overridden italic value if the font is variable font and \`ital\` value is overridden for drawing. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getOffsetX](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getOffsetX())`()` Returns the amount of X offset added to glyph position. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getOffsetY](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getOffsetY())`()` Returns the amount of Y offset added to glyph position. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWeightOverride](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getWeightOverride(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns overridden weight value if the font is variable font and \`wght\` value is overridden for drawing. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [glyphCount](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#glyphCount())`()` Returns the number of glyphs stored. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#toString())`()` <br /> |

## Constants

### NO_OVERRIDE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_OVERRIDE: Float
```

A special value returned by [getWeightOverride(int)](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getWeightOverride(kotlin.Int))and [getItalicOverride(int)](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#getItalicOverride(kotlin.Int))that indicates no font variation setting is overridden. 

 Value: 1.4E-45f

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAdvance

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvance(): Float
```

Returns the total amount of advance consumed by this positioned glyphs. The advance is an amount of width consumed by the glyph. The total amount of advance is a total amount of advance consumed by this series of glyphs. In other words, if another glyph is placed next to this series of glyphs, it's X offset should be shifted this amount of width.

| Return ||
|--------------------------------------------------------------------------------|-------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | total amount of advance |

### getAscent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAscent(): Float
```

Effective ascent value of this positioned glyphs. If two or more font files are used in this series of glyphs, the effective ascent will be the minimum ascent value across the all font files.

| Return ||
|--------------------------------------------------------------------------------|------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | effective ascent value |

### getDescent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescent(): Float
```

Effective descent value of this positioned glyphs. If two or more font files are used in this series of glyphs, the effective descent will be the maximum descent value across the all font files.

| Return ||
|--------------------------------------------------------------------------------|-------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | effective descent value |

### getFakeBold

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFakeBold(index: Int): Boolean
```

Returns true if the fake bold option used for drawing, otherwise false.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the glyph index Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the fake bold option is on, otherwise off. |

### getFakeItalic

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFakeItalic(index: Int): Boolean
```

Returns true if the fake italic option used for drawing, otherwise false.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the glyph index Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the fake italic option is on, otherwise off. |

### getFont

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFont(index: Int): Font
```

Returns the font object used for drawing the glyph at the given index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the glyph index Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Font](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font.html#) | the font object used for drawing the glyph at the given index This value cannot be`null`. |

### getGlyphId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGlyphId(index: Int): Int
```

Returns the glyph ID used for drawing the glyph at the given index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the glyph index Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A glyph ID of the font. Value is 0 or greater |

### getGlyphX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGlyphX(index: Int): Float
```

Returns the x coordinate of the glyph position at the given index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the glyph index Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|----------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A X offset in pixels |

### getGlyphY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGlyphY(index: Int): Float
```

Returns the y coordinate of the glyph position at the given index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the glyph index Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|-----------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A Y offset in pixels. |

### getItalicOverride

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getItalicOverride(index: Int): Float
```

Returns overridden italic value if the font is variable font and \`ital\` value is overridden for drawing. Otherwise returns [NO_OVERRIDE](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#NO_OVERRIDE:kotlin.Float).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the glyph index Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | overridden weight value or [NO_OVERRIDE](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#NO_OVERRIDE:kotlin.Float). |

### getOffsetX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffsetX(): Float
```

Returns the amount of X offset added to glyph position.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The X offset added to glyph position. |

### getOffsetY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffsetY(): Float
```

Returns the amount of Y offset added to glyph position.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The Y offset added to glyph position. |

### getWeightOverride

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWeightOverride(index: Int): Float
```

Returns overridden weight value if the font is variable font and \`wght\` value is overridden for drawing. Otherwise returns [NO_OVERRIDE](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#NO_OVERRIDE:kotlin.Float).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the glyph index Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | overridden weight value or [NO_OVERRIDE](https://developer.android.com/reference/kotlin/android/graphics/text/PositionedGlyphs#NO_OVERRIDE:kotlin.Float). |

### glyphCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun glyphCount(): Int
```

Returns the number of glyphs stored.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of glyphs Value is 0 or greater |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
