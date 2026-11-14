Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IsoChronology

```
class IsoChronology : AbstractChronology, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.time.chrono.AbstractChronology](AbstractChronology.md) ||
| | ↳ | [java.time.chrono.IsoChronology](IsoChronology.md) |

The ISO calendar system.

This chronology defines the rules of the ISO calendar system. This calendar system is based on the ISO-8601 standard, which is the *de facto* world calendar.

The fields are defined as follows:

- era - There are two eras, 'Current Era' (CE) and 'Before Current Era' (BCE).
- year-of-era - The year-of-era is the same as the proleptic-year for the current CE era. For the BCE era before the ISO epoch the year increases from 1 upwards as time goes backwards.
- proleptic-year - The proleptic year is the same as the year-of-era for the current era. For the previous era, years have zero, then negative values.
- month-of-year - There are 12 months in an ISO year, numbered from 1 to 12.
- day-of-month - There are between 28 and 31 days in each of the ISO month, numbered from 1 to 31. Months 4, 6, 9 and 11 have 30 days, Months 1, 3, 5, 7, 8, 10 and 12 have 31 days. Month 2 has 28 days, or 29 in a leap year.
- day-of-year - There are 365 days in a standard ISO year and 366 in a leap year. The days are numbered from 1 to 365 or 1 to 366.
- leap-year - Leap years occur every 4 years, except where the year is divisble by 100 and not divisble by 400.

## Summary

| Public methods ||
|---|---|
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#date(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an ISO local date from the proleptic-year, month-of-year and day-of-month fields. |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#date(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an ISO local date from the era, year-of-era, month-of-year and day-of-month fields. |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#date(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains an ISO local date from another date-time object. |
| --- | --- |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#dateEpochDay(kotlin.Long)(epochDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains an ISO local date from the epoch-day. |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#dateNow()()` Obtains the current ISO local date from the system clock in the default time-zone. |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#dateNow(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock.html#!)` Obtains the current ISO local date from the specified clock. |
| --- | --- |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#dateNow(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Obtains the current ISO local date from the system clock in the specified time-zone. |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#dateYearDay(kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an ISO local date from the proleptic-year and day-of-year fields. |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#dateYearDay(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an ISO local date from the era, year-of-era and day-of-year fields. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#epochSecond(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.time.ZoneOffset)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, zoneOffset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!)` Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z. |
| [IsoEra](IsoEra.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#eraOf(kotlin.Int)(eraValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates the chronology era object from the numeric value. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Era](Era.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#eras()()` Gets the list of eras for the chronology. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#getCalendarType()()` Gets the calendar type of the underlying calendar system - 'iso8601'. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#getId()()` Gets the ID of the chronology - 'ISO'. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#isIsoBased()()` `IsoChronology` is an ISO based chronology, which supports fields in `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#`, such as `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#DAY_OF_QUARTER:java.time.temporal.TemporalField` and `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#QUARTER_OF_YEAR:java.time.temporal.TemporalField`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#isLeapYear(kotlin.Long)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Checks if the year is a leap year, according to the ISO proleptic calendar system rules. |
| [LocalDateTime](../java.time/LocalDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#localDateTime(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains an ISO local date-time from another date-time object. |
| [Period](../java.time/Period.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#period(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(years: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, months: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, days: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a period for this chronology based on years, months and days. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#prolepticYear(java.time.chrono.Era,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Calculates the proleptic-year given the era and year-of-era. |
| [ValueRange](../java.time.temporal/ValueRange.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#range(java.time.temporal.ChronoField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#!)` Gets the range of valid values for the specified field. |
| [LocalDate](../java.time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#resolveDate(kotlin.collections.MutableMap,%20java.time.format.ResolverStyle)(fieldValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>!, resolverStyle: https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle.html#!)` Resolves parsed `ChronoField` values into a date during parsing. |
| --- | --- |
| [ZonedDateTime](../java.time/ZonedDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#zonedDateTime(java.time.Instant,%20java.time.ZoneId)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!, zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Obtains an ISO zoned date-time in this chronology from an `Instant`. |
| [ZonedDateTime](../java.time/ZonedDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#zonedDateTime(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains an ISO zoned date-time from another date-time object. |

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

An ISO based chronology has the same basic structure as the `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#`, i.e., the chronology has the same number of months, the number of days in each month, and day-of-year and leap years are the same as ISO chronology. It also supports the concept of week-based-year of ISO chronology. For example, the `https://developer.android.com/reference/kotlin/java/time/chrono/MinguoChronology`, `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology` and `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology` chronologies are ISO based.

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
| static [IsoChronology](IsoChronology.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#INSTANCE:java.time.chrono.IsoChronology` Singleton instance of the ISO chronology. |

## Public methods

### date

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun date(
    prolepticYear: Int, 
    month: Int, 
    dayOfMonth: Int
): LocalDate!
```

Obtains an ISO local date from the proleptic-year, month-of-year and day-of-month fields.

This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#of(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO proleptic-year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO month-of-year |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO day-of-month |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the ISO local date, not null |

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
): LocalDate!
```

Obtains an ISO local date from the era, year-of-era, month-of-year and day-of-month fields.

| Parameters ||
|---|---|
| `era` | [Era](Era.md)!: the ISO era, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO year-of-era |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO month-of-year |
| --- | --- |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO day-of-month |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the ISO local date, not null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of `era` is not `IsoEra` |
| `java.time.DateTimeException` | if unable to create the date |

### date

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun date(temporal: TemporalAccessor!): LocalDate!
```

Obtains an ISO local date from another date-time object.

This is equivalent to java.time.LocalDate#from(java.time.temporal.TemporalAccessor).

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the date-time object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the ISO local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateEpochDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateEpochDay(epochDay: Long): LocalDate!
```

Obtains an ISO local date from the epoch-day.

This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#ofEpochDay(kotlin.Long)`.

| Parameters ||
|---|---|
| `epochDay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the epoch day |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the ISO local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateNow(): LocalDate!
```

Obtains the current ISO local date from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#systemDefaultZone()` in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the current ISO local date using the system clock and default time-zone, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateNow(clock: Clock!): LocalDate!
```

Obtains the current ISO local date from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock.html#`.

| Parameters ||
|---|---|
| `clock` | [Clock](../java.time/Clock.md)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the current ISO local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateNow(zone: ZoneId!): LocalDate!
```

Obtains the current ISO local date from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#system(java.time.ZoneId)` to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](../java.time/ZoneId.md)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the current ISO local date using the system clock, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateYearDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dateYearDay(
    prolepticYear: Int, 
    dayOfYear: Int
): LocalDate!
```

Obtains an ISO local date from the proleptic-year and day-of-year fields.

This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#ofYearDay(kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO proleptic-year |
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO day-of-year |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the ISO local date, not null |

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
): LocalDate!
```

Obtains an ISO local date from the era, year-of-era and day-of-year fields.

| Parameters ||
|---|---|
| `era` | [Era](Era.md)!: the ISO era, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO year-of-era |
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO day-of-year |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the ISO local date, not null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the `era` is not of the correct type for the chronology |
| `java.time.DateTimeException` | if unable to create the date |

### epochSecond

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun epochSecond(
    prolepticYear: Int, 
    month: Int, 
    dayOfMonth: Int, 
    hour: Int, 
    minute: Int, 
    second: Int, 
    zoneOffset: ZoneOffset!
): Long
```

Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z.

The number of seconds is calculated using the year, month, day-of-month, hour, minute, second, and zoneOffset.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year, from MIN_YEAR to MAX_YEAR |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year, from 1 to 12 |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month, from 1 to 31 |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute, from 0 to 59 |
| --- | --- |
| `zoneOffset` | [ZoneOffset](../java.time/ZoneOffset.md)!: the zone offset, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of seconds relative to 1970-01-01T00:00:00Z, may be negative |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any argument is out of range, or if the day-of-month is invalid for the month-of-year |

### eraOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun eraOf(eraValue: Int): IsoEra!
```

Creates the chronology era object from the numeric value.

The era is, conceptually, the largest division of the time-line. Most calendar systems have a single epoch dividing the time-line into two eras. However, some have multiple eras, such as one for the reign of each leader. The exact meaning is determined by the chronology according to the following constraints.

The era in use at 1970-01-01 must have the value 1. Later eras must have sequentially higher values. Earlier eras must have sequentially lower values. Each chronology must refer to an enum or similar singleton to provide the era values.

This method returns the singleton era of the correct type for the specified era value.

| Parameters ||
|---|---|
| `eraValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the era value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra!` | the calendar system era, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the era |

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

Gets the calendar type of the underlying calendar system - 'iso8601'.

The calendar type is an identifier defined by the *Unicode Locale Data Markup Language (LDML)* specification. It can be used to lookup the `Chronology` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)`. It can also be used as part of a locale, accessible via `https://developer.android.com/reference/kotlin/java/util/Locale.html#getUnicodeLocaleType(kotlin.String)` with the key 'ca'.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the calendar system type - 'iso8601' |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#getId()`

### getId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String!
```

Gets the ID of the chronology - 'ISO'.

The ID uniquely identifies the `Chronology`. It can be used to lookup the `Chronology` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the chronology ID - 'ISO' |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology#getCalendarType()`

### isIsoBased

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isIsoBased(): Boolean
```

`IsoChronology` is an ISO based chronology, which supports fields in `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#`, such as `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#DAY_OF_QUARTER:java.time.temporal.TemporalField` and `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#QUARTER_OF_YEAR:java.time.temporal.TemporalField`.

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

Checks if the year is a leap year, according to the ISO proleptic calendar system rules.

This method applies the current rules for leap years across the whole time-line. In general, a year is a leap year if it is divisible by four without remainder. However, years divisible by 100, are not leap years, with the exception of years divisible by 400 which are.

For example, 1904 is a leap year it is divisible by 4. 1900 was not a leap year as it is divisible by 100, however 2000 was a leap year as it is divisible by 400.

The calculation is proleptic - applying the same rules into the far future and far past. This is historically inaccurate, but is correct for the ISO-8601 standard.

| Parameters ||
|---|---|
| `prolepticYear` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the ISO proleptic year to check |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the year is leap, false otherwise |

### localDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun localDateTime(temporal: TemporalAccessor!): LocalDateTime!
```

Obtains an ISO local date-time from another date-time object.

This is equivalent to java.time.LocalDateTime#from(java.time.temporal.TemporalAccessor).

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the date-time object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!` | the ISO local date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date-time |

### period

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun period(
    years: Int, 
    months: Int, 
    days: Int
): Period!
```

Obtains a period for this chronology based on years, months and days.

This returns a period tied to the ISO chronology using the specified years, months and days. See `https://developer.android.com/reference/kotlin/java/time/Period.html#` for further details.

| Parameters ||
|---|---|
| `years` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of years, may be negative |
| `months` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of years, may be negative |
| `days` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of years, may be negative |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Period.html#!` | the ISO period, not null |

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
): LocalDate!
```

Resolves parsed `ChronoField` values into a date during parsing.

Most `TemporalField` implementations are resolved using the resolve method on the field. By contrast, the `ChronoField` class defines fields that only have meaning relative to the chronology. As such, `ChronoField` date fields are resolved here in the context of a specific chronology.

`ChronoField` instances on the ISO calendar system are resolved as follows.

- `EPOCH_DAY` - If present, this is converted to a `LocalDate` and all other date fields are then cross-checked against the date.
- `PROLEPTIC_MONTH` - If present, then it is split into the `YEAR` and `MONTH_OF_YEAR`. If the mode is strict or smart then the field is validated.
- `YEAR_OF_ERA` and `ERA` - If both are present, then they are combined to form a `YEAR`. In lenient mode, the `YEAR_OF_ERA` range is not validated, in smart and strict mode it is. The `ERA` is validated for range in all three modes. If only the `YEAR_OF_ERA` is present, and the mode is smart or lenient, then the current era (CE/AD) is assumed. In strict mode, no era is assumed and the `YEAR_OF_ERA` is left untouched. If only the `ERA` is present, then it is left untouched.
- `YEAR`, `MONTH_OF_YEAR` and `DAY_OF_MONTH` - If all three are present, then they are combined to form a `LocalDate`. In all three modes, the `YEAR` is validated. If the mode is smart or strict, then the month and day are validated, with the day validated from 1 to 31. If the mode is lenient, then the date is combined in a manner equivalent to creating a date on the first of January in the requested year, then adding the difference in months, then the difference in days. If the mode is smart, and the day-of-month is greater than the maximum for the year-month, then the day-of-month is adjusted to the last day-of-month. If the mode is strict, then the three fields must form a valid date.
- `YEAR` and `DAY_OF_YEAR` - If both are present, then they are combined to form a `LocalDate`. In all three modes, the `YEAR` is validated. If the mode is lenient, then the date is combined in a manner equivalent to creating a date on the first of January in the requested year, then adding the difference in days. If the mode is smart or strict, then the two fields must form a valid date.
- `YEAR`, `MONTH_OF_YEAR`, `ALIGNED_WEEK_OF_MONTH` and `ALIGNED_DAY_OF_WEEK_IN_MONTH` - If all four are present, then they are combined to form a `LocalDate`. In all three modes, the `YEAR` is validated. If the mode is lenient, then the date is combined in a manner equivalent to creating a date on the first of January in the requested year, then adding the difference in months, then the difference in weeks, then in days. If the mode is smart or strict, then the all four fields are validated to their outer ranges. The date is then combined in a manner equivalent to creating a date on the first day of the requested year and month, then adding the amount in weeks and days to reach their values. If the mode is strict, the date is additionally validated to check that the day and week adjustment did not change the month.
- `YEAR`, `MONTH_OF_YEAR`, `ALIGNED_WEEK_OF_MONTH` and `DAY_OF_WEEK` - If all four are present, then they are combined to form a `LocalDate`. The approach is the same as described above for years, months and weeks in `ALIGNED_DAY_OF_WEEK_IN_MONTH`. The day-of-week is adjusted as the next or same matching day-of-week once the years, months and weeks have been handled.
- `YEAR`, `ALIGNED_WEEK_OF_YEAR` and `ALIGNED_DAY_OF_WEEK_IN_YEAR` - If all three are present, then they are combined to form a `LocalDate`. In all three modes, the `YEAR` is validated. If the mode is lenient, then the date is combined in a manner equivalent to creating a date on the first of January in the requested year, then adding the difference in weeks, then in days. If the mode is smart or strict, then the all three fields are validated to their outer ranges. The date is then combined in a manner equivalent to creating a date on the first day of the requested year, then adding the amount in weeks and days to reach their values. If the mode is strict, the date is additionally validated to check that the day and week adjustment did not change the year.
- `YEAR`, `ALIGNED_WEEK_OF_YEAR` and `DAY_OF_WEEK` - If all three are present, then they are combined to form a `LocalDate`. The approach is the same as described above for years and weeks in `ALIGNED_DAY_OF_WEEK_IN_YEAR`. The day-of-week is adjusted as the next or same matching day-of-week once the years and weeks have been handled.

| Parameters ||
|---|---|
| `fieldValues` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [TemporalField](../java.time.temporal/TemporalField.md)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>!: the map of fields to values, which can be updated, not null |
| `resolverStyle` | [ResolverStyle](../java.time.format/ResolverStyle.md)!: the requested type of resolve, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!` | the resolved date, null if insufficient information to create a date |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the date cannot be resolved, typically because of a conflict in the input data |

### zonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun zonedDateTime(
    instant: Instant!, 
    zone: ZoneId!
): ZonedDateTime!
```

Obtains an ISO zoned date-time in this chronology from an `Instant`.

This is equivalent to `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#ofInstant(java.time.Instant,%20java.time.ZoneId)`.

| Parameters ||
|---|---|
| `instant` | [Instant](../java.time/Instant.md)!: the instant to create the date-time from, not null |
| `zone` | [ZoneId](../java.time/ZoneId.md)!: the time-zone, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#!` | the zoned date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### zonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun zonedDateTime(temporal: TemporalAccessor!): ZonedDateTime!
```

Obtains an ISO zoned date-time from another date-time object.

This is equivalent to java.time.ZonedDateTime#from(java.time.temporal.TemporalAccessor).

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the date-time object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#!` | the ISO zoned date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date-time |

## Properties

### INSTANCE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTANCE: IsoChronology!
```

Singleton instance of the ISO chronology.
