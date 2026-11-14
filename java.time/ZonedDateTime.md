# ZonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZonedDateTime

```
class ZonedDateTime : ChronoZonedDateTime<LocalDate!>, Serializable, Temporal
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.ZonedDateTime](ZonedDateTime.md) |

A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`.

`ZonedDateTime`is an immutable representation of a date-time with a time-zone. This class stores all date and time fields, to a precision of nanoseconds, and a time-zone, with a zone offset used to handle ambiguous local date-times. For example, the value "2nd October 2007 at 13:45.30.123456789 +02:00 in the Europe/Paris time-zone" can be stored in a`ZonedDateTime`.

This class handles conversion from the local time-line of`LocalDateTime`to the instant time-line of`Instant`. The difference between the two time-lines is the offset from UTC/Greenwich, represented by a`ZoneOffset`.

Converting between the two time-lines involves calculating the offset using the [rules](../java.time.zone/ZoneRules.md) accessed from the`ZoneId`. Obtaining the offset for an instant is simple, as there is exactly one valid offset for each instant. By contrast, obtaining the offset for a local date-time is not straightforward. There are three cases:

- Normal, with one valid offset. For the vast majority of the year, the normal case applies, where there is a single valid offset for the local date-time.
- Gap, with zero valid offsets. This is when clocks jump forward typically due to the spring daylight savings change from "winter" to "summer". In a gap there are local date-time values with no valid offset.
- Overlap, with two valid offsets. This is when clocks are set back typically due to the autumn daylight savings change from "summer" to "winter". In an overlap there are local date-time values with two valid offsets.

Any method that converts directly or implicitly from a local date-time to an instant by obtaining the offset has the potential to be complicated.

For Gaps, the general strategy is that if the local date-time falls in the middle of a Gap, then the resulting zoned date-time will have a local date-time shifted forwards by the length of the Gap, resulting in a date-time in the later offset, typically "summer" time.

For Overlaps, the general strategy is that if the local date-time falls in the middle of an Overlap, then the previous offset will be retained. If there is no previous offset, or the previous offset is invalid, then the earlier offset is used, typically "summer" time.. Two additional methods, [withEarlierOffsetAtOverlap()](ZonedDateTime.md))and [withLaterOffsetAtOverlap()](ZonedDateTime.md)), help manage the case of an overlap.

In terms of design, this class should be viewed primarily as the combination of a`LocalDateTime`and a`ZoneId`. The`ZoneOffset`is a vital, but secondary, piece of information, used to ensure that the class represents an instant, especially during a daylight savings overlap.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ZonedDateTime.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this date-time is equal to another date-time. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](ZonedDateTime.md))`(`formatter:` ` [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!`)` Formats this date-time using the specified formatter. |
| static [ZonedDateTime](ZonedDateTime.md)! | [from](ZonedDateTime.md))`(`temporal:` ` [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!`)` Obtains an instance of`ZonedDateTime`from a temporal object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](ZonedDateTime.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` Gets the value of the specified field from this date-time as an`int`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDayOfMonth](ZonedDateTime.md))`()` Gets the day-of-month field. |
| [DayOfWeek](DayOfWeek.md)! | [getDayOfWeek](ZonedDateTime.md))`()` Gets the day-of-week field, which is an enum`DayOfWeek`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDayOfYear](ZonedDateTime.md))`()` Gets the day-of-year field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHour](ZonedDateTime.md))`()` Gets the hour-of-day field. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](ZonedDateTime.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` Gets the value of the specified field from this date-time as a`long`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinute](ZonedDateTime.md))`()` Gets the minute-of-hour field. |
| [Month](Month.md)! | [getMonth](ZonedDateTime.md))`()` Gets the month-of-year field using the`Month`enum. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMonthValue](ZonedDateTime.md))`()` Gets the month-of-year field from 1 to 12. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNano](ZonedDateTime.md))`()` Gets the nano-of-second field. |
| [ZoneOffset](ZoneOffset.md)! | [getOffset](ZonedDateTime.md))`()` Gets the zone offset, such as '+01:00'. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecond](ZonedDateTime.md))`()` Gets the second-of-minute field. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYear](ZonedDateTime.md))`()` Gets the year field. |
| [ZoneId](ZoneId.md)! | [getZone](ZonedDateTime.md))`()` Gets the time-zone, such as 'Europe/Paris'. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](ZonedDateTime.md))`()` A hash code for this date-time. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](ZonedDateTime.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` Checks if the specified field is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](ZonedDateTime.md))`(`unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Checks if the specified unit is supported. |
| [ZonedDateTime](ZonedDateTime.md)! | [minus](ZonedDateTime.md))`(`amountToSubtract:` ` [TemporalAmount](../java.time.temporal/TemporalAmount.md)!`)` Returns a copy of this date-time with the specified amount subtracted. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [minus](ZonedDateTime.md))`(`amountToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Returns a copy of this date-time with the specified amount subtracted. |
| [ZonedDateTime](ZonedDateTime.md)! | [minusDays](ZonedDateTime.md))`(`days:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of days subtracted. |
| [ZonedDateTime](ZonedDateTime.md)! | [minusHours](ZonedDateTime.md))`(`hours:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of hours subtracted. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [minusMinutes](ZonedDateTime.md))`(`minutes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of minutes subtracted. |
| [ZonedDateTime](ZonedDateTime.md)! | [minusMonths](ZonedDateTime.md))`(`months:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of months subtracted. |
| [ZonedDateTime](ZonedDateTime.md)! | [minusNanos](ZonedDateTime.md))`(`nanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of nanoseconds subtracted. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [minusSeconds](ZonedDateTime.md))`(`seconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of seconds subtracted. |
| [ZonedDateTime](ZonedDateTime.md)! | [minusWeeks](ZonedDateTime.md))`(`weeks:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of weeks subtracted. |
| [ZonedDateTime](ZonedDateTime.md)! | [minusYears](ZonedDateTime.md))`(`years:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of years subtracted. |
| --- | --- |
| static [ZonedDateTime](ZonedDateTime.md)! | [now](ZonedDateTime.md))`()` Obtains the current date-time from the system clock in the default time-zone. |
| static [ZonedDateTime](ZonedDateTime.md)! | [now](ZonedDateTime.md))`(`clock:` ` [Clock](Clock.md)!`)` Obtains the current date-time from the specified clock. |
| static [ZonedDateTime](ZonedDateTime.md)! | [now](ZonedDateTime.md))`(`zone:` ` [ZoneId](ZoneId.md)!`)` Obtains the current date-time from the system clock in the specified time-zone. |
| --- | --- |
| static [ZonedDateTime](ZonedDateTime.md)! | [of](ZonedDateTime.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nanoOfSecond:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `zone:` ` [ZoneId](ZoneId.md)!`)` Obtains an instance of`ZonedDateTime`from a year, month, day, hour, minute, second, nanosecond and time-zone. |
| static [ZonedDateTime](ZonedDateTime.md)! | [of](ZonedDateTime.md))`(`date:` ` [LocalDate](LocalDate.md)!`, `time:` ` [LocalTime](LocalTime.md)!`, `zone:` ` [ZoneId](ZoneId.md)!`)` Obtains an instance of`ZonedDateTime`from a local date and time. |
| static [ZonedDateTime](ZonedDateTime.md)! | [of](ZonedDateTime.md))`(`localDateTime:` ` [LocalDateTime](LocalDateTime.md)!`, `zone:` ` [ZoneId](ZoneId.md)!`)` Obtains an instance of`ZonedDateTime`from a local date-time. |
| --- | --- |
| static [ZonedDateTime](ZonedDateTime.md)! | [ofInstant](ZonedDateTime.md))`(`instant:` ` [Instant](Instant.md)!`, `zone:` ` [ZoneId](ZoneId.md)!`)` Obtains an instance of`ZonedDateTime`from an`Instant`. |
| static [ZonedDateTime](ZonedDateTime.md)! | [ofInstant](ZonedDateTime.md))`(`localDateTime:` ` [LocalDateTime](LocalDateTime.md)!`, `offset:` ` [ZoneOffset](ZoneOffset.md)!`, `zone:` ` [ZoneId](ZoneId.md)!`)` Obtains an instance of`ZonedDateTime`from the instant formed by combining the local date-time and offset. |
| static [ZonedDateTime](ZonedDateTime.md)! | [ofLocal](ZonedDateTime.md))`(`localDateTime:` ` [LocalDateTime](LocalDateTime.md)!`, `zone:` ` [ZoneId](ZoneId.md)!`, `preferredOffset:` ` [ZoneOffset](ZoneOffset.md)!`)` Obtains an instance of`ZonedDateTime`from a local date-time using the preferred offset if possible. |
| --- | --- |
| static [ZonedDateTime](ZonedDateTime.md)! | [ofStrict](ZonedDateTime.md))`(`localDateTime:` ` [LocalDateTime](LocalDateTime.md)!`, `offset:` ` [ZoneOffset](ZoneOffset.md)!`, `zone:` ` [ZoneId](ZoneId.md)!`)` Obtains an instance of`ZonedDateTime`strictly validating the combination of local date-time, offset and zone ID. |
| static [ZonedDateTime](ZonedDateTime.md)! | [parse](ZonedDateTime.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Obtains an instance of`ZonedDateTime`from a text string such as`2007-12-03T10:15:30+01:00[Europe/Paris]`. |
| static [ZonedDateTime](ZonedDateTime.md)! | [parse](ZonedDateTime.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `formatter:` ` [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!`)` Obtains an instance of`ZonedDateTime`from a text string using a specific formatter. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [plus](ZonedDateTime.md))`(`amountToAdd:` ` [TemporalAmount](../java.time.temporal/TemporalAmount.md)!`)` Returns a copy of this date-time with the specified amount added. |
| [ZonedDateTime](ZonedDateTime.md)! | [plus](ZonedDateTime.md))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Returns a copy of this date-time with the specified amount added. |
| [ZonedDateTime](ZonedDateTime.md)! | [plusDays](ZonedDateTime.md))`(`days:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of days added. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [plusHours](ZonedDateTime.md))`(`hours:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of hours added. |
| [ZonedDateTime](ZonedDateTime.md)! | [plusMinutes](ZonedDateTime.md))`(`minutes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of minutes added. |
| [ZonedDateTime](ZonedDateTime.md)! | [plusMonths](ZonedDateTime.md))`(`months:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of months added. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [plusNanos](ZonedDateTime.md))`(`nanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of nanoseconds added. |
| [ZonedDateTime](ZonedDateTime.md)! | [plusSeconds](ZonedDateTime.md))`(`seconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of seconds added. |
| [ZonedDateTime](ZonedDateTime.md)! | [plusWeeks](ZonedDateTime.md))`(`weeks:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of weeks added. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [plusYears](ZonedDateTime.md))`(`years:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`ZonedDateTime`with the specified number of years added. |
| R | [query](ZonedDateTime.md))`(`query:` ` [TemporalQuery](../java.time.temporal/TemporalQuery.md)<R>!`)` Queries this date-time using the specified query. |
| [ValueRange](../java.time.temporal/ValueRange.md)! | [range](ZonedDateTime.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` Gets the range of valid values for the specified field. |
| --- | --- |
| [LocalDate](LocalDate.md)! | [toLocalDate](ZonedDateTime.md))`()` Gets the`LocalDate`part of this date-time. |
| [LocalDateTime](LocalDateTime.md)! | [toLocalDateTime](ZonedDateTime.md))`()` Gets the`LocalDateTime`part of this date-time. |
| [LocalTime](LocalTime.md)! | [toLocalTime](ZonedDateTime.md))`()` Gets the`LocalTime`part of this date-time. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | [toOffsetDateTime](ZonedDateTime.md))`()` Converts this date-time to an`OffsetDateTime`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ZonedDateTime.md))`()` Outputs this date-time as a`String`, such as`2007-12-03T10:15:30+01:00[Europe/Paris]`. |
| [ZonedDateTime](ZonedDateTime.md)! | [truncatedTo](ZonedDateTime.md))`(`unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Returns a copy of this`ZonedDateTime`with the time truncated. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](ZonedDateTime.md))`(`endExclusive:` ` [Temporal](../java.time.temporal/Temporal.md)!`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Calculates the amount of time until another date-time in terms of the specified unit. |
| [ZonedDateTime](ZonedDateTime.md)! | [with](ZonedDateTime.md))`(`adjuster:` ` [TemporalAdjuster](../java.time.temporal/TemporalAdjuster.md)!`)` Returns an adjusted copy of this date-time. |
| [ZonedDateTime](ZonedDateTime.md)! | [with](ZonedDateTime.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this date-time with the specified field set to a new value. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [withDayOfMonth](ZonedDateTime.md))`(`dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`ZonedDateTime`with the day-of-month altered. |
| [ZonedDateTime](ZonedDateTime.md)! | [withDayOfYear](ZonedDateTime.md))`(`dayOfYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`ZonedDateTime`with the day-of-year altered. |
| [ZonedDateTime](ZonedDateTime.md)! | [withEarlierOffsetAtOverlap](ZonedDateTime.md))`()` Returns a copy of this date-time changing the zone offset to the earlier of the two valid offsets at a local time-line overlap. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [withFixedOffsetZone](ZonedDateTime.md))`()` Returns a copy of this date-time with the zone ID set to the offset. |
| [ZonedDateTime](ZonedDateTime.md)! | [withHour](ZonedDateTime.md))`(`hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`ZonedDateTime`with the hour-of-day altered. |
| [ZonedDateTime](ZonedDateTime.md)! | [withLaterOffsetAtOverlap](ZonedDateTime.md))`()` Returns a copy of this date-time changing the zone offset to the later of the two valid offsets at a local time-line overlap. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [withMinute](ZonedDateTime.md))`(`minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`ZonedDateTime`with the minute-of-hour altered. |
| [ZonedDateTime](ZonedDateTime.md)! | [withMonth](ZonedDateTime.md))`(`month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`ZonedDateTime`with the month-of-year altered. |
| [ZonedDateTime](ZonedDateTime.md)! | [withNano](ZonedDateTime.md))`(`nanoOfSecond:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`ZonedDateTime`with the nano-of-second altered. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [withSecond](ZonedDateTime.md))`(`second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`ZonedDateTime`with the second-of-minute altered. |
| [ZonedDateTime](ZonedDateTime.md)! | [withYear](ZonedDateTime.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`ZonedDateTime`with the year altered. |
| [ZonedDateTime](ZonedDateTime.md)! | [withZoneSameInstant](ZonedDateTime.md))`(`zone:` ` [ZoneId](ZoneId.md)!`)` Returns a copy of this date-time with a different time-zone, retaining the instant. |
| --- | --- |
| [ZonedDateTime](ZonedDateTime.md)! | [withZoneSameLocal](ZonedDateTime.md))`(`zone:` ` [ZoneId](ZoneId.md)!`)` Returns a copy of this date-time with a different time-zone, retaining the local date-time if possible. |

| Inherited functions ||
|---|---|
| From class [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md) |-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../java.time.chrono/ChronoZonedDateTime.md))`(`other:` ` [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md)<*>!`)` <br /> Compares this date-time to another date-time, including the chronology. The comparison is based first on the instant, then on the local date-time, then on the zone ID, then on the chronology. It is "consistent with equals", as defined by [Comparable](../java.lang/Comparable.md). If all the date-time objects being compared are in the same chronology, then the additional chronology stage is not required. This default implementation performs the comparison defined above. <br /> | | [Chronology](../java.time.chrono/Chronology.md)! | [getChronology](../java.time.chrono/ChronoZonedDateTime.md))`()` <br /> Gets the chronology of this date-time. The`Chronology`represents the calendar system in use. The era and other fields in [ChronoField](../java.time.temporal/ChronoField.md) are defined by the chronology. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfter](../java.time.chrono/ChronoZonedDateTime.md))`(`other:` ` [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md)<*>!`)` <br /> Checks if the instant of this date-time is after that of the specified date-time. This method differs from the comparison in [compareTo](../java.time.chrono/ChronoZonedDateTime.md))in that it only compares the instant of the date-time. This is equivalent to using`dateTime1.toInstant().isAfter(dateTime2.toInstant());`. This default implementation performs the comparison based on the epoch-second and nano-of-second. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBefore](../java.time.chrono/ChronoZonedDateTime.md))`(`other:` ` [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md)<*>!`)` <br /> Checks if the instant of this date-time is before that of the specified date-time. This method differs from the comparison in [compareTo](../java.time.chrono/ChronoZonedDateTime.md))in that it only compares the instant of the date-time. This is equivalent to using`dateTime1.toInstant().isBefore(dateTime2.toInstant());`. This default implementation performs the comparison based on the epoch-second and nano-of-second. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqual](../java.time.chrono/ChronoZonedDateTime.md))`(`other:` ` [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md)<*>!`)` <br /> Checks if the instant of this date-time is equal to that of the specified date-time. This method differs from the comparison in [compareTo](../java.time.chrono/ChronoZonedDateTime.md))and [equals](ZonedDateTime.md) in that it only compares the instant of the date-time. This is equivalent to using`dateTime1.toInstant().equals(dateTime2.toInstant());`. This default implementation performs the comparison based on the epoch-second and nano-of-second. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toEpochSecond](../java.time.chrono/ChronoZonedDateTime.md))`()` <br /> Converts this date-time to the number of seconds from the epoch of 1970-01-01T00:00:00Z. This uses the [local date-time](../java.time.chrono/ChronoZonedDateTime.md))and [offset](../java.time.chrono/ChronoZonedDateTime.md))to calculate the epoch-second value, which is the number of elapsed seconds from 1970-01-01T00:00:00Z. Instants on the time-line after the epoch are positive, earlier are negative. <br /> | | [Instant](Instant.md)! | [toInstant](../java.time.chrono/ChronoZonedDateTime.md))`()` <br /> Converts this date-time to an`Instant`. This returns an`Instant`representing the same point on the time-line as this date-time. The calculation combines the [local date-time](../java.time.chrono/ChronoZonedDateTime.md))and [offset](../java.time.chrono/ChronoZonedDateTime.md)). <br /> | ||
| From class [TemporalAccessor](../java.time.temporal/TemporalAccessor.md) |---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](../java.time.temporal/TemporalAccessor.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> Gets the value of the specified field as an`int`. This queries the date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java.time.temporal/TemporalAccessor.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> Gets the value of the specified field as a`long`. This queries the date-time for the value of the specified field. The returned value may be outside the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](../java.time.temporal/TemporalAccessor.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> Checks if the specified field is supported. This checks if the date-time can be queried for the specified field. If false, then calling the [range](../java.time.temporal/TemporalAccessor.md))and [get](../java.time.temporal/TemporalAccessor.md))methods will throw an exception. <br /> | | R | [query](../java.time.temporal/TemporalAccessor.md))`(`query:` ` [TemporalQuery](../java.time.temporal/TemporalQuery.md)<R>!`)` <br /> Queries this date-time. This queries this date-time using the specified query strategy object. Queries are a key tool for extracting information from date-times. They exists to externalize the process of querying, permitting different approaches, as per the strategy design pattern. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday. The most common query implementations are method references, such as`LocalDate::from`and`ZoneId::from`. Additional implementations are provided as static methods on [TemporalQuery](../java.time.temporal/TemporalQuery.md). <br /> | | [ValueRange](../java.time.temporal/ValueRange.md)! | [range](../java.time.temporal/TemporalAccessor.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> Gets the range of valid values for the specified field. All fields can be expressed as a`long`integer. This method returns an object that describes the valid range for that value. The value of this temporal object is used to enhance the accuracy of the returned range. If the date-time cannot return the range, because the field is unsupported or for some other reason, an exception will be thrown. Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field. <br /> | ||
| From class [Temporal](../java.time.temporal/Temporal.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](../java.time.temporal/Temporal.md))`(`endExclusive:` ` [Temporal](../java.time.temporal/Temporal.md)!`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` <br /> Calculates the amount of time until another temporal in terms of the specified unit. This calculates the amount of time between two temporal objects in terms of a single`TemporalUnit`. The start and end points are`this`and the specified temporal. The end point is converted to be of the same type as the start point if different. The result will be negative if the end is before the start. For example, the amount in hours between two temporal objects can be calculated using`startTime.until(endTime, HOURS)`. The calculation returns a whole number, representing the number of complete units between the two temporals. For example, the amount in hours between the times 11:30 and 13:29 will only be one hour as it is one minute short of two hours. There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [TemporalUnit.between(Temporal, Temporal)](../java.time.temporal/TemporalUnit.md)): ```kotlin // these two lines are equivalent temporal = start.until(end, unit); temporal = unit.between(start, end); ``` The choice should be made based on which makes the code more readable. For example, this method allows the number of days between two dates to be calculated: ```kotlin long daysBetween = start.until(end, DAYS); // or alternatively long daysBetween = DAYS.between(start, end); ``` <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

## Public methods

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Checks if this date-time is equal to another date-time.

The comparison is based on the offset date-time and the zone. Only objects of type`ZonedDateTime`are compared, other types return false.

| Parameters ||
|-------|-----------------------------------------|
| `obj` | the object to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is equal to the other date-time |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(formatter: DateTimeFormatter!): String!
```

Formats this date-time using the specified formatter.

This date-time will be passed to the formatter to produce a string.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `formatter` | [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!:the formatter to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted date-time string, not null |

| Exceptions ||
|-------------------------------|------------------------------------|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun from(temporal: TemporalAccessor!): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from a temporal object.

This obtains a zoned date-time based on the specified temporal. A`TemporalAccessor`represents an arbitrary set of date and time information, which this factory converts to an instance of`ZonedDateTime`.

The conversion will first obtain a`ZoneId`from the temporal object, falling back to a`ZoneOffset`if necessary. It will then try to obtain an`Instant`, falling back to a`LocalDateTime`if necessary. The result will be either the combination of`ZoneId`or`ZoneOffset`with`Instant`or`LocalDateTime`. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects.

This method matches the signature of the functional interface [TemporalQuery](../java.time.temporal/TemporalQuery.md) allowing it to be used as a query via method reference,`ZonedDateTime::from`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!:the temporal object to convert, not null |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the zoned date-time, not null |

| Exceptions ||
|-------------------------------|-------------------------------------------|
| `java.time.DateTimeException` | if unable to convert to an`ZonedDateTime` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this date-time as an`int`.

This queries this date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The [supported fields](ZonedDateTime.md))will return valid values based on this date-time, except`NANO_OF_DAY`,`MICRO_OF_DAY`,`EPOCH_DAY`,`PROLEPTIC_MONTH`and`INSTANT_SECONDS`which are too large to fit in an`int`and throw an`UnsupportedTemporalTypeException`. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to get, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an`int` |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDayOfMonth(): Int
```

Gets the day-of-month field.

This method returns the primitive`int`value for the day-of-month.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the day-of-month, from 1 to 31 |

### getDayOfWeek

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDayOfWeek(): DayOfWeek!
```

Gets the day-of-week field, which is an enum`DayOfWeek`.

This method returns the enum [DayOfWeek](DayOfWeek.md) for the day-of-week. This avoids confusion as to what`int`values mean. If you need access to the primitive`int`value then the enum provides the [int value](DayOfWeek.md)).

Additional information can be obtained from the`DayOfWeek`. This includes textual names of the values.

| Return ||
|----------------------------------------------------------------------------------|---------------------------|
| [DayOfWeek](DayOfWeek.md)! | the day-of-week, not null |

### getDayOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDayOfYear(): Int
```

Gets the day-of-year field.

This method returns the primitive`int`value for the day-of-year.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the day-of-year, from 1 to 365, or 366 in a leap year |

### getHour

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHour(): Int
```

Gets the hour-of-day field.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hour-of-day, from 0 to 23 |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this date-time as a`long`.

This queries this date-time for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The [supported fields](ZonedDateTime.md))will return valid values based on this date-time. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to get, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getMinute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinute(): Int
```

Gets the minute-of-hour field.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minute-of-hour, from 0 to 59 |

### getMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMonth(): Month!
```

Gets the month-of-year field using the`Month`enum.

This method returns the enum [Month](Month.md) for the month. This avoids confusion as to what`int`values mean. If you need access to the primitive`int`value then the enum provides the [int value](Month.md)).

| Return ||
|--------------------------------------------------------------------------|-----------------------------|
| [Month](Month.md)! | the month-of-year, not null |

**See Also**

- <https://developer.android.com/reference/kotlin/java/time/ZonedDateTime#getMonthValue()> 

### getMonthValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMonthValue(): Int
```

Gets the month-of-year field from 1 to 12.

This method returns the month as an`int`from 1 to 12. Application code is frequently clearer if the enum [Month](Month.md) is used by calling [getMonth()](ZonedDateTime.md)).

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the month-of-year, from 1 to 12 |

**See Also**

- <https://developer.android.com/reference/kotlin/java/time/ZonedDateTime#getMonth()> 

### getNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNano(): Int
```

Gets the nano-of-second field.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the nano-of-second, from 0 to 999,999,999 |

### getOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffset(): ZoneOffset!
```

Gets the zone offset, such as '+01:00'.

This is the offset of the local date-time from UTC/Greenwich.

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [ZoneOffset](ZoneOffset.md)! | the zone offset, not null |

### getSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecond(): Int
```

Gets the second-of-minute field.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the second-of-minute, from 0 to 59 |

### getYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getYear(): Int
```

Gets the year field.

This method returns the primitive`int`value for the year.

The year returned by this method is proleptic as per`get(YEAR)`. To obtain the year-of-era, use`get(YEAR_OF_ERA)`.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the year, from MIN_YEAR to MAX_YEAR |

### getZone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZone(): ZoneId!
```

Gets the time-zone, such as 'Europe/Paris'.

This returns the zone ID. This identifies the time-zone [rules](../java.time.zone/ZoneRules.md) that determine when and how the offset from UTC/Greenwich changes.

The zone ID may be same as the [offset](ZonedDateTime.md)). If this is true, then any future calculations, such as addition or subtraction, have no complex edge cases due to time-zone rules. See also [withFixedOffsetZone()](ZonedDateTime.md)).

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [ZoneId](ZoneId.md)! | the time-zone, not null |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

A hash code for this date-time.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a suitable hash code |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this date-time can be queried for the specified field. If false, then calling the [range](ZonedDateTime.md)), [get](ZonedDateTime.md))and [with(java.time.temporal.TemporalField,long)](ZonedDateTime.md))methods will throw an exception.

If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The supported fields are:

- `NANO_OF_SECOND`
- `NANO_OF_DAY`
- `MICRO_OF_SECOND`
- `MICRO_OF_DAY`
- `MILLI_OF_SECOND`
- `MILLI_OF_DAY`
- `SECOND_OF_MINUTE`
- `SECOND_OF_DAY`
- `MINUTE_OF_HOUR`
- `MINUTE_OF_DAY`
- `HOUR_OF_AMPM`
- `CLOCK_HOUR_OF_AMPM`
- `HOUR_OF_DAY`
- `CLOCK_HOUR_OF_DAY`
- `AMPM_OF_DAY`
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
- `INSTANT_SECONDS`
- `OFFSET_SECONDS`

All other`ChronoField`instances will return false.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field is supported on this date-time, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this date-time. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](ZonedDateTime.md))and [minus](ZonedDateTime.md))methods will throw an exception.

If the unit is a [ChronoUnit](../java.time.temporal/ChronoUnit.md) then the query is implemented here. The supported units are:

- `NANOS`
- `MICROS`
- `MILLIS`
- `SECONDS`
- `MINUTES`
- `HOURS`
- `HALF_DAYS`
- `DAYS`
- `WEEKS`
- `MONTHS`
- `YEARS`
- `DECADES`
- `CENTURIES`
- `MILLENNIA`
- `ERAS`

All other`ChronoUnit`instances will return false.

If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.isSupportedBy(Temporal)`passing`this`as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit can be added/subtracted, false if not |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(amountToSubtract: TemporalAmount!): ZonedDateTime!
```

Returns a copy of this date-time with the specified amount subtracted.

This returns a`ZonedDateTime`, based on this one, with the specified amount subtracted. The amount is typically [Period](Period.md) or [Duration](Duration.md) but may be any other type implementing the [TemporalAmount](../java.time.temporal/TemporalAmount.md) interface.

The calculation is delegated to the amount object by calling [TemporalAmount.subtractFrom(Temporal)](../java.time.temporal/TemporalAmount.md)). The amount implementation is free to implement the subtraction in any way it wishes, however it typically calls back to [minus(long,java.time.temporal.TemporalUnit)](ZonedDateTime.md)). Consult the documentation of the amount implementation to determine if it can be successfully subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | the amount to subtract, not null |
| `amountToSubtract` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!:the amount to subtract, not null |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the subtraction made, not null |

| Exceptions ||
|---------------------------------|-----------------------------------|
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): ZonedDateTime!
```

Returns a copy of this date-time with the specified amount subtracted.

This returns a`ZonedDateTime`, based on this one, with the amount in terms of the unit subtracted. If it is not possible to subtract the amount, because the unit is not supported or for some other reason, an exception is thrown.

The calculation for date and time units differ.

Date units operate on the local time-line. The period is first subtracted from the local date-time, then converted back to a zoned date-time using the zone ID. The conversion uses [ofLocal(java.time.LocalDateTime,java.time.ZoneId,java.time.ZoneOffset)](ZonedDateTime.md))with the offset before the subtraction.

Time units operate on the instant time-line. The period is first subtracted from the local date-time, then converted back to a zoned date-time using the zone ID. The conversion uses [ofInstant(java.time.LocalDateTime,java.time.ZoneOffset,java.time.ZoneId)](ZonedDateTime.md))with the offset before the subtraction.

This method is equivalent to [plus(long,java.time.temporal.TemporalUnit)](ZonedDateTime.md))with the amount negated. See that method for a full description of how addition, and thus subtraction, works.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the unit to subtract from the result, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit of the amount to subtract, not null |

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the specified amount subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------|
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### minusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusDays(days: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of days subtracted.

This operates on the local time-line, [subtracting days](LocalDateTime.md))to the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `days` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the days to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the days subtracted, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusHours(hours: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of hours subtracted.

This operates on the instant time-line, such that subtracting one hour will always be a duration of one hour earlier. This may cause the local date-time to change by an amount other than one hour. Note that this is a different approach to that used by days, months and years, thus subtracting one day is not the same as adding 24 hours.

For example, consider a time-zone, such as 'Europe/Paris', where the Autumn DST cutover means that the local times 02:00 to 02:59 occur twice changing from offset +02:00 in summer to +01:00 in winter.

- Subtracting one hour from 03:30+01:00 will result in 02:30+01:00 (both in winter time)
- Subtracting one hour from 02:30+01:00 will result in 02:30+02:00 (moving from winter to summer time)
- Subtracting one hour from 02:30+02:00 will result in 01:30+02:00 (both in summer time)
- Subtracting three hours from 03:30+01:00 will result in 01:30+02:00 (moving from winter to summer time)

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `hours` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the hours to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the hours subtracted, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusMinutes(minutes: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of minutes subtracted.

This operates on the instant time-line, such that subtracting one minute will always be a duration of one minute earlier. This may cause the local date-time to change by an amount other than one minute. Note that this is a different approach to that used by days, months and years.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `minutes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minutes to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the minutes subtracted, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusMonths(months: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of months subtracted.

This operates on the local time-line, [subtracting months](LocalDateTime.md))to the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `months` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the months to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the months subtracted, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusNanos(nanos: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of nanoseconds subtracted.

This operates on the instant time-line, such that subtracting one nano will always be a duration of one nano earlier. This may cause the local date-time to change by an amount other than one nano. Note that this is a different approach to that used by days, months and years.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the nanos to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the nanoseconds subtracted, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusSeconds(seconds: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of seconds subtracted.

This operates on the instant time-line, such that subtracting one second will always be a duration of one second earlier. This may cause the local date-time to change by an amount other than one second. Note that this is a different approach to that used by days, months and years.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the seconds to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the seconds subtracted, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusWeeks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusWeeks(weeks: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of weeks subtracted.

This operates on the local time-line, [subtracting weeks](LocalDateTime.md))to the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `weeks` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the weeks to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the weeks subtracted, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusYears(years: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of years subtracted.

This operates on the local time-line, [subtracting years](LocalDateTime.md))to the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `years` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the years to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the years subtracted, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(): ZonedDateTime!
```

Obtains the current date-time from the system clock in the default time-zone.

This will query the [system clock](Clock.md))in the default time-zone to obtain the current date-time. The zone and offset will be set based on the time-zone in the clock.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the current date-time using the system clock, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(clock: Clock!): ZonedDateTime!
```

Obtains the current date-time from the specified clock.

This will query the specified clock to obtain the current date-time. The zone and offset will be set based on the time-zone in the clock.

Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using [dependency injection](Clock.md).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `clock` | [Clock](Clock.md)!:the clock to use, not null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the current date-time, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(zone: ZoneId!): ZonedDateTime!
```

Obtains the current date-time from the system clock in the specified time-zone.

This will query the [system clock](Clock.md))to obtain the current date-time. Specifying the time-zone avoids dependence on the default time-zone. The offset will be calculated from the specified time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](ZoneId.md)!:the zone ID to use, not null |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the current date-time using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    year: Int, 
    month: Int, 
    dayOfMonth: Int, 
    hour: Int, 
    minute: Int, 
    second: Int, 
    nanoOfSecond: Int, 
    zone: ZoneId!
): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from a year, month, day, hour, minute, second, nanosecond and time-zone.

This creates a zoned date-time matching the local date-time of the seven specified fields as closely as possible. Time-zone rules, such as daylight savings, mean that not every local date-time is valid for the specified zone, thus the local date-time may be adjusted.

The local date-time is resolved to a single instant on the time-line. This is achieved by finding a valid offset from UTC/Greenwich for the local date-time as defined by the [rules](../java.time.zone/ZoneRules.md) of the zone ID.

In most cases, there is only one valid offset for a local date-time. In the case of an overlap, when clocks are set back, there are two valid offsets. This method uses the earlier offset typically corresponding to "summer".

In the case of a gap, when clocks jump forward, there is no valid offset. Instead, the local date-time is adjusted to be later by the length of the gap. For a typical one hour daylight savings change, the local date-time will be moved one hour later into the offset typically corresponding to "summer".

This method exists primarily for writing test cases. Non test-code will typically use other methods to create an offset time.`LocalDateTime`has five additional convenience variants of the equivalent factory method taking fewer arguments. They are not provided here to reduce the footprint of the API.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the year to represent, from MIN_YEAR to MAX_YEAR |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the month-of-year to represent, from 1 (January) to 12 (December) |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the day-of-month to represent, from 1 to 31 |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the hour-of-day to represent, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minute-of-hour to represent, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second-of-minute to represent, from 0 to 59 |
| --- | --- |
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the nano-of-second to represent, from 0 to 999,999,999 |
| `zone` | [ZoneId](ZoneId.md)!:the time-zone, not null |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the offset date-time, not null |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month-year |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    date: LocalDate!, 
    time: LocalTime!, 
    zone: ZoneId!
): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from a local date and time.

This creates a zoned date-time matching the input local date and time as closely as possible. Time-zone rules, such as daylight savings, mean that not every local date-time is valid for the specified zone, thus the local date-time may be adjusted.

The local date time and first combined to form a local date-time. The local date-time is then resolved to a single instant on the time-line. This is achieved by finding a valid offset from UTC/Greenwich for the local date-time as defined by the [rules](../java.time.zone/ZoneRules.md) of the zone ID.

In most cases, there is only one valid offset for a local date-time. In the case of an overlap, when clocks are set back, there are two valid offsets. This method uses the earlier offset typically corresponding to "summer".

In the case of a gap, when clocks jump forward, there is no valid offset. Instead, the local date-time is adjusted to be later by the length of the gap. For a typical one hour daylight savings change, the local date-time will be moved one hour later into the offset typically corresponding to "summer".

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `date` | [LocalDate](LocalDate.md)!:the local date, not null |
| `time` | [LocalTime](LocalTime.md)!:the local time, not null |
| `zone` | [ZoneId](ZoneId.md)!:the time-zone, not null |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the offset date-time, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    localDateTime: LocalDateTime!, 
    zone: ZoneId!
): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from a local date-time.

This creates a zoned date-time matching the input local date-time as closely as possible. Time-zone rules, such as daylight savings, mean that not every local date-time is valid for the specified zone, thus the local date-time may be adjusted.

The local date-time is resolved to a single instant on the time-line. This is achieved by finding a valid offset from UTC/Greenwich for the local date-time as defined by the [rules](../java.time.zone/ZoneRules.md) of the zone ID.

In most cases, there is only one valid offset for a local date-time. In the case of an overlap, when clocks are set back, there are two valid offsets. This method uses the earlier offset typically corresponding to "summer".

In the case of a gap, when clocks jump forward, there is no valid offset. Instead, the local date-time is adjusted to be later by the length of the gap. For a typical one hour daylight savings change, the local date-time will be moved one hour later into the offset typically corresponding to "summer".

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------|
| `localDateTime` | [LocalDateTime](LocalDateTime.md)!:the local date-time, not null |
| `zone` | [ZoneId](ZoneId.md)!:the time-zone, not null |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the zoned date-time, not null |

### ofInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofInstant(
    instant: Instant!, 
    zone: ZoneId!
): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from an`Instant`.

This creates a zoned date-time with the same instant as that specified. Calling [toInstant()](../java.time.chrono/ChronoZonedDateTime.md))will return an instant equal to the one used here.

Converting an instant to a zoned date-time is simple as there is only one valid offset for each instant.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `instant` | [Instant](Instant.md)!:the instant to create the date-time from, not null |
| `zone` | [ZoneId](ZoneId.md)!:the time-zone, not null |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the zoned date-time, not null |

| Exceptions ||
|-------------------------------|-------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### ofInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofInstant(
    localDateTime: LocalDateTime!, 
    offset: ZoneOffset!, 
    zone: ZoneId!
): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from the instant formed by combining the local date-time and offset.

This creates a zoned date-time by [combining](../java.time.chrono/ChronoLocalDateTime.md))the`LocalDateTime`and`ZoneOffset`. This combination uniquely specifies an instant without ambiguity.

Converting an instant to a zoned date-time is simple as there is only one valid offset for each instant. If the valid offset is different to the offset specified, then the date-time and offset of the zoned date-time will differ from those specified.

If the`ZoneId`to be used is a`ZoneOffset`, this method is equivalent to [of(java.time.LocalDateTime,java.time.ZoneId)](ZonedDateTime.md)).

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------|
| `localDateTime` | [LocalDateTime](LocalDateTime.md)!:the local date-time, not null |
| `offset` | [ZoneOffset](ZoneOffset.md)!:the zone offset, not null |
| `zone` | [ZoneId](ZoneId.md)!:the time-zone, not null |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the zoned date-time, not null |

### ofLocal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofLocal(
    localDateTime: LocalDateTime!, 
    zone: ZoneId!, 
    preferredOffset: ZoneOffset!
): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from a local date-time using the preferred offset if possible.

The local date-time is resolved to a single instant on the time-line. This is achieved by finding a valid offset from UTC/Greenwich for the local date-time as defined by the [rules](../java.time.zone/ZoneRules.md) of the zone ID.

In most cases, there is only one valid offset for a local date-time. In the case of an overlap, where clocks are set back, there are two valid offsets. If the preferred offset is one of the valid offsets then it is used. Otherwise the earlier valid offset is used, typically corresponding to "summer".

In the case of a gap, where clocks jump forward, there is no valid offset. Instead, the local date-time is adjusted to be later by the length of the gap. For a typical one hour daylight savings change, the local date-time will be moved one hour later into the offset typically corresponding to "summer".

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| `localDateTime` | [LocalDateTime](LocalDateTime.md)!:the local date-time, not null |
| `zone` | [ZoneId](ZoneId.md)!:the time-zone, not null |
| `preferredOffset` | [ZoneOffset](ZoneOffset.md)!:the zone offset, null if no preference |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the zoned date-time, not null |

### ofStrict

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofStrict(
    localDateTime: LocalDateTime!, 
    offset: ZoneOffset!, 
    zone: ZoneId!
): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`strictly validating the combination of local date-time, offset and zone ID.

This creates a zoned date-time ensuring that the offset is valid for the local date-time according to the rules of the specified zone. If the offset is invalid, an exception is thrown.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------|
| `localDateTime` | [LocalDateTime](LocalDateTime.md)!:the local date-time, not null |
| `offset` | [ZoneOffset](ZoneOffset.md)!:the zone offset, not null |
| `zone` | [ZoneId](ZoneId.md)!:the time-zone, not null |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the zoned date-time, not null |

| Exceptions ||
|-------------------------------|--------------------------------------------|
| `java.time.DateTimeException` | if the combination of arguments is invalid |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(text: CharSequence!): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from a text string such as`2007-12-03T10:15:30+01:00[Europe/Paris]`.

The string must represent a valid date-time and is parsed using [java.time.format.DateTimeFormatter#ISO_ZONED_DATE_TIME](../java.time.format/DateTimeFormatter.md).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to parse such as "2007-12-03T10:15:30+01:00\[Europe/Paris\]", not null |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the parsed zoned date-time, not null |

| Exceptions ||
|-------------------------------------------|------------------------------|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(
    text: CharSequence!, 
    formatter: DateTimeFormatter!
): ZonedDateTime!
```

Obtains an instance of`ZonedDateTime`from a text string using a specific formatter.

The text is parsed using the formatter, returning a date-time.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to parse, not null |
| `formatter` | [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!:the formatter to use, not null |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | the parsed zoned date-time, not null |

| Exceptions ||
|-------------------------------------------|------------------------------|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(amountToAdd: TemporalAmount!): ZonedDateTime!
```

Returns a copy of this date-time with the specified amount added.

This returns a`ZonedDateTime`, based on this one, with the specified amount added. The amount is typically [Period](Period.md) or [Duration](Duration.md) but may be any other type implementing the [TemporalAmount](../java.time.temporal/TemporalAmount.md) interface.

The calculation is delegated to the amount object by calling [TemporalAmount.addTo(Temporal)](../java.time.temporal/TemporalAmount.md)). The amount implementation is free to implement the addition in any way it wishes, however it typically calls back to [plus(long,java.time.temporal.TemporalUnit)](ZonedDateTime.md)). Consult the documentation of the amount implementation to determine if it can be successfully added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------|
| `amount` | the amount to add, not null |
| `amountToAdd` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!:the amount to add, not null |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the addition made, not null |

| Exceptions ||
|---------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): ZonedDateTime!
```

Returns a copy of this date-time with the specified amount added.

This returns a`ZonedDateTime`, based on this one, with the amount in terms of the unit added. If it is not possible to add the amount, because the unit is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoUnit](../java.time.temporal/ChronoUnit.md) then the addition is implemented here. The zone is not part of the calculation and will be unchanged in the result. The calculation for date and time units differ.

Date units operate on the local time-line. The period is first added to the local date-time, then converted back to a zoned date-time using the zone ID. The conversion uses [ofLocal(java.time.LocalDateTime,java.time.ZoneId,java.time.ZoneOffset)](ZonedDateTime.md))with the offset before the addition.

Time units operate on the instant time-line. The period is first added to the local date-time, then converted back to a zoned date-time using the zone ID. The conversion uses [ofInstant(java.time.LocalDateTime,java.time.ZoneOffset,java.time.ZoneId)](ZonedDateTime.md))with the offset before the addition.

If the field is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.addTo(Temporal, long)`passing`this`as the argument. In this case, the unit determines whether and how to perform the addition.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the unit to add to the result, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit of the amount to add, not null |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the specified amount added, not null |

| Exceptions ||
|-------------------------------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### plusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusDays(days: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of days added.

This operates on the local time-line, [adding days](LocalDateTime.md))to the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `days` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the days to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the days added, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusHours(hours: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of hours added.

This operates on the instant time-line, such that adding one hour will always be a duration of one hour later. This may cause the local date-time to change by an amount other than one hour. Note that this is a different approach to that used by days, months and years, thus adding one day is not the same as adding 24 hours.

For example, consider a time-zone, such as 'Europe/Paris', where the Autumn DST cutover means that the local times 02:00 to 02:59 occur twice changing from offset +02:00 in summer to +01:00 in winter.

- Adding one hour to 01:30+02:00 will result in 02:30+02:00 (both in summer time)
- Adding one hour to 02:30+02:00 will result in 02:30+01:00 (moving from summer to winter time)
- Adding one hour to 02:30+01:00 will result in 03:30+01:00 (both in winter time)
- Adding three hours to 01:30+02:00 will result in 03:30+01:00 (moving from summer to winter time)

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `hours` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the hours to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the hours added, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusMinutes(minutes: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of minutes added.

This operates on the instant time-line, such that adding one minute will always be a duration of one minute later. This may cause the local date-time to change by an amount other than one minute. Note that this is a different approach to that used by days, months and years.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `minutes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minutes to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the minutes added, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusMonths(months: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of months added.

This operates on the local time-line, [adding months](LocalDateTime.md))to the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------|
| `months` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the months to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the months added, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusNanos(nanos: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of nanoseconds added.

This operates on the instant time-line, such that adding one nano will always be a duration of one nano later. This may cause the local date-time to change by an amount other than one nano. Note that this is a different approach to that used by days, months and years.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the nanos to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the nanoseconds added, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusSeconds(seconds: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of seconds added.

This operates on the instant time-line, such that adding one second will always be a duration of one second later. This may cause the local date-time to change by an amount other than one second. Note that this is a different approach to that used by days, months and years.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the seconds to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the seconds added, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusWeeks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusWeeks(weeks: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of weeks added.

This operates on the local time-line, [adding weeks](LocalDateTime.md))to the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `weeks` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the weeks to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the weeks added, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusYears(years: Long): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the specified number of years added.

This operates on the local time-line, [adding years](LocalDateTime.md))to the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `years` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the years to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the years added, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this date-time using the specified query.

This queries this date-time using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](../java.time.temporal/TemporalQuery.md))method on the specified query passing`this`as the argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](../java.time.temporal/TemporalQuery.md)\<R\>!:the query to invoke, not null |

| Return ||
|---|---------------------------------------------------------------|
| R | the query result, null may be returned (defined by the query) |

| Exceptions ||
|---------------------------------|---------------------------------------------------|
| `java.time.DateTimeException` | if unable to query (defined by the query) |
| `java.lang.ArithmeticException` | if numeric overflow occurs (defined by the query) |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

The range object expresses the minimum and maximum valid values for a field. This date-time is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The [supported fields](ZonedDateTime.md))will return appropriate range instances. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.rangeRefinedBy(TemporalAccessor)`passing`this`as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](../java.time.temporal/ValueRange.md)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toLocalDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLocalDate(): LocalDate!
```

Gets the`LocalDate`part of this date-time.

This returns a`LocalDate`with the same year, month and day as this date-time.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [LocalDate](LocalDate.md)! | the date part of this date-time, not null |

### toLocalDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLocalDateTime(): LocalDateTime!
```

Gets the`LocalDateTime`part of this date-time.

This returns a`LocalDateTime`with the same year, month, day and time as this date-time.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [LocalDateTime](LocalDateTime.md)! | the local date-time part of this date-time, not null |

### toLocalTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLocalTime(): LocalTime!
```

Gets the`LocalTime`part of this date-time.

This returns a`LocalTime`with the same hour, minute, second and nanosecond as this date-time.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [LocalTime](LocalTime.md)! | the time part of this date-time, not null |

### toOffsetDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toOffsetDateTime(): OffsetDateTime!
```

Converts this date-time to an`OffsetDateTime`.

This creates an offset date-time using the local date-time and offset. The zone ID is ignored.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [OffsetDateTime](OffsetDateTime.md)! | an offset date-time representing the same local date-time and offset, not null |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Outputs this date-time as a`String`, such as`2007-12-03T10:15:30+01:00[Europe/Paris]`.

The format consists of the`LocalDateTime`followed by the`ZoneOffset`. If the`ZoneId`is not the same as the offset, then the ID is output. The output is compatible with ISO-8601 if the offset and ID are the same.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this date-time, not null |

### truncatedTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun truncatedTo(unit: TemporalUnit!): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the time truncated.

Truncation returns a copy of the original date-time with fields smaller than the specified unit set to zero. For example, truncating with the [minutes](../java.time.temporal/ChronoUnit.md) unit will set the second-of-minute and nano-of-second field to zero.

The unit must have a [duration](../java.time.temporal/TemporalUnit.md))that divides into the length of a standard day without remainder. This includes all supplied time units on [ChronoUnit](../java.time.temporal/ChronoUnit.md) and [DAYS](../java.time.temporal/ChronoUnit.md). Other units throw an exception.

This operates on the local time-line, [truncating](LocalDateTime.md))the underlying local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit to truncate to, not null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the time truncated, not null |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if unable to truncate |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

Calculates the amount of time until another date-time in terms of the specified unit.

This calculates the amount of time between two`ZonedDateTime`objects in terms of a single`TemporalUnit`. The start and end points are`this`and the specified date-time. The result will be negative if the end is before the start. For example, the amount in days between two date-times can be calculated using`startDateTime.until(endDateTime, DAYS)`.

The`Temporal`passed to this method is converted to a`ZonedDateTime`using #from(java.time.temporal.TemporalAccessor). If the time-zone differs between the two zoned date-times, the specified end date-time is normalized to have the same zone as this date-time.

The calculation returns a whole number, representing the number of complete units between the two date-times. For example, the amount in months between 2012-06-15T00:00Z and 2012-08-14T23:59Z will only be one month as it is one minute short of two months.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use [TemporalUnit.between(Temporal, Temporal)](../java.time.temporal/TemporalUnit.md)): 

```kotlin
// these two lines are equivalent
    amount = start.until(end, MONTHS);
    amount = MONTHS.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for [ChronoUnit](../java.time.temporal/ChronoUnit.md). The units`NANOS`,`MICROS`,`MILLIS`,`SECONDS`,`MINUTES`,`HOURS`and`HALF_DAYS`,`DAYS`,`WEEKS`,`MONTHS`,`YEARS`,`DECADES`,`CENTURIES`,`MILLENNIA`and`ERAS`are supported. Other`ChronoUnit`values will throw an exception.

The calculation for date and time units differ.

Date units operate on the local time-line, using the local date-time. For example, the period from noon on day 1 to noon the following day in days will always be counted as exactly one day, irrespective of whether there was a daylight savings change or not.

Time units operate on the instant time-line. The calculation effectively converts both zoned date-times to instants and then calculates the period between the instants. For example, the period from noon on day 1 to noon the following day in hours may be 23, 24 or 25 hours (or some other amount) depending on whether there was a daylight savings change or not.

If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.between(Temporal, Temporal)`passing`this`as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endExclusive` | [Temporal](../java.time.temporal/Temporal.md)!:the end date, exclusive, which is converted to a`ZonedDateTime`, not null |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit to measure the amount in, not null |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between this date-time and the end date-time |

| Exceptions ||
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to a`ZonedDateTime` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun with(adjuster: TemporalAdjuster!): ZonedDateTime!
```

Returns an adjusted copy of this date-time.

This returns a`ZonedDateTime`, based on this one, with the date-time adjusted. The adjustment takes place using the specified adjuster strategy object. Read the documentation of the adjuster to understand what adjustment will be made.

A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in [TemporalAdjusters](../java.time.temporal/TemporalAdjusters.md). These include finding the "last day of the month" and "next Wednesday". Key date-time classes also implement the`TemporalAdjuster`interface, such as [Month](Month.md) and [MonthDay](MonthDay.md). The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

For example this code returns a date on the last day of July: 

```kotlin
import static java.time.Month.*;
   import static java.time.temporal.TemporalAdjusters.*;
 
   result = zonedDateTime.with(JULY).with(lastDayOfMonth());
  
```

The classes [LocalDate](LocalDate.md) and [LocalTime](LocalTime.md) implement`TemporalAdjuster`, thus this method can be used to change the date, time or offset: 

```kotlin
result = zonedDateTime.with(date);
   result = zonedDateTime.with(time);
  
```

[ZoneOffset](ZoneOffset.md) also implements`TemporalAdjuster`however using it as an argument typically has no effect. The offset of a`ZonedDateTime`is controlled primarily by the time-zone. As such, changing the offset does not generally make sense, because there is only one valid offset for the local date-time and zone. If the zoned date-time is in a daylight savings overlap, then the offset is used to switch between the two valid offsets. In all other cases, the offset is ignored.

The result of this method is obtained by invoking the [TemporalAdjuster.adjustInto(Temporal)](../java.time.temporal/TemporalAdjuster.md))method on the specified adjuster passing`this`as the argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `adjuster` | [TemporalAdjuster](../java.time.temporal/TemporalAdjuster.md)!:the adjuster to use, not null |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on`this`with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the adjustment cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun with(
    field: TemporalField!, 
    newValue: Long
): ZonedDateTime!
```

Returns a copy of this date-time with the specified field set to a new value.

This returns a`ZonedDateTime`, based on this one, with the value for the specified field changed. This can be used to change any supported field, such as the year, month or day-of-month. If it is not possible to set the value, because the field is not supported or for some other reason, an exception is thrown.

In some cases, changing the specified field can cause the resulting date-time to become invalid, such as changing the month from 31st January to February would make the day-of-month invalid. In cases like this, the field is responsible for resolving the date. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the adjustment is implemented here.

The`INSTANT_SECONDS`field will return a date-time with the specified instant. The zone and nano-of-second are unchanged. The result will have an offset derived from the new instant and original zone. If the new instant value is outside the valid range then a`DateTimeException`will be thrown.

The`OFFSET_SECONDS`field will typically be ignored. The offset of a`ZonedDateTime`is controlled primarily by the time-zone. As such, changing the offset does not generally make sense, because there is only one valid offset for the local date-time and zone. If the zoned date-time is in a daylight savings overlap, then the offset is used to switch between the two valid offsets. In all other cases, the offset is ignored. If the new offset value is outside the valid range then a`DateTimeException`will be thrown.

The other [supported fields](ZonedDateTime.md))will behave as per the matching method on [LocalDateTime](LocalDateTime.md)). The zone is not part of the calculation and will be unchanged. When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.adjustInto(Temporal, long)`passing`this`as the argument. In this case, the field determines whether and how to adjust the instant.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field in the result |

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on`this`with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### withDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withDayOfMonth(dayOfMonth: Int): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the day-of-month altered.

This operates on the local time-line, [changing the day-of-month](LocalDateTime.md))of the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the day-of-month to set in the result, from 1 to 28-31 |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested day, not null |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the day-of-month value is invalid, or if the day-of-month is invalid for the month-year |

### withDayOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withDayOfYear(dayOfYear: Int): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the day-of-year altered.

This operates on the local time-line, [changing the day-of-year](LocalDateTime.md))of the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the day-of-year to set in the result, from 1 to 365-366 |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date with the requested day, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the day-of-year value is invalid, or if the day-of-year is invalid for the year |

### withEarlierOffsetAtOverlap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withEarlierOffsetAtOverlap(): ZonedDateTime!
```

Returns a copy of this date-time changing the zone offset to the earlier of the two valid offsets at a local time-line overlap.

This method only has any effect when the local time-line overlaps, such as at an autumn daylight savings cutover. In this scenario, there are two valid offsets for the local date-time. Calling this method will return a zoned date-time with the earlier of the two selected.

If this method is called when it is not an overlap,`this`is returned.

This instance is immutable and unaffected by this method call.

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the earlier offset, not null |

| Exceptions ||
|-------------------------------|------------------------------------------|
| `java.time.DateTimeException` | if no rules are valid for this date-time |

### withFixedOffsetZone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withFixedOffsetZone(): ZonedDateTime!
```

Returns a copy of this date-time with the zone ID set to the offset.

This returns a zoned date-time where the zone ID is the same as [getOffset()](ZonedDateTime.md)). The local date-time, offset and instant of the result will be the same as in this date-time.

Setting the date-time to a fixed single offset means that any future calculations, such as addition or subtraction, have no complex edge cases due to time-zone rules. This might also be useful when sending a zoned date-time across a network, as most protocols, such as ISO-8601, only handle offsets, and not region-based zone IDs.

This is equivalent to`ZonedDateTime.of(zdt.toLocalDateTime(), zdt.getOffset())`.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`with the zone ID set to the offset, not null |

### withHour

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withHour(hour: Int): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the hour-of-day altered.

This operates on the local time-line, [changing the time](LocalDateTime.md))of the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the hour-of-day to set in the result, from 0 to 23 |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested hour, not null |

| Exceptions ||
|-------------------------------|------------------------------|
| `java.time.DateTimeException` | if the hour value is invalid |

### withLaterOffsetAtOverlap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withLaterOffsetAtOverlap(): ZonedDateTime!
```

Returns a copy of this date-time changing the zone offset to the later of the two valid offsets at a local time-line overlap.

This method only has any effect when the local time-line overlaps, such as at an autumn daylight savings cutover. In this scenario, there are two valid offsets for the local date-time. Calling this method will return a zoned date-time with the later of the two selected.

If this method is called when it is not an overlap,`this`is returned.

This instance is immutable and unaffected by this method call.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the later offset, not null |

| Exceptions ||
|-------------------------------|------------------------------------------|
| `java.time.DateTimeException` | if no rules are valid for this date-time |

### withMinute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withMinute(minute: Int): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the minute-of-hour altered.

This operates on the local time-line, [changing the time](LocalDateTime.md))of the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minute-of-hour to set in the result, from 0 to 59 |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested minute, not null |

| Exceptions ||
|-------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the minute value is invalid |

### withMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withMonth(month: Int): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the month-of-year altered.

This operates on the local time-line, [changing the month](LocalDateTime.md))of the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the month-of-year to set in the result, from 1 (January) to 12 (December) |

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested month, not null |

| Exceptions ||
|-------------------------------|---------------------------------------|
| `java.time.DateTimeException` | if the month-of-year value is invalid |

### withNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withNano(nanoOfSecond: Int): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the nano-of-second altered.

This operates on the local time-line, [changing the time](LocalDateTime.md))of the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the nano-of-second to set in the result, from 0 to 999,999,999 |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested nanosecond, not null |

| Exceptions ||
|-------------------------------|------------------------------|
| `java.time.DateTimeException` | if the nano value is invalid |

### withSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withSecond(second: Int): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the second-of-minute altered.

This operates on the local time-line, [changing the time](LocalDateTime.md))of the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second-of-minute to set in the result, from 0 to 59 |

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested second, not null |

| Exceptions ||
|-------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the second value is invalid |

### withYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withYear(year: Int): ZonedDateTime!
```

Returns a copy of this`ZonedDateTime`with the year altered.

This operates on the local time-line, [changing the year](LocalDateTime.md))of the local date-time. This is then converted back to a`ZonedDateTime`, using the zone ID to obtain the offset.

When converting back to`ZonedDateTime`, if the local date-time is in an overlap, then the offset will be retained if possible, otherwise the earlier offset will be used. If in a gap, the local date-time will be adjusted forward by the length of the gap.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the year to set in the result, from MIN_YEAR to MAX_YEAR |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested year, not null |

| Exceptions ||
|-------------------------------|------------------------------|
| `java.time.DateTimeException` | if the year value is invalid |

### withZoneSameInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withZoneSameInstant(zone: ZoneId!): ZonedDateTime!
```

Returns a copy of this date-time with a different time-zone, retaining the instant.

This method changes the time-zone and retains the instant. This normally results in a change to the local date-time.

This method is based on retaining the same instant, thus gaps and overlaps in the local time-line have no effect on the result.

To change the offset while keeping the local time, use [withZoneSameLocal(java.time.ZoneId)](ZonedDateTime.md)).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](ZoneId.md)!:the time-zone to change to, not null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested zone, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### withZoneSameLocal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withZoneSameLocal(zone: ZoneId!): ZonedDateTime!
```

Returns a copy of this date-time with a different time-zone, retaining the local date-time if possible.

This method changes the time-zone and retains the local date-time. The local date-time is only changed if it is invalid for the new zone, determined using the same approach as [ofLocal(java.time.LocalDateTime,java.time.ZoneId,java.time.ZoneOffset)](ZonedDateTime.md)).

To change the zone and adjust the local date-time, use [withZoneSameInstant(java.time.ZoneId)](ZonedDateTime.md)).

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](ZoneId.md)!:the time-zone to change to, not null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ZonedDateTime](ZonedDateTime.md)! | a`ZonedDateTime`based on this date-time with the requested zone, not null |
