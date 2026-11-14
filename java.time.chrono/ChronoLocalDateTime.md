# ChronoLocalDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChronoLocalDateTime

```
interface ChronoLocalDateTime<D : ChronoLocalDate!> : Comparable<ChronoLocalDateTime<*>!>, Temporal, TemporalAdjuster
```

| [java.time.chrono.ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#) |

| Known Direct Subclasses [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------| | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | |

A date-time without a time-zone in an arbitrary chronology, intended for advanced globalization use cases.

**Most applications should declare method signatures, fields and variables as [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#), not this interface.**

A`ChronoLocalDateTime`is the abstract representation of a local date-time where the`Chronology chronology`, or calendar system, is pluggable. The date-time is defined in terms of fields expressed by [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#), where most common implementations are defined in [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#). The chronology defines how the calendar system operates and the meaning of the standard fields.

## When to use this interface

The design of the API encourages the use of`LocalDateTime`rather than this interface, even in the case where the application needs to deal with multiple calendar systems. The rationale for this is explored in detail in [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate).

Ensure that the discussion in`ChronoLocalDate`has been read and understood before using this interface.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | [adjustInto](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#adjustInto(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`)` Adjusts the specified temporal object to have the same date and time as this object. |
| abstract [ChronoZonedDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime)\<D\>! | [atZone](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#atZone(java.time.ZoneId))`(`zone:` ` [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!`)` Combines this time with a time-zone to create a`ChronoZonedDateTime`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#compareTo(java.time.chrono.ChronoLocalDateTime))`(`other:` ` [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<*>!`)` Compares this date-time to another date-time, including the chronology. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#format(java.time.format.DateTimeFormatter))`(`formatter:` ` [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#)!`)` Formats this date-time using the specified formatter. |
| openstatic [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<\*\>! | [from](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#from(java.time.temporal.TemporalAccessor))`(`temporal:` ` [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!`)` Obtains an instance of`ChronoLocalDateTime`from a temporal object. |
| open [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology)! | [getChronology](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#getChronology())`()` Gets the chronology of this date-time. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfter](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#isAfter(java.time.chrono.ChronoLocalDateTime))`(`other:` ` [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<*>!`)` Checks if this date-time is after the specified date-time ignoring the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBefore](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#isBefore(java.time.chrono.ChronoLocalDateTime))`(`other:` ` [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<*>!`)` Checks if this date-time is before the specified date-time ignoring the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqual](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#isEqual(java.time.chrono.ChronoLocalDateTime))`(`other:` ` [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<*>!`)` Checks if this date-time is equal to the specified date-time ignoring the chronology. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Checks if the specified field is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#isSupported(java.time.temporal.TemporalUnit))`(`unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` Checks if the specified unit is supported. |
| open [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<D\>! | [minus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#minus(java.time.temporal.TemporalAmount))`(`amount:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!`)` Returns an object of the same type as this object with an amount subtracted. |
| open [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<D\>! | [minus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` Returns an object of the same type as this object with the specified period subtracted. |
| open [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<D\>! | [plus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#plus(java.time.temporal.TemporalAmount))`(`amount:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!`)` Returns an object of the same type as this object with an amount added. |
| abstract [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<D\>! | [plus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` Returns an object of the same type as this object with the specified period added. |
| openR | [query](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)<R>!`)` Queries this date-time using the specified query. |
| openstatic [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\< [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<\*\>!\>! | [timeLineOrder](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#timeLineOrder())`()` Gets a comparator that compares`ChronoLocalDateTime`in time-line order ignoring the chronology. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toEpochSecond](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#toEpochSecond(java.time.ZoneOffset))`(`offset:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!`)` Converts this date-time to the number of seconds from the epoch of 1970-01-01T00:00:00Z. |
| open [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)! | [toInstant](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#toInstant(java.time.ZoneOffset))`(`offset:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!`)` Converts this date-time to an`Instant`. |
| abstractD | [toLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#toLocalDate())`()` Gets the local date part of this date-time. |
| abstract [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)! | [toLocalTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#toLocalTime())`()` Gets the local time part of this date-time. |
| open [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<D\>! | [with](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#with(java.time.temporal.TemporalAdjuster))`(`adjuster:` ` [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster.html#)!`)` Returns an adjusted object of the same type as this object with the adjustment made. |
| abstract [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<D\>! | [with](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#with(java.time.temporal.TemporalField,%20kotlin.Long))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns an object of the same type as this object with the specified field altered. |

| Inherited functions ||
|---|---|
| From class [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#get(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> Gets the value of the specified field as an`int`. This queries the date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> Gets the value of the specified field as a`long`. This queries the date-time for the value of the specified field. The returned value may be outside the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> Checks if the specified field is supported. This checks if the date-time can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#range(java.time.temporal.TemporalField))and [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#get(java.time.temporal.TemporalField))methods will throw an exception. <br /> | | R | [query](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)<R>!`)` <br /> Queries this date-time. This queries this date-time using the specified query strategy object. Queries are a key tool for extracting information from date-times. They exists to externalize the process of querying, permitting different approaches, as per the strategy design pattern. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday. The most common query implementations are method references, such as`LocalDate::from`and`ZoneId::from`. Additional implementations are provided as static methods on [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#). <br /> | | [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | [range](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> Gets the range of valid values for the specified field. All fields can be expressed as a`long`integer. This method returns an object that describes the valid range for that value. The value of this temporal object is used to enhance the accuracy of the returned range. If the date-time cannot return the range, because the field is unsupported or for some other reason, an exception will be thrown. Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field. <br /> | ||
| From class [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit))`(`endExclusive:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` <br /> Calculates the amount of time until another temporal in terms of the specified unit. This calculates the amount of time between two temporal objects in terms of a single`TemporalUnit`. The start and end points are`this`and the specified temporal. The end point is converted to be of the same type as the start point if different. The result will be negative if the end is before the start. For example, the amount in hours between two temporal objects can be calculated using`startTime.until(endTime, HOURS)`. The calculation returns a whole number, representing the number of complete units between the two temporals. For example, the amount in hours between the times 11:30 and 13:29 will only be one hour as it is one minute short of two hours. There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [TemporalUnit.between(Temporal, Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)): ```kotlin // these two lines are equivalent temporal = start.until(end, unit); temporal = unit.between(start, end); ``` The choice should be made based on which makes the code more readable. For example, this method allows the number of days between two dates to be calculated: ```kotlin long daysBetween = start.until(end, DAYS); // or alternatively long daysBetween = DAYS.between(start, end); ``` <br /> | ||

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same date and time as this object.

This returns a temporal object of the same observable type as the input with the date and time changed to be the same as this.

The adjustment is equivalent to using [Temporal.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalField,%20kotlin.Long))twice, passing [ChronoField.EPOCH_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) and [ChronoField.NANO_OF_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as the fields.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalAdjuster)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisLocalDateTime.adjustInto(temporal);
    temporal = temporal.with(thisLocalDateTime);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!:the target object to be adjusted, not null |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | the adjusted object, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### atZone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun atZone(zone: ZoneId!): ChronoZonedDateTime<D>!
```

Combines this time with a time-zone to create a`ChronoZonedDateTime`.

This returns a`ChronoZonedDateTime`formed from this date-time at the specified time-zone. The result will match this date-time as closely as possible. Time-zone rules, such as daylight savings, mean that not every local date-time is valid for the specified zone, thus the local date-time may be adjusted.

The local date-time is resolved to a single instant on the time-line. This is achieved by finding a valid offset from UTC/Greenwich for the local date-time as defined by the [rules](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules.html#) of the zone ID.

In most cases, there is only one valid offset for a local date-time. In the case of an overlap, where clocks are set back, there are two valid offsets. This method uses the earlier offset typically corresponding to "summer".

In the case of a gap, where clocks jump forward, there is no valid offset. Instead, the local date-time is adjusted to be later by the length of the gap. For a typical one hour daylight savings change, the local date-time will be moved one hour later into the offset typically corresponding to "summer".

To obtain the later offset during an overlap, call [ChronoZonedDateTime.withLaterOffsetAtOverlap()](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#withLaterOffsetAtOverlap())on the result of this method.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!:the time-zone to use, not null |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [ChronoZonedDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime)<D>! | the zoned date-time formed from this date-time, not null |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: ChronoLocalDateTime<*>!): Int
```

Compares this date-time to another date-time, including the chronology.

The comparison is based first on the underlying time-line date-time, then on the chronology. It is "consistent with equals", as defined by [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#).

For example, the following is the comparator order:

1. `2012-12-03T12:00 (ISO)`
2. `2012-12-04T12:00 (ISO)`
3. `2555-12-04T12:00 (ThaiBuddhist)`
4. `2012-12-05T12:00 (ISO)`

Values #2 and #3 represent the same date-time on the time-line. When two values represent the same date-time, the chronology ID is compared to distinguish them. This step is needed to make the ordering "consistent with equals".

If all the date-time objects being compared are in the same chronology, then the additional chronology stage is not required and only the local date-time is used.

This default implementation performs the comparison defined above.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<\*\>!:the other date-time to compare to, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the comparator value, negative if less, positive if greater |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

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
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `formatter` | [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#)!:the formatter to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted date-time string, not null |

| Exceptions ||
|-------------------------------|------------------------------------|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun from(temporal: TemporalAccessor!): ChronoLocalDateTime<*>!
```

Obtains an instance of`ChronoLocalDateTime`from a temporal object.

This obtains a local date-time based on the specified temporal. A`TemporalAccessor`represents an arbitrary set of date and time information, which this factory converts to an instance of`ChronoLocalDateTime`.

The conversion extracts and combines the chronology and the date-time from the temporal object. The behavior is equivalent to using [Chronology.localDateTime(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#localDateTime(java.time.temporal.TemporalAccessor))with the extracted chronology. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects.

This method matches the signature of the functional interface [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#) allowing it to be used as a query via method reference,`ChronoLocalDateTime::from`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!:the temporal object to convert, not null |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<*>! | the date-time, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------|
| `java.time.DateTimeException` | if unable to convert to a`ChronoLocalDateTime` |

**See Also**

- [java.time.chrono.Chronology#localDateTime(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#localDateTime(java.time.temporal.TemporalAccessor)) 

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChronology(): Chronology!
```

Gets the chronology of this date-time.

The`Chronology`represents the calendar system in use. The era and other fields in [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) are defined by the chronology.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology)! | the chronology, not null |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAfter(other: ChronoLocalDateTime<*>!): Boolean
```

Checks if this date-time is after the specified date-time ignoring the chronology.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#compareTo(java.time.chrono.ChronoLocalDateTime))in that it only compares the underlying date-time and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position.

This default implementation performs the comparison based on the epoch-day and nano-of-day.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<\*\>!:the other date-time to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is after the specified date-time |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBefore(other: ChronoLocalDateTime<*>!): Boolean
```

Checks if this date-time is before the specified date-time ignoring the chronology.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#compareTo(java.time.chrono.ChronoLocalDateTime))in that it only compares the underlying date-time and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position.

This default implementation performs the comparison based on the epoch-day and nano-of-day.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<\*\>!:the other date-time to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is before the specified date-time |

### isEqual

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEqual(other: ChronoLocalDateTime<*>!): Boolean
```

Checks if this date-time is equal to the specified date-time ignoring the chronology.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#compareTo(java.time.chrono.ChronoLocalDateTime))in that it only compares the underlying date and time and not the chronology. This allows date-times in different calendar systems to be compared based on the time-line position.

This default implementation performs the comparison based on the epoch-day and nano-of-day.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)\<\*\>!:the other date-time to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the underlying date-time is equal to the specified date-time on the timeline |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if the specified field can be queried on this date-time. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#range(java.time.temporal.TemporalField)), [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#get(java.time.temporal.TemporalField))and [with(java.time.temporal.TemporalField,long)](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#with(java.time.temporal.TemporalField,%20kotlin.Long))methods will throw an exception.

The set of supported fields is defined by the chronology and normally includes all`ChronoField`date and time fields.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field can be queried, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to or subtracted from this date-time. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))and [minus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))methods will throw an exception.

The set of supported units is defined by the chronology and normally includes all`ChronoUnit`units except`FOREVER`.

If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.isSupportedBy(Temporal)`passing`this`as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit can be added/subtracted, false if not |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun minus(amount: TemporalAmount!): ChronoLocalDateTime<D>!
```

Returns an object of the same type as this object with an amount subtracted.

This adjusts this temporal, subtracting according to the rules of the specified amount. The amount is typically a [java.time.Period](https://developer.android.com/reference/kotlin/java/time/Period.html#) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#) interface, such as [java.time.Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#).

Some example code indicating how and why this method is used: 

```kotlin
date = date.minus(period);               // subtract a Period instance
   date = date.minus(duration);             // subtract a Duration instance
   date = date.minus(workingDays(6));       // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!:the amount to subtract, not null |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<D>! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|-----------------------------------|
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): ChronoLocalDateTime<D>!
```

Returns an object of the same type as this object with the specified period subtracted.

This method returns a new object based on this one with the specified period subtracted. For example, on a`LocalDate`, this could be used to subtract a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st March, then subtracting one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the specified unit to subtract, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit of the amount to subtract, not null |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<D>! | an object of the same type with the specified period subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the unit cannot be subtracted |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun plus(amount: TemporalAmount!): ChronoLocalDateTime<D>!
```

Returns an object of the same type as this object with an amount added.

This adjusts this temporal, adding according to the rules of the specified amount. The amount is typically a [java.time.Period](https://developer.android.com/reference/kotlin/java/time/Period.html#) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#) interface, such as [java.time.Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#).

Some example code indicating how and why this method is used: 

```kotlin
date = date.plus(period);                // add a Period instance
   date = date.plus(duration);              // add a Duration instance
   date = date.plus(workingDays(6));        // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!:the amount to add, not null |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<D>! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): ChronoLocalDateTime<D>!
```

Returns an object of the same type as this object with the specified period added.

This method returns a new object based on this one with the specified period added. For example, on a`LocalDate`, this could be used to add a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then adding one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the specified unit to add, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit of the amount to add, not null |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<D>! | an object of the same type with the specified period added, not null |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if the unit cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this date-time using the specified query.

This queries this date-time using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#queryFrom(java.time.temporal.TemporalAccessor))method on the specified query passing`this`as the argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)\<R\>!:the query to invoke, not null |

| Return ||
|---|---------------------------------------------------------------|
| R | the query result, null may be returned (defined by the query) |

| Exceptions ||
|---------------------------------|---------------------------------------------------|
| `java.time.DateTimeException` | if unable to query (defined by the query) |
| `java.lang.ArithmeticException` | if numeric overflow occurs (defined by the query) |

### timeLineOrder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun timeLineOrder(): Comparator<ChronoLocalDateTime<*>!>!
```

Gets a comparator that compares`ChronoLocalDateTime`in time-line order ignoring the chronology.

This comparator differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#compareTo(java.time.chrono.ChronoLocalDateTime))in that it only compares the underlying date-time and not the chronology. This allows dates in different calendar systems to be compared based on the position of the date-time on the local time-line. The underlying comparison is equivalent to comparing the epoch-day and nano-of-day.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)< [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<*>!>! | a comparator that compares in time-line order ignoring the chronology |

**See Also**

- [#isAfter](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#isAfter(java.time.chrono.ChronoLocalDateTime))
- [#isBefore](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#isBefore(java.time.chrono.ChronoLocalDateTime))
- [#isEqual](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#isEqual(java.time.chrono.ChronoLocalDateTime)) 

### toEpochSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toEpochSecond(offset: ZoneOffset!): Long
```

Converts this date-time to the number of seconds from the epoch of 1970-01-01T00:00:00Z.

This combines this local date-time and the specified offset to calculate the epoch-second value, which is the number of elapsed seconds from 1970-01-01T00:00:00Z. Instants on the time-line after the epoch are positive, earlier are negative.

This default implementation calculates from the epoch-day of the date and the second-of-day of the time.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!:the offset to use for the conversion, not null |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of seconds from the epoch of 1970-01-01T00:00:00Z |

### toInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInstant(offset: ZoneOffset!): Instant!
```

Converts this date-time to an`Instant`.

This combines this local date-time and the specified offset to form an`Instant`.

This default implementation calculates from the epoch-day of the date and the second-of-day of the time.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!:the offset to use for the conversion, not null |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)! | an`Instant`representing the same instant, not null |

### toLocalDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toLocalDate(): D
```

Gets the local date part of this date-time.

This returns a local date with the same year, month and day as this date-time.

| Return ||
|---|-------------------------------------------|
| D | the date part of this date-time, not null |

### toLocalTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toLocalTime(): LocalTime!
```

Gets the local time part of this date-time.

This returns a local time with the same hour, minute, second and nanosecond as this date-time.

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------|
| [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)! | the time part of this date-time, not null |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun with(adjuster: TemporalAdjuster!): ChronoLocalDateTime<D>!
```

Returns an adjusted object of the same type as this object with the adjustment made.

This adjusts this date-time according to the rules of the specified adjuster. A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in [TemporalAdjusters](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjusters.html#). These include finding the "last day of the month" and "next Wednesday". The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

Some example code indicating how and why this method is used: 

```kotlin
date = date.with(Month.JULY);        // most key classes implement TemporalAdjuster
   date = date.with(lastDayOfMonth());  // static import from Adjusters
   date = date.with(next(WEDNESDAY));   // static import from Adjusters and DayOfWeek
  
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `adjuster` | [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster.html#)!:the adjuster to use, not null |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<D>! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun with(
    field: TemporalField!, 
    newValue: Long
): ChronoLocalDateTime<D>!
```

Returns an object of the same type as this object with the specified field altered.

This returns a new object based on this one with the value for the specified field changed. For example, on a`LocalDate`, this could be used to set the year, month or day-of-month. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then changing the month to February would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field in the result |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#)<D>! | an object of the same type with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
