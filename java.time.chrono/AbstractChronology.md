Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractChronology

```
abstract class AbstractChronology : Chronology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.chrono.AbstractChronology](AbstractChronology.md) |

Known Direct Subclasses [HijrahChronology](HijrahChronology.md), [IsoChronology](IsoChronology.md), [JapaneseChronology](JapaneseChronology.md), [MinguoChronology](MinguoChronology.md), [ThaiBuddhistChronology](ThaiBuddhistChronology.md) [HijrahChronology](HijrahChronology.md) The Hijrah calendar is a lunar calendar supporting Islamic calendars.
[IsoChronology](IsoChronology.md) The ISO calendar system.
[JapaneseChronology](JapaneseChronology.md) The Japanese Imperial calendar system.
[MinguoChronology](MinguoChronology.md) The Minguo calendar system.
[ThaiBuddhistChronology](ThaiBuddhistChronology.md) The Thai Buddhist calendar system.

An abstract implementation of a calendar system, used to organize and identify dates.

The main date and time API is built on the ISO calendar system. The chronology operates behind the scenes to represent the general concept of a calendar system.

See Chronology for more details.

## Summary

| Protected constructors ||
|---|---|
| AbstractChronology Creates an instance. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares this chronology to another chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Checks if this chronology is equal to another chronology. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode A hash code for this chronology. |
| --- | --- |
| open [ChronoLocalDate](ChronoLocalDate.md)! | resolveDate Resolves parsed `ChronoField` values into a date during parsing. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Outputs this chronology as a `String`, using the chronology ID. |

Inherited functions From class Chronology `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` date

Obtains a local date in this chronology from the proleptic-year, month-of-year and day-of-month fields.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` date

Obtains a local date in this chronology from the era, year-of-era, month-of-year and day-of-month fields.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` date

Obtains a local date in this chronology from another temporal object.

This obtains a date in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoLocalDate`.

The conversion typically uses the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` field, which is standardized across calendar systems.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::date`.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` dateEpochDay

Obtains a local date in this chronology from the epoch-day.

The definition of `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` is the same for all calendar systems, thus it can be used for conversion.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` dateNow

Obtains the current local date in this chronology from the system clock in the default time-zone.

This will query the systemDefaultZone in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` dateNow

Obtains the current local date in this chronology from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock.html#`.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` dateNow

Obtains the current local date in this chronology from the system clock in the specified time-zone.

This will query the system to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` dateYearDay

Obtains a local date in this chronology from the proleptic-year and day-of-year fields.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` dateYearDay

Obtains a local date in this chronology from the era, year-of-era and day-of-year fields.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` epochSecond

Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z.

The number of seconds is calculated using the proleptic-year, month, day-of-month, hour, minute, second, and zoneOffset.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` epochSecond

Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z.

The number of seconds is calculated using the era, year-of-era, month, day-of-month, hour, minute, second, and zoneOffset.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/Era!` eraOf

Creates the chronology era object from the numeric value.

The era is, conceptually, the largest division of the time-line. Most calendar systems have a single epoch dividing the time-line into two eras. However, some have multiple eras, such as one for the reign of each leader. The exact meaning is determined by the chronology according to the following constraints.

The era in use at 1970-01-01 must have the value 1. Later eras must have sequentially higher values. Earlier eras must have sequentially lower values. Each chronology must refer to an enum or similar singleton to provide the era values.

This method returns the singleton era of the correct type for the specified era value.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/chrono/Era!>!` eras

Gets the list of eras for the chronology.

Most calendar systems have an era, within which the year has meaning. If the calendar system does not support the concept of eras, an empty list must be returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` getCalendarType

Gets the calendar type of the calendar system.

The calendar type is an identifier defined by the CLDR and *Unicode Locale Data Markup Language (LDML)* specifications to uniquely identify a calendar. The `getCalendarType` is the concatenation of the CLDR calendar type and the variant, if applicable, is appended separated by "-". The calendar type is used to lookup the `Chronology` using of.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` getDisplayName

Gets the textual representation of this chronology.

This returns the textual name used to identify the chronology, suitable for presentation to the user. The parameters control the style of the returned text and the locale.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` getId

Gets the ID of the chronology.

The ID uniquely identifies the `Chronology`. It can be used to lookup the `Chronology` using of.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isIsoBased

Checks if this chronology is ISO based.

An ISO based chronology has the same basic structure as the IsoChronology, i.e., the chronology has the same number of months, the number of days in each month, and day-of-year and leap years are the same as ISO chronology. It also supports the concept of week-based-year of ISO chronology. For example, the MinguoChronology, ThaiBuddhistChronology and JapaneseChronology chronologies are ISO based.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isLeapYear

Checks if the specified year is a leap year.

A leap-year is a year of a longer length than normal. The exact meaning is determined by the chronology according to the following constraints.

- a leap-year must imply a year-length longer than a non leap-year.
- a chronology that does not support the concept of a year must return false.
- the correct result must be returned for all years within the valid range of years for the chronology.

Outside the range of valid years an implementation is free to return either a best guess or false. An implementation must not throw an exception, even if the year is outside the range of valid years.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` localDateTime

Obtains a local date-time in this chronology from another temporal object.

This obtains a date-time in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoLocalDateTime`.

The conversion extracts and combines the `ChronoLocalDate` and the `LocalTime` from the temporal object. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects. The result uses this chronology.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::localDateTime`.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod!` period

Obtains a period for this chronology based on years, months and days.

This returns a period tied to this chronology using the specified years, months and days. All supplied chronologies use periods based on years, months and days, however the `ChronoPeriod` API allows the period to be represented using other units.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` prolepticYear

Calculates the proleptic-year given the era and year-of-era.

This combines the era and year-of-era into the single proleptic-year field.

If the chronology makes active use of eras, such as `JapaneseChronology` then the year-of-era will be validated against the era. For other chronologies, validation is optional.

<br />

`https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#!` range

Gets the range of valid values for the specified field.

All fields can be expressed as a `long` integer. This method returns an object that describes the valid range for that value.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

This method will return a result whether or not the chronology supports the field.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` zonedDateTime

Obtains a `ChronoZonedDateTime` in this chronology from an `Instant`.

This obtains a zoned date-time with the same instant as that specified.

<br />

`https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` zonedDateTime

Obtains a `ChronoZonedDateTime` in this chronology from another temporal object.

This obtains a zoned date-time in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoZonedDateTime`.

The conversion will first obtain a `ZoneId` from the temporal object, falling back to a `ZoneOffset` if necessary. It will then try to obtain an `Instant`, falling back to a `ChronoLocalDateTime` if necessary. The result will be either the combination of `ZoneId` or `ZoneOffset` with `Instant` or `ChronoLocalDateTime`. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects. The result uses this chronology.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::zonedDateTime`.

<br />

## Protected constructors

### AbstractChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AbstractChronology()
```

Creates an instance.

## Public methods

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: Chronology!): Int
```

Compares this chronology to another chronology.

The comparison order first by the chronology ID string, then by any additional information specific to the subclass. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [Chronology](Chronology.md)!: the other chronology to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, that is this ID string compared with the `other`'s ID string |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Checks if this chronology is equal to another chronology.

The comparison is based on the entire state of the object.

| Parameters ||
|---|---|
| `obj` | the object to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is equal to the other chronology |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

A hash code for this chronology.

The hash code should be based on the entire state of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code |

### resolveDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveDate(
    fieldValues: MutableMap<TemporalField!, Long!>!, 
    resolverStyle: ResolverStyle!
): ChronoLocalDate!
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

The default implementation is suitable for most calendar systems. If `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` is found without an `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` then the last era in eras is used. The implementation assumes a 7 day week, that the first day-of-month has the value 1, that first day-of-year has the value 1, and that the first of the month and year always exists.

| Parameters ||
|---|---|
| `fieldValues` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [TemporalField](../java.time.temporal/TemporalField.md)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>!: the map of fields to values, which can be updated, not null |
| `resolverStyle` | [ResolverStyle](../java.time.format/ResolverStyle.md)!: the requested type of resolve, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the resolved date, null if insufficient information to create a date |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the date cannot be resolved, typically because of a conflict in the input data |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Outputs this chronology as a `String`, using the chronology ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this chronology, not null |
