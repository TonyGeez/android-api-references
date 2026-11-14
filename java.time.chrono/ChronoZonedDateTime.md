Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChronoZonedDateTime

```
interface ChronoZonedDateTime<D : ChronoLocalDate!> : Comparable<ChronoZonedDateTime<*>!>, Temporal
```

| [java.time.chrono.ChronoZonedDateTime](ChronoZonedDateTime.md) |

| Known Direct Subclasses [ZonedDateTime](../java.time/ZonedDateTime.md) |---|---| | [ZonedDateTime](../java.time/ZonedDateTime.md) | A date-time with a time-zone in the ISO-8601 calendar system, such as `2007-12-03T10:15:30+01:00 Europe/Paris`. | |
| --- | --- | --- | --- | --- | --- | --- |

A date-time with a time-zone in an arbitrary chronology, intended for advanced globalization use cases.

**Most applications should declare method signatures, fields and variables as `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#`, not this interface.**

A `ChronoZonedDateTime` is the abstract representation of an offset date-time where the `Chronology chronology`, or calendar system, is pluggable. The date-time is defined in terms of fields expressed by `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#`, where most common implementations are defined in `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#`. The chronology defines how the calendar system operates and the meaning of the standard fields.

## When to use this interface

The design of the API encourages the use of `ZonedDateTime` rather than this interface, even in the case where the application needs to deal with multiple calendar systems. The rationale for this is explored in detail in `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate`.

Ensure that the discussion in `ChronoLocalDate` has been read and understood before using this interface.

## Summary

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#compareTo(java.time.chrono.ChronoZonedDateTime)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<*>!)` Compares this date-time to another date-time, including the chronology. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#format(java.time.format.DateTimeFormatter)(formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#!)` Formats this date-time using the specified formatter. |
| open static [ChronoZonedDateTime](ChronoZonedDateTime.md)\<\*\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains an instance of `ChronoZonedDateTime` from a temporal object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#get(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Gets the value of the specified field as an `int`. |
| open [Chronology](Chronology.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#getChronology()()` Gets the chronology of this date-time. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Gets the value of the specified field as a `long`. |
| --- | --- |
| abstract [ZoneOffset](../java.time/ZoneOffset.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#getOffset()()` Gets the zone offset, such as '+01:00'. |
| abstract [ZoneId](../java.time/ZoneId.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#getZone()()` Gets the zone ID, such as 'Europe/Paris'. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#isAfter(java.time.chrono.ChronoZonedDateTime)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<*>!)` Checks if the instant of this date-time is after that of the specified date-time. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#isBefore(java.time.chrono.ChronoZonedDateTime)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<*>!)` Checks if the instant of this date-time is before that of the specified date-time. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#isEqual(java.time.chrono.ChronoZonedDateTime)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<*>!)` Checks if the instant of this date-time is equal to that of the specified date-time. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Checks if the specified field is supported. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#isSupported(java.time.temporal.TemporalUnit)(unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#!)` Checks if the specified unit is supported. |
| open [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#minus(java.time.temporal.TemporalAmount)(amount: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#!)` Returns an object of the same type as this object with an amount subtracted. |
| open [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#!)` Returns an object of the same type as this object with the specified period subtracted. |
| --- | --- |
| open [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#plus(java.time.temporal.TemporalAmount)(amount: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#!)` Returns an object of the same type as this object with an amount added. |
| abstract [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#!)` Returns an object of the same type as this object with the specified period added. |
| open R | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#<R>!)` Queries this date-time using the specified query. |
| --- | --- |
| open [ValueRange](../java.time.temporal/ValueRange.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Gets the range of valid values for the specified field. |
| open static [Comparator](../java.util/Comparator.md)\< [ChronoZonedDateTime](ChronoZonedDateTime.md)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#timeLineOrder()()` Gets a comparator that compares `ChronoZonedDateTime` in time-line order ignoring the chronology. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#toEpochSecond()()` Converts this date-time to the number of seconds from the epoch of 1970-01-01T00:00:00Z. |
| --- | --- |
| open [Instant](../java.time/Instant.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#toInstant()()` Converts this date-time to an `Instant`. |
| open D | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#toLocalDate()()` Gets the local date part of this date-time. |
| abstract [ChronoLocalDateTime](ChronoLocalDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#toLocalDateTime()()` Gets the local date-time part of this date-time. |
| --- | --- |
| open [LocalTime](../java.time/LocalTime.md)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#toLocalTime()()` Gets the local time part of this date-time. |
| open [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#with(java.time.temporal.TemporalAdjuster)(adjuster: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster.html#!)` Returns an adjusted object of the same type as this object with the adjustment made. |
| abstract [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#with(java.time.temporal.TemporalField,%20kotlin.Long)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns an object of the same type as this object with the specified field altered. |
| --- | --- |
| abstract [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#withEarlierOffsetAtOverlap()()` Returns a copy of this date-time changing the zone offset to the earlier of the two valid offsets at a local time-line overlap. |
| abstract [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#withLaterOffsetAtOverlap()()` Returns a copy of this date-time changing the zone offset to the later of the two valid offsets at a local time-line overlap. |
| abstract [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#withZoneSameInstant(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Returns a copy of this date-time with a different time-zone, retaining the instant. |
| --- | --- |
| abstract [ChronoZonedDateTime](ChronoZonedDateTime.md)\<D\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#withZoneSameLocal(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Returns a copy of this date-time with a different time-zone, retaining the local date-time if possible. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#get(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Gets the value of the specified field as an `int`. This queries the date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Gets the value of the specified field as a `long`. This queries the date-time for the value of the specified field. The returned value may be outside the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Checks if the specified field is supported. This checks if the date-time can be queried for the specified field. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#range(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#get(java.time.temporal.TemporalField)` methods will throw an exception. <br /> | | `R` | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#<R>!)` Queries this date-time. This queries this date-time using the specified query strategy object. Queries are a key tool for extracting information from date-times. They exists to externalize the process of querying, permitting different approaches, as per the strategy design pattern. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday. The most common query implementations are method references, such as `LocalDate::from` and `ZoneId::from`. Additional implementations are provided as static methods on `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#`. <br /> | | `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#!` | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Gets the range of valid values for the specified field. All fields can be expressed as a `long` integer. This method returns an object that describes the valid range for that value. The value of this temporal object is used to enhance the accuracy of the returned range. If the date-time cannot return the range, because the field is unsupported or for some other reason, an exception will be thrown. Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit)(endExclusive: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#!)` Calculates the amount of time until another temporal in terms of the specified unit. This calculates the amount of time between two temporal objects in terms of a single `TemporalUnit`. The start and end points are `this` and the specified temporal. The end point is converted to be of the same type as the start point if different. The result will be negative if the end is before the start. For example, the amount in hours between two temporal objects can be calculated using `startTime.until(endTime, HOURS)`. The calculation returns a whole number, representing the number of complete units between the two temporals. For example, the amount in hours between the times 11:30 and 13:29 will only be one hour as it is one minute short of two hours. There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)`: ```kotlin // these two lines are equivalent temporal = start.until(end, unit); temporal = unit.between(start, end); ``` The choice should be made based on which makes the code more readable. For example, this method allows the number of days between two dates to be calculated: ```kotlin long daysBetween = start.until(end, DAYS); // or alternatively long daysBetween = DAYS.between(start, end); ``` <br /> | ||

## Public methods

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: ChronoZonedDateTime<*>!): Int
```

Compares this date-time to another date-time, including the chronology.

The comparison is based first on the instant, then on the local date-time, then on the zone ID, then on the chronology. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

If all the date-time objects being compared are in the same chronology, then the additional chronology stage is not required.

This default implementation performs the comparison defined above.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [ChronoZonedDateTime](ChronoZonedDateTime.md)\<\*\>!: the other date-time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, negative if less, positive if greater |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(formatter: DateTimeFormatter!): String!
```

Formats this date-time using the specified formatter.

This date-time will be passed to the formatter to produce a string.

The default implementation must behave as follows:

```kotlin
return formatter.format(this);
  
```

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
open static fun from(temporal: TemporalAccessor!): ChronoZonedDateTime<*>!
```

Obtains an instance of `ChronoZonedDateTime` from a temporal object.

This creates a zoned date-time based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoZonedDateTime`.

The conversion extracts and combines the chronology, date, time and zone from the temporal object. The behavior is equivalent to using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#zonedDateTime(java.time.temporal.TemporalAccessor)` with the extracted chronology. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `ChronoZonedDateTime::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<*>!` | the date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to a `ChronoZonedDateTime` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#zonedDateTime(java.time.temporal.TemporalAccessor)`

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(field: TemporalField!): Int
```

Gets the value of the specified field as an `int`.

This queries the date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the field, within the valid range of values |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an `int` |
| --- | --- |

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChronology(): Chronology!
```

Gets the chronology of this date-time.

The `Chronology` represents the calendar system in use. The era and other fields in `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` are defined by the chronology.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology!` | the chronology, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field as a `long`.

This queries the date-time for the value of the specified field. The returned value may be outside the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown.

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

### getOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getOffset(): ZoneOffset!
```

Gets the zone offset, such as '+01:00'.

This is the offset of the local date-time from UTC/Greenwich.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!` | the zone offset, not null |

### getZone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getZone(): ZoneId!
```

Gets the zone ID, such as 'Europe/Paris'.

This returns the stored time-zone id used to determine the time-zone rules.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!` | the zone ID, not null |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAfter(other: ChronoZonedDateTime<*>!): Boolean
```

Checks if the instant of this date-time is after that of the specified date-time.

This method differs from the comparison in `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#compareTo(java.time.chrono.ChronoZonedDateTime)` in that it only compares the instant of the date-time. This is equivalent to using `dateTime1.toInstant().isAfter(dateTime2.toInstant());`.

This default implementation performs the comparison based on the epoch-second and nano-of-second.

| Parameters ||
|---|---|
| `other` | [ChronoZonedDateTime](ChronoZonedDateTime.md)\<\*\>!: the other date-time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is after the specified date-time |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isBefore(other: ChronoZonedDateTime<*>!): Boolean
```

Checks if the instant of this date-time is before that of the specified date-time.

This method differs from the comparison in `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#compareTo(java.time.chrono.ChronoZonedDateTime)` in that it only compares the instant of the date-time. This is equivalent to using `dateTime1.toInstant().isBefore(dateTime2.toInstant());`.

This default implementation performs the comparison based on the epoch-second and nano-of-second.

| Parameters ||
|---|---|
| `other` | [ChronoZonedDateTime](ChronoZonedDateTime.md)\<\*\>!: the other date-time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this point is before the specified date-time |

### isEqual

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEqual(other: ChronoZonedDateTime<*>!): Boolean
```

Checks if the instant of this date-time is equal to that of the specified date-time.

This method differs from the comparison in `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#compareTo(java.time.chrono.ChronoZonedDateTime)` and `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#` in that it only compares the instant of the date-time. This is equivalent to using `dateTime1.toInstant().equals(dateTime2.toInstant());`.

This default implementation performs the comparison based on the epoch-second and nano-of-second.

| Parameters ||
|---|---|
| `other` | [ChronoZonedDateTime](ChronoZonedDateTime.md)\<\*\>!: the other date-time to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the instant equals the instant of the specified date-time |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if the specified field can be queried on this date-time. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#range(java.time.temporal.TemporalField)`, `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#get(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#with(java.time.temporal.TemporalField,%20kotlin.Long)` methods will throw an exception.

The set of supported fields is defined by the chronology and normally includes all `ChronoField` fields.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field can be queried, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to or subtracted from this date-time. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` and `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)` methods will throw an exception.

The set of supported units is defined by the chronology and normally includes all `ChronoUnit` units except `FOREVER`.

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
open fun minus(amount: TemporalAmount!): ChronoZonedDateTime<D>!
```

Returns an object of the same type as this object with an amount subtracted.

This adjusts this temporal, subtracting according to the rules of the specified amount. The amount is typically a `https://developer.android.com/reference/kotlin/java/time/Period.html#` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#` interface, such as `https://developer.android.com/reference/kotlin/java/time/Duration.html#`.

Some example code indicating how and why this method is used:

```kotlin
date = date.minus(period);               // subtract a Period instance
   date = date.minus(duration);             // subtract a Duration instance
   date = date.minus(workingDays(6));       // example user-written workingDays method
  
```

Note that calling `plus` followed by `minus` is not guaranteed to return the same date-time.

| Parameters ||
|---|---|
| `amount` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!: the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): ChronoZonedDateTime<D>!
```

Returns an object of the same type as this object with the specified period subtracted.

This method returns a new object based on this one with the specified period subtracted. For example, on a `LocalDate`, this could be used to subtract a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st March, then subtracting one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---|---|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the specified unit to subtract, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit of the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | an object of the same type with the specified period subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the unit cannot be subtracted |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun plus(amount: TemporalAmount!): ChronoZonedDateTime<D>!
```

Returns an object of the same type as this object with an amount added.

This adjusts this temporal, adding according to the rules of the specified amount. The amount is typically a `https://developer.android.com/reference/kotlin/java/time/Period.html#` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#` interface, such as `https://developer.android.com/reference/kotlin/java/time/Duration.html#`.

Some example code indicating how and why this method is used:

```kotlin
date = date.plus(period);                // add a Period instance
   date = date.plus(duration);              // add a Duration instance
   date = date.plus(workingDays(6));        // example user-written workingDays method
  
```

Note that calling `plus` followed by `minus` is not guaranteed to return the same date-time.

| Parameters ||
|---|---|
| `amount` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!: the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): ChronoZonedDateTime<D>!
```

Returns an object of the same type as this object with the specified period added.

This method returns a new object based on this one with the specified period added. For example, on a `LocalDate`, this could be used to add a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then adding one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---|---|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the specified unit to add, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!: the unit of the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | an object of the same type with the specified period added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the unit cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this date-time using the specified query.

This queries this date-time using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#queryFrom(java.time.temporal.TemporalAccessor)` method on the specified query passing `this` as the argument.

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
open fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

All fields can be expressed as a `long` integer. This method returns an object that describes the valid range for that value. The value of this temporal object is used to enhance the accuracy of the returned range. If the date-time cannot return the range, because the field is unsupported or for some other reason, an exception will be thrown.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to query the range for, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#!` | the range of valid values for the field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### timeLineOrder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun timeLineOrder(): Comparator<ChronoZonedDateTime<*>!>!
```

Gets a comparator that compares `ChronoZonedDateTime` in time-line order ignoring the chronology.

This comparator differs from the comparison in `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#compareTo(java.time.chrono.ChronoZonedDateTime)` in that it only compares the underlying instant and not the chronology. This allows dates in different calendar systems to be compared based on the position of the date-time on the instant time-line. The underlying comparison is equivalent to comparing the epoch-second and nano-of-second.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<*>!>!` | a comparator that compares in time-line order ignoring the chronology |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#isAfter(java.time.chrono.ChronoZonedDateTime)`
- `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#isBefore(java.time.chrono.ChronoZonedDateTime)`
- `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#isEqual(java.time.chrono.ChronoZonedDateTime)`

### toEpochSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toEpochSecond(): Long
```

Converts this date-time to the number of seconds from the epoch of 1970-01-01T00:00:00Z.

This uses the [local date-time](ChronoZonedDateTime.md)) and [offset](ChronoZonedDateTime.md)) to calculate the epoch-second value, which is the number of elapsed seconds from 1970-01-01T00:00:00Z. Instants on the time-line after the epoch are positive, earlier are negative.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of seconds from the epoch of 1970-01-01T00:00:00Z |

### toInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toInstant(): Instant!
```

Converts this date-time to an `Instant`.

This returns an `Instant` representing the same point on the time-line as this date-time. The calculation combines the [local date-time](ChronoZonedDateTime.md)) and [offset](ChronoZonedDateTime.md)).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#!` | an `Instant` representing the same instant, not null |

### toLocalDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toLocalDate(): D
```

Gets the local date part of this date-time.

This returns a local date with the same year, month and day as this date-time.

| Return ||
|---|---|
| `D` | the date part of this date-time, not null |

### toLocalDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toLocalDateTime(): ChronoLocalDateTime<D>!
```

Gets the local date-time part of this date-time.

This returns a local date with the same year, month and day as this date-time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime<D>!` | the local date-time part of this date-time, not null |

### toLocalTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toLocalTime(): LocalTime!
```

Gets the local time part of this date-time.

This returns a local time with the same hour, minute, second and nanosecond as this date-time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalTime.html#!` | the time part of this date-time, not null |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun with(adjuster: TemporalAdjuster!): ChronoZonedDateTime<D>!
```

Returns an adjusted object of the same type as this object with the adjustment made.

This adjusts this date-time according to the rules of the specified adjuster. A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjusters.html#`. These include finding the "last day of the month" and "next Wednesday". The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

Some example code indicating how and why this method is used:

```kotlin
date = date.with(Month.JULY);        // most key classes implement TemporalAdjuster
   date = date.with(lastDayOfMonth());  // static import from Adjusters
   date = date.with(next(WEDNESDAY));   // static import from Adjusters and DayOfWeek
  
```

| Parameters ||
|---|---|
| `adjuster` | [TemporalAdjuster](../java.time.temporal/TemporalAdjuster.md)!: the adjuster to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if unable to make the adjustment |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun with(
    field: TemporalField!, 
    newValue: Long
): ChronoZonedDateTime<D>!
```

Returns an object of the same type as this object with the specified field altered.

This returns a new object based on this one with the value for the specified field changed. For example, on a `LocalDate`, this could be used to set the year, month or day-of-month. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then changing the month to February would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value of the field in the result |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | an object of the same type with the specified field set, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |

### withEarlierOffsetAtOverlap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun withEarlierOffsetAtOverlap(): ChronoZonedDateTime<D>!
```

Returns a copy of this date-time changing the zone offset to the earlier of the two valid offsets at a local time-line overlap.

This method only has any effect when the local time-line overlaps, such as at an autumn daylight savings cutover. In this scenario, there are two valid offsets for the local date-time. Calling this method will return a zoned date-time with the earlier of the two selected.

If this method is called when it is not an overlap, `this` is returned.

This instance is immutable and unaffected by this method call.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | a `ChronoZonedDateTime` based on this date-time with the earlier offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if no rules are valid for this date-time |

### withLaterOffsetAtOverlap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun withLaterOffsetAtOverlap(): ChronoZonedDateTime<D>!
```

Returns a copy of this date-time changing the zone offset to the later of the two valid offsets at a local time-line overlap.

This method only has any effect when the local time-line overlaps, such as at an autumn daylight savings cutover. In this scenario, there are two valid offsets for the local date-time. Calling this method will return a zoned date-time with the later of the two selected.

If this method is called when it is not an overlap, `this` is returned.

This instance is immutable and unaffected by this method call.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | a `ChronoZonedDateTime` based on this date-time with the later offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if no rules are valid for this date-time |

### withZoneSameInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun withZoneSameInstant(zone: ZoneId!): ChronoZonedDateTime<D>!
```

Returns a copy of this date-time with a different time-zone, retaining the instant.

This method changes the time-zone and retains the instant. This normally results in a change to the local date-time.

This method is based on retaining the same instant, thus gaps and overlaps in the local time-line have no effect on the result.

To change the offset while keeping the local time, use `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#withZoneSameLocal(java.time.ZoneId)`.

| Parameters ||
|---|---|
| `zone` | [ZoneId](../java.time/ZoneId.md)!: the time-zone to change to, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | a `ChronoZonedDateTime` based on this date-time with the requested zone, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported date range |

### withZoneSameLocal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun withZoneSameLocal(zone: ZoneId!): ChronoZonedDateTime<D>!
```

Returns a copy of this date-time with a different time-zone, retaining the local date-time if possible.

This method changes the time-zone and retains the local date-time. The local date-time is only changed if it is invalid for the new zone.

To change the zone and adjust the local date-time, use `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#withZoneSameInstant(java.time.ZoneId)`.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `zone` | [ZoneId](../java.time/ZoneId.md)!: the time-zone to change to, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#<D>!` | a `ChronoZonedDateTime` based on this date-time with the requested zone, not null |
