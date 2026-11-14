# DateFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateFormat

Kotlin| [Java](DateFormat.md) 
| --- | --- |

```
open class DateFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.format.DateFormat](DateFormat.md) |

Utility class for producing strings with formatted date/time.

Most callers should avoid supplying their own format strings to this class'`format`methods and rely on the correctly localized ones supplied by the system. This class' factory methods return appropriately-localized [java.text.DateFormat](../java.text/DateFormat.md) instances, suitable for both formatting and parsing dates. For the canonical documentation of format strings, see [java.text.SimpleDateFormat](../java.text/SimpleDateFormat.md).

In cases where the system does not provide a suitable pattern, this class offers the [getBestDateTimePattern](DateFormat.md))method.

The`format`methods in this class implement a subset of Unicode [UTS #35](http://www.unicode.org/reports/tr35/#Date_Format_Patterns) patterns. The subset currently supported by this class includes the following format characters:`acdEHhLKkLMmsyz`. Up to API level 17, only`adEhkMmszy`were supported. Note that this class incorrectly implements`k`as if it were`H`for backwards compatibility.

See [java.text.SimpleDateFormat](../java.text/SimpleDateFormat.md) for more documentation about patterns, or if you need a more complete or correct implementation. Note that the non-`format`methods in this class are implemented by`SimpleDateFormat`.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [DateFormat](DateFormat.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [format](DateFormat.md))`(`inFormat:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `inDate:` ` [Calendar](../java.util/Calendar.md)!`)` Given a format string and a [java.util.Calendar](../java.util/Calendar.md) object, returns a CharSequence containing the requested date. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [format](DateFormat.md))`(`inFormat:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `inDate:` ` [Date](../java.util/Date.md)!`)` Given a format string and a [java.util.Date](../java.util/Date.md) object, returns a CharSequence containing the requested date. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [format](DateFormat.md))`(`inFormat:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `inTimeInMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Given a format string and a time in milliseconds since Jan 1, 1970 GMT, returns a CharSequence containing the requested date. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBestDateTimePattern](DateFormat.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`, `skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the best possible localized form of the given skeleton for the given locale. |
| openstatic [DateFormat](../java.text/DateFormat.md)! | [getDateFormat](DateFormat.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns a [java.text.DateFormat](../java.text/DateFormat.md) object that can format the date in short form according to the context's locale. |
| openstatic [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getDateFormatOrder](DateFormat.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Gets the current date format stored as a char array. |
| --- | --- |
| openstatic [DateFormat](../java.text/DateFormat.md)! | [getLongDateFormat](DateFormat.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns a [java.text.DateFormat](../java.text/DateFormat.md) object that can format the date in long form (such as`Monday, January 3, 2000`) for the context's locale. |
| openstatic [DateFormat](../java.text/DateFormat.md)! | [getMediumDateFormat](DateFormat.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns a [java.text.DateFormat](../java.text/DateFormat.md) object that can format the date in medium form (such as`Jan 3, 2000`) for the context's locale. |
| openstatic [DateFormat](../java.text/DateFormat.md)! | [getTimeFormat](DateFormat.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns a [java.text.DateFormat](../java.text/DateFormat.md) object that can format the time according to the context's locale and the user's 12-/24-hour clock preference. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [is24HourFormat](DateFormat.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns true if times should be formatted as 24 hour times, false if times should be formatted as 12 hour (AM/PM) times. |

## Public constructors

### DateFormat

```
DateFormat()
```

## Public methods

### format

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun format(
    inFormat: CharSequence!, 
    inDate: Calendar!
): CharSequence!
```

Given a format string and a [java.util.Calendar](../java.util/Calendar.md) object, returns a CharSequence containing the requested date.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inFormat` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the format string, as described in [android.text.format.DateFormat](DateFormat.md) |
| `inDate` | [Calendar](../java.util/Calendar.md)!:the date to format |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a [CharSequence](../java.lang/CharSequence.md) containing the requested text |

### format

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun format(
    inFormat: CharSequence!, 
    inDate: Date!
): CharSequence!
```

Given a format string and a [java.util.Date](../java.util/Date.md) object, returns a CharSequence containing the requested date.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inFormat` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the format string, as described in [android.text.format.DateFormat](DateFormat.md) |
| `inDate` | [Date](../java.util/Date.md)!:the date to format |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a [CharSequence](../java.lang/CharSequence.md) containing the requested text |

### format

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun format(
    inFormat: CharSequence!, 
    inTimeInMillis: Long
): CharSequence!
```

Given a format string and a time in milliseconds since Jan 1, 1970 GMT, returns a CharSequence containing the requested date.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inFormat` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the format string, as described in [android.text.format.DateFormat](DateFormat.md) |
| `inTimeInMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):in milliseconds since Jan 1, 1970 GMT |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a [CharSequence](../java.lang/CharSequence.md) containing the requested text |

### getBestDateTimePattern

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getBestDateTimePattern(
    locale: Locale!, 
    skeleton: String!
): String!
```

Returns the best possible localized form of the given skeleton for the given locale. A skeleton is similar to, and uses the same format characters as, a Unicode [UTS #35](http://www.unicode.org/reports/tr35/#Date_Format_Patterns) pattern.

One difference is that order is irrelevant. For example, "MMMMd" will return "MMMM d" in the`en_US`locale, but "d. MMMM" in the`de_CH`locale.

Note also in that second example that the necessary punctuation for German was added. For the same input in`es_ES`, we'd have even more extra text: "d 'de' MMMM".

This method will automatically correct for grammatical necessity. Given the same "MMMMd" input, this method will return "d LLLL" in the`fa_IR`locale, where stand-alone months are necessary. Lengths are preserved where meaningful, so "Md" would give a different result to "MMMd", say, except in a locale such as`ja_JP`where there is only one length of month.

This method will only return patterns that are in CLDR, and is useful whenever you know what elements you want in your format string but don't want to make your code specific to any one locale.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the locale into which the skeleton should be localized |
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a skeleton as described above |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string pattern suitable for use with [java.text.SimpleDateFormat](../java.text/SimpleDateFormat.md). |

### getDateFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDateFormat(context: Context!): DateFormat!
```

Returns a [java.text.DateFormat](../java.text/DateFormat.md) object that can format the date in short form according to the context's locale.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the application context |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [DateFormat](../java.text/DateFormat.md)! | the [java.text.DateFormat](../java.text/DateFormat.md) object that properly formats the date. |

### getDateFormatOrder

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDateFormatOrder(context: Context!): CharArray!
```

Gets the current date format stored as a char array. Returns a 3 element array containing the day (`'d'`), month (`'M'`), and year (`'y'`)) in the order specified by the user's format preference. Note that this order is*only*appropriate for all-numeric dates; spelled-out (MEDIUM and LONG) dates will generally contain other punctuation, spaces, or words, not just the day, month, and year, and not necessarily in the same order returned here. 

### getLongDateFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLongDateFormat(context: Context!): DateFormat!
```

Returns a [java.text.DateFormat](../java.text/DateFormat.md) object that can format the date in long form (such as`Monday, January 3, 2000`) for the context's locale.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the application context |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [DateFormat](../java.text/DateFormat.md)! | the [java.text.DateFormat](../java.text/DateFormat.md) object that formats the date in long form. |

### getMediumDateFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMediumDateFormat(context: Context!): DateFormat!
```

Returns a [java.text.DateFormat](../java.text/DateFormat.md) object that can format the date in medium form (such as`Jan 3, 2000`) for the context's locale.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the application context |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [DateFormat](../java.text/DateFormat.md)! | the [java.text.DateFormat](../java.text/DateFormat.md) object that formats the date in long form. |

### getTimeFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTimeFormat(context: Context!): DateFormat!
```

Returns a [java.text.DateFormat](../java.text/DateFormat.md) object that can format the time according to the context's locale and the user's 12-/24-hour clock preference.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the application context |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [DateFormat](../java.text/DateFormat.md)! | the [java.text.DateFormat](../java.text/DateFormat.md) object that properly formats the time. |

### is24HourFormat

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun is24HourFormat(context: Context!): Boolean
```

Returns true if times should be formatted as 24 hour times, false if times should be formatted as 12 hour (AM/PM) times. Based on the user's chosen locale and other preferences.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the context to use for the content resolver |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if 24 hour time format is selected, false otherwise. |
