# java.time.temporal

# java.time.temporal

## Interfaces

| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal) | Framework-level interface defining read-write access to a temporal object, such as a date, time, offset or some combination of these. |
| --- | --- |
| [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor) | Framework-level interface defining read-only access to a temporal object, such as a date, time, offset or some combination of these. |
| [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster) | Strategy for adjusting a temporal object. |
| [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount) | Framework-level interface defining an amount of time, such as "6 hours", "8 days" or "2 years and 3 months". |
| --- | --- |
| [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField) | A field of date-time, such as month-of-year or minute-of-hour. |
| [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery) | Strategy for querying a temporal object. |
| [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit) | A unit of date-time, such as Days or Hours. |
| --- | --- |

## Classes

| [IsoFields](https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields) | Fields and units specific to the ISO-8601 calendar system, including quarter-of-year and week-based-year. |
| --- | --- |
| [JulianFields](https://developer.android.com/reference/kotlin/java/time/temporal/JulianFields) | A set of date fields that provide access to Julian Days. |
| [TemporalAdjusters](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjusters) | Common and useful TemporalAdjusters. |
| [TemporalQueries](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries) | Common implementations of`TemporalQuery`. |
| --- | --- |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange) | The range of valid values for a date-time field. |
| [WeekFields](https://developer.android.com/reference/kotlin/java/time/temporal/WeekFields) | Localized definitions of the day-of-week, week-of-month and week-of-year fields. |

## Exceptions

| [UnsupportedTemporalTypeException](https://developer.android.com/reference/kotlin/java/time/temporal/UnsupportedTemporalTypeException) | UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class. |
| --- | --- |

## Enums

| [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) | A standard set of fields. |
| --- | --- |
| [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit) | A standard set of date periods units. |
