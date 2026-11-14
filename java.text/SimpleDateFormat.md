# SimpleDateFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleDateFormat

```
open class SimpleDateFormat : DateFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format) |||
| | ↳ | [java.text.DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) ||
| | | ↳ | [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#) |

is a concrete class for formatting and parsing dates in a locale-sensitive manner. It allows for formatting (date → text), parsing (text → date), and normalization.

`SimpleDateFormat`allows you to start by choosing any user-defined patterns for date-time formatting. However, you are encouraged to create a date-time formatter with either`getTimeInstance`,`getDateInstance`, or`getDateTimeInstance`in`DateFormat`. Each of these class methods can return a date/time formatter initialized with a default format pattern. You may modify the format pattern using the`applyPattern`methods as desired. For more information on using these methods, see [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat).

## Date and Time Patterns

Date and time formats are specified by*date and time pattern* strings. Within date and time pattern strings, unquoted letters from`'A'`to`'Z'`and from`'a'`to`'z'`are interpreted as pattern letters representing the components of a date or time string. Text can be quoted using single quotes (`'`) to avoid interpretation.`"''"`represents a single quote. All other characters are not interpreted; they're simply copied into the output string during formatting or matched against the input string during parsing.

The following pattern letters are defined (all other characters from`'A'`to`'Z'`and from`'a'`to`'z'`are reserved):

| Letter | Date or Time Component | Presentation | Examples | Supported (API Levels) |
| `G` | Era designator | [Text](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#text) | `AD` | 1+ |
| `y` | Year | [Year](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#year) | `1996`;`96` | 1+ |
| `Y` | Week year | [Year](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#year) | `2009`;`09` | 24+ |
| `M` | Month in year (context sensitive) | [Month](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#month) | `July`;`Jul`;`07` | 1+ |
| `L` | Month in year (standalone form) | [Month](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#month) | `July`;`Jul`;`07` | TBD |
| `w` | Week in year | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `27` | 1+ |
| `W` | Week in month | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `2` | 1+ |
| `D` | Day in year | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `189` | 1+ |
| `d` | Day in month | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `10` | 1+ |
| `F` | Day of week in month | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `2` | 1+ |
| `E` | Day name in week | [Text](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#text) | `Tuesday`;`Tue` | 1+ |
| `u` | Day number of week (1 = Monday, ..., 7 = Sunday) | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `1` | 24+ |
| `a` | Am/pm marker | [Text](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#text) | `PM` | 1+ |
| `H` | Hour in day (0-23) | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `0` | 1+ |
| `k` | Hour in day (1-24) | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `24` | 1+ |
| `K` | Hour in am/pm (0-11) | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `0` | 1+ |
| `h` | Hour in am/pm (1-12) | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `12` | 1+ |
| `m` | Minute in hour | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `30` | 1+ |
| `s` | Second in minute | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `55` | 1+ |
| `S` | Millisecond | [Number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number) | `978` | 1+ |
| `z` | Time zone | [General time zone](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#timezone) | `Pacific Standard Time`;`PST`;`GMT-08:00` | 1+ |
| `Z` | Time zone | [RFC 822 time zone](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#rfc822timezone) | `-0800` | 1+ |
| `X` | Time zone | [ISO 8601 time zone](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#iso8601timezone) | `-08`;`-0800`;`-08:00` | 24+ |
|--------|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------|------------------------|

Pattern letters are usually repeated, as their number determines the exact presentation:

- **Text:**For formatting, if the number of pattern letters is 4 or more, the full form is used; otherwise a short or abbreviated form is used if available. For parsing, both forms are accepted, independent of the number of pattern letters.
- **Number:**For formatting, the number of pattern letters is the minimum number of digits, and shorter numbers are zero-padded to this amount. For parsing, the number of pattern letters is ignored unless it's needed to separate two adjacent fields.
- **Year:** If the formatter's [Calendar](https://developer.android.com/reference/kotlin/java/text/DateFormat#getCalendar())is the Gregorian calendar, the following rules are applied.
 - For formatting, if the number of pattern letters is 2, the year is truncated to 2 digits; otherwise it is interpreted as a [number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number).
 - For parsing, if the number of pattern letters is more than 2, the year is interpreted literally, regardless of the number of digits. So using the pattern "MM/dd/yyyy", "01/11/12" parses to Jan 11, 12 A.D.
 - For parsing with the abbreviated year pattern ("y" or "yy"),`SimpleDateFormat`must interpret the abbreviated year relative to some century. It does this by adjusting dates to be within 80 years before and 20 years after the time the`SimpleDateFormat`instance is created. For example, using a pattern of "MM/dd/yy" and a`SimpleDateFormat`instance created on Jan 1, 1997, the string "01/11/12" would be interpreted as Jan 11, 2012 while the string "05/04/64" would be interpreted as May 4, 1964. During parsing, only strings consisting of exactly two digits, as defined by [Character.isDigit(char)](https://developer.android.com/reference/kotlin/java/lang/Character.html#isDigit(kotlin.Char)), will be parsed into the default century. Any other numeric string, such as a one digit string, a three or more digit string, or a two digit string that isn't all digits (for example, "-1"), is interpreted literally. So "01/02/3" or "01/02/003" are parsed, using the same pattern, as Jan 2, 3 AD. Likewise, "01/02/-3" is parsed as Jan 2, 4 BC.

 Otherwise, calendar system specific forms are applied. For both formatting and parsing, if the number of pattern letters is 4 or more, a calendar specific [long form](https://developer.android.com/reference/kotlin/java/util/Calendar.html#LONG:kotlin.Int) is used. Otherwise, a calendar specific [short or abbreviated form](https://developer.android.com/reference/kotlin/java/util/Calendar.html#SHORT:kotlin.Int) is used. 
 If week year`'Y'`is specified and the [calendar](https://developer.android.com/reference/kotlin/java/text/DateFormat#getCalendar())doesn't support any [week years](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#week_year), the calendar year (`'y'`) is used instead. The support of week years can be tested with a call to [getCalendar()](https://developer.android.com/reference/kotlin/java/text/DateFormat#getCalendar()). [isWeekDateSupported()](https://developer.android.com/reference/kotlin/java/util/Calendar.html#isWeekDateSupported()).
- **Month:** If the number of pattern letters is 3 or more, the month is interpreted as [text](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#text); otherwise, it is interpreted as a [number](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#number).
 - Letter*M* produces context-sensitive month names, such as the embedded form of names. Letter*M* is context-sensitive in the sense that when it is used in the standalone pattern, for example, "MMMM", it gives the standalone form of a month name and when it is used in the pattern containing other field(s), for example, "d MMMM", it gives the format form of a month name. For example, January in the Catalan language is "de gener" in the format form while it is "gener" in the standalone form. In this case, "MMMM" will produce "gener" and the month part of the "d MMMM" will produce "de gener". If a`DateFormatSymbols`has been set explicitly with constructor [SimpleDateFormat(java.lang.String,java.text.DateFormatSymbols)](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20java.text.DateFormatSymbols))or method [setDateFormatSymbols(java.text.DateFormatSymbols)](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#setDateFormatSymbols(java.text.DateFormatSymbols)), the month names given by the`DateFormatSymbols`are used.
 - Letter*L*produces the standalone form of month names.

 <br />

- **General time zone:** Time zones are interpreted as [text](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#text) if they have names. For time zones representing a GMT offset value, the following syntax is used: 

  ```kotlin
  <a id="GMTOffsetTimeZone"><i>GMTOffsetTimeZone:</i></a><code>GMT</code><i>Sign</i><i>Hours</i><code>:</code><i>Minutes</i><i>Sign:</i>one of
                <code>+ -</code><i>Hours:</i><i>Digit</i><i>Digit</i><i>Digit</i><i>Minutes:</i><i>Digit</i><i>Digit</i><i>Digit:</i>one of
                <code>0 1 2 3 4 5 6 7 8 9</code>
  ```
 *Hours* must be between 0 and 23, and*Minutes* must be between 00 and 59. The format is locale independent and digits must be taken from the Basic Latin block of the Unicode standard.

 For parsing, [RFC 822 time zones](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#rfc822timezone) are also accepted.
- **RFC 822 time zone:** For formatting, the RFC 822 4-digit time zone format is used: 

  ```kotlin
  <i>RFC822TimeZone:</i><i>Sign</i><i>TwoDigitHours</i><i>Minutes</i><i>TwoDigitHours:</i><i>Digit Digit</i>
  ```
 *TwoDigitHours* must be between 00 and 23. Other definitions are as for [general time zones](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#timezone).

 For parsing, [general time zones](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#timezone) are also accepted.
- **ISO 8601 Time zone:** The number of pattern letters designates the format for both formatting and parsing as follows: 

  ```kotlin
  <i>ISO8601TimeZone:</i><i>OneLetterISO8601TimeZone</i><i>TwoLetterISO8601TimeZone</i><i>ThreeLetterISO8601TimeZone</i><i>OneLetterISO8601TimeZone:</i><i>Sign</i><i>TwoDigitHours</i><code>Z</code><i>TwoLetterISO8601TimeZone:</i><i>Sign</i><i>TwoDigitHours</i><i>Minutes</i><code>Z</code><i>ThreeLetterISO8601TimeZone:</i><i>Sign</i><i>TwoDigitHours</i><code>:</code><i>Minutes</i><code>Z</code>
  ```
 Other definitions are as for [general time zones](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#timezone) or [RFC 822 time zones](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#rfc822timezone).

 For formatting, if the offset value from GMT is 0,`"Z"`is produced. If the number of pattern letters is 1, any fraction of an hour is ignored. For example, if the pattern is`"X"`and the time zone is`"GMT+05:30"`,`"+05"`is produced.

 For parsing, the letter`"Z"`is parsed as the UTC time zone designator (therefore`"09:30Z"`is parsed as`"09:30 UTC"`. [General time zones](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#timezone) are*not*accepted.

 If the number of`"X"`pattern letters is 4 or more (e.g.`XXXX`), [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) is thrown when constructing a`SimpleDateFormat`or [applying a](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#applyPattern(kotlin.String)).

`SimpleDateFormat`also supports*localized date and time pattern* strings. In these strings, the pattern letters described above may be replaced with other, locale dependent, pattern letters.`SimpleDateFormat`does not deal with the localization of text other than the pattern letters; that's up to the client of the class.

### Examples

The following examples show how date and time patterns are interpreted in the U.S. locale. The given date and time are 2001-07-04 12:08:56 local time in the U.S. Pacific Time time zone.

| Date and Time Pattern | Result |
| `"yyyy.MM.dd G 'at' HH:mm:ss z"` | `2001.07.04 AD at 12:08:56 PDT` |
| `"EEE, MMM d, ''yy"` | `Wed, Jul 4, '01` |
| `"h:mm a"` | `12:08 PM` |
| `"hh 'o''clock' a, zzzz"` | `12 o'clock PM, Pacific Daylight Time` |
| `"K:mm a, z"` | `0:08 PM, PDT` |
| `"yyyyy.MMMMM.dd GGG hh:mm aaa"` | `02001.July.04 AD 12:08 PM` |
| `"EEE, d MMM yyyy HH:mm:ss Z"` | `Wed, 4 Jul 2001 12:08:56 -0700` |
| `"yyMMddHHmmssZ"` | `010704120856-0700` |
| `"yyyy-MM-dd'T'HH:mm:ss.SSSZ"` | `2001-07-04T12:08:56.235-0700` |
| `"yyyy-MM-dd'T'HH:mm:ss.SSSXXX"` | `2001-07-04T12:08:56.235-07:00` |
| `"YYYY-'W'ww-u"` | `2001-W27-3` |
|----------------------------------|----------------------------------------|

### Synchronization

Date formats are not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Inherited constants ||
|---|---|
| From class [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AM_PM_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#AM_PM_FIELD:kotlin.Int) <br /> Useful constant for AM_PM field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATE_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#DATE_FIELD:kotlin.Int) <br /> Useful constant for DATE field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#DAY_OF_WEEK_FIELD:kotlin.Int) <br /> Useful constant for DAY_OF_WEEK field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK_IN_MONTH_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#DAY_OF_WEEK_IN_MONTH_FIELD:kotlin.Int) <br /> Useful constant for DAY_OF_WEEK_IN_MONTH field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_YEAR_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#DAY_OF_YEAR_FIELD:kotlin.Int) <br /> Useful constant for DAY_OF_YEAR field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT](https://developer.android.com/reference/kotlin/java/text/DateFormat#DEFAULT:kotlin.Int) <br /> Constant for default style pattern. Its value is MEDIUM. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERA_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#ERA_FIELD:kotlin.Int) <br /> Useful constant for ERA field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FULL](https://developer.android.com/reference/kotlin/java/text/DateFormat#FULL:kotlin.Int) <br /> Constant for full style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR0_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#HOUR0_FIELD:kotlin.Int) <br /> Useful constant for zero-based HOUR field alignment. Used in FieldPosition of date/time formatting. HOUR0_FIELD is used for the zero-based 12-hour clock. For example, 11:30 PM + 1 hour results in 00:30 AM. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR1_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#HOUR1_FIELD:kotlin.Int) <br /> Useful constant for one-based HOUR field alignment. Used in FieldPosition of date/time formatting. HOUR1_FIELD is used for the one-based 12-hour clock. For example, 11:30 PM + 1 hour results in 12:30 AM. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR_OF_DAY0_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#HOUR_OF_DAY0_FIELD:kotlin.Int) <br /> Useful constant for zero-based HOUR_OF_DAY field alignment. Used in FieldPosition of date/time formatting. HOUR_OF_DAY0_FIELD is used for the zero-based 24-hour clock. For example, 23:59 + 01:00 results in 00:59. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR_OF_DAY1_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#HOUR_OF_DAY1_FIELD:kotlin.Int) <br /> Useful constant for one-based HOUR_OF_DAY field alignment. Used in FieldPosition of date/time formatting. HOUR_OF_DAY1_FIELD is used for the one-based 24-hour clock. For example, 23:59 + 01:00 results in 24:59. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG](https://developer.android.com/reference/kotlin/java/text/DateFormat#LONG:kotlin.Int) <br /> Constant for long style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDIUM](https://developer.android.com/reference/kotlin/java/text/DateFormat#MEDIUM:kotlin.Int) <br /> Constant for medium style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MILLISECOND_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#MILLISECOND_FIELD:kotlin.Int) <br /> Useful constant for MILLISECOND field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINUTE_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#MINUTE_FIELD:kotlin.Int) <br /> Useful constant for MINUTE field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONTH_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#MONTH_FIELD:kotlin.Int) <br /> Useful constant for MONTH field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECOND_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#SECOND_FIELD:kotlin.Int) <br /> Useful constant for SECOND field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT](https://developer.android.com/reference/kotlin/java/text/DateFormat#SHORT:kotlin.Int) <br /> Constant for short style pattern. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIMEZONE_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#TIMEZONE_FIELD:kotlin.Int) <br /> Useful constant for TIMEZONE field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_MONTH_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#WEEK_OF_MONTH_FIELD:kotlin.Int) <br /> Useful constant for WEEK_OF_MONTH field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_YEAR_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#WEEK_OF_YEAR_FIELD:kotlin.Int) <br /> Useful constant for WEEK_OF_YEAR field alignment. Used in FieldPosition of date/time formatting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YEAR_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#YEAR_FIELD:kotlin.Int) <br /> Useful constant for YEAR field alignment. Used in FieldPosition of date/time formatting. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#SimpleDateFormat())`()` Constructs a`SimpleDateFormat`using the default pattern and date format symbols for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#SimpleDateFormat(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SimpleDateFormat`using the given pattern and the default date format symbols for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20java.text.DateFormatSymbols))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `formatSymbols:` ` [DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols)!`)` Constructs a`SimpleDateFormat`using the given pattern and date format symbols. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20java.util.Locale))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Constructs a`SimpleDateFormat`using the given pattern and the default date format symbols for the given locale. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyLocalizedPattern](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#applyLocalizedPattern(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Applies the given localized pattern string to this date format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#applyPattern(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Applies the given pattern string to this date format. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#clone())`()` Creates a copy of this`SimpleDateFormat`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the given object with this`SimpleDateFormat`for equality. |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [format](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#format(java.util.Date,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`date:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)`)` Formats the given`Date`into a date/time string and appends the result to the given`StringBuffer`. |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [formatToCharacterIterator](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#formatToCharacterIterator(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an Object producing an`AttributedCharacterIterator`. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [get2DigitYearStart](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#get2DigitYearStart())`()` Returns the beginning date of the 100-year period 2-digit years are interpreted as being within. |
| open [DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols)! | [getDateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#getDateFormatSymbols())`()` Gets a copy of the date and time format symbols of this date format. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#hashCode())`()` Returns the hash code value for this`SimpleDateFormat`object. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | [parse](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#parse(kotlin.String,%20java.text.ParsePosition))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)`)` Parses text from a string to produce a`Date`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set2DigitYearStart](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#set2DigitYearStart(java.util.Date))`(`startDate:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Sets the 100-year period 2-digit years will be interpreted as being in to begin on the date the user specifies. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#setDateFormatSymbols(java.text.DateFormatSymbols))`(`newFormatSymbols:` ` [DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols)!`)` Sets the date and time format symbols of this date format. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLocalizedPattern](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#toLocalizedPattern())`()` Returns a localized pattern string describing this date format. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#toPattern())`()` Returns a pattern string describing this date format. |

| Inherited functions ||
|---|---|
| From class [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) |------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [format](https://developer.android.com/reference/kotlin/java/text/DateFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `fieldPosition:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)`)` <br /> Formats the given`Object`into a date-time string. The formatted string is appended to the given`StringBuffer`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [format](https://developer.android.com/reference/kotlin/java/text/DateFormat#format(java.util.Date))`(`date:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)`)` <br /> Formats a [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) into a date-time string. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!> | [getAvailableLocales](https://developer.android.com/reference/kotlin/java/text/DateFormat#getAvailableLocales())`()` <br /> Returns an array of all locales for which the`get*Instance`methods of this class can return localized instances. It must contain at least a`Locale`instance equal to [Locale.US](https://developer.android.com/reference/kotlin/java/util/Locale.html#US:java.util.Locale). <br /> | | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) | [getCalendar](https://developer.android.com/reference/kotlin/java/text/DateFormat#getCalendar())`()` <br /> Gets the calendar associated with this date/time formatter. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getDateInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance())`()` <br /> Gets the date formatter with the default formatting style for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getDateInstance(DEFAULT,](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale)). <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getDateInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the date formatter with the given formatting style for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getDateInstance(style,](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale)). <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getDateInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Gets the date formatter with the given formatting style for the given locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getDateTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateTimeInstance())`()` <br /> Gets the date/time formatter with the default formatting style for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getDateTimeInstance(DEFAULT,](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int,%20java.util.Locale)). <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getDateTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the date/time formatter with the given date and time formatting styles for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getDateTimeInstance(dateStyle,](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int,%20java.util.Locale)). <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getDateTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateTimeInstance(kotlin.Int,%20kotlin.Int,%20java.util.Locale))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Gets the date/time formatter with the given formatting styles for the given locale. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getInstance())`()` <br /> Get a default date/time formatter that uses the SHORT style for both the date and the time. <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getNumberFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat#getNumberFormat())`()` <br /> Gets the number formatter which this date/time formatter uses to format and parse a time. <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance())`()` <br /> Gets the time formatter with the default formatting style for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getTimeInstance(DEFAULT,](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale)). <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the time formatter with the given formatting style for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getTimeInstance(style,](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale)). <br /> | | [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) | [getTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Gets the time formatter with the given formatting style for the given locale. <br /> | | [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone.html#) | [getTimeZone](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeZone())`()` <br /> Gets the time zone. This method is equivalent to the following call. ```kotlin <code>getCalendar().getTimeZone() </code> ``` <br /> <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLenient](https://developer.android.com/reference/kotlin/java/text/DateFormat#isLenient())`()` <br /> Tell whether date/time parsing is to be lenient. This method is equivalent to the following call. ```kotlin <code>getCalendar().isLenient() </code> ``` <br /> <br /> | | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | [parse](https://developer.android.com/reference/kotlin/java/text/DateFormat#parse(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Parses text from the beginning of the given string to produce a date. The method may not use the entire text of the given string. See the [parse(java.lang.String,java.text.ParsePosition)](https://developer.android.com/reference/kotlin/java/text/DateFormat#parse(kotlin.String,%20java.text.ParsePosition))method for more information on date parsing. **WARNING:** Don't use this method to deserialize a date. The underlying localized date/time format and parsing behaviors can change across Android versions as common usage in the locale changes. Consider using`long`type for storing a timestamp or [java.time.format.DateTimeFormatter#ISO_INSTANT](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#ISO_INSTANT:java.time.format.DateTimeFormatter) for deserializing the ISO-8601 instant format. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [parseObject](https://developer.android.com/reference/kotlin/java/text/DateFormat#parseObject(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)`)` <br /> Parses text from a string to produce a`Date`. The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed date is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned. See the [parse(java.lang.String,java.text.ParsePosition)](https://developer.android.com/reference/kotlin/java/text/DateFormat#parse(kotlin.String,%20java.text.ParsePosition))method for more information on date parsing. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCalendar](https://developer.android.com/reference/kotlin/java/text/DateFormat#setCalendar(java.util.Calendar))`(`newCalendar:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)`)` <br /> Set the calendar to be used by this date format. Initially, the default calendar for the specified or default locale is used. Any [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone.html#) and [leniency](https://developer.android.com/reference/kotlin/java/text/DateFormat#isLenient())values that have previously been set are overwritten by`newCalendar`'s values. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLenient](https://developer.android.com/reference/kotlin/java/text/DateFormat#setLenient(kotlin.Boolean))`(`lenient:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Specify whether or not date/time parsing is to be lenient. With lenient parsing, the parser may use heuristics to interpret inputs that do not precisely match this object's format. With strict parsing, inputs must match this object's format. This method is equivalent to the following call. ```kotlin <code>getCalendar().setLenient(lenient) </code> ``` This leniency value is overwritten by a call to [setCalendar()](https://developer.android.com/reference/kotlin/java/text/DateFormat#setCalendar(java.util.Calendar)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNumberFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat#setNumberFormat(java.text.NumberFormat))`(`newNumberFormat:` ` [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat)`)` <br /> Allows you to set the number formatter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeZone](https://developer.android.com/reference/kotlin/java/text/DateFormat#setTimeZone(java.util.TimeZone))`(`zone:` ` [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone.html#)`)` <br /> Sets the time zone for the calendar of this`DateFormat`object. This method is equivalent to the following call. ```kotlin <code>getCalendar().setTimeZone(zone) </code> ``` <br /> The`TimeZone`set by this method is overwritten by a [setCalendar](https://developer.android.com/reference/kotlin/java/text/DateFormat#setCalendar(java.util.Calendar))call. The`TimeZone`set by this method may be overwritten as a result of a call to the parse method. <br /> | ||
| From class [Format](https://developer.android.com/reference/kotlin/java/text/Format) |----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an object to produce a string. This is equivalent to [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(obj, new StringBuffer(), new FieldPosition(0)).toString();` <br /> | | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [formatToCharacterIterator](https://developer.android.com/reference/kotlin/java/text/Format#formatToCharacterIterator(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an Object producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String. Each attribute key of the AttributedCharacterIterator will be of type`Field`. It is up to each`Format`implementation to define what the legal values are for each attribute in the`AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value. The default implementation creates an`AttributedCharacterIterator`with no attributes. Subclasses that support fields should override this and create an`AttributedCharacterIterator`with meaningful attributes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/java/text/Format#parseObject(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string. <br /> | ||

| Inherited properties ||
|---|---|
| From class [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) |---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) | [calendar](https://developer.android.com/reference/kotlin/java/text/DateFormat#calendar:java.util.Calendar) <br /> The [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) instance used for calculating the date-time fields and the instant of time. This field is used for both formatting and parsing. Subclasses should initialize this field to a [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) appropriate for the [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) associated with this`DateFormat`. <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [numberFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat#numberFormat:java.text.NumberFormat) <br /> The number formatter that`DateFormat`uses to format numbers in dates and times. Subclasses should initialize this to a number format appropriate for the locale associated with this`DateFormat`. <br /> | ||

## Public constructors

### SimpleDateFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat()
```

Constructs a`SimpleDateFormat`using the default pattern and date format symbols for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale.**Note:** This constructor may not support all locales. For full coverage, use the factory methods in the [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) class. 

### SimpleDateFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat(pattern: String!)
```

Constructs a`SimpleDateFormat`using the given pattern and the default date format symbols for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale.**Note:** This constructor may not support all locales. For full coverage, use the factory methods in the [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) class.

This is equivalent to calling [SimpleDateFormat(pattern, Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20java.util.Locale)).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern describing the date and time format |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given pattern is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category))
- [java.util.Locale.Category#FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) 

### SimpleDateFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat(
    pattern: String!, 
    formatSymbols: DateFormatSymbols!)
```

Constructs a`SimpleDateFormat`using the given pattern and date format symbols.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern describing the date and time format |
| `formatSymbols` | [DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols)!:the date format symbols to be used for formatting |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if the given pattern or formatSymbols is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid |

### SimpleDateFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleDateFormat(
    pattern: String!, 
    locale: Locale!)
```

Constructs a`SimpleDateFormat`using the given pattern and the default date format symbols for the given locale.**Note:** This constructor may not support all locales. For full coverage, use the factory methods in the [DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat) class.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern describing the date and time format |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale whose date format symbols should be used |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.NullPointerException` | if the given pattern or locale is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid |

## Public methods

### applyLocalizedPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyLocalizedPattern(pattern: String!): Unit
```

Applies the given localized pattern string to this date format.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String to be mapped to the new date and time format pattern for this format |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given pattern is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid |

### applyPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(pattern: String!): Unit
```

Applies the given pattern string to this date format.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new date and time pattern for this date format |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given pattern is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Creates a copy of this`SimpleDateFormat`. This also clones the format's date format symbols.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this`SimpleDateFormat` |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the given object with this`SimpleDateFormat`for equality.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given object is equal to this`SimpleDateFormat` |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    date: Date, 
    toAppendTo: StringBuffer, 
    pos: FieldPosition
): StringBuffer
```

Formats the given`Date`into a date/time string and appends the result to the given`StringBuffer`.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `date` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#):the date-time value to be formatted into a date-time string. |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#):where the new date-time text is to be appended. |
| `fieldPosition` | keeps track on the position of the field within the returned string. For example, given a date-time text`"1996.07.10 AD at 15:08:56 PDT"`, if the given`fieldPosition`is [DateFormat.YEAR_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#YEAR_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 0 and 4, respectively. Notice that if the same date-time field appears more than once in a pattern, the`fieldPosition`will be set for the first occurrence of that date-time field. For instance, formatting a`Date`to the date-time string`"1 PM PDT (Pacific Daylight Time)"`using the pattern`"h a z (zzzz)"`and the alignment field [DateFormat.TIMEZONE_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#TIMEZONE_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character`'z'`. |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition):keeps track on the position of the field within the returned string. For example, given a date-time text`"1996.07.10 AD at 15:08:56 PDT"`, if the given`fieldPosition`is [DateFormat.YEAR_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#YEAR_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 0 and 4, respectively. Notice that if the same date-time field appears more than once in a pattern, the`fieldPosition`will be set for the first occurrence of that date-time field. For instance, formatting a`Date`to the date-time string`"1 PM PDT (Pacific Daylight Time)"`using the pattern`"h a z (zzzz)"`and the alignment field [DateFormat.TIMEZONE_FIELD](https://developer.android.com/reference/kotlin/java/text/DateFormat#TIMEZONE_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 5 and 8, respectively, for the first occurrence of the timezone pattern character`'z'`. |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | the formatted date-time string. |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if any of the parameters is`null`. |

### formatToCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatToCharacterIterator(obj: Any!): AttributedCharacterIterator!
```

Formats an Object producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String.

Each attribute key of the AttributedCharacterIterator will be of type`DateFormat.Field`, with the corresponding attribute value being the same as the attribute key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object to format |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | AttributedCharacterIterator describing the formatted value. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if obj is null. |
| `java.lang.IllegalArgumentException` | if the Format cannot format the given object, or if the Format's pattern string is invalid. |

### get2DigitYearStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get2DigitYearStart(): Date!
```

Returns the beginning date of the 100-year period 2-digit years are interpreted as being within.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | the start of the 100-year period into which two digit years are parsed |

**See Also**

- [#set2DigitYearStart](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#set2DigitYearStart(java.util.Date)) 

### getDateFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDateFormatSymbols(): DateFormatSymbols!
```

Gets a copy of the date and time format symbols of this date format.

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols)! | the date and time format symbols of this date format |

**See Also**

- [#setDateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#setDateFormatSymbols(java.text.DateFormatSymbols)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this`SimpleDateFormat`object.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this`SimpleDateFormat`object. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    text: String, 
    pos: ParsePosition
): Date?
```

Parses text from a string to produce a`Date`.

The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed date is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned.

This parsing operation uses the [calendar](https://developer.android.com/reference/kotlin/java/text/DateFormat#calendar:java.util.Calendar) to produce a`Date`. All of the`calendar`'s date-time fields are [cleared](https://developer.android.com/reference/kotlin/java/util/Calendar.html#clear())before parsing, and the`calendar`'s default values of the date-time fields are used for any missing date-time information. For example, the year value of the parsed`Date`is 1970 with [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#) if no year value is given from the parsing operation. The`TimeZone`value may be overwritten, depending on the given pattern and the time zone value in`text`. Any`TimeZone`value that has previously been set by a call to [setTimeZone](https://developer.android.com/reference/kotlin/java/text/DateFormat#setTimeZone(java.util.TimeZone))may need to be restored for further operations.

**WARNING:** Don't use this method to deserialize a date. The underlying localized date/time format and parsing behaviors can change across Android versions as common usage in the locale changes. Consider using`long`type for storing a timestamp or [java.time.format.DateTimeFormatter#ISO_INSTANT](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#ISO_INSTANT:java.time.format.DateTimeFormatter) for deserializing the ISO-8601 instant format.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | The date/time string to be parsed |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition):A`ParsePosition`object with index and error index information as described above. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A`String`, part of which should be parsed. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)? | A`Date`parsed from the string. In case of error, returns null. |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if`text`or`pos`is null. |

### set2DigitYearStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set2DigitYearStart(startDate: Date!): Unit
```

Sets the 100-year period 2-digit years will be interpreted as being in to begin on the date the user specifies.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startDate` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:During parsing, two digit years will be placed in the range`startDate`to`startDate + 100 years`. |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`startDate`is`null`. |

**See Also**

- [#get2DigitYearStart](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#get2DigitYearStart()) 

### setDateFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDateFormatSymbols(newFormatSymbols: DateFormatSymbols!): Unit
```

Sets the date and time format symbols of this date format.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `newFormatSymbols` | [DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols)!:the new date and time format symbols |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given newFormatSymbols is null |

**See Also**

- [#getDateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#getDateFormatSymbols()) 

### toLocalizedPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLocalizedPattern(): String!
```

Returns a localized pattern string describing this date format.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a localized pattern string describing this date format. |

### toPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPattern(): String!
```

Returns a pattern string describing this date format.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a pattern string describing this date format. |
