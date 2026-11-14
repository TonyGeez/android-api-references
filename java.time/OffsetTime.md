# OffsetTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OffsetTime

```
class OffsetTime : Comparable<OffsetTime!>, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#) |

A time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`10:15:30+01:00`.

`OffsetTime`is an immutable date-time object that represents a time, often viewed as hour-minute-second-offset. This class stores all time fields, to a precision of nanoseconds, as well as a zone offset. For example, the value "13:45:30.123456789+02:00" can be stored in an`OffsetTime`.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)! | [adjustInto](https://developer.android.com/reference/kotlin/java/time/OffsetTime#adjustInto(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!`)` Adjusts the specified temporal object to have the same offset and time as this object. |
| [OffsetDateTime](https://developer.android.com/reference/kotlin/java/time/OffsetDateTime)! | [atDate](https://developer.android.com/reference/kotlin/java/time/OffsetTime#atDate(java.time.LocalDate))`(`date:` ` [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)!`)` Combines this time with a date to create an`OffsetDateTime`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/time/OffsetTime#compareTo(java.time.OffsetTime))`(`other:` ` [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)!`)` Compares this`OffsetTime`to another time. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/time/OffsetTime#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this time is equal to another time. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/time/OffsetTime#format(java.time.format.DateTimeFormatter))`(`formatter:` ` [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!`)` Formats this time using the specified formatter. |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [from](https://developer.android.com/reference/kotlin/java/time/OffsetTime#from(java.time.temporal.TemporalAccessor))`(`temporal:` ` [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor)!`)` Obtains an instance of`OffsetTime`from a temporal object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/OffsetTime#get(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the value of the specified field from this time as an`int`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHour](https://developer.android.com/reference/kotlin/java/time/OffsetTime#getHour())`()` Gets the hour-of-day field. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/OffsetTime#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the value of the specified field from this time as a`long`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinute](https://developer.android.com/reference/kotlin/java/time/OffsetTime#getMinute())`()` Gets the minute-of-hour field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNano](https://developer.android.com/reference/kotlin/java/time/OffsetTime#getNano())`()` Gets the nano-of-second field. |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)! | [getOffset](https://developer.android.com/reference/kotlin/java/time/OffsetTime#getOffset())`()` Gets the zone offset, such as '+01:00'. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecond](https://developer.android.com/reference/kotlin/java/time/OffsetTime#getSecond())`()` Gets the second-of-minute field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/time/OffsetTime#hashCode())`()` A hash code for this time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfter](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isAfter(java.time.OffsetTime))`(`other:` ` [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)!`)` Checks if the instant of this`OffsetTime`is after that of the specified time applying both times to a common date. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBefore](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isBefore(java.time.OffsetTime))`(`other:` ` [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)!`)` Checks if the instant of this`OffsetTime`is before that of the specified time applying both times to a common date. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqual](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isEqual(java.time.OffsetTime))`(`other:` ` [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)!`)` Checks if the instant of this`OffsetTime`is equal to that of the specified time applying both times to a common date. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Checks if the specified field is supported. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isSupported(java.time.temporal.TemporalUnit))`(`unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Checks if the specified unit is supported. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [minus](https://developer.android.com/reference/kotlin/java/time/OffsetTime#minus(java.time.temporal.TemporalAmount))`(`amountToSubtract:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!`)` Returns a copy of this time with the specified amount subtracted. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [minus](https://developer.android.com/reference/kotlin/java/time/OffsetTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Returns a copy of this time with the specified amount subtracted. |
| --- | --- |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [minusHours](https://developer.android.com/reference/kotlin/java/time/OffsetTime#minusHours(kotlin.Long))`(`hours:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`OffsetTime`with the specified number of hours subtracted. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [minusMinutes](https://developer.android.com/reference/kotlin/java/time/OffsetTime#minusMinutes(kotlin.Long))`(`minutes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`OffsetTime`with the specified number of minutes subtracted. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [minusNanos](https://developer.android.com/reference/kotlin/java/time/OffsetTime#minusNanos(kotlin.Long))`(`nanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`OffsetTime`with the specified number of nanoseconds subtracted. |
| --- | --- |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [minusSeconds](https://developer.android.com/reference/kotlin/java/time/OffsetTime#minusSeconds(kotlin.Long))`(`seconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`OffsetTime`with the specified number of seconds subtracted. |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [now](https://developer.android.com/reference/kotlin/java/time/OffsetTime#now())`()` Obtains the current time from the system clock in the default time-zone. |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [now](https://developer.android.com/reference/kotlin/java/time/OffsetTime#now(java.time.Clock))`(`clock:` ` [Clock](https://developer.android.com/reference/kotlin/java/time/Clock)!`)` Obtains the current time from the specified clock. |
| --- | --- |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [now](https://developer.android.com/reference/kotlin/java/time/OffsetTime#now(java.time.ZoneId))`(`zone:` ` [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!`)` Obtains the current time from the system clock in the specified time-zone. |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [of](https://developer.android.com/reference/kotlin/java/time/OffsetTime#of(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.time.ZoneOffset))`(`hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nanoOfSecond:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!`)` Obtains an instance of`OffsetTime`from an hour, minute, second and nanosecond. |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [of](https://developer.android.com/reference/kotlin/java/time/OffsetTime#of(java.time.LocalTime,%20java.time.ZoneOffset))`(`time:` ` [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime)!`, `offset:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!`)` Obtains an instance of`OffsetTime`from a local time and an offset. |
| --- | --- |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [ofInstant](https://developer.android.com/reference/kotlin/java/time/OffsetTime#ofInstant(java.time.Instant,%20java.time.ZoneId))`(`instant:` ` [Instant](https://developer.android.com/reference/kotlin/java/time/Instant)!`, `zone:` ` [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!`)` Obtains an instance of`OffsetTime`from an`Instant`and zone ID. |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [parse](https://developer.android.com/reference/kotlin/java/time/OffsetTime#parse(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Obtains an instance of`OffsetTime`from a text string such as`10:15:30+01:00`. |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [parse](https://developer.android.com/reference/kotlin/java/time/OffsetTime#parse(kotlin.CharSequence,%20java.time.format.DateTimeFormatter))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `formatter:` ` [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!`)` Obtains an instance of`OffsetTime`from a text string using a specific formatter. |
| --- | --- |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [plus](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plus(java.time.temporal.TemporalAmount))`(`amountToAdd:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!`)` Returns a copy of this time with the specified amount added. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [plus](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Returns a copy of this time with the specified amount added. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [plusHours](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plusHours(kotlin.Long))`(`hours:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`OffsetTime`with the specified number of hours added. |
| --- | --- |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [plusMinutes](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plusMinutes(kotlin.Long))`(`minutes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`OffsetTime`with the specified number of minutes added. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [plusNanos](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plusNanos(kotlin.Long))`(`nanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`OffsetTime`with the specified number of nanoseconds added. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [plusSeconds](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plusSeconds(kotlin.Long))`(`seconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this`OffsetTime`with the specified number of seconds added. |
| --- | --- |
| R | [query](https://developer.android.com/reference/kotlin/java/time/OffsetTime#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)<R>!`)` Queries this time using the specified query. |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | [range](https://developer.android.com/reference/kotlin/java/time/OffsetTime#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the range of valid values for the specified field. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toEpochSecond](https://developer.android.com/reference/kotlin/java/time/OffsetTime#toEpochSecond(java.time.LocalDate))`(`date:` ` [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)!`)` Converts this`OffsetTime`to the number of seconds since the epoch of 1970-01-01T00:00:00Z. |
| --- | --- |
| [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime)! | [toLocalTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#toLocalTime())`()` Gets the`LocalTime`part of this date-time. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/time/OffsetTime#toString())`()` Outputs this time as a`String`, such as`10:15:30+01:00`. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [truncatedTo](https://developer.android.com/reference/kotlin/java/time/OffsetTime#truncatedTo(java.time.temporal.TemporalUnit))`(`unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Returns a copy of this`OffsetTime`with the time truncated. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](https://developer.android.com/reference/kotlin/java/time/OffsetTime#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit))`(`endExclusive:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Calculates the amount of time until another time in terms of the specified unit. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [with](https://developer.android.com/reference/kotlin/java/time/OffsetTime#with(java.time.temporal.TemporalAdjuster))`(`adjuster:` ` [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster)!`)` Returns an adjusted copy of this time. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [with](https://developer.android.com/reference/kotlin/java/time/OffsetTime#with(java.time.temporal.TemporalField,%20kotlin.Long))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this time with the specified field set to a new value. |
| --- | --- |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [withHour](https://developer.android.com/reference/kotlin/java/time/OffsetTime#withHour(kotlin.Int))`(`hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`OffsetTime`with the hour-of-day altered. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [withMinute](https://developer.android.com/reference/kotlin/java/time/OffsetTime#withMinute(kotlin.Int))`(`minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`OffsetTime`with the minute-of-hour altered. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [withNano](https://developer.android.com/reference/kotlin/java/time/OffsetTime#withNano(kotlin.Int))`(`nanoOfSecond:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`OffsetTime`with the nano-of-second altered. |
| --- | --- |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [withOffsetSameInstant](https://developer.android.com/reference/kotlin/java/time/OffsetTime#withOffsetSameInstant(java.time.ZoneOffset))`(`offset:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!`)` Returns a copy of this`OffsetTime`with the specified offset ensuring that the result is at the same instant on an implied day. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [withOffsetSameLocal](https://developer.android.com/reference/kotlin/java/time/OffsetTime#withOffsetSameLocal(java.time.ZoneOffset))`(`offset:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!`)` Returns a copy of this`OffsetTime`with the specified offset ensuring that the result has the same local time. |
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [withSecond](https://developer.android.com/reference/kotlin/java/time/OffsetTime#withSecond(kotlin.Int))`(`second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this`OffsetTime`with the second-of-minute altered. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [MAX](https://developer.android.com/reference/kotlin/java/time/OffsetTime#MAX:java.time.OffsetTime) The maximum supported`OffsetTime`, '23:59:59. |
| static [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | [MIN](https://developer.android.com/reference/kotlin/java/time/OffsetTime#MIN:java.time.OffsetTime) The minimum supported`OffsetTime`, '00:00:00+18:00'. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same offset and time as this object.

This returns a temporal object of the same observable type as the input with the offset and time changed to be the same as this.

The adjustment is equivalent to using [Temporal.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long))twice, passing [ChronoField.NANO_OF_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) and [ChronoField.OFFSET_SECONDS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) as the fields.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisOffsetTime.adjustInto(temporal);
    temporal = temporal.with(thisOffsetTime);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!:the target object to be adjusted, not null |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)! | the adjusted object, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### atDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun atDate(date: LocalDate!): OffsetDateTime!
```

Combines this time with a date to create an`OffsetDateTime`.

This returns an`OffsetDateTime`formed from this time and the specified date. All possible combinations of date and time are valid.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `date` | [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)!:the date to combine with, not null |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [OffsetDateTime](https://developer.android.com/reference/kotlin/java/time/OffsetDateTime)! | the offset date-time formed from this time and the specified date, not null |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: OffsetTime!): Int
```

Compares this`OffsetTime`to another time.

The comparison is based first on the UTC equivalent instant, then on the local time. It is "consistent with equals", as defined by [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#).

For example, the following is the comparator order:

1. `10:30+01:00`
2. `11:00+01:00`
3. `12:00+02:00`
4. `11:30+01:00`
5. `12:00+01:00`
6. `12:30+01:00`

Values #2 and #3 represent the same instant on the time-line. When two values represent the same instant, the local time is compared to distinguish them. This step is needed to make the ordering consistent with`equals()`.

To compare the underlying local time of two`TemporalAccessor`instances, use [ChronoField.NANO_OF_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) as a comparator.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)!:the other time to compare to, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the comparator value, negative if less, positive if greater |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Checks if this time is equal to another time.

The comparison is based on the local-time and the offset. To compare for the same instant on the time-line, use [isEqual(java.time.OffsetTime)](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isEqual(java.time.OffsetTime)).

Only objects of type`OffsetTime`are compared, other types return false. To compare the underlying local time of two`TemporalAccessor`instances, use [ChronoField.NANO_OF_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) as a comparator.

| Parameters ||
|-------|-----------------------------------------|
| `obj` | the object to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is equal to the other time |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(formatter: DateTimeFormatter!): String!
```

Formats this time using the specified formatter.

This time will be passed to the formatter to produce a string.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `formatter` | [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!:the formatter to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted time string, not null |

| Exceptions ||
|-------------------------------|------------------------------------|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun from(temporal: TemporalAccessor!): OffsetTime!
```

Obtains an instance of`OffsetTime`from a temporal object.

This obtains an offset time based on the specified temporal. A`TemporalAccessor`represents an arbitrary set of date and time information, which this factory converts to an instance of`OffsetTime`.

The conversion extracts and combines the`ZoneOffset`and the`LocalTime`from the temporal object. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects.

This method matches the signature of the functional interface [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery) allowing it to be used as a query via method reference,`OffsetTime::from`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor)!:the temporal object to convert, not null |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the offset time, not null |

| Exceptions ||
|-------------------------------|----------------------------------------|
| `java.time.DateTimeException` | if unable to convert to an`OffsetTime` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this time as an`int`.

This queries this time for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the query is implemented here. The [supported fields](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isSupported(java.time.temporal.TemporalField))will return valid values based on this time, except`NANO_OF_DAY`and`MICRO_OF_DAY`which are too large to fit in an`int`and throw an`UnsupportedTemporalTypeException`. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to get, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an`int` |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

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

Gets the value of the specified field from this time as a`long`.

This queries this time for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the query is implemented here. The [supported fields](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isSupported(java.time.temporal.TemporalField))will return valid values based on this time. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to get, not null |

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

This is the offset of the local time from UTC/Greenwich.

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)! | the zone offset, not null |

### getSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecond(): Int
```

Gets the second-of-minute field.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the second-of-minute, from 0 to 59 |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

A hash code for this time.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a suitable hash code |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAfter(other: OffsetTime!): Boolean
```

Checks if the instant of this`OffsetTime`is after that of the specified time applying both times to a common date.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/OffsetTime#compareTo(java.time.OffsetTime))in that it only compares the instant of the time. This is equivalent to converting both times to an instant using the same date and comparing the instants.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `other` | [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)!:the other time to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is after the instant of the specified time |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBefore(other: OffsetTime!): Boolean
```

Checks if the instant of this`OffsetTime`is before that of the specified time applying both times to a common date.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/OffsetTime#compareTo(java.time.OffsetTime))in that it only compares the instant of the time. This is equivalent to converting both times to an instant using the same date and comparing the instants.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `other` | [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)!:the other time to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is before the instant of the specified time |

### isEqual

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEqual(other: OffsetTime!): Boolean
```

Checks if the instant of this`OffsetTime`is equal to that of the specified time applying both times to a common date.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/OffsetTime#compareTo(java.time.OffsetTime))and [equals](https://developer.android.com/reference/kotlin/java/time/OffsetTime#equals(kotlin.Any))in that it only compares the instant of the time. This is equivalent to converting both times to an instant using the same date and comparing the instants.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `other` | [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)!:the other time to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is equal to the instant of the specified time |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this time can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/OffsetTime#range(java.time.temporal.TemporalField)), [get](https://developer.android.com/reference/kotlin/java/time/OffsetTime#get(java.time.temporal.TemporalField))and [with(java.time.temporal.TemporalField,long)](https://developer.android.com/reference/kotlin/java/time/OffsetTime#with(java.time.temporal.TemporalField,%20kotlin.Long))methods will throw an exception.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the query is implemented here. The supported fields are:

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
- `OFFSET_SECONDS`

All other`ChronoField`instances will return false.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field is supported on this time, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this offset-time. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))and [minus](https://developer.android.com/reference/kotlin/java/time/OffsetTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))methods will throw an exception.

If the unit is a [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit) then the query is implemented here. The supported units are:

- `NANOS`
- `MICROS`
- `MILLIS`
- `SECONDS`
- `MINUTES`
- `HOURS`
- `HALF_DAYS`

All other`ChronoUnit`instances will return false.

If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.isSupportedBy(Temporal)`passing`this`as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit can be added/subtracted, false if not |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(amountToSubtract: TemporalAmount!): OffsetTime!
```

Returns a copy of this time with the specified amount subtracted.

This returns an`OffsetTime`, based on this one, with the specified amount subtracted. The amount is typically [Duration](https://developer.android.com/reference/kotlin/java/time/Duration) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount) interface.

The calculation is delegated to the amount object by calling [TemporalAmount.subtractFrom(Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#subtractFrom(java.time.temporal.Temporal)). The amount implementation is free to implement the subtraction in any way it wishes, however it typically calls back to [minus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/OffsetTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)). Consult the documentation of the amount implementation to determine if it can be successfully subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | the amount to subtract, not null |
| `amountToSubtract` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!:the amount to subtract, not null |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the subtraction made, not null |

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
): OffsetTime!
```

Returns a copy of this time with the specified amount subtracted.

This returns an`OffsetTime`, based on this one, with the amount in terms of the unit subtracted. If it is not possible to subtract the amount, because the unit is not supported or for some other reason, an exception is thrown.

This method is equivalent to [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))with the amount negated. See that method for a full description of how addition, and thus subtraction, works.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the unit to subtract from the result, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit of the amount to subtract, not null |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the specified amount subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------|
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### minusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusHours(hours: Long): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified number of hours subtracted.

This subtracts the specified number of hours from this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `hours` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the hours to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the hours subtracted, not null |

### minusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusMinutes(minutes: Long): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified number of minutes subtracted.

This subtracts the specified number of minutes from this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `minutes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minutes to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the minutes subtracted, not null |

### minusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusNanos(nanos: Long): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified number of nanoseconds subtracted.

This subtracts the specified number of nanoseconds from this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the nanos to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the nanoseconds subtracted, not null |

### minusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusSeconds(seconds: Long): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified number of seconds subtracted.

This subtracts the specified number of seconds from this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the seconds to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the seconds subtracted, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(): OffsetTime!
```

Obtains the current time from the system clock in the default time-zone.

This will query the [system clock](https://developer.android.com/reference/kotlin/java/time/Clock#systemDefaultZone())in the default time-zone to obtain the current time. The offset will be calculated from the time-zone in the clock.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the current time using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(clock: Clock!): OffsetTime!
```

Obtains the current time from the specified clock.

This will query the specified clock to obtain the current time. The offset will be calculated from the time-zone in the clock.

Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using [dependency injection](https://developer.android.com/reference/kotlin/java/time/Clock).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `clock` | [Clock](https://developer.android.com/reference/kotlin/java/time/Clock)!:the clock to use, not null |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the current time, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(zone: ZoneId!): OffsetTime!
```

Obtains the current time from the system clock in the specified time-zone.

This will query the [system clock](https://developer.android.com/reference/kotlin/java/time/Clock#system(java.time.ZoneId))to obtain the current time. Specifying the time-zone avoids dependence on the default time-zone. The offset will be calculated from the specified time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!:the zone ID to use, not null |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the current time using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    hour: Int, 
    minute: Int, 
    second: Int, 
    nanoOfSecond: Int, 
    offset: ZoneOffset!
): OffsetTime!
```

Obtains an instance of`OffsetTime`from an hour, minute, second and nanosecond.

This creates an offset time with the four specified fields.

This method exists primarily for writing test cases. Non test-code will typically use other methods to create an offset time.`LocalTime`has two additional convenience variants of the equivalent factory method taking fewer arguments. They are not provided here to reduce the footprint of the API.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the hour-of-day to represent, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minute-of-hour to represent, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second-of-minute to represent, from 0 to 59 |
| --- | --- |
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the nano-of-second to represent, from 0 to 999,999,999 |
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!:the zone offset, not null |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the offset time, not null |

| Exceptions ||
|-------------------------------|-------------------------------------------|
| `java.time.DateTimeException` | if the value of any field is out of range |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    time: LocalTime!, 
    offset: ZoneOffset!
): OffsetTime!
```

Obtains an instance of`OffsetTime`from a local time and an offset.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `time` | [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime)!:the local time, not null |
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!:the zone offset, not null |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the offset time, not null |

### ofInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofInstant(
    instant: Instant!, 
    zone: ZoneId!
): OffsetTime!
```

Obtains an instance of`OffsetTime`from an`Instant`and zone ID.

This creates an offset time with the same instant as that specified. Finding the offset from UTC/Greenwich is simple as there is only one valid offset for each instant.

The date component of the instant is dropped during the conversion. This means that the conversion can never fail due to the instant being out of the valid range of dates.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `instant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant)!:the instant to create the time from, not null |
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!:the time-zone, which may be an offset, not null |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the offset time, not null |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(text: CharSequence!): OffsetTime!
```

Obtains an instance of`OffsetTime`from a text string such as`10:15:30+01:00`.

The string must represent a valid time and is parsed using [java.time.format.DateTimeFormatter#ISO_OFFSET_TIME](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_TIME:java.time.format.DateTimeFormatter).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to parse such as "10:15:30+01:00", not null |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the parsed local time, not null |

| Exceptions ||
|-------------------------------------------|------------------------------|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(
    text: CharSequence!, 
    formatter: DateTimeFormatter!
): OffsetTime!
```

Obtains an instance of`OffsetTime`from a text string using a specific formatter.

The text is parsed using the formatter, returning a time.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to parse, not null |
| `formatter` | [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!:the formatter to use, not null |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | the parsed offset time, not null |

| Exceptions ||
|-------------------------------------------|------------------------------|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(amountToAdd: TemporalAmount!): OffsetTime!
```

Returns a copy of this time with the specified amount added.

This returns an`OffsetTime`, based on this one, with the specified amount added. The amount is typically [Duration](https://developer.android.com/reference/kotlin/java/time/Duration) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount) interface.

The calculation is delegated to the amount object by calling [TemporalAmount.addTo(Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#addTo(java.time.temporal.Temporal)). The amount implementation is free to implement the addition in any way it wishes, however it typically calls back to [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/OffsetTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)). Consult the documentation of the amount implementation to determine if it can be successfully added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------|
| `amount` | the amount to add, not null |
| `amountToAdd` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!:the amount to add, not null |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the addition made, not null |

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
): OffsetTime!
```

Returns a copy of this time with the specified amount added.

This returns an`OffsetTime`, based on this one, with the amount in terms of the unit added. If it is not possible to add the amount, because the unit is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit) then the addition is implemented by [LocalTime.plus(long, TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/LocalTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)). The offset is not part of the calculation and will be unchanged in the result.

If the field is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.addTo(Temporal, long)`passing`this`as the argument. In this case, the unit determines whether and how to perform the addition.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the unit to add to the result, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit of the amount to add, not null |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the specified amount added, not null |

| Exceptions ||
|-------------------------------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### plusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusHours(hours: Long): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified number of hours added.

This adds the specified number of hours to this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `hours` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the hours to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the hours added, not null |

### plusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusMinutes(minutes: Long): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified number of minutes added.

This adds the specified number of minutes to this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `minutes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minutes to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the minutes added, not null |

### plusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusNanos(nanos: Long): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified number of nanoseconds added.

This adds the specified number of nanoseconds to this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the nanos to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the nanoseconds added, not null |

### plusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusSeconds(seconds: Long): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified number of seconds added.

This adds the specified number of seconds to this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the seconds to add, may be negative |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the seconds added, not null |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this time using the specified query.

This queries this time using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery#queryFrom(java.time.temporal.TemporalAccessor))method on the specified query passing`this`as the argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\<R\>!:the query to invoke, not null |

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

The range object expresses the minimum and maximum valid values for a field. This time is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the query is implemented here. The [supported fields](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isSupported(java.time.temporal.TemporalField))will return appropriate range instances. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.rangeRefinedBy(TemporalAccessor)`passing`this`as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toEpochSecond

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toEpochSecond(date: LocalDate!): Long
```

Converts this`OffsetTime`to the number of seconds since the epoch of 1970-01-01T00:00:00Z.

This combines this offset time with the specified date to calculate the epoch-second value, which is the number of elapsed seconds from 1970-01-01T00:00:00Z. Instants on the time-line after the epoch are positive, earlier are negative.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `date` | [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)!:the localdate, not null |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of seconds since the epoch of 1970-01-01T00:00:00Z, may be negative |

### toLocalTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLocalTime(): LocalTime!
```

Gets the`LocalTime`part of this date-time.

This returns a`LocalTime`with the same hour, minute, second and nanosecond as this date-time.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime)! | the time part of this date-time, not null |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Outputs this time as a`String`, such as`10:15:30+01:00`.

The output will be one of the following ISO-8601 formats:

- `HH:mmXXXXX`
- `HH:mm:ssXXXXX`
- `HH:mm:ss.SSSXXXXX`
- `HH:mm:ss.SSSSSSXXXXX`
- `HH:mm:ss.SSSSSSSSSXXXXX`

The format used will be the shortest that outputs the full value of the time where the omitted parts are implied to be zero.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this time, not null |

### truncatedTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun truncatedTo(unit: TemporalUnit!): OffsetTime!
```

Returns a copy of this`OffsetTime`with the time truncated.

Truncation returns a copy of the original time with fields smaller than the specified unit set to zero. For example, truncating with the [minutes](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit) unit will set the second-of-minute and nano-of-second field to zero.

The unit must have a [duration](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#getDuration())that divides into the length of a standard day without remainder. This includes all supplied time units on [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit) and [DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit). Other units throw an exception.

The offset does not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit to truncate to, not null |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the time truncated, not null |

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

Calculates the amount of time until another time in terms of the specified unit.

This calculates the amount of time between two`OffsetTime`objects in terms of a single`TemporalUnit`. The start and end points are`this`and the specified time. The result will be negative if the end is before the start. For example, the amount in hours between two times can be calculated using`startTime.until(endTime, HOURS)`.

The`Temporal`passed to this method is converted to a`OffsetTime`using [from(java.time.temporal.TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/OffsetTime#from(java.time.temporal.TemporalAccessor)). If the offset differs between the two times, then the specified end time is normalized to have the same offset as this time.

The calculation returns a whole number, representing the number of complete units between the two times. For example, the amount in hours between 11:30Z and 13:29Z will only be one hour as it is one minute short of two hours.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use [TemporalUnit.between(Temporal, Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)): 

```kotlin
// these two lines are equivalent
    amount = start.until(end, MINUTES);
    amount = MINUTES.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit). The units`NANOS`,`MICROS`,`MILLIS`,`SECONDS`,`MINUTES`,`HOURS`and`HALF_DAYS`are supported. Other`ChronoUnit`values will throw an exception.

If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.between(Temporal, Temporal)`passing`this`as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endExclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!:the end time, exclusive, which is converted to an`OffsetTime`, not null |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit to measure the amount in, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between this time and the end time |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to an`OffsetTime` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun with(adjuster: TemporalAdjuster!): OffsetTime!
```

Returns an adjusted copy of this time.

This returns an`OffsetTime`, based on this one, with the time adjusted. The adjustment takes place using the specified adjuster strategy object. Read the documentation of the adjuster to understand what adjustment will be made.

A simple adjuster might simply set the one of the fields, such as the hour field. A more complex adjuster might set the time to the last hour of the day.

The classes [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime) and [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset) implement`TemporalAdjuster`, thus this method can be used to change the time or offset: 

```kotlin
result = offsetTime.with(time);
   result = offsetTime.with(offset);
  
```

The result of this method is obtained by invoking the [TemporalAdjuster.adjustInto(Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster#adjustInto(java.time.temporal.Temporal))method on the specified adjuster passing`this`as the argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `adjuster` | [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster)!:the adjuster to use, not null |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on`this`with the adjustment made, not null |

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
): OffsetTime!
```

Returns a copy of this time with the specified field set to a new value.

This returns an`OffsetTime`, based on this one, with the value for the specified field changed. This can be used to change any supported field, such as the hour, minute or second. If it is not possible to set the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the adjustment is implemented here.

The`OFFSET_SECONDS`field will return a time with the specified offset. The local time is unaltered. If the new offset value is outside the valid range then a`DateTimeException`will be thrown.

The other [supported fields](https://developer.android.com/reference/kotlin/java/time/OffsetTime#isSupported(java.time.temporal.TemporalField))will behave as per the matching method on [LocalTime.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/LocalTime#with(java.time.temporal.TemporalField,%20kotlin.Long))LocalTime}. In this case, the offset is not part of the calculation and will be unchanged.

All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.adjustInto(Temporal, long)`passing`this`as the argument. In this case, the field determines whether and how to adjust the instant.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field in the result |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on`this`with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### withHour

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withHour(hour: Int): OffsetTime!
```

Returns a copy of this`OffsetTime`with the hour-of-day altered.

The offset does not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the hour-of-day to set in the result, from 0 to 23 |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the requested hour, not null |

| Exceptions ||
|-------------------------------|------------------------------|
| `java.time.DateTimeException` | if the hour value is invalid |

### withMinute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withMinute(minute: Int): OffsetTime!
```

Returns a copy of this`OffsetTime`with the minute-of-hour altered.

The offset does not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minute-of-hour to set in the result, from 0 to 59 |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the requested minute, not null |

| Exceptions ||
|-------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the minute value is invalid |

### withNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withNano(nanoOfSecond: Int): OffsetTime!
```

Returns a copy of this`OffsetTime`with the nano-of-second altered.

The offset does not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the nano-of-second to set in the result, from 0 to 999,999,999 |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the requested nanosecond, not null |

| Exceptions ||
|-------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the nanos value is invalid |

### withOffsetSameInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withOffsetSameInstant(offset: ZoneOffset!): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified offset ensuring that the result is at the same instant on an implied day.

This method returns an object with the specified`ZoneOffset`and a`LocalTime`adjusted by the difference between the two offsets. This will result in the old and new objects representing the same instant on an implied day. This is useful for finding the local time in a different offset. For example, if this time represents`10:30+02:00`and the offset specified is`+03:00`, then this method will return`11:30+03:00`.

To change the offset without adjusting the local time use [withOffsetSameLocal](https://developer.android.com/reference/kotlin/java/time/OffsetTime#withOffsetSameLocal(java.time.ZoneOffset)).

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!:the zone offset to change to, not null |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the requested offset, not null |

### withOffsetSameLocal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withOffsetSameLocal(offset: ZoneOffset!): OffsetTime!
```

Returns a copy of this`OffsetTime`with the specified offset ensuring that the result has the same local time.

This method returns an object with the same`LocalTime`and the specified`ZoneOffset`. No calculation is needed or performed. For example, if this time represents`10:30+02:00`and the offset specified is`+03:00`, then this method will return`10:30+03:00`.

To take into account the difference between the offsets, and adjust the time fields, use [withOffsetSameInstant](https://developer.android.com/reference/kotlin/java/time/OffsetTime#withOffsetSameInstant(java.time.ZoneOffset)).

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!:the zone offset to change to, not null |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the requested offset, not null |

### withSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withSecond(second: Int): OffsetTime!
```

Returns a copy of this`OffsetTime`with the second-of-minute altered.

The offset does not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second-of-minute to set in the result, from 0 to 59 |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime#)! | an`OffsetTime`based on this time with the requested second, not null |

| Exceptions ||
|-------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the second value is invalid |

## Properties

### MAX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX: OffsetTime!
```

The maximum supported`OffsetTime`, '23:59:59.999999999-18:00'. This is the time just before midnight at the end of the day in the minimum offset (larger negative offsets are later on the time-line). This combines [LocalTime.MAX](https://developer.android.com/reference/kotlin/java/time/LocalTime#MAX:java.time.LocalTime) and [ZoneOffset.MIN](https://developer.android.com/reference/kotlin/java/time/ZoneOffset#MIN:java.time.ZoneOffset). This could be used by an application as a "far future" date. 

### MIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN: OffsetTime!
```

The minimum supported`OffsetTime`, '00:00:00+18:00'. This is the time of midnight at the start of the day in the maximum offset (larger offsets are earlier on the time-line). This combines [LocalTime.MIN](https://developer.android.com/reference/kotlin/java/time/LocalTime#MIN:java.time.LocalTime) and [ZoneOffset.MAX](https://developer.android.com/reference/kotlin/java/time/ZoneOffset#MAX:java.time.ZoneOffset). This could be used by an application as a "far past" date.
