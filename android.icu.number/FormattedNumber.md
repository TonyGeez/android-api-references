# FormattedNumber

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormattedNumber

Kotlin| [Java](../android/icu/number/FormattedNumber.md) 
| --- | --- |

```
open class FormattedNumber : FormattedValue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.FormattedNumber](../android/icu/number/FormattedNumber.md) |

The result of a number formatting operation. This class allows the result to be exported in several data types, including a String, an AttributedCharacterIterator, and a BigDecimal. Instances of this class are immutable and thread-safe.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openA | [appendTo](../android/icu/number/FormattedNumber.md))`(`appendable:` `A`)` Appends the formatted string to an Appendable. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](../android/icu/number/FormattedNumber.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the`char`value at the specified index. |
| open [DisplayOptions.NounClass](../android/icu/text/DisplayOptions.NounClass.md)! | [getNounClass](../android/icu/number/FormattedNumber.md))`()` Gets the noun class of the formatted output. |
| --- | --- |
| open [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [getOutputUnit](../android/icu/number/FormattedNumber.md))`()` Gets the resolved output unit. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextPosition](../android/icu/number/FormattedNumber.md))`(`cfpos:` ` [ConstrainedFieldPosition](../android/icu/text/ConstrainedFieldPosition.md)!`)` Iterates over field positions in the FormattedValue. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [subSequence](../android/icu/number/FormattedNumber.md))`(`startIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`CharSequence`that is a subsequence of this sequence. |
| --- | --- |
| open [BigDecimal](../java/math/BigDecimal.md)! | [toBigDecimal](../android/icu/number/FormattedNumber.md))`()` Export the formatted number as a BigDecimal. |
| open [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | [toCharacterIterator](../android/icu/number/FormattedNumber.md))`()` Exports the formatted number as an AttributedCharacterIterator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/icu/number/FormattedNumber.md))`()` Returns a string representation of the object. |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](../android/icu/number/FormattedNumber.md) Returns the length of this character sequence. |

## Public methods

### appendTo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <A : Appendable!> appendTo(appendable: A): A
```

Appends the formatted string to an Appendable.

If an IOException occurs when appending to the Appendable, an unchecked [ICUUncheckedIOException](../android/icu/util/ICUUncheckedIOException.md) is thrown instead.

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
| [DisplayOptions.NounClass](../android/icu/text/DisplayOptions.NounClass.md)! | NounClass |

### getOutputUnit

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputUnit(): MeasureUnit!
```

Gets the resolved output unit.

The output unit is dependent upon the localized preferences for the usage specified via NumberFormatterSettings.usage(), and may be a unit with MeasureUnit.Complexity.MIXED unit complexity (MeasureUnit.getComplexity()), such as "foot-and-inch" or "hour-and-minute-and-second".

| Return ||
|---------------------------------------------------------------------------------------------------|----------------|
| [MeasureUnit](../android/icu/util/MeasureUnit.md)! | `MeasureUnit`. |

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
| `cfpos` | [ConstrainedFieldPosition](../android/icu/text/ConstrainedFieldPosition.md)!:The object used for iteration state. This can provide constraints to iterate over only one specific field; see [ConstrainedFieldPosition.constrainField](../android/icu/text/ConstrainedFieldPosition.md)). |

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
| [BigDecimal](../java/math/BigDecimal.md)! | A BigDecimal representation of the formatted number. |

**See Also**

- [android.icu.number.NumberFormatter](../android/icu/number/NumberFormatter.md) 

### toCharacterIterator

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toCharacterIterator(): AttributedCharacterIterator!
```

Exports the formatted number as an AttributedCharacterIterator.

Consider using [nextPosition](../android/icu/text/FormattedValue.md))if you are trying to get field information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | An AttributedCharacterIterator containing full field information. |

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
