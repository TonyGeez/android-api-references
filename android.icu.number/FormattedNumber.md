# FormattedNumber

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormattedNumber

Kotlin| [Java](https://developer.android.com/reference/android/icu/number/FormattedNumber "View this page in Java") 
| --- | --- |

```
open class FormattedNumber : FormattedValue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#) |

The result of a number formatting operation. This class allows the result to be exported in several data types, including a String, an AttributedCharacterIterator, and a BigDecimal. Instances of this class are immutable and thread-safe.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openA | [appendTo](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#appendTo(android.icu.number.FormattedNumber.appendTo.A))`(`appendable:` `A`)` Appends the formatted string to an Appendable. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#get(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the`char`value at the specified index. |
| open [DisplayOptions.NounClass](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.NounClass.html#)! | [getNounClass](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#getNounClass())`()` Gets the noun class of the formatted output. |
| --- | --- |
| open [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.html#)! | [getOutputUnit](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#getOutputUnit())`()` Gets the resolved output unit. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextPosition](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#nextPosition(android.icu.text.ConstrainedFieldPosition))`(`cfpos:` ` [ConstrainedFieldPosition](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition.html#)!`)` Iterates over field positions in the FormattedValue. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [subSequence](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#subSequence(kotlin.Int,%20kotlin.Int))`(`startIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`CharSequence`that is a subsequence of this sequence. |
| --- | --- |
| open [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | [toBigDecimal](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#toBigDecimal())`()` Export the formatted number as a BigDecimal. |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)! | [toCharacterIterator](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#toCharacterIterator())`()` Exports the formatted number as an AttributedCharacterIterator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#toString())`()` Returns a string representation of the object. |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber#length:kotlin.Int) Returns the length of this character sequence. |

## Public methods

### appendTo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <A : Appendable!> appendTo(appendable: A): A
```

Appends the formatted string to an Appendable.

If an IOException occurs when appending to the Appendable, an unchecked [ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException.html#) is thrown instead.

| Parameters ||
|--------------|--------------------------------------------------------|
| `appendable` | A:The Appendable to which to append the string output. |

| Return ||
|---|------------------------------------|
| A | The same Appendable, for chaining. |

| Exceptions ||
|--------------------------------------------|--------------------------------------|
| `android.icu.util.ICUUncheckedIOException` | if the Appendable throws IOException |

### get

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(index: Int): Char
```

Returns the`char`value at the specified index. An index ranges from zero to`length() - 1`. The first`char`value of the sequence is at index zero, the next at index one, and so on, as for array indexing.

If the`char`value specified by the index is a [surrogate](https://developer.android.com//reference/java/lang/Character.html#unicode), the surrogate value is returned.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the`char`value to be returned |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the specified`char`value |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the`index`argument is negative or not less than`length()` |

### getNounClass

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNounClass(): DisplayOptions.NounClass!
```

Gets the noun class of the formatted output. Returns`UNDEFINED`when the noun class is not supported yet.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|-----------|
| [DisplayOptions.NounClass](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.NounClass.html#)! | NounClass |

### getOutputUnit

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputUnit(): MeasureUnit!
```

Gets the resolved output unit.

The output unit is dependent upon the localized preferences for the usage specified via NumberFormatterSettings.usage(), and may be a unit with MeasureUnit.Complexity.MIXED unit complexity (MeasureUnit.getComplexity()), such as "foot-and-inch" or "hour-and-minute-and-second".

| Return ||
|---------------------------------------------------------------------------------------------------|----------------|
| [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.html#)! | `MeasureUnit`. |

### nextPosition

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextPosition(cfpos: ConstrainedFieldPosition!): Boolean
```

Iterates over field positions in the FormattedValue. This lets you determine the position of specific types of substrings, like a month or a decimal separator. To loop over all field positions: 

```kotlin
ConstrainedFieldPosition cfpos = new ConstrainedFieldPosition();
      while (fmtval.nextPosition(cfpos)) {
          // handle the field position; get information from cfpos
      }
  
```

<br />

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cfpos` | [ConstrainedFieldPosition](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition.html#)!:The object used for iteration state. This can provide constraints to iterate over only one specific field; see [ConstrainedFieldPosition.constrainField](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition.html#constrainField(java.text.Format.Field)). |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a new occurrence of the field was found; false otherwise. |

### subSequence

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharSequence
```

Returns a`CharSequence`that is a subsequence of this sequence. The subsequence starts with the`char`value at the specified index and ends with the`char`value at index`end - 1`. The length (in`char`s) of the returned sequence is`end - start`, so if`start == end`then an empty sequence is returned.

| Parameters ||
|---------|----------------------------|
| `start` | the start index, inclusive |
| `end` | the end index, exclusive |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the specified subsequence |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`start`or`end`are negative, if`end`is greater than`length()`, or if`start`is greater than`end` |

### toBigDecimal

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toBigDecimal(): BigDecimal!
```

Export the formatted number as a BigDecimal. This endpoint is useful for obtaining the exact number being printed after scaling and rounding have been applied by the number formatting pipeline.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | A BigDecimal representation of the formatted number. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### toCharacterIterator

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toCharacterIterator(): AttributedCharacterIterator!
```

Exports the formatted number as an AttributedCharacterIterator.

Consider using [nextPosition](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue.html#nextPosition(android.icu.text.ConstrainedFieldPosition))if you are trying to get field information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)! | An AttributedCharacterIterator containing full field information. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The formatted string. |

## Properties

### length

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val length: Int
```

Returns the length of this character sequence. The length is the number of 16-bit`char`s in the sequence.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of`char`s in this sequence |
