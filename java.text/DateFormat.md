# DateFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateFormat

```
abstract class DateFormat : Format
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.text.Format](Format.md) ||
| | ↳ | [java.text.DateFormat](DateFormat.md) |

| Known Direct Subclasses [SimpleDateFormat](SimpleDateFormat.md) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [SimpleDateFormat](SimpleDateFormat.md) | is a concrete class for formatting and parsing dates in a locale-sensitive manner. | |
| --- | --- | --- | --- | --- | --- | --- |

`DateFormat`is an abstract class for date/time formatting subclasses which formats and parses dates or time in a language-independent manner. The date/time formatting subclass, such as [SimpleDateFormat](SimpleDateFormat.md), allows for formatting (i.e., date → text), parsing (text → date), and normalization. The date is represented as a`Date`object or as the milliseconds since January 1, 1970, 00:00:00 GMT.

`DateFormat`provides many class methods for obtaining default date/time formatters based on the default or a given locale and a number of formatting styles. The formatting styles include [FULL](DateFormat.md), [LONG](DateFormat.md), [MEDIUM](DateFormat.md), and [SHORT](DateFormat.md). More detail and examples of using these styles are provided in the method descriptions.

`DateFormat`helps you to format and parse dates for any locale. Your code can be completely independent of the locale conventions for months, days of the week, or even the calendar format: lunar vs. solar.

To format a date for the current Locale, use one of the static factory methods: 

```kotlin
<code>myString = DateFormat.getDateInstance().format(myDate);
  </code>
```

If you are formatting multiple dates, it is more efficient to get the format and use it multiple times so that the system doesn't have to fetch the information about the local language and country conventions multiple times. 

```kotlin
<code>DateFormat df = DateFormat.getDateInstance();
  for (int i = 0; i &lt; myDate.length; ++i) {
      output.println(df.format(myDate[i]) + "; ");
  }
  </code>
```

To format a date for a different Locale, specify it in the call to [getDateInstance()](DateFormat.md)). 

```kotlin
<code>DateFormat df = DateFormat.getDateInstance(DateFormat.LONG, Locale.FRANCE);
  </code>
```

You can use a DateFormat to parse also. 

```kotlin
<code>myDate = df.parse(myString);
  </code>
```

Use`getDateInstance`to get the normal date format for that country. There are other static factory methods available. Use`getTimeInstance`to get the time format for that country. Use`getDateTimeInstance`to get a date and time format. You can pass in different options to these factory methods to control the length of the result; from [SHORT](DateFormat.md) to [MEDIUM](DateFormat.md) to [LONG](DateFormat.md) to [FULL](DateFormat.md). The exact result depends on the locale, but generally:

- [SHORT](DateFormat.md) is completely numeric, such as`12.13.52`or`3:30pm`
- [MEDIUM](DateFormat.md) is longer, such as`Jan 12, 1952`
- [LONG](DateFormat.md) is longer, such as`January 12, 1952`or`3:30:32pm`
- [FULL](DateFormat.md) is pretty completely specified, such as`Tuesday, April 12, 1952 AD or 3:30:42pm PST`.

You can also set the time zone on the format if you wish. If you want even more control over the format or parsing, (or want to give your users more control), you can try casting the`DateFormat`you get from the factory methods to a [SimpleDateFormat](SimpleDateFormat.md). This will work for the majority of countries; just remember to put it in a`try`block in case you encounter an unusual one.

You can also use forms of the parse and format methods with [ParsePosition](ParsePosition.md) and [FieldPosition](FieldPosition.md) to allow you to

- progressively parse through pieces of a string.
- align any particular field, or find out where it is for selection on the screen.

## Synchronization

Date formats are not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Field](../java/text/DateFormat.Field.md) Defines constants that are used as attribute keys in the`AttributedCharacterIterator`returned from`DateFormat.formatToCharacterIterator`and as field identifiers in`FieldPosition`. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AM_PM_FIELD](DateFormat.md) Useful constant for AM_PM field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATE_FIELD](DateFormat.md) Useful constant for DATE field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK_FIELD](DateFormat.md) Useful constant for DAY_OF_WEEK field alignment. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK_IN_MONTH_FIELD](DateFormat.md) Useful constant for DAY_OF_WEEK_IN_MONTH field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_YEAR_FIELD](DateFormat.md) Useful constant for DAY_OF_YEAR field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT](DateFormat.md) Constant for default style pattern. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERA_FIELD](DateFormat.md) Useful constant for ERA field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FULL](DateFormat.md) Constant for full style pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR0_FIELD](DateFormat.md) Useful constant for zero-based HOUR field alignment. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR1_FIELD](DateFormat.md) Useful constant for one-based HOUR field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR_OF_DAY0_FIELD](DateFormat.md) Useful constant for zero-based HOUR_OF_DAY field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR_OF_DAY1_FIELD](DateFormat.md) Useful constant for one-based HOUR_OF_DAY field alignment. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG](DateFormat.md) Constant for long style pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIUM](DateFormat.md) Constant for medium style pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MILLISECOND_FIELD](DateFormat.md) Useful constant for MILLISECOND field alignment. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINUTE_FIELD](DateFormat.md) Useful constant for MINUTE field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONTH_FIELD](DateFormat.md) Useful constant for MONTH field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECOND_FIELD](DateFormat.md) Useful constant for SECOND field alignment. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT](DateFormat.md) Constant for short style pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_FIELD](DateFormat.md) Useful constant for TIMEZONE field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_MONTH_FIELD](DateFormat.md) Useful constant for WEEK_OF_MONTH field alignment. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_YEAR_FIELD](DateFormat.md) Useful constant for WEEK_OF_YEAR field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YEAR_FIELD](DateFormat.md) Useful constant for YEAR field alignment. |

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------|---|
| [DateFormat](DateFormat.md))`()` Create a new date format. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](DateFormat.md))`()` Overrides Cloneable |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](DateFormat.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Overrides equals |
| [StringBuffer](../java.lang/StringBuffer.md) | [format](DateFormat.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `toAppendTo:` ` [StringBuffer](../java.lang/StringBuffer.md)`, `fieldPosition:` ` [FieldPosition](FieldPosition.md)`)` Formats the given`Object`into a date-time string. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [format](DateFormat.md))`(`date:` ` [Date](../java.util/Date.md)`)` Formats a [Date](../java.util/Date.md) into a date-time string. |
| abstract [StringBuffer](../java.lang/StringBuffer.md) | [format](DateFormat.md))`(`date:` ` [Date](../java.util/Date.md)`, `toAppendTo:` ` [StringBuffer](../java.lang/StringBuffer.md)`, `fieldPosition:` ` [FieldPosition](FieldPosition.md)`)` Formats a [Date](../java.util/Date.md) into a date-time string. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java.util/Locale.md)!\> | [getAvailableLocales](DateFormat.md))`()` Returns an array of all locales for which the`get*Instance`methods of this class can return localized instances. |
| --- | --- |
| open [Calendar](../java.util/Calendar.md) | [getCalendar](DateFormat.md))`()` Gets the calendar associated with this date/time formatter. |
| static [DateFormat](DateFormat.md) | [getDateInstance](DateFormat.md))`()` Gets the date formatter with the default formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| static [DateFormat](DateFormat.md) | [getDateInstance](DateFormat.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the date formatter with the given formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| --- | --- |
| static [DateFormat](DateFormat.md) | [getDateInstance](DateFormat.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](../java.util/Locale.md)`)` Gets the date formatter with the given formatting style for the given locale. |
| static [DateFormat](DateFormat.md) | [getDateTimeInstance](DateFormat.md))`()` Gets the date/time formatter with the default formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| static [DateFormat](DateFormat.md) | [getDateTimeInstance](DateFormat.md))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the date/time formatter with the given date and time formatting styles for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| --- | --- |
| static [DateFormat](DateFormat.md) | [getDateTimeInstance](DateFormat.md))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](../java.util/Locale.md)`)` Gets the date/time formatter with the given formatting styles for the given locale. |
| static [DateFormat](DateFormat.md) | [getInstance](DateFormat.md))`()` Get a default date/time formatter that uses the SHORT style for both the date and the time. |
| open [NumberFormat](NumberFormat.md) | [getNumberFormat](DateFormat.md))`()` Gets the number formatter which this date/time formatter uses to format and parse a time. |
| --- | --- |
| static [DateFormat](DateFormat.md) | [getTimeInstance](DateFormat.md))`()` Gets the time formatter with the default formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| static [DateFormat](DateFormat.md) | [getTimeInstance](DateFormat.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the time formatter with the given formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| static [DateFormat](DateFormat.md) | [getTimeInstance](DateFormat.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](../java.util/Locale.md)`)` Gets the time formatter with the given formatting style for the given locale. |
| --- | --- |
| open [TimeZone](../java.util/TimeZone.md) | [getTimeZone](DateFormat.md))`()` Gets the time zone. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](DateFormat.md))`()` Overrides hashCode |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLenient](DateFormat.md))`()` Tell whether date/time parsing is to be lenient. |
| --- | --- |
| open [Date](../java.util/Date.md)? | [parse](DateFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Parses text from the beginning of the given string to produce a date. |
| abstract [Date](../java.util/Date.md)? | [parse](DateFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [ParsePosition](ParsePosition.md)`)` Parse a date/time string according to the given parse position. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [parseObject](DateFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [ParsePosition](ParsePosition.md)`)` Parses text from a string to produce a`Date`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCalendar](DateFormat.md))`(`newCalendar:` ` [Calendar](../java.util/Calendar.md)`)` Set the calendar to be used by this date format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLenient](DateFormat.md))`(`lenient:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Specify whether or not date/time parsing is to be lenient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNumberFormat](DateFormat.md))`(`newNumberFormat:` ` [NumberFormat](NumberFormat.md)`)` Allows you to set the number formatter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeZone](DateFormat.md))`(`zone:` ` [TimeZone](../java.util/TimeZone.md)`)` Sets the time zone for the calendar of this`DateFormat`object. |

| Inherited functions ||
|---|---|
| From class [Format](Format.md) |----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an object to produce a string. This is equivalent to [format](Format.md))`(obj, new StringBuffer(), new FieldPosition(0)).toString();` <br /> | | [AttributedCharacterIterator](AttributedCharacterIterator.md)! | [formatToCharacterIterator](Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an Object producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String. Each attribute key of the AttributedCharacterIterator will be of type`Field`. It is up to each`Format`implementation to define what the legal values are for each attribute in the`AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value. The default implementation creates an`AttributedCharacterIterator`with no attributes. Subclasses that support fields should override this and create an`AttributedCharacterIterator`with meaningful attributes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](Format.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string. <br /> | ||

| Properties ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Calendar](../java.util/Calendar.md) | [calendar](DateFormat.md) The [Calendar](../java.util/Calendar.md) instance used for calculating the date-time fields and the instant of time. |
| [NumberFormat](NumberFormat.md) | [numberFormat](DateFormat.md) The number formatter that`DateFormat`uses to format numbers in dates and times. |

## Constants

### AM_PM_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AM_PM_FIELD: Int
```

Useful constant for AM_PM field alignment. Used in FieldPosition of date/time formatting. 

 Value: 14

### DATE_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATE_FIELD: Int
```

Useful constant for DATE field alignment. Used in FieldPosition of date/time formatting. 

 Value: 3

### DAY_OF_WEEK_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DAY_OF_WEEK_FIELD: Int
```

Useful constant for DAY_OF_WEEK field alignment. Used in FieldPosition of date/time formatting. 

 Value: 9

### DAY_OF_WEEK_IN_MONTH_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DAY_OF_WEEK_IN_MONTH_FIELD: Int
```

Useful constant for DAY_OF_WEEK_IN_MONTH field alignment. Used in FieldPosition of date/time formatting. 

 Value: 11

### DAY_OF_YEAR_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DAY_OF_YEAR_FIELD: Int
```

Useful constant for DAY_OF_YEAR field alignment. Used in FieldPosition of date/time formatting. 

 Value: 10

### DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: Int
```

Constant for default style pattern. Its value is MEDIUM. 

 Value: 2

### ERA_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERA_FIELD: Int
```

Useful constant for ERA field alignment. Used in FieldPosition of date/time formatting. 

 Value: 0

### FULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FULL: Int
```

Constant for full style pattern. 

 Value: 0

### HOUR0_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HOUR0_FIELD: Int
```

Useful constant for zero-based HOUR field alignment. Used in FieldPosition of date/time formatting. HOUR0_FIELD is used for the zero-based 12-hour clock. For example, 11:30 PM + 1 hour results in 00:30 AM. 

 Value: 16

### HOUR1_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HOUR1_FIELD: Int
```

Useful constant for one-based HOUR field alignment. Used in FieldPosition of date/time formatting. HOUR1_FIELD is used for the one-based 12-hour clock. For example, 11:30 PM + 1 hour results in 12:30 AM. 

 Value: 15

### HOUR_OF_DAY0_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HOUR_OF_DAY0_FIELD: Int
```

Useful constant for zero-based HOUR_OF_DAY field alignment. Used in FieldPosition of date/time formatting. HOUR_OF_DAY0_FIELD is used for the zero-based 24-hour clock. For example, 23:59 + 01:00 results in 00:59. 

 Value: 5

### HOUR_OF_DAY1_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HOUR_OF_DAY1_FIELD: Int
```

Useful constant for one-based HOUR_OF_DAY field alignment. Used in FieldPosition of date/time formatting. HOUR_OF_DAY1_FIELD is used for the one-based 24-hour clock. For example, 23:59 + 01:00 results in 24:59. 

 Value: 4

### LONG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LONG: Int
```

Constant for long style pattern. 

 Value: 1

### MEDIUM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIUM: Int
```

Constant for medium style pattern. 

 Value: 2

### MILLISECOND_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MILLISECOND_FIELD: Int
```

Useful constant for MILLISECOND field alignment. Used in FieldPosition of date/time formatting. 

 Value: 8

### MINUTE_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MINUTE_FIELD: Int
```

Useful constant for MINUTE field alignment. Used in FieldPosition of date/time formatting. 

 Value: 6

### MONTH_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MONTH_FIELD: Int
```

Useful constant for MONTH field alignment. Used in FieldPosition of date/time formatting. 

 Value: 2

### SECOND_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECOND_FIELD: Int
```

Useful constant for SECOND field alignment. Used in FieldPosition of date/time formatting. 

 Value: 7

### SHORT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHORT: Int
```

Constant for short style pattern. 

 Value: 3

### TIMEZONE_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMEZONE_FIELD: Int
```

Useful constant for TIMEZONE field alignment. Used in FieldPosition of date/time formatting. 

 Value: 17

### WEEK_OF_MONTH_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEEK_OF_MONTH_FIELD: Int
```

Useful constant for WEEK_OF_MONTH field alignment. Used in FieldPosition of date/time formatting. 

 Value: 13

### WEEK_OF_YEAR_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEEK_OF_YEAR_FIELD: Int
```

Useful constant for WEEK_OF_YEAR field alignment. Used in FieldPosition of date/time formatting. 

 Value: 12

### YEAR_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YEAR_FIELD: Int
```

Useful constant for YEAR field alignment. Used in FieldPosition of date/time formatting. 

 Value: 1

## Protected constructors

### DateFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected DateFormat()
```

Create a new date format.

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Overrides Cloneable

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Overrides equals

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    obj: Any, 
    toAppendTo: StringBuffer, 
    fieldPosition: FieldPosition
): StringBuffer
```

Formats the given`Object`into a date-time string. The formatted string is appended to the given`StringBuffer`.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):Must be a`Date`or a`Number`representing a millisecond offset from the [Epoch](../java.util/Calendar.md). |
| `toAppendTo` | [StringBuffer](../java.lang/StringBuffer.md):The string buffer for the returning date-time string. |
| `pos` | A`FieldPosition`identifying a field in the formatted text |
| --- | --- |
| `fieldPosition` | [FieldPosition](FieldPosition.md):keeps track on the position of the field within the returned string. For example, given a date-time text`"1996.07.10 AD at 15:08:56 PDT"`, if the given`fieldPosition`is [DateFormat.YEAR_FIELD](DateFormat.md), the begin index and end index of`fieldPosition`will be set to 0 and 4, respectively. Notice that if the same date-time field appears more than once in a pattern, the`fieldPosition`will be set for the first occurrence of that date-time field. For instance, formatting a`Date`to the date-time string`"1 PM PDT (Pacific Daylight Time)"`using the pattern`"h a z (zzzz)"`and the alignment field [DateFormat.TIMEZONE_FIELD](DateFormat.md), the begin index and end index of`fieldPosition`will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character`'z'`. |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [StringBuffer](../java.lang/StringBuffer.md) | the string buffer passed in as`toAppendTo`, with formatted text appended. |

| Exceptions ||
|--------------------------------------|---------------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if the`Format`cannot format the given`obj`. |

**See Also**

- [java.text.Format](Format.md) 

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(date: Date): String
```

Formats a [Date](../java.util/Date.md) into a date-time string.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `date` | [Date](../java.util/Date.md):the time value to be formatted into a date-time string. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the formatted date-time string. |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    date: Date, 
    toAppendTo: StringBuffer, 
    fieldPosition: FieldPosition
): StringBuffer
```

Formats a [Date](../java.util/Date.md) into a date-time string. The formatted string is appended to the given`StringBuffer`.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `date` | [Date](../java.util/Date.md):a Date to be formatted into a date-time string. |
| `toAppendTo` | [StringBuffer](../java.lang/StringBuffer.md):the string buffer for the returning date-time string. |
| `fieldPosition` | [FieldPosition](FieldPosition.md):keeps track on the position of the field within the returned string. For example, given a date-time text`"1996.07.10 AD at 15:08:56 PDT"`, if the given`fieldPosition`is [DateFormat.YEAR_FIELD](DateFormat.md), the begin index and end index of`fieldPosition`will be set to 0 and 4, respectively. Notice that if the same date-time field appears more than once in a pattern, the`fieldPosition`will be set for the first occurrence of that date-time field. For instance, formatting a`Date`to the date-time string`"1 PM PDT (Pacific Daylight Time)"`using the pattern`"h a z (zzzz)"`and the alignment field [DateFormat.TIMEZONE_FIELD](DateFormat.md), the begin index and end index of`fieldPosition`will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character`'z'`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [StringBuffer](../java.lang/StringBuffer.md) | the string buffer passed in as`toAppendTo`, with formatted text appended. |

### getAvailableLocales

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>
```

Returns an array of all locales for which the`get*Instance`methods of this class can return localized instances. It must contain at least a`Locale`instance equal to [Locale.US](../java.util/Locale.md).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java.util/Locale.md)!> | An array of locales for which localized`DateFormat`instances are available. |

### getCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCalendar(): Calendar
```

Gets the calendar associated with this date/time formatter.

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Calendar](../java.util/Calendar.md) | the calendar associated with this date/time formatter. |

### getDateInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDateInstance(): DateFormat
```

Gets the date formatter with the default formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale.

This is equivalent to calling [getDateInstance(DEFAULT,](DateFormat.md)).

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [DateFormat](DateFormat.md) | a date formatter. |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](../java.util/Locale.md))
- [java.util.Locale.Category#FORMAT](../java/util/Locale.Category.md) 

### getDateInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDateInstance(style: Int): DateFormat
```

Gets the date formatter with the given formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale.

This is equivalent to calling [getDateInstance(style,](DateFormat.md)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given formatting style. For example, SHORT for "M/d/yy" in the US locale. |

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [DateFormat](DateFormat.md) | a date formatter. |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](../java.util/Locale.md))
- [java.util.Locale.Category#FORMAT](../java/util/Locale.Category.md) 

### getDateInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDateInstance(
    style: Int, 
    aLocale: Locale
): DateFormat
```

Gets the date formatter with the given formatting style for the given locale.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given formatting style. For example, SHORT for "M/d/yy" in the US locale. |
| `aLocale` | [Locale](../java.util/Locale.md):the given locale. |

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [DateFormat](DateFormat.md) | a date formatter. |

### getDateTimeInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDateTimeInstance(): DateFormat
```

Gets the date/time formatter with the default formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale.

This is equivalent to calling [getDateTimeInstance(DEFAULT,](DateFormat.md)).

| Return ||
|------------------------------------------------------------------------------------|------------------------|
| [DateFormat](DateFormat.md) | a date/time formatter. |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](../java.util/Locale.md))
- [java.util.Locale.Category#FORMAT](../java/util/Locale.Category.md) 

### getDateTimeInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDateTimeInstance(
    dateStyle: Int, 
    timeStyle: Int
): DateFormat
```

Gets the date/time formatter with the given date and time formatting styles for the default [FORMAT](../java/util/Locale.Category.md) locale.

This is equivalent to calling [getDateTimeInstance(dateStyle,](DateFormat.md)).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given date formatting style. For example, SHORT for "M/d/yy" in the US locale. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given time formatting style. For example, SHORT for "h:mm a" in the US locale. |

| Return ||
|------------------------------------------------------------------------------------|------------------------|
| [DateFormat](DateFormat.md) | a date/time formatter. |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](../java.util/Locale.md))
- [java.util.Locale.Category#FORMAT](../java/util/Locale.Category.md) 

### getDateTimeInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDateTimeInstance(
    dateStyle: Int, 
    timeStyle: Int, 
    aLocale: Locale
): DateFormat
```

Gets the date/time formatter with the given formatting styles for the given locale.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------|
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given date formatting style. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given time formatting style. |
| `aLocale` | [Locale](../java.util/Locale.md):the given locale. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------|
| [DateFormat](DateFormat.md) | a date/time formatter. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): DateFormat
```

Get a default date/time formatter that uses the SHORT style for both the date and the time.

| Return ||
|------------------------------------------------------------------------------------|-----------------------|
| [DateFormat](DateFormat.md) | a date/time formatter |

### getNumberFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumberFormat(): NumberFormat
```

Gets the number formatter which this date/time formatter uses to format and parse a time.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [NumberFormat](NumberFormat.md) | the number formatter which this date/time formatter uses. |

### getTimeInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getTimeInstance(): DateFormat
```

Gets the time formatter with the default formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale.

This is equivalent to calling [getTimeInstance(DEFAULT,](DateFormat.md)).

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [DateFormat](DateFormat.md) | a time formatter. |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](../java.util/Locale.md))
- [java.util.Locale.Category#FORMAT](../java/util/Locale.Category.md) 

### getTimeInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getTimeInstance(style: Int): DateFormat
```

Gets the time formatter with the given formatting style for the default [FORMAT](../java/util/Locale.Category.md) locale.

This is equivalent to calling [getTimeInstance(style,](DateFormat.md)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given formatting style. For example, SHORT for "h:mm a" in the US locale. |

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [DateFormat](DateFormat.md) | a time formatter. |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](../java.util/Locale.md))
- [java.util.Locale.Category#FORMAT](../java/util/Locale.Category.md) 

### getTimeInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getTimeInstance(
    style: Int, 
    aLocale: Locale
): DateFormat
```

Gets the time formatter with the given formatting style for the given locale.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given formatting style. For example, SHORT for "h:mm a" in the US locale. |
| `aLocale` | [Locale](../java.util/Locale.md):the given locale. |

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [DateFormat](DateFormat.md) | a time formatter. |

### getTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimeZone(): TimeZone
```

Gets the time zone. This method is equivalent to the following call. 

```kotlin
<code>getCalendar().getTimeZone()
  </code>
```

<br />

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [TimeZone](../java.util/TimeZone.md) | the time zone associated with the calendar of DateFormat. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Overrides hashCode

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isLenient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLenient(): Boolean
```

Tell whether date/time parsing is to be lenient. This method is equivalent to the following call. 

```kotlin
<code>getCalendar().isLenient()
  </code>
```

<br />

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the [calendar](DateFormat.md) is lenient;`false`otherwise. |

**See Also**

- [java.util.Calendar#isLenient()](../java.util/Calendar.md)) 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(source: String): Date?
```

Parses text from the beginning of the given string to produce a date. The method may not use the entire text of the given string.

See the [parse(java.lang.String,java.text.ParsePosition)](DateFormat.md))method for more information on date parsing.

**WARNING:** Don't use this method to deserialize a date. The underlying localized date/time format and parsing behaviors can change across Android versions as common usage in the locale changes. Consider using`long`type for storing a timestamp or [java.time.format.DateTimeFormatter#ISO_INSTANT](../java.time.format/DateTimeFormatter.md) for deserializing the ISO-8601 instant format.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A`String`whose beginning should be parsed. |

| Return ||
|------------------------------------------------------------------------------|--------------------------------|
| [Date](../java.util/Date.md)? | A`Date`parsed from the string. |

| Exceptions ||
|----------------------------|------------------------------------------------------------|
| `java.text.ParseException` | if the beginning of the specified string cannot be parsed. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(
    source: String, 
    pos: ParsePosition
): Date?
```

Parse a date/time string according to the given parse position. For example, a time text`"07/10/96 4:5 PM, PDT"`will be parsed into a`Date`that is equivalent to`Date(837039900000L)`.

By default, parsing is lenient: If the input is not in the form used by this object's format method but can still be parsed as a date, then the parse succeeds. Clients may insist on strict adherence to the format by calling [setLenient(false)](DateFormat.md)).

**WARNING:** Don't use this method to deserialize a date. The underlying localized date/time format and parsing behaviors can change across Android versions as common usage in the locale changes. Consider using`long`type for storing a timestamp or [java.time.format.DateTimeFormatter#ISO_INSTANT](../java.time.format/DateTimeFormatter.md) for deserializing the ISO-8601 instant format.

This parsing operation uses the [calendar](DateFormat.md) to produce a`Date`. As a result, the`calendar`'s date-time fields and the`TimeZone`value may have been overwritten, depending on subclass implementations. Any`TimeZone`value that has previously been set by a call to [setTimeZone](DateFormat.md))may need to be restored for further operations.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The date/time string to be parsed |
| `pos` | [ParsePosition](ParsePosition.md):On input, the position at which to start parsing; on output, the position at which parsing terminated, or the start position if the parse failed. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------|
| [Date](../java.util/Date.md)? | A`Date`, or`null`if the input could not be parsed |

### parseObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseObject(
    source: String, 
    pos: ParsePosition
): Any?
```

Parses text from a string to produce a`Date`.

The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed date is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned.

See the [parse(java.lang.String,java.text.ParsePosition)](DateFormat.md))method for more information on date parsing.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A`String`, part of which should be parsed. |
| `pos` | [ParsePosition](ParsePosition.md):A`ParsePosition`object with index and error index information as described above. |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | A`Date`parsed from the string. In case of error, returns null. |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if`source`or`pos`is null. |

### setCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCalendar(newCalendar: Calendar): Unit
```

Set the calendar to be used by this date format. Initially, the default calendar for the specified or default locale is used.

Any [TimeZone](../java.util/TimeZone.md) and [leniency](DateFormat.md))values that have previously been set are overwritten by`newCalendar`'s values.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------|
| `newCalendar` | [Calendar](../java.util/Calendar.md):the new`Calendar`to be used by the date format |

### setLenient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLenient(lenient: Boolean): Unit
```

Specify whether or not date/time parsing is to be lenient. With lenient parsing, the parser may use heuristics to interpret inputs that do not precisely match this object's format. With strict parsing, inputs must match this object's format.

This method is equivalent to the following call. 

```kotlin
<code>getCalendar().setLenient(lenient)
  </code>
```

This leniency value is overwritten by a call to [setCalendar()](DateFormat.md)).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `lenient` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):when`true`, parsing is lenient |

**See Also**

- [java.util.Calendar#setLenient(boolean)](../java.util/Calendar.md)) 

### setNumberFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNumberFormat(newNumberFormat: NumberFormat): Unit
```

Allows you to set the number formatter.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| `newNumberFormat` | [NumberFormat](NumberFormat.md):the given new NumberFormat. |

### setTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTimeZone(zone: TimeZone): Unit
```

Sets the time zone for the calendar of this`DateFormat`object. This method is equivalent to the following call. 

```kotlin
<code>getCalendar().setTimeZone(zone)
  </code>
```

<br />

The`TimeZone`set by this method is overwritten by a [setCalendar](DateFormat.md))call.

The`TimeZone`set by this method may be overwritten as a result of a call to the parse method.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `zone` | [TimeZone](../java.util/TimeZone.md):the given new time zone. |

## Properties

### calendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var calendar: Calendar
```

The [Calendar](../java.util/Calendar.md) instance used for calculating the date-time fields and the instant of time. This field is used for both formatting and parsing.

Subclasses should initialize this field to a [Calendar](../java.util/Calendar.md) appropriate for the [Locale](../java.util/Locale.md) associated with this`DateFormat`. 

### numberFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var numberFormat: NumberFormat
```

The number formatter that`DateFormat`uses to format numbers in dates and times. Subclasses should initialize this to a number format appropriate for the locale associated with this`DateFormat`.
