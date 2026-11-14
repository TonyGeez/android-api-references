Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalDate

```
class LocalDate : ChronoLocalDate, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.LocalDate](LocalDate.md) |

A date without a time-zone in the ISO-8601 calendar system, such as `2007-12-03`.

`LocalDate` is an immutable date-time object that represents a date, often viewed as year-month-day. Other date fields, such as day-of-year, day-of-week and week-of-year, can also be accessed. For example, the value "2nd October 2007" can be stored in a `LocalDate`.

This class does not store or represent a time or time-zone. Instead, it is a description of the date, as used for birthdays. It cannot represent an instant on the time-line without additional information such as an offset or time-zone.

The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. It is equivalent to the proleptic Gregorian calendar system, in which today's rules for leap years are applied for all time. For most applications written today, the ISO-8601 rules are entirely suitable. However, any application that makes use of historical dates, and requires them to be accurate will find the ISO-8601 approach unsuitable.

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](LocalDate.md)) as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. The `equals` method should be used for comparisons.

## Summary

| Public methods ||
|---|---|
| [Temporal](../java.time.temporal/Temporal.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#adjustInto(java.time.temporal.Temporal)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!)` Adjusts the specified temporal object to have the same date as this object. |
| [LocalDateTime](LocalDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#atStartOfDay()()` Combines this date with the time of midnight to create a `LocalDateTime` at the start of this date. |
| [ZonedDateTime](ZonedDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#atStartOfDay(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId!)` Returns a zoned date-time from this date at the earliest valid time according to the rules in the time-zone. |
| --- | --- |
| [LocalDateTime](LocalDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#atTime(kotlin.Int,%20kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Combines this date with a time to create a `LocalDateTime`. |
| [LocalDateTime](LocalDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#atTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Combines this date with a time to create a `LocalDateTime`. |
| [LocalDateTime](LocalDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#atTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, nanoOfSecond: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Combines this date with a time to create a `LocalDateTime`. |
| --- | --- |
| [LocalDateTime](LocalDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#atTime(java.time.LocalTime)(time: https://developer.android.com/reference/kotlin/java/time/LocalTime!)` Combines this date with a time to create a `LocalDateTime`. |
| [OffsetDateTime](OffsetDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#atTime(java.time.OffsetTime)(time: https://developer.android.com/reference/kotlin/java/time/OffsetTime!)` Combines this date with an offset time to create an `OffsetDateTime`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#compareTo(java.time.chrono.ChronoLocalDate)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Compares this date to another date. |
| --- | --- |
| [Stream](../java.util.stream/Stream.md)\< [LocalDate](LocalDate.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#datesUntil(java.time.LocalDate)(endExclusive: https://developer.android.com/reference/kotlin/java/time/LocalDate#!)` Returns a sequential ordered stream of dates. |
| [Stream](../java.util.stream/Stream.md)\< [LocalDate](LocalDate.md)!\>! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#datesUntil(java.time.LocalDate,%20java.time.Period)(endExclusive: https://developer.android.com/reference/kotlin/java/time/LocalDate#!, step: https://developer.android.com/reference/kotlin/java/time/Period!)` Returns a sequential ordered stream of dates by given incremental step. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks if this date is equal to another date. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#format(java.time.format.DateTimeFormatter)(formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Formats this date using the specified formatter. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Obtains an instance of `LocalDate` from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#get(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this date as an `int`. |
| --- | --- |
| [IsoChronology](../java.time.chrono/IsoChronology.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getChronology()()` Gets the chronology of this date, which is the ISO calendar system. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getDayOfMonth()()` Gets the day-of-month field. |
| [DayOfWeek](DayOfWeek.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getDayOfWeek()()` Gets the day-of-week field, which is an enum `DayOfWeek`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getDayOfYear()()` Gets the day-of-year field. |
| [Era](../java.time.chrono/Era.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getEra()()` Gets the era applicable at this date. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this date as a `long`. |
| --- | --- |
| [Month](Month.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getMonth()()` Gets the month-of-year field using the `Month` enum. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getMonthValue()()` Gets the month-of-year field from 1 to 12. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#getYear()()` Gets the year field. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#hashCode()()` A hash code for this date. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#isAfter(java.time.chrono.ChronoLocalDate)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Checks if this date is after the specified date. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#isBefore(java.time.chrono.ChronoLocalDate)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Checks if this date is before the specified date. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#isEqual(java.time.chrono.ChronoLocalDate)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Checks if this date is equal to the specified date. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#isLeapYear()()` Checks if the year is a leap year, according to the ISO proleptic calendar system rules. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Checks if the specified field is supported. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#isSupported(java.time.temporal.TemporalUnit)(unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Checks if the specified unit is supported. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#lengthOfMonth()()` Returns the length of the month represented by this date. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#lengthOfYear()()` Returns the length of the year represented by this date. |
| --- | --- |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#minus(java.time.temporal.TemporalAmount)(amountToSubtract: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount!)` Returns a copy of this date with the specified amount subtracted. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this date with the specified amount subtracted. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#minusDays(kotlin.Long)(daysToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalDate` with the specified number of days subtracted. |
| --- | --- |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#minusMonths(kotlin.Long)(monthsToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalDate` with the specified number of months subtracted. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#minusWeeks(kotlin.Long)(weeksToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalDate` with the specified number of weeks subtracted. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#minusYears(kotlin.Long)(yearsToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalDate` with the specified number of years subtracted. |
| --- | --- |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#now()()` Obtains the current date from the system clock in the default time-zone. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#now(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock!)` Obtains the current date from the specified clock. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#now(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId!)` Obtains the current date from the system clock in the specified time-zone. |
| --- | --- |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#of(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `LocalDate` from a year, month and day. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#of(kotlin.Int,%20java.time.Month,%20kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://developer.android.com/reference/kotlin/java/time/Month!, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `LocalDate` from a year, month and day. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#ofEpochDay(kotlin.Long)(epochDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains an instance of `LocalDate` from the epoch day count. |
| --- | --- |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#ofInstant(java.time.Instant,%20java.time.ZoneId)(instant: https://developer.android.com/reference/kotlin/java/time/Instant!, zone: https://developer.android.com/reference/kotlin/java/time/ZoneId!)` Obtains an instance of `LocalDate` from an `Instant` and zone ID. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#ofYearDay(kotlin.Int,%20kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `LocalDate` from a year and day-of-year. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#parse(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Obtains an instance of `LocalDate` from a text string such as `2007-12-03`. |
| --- | --- |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#parse(kotlin.CharSequence,%20java.time.format.DateTimeFormatter)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Obtains an instance of `LocalDate` from a text string using a specific formatter. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#plus(java.time.temporal.TemporalAmount)(amountToAdd: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount!)` Returns a copy of this date with the specified amount added. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this date with the specified amount added. |
| --- | --- |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusDays(kotlin.Long)(daysToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalDate` with the specified number of days added. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusMonths(kotlin.Long)(monthsToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalDate` with the specified number of months added. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusWeeks(kotlin.Long)(weeksToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalDate` with the specified number of weeks added. |
| --- | --- |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusYears(kotlin.Long)(yearsToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalDate` with the specified number of years added. |
| R | `https://developer.android.com/reference/kotlin/java/time/LocalDate#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<R>!)` Queries this date using the specified query. |
| [ValueRange](../java.time.temporal/ValueRange.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the range of valid values for the specified field. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#toEpochDay()()` Converts this date to the Epoch Day. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#toEpochSecond(java.time.LocalTime,%20java.time.ZoneOffset)(time: https://developer.android.com/reference/kotlin/java/time/LocalTime!, offset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset!)` Converts this `LocalDate` to the number of seconds since the epoch of 1970-01-01T00:00:00Z. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#toString()()` Outputs this date as a `String`, such as `2007-12-03`. |
| --- | --- |
| [Period](Period.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#until(java.time.chrono.ChronoLocalDate)(endDateExclusive: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Calculates the period between this date and another date as a `Period`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalDate#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit)(endExclusive: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Calculates the amount of time until another date in terms of the specified unit. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#with(java.time.temporal.TemporalAdjuster)(adjuster: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster!)` Returns an adjusted copy of this date. |
| --- | --- |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#with(java.time.temporal.TemporalField,%20kotlin.Long)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this date with the specified field set to a new value. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#withDayOfMonth(kotlin.Int)(dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `LocalDate` with the day-of-month altered. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#withDayOfYear(kotlin.Int)(dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `LocalDate` with the day-of-year altered. |
| --- | --- |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#withMonth(kotlin.Int)(month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `LocalDate` with the month-of-year altered. |
| [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#withYear(kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `LocalDate` with the year altered. |

| Properties ||
|---|---|
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#EPOCH:java.time.LocalDate` The epoch year `LocalDate`, '1970-01-01'. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#MAX:java.time.LocalDate` The maximum supported `LocalDate`, '+999999999-12-31'. |
| static [LocalDate](LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalDate#MIN:java.time.LocalDate` The minimum supported `LocalDate`, '-999999999-01-01'. |
| --- | --- |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same date as this object.

This returns a temporal object of the same observable type as the input with the date changed to be the same as this.

The adjustment is equivalent to using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long)` passing `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` as the field.

In most cases, it is clearer to reverse the calling pattern by using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisLocalDate.adjustInto(temporal);
    temporal = temporal.with(thisLocalDate);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `temporal` | [Temporal](../java.time.temporal/Temporal.md)!: the target object to be adjusted, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!` | the adjusted object, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if unable to make the adjustment |

### atStartOfDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atStartOfDay(): LocalDateTime!
```

Combines this date with the time of midnight to create a `LocalDateTime` at the start of this date.

This returns a `LocalDateTime` formed from this date at the time of midnight, 00:00, at the start of this date.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime!` | the local date-time of midnight at the start of this date, not null |

### atStartOfDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atStartOfDay(zone: ZoneId!): ZonedDateTime!
```

Returns a zoned date-time from this date at the earliest valid time according to the rules in the time-zone.

Time-zone rules, such as daylight savings, mean that not every local date-time is valid for the specified zone, thus the local date-time may not be midnight.

In most cases, there is only one valid offset for a local date-time. In the case of an overlap, there are two valid offsets, and the earlier one is used, corresponding to the first occurrence of midnight on the date. In the case of a gap, the zoned date-time will represent the instant just after the gap.

If the zone ID is a `https://developer.android.com/reference/kotlin/java/time/ZoneOffset`, then the result always has a time of midnight.

To convert to a specific time in a given time-zone call `https://developer.android.com/reference/kotlin/java/time/LocalDate#atTime(java.time.LocalTime)` followed by `https://developer.android.com/reference/kotlin/java/time/LocalDateTime#atZone(java.time.ZoneId)`.

| Parameters ||
|---|---|
| `zone` | [ZoneId](ZoneId.md)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime!` | the zoned date-time formed from this date and the earliest valid time for the zone, not null |

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atTime(
    hour: Int, 
    minute: Int
): LocalDateTime!
```

Combines this date with a time to create a `LocalDateTime`.

This returns a `LocalDateTime` formed from this date at the specified hour and minute. The seconds and nanosecond fields will be set to zero. The individual time fields must be within their valid range. All possible combinations of date and time are valid.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to use, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to use, from 0 to 59 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime!` | the local date-time formed from this date and the specified time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range |

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atTime(
    hour: Int, 
    minute: Int, 
    second: Int
): LocalDateTime!
```

Combines this date with a time to create a `LocalDateTime`.

This returns a `LocalDateTime` formed from this date at the specified hour, minute and second. The nanosecond field will be set to zero. The individual time fields must be within their valid range. All possible combinations of date and time are valid.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to use, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to use, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute to represent, from 0 to 59 |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime!` | the local date-time formed from this date and the specified time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range |

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atTime(
    hour: Int, 
    minute: Int, 
    second: Int, 
    nanoOfSecond: Int
): LocalDateTime!
```

Combines this date with a time to create a `LocalDateTime`.

This returns a `LocalDateTime` formed from this date at the specified hour, minute, second and nanosecond. The individual time fields must be within their valid range. All possible combinations of date and time are valid.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to use, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to use, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute to represent, from 0 to 59 |
| --- | --- |
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the nano-of-second to represent, from 0 to 999,999,999 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime!` | the local date-time formed from this date and the specified time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range |

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atTime(time: LocalTime!): LocalDateTime!
```

Combines this date with a time to create a `LocalDateTime`.

This returns a `LocalDateTime` formed from this date at the specified time. All possible combinations of date and time are valid.

| Parameters ||
|---|---|
| `localTime` | the local time to use, not null |
| `time` | [LocalTime](LocalTime.md)!: the time to combine with, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime!` | the local date-time formed from this date and the specified time, not null |

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atTime(time: OffsetTime!): OffsetDateTime!
```

Combines this date with an offset time to create an `OffsetDateTime`.

This returns an `OffsetDateTime` formed from this date at the specified time. All possible combinations of date and time are valid.

| Parameters ||
|---|---|
| `time` | [OffsetTime](OffsetTime.md)!: the time to combine with, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime!` | the offset date-time formed from this date and the specified time, not null |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: ChronoLocalDate!): Int
```

Compares this date to another date.

The comparison is primarily based on the date, from earliest to latest. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

If all the dates being compared are instances of `LocalDate`, then the comparison will be entirely based on the date. If some dates being compared are in different chronologies, then the chronology is also considered, see `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate)`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md)!: the other date to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, that is the comparison of this local date with the `other` local date and this chronology with the `other` chronology, in order, returning the first non-zero result, and otherwise returning zero |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/LocalDate#isBefore(java.time.chrono.ChronoLocalDate)`
- `https://developer.android.com/reference/kotlin/java/time/LocalDate#isAfter(java.time.chrono.ChronoLocalDate)`

### datesUntil

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun datesUntil(endExclusive: LocalDate!): Stream<LocalDate!>!
```

Returns a sequential ordered stream of dates. The returned stream starts from this date (inclusive) and goes to `endExclusive` (exclusive) by an incremental step of 1 day.

This method is equivalent to `datesUntil(endExclusive, Period.ofDays(1))`.

| Parameters ||
|---|---|
| `endExclusive` | [LocalDate](LocalDate.md)!: the end date, exclusive, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#<https://developer.android.com/reference/kotlin/java/time/LocalDate#!>!` | a sequential `Stream` for the range of `LocalDate` values |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if end date is before this date |

### datesUntil

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun datesUntil(
    endExclusive: LocalDate!, 
    step: Period!
): Stream<LocalDate!>!
```

Returns a sequential ordered stream of dates by given incremental step. The returned stream starts from this date (inclusive) and goes to `endExclusive` (exclusive).

The n-th date which appears in the stream is equal to `this.plus(step.multipliedBy(n))` (but the result of step multiplication never overflows). For example, if this date is `2015-01-31`, the end date is `2015-05-01` and the step is 1 month, then the stream contains `2015-01-31`, `2015-02-28`, `2015-03-31`, and `2015-04-30`.

| Parameters ||
|---|---|
| `endExclusive` | [LocalDate](LocalDate.md)!: the end date, exclusive, not null |
| `step` | [Period](Period.md)!: the non-zero, non-negative `Period` which represents the step. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#<https://developer.android.com/reference/kotlin/java/time/LocalDate#!>!` | a sequential `Stream` for the range of `LocalDate` values |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if step is zero, or `step.getDays()` and `step.toTotalMonths()` have opposite sign, or end date is before this date and step is positive, or end date is after this date and step is negative |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this date is equal to another date.

Compares this `LocalDate` with another ensuring that the date is the same.

Only objects of type `LocalDate` are compared, other types return false. To compare the dates of two `TemporalAccessor` instances, including dates in two different chronologies, use `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` as a comparator.

| Parameters ||
|---|---|
| `obj` | the object to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is equal to the other date |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(formatter: DateTimeFormatter!): String!
```

Formats this date using the specified formatter.

This date will be passed to the formatter to produce a string.

| Parameters ||
|---|---|
| `formatter` | [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the formatted date string, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): LocalDate!
```

Obtains an instance of `LocalDate` from a temporal object.

This obtains a local date based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `LocalDate`.

The conversion uses the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#localDate()` query, which relies on extracting the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` field.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery` allowing it to be used as a query via method reference, `LocalDate::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to a `LocalDate` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this date as an `int`.

This queries this date for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/LocalDate#isSupported(java.time.temporal.TemporalField)` will return valid values based on this date, except `EPOCH_DAY` and `PROLEPTIC_MONTH` which are too large to fit in an `int` and throw an `UnsupportedTemporalTypeException`. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an `int` |
| --- | --- |

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChronology(): IsoChronology!
```

Gets the chronology of this date, which is the ISO calendar system.

The `Chronology` represents the calendar system in use. The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. It is equivalent to the proleptic Gregorian calendar system, in which today's rules for leap years are applied for all time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology!` | the ISO chronology, not null |

### getDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDayOfMonth(): Int
```

Gets the day-of-month field.

This method returns the primitive `int` value for the day-of-month.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the day-of-month, from 1 to 31 |

### getDayOfWeek

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDayOfWeek(): DayOfWeek!
```

Gets the day-of-week field, which is an enum `DayOfWeek`.

This method returns the enum `https://developer.android.com/reference/kotlin/java/time/DayOfWeek` for the day-of-week. This avoids confusion as to what `int` values mean. If you need access to the primitive `int` value then the enum provides the `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#getValue()`.

Additional information can be obtained from the `DayOfWeek`. This includes textual names of the values.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek!` | the day-of-week, not null |

### getDayOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDayOfYear(): Int
```

Gets the day-of-year field.

This method returns the primitive `int` value for the day-of-year.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the day-of-year, from 1 to 365, or 366 in a leap year |

### getEra

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEra(): Era!
```

Gets the era applicable at this date.

The official ISO-8601 standard does not define eras, however `IsoChronology` does. It defines two eras, 'CE' from year one onwards and 'BCE' from year zero backwards. Since dates before the Julian-Gregorian cutover are not in line with history, the cutover between 'BCE' and 'CE' is also not aligned with the commonly used eras, often referred to using 'BC' and 'AD'.

Users of this class should typically ignore this method as it exists primarily to fulfill the `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate` contract where it is necessary to support the Japanese calendar system.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/Era!` | the IsoEra applicable at this date, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this date as a `long`.

This queries this date for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/LocalDate#isSupported(java.time.temporal.TemporalField)` will return valid values based on this date. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |

### getMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMonth(): Month!
```

Gets the month-of-year field using the `Month` enum.

This method returns the enum `https://developer.android.com/reference/kotlin/java/time/Month` for the month. This avoids confusion as to what `int` values mean. If you need access to the primitive `int` value then the enum provides the `https://developer.android.com/reference/kotlin/java/time/Month#getValue()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Month!` | the month-of-year, not null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/LocalDate#getMonthValue()`

### getMonthValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMonthValue(): Int
```

Gets the month-of-year field from 1 to 12.

This method returns the month as an `int` from 1 to 12. Application code is frequently clearer if the enum `https://developer.android.com/reference/kotlin/java/time/Month` is used by calling `https://developer.android.com/reference/kotlin/java/time/LocalDate#getMonth()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the month-of-year, from 1 to 12 |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/LocalDate#getMonth()`

### getYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getYear(): Int
```

Gets the year field.

This method returns the primitive `int` value for the year.

The year returned by this method is proleptic as per `get(YEAR)`. To obtain the year-of-era, use `get(YEAR_OF_ERA)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the year, from MIN_YEAR to MAX_YEAR |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

A hash code for this date.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAfter(other: ChronoLocalDate!): Boolean
```

Checks if this date is after the specified date.

This checks to see if this date represents a point on the local time-line after the other date.

```kotlin
LocalDate a = LocalDate.of(2012, 6, 30);
    LocalDate b = LocalDate.of(2012, 7, 1);
    a.isAfter(b) == false
    a.isAfter(a) == false
    b.isAfter(a) == true
  
```

This method only considers the position of the two dates on the local time-line. It does not take into account the chronology, or calendar system. This is different from the comparison in `https://developer.android.com/reference/kotlin/java/time/LocalDate#compareTo(java.time.chrono.ChronoLocalDate)`, but is the same approach as `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#timeLineOrder()`.

| Parameters ||
|---|---|
| `other` | [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md)!: the other date to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this date is after the specified date |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBefore(other: ChronoLocalDate!): Boolean
```

Checks if this date is before the specified date.

This checks to see if this date represents a point on the local time-line before the other date.

```kotlin
LocalDate a = LocalDate.of(2012, 6, 30);
    LocalDate b = LocalDate.of(2012, 7, 1);
    a.isBefore(b) == true
    a.isBefore(a) == false
    b.isBefore(a) == false
  
```

This method only considers the position of the two dates on the local time-line. It does not take into account the chronology, or calendar system. This is different from the comparison in `https://developer.android.com/reference/kotlin/java/time/LocalDate#compareTo(java.time.chrono.ChronoLocalDate)`, but is the same approach as `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#timeLineOrder()`.

| Parameters ||
|---|---|
| `other` | [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md)!: the other date to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this date is before the specified date |

### isEqual

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEqual(other: ChronoLocalDate!): Boolean
```

Checks if this date is equal to the specified date.

This checks to see if this date represents the same point on the local time-line as the other date.

```kotlin
LocalDate a = LocalDate.of(2012, 6, 30);
    LocalDate b = LocalDate.of(2012, 7, 1);
    a.isEqual(b) == false
    a.isEqual(a) == true
    b.isEqual(a) == false
  
```

This method only considers the position of the two dates on the local time-line. It does not take into account the chronology, or calendar system. This is different from the comparison in `https://developer.android.com/reference/kotlin/java/time/LocalDate#compareTo(java.time.chrono.ChronoLocalDate)` but is the same approach as `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#timeLineOrder()`.

| Parameters ||
|---|---|
| `other` | [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md)!: the other date to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this date is equal to the specified date |

### isLeapYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeapYear(): Boolean
```

Checks if the year is a leap year, according to the ISO proleptic calendar system rules.

This method applies the current rules for leap years across the whole time-line. In general, a year is a leap year if it is divisible by four without remainder. However, years divisible by 100, are not leap years, with the exception of years divisible by 400 which are.

For example, 1904 is a leap year it is divisible by 4. 1900 was not a leap year as it is divisible by 100, however 2000 was a leap year as it is divisible by 400.

The calculation is proleptic - applying the same rules into the far future and far past. This is historically inaccurate, but is correct for the ISO-8601 standard.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the year is leap, false otherwise |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this date can be queried for the specified field. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/LocalDate#range(java.time.temporal.TemporalField)`, `https://developer.android.com/reference/kotlin/java/time/LocalDate#get(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/LocalDate#with(java.time.temporal.TemporalField,%20kotlin.Long)` methods will throw an exception.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The supported fields are:

- `DAY_OF_WEEK`
- `ALIGNED_DAY_OF_WEEK_IN_MONTH`
- `ALIGNED_DAY_OF_WEEK_IN_YEAR`
- `DAY_OF_MONTH`
- `DAY_OF_YEAR`
- `EPOCH_DAY`
- `ALIGNED_WEEK_OF_MONTH`
- `ALIGNED_WEEK_OF_YEAR`
- `MONTH_OF_YEAR`
- `PROLEPTIC_MONTH`
- `YEAR_OF_ERA`
- `YEAR`
- `ERA`

All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field is supported on this date, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this date. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/LocalDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` and `https://developer.android.com/reference/kotlin/java/time/LocalDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)` methods will throw an exception.

If the unit is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` then the query is implemented here. The supported units are:

- `DAYS`
- `WEEKS`
- `MONTHS`
- `YEARS`
- `DECADES`
- `CENTURIES`
- `MILLENNIA`
- `ERAS`

All other `ChronoUnit` instances will return false.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.isSupportedBy(Temporal)` passing `this` as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|---|---|
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the unit can be added/subtracted, false if not |

### lengthOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lengthOfMonth(): Int
```

Returns the length of the month represented by this date.

This returns the length of the month in days. For example, a date in January would return 31.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the length of the month in days |

### lengthOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lengthOfYear(): Int
```

Returns the length of the year represented by this date.

This returns the length of the year in days, either 365 or 366.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | 366 if the year is leap, 365 otherwise |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(amountToSubtract: TemporalAmount!): LocalDate!
```

Returns a copy of this date with the specified amount subtracted.

This returns a `LocalDate`, based on this one, with the specified amount subtracted. The amount is typically `https://developer.android.com/reference/kotlin/java/time/Period` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount` interface.

The calculation is delegated to the amount object by calling `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#subtractFrom(java.time.temporal.Temporal)`. The amount implementation is free to implement the subtraction in any way it wishes, however it typically calls back to `https://developer.android.com/reference/kotlin/java/time/LocalDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)`. Consult the documentation of the amount implementation to determine if it can be successfully subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to subtract, not null |
| `amountToSubtract` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!: the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the subtraction made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): LocalDate!
```

Returns a copy of this date with the specified amount subtracted.

This returns a `LocalDate`, based on this one, with the amount in terms of the unit subtracted. If it is not possible to subtract the amount, because the unit is not supported or for some other reason, an exception is thrown.

This method is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` with the amount negated. See that method for a full description of how addition, and thus subtraction, works.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to subtract from the result, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit of the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the specified amount subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### minusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusDays(daysToSubtract: Long): LocalDate!
```

Returns a copy of this `LocalDate` with the specified number of days subtracted.

This method subtracts the specified amount from the days field decrementing the month and year fields as necessary to ensure the result remains valid. The result is only invalid if the maximum/minimum year is exceeded.

For example, 2009-01-01 minus one day would result in 2008-12-31.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `daysToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the days to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the days subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusMonths(monthsToSubtract: Long): LocalDate!
```

Returns a copy of this `LocalDate` with the specified number of months subtracted.

This method subtracts the specified amount from the months field in three steps:

1. Subtract the input months from the month-of-year field
2. Check if the resulting date would be invalid
3. Adjust the day-of-month to the last valid day if necessary

For example, 2007-03-31 minus one month would result in the invalid date 2007-02-31. Instead of returning an invalid result, the last valid day of the month, 2007-02-28, is selected instead.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `monthsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the months to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the months subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusWeeks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusWeeks(weeksToSubtract: Long): LocalDate!
```

Returns a copy of this `LocalDate` with the specified number of weeks subtracted.

This method subtracts the specified amount in weeks from the days field decrementing the month and year fields as necessary to ensure the result remains valid. The result is only invalid if the maximum/minimum year is exceeded.

For example, 2009-01-07 minus one week would result in 2008-12-31.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `weeksToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the weeks to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the weeks subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusYears(yearsToSubtract: Long): LocalDate!
```

Returns a copy of this `LocalDate` with the specified number of years subtracted.

This method subtracts the specified amount from the years field in three steps:

1. Subtract the input years from the year field
2. Check if the resulting date would be invalid
3. Adjust the day-of-month to the last valid day if necessary

For example, 2008-02-29 (leap year) minus one year would result in the invalid date 2007-02-29 (standard year). Instead of returning an invalid result, the last valid day of the month, 2007-02-28, is selected instead.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `yearsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the years to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the years subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(): LocalDate!
```

Obtains the current date from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#systemDefaultZone()` in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the current date using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(clock: Clock!): LocalDate!
```

Obtains the current date from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock`.

| Parameters ||
|---|---|
| `clock` | [Clock](Clock.md)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the current date, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(zone: ZoneId!): LocalDate!
```

Obtains the current date from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#system(java.time.ZoneId)` to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](ZoneId.md)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the current date using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    year: Int, 
    month: Int, 
    dayOfMonth: Int
): LocalDate!
```

Obtains an instance of `LocalDate` from a year, month and day.

This returns a `LocalDate` with the specified year, month and day-of-month. The day must be valid for the year and month, otherwise an exception will be thrown.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to represent, from MIN_YEAR to MAX_YEAR |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to represent, from 1 (January) to 12 (December) |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to represent, from 1 to 31 |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month-year |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    year: Int, 
    month: Month!, 
    dayOfMonth: Int
): LocalDate!
```

Obtains an instance of `LocalDate` from a year, month and day.

This returns a `LocalDate` with the specified year, month and day-of-month. The day must be valid for the year and month, otherwise an exception will be thrown.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to represent, from MIN_YEAR to MAX_YEAR |
| `month` | [Month](Month.md)!: the month-of-year to represent, not null |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to represent, from 1 to 31 |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month-year |

### ofEpochDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofEpochDay(epochDay: Long): LocalDate!
```

Obtains an instance of `LocalDate` from the epoch day count.

This returns a `LocalDate` with the specified epoch-day. The `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` is a simple incrementing count of days where day 0 is 1970-01-01. Negative numbers represent earlier days.

| Parameters ||
|---|---|
| `epochDay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the Epoch Day to convert, based on the epoch 1970-01-01 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the epoch day exceeds the supported date range |

### ofInstant

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofInstant(
    instant: Instant!, 
    zone: ZoneId!
): LocalDate!
```

Obtains an instance of `LocalDate` from an `Instant` and zone ID.

This creates a local date based on the specified instant. First, the offset from UTC/Greenwich is obtained using the zone ID and instant, which is simple as there is only one valid offset for each instant. Then, the instant and offset are used to calculate the local date.

| Parameters ||
|---|---|
| `instant` | [Instant](Instant.md)!: the instant to create the date from, not null |
| `zone` | [ZoneId](ZoneId.md)!: the time-zone, which may be an offset, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### ofYearDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofYearDay(
    year: Int, 
    dayOfYear: Int
): LocalDate!
```

Obtains an instance of `LocalDate` from a year and day-of-year.

This returns a `LocalDate` with the specified year and day-of-year. The day-of-year must be valid for the year, otherwise an exception will be thrown.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to represent, from MIN_YEAR to MAX_YEAR |
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-year to represent, from 1 to 366 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-year is invalid for the year |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(text: CharSequence!): LocalDate!
```

Obtains an instance of `LocalDate` from a text string such as `2007-12-03`.

The string must represent a valid date and is parsed using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_DATE:java.time.format.DateTimeFormatter`.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse such as "2007-12-03", not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the parsed local date, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(
    text: CharSequence!, 
    formatter: DateTimeFormatter!
): LocalDate!
```

Obtains an instance of `LocalDate` from a text string using a specific formatter.

The text is parsed using the formatter, returning a date.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `formatter` | [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | the parsed local date, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(amountToAdd: TemporalAmount!): LocalDate!
```

Returns a copy of this date with the specified amount added.

This returns a `LocalDate`, based on this one, with the specified amount added. The amount is typically `https://developer.android.com/reference/kotlin/java/time/Period` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount` interface.

The calculation is delegated to the amount object by calling `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#addTo(java.time.temporal.Temporal)`. The amount implementation is free to implement the addition in any way it wishes, however it typically calls back to `https://developer.android.com/reference/kotlin/java/time/LocalDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)`. Consult the documentation of the amount implementation to determine if it can be successfully added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to add, not null |
| `amountToAdd` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!: the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the addition made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): LocalDate!
```

Returns a copy of this date with the specified amount added.

This returns a `LocalDate`, based on this one, with the amount in terms of the unit added. If it is not possible to add the amount, because the unit is not supported or for some other reason, an exception is thrown.

In some cases, adding the amount can cause the resulting date to become invalid. For example, adding one month to 31st January would result in 31st February. In cases like this, the unit is responsible for resolving the date. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` then the addition is implemented here. The supported fields behave as follows:

- `DAYS` - Returns a `LocalDate` with the specified number of days added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusDays(kotlin.Long)`.
- `WEEKS` - Returns a `LocalDate` with the specified number of weeks added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusWeeks(kotlin.Long)` and uses a 7 day week.
- `MONTHS` - Returns a `LocalDate` with the specified number of months added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusMonths(kotlin.Long)`. The day-of-month will be unchanged unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `YEARS` - Returns a `LocalDate` with the specified number of years added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusYears(kotlin.Long)`. The day-of-month will be unchanged unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `DECADES` - Returns a `LocalDate` with the specified number of decades added. This is equivalent to calling `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusYears(kotlin.Long)` with the amount multiplied by 10. The day-of-month will be unchanged unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `CENTURIES` - Returns a `LocalDate` with the specified number of centuries added. This is equivalent to calling `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusYears(kotlin.Long)` with the amount multiplied by 100. The day-of-month will be unchanged unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `MILLENNIA` - Returns a `LocalDate` with the specified number of millennia added. This is equivalent to calling `https://developer.android.com/reference/kotlin/java/time/LocalDate#plusYears(kotlin.Long)` with the amount multiplied by 1,000. The day-of-month will be unchanged unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `ERAS` - Returns a `LocalDate` with the specified number of eras added. Only two eras are supported so the amount must be one, zero or minus one. If the amount is non-zero then the year is changed such that the year-of-era is unchanged. The day-of-month will be unchanged unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.

All other `ChronoUnit` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.addTo(Temporal, long)` passing `this` as the argument. In this case, the unit determines whether and how to perform the addition.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to add to the result, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit of the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the specified amount added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### plusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusDays(daysToAdd: Long): LocalDate!
```

Returns a copy of this `LocalDate` with the specified number of days added.

This method adds the specified amount to the days field incrementing the month and year fields as necessary to ensure the result remains valid. The result is only invalid if the maximum/minimum year is exceeded.

For example, 2008-12-31 plus one day would result in 2009-01-01.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `daysToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the days to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the days added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusMonths(monthsToAdd: Long): LocalDate!
```

Returns a copy of this `LocalDate` with the specified number of months added.

This method adds the specified amount to the months field in three steps:

1. Add the input months to the month-of-year field
2. Check if the resulting date would be invalid
3. Adjust the day-of-month to the last valid day if necessary

For example, 2007-03-31 plus one month would result in the invalid date 2007-04-31. Instead of returning an invalid result, the last valid day of the month, 2007-04-30, is selected instead.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `monthsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the months to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the months added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusWeeks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusWeeks(weeksToAdd: Long): LocalDate!
```

Returns a copy of this `LocalDate` with the specified number of weeks added.

This method adds the specified amount in weeks to the days field incrementing the month and year fields as necessary to ensure the result remains valid. The result is only invalid if the maximum/minimum year is exceeded.

For example, 2008-12-31 plus one week would result in 2009-01-07.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `weeksToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the weeks to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the weeks added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusYears(yearsToAdd: Long): LocalDate!
```

Returns a copy of this `LocalDate` with the specified number of years added.

This method adds the specified amount to the years field in three steps:

1. Add the input years to the year field
2. Check if the resulting date would be invalid
3. Adjust the day-of-month to the last valid day if necessary

For example, 2008-02-29 (leap year) plus one year would result in the invalid date 2009-02-29 (standard year). Instead of returning an invalid result, the last valid day of the month, 2009-02-28, is selected instead.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `yearsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the years to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the years added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this date using the specified query.

This queries this date using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery#queryFrom(java.time.temporal.TemporalAccessor)` method on the specified query passing `this` as the argument.

| Parameters ||
|---|---|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](../java.time.temporal/TemporalQuery.md)\<R\>!: the query to invoke, not null |

| Return ||
|---|---|
| `R` | the query result, null may be returned (defined by the query) |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs (defined by the query) |
| `java.time.DateTimeException` | if unable to query (defined by the query) |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

The range object expresses the minimum and maximum valid values for a field. This date is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/LocalDate#isSupported(java.time.temporal.TemporalField)` will return appropriate range instances. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.rangeRefinedBy(TemporalAccessor)` passing `this` as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to query the range for, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange!` | the range of valid values for the field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toEpochDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toEpochDay(): Long
```

Converts this date to the Epoch Day.

The `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` is a simple incrementing count of days where day 0 is 1970-01-01 (ISO). This definition is the same for all chronologies, enabling conversion.

This default implementation queries the `EPOCH_DAY` field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the Epoch Day equivalent to this date |

### toEpochSecond

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toEpochSecond(
    time: LocalTime!, 
    offset: ZoneOffset!
): Long
```

Converts this `LocalDate` to the number of seconds since the epoch of 1970-01-01T00:00:00Z.

This combines this local date with the specified time and offset to calculate the epoch-second value, which is the number of elapsed seconds from 1970-01-01T00:00:00Z. Instants on the time-line after the epoch are positive, earlier are negative.

| Parameters ||
|---|---|
| `time` | [LocalTime](LocalTime.md)!: the local time, not null |
| `offset` | [ZoneOffset](ZoneOffset.md)!: the zone offset, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of seconds since the epoch of 1970-01-01T00:00:00Z, may be negative |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Outputs this date as a `String`, such as `2007-12-03`.

The output will be in the ISO-8601 format `uuuu-MM-dd`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this date, not null |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun until(endDateExclusive: ChronoLocalDate!): Period!
```

Calculates the period between this date and another date as a `Period`.

This calculates the period between two dates in terms of years, months and days. The start and end points are `this` and the specified date. The result will be negative if the end is before the start. The negative sign will be the same in each of year, month and day.

The calculation is performed using the ISO calendar system. If necessary, the input date will be converted to ISO.

The start date is included, but the end date is not. The period is calculated by removing complete months, then calculating the remaining number of days, adjusting to ensure that both have the same sign. The number of months is then normalized into years and months based on a 12 month year. A month is considered to be complete if the end day-of-month is greater than or equal to the start day-of-month. For example, from `2010-01-15` to `2011-03-18` is "1 year, 2 months and 3 days".

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use `https://developer.android.com/reference/kotlin/java/time/Period#between(java.time.LocalDate,%20java.time.LocalDate)`:

```kotlin
// these two lines are equivalent
    period = start.until(end);
    period = Period.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

| Parameters ||
|---|---|
| `endDateExclusive` | [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md)!: the end date, exclusive, which may be in any chronology, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Period!` | the period between this date and the end date, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the period cannot be calculated |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

Calculates the amount of time until another date in terms of the specified unit.

This calculates the amount of time between two `LocalDate` objects in terms of a single `TemporalUnit`. The start and end points are `this` and the specified date. The result will be negative if the end is before the start. The `Temporal` passed to this method is converted to a `LocalDate` using #from(java.time.temporal.TemporalAccessor). For example, the amount in days between two dates can be calculated using `startDate.until(endDate, DAYS)`.

The calculation returns a whole number, representing the number of complete units between the two dates. For example, the amount in months between 2012-06-15 and 2012-08-14 will only be one month as it is one day short of two months.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)`:

```kotlin
// these two lines are equivalent
    amount = start.until(end, MONTHS);
    amount = MONTHS.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit`. The units `DAYS`, `WEEKS`, `MONTHS`, `YEARS`, `DECADES`, `CENTURIES`, `MILLENNIA` and `ERAS` are supported. Other `ChronoUnit` values will throw an exception.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.between(Temporal, Temporal)` passing `this` as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `endExclusive` | [Temporal](../java.time.temporal/Temporal.md)!: the end date, exclusive, which is converted to a `LocalDate`, not null |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit to measure the amount in, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the amount of time between this date and the end date |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to a `LocalDate` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(adjuster: TemporalAdjuster!): LocalDate!
```

Returns an adjusted copy of this date.

This returns a `LocalDate`, based on this one, with the date adjusted. The adjustment takes place using the specified adjuster strategy object. Read the documentation of the adjuster to understand what adjustment will be made.

A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month.

A selection of common adjustments is provided in `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjusters`. These include finding the "last day of the month" and "next Wednesday". Key date-time classes also implement the `TemporalAdjuster` interface, such as `https://developer.android.com/reference/kotlin/java/time/Month` and `https://developer.android.com/reference/kotlin/java/time/MonthDay`. The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

For example this code returns a date on the last day of July:

```kotlin
import static java.time.Month.*;
   import static java.time.temporal.TemporalAdjusters.*;
 
   result = localDate.with(JULY).with(lastDayOfMonth());
  
```

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster#adjustInto(java.time.temporal.Temporal)` method on the specified adjuster passing `this` as the argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `adjuster` | [TemporalAdjuster](../java.time.temporal/TemporalAdjuster.md)!: the adjuster to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on `this` with the adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the adjustment cannot be made |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(
    field: TemporalField!, 
    newValue: Long
): LocalDate!
```

Returns a copy of this date with the specified field set to a new value.

This returns a `LocalDate`, based on this one, with the value for the specified field changed. This can be used to change any supported field, such as the year, month or day-of-month. If it is not possible to set the value, because the field is not supported or for some other reason, an exception is thrown.

In some cases, changing the specified field can cause the resulting date to become invalid, such as changing the month from 31st January to February would make the day-of-month invalid. In cases like this, the field is responsible for resolving the date. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the adjustment is implemented here. The supported fields behave as follows:

- `DAY_OF_WEEK` - Returns a `LocalDate` with the specified day-of-week. The date is adjusted up to 6 days forward or backward within the boundary of a Monday to Sunday week.
- `ALIGNED_DAY_OF_WEEK_IN_MONTH` - Returns a `LocalDate` with the specified aligned-day-of-week. The date is adjusted to the specified month-based aligned-day-of-week. Aligned weeks are counted such that the first week of a given month starts on the first day of that month. This may cause the date to be moved up to 6 days into the following month.
- `ALIGNED_DAY_OF_WEEK_IN_YEAR` - Returns a `LocalDate` with the specified aligned-day-of-week. The date is adjusted to the specified year-based aligned-day-of-week. Aligned weeks are counted such that the first week of a given year starts on the first day of that year. This may cause the date to be moved up to 6 days into the following year.
- `DAY_OF_MONTH` - Returns a `LocalDate` with the specified day-of-month. The month and year will be unchanged. If the day-of-month is invalid for the year and month, then a `DateTimeException` is thrown.
- `DAY_OF_YEAR` - Returns a `LocalDate` with the specified day-of-year. The year will be unchanged. If the day-of-year is invalid for the year, then a `DateTimeException` is thrown.
- `EPOCH_DAY` - Returns a `LocalDate` with the specified epoch-day. This completely replaces the date and is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalDate#ofEpochDay(kotlin.Long)`.
- `ALIGNED_WEEK_OF_MONTH` - Returns a `LocalDate` with the specified aligned-week-of-month. Aligned weeks are counted such that the first week of a given month starts on the first day of that month. This adjustment moves the date in whole week chunks to match the specified week. The result will have the same day-of-week as this date. This may cause the date to be moved into the following month.
- `ALIGNED_WEEK_OF_YEAR` - Returns a `LocalDate` with the specified aligned-week-of-year. Aligned weeks are counted such that the first week of a given year starts on the first day of that year. This adjustment moves the date in whole week chunks to match the specified week. The result will have the same day-of-week as this date. This may cause the date to be moved into the following year.
- `MONTH_OF_YEAR` - Returns a `LocalDate` with the specified month-of-year. The year will be unchanged. The day-of-month will also be unchanged, unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `PROLEPTIC_MONTH` - Returns a `LocalDate` with the specified proleptic-month. The day-of-month will be unchanged, unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `YEAR_OF_ERA` - Returns a `LocalDate` with the specified year-of-era. The era and month will be unchanged. The day-of-month will also be unchanged, unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `YEAR` - Returns a `LocalDate` with the specified year. The month will be unchanged. The day-of-month will also be unchanged, unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.
- `ERA` - Returns a `LocalDate` with the specified era. The year-of-era and month will be unchanged. The day-of-month will also be unchanged, unless it would be invalid for the new month and year. In that case, the day-of-month is adjusted to the maximum valid value for the new month and year.

In all cases, if the new value is outside the valid range of values for the field then a `DateTimeException` will be thrown.

All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.adjustInto(Temporal, long)` passing `this` as the argument. In this case, the field determines whether and how to adjust the instant.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value of the field in the result |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on `this` with the specified field set, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |

### withDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withDayOfMonth(dayOfMonth: Int): LocalDate!
```

Returns a copy of this `LocalDate` with the day-of-month altered.

If the resulting date is invalid, an exception is thrown.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to set in the result, from 1 to 28-31 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the requested day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the day-of-month value is invalid, or if the day-of-month is invalid for the month-year |

### withDayOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withDayOfYear(dayOfYear: Int): LocalDate!
```

Returns a copy of this `LocalDate` with the day-of-year altered.

If the resulting date is invalid, an exception is thrown.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-year to set in the result, from 1 to 365-366 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the requested day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the day-of-year value is invalid, or if the day-of-year is invalid for the year |

### withMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withMonth(month: Int): LocalDate!
```

Returns a copy of this `LocalDate` with the month-of-year altered.

If the day-of-month is invalid for the year, it will be changed to the last valid day of the month.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to set in the result, from 1 (January) to 12 (December) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the requested month, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the month-of-year value is invalid |

### withYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withYear(year: Int): LocalDate!
```

Returns a copy of this `LocalDate` with the year altered.

If the day-of-month is invalid for the year, it will be changed to the last valid day of the month.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to set in the result, from MIN_YEAR to MAX_YEAR |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate#!` | a `LocalDate` based on this date with the requested year, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the year value is invalid |

## Properties

### EPOCH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EPOCH: LocalDate!
```

The epoch year `LocalDate`, '1970-01-01'.

### MAX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX: LocalDate!
```

The maximum supported `LocalDate`, '+999999999-12-31'. This could be used by an application as a "far future" date.

### MIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN: LocalDate!
```

The minimum supported `LocalDate`, '-999999999-01-01'. This could be used by an application as a "far past" date.
