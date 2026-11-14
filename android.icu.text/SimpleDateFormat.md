# SimpleDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleDateFormat

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/SimpleDateFormat "View this page in Java") 

```
open class SimpleDateFormat : DateFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format.html#) ||||
| | ↳ | [android.icu.text.UFormat](https://developer.android.com/reference/kotlin/android/icu/text/UFormat) |||
| | | ↳ | [android.icu.text.DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) ||
| | | | ↳ | [android.icu.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#) |

**\[icu enhancement\]** ICU's replacement for [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

`SimpleDateFormat`is a concrete class for formatting and parsing dates in a locale-sensitive manner. It allows for formatting (date -\> text), parsing (text -\> date), and normalization.

Clients are encouraged to create a date-time formatter using`DateFormat.getDateInstance()`,`DateFormat.getDateInstance()`, or`DateFormat.getDateTimeInstance()`rather than explicitly constructing an instance of`SimpleDateFormat`. This way, the client is guaranteed to get an appropriate formatting pattern for whatever locale the program is running in. If the client needs more control, they should consider using`DateFormat.getInstanceForSkeleton()`. However, if the client needs something more unusual than the default patterns in the locales, he can construct a`SimpleDateFormat`directly and give it an appropriate pattern (or use one of the factory methods on DateFormat and modify the pattern after the fact with`toPattern()`and`applyPattern()`. For more information on using these methods, see [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat).

**Date and Time Patterns:**

Date and time formats are specified by*date and time pattern* strings. The full syntax for date and time patterns can be found at<https://unicode.org/reports/tr35/tr35-dates.html#Date_Format_Patterns>.

Within date and time pattern strings, all unquoted ASCII letters \[A-Za-z\] are reserved as pattern letters representing calendar fields. Some of the most commonly used pattern letters are:

| Sym. | No. | Example | Description |
|------|------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| G | 1..3 | AD | Era - Replaced with the Era string for the current date. One to three letters for the abbreviated form, four letters for the long (wide) form, five for the narrow form. |
| y | 1..n | 1996 | Year. Normally the length specifies the padding, but for two letters it also specifies the maximum length. Example: <br /> | Year | y | yy | yyy | yyyy | yyyyy | |----------|-------|----|-------|-------|-------| | AD 1 | 1 | 01 | 001 | 0001 | 00001 | | AD 12 | 12 | 12 | 012 | 0012 | 00012 | | AD 123 | 123 | 23 | 123 | 0123 | 00123 | | AD 1234 | 1234 | 34 | 1234 | 1234 | 01234 | | AD 12345 | 12345 | 45 | 12345 | 12345 | 12345 | <br /> |
| Q | 1..2 | 02 | Quarter - Use one or two for the numerical quarter, three for the abbreviation, or four for the full (wide) name (five for the narrow name is not yet supported). |
| Q | 3 | Q2 | Quarter - Use one or two for the numerical quarter, three for the abbreviation, or four for the full (wide) name (five for the narrow name is not yet supported). |
| Q | 4 | 2nd quarter | Quarter - Use one or two for the numerical quarter, three for the abbreviation, or four for the full (wide) name (five for the narrow name is not yet supported). |
| M | 1..2 | 09 | Month - Use one or two for the numerical month, three for the abbreviation, four for the full (wide) name, or five for the narrow name. With two ("MM"), the month number is zero-padded if necessary (e.g. "08"). |
| M | 3 | Sep | Month - Use one or two for the numerical month, three for the abbreviation, four for the full (wide) name, or five for the narrow name. With two ("MM"), the month number is zero-padded if necessary (e.g. "08"). |
| M | 4 | September | Month - Use one or two for the numerical month, three for the abbreviation, four for the full (wide) name, or five for the narrow name. With two ("MM"), the month number is zero-padded if necessary (e.g. "08"). |
| M | 5 | S | Month - Use one or two for the numerical month, three for the abbreviation, four for the full (wide) name, or five for the narrow name. With two ("MM"), the month number is zero-padded if necessary (e.g. "08"). |
| d | 1..2 | 1 | Date - Day of the month. Use "d" to show the minimum number of digits, or "dd" to always show two digits (zero-padding if necessary, e.g. "08"). |
| E | 1..3 | Tue | Day of week - Use one through three letters for the short day, four for the full (wide) name, five for the narrow name, or six for the short name. |
| E | 4 | Tuesday | Day of week - Use one through three letters for the short day, four for the full (wide) name, five for the narrow name, or six for the short name. |
| E | 5 | T | Day of week - Use one through three letters for the short day, four for the full (wide) name, five for the narrow name, or six for the short name. |
| E | 6 | Tu | Day of week - Use one through three letters for the short day, four for the full (wide) name, five for the narrow name, or six for the short name. |
| a | 1 | AM | AM or PM |
| h | 1..2 | 11 | Hour \[1-12\]. When used in skeleton data or in a skeleton passed in an API for flexible data pattern generation, it should match the 12-hour-cycle format preferred by the locale (h or K); it should not match a 24-hour-cycle format (H or k). Use hh for zero padding. |
| H | 1..2 | 13 | Hour \[0-23\]. When used in skeleton data or in a skeleton passed in an API for flexible data pattern generation, it should match the 24-hour-cycle format preferred by the locale (H or k); it should not match a 12-hour-cycle format (h or K). Use HH for zero padding. |
| m | 1..2 | 59 | Minute. Use "m" to show the minimum number of digits, or "mm" to always show two digits (zero-padding if necessary, e.g. "08").. |
| s | 1..2 | 12 | Second. Use "s" to show the minimum number of digits, or "ss" to always show two digits (zero-padding if necessary, e.g. "08"). |
| z | 1..3 | PDT | Time zone. The*short specific non-location format* . Where that is unavailable, falls back to the*short localized GMT format*("O"). |
| z | 4 | Pacific Daylight Time | The*long specific non-location format* . Where that is unavailable, falls back to the*long localized GMT format*("OOOO"). |
| v | 1 | PT | Time zone. The*short generic non-location format* . Where that is unavailable, falls back to the*generic location format* ("VVVV"), then the*short localized GMT format*as the final fallback. |
| v | 4 | Pacific Time | The*long generic non-location format* . Where that is unavailable, falls back to*generic location format*("VVVV"). |

Any characters in the pattern that are not in the ranges of \['a'..'z'\] and \['A'..'Z'\] will be treated as quoted text. For instance, characters like ':', '.', ' ', '#' and '@' will appear in the resulting time text even they are not embraced within single quotes.

A pattern containing any invalid pattern letter will result in a thrown exception during formatting or parsing.

**Examples Using the US Locale:** 

```kotlin
Format Pattern                         Result
  --------------                         -------
  "yyyy.MM.dd G 'at' HH:mm:ss vvvv" ->>  1996.07.10 AD at 15:08:56 Pacific Time
  "EEE, MMM d, ''yy"                ->>  Wed, July 10, '96
  "h:mm a"                          ->>  12:08 PM
  "hh 'o''clock' a, zzzz"           ->>  12 o'clock PM, Pacific Daylight Time
  "K:mm a, vvv"                     ->>  0:00 PM, PT
  "yyyyy.MMMMM.dd GGG hh:mm aaa"    ->>  01996.July.10 AD 12:08 PM
  
```
**Code Sample:** 

```kotlin
SimpleTimeZone pdt = new SimpleTimeZone(-8 * 60 * 60 * 1000, "PST");
  pdt.setStartRule(Calendar.APRIL, 1, Calendar.SUNDAY, 2*60*60*1000);
  pdt.setEndRule(Calendar.OCTOBER, -1, Calendar.SUNDAY, 2*60*60*1000);
  <br>// Format the current time.
  SimpleDateFormat formatter
      = new SimpleDateFormat ("yyyy.MM.dd G 'at' hh:mm:ss a zzz");
  Date currentTime_1 = new Date();
  String dateString = formatter.format(currentTime_1);
  <br>// Parse the previous string back into a Date.
  ParsePosition pos = new ParsePosition(0);
  Date currentTime_2 = formatter.parse(dateString, pos);
  
```
In the example, the time value`currentTime_2`obtained from parsing will be equal to`currentTime_1`. However, they may not be equal if the am/pm marker 'a' is left out from the format pattern while the "hour in am/pm" pattern symbol is used. This information loss can happen when formatting the time in PM.

When parsing a date string using the abbreviated year pattern ("yy"), SimpleDateFormat must interpret the abbreviated year relative to some century. It does this by adjusting dates to be within 80 years before and 20 years after the time the SimpleDateFormat instance is created. For example, using a pattern of "MM/dd/yy" and a SimpleDateFormat instance created on Jan 1, 1997, the string "01/11/12" would be interpreted as Jan 11, 2012 while the string "05/04/64" would be interpreted as May 4, 1964. During parsing, only strings consisting of exactly two digits, as defined by [android.icu.lang.UCharacter#isDigit(int)](https://developer.android.com/reference/kotlin/android/icu/lang/UCharacter.html#isDigit(kotlin.Int)), will be parsed into the default century. Any other numeric string, such as a one digit string, a three or more digit string, or a two digit string that isn't all digits (for example, "-1"), is interpreted literally. So "01/02/3" or "01/02/003" are parsed, using the same pattern, as Jan 2, 3 AD. Likewise, "01/02/-3" is parsed as Jan 2, 4 BC.

If the year pattern does not have exactly two 'y' characters, the year is interpreted literally, regardless of the number of digits. So using the pattern "MM/dd/yyyy", "01/11/12" parses to Jan 11, 12 A.D.

When numeric fields abut one another directly, with no intervening delimiter characters, they constitute a run of abutting numeric fields. Such runs are parsed specially. For example, the format "HHmmss" parses the input text "123456" to 12:34:56, parses the input text "12345" to 1:23:45, and fails to parse "1234". In other words, the leftmost field of the run is flexible, while the others keep a fixed width. If the parse fails anywhere in the run, then the leftmost field is shortened by one character, and the entire run is parsed again. This is repeated until either the parse succeeds or the leftmost field is one character in length. If the parse still fails at that point, the parse of the run fails.

For time zones that have no names, use strings GMT+hours:minutes or GMT-hours:minutes.

The calendar defines what is the first day of the week, the first week of the year, whether hours are zero based or not (0 vs 12 or 24), and the time zone. There is one common decimal format to handle all the numbers; the digit count is handled programmatically according to the pattern.

### Synchronization

Date formats are not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Inherited constants ||
|---|---|
| From class [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) |----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBR_GENERIC_TZ](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_GENERIC_TZ:kotlin.String) <br /> **\[icu\]** Constant for*generic non-location format*, abbreviated if possible, such as PT; used in combinations date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBR_MONTH](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with abbreviated month. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBR_MONTH_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with abbreviated month and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBR_MONTH_WEEKDAY_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_MONTH_WEEKDAY_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with abbreviated month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBR_QUARTER](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_QUARTER:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with abbreviated quarter. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBR_SPECIFIC_TZ](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_SPECIFIC_TZ:kotlin.String) <br /> **\[icu\]** Constant for*specific non-location format*, abbreviated if possible, such as PDT; used in combinations date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBR_UTC_TZ](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_UTC_TZ:kotlin.String) <br /> **\[icu\]** Constant for*localized GMT/UTC format*, such as GMT+8:00 or HPG-8:00; used in combinations date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBR_WEEKDAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ABBR_WEEKDAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with abbreviated weekday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AM_PM_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#AM_PM_FIELD:kotlin.Int) <br /> FieldPosition selector for 'a' field alignment, corresponding to the [Calendar.AM_PM](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#AM_PM:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AM_PM_MIDNIGHT_NOON_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#AM_PM_MIDNIGHT_NOON_FIELD:kotlin.Int) <br /> **\[icu\]**FieldPosition selector for 'b' field alignment. No related Calendar field. This displays the fixed day period (am/pm/midnight/noon). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATE_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DATE_FIELD:kotlin.Int) <br /> FieldPosition selector for 'd' field alignment, corresponding to the [Calendar.DATE](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DATE:kotlin.Int) field. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with day. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DAY_OF_WEEK_FIELD:kotlin.Int) <br /> FieldPosition selector for 'E' field alignment, corresponding to the [Calendar.DAY_OF_WEEK](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK_IN_MONTH_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DAY_OF_WEEK_IN_MONTH_FIELD:kotlin.Int) <br /> FieldPosition selector for 'F' field alignment, corresponding to the [Calendar.DAY_OF_WEEK_IN_MONTH](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK_IN_MONTH:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_YEAR_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DAY_OF_YEAR_FIELD:kotlin.Int) <br /> FieldPosition selector for 'D' field alignment, corresponding to the [Calendar.DAY_OF_YEAR](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_YEAR:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DEFAULT:kotlin.Int) <br /> Constant for default style pattern. Its value is MEDIUM. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOW_LOCAL_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#DOW_LOCAL_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'e' field alignment, corresponding to the [Calendar.DOW_LOCAL](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DOW_LOCAL:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERA_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#ERA_FIELD:kotlin.Int) <br /> FieldPosition selector for 'G' field alignment, corresponding to the [Calendar.ERA](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ERA:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTENDED_YEAR_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#EXTENDED_YEAR_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'u' field alignment, corresponding to the [Calendar.EXTENDED_YEAR](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#EXTENDED_YEAR:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLEXIBLE_DAY_PERIOD_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#FLEXIBLE_DAY_PERIOD_FIELD:kotlin.Int) <br /> **\[icu\]**FieldPosition selector for 'B' field alignment. No related Calendar field. This displays the flexible day period. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRACTIONAL_SECOND_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#FRACTIONAL_SECOND_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'S' field alignment, corresponding to the [Calendar.MILLISECOND](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MILLISECOND:kotlin.Int) field. Note: Time formats that use 'S' can display a maximum of three significant digits for fractional seconds, corresponding to millisecond resolution and a fractional seconds sub-pattern of SSS. If the sub-pattern is S or SS, the fractional seconds value will be truncated (not rounded) to the number of display places specified. If the fractional seconds sub-pattern is longer than SSS, the additional display places will be filled with zeros. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FULL](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#FULL:kotlin.Int) <br /> Constant for full style pattern. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [GENERIC_TZ](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#GENERIC_TZ:kotlin.String) <br /> **\[icu\]** Constant for*generic non-location format*, such as Pacific Time; used in combinations date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HOUR](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with hour, with the locale's preferred hour format (12 or 24). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR0_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR0_FIELD:kotlin.Int) <br /> FieldPosition selector for 'K' field alignment, corresponding to the [Calendar.HOUR](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR:kotlin.Int) field. HOUR0_FIELD is used for the zero-based 12-hour clock. For example, 11:30 PM + 1 hour results in 00:30 AM. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR1_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR1_FIELD:kotlin.Int) <br /> FieldPosition selector for 'h' field alignment, corresponding to the [Calendar.HOUR](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR:kotlin.Int) field. HOUR1_FIELD is used for the one-based 12-hour clock. For example, 11:30 PM + 1 hour results in 12:30 AM. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HOUR24](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR24:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with hour in 24-hour presentation. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HOUR24_MINUTE](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR24_MINUTE:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with hour and minute in 24-hour presentation. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HOUR24_MINUTE_SECOND](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR24_MINUTE_SECOND:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with hour, minute, and second in 24-hour presentation. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HOUR_MINUTE](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR_MINUTE:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with hour and minute, with the locale's preferred hour format (12 or 24). Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HOUR_MINUTE_SECOND](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR_MINUTE_SECOND:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with hour, minute, and second, with the locale's preferred hour format (12 or 24). Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR_OF_DAY0_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR_OF_DAY0_FIELD:kotlin.Int) <br /> FieldPosition selector for 'H' field alignment, corresponding to the [Calendar.HOUR_OF_DAY](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR_OF_DAY:kotlin.Int) field. HOUR_OF_DAY0_FIELD is used for the zero-based 24-hour clock. For example, 23:59 + 01:00 results in 00:59. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR_OF_DAY1_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#HOUR_OF_DAY1_FIELD:kotlin.Int) <br /> FieldPosition selector for 'k' field alignment, corresponding to the [Calendar.HOUR_OF_DAY](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#HOUR_OF_DAY:kotlin.Int) field. HOUR_OF_DAY1_FIELD is used for the one-based 24-hour clock. For example, 23:59 + 01:00 results in 24:59. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JULIAN_DAY_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#JULIAN_DAY_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'g' field alignment, corresponding to the [Calendar.JULIAN_DAY](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#JULIAN_DAY:kotlin.Int) field. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LOCATION_TZ](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#LOCATION_TZ:kotlin.String) <br /> **\[icu\]** Constant for*generic location format*, such as Los Angeles Time; used in combinations date + time + zone, or time + zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#LONG:kotlin.Int) <br /> Constant for long style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIUM](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MEDIUM:kotlin.Int) <br /> Constant for medium style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MILLISECONDS_IN_DAY_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MILLISECONDS_IN_DAY_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'A' field alignment, corresponding to the [Calendar.MILLISECONDS_IN_DAY](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MILLISECONDS_IN_DAY:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MILLISECOND_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MILLISECOND_FIELD:kotlin.Int) <br /> Alias for FRACTIONAL_SECOND_FIELD. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MINUTE](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MINUTE:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with minute. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINUTE_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MINUTE_FIELD:kotlin.Int) <br /> FieldPosition selector for 'm' field alignment, corresponding to the [Calendar.MINUTE](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MINUTE:kotlin.Int) field. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MINUTE_SECOND](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MINUTE_SECOND:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with minute and second. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MONTH](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with month. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MONTH_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with long month and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONTH_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_FIELD:kotlin.Int) <br /> FieldPosition selector for 'M' field alignment, corresponding to the [Calendar.MONTH](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int) field. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MONTH_WEEKDAY_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#MONTH_WEEKDAY_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONE](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#NONE:kotlin.Int) <br /> **\[icu\]**Constant for empty style pattern. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUM_MONTH](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#NUM_MONTH:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with numeric month. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUM_MONTH_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#NUM_MONTH_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with numeric month and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUM_MONTH_WEEKDAY_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#NUM_MONTH_WEEKDAY_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with numeric month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUARTER](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#QUARTER:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with quarter. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUARTER_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#QUARTER_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'Q' field alignment, corresponding to the [Calendar.MONTH](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int) field. This displays the quarter. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE:kotlin.Int) <br /> **\[icu\]**Constant for relative style mask. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_DEFAULT:kotlin.Int) <br /> **\[icu\]**Constant for relative default style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_FULL](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_FULL:kotlin.Int) <br /> **\[icu\]**Constant for relative full style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_LONG](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_LONG:kotlin.Int) <br /> **\[icu\]**Constant for relative style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_MEDIUM](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_MEDIUM:kotlin.Int) <br /> **\[icu\]**Constant for relative style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_SHORT](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#RELATIVE_SHORT:kotlin.Int) <br /> **\[icu\]**Constant for relative style pattern. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SECOND](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SECOND:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with second. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECOND_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SECOND_FIELD:kotlin.Int) <br /> FieldPosition selector for 's' field alignment, corresponding to the [Calendar.SECOND](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#SECOND:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SHORT:kotlin.Int) <br /> Constant for short style pattern. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SPECIFIC_TZ](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#SPECIFIC_TZ:kotlin.String) <br /> **\[icu\]** Constant for*specific non-location format*, such as Pacific Daylight Time; used in combinations date + time + zone, or time + zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDALONE_DAY_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#STANDALONE_DAY_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'c' field alignment, corresponding to the [Calendar.DAY_OF_WEEK](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DAY_OF_WEEK:kotlin.Int) field. This displays the stand alone day name, if available. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDALONE_MONTH_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#STANDALONE_MONTH_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'L' field alignment, corresponding to the [Calendar.MONTH](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int) field. This displays the stand alone month name, if available. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDALONE_QUARTER_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#STANDALONE_QUARTER_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'q' field alignment, corresponding to the [Calendar.MONTH](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#MONTH:kotlin.Int) field. This displays the stand alone quarter, if available. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_FIELD:kotlin.Int) <br /> FieldPosition selector for 'z' field alignment, corresponding to the [Calendar.ZONE_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int) and [Calendar.DST_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int) fields. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_GENERIC_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_GENERIC_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'v' field alignment, corresponding to the [Calendar.ZONE_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int) and [Calendar.DST_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int) fields. This displays the generic zone name, if available. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_ISO_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_ISO_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'X' field alignment, corresponding to the [Calendar.ZONE_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int) and [Calendar.DST_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int) fields. This displays the ISO 8601 local time offset format or UTC indicator ("Z"). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_ISO_LOCAL_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_ISO_LOCAL_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'x' field alignment, corresponding to the [Calendar.ZONE_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int) and [Calendar.DST_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int) fields. This displays the ISO 8601 local time offset format. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_LOCALIZED_GMT_OFFSET_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_LOCALIZED_GMT_OFFSET_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'O' field alignment, corresponding to the [Calendar.ZONE_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int) and [Calendar.DST_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int) fields. This displays the localized GMT format. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_RFC_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_RFC_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'Z' field alignment, corresponding to the [Calendar.ZONE_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int) and [Calendar.DST_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int) fields. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_SPECIAL_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#TIMEZONE_SPECIAL_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'V' field alignment, corresponding to the [Calendar.ZONE_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#ZONE_OFFSET:kotlin.Int) and [Calendar.DST_OFFSET](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#DST_OFFSET:kotlin.Int) fields. This displays the fallback timezone name when VVVV is specified, and the short standard or daylight timezone name ignoring commonlyUsed when a single V is specified. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WEEKDAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#WEEKDAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with weekday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_MONTH_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#WEEK_OF_MONTH_FIELD:kotlin.Int) <br /> FieldPosition selector for 'W' field alignment, corresponding to the [Calendar.WEEK_OF_MONTH](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#WEEK_OF_MONTH:kotlin.Int) field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_YEAR_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#WEEK_OF_YEAR_FIELD:kotlin.Int) <br /> FieldPosition selector for 'w' field alignment, corresponding to the [Calendar.WEEK_OF_YEAR](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#WEEK_OF_YEAR:kotlin.Int) field. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_ABBR_MONTH](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_MONTH:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year and abbreviated month. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_ABBR_MONTH_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_MONTH_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year, abbreviated month, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_ABBR_MONTH_WEEKDAY_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_MONTH_WEEKDAY_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year, abbreviated month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_ABBR_QUARTER](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_ABBR_QUARTER:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year and abbreviated quarter. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YEAR_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_FIELD:kotlin.Int) <br /> FieldPosition selector for 'y' field alignment, corresponding to the [Calendar.YEAR](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR:kotlin.Int) field. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_MONTH](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_MONTH:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year and month. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_MONTH_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_MONTH_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year, month, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_MONTH_WEEKDAY_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_MONTH_WEEKDAY_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year, month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YEAR_NAME_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_NAME_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'U' field alignment, corresponding to the [Calendar.YEAR](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR:kotlin.Int) field. This displays the cyclic year name, if available. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_NUM_MONTH](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_NUM_MONTH:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year and numeric month. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_NUM_MONTH_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_NUM_MONTH_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year, numeric month, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_NUM_MONTH_WEEKDAY_DAY](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_NUM_MONTH_WEEKDAY_DAY:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year, numeric month, weekday, and day. Used in combinations date + time, date + time + zone, or time + zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_QUARTER](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_QUARTER:kotlin.String) <br /> **\[icu\]**Constant for date skeleton with year and quarter. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YEAR_WOY_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#YEAR_WOY_FIELD:kotlin.Int) <br /> **\[icu\]** FieldPosition selector for 'Y' field alignment, corresponding to the [Calendar.YEAR_WOY](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#YEAR_WOY:kotlin.Int) field. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#SimpleDateFormat())`()` Constructs a SimpleDateFormat using the default pattern for the default`FORMAT`locale. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#SimpleDateFormat(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a SimpleDateFormat using the given pattern in the default`FORMAT`locale. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20android.icu.text.DateFormatSymbols))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `formatData:` ` [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols)!`)` Constructs a SimpleDateFormat using the given pattern and locale-specific symbol data. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20android.icu.util.ULocale))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `loc:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Constructs a SimpleDateFormat using the given pattern and locale. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20kotlin.String,%20android.icu.util.ULocale))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `override:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `loc:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Constructs a SimpleDateFormat using the given pattern , override and locale. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20java.util.Locale))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `loc:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Constructs a SimpleDateFormat using the given pattern and locale. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyLocalizedPattern](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#applyLocalizedPattern(kotlin.String))`(`pat:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Apply the given localized pattern string to this date format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#applyPattern(kotlin.String))`(`pat:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Apply the given unlocalized pattern string to this date format. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#clone())`()` Overrides Cloneable |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Override equals. |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#format(android.icu.util.Calendar,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` Formats a date or time, which is the standard millis since January 1, 1970, 00:00:00 GMT. |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)! | [formatToCharacterIterator](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#formatToCharacterIterator(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Format the object to an attributed string, and return the corresponding iterator Overrides superclass method. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [get2DigitYearStart](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#get2DigitYearStart())`()` Returns the beginning date of the 100-year period 2-digit years are interpreted as being within. |
| open [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols)! | [getDateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#getDateFormatSymbols())`()` Gets the date/time formatting data. |
| open [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)! | [getNumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#getNumberFormat(kotlin.Char))`(`field:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` give the NumberFormat used for the field like 'y'(year) and 'M'(year) |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat)! | [getTimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#getTimeZoneFormat())`()` **\[icu\]**Gets the time zone formatter which this date/time formatter uses to format and parse a time zone. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#hashCode())`()` Override hashCode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#parse(kotlin.String,%20android.icu.util.Calendar,%20java.text.ParsePosition))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `parsePos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!`)` Overrides DateFormat |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set2DigitYearStart](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#set2DigitYearStart(java.util.Date))`(`startDate:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Sets the 100-year period 2-digit years will be interpreted as being in to begin on the date the user specifies. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#setContext(android.icu.text.DisplayContext))`(`context:` ` [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!`)` **\[icu\]**Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#setDateFormatSymbols(android.icu.text.DateFormatSymbols))`(`newFormatSymbols:` ` [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols)!`)` Allows you to set the date/time formatting data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#setNumberFormat(android.icu.text.NumberFormat))`(`newNumberFormat:` ` [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!`)` Overrides superclass method and This method also clears per field NumberFormat instances previously set by [setNumberFormat(java.lang.String,android.icu.text.NumberFormat)](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#setNumberFormat(kotlin.String,%20android.icu.text.NumberFormat)) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#setNumberFormat(kotlin.String,%20android.icu.text.NumberFormat))`(`fields:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `overrideNF:` ` [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!`)` allow the user to set the NumberFormat for several fields It can be a single field like: "y"(year) or "M"(month) It can be several field combined together: "yMd"(year, month and date) Note: 1 symbol field is enough for multiple symbol fields (so "y" will override "yy", "yyy") If the field is not numeric, then override has no effect (like "MMM" will use abbreviation, not numerical field) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#setTimeZoneFormat(android.icu.text.TimeZoneFormat))`(`tzfmt:` ` [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat)!`)` **\[icu\]**Allows you to set the time zone formatter. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLocalizedPattern](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#toLocalizedPattern())`()` Return a localized pattern string describing this date format. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#toPattern())`()` Return a pattern string describing this date format. |

| Protected methods ||
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols)! | [getSymbols](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#getSymbols())`()` Method for subclasses to access the DateFormatSymbols. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [matchQuarterString](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#matchQuarterString(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array,%20android.icu.util.Calendar))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`)` Attempt to match the text at a given position against an array of quarter strings. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [matchString](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#matchString(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Array,%20android.icu.util.Calendar))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`)` Attempt to match the text at a given position against an array of strings. |
| open [DateFormat.Field](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.Field)! | [patternCharToDateFormatField](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#patternCharToDateFormatField(kotlin.Char))`(`ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns a DateFormat. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [subFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#subFormat(kotlin.Char,%20kotlin.Int,%20kotlin.Int,%20java.text.FieldPosition,%20android.icu.text.DateFormatSymbols,%20android.icu.util.Calendar))`(`ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `beginOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`, `fmtData:` ` [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`)` Formats a single field, given its pattern character. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [subParse](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#subParse(kotlin.String,%20kotlin.Int,%20kotlin.Char,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.BooleanArray,%20android.icu.util.Calendar))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ch:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obeyCount:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `allowNegative:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `ambiguousYear:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`)` Protected method that converts one field of the input string into a numeric field value in`cal`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [zeroPaddingNumber](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#zeroPaddingNumber(kotlin.Long,%20kotlin.Int,%20kotlin.Int))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Formats a number with the specified minimum and maximum number of digits. |

| Inherited functions ||
|---|---|
| From class [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `fieldPosition:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` <br /> Formats a time object into a time string. Examples of time objects are a time value expressed in milliseconds and a Date object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(java.util.Date))`(`date:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` <br /> Formats a Date into a date/time string. <br /> | | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#format(java.util.Date,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`date:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `fieldPosition:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` <br /> Formats a Date into a date/time string. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!>! | [getAvailableLocales](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getAvailableLocales())`()` <br /> Returns the set of locales for which DateFormats are installed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBooleanAttribute](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getBooleanAttribute(android.icu.text.DateFormat.BooleanAttribute))`(`key:` ` [DateFormat.BooleanAttribute](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.BooleanAttribute)!`)` <br /> Returns the current value for the specified BooleanAttribute for this instance if attribute is missing false is returned. <br /> | | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)! | [getCalendar](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getCalendar())`()` <br /> Returns the calendar associated with this date/time formatter. <br /> | | [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)! | [getContext](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getContext(android.icu.text.DisplayContext.Type))`(`type:` ` [DisplayContext.Type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type)!`)` <br /> **\[icu\]**Get the formatter's DisplayContext value for the specified DisplayContext.Type, such as CAPITALIZATION. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance())`()` <br /> Returns the date formatter with the default formatting style for the default`FORMAT`locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(android.icu.util.Calendar,%20kotlin.Int))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object for the default locale that can be used to format dates in the calendar system specified by`cal`. <br /> <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(android.icu.util.Calendar,%20kotlin.Int,%20android.icu.util.ULocale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates in the calendar system specified by`cal`. <br /> <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(android.icu.util.Calendar,%20kotlin.Int,%20java.util.Locale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates in the calendar system specified by`cal`. <br /> <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(kotlin.Int))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the date formatter with the given formatting style for the default`FORMAT`locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(kotlin.Int,%20android.icu.util.ULocale))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> Returns the date formatter with the given formatting style for the given locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> Returns the date formatter with the given formatting style for the given locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance())`()` <br /> Returns the date/time formatter with the default formatting style for the default`FORMAT`locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20kotlin.Int))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object for the default locale that can be used to format dates and times in the calendar system specified by`cal`. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20kotlin.Int,%20android.icu.util.ULocale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the calendar system specified by`cal`. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20kotlin.Int,%20java.util.Locale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the calendar system specified by`cal`. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the date/time formatter with the given date and time formatting styles for the default`FORMAT`locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int,%20android.icu.util.ULocale))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> Returns the date/time formatter with the given formatting styles for the given locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getDateTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int,%20java.util.Locale))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> Returns the date/time formatter with the given formatting styles for the given locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstance())`()` <br /> Returns a default date/time formatter that uses the SHORT style for both the date and the time. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstance(android.icu.util.Calendar))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`)` <br /> Returns a default date/time formatter that uses the SHORT style for both the date and the time. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstance(android.icu.util.Calendar,%20android.icu.util.ULocale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> Returns a date/time formatter that uses the SHORT style for both the date and the time. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstance(android.icu.util.Calendar,%20java.util.Locale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> Returns a date/time formatter that uses the SHORT style for both the date and the time. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstanceForSkeleton](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(android.icu.util.Calendar,%20kotlin.String,%20android.icu.util.ULocale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> **\[icu\]** Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the calendar system specified by`cal`. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstanceForSkeleton](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(android.icu.util.Calendar,%20kotlin.String,%20java.util.Locale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> **\[icu\]** Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the calendar system specified by`cal`. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstanceForSkeleton](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(kotlin.String))`(`skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> **\[icu\]** Returns a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the default locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstanceForSkeleton](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(kotlin.String,%20android.icu.util.ULocale))`(`skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> **\[icu\]** Returns a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the given locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getInstanceForSkeleton](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getInstanceForSkeleton(kotlin.String,%20java.util.Locale))`(`skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> **\[icu\]** Returns a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the given locale. <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)! | [getNumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getNumberFormat())`()` <br /> Returns the number formatter which this date/time formatter uses to format and parse a time. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getPatternInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(android.icu.util.Calendar,%20kotlin.String,%20android.icu.util.ULocale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> **\[icu\]** Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the calendar system specified by`cal`. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getPatternInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(android.icu.util.Calendar,%20kotlin.String,%20java.util.Locale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> **\[icu\]** Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the calendar system specified by`cal`. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getPatternInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(kotlin.String))`(`skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> **\[icu\]** Returns a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the default locale. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getPatternInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(kotlin.String,%20android.icu.util.ULocale))`(`skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> **\[icu\]** Returns a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the given locale. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getPatternInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getPatternInstance(kotlin.String,%20java.util.Locale))`(`skeleton:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> **\[icu\]** Returns a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format dates and times in the given locale. The getInstanceForSkeleton methods are preferred over the getPatternInstance methods. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance())`()` <br /> Gets the time formatter with the default formatting style for the default`FORMAT`locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(android.icu.util.Calendar,%20kotlin.Int))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format times in the calendar system specified by`cal`. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20android.icu.util.ULocale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format times in the calendar system specified by`cal`. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(android.icu.util.Calendar,%20kotlin.Int,%20java.util.Locale))`(`cal:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> Creates a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) object that can be used to format times in the calendar system specified by`cal`. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(kotlin.Int))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the time formatter with the given formatting style for the default`FORMAT`locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(kotlin.Int,%20android.icu.util.ULocale))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` <br /> Returns the time formatter with the given formatting style for the given locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [getTimeInstance](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` <br /> Returns the time formatter with the given formatting style for the given locale. <br /> | | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)! | [getTimeZone](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#getTimeZone())`()` <br /> Returns the time zone. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCalendarLenient](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#isCalendarLenient())`()` <br /> Returns whether date/time parsing in the encapsulated Calendar object is lenient. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLenient](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#isLenient())`()` <br /> Returns whether both date/time parsing in the encapsulated Calendar object and DateFormat whitespace \& numeric processing is lenient. <br /> | | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [parse](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parse(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Parses a date/time string. For example, a time text "07/10/96 4:5 PM, PDT" will be parsed into a Date that is equivalent to Date(837039928046). Parsing begins at the beginning of the string and proceeds as far as possible. Assuming no parse errors were encountered, this function doesn't return any information about how much of the string was consumed by the parsing. If you need that information, use a version of parse() that takes a ParsePosition. By default, parsing is lenient: If the input is not in the form used by this object's format method but can still be parsed as a date, then the parse succeeds. Clients may insist on strict adherence to the format by calling setLenient(false). Note that the normal date formats associated with some calendars - such as the Chinese lunar calendar - do not specify enough fields to enable dates to be parsed unambiguously. In the case of the Chinese lunar calendar, while the year within the current 60-year cycle is specified, the number of such cycles since the start date of the calendar (in the ERA field of the Calendar object) is not normally part of the format, and parsing may assume the wrong era. For cases such as this it is recommended that clients parse using the parse method that takes a Calendar with the Calendar passed in set to the current date, or to a date within the era/cycle that should be assumed if absent in the format. <br /> | | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [parse](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parse(kotlin.String,%20java.text.ParsePosition))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!`)` <br /> Parses a date/time string according to the given parse position. For example, a time text "07/10/96 4:5 PM, PDT" will be parsed into a Date that is equivalent to Date(837039928046). By default, parsing is lenient: If the input is not in the form used by this object's format method but can still be parsed as a date, then the parse succeeds. Clients may insist on strict adherence to the format by calling setLenient(false). Note that the normal date formats associated with some calendars - such as the Chinese lunar calendar - do not specify enough fields to enable dates to be parsed unambiguously. In the case of the Chinese lunar calendar, while the year within the current 60-year cycle is specified, the number of such cycles since the start date of the calendar (in the ERA field of the Calendar object) is not normally part of the format, and parsing may assume the wrong era. For cases such as this it is recommended that clients parse using the parse method that takes a Calendar with the Calendar passed in set to the current date, or to a date within the era/cycle that should be assumed if absent in the format. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#parseObject(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!`)` <br /> Parses a date/time string into an Object. This convenience method simply calls parse(String, ParsePosition). <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)! | [setBooleanAttribute](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setBooleanAttribute(android.icu.text.DateFormat.BooleanAttribute,%20kotlin.Boolean))`(`key:` ` [DateFormat.BooleanAttribute](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.BooleanAttribute)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets a boolean attribute for this instance. Aspects of DateFormat leniency are controlled by boolean attributes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCalendar](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setCalendar(android.icu.util.Calendar))`(`newCalendar:` ` [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!`)` <br /> Sets the calendar to be used by this date format. Initially, the default calendar for the specified or default locale is used. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCalendarLenient](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setCalendarLenient(kotlin.Boolean))`(`lenient:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Specifies whether date/time parsing in the encapsulated Calendar object should be lenient. With lenient parsing, the parser may use heuristics to interpret inputs that do not precisely match this object's format. Without lenient parsing, inputs must match this object's format more closely. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLenient](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setLenient(kotlin.Boolean))`(`lenient:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Specifies whether date/time parsing is to be lenient. With lenient parsing, the parser may use heuristics to interpret inputs that do not precisely match this object's format. Without lenient parsing, inputs must match this object's format more closely. **Note:**ICU 53 introduced finer grained control of leniency (and added new control points) making the preferred method a combination of setCalendarLenient() \& setBooleanAttribute() calls. This method supports prior functionality but may not support all future leniency control \& behavior of DateFormat. For control of pre 53 leniency, Calendar and DateFormat whitespace \& numeric tolerance, this method is safe to use. However, mixing leniency control via this method and modification of the newer attributes via setBooleanAttribute() may produce undesirable results. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeZone](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#setTimeZone(android.icu.util.TimeZone))`(`zone:` ` [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)!`)` <br /> Sets the time zone for the calendar of this DateFormat object. <br /> | ||

| Inherited properties ||
|---|---|
| From class [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) |-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)! | [calendar](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#calendar:android.icu.util.Calendar) <br /> The calendar that`DateFormat`uses to produce the time field values needed to implement date and time formatting. Subclasses should initialize this to a calendar appropriate for the locale associated with this`DateFormat`. <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)! | [numberFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat#numberFormat:android.icu.text.NumberFormat) <br /> The number formatter that`DateFormat`uses to format numbers in dates and times. Subclasses should initialize this to a number format appropriate for the locale associated with this`DateFormat`. <br /> | ||

## Public constructors

### SimpleDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat()
```

Constructs a SimpleDateFormat using the default pattern for the default`FORMAT`locale.**Note:**Not all locales support SimpleDateFormat; for full generality, use the factory methods in the DateFormat class. 
**See Also**

- [android.icu.text.DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat)
- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### SimpleDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat(pattern: String!)
```

Constructs a SimpleDateFormat using the given pattern in the default`FORMAT`locale.**Note:**Not all locales support SimpleDateFormat; for full generality, use the factory methods in the DateFormat class. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### SimpleDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat(
    pattern: String!, 
    formatData: DateFormatSymbols!)
```

Constructs a SimpleDateFormat using the given pattern and locale-specific symbol data. Warning: uses default`FORMAT`locale for digits! 

### SimpleDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat(
    pattern: String!, 
    loc: ULocale!)
```

Constructs a SimpleDateFormat using the given pattern and locale.**Note:**Not all locales support SimpleDateFormat; for full generality, use the factory methods in the DateFormat class. 

### SimpleDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat(
    pattern: String!, 
    override: String!, 
    loc: ULocale!)
```

Constructs a SimpleDateFormat using the given pattern , override and locale.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The pattern to be used |
| `override` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The override string. A numbering system override string can take one of the following forms: 1). If just a numbering system name is specified, it applies to all numeric fields in the date format pattern. 2). To specify an alternate numbering system on a field by field basis, use the field letters from the pattern followed by an = sign, followed by the numbering system name. For example, to specify that just the year be formatted using Hebrew digits, use the override "y=hebr". Multiple overrides can be specified in a single string by separating them with a semi-colon. For example, the override string "m=thai;y=deva" would format using Thai digits for the month and Devanagari digits for the year. |
| `loc` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:The locale to be used |

### SimpleDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat(
    pattern: String!, 
    loc: Locale!)
```

Constructs a SimpleDateFormat using the given pattern and locale.**Note:**Not all locales support SimpleDateFormat; for full generality, use the factory methods in the DateFormat class.

## Public methods

### applyLocalizedPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyLocalizedPattern(pat: String!): Unit
```

Apply the given localized pattern string to this date format. 

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(pat: String!): Unit
```

Apply the given unlocalized pattern string to this date format. 

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Override equals.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    cal: Calendar!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats a date or time, which is the standard millis since January 1, 1970, 00:00:00 GMT.

Example: using the US locale: "yyyy.MM.dd G 'at' HH:mm:ss zzz" -\>\> 1996.07.10 AD at 15:08:56 PDT

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!:the calendar whose date-time value is to be formatted into a date-time string |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!:where the new date-time text is to be appended |
| `fieldPosition` | keeps track of the position of the field within the returned string. On input: an alignment field, if desired. On output: the offsets of the alignment field. For example, given a time text "1996.07.10 AD at 15:08:56 PDT", if the given fieldPosition is DateFormat.YEAR_FIELD, the begin index and end index of fieldPosition will be set to 0 and 4, respectively. Notice that if the same time field appears more than once in a pattern, the fieldPosition will be set for the first occurrence of that time field. For instance, formatting a Date to the time string "1 PM PDT (Pacific Daylight Time)" using the pattern "h a z (zzzz)" and the alignment field DateFormat.TIMEZONE_FIELD, the begin index and end index of fieldPosition will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character 'z'. |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!:the formatting position. On input: an alignment field, if desired. On output: the offsets of the alignment field. |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | the formatted date-time string. |

**See Also**

- [android.icu.text.DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) 

### formatToCharacterIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatToCharacterIterator(obj: Any!): AttributedCharacterIterator!
```

Format the object to an attributed string, and return the corresponding iterator Overrides superclass method.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object to format |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)! | `AttributedCharacterIterator`describing the formatted value. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.NullPointerException` | if obj is null. |
| `java.lang.IllegalArgumentException` | when the Format cannot format the given object. |

### get2DigitYearStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get2DigitYearStart(): Date!
```

Returns the beginning date of the 100-year period 2-digit years are interpreted as being within.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | the start of the 100-year period into which two digit years are parsed |

### getDateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDateFormatSymbols(): DateFormatSymbols!
```

Gets the date/time formatting data.

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols)! | a copy of the date-time formatting data associated with this date-time formatter. |

### getNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumberFormat(field: Char): NumberFormat!
```

give the NumberFormat used for the field like 'y'(year) and 'M'(year)

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `field` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the field the user wants |

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)! | override NumberFormat used for the field |

### getTimeZoneFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimeZoneFormat(): TimeZoneFormat!
```

**\[icu\]**Gets the time zone formatter which this date/time formatter uses to format and parse a time zone.

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat)! | the time zone formatter which this date/time formatter uses. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Override hashCode. Generates the hash code for the SimpleDateFormat object

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    text: String!, 
    cal: Calendar!, 
    parsePos: ParsePosition!
): Unit
```

Overrides DateFormat

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The date/time string to be parsed |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!:The calendar set on input to the date and time to be used for missing values in the date/time string being parsed, and set on output to the parsed date/time. In general, this should be initialized before calling this method - either cleared or set to the current date, depending on desired behavior. If this parse fails, the calendar may still have been modified. When the calendar type is different from the internal calendar held by this DateFormat instance, calendar field values will be parsed based on the internal calendar initialized with the time and the time zone taken from this calendar, then the parse result (time in milliseconds and time zone) will be set back to this calendar. |
| `pos` | On input, the position at which to start parsing; on output, the position at which parsing terminated, or the start position if the parse failed. |

**See Also**

- [android.icu.text.DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) 

### set2DigitYearStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set2DigitYearStart(startDate: Date!): Unit
```

Sets the 100-year period 2-digit years will be interpreted as being in to begin on the date the user specifies.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startDate` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:During parsing, two digit years will be placed in the range`startDate`to`startDate + 100 years`. |

### setContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContext(context: DisplayContext!): Unit
```

**\[icu\]**Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE. Note: For getContext, see DateFormat.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!:The DisplayContext value to set. |

### setDateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDateFormatSymbols(newFormatSymbols: DateFormatSymbols!): Unit
```

Allows you to set the date/time formatting data.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| `newFormatSymbols` | [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols)!:the new symbols |

### setNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNumberFormat(newNumberFormat: NumberFormat!): Unit
```

Overrides superclass method and This method also clears per field NumberFormat instances previously set by [setNumberFormat(java.lang.String,android.icu.text.NumberFormat)](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#setNumberFormat(kotlin.String,%20android.icu.text.NumberFormat))

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| `newNumberFormat` | [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!:the given new NumberFormat. |

### setNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNumberFormat(
    fields: String!, 
    overrideNF: NumberFormat!
): Unit
```

allow the user to set the NumberFormat for several fields It can be a single field like: "y"(year) or "M"(month) It can be several field combined together: "yMd"(year, month and date) Note: 1 symbol field is enough for multiple symbol fields (so "y" will override "yy", "yyy") If the field is not numeric, then override has no effect (like "MMM" will use abbreviation, not numerical field)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| `fields` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the fields to override |
| `overrideNF` | [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!:the NumbeferFormat used |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | when the fields contain invalid field |

### setTimeZoneFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTimeZoneFormat(tzfmt: TimeZoneFormat!): Unit
```

**\[icu\]**Allows you to set the time zone formatter.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `tzfmt` | [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat)!:the new time zone formatter |

### toLocalizedPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLocalizedPattern(): String!
```

Return a localized pattern string describing this date format.

**Note:** This implementation depends on [DateFormatSymbols.getLocalPatternChars()](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols#getLocalPatternChars())to get localized format pattern characters. ICU does not include localized pattern character data, therefore, unless user sets localized pattern characters manually, this method returns the same result as [toPattern()](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat#toPattern()). 

### toPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPattern(): String!
```

Return a pattern string describing this date format.

## Protected methods

### getSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getSymbols(): DateFormatSymbols!
```

Method for subclasses to access the DateFormatSymbols. 

### matchQuarterString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun matchQuarterString(
    text: String!, 
    start: Int, 
    field: Int, 
    data: Array<String!>!, 
    cal: Calendar!
): Int
```

Attempt to match the text at a given position against an array of quarter strings. Since multiple strings in the array may match (for example, if the array contains "a", "ab", and "abc", all will match the input string "abcd") the longest match is returned. As a side effect, the given field of`cal`is set to the index of the best match, if there is one.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the time text being parsed. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):where to start parsing. |
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the date field being parsed. |
| `data` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the string array to parsed. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the new start position if matching succeeded; a negative number indicating matching failure, otherwise. As a side effect, sets the`cal`field`field`to the index of the best match, if matching succeeded. |

### matchString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun matchString(
    text: String!, 
    start: Int, 
    field: Int, 
    data: Array<String!>!, 
    cal: Calendar!
): Int
```

Attempt to match the text at a given position against an array of strings. Since multiple strings in the array may match (for example, if the array contains "a", "ab", and "abc", all will match the input string "abcd") the longest match is returned. As a side effect, the given field of`cal`is set to the index of the best match, if there is one.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the time text being parsed. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):where to start parsing. |
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the date field being parsed. |
| `data` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the string array to parsed. |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!: |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the new start position if matching succeeded; a negative number indicating matching failure, otherwise. As a side effect, sets the`cal`field`field`to the index of the best match, if matching succeeded. |

### patternCharToDateFormatField

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun patternCharToDateFormatField(ch: Char): DateFormat.Field!
```

Returns a DateFormat.Field constant associated with the specified format pattern character.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The pattern character |

| Return ||
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [DateFormat.Field](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.Field)! | DateFormat.Field associated with the pattern character |

### subFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun subFormat(
    ch: Char, 
    count: Int, 
    beginOffset: Int, 
    pos: FieldPosition!, 
    fmtData: DateFormatSymbols!, 
    cal: Calendar!
): String!
```

Formats a single field, given its pattern character. Subclasses may override this method in order to modify or add formatting capabilities.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the pattern character |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of times ch is repeated in the pattern |
| `beginOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset of the output string at the start of this field; used to set pos when appropriate |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!:receives the position of a field, when appropriate |
| `fmtData` | [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols)!:the symbols for this formatter |

### subParse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun subParse(
    text: String!, 
    start: Int, 
    ch: Char, 
    count: Int, 
    obeyCount: Boolean, 
    allowNegative: Boolean, 
    ambiguousYear: BooleanArray!, 
    cal: Calendar!
): Int
```

Protected method that converts one field of the input string into a numeric field value in`cal`. Returns -start (for ParsePosition) if failed. Subclasses may override this method to modify or add parsing capabilities.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the time text to be parsed. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):where to start parsing. |
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the pattern character for the date field text to be parsed. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the count of a pattern character. |
| `obeyCount` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, then the next field directly abuts this one, and we should use the count to know when to stop parsing. |
| `ambiguousYear` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:return parameter; upon return, if ambiguousYear\[0\] is true, then a two-digit year was parsed and may need to be readjusted. |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.html#)!: |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the new start position if matching succeeded; a negative number indicating matching failure, otherwise. As a side effect, set the appropriate field of`cal`with the parsed value. |

### zeroPaddingNumber

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun zeroPaddingNumber(
    value: Long, 
    minDigits: Int, 
    maxDigits: Int
): String!
```

Formats a number with the specified minimum and maximum number of digits.
