# Duration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Duration

```
class Duration : Comparable<Duration!>, Serializable, TemporalAmount
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.Duration](Duration.md) |

A time-based amount of time, such as '34.5 seconds'.

This class models a quantity or amount of time in terms of seconds and nanoseconds. It can be accessed using other duration-based units, such as minutes and hours. In addition, the [DAYS](../java.time.temporal/ChronoUnit.md) unit can be used and is treated as exactly equal to 24 hours, thus ignoring daylight savings effects. See [Period](Period.md) for the date-based equivalent to this class.

A physical duration could be of infinite length. For practicality, the duration is stored with constraints similar to [Instant](Instant.md). The duration uses nanosecond resolution with a maximum value of the seconds that can be held in a`long`. This is greater than the current estimated age of the universe.

The range of a duration requires the storage of a number larger than a`long`. To achieve this, the class stores a`long`representing seconds and an`int`representing nanosecond-of-second, which will always be between 0 and 999,999,999. The model is of a directed duration, meaning that the duration may be negative.

The duration is measured in "seconds", but these are not necessarily identical to the scientific "SI second" definition based on atomic clocks. This difference only impacts durations measured near a leap-second and should not affect most applications. See [Instant](Instant.md) for a discussion as to the meaning of the second and time-scales.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Duration](Duration.md)! | [abs](Duration.md))`()` Returns a copy of this duration with a positive length. |
| [Temporal](../java.time.temporal/Temporal.md)! | [addTo](Duration.md))`(`temporal:` ` [Temporal](../java.time.temporal/Temporal.md)!`)` Adds this duration to the specified temporal object. |
| static [Duration](Duration.md)! | [between](Duration.md))`(`startInclusive:` ` [Temporal](../java.time.temporal/Temporal.md)!`, `endExclusive:` ` [Temporal](../java.time.temporal/Temporal.md)!`)` Obtains a`Duration`representing the duration between two temporal objects. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](Duration.md))`(`other:` ` [Duration](Duration.md)!`)` Compares this duration to the specified`Duration`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [dividedBy](Duration.md))`(`divisor:` ` [Duration](Duration.md)!`)` Returns number of whole times a specified Duration occurs within this Duration. |
| [Duration](Duration.md)! | [dividedBy](Duration.md))`(`divisor:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration divided by the specified value. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Duration.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this duration is equal to the specified`Duration`. |
| static [Duration](Duration.md)! | [from](Duration.md))`(`amount:` ` [TemporalAmount](../java.time.temporal/TemporalAmount.md)!`)` Obtains an instance of`Duration`from a temporal amount. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](Duration.md))`(`unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Gets the value of the requested unit. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNano](Duration.md))`()` Gets the number of nanoseconds within the second in this duration. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSeconds](Duration.md))`()` Gets the number of seconds in this duration. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TemporalUnit](../java.time.temporal/TemporalUnit.md)!\>! | [getUnits](Duration.md))`()` Gets the set of units supported by this duration. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Duration.md))`()` A hash code for this duration. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNegative](Duration.md))`()` Checks if this duration is negative, excluding zero. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPositive](Duration.md))`()` Checks if this duration is positive, excluding zero. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isZero](Duration.md))`()` Checks if this duration is zero length. |
| [Duration](Duration.md)! | [minus](Duration.md))`(`duration:` ` [Duration](Duration.md)!`)` Returns a copy of this duration with the specified duration subtracted. |
| [Duration](Duration.md)! | [minus](Duration.md))`(`amountToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Returns a copy of this duration with the specified duration subtracted. |
| --- | --- |
| [Duration](Duration.md)! | [minusDays](Duration.md))`(`daysToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in standard 24 hour days subtracted. |
| [Duration](Duration.md)! | [minusHours](Duration.md))`(`hoursToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in hours subtracted. |
| [Duration](Duration.md)! | [minusMillis](Duration.md))`(`millisToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in milliseconds subtracted. |
| --- | --- |
| [Duration](Duration.md)! | [minusMinutes](Duration.md))`(`minutesToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in minutes subtracted. |
| [Duration](Duration.md)! | [minusNanos](Duration.md))`(`nanosToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in nanoseconds subtracted. |
| [Duration](Duration.md)! | [minusSeconds](Duration.md))`(`secondsToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in seconds subtracted. |
| --- | --- |
| [Duration](Duration.md)! | [multipliedBy](Duration.md))`(`multiplicand:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration multiplied by the scalar. |
| [Duration](Duration.md)! | [negated](Duration.md))`()` Returns a copy of this duration with the length negated. |
| static [Duration](Duration.md)! | [of](Duration.md))`(`amount:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Obtains a`Duration`representing an amount in the specified unit. |
| --- | --- |
| static [Duration](Duration.md)! | [ofDays](Duration.md))`(`days:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a`Duration`representing a number of standard 24 hour days. |
| static [Duration](Duration.md)! | [ofHours](Duration.md))`(`hours:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a`Duration`representing a number of standard hours. |
| static [Duration](Duration.md)! | [ofMillis](Duration.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a`Duration`representing a number of milliseconds. |
| --- | --- |
| static [Duration](Duration.md)! | [ofMinutes](Duration.md))`(`minutes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a`Duration`representing a number of standard minutes. |
| static [Duration](Duration.md)! | [ofNanos](Duration.md))`(`nanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a`Duration`representing a number of nanoseconds. |
| static [Duration](Duration.md)! | [ofSeconds](Duration.md))`(`seconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a`Duration`representing a number of seconds. |
| --- | --- |
| static [Duration](Duration.md)! | [ofSeconds](Duration.md))`(`seconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `nanoAdjustment:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a`Duration`representing a number of seconds and an adjustment in nanoseconds. |
| static [Duration](Duration.md)! | [parse](Duration.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Obtains a`Duration`from a text string such as`PnDTnHnMn.nS`. |
| [Duration](Duration.md)! | [plus](Duration.md))`(`duration:` ` [Duration](Duration.md)!`)` Returns a copy of this duration with the specified duration added. |
| --- | --- |
| [Duration](Duration.md)! | [plus](Duration.md))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Returns a copy of this duration with the specified duration added. |
| [Duration](Duration.md)! | [plusDays](Duration.md))`(`daysToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in standard 24 hour days added. |
| [Duration](Duration.md)! | [plusHours](Duration.md))`(`hoursToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in hours added. |
| --- | --- |
| [Duration](Duration.md)! | [plusMillis](Duration.md))`(`millisToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in milliseconds added. |
| [Duration](Duration.md)! | [plusMinutes](Duration.md))`(`minutesToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in minutes added. |
| [Duration](Duration.md)! | [plusNanos](Duration.md))`(`nanosToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in nanoseconds added. |
| --- | --- |
| [Duration](Duration.md)! | [plusSeconds](Duration.md))`(`secondsToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified duration in seconds added. |
| [Temporal](../java.time.temporal/Temporal.md)! | [subtractFrom](Duration.md))`(`temporal:` ` [Temporal](../java.time.temporal/Temporal.md)!`)` Subtracts this duration from the specified temporal object. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toDays](Duration.md))`()` Gets the number of days in this duration. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toDaysPart](Duration.md))`()` Extracts the number of days in the duration. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toHours](Duration.md))`()` Gets the number of hours in this duration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toHoursPart](Duration.md))`()` Extracts the number of hours part in the duration. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toMillis](Duration.md))`()` Converts this duration to the total length in milliseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toMillisPart](Duration.md))`()` Extracts the number of milliseconds part of the duration. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toMinutes](Duration.md))`()` Gets the number of minutes in this duration. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toMinutesPart](Duration.md))`()` Extracts the number of minutes part in the duration. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toNanos](Duration.md))`()` Converts this duration to the total length in nanoseconds expressed as a`long`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toNanosPart](Duration.md))`()` Get the nanoseconds part within seconds of the duration. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toSeconds](Duration.md))`()` Gets the number of seconds in this duration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toSecondsPart](Duration.md))`()` Extracts the number of seconds part in the duration. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Duration.md))`()` A string representation of this duration using ISO-8601 seconds based representation, such as`PT8H6M12.345S`. |
| --- | --- |
| [Duration](Duration.md)! | [truncatedTo](Duration.md))`(`unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` Returns a copy of this`Duration`truncated to the specified unit. |
| [Duration](Duration.md)! | [withNanos](Duration.md))`(`nanoOfSecond:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this duration with the specified nano-of-second. |
| [Duration](Duration.md)! | [withSeconds](Duration.md))`(`seconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this duration with the specified amount of seconds. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Duration](Duration.md)! | [ZERO](Duration.md) Constant for a duration of zero. |

## Public methods

### abs

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun abs(): Duration!
```

Returns a copy of this duration with a positive length.

This method returns a positive duration by effectively removing the sign from any negative total length. For example,`PT-1.3S`will be returned as`PT1.3S`.

This instance is immutable and unaffected by this method call.

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with an absolute length, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### addTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addTo(temporal: Temporal!): Temporal!
```

Adds this duration to the specified temporal object.

This returns a temporal object of the same observable type as the input with this duration added.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.plus(TemporalAmount)](../java.time.temporal/Temporal.md)). 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    dateTime = thisDuration.addTo(dateTime);
    dateTime = dateTime.plus(thisDuration);
  
```

The calculation will add the seconds, then nanos. Only non-zero amounts will be added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java.time.temporal/Temporal.md)!:the temporal object to adjust, not null |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Temporal](../java.time.temporal/Temporal.md)! | an object of the same type with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to add |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### between

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun between(
    startInclusive: Temporal!, 
    endExclusive: Temporal!
): Duration!
```

Obtains a`Duration`representing the duration between two temporal objects.

This calculates the duration between two temporal objects. If the objects are of different types, then the duration is calculated based on the type of the first object. For example, if the first argument is a`LocalTime`then the second argument is converted to a`LocalTime`.

The specified temporal objects must support the [SECONDS](../java.time.temporal/ChronoUnit.md) unit. For full accuracy, either the [NANOS](../java.time.temporal/ChronoUnit.md) unit or the [NANO_OF_SECOND](../java.time.temporal/ChronoField.md) field should be supported.

The result of this method can be a negative period if the end is before the start. To guarantee to obtain a positive duration call [abs()](Duration.md))on the result.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `startInclusive` | [Temporal](../java.time.temporal/Temporal.md)!:the start instant, inclusive, not null |
| `endExclusive` | [Temporal](../java.time.temporal/Temporal.md)!:the end instant, exclusive, not null |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

| Exceptions ||
|---------------------------------|---------------------------------------------------------|
| `java.time.DateTimeException` | if the seconds between the temporals cannot be obtained |
| `java.lang.ArithmeticException` | if the calculation exceeds the capacity of`Duration` |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Duration!): Int
```

Compares this duration to the specified`Duration`.

The comparison is based on the total length of the durations. It is "consistent with equals", as defined by [Comparable](../java.lang/Comparable.md).

| Parameters ||
|-----------------|--------------------------------------------|
| `o` | the object to be compared. |
| `otherDuration` | the other duration to compare to, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the comparator value, negative if less, positive if greater |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### dividedBy

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dividedBy(divisor: Duration!): Long
```

Returns number of whole times a specified Duration occurs within this Duration.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [Duration](Duration.md)!:the value to divide the duration by, positive or negative, not null |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | number of whole times, rounded toward zero, a specified`Duration`occurs within this Duration, may be negative |

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `java.lang.ArithmeticException` | if the divisor is zero, or if numeric overflow occurs |

### dividedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dividedBy(divisor: Long): Duration!
```

Returns a copy of this duration divided by the specified value.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `divisor` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to divide the duration by, positive or negative, not zero |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration divided by the specified divisor, not null |

| Exceptions ||
|---------------------------------|------------------------------------------------------|
| `java.lang.ArithmeticException` | if the divisor is zero or if numeric overflow occurs |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Checks if this duration is equal to the specified`Duration`.

The comparison is based on the total length of the durations.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the other duration, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the other duration is equal to this one |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun from(amount: TemporalAmount!): Duration!
```

Obtains an instance of`Duration`from a temporal amount.

This obtains a duration based on the specified amount. A`TemporalAmount`represents an amount of time, which may be date-based or time-based, which this factory extracts to a duration.

The conversion loops around the set of units from the amount and uses the [duration](../java.time.temporal/TemporalUnit.md))of the unit to calculate the total`Duration`. Only a subset of units are accepted by this method. The unit must either have an [exact duration](../java.time.temporal/TemporalUnit.md))or be [ChronoUnit.DAYS](../java.time.temporal/ChronoUnit.md) which is treated as 24 hours. If any other units are found then an exception is thrown.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!:the temporal amount to convert, not null |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------|
| [Duration](Duration.md)! | the equivalent duration, not null |

| Exceptions ||
|---------------------------------|-------------------------------------|
| `java.time.DateTimeException` | if unable to convert to a`Duration` |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(unit: TemporalUnit!): Long
```

Gets the value of the requested unit.

This returns a value for each of the two supported units, [SECONDS](../java.time.temporal/ChronoUnit.md) and [NANOS](../java.time.temporal/ChronoUnit.md). All other units throw an exception.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the`TemporalUnit`for which to return the value |

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the long value of the unit |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if the unit is not supported |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### getNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNano(): Int
```

Gets the number of nanoseconds within the second in this duration.

The length of the duration is stored using two fields - seconds and nanoseconds. The nanoseconds part is a value from 0 to 999,999,999 that is an adjustment to the length in seconds. The total duration is defined by calling this method and [getSeconds()](Duration.md)).

A`Duration`represents a directed distance between two points on the time-line. A negative duration is expressed by the negative sign of the seconds part. A duration of -1 nanosecond is stored as -1 seconds plus 999,999,999 nanoseconds.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the nanoseconds within the second part of the length of the duration, from 0 to 999,999,999 |

### getSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSeconds(): Long
```

Gets the number of seconds in this duration.

The length of the duration is stored using two fields - seconds and nanoseconds. The nanoseconds part is a value from 0 to 999,999,999 that is an adjustment to the length in seconds. The total duration is defined by calling this method and [getNano()](Duration.md)).

A`Duration`represents a directed distance between two points on the time-line. A negative duration is expressed by the negative sign of the seconds part. A duration of -1 nanosecond is stored as -1 seconds plus 999,999,999 nanoseconds.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the whole seconds part of the length of the duration, positive or negative |

### getUnits

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUnits(): MutableList<TemporalUnit!>!
```

Gets the set of units supported by this duration.

The supported units are [SECONDS](../java.time.temporal/ChronoUnit.md), and [NANOS](../java.time.temporal/ChronoUnit.md). They are returned in the order seconds, nanos.

This set can be used in conjunction with [get(java.time.temporal.TemporalUnit)](Duration.md))to access the entire state of the duration.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TemporalUnit](../java.time.temporal/TemporalUnit.md)!>! | a list containing the seconds and nanos units, not null |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

A hash code for this duration.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a suitable hash code |

### isNegative

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isNegative(): Boolean
```

Checks if this duration is negative, excluding zero.

A`Duration`represents a directed distance between two points on the time-line and can therefore be positive, zero or negative. This method checks whether the length is less than zero.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this duration has a total length less than zero |

### isPositive

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPositive(): Boolean
```

Checks if this duration is positive, excluding zero.

A`Duration`represents a directed distance between two points on the time-line and can therefore be positive, zero or negative. This method checks whether the length is greater than zero.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this duration has a total length greater than zero |

### isZero

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isZero(): Boolean
```

Checks if this duration is zero length.

A`Duration`represents a directed distance between two points on the time-line and can therefore be positive, zero or negative. This method checks whether the length is zero.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this duration has a total length equal to zero |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(duration: Duration!): Duration!
```

Returns a copy of this duration with the specified duration subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Duration](Duration.md)!:the duration to subtract, positive or negative, not null |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified duration subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): Duration!
```

Returns a copy of this duration with the specified duration subtracted.

The duration amount is measured in terms of the specified unit. Only a subset of units are accepted by this method. The unit must either have an [exact duration](../java.time.temporal/TemporalUnit.md))or be [ChronoUnit.DAYS](../java.time.temporal/ChronoUnit.md) which is treated as 24 hours. Other units throw an exception.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount to subtract, measured in terms of the unit, positive or negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit that the amount is measured in, must have an exact duration, not null |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified duration subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusDays(daysToSubtract: Long): Duration!
```

Returns a copy of this duration with the specified duration in standard 24 hour days subtracted.

The number of days is multiplied by 86400 to obtain the number of seconds to subtract. This is based on the standard definition of a day as 24 hours.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| `daysToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the days to subtract, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified days subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusHours(hoursToSubtract: Long): Duration!
```

Returns a copy of this duration with the specified duration in hours subtracted.

The number of hours is multiplied by 3600 to obtain the number of seconds to subtract.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| `hoursToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the hours to subtract, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified hours subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusMillis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusMillis(millisToSubtract: Long): Duration!
```

Returns a copy of this duration with the specified duration in milliseconds subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `millisToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the milliseconds to subtract, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified milliseconds subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusMinutes(minutesToSubtract: Long): Duration!
```

Returns a copy of this duration with the specified duration in minutes subtracted.

The number of hours is multiplied by 60 to obtain the number of seconds to subtract.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| `minutesToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minutes to subtract, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified minutes subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusNanos(nanosToSubtract: Long): Duration!
```

Returns a copy of this duration with the specified duration in nanoseconds subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `nanosToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the nanoseconds to subtract, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified nanoseconds subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusSeconds(secondsToSubtract: Long): Duration!
```

Returns a copy of this duration with the specified duration in seconds subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| `secondsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the seconds to subtract, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified seconds subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### multipliedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun multipliedBy(multiplicand: Long): Duration!
```

Returns a copy of this duration multiplied by the scalar.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `multiplicand` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to multiply the duration by, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration multiplied by the specified scalar, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### negated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun negated(): Duration!
```

Returns a copy of this duration with the length negated.

This method swaps the sign of the total length of this duration. For example,`PT1.3S`will be returned as`PT-1.3S`.

This instance is immutable and unaffected by this method call.

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the amount negated, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    amount: Long, 
    unit: TemporalUnit!
): Duration!
```

Obtains a`Duration`representing an amount in the specified unit.

The parameters represent the two parts of a phrase like '6 Hours'. For example: 

```kotlin
Duration.of(3, SECONDS);
   Duration.of(465, HOURS);
  
```
Only a subset of units are accepted by this method. The unit must either have an [exact duration](../java.time.temporal/TemporalUnit.md))or be [ChronoUnit.DAYS](../java.time.temporal/ChronoUnit.md) which is treated as 24 hours. Other units throw an exception.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the duration, measured in terms of the unit, positive or negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit that the duration is measured in, must have an exact duration, not null |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

| Exceptions ||
|---------------------------------|----------------------------------------------|
| `java.time.DateTimeException` | if the period unit has an estimated duration |
| `java.lang.ArithmeticException` | if a numeric overflow occurs |

### ofDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofDays(days: Long): Duration!
```

Obtains a`Duration`representing a number of standard 24 hour days.

The seconds are calculated based on the standard definition of a day, where each day is 86400 seconds which implies a 24 hour day. The nanosecond in second field is set to zero.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `days` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of days, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

| Exceptions ||
|---------------------------------|-----------------------------------------------------|
| `java.lang.ArithmeticException` | if the input days exceeds the capacity of`Duration` |

### ofHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofHours(hours: Long): Duration!
```

Obtains a`Duration`representing a number of standard hours.

The seconds are calculated based on the standard definition of an hour, where each hour is 3600 seconds. The nanosecond in second field is set to zero.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `hours` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of hours, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

| Exceptions ||
|---------------------------------|------------------------------------------------------|
| `java.lang.ArithmeticException` | if the input hours exceeds the capacity of`Duration` |

### ofMillis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofMillis(millis: Long): Duration!
```

Obtains a`Duration`representing a number of milliseconds.

The seconds and nanoseconds are extracted from the specified milliseconds.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of milliseconds, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

### ofMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofMinutes(minutes: Long): Duration!
```

Obtains a`Duration`representing a number of standard minutes.

The seconds are calculated based on the standard definition of a minute, where each minute is 60 seconds. The nanosecond in second field is set to zero.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------|
| `minutes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of minutes, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

| Exceptions ||
|---------------------------------|--------------------------------------------------------|
| `java.lang.ArithmeticException` | if the input minutes exceeds the capacity of`Duration` |

### ofNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofNanos(nanos: Long): Duration!
```

Obtains a`Duration`representing a number of nanoseconds.

The seconds and nanoseconds are extracted from the specified nanoseconds.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `nanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of nanoseconds, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

### ofSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofSeconds(seconds: Long): Duration!
```

Obtains a`Duration`representing a number of seconds.

The nanosecond in second field is set to zero.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of seconds, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

### ofSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofSeconds(
    seconds: Long, 
    nanoAdjustment: Long
): Duration!
```

Obtains a`Duration`representing a number of seconds and an adjustment in nanoseconds.

This method allows an arbitrary number of nanoseconds to be passed in. The factory will alter the values of the second and nanosecond in order to ensure that the stored nanosecond is in the range 0 to 999,999,999. For example, the following will result in exactly the same duration: 

```kotlin
Duration.ofSeconds(3, 1);
   Duration.ofSeconds(4, -999_999_999);
   Duration.ofSeconds(2, 1000_000_001);
  
```

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of seconds, positive or negative |
| `nanoAdjustment` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the nanosecond adjustment to the number of seconds, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [Duration](Duration.md)! | a`Duration`, not null |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if the adjustment causes the seconds to exceed the capacity of`Duration` |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(text: CharSequence!): Duration!
```

Obtains a`Duration`from a text string such as`PnDTnHnMn.nS`.

This will parse a textual representation of a duration, including the string produced by`toString()`. The formats accepted are based on the ISO-8601 duration format`PnDTnHnMn.nS`with days considered to be exactly 24 hours.

The string starts with an optional sign, denoted by the ASCII negative or positive symbol. If negative, the whole period is negated. The ASCII letter "P" is next in upper or lower case. There are then four sections, each consisting of a number and a suffix. The sections have suffixes in ASCII of "D", "H", "M" and "S" for days, hours, minutes and seconds, accepted in upper or lower case. The suffixes must occur in order. The ASCII letter "T" must occur before the first occurrence, if any, of an hour, minute or second section. At least one of the four sections must be present, and if "T" is present there must be at least one section after the "T". The number part of each section must consist of one or more ASCII digits. The number may be prefixed by the ASCII negative or positive symbol. The number of days, hours and minutes must parse to an`long`. The number of seconds must parse to an`long`with optional fraction. The decimal point may be either a dot or a comma. The fractional part may have from zero to 9 digits.

The leading plus/minus sign, and negative values for other units are not part of the ISO-8601 standard.

Examples: 

```kotlin
"PT20.345S" -- parses as "20.345 seconds"
     "PT15M"     -- parses as "15 minutes" (where a minute is 60 seconds)
     "PT10H"     -- parses as "10 hours" (where an hour is 3600 seconds)
     "P2D"       -- parses as "2 days" (where a day is 24 hours or 86400 seconds)
     "P2DT3H4M"  -- parses as "2 days, 3 hours and 4 minutes"
     "P-6H3M"    -- parses as "-6 hours and +3 minutes"
     "-P6H3M"    -- parses as "-6 hours and -3 minutes"
     "-P-6H+3M"  -- parses as "+6 hours and -3 minutes"
  
```

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to parse, not null |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------|
| [Duration](Duration.md)! | the parsed duration, not null |

| Exceptions ||
|-------------------------------------------|--------------------------------------------|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed to a duration |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(duration: Duration!): Duration!
```

Returns a copy of this duration with the specified duration added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Duration](Duration.md)!:the duration to add, positive or negative, not null |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified duration added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): Duration!
```

Returns a copy of this duration with the specified duration added.

The duration amount is measured in terms of the specified unit. Only a subset of units are accepted by this method. The unit must either have an [exact duration](../java.time.temporal/TemporalUnit.md))or be [ChronoUnit.DAYS](../java.time.temporal/ChronoUnit.md) which is treated as 24 hours. Other units throw an exception.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount to add, measured in terms of the unit, positive or negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit that the amount is measured in, must have an exact duration, not null |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified duration added, not null |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusDays(daysToAdd: Long): Duration!
```

Returns a copy of this duration with the specified duration in standard 24 hour days added.

The number of days is multiplied by 86400 to obtain the number of seconds to add. This is based on the standard definition of a day as 24 hours.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------|
| `daysToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the days to add, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified days added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusHours(hoursToAdd: Long): Duration!
```

Returns a copy of this duration with the specified duration in hours added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `hoursToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the hours to add, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified hours added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusMillis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusMillis(millisToAdd: Long): Duration!
```

Returns a copy of this duration with the specified duration in milliseconds added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| `millisToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the milliseconds to add, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified milliseconds added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusMinutes(minutesToAdd: Long): Duration!
```

Returns a copy of this duration with the specified duration in minutes added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| `minutesToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minutes to add, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified minutes added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusNanos(nanosToAdd: Long): Duration!
```

Returns a copy of this duration with the specified duration in nanoseconds added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| `nanosToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the nanoseconds to add, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified nanoseconds added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusSeconds(secondsToAdd: Long): Duration!
```

Returns a copy of this duration with the specified duration in seconds added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| `secondsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the seconds to add, positive or negative |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the specified seconds added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### subtractFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun subtractFrom(temporal: Temporal!): Temporal!
```

Subtracts this duration from the specified temporal object.

This returns a temporal object of the same observable type as the input with this duration subtracted.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.minus(TemporalAmount)](../java.time.temporal/Temporal.md)). 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    dateTime = thisDuration.subtractFrom(dateTime);
    dateTime = dateTime.minus(thisDuration);
  
```

The calculation will subtract the seconds, then nanos. Only non-zero amounts will be added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java.time.temporal/Temporal.md)!:the temporal object to adjust, not null |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Temporal](../java.time.temporal/Temporal.md)! | an object of the same type with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to subtract |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### toDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDays(): Long
```

Gets the number of days in this duration.

This returns the total number of days in the duration by dividing the number of seconds by 86400. This is based on the standard definition of a day as 24 hours.

This instance is immutable and unaffected by this method call.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of days in the duration, may be negative |

### toDaysPart

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDaysPart(): Long
```

Extracts the number of days in the duration.

This returns the total number of days in the duration by dividing the number of seconds by 86400. This is based on the standard definition of a day as 24 hours.

This instance is immutable and unaffected by this method call.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of days in the duration, may be negative |

### toHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHours(): Long
```

Gets the number of hours in this duration.

This returns the total number of hours in the duration by dividing the number of seconds by 3600.

This instance is immutable and unaffected by this method call.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of hours in the duration, may be negative |

### toHoursPart

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHoursPart(): Int
```

Extracts the number of hours part in the duration.

This returns the number of remaining hours when dividing [toHours](Duration.md))by hours in a day. This is based on the standard definition of a day as 24 hours.

This instance is immutable and unaffected by this method call.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of hours part in the duration, may be negative |

### toMillis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMillis(): Long
```

Converts this duration to the total length in milliseconds.

If this duration is too large to fit in a`long`milliseconds, then an exception is thrown.

If this duration has greater than millisecond precision, then the conversion will drop any excess precision information as though the amount in nanoseconds was subject to integer division by one million.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total length of the duration in milliseconds |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### toMillisPart

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMillisPart(): Int
```

Extracts the number of milliseconds part of the duration.

This returns the milliseconds part by dividing the number of nanoseconds by 1,000,000. The length of the duration is stored using two fields - seconds and nanoseconds. The nanoseconds part is a value from 0 to 999,999,999 that is an adjustment to the length in seconds. The total duration is defined by calling [getNano()](Duration.md))and [getSeconds()](Duration.md)).

This instance is immutable and unaffected by this method call.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of milliseconds part of the duration. |

### toMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMinutes(): Long
```

Gets the number of minutes in this duration.

This returns the total number of minutes in the duration by dividing the number of seconds by 60.

This instance is immutable and unaffected by this method call.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of minutes in the duration, may be negative |

### toMinutesPart

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMinutesPart(): Int
```

Extracts the number of minutes part in the duration.

This returns the number of remaining minutes when dividing [toMinutes](Duration.md))by minutes in an hour. This is based on the standard definition of an hour as 60 minutes.

This instance is immutable and unaffected by this method call.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of minutes parts in the duration, may be negative |

### toNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toNanos(): Long
```

Converts this duration to the total length in nanoseconds expressed as a`long`.

If this duration is too large to fit in a`long`nanoseconds, then an exception is thrown.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total length of the duration in nanoseconds |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### toNanosPart

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toNanosPart(): Int
```

Get the nanoseconds part within seconds of the duration.

The length of the duration is stored using two fields - seconds and nanoseconds. The nanoseconds part is a value from 0 to 999,999,999 that is an adjustment to the length in seconds. The total duration is defined by calling [getNano()](Duration.md))and [getSeconds()](Duration.md)).

This instance is immutable and unaffected by this method call.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the nanoseconds within the second part of the length of the duration, from 0 to 999,999,999 |

### toSeconds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toSeconds(): Long
```

Gets the number of seconds in this duration.

This returns the total number of whole seconds in the duration.

This instance is immutable and unaffected by this method call.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the whole seconds part of the length of the duration, positive or negative |

### toSecondsPart

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toSecondsPart(): Int
```

Extracts the number of seconds part in the duration.

This returns the remaining seconds when dividing [toSeconds](Duration.md))by seconds in a minute. This is based on the standard definition of a minute as 60 seconds.

This instance is immutable and unaffected by this method call.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of seconds parts in the duration, may be negative |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

A string representation of this duration using ISO-8601 seconds based representation, such as`PT8H6M12.345S`.

The format of the returned string will be`PTnHnMnS`, where n is the relevant hours, minutes or seconds part of the duration. Any fractional seconds are placed after a decimal point in the seconds section. If a section has a zero value, it is omitted. The hours, minutes and seconds will all have the same sign.

Examples: 

```kotlin
"20.345 seconds"                 -- "PT20.345S
     "15 minutes" (15 * 60 seconds)   -- "PT15M"
     "10 hours" (10 * 3600 seconds)   -- "PT10H"
     "2 days" (2 * 86400 seconds)     -- "PT48H"
  
```
Note that multiples of 24 hours are not output as days to avoid confusion with`Period`.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | an ISO-8601 representation of this duration, not null |

### truncatedTo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun truncatedTo(unit: TemporalUnit!): Duration!
```

Returns a copy of this`Duration`truncated to the specified unit.

Truncating the duration returns a copy of the original with conceptual fields smaller than the specified unit set to zero. For example, truncating with the [MINUTES](../java.time.temporal/ChronoUnit.md) unit will round down towards zero to the nearest minute, setting the seconds and nanoseconds to zero.

The unit must have a [duration](../java.time.temporal/TemporalUnit.md))that divides into the length of a standard day without remainder. This includes all [java.time.temporal.ChronoUnit#isTimeBased()](../java.time.temporal/ChronoUnit.md))} and [DAYS](../java.time.temporal/ChronoUnit.md). Other ChronoUnits throw an exception.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit to truncate to, not null |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this duration with the time truncated, not null |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------|
| `java.time.DateTimeException` | if the unit is invalid for truncation |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### withNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withNanos(nanoOfSecond: Int): Duration!
```

Returns a copy of this duration with the specified nano-of-second.

This returns a duration with the specified nano-of-second, retaining the seconds part of this duration.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `nanoOfSecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the nano-of-second to represent, from 0 to 999,999,999 |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this period with the requested nano-of-second, not null |

| Exceptions ||
|-------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the nano-of-second is invalid |

### withSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withSeconds(seconds: Long): Duration!
```

Returns a copy of this duration with the specified amount of seconds.

This returns a duration with the specified seconds, retaining the nano-of-second part of this duration.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the seconds to represent, may be negative |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Duration](Duration.md)! | a`Duration`based on this period with the requested seconds, not null |

## Properties

### ZERO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ZERO: Duration!
```

Constant for a duration of zero.
