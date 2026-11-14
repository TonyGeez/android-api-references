# ChronoUnit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChronoUnit

```
class ChronoUnit : TemporalUnit
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.temporal.ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#)\> ||
| | ↳ | [java.time.temporal.ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#) |

| Known Direct Subclasses [ChronoUnit.CENTURIES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:CENTURIES), [ChronoUnit.DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:DAYS), [ChronoUnit.DECADES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:DECADES), [ChronoUnit.ERAS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:ERAS), [ChronoUnit.FOREVER](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:FOREVER), [ChronoUnit.HALF_DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:HALF_DAYS), [ChronoUnit.HOURS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:HOURS), [ChronoUnit.MICROS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MICROS), [ChronoUnit.MILLENNIA](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MILLENNIA), [ChronoUnit.MILLIS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MILLIS), [ChronoUnit.MINUTES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MINUTES), [ChronoUnit.MONTHS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MONTHS), and 4 others. |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------| | [ChronoUnit.CENTURIES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:CENTURIES) | Unit that represents the concept of a century. | | [ChronoUnit.DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:DAYS) | Unit that represents the concept of a day. | | [ChronoUnit.DECADES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:DECADES) | Unit that represents the concept of a decade. | | [ChronoUnit.ERAS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:ERAS) | Unit that represents the concept of an era. | | [ChronoUnit.FOREVER](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:FOREVER) | Artificial unit that represents the concept of forever. | | [ChronoUnit.HALF_DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:HALF_DAYS) | Unit that represents the concept of half a day, as used in AM/PM. | | [ChronoUnit.HOURS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:HOURS) | Unit that represents the concept of an hour. | | [ChronoUnit.MICROS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MICROS) | Unit that represents the concept of a microsecond. | | [ChronoUnit.MILLENNIA](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MILLENNIA) | Unit that represents the concept of a millennium. | | [ChronoUnit.MILLIS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MILLIS) | Unit that represents the concept of a millisecond. | | [ChronoUnit.MINUTES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MINUTES) | Unit that represents the concept of a minute. | | [ChronoUnit.MONTHS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MONTHS) | Unit that represents the concept of a month. | | [ChronoUnit.NANOS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:NANOS) | Unit that represents the concept of a nanosecond, the smallest supported unit of time. | | [ChronoUnit.SECONDS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:SECONDS) | Unit that represents the concept of a second. | | [ChronoUnit.WEEKS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:WEEKS) | Unit that represents the concept of a week. | | [ChronoUnit.YEARS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:YEARS) | Unit that represents the concept of a year. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A standard set of date periods units.

This set of units provide unit-based access to manipulate a date, time or date-time. The standard set of units can be extended by implementing [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit).

These units are intended to be applicable in multiple calendar systems. For example, most non-ISO calendar systems define units of years, months and days, just with slightly different rules. The documentation of each unit explains how it operates.

## Summary

| Enum values ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CENTURIES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:CENTURIES) Unit that represents the concept of a century. |
| [DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:DAYS) Unit that represents the concept of a day. |
| [DECADES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:DECADES) Unit that represents the concept of a decade. |
| [ERAS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:ERAS) Unit that represents the concept of an era. |
| [FOREVER](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:FOREVER) Artificial unit that represents the concept of forever. |
| [HALF_DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:HALF_DAYS) Unit that represents the concept of half a day, as used in AM/PM. |
| [HOURS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:HOURS) Unit that represents the concept of an hour. |
| [MICROS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MICROS) Unit that represents the concept of a microsecond. |
| [MILLENNIA](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MILLENNIA) Unit that represents the concept of a millennium. |
| [MILLIS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MILLIS) Unit that represents the concept of a millisecond. |
| [MINUTES](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MINUTES) Unit that represents the concept of a minute. |
| [MONTHS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:MONTHS) Unit that represents the concept of a month. |
| [NANOS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:NANOS) Unit that represents the concept of a nanosecond, the smallest supported unit of time. |
| [SECONDS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:SECONDS) Unit that represents the concept of a second. |
| [WEEKS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:WEEKS) Unit that represents the concept of a week. |
| [YEARS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#ENUM_VALUE:YEARS) Unit that represents the concept of a year. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| R | [addTo](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#addTo(java.time.temporal.ChronoUnit.addTo.R,%20kotlin.Long))`(`temporal:` `R`, `amount:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [between](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal))`(`temporal1Inclusive:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!`, `temporal2Exclusive:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!`)` <br /> |
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)! | [getDuration](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#getDuration())`()` Gets the estimated duration of this unit in the ISO calendar system. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDateBased](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#isDateBased())`()` Checks if this unit is a date unit. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDurationEstimated](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#isDurationEstimated())`()` Checks if the duration of the unit is an estimate. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupportedBy](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#isSupportedBy(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!`)` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTimeBased](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#isTimeBased())`()` Checks if this unit is a time unit. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit#toString())`()` <br /> |

## Enum values

### CENTURIES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CENTURIES : ChronoUnit
```

Unit that represents the concept of a century. For the ISO calendar system, it is equal to 100 years.

When used with other calendar systems it must correspond to an integral number of days and is normally an integral number of years. 

### DAYS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DAYS : ChronoUnit
```

Unit that represents the concept of a day. For the ISO calendar system, it is the standard day from midnight to midnight. The estimated duration of a day is`24 Hours`.

When used with other calendar systems it must correspond to the day defined by the rising and setting of the Sun on Earth. It is not required that days begin at midnight - when converting between calendar systems, the date should be equivalent at midday. 

### DECADES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DECADES : ChronoUnit
```

Unit that represents the concept of a decade. For the ISO calendar system, it is equal to 10 years.

When used with other calendar systems it must correspond to an integral number of days and is normally an integral number of years. 

### ERAS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ERAS : ChronoUnit
```

Unit that represents the concept of an era. The ISO calendar system doesn't have eras thus it is impossible to add an era to a date or date-time. The estimated duration of the era is artificially defined as`1,000,000,000 Years`.

When used with other calendar systems there are no restrictions on the unit. 

### FOREVER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val FOREVER : ChronoUnit
```

Artificial unit that represents the concept of forever. This is primarily used with [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField) to represent unbounded fields such as the year or era. The estimated duration of this unit is artificially defined as the largest duration supported by [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#). 

### HALF_DAYS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val HALF_DAYS : ChronoUnit
```

Unit that represents the concept of half a day, as used in AM/PM. For the ISO calendar system, it is equal to 12 hours. 

### HOURS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val HOURS : ChronoUnit
```

Unit that represents the concept of an hour. For the ISO calendar system, it is equal to 60 minutes. 

### MICROS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MICROS : ChronoUnit
```

Unit that represents the concept of a microsecond. For the ISO calendar system, it is equal to the 1,000,000th part of the second unit. 

### MILLENNIA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MILLENNIA : ChronoUnit
```

Unit that represents the concept of a millennium. For the ISO calendar system, it is equal to 1000 years.

When used with other calendar systems it must correspond to an integral number of days and is normally an integral number of years. 

### MILLIS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MILLIS : ChronoUnit
```

Unit that represents the concept of a millisecond. For the ISO calendar system, it is equal to the 1000th part of the second unit. 

### MINUTES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MINUTES : ChronoUnit
```

Unit that represents the concept of a minute. For the ISO calendar system, it is equal to 60 seconds. 

### MONTHS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MONTHS : ChronoUnit
```

Unit that represents the concept of a month. For the ISO calendar system, the length of the month varies by month-of-year. The estimated duration of a month is one twelfth of`365.2425 Days`.

When used with other calendar systems it must correspond to an integral number of days. 

### NANOS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NANOS : ChronoUnit
```

Unit that represents the concept of a nanosecond, the smallest supported unit of time. For the ISO calendar system, it is equal to the 1,000,000,000th part of the second unit. 

### SECONDS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SECONDS : ChronoUnit
```

Unit that represents the concept of a second. For the ISO calendar system, it is equal to the second in the SI system of units, except around a leap-second. 

### WEEKS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val WEEKS : ChronoUnit
```

Unit that represents the concept of a week. For the ISO calendar system, it is equal to 7 days.

When used with other calendar systems it must correspond to an integral number of days. 

### YEARS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val YEARS : ChronoUnit
```

Unit that represents the concept of a year. For the ISO calendar system, it is equal to 12 months. The estimated duration of a year is`365.2425 Days`.

When used with other calendar systems it must correspond to an integral number of days or months roughly equal to a year defined by the passage of the Earth around the Sun.

## Public methods

### addTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <R : Temporal!> addTo(
    temporal: R, 
    amount: Long
): R
```

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the Temporal object |
| `temporal` | R:the temporal object to adjust, not null |
| `amount` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of this unit to add, positive or negative |
| --- | --- |

| Return ||
|---|----------------------------------------|
| R | the adjusted temporal object, not null |

| Exceptions ||
|-------------------------------------------------------|----------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported by the temporal |

### between

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun between(
    temporal1Inclusive: Temporal!, 
    temporal2Exclusive: Temporal!
): Long
```

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `temporal1Inclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!:the base temporal object, not null |
| `temporal2Exclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!:the other temporal object, exclusive, not null |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between temporal1Inclusive and temporal2Exclusive in terms of this unit; positive if temporal2Exclusive is later than temporal1Inclusive, negative if earlier |

| Exceptions ||
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to the same type as the start temporal |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported by the temporal |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getDuration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDuration(): Duration!
```

Gets the estimated duration of this unit in the ISO calendar system.

All of the units in this class have an estimated duration. Days vary due to daylight saving time, while months have different lengths.

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)! | the estimated duration of this unit, not null |

### isDateBased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDateBased(): Boolean
```

Checks if this unit is a date unit.

All units from days to eras inclusive are date-based. Time-based units and`FOREVER`return false.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a date unit, false if a time unit |

### isDurationEstimated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDurationEstimated(): Boolean
```

Checks if the duration of the unit is an estimate.

All time units in this class are considered to be accurate, while all date units in this class are considered to be estimated.

This definition ignores leap seconds, but considers that Days vary due to daylight saving time and months have different lengths.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the duration is estimated, false if accurate |

### isSupportedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupportedBy(temporal: Temporal!): Boolean
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!:the temporal object to check, not null |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit is supported |

### isTimeBased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isTimeBased(): Boolean
```

Checks if this unit is a time unit.

All units from nanos to half-days inclusive are time-based. Date-based units and`FOREVER`return false.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a time unit, false if a date unit |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the name of this unit, not null |
