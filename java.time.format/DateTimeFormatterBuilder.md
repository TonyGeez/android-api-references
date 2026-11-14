Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateTimeFormatterBuilder

```
class DateTimeFormatterBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.format.DateTimeFormatterBuilder](DateTimeFormatterBuilder.md) |

Builder to create date-time formatters.

This allows a `DateTimeFormatter` to be created. All date-time formatters are created ultimately using this builder.

The basic elements of date-time can all be added:

- Value - a numeric value
- Fraction - a fractional value including the decimal place. Always use this when outputting fractions to ensure that the fraction is parsed correctly
- Text - the textual equivalent for the value
- OffsetId/Offset - the [zone offset](../java.time/ZoneOffset.md)
- ZoneId - the [time-zone](../java.time/ZoneId.md) id
- ZoneText - the name of the time-zone
- ChronologyId - the [chronology](../java.time.chrono/Chronology.md) id
- ChronologyText - the name of the chronology
- Literal - a text literal
- Nested and Optional - formats can be nested or made optional

In addition, any of the elements may be decorated by padding, either with spaces or any other character.

Finally, a shorthand pattern, mostly compatible with `java.text.SimpleDateFormat SimpleDateFormat` can be used, see `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendPattern(kotlin.String)`. In practice, this simply parses the pattern and calls other methods on the builder.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#DateTimeFormatterBuilder()()` Constructs a new instance of the builder. |

| Public methods ||
|---|---|
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#append(java.time.format.DateTimeFormatter)(formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` <br /> |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendChronologyId()()` Appends the chronology ID, such as 'ISO' or 'ThaiBuddhist', to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendChronologyText(java.time.format.TextStyle)(textStyle: https://developer.android.com/reference/kotlin/java/time/format/TextStyle!)` Appends the chronology name to the formatter. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendFraction(java.time.temporal.TemporalField,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, minWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, decimalPoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Appends the fractional value of a date-time field to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendGenericZoneText(java.time.format.TextStyle)(textStyle: https://developer.android.com/reference/kotlin/java/time/format/TextStyle!)` Appends the generic time-zone name, such as 'Pacific Time', to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendGenericZoneText(java.time.format.TextStyle,%20kotlin.collections.MutableSet)(textStyle: https://developer.android.com/reference/kotlin/java/time/format/TextStyle!, preferredZones: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!>!)` Appends the generic time-zone name, such as 'Pacific Time', to the formatter. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendInstant()()` Appends an instant using ISO-8601 to the formatter, formatting fractional digits in groups of three. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendInstant(kotlin.Int)(fractionalDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Appends an instant using ISO-8601 to the formatter with control over the number of fractional digits. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendLiteral(kotlin.Char)(literal: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Appends a character literal to the formatter. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendLiteral(kotlin.String)(literal: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Appends a string literal to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md) | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendLocalized(kotlin.String)(requestedTemplate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Appends a localized pattern to the formatter using the requested template. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendLocalized(java.time.format.FormatStyle,%20java.time.format.FormatStyle)(dateStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!, timeStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!)` Appends a localized date-time pattern to the formatter. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendLocalizedOffset(java.time.format.TextStyle)(style: https://developer.android.com/reference/kotlin/java/time/format/TextStyle!)` Appends the localized zone offset, such as 'GMT+01:00', to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOffset(kotlin.String,%20kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, noOffsetText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Appends the zone offset, such as '+01:00', to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOffsetId()()` Appends the zone offset, such as '+01:00', to the formatter. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOptional(java.time.format.DateTimeFormatter)(formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Appends a formatter to the builder which will optionally format/parse. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendPattern(kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Appends the elements defined by the specified pattern to the builder. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendText(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Appends the text of a date-time field to the formatter using the full text style. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendText(java.time.temporal.TemporalField,%20java.time.format.TextStyle)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, textStyle: https://developer.android.com/reference/kotlin/java/time/format/TextStyle!)` Appends the text of a date-time field to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendText(java.time.temporal.TemporalField,%20kotlin.collections.MutableMap)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, textLookup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Appends the text of a date-time field to the formatter using the specified map to supply the text. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValue(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Appends the value of a date-time field to the formatter using a normal output style. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValue(java.time.temporal.TemporalField,%20kotlin.Int)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Appends the value of a date-time field to the formatter using a fixed width, zero-padded approach. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValue(java.time.temporal.TemporalField,%20kotlin.Int,%20kotlin.Int,%20java.time.format.SignStyle)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, minWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, signStyle: https://developer.android.com/reference/kotlin/java/time/format/SignStyle!)` Appends the value of a date-time field to the formatter providing full control over formatting. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValueReduced(java.time.temporal.TemporalField,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, baseValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Appends the reduced value of a date-time field to the formatter. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValueReduced(java.time.temporal.TemporalField,%20kotlin.Int,%20kotlin.Int,%20java.time.chrono.ChronoLocalDate)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, baseDate: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#!)` Appends the reduced value of a date-time field to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneId()()` Appends the time-zone ID, such as 'Europe/Paris' or '+02:00', to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneOrOffsetId()()` Appends the time-zone ID, such as 'Europe/Paris' or '+02:00', to the formatter, using the best available zone ID. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneRegionId()()` Appends the time-zone region ID, such as 'Europe/Paris', to the formatter, rejecting the zone ID if it is a `ZoneOffset`. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneText(java.time.format.TextStyle)(textStyle: https://developer.android.com/reference/kotlin/java/time/format/TextStyle!)` Appends the time-zone name, such as 'British Summer Time', to the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneText(java.time.format.TextStyle,%20kotlin.collections.MutableSet)(textStyle: https://developer.android.com/reference/kotlin/java/time/format/TextStyle!, preferredZones: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!>!)` Appends the time-zone name, such as 'British Summer Time', to the formatter. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#getLocalizedDateTimePattern(kotlin.String,%20java.time.chrono.Chronology,%20java.util.Locale)(requestedTemplate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, chrono: https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#)` Returns the formatting pattern for the requested template for a locale and chronology. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#getLocalizedDateTimePattern(java.time.format.FormatStyle,%20java.time.format.FormatStyle,%20java.time.chrono.Chronology,%20java.util.Locale)(dateStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!, timeStyle: https://developer.android.com/reference/kotlin/java/time/format/FormatStyle!, chrono: https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Gets the formatting pattern for date and time styles for a locale and chronology. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalEnd()()` Ends an optional section. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalStart()()` Mark the start of an optional section. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#padNext(kotlin.Int)(padWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Causes the next added printer/parser to pad to a fixed width using a space. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#padNext(kotlin.Int,%20kotlin.Char)(padWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, padChar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Causes the next added printer/parser to pad to a fixed width. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseCaseInsensitive()()` Changes the parse style to be case insensitive for the remainder of the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseCaseSensitive()()` Changes the parse style to be case sensitive for the remainder of the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseDefaulting(java.time.temporal.TemporalField,%20kotlin.Long)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Appends a default value for a field to the formatter for use in parsing. |
| --- | --- |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseLenient()()` Changes the parse style to be lenient for the remainder of the formatter. |
| [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseStrict()()` Changes the parse style to be strict for the remainder of the formatter. |
| [DateTimeFormatter](DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#toFormatter()()` Completes this builder by creating the `DateTimeFormatter` using the default locale. |
| --- | --- |
| [DateTimeFormatter](DateTimeFormatter.md)! | `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#toFormatter(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Completes this builder by creating the `DateTimeFormatter` using the specified locale. |

## Public constructors

### DateTimeFormatterBuilder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DateTimeFormatterBuilder()
```

Constructs a new instance of the builder.

## Public methods

### append

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun append(formatter: DateTimeFormatter!): DateTimeFormatterBuilder!
```

### appendChronologyId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendChronologyId(): DateTimeFormatterBuilder!
```

Appends the chronology ID, such as 'ISO' or 'ThaiBuddhist', to the formatter.

This appends an instruction to format/parse the chronology ID to the builder.

During formatting, the chronology is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#chronology()`. It will be printed using the result of `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#getId()`. If the chronology cannot be obtained then an exception is thrown unless the section of the formatter is optional.

During parsing, the chronology is parsed and must match one of the chronologies in `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#getAvailableChronologies()`. If the chronology cannot be parsed then an exception is thrown unless the section of the formatter is optional. The parser uses the [case sensitive](DateTimeFormatterBuilder.md)) setting.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendChronologyText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendChronologyText(textStyle: TextStyle!): DateTimeFormatterBuilder!
```

Appends the chronology name to the formatter.

The calendar system name will be output during a format. If the chronology cannot be obtained then an exception will be thrown.

| Parameters ||
|---|---|
| `textStyle` | [TextStyle](TextStyle.md)!: the text style to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendFraction

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendFraction(
    field: TemporalField!, 
    minWidth: Int, 
    maxWidth: Int, 
    decimalPoint: Boolean
): DateTimeFormatterBuilder!
```

Appends the fractional value of a date-time field to the formatter.

The fractional value of the field will be output including the preceding decimal point. The preceding value is not output. For example, the second-of-minute value of 15 would be output as `.25`.

The width of the printed fraction can be controlled. Setting the minimum width to zero will cause no output to be generated. The printed fraction will have the minimum width necessary between the minimum and maximum widths - trailing zeroes are omitted. No rounding occurs due to the maximum width - digits are simply dropped.

When parsing in strict mode, the number of parsed digits must be between the minimum and maximum width. In strict mode, if the minimum and maximum widths are equal and there is no decimal point then the parser will participate in adjacent value parsing, see `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValue(java.time.temporal.TemporalField,%20kotlin.Int)`. When parsing in lenient mode, the minimum width is considered to be zero and the maximum is nine.

If the value cannot be obtained then an exception will be thrown. If the value is negative an exception will be thrown. If the field does not have a fixed set of valid values then an exception will be thrown. If the field value in the date-time to be printed is outside the range of valid values then an exception will be thrown.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |
| `minWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minimum width of the field excluding the decimal point, from 0 to 9 |
| `maxWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum width of the field excluding the decimal point, from 1 to 9 |
| --- | --- |
| `decimalPoint` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to output the localized decimal point symbol |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the field has a variable set of valid values or either width is invalid |

### appendGenericZoneText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendGenericZoneText(textStyle: TextStyle!): DateTimeFormatterBuilder!
```

Appends the generic time-zone name, such as 'Pacific Time', to the formatter.

This appends an instruction to format/parse the generic textual name of the zone to the builder. The generic name is the same throughout the whole year, ignoring any daylight saving changes. For example, 'Pacific Time' is the generic name, whereas 'Pacific Standard Time' and 'Pacific Daylight Time' are the specific names, see `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneText(java.time.format.TextStyle)`.

During formatting, the zone is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#zoneId()`. If the zone is a `ZoneOffset` it will be printed using the result of `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the zone is not an offset, the textual name will be looked up for the locale set in the `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter`. If the lookup for text does not find any suitable result, then the `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#getId()` will be printed. If the zone cannot be obtained then an exception is thrown unless the section of the formatter is optional.

During parsing, either the textual zone name, the zone ID or the offset is accepted. Many textual zone names are not unique, such as CST can be for both "Central Standard Time" and "China Standard Time". In this situation, the zone id will be determined by the region information from formatter's `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getLocale()` and the standard zone id for that area, for example, America/New_York for the America Eastern zone. The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendGenericZoneText(java.time.format.TextStyle,%20kotlin.collections.MutableSet)` may be used to specify a set of preferred `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#` in this situation.

| Parameters ||
|---|---|
| `textStyle` | [TextStyle](TextStyle.md)!: the text style to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendGenericZoneText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendGenericZoneText(
    textStyle: TextStyle!, 
    preferredZones: MutableSet<ZoneId!>!
): DateTimeFormatterBuilder!
```

Appends the generic time-zone name, such as 'Pacific Time', to the formatter.

This appends an instruction to format/parse the generic textual name of the zone to the builder. The generic name is the same throughout the whole year, ignoring any daylight saving changes. For example, 'Pacific Time' is the generic name, whereas 'Pacific Standard Time' and 'Pacific Daylight Time' are the specific names, see `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneText(java.time.format.TextStyle)`.

This method also allows a set of preferred `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#` to be specified for parsing. The matched preferred zone id will be used if the textural zone name being parsed is not unique.

See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendGenericZoneText(java.time.format.TextStyle)` for details about formatting and parsing.

| Parameters ||
|---|---|
| `textStyle` | [TextStyle](TextStyle.md)!: the text style to use, not null |
| `preferredZones` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ZoneId](../java.time/ZoneId.md)!\>!: the set of preferred zone ids, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendInstant(): DateTimeFormatterBuilder!
```

Appends an instant using ISO-8601 to the formatter, formatting fractional digits in groups of three.

Instants have a fixed output format. They are converted to a date-time with a zone-offset of UTC and formatted using the standard ISO-8601 format. With this method, formatting nano-of-second outputs zero, three, six or nine digits as necessary. The localized decimal style is not used.

The instant is obtained using `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and optionally `NANO_OF_SECOND`. The value of `INSTANT_SECONDS` may be outside the maximum range of `LocalDateTime`.

The [resolver style](ResolverStyle.md) has no effect on instant parsing. The end-of-day time of '24:00' is handled as midnight at the start of the following day. The leap-second time of '23:59:59' is handled to some degree, see `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parsedLeapSecond()` for full details.

When formatting, the instant will always be suffixed by 'Z' to indicate UTC. When parsing, the behaviour of `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOffsetId()` will be used to parse the offset, converting the instant to UTC as necessary.

An alternative to this method is to format/parse the instant as a single epoch-seconds value. That is achieved using `appendValue(INSTANT_SECONDS)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendInstant(fractionalDigits: Int): DateTimeFormatterBuilder!
```

Appends an instant using ISO-8601 to the formatter with control over the number of fractional digits.

Instants have a fixed output format, although this method provides some control over the fractional digits. They are converted to a date-time with a zone-offset of UTC and printed using the standard ISO-8601 format. The localized decimal style is not used.

The `fractionalDigits` parameter allows the output of the fractional second to be controlled. Specifying zero will cause no fractional digits to be output. From 1 to 9 will output an increasing number of digits, using zero right-padding if necessary. The special value -1 is used to output as many digits as necessary to avoid any trailing zeroes.

When parsing in strict mode, the number of parsed digits must match the fractional digits. When parsing in lenient mode, any number of fractional digits from zero to nine are accepted.

The instant is obtained using `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and optionally `NANO_OF_SECOND`. The value of `INSTANT_SECONDS` may be outside the maximum range of `LocalDateTime`.

The [resolver style](ResolverStyle.md) has no effect on instant parsing. The end-of-day time of '24:00' is handled as midnight at the start of the following day. The leap-second time of '23:59:60' is handled to some degree, see `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#parsedLeapSecond()` for full details.

An alternative to this method is to format/parse the instant as a single epoch-seconds value. That is achieved using `appendValue(INSTANT_SECONDS)`.

| Parameters ||
|---|---|
| `fractionalDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of fractional second digits to format with, from 0 to 9, or -1 to use as many digits as necessary |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the number of fractional digits is invalid |

### appendLiteral

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendLiteral(literal: Char): DateTimeFormatterBuilder!
```

Appends a character literal to the formatter.

This character will be output during a format.

| Parameters ||
|---|---|
| `literal` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the literal to append, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendLiteral

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendLiteral(literal: String!): DateTimeFormatterBuilder!
```

Appends a string literal to the formatter.

This string will be output during a format.

If the literal is empty, nothing is added to the formatter.

| Parameters ||
|---|---|
| `literal` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the literal to append, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendLocalized

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendLocalized(requestedTemplate: String): DateTimeFormatterBuilder
```

Appends a localized pattern to the formatter using the requested template.

This appends a localized section to the builder, suitable for outputting a date, time or date-time combination. The format of the localized section is lazily looked up based on three items:

- the `requestedTemplate` specified to this method
- the `Locale` of the `DateTimeFormatter`
- the `Chronology` of the `DateTimeFormatter` unless overridden

During formatting, the chronology is obtained from the temporal object being formatted, which may have been overridden by `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withChronology(java.time.chrono.Chronology)`.

During parsing, if a chronology has already been parsed, then it is used. Otherwise the default from `DateTimeFormatter.withChronology(Chronology)` is used, with `IsoChronology` as the fallback.

The requested template is a series of typical pattern symbols in canonical order from the largest date or time unit to the smallest, which can be expressed with the following regular expression: {@snippet : \* "G{0,5}" + // Era \* "y\*" + // Year \* "Q{0,5}" + // Quarter \* "M{0,5}" + // Month \* "w\*" + // Week of Week Based Year \* "E{0,5}" + // Day of Week \* "d{0,2}" + // Day of Month \* "B{0,5}" + // Period/AmPm of Day \* "\[hHjC\]{0,2}" + // Hour of Day/AmPm (refer to LDML for 'j' and 'C') \* "m{0,2}" + // Minute of Hour \* "s{0,2}" + // Second of Minute \* "\[vz\]{0,4}" // Zone \* } All pattern symbols are optional, and each pattern symbol represents a field, for example, 'M' represents the Month field. The number of the pattern symbol letters follows the same presentation, such as "number" or "text" as in the [Patterns for Formatting and Parsing](DateTimeFormatter.md) section. Other pattern symbols in the requested template are invalid.

The mapping of the requested template to the closest of the available localized formats is defined by the [Unicode LDML specification](https://www.unicode.org/reports/tr35/tr35-dates.html#availableFormats_appendItems). For example, the formatter created from the requested template `yMMM` will format the date '2020-06-16' to 'Jun 2020' in the `https://developer.android.com/reference/kotlin/java/util/Locale.html#US:java.util.Locale`.

| Parameters ||
|---|---|
| `requestedTemplate` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the requested template to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `requestedTemplate` is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendPattern(kotlin.String)`

### appendLocalized

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendLocalized(
    dateStyle: FormatStyle!, 
    timeStyle: FormatStyle!
): DateTimeFormatterBuilder!
```

Appends a localized date-time pattern to the formatter.

This appends a localized section to the builder, suitable for outputting a date, time or date-time combination. The format of the localized section is lazily looked up based on four items:

- the `dateStyle` specified to this method
- the `timeStyle` specified to this method
- the `Locale` of the `DateTimeFormatter`
- the `Chronology`, selecting the best available

During formatting, the chronology is obtained from the temporal object being formatted, which may have been overridden by `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withChronology(java.time.chrono.Chronology)`. The `FULL` and `LONG` styles typically require a time-zone. When formatting using these styles, a `ZoneId` must be available, either by using `ZonedDateTime` or `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#withZone(java.time.ZoneId)`.

During parsing, if a chronology has already been parsed, then it is used. Otherwise the default from `DateTimeFormatter.withChronology(Chronology)` is used, with `IsoChronology` as the fallback.

Note that this method provides similar functionality to methods on `DateFormat` such as `https://developer.android.com/reference/kotlin/java/text/DateFormat.html#getDateTimeInstance(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `dateStyle` | [FormatStyle](FormatStyle.md)!: the date style to use, null means no date required |
| `timeStyle` | [FormatStyle](FormatStyle.md)!: the time style to use, null means no time required |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if both the date and time styles are null |

### appendLocalizedOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendLocalizedOffset(style: TextStyle!): DateTimeFormatterBuilder!
```

Appends the localized zone offset, such as 'GMT+01:00', to the formatter.

This appends a localized zone offset to the builder, the format of the localized offset is controlled by the specified `https://developer.android.com/reference/kotlin/java/time/format/FormatStyle` to this method:

- `https://developer.android.com/reference/kotlin/java/time/format/TextStyle` - formats with localized offset text, such as 'GMT, 2-digit hour and minute field, optional second field if non-zero, and colon.
- `https://developer.android.com/reference/kotlin/java/time/format/TextStyle` - formats with localized offset text, such as 'GMT, hour without leading zero, optional 2-digit minute and second if non-zero, and colon.

During formatting, the offset is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#offset()`. If the offset cannot be obtained then an exception is thrown unless the section of the formatter is optional.

During parsing, the offset is parsed using the format defined above. If the offset cannot be parsed then an exception is thrown unless the section of the formatter is optional.

| Parameters ||
|---|---|
| `style` | [TextStyle](TextStyle.md)!: the format style to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if style is neither `https://developer.android.com/reference/kotlin/java/time/format/TextStyle` nor `https://developer.android.com/reference/kotlin/java/time/format/TextStyle` |

### appendOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendOffset(
    pattern: String!, 
    noOffsetText: String!
): DateTimeFormatterBuilder!
```

Appends the zone offset, such as '+01:00', to the formatter.

This appends an instruction to format/parse the offset ID to the builder.

During formatting, the offset is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#offset()`. It will be printed using the format defined below. If the offset cannot be obtained then an exception is thrown unless the section of the formatter is optional.

When parsing in strict mode, the input must contain the mandatory and optional elements are defined by the specified pattern. If the offset cannot be parsed then an exception is thrown unless the section of the formatter is optional.

When parsing in lenient mode, only the hours are mandatory - minutes and seconds are optional. The colons are required if the specified pattern contains a colon. If the specified pattern is "+HH", the presence of colons is determined by whether the character after the hour digits is a colon or not. If the offset cannot be parsed then an exception is thrown unless the section of the formatter is optional.

The format of the offset is controlled by a pattern which must be one of the following:

- `+HH` - hour only, ignoring minute and second
- `+HHmm` - hour, with minute if non-zero, ignoring second, no colon
- `+HH:mm` - hour, with minute if non-zero, ignoring second, with colon
- `+HHMM` - hour and minute, ignoring second, no colon
- `+HH:MM` - hour and minute, ignoring second, with colon
- `+HHMMss` - hour and minute, with second if non-zero, no colon
- `+HH:MM:ss` - hour and minute, with second if non-zero, with colon
- `+HHMMSS` - hour, minute and second, no colon
- `+HH:MM:SS` - hour, minute and second, with colon
- `+HHmmss` - hour, with minute if non-zero or with minute and second if non-zero, no colon
- `+HH:mm:ss` - hour, with minute if non-zero or with minute and second if non-zero, with colon
- `+H` - hour only, ignoring minute and second
- `+Hmm` - hour, with minute if non-zero, ignoring second, no colon
- `+H:mm` - hour, with minute if non-zero, ignoring second, with colon
- `+HMM` - hour and minute, ignoring second, no colon
- `+H:MM` - hour and minute, ignoring second, with colon
- `+HMMss` - hour and minute, with second if non-zero, no colon
- `+H:MM:ss` - hour and minute, with second if non-zero, with colon
- `+HMMSS` - hour, minute and second, no colon
- `+H:MM:SS` - hour, minute and second, with colon
- `+Hmmss` - hour, with minute if non-zero or with minute and second if non-zero, no colon
- `+H:mm:ss` - hour, with minute if non-zero or with minute and second if non-zero, with colon

Patterns containing "HH" will format and parse a two digit hour, zero-padded if necessary. Patterns containing "H" will format with no zero-padding, and parse either one or two digits. In lenient mode, the parser will be greedy and parse the maximum digits possible. The "no offset" text controls what text is printed when the total amount of the offset fields to be output is zero. Example values would be 'Z', '+00:00', 'UTC' or 'GMT'. Three formats are accepted for parsing UTC - the "no offset" text, and the plus and minus versions of zero defined by the pattern.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern to use, not null |
| `noOffsetText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text to use when the offset is zero, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

### appendOffsetId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendOffsetId(): DateTimeFormatterBuilder!
```

Appends the zone offset, such as '+01:00', to the formatter.

This appends an instruction to format/parse the offset ID to the builder. This is equivalent to calling `appendOffset("+HH:mm:ss", "Z")`. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOffset(kotlin.String,%20kotlin.String)` for details on formatting and parsing.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendOptional

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendOptional(formatter: DateTimeFormatter!): DateTimeFormatterBuilder!
```

Appends a formatter to the builder which will optionally format/parse.

This method has the same effect as appending each of the constituent parts directly to this builder surrounded by an `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalStart()` and `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalEnd()`.

The formatter will format if data is available for all the fields contained within it. The formatter will parse if the string matches, otherwise no error is returned.

| Parameters ||
|---|---|
| `formatter` | [DateTimeFormatter](DateTimeFormatter.md)!: the formatter to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendPattern

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendPattern(pattern: String!): DateTimeFormatterBuilder!
```

Appends the elements defined by the specified pattern to the builder.

All letters 'A' to 'Z' and 'a' to 'z' are reserved as pattern letters. The characters '#', '{' and '}' are reserved for future use. The characters '\[' and '\]' indicate optional patterns. The following pattern letters are defined:

```kotlin
Symbol  Meaning                     Presentation      Examples
   ---  ---                     ---      ---
    G       era                         text              AD; Anno Domini; A
    u       year                        year              2004; 04
    y       year-of-era                 year              2004; 04
    D       day-of-year                 number            189
    M/L     month-of-year               number/text       7; 07; Jul; July; J
    d       day-of-month                number            10
    g       modified-julian-day         number            2451334
 
    Q/q     quarter-of-year             number/text       3; 03; Q3; 3rd quarter
    Y       week-based-year             year              1996; 96
    w       week-of-week-based-year     number            27
    W       week-of-month               number            4
    E       day-of-week                 text              Tue; Tuesday; T
    e/c     localized day-of-week       number/text       2; 02; Tue; Tuesday; T
    F       day-of-week-in-month        number            3
 
    a       am-pm-of-day                text              PM
    h       clock-hour-of-am-pm (1-12)  number            12
    K       hour-of-am-pm (0-11)        number            0
    k       clock-hour-of-day (1-24)    number            24
 
    H       hour-of-day (0-23)          number            0
    m       minute-of-hour              number            30
    s       second-of-minute            number            55
    S       fraction-of-second          fraction          978
    A       milli-of-day                number            1234
    n       nano-of-second              number            987654321
    N       nano-of-day                 number            1234000000
 
    V       time-zone ID                zone-id           America/Los_Angeles; Z; -08:30
    v       generic time-zone name      zone-name         PT, Pacific Time
    z       time-zone name              zone-name         Pacific Standard Time; PST
    O       localized zone-offset       offset-O          GMT+8; GMT+08:00; UTC-08:00;
    X       zone-offset 'Z' for zero    offset-X          Z; -08; -0830; -08:30; -083015; -08:30:15
    x       zone-offset                 offset-x          +0000; -08; -0830; -08:30; -083015; -08:30:15
    Z       zone-offset                 offset-Z          +0000; -0800; -08:00
 
    p       pad next                    pad modifier      1
 
    '       escape for text             delimiter
    ''      single quote                literal           '
    [       optional section start
    ]       optional section end
    #       reserved for future use
    {       reserved for future use
    }       reserved for future use
  
```

The count of pattern letters determine the format. See [DateTimeFormatter](DateTimeFormatter.md) for a user-focused description of the patterns. The following tables define how the pattern letters map to the builder.

**Date fields**: Pattern letters to output a date.

```kotlin
Pattern  Count  Equivalent builder methods
   ---  ---  ---
     G       1      appendText(ChronoField.ERA, TextStyle.SHORT)
     GG      2      appendText(ChronoField.ERA, TextStyle.SHORT)
     GGG     3      appendText(ChronoField.ERA, TextStyle.SHORT)
     GGGG    4      appendText(ChronoField.ERA, TextStyle.FULL)
     GGGGG   5      appendText(ChronoField.ERA, TextStyle.NARROW)
 
     u       1      appendValue(ChronoField.YEAR, 1, 19, SignStyle.NORMAL)
     uu      2      appendValueReduced(ChronoField.YEAR, 2, 2, 2000)
     uuu     3      appendValue(ChronoField.YEAR, 3, 19, SignStyle.NORMAL)
     u..u    4..n   appendValue(ChronoField.YEAR, n, 19, SignStyle.EXCEEDS_PAD)
     y       1      appendValue(ChronoField.YEAR_OF_ERA, 1, 19, SignStyle.NORMAL)
     yy      2      appendValueReduced(ChronoField.YEAR_OF_ERA, 2, 2, 2000)
     yyy     3      appendValue(ChronoField.YEAR_OF_ERA, 3, 19, SignStyle.NORMAL)
     y..y    4..n   appendValue(ChronoField.YEAR_OF_ERA, n, 19, SignStyle.EXCEEDS_PAD)
     Y       1      append special localized WeekFields element for numeric week-based-year
     YY      2      append special localized WeekFields element for reduced numeric week-based-year 2 digits
     YYY     3      append special localized WeekFields element for numeric week-based-year (3, 19, SignStyle.NORMAL)
     Y..Y    4..n   append special localized WeekFields element for numeric week-based-year (n, 19, SignStyle.EXCEEDS_PAD)
 
     Q       1      appendValue(IsoFields.QUARTER_OF_YEAR)
     QQ      2      appendValue(IsoFields.QUARTER_OF_YEAR, 2)
     QQQ     3      appendText(IsoFields.QUARTER_OF_YEAR, TextStyle.SHORT)
     QQQQ    4      appendText(IsoFields.QUARTER_OF_YEAR, TextStyle.FULL)
     QQQQQ   5      appendText(IsoFields.QUARTER_OF_YEAR, TextStyle.NARROW)
     q       1      appendValue(IsoFields.QUARTER_OF_YEAR)
     qq      2      appendValue(IsoFields.QUARTER_OF_YEAR, 2)
     qqq     3      appendText(IsoFields.QUARTER_OF_YEAR, TextStyle.SHORT_STANDALONE)
     qqqq    4      appendText(IsoFields.QUARTER_OF_YEAR, TextStyle.FULL_STANDALONE)
     qqqqq   5      appendText(IsoFields.QUARTER_OF_YEAR, TextStyle.NARROW_STANDALONE)
 
     M       1      appendValue(ChronoField.MONTH_OF_YEAR)
     MM      2      appendValue(ChronoField.MONTH_OF_YEAR, 2)
     MMM     3      appendText(ChronoField.MONTH_OF_YEAR, TextStyle.SHORT)
     MMMM    4      appendText(ChronoField.MONTH_OF_YEAR, TextStyle.FULL)
     MMMMM   5      appendText(ChronoField.MONTH_OF_YEAR, TextStyle.NARROW)
     L       1      appendValue(ChronoField.MONTH_OF_YEAR)
     LL      2      appendValue(ChronoField.MONTH_OF_YEAR, 2)
     LLL     3      appendText(ChronoField.MONTH_OF_YEAR, TextStyle.SHORT_STANDALONE)
     LLLL    4      appendText(ChronoField.MONTH_OF_YEAR, TextStyle.FULL_STANDALONE)
     LLLLL   5      appendText(ChronoField.MONTH_OF_YEAR, TextStyle.NARROW_STANDALONE)
 
     w       1      append special localized WeekFields element for numeric week-of-year
     ww      2      append special localized WeekFields element for numeric week-of-year, zero-padded
     W       1      append special localized WeekFields element for numeric week-of-month
     d       1      appendValue(ChronoField.DAY_OF_MONTH)
     dd      2      appendValue(ChronoField.DAY_OF_MONTH, 2)
     D       1      appendValue(ChronoField.DAY_OF_YEAR)
     DD      2      appendValue(ChronoField.DAY_OF_YEAR, 2, 3, SignStyle.NOT_NEGATIVE)
     DDD     3      appendValue(ChronoField.DAY_OF_YEAR, 3)
     F       1      appendValue(ChronoField.ALIGNED_WEEK_OF_MONTH)
     g..g    1..n   appendValue(JulianFields.MODIFIED_JULIAN_DAY, n, 19, SignStyle.NORMAL)
     E       1      appendText(ChronoField.DAY_OF_WEEK, TextStyle.SHORT)
     EE      2      appendText(ChronoField.DAY_OF_WEEK, TextStyle.SHORT)
     EEE     3      appendText(ChronoField.DAY_OF_WEEK, TextStyle.SHORT)
     EEEE    4      appendText(ChronoField.DAY_OF_WEEK, TextStyle.FULL)
     EEEEE   5      appendText(ChronoField.DAY_OF_WEEK, TextStyle.NARROW)
     e       1      append special localized WeekFields element for numeric day-of-week
     ee      2      append special localized WeekFields element for numeric day-of-week, zero-padded
     eee     3      appendText(ChronoField.DAY_OF_WEEK, TextStyle.SHORT)
     eeee    4      appendText(ChronoField.DAY_OF_WEEK, TextStyle.FULL)
     eeeee   5      appendText(ChronoField.DAY_OF_WEEK, TextStyle.NARROW)
     c       1      append special localized WeekFields element for numeric day-of-week
     ccc     3      appendText(ChronoField.DAY_OF_WEEK, TextStyle.SHORT_STANDALONE)
     cccc    4      appendText(ChronoField.DAY_OF_WEEK, TextStyle.FULL_STANDALONE)
     ccccc   5      appendText(ChronoField.DAY_OF_WEEK, TextStyle.NARROW_STANDALONE)
  
```

**Time fields**: Pattern letters to output a time.

```kotlin
Pattern  Count  Equivalent builder methods
   ---  ---  ---
     a       1      appendText(ChronoField.AMPM_OF_DAY, TextStyle.SHORT)
     h       1      appendValue(ChronoField.CLOCK_HOUR_OF_AMPM)
     hh      2      appendValue(ChronoField.CLOCK_HOUR_OF_AMPM, 2)
     H       1      appendValue(ChronoField.HOUR_OF_DAY)
     HH      2      appendValue(ChronoField.HOUR_OF_DAY, 2)
     k       1      appendValue(ChronoField.CLOCK_HOUR_OF_DAY)
     kk      2      appendValue(ChronoField.CLOCK_HOUR_OF_DAY, 2)
     K       1      appendValue(ChronoField.HOUR_OF_AMPM)
     KK      2      appendValue(ChronoField.HOUR_OF_AMPM, 2)
     m       1      appendValue(ChronoField.MINUTE_OF_HOUR)
     mm      2      appendValue(ChronoField.MINUTE_OF_HOUR, 2)
     s       1      appendValue(ChronoField.SECOND_OF_MINUTE)
     ss      2      appendValue(ChronoField.SECOND_OF_MINUTE, 2)
 
     S..S    1..n   appendFraction(ChronoField.NANO_OF_SECOND, n, n, false)
     A..A    1..n   appendValue(ChronoField.MILLI_OF_DAY, n, 19, SignStyle.NOT_NEGATIVE)
     n..n    1..n   appendValue(ChronoField.NANO_OF_SECOND, n, 19, SignStyle.NOT_NEGATIVE)
     N..N    1..n   appendValue(ChronoField.NANO_OF_DAY, n, 19, SignStyle.NOT_NEGATIVE)
  
```

**Zone ID** : Pattern letters to output `ZoneId`.

```kotlin
Pattern  Count  Equivalent builder methods
   ---  ---  ---
     VV      2      appendZoneId()
     v       1      appendGenericZoneText(TextStyle.SHORT)
     vvvv    4      appendGenericZoneText(TextStyle.FULL)
     z       1      appendZoneText(TextStyle.SHORT)
     zz      2      appendZoneText(TextStyle.SHORT)
     zzz     3      appendZoneText(TextStyle.SHORT)
     zzzz    4      appendZoneText(TextStyle.FULL)
  
```

**Zone offset** : Pattern letters to output `ZoneOffset`.

```kotlin
Pattern  Count  Equivalent builder methods
   ---  ---  ---
     O       1      appendLocalizedOffset(TextStyle.SHORT)
     OOOO    4      appendLocalizedOffset(TextStyle.FULL)
     X       1      appendOffset("+HHmm","Z")
     XX      2      appendOffset("+HHMM","Z")
     XXX     3      appendOffset("+HH:MM","Z")
     XXXX    4      appendOffset("+HHMMss","Z")
     XXXXX   5      appendOffset("+HH:MM:ss","Z")
     x       1      appendOffset("+HHmm","+00")
     xx      2      appendOffset("+HHMM","+0000")
     xxx     3      appendOffset("+HH:MM","+00:00")
     xxxx    4      appendOffset("+HHMMss","+0000")
     xxxxx   5      appendOffset("+HH:MM:ss","+00:00")
     Z       1      appendOffset("+HHMM","+0000")
     ZZ      2      appendOffset("+HHMM","+0000")
     ZZZ     3      appendOffset("+HHMM","+0000")
     ZZZZ    4      appendLocalizedOffset(TextStyle.FULL)
     ZZZZZ   5      appendOffset("+HH:MM:ss","Z")
  
```

**Modifiers**: Pattern letters that modify the rest of the pattern:

```kotlin
Pattern  Count  Equivalent builder methods
   ---  ---  ---
     [       1      optionalStart()
     ]       1      optionalEnd()
     p..p    1..n   padNext(n)
  
```

Any sequence of letters not specified above, unrecognized letter or reserved character will throw an exception. Future versions may add to the set of patterns. It is recommended to use single quotes around all characters that you want to output directly to ensure that future changes do not break your application.

Note that the pattern string is similar, but not identical, to `https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#`. The pattern string is also similar, but not identical, to that defined by the Unicode Common Locale Data Repository (CLDR/LDML). Pattern letters 'X' and 'u' are aligned with Unicode CLDR/LDML. By contrast, `SimpleDateFormat` uses 'u' for the numeric day of week. Pattern letters 'y' and 'Y' parse years of two digits and more than 4 digits differently. Pattern letters 'n', 'A', 'N', and 'p' are added. Number types will reject large numbers.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

### appendText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendText(field: TemporalField!): DateTimeFormatterBuilder!
```

Appends the text of a date-time field to the formatter using the full text style.

The text of the field will be output during a format. The value must be within the valid range of the field. If the value cannot be obtained then an exception will be thrown. If the field has no textual representation, then the numeric value will be used.

The value will be printed as per the normal format of an integer value. Only negative numbers will be signed. No padding will be added.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendText(
    field: TemporalField!, 
    textStyle: TextStyle!
): DateTimeFormatterBuilder!
```

Appends the text of a date-time field to the formatter.

The text of the field will be output during a format. The value must be within the valid range of the field. If the value cannot be obtained then an exception will be thrown. If the field has no textual representation, then the numeric value will be used.

The value will be printed as per the normal format of an integer value. Only negative numbers will be signed. No padding will be added.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |
| `textStyle` | [TextStyle](TextStyle.md)!: the text style to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendText(
    field: TemporalField!, 
    textLookup: MutableMap<Long!, String!>!
): DateTimeFormatterBuilder!
```

Appends the text of a date-time field to the formatter using the specified map to supply the text.

The standard text outputting methods use the localized text in the JDK. This method allows that text to be specified directly. The supplied map is not validated by the builder to ensure that formatting or parsing is possible, thus an invalid map may throw an error during later use.

Supplying the map of text provides considerable flexibility in formatting and parsing. For example, a legacy application might require or supply the months of the year as "JNY", "FBY", "MCH" etc. These do not match the standard set of text for localized month names. Using this method, a map can be created which defines the connection between each value and the text:

```kotlin
Map<Long, String> map = new HashMap<>();
  map.put(1L, "JNY");
  map.put(2L, "FBY");
  map.put(3L, "MCH");
  ...
  builder.appendText(MONTH_OF_YEAR, map);
  
```

Other uses might be to output the value with a suffix, such as "1st", "2nd", "3rd", or as Roman numerals "I", "II", "III", "IV".

During formatting, the value is obtained and checked that it is in the valid range. If text is not available for the value then it is output as a number. During parsing, the parser will match against the map of text and numeric values.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |
| `textLookup` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: the map from the value to the text |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendValue(field: TemporalField!): DateTimeFormatterBuilder!
```

Appends the value of a date-time field to the formatter using a normal output style.

The value of the field will be output during a format. If the value cannot be obtained then an exception will be thrown.

The value will be printed as per the normal format of an integer value. Only negative numbers will be signed. No padding will be added.

The parser for a variable width value such as this normally behaves greedily, requiring one digit, but accepting as many digits as possible. This behavior can be affected by 'adjacent value parsing'. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValue(java.time.temporal.TemporalField,%20kotlin.Int)` for full details.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendValue(
    field: TemporalField!, 
    width: Int
): DateTimeFormatterBuilder!
```

Appends the value of a date-time field to the formatter using a fixed width, zero-padded approach.

The value of the field will be output during a format. If the value cannot be obtained then an exception will be thrown.

The value will be zero-padded on the left. If the size of the value means that it cannot be printed within the width then an exception is thrown. If the value of the field is negative then an exception is thrown during formatting.

This method supports a special technique of parsing known as 'adjacent value parsing'. This technique solves the problem where a value, variable or fixed width, is followed by one or more fixed length values. The standard parser is greedy, and thus it would normally steal the digits that are needed by the fixed width value parsers that follow the variable width one.

No action is required to initiate 'adjacent value parsing'. When a call to `appendValue` is made, the builder enters adjacent value parsing setup mode. If the immediately subsequent method call or calls on the same builder are for a fixed width value, then the parser will reserve space so that the fixed width values can be parsed.

For example, consider `builder.appendValue(YEAR).appendValue(MONTH_OF_YEAR, 2);` The year is a variable width parse of between 1 and 19 digits. The month is a fixed width parse of 2 digits. Because these were appended to the same builder immediately after one another, the year parser will reserve two digits for the month to parse. Thus, the text '201106' will correctly parse to a year of 2011 and a month of 6. Without adjacent value parsing, the year would greedily parse all six digits and leave nothing for the month.

Adjacent value parsing applies to each set of fixed width not-negative values in the parser that immediately follow any kind of value, variable or fixed width. Calling any other append method will end the setup of adjacent value parsing. Thus, in the unlikely event that you need to avoid adjacent value parsing behavior, simply add the `appendValue` to another `DateTimeFormatterBuilder` and add that to this builder.

If adjacent parsing is active, then parsing must match exactly the specified number of digits in both strict and lenient modes. In addition, no positive or negative sign is permitted.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the width of the printed field, from 1 to 19 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width is invalid |

### appendValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendValue(
    field: TemporalField!, 
    minWidth: Int, 
    maxWidth: Int, 
    signStyle: SignStyle!
): DateTimeFormatterBuilder!
```

Appends the value of a date-time field to the formatter providing full control over formatting.

The value of the field will be output during a format. If the value cannot be obtained then an exception will be thrown.

This method provides full control of the numeric formatting, including zero-padding and the positive/negative sign.

The parser for a variable width value such as this normally behaves greedily, accepting as many digits as possible. This behavior can be affected by 'adjacent value parsing'. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValue(java.time.temporal.TemporalField,%20kotlin.Int)` for full details.

In strict parsing mode, the minimum number of parsed digits is `minWidth` and the maximum is `maxWidth`. In lenient parsing mode, the minimum number of parsed digits is one and the maximum is 19 (except as limited by adjacent value parsing).

If this method is invoked with equal minimum and maximum widths and a sign style of `NOT_NEGATIVE` then it delegates to `appendValue(TemporalField,int)`. In this scenario, the formatting and parsing behavior described there occur.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |
| `minWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minimum field width of the printed field, from 1 to 19 |
| `maxWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum field width of the printed field, from 1 to 19 |
| --- | --- |
| `signStyle` | [SignStyle](SignStyle.md)!: the positive/negative output style, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the widths are invalid |

### appendValueReduced

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendValueReduced(
    field: TemporalField!, 
    width: Int, 
    maxWidth: Int, 
    baseValue: Int
): DateTimeFormatterBuilder!
```

Appends the reduced value of a date-time field to the formatter.

Since fields such as year vary by chronology, it is recommended to use the `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendValueReduced(java.time.temporal.TemporalField,%20kotlin.Int,%20kotlin.Int,%20java.time.chrono.ChronoLocalDate)` date} variant of this method in most cases. This variant is suitable for simple fields or working with only the ISO chronology.

For formatting, the `width` and `maxWidth` are used to determine the number of characters to format. If they are equal then the format is fixed width. If the value of the field is within the range of the `baseValue` using `width` characters then the reduced value is formatted otherwise the value is truncated to fit `maxWidth`. The rightmost characters are output to match the width, left padding with zero.

For strict parsing, the number of characters allowed by `width` to `maxWidth` are parsed. For lenient parsing, the number of characters must be at least 1 and less than 10. If the number of digits parsed is equal to `width` and the value is positive, the value of the field is computed to be the first number greater than or equal to the `baseValue` with the same least significant characters, otherwise the value parsed is the field value. This allows a reduced value to be entered for values in range of the baseValue and width and absolute values can be entered for values outside the range.

For example, a base value of `1980` and a width of `2` will have valid values from `1980` to `2079`. During parsing, the text `"12"` will result in the value `2012` as that is the value within the range where the last two characters are "12". By contrast, parsing the text `"1915"` will result in the value `1915`.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the field width of the printed and parsed field, from 1 to 10 |
| `maxWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum field width of the printed field, from 1 to 10 |
| --- | --- |
| `baseValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the base value of the range of valid values |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or base value is invalid |

### appendValueReduced

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendValueReduced(
    field: TemporalField!, 
    width: Int, 
    maxWidth: Int, 
    baseDate: ChronoLocalDate!
): DateTimeFormatterBuilder!
```

Appends the reduced value of a date-time field to the formatter.

This is typically used for formatting and parsing a two digit year.

The base date is used to calculate the full value during parsing. For example, if the base date is 1950-01-01 then parsed values for a two digit year parse will be in the range 1950-01-01 to 2049-12-31. Only the year would be extracted from the date, thus a base date of 1950-08-25 would also parse to the range 1950-01-01 to 2049-12-31. This behavior is necessary to support fields such as week-based-year or other calendar systems where the parsed value does not align with standard ISO years.

The exact behavior is as follows. Parse the full set of fields and determine the effective chronology using the last chronology if it appears more than once. Then convert the base date to the effective chronology. Then extract the specified field from the chronology-specific base date and use it to determine the `baseValue` used below.

For formatting, the `width` and `maxWidth` are used to determine the number of characters to format. If they are equal then the format is fixed width. If the value of the field is within the range of the `baseValue` using `width` characters then the reduced value is formatted otherwise the value is truncated to fit `maxWidth`. The rightmost characters are output to match the width, left padding with zero.

For strict parsing, the number of characters allowed by `width` to `maxWidth` are parsed. For lenient parsing, the number of characters must be at least 1 and less than 10. If the number of digits parsed is equal to `width` and the value is positive, the value of the field is computed to be the first number greater than or equal to the `baseValue` with the same least significant characters, otherwise the value parsed is the field value. This allows a reduced value to be entered for values in range of the baseValue and width and absolute values can be entered for values outside the range.

For example, a base value of `1980` and a width of `2` will have valid values from `1980` to `2079`. During parsing, the text `"12"` will result in the value `2012` as that is the value within the range where the last two characters are "12". By contrast, parsing the text `"1915"` will result in the value `1915`.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to append, not null |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the field width of the printed and parsed field, from 1 to 10 |
| `maxWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum field width of the printed field, from 1 to 10 |
| --- | --- |
| `baseDate` | [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md)!: the base date used to calculate the base value for the range of valid values in the parsed chronology, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or base value is invalid |

### appendZoneId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendZoneId(): DateTimeFormatterBuilder!
```

Appends the time-zone ID, such as 'Europe/Paris' or '+02:00', to the formatter.

This appends an instruction to format/parse the zone ID to the builder. The zone ID is obtained in a strict manner suitable for `ZonedDateTime`. By contrast, `OffsetDateTime` does not have a zone ID suitable for use with this method, see `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneOrOffsetId()`.

During formatting, the zone is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#zoneId()`. It will be printed using the result of `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#getId()`. If the zone cannot be obtained then an exception is thrown unless the section of the formatter is optional.

During parsing, the text must match a known zone or offset. There are two types of zone ID, offset-based, such as '+01:30' and region-based, such as 'Europe/London'. These are parsed differently. If the parse starts with '+' or '-', then the parser expects an offset-based zone and will not match region-based zones. The offset ID parsing is equivalent to using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOffset(kotlin.String,%20kotlin.String)` using the arguments 'HH:MM:ss' and the no offset string '0'. If the parse starts with 'UT', 'UTC' or 'GMT', and the parser can match a following offset, then a region-based zone with the parsed offset will be returned, or else if the parser cannot match a following offset, then `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#UTC:java.time.ZoneOffset` is selected. In all other cases, the list of known region-based zones is used to find the longest available match. If no match is found, and the parse starts with 'Z', then `ZoneOffset.UTC` is selected. The parser uses the [case sensitive](DateTimeFormatterBuilder.md)) setting.

For example, the following will parse:

```kotlin
"Europe/London"           -- ZoneId.of("Europe/London")
    "Z"                       -- ZoneOffset.UTC
    "UT"                      -- ZoneId.of("UT")
    "UTC"                     -- ZoneId.of("UTC")
    "GMT"                     -- ZoneId.of("GMT")
    "+01:30"                  -- ZoneOffset.of("+01:30")
    "UT+01:30"                -- ZoneId.of("UT+01:30")
    "UTC+01:30"               -- ZoneId.of("UTC+01:30")
    "GMT+01:30"               -- ZoneId.of("GMT+01:30")
  
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneRegionId()`

### appendZoneOrOffsetId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendZoneOrOffsetId(): DateTimeFormatterBuilder!
```

Appends the time-zone ID, such as 'Europe/Paris' or '+02:00', to the formatter, using the best available zone ID.

This appends an instruction to format/parse the best available zone or offset ID to the builder. The zone ID is obtained in a lenient manner that first attempts to find a true zone ID, such as that on `ZonedDateTime`, and then attempts to find an offset, such as that on `OffsetDateTime`.

During formatting, the zone is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#zone()`. It will be printed using the result of `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#getId()`. If the zone cannot be obtained then an exception is thrown unless the section of the formatter is optional.

During parsing, the text must match a known zone or offset. There are two types of zone ID, offset-based, such as '+01:30' and region-based, such as 'Europe/London'. These are parsed differently. If the parse starts with '+' or '-', then the parser expects an offset-based zone and will not match region-based zones. The offset ID parsing is equivalent to using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOffset(kotlin.String,%20kotlin.String)` using the arguments 'HH:MM:ss' and the no offset string '0'. If the parse starts with 'UT', 'UTC' or 'GMT', and the parser can match a following offset, then a region-based zone with the parsed offset will be returned, or else if the parser cannot match a following offset, then `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#UTC:java.time.ZoneOffset` is selected. In all other cases, the list of known region-based zones is used to find the longest available match. If no match is found, and the parse starts with 'Z', then `ZoneOffset.UTC` is selected. The parser uses the [case sensitive](DateTimeFormatterBuilder.md)) setting.

For example, the following will parse:

```kotlin
"Europe/London"           -- ZoneId.of("Europe/London")
    "Z"                       -- ZoneOffset.UTC
    "UT"                      -- ZoneId.of("UT")
    "UTC"                     -- ZoneId.of("UTC")
    "GMT"                     -- ZoneId.of("GMT")
    "+01:30"                  -- ZoneOffset.of("+01:30")
    "UT+01:30"                -- ZoneId.of("UT+01:30")
    "UTC+01:30"               -- ZoneId.of("UTC+01:30")
    "GMT+01:30"               -- ZoneId.of("GMT+01:30")
  
```

Note that this method is identical to `appendZoneId()` except in the mechanism used to obtain the zone.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneId()`

### appendZoneRegionId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendZoneRegionId(): DateTimeFormatterBuilder!
```

Appends the time-zone region ID, such as 'Europe/Paris', to the formatter, rejecting the zone ID if it is a `ZoneOffset`.

This appends an instruction to format only region-based zone IDs to the builder.

During formatting, the zone is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#zoneId()`. If the zone is a `ZoneOffset` or it cannot be obtained then an exception is thrown unless the section of the formatter is optional. If the zone is not an offset, then the zone will be printed using the zone ID from `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#getId()`.

During parsing, the text must match a known zone or offset. There are two types of zone ID, offset-based, such as '+01:30' and region-based, such as 'Europe/London'. These are parsed differently. If the parse starts with '+' or '-', then the parser expects an offset-based zone and will not match region-based zones. The offset ID parsing is equivalent to using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendOffset(kotlin.String,%20kotlin.String)` using the arguments 'HH:MM:ss' and the no offset string '0'. If the parse starts with 'UT', 'UTC' or 'GMT', and the parser can match a following offset, then a region-based zone with the parsed offset will be returned, or else if the parser cannot match a following offset, then `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#UTC:java.time.ZoneOffset` is selected. In all other cases, the list of known region-based zones is used to find the longest available match. If no match is found, and the parse starts with 'Z', then `ZoneOffset.UTC` is selected. The parser uses the [case sensitive](DateTimeFormatterBuilder.md)) setting.

For example, the following will parse:

```kotlin
"Europe/London"           -- ZoneId.of("Europe/London")
    "Z"                       -- ZoneOffset.UTC
    "UT"                      -- ZoneId.of("UT")
    "UTC"                     -- ZoneId.of("UTC")
    "GMT"                     -- ZoneId.of("GMT")
    "+01:30"                  -- ZoneOffset.of("+01:30")
    "UT+01:30"                -- ZoneId.of("UT+01:30")
    "UTC+01:30"               -- ZoneId.of("UTC+01:30")
    "GMT+01:30"               -- ZoneId.of("GMT+01:30")
  
```

Note that this method is identical to `appendZoneId()` except in the mechanism used to obtain the zone. Note also that parsing accepts offsets, whereas formatting will never produce one.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneId()`

### appendZoneText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendZoneText(textStyle: TextStyle!): DateTimeFormatterBuilder!
```

Appends the time-zone name, such as 'British Summer Time', to the formatter.

This appends an instruction to format/parse the textual name of the zone to the builder.

During formatting, the zone is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#zoneId()`. If the zone is a `ZoneOffset` it will be printed using the result of `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the zone is not an offset, the textual name will be looked up for the locale set in the `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter`. If the temporal object being printed represents an instant, or if it is a local date-time that is not in a daylight saving gap or overlap then the text will be the summer or winter time text as appropriate. If the lookup for text does not find any suitable result, then the `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#getId()` will be printed. If the zone cannot be obtained then an exception is thrown unless the section of the formatter is optional.

During parsing, either the textual zone name, the zone ID or the offset is accepted. Many textual zone names are not unique, such as CST can be for both "Central Standard Time" and "China Standard Time". In this situation, the zone id will be determined by the region information from formatter's `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getLocale()` and the standard zone id for that area, for example, America/New_York for the America Eastern zone. The `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendZoneText(java.time.format.TextStyle,%20kotlin.collections.MutableSet)` may be used to specify a set of preferred `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#` in this situation.

| Parameters ||
|---|---|
| `textStyle` | [TextStyle](TextStyle.md)!: the text style to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### appendZoneText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun appendZoneText(
    textStyle: TextStyle!, 
    preferredZones: MutableSet<ZoneId!>!
): DateTimeFormatterBuilder!
```

Appends the time-zone name, such as 'British Summer Time', to the formatter.

This appends an instruction to format/parse the textual name of the zone to the builder.

During formatting, the zone is obtained using a mechanism equivalent to querying the temporal with `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#zoneId()`. If the zone is a `ZoneOffset` it will be printed using the result of `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getId()`. If the zone is not an offset, the textual name will be looked up for the locale set in the `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter`. If the temporal object being printed represents an instant, or if it is a local date-time that is not in a daylight saving gap or overlap, then the text will be the summer or winter time text as appropriate. If the lookup for text does not find any suitable result, then the `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#getId()` will be printed. If the zone cannot be obtained then an exception is thrown unless the section of the formatter is optional.

During parsing, either the textual zone name, the zone ID or the offset is accepted. Many textual zone names are not unique, such as CST can be for both "Central Standard Time" and "China Standard Time". In this situation, the zone id will be determined by the region information from formatter's `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#getLocale()` and the standard zone id for that area, for example, America/New_York for the America Eastern zone. This method also allows a set of preferred `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#` to be specified for parsing. The matched preferred zone id will be used if the textural zone name being parsed is not unique.

If the zone cannot be parsed then an exception is thrown unless the section of the formatter is optional.

| Parameters ||
|---|---|
| `textStyle` | [TextStyle](TextStyle.md)!: the text style to use, not null |
| `preferredZones` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ZoneId](../java.time/ZoneId.md)!\>!: the set of preferred zone ids, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### getLocalizedDateTimePattern

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getLocalizedDateTimePattern(
    requestedTemplate: String, 
    chrono: Chronology, 
    locale: Locale
): String
```

Returns the formatting pattern for the requested template for a locale and chronology. The locale and chronology are used to lookup the locale specific format for the requested template.

Refer to `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendLocalized(kotlin.String)` for the detail of `requestedTemplate` argument.

| Parameters ||
|---|---|
| `requestedTemplate` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the requested template, not null |
| `chrono` | [Chronology](../java.time.chrono/Chronology.md): the Chronology, non-null |
| `locale` | [Locale](../java.util/Locale.md): the locale, non-null |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the locale and Chronology specific formatting pattern |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `requestedTemplate` does not match the regular expression syntax described in `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendLocalized(kotlin.String)`. |
| `java.time.DateTimeException` | if a match for the localized pattern for `requestedTemplate` is not available |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#appendLocalized(kotlin.String)`

### getLocalizedDateTimePattern

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getLocalizedDateTimePattern(
    dateStyle: FormatStyle!, 
    timeStyle: FormatStyle!, 
    chrono: Chronology!, 
    locale: Locale!
): String!
```

Gets the formatting pattern for date and time styles for a locale and chronology. The locale and chronology are used to lookup the locale specific format for the requested dateStyle and/or timeStyle.

| Parameters ||
|---|---|
| `dateStyle` | [FormatStyle](FormatStyle.md)!: the FormatStyle for the date, null for time-only pattern |
| `timeStyle` | [FormatStyle](FormatStyle.md)!: the FormatStyle for the time, null for date-only pattern |
| `chrono` | [Chronology](../java.time.chrono/Chronology.md)!: the Chronology, non-null |
| --- | --- |
| `locale` | [Locale](../java.util/Locale.md)!: the locale, non-null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the locale and Chronology specific formatting pattern |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if both dateStyle and timeStyle are null |

### optionalEnd

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun optionalEnd(): DateTimeFormatterBuilder!
```

Ends an optional section.

The output of formatting can include optional sections, which may be nested. An optional section is started by calling `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalStart()` and ended using this method (or at the end of the builder).

Calling this method without having previously called `optionalStart` will throw an exception. Calling this method immediately after calling `optionalStart` has no effect on the formatter other than ending the (empty) optional section.

All elements in the optional section are treated as optional. During formatting, the section is only output if data is available in the `TemporalAccessor` for all the elements in the section. During parsing, the whole section may be missing from the parsed string.

For example, consider a builder setup as `builder.appendValue(HOUR_OF_DAY,2).optionalStart().appendValue(MINUTE_OF_HOUR,2).optionalEnd()`. During formatting, the minute will only be output if its value can be obtained from the date-time. During parsing, the input will be successfully parsed whether the minute is present or not.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if there was no previous call to `optionalStart` |

### optionalStart

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun optionalStart(): DateTimeFormatterBuilder!
```

Mark the start of an optional section.

The output of formatting can include optional sections, which may be nested. An optional section is started by calling this method and ended by calling `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalEnd()` or by ending the build process.

All elements in the optional section are treated as optional. During formatting, the section is only output if data is available in the `TemporalAccessor` for all the elements in the section. During parsing, the whole section may be missing from the parsed string.

For example, consider a builder setup as `builder.appendValue(HOUR_OF_DAY,2).optionalStart().appendValue(MINUTE_OF_HOUR,2)`. The optional section ends automatically at the end of the builder. During formatting, the minute will only be output if its value can be obtained from the date-time. During parsing, the input will be successfully parsed whether the minute is present or not.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### padNext

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun padNext(padWidth: Int): DateTimeFormatterBuilder!
```

Causes the next added printer/parser to pad to a fixed width using a space.

This padding will pad to a fixed width using spaces.

During formatting, the decorated element will be output and then padded to the specified width. An exception will be thrown during formatting if the pad width is exceeded.

During parsing, the padding and decorated element are parsed. If parsing is lenient, then the pad width is treated as a maximum. The padding is parsed greedily. Thus, if the decorated element starts with the pad character, it will not be parsed.

| Parameters ||
|---|---|
| `padWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the pad width, 1 or greater |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if pad width is too small |

### padNext

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun padNext(
    padWidth: Int, 
    padChar: Char
): DateTimeFormatterBuilder!
```

Causes the next added printer/parser to pad to a fixed width.

This padding is intended for padding other than zero-padding. Zero-padding should be achieved using the appendValue methods.

During formatting, the decorated element will be output and then padded to the specified width. An exception will be thrown during formatting if the pad width is exceeded.

During parsing, the padding and decorated element are parsed. If parsing is lenient, then the pad width is treated as a maximum. If parsing is case insensitive, then the pad character is matched ignoring case. The padding is parsed greedily. Thus, if the decorated element starts with the pad character, it will not be parsed.

| Parameters ||
|---|---|
| `padWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the pad width, 1 or greater |
| `padChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the pad character |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if pad width is too small |

### parseCaseInsensitive

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parseCaseInsensitive(): DateTimeFormatterBuilder!
```

Changes the parse style to be case insensitive for the remainder of the formatter.

Parsing can be case sensitive or insensitive - by default it is case sensitive. This method allows the case sensitivity setting of parsing to be changed.

Calling this method changes the state of the builder such that all subsequent builder method calls will parse text in case insensitive mode. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseCaseSensitive()` for the opposite setting. The parse case sensitive/insensitive methods may be called at any point in the builder, thus the parser can swap between case parsing modes multiple times during the parse.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### parseCaseSensitive

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parseCaseSensitive(): DateTimeFormatterBuilder!
```

Changes the parse style to be case sensitive for the remainder of the formatter.

Parsing can be case sensitive or insensitive - by default it is case sensitive. This method allows the case sensitivity setting of parsing to be changed.

Calling this method changes the state of the builder such that all subsequent builder method calls will parse text in case sensitive mode. See `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseCaseInsensitive()` for the opposite setting. The parse case sensitive/insensitive methods may be called at any point in the builder, thus the parser can swap between case parsing modes multiple times during the parse.

Since the default is case sensitive, this method should only be used after a previous call to `parseCaseInsensitive`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### parseDefaulting

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parseDefaulting(
    field: TemporalField!, 
    value: Long
): DateTimeFormatterBuilder!
```

Appends a default value for a field to the formatter for use in parsing.

This appends an instruction to the builder to inject a default value into the parsed result. This is especially useful in conjunction with optional parts of the formatter.

For example, consider a formatter that parses the year, followed by an optional month, with a further optional day-of-month. Using such a formatter would require the calling code to check whether a full date, year-month or just a year had been parsed. This method can be used to default the month and day-of-month to a sensible value, such as the first of the month, allowing the calling code to always get a date.

During formatting, this method has no effect.

During parsing, the current state of the parse is inspected. If the specified field has no associated value, because it has not been parsed successfully at that point, then the specified value is injected into the parse result. Injection is immediate, thus the field-value pair will be visible to any subsequent elements in the formatter. As such, this method is normally called at the end of the builder.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to default the value of, not null |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to default the field to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### parseLenient

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parseLenient(): DateTimeFormatterBuilder!
```

Changes the parse style to be lenient for the remainder of the formatter. Note that case sensitivity is set separately to this method.

Parsing can be strict or lenient - by default it is strict. This controls the degree of flexibility in matching the text and sign styles. Applications calling this method should typically also call `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseCaseInsensitive()`.

When used, this method changes the parsing to be lenient from this point onwards. The change will remain in force until the end of the formatter that is eventually constructed or until `parseStrict` is called.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### parseStrict

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parseStrict(): DateTimeFormatterBuilder!
```

Changes the parse style to be strict for the remainder of the formatter.

Parsing can be strict or lenient - by default it is strict. This controls the degree of flexibility in matching the text and sign styles.

When used, this method changes the parsing to be strict from this point onwards. As strict is the default, this is normally only needed after calling `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#parseLenient()`. The change will remain in force until the end of the formatter that is eventually constructed or until `parseLenient` is called.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#!` | this, for chaining, not null |

### toFormatter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toFormatter(): DateTimeFormatter!
```

Completes this builder by creating the `DateTimeFormatter` using the default locale.

This will create a formatter with the [default FORMAT locale](../java.util/Locale.md)). Numbers will be printed and parsed using the standard DecimalStyle. The resolver style will be `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle`.

Calling this method will end any open optional sections by repeatedly calling `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalEnd()` before creating the formatter.

This builder can still be used after creating the formatter if desired, although the state may have been changed by calls to `optionalEnd`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!` | the created formatter, not null |

### toFormatter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toFormatter(locale: Locale!): DateTimeFormatter!
```

Completes this builder by creating the `DateTimeFormatter` using the specified locale.

This will create a formatter with the specified locale. Numbers will be printed and parsed using the standard DecimalStyle. The resolver style will be `https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle`.

Calling this method will end any open optional sections by repeatedly calling `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatterBuilder#optionalEnd()` before creating the formatter.

This builder can still be used after creating the formatter if desired, although the state may have been changed by calls to `optionalEnd`.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the locale to use for formatting, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!` | the created formatter, not null |
