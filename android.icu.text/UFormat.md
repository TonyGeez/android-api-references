# UFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UFormat

Kotlin | [Java](UFormat.md) 
| --- | --- |

```
abstract class UFormat : Format
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.text.Format](../java.text/Format.md) ||
| | ↳ | [android.icu.text.UFormat](UFormat.md) |

| Known Direct Subclasses [DateFormat](DateFormat.md), [DateIntervalFormat](DateIntervalFormat.md), [MeasureFormat](MeasureFormat.md), [MessageFormat](MessageFormat.md), [NumberFormat](NumberFormat.md), [PluralFormat](PluralFormat.md), [TimeZoneFormat](TimeZoneFormat.md) |----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------| | [DateFormat](DateFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormat](../java.text/DateFormat.md). | | [DateIntervalFormat](DateIntervalFormat.md) | DateIntervalFormat is a class for formatting and parsing date intervals in a language-independent manner. | | [MeasureFormat](MeasureFormat.md) | A formatter for Measure objects. | | [MessageFormat](MessageFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.MessageFormat](../java.text/MessageFormat.md). | | [NumberFormat](NumberFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.NumberFormat](../java.text/NumberFormat.md). | | [PluralFormat](PluralFormat.md) | `PluralFormat` supports the creation of internationalized messages with plural inflection. | | [TimeZoneFormat](TimeZoneFormat.md) | `TimeZoneFormat` supports time zone display name formatting and parsing. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CompactDecimalFormat](CompactDecimalFormat.md), [DecimalFormat](DecimalFormat.md), [SimpleDateFormat](SimpleDateFormat.md) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CompactDecimalFormat](CompactDecimalFormat.md) | Formats numbers in compact (abbreviated) notation, like "1. | | [DecimalFormat](DecimalFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormat](../java.text/DecimalFormat.md). | | [SimpleDateFormat](SimpleDateFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.SimpleDateFormat](../java.text/SimpleDateFormat.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An abstract class that extends [java.text.Format](../java.text/Format.md) to provide additional ICU protocol, specifically, the getLocale() API. All ICU format classes are subclasses of this class.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------|---|
| [UFormat](UFormat.md))`()` Default constructor. |

| Inherited functions ||
|---|---|
| From class [Format](../java.text/Format.md) |----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java.text/Format.md))`()` Creates and returns a copy of this object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../java.text/Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an object to produce a string. This is equivalent to [format](../java.text/Format.md))`(obj, new StringBuffer(), new FieldPosition(0)).toString();` <br /> | | [StringBuffer](../java.lang/StringBuffer.md)! | [format](../java.text/Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](../java.lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java.text/FieldPosition.md)!`)` Formats an object and appends the resulting text to a given string buffer. If the `pos` argument identifies a field used by the format, then its indices are set to the beginning and end of the first such field encountered. <br /> | | [AttributedCharacterIterator](../java.text/AttributedCharacterIterator.md)! | [formatToCharacterIterator](../java.text/Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an Object producing an `AttributedCharacterIterator`. You can use the returned `AttributedCharacterIterator` to build the resulting String, as well as to determine information about the resulting String. Each attribute key of the AttributedCharacterIterator will be of type `Field`. It is up to each `Format` implementation to define what the legal values are for each attribute in the `AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value. The default implementation creates an `AttributedCharacterIterator` with no attributes. Subclasses that support fields should override this and create an `AttributedCharacterIterator` with meaningful attributes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](../java.text/Format.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](../java.text/Format.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](../java.text/ParsePosition.md)!`)` Parses text from a string to produce an object. The method attempts to parse text starting at the index given by `pos`. If parsing succeeds, then the index of `pos` is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed object is returned. The updated `pos` can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of `pos` is not changed, the error index of `pos` is set to the index of the character where the error occurred, and null is returned. <br /> | ||

## Public constructors

### UFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UFormat()
```

Default constructor.
