# FormattedValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormattedValue

Kotlin| [Java](../android/icu/text/FormattedValue.md) 
| --- | --- |

```
interface FormattedValue : CharSequence
```

| [android.icu.text.FormattedValue](../android/icu/text/FormattedValue.md) |

| Known Direct Subclasses [DateIntervalFormat.FormattedDateInterval](../android/icu/text/DateIntervalFormat.FormattedDateInterval.md), [FormattedNumber](../android/icu/number/FormattedNumber.md), [FormattedNumberRange](../android/icu/number/FormattedNumberRange.md), [ListFormatter.FormattedList](../android/icu/text/ListFormatter.FormattedList.md), [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [DateIntervalFormat.FormattedDateInterval](../android/icu/text/DateIntervalFormat.FormattedDateInterval.md) | An immutable class containing the result of a date interval formatting operation. | | [FormattedNumber](../android/icu/number/FormattedNumber.md) | The result of a number formatting operation. | | [FormattedNumberRange](../android/icu/number/FormattedNumberRange.md) | The result of a number range formatting operation. | | [ListFormatter.FormattedList](../android/icu/text/ListFormatter.FormattedList.md) | An immutable class containing the result of a list formatting operation. | | [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md) | Represents the result of a formatting operation of a relative datetime. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An abstract formatted value: a string with associated field attributes. Many formatters format to classes implementing FormattedValue.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractA | [appendTo](../android/icu/text/FormattedValue.md))`(`appendable:` `A`)` Appends the formatted string to an Appendable. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextPosition](../android/icu/text/FormattedValue.md))`(`cfpos:` ` [ConstrainedFieldPosition](../android/icu/text/ConstrainedFieldPosition.md)!`)` Iterates over field positions in the FormattedValue. |
| abstract [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | [toCharacterIterator](../android/icu/text/FormattedValue.md))`()` Exports the formatted number as an AttributedCharacterIterator. |
| --- | --- |

## Public methods

### appendTo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Appendable!> appendTo(appendable: A): A
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

### nextPosition

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextPosition(cfpos: ConstrainedFieldPosition!): Boolean
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
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cfpos` | [ConstrainedFieldPosition](../android/icu/text/ConstrainedFieldPosition.md)!:The object used for iteration state. This can provide constraints to iterate over only one specific field; see [ConstrainedFieldPosition.constrainField](../android/icu/text/ConstrainedFieldPosition.md)). |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a new occurrence of the field was found; false otherwise. |

### toCharacterIterator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toCharacterIterator(): AttributedCharacterIterator!
```

Exports the formatted number as an AttributedCharacterIterator.

Consider using [nextPosition](../android/icu/text/FormattedValue.md))if you are trying to get field information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | An AttributedCharacterIterator containing full field information. |
