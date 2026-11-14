# TemporalAccessor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalAccessor

```
interface TemporalAccessor
```

| [java.time.temporal.TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#) |

| Known Direct Subclasses [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#), [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era.html#), [Month](https://developer.android.com/reference/kotlin/java/time/Month.html#), [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay.html#), [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal), [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#) |-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#) | A day-of-week, such as 'Tuesday'. | | [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era.html#) | An era of the time-line. | | [Month](https://developer.android.com/reference/kotlin/java/time/Month.html#) | A month-of-year, such as 'July'. | | [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay.html#) | A month-day in the ISO-8601 calendar system, such as`--12-03`. | | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal) | Framework-level interface defining read-write access to a temporal object, such as a date, time, offset or some combination of these. | | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#) | A time-zone offset from Greenwich/UTC, such as`+02:00`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#), [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime.html#), [ChronoZonedDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime.html#), [DayOfWeek.FRIDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:FRIDAY), [DayOfWeek.MONDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:MONDAY), [DayOfWeek.SATURDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:SATURDAY), [DayOfWeek.SUNDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:SUNDAY), [DayOfWeek.THURSDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:THURSDAY), [DayOfWeek.TUESDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:TUESDAY), [DayOfWeek.WEDNESDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:WEDNESDAY), [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate.html#), [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate.html#), and 42 others. |----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#) | A date without time-of-day or time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime.html#) | A date-time without a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoZonedDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime.html#) | A date-time with a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [DayOfWeek.FRIDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:FRIDAY) | The singleton instance for the day-of-week of Friday. | | [DayOfWeek.MONDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:MONDAY) | The singleton instance for the day-of-week of Monday. | | [DayOfWeek.SATURDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:SATURDAY) | The singleton instance for the day-of-week of Saturday. | | [DayOfWeek.SUNDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:SUNDAY) | The singleton instance for the day-of-week of Sunday. | | [DayOfWeek.THURSDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:THURSDAY) | The singleton instance for the day-of-week of Thursday. | | [DayOfWeek.TUESDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:TUESDAY) | The singleton instance for the day-of-week of Tuesday. | | [DayOfWeek.WEDNESDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#ENUM_VALUE:WEDNESDAY) | The singleton instance for the day-of-week of Wednesday. | | [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate.html#) | A date in the Hijrah calendar system. | | [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate.html#) | A date in the Hijrah calendar system. | | [HijrahEra](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra.html#) | An era in the Hijrah calendar system. | | [HijrahEra.AH](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra.html#ENUM_VALUE:AH) | The singleton instance for the current era, 'Anno Hegirae', which has the numeric value 1. | | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | An instantaneous point on the time-line. | | [IsoEra](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra.html#) | An era in the ISO calendar system. | | [IsoEra.BCE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra.html#ENUM_VALUE:BCE) | The singleton instance for the era before the current one, 'Before Current Era', which has the numeric value 0. | | [IsoEra.CE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra.html#ENUM_VALUE:CE) | The singleton instance for the current era, 'Current Era', which has the numeric value 1. | | [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate.html#) | A date in the Japanese Imperial calendar system. | | [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate.html#) | A date in the Japanese Imperial calendar system. | | [JapaneseEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra.html#) | An era in the Japanese Imperial calendar system. | | [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#) | A time without a time-zone in the ISO-8601 calendar system, such as`10:15:30`. | | [MinguoDate](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoDate.html#) | A date in the Minguo calendar system. | | [MinguoDate](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoDate.html#) | A date in the Minguo calendar system. | | [MinguoEra](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra.html#) | An era in the Minguo calendar system. | | [MinguoEra.BEFORE_ROC](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra.html#ENUM_VALUE:BEFORE_ROC) | The singleton instance for the era before the current one, 'Before Republic of China Era', which has the numeric value 0. | | [MinguoEra.ROC](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra.html#ENUM_VALUE:ROC) | The singleton instance for the current era, 'Republic of China Era', which has the numeric value 1. | | [Month.APRIL](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:APRIL) | The singleton instance for the month of April with 30 days. | | [Month.AUGUST](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:AUGUST) | The singleton instance for the month of August with 31 days. | | [Month.DECEMBER](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:DECEMBER) | The singleton instance for the month of December with 31 days. | | [Month.FEBRUARY](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:FEBRUARY) | The singleton instance for the month of February with 28 days, or 29 in a leap year. | | [Month.JANUARY](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:JANUARY) | The singleton instance for the month of January with 31 days. | | [Month.JULY](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:JULY) | The singleton instance for the month of July with 31 days. | | [Month.JUNE](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:JUNE) | The singleton instance for the month of June with 30 days. | | [Month.MARCH](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:MARCH) | The singleton instance for the month of March with 31 days. | | [Month.MAY](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:MAY) | The singleton instance for the month of May with 31 days. | | [Month.NOVEMBER](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:NOVEMBER) | The singleton instance for the month of November with 30 days. | | [Month.OCTOBER](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:OCTOBER) | The singleton instance for the month of October with 31 days. | | [Month.SEPTEMBER](https://developer.android.com/reference/kotlin/java/time/Month.html#ENUM_VALUE:SEPTEMBER) | The singleton instance for the month of September with 30 days. | | [OffsetDateTime](https://developer.android.com/reference/kotlin/java/time/OffsetDateTime.html#) | A date-time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00`. | | [OffsetTime](https://developer.android.com/reference/kotlin/java/time/OffsetTime.html#) | A time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`10:15:30+01:00`. | | [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate.html#) | A date in the Thai Buddhist calendar system. | | [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate.html#) | A date in the Thai Buddhist calendar system. | | [ThaiBuddhistEra](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra.html#) | An era in the Thai Buddhist calendar system. | | [ThaiBuddhistEra.BE](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra.html#ENUM_VALUE:BE) | The singleton instance for the current era, 'Buddhist Era', which has the numeric value 1. | | [ThaiBuddhistEra.BEFORE_BE](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra.html#ENUM_VALUE:BEFORE_BE) | The singleton instance for the era before the current one, 'Before Buddhist Era', which has the numeric value 0. | | [Year](https://developer.android.com/reference/kotlin/java/time/Year.html#) | A year in the ISO-8601 calendar system, such as`2007`. | | [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth.html#) | A year-month in the ISO-8601 calendar system, such as`2007-12`. | | [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#) | A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`. | | [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#) | A date-time with a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00 Europe/Paris`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Framework-level interface defining read-only access to a temporal object, such as a date, time, offset or some combination of these.

This is the base interface type for date, time and offset objects. It is implemented by those classes that can provide information as [fields](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField) or [queries](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery).

Most date and time information can be represented as a number. These are modeled using`TemporalField`with the number held using a`long`to handle large values. Year, month and day-of-month are simple examples of fields, but they also include instant and offsets. See [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) for the standard set of fields.

Two pieces of date/time information cannot be represented by numbers, the [chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#) and the [time-zone](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#). These can be accessed via [queries](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#query(java.time.temporal.TemporalQuery))using the static methods defined on [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery).

A sub-interface, [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal), extends this definition to one that also supports adjustment and manipulation on more complete temporal objects.

This interface is a framework-level interface that should not be widely used in application code. Instead, applications should create and pass around instances of concrete types, such as`LocalDate`. There are many reasons for this, part of which is that implementations of this interface may be in calendar systems other than ISO. See [java.time.chrono.ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#) for a fuller discussion of the issues.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#get(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the value of the specified field as an`int`. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the value of the specified field as a`long`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Checks if the specified field is supported. |
| --- | --- |
| openR | [query](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)<R>!`)` Queries this date-time. |
| open [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | [range](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the range of valid values for the specified field. |

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
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to get, not null |

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

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if the date-time can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#range(java.time.temporal.TemporalField))and [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#get(java.time.temporal.TemporalField))methods will throw an exception.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to check, null returns false |

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

The most common query implementations are method references, such as`LocalDate::from`and`ZoneId::from`. Additional implementations are provided as static methods on [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\<R\>!:the query to invoke, not null |

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
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
