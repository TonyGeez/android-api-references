Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateTimeFormatter

```
class DateTimeFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.format.DateTimeFormatter](../java/time/format/DateTimeFormatter.md) |

Formatter for printing and parsing date-time objects.

This class provides the main application entry point for printing and parsing and provides common implementations of `DateTimeFormatter`:

- Using predefined constants, such as `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE:java.time.format.DateTimeFormatter`
- Using pattern letters, such as `uuuu-MMM-dd`
- Using localized styles, such as `long` or `medium`

More complex formatters are provided by `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder`.

The main date-time classes provide two methods - one for formatting, `format(DateTimeFormatter formatter)`, and one for parsing, `parse(CharSequence text, DateTimeFormatter formatter)`.

For example:

```kotlin
LocalDate date = LocalDate.now();
   String text = date.format(formatter);
   LocalDate parsedDate = LocalDate.parse(text, formatter);
  
```

In addition to the format, formatters can be created with desired Locale, Chronology, ZoneId, and DecimalStyle.

The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` method returns a new formatter that overrides the locale. The locale affects some aspects of formatting and parsing. For example, the `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofLocalizedDate(java.time.format.FormatStyle)` provides a formatter that uses the locale specific date format.

The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withChronology(java.time.chrono.Chronology)` method returns a new formatter that overrides the chronology. If overridden, the date-time value is converted to the chronology before formatting. During parsing the date-time value is converted to the chronology before it is returned.

The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withZone(java.time.ZoneId)` method returns a new formatter that overrides the zone. If overridden, the date-time value is converted to a ZonedDateTime with the requested ZoneId before formatting. During parsing the ZoneId is applied before the value is returned.

The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withDecimalStyle(java.time.format.DecimalStyle)` method returns a new formatter that overrides the `https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle`. The DecimalStyle symbols are used for formatting and parsing.

Some applications may need to use the older `https://developer.android.com/reference/kotlin/java/text/Format.html#` class for formatting. The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#toFormat()` method returns an implementation of `java.text.Format`.

## Predefined Formatters

| Formatter | Description | Example |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofLocalizedDate(java.time.format.FormatStyle)` | Formatter with date style from the locale | '2011-12-03' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofLocalizedTime(java.time.format.FormatStyle)` | Formatter with time style from the locale | '10:15:30' |
| #ofLocalizedDateTime | Formatter with a style for date and time from the locale | '3 Jun 2008 11:05:30' |
| --- | --- | --- |
| #ofLocalizedDateTime | Formatter with date and time styles from the locale | '3 Jun 2008 11:05' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#BASIC_ISO_DATE:java.time.format.DateTimeFormatter` | Basic ISO date | '20111203' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE:java.time.format.DateTimeFormatter` | ISO Local Date | '2011-12-03' |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_DATE:java.time.format.DateTimeFormatter` | ISO Date with offset | '2011-12-03+01:00' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_DATE:java.time.format.DateTimeFormatter` | ISO Date with or without offset | '2011-12-03+01:00'; '2011-12-03' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_TIME:java.time.format.DateTimeFormatter` | Time without offset | '10:15:30' |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_TIME:java.time.format.DateTimeFormatter` | Time with offset | '10:15:30+01:00' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_TIME:java.time.format.DateTimeFormatter` | Time with or without offset | '10:15:30+01:00'; '10:15:30' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE_TIME:java.time.format.DateTimeFormatter` | ISO Local Date and Time | '2011-12-03T10:15:30' |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_DATE_TIME:java.time.format.DateTimeFormatter` | Date Time with Offset | '2011-12-03T10:15:30+01:00' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_ZONED_DATE_TIME:java.time.format.DateTimeFormatter` | Zoned Date Time | '2011-12-03T10:15:30+01:00\[Europe/Paris\]' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_DATE_TIME:java.time.format.DateTimeFormatter` | Date and time with ZoneId | '2011-12-03T10:15:30+01:00\[Europe/Paris\]' |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_ORDINAL_DATE:java.time.format.DateTimeFormatter` | Year and day of year | '2012-337' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_WEEK_DATE:java.time.format.DateTimeFormatter` | Year and Week | '2012-W48-6' |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_INSTANT:java.time.format.DateTimeFormatter` | Date and Time of an Instant | '2011-12-03T10:15:30Z' |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#RFC_1123_DATE_TIME:java.time.format.DateTimeFormatter` | RFC 1123 / RFC 822 | 'Tue, 3 Jun 2008 11:05:30 GMT' |
|---|---|---|

## Patterns for Formatting and Parsing

Patterns are based on a simple sequence of letters and symbols. A pattern is used to create a Formatter using the `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofPattern(kotlin.String)` and `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofPattern(kotlin.String,%20java.util.Locale)` methods. For example, `"d MMM uuuu"` will format 2011-12-03 as '3 Dec 2011'. A formatter created from a pattern can be used as many times as necessary, it is immutable and is thread-safe.

For example:

```kotlin
LocalDate date = LocalDate.now();
   DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy MM dd");
   String text = date.format(formatter);
   LocalDate parsedDate = LocalDate.parse(text, formatter);
  
```

All letters 'A' to 'Z' and 'a' to 'z' are reserved as pattern letters. The following pattern letters are defined:

| Symbol | Meaning | Presentation | Examples |
| --- | --- | --- | --- |
| G | era | text | AD; Anno Domini; A |
| u | year | year | 2004; 04 |
| y | year-of-era | year | 2004; 04 |
| --- | --- | --- | --- |
| D | day-of-year | number | 189 |
| M/L | month-of-year | number/text | 7; 07; Jul; July; J |
| d | day-of-month | number | 10 |
| --- | --- | --- | --- |
| g | modified-julian-day | number | 2451334 |
| Q/q | quarter-of-year | number/text | 3; 03; Q3; 3rd quarter |
| Y | week-based-year | year | 1996; 96 |
| --- | --- | --- | --- |
| w | week-of-week-based-year | number | 27 |
| W | week-of-month | number | 4 |
| E | day-of-week | text | Tue; Tuesday; T |
| --- | --- | --- | --- |
| e/c | localized day-of-week | number/text | 2; 02; Tue; Tuesday; T |
| F | aligned-week-of-month | number | 3 |
| a | am-pm-of-day | text | PM |
| --- | --- | --- | --- |
| h | clock-hour-of-am-pm (1-12) | number | 12 |
| K | hour-of-am-pm (0-11) | number | 0 |
| k | clock-hour-of-day (1-24) | number | 24 |
| --- | --- | --- | --- |
| H | hour-of-day (0-23) | number | 0 |
| m | minute-of-hour | number | 30 |
| s | second-of-minute | number | 55 |
| --- | --- | --- | --- |
| S | fraction-of-second | fraction | 978 |
| A | milli-of-day | number | 1234 |
| n | nano-of-second | number | 987654321 |
| --- | --- | --- | --- |
| N | nano-of-day | number | 1234000000 |
| V | time-zone ID | zone-id | America/Los_Angeles; Z; -08:30 |
| v | generic time-zone name | zone-name | Pacific Time; PT |
| --- | --- | --- | --- |
| z | time-zone name | zone-name | Pacific Standard Time; PST |
| O | localized zone-offset | offset-O | GMT+8; GMT+08:00; UTC-08:00 |
| X | zone-offset 'Z' for zero | offset-X | Z; -08; -0830; -08:30; -083015; -08:30:15 |
| --- | --- | --- | --- |
| x | zone-offset | offset-x | +0000; -08; -0830; -08:30; -083015; -08:30:15 |
| Z | zone-offset | offset-Z | +0000; -0800; -08:00 |
| p | pad next | pad modifier | 1 |
| --- | --- | --- | --- |
| ' | escape for text | delimiter | |
| '' | single quote | literal | ' |
| \[ | optional section start | | |
| --- | --- | --- | --- |
| \] | optional section end | | |
| | reserved for future use | | |
| { | reserved for future use | | |
| --- | --- | --- | --- |
| } | reserved for future use | | |
|---|---|---|---|

The count of pattern letters determines the format.

**Text** : The text style is determined based on the number of pattern letters used. Less than 4 pattern letters will use the `https://developer.android.com/reference/kotlin/java/time/format/TextStyle`. Exactly 4 pattern letters will use the `https://developer.android.com/reference/kotlin/java/time/format/TextStyle`. Exactly 5 pattern letters will use the `https://developer.android.com/reference/kotlin/java/time/format/TextStyle`. Pattern letters 'L', 'c', and 'q' specify the stand-alone form of the text styles.

**Number**: If the count of letters is one, then the value is output using the minimum number of digits and without padding. Otherwise, the count of digits is used as the width of the output field, with the value zero-padded as necessary. The following pattern letters have constraints on the count of letters. Only one letter of 'c' and 'F' can be specified. Up to two letters of 'd', 'H', 'h', 'K', 'k', 'm', and 's' can be specified. Up to three letters of 'D' can be specified.

**Number/Text**: If the count of pattern letters is 3 or greater, use the Text rules above. Otherwise use the Number rules above.

**Fraction**: Outputs the nano-of-second field as a fraction-of-second. The nano-of-second value has nine digits, thus the count of pattern letters is from 1 to 9. If it is less than 9, then the nano-of-second value is truncated, with only the most significant digits being output.

**Year** : The count of letters determines the minimum field width below which padding is used. If the count of letters is two, then a java.time.format.DateTimeFormatterBuilder#appendValueReduced two digit form is used. For printing, this outputs the rightmost two digits. For parsing, this will parse using the base value of 2000, resulting in a year within the range 2000 to 2099 inclusive. If the count of letters is less than four (but not two), then the sign is only output for negative years as per `https://developer.android.com/reference/kotlin/java/time/format/SignStyle`. Otherwise, the sign is output if the pad width is exceeded, as per `https://developer.android.com/reference/kotlin/java/time/format/SignStyle`.

**ZoneId** : This outputs the time-zone ID, such as 'Europe/Paris'. If the count of letters is two, then the time-zone ID is output. Any other count of letters throws `IllegalArgumentException`.

**Zone names** : This outputs the display name of the time-zone ID. If the pattern letter is 'z' the output is the daylight saving aware zone name. If there is insufficient information to determine whether DST applies, the name ignoring daylight saving time will be used. If the count of letters is one, two or three, then the short name is output. If the count of letters is four, then the full name is output. Five or more letters throws `IllegalArgumentException`.

If the pattern letter is 'v' the output provides the zone name ignoring daylight saving time. If the count of letters is one, then the short name is output. If the count of letters is four, then the full name is output. Two, three and five or more letters throw `IllegalArgumentException`.

**Offset X and x** : This formats the offset based on the number of pattern letters. One letter outputs just the hour, such as '+01', unless the minute is non-zero in which case the minute is also output, such as '+0130'. Two letters outputs the hour and minute, without a colon, such as '+0130'. Three letters outputs the hour and minute, with a colon, such as '+01:30'. Four letters outputs the hour and minute and optional second, without a colon, such as '+013015'. Five letters outputs the hour and minute and optional second, with a colon, such as '+01:30:15'. Six or more letters throws `IllegalArgumentException`. Pattern letter 'X' (upper case) will output 'Z' when the offset to be output would be zero, whereas pattern letter 'x' (lower case) will output '+00', '+0000', or '+00:00'.

**Offset O** : With a non-zero offset, this formats the localized offset based on the number of pattern letters. One letter outputs the [short](../java/time/format/TextStyle.md) form of the localized offset, which is localized offset text, such as 'GMT', with hour without leading zero, optional 2-digit minute and second if non-zero, and colon, for example 'GMT+8'. Four letters outputs the [full](../java/time/format/TextStyle.md) form, which is localized offset text, such as 'GMT, with 2-digit hour and minute field, optional second field if non-zero, and colon, for example 'GMT+08:00'. If the offset is zero, only localized text is output. Any other count of letters throws `IllegalArgumentException`.

**Offset Z** : This formats the offset based on the number of pattern letters. One, two or three letters outputs the hour and minute, without a colon, such as '+0130'. The output will be '+0000' when the offset is zero. Four letters outputs the [full](../java/time/format/TextStyle.md) form of localized offset, equivalent to four letters of Offset-O. The output will be the corresponding localized offset text if the offset is zero. Five letters outputs the hour, minute, with optional second if non-zero, with colon. It outputs 'Z' if the offset is zero. Six or more letters throws `IllegalArgumentException`.

**Optional section** : The optional section markers work exactly like calling `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalStart()` and `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalEnd()`.

**Pad modifier** : Modifies the pattern that immediately follows to be padded with spaces. The pad width is determined by the number of pattern letters. This is the same as calling `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#padNext(kotlin.Int)`.

For example, 'ppH' outputs the hour-of-day padded on the left with spaces to a width of 2.

Any unrecognized letter is an error. Any non-letter character, other than '\[', '\]', '{', '}', '#' and the single quote will be output directly. Despite this, it is recommended to use single quotes around all characters that you want to output directly to ensure that future changes do not break your application.

## Resolving

Parsing is implemented as a two-phase operation. First, the text is parsed using the layout defined by the formatter, producing a `Map` of field to value, a `ZoneId` and a `Chronology`. Second, the parsed data is *resolved* , by validating, combining and simplifying the various fields into more useful ones.

Five parsing methods are supplied by this class. Four of these perform both the parse and resolve phases. The fifth method, `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseUnresolved(kotlin.CharSequence,%20java.text.ParsePosition)`, only performs the first phase, leaving the result unresolved. As such, it is essentially a low-level operation.

The resolve phase is controlled by two parameters, set on this class.

The `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` is an enum that offers three different approaches, strict, smart and lenient. The smart option is the default. It can be set using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withResolverStyle(java.time.format.ResolverStyle)`.

The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withResolverFields(java.time.temporal.TemporalField)` parameter allows the set of fields that will be resolved to be filtered before resolving starts. For example, if the formatter has parsed a year, month, day-of-month and day-of-year, then there are two approaches to resolve a date: (year + month + day-of-month) and (year + day-of-year). The resolver fields allows one of the two approaches to be selected. If no resolver fields are set then both approaches must result in the same date.

Resolving separate fields to form a complete date and time is a complex process with behaviour distributed across a number of classes. It follows these steps:

1. The chronology is determined. The chronology of the result is either the chronology that was parsed, or if no chronology was parsed, it is the chronology set on this class, or if that is null, it is `IsoChronology`.
2. The `ChronoField` date fields are resolved. This is achieved using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#resolveDate(kotlin.collections.MutableMap,%20java.time.format.ResolverStyle)`. Documentation about field resolution is located in the implementation of `Chronology`.
3. The `ChronoField` time fields are resolved. This is documented on `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and is the same for all chronologies.
4. Any fields that are not `ChronoField` are processed. This is achieved using `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#resolve(kotlin.collections.MutableMap,%20java.time.temporal.TemporalAccessor,%20java.time.format.ResolverStyle)`. Documentation about field resolution is located in the implementation of `TemporalField`.
5. The `ChronoField` date and time fields are re-resolved. This allows fields in step four to produce `ChronoField` values and have them be processed into dates and times.
6. A `LocalTime` is formed if there is at least an hour-of-day available. This involves providing default values for minute, second and fraction of second.
7. Any remaining unresolved fields are cross-checked against any date and/or time that was resolved. Thus, an earlier stage would resolve (year + month + day-of-month) to a date, and this stage would check that day-of-week was valid for the date.
8. If an [excess number of days](../java/time/format/DateTimeFormatter.md)) was parsed then it is added to the date if a date is available.
9. If a second-based field is present, but `LocalTime` was not parsed, then the resolver ensures that milli, micro and nano second values are available to meet the contract of `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. These will be set to zero if missing.
10. If both date and time were parsed and either an offset or zone is present, the field `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` is created. If an offset was parsed then the offset will be combined with the `LocalDateTime` to form the instant, with any zone ignored. If a `ZoneId` was parsed without an offset then the zone will be combined with the `LocalDateTime` to form the instant using the rules of `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime.html#atZone(java.time.ZoneId)`. If the `ZoneId` was parsed from a zone name that indicates whether daylight saving time is in operation or not, then that fact will be used to select the correct offset at the local time-line overlap.

## Summary

| Public methods ||
|---|---|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#format(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Formats a date-time object using this formatter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#formatTo(java.time.temporal.TemporalAccessor,%20java.lang.Appendable)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!, appendable: https://developer.android.com/reference/kotlin/java/lang/Appendable.html#!)` Formats a date-time object to an `Appendable` using this formatter. |
| [Chronology](../java/time/chrono/Chronology.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getChronology()()` Gets the overriding chronology to be used during formatting. |
| --- | --- |
| [DecimalStyle](../java/time/format/DecimalStyle.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getDecimalStyle()()` Gets the DecimalStyle to be used during formatting. |
| [Locale](../java/util/Locale.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getLocale()()` Gets the locale to be used during formatting. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TemporalField](../java/time/temporal/TemporalField.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getResolverFields()()` Gets the resolver fields to use during parsing. |
| --- | --- |
| [ResolverStyle](../java/time/format/ResolverStyle.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getResolverStyle()()` Gets the resolver style to use during parsing. |
| [ZoneId](../java/time/ZoneId.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getZone()()` Gets the overriding zone to be used during formatting. |
| [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#localizedBy(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns a copy of this formatter with localized values of the locale, calendar, decimal style and/or timezone, that superseded values in this formatter. |
| --- | --- |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofLocalizedDate(java.time.format.FormatStyle)(dateStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!)` Returns a locale specific date format for the ISO chronology. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofLocalizedDateTime(java.time.format.FormatStyle)(dateTimeStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!)` Returns a locale specific date-time formatter for the ISO chronology. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofLocalizedDateTime(java.time.format.FormatStyle,%20java.time.format.FormatStyle)(dateStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!, timeStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!)` Returns a locale specific date and time format for the ISO chronology. |
| --- | --- |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md) | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofLocalizedPattern(kotlin.String)(requestedTemplate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Creates a locale specific formatter derived from the requested template for the ISO chronology. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofLocalizedTime(java.time.format.FormatStyle)(timeStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!)` Returns a locale specific time format for the ISO chronology. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofPattern(kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a formatter using the specified pattern. |
| --- | --- |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofPattern(kotlin.String,%20java.util.Locale)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Creates a formatter using the specified pattern and locale. |
| [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parse(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Fully parses the text producing a temporal object. |
| [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parse(kotlin.CharSequence,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, position: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Parses the text using this formatter, providing control over the text position. |
| --- | --- |
| T | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parse(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#<T>!)` Fully parses the text producing an object of the specified type. |
| [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseBest(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, vararg queries: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#<*>!)` Fully parses the text producing an object of one of the specified types. |
| [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseUnresolved(kotlin.CharSequence,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, position: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Parses the text using this formatter, without resolving the result, intended for advanced use cases. |
| --- | --- |
| static [TemporalQuery](../java/time/temporal/TemporalQuery.md)\< [Period](../java/time/Period.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parsedExcessDays()()` A query that provides access to the excess days that were parsed. |
| static [TemporalQuery](../java/time/temporal/TemporalQuery.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parsedLeapSecond()()` A query that provides access to whether a leap-second was parsed. |
| [Format](../java/text/Format.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#toFormat()()` Returns this formatter as a `java.text.Format` instance. |
| --- | --- |
| [Format](../java/text/Format.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#toFormat(java.time.temporal.TemporalQuery)(parseQuery: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#<*>!)` Returns this formatter as a `java.text.Format` instance that will parse using the specified query. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#toString()()` Returns a description of the underlying formatters. |
| [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withChronology(java.time.chrono.Chronology)(chrono: https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#!)` Returns a copy of this formatter with a new override chronology. |
| --- | --- |
| [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withDecimalStyle(java.time.format.DecimalStyle)(decimalStyle: https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle!)` Returns a copy of this formatter with a new DecimalStyle. |
| [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns a copy of this formatter with a new locale. |
| [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withResolverFields(java.time.temporal.TemporalField)(vararg resolverFields: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Returns a copy of this formatter with a new set of resolver fields. |
| --- | --- |
| [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withResolverFields(kotlin.collections.MutableSet)(resolverFields: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!>!)` Returns a copy of this formatter with a new set of resolver fields. |
| [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withResolverStyle(java.time.format.ResolverStyle)(resolverStyle: https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle!)` Returns a copy of this formatter with a new resolver style. |
| [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withZone(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Returns a copy of this formatter with a new override zone. |
| --- | --- |

| Properties ||
|---|---|
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#BASIC_ISO_DATE:java.time.format.DateTimeFormatter` The ISO date formatter that formats or parses a date without an offset, such as '20111203'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_DATE:java.time.format.DateTimeFormatter` The ISO date formatter that formats or parses a date with the offset if available, such as '2011-12-03' or '2011-12-03+01:00'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_DATE_TIME:java.time.format.DateTimeFormatter` The ISO-like date-time formatter that formats or parses a date-time with the offset and zone if available, such as '2011-12-03T10:15:30', '2011-12-03T10:15:30+01:00' or '2011-12-03T10:15:30+01:00\[Europe/Paris\]'. |
| --- | --- |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_INSTANT:java.time.format.DateTimeFormatter` The ISO instant formatter that formats or parses an instant in UTC, such as '2011-12-03T10:15:30Z'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE:java.time.format.DateTimeFormatter` The ISO date formatter that formats or parses a date without an offset, such as '2011-12-03'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE_TIME:java.time.format.DateTimeFormatter` The ISO date-time formatter that formats or parses a date-time without an offset, such as '2011-12-03T10:15:30'. |
| --- | --- |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_TIME:java.time.format.DateTimeFormatter` The ISO time formatter that formats or parses a time without an offset, such as '10:15' or '10:15:30'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_DATE:java.time.format.DateTimeFormatter` The ISO date formatter that formats or parses a date with an offset, such as '2011-12-03+01:00'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_DATE_TIME:java.time.format.DateTimeFormatter` The ISO date-time formatter that formats or parses a date-time with an offset, such as '2011-12-03T10:15:30+01:00'. |
| --- | --- |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_TIME:java.time.format.DateTimeFormatter` The ISO time formatter that formats or parses a time with an offset, such as '10:15+01:00' or '10:15:30+01:00'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_ORDINAL_DATE:java.time.format.DateTimeFormatter` The ISO date formatter that formats or parses the ordinal date without an offset, such as '2012-337'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_TIME:java.time.format.DateTimeFormatter` The ISO time formatter that formats or parses a time, with the offset if available, such as '10:15', '10:15:30' or '10:15:30+01:00'. |
| --- | --- |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_WEEK_DATE:java.time.format.DateTimeFormatter` The ISO date formatter that formats or parses the week-based date without an offset, such as '2012-W48-6'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_ZONED_DATE_TIME:java.time.format.DateTimeFormatter` The ISO-like date-time formatter that formats or parses a date-time with offset and zone, such as '2011-12-03T10:15:30+01:00\[Europe/Paris\]'. |
| static [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#RFC_1123_DATE_TIME:java.time.format.DateTimeFormatter` The RFC-1123 date-time formatter, such as 'Tue, 3 Jun 2008 11:05:30 GMT'. |
| --- | --- |

## Public methods

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(temporal: TemporalAccessor!): String!
```

Formats a date-time object using this formatter.

This formats the date-time to a String using the rules of the formatter.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)!: the temporal object to format, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the formatted string, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if an error occurs during formatting |

### formatTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun formatTo(
    temporal: TemporalAccessor!, 
    appendable: Appendable!
): Unit
```

Formats a date-time object to an `Appendable` using this formatter.

This outputs the formatted date-time to the specified destination. `https://developer.android.com/reference/kotlin/java/lang/Appendable.html#` is a general purpose interface that is implemented by all key character output classes including `StringBuffer`, `StringBuilder`, `PrintStream` and `Writer`.

Although `Appendable` methods throw an `IOException`, this method does not. Instead, any `IOException` is wrapped in a runtime exception.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)!: the temporal object to format, not null |
| `appendable` | [Appendable](../java/lang/Appendable.md)!: the appendable to format to, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if an error occurs during formatting |

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChronology(): Chronology!
```

Gets the overriding chronology to be used during formatting.

This returns the override chronology, used to convert dates. By default, a formatter has no override chronology, returning null. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withChronology(java.time.chrono.Chronology)` for more details on overriding.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#!` | the override chronology of this formatter, null if no override |

### getDecimalStyle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDecimalStyle(): DecimalStyle!
```

Gets the DecimalStyle to be used during formatting.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle!` | the DecimalStyle of this formatter, not null |

### getLocale

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocale(): Locale!
```

Gets the locale to be used during formatting.

This is used to lookup any part of the formatter needing specific localization, such as the text or localized pattern.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale.html#!` | the locale of this formatter, not null |

### getResolverFields

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResolverFields(): MutableSet<TemporalField!>!
```

Gets the resolver fields to use during parsing.

This returns the resolver fields, used during the second phase of parsing when fields are resolved into dates and times. By default, a formatter has no resolver fields, and thus returns null. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withResolverFields(kotlin.collections.MutableSet)` for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!>!` | the immutable set of resolver fields of this formatter, null if no fields |

### getResolverStyle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResolverStyle(): ResolverStyle!
```

Gets the resolver style to use during parsing.

This returns the resolver style, used during the second phase of parsing when fields are resolved into dates and times. By default, a formatter has the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withResolverStyle(java.time.format.ResolverStyle)` for more details.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle!` | the resolver style of this formatter, not null |

### getZone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getZone(): ZoneId!
```

Gets the overriding zone to be used during formatting.

This returns the override zone, used to convert instants. By default, a formatter has no override zone, returning null. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withZone(java.time.ZoneId)` for more details on overriding.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!` | the override zone of this formatter, null if no override |

### localizedBy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun localizedBy(locale: Locale!): DateTimeFormatter!
```

Returns a copy of this formatter with localized values of the locale, calendar, decimal style and/or timezone, that superseded values in this formatter.

This is used to lookup any part of the formatter needing specific localization, such as the text or localized pattern. If the locale contains the "ca" (calendar), "nu" (numbering system) and/or "tz" (timezone) [Unicode extensions](../java/util/Locale.md), the chronology, numbering system and/or the zone are overridden.

Unlike the `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` method, the call to this method may produce a different formatter depending on the order of method chaining with other withXXXX() methods.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `locale` | [Locale](../java/util/Locale.md)!: the locale, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | a formatter based on this formatter with localized values of the calendar, decimal style and/or timezone, that superseded values in this formatter. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)`

### ofLocalizedDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofLocalizedDate(dateStyle: FormatStyle!): DateTimeFormatter!
```

Returns a locale specific date format for the ISO chronology.

This returns a formatter that will format or parse a date. The exact format pattern used varies by locale.

The locale is determined from the formatter. The formatter returned directly by this method will use the `https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category)`. The locale can be controlled using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` on the result of this method.

Note that the localized pattern is looked up lazily. This `DateTimeFormatter` holds the style required and the locale, looking up the pattern required on demand.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

| Parameters ||
|---|---|
| `dateStyle` | [FormatStyle](../java/time/format/FormatStyle.md)!: the formatter style to obtain, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | the date formatter, not null |

### ofLocalizedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofLocalizedDateTime(dateTimeStyle: FormatStyle!): DateTimeFormatter!
```

Returns a locale specific date-time formatter for the ISO chronology.

This returns a formatter that will format or parse a date-time. The exact format pattern used varies by locale.

The locale is determined from the formatter. The formatter returned directly by this method will use the `https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category)`. The locale can be controlled using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` on the result of this method.

Note that the localized pattern is looked up lazily. This `DateTimeFormatter` holds the style required and the locale, looking up the pattern required on demand.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style. The `FULL` and `LONG` styles typically require a time-zone. When formatting using these styles, a `ZoneId` must be available, either by using `ZonedDateTime` or `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withZone(java.time.ZoneId)`.

| Parameters ||
|---|---|
| `dateTimeStyle` | [FormatStyle](../java/time/format/FormatStyle.md)!: the formatter style to obtain, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | the date-time formatter, not null |

### ofLocalizedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofLocalizedDateTime(
    dateStyle: FormatStyle!, 
    timeStyle: FormatStyle!
): DateTimeFormatter!
```

Returns a locale specific date and time format for the ISO chronology.

This returns a formatter that will format or parse a date-time. The exact format pattern used varies by locale.

The locale is determined from the formatter. The formatter returned directly by this method will use the `https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()`. The locale can be controlled using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` on the result of this method.

Note that the localized pattern is looked up lazily. This `DateTimeFormatter` holds the style required and the locale, looking up the pattern required on demand.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style. The `FULL` and `LONG` styles typically require a time-zone. When formatting using these styles, a `ZoneId` must be available, either by using `ZonedDateTime` or `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withZone(java.time.ZoneId)`.

| Parameters ||
|---|---|
| `dateStyle` | [FormatStyle](../java/time/format/FormatStyle.md)!: the date formatter style to obtain, not null |
| `timeStyle` | [FormatStyle](../java/time/format/FormatStyle.md)!: the time formatter style to obtain, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | the date, time or date-time formatter, not null |

### ofLocalizedPattern

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofLocalizedPattern(requestedTemplate: String): DateTimeFormatter
```

Creates a locale specific formatter derived from the requested template for the ISO chronology. The requested template is a series of typical pattern symbols in canonical order from the largest date or time unit to the smallest, which can be expressed with the following regular expression: {@snippet : \* "G{0,5}" + // Era \* "y\*" + // Year \* "Q{0,5}" + // Quarter \* "M{0,5}" + // Month \* "w\*" + // Week of Week Based Year \* "E{0,5}" + // Day of Week \* "d{0,2}" + // Day of Month \* "B{0,5}" + // Period/AmPm of Day \* "\[hHjC\]{0,2}" + // Hour of Day/AmPm (refer to LDML for 'j' and 'C') \* "m{0,2}" + // Minute of Hour \* "s{0,2}" + // Second of Minute \* "\[vz\]{0,4}" // Zone \* } All pattern symbols are optional, and each pattern symbol represents a field, for example, 'M' represents the Month field. The number of the pattern symbol letters follows the same presentation, such as "number" or "text" as in the [Patterns for Formatting and Parsing](../java/time/format/DateTimeFormatter.md) section. Other pattern symbols in the requested template are invalid.

The mapping of the requested template to the closest of the available localized formats is defined by the [Unicode LDML specification](https://www.unicode.org/reports/tr35/tr35-dates.html#availableFormats_appendItems). For example, the formatter created from the requested template `yMMM` will format the date '2020-06-16' to 'Jun 2020' in the `https://developer.android.com/reference/kotlin/java/util/Locale.html#US:java.util.Locale`.

The locale is determined from the formatter. The formatter returned directly by this method uses the `https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()`. The locale can be controlled using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` on the result of this method.

The returned formatter has no override zone. It uses `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

| Parameters ||
|---|---|
| `requestedTemplate` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the requested template, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#` | the formatter based on the `requestedTemplate` pattern, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `requestedTemplate` is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofPattern(kotlin.String)`

### ofLocalizedTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofLocalizedTime(timeStyle: FormatStyle!): DateTimeFormatter!
```

Returns a locale specific time format for the ISO chronology.

This returns a formatter that will format or parse a time. The exact format pattern used varies by locale.

The locale is determined from the formatter. The formatter returned directly by this method will use the `https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category)`. The locale can be controlled using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` on the result of this method.

Note that the localized pattern is looked up lazily. This `DateTimeFormatter` holds the style required and the locale, looking up the pattern required on demand.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style. The `FULL` and `LONG` styles typically require a time-zone. When formatting using these styles, a `ZoneId` must be available, either by using `ZonedDateTime` or `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withZone(java.time.ZoneId)`.

| Parameters ||
|---|---|
| `timeStyle` | [FormatStyle](../java/time/format/FormatStyle.md)!: the formatter style to obtain, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | the time formatter, not null |

### ofPattern

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofPattern(pattern: String!): DateTimeFormatter!
```

Creates a formatter using the specified pattern.

This method will create a formatter based on a simple [pattern of letters and symbols](../java/time/format/DateTimeFormatter.md) as described in the class documentation. For example, `d MMM uuuu` will format 2011-12-03 as '3 Dec 2011'.

The formatter will use the `https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category)`. This can be changed using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` on the returned formatter. Alternatively use the `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ofPattern(kotlin.String,%20java.util.Locale)` variant of this method.

The returned formatter has no override chronology or zone. It uses `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | the formatter based on the pattern, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendPattern(kotlin.String)`

### ofPattern

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofPattern(
    pattern: String!, 
    locale: Locale!
): DateTimeFormatter!
```

Creates a formatter using the specified pattern and locale.

This method will create a formatter based on a simple [pattern of letters and symbols](../java/time/format/DateTimeFormatter.md) as described in the class documentation. For example, `d MMM uuuu` will format 2011-12-03 as '3 Dec 2011'.

The formatter will use the specified locale. This can be changed using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withLocale(java.util.Locale)` on the returned formatter.

The returned formatter has no override chronology or zone. It uses `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern to use, not null |
| `locale` | [Locale](../java/util/Locale.md)!: the locale to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | the formatter based on the pattern, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendPattern(kotlin.String)`

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parse(text: CharSequence!): TemporalAccessor!
```

Fully parses the text producing a temporal object.

This parses the entire text producing a temporal object. It is typically more useful to use `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parse(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)`. The result of this method is `TemporalAccessor` which has been resolved, applying basic validation checks to help ensure a valid date-time.

If the parse completes without reading the entire length of the text, or a problem occurs during parsing or merging, then an exception is thrown.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!` | the parsed temporal object, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if unable to parse the requested result |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parse(
    text: CharSequence!, 
    position: ParsePosition!
): TemporalAccessor!
```

Parses the text using this formatter, providing control over the text position.

This parses the text without requiring the parse to start from the beginning of the string or finish at the end. The result of this method is `TemporalAccessor` which has been resolved, applying basic validation checks to help ensure a valid date-time.

The text will be parsed from the specified start `ParsePosition`. The entire length of the text does not have to be parsed, the `ParsePosition` will be updated with the index at the end of parsing.

The operation of this method is slightly different to similar methods using `ParsePosition` on `java.text.Format`. That class will return errors using the error index on the `ParsePosition`. By contrast, this method will throw a `https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException` if an error occurs, with the exception containing the error index. This change in behavior is necessary due to the increased complexity of parsing and resolving dates/times in this API.

If the formatter parses the same field more than once with different values, the result will be an error.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `position` | [ParsePosition](../java/text/ParsePosition.md)!: the position to parse from, updated with length parsed and the index of any error, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!` | the parsed temporal object, not null |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the position is invalid |
| `java.time.format.DateTimeParseException` | if unable to parse the requested result |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> parse(
    text: CharSequence!, 
    query: TemporalQuery<T>!
): T
```

Fully parses the text producing an object of the specified type.

Most applications should use this method for parsing. It parses the entire text to produce the required date-time. The query is typically a method reference to a `from(TemporalAccessor)` method. For example:

```kotlin
LocalDateTime dt = parser.parse(str, LocalDateTime::from);
  
```
If the parse completes without reading the entire length of the text, or a problem occurs during parsing or merging, then an exception is thrown.

| Parameters ||
|---|---|
| `<T>` | the type of the parsed date-time |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `query` | [TemporalQuery](../java/time/temporal/TemporalQuery.md)\<T\>!: the query defining the type to parse to, not null |
| --- | --- |

| Return ||
|---|---|
| `T` | the parsed date-time, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if unable to parse the requested result |

### parseBest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parseBest(
    text: CharSequence!, 
    vararg queries: TemporalQuery<*>!
): TemporalAccessor!
```

Fully parses the text producing an object of one of the specified types.

This parse method is convenient for use when the parser can handle optional elements. For example, a pattern of 'uuuu-MM-dd HH.mm\[ VV\]' can be fully parsed to a `ZonedDateTime`, or partially parsed to a `LocalDateTime`. The queries must be specified in order, starting from the best matching full-parse option and ending with the worst matching minimal parse option. The query is typically a method reference to a `from(TemporalAccessor)` method.

The result is associated with the first type that successfully parses. Normally, applications will use `instanceof` to check the result. For example:

```kotlin
TemporalAccessor dt = parser.parseBest(str, ZonedDateTime::from, LocalDateTime::from);
   if (dt instanceof ZonedDateTime) {
    ...
   } else {
    ...
   }
  
```
If the parse completes without reading the entire length of the text, or a problem occurs during parsing or merging, then an exception is thrown.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `queries` | [TemporalQuery](../java/time/temporal/TemporalQuery.md)\<\*\>!: the queries defining the types to attempt to parse to, must implement `TemporalAccessor`, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!` | the parsed date-time, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if less than 2 types are specified |
| `java.time.format.DateTimeParseException` | if unable to parse the requested result |

### parseUnresolved

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parseUnresolved(
    text: CharSequence!, 
    position: ParsePosition!
): TemporalAccessor!
```

Parses the text using this formatter, without resolving the result, intended for advanced use cases.

Parsing is implemented as a two-phase operation. First, the text is parsed using the layout defined by the formatter, producing a `Map` of field to value, a `ZoneId` and a `Chronology`. Second, the parsed data is *resolved*, by validating, combining and simplifying the various fields into more useful ones. This method performs the parsing stage but not the resolving stage.

The result of this method is `TemporalAccessor` which represents the data as seen in the input. Values are not validated, thus parsing a date string of '2012-00-65' would result in a temporal with three fields - year of '2012', month of '0' and day-of-month of '65'.

The text will be parsed from the specified start `ParsePosition`. The entire length of the text does not have to be parsed, the `ParsePosition` will be updated with the index at the end of parsing.

Errors are returned using the error index field of the `ParsePosition` instead of `DateTimeParseException`. The returned error index will be set to an index indicative of the error. Callers must check for errors before using the result.

If the formatter parses the same field more than once with different values, the result will be an error.

This method is intended for advanced use cases that need access to the internal state during parsing. Typical application code should use `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parse(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)` or the parse method on the target type.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `position` | [ParsePosition](../java/text/ParsePosition.md)!: the position to parse from, updated with length parsed and the index of any error, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!` | the parsed text, null if the parse results in an error |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the position is invalid |
| `java.time.DateTimeException` | if some problem occurs during parsing |

### parsedExcessDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parsedExcessDays(): TemporalQuery<Period!>!
```

A query that provides access to the excess days that were parsed.

This returns a singleton [query](../java/time/temporal/TemporalQuery.md) that provides access to additional information from the parse. The query always returns a non-null period, with a zero period returned instead of null.

There are two situations where this query may return a non-zero period.

- If the `ResolverStyle` is `LENIENT` and a time is parsed without a date, then the complete result of the parse consists of a `LocalTime` and an excess `Period` in days.
- If the `ResolverStyle` is `SMART` and a time is parsed without a date where the time is 24:00:00, then the complete result of the parse consists of a `LocalTime` of 00:00:00 and an excess `Period` of one day.

In both cases, if a complete `ChronoLocalDateTime` or `Instant` is parsed, then the excess days are added to the date part. As a result, this query will return a zero period.

The `SMART` behaviour handles the common "end of day" 24:00 value. Processing in `LENIENT` mode also produces the same result:

```kotlin
Text to parse        Parsed object                         Excess days
   "2012-12-03T00:00"   LocalDateTime.of(2012, 12, 3, 0, 0)   ZERO
   "2012-12-03T24:00"   LocalDateTime.of(2012, 12, 4, 0, 0)   ZERO
   "00:00"              LocalTime.of(0, 0)                    ZERO
   "24:00"              LocalTime.of(0, 0)                    Period.ofDays(1)
  
```
The query can be used as follows:

```kotlin
TemporalAccessor parsed = formatter.parse(str);
   LocalTime time = parsed.query(LocalTime::from);
   Period extraDays = parsed.query(DateTimeFormatter.parsedExcessDays());
  
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#<https://developer.android.com/reference/kotlin/java/time/Period.html#!>!` | a query that provides access to the excess days that were parsed |

### parsedLeapSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parsedLeapSecond(): TemporalQuery<Boolean!>!
```

A query that provides access to whether a leap-second was parsed.

This returns a singleton [query](../java/time/temporal/TemporalQuery.md) that provides access to additional information from the parse. The query always returns a non-null boolean, true if parsing saw a leap-second, false if not.

Instant parsing handles the special "leap second" time of '23:59:60'. Leap seconds occur at '23:59:60' in the UTC time-zone, but at other local times in different time-zones. To avoid this potential ambiguity, the handling of leap-seconds is limited to `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendInstant()`, as that method always parses the instant with the UTC zone offset.

If the time '23:59:60' is received, then a simple conversion is applied, replacing the second-of-minute of 60 with 59. This query can be used on the parse result to determine if the leap-second adjustment was made. The query will return `true` if it did adjust to remove the leap-second, and `false` if not. Note that applying a leap-second smoothing mechanism, such as UTC-SLS, is the responsibility of the application, as follows:

```kotlin
TemporalAccessor parsed = formatter.parse(str);
   Instant instant = parsed.query(Instant::from);
   if (parsed.query(DateTimeFormatter.parsedLeapSecond())) {
     // validate leap-second is correct and apply correct smoothing
   }
  
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>!` | a query that provides access to whether a leap-second was parsed |

### toFormat

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toFormat(): Format!
```

Returns this formatter as a `java.text.Format` instance.

The returned `https://developer.android.com/reference/kotlin/java/text/Format.html#` instance will format any `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#` and parses to a resolved `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#`.

Exceptions will follow the definitions of `Format`, see those methods for details about `IllegalArgumentException` during formatting and `ParseException` or null during parsing. The format does not support attributing of the returned format string.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/text/Format.html#!` | this formatter as a classic format instance, not null |

### toFormat

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toFormat(parseQuery: TemporalQuery<*>!): Format!
```

Returns this formatter as a `java.text.Format` instance that will parse using the specified query.

The returned `https://developer.android.com/reference/kotlin/java/text/Format.html#` instance will format any `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#` and parses to the type specified. The type must be one that is supported by #parse.

Exceptions will follow the definitions of `Format`, see those methods for details about `IllegalArgumentException` during formatting and `ParseException` or null during parsing. The format does not support attributing of the returned format string.

| Parameters ||
|---|---|
| `parseQuery` | [TemporalQuery](../java/time/temporal/TemporalQuery.md)\<\*\>!: the query defining the type to parse to, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/text/Format.html#!` | this formatter as a classic format instance, not null |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a description of the underlying formatters.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a description of this formatter, not null |

### withChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withChronology(chrono: Chronology!): DateTimeFormatter!
```

Returns a copy of this formatter with a new override chronology.

This returns a formatter with similar state to this formatter but with the override chronology set. By default, a formatter has no override chronology, returning null.

If an override is added, then any date that is formatted or parsed will be affected.

When formatting, if the temporal object contains a date, then it will be converted to a date in the override chronology. Whether the temporal contains a date is determined by querying the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` field. Any time or zone will be retained unaltered unless overridden.

If the temporal object does not contain a date, but does contain one or more `ChronoField` date fields, then a `DateTimeException` is thrown. In all other cases, the override chronology is added to the temporal, replacing any previous chronology, but without changing the date/time.

When parsing, there are two distinct cases to consider. If a chronology has been parsed directly from the text, perhaps because `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendChronologyId()` was used, then this override chronology has no effect. If no zone has been parsed, then this override chronology will be used to interpret the `ChronoField` values into a date according to the date resolving rules of the chronology.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `chrono` | [Chronology](../java/time/chrono/Chronology.md)!: the new chronology, null if no override |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | a formatter based on this formatter with the requested override chronology, not null |

### withDecimalStyle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withDecimalStyle(decimalStyle: DecimalStyle!): DateTimeFormatter!
```

Returns a copy of this formatter with a new DecimalStyle.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `decimalStyle` | [DecimalStyle](../java/time/format/DecimalStyle.md)!: the new DecimalStyle, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | a formatter based on this formatter with the requested DecimalStyle, not null |

### withLocale

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withLocale(locale: Locale!): DateTimeFormatter!
```

Returns a copy of this formatter with a new locale.

This is used to lookup any part of the formatter needing specific localization, such as the text or localized pattern.

The locale is stored as passed in, without further processing.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `locale` | [Locale](../java/util/Locale.md)!: the new locale, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | a formatter based on this formatter with the requested locale, not null |

### withResolverFields

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withResolverFields(vararg resolverFields: TemporalField!): DateTimeFormatter!
```

Returns a copy of this formatter with a new set of resolver fields.

This returns a formatter with similar state to this formatter but with the resolver fields set. By default, a formatter has no resolver fields.

Changing the resolver fields only has an effect during parsing. Parsing a text string occurs in two phases. Phase 1 is a basic text parse according to the fields added to the builder. Phase 2 resolves the parsed field-value pairs into date and/or time objects. The resolver fields are used to filter the field-value pairs between phase 1 and 2.

This can be used to select between two or more ways that a date or time might be resolved. For example, if the formatter consists of year, month, day-of-month and day-of-year, then there are two ways to resolve a date. Calling this method with the arguments `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` will ensure that the date is resolved using the year and day-of-year, effectively meaning that the month and day-of-month are ignored during the resolving phase.

In a similar manner, this method can be used to ignore secondary fields that would otherwise be cross-checked. For example, if the formatter consists of year, month, day-of-month and day-of-week, then there is only one way to resolve a date, but the parsed value for day-of-week will be cross-checked against the resolved date. Calling this method with the arguments `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`, `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` will ensure that the date is resolved correctly, but without any cross-check for the day-of-week.

In implementation terms, this method behaves as follows. The result of the parsing phase can be considered to be a map of field to value. The behavior of this method is to cause that map to be filtered between phase 1 and 2, removing all fields other than those specified as arguments to this method.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `resolverFields` | [TemporalField](../java/time/temporal/TemporalField.md)!: the new set of resolver fields, null if no fields |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | a formatter based on this formatter with the requested resolver style, not null |

### withResolverFields

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withResolverFields(resolverFields: MutableSet<TemporalField!>!): DateTimeFormatter!
```

Returns a copy of this formatter with a new set of resolver fields.

This returns a formatter with similar state to this formatter but with the resolver fields set. By default, a formatter has no resolver fields.

Changing the resolver fields only has an effect during parsing. Parsing a text string occurs in two phases. Phase 1 is a basic text parse according to the fields added to the builder. Phase 2 resolves the parsed field-value pairs into date and/or time objects. The resolver fields are used to filter the field-value pairs between phase 1 and 2.

This can be used to select between two or more ways that a date or time might be resolved. For example, if the formatter consists of year, month, day-of-month and day-of-year, then there are two ways to resolve a date. Calling this method with the arguments `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` will ensure that the date is resolved using the year and day-of-year, effectively meaning that the month and day-of-month are ignored during the resolving phase.

In a similar manner, this method can be used to ignore secondary fields that would otherwise be cross-checked. For example, if the formatter consists of year, month, day-of-month and day-of-week, then there is only one way to resolve a date, but the parsed value for day-of-week will be cross-checked against the resolved date. Calling this method with the arguments `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`, `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` will ensure that the date is resolved correctly, but without any cross-check for the day-of-week.

In implementation terms, this method behaves as follows. The result of the parsing phase can be considered to be a map of field to value. The behavior of this method is to cause that map to be filtered between phase 1 and 2, removing all fields other than those specified as arguments to this method.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `resolverFields` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TemporalField](../java/time/temporal/TemporalField.md)!\>!: the new set of resolver fields, null if no fields |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | a formatter based on this formatter with the requested resolver style, not null |

### withResolverStyle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withResolverStyle(resolverStyle: ResolverStyle!): DateTimeFormatter!
```

Returns a copy of this formatter with a new resolver style.

This returns a formatter with similar state to this formatter but with the resolver style set. By default, a formatter has the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

Changing the resolver style only has an effect during parsing. Parsing a text string occurs in two phases. Phase 1 is a basic text parse according to the fields added to the builder. Phase 2 resolves the parsed field-value pairs into date and/or time objects. The resolver style is used to control how phase 2, resolving, happens. See `ResolverStyle` for more information on the options available.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `resolverStyle` | [ResolverStyle](../java/time/format/ResolverStyle.md)!: the new resolver style, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | a formatter based on this formatter with the requested resolver style, not null |

### withZone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withZone(zone: ZoneId!): DateTimeFormatter!
```

Returns a copy of this formatter with a new override zone.

This returns a formatter with similar state to this formatter but with the override zone set. By default, a formatter has no override zone, returning null.

If an override is added, then any instant that is formatted or parsed will be affected.

When formatting, if the temporal object contains an instant, then it will be converted to a zoned date-time using the override zone. Whether the temporal is an instant is determined by querying the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` field. If the input has a chronology then it will be retained unless overridden. If the input does not have a chronology, such as `Instant`, then the ISO chronology will be used.

If the temporal object does not contain an instant, but does contain an offset then an additional check is made. If the normalized override zone is an offset that differs from the offset of the temporal, then a `DateTimeException` is thrown. In all other cases, the override zone is added to the temporal, replacing any previous zone, but without changing the date/time.

When parsing, there are two distinct cases to consider. If a zone has been parsed directly from the text, perhaps because `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneId()` was used, then this override zone has no effect. If no zone has been parsed, then this override zone will be included in the result of the parse where it can be used to build instants and date-times.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `zone` | [ZoneId](../java/time/ZoneId.md)!: the new override zone, null if no override |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#!` | a formatter based on this formatter with the requested override zone, not null |

## Properties

### BASIC_ISO_DATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BASIC_ISO_DATE: DateTimeFormatter!
```

The ISO date formatter that formats or parses a date without an offset, such as '20111203'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 basic local date format. The format consists of:

- Four digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. Only years in the range 0000 to 9999 are supported.
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- If the offset is not available to format or parse then the format is complete.
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()` without colons. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard. The offset parsing is lenient, which allows the minutes and seconds to be optional. Parsing is case insensitive.

As this formatter has an optional element, it may be necessary to parse using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseBest(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)`.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_DATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_DATE: DateTimeFormatter!
```

The ISO date formatter that formats or parses a date with the offset if available, such as '2011-12-03' or '2011-12-03+01:00'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended date format. The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE:java.time.format.DateTimeFormatter`
- If the offset is not available then the format is complete.
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard. Parsing is case insensitive.

As this formatter has an optional element, it may be necessary to parse using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseBest(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)`.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_DATE_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_DATE_TIME: DateTimeFormatter!
```

The ISO-like date-time formatter that formats or parses a date-time with the offset and zone if available, such as '2011-12-03T10:15:30', '2011-12-03T10:15:30+01:00' or '2011-12-03T10:15:30+01:00\[Europe/Paris\]'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended local or offset date-time format, as well as the extended non-ISO form specifying the time-zone. The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE_TIME:java.time.format.DateTimeFormatter`
- If the offset is not available to format or parse then the format is complete.
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard.
- If the zone ID is not available or is a `ZoneOffset` then the format is complete.
- An open square bracket '\['.
- The `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#getId()`. This is not part of the ISO-8601 standard. Parsing is case sensitive.
- A close square bracket '\]'.

As this formatter has an optional element, it may be necessary to parse using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseBest(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)`.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_INSTANT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_INSTANT: DateTimeFormatter!
```

The ISO instant formatter that formats or parses an instant in UTC, such as '2011-12-03T10:15:30Z'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 instant format. When formatting, the instant will always be suffixed by 'Z' to indicate UTC. The second-of-minute is always output. The nano-of-second outputs zero, three, six or nine digits as necessary. When parsing, the behaviour of `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOffsetId()` will be used to parse the offset, converting the instant to UTC as necessary. The time to at least the seconds field is required. Fractional seconds from zero to nine are parsed. The localized decimal style is not used.

This is a special case formatter intended to allow a human readable form of an `https://developer.android.com/reference/kotlin/java/time/Instant.html#`. The `Instant` class is designed to only represent a point in time and internally stores a value in nanoseconds from a fixed epoch of 1970-01-01Z. As such, an `Instant` cannot be formatted as a date or time without providing some form of time-zone. This formatter allows the `Instant` to be formatted, by providing a suitable conversion using `ZoneOffset.UTC`.

The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_DATE_TIME:java.time.format.DateTimeFormatter` where the instant is converted from `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` using the `UTC` offset. Parsing is case insensitive.

The returned formatter has no override chronology or zone. It uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_LOCAL_DATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_LOCAL_DATE: DateTimeFormatter!
```

The ISO date formatter that formats or parses a date without an offset, such as '2011-12-03'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended local date format. The format consists of:

- Four digits or more for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. Years in the range 0000 to 9999 will be pre-padded by zero to ensure four digits. Years outside that range will have a prefixed positive or negative symbol.
- A hyphen ('HYPHEN-MINUS', U+002D)
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- A hyphen ('HYPHEN-MINUS', U+002D)
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_LOCAL_DATE_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_LOCAL_DATE_TIME: DateTimeFormatter!
```

The ISO date-time formatter that formats or parses a date-time without an offset, such as '2011-12-03T10:15:30'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended offset date-time format. The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE:java.time.format.DateTimeFormatter`
- The letter 'T'. Parsing is case insensitive.
- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_TIME:java.time.format.DateTimeFormatter`

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_LOCAL_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_LOCAL_TIME: DateTimeFormatter!
```

The ISO time formatter that formats or parses a time without an offset, such as '10:15' or '10:15:30'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended local time format. The format consists of:

- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- A colon
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- If the second-of-minute is not available then the format is complete.
- A colon
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- If the nano-of-second is zero or not available then the format is complete.
- A decimal point
- One to nine digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. As many digits will be output as required.

The returned formatter has no override chronology or zone. It uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_OFFSET_DATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_OFFSET_DATE: DateTimeFormatter!
```

The ISO date formatter that formats or parses a date with an offset, such as '2011-12-03+01:00'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended offset date format. The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE:java.time.format.DateTimeFormatter`
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard. Parsing is case insensitive.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_OFFSET_DATE_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_OFFSET_DATE_TIME: DateTimeFormatter!
```

The ISO date-time formatter that formats or parses a date-time with an offset, such as '2011-12-03T10:15:30+01:00'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended offset date-time format. The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE_TIME:java.time.format.DateTimeFormatter`
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard. The offset parsing is lenient, which allows the minutes and seconds to be optional. Parsing is case insensitive.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_OFFSET_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_OFFSET_TIME: DateTimeFormatter!
```

The ISO time formatter that formats or parses a time with an offset, such as '10:15+01:00' or '10:15:30+01:00'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended offset time format. The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_TIME:java.time.format.DateTimeFormatter`
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard. Parsing is case insensitive.

The returned formatter has no override chronology or zone. It uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_ORDINAL_DATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_ORDINAL_DATE: DateTimeFormatter!
```

The ISO date formatter that formats or parses the ordinal date without an offset, such as '2012-337'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended ordinal date format. The format consists of:

- Four digits or more for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. Years in the range 0000 to 9999 will be pre-padded by zero to ensure four digits. Years outside that range will have a prefixed positive or negative symbol.
- A hyphen ('HYPHEN-MINUS', U+002D)
- Three digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure three digits.
- If the offset is not available to format or parse then the format is complete.
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard. Parsing is case insensitive.

As this formatter has an optional element, it may be necessary to parse using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseBest(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)`.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_TIME: DateTimeFormatter!
```

The ISO time formatter that formats or parses a time, with the offset if available, such as '10:15', '10:15:30' or '10:15:30+01:00'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended offset time format. The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_TIME:java.time.format.DateTimeFormatter`
- If the offset is not available then the format is complete.
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard. Parsing is case insensitive.

As this formatter has an optional element, it may be necessary to parse using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseBest(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)`.

The returned formatter has no override chronology or zone. It uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_WEEK_DATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_WEEK_DATE: DateTimeFormatter!
```

The ISO date formatter that formats or parses the week-based date without an offset, such as '2012-W48-6'.

This returns an immutable formatter capable of formatting and parsing the ISO-8601 extended week-based date format. The format consists of:

- Four digits or more for the `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#WEEK_BASED_YEAR:java.time.temporal.TemporalField`. Years in the range 0000 to 9999 will be pre-padded by zero to ensure four digits. Years outside that range will have a prefixed positive or negative symbol.
- A hyphen ('HYPHEN-MINUS', U+002D)
- The letter 'W'. Parsing is case insensitive.
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#WEEK_OF_WEEK_BASED_YEAR:java.time.temporal.TemporalField`. This is pre-padded by zero to ensure three digits.
- A hyphen ('HYPHEN-MINUS', U+002D)
- One digit for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. The value run from Monday (1) to Sunday (7).
- If the offset is not available to format or parse then the format is complete.
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the offset has seconds then they will be handled even though this is not part of the ISO-8601 standard. Parsing is case insensitive.

As this formatter has an optional element, it may be necessary to parse using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parseBest(kotlin.CharSequence,%20java.time.temporal.TemporalQuery)`.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### ISO_ZONED_DATE_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ISO_ZONED_DATE_TIME: DateTimeFormatter!
```

The ISO-like date-time formatter that formats or parses a date-time with offset and zone, such as '2011-12-03T10:15:30+01:00\[Europe/Paris\]'.

This returns an immutable formatter capable of formatting and parsing a format that extends the ISO-8601 extended offset date-time format to add the time-zone. The section in square brackets is not part of the ISO-8601 standard. The format consists of:

- The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_DATE_TIME:java.time.format.DateTimeFormatter`
- If the zone ID is not available or is a `ZoneOffset` then the format is complete.
- An open square bracket '\['.
- The `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#getId()`. This is not part of the ISO-8601 standard. Parsing is case sensitive.
- A close square bracket '\]'.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.

### RFC_1123_DATE_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RFC_1123_DATE_TIME: DateTimeFormatter!
```

The RFC-1123 date-time formatter, such as 'Tue, 3 Jun 2008 11:05:30 GMT'.

This returns an immutable formatter capable of formatting and parsing most of the RFC-1123 format. RFC-1123 updates RFC-822 changing the year from two digits to four. This implementation requires a four digit year. This implementation also does not handle North American or military zone names, only 'GMT' and offset amounts.

The format consists of:

- If the day-of-week is not available to format or parse then jump to day-of-month.
- Three letter `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` in English.
- A comma
- A space
- One or two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`.
- A space
- Three letter `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` in English.
- A space
- Four digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. Only years in the range 0000 to 9999 are supported.
- A space
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- A colon
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- If the second-of-minute is not available then jump to the next space.
- A colon
- Two digits for the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. This is pre-padded by zero to ensure two digits.
- A space
- The `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()` without colons or seconds. An offset of zero uses "GMT". North American zone names and military zone names are not handled.

Parsing is case insensitive.

The returned formatter has a chronology of ISO set to ensure dates in other calendar systems are correctly converted. It has no override zone and uses the `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle` resolver style.
