# FormattedNumberRange

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormattedNumberRange

Kotlin| [Java](FormattedNumberRange.md) 
| --- | --- |

```
open class FormattedNumberRange : FormattedValue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.FormattedNumberRange](FormattedNumberRange.md) |

The result of a number range formatting operation. This class allows the result to be exported in several data types, including a String, an AttributedCharacterIterator, and a BigDecimal. Instances of this class are immutable and thread-safe.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openA | [appendTo](FormattedNumberRange.md))`(`appendable:` `A`)` Appends the formatted string to an Appendable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](FormattedNumberRange.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](FormattedNumberRange.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the`char`value at the specified index. |
| --- | --- |
| open [BigDecimal](../java.math/BigDecimal.md)! | [getFirstBigDecimal](FormattedNumberRange.md))`()` Export the first formatted number as a BigDecimal. |
| open [NumberRangeFormatter.RangeIdentityResult](../android/icu/number/NumberRangeFormatter.RangeIdentityResult.md)! | [getIdentityResult](FormattedNumberRange.md))`()` Returns whether the pair of numbers was successfully formatted as a range or whether an identity fallback was used. |
| open [BigDecimal](../java.math/BigDecimal.md)! | [getSecondBigDecimal](FormattedNumberRange.md))`()` Export the second formatted number as a BigDecimal. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](FormattedNumberRange.md))`()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextPosition](FormattedNumberRange.md))`(`cfpos:` ` [ConstrainedFieldPosition](../android.icu.text/ConstrainedFieldPosition.md)!`)` Iterates over field positions in the FormattedValue. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [subSequence](FormattedNumberRange.md))`(`startIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`CharSequence`that is a subsequence of this sequence. |
| --- | --- |
| open [AttributedCharacterIterator](../java.text/AttributedCharacterIterator.md)! | [toCharacterIterator](FormattedNumberRange.md))`()` Exports the formatted number as an AttributedCharacterIterator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](FormattedNumberRange.md))`()` Returns a string representation of the object. |

| Properties ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](FormattedNumberRange.md) Returns the length of this character sequence. |

## Public methods

### appendTo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <A : Appendable!> appendTo(appendable: A): A
```

Appends the formatted string to an Appendable.

If an IOException occurs when appending to the Appendable, an unchecked [ICUUncheckedIOException](../android.icu.util/ICUUncheckedIOException.md) is thrown instead.

| Parameters ||
|--------------|--------------------------------------------------------|
| `appendable` | A:The Appendable to which to append the string output. |

| Return ||
|---|------------------------------------|
| A | The same Appendable, for chaining. |

| Exceptions ||
|--------------------------------------------|--------------------------------------|
| `android.icu.util.ICUUncheckedIOException` | if the Appendable throws IOException |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
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

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

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

### getFirstBigDecimal

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFirstBigDecimal(): BigDecimal!
```

Export the first formatted number as a BigDecimal. This endpoint is useful for obtaining the exact number being printed after scaling and rounding have been applied by the number range formatting pipeline.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [BigDecimal](../java.math/BigDecimal.md)! | A BigDecimal representation of the first formatted number. |

**See Also**

- [android.icu.number.NumberRangeFormatter](NumberRangeFormatter.md)
- [#getSecondBigDecimal](FormattedNumberRange.md)) 

### getIdentityResult

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIdentityResult(): NumberRangeFormatter.RangeIdentityResult!
```

Returns whether the pair of numbers was successfully formatted as a range or whether an identity fallback was used. For example, if the first and second number were the same either before or after rounding occurred, an identity fallback was used.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [NumberRangeFormatter.RangeIdentityResult](../android/icu/number/NumberRangeFormatter.RangeIdentityResult.md)! | A RangeIdentityType indicating the resulting identity situation in the formatted number range. |

**See Also**

- [android.icu.number.NumberRangeFormatter](NumberRangeFormatter.md)
- [android.icu.number.NumberRangeFormatter.RangeIdentityFallback](../android/icu/number/NumberRangeFormatter.RangeIdentityFallback.md) 

### getSecondBigDecimal

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSecondBigDecimal(): BigDecimal!
```

Export the second formatted number as a BigDecimal. This endpoint is useful for obtaining the exact number being printed after scaling and rounding have been applied by the number range formatting pipeline.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [BigDecimal](../java.math/BigDecimal.md)! | A BigDecimal representation of the second formatted number. |

**See Also**

- [android.icu.number.NumberRangeFormatter](NumberRangeFormatter.md)
- [#getFirstBigDecimal](FormattedNumberRange.md)) 

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java.util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java.lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java.lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

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
| `cfpos` | [ConstrainedFieldPosition](../android.icu.text/ConstrainedFieldPosition.md)!:The object used for iteration state. This can provide constraints to iterate over only one specific field; see [ConstrainedFieldPosition.constrainField](../android.icu.text/ConstrainedFieldPosition.md)). |

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

### toCharacterIterator

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toCharacterIterator(): AttributedCharacterIterator!
```

Exports the formatted number as an AttributedCharacterIterator.

Consider using [nextPosition](../android.icu.text/FormattedValue.md))if you are trying to get field information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [AttributedCharacterIterator](../java.text/AttributedCharacterIterator.md)! | An AttributedCharacterIterator containing full field information. |

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
