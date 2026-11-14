Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JapaneseChronology

```
class JapaneseChronology : AbstractChronology, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.time.chrono.AbstractChronology](AbstractChronology.md) ||
| | ↳ | [java.time.chrono.JapaneseChronology](JapaneseChronology.md) |

The Japanese Imperial calendar system.

This chronology defines the rules of the Japanese Imperial calendar system. This calendar system is primarily used in Japan. The Japanese Imperial calendar system is the same as the ISO calendar system apart from the era-based year numbering.

Japan introduced the Gregorian calendar starting with Meiji 6. Only Meiji and later eras are supported; dates before Meiji 6, January 1 are not supported.

The supported `ChronoField` instances are:

- `DAY_OF_WEEK`
- `DAY_OF_MONTH`
- `DAY_OF_YEAR`
- `EPOCH_DAY`
- `MONTH_OF_YEAR`
- `PROLEPTIC_MONTH`
- `YEAR_OF_ERA`
- `YEAR`
- `ERA`

## Summary

| Public methods ||
|---|---|
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#date(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a local date in Japanese calendar system from the proleptic-year, month-of-year and day-of-month fields. |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#date(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a local date in Japanese calendar system from the era, year-of-era, month-of-year and day-of-month fields. |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#date(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains a local date in this chronology from another temporal object. |
| --- | --- |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#dateEpochDay(kotlin.Long)(epochDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains a local date in the Japanese calendar system from the epoch-day. |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#dateNow()()` Obtains the current local date in this chronology from the system clock in the default time-zone. |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#dateNow(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock.html#!)` Obtains the current local date in this chronology from the specified clock. |
| --- | --- |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#dateNow(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Obtains the current local date in this chronology from the system clock in the specified time-zone. |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#dateYearDay(kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a local date in Japanese calendar system from the proleptic-year and day-of-year fields. |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#dateYearDay(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a local date in Japanese calendar system from the era, year-of-era and day-of-year fields. |
| --- | --- |
| [JapaneseEra](JapaneseEra.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#eraOf(kotlin.Int)(eraValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the calendar system era object from the given numeric value. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Era](Era.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#eras()()` Gets the list of eras for the chronology. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#getCalendarType()()` Gets the calendar type of the underlying calendar system - 'japanese'. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#getId()()` Gets the ID of the chronology - 'Japanese'. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#isIsoBased()()` `JapaneseChronology` is an ISO based chronology, which supports fields in `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#`, such as `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#DAY_OF_QUARTER:java.time.temporal.TemporalField` and `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#QUARTER_OF_YEAR:java.time.temporal.TemporalField`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#isLeapYear(kotlin.Long)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Checks if the specified year is a leap year. |
| --- | --- |
| [ChronoLocalDateTime](ChronoLocalDateTime.md)\< [JapaneseDate](JapaneseDate.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#localDateTime(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains a local date-time in this chronology from another temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#prolepticYear(java.time.chrono.Era,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Calculates the proleptic-year given the era and year-of-era. |
| [ValueRange](../java.time.temporal/ValueRange.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#range(java.time.temporal.ChronoField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#!)` Gets the range of valid values for the specified field. |
| --- | --- |
| [JapaneseDate](JapaneseDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#resolveDate(kotlin.collections.MutableMap,%20java.time.format.ResolverStyle)(fieldValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>!, resolverStyle: https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle.html#!)` Resolves parsed `ChronoField` values into a date during parsing. |
| [ChronoZonedDateTime](ChronoZonedDateTime.md)\< [JapaneseDate](JapaneseDate.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#zonedDateTime(java.time.Instant,%20java.time.ZoneId)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!, zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Obtains a `ChronoZonedDateTime` in this chronology from an `Instant`. |
| [ChronoZonedDateTime](ChronoZonedDateTime.md)\< [JapaneseDate](JapaneseDate.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#zonedDateTime(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains a `ChronoZonedDateTime` in this chronology from another temporal object. |
| --- | --- |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/time/chrono/AbstractChronology` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/AbstractChronology#compareTo(java.time.chrono.Chronology)(other: https://developer.android.com/reference/kotlin/java/time/chrono/Chronology!)`

Compares this chronology to another chronology.

The comparison order first by the chronology ID string, then by any additional information specific to the subclass. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/AbstractChronology#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)`

Checks if this chronology is equal to another chronology.

The comparison is based on the entire state of the object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/AbstractChronology#hashCode()()`

A hash code for this chronology.

The hash code should be based on the entire state of the object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/AbstractChronology#toString()()`

Outputs this chronology as a `String`, using the chronology ID.

<br />

From class `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology` `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Obtains a local date in this chronology from the proleptic-year, month-of-year and day-of-month fields.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Obtains a local date in this chronology from the era, year-of-era, month-of-year and day-of-month fields.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)`

Obtains a local date in this chronology from another temporal object.

This obtains a date in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoLocalDate`.

The conversion typically uses the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` field, which is standardized across calendar systems.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::date`.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateEpochDay(kotlin.Long)(epochDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Obtains a local date in this chronology from the epoch-day.

The definition of `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` is the same for all calendar systems, thus it can be used for conversion.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow()()`

Obtains the current local date in this chronology from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#systemDefaultZone()` in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock.html#!)`

Obtains the current local date in this chronology from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock.html#`.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)`

Obtains the current local date in this chronology from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#system(java.time.ZoneId)` to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateYearDay(kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Obtains a local date in this chronology from the proleptic-year and day-of-year fields.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateYearDay(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Obtains a local date in this chronology from the era, year-of-era and day-of-year fields.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#epochSecond(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.time.ZoneOffset)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, zoneOffset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!)`

Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z.

The number of seconds is calculated using the proleptic-year, month, day-of-month, hour, minute, second, and zoneOffset.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#epochSecond(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.time.ZoneOffset)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, zoneOffset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!)`

Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z.

The number of seconds is calculated using the era, year-of-era, month, day-of-month, hour, minute, second, and zoneOffset.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/Era!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#eraOf(kotlin.Int)(eraValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Creates the chronology era object from the numeric value.

The era is, conceptually, the largest division of the time-line. Most calendar systems have a single epoch dividing the time-line into two eras. However, some have multiple eras, such as one for the reign of each leader. The exact meaning is determined by the chronology according to the following constraints.

The era in use at 1970-01-01 must have the value 1. Later eras must have sequentially higher values. Earlier eras must have sequentially lower values. Each chronology must refer to an enum or similar singleton to provide the era values.

This method returns the singleton era of the correct type for the specified era value.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/chrono/Era!>!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#eras()()`

Gets the list of eras for the chronology.

Most calendar systems have an era, within which the year has meaning. If the calendar system does not support the concept of eras, an empty list must be returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getCalendarType()()`

Gets the calendar type of the calendar system.

The calendar type is an identifier defined by the CLDR and *Unicode Locale Data Markup Language (LDML)* specifications to uniquely identify a calendar. The `getCalendarType` is the concatenation of the CLDR calendar type and the variant, if applicable, is appended separated by "-". The calendar type is used to lookup the `Chronology` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getDisplayName(java.time.format.TextStyle,%20java.util.Locale)(style: https://developer.android.com/reference/kotlin/java/time/format/TextStyle.html#!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)`

Gets the textual representation of this chronology.

This returns the textual name used to identify the chronology, suitable for presentation to the user. The parameters control the style of the returned text and the locale.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getId()()`

Gets the ID of the chronology.

The ID uniquely identifies the `Chronology`. It can be used to lookup the `Chronology` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#isIsoBased()()`

Checks if this chronology is ISO based.

An ISO based chronology has the same basic structure as the `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology`, i.e., the chronology has the same number of months, the number of days in each month, and day-of-year and leap years are the same as ISO chronology. It also supports the concept of week-based-year of ISO chronology. For example, the `https://developer.android.com/reference/kotlin/java/time/chrono/MinguoChronology`, `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology` and `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#` chronologies are ISO based.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#isLeapYear(kotlin.Long)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`

Checks if the specified year is a leap year.

A leap-year is a year of a longer length than normal. The exact meaning is determined by the chronology according to the following constraints.

- a leap-year must imply a year-length longer than a non leap-year.
- a chronology that does not support the concept of a year must return false.
- the correct result must be returned for all years within the valid range of years for the chronology.

Outside the range of valid years an implementation is free to return either a best guess or false. An implementation must not throw an exception, even if the year is outside the range of valid years.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#localDateTime(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)`

Obtains a local date-time in this chronology from another temporal object.

This obtains a date-time in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoLocalDateTime`.

The conversion extracts and combines the `ChronoLocalDate` and the `LocalTime` from the temporal object. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects. The result uses this chronology.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::localDateTime`.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#period(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(years: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, months: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, days: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Obtains a period for this chronology based on years, months and days.

This returns a period tied to this chronology using the specified years, months and days. All supplied chronologies use periods based on years, months and days, however the `ChronoPeriod` API allows the period to be represented using other units.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#prolepticYear(java.time.chrono.Era,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Calculates the proleptic-year given the era and year-of-era.

This combines the era and year-of-era into the single proleptic-year field.

If the chronology makes active use of eras, such as `JapaneseChronology` then the year-of-era will be validated against the era. For other chronologies, validation is optional.

<br />

`https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#range(java.time.temporal.ChronoField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#!)`

Gets the range of valid values for the specified field.

All fields can be expressed as a `long` integer. This method returns an object that describes the valid range for that value.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

This method will return a result whether or not the chronology supports the field.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#zonedDateTime(java.time.Instant,%20java.time.ZoneId)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!, zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)`

Obtains a `ChronoZonedDateTime` in this chronology from an `Instant`.

This obtains a zoned date-time with the same instant as that specified.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#zonedDateTime(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)`

Obtains a `ChronoZonedDateTime` in this chronology from another temporal object.

This obtains a zoned date-time in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoZonedDateTime`.

The conversion will first obtain a `ZoneId` from the temporal object, falling back to a `ZoneOffset` if necessary. It will then try to obtain an `Instant`, falling back to a `ChronoLocalDateTime` if necessary. The result will be either the combination of `ZoneId` or `ZoneOffset` with `Instant` or `ChronoLocalDateTime`. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects. The result uses this chronology.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::zonedDateTime`.

<br />

| Properties ||
|---|---|
| static [JapaneseChronology](JapaneseChronology.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#INSTANCE:java.time.chrono.JapaneseChronology` Singleton instance for Japanese chronology. |

## Public methods

### date

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun date(
    prolepticYear: Int, 
    month: Int, 
    dayOfMonth: Int
): JapaneseDate!
```

Obtains a local date in Japanese calendar system from the proleptic-year, month-of-year and day-of-month fields.

The Japanese proleptic year, month and day-of-month are the same as those in the ISO calendar system. They are not reset when the era changes.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the proleptic-year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the Japanese local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### date

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun date(
    era: Era!, 
    yearOfEra: Int, 
    month: Int, 
    dayOfMonth: Int
): JapaneseDate!
```

Obtains a local date in Japanese calendar system from the era, year-of-era, month-of-year and day-of-month fields.

The Japanese month and day-of-month are the same as those in the ISO calendar system. They are not reset when the era changes. For example:

```kotlin
6th Jan Showa 64 = ISO 1989-01-06
   7th Jan Showa 64 = ISO 1989-01-07
   8th Jan Heisei 1 = ISO 1989-01-08
   9th Jan Heisei 1 = ISO 1989-01-09
  
```

| Parameters ||
|---|---|
| `era` | [Era](Era.md)!: the Japanese era, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year-of-era |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year |
| --- | --- |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the Japanese local date, not null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the `era` is not a `JapaneseEra` |
| `java.time.DateTimeException` | if unable to create the date |

### date

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun date(temporal: TemporalAccessor!): JapaneseDate!
```

Obtains a local date in this chronology from another temporal object.

This obtains a date in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoLocalDate`.

The conversion typically uses the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` field, which is standardized across calendar systems.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::date`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the local date in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateEpochDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateEpochDay(epochDay: Long): JapaneseDate!
```

Obtains a local date in the Japanese calendar system from the epoch-day.

| Parameters ||
|---|---|
| `epochDay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the epoch day |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the Japanese local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateNow(): JapaneseDate!
```

Obtains the current local date in this chronology from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#systemDefaultZone()` in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the current local date using the system clock and default time-zone, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateNow(clock: Clock!): JapaneseDate!
```

Obtains the current local date in this chronology from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock.html#`.

| Parameters ||
|---|---|
| `clock` | [Clock](../java.time/Clock.md)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the current local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateNow(zone: ZoneId!): JapaneseDate!
```

Obtains the current local date in this chronology from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#system(java.time.ZoneId)` to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](../java.time/ZoneId.md)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the current local date using the system clock, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateYearDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateYearDay(
    prolepticYear: Int, 
    dayOfYear: Int
): JapaneseDate!
```

Obtains a local date in Japanese calendar system from the proleptic-year and day-of-year fields.

The day-of-year in this factory is expressed relative to the start of the proleptic year. The Japanese proleptic year and day-of-year are the same as those in the ISO calendar system. They are not reset when the era changes.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the proleptic-year |
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-year |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the Japanese local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateYearDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateYearDay(
    era: Era!, 
    yearOfEra: Int, 
    dayOfYear: Int
): JapaneseDate!
```

Obtains a local date in Japanese calendar system from the era, year-of-era and day-of-year fields.

The day-of-year in this factory is expressed relative to the start of the year-of-era. This definition changes the normal meaning of day-of-year only in those years where the year-of-era is reset to one due to a change in the era. For example:

```kotlin
6th Jan Showa 64 = day-of-year 6
   7th Jan Showa 64 = day-of-year 7
   8th Jan Heisei 1 = day-of-year 1
   9th Jan Heisei 1 = day-of-year 2
  
```

| Parameters ||
|---|---|
| `era` | [Era](Era.md)!: the Japanese era, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year-of-era |
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-year |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the Japanese local date, not null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the `era` is not a `JapaneseEra` |
| `java.time.DateTimeException` | if unable to create the date |

### eraOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun eraOf(eraValue: Int): JapaneseEra!
```

Returns the calendar system era object from the given numeric value. The numeric values supported by this method are the same as the numeric values supported by `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra#of(kotlin.Int)`.

| Parameters ||
|---|---|
| `eraValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the era value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra!` | the Japanese `Era` for the given numeric era value |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if `eraValue` is invalid |

### eras

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun eras(): MutableList<Era!>!
```

Gets the list of eras for the chronology.

Most calendar systems have an era, within which the year has meaning. If the calendar system does not support the concept of eras, an empty list must be returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/chrono/Era!>!` | the list of eras for the chronology, may be immutable, not null |

### getCalendarType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCalendarType(): String!
```

Gets the calendar type of the underlying calendar system - 'japanese'.

The calendar type is an identifier defined by the *Unicode Locale Data Markup Language (LDML)* specification. It can be used to lookup the `Chronology` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)`. It can also be used as part of a locale, accessible via `https://developer.android.com/reference/kotlin/java/util/Locale.html#getUnicodeLocaleType(kotlin.String)` with the key 'ca'.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the calendar system type - 'japanese' |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#getId()`

### getId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String!
```

Gets the ID of the chronology - 'Japanese'.

The ID uniquely identifies the `Chronology`. It can be used to lookup the `Chronology` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the chronology ID - 'Japanese' |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology#getCalendarType()`

### isIsoBased

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isIsoBased(): Boolean
```

`JapaneseChronology` is an ISO based chronology, which supports fields in `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#`, such as `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#DAY_OF_QUARTER:java.time.temporal.TemporalField` and `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#QUARTER_OF_YEAR:java.time.temporal.TemporalField`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#`

### isLeapYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeapYear(prolepticYear: Long): Boolean
```

Checks if the specified year is a leap year.

Japanese calendar leap years occur exactly in line with ISO leap years. This method does not validate the year passed in, and only has a well-defined result for years in the supported range.

| Parameters ||
|---|---|
| `prolepticYear` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the proleptic-year to check, not validated for range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the year is a leap year |

### localDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun localDateTime(temporal: TemporalAccessor!): ChronoLocalDateTime<JapaneseDate!>!
```

Obtains a local date-time in this chronology from another temporal object.

This obtains a date-time in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoLocalDateTime`.

The conversion extracts and combines the `ChronoLocalDate` and the `LocalTime` from the temporal object. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects. The result uses this chronology.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::localDateTime`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime<https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!>!` | the local date-time in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date-time |

### prolepticYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun prolepticYear(
    era: Era!, 
    yearOfEra: Int
): Int
```

Calculates the proleptic-year given the era and year-of-era.

This combines the era and year-of-era into the single proleptic-year field.

If the chronology makes active use of eras, such as `JapaneseChronology` then the year-of-era will be validated against the era. For other chronologies, validation is optional.

| Parameters ||
|---|---|
| `era` | [Era](Era.md)!: the era of the correct type for the chronology, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology year-of-era |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the proleptic-year |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the `era` is not of the correct type for the chronology |
| `java.time.DateTimeException` | if unable to convert to a proleptic-year, such as if the year is invalid for the era |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun range(field: ChronoField!): ValueRange!
```

Gets the range of valid values for the specified field.

All fields can be expressed as a `long` integer. This method returns an object that describes the valid range for that value.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

This method will return a result whether or not the chronology supports the field.

| Parameters ||
|---|---|
| `field` | [ChronoField](../java.time.temporal/ChronoField.md)!: the field to get the range for, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#!` | the range of valid values for the field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |

### resolveDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun resolveDate(
    fieldValues: MutableMap<TemporalField!, Long!>!, 
    resolverStyle: ResolverStyle!
): JapaneseDate!
```

Resolves parsed `ChronoField` values into a date during parsing.

Most `TemporalField` implementations are resolved using the resolve method on the field. By contrast, the `ChronoField` class defines fields that only have meaning relative to the chronology. As such, `ChronoField` date fields are resolved here in the context of a specific chronology.

`ChronoField` instances are resolved by this method, which may be overridden in subclasses.

- `EPOCH_DAY` - If present, this is converted to a date and all other date fields are then cross-checked against the date.
- `PROLEPTIC_MONTH` - If present, then it is split into the `YEAR` and `MONTH_OF_YEAR`. If the mode is strict or smart then the field is validated.
- `YEAR_OF_ERA` and `ERA` - If both are present, then they are combined to form a `YEAR`. In lenient mode, the `YEAR_OF_ERA` range is not validated, in smart and strict mode it is. The `ERA` is validated for range in all three modes. If only the `YEAR_OF_ERA` is present, and the mode is smart or lenient, then the last available era is assumed. In strict mode, no era is assumed and the `YEAR_OF_ERA` is left untouched. If only the `ERA` is present, then it is left untouched.
- `YEAR`, `MONTH_OF_YEAR` and `DAY_OF_MONTH` - If all three are present, then they are combined to form a date. In all three modes, the `YEAR` is validated. If the mode is smart or strict, then the month and day are validated. If the mode is lenient, then the date is combined in a manner equivalent to creating a date on the first day of the first month in the requested year, then adding the difference in months, then the difference in days. If the mode is smart, and the day-of-month is greater than the maximum for the year-month, then the day-of-month is adjusted to the last day-of-month. If the mode is strict, then the three fields must form a valid date.
- `YEAR` and `DAY_OF_YEAR` - If both are present, then they are combined to form a date. In all three modes, the `YEAR` is validated. If the mode is lenient, then the date is combined in a manner equivalent to creating a date on the first day of the requested year, then adding the difference in days. If the mode is smart or strict, then the two fields must form a valid date.
- `YEAR`, `MONTH_OF_YEAR`, `ALIGNED_WEEK_OF_MONTH` and `ALIGNED_DAY_OF_WEEK_IN_MONTH` - If all four are present, then they are combined to form a date. In all three modes, the `YEAR` is validated. If the mode is lenient, then the date is combined in a manner equivalent to creating a date on the first day of the first month in the requested year, then adding the difference in months, then the difference in weeks, then in days. If the mode is smart or strict, then the all four fields are validated to their outer ranges. The date is then combined in a manner equivalent to creating a date on the first day of the requested year and month, then adding the amount in weeks and days to reach their values. If the mode is strict, the date is additionally validated to check that the day and week adjustment did not change the month.
- `YEAR`, `MONTH_OF_YEAR`, `ALIGNED_WEEK_OF_MONTH` and `DAY_OF_WEEK` - If all four are present, then they are combined to form a date. The approach is the same as described above for years, months and weeks in `ALIGNED_DAY_OF_WEEK_IN_MONTH`. The day-of-week is adjusted as the next or same matching day-of-week once the years, months and weeks have been handled.
- `YEAR`, `ALIGNED_WEEK_OF_YEAR` and `ALIGNED_DAY_OF_WEEK_IN_YEAR` - If all three are present, then they are combined to form a date. In all three modes, the `YEAR` is validated. If the mode is lenient, then the date is combined in a manner equivalent to creating a date on the first day of the requested year, then adding the difference in weeks, then in days. If the mode is smart or strict, then the all three fields are validated to their outer ranges. The date is then combined in a manner equivalent to creating a date on the first day of the requested year, then adding the amount in weeks and days to reach their values. If the mode is strict, the date is additionally validated to check that the day and week adjustment did not change the year.
- `YEAR`, `ALIGNED_WEEK_OF_YEAR` and `DAY_OF_WEEK` - If all three are present, then they are combined to form a date. The approach is the same as described above for years and weeks in `ALIGNED_DAY_OF_WEEK_IN_YEAR`. The day-of-week is adjusted as the next or same matching day-of-week once the years and weeks have been handled.

The default implementation is suitable for most calendar systems. If `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` is found without an `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` then the last era in `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#eras()` is used. The implementation assumes a 7 day week, that the first day-of-month has the value 1, that first day-of-year has the value 1, and that the first of the month and year always exists.

| Parameters ||
|---|---|
| `fieldValues` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [TemporalField](../java.time.temporal/TemporalField.md)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>!: the map of fields to values, which can be updated, not null |
| `resolverStyle` | [ResolverStyle](../java.time.format/ResolverStyle.md)!: the requested type of resolve, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!` | the resolved date, null if insufficient information to create a date |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the date cannot be resolved, typically because of a conflict in the input data |

### zonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun zonedDateTime(
    instant: Instant!, 
    zone: ZoneId!
): ChronoZonedDateTime<JapaneseDate!>!
```

Obtains a `ChronoZonedDateTime` in this chronology from an `Instant`.

This obtains a zoned date-time with the same instant as that specified.

| Parameters ||
|---|---|
| `instant` | [Instant](../java.time/Instant.md)!: the instant to create the date-time from, not null |
| `zone` | [ZoneId](../java.time/ZoneId.md)!: the time-zone, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime<https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!>!` | the zoned date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### zonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun zonedDateTime(temporal: TemporalAccessor!): ChronoZonedDateTime<JapaneseDate!>!
```

Obtains a `ChronoZonedDateTime` in this chronology from another temporal object.

This obtains a zoned date-time in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoZonedDateTime`.

The conversion will first obtain a `ZoneId` from the temporal object, falling back to a `ZoneOffset` if necessary. It will then try to obtain an `Instant`, falling back to a `ChronoLocalDateTime` if necessary. The result will be either the combination of `ZoneId` or `ZoneOffset` with `Instant` or `ChronoLocalDateTime`. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects. The result uses this chronology.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::zonedDateTime`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime<https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate!>!` | the zoned date-time in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date-time |

## Properties

### INSTANCE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTANCE: JapaneseChronology!
```

Singleton instance for Japanese chronology.
