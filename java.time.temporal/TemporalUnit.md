# TemporalUnit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalUnit

```
interface TemporalUnit
```

| [java.time.temporal.TemporalUnit](TemporalUnit.md) |

| Known Direct Subclasses [ChronoUnit](ChronoUnit.md) |--------------------------------------------------------------------------------------------|---------------------------------------| | [ChronoUnit](ChronoUnit.md) | A standard set of date periods units. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ChronoUnit.CENTURIES](ChronoUnit.md), [ChronoUnit.DAYS](ChronoUnit.md), [ChronoUnit.DECADES](ChronoUnit.md), [ChronoUnit.ERAS](ChronoUnit.md), [ChronoUnit.FOREVER](ChronoUnit.md), [ChronoUnit.HALF_DAYS](ChronoUnit.md), [ChronoUnit.HOURS](ChronoUnit.md), [ChronoUnit.MICROS](ChronoUnit.md), [ChronoUnit.MILLENNIA](ChronoUnit.md), [ChronoUnit.MILLIS](ChronoUnit.md), [ChronoUnit.MINUTES](ChronoUnit.md), [ChronoUnit.MONTHS](ChronoUnit.md), and 4 others. |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------| | [ChronoUnit.CENTURIES](ChronoUnit.md) | Unit that represents the concept of a century. | | [ChronoUnit.DAYS](ChronoUnit.md) | Unit that represents the concept of a day. | | [ChronoUnit.DECADES](ChronoUnit.md) | Unit that represents the concept of a decade. | | [ChronoUnit.ERAS](ChronoUnit.md) | Unit that represents the concept of an era. | | [ChronoUnit.FOREVER](ChronoUnit.md) | Artificial unit that represents the concept of forever. | | [ChronoUnit.HALF_DAYS](ChronoUnit.md) | Unit that represents the concept of half a day, as used in AM/PM. | | [ChronoUnit.HOURS](ChronoUnit.md) | Unit that represents the concept of an hour. | | [ChronoUnit.MICROS](ChronoUnit.md) | Unit that represents the concept of a microsecond. | | [ChronoUnit.MILLENNIA](ChronoUnit.md) | Unit that represents the concept of a millennium. | | [ChronoUnit.MILLIS](ChronoUnit.md) | Unit that represents the concept of a millisecond. | | [ChronoUnit.MINUTES](ChronoUnit.md) | Unit that represents the concept of a minute. | | [ChronoUnit.MONTHS](ChronoUnit.md) | Unit that represents the concept of a month. | | [ChronoUnit.NANOS](ChronoUnit.md) | Unit that represents the concept of a nanosecond, the smallest supported unit of time. | | [ChronoUnit.SECONDS](ChronoUnit.md) | Unit that represents the concept of a second. | | [ChronoUnit.WEEKS](ChronoUnit.md) | Unit that represents the concept of a week. | | [ChronoUnit.YEARS](ChronoUnit.md) | Unit that represents the concept of a year. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A unit of date-time, such as Days or Hours.

Measurement of time is built on units, such as years, months, days, hours, minutes and seconds. Implementations of this interface represent those units.

An instance of this interface represents the unit itself, rather than an amount of the unit. See [Period](../java.time/Period.md) for a class that represents an amount in terms of the common units.

The most commonly used units are defined in [ChronoUnit](ChronoUnit.md). Further units are supplied in [IsoFields](IsoFields.md). Units can also be written by application code by implementing this interface.

The unit works using double dispatch. Client code calls methods on a date-time like`LocalDateTime`which check if the unit is a`ChronoUnit`. If it is, then the date-time must handle it. Otherwise, the method call is re-dispatched to the matching method in this interface.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [addTo](TemporalUnit.md))`(`temporal:` `R`, `amount:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of the specified temporal object with the specified period added. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [between](TemporalUnit.md))`(`temporal1Inclusive:` ` [Temporal](Temporal.md)!`, `temporal2Exclusive:` ` [Temporal](Temporal.md)!`)` Calculates the amount of time between two temporal objects. |
| abstract [Duration](../java.time/Duration.md)! | [getDuration](TemporalUnit.md))`()` Gets the duration of this unit, which may be an estimate. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDateBased](TemporalUnit.md))`()` Checks if this unit represents a component of a date. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDurationEstimated](TemporalUnit.md))`()` Checks if the duration of the unit is an estimate. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupportedBy](TemporalUnit.md))`(`temporal:` ` [Temporal](Temporal.md)!`)` Checks if this unit is supported by the specified temporal object. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTimeBased](TemporalUnit.md))`()` Checks if this unit represents a component of a time. |

## Public methods

### addTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Temporal!> addTo(
    temporal: R, 
    amount: Long
): R
```

Returns a copy of the specified temporal object with the specified period added.

The period added is a multiple of this unit. For example, this method could be used to add "3 days" to a date by calling this method on the instance representing "days", passing the date and the period "3". The period to be added may be negative, which is equivalent to subtraction.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [Temporal.plus(long, TemporalUnit)](Temporal.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisUnit.addTo(temporal);
    temporal = temporal.plus(thisUnit);
  
```
It is recommended to use the second approach,`plus(TemporalUnit)`, as it is a lot clearer to read in code.

Implementations should perform any queries or calculations using the units available in [ChronoUnit](ChronoUnit.md) or the fields available in [ChronoField](ChronoField.md). If the unit is not supported an`UnsupportedTemporalTypeException`must be thrown.

Implementations must not alter the specified temporal object. Instead, an adjusted copy of the original must be returned. This provides equivalent, safe behavior for immutable and mutable implementations.

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
abstract fun between(
    temporal1Inclusive: Temporal!, 
    temporal2Exclusive: Temporal!
): Long
```

Calculates the amount of time between two temporal objects.

This calculates the amount in terms of this unit. The start and end points are supplied as temporal objects and must be of compatible types. The implementation will convert the second type to be an instance of the first type before the calculating the amount. The result will be negative if the end is before the start. For example, the amount in hours between two temporal objects can be calculated using`HOURS.between(startTime, endTime)`.

The calculation returns a whole number, representing the number of complete units between the two temporals. For example, the amount in hours between the times 11:30 and 13:29 will only be one hour as it is one minute short of two hours.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [Temporal.until(Temporal, TemporalUnit)](Temporal.md)): 

```kotlin
// these two lines are equivalent
    between = thisUnit.between(start, end);
    between = start.until(end, thisUnit);
  
```
The choice should be made based on which makes the code more readable.

For example, this method allows the number of days between two dates to be calculated: 

```kotlin
long daysBetween = DAYS.between(start, end);
   // or alternatively
   long daysBetween = start.until(end, DAYS);
  
```

Implementations should perform any queries or calculations using the units available in [ChronoUnit](ChronoUnit.md) or the fields available in [ChronoField](ChronoField.md). If the unit is not supported an`UnsupportedTemporalTypeException`must be thrown. Implementations must not alter the specified temporal objects.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `temporal1Inclusive` | [Temporal](Temporal.md)!:the base temporal object, not null |
| `temporal2Exclusive` | [Temporal](Temporal.md)!:the other temporal object, exclusive, not null |

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
abstract fun getDuration(): Duration!
```

Gets the duration of this unit, which may be an estimate.

All units return a duration measured in standard nanoseconds from this method. The duration will be positive and non-zero. For example, an hour has a duration of`60 * 60 * 1,000,000,000ns`.

Some units may return an accurate duration while others return an estimate. For example, days have an estimated duration due to the possibility of daylight saving time changes. To determine if the duration is an estimate, use [isDurationEstimated()](TemporalUnit.md)).

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Duration](../java.time/Duration.md)! | the duration of this unit, which may be an estimate, not null |

### isDateBased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDateBased(): Boolean
```

Checks if this unit represents a component of a date.

A date is time-based if it can be used to imply meaning from a date. It must have a [duration](TemporalUnit.md))that is an integral multiple of the length of a standard day. Note that it is valid for both`isDateBased()`and`isTimeBased()`to return false, such as when representing a unit like 36 hours.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this unit is a component of a date |

### isDurationEstimated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDurationEstimated(): Boolean
```

Checks if the duration of the unit is an estimate.

All units have a duration, however the duration is not always accurate. For example, days have an estimated duration due to the possibility of daylight saving time changes. This method returns true if the duration is an estimate and false if it is accurate. Note that accurate/estimated ignores leap seconds.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the duration is estimated, false if accurate |

### isSupportedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSupportedBy(temporal: Temporal!): Boolean
```

Checks if this unit is supported by the specified temporal object.

This checks that the implementing date-time can add/subtract this unit. This can be used to avoid throwing an exception.

This default implementation derives the value using [Temporal.plus(long, TemporalUnit)](Temporal.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](Temporal.md)!:the temporal object to check, not null |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit is supported |

### isTimeBased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isTimeBased(): Boolean
```

Checks if this unit represents a component of a time.

A unit is time-based if it can be used to imply meaning from a time. It must have a [duration](TemporalUnit.md))that divides into the length of a standard day without remainder. Note that it is valid for both`isDateBased()`and`isTimeBased()`to return false, such as when representing a unit like 36 hours.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this unit is a component of a time |
