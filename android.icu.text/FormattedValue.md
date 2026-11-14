# FormattedValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormattedValue

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/FormattedValue "View this page in Java") 

```
interface FormattedValue : CharSequence
```

| [android.icu.text.FormattedValue](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue#) |

| Known Direct Subclasses [DateIntervalFormat.FormattedDateInterval](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval), [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber.html#), [FormattedNumberRange](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumberRange.html#), [ListFormatter.FormattedList](https://developer.android.com/reference/kotlin/android/icu/text/ListFormatter.FormattedList), [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [DateIntervalFormat.FormattedDateInterval](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval) | An immutable class containing the result of a date interval formatting operation. | | [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber.html#) | The result of a number formatting operation. | | [FormattedNumberRange](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumberRange.html#) | The result of a number range formatting operation. | | [ListFormatter.FormattedList](https://developer.android.com/reference/kotlin/android/icu/text/ListFormatter.FormattedList) | An immutable class containing the result of a list formatting operation. | | [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime) | Represents the result of a formatting operation of a relative datetime. | |

An abstract formatted value: a string with associated field attributes. Many formatters format to classes implementing FormattedValue.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractA | [appendTo](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue#appendTo(android.icu.text.FormattedValue.appendTo.A))`(`appendable:` `A`)` Appends the formatted string to an Appendable. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextPosition](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue#nextPosition(android.icu.text.ConstrainedFieldPosition))`(`cfpos:` ` [ConstrainedFieldPosition](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition)!`)` Iterates over field positions in the FormattedValue. |
| abstract [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)! | [toCharacterIterator](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue#toCharacterIterator())`()` Exports the formatted number as an AttributedCharacterIterator. |

## Public methods

### appendTo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Appendable!> appendTo(appendable: A): A
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
| `cfpos` | [ConstrainedFieldPosition](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition)!:The object used for iteration state. This can provide constraints to iterate over only one specific field; see [ConstrainedFieldPosition.constrainField](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#constrainField(java.text.Format.Field)). |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a new occurrence of the field was found; false otherwise. |

### toCharacterIterator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toCharacterIterator(): AttributedCharacterIterator!
```

Exports the formatted number as an AttributedCharacterIterator.

Consider using [nextPosition](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue#nextPosition(android.icu.text.ConstrainedFieldPosition))if you are trying to get field information.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)! | An AttributedCharacterIterator containing full field information. |
