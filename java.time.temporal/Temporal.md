# Temporal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Temporal

```
interface Temporal : TemporalAccessor
```

| [java.time.temporal.Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#) |

| Known Direct Subclasses [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#), [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime.html#), [ChronoZonedDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime.html#), [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate.html#), [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#), [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate.html#), [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#), [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#), [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#), [MinguoDate](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoDate.html#), [OffsetDateTime](https://developer.android.com/reference/kotlin/java/time/OffsetDateTime.html#), [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime.html#), and 4 others. |------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#) | A date without time-of-day or time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime.html#) | A date-time without a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoZonedDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime.html#) | A date-time with a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate.html#) | A date in the Hijrah calendar system. | | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | An instantaneous point on the time-line. | | [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate.html#) | A date in the Japanese Imperial calendar system. | | [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#) | A time without a time-zone in the ISO-8601 calendar system, such as`10:15:30`. | | [MinguoDate](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoDate.html#) | A date in the Minguo calendar system. | | [OffsetDateTime](https://developer.android.com/reference/kotlin/java/time/OffsetDateTime.html#) | A date-time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00`. | | [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime.html#) | A time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`10:15:30+01:00`. | | [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate.html#) | A date in the Thai Buddhist calendar system. | | [Year](https://developer.android.com/reference/kotlin/java/time/Year.html#) | A year in the ISO-8601 calendar system, such as`2007`. | | [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth.html#) | A year-month in the ISO-8601 calendar system, such as`2007-12`. | | [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#) | A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`. | |

| Known Indirect Subclasses [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate.html#), [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate.html#), [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#), [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#), [MinguoDate](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoDate.html#), [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate.html#), [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------| | [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate.html#) | A date in the Hijrah calendar system. | | [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate.html#) | A date in the Japanese Imperial calendar system. | | [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [MinguoDate](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoDate.html#) | A date in the Minguo calendar system. | | [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate.html#) | A date in the Thai Buddhist calendar system. | | [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#) | A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`. | |

Framework-level interface defining read-write access to a temporal object, such as a date, time, offset or some combination of these.

This is the base interface type for date, time and offset objects that are complete enough to be manipulated using plus and minus. It is implemented by those classes that can provide and manipulate information as [fields](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField) or [queries](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery). See [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor) for the read-only version of this interface.

Most date and time information can be represented as a number. These are modeled using`TemporalField`with the number held using a`long`to handle large values. Year, month and day-of-month are simple examples of fields, but they also include instant and offsets. See [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) for the standard set of fields.

Two pieces of date/time information cannot be represented by numbers, the [chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#) and the [time-zone](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#). These can be accessed via [queries](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#query(java.time.temporal.TemporalQuery))using the static methods defined on [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery).

This interface is a framework-level interface that should not be widely used in application code. Instead, applications should create and pass around instances of concrete types, such as`LocalDate`. There are many reasons for this, part of which is that implementations of this interface may be in calendar systems other than ISO. See [java.time.chrono.ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#) for a fuller discussion of the issues.

## When to implement

A class should implement this interface if it meets three criteria:

- it provides access to date/time/offset information, as per`TemporalAccessor`
- the set of fields are contiguous from the largest to the smallest
- the set of fields are complete, such that no other field is needed to define the valid range of values for the fields that are represented

Four examples make this clear:

- `LocalDate`implements this interface as it represents a set of fields that are contiguous from days to forever and require no external information to determine the validity of each date. It is therefore able to implement plus/minus correctly.
- `LocalTime`implements this interface as it represents a set of fields that are contiguous from nanos to within days and require no external information to determine validity. It is able to implement plus/minus correctly, by wrapping around the day.
- `MonthDay`, the combination of month-of-year and day-of-month, does not implement this interface. While the combination is contiguous, from days to months within years, the combination does not have sufficient information to define the valid range of values for day-of-month. As such, it is unable to implement plus/minus correctly.
- The combination day-of-week and day-of-month ("Friday the 13th") should not implement this interface. It does not represent a contiguous set of fields, as days to weeks overlaps days to months.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#isSupported(java.time.temporal.TemporalUnit))`(`unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Checks if the specified unit is supported. |
| open [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | [minus](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#minus(java.time.temporal.TemporalAmount))`(`amount:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!`)` Returns an object of the same type as this object with an amount subtracted. |
| open [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | [minus](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Returns an object of the same type as this object with the specified period subtracted. |
| open [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | [plus](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#plus(java.time.temporal.TemporalAmount))`(`amount:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!`)` Returns an object of the same type as this object with an amount added. |
| abstract [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | [plus](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Returns an object of the same type as this object with the specified period added. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit))`(`endExclusive:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)!`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Calculates the amount of time until another temporal in terms of the specified unit. |
| open [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | [with](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster))`(`adjuster:` ` [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster)!`)` Returns an adjusted object of the same type as this object with the adjustment made. |
| abstract [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | [with](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns an object of the same type as this object with the specified field altered. |

| Inherited functions ||
|---|---|
| From class [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor) |---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#get(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` <br /> Gets the value of the specified field as an`int`. This queries the date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` <br /> Gets the value of the specified field as a`long`. This queries the date-time for the value of the specified field. The returned value may be outside the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` <br /> Checks if the specified field is supported. This checks if the date-time can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#range(java.time.temporal.TemporalField))and [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#get(java.time.temporal.TemporalField))methods will throw an exception. <br /> | | R | [query](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)<R>!`)` <br /> Queries this date-time. This queries this date-time using the specified query strategy object. Queries are a key tool for extracting information from date-times. They exists to externalize the process of querying, permitting different approaches, as per the strategy design pattern. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday. The most common query implementations are method references, such as`LocalDate::from`and`ZoneId::from`. Additional implementations are provided as static methods on [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery). <br /> | | [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | [range](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` <br /> Gets the range of valid values for the specified field. All fields can be expressed as a`long`integer. This method returns an object that describes the valid range for that value. The value of this temporal object is used to enhance the accuracy of the returned range. If the date-time cannot return the range, because the field is unsupported or for some other reason, an exception will be thrown. Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field. <br /> | ||

## Public methods

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this date-time. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))and [minus](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))methods will throw an exception.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit can be added/subtracted, false if not |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun minus(amount: TemporalAmount!): Temporal!
```

Returns an object of the same type as this object with an amount subtracted.

This adjusts this temporal, subtracting according to the rules of the specified amount. The amount is typically a [java.time.Period](https://developer.android.com/reference/kotlin/java/time/Period.html#) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount) interface, such as [java.time.Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#).

Some example code indicating how and why this method is used: 

```kotlin
date = date.minus(period);               // subtract a Period instance
   date = date.minus(duration);             // subtract a Duration instance
   date = date.minus(workingDays(6));       // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!:the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | an object of the same type with the specified adjustment made, not null |

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
): Temporal!
```

Returns an object of the same type as this object with the specified period subtracted.

This method returns a new object based on this one with the specified period subtracted. For example, on a`LocalDate`, this could be used to subtract a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st March, then subtracting one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the specified unit to subtract, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit of the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | an object of the same type with the specified period subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the unit cannot be subtracted |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun plus(amount: TemporalAmount!): Temporal!
```

Returns an object of the same type as this object with an amount added.

This adjusts this temporal, adding according to the rules of the specified amount. The amount is typically a [java.time.Period](https://developer.android.com/reference/kotlin/java/time/Period.html#) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount) interface, such as [java.time.Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#).

Some example code indicating how and why this method is used: 

```kotlin
date = date.plus(period);                // add a Period instance
   date = date.plus(duration);              // add a Duration instance
   date = date.plus(workingDays(6));        // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!:the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | an object of the same type with the specified adjustment made, not null |

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
): Temporal!
```

Returns an object of the same type as this object with the specified period added.

This method returns a new object based on this one with the specified period added. For example, on a`LocalDate`, this could be used to add a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then adding one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the specified unit to add, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit of the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | an object of the same type with the specified period added, not null |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if the unit cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

Calculates the amount of time until another temporal in terms of the specified unit.

This calculates the amount of time between two temporal objects in terms of a single`TemporalUnit`. The start and end points are`this`and the specified temporal. The end point is converted to be of the same type as the start point if different. The result will be negative if the end is before the start. For example, the amount in hours between two temporal objects can be calculated using`startTime.until(endTime, HOURS)`.

The calculation returns a whole number, representing the number of complete units between the two temporals. For example, the amount in hours between the times 11:30 and 13:29 will only be one hour as it is one minute short of two hours.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [TemporalUnit.between(Temporal, Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)): 

```kotlin
// these two lines are equivalent
    temporal = start.until(end, unit);
    temporal = unit.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

For example, this method allows the number of days between two dates to be calculated: 

```kotlin
long daysBetween = start.until(end, DAYS);
   // or alternatively
   long daysBetween = DAYS.between(start, end);
  
```

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endExclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)!:the end temporal, exclusive, converted to be of the same type as this object, not null |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!:the unit to measure the amount in, not null |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between this temporal object and the specified one in terms of the unit; positive if the specified object is later than this one, negative if it is earlier than this one |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to the same type as this temporal |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun with(adjuster: TemporalAdjuster!): Temporal!
```

Returns an adjusted object of the same type as this object with the adjustment made.

This adjusts this date-time according to the rules of the specified adjuster. A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in [TemporalAdjusters](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjusters). These include finding the "last day of the month" and "next Wednesday". The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

Some example code indicating how and why this method is used: 

```kotlin
date = date.with(Month.JULY);        // most key classes implement TemporalAdjuster
   date = date.with(lastDayOfMonth());  // static import from Adjusters
   date = date.with(next(WEDNESDAY));   // static import from Adjusters and DayOfWeek
  
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `adjuster` | [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster)!:the adjuster to use, not null |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | an object of the same type with the specified adjustment made, not null |

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
): Temporal!
```

Returns an object of the same type as this object with the specified field altered.

This returns a new object based on this one with the value for the specified field changed. For example, on a`LocalDate`, this could be used to set the year, month or day-of-month. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then changing the month to February would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field in the result |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#)! | an object of the same type with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
