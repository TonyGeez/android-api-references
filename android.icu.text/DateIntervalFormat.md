Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateIntervalFormat

```
open class DateIntervalFormat : UFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format.html#) |||
| | ↳ | [android.icu.text.UFormat](https://developer.android.com/reference/kotlin/android/icu/text/UFormat) ||
| | | ↳ | [android.icu.text.DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#) |

DateIntervalFormat is a class for formatting and parsing date intervals in a language-independent manner. Only formatting is supported. Parsing is not supported.

Date interval means from one date to another date, for example, from "Jan 11, 2008" to "Jan 18, 2008". We introduced class DateInterval to represent it. DateInterval is a pair of UDate, which is the standard milliseconds since 24:00 GMT, Jan 1, 1970.

DateIntervalFormat formats a DateInterval into text as compactly as possible. For example, the date interval format from "Jan 11, 2008" to "Jan 18,. 2008" is "Jan 11-18, 2008" for English. And it parses text into DateInterval, although initially, parsing is not supported.

There is no structural information in date time patterns. For any punctuations and string literals inside a date time pattern, we do not know whether it is just a separator, or a prefix, or a suffix. Without such information, so, it is difficult to generate a sub-pattern (or super-pattern) by algorithm. So, formatting a DateInterval is pattern-driven. It is very similar to formatting in SimpleDateFormat. We introduce class DateIntervalInfo to save date interval patterns, similar to date time pattern in SimpleDateFormat.

Logically, the interval patterns are mappings from (skeleton, the_largest_different_calendar_field) to (date_interval_pattern).

A skeleton

1. only keeps the field pattern letter and ignores all other parts in a pattern, such as space, punctuations, and string literals.
2. hides the order of fields.
3. might hide a field's pattern letter length. For those non-digit calendar fields, the pattern letter length is important, such as MMM, MMMM, and MMMMM; EEE and EEEE, and the field's pattern letter length is honored. For the digit calendar fields, such as M or MM, d or dd, yy or yyyy, the field pattern length is ignored and the best match, which is defined in date time patterns, will be returned without honor the field pattern letter length in skeleton.

The calendar fields we support for interval formatting are: year, month, date, day-of-week, am-pm, hour, hour-of-day, minute, and second (though we do not currently have specific intervalFormat data for skeletons with seconds). Those calendar fields can be defined in the following order: year \> month \> date \> hour (in day) \> minute \> second The largest different calendar fields between 2 calendars is the first different calendar field in above order. For example: the largest different calendar fields between "Jan 10, 2007" and "Feb 20, 2008" is year.

For other calendar fields, the compact interval formatting is not supported. And the interval format will be fall back to fall-back patterns, which is mostly "{date0} - {date1}".

There is a set of pre-defined static skeleton strings in DateFormat, There are pre-defined interval patterns for those pre-defined skeletons in locales' resource files. For example, for a skeleton YEAR_ABBR_MONTH_DAY, which is "yMMMd", in en_US, if the largest different calendar field between date1 and date2 is "year", the date interval pattern is "MMM d, yyyy - MMM d, yyyy", such as "Jan 10, 2007 - Jan 10, 2008". If the largest different calendar field between date1 and date2 is "month", the date interval pattern is "MMM d - MMM d, yyyy", such as "Jan 10 - Feb 10, 2007". If the largest different calendar field between date1 and date2 is "day", the date interval pattern is ""MMM d-d, yyyy", such as "Jan 10-20, 2007". For date skeleton, the interval patterns when year, or month, or date is different are defined in resource files. For time skeleton, the interval patterns when am/pm, or hour, or minute is different are defined in resource files.

If a skeleton is not found in a locale's DateIntervalInfo, which means the interval patterns for the skeleton is not defined in resource file, the interval pattern will falls back to the interval "fallback" pattern defined in resource file. If the interval "fallback" pattern is not defined, the default fall-back is "{date0} - {data1}".

For the combination of date and time, The rule to genearte interval patterns are:

1. when the year, month, or day differs, falls back to fall-back interval pattern, which mostly is the concatenate the two original expressions with a separator between, For example, interval pattern from "Jan 10, 2007 10:10 am" to "Jan 11, 2007 10:10am" is "Jan 10, 2007 10:10 am - Jan 11, 2007 10:10am"
2. otherwise, present the date followed by the range expression for the time. For example, interval pattern from "Jan 10, 2007 10:10 am" to "Jan 10, 2007 11:10am" is "Jan 10, 2007 10:10 am - 11:10am"

If two dates are the same, the interval pattern is the single date pattern. For example, interval pattern from "Jan 10, 2007" to "Jan 10, 2007" is "Jan 10, 2007". Or if the presenting fields between 2 dates have the exact same values, the interval pattern is the single date pattern. For example, if user only requests year and month, the interval pattern from "Jan 10, 2007" to "Jan 20, 2007" is "Jan 2007".

DateIntervalFormat needs the following information for correct formatting: time zone, calendar type, pattern, date format symbols, and date interval patterns. It can be instantiated in several ways:

1. create an instance using default or given locale plus given skeleton. Users are encouraged to created date interval formatter this way and to use the pre-defined skeleton macros, such as YEAR_NUM_MONTH, which consists the calendar fields and the format style.
2. create an instance using default or given locale plus given skeleton plus a given DateIntervalInfo. This factory method is for powerful users who want to provide their own interval patterns. Locale provides the timezone, calendar, and format symbols information. Local plus skeleton provides full pattern information. DateIntervalInfo provides the date interval patterns.

For the calendar field pattern letter, such as G, y, M, d, a, h, H, m, s etc. DateIntervalFormat uses the same syntax as that of DateTime format.

Code Sample: general usage

```kotlin
// the date interval object which the DateIntervalFormat formats on
    // and parses into
    DateInterval dtInterval = new DateInterval(1000*3600*24L, 1000*3600*24*2L);
    DateIntervalFormat dtIntervalFmt = DateIntervalFormat.getInstance(
            DateFormat.YEAR_MONTH_DAY, new Locale("en", "GB", ""));
    StringBuffer result = new StringBuffer("");
    FieldPosition pos = new FieldPosition(-1);
    // formatting
    dtIntervalFmt.format(dtInterval, result, pos);
    assertEquals("interval", "1--2 January 1970", result.toString());
 
  
```

Code Sample: for powerful users who wants to use their own interval pattern

```kotlin
import android.icu.text.DateIntervalInfo;
      import android.icu.text.DateIntervalFormat;
      ....................
 
      // Get DateIntervalFormat instance using default locale
      DateIntervalFormat dtitvfmt = DateIntervalFormat.getInstance(YEAR_MONTH_DAY);
 
      // Create an empty DateIntervalInfo object, which does not have any interval patterns inside.
      dtitvinf = new DateIntervalInfo();
 
      // a series of set interval patterns.
      // Only ERA, YEAR, MONTH, DATE,  DAY_OF_MONTH, DAY_OF_WEEK, AM_PM,  HOUR, HOUR_OF_DAY,
      MINUTE, SECOND and MILLISECOND are supported.
      dtitvinf.setIntervalPattern("yMMMd", Calendar.YEAR, "'y ~ y'");
      dtitvinf.setIntervalPattern("yMMMd", Calendar.MONTH, "yyyy 'diff' MMM d - MMM d");
      dtitvinf.setIntervalPattern("yMMMd", Calendar.DATE, "yyyy MMM d ~ d");
      dtitvinf.setIntervalPattern("yMMMd", Calendar.HOUR_OF_DAY, "yyyy MMM d HH:mm ~ HH:mm");
 
      // Set fallback interval pattern. Fallback pattern is used when interval pattern is not found.
      // If the fall-back pattern is not set,  falls back to {date0} - {date1} if interval pattern is not found.
      dtitvinf.setFallbackIntervalPattern("{0} - {1}");
 
      // Set above DateIntervalInfo object as the interval patterns of date interval formatter
      dtitvfmt.setDateIntervalInfo(dtitvinf);
 
      // Prepare to format
      pos = new FieldPosition(0);
      str = new StringBuffer("");
 
      // The 2 calendars should be equivalent, otherwise,  IllegalArgumentException will be thrown by format()
      Calendar fromCalendar = (Calendar) dtfmt.getCalendar().clone();
      Calendar toCalendar = (Calendar) dtfmt.getCalendar().clone();
      fromCalendar.setTimeInMillis(....);
      toCalendar.setTimeInMillis(...);
 
      //Formatting given 2 calendars
      dtitvfmt.format(fromCalendar, toCalendar, str, pos);
 
 
  
```

### Synchronization

The format methods of DateIntervalFormat may be used concurrently from multiple threads. Functions that alter the state of a DateIntervalFormat object (setters) may not be used concurrently with any other functions.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval` An immutable class containing the result of a date interval formatting operation. |

| Public methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#clone()()` Clone this Format object polymorphically. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#format(android.icu.util.Calendar,%20android.icu.util.Calendar,%20java.lang.StringBuffer,%20java.text.FieldPosition)(fromCalendar: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, toCalendar: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, appendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, pos: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Format 2 Calendars to produce a string. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#format(android.icu.util.DateInterval,%20java.lang.StringBuffer,%20java.text.FieldPosition)(dtInterval: https://developer.android.com/reference/kotlin/android/icu/util/DateInterval.html#!, appendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Format a DateInterval to produce a string. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, appendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Format an object to produce a string. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#format(java.time.temporal.Temporal,%20java.time.temporal.Temporal,%20java.lang.StringBuffer,%20java.text.FieldPosition)(fromTemporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!, toTemporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!, appendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, pos: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Format two `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#`s to produce a string. |
| open [DateIntervalFormat.FormattedDateInterval](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#formatToValue(android.icu.util.Calendar,%20android.icu.util.Calendar)(fromCalendar: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, toCalendar: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!)` Format 2 Calendars to produce a FormattedDateInterval. |
| open [DateIntervalFormat.FormattedDateInterval](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#formatToValue(android.icu.util.DateInterval)(dtInterval: https://developer.android.com/reference/kotlin/android/icu/util/DateInterval.html#!)` Format a DateInterval to produce a FormattedDateInterval. |
| open [DateIntervalFormat.FormattedDateInterval](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#formatToValue(java.time.temporal.Temporal,%20java.time.temporal.Temporal)(fromTemporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!, toTemporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!)` Format two `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#`s to produce a FormattedDateInterval. |
| open [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getContext(android.icu.text.DisplayContext.Type)(type: https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type!)` **\[icu\]** Get the formatter's DisplayContext value for the specified DisplayContext. |
| open [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getDateFormat()()` Gets the date formatter |
| open [DateIntervalInfo](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getDateIntervalInfo()()` Gets the date time interval patterns. |
| static [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getInstance(kotlin.String)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Construct a DateIntervalFormat from skeleton and the default `FORMAT` locale. |
| static [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getInstance(kotlin.String,%20android.icu.text.DateIntervalInfo)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, dtitvinf: https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo!)` Construct a DateIntervalFormat from skeleton DateIntervalInfo, and the default `FORMAT` locale. |
| static [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getInstance(kotlin.String,%20android.icu.util.ULocale)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Construct a DateIntervalFormat from skeleton and a given locale. |
| static [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getInstance(kotlin.String,%20android.icu.util.ULocale,%20android.icu.text.DateIntervalInfo)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!, dtitvinf: https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo!)` Construct a DateIntervalFormat from skeleton a DateIntervalInfo, and the given locale. |
| static [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getInstance(kotlin.String,%20java.util.Locale)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Construct a DateIntervalFormat from skeleton and a given locale. |
| static [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getInstance(kotlin.String,%20java.util.Locale,%20android.icu.text.DateIntervalInfo)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!, dtitvinf: https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo!)` Construct a DateIntervalFormat from skeleton a DateIntervalInfo, and the given locale. |
| open [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#getTimeZone()()` Get the TimeZone |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#parseObject(kotlin.String,%20java.text.ParsePosition)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, parse_pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Date interval parsing is not supported. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#setContext(android.icu.text.DisplayContext)(context: https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext!)` **\[icu\]** Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#setDateIntervalInfo(android.icu.text.DateIntervalInfo)(newItvPattern: https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo!)` Set the date time interval patterns. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#setTimeZone(android.icu.util.TimeZone)(zone: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!)` Set the TimeZone for the calendar used by this DateIntervalFormat object. |

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Clone this Format object polymorphically.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | A copy of the object. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(
    fromCalendar: Calendar!, 
    toCalendar: Calendar!, 
    appendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Format 2 Calendars to produce a string.

| Parameters ||
|---|---|
| `fromCalendar` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!: calendar set to the from date in date interval to be formatted into date interval string |
| `toCalendar` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!: calendar set to the to date in date interval to be formatted into date interval string |
| `appendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!: Output parameter to receive result. Result is appended to existing contents. |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!: On input: an alignment field, if desired. On output: the offsets of the alignment field. There may be multiple instances of a given field type in an interval format; in this case the fieldPosition offsets refer to the first instance. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | Reference to 'appendTo' parameter. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the two calendars are not equivalent. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(
    dtInterval: DateInterval!, 
    appendTo: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

Format a DateInterval to produce a string.

| Parameters ||
|---|---|
| `dtInterval` | [DateInterval](https://developer.android.com/reference/kotlin/android/icu/util/DateInterval.html#)!: DateInterval to be formatted. |
| `appendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!: Output parameter to receive result. Result is appended to existing contents. |
| `fieldPosition` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!: On input: an alignment field, if desired. On output: the offsets of the alignment field. There may be multiple instances of a given field type in an interval format; in this case the fieldPosition offsets refer to the first instance. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | Reference to 'appendTo' parameter. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(
    obj: Any!, 
    appendTo: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

Format an object to produce a string. This method handles Formattable objects with a DateInterval type. If a the Formattable object type is not a DateInterval, IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The object to format. Must be a DateInterval. |
| `toAppendTo` | where the text is to be appended |
| `pos` | A `FieldPosition` identifying a field in the formatted text |
| `appendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!: Output parameter to receive result. Result is appended to existing contents. |
| `fieldPosition` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!: On input: an alignment field, if desired. On output: the offsets of the alignment field. There may be multiple instances of a given field type in an interval format; in this case the fieldPosition offsets refer to the first instance. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | Reference to 'appendTo' parameter. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the formatted object is not DateInterval object |
| `java.lang.NullPointerException` | if `toAppendTo` or `pos` is null |

### format

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(
    fromTemporal: Temporal!, 
    toTemporal: Temporal!, 
    appendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Format two `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#`s to produce a string.

| Parameters ||
|---|---|
| `fromTemporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!: temporal set to the start of the interval to be formatted into a string |
| `toTemporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!: temporal set to the end of the interval to be formatted into a string |
| `appendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!: Output parameter to receive result. Result is appended to existing contents. |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!: On input: an alignment field, if desired. On output: the offsets of the alignment field. There may be multiple instances of a given field type in an interval format; in this case the fieldPosition offsets refer to the first instance. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | Reference to 'appendTo' parameter. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the two calendars are not equivalent. |

### formatToValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun formatToValue(
    fromCalendar: Calendar!, 
    toCalendar: Calendar!
): DateIntervalFormat.FormattedDateInterval!
```

Format 2 Calendars to produce a FormattedDateInterval. The FormattedDateInterval exposes field information about the formatted string.

| Parameters ||
|---|---|
| `fromCalendar` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!: calendar set to the from date in date interval to be formatted into date interval string |
| `toCalendar` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!: calendar set to the to date in date interval to be formatted into date interval string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval!` | A FormattedDateInterval containing the format result. |

### formatToValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun formatToValue(dtInterval: DateInterval!): DateIntervalFormat.FormattedDateInterval!
```

Format a DateInterval to produce a FormattedDateInterval. The FormattedDateInterval exposes field information about the formatted string.

| Parameters ||
|---|---|
| `dtInterval` | [DateInterval](https://developer.android.com/reference/kotlin/android/icu/util/DateInterval.html#)!: DateInterval to be formatted. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval!` | A FormattedDateInterval containing the format result. |

### formatToValue

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun formatToValue(
    fromTemporal: Temporal!, 
    toTemporal: Temporal!
): DateIntervalFormat.FormattedDateInterval!
```

Format two `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#`s to produce a FormattedDateInterval. The FormattedDateInterval exposes field information about the formatted string.

| Parameters ||
|---|---|
| `fromTemporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!: temporal set to the start of the interval to be formatted into a string |
| `toTemporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!: temporal set to the end of the interval to be formatted into a string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat.FormattedDateInterval!` | A FormattedDateInterval containing the format result. |

### getContext

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContext(type: DisplayContext.Type!): DisplayContext!
```

**\[icu\]** Get the formatter's DisplayContext value for the specified DisplayContext.Type, such as CAPITALIZATION.

| Parameters ||
|---|---|
| `type` | [DisplayContext.Type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type)!: the DisplayContext.Type whose value to return |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext!` | the current DisplayContext setting for the specified type |

### getDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDateFormat(): DateFormat!
```

Gets the date formatter

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat!` | a copy of the date formatter associated with this date interval formatter. |

### getDateIntervalInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDateIntervalInfo(): DateIntervalInfo!
```

Gets the date time interval patterns.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo!` | a copy of the date time interval patterns associated with this date interval formatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(skeleton: String!): DateIntervalFormat!
```

Construct a DateIntervalFormat from skeleton and the default `FORMAT` locale. This is a convenient override of getInstance(String skeleton, ULocale locale) with the value of locale as default `FORMAT` locale.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the skeleton on which interval format based. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#!` | a date time interval formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    skeleton: String!, 
    dtitvinf: DateIntervalInfo!
): DateIntervalFormat!
```

Construct a DateIntervalFormat from skeleton DateIntervalInfo, and the default `FORMAT` locale. This is a convenient override of getInstance(String skeleton, ULocale locale, DateIntervalInfo dtitvinf) with the locale value as default `FORMAT` locale.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the skeleton on which interval format based. |
| `dtitvinf` | [DateIntervalInfo](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo)!: the DateIntervalInfo object to be adopted. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#!` | a date time interval formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    skeleton: String!, 
    locale: ULocale!
): DateIntervalFormat!
```

Construct a DateIntervalFormat from skeleton and a given locale.

In this factory method, the date interval pattern information is load from resource files. Users are encouraged to created date interval formatter this way and to use the pre-defined skeleton macros.

There are pre-defined skeletons in DateFormat, such as MONTH_DAY, YEAR_MONTH_WEEKDAY_DAY etc. Those skeletons have pre-defined interval patterns in resource files. Users are encouraged to use them. For example: DateIntervalFormat.getInstance(DateFormat.MONTH_DAY, false, loc); The given Locale provides the interval patterns. For example, for en_GB, if skeleton is YEAR_ABBR_MONTH_WEEKDAY_DAY, which is "yMMMEEEd", the interval patterns defined in resource file to above skeleton are: "EEE, d MMM, yyyy - EEE, d MMM, yyyy" for year differs, "EEE, d MMM - EEE, d MMM, yyyy" for month differs, "EEE, d - EEE, d MMM, yyyy" for day differs,

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the skeleton on which interval format based. |
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!: the given locale |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#!` | a date time interval formatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    skeleton: String!, 
    locale: ULocale!, 
    dtitvinf: DateIntervalInfo!
): DateIntervalFormat!
```

Construct a DateIntervalFormat from skeleton a DateIntervalInfo, and the given locale.

In this factory method, user provides its own date interval pattern information, instead of using those pre-defined data in resource file. This factory method is for powerful users who want to provide their own interval patterns.

There are pre-defined skeleton in DateFormat, such as MONTH_DAY, YEAR_MONTH_WEEKDAY_DAY etc. Those skeletons have pre-defined interval patterns in resource files. Users are encouraged to use them. For example: DateIntervalFormat.getInstance(DateFormat.MONTH_DAY, false, loc,itvinf); the DateIntervalInfo provides the interval patterns. User are encouraged to set default interval pattern in DateIntervalInfo as well, if they want to set other interval patterns ( instead of reading the interval patterns from resource files). When the corresponding interval pattern for a largest calendar different field is not found ( if user not set it ), interval format fallback to the default interval pattern. If user does not provide default interval pattern, it fallback to "{date0} - {date1}"

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the skeleton on which interval format based. |
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!: the given locale |
| `dtitvinf` | [DateIntervalInfo](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo)!: the DateIntervalInfo object to be adopted. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#!` | a date time interval formatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    skeleton: String!, 
    locale: Locale!
): DateIntervalFormat!
```

Construct a DateIntervalFormat from skeleton and a given locale. This is a convenient override of getInstance(String skeleton, ULocale locale)

Example code:

```kotlin
import java.util.Date;
 
  import android.icu.text.DateFormat;
  import android.icu.text.DateIntervalFormat;
  import android.icu.text.DateIntervalInfo;
  import android.icu.util.Calendar;
  import android.icu.util.DateInterval;
  import android.icu.util.GregorianCalendar;
  import android.icu.util.ULocale;
  ...
  final Date date[] = {
          new GregorianCalendar(2007,10,10,10,10,10).getTime(),
          new GregorianCalendar(2008,10,10,10,10,10).getTime(),
          new GregorianCalendar(2008,11,10,10,10,10).getTime(),
          new GregorianCalendar(2008,11,10,15,10,10).getTime(),
  };
  final DateInterval dtitv[] = {
          new DateInterval(date[0].getTime(),date[1].getTime()),
          new DateInterval(date[1].getTime(),date[2].getTime()),
          new DateInterval(date[2].getTime(),date[3].getTime()),
  };
  final String [] skeletons = {
          DateFormat.YEAR_ABBR_MONTH_DAY,
          DateFormat.MONTH_DAY,
          DateFormat.HOUR_MINUTE,
  };
  System.out.printf("%-15s%-35s%-35s%-35s%-35s\n", "Skeleton", "from","to","Date Interval in en_US", "Date Interval in Ja");
  int i=0;
  for (String skeleton:skeletons) {
      System.out.printf("%-15s%-35s%-35s", skeleton,date[i].toString(), date[i+1].toString());
      DateIntervalFormat dtitvfmtEn = DateIntervalFormat.getInstance(skeleton, ULocale.ENGLISH);
      DateIntervalFormat dtitvfmtJa = DateIntervalFormat.getInstance(skeleton, ULocale.JAPANESE);
      System.out.printf("%-35s%-35s\n", dtitvfmtEn.format(dtitv[i]),dtitvfmtJa.format(dtitv[i]));
      i++;
  }
  /** output of the sample code:
   *********************************************************************************************************************************************************
   Skeleton       from                               to                                 Date Interval in en_US             Date Interval in Ja
   yMMMd          Sat Nov 10 10:10:10 EST 2007       Mon Nov 10 10:10:10 EST 2008       Nov 10, 2007 -- Nov 10, 2008        2007年11月10日～2008年11月10日
   MMMMd          Mon Nov 10 10:10:10 EST 2008       Wed Dec 10 10:10:10 EST 2008       November 10 -- December 10          11月10日～12月10日
   jm             Wed Dec 10 10:10:10 EST 2008       Wed Dec 10 15:10:10 EST 2008       10:10 AM -- 3:10 PM                 10:10～15:10
   *********************************************************************************************************************************************************<code>/</code>
```

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the skeleton on which interval format based. |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the given locale |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#!` | a date time interval formatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    skeleton: String!, 
    locale: Locale!, 
    dtitvinf: DateIntervalInfo!
): DateIntervalFormat!
```

Construct a DateIntervalFormat from skeleton a DateIntervalInfo, and the given locale. This is a convenient override of getInstance(String skeleton, ULocale locale, DateIntervalInfo dtitvinf)

Example code:

```kotlin
final Date date[] = {
          new GregorianCalendar(2007,9,10,10,10,10).getTime(),
          new GregorianCalendar(2007,10,10,10,10,10).getTime(),
          new GregorianCalendar(2007,10,10,22,10,10).getTime(),
  };
  final DateInterval dtitv[] = {
          new DateInterval(date[0].getTime(),date[1].getTime()),
          new DateInterval(date[1].getTime(),date[2].getTime()),
  };
  final String [] skeletons = {
          DateFormat.YEAR_ABBR_MONTH_DAY,
          DateFormat.HOUR24_MINUTE,
  };
  System.out.printf("%-15s%-35s%-35s%-45s%-35s\n", "Skeleton", "from","to", "Date Interval in en_US", "Date Interval in Ja");
  // Create an empty DateIntervalInfo object
  DateIntervalInfo dtitvinf = new DateIntervalInfo(ULocale.ENGLISH);
  // Set Date Time internal pattern for MONTH, DAY_OF_MONTH, HOUR_OF_DAY
  dtitvinf.setIntervalPattern("yMMMd", Calendar.MONTH, "y 'Diff' MMM d --- MMM d");
  dtitvinf.setIntervalPattern("Hm", Calendar.HOUR_OF_DAY, "yyyy MMM d HH:mm ~ HH:mm");
  // Set fallback interval pattern
  dtitvinf.setFallbackIntervalPattern("{0} ~~~ {1}");
  // Get the DateIntervalFormat with the custom pattern
  for (String skeleton:skeletons){
      for (int i=0;i<2;i++) {
          System.out.printf("%-15s%-35s%-35s", skeleton,date[i].toString(), date[i+1].toString());
          DateIntervalFormat dtitvfmtEn = DateIntervalFormat.getInstance(skeleton,ULocale.ENGLISH,dtitvinf);
          DateIntervalFormat dtitvfmtJa = DateIntervalFormat.getInstance(skeleton,ULocale.JAPANESE,dtitvinf);
          System.out.printf("%-45s%-35s\n", dtitvfmtEn.format(dtitv[i]),dtitvfmtJa.format(dtitv[i]));
      }
  }
  /** output of the sample code:
   *************************************************************************************************************************************************************************
    Skeleton       from                               to                                 Date Interval in en_US                       Date Interval in Ja
    yMMMd          Wed Oct 10 10:10:10 EDT 2007       Sat Nov 10 10:10:10 EST 2007       2007 Diff Oct 10 --- Nov 10                  2007 Diff 10月 10 --- 11月 10
    yMMMd          Sat Nov 10 10:10:10 EST 2007       Sat Nov 10 22:10:10 EST 2007       Nov 10, 2007                                 2007年11月10日
    Hm             Wed Oct 10 10:10:10 EDT 2007       Sat Nov 10 10:10:10 EST 2007       10/10/2007, 10:10 ~~~ 11/10/2007, 10:10      2007/10/10 10:10 ~~~ 2007/11/10 10:10
    Hm             Sat Nov 10 10:10:10 EST 2007       Sat Nov 10 22:10:10 EST 2007       2007 Nov 10 10:10 ~ 22:10                    2007 11月 10 10:10 ~ 22:10
   *************************************************************************************************************************************************************************<code>/</code>
```

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the skeleton on which interval format based. |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the given locale |
| `dtitvinf` | [DateIntervalInfo](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo)!: the DateIntervalInfo object to be adopted. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat#!` | a date time interval formatter. |

### getTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeZone(): TimeZone!
```

Get the TimeZone

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!` | A copy of the TimeZone associated with this date interval formatter. |

### parseObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseObject(
    source: String!, 
    parse_pos: ParsePosition!
): Any!
```

**Deprecated:** *This API is ICU internal only.*

Date interval parsing is not supported.

This method should handle parsing of date time interval strings into Formattable objects with DateInterval type, which is a pair of UDate.

Before calling, set parse_pos.index to the offset you want to start parsing at in the source. After calling, parse_pos.index is the end of the text you parsed. If error occurs, index is unchanged.

When parsing, leading whitespace is discarded (with a successful parse), while trailing whitespace is left as is.

See Format.parseObject() for more.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The string to be parsed into an object. |
| `pos` | A `ParsePosition` object with index and error index information as described above. |
| `parse_pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: The position to start parsing at. Since no parsing is supported, upon return this param is unchanged. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | A newly created `Formattable` object, or NULL on failure. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `source` or `pos` is null. |

### setContext

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContext(context: DisplayContext!): Unit
```

**\[icu\]** Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE. This causes the formatted result to be capitalized appropriately for the context in which it is intended to be used, considering both the locale and the type of field at the beginning of the formatted result.

| Parameters ||
|---|---|
| `context` | [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!: The DisplayContext value to set. |

### setDateIntervalInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDateIntervalInfo(newItvPattern: DateIntervalInfo!): Unit
```

Set the date time interval patterns.

| Parameters ||
|---|---|
| `newItvPattern` | [DateIntervalInfo](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo)!: the given interval patterns to copy. |

### setTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTimeZone(zone: TimeZone!): Unit
```

Set the TimeZone for the calendar used by this DateIntervalFormat object.

| Parameters ||
|---|---|
| `zone` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)!: The new TimeZone, will be cloned for use by this DateIntervalFormat. |
