# Format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Format

```
abstract class Format : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format#) |

| Known Direct Subclasses [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat), [MessageFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat), [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat), [SelectFormat](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat.html#), [UFormat](https://developer.android.com/reference/kotlin/android/icu/text/UFormat.html#) |----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | `DateFormat`is an abstract class for date/time formatting subclasses which formats and parses dates or time in a language-independent manner. | | [MessageFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat) | provides a means to produce concatenated messages in a language-neutral way. | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | `NumberFormat`is the abstract base class for all number formats. | | [SelectFormat](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat.html#) | `SelectFormat`supports the creation of internationalized messages by selecting phrases based on keywords. | | [UFormat](https://developer.android.com/reference/kotlin/android/icu/text/UFormat.html#) | An abstract class that extends [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format#) to provide additional ICU protocol, specifically, the getLocale() API. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat), [CompactDecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/CompactDecimalFormat.html#), [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#), [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.html#), [DecimalFormat](https://developer.android.com/reference/kotlin/java/text/DecimalFormat), [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat.html#), [MeasureFormat](https://developer.android.com/reference/kotlin/android/icu/text/MeasureFormat.html#), [MessageFormat](https://developer.android.com/reference/kotlin/android/icu/text/MessageFormat.html#), [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat.html#), [PluralFormat](https://developer.android.com/reference/kotlin/android/icu/text/PluralFormat.html#), [SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat), [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat.html#), and 1 others. |--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------| | [ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat) | A`ChoiceFormat`allows you to attach a format to a range of numbers. | | [CompactDecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/CompactDecimalFormat.html#) | Formats numbers in compact (abbreviated) notation, like "1. | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat). | | [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.html#) | DateIntervalFormat is a class for formatting and parsing date intervals in a language-independent manner. | | [DecimalFormat](https://developer.android.com/reference/kotlin/java/text/DecimalFormat) | is a concrete subclass of`NumberFormat`that formats decimal numbers. | | [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat.html#) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormat](https://developer.android.com/reference/kotlin/java/text/DecimalFormat). | | [MeasureFormat](https://developer.android.com/reference/kotlin/android/icu/text/MeasureFormat.html#) | A formatter for Measure objects. | | [MessageFormat](https://developer.android.com/reference/kotlin/android/icu/text/MessageFormat.html#) | **\[icu enhancement\]** ICU's replacement for [java.text.MessageFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat). | | [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat.html#) | **\[icu enhancement\]** ICU's replacement for [java.text.NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat). | | [PluralFormat](https://developer.android.com/reference/kotlin/android/icu/text/PluralFormat.html#) | `PluralFormat`supports the creation of internationalized messages with plural inflection. | | [SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat) | is a concrete class for formatting and parsing dates in a locale-sensitive manner. | | [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat.html#) | **\[icu enhancement\]** ICU's replacement for [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat). | | [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.html#) | `TimeZoneFormat`supports time zone display name formatting and parsing. | |
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

And finally subclasses may define a set of constants to identify the various fields in the formatted output. These constants are used to create a FieldPosition object which identifies what information is contained in the field and its position in the formatted result. These constants should be named*item*`_FIELD`where*item*identifies the field. For examples of these constants, see`ERA_FIELD`and its friends in [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat).

### Synchronization

Formats are generally not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Field](https://developer.android.com/reference/kotlin/java/text/Format.Field) Defines constants that are used as attribute keys in the`AttributedCharacterIterator`returned from`Format.formatToCharacterIterator`and as field identifiers in`FieldPosition`. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------|---|
| [Format](https://developer.android.com/reference/kotlin/java/text/Format#Format())`()` Sole constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/Format#clone())`()` Creates and returns a copy of this object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an object to produce a string. |
| abstract [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)!`)` Formats an object and appends the resulting text to a given string buffer. |
| --- | --- |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [formatToCharacterIterator](https://developer.android.com/reference/kotlin/java/text/Format#formatToCharacterIterator(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an Object producing an`AttributedCharacterIterator`. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/java/text/Format#parseObject(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses text from the beginning of the given string to produce an object. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/java/text/Format#parseObject(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)!`)` Parses text from a string to produce an object. |
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

Formats an object to produce a string. This is equivalent to [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(obj, new StringBuffer(), new FieldPosition(0)).toString();`

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
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!:where the text is to be appended |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)!:A`FieldPosition`identifying a field in the formatted text |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | the string buffer passed in as`toAppendTo`, with formatted text appended |

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
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | AttributedCharacterIterator describing the formatted value. |

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
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)!:A`ParsePosition`object with index and error index information as described above. |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | An`Object`parsed from the string. In case of error, returns null. |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if`source`or`pos`is null. |
