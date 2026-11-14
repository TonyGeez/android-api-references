Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateFormat

```
abstract class DateFormat : UFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.text.Format](../java.text/Format.md) |||
| | ↳ | [android.icu.text.UFormat](UFormat.md) ||
| | | ↳ | [android.icu.text.DateFormat](DateFormat.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [SimpleDateFormat](SimpleDateFormat.md) |---|---| | [SimpleDateFormat](SimpleDateFormat.md) | **\[icu enhancement\]** ICU's replacement for `https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#`. | |
| --- | --- | --- | --- | --- | --- | --- |

**\[icu enhancement\]** ICU's replacement for `https://developer.android.com/reference/kotlin/java/text/DateFormat.html#`. Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

DateFormat is an abstract class for date/time formatting subclasses which formats and parses dates or time in a language-independent manner. The date/time formatting subclass, such as SimpleDateFormat, allows for formatting (i.e., date -\> text), parsing (text -\> date), and normalization. The date is represented as a `Date` object or as the milliseconds since January 1, 1970, 00:00:00 GMT.

DateFormat helps you to format and parse dates for any locale. Your code can be completely independent of the locale conventions for months, days of the week, or even the calendar format: lunar vs. solar. It provides many class methods for obtaining default date/time formatters based on the default for a given locale and a number of formatting styles or arbitrary "skeletons".

1. The formatting styles include FULL, LONG, MEDIUM, and SHORT. More detail and examples of using these styles are provided in the method descriptions.
2. The formatting styles only cover a fraction of the necessary usage. You often need to have just certain combinations of fields, like Month and Year, but have it to be formatted appropriate to a given locale. This is done using the (misnamed) getPatternInstance() method, supplying a skeleton. There are a number of constants that have common pre-defined skeletons, such as `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MINUTE_SECOND:kotlin.String` for something like "13:45" or `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_MONTH:kotlin.String` for something like "Sept 2012".

To format a date for the current Locale, use one of the static factory methods:

```kotlin
myString = DateFormat.getDateInstance().format(myDate);
  myString = DateFormat.getPatternInstance(DateFormat.YEAR_ABBR_MONTH).format(myDate);
  
```

If you are formatting multiple numbers, it is more efficient to get the format and use it multiple times so that the system doesn't have to fetch the information about the local language and country conventions multiple times.

```kotlin
DateFormat df = DateFormat.getDateInstance();
  for (int i = 0; i < a.length; ++i) {
      output.println(df.format(myDate[i]) + "; ");
  }
  
```

To format a date for a different Locale, specify it in the call to getDateInstance().

```kotlin
DateFormat df = DateFormat.getDateInstance(DateFormat.LONG, Locale.FRANCE);
  
```

You can use a DateFormat to parse also.

```kotlin
myDate = df.parse(myString);
  
```

There are many static factory methods available. Use getDateInstance to get the normal date format for that country. Use getTimeInstance to get the time format for that country. Use getDateTimeInstance to get a date and time format. You can pass in different options to these factory methods to control the length of the result; from SHORT to MEDIUM to LONG to FULL. The exact result depends on the locale, but generally:

- SHORT is completely numeric, such as 12.13.52 or 3:30pm
- MEDIUM is longer, such as Jan 12, 1952
- LONG is longer, such as January 12, 1952 or 3:30:32pm
- FULL is pretty completely specified, such as Tuesday, April 12, 1952 AD or 3:30:42pm PST.

Use getPatternInstance to format with a skeleton. Typically this is with a predefined skeleton, like `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_MONTH:kotlin.String` for something like "Sept 2012". If you don't want to use one of the predefined skeletons, you can supply your own. The skeletons are like the patterns in SimpleDateFormat, except they:

1. only keep the field pattern letter and ignore all other parts in a pattern, such as space, punctuation, and string literals.
2. are independent of the order of fields.
3. ignore certain differences in the field's pattern letter length:
 1. For those non-digit calendar fields, the pattern letter length is important, such as MMM, MMMM, and MMMMM; E and EEEE, and the field's pattern letter length is honored.
 2. For the digit calendar fields, such as M or MM, d or dd, yy or yyyy, the field pattern length is ignored and the best match, which is defined in date time patterns, will be returned without honor the field pattern letter length in skeleton.

You can also set the time zone on the format if you wish. If you want even more control over the format or parsing, (or want to give your users more control), you can try casting the DateFormat you get from the factory methods to a SimpleDateFormat. This will work for the majority of countries; just remember to put it in a try block in case you encounter an unusual one.

You can also use forms of the parse and format methods with ParsePosition and FieldPosition to allow you to

- progressively parse through pieces of a string.
- align any particular field, or find out where it is for selection on the screen.

### Synchronization

Date formats are not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.BooleanAttribute` boolean attributes |
| open | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.Field` The instances of this inner class are used as attribute keys and values in AttributedCharacterIterator that DateFormat. |
| | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.HourCycle` Hour Cycle |
| --- | --- |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_GENERIC_TZ:kotlin.String` **\[icu\]** Constant for *generic non-location format*, abbreviated if possible, such as PT; used in combinations date + time + zone, or time + zone. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String` **\[icu\]** Constant for date skeleton with abbreviated month. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with abbreviated month and day. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH_WEEKDAY_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with abbreviated month, weekday, and day. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_QUARTER:kotlin.String` **\[icu\]** Constant for date skeleton with abbreviated quarter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_SPECIFIC_TZ:kotlin.String` **\[icu\]** Constant for *specific non-location format*, abbreviated if possible, such as PDT; used in combinations date + time + zone, or time + zone. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_UTC_TZ:kotlin.String` **\[icu\]** Constant for *localized GMT/UTC format*, such as GMT+8:00 or HPG-8:00; used in combinations date + time + zone, or time + zone. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_WEEKDAY:kotlin.String` **\[icu\]** Constant for date skeleton with abbreviated weekday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#AM_PM_FIELD:kotlin.Int` FieldPosition selector for 'a' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#AM_PM:kotlin.Int` field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#AM_PM_MIDNIGHT_NOON_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'b' field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DATE_FIELD:kotlin.Int` FieldPosition selector for 'd' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DATE:kotlin.Int` field. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DAY:kotlin.String` **\[icu\]** Constant for date skeleton with day. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DAY_OF_WEEK_FIELD:kotlin.Int` FieldPosition selector for 'E' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DAY_OF_WEEK_IN_MONTH_FIELD:kotlin.Int` FieldPosition selector for 'F' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK_IN_MONTH:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DAY_OF_YEAR_FIELD:kotlin.Int` FieldPosition selector for 'D' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_YEAR:kotlin.Int` field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DEFAULT:kotlin.Int` Constant for default style pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DOW_LOCAL_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'e' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DOW_LOCAL:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ERA_FIELD:kotlin.Int` FieldPosition selector for 'G' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ERA:kotlin.Int` field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#EXTENDED_YEAR_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'u' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#EXTENDED_YEAR:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#FLEXIBLE_DAY_PERIOD_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'B' field alignment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#FRACTIONAL_SECOND_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'S' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MILLISECOND:kotlin.Int` field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#FULL:kotlin.Int` Constant for full style pattern. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#GENERIC_TZ:kotlin.String` **\[icu\]** Constant for *generic non-location format*, such as Pacific Time; used in combinations date + time + zone, or time + zone. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR:kotlin.String` **\[icu\]** Constant for date skeleton with hour, with the locale's preferred hour format (12 or 24). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR0_FIELD:kotlin.Int` FieldPosition selector for 'K' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR1_FIELD:kotlin.Int` FieldPosition selector for 'h' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR:kotlin.Int` field. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR24:kotlin.String` **\[icu\]** Constant for date skeleton with hour in 24-hour presentation. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR24_MINUTE:kotlin.String` **\[icu\]** Constant for date skeleton with hour and minute in 24-hour presentation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR24_MINUTE_SECOND:kotlin.String` **\[icu\]** Constant for date skeleton with hour, minute, and second in 24-hour presentation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR_MINUTE:kotlin.String` **\[icu\]** Constant for date skeleton with hour and minute, with the locale's preferred hour format (12 or 24). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR_MINUTE_SECOND:kotlin.String` **\[icu\]** Constant for date skeleton with hour, minute, and second, with the locale's preferred hour format (12 or 24). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR_OF_DAY0_FIELD:kotlin.Int` FieldPosition selector for 'H' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR_OF_DAY:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR_OF_DAY1_FIELD:kotlin.Int` FieldPosition selector for 'k' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR_OF_DAY:kotlin.Int` field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#JULIAN_DAY_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'g' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#JULIAN_DAY:kotlin.Int` field. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#LOCATION_TZ:kotlin.String` **\[icu\]** Constant for *generic location format*, such as Los Angeles Time; used in combinations date + time + zone, or time + zone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#LONG:kotlin.Int` Constant for long style pattern. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int` Constant for medium style pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MILLISECONDS_IN_DAY_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'A' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MILLISECONDS_IN_DAY:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MILLISECOND_FIELD:kotlin.Int` Alias for FRACTIONAL_SECOND_FIELD. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MINUTE:kotlin.String` **\[icu\]** Constant for date skeleton with minute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MINUTE_FIELD:kotlin.Int` FieldPosition selector for 'm' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MINUTE:kotlin.Int` field. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MINUTE_SECOND:kotlin.String` **\[icu\]** Constant for date skeleton with minute and second. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH:kotlin.String` **\[icu\]** Constant for date skeleton with month. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with long month and day. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_FIELD:kotlin.Int` FieldPosition selector for 'M' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int` field. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with month, weekday, and day. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#NONE:kotlin.Int` **\[icu\]** Constant for empty style pattern. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#NUM_MONTH:kotlin.String` **\[icu\]** Constant for date skeleton with numeric month. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#NUM_MONTH_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with numeric month and day. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#NUM_MONTH_WEEKDAY_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with numeric month, weekday, and day. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#QUARTER:kotlin.String` **\[icu\]** Constant for date skeleton with quarter. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#QUARTER_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'Q' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE:kotlin.Int` **\[icu\]** Constant for relative style mask. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_DEFAULT:kotlin.Int` **\[icu\]** Constant for relative default style pattern. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_FULL:kotlin.Int` **\[icu\]** Constant for relative full style pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_LONG:kotlin.Int` **\[icu\]** Constant for relative style pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_MEDIUM:kotlin.Int` **\[icu\]** Constant for relative style pattern. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_SHORT:kotlin.Int` **\[icu\]** Constant for relative style pattern. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SECOND:kotlin.String` **\[icu\]** Constant for date skeleton with second. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SECOND_FIELD:kotlin.Int` FieldPosition selector for 's' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#SECOND:kotlin.Int` field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int` Constant for short style pattern. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SPECIFIC_TZ:kotlin.String` **\[icu\]** Constant for *specific non-location format*, such as Pacific Daylight Time; used in combinations date + time + zone, or time + zone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#STANDALONE_DAY_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'c' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK:kotlin.Int` field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#STANDALONE_MONTH_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'L' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#STANDALONE_QUARTER_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'q' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_FIELD:kotlin.Int` FieldPosition selector for 'z' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_GENERIC_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'v' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_ISO_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'X' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_ISO_LOCAL_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'x' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_LOCALIZED_GMT_OFFSET_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'O' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_RFC_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'Z' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_SPECIAL_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'V' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#WEEKDAY:kotlin.String` **\[icu\]** Constant for date skeleton with weekday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#WEEK_OF_MONTH_FIELD:kotlin.Int` FieldPosition selector for 'W' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#WEEK_OF_MONTH:kotlin.Int` field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#WEEK_OF_YEAR_FIELD:kotlin.Int` FieldPosition selector for 'w' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#WEEK_OF_YEAR:kotlin.Int` field. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR:kotlin.String` **\[icu\]** Constant for date skeleton with year. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_MONTH:kotlin.String` **\[icu\]** Constant for date skeleton with year and abbreviated month. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_MONTH_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with year, abbreviated month, and day. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_MONTH_WEEKDAY_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with year, abbreviated month, weekday, and day. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_QUARTER:kotlin.String` **\[icu\]** Constant for date skeleton with year and abbreviated quarter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_FIELD:kotlin.Int` FieldPosition selector for 'y' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR:kotlin.Int` field. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_MONTH:kotlin.String` **\[icu\]** Constant for date skeleton with year and month. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_MONTH_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with year, month, and day. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_MONTH_WEEKDAY_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with year, month, weekday, and day. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_NAME_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'U' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR:kotlin.Int` field. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_NUM_MONTH:kotlin.String` **\[icu\]** Constant for date skeleton with year and numeric month. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_NUM_MONTH_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with year, numeric month, and day. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_NUM_MONTH_WEEKDAY_DAY:kotlin.String` **\[icu\]** Constant for date skeleton with year, numeric month, weekday, and day. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_QUARTER:kotlin.String` **\[icu\]** Constant for date skeleton with year and quarter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_WOY_FIELD:kotlin.Int` **\[icu\]** FieldPosition selector for 'Y' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR_WOY:kotlin.Int` field. |
| --- | --- |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DateFormat()()` Creates a new date format. |

| Public methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#clone()()` Overrides clone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Overrides equals. |
| abstract [StringBuffer](../java.lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(android.icu.util.Calendar,%20java.lang.StringBuffer,%20java.text.FieldPosition)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, toAppendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Formats a date into a date/time string. |
| --- | --- |
| [StringBuffer](../java.lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, toAppendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Formats a time object into a time string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(java.time.temporal.Temporal)(date: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!)` Formats a `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#` into a date/time string. |
| open [StringBuffer](../java.lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(java.time.temporal.Temporal,%20java.lang.StringBuffer,%20java.text.FieldPosition)(date: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!, toAppendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Formats a `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#` into a date/time string. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(java.util.Date)(date: https://developer.android.com/reference/kotlin/java/util/Date.html#!)` Formats a Date into a date/time string. |
| open [StringBuffer](../java.lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(java.util.Date,%20java.lang.StringBuffer,%20java.text.FieldPosition)(date: https://developer.android.com/reference/kotlin/java/util/Date.html#!, toAppendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Formats a Date into a date/time string. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java.util/Locale.md)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getAvailableLocales()()` Returns the set of locales for which DateFormats are installed. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getBooleanAttribute(android.icu.text.DateFormat.BooleanAttribute)(key: https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.BooleanAttribute!)` Returns the current value for the specified BooleanAttribute for this instance if attribute is missing false is returned. |
| open [Calendar](../android.icu.util/Calendar.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getCalendar()()` Returns the calendar associated with this date/time formatter. |
| open [DisplayContext](DisplayContext.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getContext(android.icu.text.DisplayContext.Type)(type: https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type!)` **\[icu\]** Get the formatter's DisplayContext value for the specified DisplayContext. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance()()` Returns the date formatter with the default formatting style for the default `FORMAT` locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(android.icu.util.Calendar,%20kotlin.Int)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object for the default locale that can be used to format dates in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(android.icu.util.Calendar,%20kotlin.Int,%20android.icu.util.ULocale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates in the calendar system specified by `cal`. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(android.icu.util.Calendar,%20kotlin.Int,%20java.util.Locale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the date formatter with the given formatting style for the default `FORMAT` locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(kotlin.Int,%20android.icu.util.ULocale)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Returns the date formatter with the given formatting style for the given locale. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, aLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns the date formatter with the given formatting style for the given locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance()()` Returns the date/time formatter with the default formatting style for the default `FORMAT` locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20kotlin.Int)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object for the default locale that can be used to format dates and times in the calendar system specified by `cal`. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20kotlin.Int,%20android.icu.util.ULocale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20kotlin.Int,%20java.util.Locale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int)(dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the date/time formatter with the given date and time formatting styles for the default `FORMAT` locale. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int,%20android.icu.util.ULocale)(dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Returns the date/time formatter with the given formatting styles for the given locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int,%20java.util.Locale)(dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, aLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns the date/time formatter with the given formatting styles for the given locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstance()()` Returns a default date/time formatter that uses the SHORT style for both the date and the time. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstance(android.icu.util.Calendar)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!)` Returns a default date/time formatter that uses the SHORT style for both the date and the time. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstance(android.icu.util.Calendar,%20android.icu.util.ULocale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Returns a date/time formatter that uses the SHORT style for both the date and the time. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstance(android.icu.util.Calendar,%20java.util.Locale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns a date/time formatter that uses the SHORT style for both the date and the time. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(android.icu.util.Calendar,%20kotlin.String,%20android.icu.util.ULocale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **\[icu\]** Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(android.icu.util.Calendar,%20kotlin.String,%20java.util.Locale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **\[icu\]** Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(kotlin.String)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the default locale. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(kotlin.String,%20android.icu.util.ULocale)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the given locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(kotlin.String,%20java.util.Locale)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the given locale. |
| open [NumberFormat](NumberFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getNumberFormat()()` Returns the number formatter which this date/time formatter uses to format and parse a time. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(android.icu.util.Calendar,%20kotlin.String,%20android.icu.util.ULocale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **\[icu\]** Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(android.icu.util.Calendar,%20kotlin.String,%20java.util.Locale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **\[icu\]** Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(kotlin.String)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the default locale. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(kotlin.String,%20android.icu.util.ULocale)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the given locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(kotlin.String,%20java.util.Locale)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the given locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance()()` Gets the time formatter with the default formatting style for the default `FORMAT` locale. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(android.icu.util.Calendar,%20kotlin.Int)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format times in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20android.icu.util.ULocale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format times in the calendar system specified by `cal`. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20java.util.Locale)(cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format times in the calendar system specified by `cal`. |
| --- | --- |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the time formatter with the given formatting style for the default `FORMAT` locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(kotlin.Int,%20android.icu.util.ULocale)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Returns the time formatter with the given formatting style for the given locale. |
| static [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, aLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns the time formatter with the given formatting style for the given locale. |
| --- | --- |
| open [TimeZone](../android.icu.util/TimeZone.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeZone()()` Returns the time zone. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#hashCode()()` Overrides hashCode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#isCalendarLenient()()` Returns whether date/time parsing in the encapsulated Calendar object is lenient. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#isLenient()()` Returns whether both date/time parsing in the encapsulated Calendar object and DateFormat whitespace \& numeric processing is lenient. |
| open [Date](../java.util/Date.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parse(kotlin.String)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Parses a date/time string. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parse(kotlin.String,%20android.icu.util.Calendar,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cal: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Parses a date/time string according to the given parse position. |
| --- | --- |
| open [Date](../java.util/Date.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parse(kotlin.String,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Parses a date/time string according to the given parse position. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parseObject(kotlin.String,%20java.text.ParsePosition)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Parses a date/time string into an Object. |
| open [DateFormat](DateFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setBooleanAttribute(android.icu.text.DateFormat.BooleanAttribute,%20kotlin.Boolean)(key: https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.BooleanAttribute!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets a boolean attribute for this instance. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setCalendar(android.icu.util.Calendar)(newCalendar: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!)` Sets the calendar to be used by this date format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setCalendarLenient(kotlin.Boolean)(lenient: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies whether date/time parsing in the encapsulated Calendar object should be lenient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setContext(android.icu.text.DisplayContext)(context: https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext!)` **\[icu\]** Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setLenient(kotlin.Boolean)(lenient: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specifies whether date/time parsing is to be lenient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setNumberFormat(android.icu.text.NumberFormat)(newNumberFormat: https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!)` Sets the number formatter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setTimeZone(android.icu.util.TimeZone)(zone: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!)` Sets the time zone for the calendar of this DateFormat object. |
| --- | --- |

| Properties ||
|---|---|
| [Calendar](../android.icu.util/Calendar.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#calendar:android.icu.util.Calendar` The calendar that `DateFormat` uses to produce the time field values needed to implement date and time formatting. |
| [NumberFormat](NumberFormat.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#numberFormat:android.icu.text.NumberFormat` The number formatter that `DateFormat` uses to format numbers in dates and times. |

## Constants

### ABBR_GENERIC_TZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABBR_GENERIC_TZ: String
```

**\[icu\]** Constant for *generic non-location format*, abbreviated if possible, such as PT; used in combinations date + time + zone, or time + zone.

 Value: "v"

**See Also**

### ABBR_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABBR_MONTH: String
```

**\[icu\]** Constant for date skeleton with abbreviated month.

 Value: "MMM"

### ABBR_MONTH_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABBR_MONTH_DAY: String
```

**\[icu\]** Constant for date skeleton with abbreviated month and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "MMMd"

### ABBR_MONTH_WEEKDAY_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABBR_MONTH_WEEKDAY_DAY: String
```

**\[icu\]** Constant for date skeleton with abbreviated month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "MMMEd"

### ABBR_QUARTER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABBR_QUARTER: String
```

**\[icu\]** Constant for date skeleton with abbreviated quarter.

 Value: "QQQ"

### ABBR_SPECIFIC_TZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABBR_SPECIFIC_TZ: String
```

**\[icu\]** Constant for *specific non-location format*, abbreviated if possible, such as PDT; used in combinations date + time + zone, or time + zone.

 Value: "z"

**See Also**

### ABBR_UTC_TZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABBR_UTC_TZ: String
```

**\[icu\]** Constant for *localized GMT/UTC format*, such as GMT+8:00 or HPG-8:00; used in combinations date + time + zone, or time + zone.

 Value: "ZZZZ"

**See Also**

### ABBR_WEEKDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ABBR_WEEKDAY: String
```

**\[icu\]** Constant for date skeleton with abbreviated weekday.

 Value: "E"

### AM_PM_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AM_PM_FIELD: Int
```

FieldPosition selector for 'a' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#AM_PM:kotlin.Int` field.

 Value: 14

### AM_PM_MIDNIGHT_NOON_FIELD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AM_PM_MIDNIGHT_NOON_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'b' field alignment. No related Calendar field. This displays the fixed day period (am/pm/midnight/noon).

 Value: 35

### DATE_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATE_FIELD: Int
```

FieldPosition selector for 'd' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DATE:kotlin.Int` field.

 Value: 3

### DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY: String
```

**\[icu\]** Constant for date skeleton with day.

 Value: "d"

### DAY_OF_WEEK_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_WEEK_FIELD: Int
```

FieldPosition selector for 'E' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK:kotlin.Int` field.

 Value: 9

### DAY_OF_WEEK_IN_MONTH_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_WEEK_IN_MONTH_FIELD: Int
```

FieldPosition selector for 'F' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK_IN_MONTH:kotlin.Int` field.

 Value: 11

### DAY_OF_YEAR_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_YEAR_FIELD: Int
```

FieldPosition selector for 'D' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_YEAR:kotlin.Int` field.

 Value: 10

### DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT: Int
```

Constant for default style pattern. Its value is MEDIUM.

 Value: 2

### DOW_LOCAL_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOW_LOCAL_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'e' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DOW_LOCAL:kotlin.Int` field.

 Value: 19

### ERA_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERA_FIELD: Int
```

FieldPosition selector for 'G' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ERA:kotlin.Int` field.

 Value: 0

### EXTENDED_YEAR_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENDED_YEAR_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'u' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#EXTENDED_YEAR:kotlin.Int` field.

 Value: 20

### FLEXIBLE_DAY_PERIOD_FIELD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLEXIBLE_DAY_PERIOD_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'B' field alignment. No related Calendar field. This displays the flexible day period.

 Value: 36

### FRACTIONAL_SECOND_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRACTIONAL_SECOND_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'S' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MILLISECOND:kotlin.Int` field. Note: Time formats that use 'S' can display a maximum of three significant digits for fractional seconds, corresponding to millisecond resolution and a fractional seconds sub-pattern of SSS. If the sub-pattern is S or SS, the fractional seconds value will be truncated (not rounded) to the number of display places specified. If the fractional seconds sub-pattern is longer than SSS, the additional display places will be filled with zeros.

 Value: 8

### FULL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FULL: Int
```

Constant for full style pattern.

 Value: 0

### GENERIC_TZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GENERIC_TZ: String
```

**\[icu\]** Constant for *generic non-location format*, such as Pacific Time; used in combinations date + time + zone, or time + zone.

 Value: "vvvv"

**See Also**

### HOUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR: String
```

**\[icu\]** Constant for date skeleton with hour, with the locale's preferred hour format (12 or 24).

 Value: "j"

### HOUR0_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR0_FIELD: Int
```

FieldPosition selector for 'K' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR:kotlin.Int` field. HOUR0_FIELD is used for the zero-based 12-hour clock. For example, 11:30 PM + 1 hour results in 00:30 AM.

 Value: 16

### HOUR1_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR1_FIELD: Int
```

FieldPosition selector for 'h' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR:kotlin.Int` field. HOUR1_FIELD is used for the one-based 12-hour clock. For example, 11:30 PM + 1 hour results in 12:30 AM.

 Value: 15

### HOUR24

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR24: String
```

**\[icu\]** Constant for date skeleton with hour in 24-hour presentation.

 Value: "H"

### HOUR24_MINUTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR24_MINUTE: String
```

**\[icu\]** Constant for date skeleton with hour and minute in 24-hour presentation. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "Hm"

### HOUR24_MINUTE_SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR24_MINUTE_SECOND: String
```

**\[icu\]** Constant for date skeleton with hour, minute, and second in 24-hour presentation. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "Hms"

### HOUR_MINUTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR_MINUTE: String
```

**\[icu\]** Constant for date skeleton with hour and minute, with the locale's preferred hour format (12 or 24). Used in combinations date + time, date + time + zone, or time + zone.

 Value: "jm"

### HOUR_MINUTE_SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR_MINUTE_SECOND: String
```

**\[icu\]** Constant for date skeleton with hour, minute, and second, with the locale's preferred hour format (12 or 24). Used in combinations date + time, date + time + zone, or time + zone.

 Value: "jms"

### HOUR_OF_DAY0_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR_OF_DAY0_FIELD: Int
```

FieldPosition selector for 'H' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR_OF_DAY:kotlin.Int` field. HOUR_OF_DAY0_FIELD is used for the zero-based 24-hour clock. For example, 23:59 + 01:00 results in 00:59.

 Value: 5

### HOUR_OF_DAY1_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR_OF_DAY1_FIELD: Int
```

FieldPosition selector for 'k' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR_OF_DAY:kotlin.Int` field. HOUR_OF_DAY1_FIELD is used for the one-based 24-hour clock. For example, 23:59 + 01:00 results in 24:59.

 Value: 4

### JULIAN_DAY_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JULIAN_DAY_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'g' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#JULIAN_DAY:kotlin.Int` field.

 Value: 21

### LOCATION_TZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCATION_TZ: String
```

**\[icu\]** Constant for *generic location format*, such as Los Angeles Time; used in combinations date + time + zone, or time + zone.

 Value: "VVVV"

**See Also**

### LONG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LONG: Int
```

Constant for long style pattern.

 Value: 1

### MEDIUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEDIUM: Int
```

Constant for medium style pattern.

 Value: 2

### MILLISECONDS_IN_DAY_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MILLISECONDS_IN_DAY_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'A' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MILLISECONDS_IN_DAY:kotlin.Int` field.

 Value: 22

### MILLISECOND_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MILLISECOND_FIELD: Int
```

Alias for FRACTIONAL_SECOND_FIELD.

 Value: 8

### MINUTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINUTE: String
```

**\[icu\]** Constant for date skeleton with minute.

 Value: "m"

### MINUTE_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINUTE_FIELD: Int
```

FieldPosition selector for 'm' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MINUTE:kotlin.Int` field.

 Value: 6

### MINUTE_SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINUTE_SECOND: String
```

**\[icu\]** Constant for date skeleton with minute and second. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "ms"

### MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH: String
```

**\[icu\]** Constant for date skeleton with month.

 Value: "MMMM"

### MONTH_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_DAY: String
```

**\[icu\]** Constant for date skeleton with long month and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "MMMMd"

### MONTH_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_FIELD: Int
```

FieldPosition selector for 'M' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int` field.

 Value: 2

### MONTH_WEEKDAY_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_WEEKDAY_DAY: String
```

**\[icu\]** Constant for date skeleton with month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "MMMMEEEEd"

### NONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NONE: Int
```

**\[icu\]** Constant for empty style pattern.

 Value: -1

### NUM_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NUM_MONTH: String
```

**\[icu\]** Constant for date skeleton with numeric month.

 Value: "M"

### NUM_MONTH_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NUM_MONTH_DAY: String
```

**\[icu\]** Constant for date skeleton with numeric month and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "Md"

### NUM_MONTH_WEEKDAY_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NUM_MONTH_WEEKDAY_DAY: String
```

**\[icu\]** Constant for date skeleton with numeric month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "MEd"

### QUARTER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUARTER: String
```

**\[icu\]** Constant for date skeleton with quarter.

 Value: "QQQQ"

### QUARTER_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUARTER_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'Q' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int` field. This displays the quarter.

 Value: 27

### RELATIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE: Int
```

**\[icu\]** Constant for relative style mask.

 Value: 128

### RELATIVE_DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE_DEFAULT: Int
```

**\[icu\]** Constant for relative default style pattern.

 Value: 130

### RELATIVE_FULL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE_FULL: Int
```

**\[icu\]** Constant for relative full style pattern.

 Value: 128

### RELATIVE_LONG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE_LONG: Int
```

**\[icu\]** Constant for relative style pattern.

 Value: 129

### RELATIVE_MEDIUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE_MEDIUM: Int
```

**\[icu\]** Constant for relative style pattern.

 Value: 130

### RELATIVE_SHORT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE_SHORT: Int
```

**\[icu\]** Constant for relative style pattern.

 Value: 131

### SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECOND: String
```

**\[icu\]** Constant for date skeleton with second.

 Value: "s"

### SECOND_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECOND_FIELD: Int
```

FieldPosition selector for 's' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#SECOND:kotlin.Int` field.

 Value: 7

### SHORT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHORT: Int
```

Constant for short style pattern.

 Value: 3

### SPECIFIC_TZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SPECIFIC_TZ: String
```

**\[icu\]** Constant for *specific non-location format*, such as Pacific Daylight Time; used in combinations date + time + zone, or time + zone.

 Value: "zzzz"

**See Also**

### STANDALONE_DAY_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDALONE_DAY_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'c' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK:kotlin.Int` field. This displays the stand alone day name, if available.

 Value: 25

### STANDALONE_MONTH_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDALONE_MONTH_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'L' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int` field. This displays the stand alone month name, if available.

 Value: 26

### STANDALONE_QUARTER_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDALONE_QUARTER_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'q' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int` field. This displays the stand alone quarter, if available.

 Value: 28

### TIMEZONE_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_FIELD: Int
```

FieldPosition selector for 'z' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields.

 Value: 17

### TIMEZONE_GENERIC_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_GENERIC_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'v' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. This displays the generic zone name, if available.

 Value: 24

### TIMEZONE_ISO_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_ISO_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'X' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. This displays the ISO 8601 local time offset format or UTC indicator ("Z").

 Value: 32

### TIMEZONE_ISO_LOCAL_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_ISO_LOCAL_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'x' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. This displays the ISO 8601 local time offset format.

 Value: 33

### TIMEZONE_LOCALIZED_GMT_OFFSET_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_LOCALIZED_GMT_OFFSET_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'O' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. This displays the localized GMT format.

 Value: 31

### TIMEZONE_RFC_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_RFC_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'Z' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields.

 Value: 23

### TIMEZONE_SPECIAL_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_SPECIAL_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'V' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int` fields. This displays the fallback timezone name when VVVV is specified, and the short standard or daylight timezone name ignoring commonlyUsed when a single V is specified.

 Value: 29

### WEEKDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY: String
```

**\[icu\]** Constant for date skeleton with weekday.

 Value: "EEEE"

### WEEK_OF_MONTH_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_OF_MONTH_FIELD: Int
```

FieldPosition selector for 'W' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#WEEK_OF_MONTH:kotlin.Int` field.

 Value: 13

### WEEK_OF_YEAR_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_OF_YEAR_FIELD: Int
```

FieldPosition selector for 'w' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#WEEK_OF_YEAR:kotlin.Int` field.

 Value: 12

### YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR: String
```

**\[icu\]** Constant for date skeleton with year.

 Value: "y"

### YEAR_ABBR_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_ABBR_MONTH: String
```

**\[icu\]** Constant for date skeleton with year and abbreviated month.

 Value: "yMMM"

### YEAR_ABBR_MONTH_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_ABBR_MONTH_DAY: String
```

**\[icu\]** Constant for date skeleton with year, abbreviated month, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "yMMMd"

### YEAR_ABBR_MONTH_WEEKDAY_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_ABBR_MONTH_WEEKDAY_DAY: String
```

**\[icu\]** Constant for date skeleton with year, abbreviated month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "yMMMEd"

### YEAR_ABBR_QUARTER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_ABBR_QUARTER: String
```

**\[icu\]** Constant for date skeleton with year and abbreviated quarter.

 Value: "yQQQ"

### YEAR_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_FIELD: Int
```

FieldPosition selector for 'y' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR:kotlin.Int` field.

 Value: 1

### YEAR_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_MONTH: String
```

**\[icu\]** Constant for date skeleton with year and month.

 Value: "yMMMM"

### YEAR_MONTH_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_MONTH_DAY: String
```

**\[icu\]** Constant for date skeleton with year, month, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "yMMMMd"

### YEAR_MONTH_WEEKDAY_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_MONTH_WEEKDAY_DAY: String
```

**\[icu\]** Constant for date skeleton with year, month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "yMMMMEEEEd"

### YEAR_NAME_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_NAME_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'U' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR:kotlin.Int` field. This displays the cyclic year name, if available.

 Value: 30

### YEAR_NUM_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_NUM_MONTH: String
```

**\[icu\]** Constant for date skeleton with year and numeric month.

 Value: "yM"

### YEAR_NUM_MONTH_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_NUM_MONTH_DAY: String
```

**\[icu\]** Constant for date skeleton with year, numeric month, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "yMd"

### YEAR_NUM_MONTH_WEEKDAY_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_NUM_MONTH_WEEKDAY_DAY: String
```

**\[icu\]** Constant for date skeleton with year, numeric month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone.

 Value: "yMEd"

### YEAR_QUARTER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_QUARTER: String
```

**\[icu\]** Constant for date skeleton with year and quarter.

 Value: "yQQQQ"

### YEAR_WOY_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_WOY_FIELD: Int
```

**\[icu\]** FieldPosition selector for 'Y' field alignment, corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR_WOY:kotlin.Int` field.

 Value: 18

## Protected constructors

### DateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected DateFormat()
```

Creates a new date format.

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Overrides clone.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Overrides equals.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun format(
    cal: Calendar!, 
    toAppendTo: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

Formats a date into a date/time string.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: a Calendar set to the date and time to be formatted into a date/time string. When the calendar type is different from the internal calendar held by this DateFormat instance, the date and the time zone will be inherited from the input calendar, but other calendar field values will be calculated by the internal calendar. |
| `toAppendTo` | [StringBuffer](../java.lang/StringBuffer.md)!: the string buffer for the returning date/time string. |
| `fieldPosition` | [FieldPosition](../java.text/FieldPosition.md)!: keeps track of the position of the field within the returned string. On input: an alignment field, if desired. On output: the offsets of the alignment field. For example, given a time text "1996.07.10 AD at 15:08:56 PDT", if the given fieldPosition is DateFormat.YEAR_FIELD, the begin index and end index of fieldPosition will be set to 0 and 4, respectively. Notice that if the same time field appears more than once in a pattern, the fieldPosition will be set for the first occurrence of that time field. For instance, formatting a Date to the time string "1 PM PDT (Pacific Daylight Time)" using the pattern "h a z (zzzz)" and the alignment field DateFormat.TIMEZONE_FIELD, the begin index and end index of fieldPosition will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character 'z'. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | the formatted date/time string. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(
    obj: Any!, 
    toAppendTo: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

Formats a time object into a time string. Examples of time objects are a time value expressed in milliseconds and a Date object.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: must be a Number or a Date or a Calendar. |
| `toAppendTo` | [StringBuffer](../java.lang/StringBuffer.md)!: the string buffer for the returning time string. |
| `pos` | A `FieldPosition` identifying a field in the formatted text |
| --- | --- |
| `fieldPosition` | [FieldPosition](../java.text/FieldPosition.md)!: keeps track of the position of the field within the returned string. On input: an alignment field, if desired. On output: the offsets of the alignment field. For example, given a time text "1996.07.10 AD at 15:08:56 PDT", if the given fieldPosition is DateFormat.YEAR_FIELD, the begin index and end index of fieldPosition will be set to 0 and 4, respectively. Notice that if the same time field appears more than once in a pattern, the fieldPosition will be set for the first occurrence of that time field. For instance, formatting a Date to the time string "1 PM PDT (Pacific Daylight Time)" using the pattern "h a z (zzzz)" and the alignment field DateFormat.TIMEZONE_FIELD, the begin index and end index of fieldPosition will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character 'z'. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | the formatted time string. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Format cannot format the given object |
| `java.lang.NullPointerException` | if `toAppendTo` or `pos` is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/text/Format.html#`

### format

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(date: Temporal!): String!
```

Formats a `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#` into a date/time string.

| Parameters ||
|---|---|
| `date` | [Temporal](../java.time.temporal/Temporal.md)!: the time value to be formatted into a time string. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the formatted time string. |

### format

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    date: Temporal!, 
    toAppendTo: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

Formats a `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#` into a date/time string.

| Parameters ||
|---|---|
| `date` | [Temporal](../java.time.temporal/Temporal.md)!: a `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#` to be formatted into a date/time string. |
| `toAppendTo` | [StringBuffer](../java.lang/StringBuffer.md)!: the string buffer for the returning date/time string. |
| `fieldPosition` | [FieldPosition](../java.text/FieldPosition.md)!: keeps track of the position of the field within the returned string. On input: an alignment field, if desired. On output: the offsets of the alignment field. For example, given a time text "1996.07.10 AD at 15:08:56 PDT", if the given `fieldPosition` is `DateFormat.YEAR_FIELD`, the begin index and end index of `fieldPosition` will be set to 0 and 4, respectively. Notice that if the same time field appears more than once in a pattern, the fieldPosition will be set for the first occurrence of that time field. For instance, formatting a `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#` to the time string "1 PM PDT (Pacific Daylight Time)" using the pattern "h a z (zzzz)" and the alignment field `DateFormat.TIMEZONE_FIELD`, the begin index and end index of `fieldPosition` will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character 'z'. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | the formatted date/time string. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(date: Date!): String!
```

Formats a Date into a date/time string.

| Parameters ||
|---|---|
| `date` | [Date](../java.util/Date.md)!: the time value to be formatted into a time string. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the formatted time string. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    date: Date!, 
    toAppendTo: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

Formats a Date into a date/time string.

| Parameters ||
|---|---|
| `date` | [Date](../java.util/Date.md)!: a Date to be formatted into a date/time string. |
| `toAppendTo` | [StringBuffer](../java.lang/StringBuffer.md)!: the string buffer for the returning date/time string. |
| `fieldPosition` | [FieldPosition](../java.text/FieldPosition.md)!: keeps track of the position of the field within the returned string. On input: an alignment field, if desired. On output: the offsets of the alignment field. For example, given a time text "1996.07.10 AD at 15:08:56 PDT", if the given fieldPosition is DateFormat.YEAR_FIELD, the begin index and end index of fieldPosition will be set to 0 and 4, respectively. Notice that if the same time field appears more than once in a pattern, the fieldPosition will be set for the first occurrence of that time field. For instance, formatting a Date to the time string "1 PM PDT (Pacific Daylight Time)" using the pattern "h a z (zzzz)" and the alignment field DateFormat.TIMEZONE_FIELD, the begin index and end index of fieldPosition will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character 'z'. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | the formatted date/time string. |

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns the set of locales for which DateFormats are installed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.html#!>!` | the set of locales for which DateFormats are installed. |

### getBooleanAttribute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBooleanAttribute(key: DateFormat.BooleanAttribute!): Boolean
```

Returns the current value for the specified BooleanAttribute for this instance if attribute is missing false is returned.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.BooleanAttribute`

### getCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCalendar(): Calendar!
```

Returns the calendar associated with this date/time formatter.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#!` | the calendar associated with this date/time formatter. |

### getContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContext(type: DisplayContext.Type!): DisplayContext!
```

**\[icu\]** Get the formatter's DisplayContext value for the specified DisplayContext.Type, such as CAPITALIZATION.

| Parameters ||
|---|---|
| `type` | [DisplayContext.Type](../android/icu/text/DisplayContext.Type.md)!: the DisplayContext.Type whose value to return |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext!` | the current DisplayContext setting for the specified type |

### getDateInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateInstance(): DateFormat!
```

Returns the date formatter with the default formatting style for the default `FORMAT` locale.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a date formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getDateInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateInstance(
    cal: Calendar!, 
    dateStyle: Int
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object for the default locale that can be used to format dates in the calendar system specified by `cal`.

<br />

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date format is desired. |
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of date format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |

### getDateInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateInstance(
    cal: Calendar!, 
    dateStyle: Int, 
    locale: ULocale!
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates in the calendar system specified by `cal`.

<br />

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date format is desired. |
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of date format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: The locale for which the date format is desired. |
| --- | --- |

### getDateInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateInstance(
    cal: Calendar!, 
    dateStyle: Int, 
    locale: Locale!
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates in the calendar system specified by `cal`.

<br />

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date format is desired. |
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of date format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the date format is desired. |
| --- | --- |

### getDateInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateInstance(style: Int): DateFormat!
```

Returns the date formatter with the given formatting style for the default `FORMAT` locale.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given formatting style. For example, SHORT for "M/d/yy" in the US locale. As currently implemented, relative date formatting only affects a limited range of calendar days before or after the current date, based on the CLDR \<field type="day"\>/\<relative\> data: For example, in English, "Yesterday", "Today", and "Tomorrow". Outside of this range, relative dates are formatted using the corresponding non-relative style. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a date formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getDateInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateInstance(
    style: Int, 
    locale: ULocale!
): DateFormat!
```

Returns the date formatter with the given formatting style for the given locale.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given formatting style. For example, SHORT for "M/d/yy" in the US locale. As currently implemented, relative date formatting only affects a limited range of calendar days before or after the current date, based on the CLDR \<field type="day"\>/\<relative\> data: For example, in English, "Yesterday", "Today", and "Tomorrow". Outside of this range, relative dates are formatted using the corresponding non-relative style. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: the given ulocale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a date formatter. |

### getDateInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateInstance(
    style: Int, 
    aLocale: Locale!
): DateFormat!
```

Returns the date formatter with the given formatting style for the given locale.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given formatting style. For example, SHORT for "M/d/yy" in the US locale. As currently implemented, relative date formatting only affects a limited range of calendar days before or after the current date, based on the CLDR \<field type="day"\>/\<relative\> data: For example, in English, "Yesterday", "Today", and "Tomorrow". Outside of this range, relative dates are formatted using the corresponding non-relative style. |
| `aLocale` | [Locale](../java.util/Locale.md)!: the given locale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a date formatter. |

### getDateTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateTimeInstance(): DateFormat!
```

Returns the date/time formatter with the default formatting style for the default `FORMAT` locale.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a date/time formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getDateTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateTimeInstance(
    cal: Calendar!, 
    dateStyle: Int, 
    timeStyle: Int
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object for the default locale that can be used to format dates and times in the calendar system specified by `cal`.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of date format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of time format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| --- | --- |

**See Also**

### getDateTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateTimeInstance(
    cal: Calendar!, 
    dateStyle: Int, 
    timeStyle: Int, 
    locale: ULocale!
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of date format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of time format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| --- | --- |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: The locale for which the date/time format is desired. |

**See Also**

### getDateTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateTimeInstance(
    cal: Calendar!, 
    dateStyle: Int, 
    timeStyle: Int, 
    locale: Locale!
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of date format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of time format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| --- | --- |
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the date/time format is desired. |

**See Also**

### getDateTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateTimeInstance(
    dateStyle: Int, 
    timeStyle: Int
): DateFormat!
```

Returns the date/time formatter with the given date and time formatting styles for the default `FORMAT` locale.

| Parameters ||
|---|---|
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given date formatting style. For example, SHORT for "M/d/yy" in the US locale. As currently implemented, relative date formatting only affects a limited range of calendar days before or after the current date, based on the CLDR \<field type="day"\>/\<relative\> data: For example, in English, "Yesterday", "Today", and "Tomorrow". Outside of this range, relative dates are formatted using the corresponding non-relative style. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time formatting style. For example, SHORT for "h:mm a" in the US locale. Relative time styles are not currently supported, and behave just like the corresponding non-relative style. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a date/time formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getDateTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateTimeInstance(
    dateStyle: Int, 
    timeStyle: Int, 
    locale: ULocale!
): DateFormat!
```

Returns the date/time formatter with the given formatting styles for the given locale.

| Parameters ||
|---|---|
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given date formatting style. As currently implemented, relative date formatting only affects a limited range of calendar days before or after the current date, based on the CLDR \<field type="day"\>/\<relative\> data: For example, in English, "Yesterday", "Today", and "Tomorrow". Outside of this range, relative dates are formatted using the corresponding non-relative style. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time formatting style. Relative time styles are not currently supported, and behave just like the corresponding non-relative style. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: the given ulocale. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a date/time formatter. |

### getDateTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDateTimeInstance(
    dateStyle: Int, 
    timeStyle: Int, 
    aLocale: Locale!
): DateFormat!
```

Returns the date/time formatter with the given formatting styles for the given locale.

| Parameters ||
|---|---|
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given date formatting style. As currently implemented, relative date formatting only affects a limited range of calendar days before or after the current date, based on the CLDR \<field type="day"\>/\<relative\> data: For example, in English, "Yesterday", "Today", and "Tomorrow". Outside of this range, relative dates are formatted using the corresponding non-relative style. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time formatting style. Relative time styles are not currently supported, and behave just like the corresponding non-relative style. |
| `aLocale` | [Locale](../java.util/Locale.md)!: the given locale. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a date/time formatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(): DateFormat!
```

Returns a default date/time formatter that uses the SHORT style for both the date and the time.

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(cal: Calendar!): DateFormat!
```

Returns a default date/time formatter that uses the SHORT style for both the date and the time.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |

### getInstance

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    cal: Calendar!, 
    locale: ULocale!
): DateFormat!
```

Returns a date/time formatter that uses the SHORT style for both the date and the time.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: The locale for which the date/time format is desired. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    cal: Calendar!, 
    locale: Locale!
): DateFormat!
```

Returns a date/time formatter that uses the SHORT style for both the date and the time.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the date/time format is desired. |

### getInstanceForSkeleton

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstanceForSkeleton(
    cal: Calendar!, 
    skeleton: String!, 
    locale: ULocale!
): DateFormat!
```

**\[icu\]** Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: The locale for which the date/time format is desired. |
| --- | --- |

### getInstanceForSkeleton

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstanceForSkeleton(
    cal: Calendar!, 
    skeleton: String!, 
    locale: Locale!
): DateFormat!
```

**\[icu\]** Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the date/time format is desired. |
| --- | --- |

### getInstanceForSkeleton

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstanceForSkeleton(skeleton: String!): DateFormat!
```

**\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the default locale.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |

### getInstanceForSkeleton

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstanceForSkeleton(
    skeleton: String!, 
    locale: ULocale!
): DateFormat!
```

**\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the given locale.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: The locale for which the date/time format is desired. |

### getInstanceForSkeleton

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstanceForSkeleton(
    skeleton: String!, 
    locale: Locale!
): DateFormat!
```

**\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the given locale.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the date/time format is desired. |

### getNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNumberFormat(): NumberFormat!
```

Returns the number formatter which this date/time formatter uses to format and parse a time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | the number formatter which this date/time formatter uses. |

### getPatternInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getPatternInstance(
    cal: Calendar!, 
    skeleton: String!, 
    locale: ULocale!
): DateFormat!
```

**\[icu\]** Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: The locale for which the date/time format is desired. |
| --- | --- |

### getPatternInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getPatternInstance(
    cal: Calendar!, 
    skeleton: String!, 
    locale: Locale!
): DateFormat!
```

**\[icu\]** Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the calendar system specified by `cal`. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a date/time format is desired. |
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the date/time format is desired. |
| --- | --- |

### getPatternInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getPatternInstance(skeleton: String!): DateFormat!
```

**\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the default locale. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |

### getPatternInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getPatternInstance(
    skeleton: String!, 
    locale: ULocale!
): DateFormat!
```

**\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the given locale. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: The locale for which the date/time format is desired. |

### getPatternInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getPatternInstance(
    skeleton: String!, 
    locale: Locale!
): DateFormat!
```

**\[icu\]** Returns a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format dates and times in the given locale. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton that selects the fields to be formatted. (Uses the `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator`.) This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String`, etc. |
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the date/time format is desired. |

### getTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTimeInstance(): DateFormat!
```

Gets the time formatter with the default formatting style for the default `FORMAT` locale.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a time formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTimeInstance(
    cal: Calendar!, 
    timeStyle: Int
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format times in the calendar system specified by `cal`.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a time format is desired. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of time format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |

**See Also**

### getTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTimeInstance(
    cal: Calendar!, 
    timeStyle: Int, 
    locale: ULocale!
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format times in the calendar system specified by `cal`.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a time format is desired. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of time format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: The locale for which the time format is desired. |
| --- | --- |

**See Also**

### getTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTimeInstance(
    cal: Calendar!, 
    timeStyle: Int, 
    locale: Locale!
): DateFormat!
```

Creates a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#` object that can be used to format times in the calendar system specified by `cal`.

| Parameters ||
|---|---|
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar system for which a time format is desired. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of time format desired. This can be `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int`, etc. |
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the time format is desired. |
| --- | --- |

**See Also**

### getTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTimeInstance(style: Int): DateFormat!
```

Returns the time formatter with the given formatting style for the default `FORMAT` locale.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given formatting style. For example, SHORT for "h:mm a" in the US locale. Relative time styles are not currently supported, and behave just like the corresponding non-relative style. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a time formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTimeInstance(
    style: Int, 
    locale: ULocale!
): DateFormat!
```

Returns the time formatter with the given formatting style for the given locale.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given formatting style. For example, SHORT for "h:mm a" in the US locale. Relative time styles are not currently supported, and behave just like the corresponding non-relative style. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: the given ulocale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a time formatter. |

### getTimeInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTimeInstance(
    style: Int, 
    aLocale: Locale!
): DateFormat!
```

Returns the time formatter with the given formatting style for the given locale.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given formatting style. For example, SHORT for "h:mm a" in the US locale. Relative time styles are not currently supported, and behave just like the corresponding non-relative style. |
| `aLocale` | [Locale](../java.util/Locale.md)!: the given locale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#!` | a time formatter. |

### getTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeZone(): TimeZone!
```

Returns the time zone.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!` | the time zone associated with the calendar of DateFormat. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Overrides hashCode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isCalendarLenient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCalendarLenient(): Boolean
```

Returns whether date/time parsing in the encapsulated Calendar object is lenient.

### isLenient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLenient(): Boolean
```

Returns whether both date/time parsing in the encapsulated Calendar object and DateFormat whitespace \& numeric processing is lenient.

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parse(text: String!): Date!
```

Parses a date/time string. For example, a time text "07/10/96 4:5 PM, PDT" will be parsed into a Date that is equivalent to Date(837039928046). Parsing begins at the beginning of the string and proceeds as far as possible. Assuming no parse errors were encountered, this function doesn't return any information about how much of the string was consumed by the parsing. If you need that information, use a version of parse() that takes a ParsePosition.

By default, parsing is lenient: If the input is not in the form used by this object's format method but can still be parsed as a date, then the parse succeeds. Clients may insist on strict adherence to the format by calling setLenient(false).

Note that the normal date formats associated with some calendars - such as the Chinese lunar calendar - do not specify enough fields to enable dates to be parsed unambiguously. In the case of the Chinese lunar calendar, while the year within the current 60-year cycle is specified, the number of such cycles since the start date of the calendar (in the ERA field of the Calendar object) is not normally part of the format, and parsing may assume the wrong era. For cases such as this it is recommended that clients parse using the parse method that takes a Calendar with the Calendar passed in set to the current date, or to a date within the era/cycle that should be assumed if absent in the format.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The date/time string to be parsed |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | A Date, or null if the input could not be parsed |

| Exceptions ||
|---|---|
| `java.text.ParseException` | If the given string cannot be parsed as a date. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parse(kotlin.String,%20java.text.ParsePosition)`

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun parse(
    text: String!, 
    cal: Calendar!, 
    pos: ParsePosition!
): Unit
```

Parses a date/time string according to the given parse position. For example, a time text "07/10/96 4:5 PM, PDT" will be parsed into a Calendar that is equivalent to Date(837039928046). Before calling this method the caller should initialize the calendar in one of two ways (unless existing field information is to be kept): (1) clear the calendar, or (2) set the calendar to the current date (or to any date whose fields should be used to supply values that are missing in the parsed date). For example, Chinese calendar dates do not normally provide an era/cycle; in this case the calendar that is passed in should be set to a date within the era that should be assumed, normally the current era.

By default, parsing is lenient: If the input is not in the form used by this object's format method but can still be parsed as a date, then the parse succeeds. Clients may insist on strict adherence to the format by calling setLenient(false).

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The date/time string to be parsed |
| `cal` | [Calendar](../android.icu.util/Calendar.md)!: The calendar set on input to the date and time to be used for missing values in the date/time string being parsed, and set on output to the parsed date/time. In general, this should be initialized before calling this method - either cleared or set to the current date, depending on desired behavior. If this parse fails, the calendar may still have been modified. When the calendar type is different from the internal calendar held by this DateFormat instance, calendar field values will be parsed based on the internal calendar initialized with the time and the time zone taken from this calendar, then the parse result (time in milliseconds and time zone) will be set back to this calendar. |
| `pos` | [ParsePosition](../java.text/ParsePosition.md)!: On input, the position at which to start parsing; on output, the position at which parsing terminated, or the start position if the parse failed. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setLenient(kotlin.Boolean)`

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parse(
    text: String!, 
    pos: ParsePosition!
): Date!
```

Parses a date/time string according to the given parse position. For example, a time text "07/10/96 4:5 PM, PDT" will be parsed into a Date that is equivalent to Date(837039928046).

By default, parsing is lenient: If the input is not in the form used by this object's format method but can still be parsed as a date, then the parse succeeds. Clients may insist on strict adherence to the format by calling setLenient(false).

Note that the normal date formats associated with some calendars - such as the Chinese lunar calendar - do not specify enough fields to enable dates to be parsed unambiguously. In the case of the Chinese lunar calendar, while the year within the current 60-year cycle is specified, the number of such cycles since the start date of the calendar (in the ERA field of the Calendar object) is not normally part of the format, and parsing may assume the wrong era. For cases such as this it is recommended that clients parse using the parse method that takes a Calendar with the Calendar passed in set to the current date, or to a date within the era/cycle that should be assumed if absent in the format.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The date/time string to be parsed |
| `pos` | [ParsePosition](../java.text/ParsePosition.md)!: On input, the position at which to start parsing; on output, the position at which parsing terminated, or the start position if the parse failed. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | A Date, or null if the input could not be parsed |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setLenient(kotlin.Boolean)`

### parseObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseObject(
    source: String!, 
    pos: ParsePosition!
): Any!
```

Parses a date/time string into an Object. This convenience method simply calls parse(String, ParsePosition).

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A `String`, part of which should be parsed. |
| `pos` | [ParsePosition](../java.text/ParsePosition.md)!: A `ParsePosition` object with index and error index information as described above. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | An `Object` parsed from the string. In case of error, returns null. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `source` or `pos` is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parse(kotlin.String,%20java.text.ParsePosition)`

### setBooleanAttribute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBooleanAttribute(
    key: DateFormat.BooleanAttribute!, 
    value: Boolean
): DateFormat!
```

Sets a boolean attribute for this instance. Aspects of DateFormat leniency are controlled by boolean attributes.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.BooleanAttribute`

### setCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCalendar(newCalendar: Calendar!): Unit
```

Sets the calendar to be used by this date format. Initially, the default calendar for the specified or default locale is used.

| Parameters ||
|---|---|
| `newCalendar` | [Calendar](../android.icu.util/Calendar.md)!: the new Calendar to be used by the date format |

### setCalendarLenient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCalendarLenient(lenient: Boolean): Unit
```

Specifies whether date/time parsing in the encapsulated Calendar object should be lenient. With lenient parsing, the parser may use heuristics to interpret inputs that do not precisely match this object's format. Without lenient parsing, inputs must match this object's format more closely.

| Parameters ||
|---|---|
| `lenient` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): when true, Calendar parsing is lenient |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#setLenient(kotlin.Boolean)`

### setContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContext(context: DisplayContext!): Unit
```

**\[icu\]** Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE.

| Parameters ||
|---|---|
| `context` | [DisplayContext](DisplayContext.md)!: The DisplayContext value to set. |

### setLenient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLenient(lenient: Boolean): Unit
```

Specifies whether date/time parsing is to be lenient. With lenient parsing, the parser may use heuristics to interpret inputs that do not precisely match this object's format. Without lenient parsing, inputs must match this object's format more closely. 

**Note:** ICU 53 introduced finer grained control of leniency (and added new control points) making the preferred method a combination of setCalendarLenient() \& setBooleanAttribute() calls. This method supports prior functionality but may not support all future leniency control \& behavior of DateFormat. For control of pre 53 leniency, Calendar and DateFormat whitespace \& numeric tolerance, this method is safe to use. However, mixing leniency control via this method and modification of the newer attributes via setBooleanAttribute() may produce undesirable results.

| Parameters ||
|---|---|
| `lenient` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True specifies date/time interpretation to be lenient. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#setLenient(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setBooleanAttribute(android.icu.text.DateFormat.BooleanAttribute,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setCalendarLenient(kotlin.Boolean)`

### setNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNumberFormat(newNumberFormat: NumberFormat!): Unit
```

Sets the number formatter.

| Parameters ||
|---|---|
| `newNumberFormat` | [NumberFormat](NumberFormat.md)!: the given new NumberFormat. |

### setTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTimeZone(zone: TimeZone!): Unit
```

Sets the time zone for the calendar of this DateFormat object.

| Parameters ||
|---|---|
| `zone` | [TimeZone](../android.icu.util/TimeZone.md)!: the given new time zone. |

## Properties

### calendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var calendar: Calendar!
```

The calendar that `DateFormat` uses to produce the time field values needed to implement date and time formatting. Subclasses should initialize this to a calendar appropriate for the locale associated with this `DateFormat`.

### numberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var numberFormat: NumberFormat!
```

The number formatter that `DateFormat` uses to format numbers in dates and times. Subclasses should initialize this to a number format appropriate for the locale associated with this `DateFormat`.
