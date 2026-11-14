# NumericShaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumericShaper

```
class NumericShaper : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.awt.font.NumericShaper](NumericShaper.md) |

The class is used to convert Latin-1 (European) digits to other Unicode decimal digits. Users of this class will primarily be people who wish to present data using national digit shapes, but find it more convenient to represent the data internally using Latin-1 (European) digits. This does not interpret the deprecated numeric shape selector character (U+206E).

Instances of`NumericShaper`are typically applied as attributes to text with the [NUMERIC_SHAPING](TextAttribute.md) attribute of the`TextAttribute`class. For example, this code snippet causes a`TextLayout`to shape European digits to Arabic in an Arabic context: 

```kotlin
Map map = new HashMap();
  map.put(TextAttribute.NUMERIC_SHAPING,
      NumericShaper.getContextualShaper(NumericShaper.ARABIC));
  FontRenderContext frc = ...;
  TextLayout layout = new TextLayout(text, map, frc);
  layout.draw(g2d, x, y);
  
```

It is also possible to perform numeric shaping explicitly using instances of`NumericShaper`, as this code snippet demonstrates: 

```kotlin
char[] text = ...;
  // shape all EUROPEAN digits (except zero) to ARABIC digits
  NumericShaper shaper = NumericShaper.getShaper(NumericShaper.ARABIC);
  shaper.shape(text, start, count);
 
  // shape European digits to ARABIC digits if preceding text is Arabic, or
  // shape European digits to TAMIL digits if preceding text is Tamil, or
  // leave European digits alone if there is no preceding text, or
  // preceding text is neither Arabic nor Tamil
  NumericShaper shaper =
      NumericShaper.getContextualShaper(NumericShaper.ARABIC |
                                          NumericShaper.TAMIL,
                                        NumericShaper.EUROPEAN);
  shaper.shape(text, start, count);
  
```

**Bit mask- and enum-based Unicode ranges**

This class supports two different programming interfaces to represent Unicode ranges for script-specific digits: bit mask-based ones, such as [NumericShaper.ARABIC](NumericShaper.md), and enum-based ones, such as [NumericShaper.Range.ARABIC](../java/awt/font/NumericShaper.Range.md). Multiple ranges can be specified by ORing bit mask-based constants, such as: 

```kotlin
NumericShaper.ARABIC | NumericShaper.TAMIL
  
```
or creating a`Set`with the [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md) constants, such as: 

```kotlin
EnumSet.of(NumericShaper.Scirpt.ARABIC, NumericShaper.Range.TAMIL)
  
```
The enum-based ranges are a super set of the bit mask-based ones.

If the two interfaces are mixed (including serialization), Unicode range values are mapped to their counterparts where such mapping is possible, such as`NumericShaper.Range.ARABIC`from/to`NumericShaper.ARABIC`. If any unmappable range values are specified, such as`NumericShaper.Range.BALINESE`, those ranges are ignored.

**Decimal Digits Precedence**

A Unicode range may have more than one set of decimal digits. If multiple decimal digits sets are specified for the same Unicode range, one of the sets will take precedence as follows.

| Unicode Range | `NumericShaper`Constants | Precedence |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Arabic | [NumericShaper.ARABIC](NumericShaper.md) [NumericShaper.EASTERN_ARABIC](NumericShaper.md) | [NumericShaper.EASTERN_ARABIC](NumericShaper.md) |
| Arabic | [NumericShaper.Range.ARABIC](../java/awt/font/NumericShaper.Range.md) [NumericShaper.Range.EASTERN_ARABIC](../java/awt/font/NumericShaper.Range.md) | [NumericShaper.Range.EASTERN_ARABIC](../java/awt/font/NumericShaper.Range.md) |
| Tai Tham | [NumericShaper.Range.TAI_THAM_HORA](../java/awt/font/NumericShaper.Range.md) [NumericShaper.Range.TAI_THAM_THAM](../java/awt/font/NumericShaper.Range.md) | [NumericShaper.Range.TAI_THAM_THAM](../java/awt/font/NumericShaper.Range.md) |
| --- | --- | --- |

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Range](../java/awt/font/NumericShaper.Range.md) A`NumericShaper.Range`represents a Unicode range of a script having its own decimal digits. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALL_RANGES](NumericShaper.md) Identifies all ranges, for full contextual shaping. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ARABIC](NumericShaper.md) Identifies the ARABIC range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BENGALI](NumericShaper.md) Identifies the BENGALI range and decimal base. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVANAGARI](NumericShaper.md) Identifies the DEVANAGARI range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EASTERN_ARABIC](NumericShaper.md) Identifies the ARABIC range and ARABIC_EXTENDED decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ETHIOPIC](NumericShaper.md) Identifies the ETHIOPIC range and decimal base. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EUROPEAN](NumericShaper.md) Identifies the Latin-1 (European) and extended range, and Latin-1 (European) decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GUJARATI](NumericShaper.md) Identifies the GUJARATI range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GURMUKHI](NumericShaper.md) Identifies the GURMUKHI range and decimal base. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KANNADA](NumericShaper.md) Identifies the KANNADA range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KHMER](NumericShaper.md) Identifies the KHMER range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LAO](NumericShaper.md) Identifies the LAO range and decimal base. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MALAYALAM](NumericShaper.md) Identifies the MALAYALAM range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONGOLIAN](NumericShaper.md) Identifies the MONGOLIAN range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MYANMAR](NumericShaper.md) Identifies the MYANMAR range and decimal base. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIYA](NumericShaper.md) Identifies the ORIYA range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TAMIL](NumericShaper.md) Identifies the TAMIL range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TELUGU](NumericShaper.md) Identifies the TELUGU range and decimal base. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THAI](NumericShaper.md) Identifies the THAI range and decimal base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIBETAN](NumericShaper.md) Identifies the TIBETAN range and decimal base. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](NumericShaper.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns`true`if the specified object is an instance of`NumericShaper`and shapes identically to this one, regardless of the range representations, the bit mask or the enum. |
| static [NumericShaper](NumericShaper.md)! | [getContextualShaper](NumericShaper.md))`(`ranges:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a contextual shaper for the provided unicode range(s). |
| static [NumericShaper](NumericShaper.md)! | [getContextualShaper](NumericShaper.md))`(`ranges:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultContext:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a contextual shaper for the provided unicode range(s). |
| --- | --- |
| static [NumericShaper](NumericShaper.md)! | [getContextualShaper](NumericShaper.md))`(`ranges:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!>!`)` Returns a contextual shaper for the provided Unicode range(s). |
| static [NumericShaper](NumericShaper.md)! | [getContextualShaper](NumericShaper.md))`(`ranges:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!>!`, `defaultContext:` ` [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!`)` Returns a contextual shaper for the provided Unicode range(s). |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!\>! | [getRangeSet](NumericShaper.md))`()` Returns a`Set`representing all the Unicode ranges in this`NumericShaper`that will be shaped. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRanges](NumericShaper.md))`()` Returns an`int`that ORs together the values for all the ranges that will be shaped. |
| static [NumericShaper](NumericShaper.md)! | [getShaper](NumericShaper.md))`(`singleRange:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a shaper for the provided unicode range. |
| static [NumericShaper](NumericShaper.md)! | [getShaper](NumericShaper.md))`(`singleRange:` ` [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!`)` Returns a shaper for the provided Unicode range. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](NumericShaper.md))`()` Returns a hash code for this shaper. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isContextual](NumericShaper.md))`()` Returns a`boolean`indicating whether or not this shaper shapes contextually. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shape](NumericShaper.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts the digits in the text that occur between start and start + count. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shape](NumericShaper.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts the digits in the text that occur between start and start + count, using the provided context. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shape](NumericShaper.md))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `context:` ` [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!`)` Converts the digits in the text that occur between`start`and`start + count`, using the provided`context`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](NumericShaper.md))`()` Returns a`String`that describes this shaper. |
| --- | --- |

## Constants

### ALL_RANGES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL_RANGES: Int
```

Identifies all ranges, for full contextual shaping.

This constant specifies all of the bit mask-based ranges. Use`EmunSet.allOf(NumericShaper.Range.class)`to specify all of the enum-based ranges. 

 Value: 524287

### ARABIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ARABIC: Int
```

Identifies the ARABIC range and decimal base. 

 Value: 2

### BENGALI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BENGALI: Int
```

Identifies the BENGALI range and decimal base. 

 Value: 16

### DEVANAGARI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVANAGARI: Int
```

Identifies the DEVANAGARI range and decimal base. 

 Value: 8

### EASTERN_ARABIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EASTERN_ARABIC: Int
```

Identifies the ARABIC range and ARABIC_EXTENDED decimal base. 

 Value: 4

### ETHIOPIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ETHIOPIC: Int
```

Identifies the ETHIOPIC range and decimal base. 

 Value: 65536

### EUROPEAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EUROPEAN: Int
```

Identifies the Latin-1 (European) and extended range, and Latin-1 (European) decimal base. 

 Value: 1

### GUJARATI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GUJARATI: Int
```

Identifies the GUJARATI range and decimal base. 

 Value: 64

### GURMUKHI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GURMUKHI: Int
```

Identifies the GURMUKHI range and decimal base. 

 Value: 32

### KANNADA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KANNADA: Int
```

Identifies the KANNADA range and decimal base. 

 Value: 1024

### KHMER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KHMER: Int
```

Identifies the KHMER range and decimal base. 

 Value: 131072

### LAO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LAO: Int
```

Identifies the LAO range and decimal base. 

 Value: 8192

### MALAYALAM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MALAYALAM: Int
```

Identifies the MALAYALAM range and decimal base. 

 Value: 2048

### MONGOLIAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MONGOLIAN: Int
```

Identifies the MONGOLIAN range and decimal base. 

 Value: 262144

### MYANMAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MYANMAR: Int
```

Identifies the MYANMAR range and decimal base. 

 Value: 32768

### ORIYA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIYA: Int
```

Identifies the ORIYA range and decimal base. 

 Value: 128

### TAMIL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAMIL: Int
```

Identifies the TAMIL range and decimal base. 

 Value: 256

### TELUGU

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TELUGU: Int
```

Identifies the TELUGU range and decimal base. 

 Value: 512

### THAI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val THAI: Int
```

Identifies the THAI range and decimal base. 

 Value: 4096

### TIBETAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIBETAN: Int
```

Identifies the TIBETAN range and decimal base. 

 Value: 16384

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Returns`true`if the specified object is an instance of`NumericShaper`and shapes identically to this one, regardless of the range representations, the bit mask or the enum. For example, the following code produces`"true"`. 

```kotlin
NumericShaper ns1 = NumericShaper.getShaper(NumericShaper.ARABIC);
  NumericShaper ns2 = NumericShaper.getShaper(NumericShaper.Range.ARABIC);
  System.out.println(ns1.equals(ns2));
  
```

<br />

| Parameters ||
|-------|--------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the specified object to compare to this`NumericShaper` |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`o`is an instance of`NumericShaper`and shapes in the same way;`false`otherwise. |

**See Also**

- [java.lang.Object#equals(java.lang.Object)](../java.lang/Object.md)) 

### getContextualShaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getContextualShaper(ranges: Int): NumericShaper!
```

Returns a contextual shaper for the provided unicode range(s). Latin-1 (EUROPEAN) digits are converted to the decimal digits corresponding to the range of the preceding text, if the range is one of the provided ranges. Multiple ranges are represented by or-ing the values together, such as,`NumericShaper.ARABIC | NumericShaper.THAI`. The shaper assumes EUROPEAN as the starting context, that is, if EUROPEAN digits are encountered before any strong directional text in the string, the context is presumed to be EUROPEAN, and so the digits will not shape.
| --- | --- |

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `ranges` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the specified Unicode ranges |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------|
| [NumericShaper](NumericShaper.md)! | a shaper for the specified ranges |

### getContextualShaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getContextualShaper(
    ranges: Int, 
    defaultContext: Int
): NumericShaper!
```

Returns a contextual shaper for the provided unicode range(s). Latin-1 (EUROPEAN) digits will be converted to the decimal digits corresponding to the range of the preceding text, if the range is one of the provided ranges. Multiple ranges are represented by or-ing the values together, for example,`NumericShaper.ARABIC | NumericShaper.THAI`. The shaper uses defaultContext as the starting context.
| --- | --- |

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `ranges` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the specified Unicode ranges |
| `defaultContext` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the starting context, such as`NumericShaper.EUROPEAN` |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------|
| [NumericShaper](NumericShaper.md)! | a shaper for the specified Unicode ranges. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified`defaultContext`is not a single valid range. |

### getContextualShaper

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getContextualShaper(ranges: MutableSet<NumericShaper.Range!>!): NumericShaper!
```

Returns a contextual shaper for the provided Unicode range(s). The Latin-1 (EUROPEAN) digits are converted to the decimal digits corresponding to the range of the preceding text, if the range is one of the provided ranges.

The shaper assumes EUROPEAN as the starting context, that is, if EUROPEAN digits are encountered before any strong directional text in the string, the context is presumed to be EUROPEAN, and so the digits will not shape.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ranges` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!\>!:the specified Unicode ranges |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| [NumericShaper](NumericShaper.md)! | a contextual shaper for the specified ranges |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if`ranges`is`null`. |

### getContextualShaper

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getContextualShaper(
    ranges: MutableSet<NumericShaper.Range!>!, 
    defaultContext: NumericShaper.Range!
): NumericShaper!
```

Returns a contextual shaper for the provided Unicode range(s). The Latin-1 (EUROPEAN) digits will be converted to the decimal digits corresponding to the range of the preceding text, if the range is one of the provided ranges. The shaper uses`defaultContext`as the starting context.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ranges` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!\>!:the specified Unicode ranges |
| `defaultContext` | [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!:the starting context, such as`NumericShaper.Range.EUROPEAN` |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [NumericShaper](NumericShaper.md)! | a contextual shaper for the specified Unicode ranges. |

| Exceptions ||
|----------------------------------|--------------------------------------|
| `java.lang.NullPointerException` | if`ranges`or`defaultContext`is`null` |

### getRangeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangeSet(): MutableSet<NumericShaper.Range!>!
```

Returns a`Set`representing all the Unicode ranges in this`NumericShaper`that will be shaped.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!>! | all the Unicode ranges to be shaped. |

### getRanges

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRanges(): Int
```

Returns an`int`that ORs together the values for all the ranges that will be shaped.

For example, to check if a shaper shapes to Arabic, you would use the following:
`if ((shaper.getRanges() & shaper.ARABIC) != 0) &#123; ... `

Note that this method supports only the bit mask-based ranges. Call [getRangeSet()](NumericShaper.md))for the enum-based ranges.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the values for all the ranges to be shaped. |

### getShaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getShaper(singleRange: Int): NumericShaper!
```

Returns a shaper for the provided unicode range. All Latin-1 (EUROPEAN) digits are converted to the corresponding decimal unicode digits.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------|
| `singleRange` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the specified Unicode range |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------|
| [NumericShaper](NumericShaper.md)! | a non-contextual numeric shaper |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | if the range is not a single range |

### getShaper

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getShaper(singleRange: NumericShaper.Range!): NumericShaper!
```

Returns a shaper for the provided Unicode range. All Latin-1 (EUROPEAN) digits are converted to the corresponding decimal digits of the specified Unicode range.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `singleRange` | [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!:the Unicode range given by a [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md) constant. |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------|
| [NumericShaper](NumericShaper.md)! | a non-contextual`NumericShaper`. |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if`singleRange`is`null` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code for this shaper.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this shaper's hash code. |

**See Also**

- [java.lang.Object#hashCode](../java.lang/Object.md)) 

### isContextual

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isContextual(): Boolean
```

Returns a`boolean`indicating whether or not this shaper shapes contextually.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this shaper is contextual;`false`otherwise. |

### shape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shape(
    text: CharArray!, 
    start: Int, 
    count: Int
): Unit
```

Converts the digits in the text that occur between start and start + count.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array of characters to convert |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into`text`to start converting |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters in`text`to convert |
| --- | --- |

| Exceptions ||
|---------------------------------------|--------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if start or start + count is out of bounds |
| `java.lang.NullPointerException` | if text is null |

### shape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shape(
    text: CharArray!, 
    start: Int, 
    count: Int, 
    context: Int
): Unit
```

Converts the digits in the text that occur between start and start + count, using the provided context. Context is ignored if the shaper is not a contextual shaper.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array of characters |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into`text`to start converting |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters in`text`to convert |
| --- | --- |
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the context to which to convert the characters, such as`NumericShaper.EUROPEAN` |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if start or start + count is out of bounds |
| `java.lang.NullPointerException` | if text is null |
| `java.lang.IllegalArgumentException` | if this is a contextual shaper and the specified`context`is not a single valid range. |
| --- | --- |

### shape

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shape(
    text: CharArray!, 
    start: Int, 
    count: Int, 
    context: NumericShaper.Range!
): Unit
```

Converts the digits in the text that occur between`start`and`start + count`, using the provided`context`.`Context`is ignored if the shaper is not a contextual shaper.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:a`char`array |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into`text`to start converting |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of`char`s in`text`to convert |
| --- | --- |
| `context` | [NumericShaper.Range](../java/awt/font/NumericShaper.Range.md)!:the context to which to convert the characters, such as`NumericShaper.Range.EUROPEAN` |

| Exceptions ||
|---------------------------------------|--------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`start`or`start + count`is out of bounds |
| `java.lang.NullPointerException` | if`text`or`context`is null |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a`String`that describes this shaper. This method is used for debugging purposes only.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`describing this shaper. |
