# TemporalAdjuster

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalAdjuster

```
@FunctionalInterface interface TemporalAdjuster
```

| [java.time.temporal.TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md) |

| Known Direct Subclasses [ChronoLocalDate](../java/time/chrono/ChronoLocalDate.md), [ChronoLocalDateTime](../java/time/chrono/ChronoLocalDateTime.md), [DayOfWeek](../java/time/DayOfWeek.md), [Era](../java/time/chrono/Era.md), [HijrahDate](../java/time/chrono/HijrahDate.md), [Instant](../java/time/Instant.md), [JapaneseDate](../java/time/chrono/JapaneseDate.md), [LocalDate](../java/time/LocalDate.md), [LocalDateTime](../java/time/LocalDateTime.md), [LocalTime](../java/time/LocalTime.md), [MinguoDate](../java/time/chrono/MinguoDate.md), [Month](../java/time/Month.md), and 7 others. |------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [ChronoLocalDate](../java/time/chrono/ChronoLocalDate.md) | A date without time-of-day or time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [ChronoLocalDateTime](../java/time/chrono/ChronoLocalDateTime.md) | A date-time without a time-zone in an arbitrary chronology, intended for advanced globalization use cases. | | [DayOfWeek](../java/time/DayOfWeek.md) | A day-of-week, such as 'Tuesday'. | | [Era](../java/time/chrono/Era.md) | An era of the time-line. | | [HijrahDate](../java/time/chrono/HijrahDate.md) | A date in the Hijrah calendar system. | | [Instant](../java/time/Instant.md) | An instantaneous point on the time-line. | | [JapaneseDate](../java/time/chrono/JapaneseDate.md) | A date in the Japanese Imperial calendar system. | | [LocalDate](../java/time/LocalDate.md) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDateTime](../java/time/LocalDateTime.md) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [LocalTime](../java/time/LocalTime.md) | A time without a time-zone in the ISO-8601 calendar system, such as`10:15:30`. | | [MinguoDate](../java/time/chrono/MinguoDate.md) | A date in the Minguo calendar system. | | [Month](../java/time/Month.md) | A month-of-year, such as 'July'. | | [MonthDay](../java/time/MonthDay.md) | A month-day in the ISO-8601 calendar system, such as`--12-03`. | | [OffsetDateTime](../java/time/OffsetDateTime.md) | A date-time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`2007-12-03T10:15:30+01:00`. | | [OffsetTime](../java/time/OffsetTime.md) | A time with an offset from UTC/Greenwich in the ISO-8601 calendar system, such as`10:15:30+01:00`. | | [ThaiBuddhistDate](../java/time/chrono/ThaiBuddhistDate.md) | A date in the Thai Buddhist calendar system. | | [Year](../java/time/Year.md) | A year in the ISO-8601 calendar system, such as`2007`. | | [YearMonth](../java/time/YearMonth.md) | A year-month in the ISO-8601 calendar system, such as`2007-12`. | | [ZoneOffset](../java/time/ZoneOffset.md) | A time-zone offset from Greenwich/UTC, such as`+02:00`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DayOfWeek.FRIDAY](../java/time/DayOfWeek.md), [DayOfWeek.MONDAY](../java/time/DayOfWeek.md), [DayOfWeek.SATURDAY](../java/time/DayOfWeek.md), [DayOfWeek.SUNDAY](../java/time/DayOfWeek.md), [DayOfWeek.THURSDAY](../java/time/DayOfWeek.md), [DayOfWeek.TUESDAY](../java/time/DayOfWeek.md), [DayOfWeek.WEDNESDAY](../java/time/DayOfWeek.md), [HijrahDate](../java/time/chrono/HijrahDate.md), [HijrahEra](../java/time/chrono/HijrahEra.md), [HijrahEra.AH](../java/time/chrono/HijrahEra.md), [IsoEra](../java/time/chrono/IsoEra.md), [IsoEra.BCE](../java/time/chrono/IsoEra.md), and 25 others. |----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [DayOfWeek.FRIDAY](../java/time/DayOfWeek.md) | The singleton instance for the day-of-week of Friday. | | [DayOfWeek.MONDAY](../java/time/DayOfWeek.md) | The singleton instance for the day-of-week of Monday. | | [DayOfWeek.SATURDAY](../java/time/DayOfWeek.md) | The singleton instance for the day-of-week of Saturday. | | [DayOfWeek.SUNDAY](../java/time/DayOfWeek.md) | The singleton instance for the day-of-week of Sunday. | | [DayOfWeek.THURSDAY](../java/time/DayOfWeek.md) | The singleton instance for the day-of-week of Thursday. | | [DayOfWeek.TUESDAY](../java/time/DayOfWeek.md) | The singleton instance for the day-of-week of Tuesday. | | [DayOfWeek.WEDNESDAY](../java/time/DayOfWeek.md) | The singleton instance for the day-of-week of Wednesday. | | [HijrahDate](../java/time/chrono/HijrahDate.md) | A date in the Hijrah calendar system. | | [HijrahEra](../java/time/chrono/HijrahEra.md) | An era in the Hijrah calendar system. | | [HijrahEra.AH](../java/time/chrono/HijrahEra.md) | The singleton instance for the current era, 'Anno Hegirae', which has the numeric value 1. | | [IsoEra](../java/time/chrono/IsoEra.md) | An era in the ISO calendar system. | | [IsoEra.BCE](../java/time/chrono/IsoEra.md) | The singleton instance for the era before the current one, 'Before Current Era', which has the numeric value 0. | | [IsoEra.CE](../java/time/chrono/IsoEra.md) | The singleton instance for the current era, 'Current Era', which has the numeric value 1. | | [JapaneseDate](../java/time/chrono/JapaneseDate.md) | A date in the Japanese Imperial calendar system. | | [JapaneseEra](../java/time/chrono/JapaneseEra.md) | An era in the Japanese Imperial calendar system. | | [LocalDate](../java/time/LocalDate.md) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [LocalDateTime](../java/time/LocalDateTime.md) | A date-time without a time-zone in the ISO-8601 calendar system, such as`2007-12-03T10:15:30`. | | [MinguoDate](../java/time/chrono/MinguoDate.md) | A date in the Minguo calendar system. | | [MinguoEra](../java/time/chrono/MinguoEra.md) | An era in the Minguo calendar system. | | [MinguoEra.BEFORE_ROC](../java/time/chrono/MinguoEra.md) | The singleton instance for the era before the current one, 'Before Republic of China Era', which has the numeric value 0. | | [MinguoEra.ROC](../java/time/chrono/MinguoEra.md) | The singleton instance for the current era, 'Republic of China Era', which has the numeric value 1. | | [Month.APRIL](../java/time/Month.md) | The singleton instance for the month of April with 30 days. | | [Month.AUGUST](../java/time/Month.md) | The singleton instance for the month of August with 31 days. | | [Month.DECEMBER](../java/time/Month.md) | The singleton instance for the month of December with 31 days. | | [Month.FEBRUARY](../java/time/Month.md) | The singleton instance for the month of February with 28 days, or 29 in a leap year. | | [Month.JANUARY](../java/time/Month.md) | The singleton instance for the month of January with 31 days. | | [Month.JULY](../java/time/Month.md) | The singleton instance for the month of July with 31 days. | | [Month.JUNE](../java/time/Month.md) | The singleton instance for the month of June with 30 days. | | [Month.MARCH](../java/time/Month.md) | The singleton instance for the month of March with 31 days. | | [Month.MAY](../java/time/Month.md) | The singleton instance for the month of May with 31 days. | | [Month.NOVEMBER](../java/time/Month.md) | The singleton instance for the month of November with 30 days. | | [Month.OCTOBER](../java/time/Month.md) | The singleton instance for the month of October with 31 days. | | [Month.SEPTEMBER](../java/time/Month.md) | The singleton instance for the month of September with 30 days. | | [ThaiBuddhistDate](../java/time/chrono/ThaiBuddhistDate.md) | A date in the Thai Buddhist calendar system. | | [ThaiBuddhistEra](../java/time/chrono/ThaiBuddhistEra.md) | An era in the Thai Buddhist calendar system. | | [ThaiBuddhistEra.BE](../java/time/chrono/ThaiBuddhistEra.md) | The singleton instance for the current era, 'Buddhist Era', which has the numeric value 1. | | [ThaiBuddhistEra.BEFORE_BE](../java/time/chrono/ThaiBuddhistEra.md) | The singleton instance for the era before the current one, 'Before Buddhist Era', which has the numeric value 0. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Strategy for adjusting a temporal object.

Adjusters are a key tool for modifying temporal objects. They exist to externalize the process of adjustment, permitting different approaches, as per the strategy design pattern. Examples might be an adjuster that sets the date avoiding weekends, or one that sets the date to the last day of the month.

There are two equivalent ways of using a`TemporalAdjuster`. The first is to invoke the method on this interface directly. The second is to use [Temporal.with(TemporalAdjuster)](../java/time/temporal/Temporal.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisAdjuster.adjustInto(temporal);
    temporal = temporal.with(thisAdjuster);
  
```
It is recommended to use the second approach,`with(TemporalAdjuster)`, as it is a lot clearer to read in code.

The [TemporalAdjusters](../java/time/temporal/TemporalAdjusters.md) class contains a standard set of adjusters, available as static methods. These include:

- finding the first or last day of the month
- finding the first day of next month
- finding the first or last day of the year
- finding the first day of next year
- finding the first or last day-of-week within a month, such as "first Wednesday in June"
- finding the next or previous day-of-week, such as "next Thursday"

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Temporal](../java/time/temporal/Temporal.md)! | [adjustInto](../java/time/temporal/TemporalAdjuster.md))`(`temporal:` ` [Temporal](../java/time/temporal/Temporal.md)!`)` Adjusts the specified temporal object. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object.

This adjusts the specified temporal object using the logic encapsulated in the implementing class. Examples might be an adjuster that sets the date avoiding weekends, or one that sets the date to the last day of the month.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [Temporal.with(TemporalAdjuster)](../java/time/temporal/Temporal.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisAdjuster.adjustInto(temporal);
    temporal = temporal.with(thisAdjuster);
  
```
It is recommended to use the second approach,`with(TemporalAdjuster)`, as it is a lot clearer to read in code.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java/time/temporal/Temporal.md)!:the temporal object to adjust, not null |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | an object of the same observable type with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
