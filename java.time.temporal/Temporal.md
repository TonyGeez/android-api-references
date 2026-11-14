# Temporal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Temporal

```
interface Temporal : TemporalAccessor
```

| [java.time.temporal.Temporal](Temporal.md) |

| Known Direct Subclasses [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md), [ChronoLocalDateTime](../java.time.chrono/ChronoLocalDateTime.md), [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md), [HijrahDate](../java.time.chrono/HijrahDate.md), [Instant](../java.time/Instant.md), [JapaneseDate](../java.time.chrono/JapaneseDate.md), [LocalDate](../java.time/LocalDate.md), [LocalDateTime](../java.time/LocalDateTime.md), [LocalTime](../java.time/LocalTime.md), [MinguoDate](../java.time.chrono/MinguoDate.md), [OffsetDateTime](../java.time/OffsetDateTime.md), [OffsetTime](../java.time/OffsetTime.md), and 4 others. |------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md) | A date without time-of-day or time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoLocalDateTime](../java.time.chrono/ChronoLocalDateTime.md) | A date-time without a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md) | A date-time with a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [HijrahDate](../java.time.chrono/HijrahDate.md) | A date in the Hijrah calendar system. | | [Instant](../java.time/Instant.md) | An instantaneous point on the time-line. | | [JapaneseDate](../java.time.chrono/JapaneseDate.md) | A date in the Japanese Imperial calendar system. | | [LocalDate](../java.time/LocalDate.md) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDateTime](../java.time/LocalDateTime.md) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [LocalTime](../java.time/LocalTime.md) | A time without a time-zone in the ISO-8601 calendar system, such as`10:15:30`. | | [MinguoDate](../java.time.chrono/MinguoDate.md) | A date in the Minguo calendar system. | | [OffsetDateTime](../java.time/OffsetDateTime.md) | A date-time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00`. | | [OffsetTime](../java.time/OffsetTime.md) | A time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`10:15:30+01:00`. | | [ThaiBuddhistDate](../java.time.chrono/ThaiBuddhistDate.md) | A date in the Thai Buddhist calendar system. | | [Year](../java.time/Year.md) | A year in the ISO-8601 calendar system, such as`2007`. | | [YearMonth](../java.time/YearMonth.md) | A year-month in the ISO-8601 calendar system, such as`2007-12`. | | [ZonedDateTime](../java.time/ZonedDateTime.md) | A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [HijrahDate](../java.time.chrono/HijrahDate.md), [JapaneseDate](../java.time.chrono/JapaneseDate.md), [LocalDate](../java.time/LocalDate.md), [LocalDateTime](../java.time/LocalDateTime.md), [MinguoDate](../java.time.chrono/MinguoDate.md), [ThaiBuddhistDate](../java.time.chrono/ThaiBuddhistDate.md), [ZonedDateTime](../java.time/ZonedDateTime.md) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------| | [HijrahDate](../java.time.chrono/HijrahDate.md) | A date in the Hijrah calendar system. | | [JapaneseDate](../java.time.chrono/JapaneseDate.md) | A date in the Japanese Imperial calendar system. | | [LocalDate](../java.time/LocalDate.md) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDateTime](../java.time/LocalDateTime.md) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [MinguoDate](../java.time.chrono/MinguoDate.md) | A date in the Minguo calendar system. | | [ThaiBuddhistDate](../java.time.chrono/ThaiBuddhistDate.md) | A date in the Thai Buddhist calendar system. | | [ZonedDateTime](../java.time/ZonedDateTime.md) | A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Framework-level interface defining read-write access to a temporal object, such as a date, time, offset or some combination of these.

This is the base interface type for date, time and offset objects that are complete enough to be manipulated using plus and minus. It is implemented by those classes that can provide and manipulate information as [fields](TemporalField.md) or [queries](TemporalQuery.md). See [TemporalAccessor](TemporalAccessor.md) for the read-only version of this interface.

Most date and time information can be represented as a number. These are modeled using`TemporalField`with the number held using a`long`to handle large values. Year, month and day-of-month are simple examples of fields, but they also include instant and offsets. See [ChronoField](ChronoField.md) for the standard set of fields.

Two pieces of date/time information cannot be represented by numbers, the [chronology](../java.time.chrono/Chronology.md) and the [time-zone](../java.time/ZoneId.md). These can be accessed via [queries](TemporalAccessor.md))using the static methods defined on [TemporalQuery](TemporalQuery.md).

This interface is a framework-level interface that should not be widely used in application code. Instead, applications should create and pass around instances of concrete types, such as`LocalDate`. There are many reasons for this, part of which is that implementations of this interface may be in calendar systems other than ISO. See [java.time.chrono.ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md) for a fuller discussion of the issues.

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
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](Temporal.md))`(`unit:` ` [TemporalUnit](TemporalUnit.md)!`)` Checks if the specified unit is supported. |
| open [Temporal](Temporal.md)! | [minus](Temporal.md))`(`amount:` ` [TemporalAmount](TemporalAmount.md)!`)` Returns an object of the same type as this object with an amount subtracted. |
| open [Temporal](Temporal.md)! | [minus](Temporal.md))`(`amountToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](TemporalUnit.md)!`)` Returns an object of the same type as this object with the specified period subtracted. |
| --- | --- |
| open [Temporal](Temporal.md)! | [plus](Temporal.md))`(`amount:` ` [TemporalAmount](TemporalAmount.md)!`)` Returns an object of the same type as this object with an amount added. |
| abstract [Temporal](Temporal.md)! | [plus](Temporal.md))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](TemporalUnit.md)!`)` Returns an object of the same type as this object with the specified period added. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](Temporal.md))`(`endExclusive:` ` [Temporal](Temporal.md)!`, `unit:` ` [TemporalUnit](TemporalUnit.md)!`)` Calculates the amount of time until another temporal in terms of the specified unit. |
| --- | --- |
| open [Temporal](Temporal.md)! | [with](Temporal.md))`(`adjuster:` ` [TemporalAdjuster](TemporalAdjuster.md)!`)` Returns an adjusted object of the same type as this object with the adjustment made. |
| abstract [Temporal](Temporal.md)! | [with](Temporal.md))`(`field:` ` [TemporalField](TemporalField.md)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns an object of the same type as this object with the specified field altered. |

| Inherited functions ||
|---|---|
| From class [TemporalAccessor](TemporalAccessor.md) |---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](TemporalAccessor.md))`(`field:` ` [TemporalField](TemporalField.md)!`)` <br /> Gets the value of the specified field as an`int`. This queries the date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](TemporalAccessor.md))`(`field:` ` [TemporalField](TemporalField.md)!`)` <br /> Gets the value of the specified field as a`long`. This queries the date-time for the value of the specified field. The returned value may be outside the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](TemporalAccessor.md))`(`field:` ` [TemporalField](TemporalField.md)!`)` <br /> Checks if the specified field is supported. This checks if the date-time can be queried for the specified field. If false, then calling the [range](TemporalAccessor.md))and [get](TemporalAccessor.md))methods will throw an exception. <br /> | | R | [query](TemporalAccessor.md))`(`query:` ` [TemporalQuery](TemporalQuery.md)<R>!`)` <br /> Queries this date-time. This queries this date-time using the specified query strategy object. Queries are a key tool for extracting information from date-times. They exists to externalize the process of querying, permitting different approaches, as per the strategy design pattern. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday. The most common query implementations are method references, such as`LocalDate::from`and`ZoneId::from`. Additional implementations are provided as static methods on [TemporalQuery](TemporalQuery.md). <br /> | | [ValueRange](ValueRange.md)! | [range](TemporalAccessor.md))`(`field:` ` [TemporalField](TemporalField.md)!`)` <br /> Gets the range of valid values for the specified field. All fields can be expressed as a`long`integer. This method returns an object that describes the valid range for that value. The value of this temporal object is used to enhance the accuracy of the returned range. If the date-time cannot return the range, because the field is unsupported or for some other reason, an exception will be thrown. Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field. <br /> | ||

## Public methods

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this date-time. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](Temporal.md))and [minus](Temporal.md))methods will throw an exception.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](TemporalUnit.md)!:the unit to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit can be added/subtracted, false if not |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun minus(amount: TemporalAmount!): Temporal!
```

Returns an object of the same type as this object with an amount subtracted.

This adjusts this temporal, subtracting according to the rules of the specified amount. The amount is typically a [java.time.Period](../java.time/Period.md) but may be any other type implementing the [TemporalAmount](TemporalAmount.md) interface, such as [java.time.Duration](../java.time/Duration.md).

Some example code indicating how and why this method is used: 

```kotlin
date = date.minus(period);               // subtract a Period instance
   date = date.minus(duration);             // subtract a Duration instance
   date = date.minus(workingDays(6));       // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](TemporalAmount.md)!:the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Temporal](Temporal.md)! | an object of the same type with the specified adjustment made, not null |

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
| `unit` | [TemporalUnit](TemporalUnit.md)!:the unit of the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Temporal](Temporal.md)! | an object of the same type with the specified period subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the unit cannot be subtracted |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun plus(amount: TemporalAmount!): Temporal!
```

Returns an object of the same type as this object with an amount added.

This adjusts this temporal, adding according to the rules of the specified amount. The amount is typically a [java.time.Period](../java.time/Period.md) but may be any other type implementing the [TemporalAmount](TemporalAmount.md) interface, such as [java.time.Duration](../java.time/Duration.md).

Some example code indicating how and why this method is used: 

```kotlin
date = date.plus(period);                // add a Period instance
   date = date.plus(duration);              // add a Duration instance
   date = date.plus(workingDays(6));        // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](TemporalAmount.md)!:the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Temporal](Temporal.md)! | an object of the same type with the specified adjustment made, not null |

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
| `unit` | [TemporalUnit](TemporalUnit.md)!:the unit of the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Temporal](Temporal.md)! | an object of the same type with the specified period added, not null |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if the unit cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

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

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [TemporalUnit.between(Temporal, Temporal)](TemporalUnit.md)): 

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
| `endExclusive` | [Temporal](Temporal.md)!:the end temporal, exclusive, converted to be of the same type as this object, not null |
| `unit` | [TemporalUnit](TemporalUnit.md)!:the unit to measure the amount in, not null |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between this temporal object and the specified one in terms of the unit; positive if the specified object is later than this one, negative if it is earlier than this one |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to the same type as this temporal |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun with(adjuster: TemporalAdjuster!): Temporal!
```

Returns an adjusted object of the same type as this object with the adjustment made.

This adjusts this date-time according to the rules of the specified adjuster. A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in [TemporalAdjusters](TemporalAdjusters.md). These include finding the "last day of the month" and "next Wednesday". The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

Some example code indicating how and why this method is used: 

```kotlin
date = date.with(Month.JULY);        // most key classes implement TemporalAdjuster
   date = date.with(lastDayOfMonth());  // static import from Adjusters
   date = date.with(next(WEDNESDAY));   // static import from Adjusters and DayOfWeek
  
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `adjuster` | [TemporalAdjuster](TemporalAdjuster.md)!:the adjuster to use, not null |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Temporal](Temporal.md)! | an object of the same type with the specified adjustment made, not null |

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
| `field` | [TemporalField](TemporalField.md)!:the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field in the result |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Temporal](Temporal.md)! | an object of the same type with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |
