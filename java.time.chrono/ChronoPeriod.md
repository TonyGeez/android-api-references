# ChronoPeriod

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChronoPeriod

```
interface ChronoPeriod : TemporalAmount
```

| [java.time.chrono.ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#) |

| Known Direct Subclasses [Period](https://developer.android.com/reference/kotlin/java/time/Period.html#) |---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------| | [Period](https://developer.android.com/reference/kotlin/java/time/Period.html#) | A date-based amount of time in the ISO-8601 calendar system, such as '2 years, 3 months and 4 days'. | |
| --- | --- | --- | --- | --- | --- | --- |

A date-based amount of time, such as '3 years, 4 months and 5 days' in an arbitrary chronology, intended for advanced globalization use cases.

This interface models a date-based amount of time in a calendar system. While most calendar systems use years, months and days, some do not. Therefore, this interface operates solely in terms of a set of supported units that are defined by the`Chronology`. The set of supported units is fixed for a given chronology. The amount of a supported unit may be set to zero.

The period is modeled as a directed amount of time, meaning that individual parts of the period may be negative.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | [addTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#addTo(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`)` Adds this period to the specified temporal object. |
| openstatic [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | [between](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#between(java.time.chrono.ChronoLocalDate,%20java.time.chrono.ChronoLocalDate))`(`startDateInclusive:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!`, `endDateExclusive:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!`)` Obtains a`ChronoPeriod`consisting of amount of time between two dates. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#get(java.time.temporal.TemporalUnit))`(`unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` Gets the value of the requested unit. |
| --- | --- |
| abstract [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology)! | [getChronology](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#getChronology())`()` Gets the chronology that defines the meaning of the supported units. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!\>! | [getUnits](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#getUnits())`()` Gets the set of units supported by this period. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNegative](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#isNegative())`()` Checks if any of the supported units of this period are negative. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isZero](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#isZero())`()` Checks if all the supported units of this period are zero. |
| abstract [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | [minus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#minus(java.time.temporal.TemporalAmount))`(`amountToSubtract:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!`)` Returns a copy of this period with the specified period subtracted. |
| abstract [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | [multipliedBy](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#multipliedBy(kotlin.Int))`(`scalar:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a new instance with each amount in this period in this period multiplied by the specified scalar. |
| --- | --- |
| open [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | [negated](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#negated())`()` Returns a new instance with each amount in this period negated. |
| abstract [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | [normalized](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#normalized())`()` Returns a copy of this period with the amounts of each unit normalized. |
| abstract [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | [plus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#plus(java.time.temporal.TemporalAmount))`(`amountToAdd:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!`)` Returns a copy of this period with the specified period added. |
| --- | --- |
| abstract [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | [subtractFrom](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#subtractFrom(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`)` Subtracts this period from the specified temporal object. |

## Public methods

### addTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addTo(temporal: Temporal!): Temporal!
```

Adds this period to the specified temporal object.

This returns a temporal object of the same observable type as the input with this period added.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.plus(TemporalAmount)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#plus(java.time.temporal.TemporalAmount)). 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    dateTime = thisPeriod.addTo(dateTime);
    dateTime = dateTime.plus(thisPeriod);
  
```

The specified temporal must have the same chronology as this period. This returns a temporal with the non-zero supported units added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!:the temporal object to adjust, not null |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | an object of the same type with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to add |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### between

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun between(
    startDateInclusive: ChronoLocalDate!, 
    endDateExclusive: ChronoLocalDate!
): ChronoPeriod!
```

Obtains a`ChronoPeriod`consisting of amount of time between two dates.

The start date is included, but the end date is not. The period is calculated using [ChronoLocalDate.until(ChronoLocalDate)](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#until(java.time.chrono.ChronoLocalDate)). As such, the calculation is chronology specific.

The chronology of the first date is used. The chronology of the second date is ignored, with the date being converted to the target chronology system before the calculation starts.

The result of this method can be a negative period if the end is before the start. In most cases, the positive/negative sign will be the same in each of the supported fields.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startDateInclusive` | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!:the start date, inclusive, specifying the chronology of the calculation, not null |
| `endDateExclusive` | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!:the end date, exclusive, in any chronology, not null |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | the period between this date and the end date, not null |

**See Also**

- [java.time.chrono.ChronoLocalDate#until(ChronoLocalDate)](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#until(java.time.chrono.ChronoLocalDate)) 

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(unit: TemporalUnit!): Long
```

Gets the value of the requested unit.

The supported units are chronology specific. They will typically be [YEARS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#), [MONTHS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#) and [DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#). Requesting an unsupported unit will throw an exception.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the`TemporalUnit`for which to return the value |

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the long value of the unit |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if the unit is not supported |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChronology(): Chronology!
```

Gets the chronology that defines the meaning of the supported units.

The period is defined by the chronology. It controls the supported units and restricts addition/subtraction to`ChronoLocalDate`instances of the same chronology.

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------|
| [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology)! | the chronology defining the period, not null |

### getUnits

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUnits(): MutableList<TemporalUnit!>!
```

Gets the set of units supported by this period.

The supported units are chronology specific. They will typically be [YEARS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#), [MONTHS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#) and [DAYS](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#). They are returned in order from largest to smallest.

This set can be used in conjunction with [get(java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#get(java.time.temporal.TemporalUnit))to access the entire state of the period.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!>! | a list containing the supported units, not null |

### isNegative

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isNegative(): Boolean
```

Checks if any of the supported units of this period are negative.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any unit of this period is negative |

### isZero

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isZero(): Boolean
```

Checks if all the supported units of this period are zero.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this period is zero-length |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun minus(amountToSubtract: TemporalAmount!): ChronoPeriod!
```

Returns a copy of this period with the specified period subtracted.

If the specified amount is a`ChronoPeriod`then it must have the same chronology as this period. Implementations may choose to accept or reject other`TemporalAmount`implementations.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!:the period to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | a`ChronoPeriod`based on this period with the requested period subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### multipliedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun multipliedBy(scalar: Int): ChronoPeriod!
```

Returns a new instance with each amount in this period in this period multiplied by the specified scalar.

This returns a period with each supported unit individually multiplied. For example, a period of "2 years, -3 months and 4 days" multiplied by 3 will return "6 years, -9 months and 12 days". No normalization is performed.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `scalar` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the scalar to multiply by, not null |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | a`ChronoPeriod`based on this period with the amounts multiplied by the scalar, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### negated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun negated(): ChronoPeriod!
```

Returns a new instance with each amount in this period negated.

This returns a period with each supported unit individually negated. For example, a period of "2 years, -3 months and 4 days" will be negated to "-2 years, 3 months and -4 days". No normalization is performed.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | a`ChronoPeriod`based on this period with the amounts negated, not null |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs, which only happens if one of the units has the value`Long.MIN_VALUE` |

### normalized

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun normalized(): ChronoPeriod!
```

Returns a copy of this period with the amounts of each unit normalized.

The process of normalization is specific to each calendar system. For example, in the ISO calendar system, the years and months are normalized but the days are not, such that "15 months" would be normalized to "1 year and 3 months".

This instance is immutable and unaffected by this method call.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | a`ChronoPeriod`based on this period with the amounts of each unit normalized, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun plus(amountToAdd: TemporalAmount!): ChronoPeriod!
```

Returns a copy of this period with the specified period added.

If the specified amount is a`ChronoPeriod`then it must have the same chronology as this period. Implementations may choose to accept or reject other`TemporalAmount`implementations.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!:the period to add, not null |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod#)! | a`ChronoPeriod`based on this period with the requested period added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### subtractFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subtractFrom(temporal: Temporal!): Temporal!
```

Subtracts this period from the specified temporal object.

This returns a temporal object of the same observable type as the input with this period subtracted.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.minus(TemporalAmount)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#minus(java.time.temporal.TemporalAmount)). 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    dateTime = thisPeriod.subtractFrom(dateTime);
    dateTime = dateTime.minus(thisPeriod);
  
```

The specified temporal must have the same chronology as this period. This returns a temporal with the non-zero supported units subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!:the temporal object to adjust, not null |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | an object of the same type with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to subtract |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
