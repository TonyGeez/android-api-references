# java.time.temporal

# java.time.temporal

## Interfaces

| [Temporal](Temporal.md) | Framework-level interface defining read-write access to a temporal object, such as a date, time, offset or some combination of these. |
| --- | --- |
| [TemporalAccessor](TemporalAccessor.md) | Framework-level interface defining read-only access to a temporal object, such as a date, time, offset or some combination of these. |
| [TemporalAdjuster](TemporalAdjuster.md) | Strategy for adjusting a temporal object. |
| [TemporalAmount](TemporalAmount.md) | Framework-level interface defining an amount of time, such as "6 hours", "8 days" or "2 years and 3 months". |
| --- | --- |
| [TemporalField](TemporalField.md) | A field of date-time, such as month-of-year or minute-of-hour. |
| [TemporalQuery](TemporalQuery.md) | Strategy for querying a temporal object. |
| [TemporalUnit](TemporalUnit.md) | A unit of date-time, such as Days or Hours. |
| --- | --- |

## Classes

| [IsoFields](IsoFields.md) | Fields and units specific to the ISO-8601 calendar system, including quarter-of-year and week-based-year. |
| --- | --- |
| [JulianFields](JulianFields.md) | A set of date fields that provide access to Julian Days. |
| [TemporalAdjusters](TemporalAdjusters.md) | Common and useful TemporalAdjusters. |
| [TemporalQueries](TemporalQueries.md) | Common implementations of`TemporalQuery`. |
| --- | --- |
| [ValueRange](ValueRange.md) | The range of valid values for a date-time field. |
| [WeekFields](WeekFields.md) | Localized definitions of the day-of-week, week-of-month and week-of-year fields. |

## Exceptions

| [UnsupportedTemporalTypeException](UnsupportedTemporalTypeException.md) | UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class. |
| --- | --- |

## Enums

| [ChronoField](ChronoField.md) | A standard set of fields. |
| --- | --- |
| [ChronoUnit](ChronoUnit.md) | A standard set of date periods units. |
