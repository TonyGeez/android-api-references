# Font

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Font

Kotlin| [Java](https://developer.android.com/reference/android/graphics/fonts/Font "View this page in Java") 
| --- | --- |

```
class Font
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.fonts.Font](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#) |

A font class can be used for creating FontFamily.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font.Builder) A builder class for creating new Font. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FontVariationAxis](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontVariationAxis)!\>? | [getAxes](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getAxes())`()` Get a font variation settings associated with this font |
| [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#) | [getBuffer](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getBuffer())`()` Returns a font file buffer. |
| --- | --- |
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#)? | [getFile](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getFile())`()` Returns a file path of this font. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGlyphBounds](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getGlyphBounds(kotlin.Int,%20android.graphics.Paint,%20android.graphics.RectF))`(`glyphId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)`, `outBoundingBox:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)?`)` Retrieve the glyph horizontal advance and bounding box. |
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | [getLocaleList](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getLocaleList())`()` Get a locale list of this font. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getMetrics](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getMetrics(android.graphics.Paint,%20android.graphics.Paint.FontMetrics))`(`paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)`, `outMetrics:` ` [Paint.FontMetrics](https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics.html#)?`)` Retrieve the font metrics information. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSourceIdentifier](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getSourceIdentifier())`()` Returns the unique ID of the source font data. |
| [FontStyle](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle) | [getStyle](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getStyle())`()` Get a style associated with this font. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTtcIndex](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#getTtcIndex())`()` Get a TTC index value associated with this font. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font#toString())`()` <br /> |
| --- | --- |

## Public methods

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAxes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAxes(): Array<FontVariationAxis!>?
```

Get a font variation settings associated with this font

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FontVariationAxis](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontVariationAxis)!>? | font variation settings This value may be`null`. |

**See Also**

- [android.graphics.fonts.Font.Builder#setFontVariationSettings(String)](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font.Builder#setFontVariationSettings(kotlin.String))
- [android.graphics.fonts.Font.Builder#setFontVariationSettings(FontVariationAxis[])](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font.Builder#setFontVariationSettings(kotlin.Array)) 

### getBuffer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBuffer(): ByteBuffer
```

Returns a font file buffer. Duplicate before reading values by [ByteBuffer.duplicate()](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#duplicate())for avoiding unexpected reading position sharing.

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------|
| [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#) | a font buffer This value cannot be`null`. |

### getFile

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFile(): File?
```

Returns a file path of this font. This returns null if this font is not created from regular file.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#)? | a file path of the font |

### getGlyphBounds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGlyphBounds(
    glyphId: Int, 
    paint: Paint, 
    outBoundingBox: RectF?
): Float
```

Retrieve the glyph horizontal advance and bounding box. Note that [android.graphics.Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#) in [android.graphics.Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#) is ignored.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `glyphId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a glyph ID Value is 0 or greater |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#):a paint object used for resolving glyph style This value cannot be`null`. |
| `outBoundingBox` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)?:a nullable destination object. If null is passed, this function just return the horizontal advance. If non-null is passed, this function fills bounding box information to this object. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the amount of horizontal advance in pixels |

### getLocaleList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocaleList(): LocaleList
```

Get a locale list of this font. This is always empty if this font is not a system font.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------|
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) | a locale list This value cannot be`null`. |

### getMetrics

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetrics(
    paint: Paint, 
    outMetrics: Paint.FontMetrics?
): Unit
```

Retrieve the font metrics information. Note that [android.graphics.Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#) in [android.graphics.Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#) is ignored.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#):a paint object used for retrieving font metrics. This value cannot be`null`. |
| `outMetrics` | [Paint.FontMetrics](https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetrics.html#)?:a nullable destination object. If null is passed, this function only retrieve recommended interline spacing. If non-null is passed, this function fills to font metrics to it. |

**See Also**

- [android.graphics.Paint#getFontMetrics()](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetrics())
- [android.graphics.Paint#getFontMetricsInt()](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#getFontMetricsInt()) 

### getSourceIdentifier

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSourceIdentifier(): Int
```

Returns the unique ID of the source font data. You can use this identifier as a key of the cache or checking if two fonts can be interpolated with font variation settings. 

```kotlin
<code>
    // Following three Fonts, fontA, fontB, fontC have the same identifier.
    Font fontA = new Font.Builder("/path/to/font").build();
    Font fontB = new Font.Builder(fontA).setTtcIndex(1).build();
    Font fontC = new Font.Builder(fontB).setFontVariationSettings("'wght' 700).build();
 
    // Following fontD has the different identifier from above three.
    Font fontD = new Font.Builder("/path/to/another/font").build();
 
    // Following fontE has different identifier from above four even the font path is the same.
    // To get the same identifier, please create new Font instance from existing fonts.
    Font fontE = new Font.Builder("/path/to/font").build();
  </code>
```
Here is an example of caching font object that has 

```kotlin
<code>
    private LongSparseArray
 <sparsearray<font>
  &gt; mCache = new LongSparseArray&lt;&gt;(); private Font getFontWeightVariation(Font font, int weight) { // Different collection index is treated as different font. long key = ((long) font.getSourceIdentifier()) &lt;&lt; 32 | (long) font.getTtcIndex(); SparseArray
  <font> weightCache = mCache.get(key); if (weightCache == null) { weightCache = new SparseArray&lt;&gt;(); mCache.put(key, weightCache); } Font cachedFont = weightCache.get(weight); if (cachedFont != null) { return cachedFont; } Font newFont = new Font.Builder(cachedFont) .setFontVariationSettings("'wght' " + weight); .build(); weightCache.put(weight, newFont); return newFont; } </font>
 </sparsearray<font></code><font>
  </font>
```

<br />

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an unique identifier for the font source data. |

### getStyle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStyle(): FontStyle
```

Get a style associated with this font.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [FontStyle](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle) | a font style This value cannot be`null`. |

**See Also**

- [android.graphics.fonts.Font.Builder#setWeight(int)](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font.Builder#setWeight(kotlin.Int))
- [android.graphics.fonts.Font.Builder#setSlant(int)](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font.Builder#setSlant(kotlin.Int)) 

### getTtcIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTtcIndex(): Int
```

Get a TTC index value associated with this font. If TTF/OTF file is provided, this value is always 0.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a TTC index value Value is 0 or greater |

**See Also**

- [android.graphics.fonts.Font.Builder#setTtcIndex(int)](https://developer.android.com/reference/kotlin/android/graphics/fonts/Font.Builder#setTtcIndex(kotlin.Int)) 

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
