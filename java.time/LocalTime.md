Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalTime

```
class LocalTime : Comparable<LocalTime!>, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.LocalTime](LocalTime.md) |

A time without a time-zone in the ISO-8601 calendar system, such as `10:15:30`.

`LocalTime` is an immutable date-time object that represents a time, often viewed as hour-minute-second. Time is represented to nanosecond precision. For example, the value "13:45.30.123456789" can be stored in a `LocalTime`.

This class does not store or represent a date or time-zone. Instead, it is a description of the local time as seen on a wall clock. It cannot represent an instant on the time-line without additional information such as an offset or time-zone.

The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. This API assumes that all calendar systems use the same representation, this class, for time-of-day.

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](LocalTime.md)) as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. The `equals` method should be used for comparisons.

## Summary

| Public methods ||
|---|---|
| [Temporal](../java.time.temporal/Temporal.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#adjustInto(java.time.temporal.Temporal)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!)` Adjusts the specified temporal object to have the same time as this object. |
| [LocalDateTime](LocalDateTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#atDate(java.time.LocalDate)(date: https://developer.android.com/reference/kotlin/java/time/LocalDate!)` Combines this time with a date to create a `LocalDateTime`. |
| [OffsetTime](OffsetTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#atOffset(java.time.ZoneOffset)(offset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset!)` Combines this time with an offset to create an `OffsetTime`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#compareTo(java.time.LocalTime)(other: https://developer.android.com/reference/kotlin/java/time/LocalTime#!)` Compares this time to another time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks if this time is equal to another time. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#format(java.time.format.DateTimeFormatter)(formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Formats this time using the specified formatter. |
| --- | --- |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Obtains an instance of `LocalTime` from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#get(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this time as an `int`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#getHour()()` Gets the hour-of-day field. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this time as a `long`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#getMinute()()` Gets the minute-of-hour field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#getNano()()` Gets the nano-of-second field. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#getSecond()()` Gets the second-of-minute field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#hashCode()()` A hash code for this time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#isAfter(java.time.LocalTime)(other: https://developer.android.com/reference/kotlin/java/time/LocalTime#!)` Checks if this time is after the specified time. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#isBefore(java.time.LocalTime)(other: https://developer.android.com/reference/kotlin/java/time/LocalTime#!)` Checks if this time is before the specified time. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Checks if the specified field is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#isSupported(java.time.temporal.TemporalUnit)(unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Checks if the specified unit is supported. |
| --- | --- |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#minus(java.time.temporal.TemporalAmount)(amountToSubtract: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount!)` Returns a copy of this time with the specified amount subtracted. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this time with the specified amount subtracted. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#minusHours(kotlin.Long)(hoursToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalTime` with the specified number of hours subtracted. |
| --- | --- |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#minusMinutes(kotlin.Long)(minutesToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalTime` with the specified number of minutes subtracted. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#minusNanos(kotlin.Long)(nanosToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalTime` with the specified number of nanoseconds subtracted. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#minusSeconds(kotlin.Long)(secondsToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalTime` with the specified number of seconds subtracted. |
| --- | --- |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#now()()` Obtains the current time from the system clock in the default time-zone. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#now(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock!)` Obtains the current time from the specified clock. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#now(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId!)` Obtains the current time from the system clock in the specified time-zone. |
| --- | --- |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#of(kotlin.Int,%20kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `LocalTime` from an hour and minute. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#of(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `LocalTime` from an hour, minute and second. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#of(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, nanoOfSecond: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `LocalTime` from an hour, minute, second and nanosecond. |
| --- | --- |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#ofInstant(java.time.Instant,%20java.time.ZoneId)(instant: https://developer.android.com/reference/kotlin/java/time/Instant!, zone: https://developer.android.com/reference/kotlin/java/time/ZoneId!)` Obtains an instance of `LocalTime` from an `Instant` and zone ID. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#ofNanoOfDay(kotlin.Long)(nanoOfDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains an instance of `LocalTime` from a nanos-of-day value. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#ofSecondOfDay(kotlin.Long)(secondOfDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains an instance of `LocalTime` from a second-of-day value. |
| --- | --- |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#parse(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Obtains an instance of `LocalTime` from a text string such as `10:15`. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#parse(kotlin.CharSequence,%20java.time.format.DateTimeFormatter)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Obtains an instance of `LocalTime` from a text string using a specific formatter. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#plus(java.time.temporal.TemporalAmount)(amountToAdd: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount!)` Returns a copy of this time with the specified amount added. |
| --- | --- |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this time with the specified amount added. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusHours(kotlin.Long)(hoursToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalTime` with the specified number of hours added. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusMinutes(kotlin.Long)(minutesToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalTime` with the specified number of minutes added. |
| --- | --- |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusNanos(kotlin.Long)(nanosToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalTime` with the specified number of nanoseconds added. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusSeconds(kotlin.Long)(secondstoAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `LocalTime` with the specified number of seconds added. |
| R | `https://developer.android.com/reference/kotlin/java/time/LocalTime#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<R>!)` Queries this time using the specified query. |
| --- | --- |
| [ValueRange](../java.time.temporal/ValueRange.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the range of valid values for the specified field. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#toEpochSecond(java.time.LocalDate,%20java.time.ZoneOffset)(date: https://developer.android.com/reference/kotlin/java/time/LocalDate!, offset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset!)` Converts this `LocalTime` to the number of seconds since the epoch of 1970-01-01T00:00:00Z. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#toNanoOfDay()()` Extracts the time as nanos of day, from `0` to `24 * 60 * 60 * 1,000,000,000 - 1`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#toSecondOfDay()()` Extracts the time as seconds of day, from `0` to `24 * 60 * 60 - 1`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#toString()()` Outputs this time as a `String`, such as `10:15`. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#truncatedTo(java.time.temporal.TemporalUnit)(unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this `LocalTime` with the time truncated. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/LocalTime#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit)(endExclusive: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Calculates the amount of time until another time in terms of the specified unit. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#with(java.time.temporal.TemporalAdjuster)(adjuster: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster!)` Returns an adjusted copy of this time. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#with(java.time.temporal.TemporalField,%20kotlin.Long)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this time with the specified field set to a new value. |
| --- | --- |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#withHour(kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `LocalTime` with the hour-of-day altered. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#withMinute(kotlin.Int)(minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `LocalTime` with the minute-of-hour altered. |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#withNano(kotlin.Int)(nanoOfSecond: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `LocalTime` with the nano-of-second altered. |
| --- | --- |
| [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#withSecond(kotlin.Int)(second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `LocalTime` with the second-of-minute altered. |

| Properties ||
|---|---|
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#MAX:java.time.LocalTime` The maximum supported `LocalTime`, '23:59:59. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#MIDNIGHT:java.time.LocalTime` The time of midnight at the start of the day, '00:00'. |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#MIN:java.time.LocalTime` The minimum supported `LocalTime`, '00:00'. |
| --- | --- |
| static [LocalTime](LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/LocalTime#NOON:java.time.LocalTime` The time of noon in the middle of the day, '12:00'. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same time as this object.

This returns a temporal object of the same observable type as the input with the time changed to be the same as this.

The adjustment is equivalent to using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long)` passing `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` as the field.

In most cases, it is clearer to reverse the calling pattern by using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisLocalTime.adjustInto(temporal);
    temporal = temporal.with(thisLocalTime);
  
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

### atDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atDate(date: LocalDate!): LocalDateTime!
```

Combines this time with a date to create a `LocalDateTime`.

This returns a `LocalDateTime` formed from this time at the specified date. All possible combinations of date and time are valid.

| Parameters ||
|---|---|
| `date` | [LocalDate](LocalDate.md)!: the date to combine with, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime!` | the local date-time formed from this time and the specified date, not null |

### atOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atOffset(offset: ZoneOffset!): OffsetTime!
```

Combines this time with an offset to create an `OffsetTime`.

This returns an `OffsetTime` formed from this time at the specified offset. All possible combinations of time and offset are valid.

| Parameters ||
|---|---|
| `offset` | [ZoneOffset](ZoneOffset.md)!: the offset to combine with, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetTime!` | the offset time formed from this time and the specified offset, not null |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: LocalTime!): Int
```

Compares this time to another time.

The comparison is based on the time-line position of the local times within a day. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [LocalTime](LocalTime.md)!: the other time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, that is less than zero if this is before `other`, zero if they are equal, or greater than zero if this is after `other` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/LocalTime#isBefore(java.time.LocalTime)`
- `https://developer.android.com/reference/kotlin/java/time/LocalTime#isAfter(java.time.LocalTime)`

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this time is equal to another time.

The comparison is based on the time-line position of the time within a day.

Only objects of type `LocalTime` are compared, other types return false. To compare the date of two `TemporalAccessor` instances, use `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` as a comparator.

| Parameters ||
|---|---|
| `obj` | the object to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is equal to the other time |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(formatter: DateTimeFormatter!): String!
```

Formats this time using the specified formatter.

This time will be passed to the formatter to produce a string.

| Parameters ||
|---|---|
| `formatter` | [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the formatted time string, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): LocalTime!
```

Obtains an instance of `LocalTime` from a temporal object.

This obtains a local time based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `LocalTime`.

The conversion uses the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#localTime()` query, which relies on extracting the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` field.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery` allowing it to be used as a query via method reference, `LocalTime::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the local time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to a `LocalTime` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this time as an `int`.

This queries this time for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/LocalTime#isSupported(java.time.temporal.TemporalField)` will return valid values based on this time, except `NANO_OF_DAY` and `MICRO_OF_DAY` which are too large to fit in an `int` and throw an `UnsupportedTemporalTypeException`. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

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

Gets the value of the specified field from this time as a `long`.

This queries this time for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/LocalTime#isSupported(java.time.temporal.TemporalField)` will return valid values based on this time. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

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

### getNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNano(): Int
```

Gets the nano-of-second field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the nano-of-second, from 0 to 999,999,999 |

### getSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSecond(): Int
```

Gets the second-of-minute field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the second-of-minute, from 0 to 59 |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

A hash code for this time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAfter(other: LocalTime!): Boolean
```

Checks if this time is after the specified time.

The comparison is based on the time-line position of the time within a day.

| Parameters ||
|---|---|
| `other` | [LocalTime](LocalTime.md)!: the other time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is after the specified time |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `other` is null |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBefore(other: LocalTime!): Boolean
```

Checks if this time is before the specified time.

The comparison is based on the time-line position of the time within a day.

| Parameters ||
|---|---|
| `other` | [LocalTime](LocalTime.md)!: the other time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this point is before the specified time |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `other` is null |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this time can be queried for the specified field. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/LocalTime#range(java.time.temporal.TemporalField)`, `https://developer.android.com/reference/kotlin/java/time/LocalTime#get(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/LocalTime#with(java.time.temporal.TemporalField,%20kotlin.Long)` methods will throw an exception.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The supported fields are:

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

All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field is supported on this time, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this time. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/LocalTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` and `https://developer.android.com/reference/kotlin/java/time/LocalTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)` methods will throw an exception.

If the unit is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` then the query is implemented here. The supported units are:

- `NANOS`
- `MICROS`
- `MILLIS`
- `SECONDS`
- `MINUTES`
- `HOURS`
- `HALF_DAYS`

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
fun minus(amountToSubtract: TemporalAmount!): LocalTime!
```

Returns a copy of this time with the specified amount subtracted.

This returns a `LocalTime`, based on this one, with the specified amount subtracted. The amount is typically `https://developer.android.com/reference/kotlin/java/time/Duration` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount` interface.

The calculation is delegated to the amount object by calling `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#subtractFrom(java.time.temporal.Temporal)`. The amount implementation is free to implement the subtraction in any way it wishes, however it typically calls back to `https://developer.android.com/reference/kotlin/java/time/LocalTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)`. Consult the documentation of the amount implementation to determine if it can be successfully subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to subtract, not null |
| `amountToSubtract` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!: the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the subtraction made, not null |

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
): LocalTime!
```

Returns a copy of this time with the specified amount subtracted.

This returns a `LocalTime`, based on this one, with the amount in terms of the unit subtracted. If it is not possible to subtract the amount, because the unit is not supported or for some other reason, an exception is thrown.

This method is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` with the amount negated. See that method for a full description of how addition, and thus subtraction, works.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to subtract from the result, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit of the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the specified amount subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### minusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusHours(hoursToSubtract: Long): LocalTime!
```

Returns a copy of this `LocalTime` with the specified number of hours subtracted.

This subtracts the specified number of hours from this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `hoursToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the hours to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the hours subtracted, not null |

### minusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusMinutes(minutesToSubtract: Long): LocalTime!
```

Returns a copy of this `LocalTime` with the specified number of minutes subtracted.

This subtracts the specified number of minutes from this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `minutesToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the minutes to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the minutes subtracted, not null |

### minusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusNanos(nanosToSubtract: Long): LocalTime!
```

Returns a copy of this `LocalTime` with the specified number of nanoseconds subtracted.

This subtracts the specified number of nanoseconds from this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `nanosToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the nanos to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the nanoseconds subtracted, not null |

### minusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusSeconds(secondsToSubtract: Long): LocalTime!
```

Returns a copy of this `LocalTime` with the specified number of seconds subtracted.

This subtracts the specified number of seconds from this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `secondsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the seconds to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the seconds subtracted, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(): LocalTime!
```

Obtains the current time from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#systemDefaultZone()` in the default time-zone to obtain the current time.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the current time using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(clock: Clock!): LocalTime!
```

Obtains the current time from the specified clock.

This will query the specified clock to obtain the current time. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock`.

| Parameters ||
|---|---|
| `clock` | [Clock](Clock.md)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the current time, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(zone: ZoneId!): LocalTime!
```

Obtains the current time from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#system(java.time.ZoneId)` to obtain the current time. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](ZoneId.md)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the current time using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    hour: Int, 
    minute: Int
): LocalTime!
```

Obtains an instance of `LocalTime` from an hour and minute.

This returns a `LocalTime` with the specified hour and minute. The second and nanosecond fields will be set to zero.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to represent, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to represent, from 0 to 59 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the local time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    hour: Int, 
    minute: Int, 
    second: Int
): LocalTime!
```

Obtains an instance of `LocalTime` from an hour, minute and second.

This returns a `LocalTime` with the specified hour, minute and second. The nanosecond field will be set to zero.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to represent, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to represent, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute to represent, from 0 to 59 |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the local time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    hour: Int, 
    minute: Int, 
    second: Int, 
    nanoOfSecond: Int
): LocalTime!
```

Obtains an instance of `LocalTime` from an hour, minute, second and nanosecond.

This returns a `LocalTime` with the specified hour, minute, second and nanosecond.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to represent, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to represent, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute to represent, from 0 to 59 |
| --- | --- |
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the nano-of-second to represent, from 0 to 999,999,999 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the local time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range |

### ofInstant

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofInstant(
    instant: Instant!, 
    zone: ZoneId!
): LocalTime!
```

Obtains an instance of `LocalTime` from an `Instant` and zone ID.

This creates a local time based on the specified instant. First, the offset from UTC/Greenwich is obtained using the zone ID and instant, which is simple as there is only one valid offset for each instant. Then, the instant and offset are used to calculate the local time.

| Parameters ||
|---|---|
| `instant` | [Instant](Instant.md)!: the instant to create the time from, not null |
| `zone` | [ZoneId](ZoneId.md)!: the time-zone, which may be an offset, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the local time, not null |

### ofNanoOfDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofNanoOfDay(nanoOfDay: Long): LocalTime!
```

Obtains an instance of `LocalTime` from a nanos-of-day value.

This returns a `LocalTime` with the specified nanosecond-of-day.

| Parameters ||
|---|---|
| `nanoOfDay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the nano of day, from `0` to `24 * 60 * 60 * 1,000,000,000 - 1` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the local time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the nanos of day value is invalid |

### ofSecondOfDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofSecondOfDay(secondOfDay: Long): LocalTime!
```

Obtains an instance of `LocalTime` from a second-of-day value.

This returns a `LocalTime` with the specified second-of-day. The nanosecond field will be set to zero.

| Parameters ||
|---|---|
| `secondOfDay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the second-of-day, from `0` to `24 * 60 * 60 - 1` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the local time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the second-of-day value is invalid |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(text: CharSequence!): LocalTime!
```

Obtains an instance of `LocalTime` from a text string such as `10:15`.

The string must represent a valid time and is parsed using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_LOCAL_TIME:java.time.format.DateTimeFormatter`.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse such as "10:15:30", not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the parsed local time, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(
    text: CharSequence!, 
    formatter: DateTimeFormatter!
): LocalTime!
```

Obtains an instance of `LocalTime` from a text string using a specific formatter.

The text is parsed using the formatter, returning a time.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `formatter` | [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | the parsed local time, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(amountToAdd: TemporalAmount!): LocalTime!
```

Returns a copy of this time with the specified amount added.

This returns a `LocalTime`, based on this one, with the specified amount added. The amount is typically `https://developer.android.com/reference/kotlin/java/time/Duration` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount` interface.

The calculation is delegated to the amount object by calling `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#addTo(java.time.temporal.Temporal)`. The amount implementation is free to implement the addition in any way it wishes, however it typically calls back to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)`. Consult the documentation of the amount implementation to determine if it can be successfully added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to add, not null |
| `amountToAdd` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!: the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the addition made, not null |

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
): LocalTime!
```

Returns a copy of this time with the specified amount added.

This returns a `LocalTime`, based on this one, with the amount in terms of the unit added. If it is not possible to add the amount, because the unit is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` then the addition is implemented here. The supported fields behave as follows:

- `NANOS` - Returns a `LocalTime` with the specified number of nanoseconds added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusNanos(kotlin.Long)`.
- `MICROS` - Returns a `LocalTime` with the specified number of microseconds added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusNanos(kotlin.Long)` with the amount multiplied by 1,000.
- `MILLIS` - Returns a `LocalTime` with the specified number of milliseconds added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusNanos(kotlin.Long)` with the amount multiplied by 1,000,000.
- `SECONDS` - Returns a `LocalTime` with the specified number of seconds added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusSeconds(kotlin.Long)`.
- `MINUTES` - Returns a `LocalTime` with the specified number of minutes added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusMinutes(kotlin.Long)`.
- `HOURS` - Returns a `LocalTime` with the specified number of hours added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusHours(kotlin.Long)`.
- `HALF_DAYS` - Returns a `LocalTime` with the specified number of half-days added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#plusHours(kotlin.Long)` with the amount multiplied by 12.

All other `ChronoUnit` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.addTo(Temporal, long)` passing `this` as the argument. In this case, the unit determines whether and how to perform the addition.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to add to the result, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit of the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the specified amount added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### plusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusHours(hoursToAdd: Long): LocalTime!
```

Returns a copy of this `LocalTime` with the specified number of hours added.

This adds the specified number of hours to this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `hoursToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the hours to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the hours added, not null |

### plusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusMinutes(minutesToAdd: Long): LocalTime!
```

Returns a copy of this `LocalTime` with the specified number of minutes added.

This adds the specified number of minutes to this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `minutesToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the minutes to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the minutes added, not null |

### plusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusNanos(nanosToAdd: Long): LocalTime!
```

Returns a copy of this `LocalTime` with the specified number of nanoseconds added.

This adds the specified number of nanoseconds to this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `nanosToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the nanos to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the nanoseconds added, not null |

### plusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusSeconds(secondstoAdd: Long): LocalTime!
```

Returns a copy of this `LocalTime` with the specified number of seconds added.

This adds the specified number of seconds to this time, returning a new time. The calculation wraps around midnight.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `secondstoAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the seconds to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the seconds added, not null |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this time using the specified query.

This queries this time using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

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

The range object expresses the minimum and maximum valid values for a field. This time is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/LocalTime#isSupported(java.time.temporal.TemporalField)` will return appropriate range instances. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

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

### toEpochSecond

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toEpochSecond(
    date: LocalDate!, 
    offset: ZoneOffset!
): Long
```

Converts this `LocalTime` to the number of seconds since the epoch of 1970-01-01T00:00:00Z.

This combines this local time with the specified date and offset to calculate the epoch-second value, which is the number of elapsed seconds from 1970-01-01T00:00:00Z. Instants on the time-line after the epoch are positive, earlier are negative.

| Parameters ||
|---|---|
| `date` | [LocalDate](LocalDate.md)!: the local date, not null |
| `offset` | [ZoneOffset](ZoneOffset.md)!: the zone offset, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of seconds since the epoch of 1970-01-01T00:00:00Z, may be negative |

### toNanoOfDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toNanoOfDay(): Long
```

Extracts the time as nanos of day, from `0` to `24 * 60 * 60 * 1,000,000,000 - 1`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the nano of day equivalent to this time |

### toSecondOfDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toSecondOfDay(): Int
```

Extracts the time as seconds of day, from `0` to `24 * 60 * 60 - 1`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the second-of-day equivalent to this time |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Outputs this time as a `String`, such as `10:15`.

The output will be one of the following ISO-8601 formats:

- `HH:mm`
- `HH:mm:ss`
- `HH:mm:ss.SSS`
- `HH:mm:ss.SSSSSS`
- `HH:mm:ss.SSSSSSSSS`

The format used will be the shortest that outputs the full value of the time where the omitted parts are implied to be zero.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this time, not null |

### truncatedTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun truncatedTo(unit: TemporalUnit!): LocalTime!
```

Returns a copy of this `LocalTime` with the time truncated.

Truncation returns a copy of the original time with fields smaller than the specified unit set to zero. For example, truncating with the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` unit will set the second-of-minute and nano-of-second field to zero.

The unit must have a [duration](../java.time.temporal/TemporalUnit.md)) that divides into the length of a standard day without remainder. This includes all supplied time units on `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit`. Other units throw an exception.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit to truncate to, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the time truncated, not null |

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

Calculates the amount of time until another time in terms of the specified unit.

This calculates the amount of time between two `LocalTime` objects in terms of a single `TemporalUnit`. The start and end points are `this` and the specified time. The result will be negative if the end is before the start. The `Temporal` passed to this method is converted to a `LocalTime` using `https://developer.android.com/reference/kotlin/java/time/LocalTime#from(java.time.temporal.TemporalAccessor)`. For example, the amount in hours between two times can be calculated using `startTime.until(endTime, HOURS)`.

The calculation returns a whole number, representing the number of complete units between the two times. For example, the amount in hours between 11:30 and 13:29 will only be one hour as it is one minute short of two hours.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)`:

```kotlin
// these two lines are equivalent
    amount = start.until(end, MINUTES);
    amount = MINUTES.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit`. The units `NANOS`, `MICROS`, `MILLIS`, `SECONDS`, `MINUTES`, `HOURS` and `HALF_DAYS` are supported. Other `ChronoUnit` values will throw an exception.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.between(Temporal, Temporal)` passing `this` as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `endExclusive` | [Temporal](../java.time.temporal/Temporal.md)!: the end time, exclusive, which is converted to a `LocalTime`, not null |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit to measure the amount in, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the amount of time between this time and the end time |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to a `LocalTime` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(adjuster: TemporalAdjuster!): LocalTime!
```

Returns an adjusted copy of this time.

This returns a `LocalTime`, based on this one, with the time adjusted. The adjustment takes place using the specified adjuster strategy object. Read the documentation of the adjuster to understand what adjustment will be made.

A simple adjuster might simply set the one of the fields, such as the hour field. A more complex adjuster might set the time to the last hour of the day.

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster#adjustInto(java.time.temporal.Temporal)` method on the specified adjuster passing `this` as the argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `adjuster` | [TemporalAdjuster](../java.time.temporal/TemporalAdjuster.md)!: the adjuster to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on `this` with the adjustment made, not null |

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
): LocalTime!
```

Returns a copy of this time with the specified field set to a new value.

This returns a `LocalTime`, based on this one, with the value for the specified field changed. This can be used to change any supported field, such as the hour, minute or second. If it is not possible to set the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the adjustment is implemented here. The supported fields behave as follows:

- `NANO_OF_SECOND` - Returns a `LocalTime` with the specified nano-of-second. The hour, minute and second will be unchanged.
- `NANO_OF_DAY` - Returns a `LocalTime` with the specified nano-of-day. This completely replaces the time and is equivalent to `https://developer.android.com/reference/kotlin/java/time/LocalTime#ofNanoOfDay(kotlin.Long)`.
- `MICRO_OF_SECOND` - Returns a `LocalTime` with the nano-of-second replaced by the specified micro-of-second multiplied by 1,000. The hour, minute and second will be unchanged.
- `MICRO_OF_DAY` - Returns a `LocalTime` with the specified micro-of-day. This completely replaces the time and is equivalent to using `https://developer.android.com/reference/kotlin/java/time/LocalTime#ofNanoOfDay(kotlin.Long)` with the micro-of-day multiplied by 1,000.
- `MILLI_OF_SECOND` - Returns a `LocalTime` with the nano-of-second replaced by the specified milli-of-second multiplied by 1,000,000. The hour, minute and second will be unchanged.
- `MILLI_OF_DAY` - Returns a `LocalTime` with the specified milli-of-day. This completely replaces the time and is equivalent to using `https://developer.android.com/reference/kotlin/java/time/LocalTime#ofNanoOfDay(kotlin.Long)` with the milli-of-day multiplied by 1,000,000.
- `SECOND_OF_MINUTE` - Returns a `LocalTime` with the specified second-of-minute. The hour, minute and nano-of-second will be unchanged.
- `SECOND_OF_DAY` - Returns a `LocalTime` with the specified second-of-day. The nano-of-second will be unchanged.
- `MINUTE_OF_HOUR` - Returns a `LocalTime` with the specified minute-of-hour. The hour, second-of-minute and nano-of-second will be unchanged.
- `MINUTE_OF_DAY` - Returns a `LocalTime` with the specified minute-of-day. The second-of-minute and nano-of-second will be unchanged.
- `HOUR_OF_AMPM` - Returns a `LocalTime` with the specified hour-of-am-pm. The AM/PM, minute-of-hour, second-of-minute and nano-of-second will be unchanged.
- `CLOCK_HOUR_OF_AMPM` - Returns a `LocalTime` with the specified clock-hour-of-am-pm. The AM/PM, minute-of-hour, second-of-minute and nano-of-second will be unchanged.
- `HOUR_OF_DAY` - Returns a `LocalTime` with the specified hour-of-day. The minute-of-hour, second-of-minute and nano-of-second will be unchanged.
- `CLOCK_HOUR_OF_DAY` - Returns a `LocalTime` with the specified clock-hour-of-day. The minute-of-hour, second-of-minute and nano-of-second will be unchanged.
- `AMPM_OF_DAY` - Returns a `LocalTime` with the specified AM/PM. The hour-of-am-pm, minute-of-hour, second-of-minute and nano-of-second will be unchanged.

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
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on `this` with the specified field set, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |

### withHour

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withHour(hour: Int): LocalTime!
```

Returns a copy of this `LocalTime` with the hour-of-day altered.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day to set in the result, from 0 to 23 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the requested hour, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the hour value is invalid |

### withMinute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withMinute(minute: Int): LocalTime!
```

Returns a copy of this `LocalTime` with the minute-of-hour altered.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour to set in the result, from 0 to 59 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the requested minute, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the minute value is invalid |

### withNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withNano(nanoOfSecond: Int): LocalTime!
```

Returns a copy of this `LocalTime` with the nano-of-second altered.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the nano-of-second to set in the result, from 0 to 999,999,999 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the requested nanosecond, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the nanos value is invalid |

### withSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withSecond(second: Int): LocalTime!
```

Returns a copy of this `LocalTime` with the second-of-minute altered.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute to set in the result, from 0 to 59 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime#!` | a `LocalTime` based on this time with the requested second, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the second value is invalid |

## Properties

### MAX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX: LocalTime!
```

The maximum supported `LocalTime`, '23:59:59.999999999'. This is the time just before midnight at the end of the day.

### MIDNIGHT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIDNIGHT: LocalTime!
```

The time of midnight at the start of the day, '00:00'.

### MIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN: LocalTime!
```

The minimum supported `LocalTime`, '00:00'. This is the time of midnight at the start of the day.

### NOON

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOON: LocalTime!
```

The time of noon in the middle of the day, '12:00'.
