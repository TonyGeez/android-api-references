# TemporalAccessor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalAccessor

```
interface TemporalAccessor
```

| [java.time.temporal.TemporalAccessor](TemporalAccessor.md) |

| Known Direct Subclasses [DayOfWeek](../java.time/DayOfWeek.md), [Era](../java.time.chrono/Era.md), [Month](../java.time/Month.md), [MonthDay](../java.time/MonthDay.md), [Temporal](Temporal.md), [ZoneOffset](../java.time/ZoneOffset.md) |-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [DayOfWeek](../java.time/DayOfWeek.md) | A day-of-week, such as 'Tuesday'. | | [Era](../java.time.chrono/Era.md) | An era of the time-line. | | [Month](../java.time/Month.md) | A month-of-year, such as 'July'. | | [MonthDay](../java.time/MonthDay.md) | A month-day in the ISO-8601 calendar system, such as`--12-03`. | | [Temporal](Temporal.md) | Framework-level interface defining read-write access to a temporal object, such as a date, time, offset or some combination of these. | | [ZoneOffset](../java.time/ZoneOffset.md) | A time-zone offset from Greenwich/UTC, such as`+02:00`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md), [ChronoLocalDateTime](../java.time.chrono/ChronoLocalDateTime.md), [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md), [DayOfWeek.FRIDAY](../java.time/DayOfWeek.md), [DayOfWeek.MONDAY](../java.time/DayOfWeek.md), [DayOfWeek.SATURDAY](../java.time/DayOfWeek.md), [DayOfWeek.SUNDAY](../java.time/DayOfWeek.md), [DayOfWeek.THURSDAY](../java.time/DayOfWeek.md), [DayOfWeek.TUESDAY](../java.time/DayOfWeek.md), [DayOfWeek.WEDNESDAY](../java.time/DayOfWeek.md), [HijrahDate](../java.time.chrono/HijrahDate.md), [HijrahDate](../java.time.chrono/HijrahDate.md), and 42 others. |----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md) | A date without time-of-day or time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoLocalDateTime](../java.time.chrono/ChronoLocalDateTime.md) | A date-time without a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoZonedDateTime](../java.time.chrono/ChronoZonedDateTime.md) | A date-time with a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [DayOfWeek.FRIDAY](../java.time/DayOfWeek.md) | The singleton instance for the day-of-week of Friday. | | [DayOfWeek.MONDAY](../java.time/DayOfWeek.md) | The singleton instance for the day-of-week of Monday. | | [DayOfWeek.SATURDAY](../java.time/DayOfWeek.md) | The singleton instance for the day-of-week of Saturday. | | [DayOfWeek.SUNDAY](../java.time/DayOfWeek.md) | The singleton instance for the day-of-week of Sunday. | | [DayOfWeek.THURSDAY](../java.time/DayOfWeek.md) | The singleton instance for the day-of-week of Thursday. | | [DayOfWeek.TUESDAY](../java.time/DayOfWeek.md) | The singleton instance for the day-of-week of Tuesday. | | [DayOfWeek.WEDNESDAY](../java.time/DayOfWeek.md) | The singleton instance for the day-of-week of Wednesday. | | [HijrahDate](../java.time.chrono/HijrahDate.md) | A date in the Hijrah calendar system. | | [HijrahDate](../java.time.chrono/HijrahDate.md) | A date in the Hijrah calendar system. | | [HijrahEra](../java.time.chrono/HijrahEra.md) | An era in the Hijrah calendar system. | | [HijrahEra.AH](../java.time.chrono/HijrahEra.md) | The singleton instance for the current era, 'Anno Hegirae', which has the numeric value 1. | | [Instant](../java.time/Instant.md) | An instantaneous point on the time-line. | | [IsoEra](../java.time.chrono/IsoEra.md) | An era in the ISO calendar system. | | [IsoEra.BCE](../java.time.chrono/IsoEra.md) | The singleton instance for the era before the current one, 'Before Current Era', which has the numeric value 0. | | [IsoEra.CE](../java.time.chrono/IsoEra.md) | The singleton instance for the current era, 'Current Era', which has the numeric value 1. | | [JapaneseDate](../java.time.chrono/JapaneseDate.md) | A date in the Japanese Imperial calendar system. | | [JapaneseDate](../java.time.chrono/JapaneseDate.md) | A date in the Japanese Imperial calendar system. | | [JapaneseEra](../java.time.chrono/JapaneseEra.md) | An era in the Japanese Imperial calendar system. | | [LocalDate](../java.time/LocalDate.md) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDate](../java.time/LocalDate.md) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDateTime](../java.time/LocalDateTime.md) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [LocalDateTime](../java.time/LocalDateTime.md) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [LocalTime](../java.time/LocalTime.md) | A time without a time-zone in the ISO-8601 calendar system, such as`10:15:30`. | | [MinguoDate](../java.time.chrono/MinguoDate.md) | A date in the Minguo calendar system. | | [MinguoDate](../java.time.chrono/MinguoDate.md) | A date in the Minguo calendar system. | | [MinguoEra](../java.time.chrono/MinguoEra.md) | An era in the Minguo calendar system. | | [MinguoEra.BEFORE_ROC](../java.time.chrono/MinguoEra.md) | The singleton instance for the era before the current one, 'Before Republic of China Era', which has the numeric value 0. | | [MinguoEra.ROC](../java.time.chrono/MinguoEra.md) | The singleton instance for the current era, 'Republic of China Era', which has the numeric value 1. | | [Month.APRIL](../java.time/Month.md) | The singleton instance for the month of April with 30 days. | | [Month.AUGUST](../java.time/Month.md) | The singleton instance for the month of August with 31 days. | | [Month.DECEMBER](../java.time/Month.md) | The singleton instance for the month of December with 31 days. | | [Month.FEBRUARY](../java.time/Month.md) | The singleton instance for the month of February with 28 days, or 29 in a leap year. | | [Month.JANUARY](../java.time/Month.md) | The singleton instance for the month of January with 31 days. | | [Month.JULY](../java.time/Month.md) | The singleton instance for the month of July with 31 days. | | [Month.JUNE](../java.time/Month.md) | The singleton instance for the month of June with 30 days. | | [Month.MARCH](../java.time/Month.md) | The singleton instance for the month of March with 31 days. | | [Month.MAY](../java.time/Month.md) | The singleton instance for the month of May with 31 days. | | [Month.NOVEMBER](../java.time/Month.md) | The singleton instance for the month of November with 30 days. | | [Month.OCTOBER](../java.time/Month.md) | The singleton instance for the month of October with 31 days. | | [Month.SEPTEMBER](../java.time/Month.md) | The singleton instance for the month of September with 30 days. | | [OffsetDateTime](../java.time/OffsetDateTime.md) | A date-time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00`. | | [OffsetTime](../java.time/OffsetTime.md) | A time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`10:15:30+01:00`. | | [ThaiBuddhistDate](../java.time.chrono/ThaiBuddhistDate.md) | A date in the Thai Buddhist calendar system. | | [ThaiBuddhistDate](../java.time.chrono/ThaiBuddhistDate.md) | A date in the Thai Buddhist calendar system. | | [ThaiBuddhistEra](../java.time.chrono/ThaiBuddhistEra.md) | An era in the Thai Buddhist calendar system. | | [ThaiBuddhistEra.BE](../java.time.chrono/ThaiBuddhistEra.md) | The singleton instance for the current era, 'Buddhist Era', which has the numeric value 1. | | [ThaiBuddhistEra.BEFORE_BE](../java.time.chrono/ThaiBuddhistEra.md) | The singleton instance for the era before the current one, 'Before Buddhist Era', which has the numeric value 0. | | [Year](../java.time/Year.md) | A year in the ISO-8601 calendar system, such as`2007`. | | [YearMonth](../java.time/YearMonth.md) | A year-month in the ISO-8601 calendar system, such as`2007-12`. | | [ZonedDateTime](../java.time/ZonedDateTime.md) | A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`. | | [ZonedDateTime](../java.time/ZonedDateTime.md) | A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Framework-level interface defining read-only access to a temporal object, such as a date, time, offset or some combination of these.

This is the base interface type for date, time and offset objects. It is implemented by those classes that can provide information as [fields](TemporalField.md) or [queries](TemporalQuery.md).

Most date and time information can be represented as a number. These are modeled using`TemporalField`with the number held using a`long`to handle large values. Year, month and day-of-month are simple examples of fields, but they also include instant and offsets. See [ChronoField](ChronoField.md) for the standard set of fields.

Two pieces of date/time information cannot be represented by numbers, the [chronology](../java.time.chrono/Chronology.md) and the [time-zone](../java.time/ZoneId.md). These can be accessed via [queries](TemporalAccessor.md))using the static methods defined on [TemporalQuery](TemporalQuery.md).

A sub-interface, [Temporal](Temporal.md), extends this definition to one that also supports adjustment and manipulation on more complete temporal objects.

This interface is a framework-level interface that should not be widely used in application code. Instead, applications should create and pass around instances of concrete types, such as`LocalDate`. There are many reasons for this, part of which is that implementations of this interface may be in calendar systems other than ISO. See [java.time.chrono.ChronoLocalDate](../java.time.chrono/ChronoLocalDate.md) for a fuller discussion of the issues.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](TemporalAccessor.md))`(`field:` ` [TemporalField](TemporalField.md)!`)` Gets the value of the specified field as an`int`. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](TemporalAccessor.md))`(`field:` ` [TemporalField](TemporalField.md)!`)` Gets the value of the specified field as a`long`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](TemporalAccessor.md))`(`field:` ` [TemporalField](TemporalField.md)!`)` Checks if the specified field is supported. |
| --- | --- |
| openR | [query](TemporalAccessor.md))`(`query:` ` [TemporalQuery](TemporalQuery.md)<R>!`)` Queries this date-time. |
| open [ValueRange](ValueRange.md)! | [range](TemporalAccessor.md))`(`field:` ` [TemporalField](TemporalField.md)!`)` Gets the range of valid values for the specified field. |

## Public methods

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(field: TemporalField!): Int
```

Gets the value of the specified field as an`int`.

This queries the date-time for the value of the specified field. The returned value will always be within the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](TemporalField.md)!:the field to get, not null |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value for the field, within the valid range of values |

| Exceptions ||
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an`int` |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field as a`long`.

This queries the date-time for the value of the specified field. The returned value may be outside the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](TemporalField.md)!:the field to get, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if the date-time can be queried for the specified field. If false, then calling the [range](TemporalAccessor.md))and [get](TemporalAccessor.md))methods will throw an exception.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](TemporalField.md)!:the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this date-time can be queried for the field, false if not |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this date-time.

This queries this date-time using the specified query strategy object.

Queries are a key tool for extracting information from date-times. They exists to externalize the process of querying, permitting different approaches, as per the strategy design pattern. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday.

The most common query implementations are method references, such as`LocalDate::from`and`ZoneId::from`. Additional implementations are provided as static methods on [TemporalQuery](TemporalQuery.md).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](TemporalQuery.md)\<R\>!:the query to invoke, not null |

| Return ||
|---|---------------------------------------------------------------|
| R | the query result, null may be returned (defined by the query) |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to query |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

All fields can be expressed as a`long`integer. This method returns an object that describes the valid range for that value. The value of this temporal object is used to enhance the accuracy of the returned range. If the date-time cannot return the range, because the field is unsupported or for some other reason, an exception will be thrown.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](TemporalField.md)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](ValueRange.md)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
