Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChronoField

```
class ChronoField : TemporalField
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.temporal.ChronoField](ChronoField.md)\> ||
| | ↳ | [java.time.temporal.ChronoField](ChronoField.md) |

Known Direct Subclasses [ChronoField.ALIGNED_DAY_OF_WEEK_IN_MONTH](ChronoField.md), [ChronoField.ALIGNED_DAY_OF_WEEK_IN_YEAR](ChronoField.md), [ChronoField.ALIGNED_WEEK_OF_MONTH](ChronoField.md), [ChronoField.ALIGNED_WEEK_OF_YEAR](ChronoField.md), [ChronoField.AMPM_OF_DAY](ChronoField.md), [ChronoField.CLOCK_HOUR_OF_AMPM](ChronoField.md), [ChronoField.CLOCK_HOUR_OF_DAY](ChronoField.md), [ChronoField.DAY_OF_MONTH](ChronoField.md), [ChronoField.DAY_OF_WEEK](ChronoField.md), [ChronoField.DAY_OF_YEAR](ChronoField.md), [ChronoField.EPOCH_DAY](ChronoField.md), [ChronoField.ERA](ChronoField.md), and 18 others. [ChronoField.ALIGNED_DAY_OF_WEEK_IN_MONTH](ChronoField.md) The aligned day-of-week within a month.
[ChronoField.ALIGNED_DAY_OF_WEEK_IN_YEAR](ChronoField.md) The aligned day-of-week within a year.
[ChronoField.ALIGNED_WEEK_OF_MONTH](ChronoField.md) The aligned week within a month.
[ChronoField.ALIGNED_WEEK_OF_YEAR](ChronoField.md) The aligned week within a year.
[ChronoField.AMPM_OF_DAY](ChronoField.md) The am-pm-of-day.
[ChronoField.CLOCK_HOUR_OF_AMPM](ChronoField.md) The clock-hour-of-am-pm.
[ChronoField.CLOCK_HOUR_OF_DAY](ChronoField.md) The clock-hour-of-day.
[ChronoField.DAY_OF_MONTH](ChronoField.md) The day-of-month.
[ChronoField.DAY_OF_WEEK](ChronoField.md) The day-of-week, such as Tuesday.
[ChronoField.DAY_OF_YEAR](ChronoField.md) The day-of-year.
[ChronoField.EPOCH_DAY](ChronoField.md) The epoch-day, based on the Java epoch of 1970-01-01 (ISO).
[ChronoField.ERA](ChronoField.md) The era.
[ChronoField.HOUR_OF_AMPM](ChronoField.md) The hour-of-am-pm.
[ChronoField.HOUR_OF_DAY](ChronoField.md) The hour-of-day.
[ChronoField.INSTANT_SECONDS](ChronoField.md) The instant epoch-seconds.
[ChronoField.MICRO_OF_DAY](ChronoField.md) The micro-of-day.
[ChronoField.MICRO_OF_SECOND](ChronoField.md) The micro-of-second.
[ChronoField.MILLI_OF_DAY](ChronoField.md) The milli-of-day.
[ChronoField.MILLI_OF_SECOND](ChronoField.md) The milli-of-second.
[ChronoField.MINUTE_OF_DAY](ChronoField.md) The minute-of-day.
[ChronoField.MINUTE_OF_HOUR](ChronoField.md) The minute-of-hour.
[ChronoField.MONTH_OF_YEAR](ChronoField.md) The month-of-year, such as March.
[ChronoField.NANO_OF_DAY](ChronoField.md) The nano-of-day.
[ChronoField.NANO_OF_SECOND](ChronoField.md) The nano-of-second.
[ChronoField.OFFSET_SECONDS](ChronoField.md) The offset from UTC/Greenwich.
[ChronoField.PROLEPTIC_MONTH](ChronoField.md) The proleptic-month based, counting months sequentially from year 0.
[ChronoField.SECOND_OF_DAY](ChronoField.md) The second-of-day.
[ChronoField.SECOND_OF_MINUTE](ChronoField.md) The second-of-minute.
[ChronoField.YEAR](ChronoField.md) The proleptic year, such as 2012.
[ChronoField.YEAR_OF_ERA](ChronoField.md) The year within the era.

A standard set of fields.

This set of fields provide field-based access to manipulate a date, time or date-time. The standard set of fields can be extended by implementing `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField`.

These fields are intended to be applicable in multiple calendar systems. For example, most non-ISO calendar systems define dates as a year, month and day, just with slightly different rules. The documentation of each field explains how it operates.

## Summary

| Enum values ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:ALIGNED_DAY_OF_WEEK_IN_MONTH` The aligned day-of-week within a month. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:ALIGNED_DAY_OF_WEEK_IN_YEAR` The aligned day-of-week within a year. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:ALIGNED_WEEK_OF_MONTH` The aligned week within a month. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:ALIGNED_WEEK_OF_YEAR` The aligned week within a year. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:AMPM_OF_DAY` The am-pm-of-day. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:CLOCK_HOUR_OF_AMPM` The clock-hour-of-am-pm. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:CLOCK_HOUR_OF_DAY` The clock-hour-of-day. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:DAY_OF_MONTH` The day-of-month. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:DAY_OF_WEEK` The day-of-week, such as Tuesday. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:DAY_OF_YEAR` The day-of-year. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:EPOCH_DAY` The epoch-day, based on the Java epoch of 1970-01-01 (ISO). |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:ERA` The era. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:HOUR_OF_AMPM` The hour-of-am-pm. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:HOUR_OF_DAY` The hour-of-day. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:INSTANT_SECONDS` The instant epoch-seconds. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:MICRO_OF_DAY` The micro-of-day. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:MICRO_OF_SECOND` The micro-of-second. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:MILLI_OF_DAY` The milli-of-day. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:MILLI_OF_SECOND` The milli-of-second. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:MINUTE_OF_DAY` The minute-of-day. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:MINUTE_OF_HOUR` The minute-of-hour. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:MONTH_OF_YEAR` The month-of-year, such as March. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:NANO_OF_DAY` The nano-of-day. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:NANO_OF_SECOND` The nano-of-second. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:OFFSET_SECONDS` The offset from UTC/Greenwich. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:PROLEPTIC_MONTH` The proleptic-month based, counting months sequentially from year 0. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:SECOND_OF_DAY` The second-of-day. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:SECOND_OF_MINUTE` The second-of-minute. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:YEAR` The proleptic year, such as 2012. |
| `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#ENUM_VALUE:YEAR_OF_ERA` The year within the era. |

| Public methods ||
|---|---|
| R | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#adjustInto(java.time.temporal.ChronoField.adjustInto.R,%20kotlin.Long)(temporal: R, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of the specified temporal object with the value of this field set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#checkValidIntValue(kotlin.Long)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Checks that the specified value is valid and fits in an `int`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#checkValidValue(kotlin.Long)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Checks that the specified value is valid for this field. |
| --- | --- |
| [TemporalUnit](TemporalUnit.md)! | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#getBaseUnit()()` Gets the unit that the field is measured in. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#getDisplayName(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Gets the display name for the field in the requested locale. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#getFrom(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Gets the value of this field from the specified temporal object. |
| --- | --- |
| [TemporalUnit](TemporalUnit.md)! | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#getRangeUnit()()` Gets the range that the field is bound by. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#isDateBased()()` Checks if this field represents a component of a date. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#isSupportedBy(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Checks if this field is supported by the temporal object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#isTimeBased()()` Checks if this field represents a component of a time. |
| [ValueRange](ValueRange.md)! | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#range()()` Gets the range of valid values for the field. |
| [ValueRange](ValueRange.md)! | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#rangeRefinedBy(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Get the range of valid values for this field using the temporal object to refine the result. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#toString()()` Returns the name of this enum constant, as contained in the declaration. |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField` `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!` `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField#resolve(kotlin.collections.MutableMap,%20java.time.temporal.TemporalAccessor,%20java.time.format.ResolverStyle)(fieldValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>!, partialTemporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!, resolverStyle: https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle.html#!)`

<br />

Resolves this field to provide a simpler alternative or a date.

This method is invoked during the resolve phase of parsing. It is designed to allow application defined fields to be simplified into more standard fields, such as those on `ChronoField`, or into a date.

Applications should not normally invoke this method directly.

<br />

## Enum values

### ALIGNED_DAY_OF_WEEK_IN_MONTH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val ALIGNED_DAY_OF_WEEK_IN_MONTH : ChronoField
```

The aligned day-of-week within a month.

This represents concept of the count of days within the period of a week where the weeks are aligned to the start of the month. This field is typically used with `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`.

For example, in a calendar systems with a seven day week, the first aligned-week-of-month starts on day-of-month 1, the second aligned-week starts on day-of-month 8, and so on. Within each of these aligned-weeks, the days are numbered from 1 to 7 and returned as the value of this field. As such, day-of-month 1 to 7 will have aligned-day-of-week values from 1 to 7. And day-of-month 8 to 14 will repeat this with aligned-day-of-week values from 1 to 7.

Calendar systems that do not have a seven day week should typically implement this field in the same way, but using the alternate week length.

### ALIGNED_DAY_OF_WEEK_IN_YEAR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val ALIGNED_DAY_OF_WEEK_IN_YEAR : ChronoField
```

The aligned day-of-week within a year.

This represents concept of the count of days within the period of a week where the weeks are aligned to the start of the year. This field is typically used with `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`.

For example, in a calendar systems with a seven day week, the first aligned-week-of-year starts on day-of-year 1, the second aligned-week starts on day-of-year 8, and so on. Within each of these aligned-weeks, the days are numbered from 1 to 7 and returned as the value of this field. As such, day-of-year 1 to 7 will have aligned-day-of-week values from 1 to 7. And day-of-year 8 to 14 will repeat this with aligned-day-of-week values from 1 to 7.

Calendar systems that do not have a seven day week should typically implement this field in the same way, but using the alternate week length.

### ALIGNED_WEEK_OF_MONTH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val ALIGNED_WEEK_OF_MONTH : ChronoField
```

The aligned week within a month.

This represents concept of the count of weeks within the period of a month where the weeks are aligned to the start of the month. This field is typically used with `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`.

For example, in a calendar systems with a seven day week, the first aligned-week-of-month starts on day-of-month 1, the second aligned-week starts on day-of-month 8, and so on. Thus, day-of-month values 1 to 7 are in aligned-week 1, while day-of-month values 8 to 14 are in aligned-week 2, and so on.

Calendar systems that do not have a seven day week should typically implement this field in the same way, but using the alternate week length.

### ALIGNED_WEEK_OF_YEAR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val ALIGNED_WEEK_OF_YEAR : ChronoField
```

The aligned week within a year.

This represents concept of the count of weeks within the period of a year where the weeks are aligned to the start of the year. This field is typically used with `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`.

For example, in a calendar systems with a seven day week, the first aligned-week-of-year starts on day-of-year 1, the second aligned-week starts on day-of-year 8, and so on. Thus, day-of-year values 1 to 7 are in aligned-week 1, while day-of-year values 8 to 14 are in aligned-week 2, and so on.

Calendar systems that do not have a seven day week should typically implement this field in the same way, but using the alternate week length.

### AMPM_OF_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val AMPM_OF_DAY : ChronoField
```

The am-pm-of-day.

This counts the AM/PM within the day, from 0 (AM) to 1 (PM). This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated from 0 to 1 in strict and smart mode. In lenient mode the value is not validated. It is combined with `HOUR_OF_AMPM` (if not present, it defaults to '6') to form `HOUR_OF_DAY` by multiplying the `AMPM_OF_DAY` value by 12.

### CLOCK_HOUR_OF_AMPM

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val CLOCK_HOUR_OF_AMPM : ChronoField
```

The clock-hour-of-am-pm.

This counts the hour within the AM/PM, from 1 to 12. This is the hour that would be observed on a standard 12-hour analog wall clock. This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated from 1 to 12 in strict mode and from 0 to 12 in smart mode. In lenient mode the value is not validated. The field is converted to an `HOUR_OF_AMPM` with the same value, unless the value is 12, in which case it is converted to 0.

See `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` for the related field that counts hours from 0 to 11.

### CLOCK_HOUR_OF_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val CLOCK_HOUR_OF_DAY : ChronoField
```

The clock-hour-of-day.

This counts the hour within the day, from 1 to 24. This is the hour that would be observed on a 24-hour analog wall clock. This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated from 1 to 24 in strict mode and from 0 to 24 in smart mode. In lenient mode the value is not validated. The field is converted to an `HOUR_OF_DAY` with the same value, unless the value is 24, in which case it is converted to 0.

See `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` for the related field that counts hours from 0 to 23.

### DAY_OF_MONTH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val DAY_OF_MONTH : ChronoField
```

The day-of-month.

This represents the concept of the day within the month. In the default ISO calendar system, this has values from 1 to 31 in most months. April, June, September, November have days from 1 to 30, while February has days from 1 to 28, or 29 in a leap year.

Non-ISO calendar systems should implement this field using the most recognized day-of-month values for users of the calendar system. Normally, this is a count of days from 1 to the length of the month.

### DAY_OF_WEEK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val DAY_OF_WEEK : ChronoField
```

The day-of-week, such as Tuesday.

This represents the standard concept of the day of the week. In the default ISO calendar system, this has values from Monday (1) to Sunday (7). The `https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#` class can be used to interpret the result.

Most non-ISO calendar systems also define a seven day week that aligns with ISO. Those calendar systems must also use the same numbering system, from Monday (1) to Sunday (7), which allows `DayOfWeek` to be used.

Calendar systems that do not have a standard seven day week should implement this field if they have a similar concept of named or numbered days within a period similar to a week. It is recommended that the numbering starts from 1.

### DAY_OF_YEAR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val DAY_OF_YEAR : ChronoField
```

The day-of-year.

This represents the concept of the day within the year. In the default ISO calendar system, this has values from 1 to 365 in standard years and 1 to 366 in leap years.

Non-ISO calendar systems should implement this field using the most recognized day-of-year values for users of the calendar system. Normally, this is a count of days from 1 to the length of the year.

Note that a non-ISO calendar system may have year numbering system that changes at a different point to the natural reset in the month numbering. An example of this is the Japanese calendar system where a change of era, which resets the year number to 1, can happen on any date. The era and year reset also cause the day-of-year to be reset to 1, but not the month-of-year or day-of-month.

### EPOCH_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val EPOCH_DAY : ChronoField
```

The epoch-day, based on the Java epoch of 1970-01-01 (ISO).

This field is the sequential count of days where 1970-01-01 (ISO) is zero. Note that this uses the *local* time-line, ignoring offset and time-zone.

This field is strictly defined to have the same meaning in all calendar systems. This is necessary to ensure interoperation between calendars.

Range of EpochDay is between (LocalDate.MIN.toEpochDay(), LocalDate.MAX.toEpochDay()) both inclusive.

### ERA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val ERA : ChronoField
```

The era.

This represents the concept of the era, which is the largest division of the time-line. This field is typically used with `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`.

In the default ISO calendar system, there are two eras defined, 'BCE' and 'CE'. The era 'CE' is the one currently in use and year-of-era runs from 1 to the maximum value. The era 'BCE' is the previous era, and the year-of-era runs backwards. See `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` for a full example.

Non-ISO calendar systems should implement this field to define eras. The value of the era that was active on 1970-01-01 (ISO) must be assigned the value 1. Earlier eras must have sequentially smaller values. Later eras must have sequentially larger values,

### HOUR_OF_AMPM

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val HOUR_OF_AMPM : ChronoField
```

The hour-of-am-pm.

This counts the hour within the AM/PM, from 0 to 11. This is the hour that would be observed on a standard 12-hour digital clock. This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated from 0 to 11 in strict and smart mode. In lenient mode the value is not validated. It is combined with `AMPM_OF_DAY` to form `HOUR_OF_DAY` by multiplying the `AMPM_OF_DAY` value by 12.

See `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` for the related field that counts hours from 1 to 12.

### HOUR_OF_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val HOUR_OF_DAY : ChronoField
```

The hour-of-day.

This counts the hour within the day, from 0 to 23. This is the hour that would be observed on a standard 24-hour digital clock. This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The field is combined with `MINUTE_OF_HOUR`, `SECOND_OF_MINUTE` and `NANO_OF_SECOND` to produce a `LocalTime`. In lenient mode, any excess days are added to the parsed date, or made available via `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#parsedExcessDays()`.

See `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` for the related field that counts hours from 1 to 24.

### INSTANT_SECONDS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val INSTANT_SECONDS : ChronoField
```

The instant epoch-seconds.

This represents the concept of the sequential count of seconds where 1970-01-01T00:00Z (ISO) is zero. This field may be used with `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` to represent the fraction of the second.

An `https://developer.android.com/reference/kotlin/java/time/Instant.html#` represents an instantaneous point on the time-line. On their own, an instant has insufficient information to allow a local date-time to be obtained. Only when paired with an offset or time-zone can the local date or time be calculated.

This field is strictly defined to have the same meaning in all calendar systems. This is necessary to ensure interoperation between calendars.

Range of InstantSeconds is between `https://developer.android.com/reference/kotlin/java/time/Instant.html#MIN:java.time.Instant` and `https://developer.android.com/reference/kotlin/java/time/Instant.html#MAX:java.time.Instant` [epoch second](../java.time/Instant.md)), both inclusive.

### MICRO_OF_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val MICRO_OF_DAY : ChronoField
```

The micro-of-day.

This counts the microsecond within the day, from 0 to (24 \* 60 \* 60 \* 1,000,000) - 1. This field has the same meaning for all calendar systems.

This field is used to represent the micro-of-day handling any fraction of the second. Implementations of `TemporalAccessor` should provide a value for this field if they can return a value for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` filling unknown precision with zero.

When this field is used for setting a value, it should behave in the same way as setting `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` with the value multiplied by 1,000.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The value is split to form `MICRO_OF_SECOND`, `SECOND_OF_MINUTE`, `MINUTE_OF_HOUR` and `HOUR_OF_DAY` fields.

### MICRO_OF_SECOND

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val MICRO_OF_SECOND : ChronoField
```

The micro-of-second.

This counts the microsecond within the second, from 0 to 999,999. This field has the same meaning for all calendar systems.

This field is used to represent the micro-of-second handling any fraction of the second. Implementations of `TemporalAccessor` should provide a value for this field if they can return a value for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`, `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` or `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` filling unknown precision with zero.

When this field is used for setting a value, it should behave in the same way as setting `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` with the value multiplied by 1,000.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The field is resolved in combination with `MILLI_OF_SECOND` to produce `NANO_OF_SECOND`.

### MILLI_OF_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val MILLI_OF_DAY : ChronoField
```

The milli-of-day.

This counts the millisecond within the day, from 0 to (24 \* 60 \* 60 \* 1,000) - 1. This field has the same meaning for all calendar systems.

This field is used to represent the milli-of-day handling any fraction of the second. Implementations of `TemporalAccessor` should provide a value for this field if they can return a value for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` filling unknown precision with zero.

When this field is used for setting a value, it should behave in the same way as setting `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` with the value multiplied by 1,000,000.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The value is split to form `MILLI_OF_SECOND`, `SECOND_OF_MINUTE`, `MINUTE_OF_HOUR` and `HOUR_OF_DAY` fields.

### MILLI_OF_SECOND

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val MILLI_OF_SECOND : ChronoField
```

The milli-of-second.

This counts the millisecond within the second, from 0 to 999. This field has the same meaning for all calendar systems.

This field is used to represent the milli-of-second handling any fraction of the second. Implementations of `TemporalAccessor` should provide a value for this field if they can return a value for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`, `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` or `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` filling unknown precision with zero.

When this field is used for setting a value, it should behave in the same way as setting `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` with the value multiplied by 1,000,000.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The field is resolved in combination with `MICRO_OF_SECOND` to produce `NANO_OF_SECOND`.

### MINUTE_OF_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val MINUTE_OF_DAY : ChronoField
```

The minute-of-day.

This counts the minute within the day, from 0 to (24 \* 60) - 1. This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The value is split to form `MINUTE_OF_HOUR` and `HOUR_OF_DAY` fields.

### MINUTE_OF_HOUR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val MINUTE_OF_HOUR : ChronoField
```

The minute-of-hour.

This counts the minute within the hour, from 0 to 59. This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode.

### MONTH_OF_YEAR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val MONTH_OF_YEAR : ChronoField
```

The month-of-year, such as March.

This represents the concept of the month within the year. In the default ISO calendar system, this has values from January (1) to December (12).

Non-ISO calendar systems should implement this field using the most recognized month-of-year values for users of the calendar system. Normally, this is a count of months starting from 1.

### NANO_OF_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val NANO_OF_DAY : ChronoField
```

The nano-of-day.

This counts the nanosecond within the day, from 0 to (24 \* 60 \* 60 \* 1,000,000,000) - 1. This field has the same meaning for all calendar systems.

This field is used to represent the nano-of-day handling any fraction of the second. Implementations of `TemporalAccessor` should provide a value for this field if they can return a value for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` filling unknown precision with zero.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The value is split to form `NANO_OF_SECOND`, `SECOND_OF_MINUTE`, `MINUTE_OF_HOUR` and `HOUR_OF_DAY` fields.

### NANO_OF_SECOND

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val NANO_OF_SECOND : ChronoField
```

The nano-of-second.

This counts the nanosecond within the second, from 0 to 999,999,999. This field has the same meaning for all calendar systems.

This field is used to represent the nano-of-second handling any fraction of the second. Implementations of `TemporalAccessor` should provide a value for this field if they can return a value for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`, `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` or `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` filling unknown precision with zero.

When this field is used for setting a value, it should set as much precision as the object stores, using integer division to remove excess precision. For example, if the `TemporalAccessor` stores time to millisecond precision, then the nano-of-second must be divided by 1,000,000 before replacing the milli-of-second.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The field is resolved in combination with `MILLI_OF_SECOND` and `MICRO_OF_SECOND`.

### OFFSET_SECONDS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val OFFSET_SECONDS : ChronoField
```

The offset from UTC/Greenwich.

This represents the concept of the offset in seconds of local time from UTC/Greenwich.

A `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` represents the period of time that local time differs from UTC/Greenwich. This is usually a fixed number of hours and minutes. It is equivalent to the `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#getTotalSeconds()` of the offset in seconds. For example, during the winter Paris has an offset of `+01:00`, which is 3600 seconds.

This field is strictly defined to have the same meaning in all calendar systems. This is necessary to ensure interoperation between calendars.

### PROLEPTIC_MONTH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val PROLEPTIC_MONTH : ChronoField
```

The proleptic-month based, counting months sequentially from year 0.

This field is the sequential count of months where the first month in proleptic-year zero has the value zero. Later months have increasingly larger values. Earlier months have increasingly small values. There are no gaps or breaks in the sequence of months. Note that this uses the *local* time-line, ignoring offset and time-zone.

In the default ISO calendar system, June 2012 would have the value `(2012 * 12 + 6 - 1)`. This field is primarily for internal use.

Non-ISO calendar systems must implement this field as per the definition above. It is just a simple zero-based count of elapsed months from the start of proleptic-year 0. All calendar systems with a full proleptic-year definition will have a year zero. If the calendar system has a minimum year that excludes year zero, then one must be extrapolated in order for this method to be defined.

### SECOND_OF_DAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val SECOND_OF_DAY : ChronoField
```

The second-of-day.

This counts the second within the day, from 0 to (24 \* 60 \* 60) - 1. This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode. The value is split to form `SECOND_OF_MINUTE`, `MINUTE_OF_HOUR` and `HOUR_OF_DAY` fields.

### SECOND_OF_MINUTE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val SECOND_OF_MINUTE : ChronoField
```

The second-of-minute.

This counts the second within the minute, from 0 to 59. This field has the same meaning for all calendar systems.

When parsing this field it behaves equivalent to the following: The value is validated in strict and smart mode but not in lenient mode.

### YEAR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val YEAR : ChronoField
```

The proleptic year, such as 2012.

This represents the concept of the year, counting sequentially and using negative numbers. The proleptic year is not interpreted in terms of the era. See `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#` for an example showing the mapping from proleptic year to year-of-era.

The standard mental model for a date is based on three concepts - year, month and day. These map onto the `YEAR`, `MONTH_OF_YEAR` and `DAY_OF_MONTH` fields. Note that there is no reference to eras. The full model for a date requires four concepts - era, year, month and day. These map onto the `ERA`, `YEAR_OF_ERA`, `MONTH_OF_YEAR` and `DAY_OF_MONTH` fields. Whether this field or `YEAR_OF_ERA` is used depends on which mental model is being used. See `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#` for more discussion on this topic.

Non-ISO calendar systems should implement this field as follows. If the calendar system has only two eras, before and after a fixed date, then the proleptic-year value must be the same as the year-of-era value for the later era, and increasingly negative for the earlier era. If the calendar system has more than two eras, then the proleptic-year value may be defined with any appropriate value, although defining it to be the same as ISO may be the best option.

### YEAR_OF_ERA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val YEAR_OF_ERA : ChronoField
```

The year within the era.

This represents the concept of the year within the era. This field is typically used with `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`.

The standard mental model for a date is based on three concepts - year, month and day. These map onto the `YEAR`, `MONTH_OF_YEAR` and `DAY_OF_MONTH` fields. Note that there is no reference to eras. The full model for a date requires four concepts - era, year, month and day. These map onto the `ERA`, `YEAR_OF_ERA`, `MONTH_OF_YEAR` and `DAY_OF_MONTH` fields. Whether this field or `YEAR` is used depends on which mental model is being used. See `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate.html#` for more discussion on this topic.

In the default ISO calendar system, there are two eras defined, 'BCE' and 'CE'. The era 'CE' is the one currently in use and year-of-era runs from 1 to the maximum value. The era 'BCE' is the previous era, and the year-of-era runs backwards.

For example, subtracting a year each time yield the following: 

- year-proleptic 2 = 'CE' year-of-era 2 

- year-proleptic 1 = 'CE' year-of-era 1 

- year-proleptic 0 = 'BCE' year-of-era 1 

- year-proleptic -1 = 'BCE' year-of-era 2 

Note that the ISO-8601 standard does not actually define eras. Note also that the ISO eras do not align with the well-known AD/BC eras due to the change between the Julian and Gregorian calendar systems.

Non-ISO calendar systems should implement this field using the most recognized year-of-era value for users of the calendar system. Since most calendar systems have only two eras, the year-of-era numbering approach will typically be the same as that used by the ISO calendar system. The year-of-era value should typically always be positive, however this is not required.

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Temporal!> adjustInto(
    temporal: R, 
    newValue: Long
): R
```

Returns a copy of the specified temporal object with the value of this field set.

This returns a new temporal object based on the specified one with the value for this field changed. For example, on a `LocalDate`, this could be used to set the year, month or day-of-month. The returned object has the same observable type as the specified object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then changing the month to February would be unclear. In cases like this, the implementation is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisField.adjustInto(temporal);
    temporal = temporal.with(thisField);
  
```
It is recommended to use the second approach, `with(TemporalField)`, as it is a lot clearer to read in code.

Implementations should perform any queries or calculations using the fields available in `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`. If the field is not supported an `UnsupportedTemporalTypeException` must be thrown.

Implementations must not alter the specified temporal object. Instead, an adjusted copy of the original must be returned. This provides equivalent, safe behavior for immutable and mutable implementations.

| Parameters ||
|---|---|
| `<R>` | the type of the Temporal object |
| `temporal` | R: the temporal object to adjust, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value of the field |
| --- | --- |

| Return ||
|---|---|
| `R` | the adjusted temporal object, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported by the temporal |
| --- | --- |

### checkValidIntValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun checkValidIntValue(value: Long): Int
```

Checks that the specified value is valid and fits in an `int`.

This validates that the value is within the outer range of valid values returned by `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#range()`. It also checks that all valid values are within the bounds of an `int`.

This method checks against the range of the field in the ISO-8601 calendar system. This range may be incorrect for other calendar systems. Use `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#range(java.time.temporal.ChronoField)` to access the correct range for a different calendar system.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to check |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value that was passed in |

### checkValidValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun checkValidValue(value: Long): Long
```

Checks that the specified value is valid for this field.

This validates that the value is within the outer range of valid values returned by `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#range()`.

This method checks against the range of the field in the ISO-8601 calendar system. This range may be incorrect for other calendar systems. Use `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#range(java.time.temporal.ChronoField)` to access the correct range for a different calendar system.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to check |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value that was passed in |

### getBaseUnit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBaseUnit(): TemporalUnit!
```

Gets the unit that the field is measured in.

The unit of the field is the period that varies within the range. For example, in the field 'MonthOfYear', the unit is 'Months'. See also `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField#getRangeUnit()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!` | the unit defining the base unit of the field, not null |

### getDisplayName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(locale: Locale!): String!
```

Gets the display name for the field in the requested locale.

If there is no display name for the locale then a suitable default must be returned.

The default implementation must check the locale is not null and return `toString()`.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the locale to use, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the display name for the locale or a suitable default, not null |

### getFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFrom(temporal: TemporalAccessor!): Long
```

Gets the value of this field from the specified temporal object.

This queries the temporal object for the value of this field.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#getLong(java.time.temporal.TemporalField)` (or `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#get(java.time.temporal.TemporalField)`):

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisField.getFrom(temporal);
    temporal = temporal.getLong(thisField);
  
```
It is recommended to use the second approach, `getLong(TemporalField)`, as it is a lot clearer to read in code.

Implementations should perform any queries or calculations using the fields available in `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`. If the field is not supported an `UnsupportedTemporalTypeException` must be thrown.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](TemporalAccessor.md)!: the temporal object to query, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value of this field, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported by the temporal |
| --- | --- |

### getRangeUnit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRangeUnit(): TemporalUnit!
```

Gets the range that the field is bound by.

The range of the field is the period that the field varies within. For example, in the field 'MonthOfYear', the range is 'Years'. See also `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField#getBaseUnit()`.

The range is never null. For example, the 'Year' field is shorthand for 'YearOfForever'. It therefore has a unit of 'Years' and a range of 'Forever'.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!` | the unit defining the range of the field, not null |

### isDateBased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDateBased(): Boolean
```

Checks if this field represents a component of a date.

Fields from day-of-week to era are date-based.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if it is a component of a date |

### isSupportedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupportedBy(temporal: TemporalAccessor!): Boolean
```

Checks if this field is supported by the temporal object.

This determines whether the temporal accessor supports this field. If this returns false, then the temporal cannot be queried for this field.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#isSupported(java.time.temporal.TemporalField)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisField.isSupportedBy(temporal);
    temporal = temporal.isSupported(thisField);
  
```
It is recommended to use the second approach, `isSupported(TemporalField)`, as it is a lot clearer to read in code.

Implementations should determine whether they are supported using the fields available in `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](TemporalAccessor.md)!: the temporal object to query, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the date-time can be queried for this field, false if not |

### isTimeBased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isTimeBased(): Boolean
```

Checks if this field represents a component of a time.

Fields from nano-of-second to am-pm-of-day are time-based.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if it is a component of a time |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun range(): ValueRange!
```

Gets the range of valid values for the field.

All fields can be expressed as a `long` integer. This method returns an object that describes the valid range for that value.

This method returns the range of the field in the ISO-8601 calendar system. This range may be incorrect for other calendar systems. Use `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#range(java.time.temporal.ChronoField)` to access the correct range for a different calendar system.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange!` | the range of valid values for the field, not null |

### rangeRefinedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun rangeRefinedBy(temporal: TemporalAccessor!): ValueRange!
```

Get the range of valid values for this field using the temporal object to refine the result.

This uses the temporal object to find the range of valid values for the field. This is similar to `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField#range()`, however this method refines the result using the temporal. For example, if the field is `DAY_OF_MONTH` the `range` method is not accurate as there are four possible month lengths, 28, 29, 30 and 31 days. Using this method with a date allows the range to be accurate, returning just one of those four options.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#range(java.time.temporal.TemporalField)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisField.rangeRefinedBy(temporal);
    temporal = temporal.range(thisField);
  
```
It is recommended to use the second approach, `range(TemporalField)`, as it is a lot clearer to read in code.

Implementations should perform any queries or calculations using the fields available in `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField#`. If the field is not supported an `UnsupportedTemporalTypeException` must be thrown.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](TemporalAccessor.md)!: the temporal object used to refine the result, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange!` | the range of valid values for this field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported by the temporal |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns the name of this enum constant, as contained in the declaration. This method may be overridden, though it typically isn't necessary or desirable. An enum class should override this method when a more "programmer-friendly" string form exists.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the name of the field, not null |
