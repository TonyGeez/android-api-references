# java.time.temporal

# java.time.temporal

## Interfaces

| [Temporal](../java/time/temporal/Temporal.md) | Framework-level interface defining read-write access to a temporal object, such as a date, time, offset or some combination of these. |
| --- | --- |
| [TemporalAccessor](../java/time/temporal/TemporalAccessor.md) | Framework-level interface defining read-only access to a temporal object, such as a date, time, offset or some combination of these. |
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md) | Strategy for adjusting a temporal object. |
| [TemporalAmount](../java/time/temporal/TemporalAmount.md) | Framework-level interface defining an amount of time, such as "6 hours", "8 days" or "2 years and 3 months". |
| --- | --- |
| [TemporalField](../java/time/temporal/TemporalField.md) | A field of date-time, such as month-of-year or minute-of-hour. |
| [TemporalQuery](../java/time/temporal/TemporalQuery.md) | Strategy for querying a temporal object. |
| [TemporalUnit](../java/time/temporal/TemporalUnit.md) | A unit of date-time, such as Days or Hours. |
| --- | --- |

## Classes

| [IsoFields](../java/time/temporal/IsoFields.md) | Fields and units specific to the ISO-8601 calendar system, including quarter-of-year and week-based-year. |
| --- | --- |
| [JulianFields](../java/time/temporal/JulianFields.md) | A set of date fields that provide access to Julian Days. |
| [TemporalAdjusters](../java/time/temporal/TemporalAdjusters.md) | Common and useful TemporalAdjusters. |
| [TemporalQueries](../java/time/temporal/TemporalQueries.md) | Common implementations of`TemporalQuery`. |
| --- | --- |
| [ValueRange](../java/time/temporal/ValueRange.md) | The range of valid values for a date-time field. |
| [WeekFields](../java/time/temporal/WeekFields.md) | Localized definitions of the day-of-week, week-of-month and week-of-year fields. |

## Exceptions

| [UnsupportedTemporalTypeException](../java/time/temporal/UnsupportedTemporalTypeException.md) | UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class. |
| --- | --- |

## Enums

| [ChronoField](../java/time/temporal/ChronoField.md) | A standard set of fields. |
| --- | --- |
| [ChronoUnit](../java/time/temporal/ChronoUnit.md) | A standard set of date periods units. |
