# Format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Format

```
abstract class Format : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.Format](../java/text/Format.md) |

| Known Direct Subclasses [DateFormat](../java/text/DateFormat.md), [MessageFormat](../java/text/MessageFormat.md), [NumberFormat](../java/text/NumberFormat.md), [SelectFormat](../android/icu/text/SelectFormat.md), [UFormat](../android/icu/text/UFormat.md) |----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DateFormat](../java/text/DateFormat.md) | `DateFormat`is an abstract class for date/time formatting subclasses which formats and parses dates or time in a language-independent manner. | | [MessageFormat](../java/text/MessageFormat.md) | provides a means to produce concatenated messages in a language-neutral way. | | [NumberFormat](../java/text/NumberFormat.md) | `NumberFormat`is the abstract base class for all number formats. | | [SelectFormat](../android/icu/text/SelectFormat.md) | `SelectFormat`supports the creation of internationalized messages by selecting phrases based on keywords. | | [UFormat](../android/icu/text/UFormat.md) | An abstract class that extends [java.text.Format](../java/text/Format.md) to provide additional ICU protocol, specifically, the getLocale() API. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ChoiceFormat](../java/text/ChoiceFormat.md), [CompactDecimalFormat](../android/icu/text/CompactDecimalFormat.md), [DateFormat](../android/icu/text/DateFormat.md), [DateIntervalFormat](../android/icu/text/DateIntervalFormat.md), [DecimalFormat](../java/text/DecimalFormat.md), [DecimalFormat](../android/icu/text/DecimalFormat.md), [MeasureFormat](../android/icu/text/MeasureFormat.md), [MessageFormat](../android/icu/text/MessageFormat.md), [NumberFormat](../android/icu/text/NumberFormat.md), [PluralFormat](../android/icu/text/PluralFormat.md), [SimpleDateFormat](../java/text/SimpleDateFormat.md), [SimpleDateFormat](../android/icu/text/SimpleDateFormat.md), and 1 others. |--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------| | [ChoiceFormat](../java/text/ChoiceFormat.md) | A`ChoiceFormat`allows you to attach a format to a range of numbers. | | [CompactDecimalFormat](../android/icu/text/CompactDecimalFormat.md) | Formats numbers in compact (abbreviated) notation, like "1. | | [DateFormat](../android/icu/text/DateFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormat](../java/text/DateFormat.md). | | [DateIntervalFormat](../android/icu/text/DateIntervalFormat.md) | DateIntervalFormat is a class for formatting and parsing date intervals in a language-independent manner. | | [DecimalFormat](../java/text/DecimalFormat.md) | is a concrete subclass of`NumberFormat`that formats decimal numbers. | | [DecimalFormat](../android/icu/text/DecimalFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormat](../java/text/DecimalFormat.md). | | [MeasureFormat](../android/icu/text/MeasureFormat.md) | A formatter for Measure objects. | | [MessageFormat](../android/icu/text/MessageFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.MessageFormat](../java/text/MessageFormat.md). | | [NumberFormat](../android/icu/text/NumberFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.NumberFormat](../java/text/NumberFormat.md). | | [PluralFormat](../android/icu/text/PluralFormat.md) | `PluralFormat`supports the creation of internationalized messages with plural inflection. | | [SimpleDateFormat](../java/text/SimpleDateFormat.md) | is a concrete class for formatting and parsing dates in a locale-sensitive manner. | | [SimpleDateFormat](../android/icu/text/SimpleDateFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.SimpleDateFormat](../java/text/SimpleDateFormat.md). | | [TimeZoneFormat](../android/icu/text/TimeZoneFormat.md) | `TimeZoneFormat`supports time zone display name formatting and parsing. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

`Format`is an abstract base class for formatting locale-sensitive information such as dates, messages, and numbers.

`Format`defines the programming interface for formatting locale-sensitive objects into`String`s (the`format`method) and for parsing`String`s back into objects (the`parseObject`method).

Generally, a format's`parseObject`method must be able to parse any string formatted by its`format`method. However, there may be exceptional cases where this is not possible. For example, a`format`method might create two adjacent integer numbers with no separator in between, and in this case the`parseObject`could not tell which digits belong to which number.

## Subclassing

The Java Platform provides three specialized subclasses of`Format`--`DateFormat`,`MessageFormat`, and`NumberFormat`--for formatting dates, messages, and numbers, respectively.

Concrete subclasses must implement three methods:

1. `format(Object obj, StringBuffer toAppendTo, FieldPosition pos)`
2. `formatToCharacterIterator(Object obj)`
3. `parseObject(String source, ParsePosition pos)`

These general methods allow polymorphic parsing and formatting of objects and are used, for example, by`MessageFormat`. Subclasses often also provide additional`format`methods for specific input types as well as`parse`methods for specific result types. Any`parse`method that does not take a`ParsePosition`argument should throw`ParseException`when no text in the required format is at the beginning of the input text.

Most subclasses will also implement the following factory methods:

1. `getInstance`for getting a useful format object appropriate for the current locale
2. `getInstance(Locale)`for getting a useful format object appropriate for the specified locale

In addition, some subclasses may also implement other`getXxxxInstance`methods for more specialized control. For example, the`NumberFormat`class provides`getPercentInstance`and`getCurrencyInstance`methods for getting specialized number formatters.

Subclasses of`Format`that allow programmers to create objects for locales (with`getInstance(Locale)`for example) must also implement the following class method: 

```kotlin
public static Locale[] getAvailableLocales()
  
```

And finally subclasses may define a set of constants to identify the various fields in the formatted output. These constants are used to create a FieldPosition object which identifies what information is contained in the field and its position in the formatted result. These constants should be named*item*`_FIELD`where*item*identifies the field. For examples of these constants, see`ERA_FIELD`and its friends in [DateFormat](../java/text/DateFormat.md).

### Synchronization

Formats are generally not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Field](../java/text/Format.Field.md) Defines constants that are used as attribute keys in the`AttributedCharacterIterator`returned from`Format.formatToCharacterIterator`and as field identifiers in`FieldPosition`. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------|---|
| [Format](../java/text/Format.md))`()` Sole constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/text/Format.md))`()` Creates and returns a copy of this object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../java/text/Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an object to produce a string. |
| abstract [StringBuffer](../java/lang/StringBuffer.md)! | [format](../java/text/Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` Formats an object and appends the resulting text to a given string buffer. |
| --- | --- |
| open [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | [formatToCharacterIterator](../java/text/Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an Object producing an`AttributedCharacterIterator`. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](../java/text/Format.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses text from the beginning of the given string to produce an object. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](../java/text/Format.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` Parses text from a string to produce an object. |
| --- | --- |

## Protected constructors

### Format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Format()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Creates and returns a copy of this object.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(obj: Any!): String!
```

Formats an object to produce a string. This is equivalent to [format](../java/text/Format.md))`(obj, new StringBuffer(), new FieldPosition(0)).toString();`

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object to format |

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Formatted string. |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | if the Format cannot format the given object |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    obj: Any!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats an object and appends the resulting text to a given string buffer. If the`pos`argument identifies a field used by the format, then its indices are set to the beginning and end of the first such field encountered.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object to format |
| `toAppendTo` | [StringBuffer](../java/lang/StringBuffer.md)!:where the text is to be appended |
| `pos` | [FieldPosition](../java/text/FieldPosition.md)!:A`FieldPosition`identifying a field in the formatted text |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](../java/lang/StringBuffer.md)! | the string buffer passed in as`toAppendTo`, with formatted text appended |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if the Format cannot format the given object |

### formatToCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatToCharacterIterator(obj: Any!): AttributedCharacterIterator!
```

Formats an Object producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String.

Each attribute key of the AttributedCharacterIterator will be of type`Field`. It is up to each`Format`implementation to define what the legal values are for each attribute in the`AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value.

The default implementation creates an`AttributedCharacterIterator`with no attributes. Subclasses that support fields should override this and create an`AttributedCharacterIterator`with meaningful attributes.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object to format |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | AttributedCharacterIterator describing the formatted value. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.NullPointerException` | if obj is null. |
| `java.lang.IllegalArgumentException` | when the Format cannot format the given object. |

### parseObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseObject(source: String!): Any!
```

Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A`String`whose beginning should be parsed. |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | An`Object`parsed from the string. |

| Exceptions ||
|----------------------------------|------------------------------------------------------------|
| `java.text.ParseException` | if the beginning of the specified string cannot be parsed. |
| `java.lang.NullPointerException` | if`source`is null. |

### parseObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parseObject(
    source: String!, 
    pos: ParsePosition!
): Any!
```

Parses text from a string to produce an object.

The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed object is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A`String`, part of which should be parsed. |
| `pos` | [ParsePosition](../java/text/ParsePosition.md)!:A`ParsePosition`object with index and error index information as described above. |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | An`Object`parsed from the string. In case of error, returns null. |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if`source`or`pos`is null. |
