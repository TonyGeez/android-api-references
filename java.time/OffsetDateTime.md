Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OffsetDateTime

```
class OffsetDateTime : Comparable<OffsetDateTime!>, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.OffsetDateTime](OffsetDateTime.md) |

A date-time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as `2007-12-03T10:15:30+01:00`.

`OffsetDateTime` is an immutable representation of a date-time with an offset. This class stores all date and time fields, to a precision of nanoseconds, as well as the offset from UTC/Greenwich. For example, the value "2nd October 2007 at 13:45:30.123456789 +02:00" can be stored in an `OffsetDateTime`.

`OffsetDateTime`, ZonedDateTime and Instant all store an instant on the time-line to nanosecond precision. `Instant` is the simplest, simply representing the instant. `OffsetDateTime` adds to the instant the offset from UTC/Greenwich, which allows the local date-time to be obtained. `ZonedDateTime` adds full time-zone rules.

It is intended that `ZonedDateTime` or `Instant` is used to model data in simpler applications. This class may be used when modeling date-time concepts in more detail, or when communicating to a database or in a network protocol.

This is a [value-based\<\> class; programmers should treat instances that are](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) [equal](OffsetDateTime.md)) as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. The `equals` method should be used for comparisons.

## Summary

| Public methods ||
|---|---|
| [Temporal](../java.time.temporal/Temporal.md)! | adjustInto Adjusts the specified temporal object to have the same offset, date and time as this object. |
| [ZonedDateTime](ZonedDateTime.md)! | atZoneSameInstant Combines this date-time with a time-zone to create a `ZonedDateTime` ensuring that the result has the same instant. |
| [ZonedDateTime](ZonedDateTime.md)! | atZoneSimilarLocal Combines this date-time with a time-zone to create a `ZonedDateTime` trying to keep the same local date and time. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares this date-time to another date-time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Checks if this date-time is equal to another date-time. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | format Formats this date-time using the specified formatter. |
| --- | --- |
| static [OffsetDateTime](OffsetDateTime.md)! | from Obtains an instance of `OffsetDateTime` from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | get Gets the value of the specified field from this date-time as an `int`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDayOfMonth Gets the day-of-month field. |
| --- | --- |
| [DayOfWeek](DayOfWeek.md)! | getDayOfWeek Gets the day-of-week field, which is an enum `DayOfWeek`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDayOfYear Gets the day-of-year field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHour Gets the hour-of-day field. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getLong Gets the value of the specified field from this date-time as a `long`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMinute Gets the minute-of-hour field. |
| [Month](Month.md)! | getMonth Gets the month-of-year field using the `Month` enum. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMonthValue Gets the month-of-year field from 1 to 12. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNano Gets the nano-of-second field. |
| [ZoneOffset](ZoneOffset.md)! | getOffset Gets the zone offset, such as '+01:00'. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSecond Gets the second-of-minute field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getYear Gets the year field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode A hash code for this date-time. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAfter Checks if the instant of this date-time is after that of the specified date-time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isBefore Checks if the instant of this date-time is before that of the specified date-time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEqual Checks if the instant of this date-time is equal to that of the specified date-time. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSupported Checks if the specified field is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSupported Checks if the specified unit is supported. |
| [OffsetDateTime](OffsetDateTime.md)! | minus Returns a copy of this date-time with the specified amount subtracted. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | minus Returns a copy of this date-time with the specified amount subtracted. |
| [OffsetDateTime](OffsetDateTime.md)! | minusDays Returns a copy of this `OffsetDateTime` with the specified number of days subtracted. |
| [OffsetDateTime](OffsetDateTime.md)! | minusHours Returns a copy of this `OffsetDateTime` with the specified number of hours subtracted. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | minusMinutes Returns a copy of this `OffsetDateTime` with the specified number of minutes subtracted. |
| [OffsetDateTime](OffsetDateTime.md)! | minusMonths Returns a copy of this `OffsetDateTime` with the specified number of months subtracted. |
| [OffsetDateTime](OffsetDateTime.md)! | minusNanos Returns a copy of this `OffsetDateTime` with the specified number of nanoseconds subtracted. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | minusSeconds Returns a copy of this `OffsetDateTime` with the specified number of seconds subtracted. |
| [OffsetDateTime](OffsetDateTime.md)! | minusWeeks Returns a copy of this `OffsetDateTime` with the specified number of weeks subtracted. |
| [OffsetDateTime](OffsetDateTime.md)! | minusYears Returns a copy of this `OffsetDateTime` with the specified number of years subtracted. |
| --- | --- |
| static [OffsetDateTime](OffsetDateTime.md)! | now Obtains the current date-time from the system clock in the default time-zone. |
| static [OffsetDateTime](OffsetDateTime.md)! | now Obtains the current date-time from the specified clock. |
| static [OffsetDateTime](OffsetDateTime.md)! | now Obtains the current date-time from the system clock in the specified time-zone. |
| --- | --- |
| static [OffsetDateTime](OffsetDateTime.md)! | of Obtains an instance of `OffsetDateTime` from a year, month, day, hour, minute, second, nanosecond and offset. |
| static [OffsetDateTime](OffsetDateTime.md)! | of Obtains an instance of `OffsetDateTime` from a date, time and offset. |
| static [OffsetDateTime](OffsetDateTime.md)! | of Obtains an instance of `OffsetDateTime` from a date-time and offset. |
| --- | --- |
| static [OffsetDateTime](OffsetDateTime.md)! | ofInstant Obtains an instance of `OffsetDateTime` from an `Instant` and zone ID. |
| static [OffsetDateTime](OffsetDateTime.md)! | parse Obtains an instance of `OffsetDateTime` from a text string such as `2007-12-03T10:15:30+01:00`. |
| static [OffsetDateTime](OffsetDateTime.md)! | parse Obtains an instance of `OffsetDateTime` from a text string using a specific formatter. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | plus Returns a copy of this date-time with the specified amount added. |
| [OffsetDateTime](OffsetDateTime.md)! | plus Returns a copy of this date-time with the specified amount added. |
| [OffsetDateTime](OffsetDateTime.md)! | plusDays Returns a copy of this OffsetDateTime with the specified number of days added. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | plusHours Returns a copy of this `OffsetDateTime` with the specified number of hours added. |
| [OffsetDateTime](OffsetDateTime.md)! | plusMinutes Returns a copy of this `OffsetDateTime` with the specified number of minutes added. |
| [OffsetDateTime](OffsetDateTime.md)! | plusMonths Returns a copy of this `OffsetDateTime` with the specified number of months added. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | plusNanos Returns a copy of this `OffsetDateTime` with the specified number of nanoseconds added. |
| [OffsetDateTime](OffsetDateTime.md)! | plusSeconds Returns a copy of this `OffsetDateTime` with the specified number of seconds added. |
| [OffsetDateTime](OffsetDateTime.md)! | plusWeeks Returns a copy of this OffsetDateTime with the specified number of weeks added. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | plusYears Returns a copy of this `OffsetDateTime` with the specified number of years added. |
| R | query Queries this date-time using the specified query. |
| [ValueRange](../java.time.temporal/ValueRange.md)! | range Gets the range of valid values for the specified field. |
| --- | --- |
| static [Comparator](../java.util/Comparator.md)\< [OffsetDateTime](OffsetDateTime.md)!\>! | timeLineOrder Gets a comparator that compares two `OffsetDateTime` instances based solely on the instant. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | toEpochSecond Converts this date-time to the number of seconds from the epoch of 1970-01-01T00:00:00Z. |
| [Instant](Instant.md)! | toInstant Converts this date-time to an `Instant`. |
| --- | --- |
| [LocalDate](LocalDate.md)! | toLocalDate Gets the `LocalDate` part of this date-time. |
| [LocalDateTime](LocalDateTime.md)! | toLocalDateTime Gets the `LocalDateTime` part of this date-time. |
| [LocalTime](LocalTime.md)! | toLocalTime Gets the `LocalTime` part of this date-time. |
| --- | --- |
| [OffsetTime](OffsetTime.md)! | toOffsetTime Converts this date-time to an `OffsetTime`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Outputs this date-time as a `String`, such as `2007-12-03T10:15:30+01:00`. |
| [ZonedDateTime](ZonedDateTime.md)! | toZonedDateTime Converts this date-time to a `ZonedDateTime` using the offset as the zone ID. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | truncatedTo Returns a copy of this `OffsetDateTime` with the time truncated. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | until Calculates the amount of time until another date-time in terms of the specified unit. |
| [OffsetDateTime](OffsetDateTime.md)! | with Returns an adjusted copy of this date-time. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | with Returns a copy of this date-time with the specified field set to a new value. |
| [OffsetDateTime](OffsetDateTime.md)! | withDayOfMonth Returns a copy of this `OffsetDateTime` with the day-of-month altered. |
| [OffsetDateTime](OffsetDateTime.md)! | withDayOfYear Returns a copy of this `OffsetDateTime` with the day-of-year altered. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | withHour Returns a copy of this `OffsetDateTime` with the hour-of-day altered. |
| [OffsetDateTime](OffsetDateTime.md)! | withMinute Returns a copy of this `OffsetDateTime` with the minute-of-hour altered. |
| [OffsetDateTime](OffsetDateTime.md)! | withMonth Returns a copy of this `OffsetDateTime` with the month-of-year altered. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | withNano Returns a copy of this `OffsetDateTime` with the nano-of-second altered. |
| [OffsetDateTime](OffsetDateTime.md)! | withOffsetSameInstant Returns a copy of this `OffsetDateTime` with the specified offset ensuring that the result is at the same instant. |
| [OffsetDateTime](OffsetDateTime.md)! | withOffsetSameLocal Returns a copy of this `OffsetDateTime` with the specified offset ensuring that the result has the same local date-time. |
| --- | --- |
| [OffsetDateTime](OffsetDateTime.md)! | withSecond Returns a copy of this `OffsetDateTime` with the second-of-minute altered. |
| [OffsetDateTime](OffsetDateTime.md)! | withYear Returns a copy of this `OffsetDateTime` with the year altered. |

| Properties ||
|---|---|
| static [OffsetDateTime](OffsetDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#MAX:java.time.OffsetDateTime` The maximum supported `OffsetDateTime`, '+999999999-12-31T23:59:59. |
| static [OffsetDateTime](OffsetDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#MIN:java.time.OffsetDateTime` The minimum supported `OffsetDateTime`, '-999999999-01-01T00:00:00+18:00'. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same offset, date and time as this object.

This returns a temporal object of the same observable type as the input with the offset, date and time changed to be the same as this.

The adjustment is equivalent to using with three times, passing ChronoField, ChronoField and ChronoField as the fields.

In most cases, it is clearer to reverse the calling pattern by using with:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisOffsetDateTime.adjustInto(temporal);
    temporal = temporal.with(thisOffsetDateTime);
  
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

### atZoneSameInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atZoneSameInstant(zone: ZoneId!): ZonedDateTime!
```

Combines this date-time with a time-zone to create a `ZonedDateTime` ensuring that the result has the same instant.

This returns a `ZonedDateTime` formed from this date-time and the specified time-zone. This conversion will ignore the visible local date-time and use the underlying instant instead. This avoids any problems with local time-line gaps or overlaps. The result might have different values for fields such as hour, minute an even day.

To attempt to retain the values of the fields, use atZoneSimilarLocal. To use the offset as the zone ID, use toZonedDateTime.

| Parameters ||
|---|---|
| `zone` | [ZoneId](ZoneId.md)!: the time-zone to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime!` | the zoned date-time formed from this date-time, not null |

### atZoneSimilarLocal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atZoneSimilarLocal(zone: ZoneId!): ZonedDateTime!
```

Combines this date-time with a time-zone to create a `ZonedDateTime` trying to keep the same local date and time.

This returns a `ZonedDateTime` formed from this date-time and the specified time-zone. Where possible, the result will have the same local date-time as this object.

Time-zone rules, such as daylight savings, mean that not every time on the local time-line exists. If the local date-time is in a gap or overlap according to the rules then a resolver is used to determine the resultant local time and offset. This method uses ofLocal to retain the offset from this instance if possible.

Finer control over gaps and overlaps is available in two ways. If you simply want to use the later offset at overlaps then call withLaterOffsetAtOverlap immediately after this method.

To create a zoned date-time at the same instant irrespective of the local time-line, use atZoneSameInstant. To use the offset as the zone ID, use toZonedDateTime.

| Parameters ||
|---|---|
| `zone` | [ZoneId](ZoneId.md)!: the time-zone to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime!` | the zoned date-time formed from this date and the earliest valid time for the zone, not null |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: OffsetDateTime!): Int
```

Compares this date-time to another date-time.

The comparison is based on the instant then on the local date-time. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

For example, the following is the comparator order:

1. `2008-12-03T10:30+01:00`
2. `2008-12-03T11:00+01:00`
3. `2008-12-03T12:00+02:00`
4. `2008-12-03T11:30+01:00`
5. `2008-12-03T12:00+01:00`
6. `2008-12-03T12:30+01:00`

Values #2 and #3 represent the same instant on the time-line. When two values represent the same instant, the local date-time is compared to distinguish them. This step is needed to make the ordering consistent with `equals()`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [OffsetDateTime](OffsetDateTime.md)!: the other date-time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, that is the comparison with the `other`'s instant, if they are not equal; and if equal to the `other`'s instant, the comparison of the `other`'s local date-time |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

**See Also**

- isBefore
- isAfter

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this date-time is equal to another date-time.

The comparison is based on the local date-time and the offset. To compare for the same instant on the time-line, use isEqual. Only objects of type `OffsetDateTime` are compared, other types return false.

| Parameters ||
|---|---|
| `obj` | the object to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is equal to the other date-time |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(formatter: DateTimeFormatter!): String!
```

Formats this date-time using the specified formatter.

This date-time will be passed to the formatter to produce a string.

| Parameters ||
|---|---|
| `formatter` | [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the formatted date-time string, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): OffsetDateTime!
```

Obtains an instance of `OffsetDateTime` from a temporal object.

This obtains an offset date-time based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `OffsetDateTime`.

The conversion will first obtain a `ZoneOffset` from the temporal object. It will then try to obtain a `LocalDateTime`, falling back to an `Instant` if necessary. The result will be the combination of `ZoneOffset` with either with `LocalDateTime` or `Instant`. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects.

This method matches the signature of the functional interface TemporalQuery allowing it to be used as a query via method reference, `OffsetDateTime::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the offset date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to an `OffsetDateTime` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this date-time as an `int`.

This queries this date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a ChronoField then the query is implemented here. The isSupported will return valid values based on this date-time, except `NANO_OF_DAY`, `MICRO_OF_DAY`, `EPOCH_DAY`, `PROLEPTIC_MONTH` and `INSTANT_SECONDS` which are too large to fit in an `int` and throw an `UnsupportedTemporalTypeException`. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

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

This method returns the enum DayOfWeek for the day-of-week. This avoids confusion as to what `int` values mean. If you need access to the primitive `int` value then the enum provides the getValue.

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

### getHour

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHour(): Int
```

Gets the hour-of-day field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hour-of-day, from 0 to 23 |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this date-time as a `long`.

This queries this date-time for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a ChronoField then the query is implemented here. The isSupported will return valid values based on this date-time. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

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

### getMinute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinute(): Int
```

Gets the minute-of-hour field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minute-of-hour, from 0 to 59 |

### getMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMonth(): Month!
```

Gets the month-of-year field using the `Month` enum.

This method returns the enum Month for the month. This avoids confusion as to what `int` values mean. If you need access to the primitive `int` value then the enum provides the getValue.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Month!` | the month-of-year, not null |

**See Also**

- getMonthValue

### getMonthValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMonthValue(): Int
```

Gets the month-of-year field from 1 to 12.

This method returns the month as an `int` from 1 to 12. Application code is frequently clearer if the enum Month is used by calling getMonth.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the month-of-year, from 1 to 12 |

**See Also**

- getMonth

### getNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNano(): Int
```

Gets the nano-of-second field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the nano-of-second, from 0 to 999,999,999 |

### getOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOffset(): ZoneOffset!
```

Gets the zone offset, such as '+01:00'.

This is the offset of the local date-time from UTC/Greenwich.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset!` | the zone offset, not null |

### getSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSecond(): Int
```

Gets the second-of-minute field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the second-of-minute, from 0 to 59 |

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

A hash code for this date-time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAfter(other: OffsetDateTime!): Boolean
```

Checks if the instant of this date-time is after that of the specified date-time.

This method differs from the comparison in compareTo and equals in that it only compares the instant of the date-time. This is equivalent to using `dateTime1.toInstant().isAfter(dateTime2.toInstant());`.

| Parameters ||
|---|---|
| `other` | [OffsetDateTime](OffsetDateTime.md)!: the other date-time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is after the instant of the specified date-time |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBefore(other: OffsetDateTime!): Boolean
```

Checks if the instant of this date-time is before that of the specified date-time.

This method differs from the comparison in compareTo in that it only compares the instant of the date-time. This is equivalent to using `dateTime1.toInstant().isBefore(dateTime2.toInstant());`.

| Parameters ||
|---|---|
| `other` | [OffsetDateTime](OffsetDateTime.md)!: the other date-time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is before the instant of the specified date-time |

### isEqual

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEqual(other: OffsetDateTime!): Boolean
```

Checks if the instant of this date-time is equal to that of the specified date-time.

This method differs from the comparison in compareTo and equals in that it only compares the instant of the date-time. This is equivalent to using `dateTime1.toInstant().equals(dateTime2.toInstant());`.

| Parameters ||
|---|---|
| `other` | [OffsetDateTime](OffsetDateTime.md)!: the other date-time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the instant equals the instant of the specified date-time |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this date-time can be queried for the specified field. If false, then calling the range, get and with methods will throw an exception.

If the field is a ChronoField then the query is implemented here. The supported fields are:

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

All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field is supported on this date-time, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this date-time. If false, then calling the plus and minus methods will throw an exception.

If the unit is a ChronoUnit then the query is implemented here. The supported units are:

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

All other `ChronoUnit` instances will return false.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.isSupportedBy(Temporal)` passing `this` as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|---|---|
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the unit can be added/subtracted, false if not |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(amountToSubtract: TemporalAmount!): OffsetDateTime!
```

Returns a copy of this date-time with the specified amount subtracted.

This returns an `OffsetDateTime`, based on this one, with the specified amount subtracted. The amount is typically Period or Duration but may be any other type implementing the TemporalAmount interface.

The calculation is delegated to the amount object by calling subtractFrom. The amount implementation is free to implement the subtraction in any way it wishes, however it typically calls back to minus. Consult the documentation of the amount implementation to determine if it can be successfully subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to subtract, not null |
| `amountToSubtract` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!: the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the subtraction made, not null |

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
): OffsetDateTime!
```

Returns a copy of this date-time with the specified amount subtracted.

This returns an `OffsetDateTime`, based on this one, with the amount in terms of the unit subtracted. If it is not possible to subtract the amount, because the unit is not supported or for some other reason, an exception is thrown.

This method is equivalent to plus with the amount negated. See that method for a full description of how addition, and thus subtraction, works.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to subtract from the result, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit of the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the specified amount subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### minusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusDays(days: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of days subtracted.

This method subtracts the specified amount from the days field decrementing the month and year fields as necessary to ensure the result remains valid. The result is only invalid if the maximum/minimum year is exceeded.

For example, 2009-01-01 minus one day would result in 2008-12-31.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `days` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the days to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the days subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusHours(hours: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of hours subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `hours` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the hours to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the hours subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusMinutes(minutes: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of minutes subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `minutes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the minutes to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the minutes subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusMonths(months: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of months subtracted.

This method subtracts the specified amount from the months field in three steps:

1. Subtract the input months from the month-of-year field
2. Check if the resulting date would be invalid
3. Adjust the day-of-month to the last valid day if necessary

For example, 2007-03-31 minus one month would result in the invalid date 2007-02-31. Instead of returning an invalid result, the last valid day of the month, 2007-02-28, is selected instead.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `months` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the months to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the months subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusNanos(nanos: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of nanoseconds subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the nanos to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the nanoseconds subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusSeconds(seconds: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of seconds subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the seconds to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the seconds subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusWeeks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusWeeks(weeks: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of weeks subtracted.

This method subtracts the specified amount in weeks from the days field decrementing the month and year fields as necessary to ensure the result remains valid. The result is only invalid if the maximum/minimum year is exceeded.

For example, 2009-01-07 minus one week would result in 2008-12-31.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `weeks` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the weeks to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the weeks subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### minusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusYears(years: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of years subtracted.

This method subtracts the specified amount from the years field in three steps:

1. Subtract the input years from the year field
2. Check if the resulting date would be invalid
3. Adjust the day-of-month to the last valid day if necessary

For example, 2008-02-29 (leap year) minus one year would result in the invalid date 2007-02-29 (standard year). Instead of returning an invalid result, the last valid day of the month, 2007-02-28, is selected instead.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `years` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the years to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the years subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(): OffsetDateTime!
```

Obtains the current date-time from the system clock in the default time-zone.

This will query the systemDefaultZone in the default time-zone to obtain the current date-time. The offset will be calculated from the time-zone in the clock.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the current date-time using the system clock, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(clock: Clock!): OffsetDateTime!
```

Obtains the current date-time from the specified clock.

This will query the specified clock to obtain the current date-time. The offset will be calculated from the time-zone in the clock.

Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using Clock.

| Parameters ||
|---|---|
| `clock` | [Clock](Clock.md)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the current date-time, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(zone: ZoneId!): OffsetDateTime!
```

Obtains the current date-time from the system clock in the specified time-zone.

This will query the system to obtain the current date-time. Specifying the time-zone avoids dependence on the default time-zone. The offset will be calculated from the specified time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](ZoneId.md)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the current date-time using the system clock, not null |

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
    offset: ZoneOffset!
): OffsetDateTime!
```

Obtains an instance of `OffsetDateTime` from a year, month, day, hour, minute, second, nanosecond and offset.

This creates an offset date-time with the seven specified fields.

This method exists primarily for writing test cases. Non test-code will typically use other methods to create an offset time. `LocalDateTime` has five additional convenience variants of the equivalent factory method taking fewer arguments. They are not provided here to reduce the footprint of the API.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to represent, from MIN_YEAR to MAX_YEAR |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to represent, from 1 (January) to 12 (December) |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to represent, from 1 to 31 |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to represent, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to represent, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute to represent, from 0 to 59 |
| --- | --- |
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the nano-of-second to represent, from 0 to 999,999,999 |
| `offset` | [ZoneOffset](ZoneOffset.md)!: the zone offset, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the offset date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month-year |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    date: LocalDate!, 
    time: LocalTime!, 
    offset: ZoneOffset!
): OffsetDateTime!
```

Obtains an instance of `OffsetDateTime` from a date, time and offset.

This creates an offset date-time with the specified local date, time and offset.

| Parameters ||
|---|---|
| `date` | [LocalDate](LocalDate.md)!: the local date, not null |
| `time` | [LocalTime](LocalTime.md)!: the local time, not null |
| `offset` | [ZoneOffset](ZoneOffset.md)!: the zone offset, not null |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the offset date-time, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    dateTime: LocalDateTime!, 
    offset: ZoneOffset!
): OffsetDateTime!
```

Obtains an instance of `OffsetDateTime` from a date-time and offset.

This creates an offset date-time with the specified local date-time and offset.

| Parameters ||
|---|---|
| `dateTime` | [LocalDateTime](LocalDateTime.md)!: the local date-time, not null |
| `offset` | [ZoneOffset](ZoneOffset.md)!: the zone offset, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the offset date-time, not null |

### ofInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofInstant(
    instant: Instant!, 
    zone: ZoneId!
): OffsetDateTime!
```

Obtains an instance of `OffsetDateTime` from an `Instant` and zone ID.

This creates an offset date-time with the same instant as that specified. Finding the offset from UTC/Greenwich is simple as there is only one valid offset for each instant.

| Parameters ||
|---|---|
| `instant` | [Instant](Instant.md)!: the instant to create the date-time from, not null |
| `zone` | [ZoneId](ZoneId.md)!: the time-zone, which may be an offset, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the offset date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(text: CharSequence!): OffsetDateTime!
```

Obtains an instance of `OffsetDateTime` from a text string such as `2007-12-03T10:15:30+01:00`.

The string must represent a valid date-time and is parsed using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_OFFSET_DATE_TIME:java.time.format.DateTimeFormatter`.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse such as "2007-12-03T10:15:30+01:00", not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the parsed offset date-time, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(
    text: CharSequence!, 
    formatter: DateTimeFormatter!
): OffsetDateTime!
```

Obtains an instance of `OffsetDateTime` from a text string using a specific formatter.

The text is parsed using the formatter, returning a date-time.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `formatter` | [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | the parsed offset date-time, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(amountToAdd: TemporalAmount!): OffsetDateTime!
```

Returns a copy of this date-time with the specified amount added.

This returns an `OffsetDateTime`, based on this one, with the specified amount added. The amount is typically Period or Duration but may be any other type implementing the TemporalAmount interface.

The calculation is delegated to the amount object by calling addTo. The amount implementation is free to implement the addition in any way it wishes, however it typically calls back to plus. Consult the documentation of the amount implementation to determine if it can be successfully added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to add, not null |
| `amountToAdd` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!: the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the addition made, not null |

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
): OffsetDateTime!
```

Returns a copy of this date-time with the specified amount added.

This returns an `OffsetDateTime`, based on this one, with the amount in terms of the unit added. If it is not possible to add the amount, because the unit is not supported or for some other reason, an exception is thrown.

If the field is a ChronoUnit then the addition is implemented by plus. The offset is not part of the calculation and will be unchanged in the result.

If the field is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.addTo(Temporal, long)` passing `this` as the argument. In this case, the unit determines whether and how to perform the addition.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to add to the result, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit of the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the specified amount added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### plusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusDays(days: Long): OffsetDateTime!
```

Returns a copy of this OffsetDateTime with the specified number of days added.

This method adds the specified amount to the days field incrementing the month and year fields as necessary to ensure the result remains valid. The result is only invalid if the maximum/minimum year is exceeded.

For example, 2008-12-31 plus one day would result in 2009-01-01.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `days` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the days to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the days added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusHours(hours: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of hours added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `hours` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the hours to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the hours added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusMinutes(minutes: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of minutes added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `minutes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the minutes to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the minutes added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusMonths(months: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of months added.

This method adds the specified amount to the months field in three steps:

1. Add the input months to the month-of-year field
2. Check if the resulting date would be invalid
3. Adjust the day-of-month to the last valid day if necessary

For example, 2007-03-31 plus one month would result in the invalid date 2007-04-31. Instead of returning an invalid result, the last valid day of the month, 2007-04-30, is selected instead.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `months` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the months to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the months added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusNanos(nanos: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of nanoseconds added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the nanos to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the nanoseconds added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the unit cannot be added to this type |

### plusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusSeconds(seconds: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of seconds added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the seconds to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the seconds added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusWeeks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusWeeks(weeks: Long): OffsetDateTime!
```

Returns a copy of this OffsetDateTime with the specified number of weeks added.

This method adds the specified amount in weeks to the days field incrementing the month and year fields as necessary to ensure the result remains valid. The result is only invalid if the maximum/minimum year is exceeded.

For example, 2008-12-31 plus one week would result in 2009-01-07.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `weeks` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the weeks to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the weeks added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### plusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusYears(years: Long): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified number of years added.

This method adds the specified amount to the years field in three steps:

1. Add the input years to the year field
2. Check if the resulting date would be invalid
3. Adjust the day-of-month to the last valid day if necessary

For example, 2008-02-29 (leap year) plus one year would result in the invalid date 2009-02-29 (standard year). Instead of returning an invalid result, the last valid day of the month, 2009-02-28, is selected instead.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `years` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the years to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the years added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this date-time using the specified query.

This queries this date-time using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the queryFrom method on the specified query passing `this` as the argument.

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

The range object expresses the minimum and maximum valid values for a field. This date-time is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a ChronoField then the query is implemented here. The isSupported will return appropriate range instances. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

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

### timeLineOrder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun timeLineOrder(): Comparator<OffsetDateTime!>!
```

Gets a comparator that compares two `OffsetDateTime` instances based solely on the instant.

This method differs from the comparison in compareTo in that it only compares the underlying instant.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!>!` | a comparator that compares in time-line order |

**See Also**

- isAfter
- isBefore
- isEqual

### toEpochSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toEpochSecond(): Long
```

Converts this date-time to the number of seconds from the epoch of 1970-01-01T00:00:00Z.

This allows this date-time to be converted to a value of the ChronoField field. This is primarily intended for low-level conversions rather than general application usage.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of seconds from the epoch of 1970-01-01T00:00:00Z |

### toInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toInstant(): Instant!
```

Converts this date-time to an `Instant`.

This returns an `Instant` representing the same point on the time-line as this date-time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant!` | an `Instant` representing the same instant, not null |

### toLocalDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLocalDate(): LocalDate!
```

Gets the `LocalDate` part of this date-time.

This returns a `LocalDate` with the same year, month and day as this date-time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate!` | the date part of this date-time, not null |

### toLocalDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLocalDateTime(): LocalDateTime!
```

Gets the `LocalDateTime` part of this date-time.

This returns a `LocalDateTime` with the same year, month, day and time as this date-time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime!` | the local date-time part of this date-time, not null |

### toLocalTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLocalTime(): LocalTime!
```

Gets the `LocalTime` part of this date-time.

This returns a `LocalTime` with the same hour, minute, second and nanosecond as this date-time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime!` | the time part of this date-time, not null |

### toOffsetTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toOffsetTime(): OffsetTime!
```

Converts this date-time to an `OffsetTime`.

This returns an offset time with the same local time and offset.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetTime!` | an OffsetTime representing the time and offset, not null |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Outputs this date-time as a `String`, such as `2007-12-03T10:15:30+01:00`.

The output will be one of the following formats:

- `uuuu-MM-dd'T'HH:mmXXXXX`
- `uuuu-MM-dd'T'HH:mm:ssXXXXX`
- `uuuu-MM-dd'T'HH:mm:ss.SSSXXXXX`
- `uuuu-MM-dd'T'HH:mm:ss.SSSSSSXXXXX`
- `uuuu-MM-dd'T'HH:mm:ss.SSSSSSSSSXXXXX`

The format used will be the shortest that outputs the full value of the time where the omitted parts are implied to be zero. The output is compatible with ISO 8601 if the seconds in the offset are zero.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this date-time, not null |

### toZonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toZonedDateTime(): ZonedDateTime!
```

Converts this date-time to a `ZonedDateTime` using the offset as the zone ID.

This creates the simplest possible `ZonedDateTime` using the offset as the zone ID.

To control the time-zone used, see atZoneSameInstant and atZoneSimilarLocal.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime!` | a zoned date-time representing the same local date-time and offset, not null |

### truncatedTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun truncatedTo(unit: TemporalUnit!): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the time truncated.

Truncation returns a copy of the original date-time with fields smaller than the specified unit set to zero. For example, truncating with the ChronoUnit unit will set the second-of-minute and nano-of-second field to zero.

The unit must have a [duration](../java.time.temporal/TemporalUnit.md)) that divides into the length of a standard day without remainder. This includes all supplied time units on ChronoUnit and ChronoUnit. Other units throw an exception.

The offset does not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit to truncate to, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the time truncated, not null |

| Exceptions ||
|---|---|
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

This calculates the amount of time between two `OffsetDateTime` objects in terms of a single `TemporalUnit`. The start and end points are `this` and the specified date-time. The result will be negative if the end is before the start. For example, the amount in days between two date-times can be calculated using `startDateTime.until(endDateTime, DAYS)`.

The `Temporal` passed to this method is converted to a `OffsetDateTime` using from. If the offset differs between the two date-times, the specified end date-time is normalized to have the same offset as this date-time.

The calculation returns a whole number, representing the number of complete units between the two date-times. For example, the amount in months between 2012-06-15T00:00Z and 2012-08-14T23:59Z will only be one month as it is one minute short of two months.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use between:

```kotlin
// these two lines are equivalent
    amount = start.until(end, MONTHS);
    amount = MONTHS.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for ChronoUnit. The units `NANOS`, `MICROS`, `MILLIS`, `SECONDS`, `MINUTES`, `HOURS` and `HALF_DAYS`, `DAYS`, `WEEKS`, `MONTHS`, `YEARS`, `DECADES`, `CENTURIES`, `MILLENNIA` and `ERAS` are supported. Other `ChronoUnit` values will throw an exception.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.between(Temporal, Temporal)` passing `this` as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `endExclusive` | [Temporal](../java.time.temporal/Temporal.md)!: the end date, exclusive, which is converted to an `OffsetDateTime`, not null |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit to measure the amount in, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the amount of time between this date-time and the end date-time |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to an `OffsetDateTime` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(adjuster: TemporalAdjuster!): OffsetDateTime!
```

Returns an adjusted copy of this date-time.

This returns an `OffsetDateTime`, based on this one, with the date-time adjusted. The adjustment takes place using the specified adjuster strategy object. Read the documentation of the adjuster to understand what adjustment will be made.

A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in TemporalAdjusters. These include finding the "last day of the month" and "next Wednesday". Key date-time classes also implement the `TemporalAdjuster` interface, such as Month and MonthDay. The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

For example this code returns a date on the last day of July:

```kotlin
import static java.time.Month.*;
   import static java.time.temporal.TemporalAdjusters.*;
 
   result = offsetDateTime.with(JULY).with(lastDayOfMonth());
  
```

The classes LocalDate, LocalTime and ZoneOffset implement `TemporalAdjuster`, thus this method can be used to change the date, time or offset:

```kotlin
result = offsetDateTime.with(date);
   result = offsetDateTime.with(time);
   result = offsetDateTime.with(offset);
  
```

The result of this method is obtained by invoking the adjustInto method on the specified adjuster passing `this` as the argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `adjuster` | [TemporalAdjuster](../java.time.temporal/TemporalAdjuster.md)!: the adjuster to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on `this` with the adjustment made, not null |

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
): OffsetDateTime!
```

Returns a copy of this date-time with the specified field set to a new value.

This returns an `OffsetDateTime`, based on this one, with the value for the specified field changed. This can be used to change any supported field, such as the year, month or day-of-month. If it is not possible to set the value, because the field is not supported or for some other reason, an exception is thrown.

In some cases, changing the specified field can cause the resulting date-time to become invalid, such as changing the month from 31st January to February would make the day-of-month invalid. In cases like this, the field is responsible for resolving the date. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

If the field is a ChronoField then the adjustment is implemented here.

The `INSTANT_SECONDS` field will return a date-time with the specified instant. The offset and nano-of-second are unchanged. If the new instant value is outside the valid range then a `DateTimeException` will be thrown.

The `OFFSET_SECONDS` field will return a date-time with the specified offset. The local date-time is unaltered. If the new offset value is outside the valid range then a `DateTimeException` will be thrown.

The other isSupported will behave as per the matching method on with. In this case, the offset is not part of the calculation and will be unchanged.

All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.adjustInto(Temporal, long)` passing `this` as the argument. In this case, the field determines whether and how to adjust the instant.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value of the field in the result |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on `this` with the specified field set, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |

### withDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withDayOfMonth(dayOfMonth: Int): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the day-of-month altered.

If the resulting `OffsetDateTime` is invalid, an exception is thrown. The time and offset do not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to set in the result, from 1 to 28-31 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the day-of-month value is invalid, or if the day-of-month is invalid for the month-year |

### withDayOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withDayOfYear(dayOfYear: Int): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the day-of-year altered.

The time and offset do not affect the calculation and will be the same in the result. If the resulting `OffsetDateTime` is invalid, an exception is thrown.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-year to set in the result, from 1 to 365-366 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date with the requested day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the day-of-year value is invalid, or if the day-of-year is invalid for the year |

### withHour

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withHour(hour: Int): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the hour-of-day altered.

The date and offset do not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to set in the result, from 0 to 23 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested hour, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the hour value is invalid |

### withMinute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withMinute(minute: Int): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the minute-of-hour altered.

The date and offset do not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to set in the result, from 0 to 59 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested minute, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the minute value is invalid |

### withMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withMonth(month: Int): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the month-of-year altered.

The time and offset do not affect the calculation and will be the same in the result. If the day-of-month is invalid for the year, it will be changed to the last valid day of the month.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to set in the result, from 1 (January) to 12 (December) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested month, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the month-of-year value is invalid |

### withNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withNano(nanoOfSecond: Int): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the nano-of-second altered.

The date and offset do not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the nano-of-second to set in the result, from 0 to 999,999,999 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested nanosecond, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the nano value is invalid |

### withOffsetSameInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withOffsetSameInstant(offset: ZoneOffset!): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified offset ensuring that the result is at the same instant.

This method returns an object with the specified `ZoneOffset` and a `LocalDateTime` adjusted by the difference between the two offsets. This will result in the old and new objects representing the same instant. This is useful for finding the local time in a different offset. For example, if this time represents `2007-12-03T10:30+02:00` and the offset specified is `+03:00`, then this method will return `2007-12-03T11:30+03:00`.

To change the offset without adjusting the local time use withOffsetSameLocal.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `offset` | [ZoneOffset](ZoneOffset.md)!: the zone offset to change to, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### withOffsetSameLocal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withOffsetSameLocal(offset: ZoneOffset!): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the specified offset ensuring that the result has the same local date-time.

This method returns an object with the same `LocalDateTime` and the specified `ZoneOffset`. No calculation is needed or performed. For example, if this time represents `2007-12-03T10:30+02:00` and the offset specified is `+03:00`, then this method will return `2007-12-03T10:30+03:00`.

To take into account the difference between the offsets, and adjust the time fields, use withOffsetSameInstant.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `offset` | [ZoneOffset](ZoneOffset.md)!: the zone offset to change to, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested offset, not null |

### withSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withSecond(second: Int): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the second-of-minute altered.

The date and offset do not affect the calculation and will be the same in the result.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute to set in the result, from 0 to 59 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested second, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the second value is invalid |

### withYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withYear(year: Int): OffsetDateTime!
```

Returns a copy of this `OffsetDateTime` with the year altered.

The time and offset do not affect the calculation and will be the same in the result. If the day-of-month is invalid for the year, it will be changed to the last valid day of the month.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to set in the result, from MIN_YEAR to MAX_YEAR |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#!` | an `OffsetDateTime` based on this date-time with the requested year, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the year value is invalid |

## Properties

### MAX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX: OffsetDateTime!
```

The maximum supported `OffsetDateTime`, '+999999999-12-31T23:59:59.999999999-18:00'. This is the local date-time just before midnight at the end of the maximum date in the minimum offset (larger negative offsets are later on the time-line). This combines `https://developer.android.com/reference/kotlin/java/time/LocalDateTime#MAX:java.time.LocalDateTime` and `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#MIN:java.time.ZoneOffset`. This could be used by an application as a "far future" date-time.

### MIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN: OffsetDateTime!
```

The minimum supported `OffsetDateTime`, '-999999999-01-01T00:00:00+18:00'. This is the local date-time of midnight at the start of the minimum date in the maximum offset (larger offsets are earlier on the time-line). This combines `https://developer.android.com/reference/kotlin/java/time/LocalDateTime#MIN:java.time.LocalDateTime` and `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#MAX:java.time.ZoneOffset`. This could be used by an application as a "far past" date-time.
