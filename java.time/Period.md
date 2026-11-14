# Period

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Period

```
class Period : ChronoPeriod, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.Period](../java/time/Period.md) |

A date-based amount of time in the ISO-8601 calendar system, such as '2 years, 3 months and 4 days'.

This class models a quantity or amount of time in terms of years, months and days. See [Duration](../java/time/Duration.md) for the time-based equivalent to this class.

Durations and periods differ in their treatment of daylight savings time when added to [ZonedDateTime](../java/time/ZonedDateTime.md). A`Duration`will add an exact number of seconds, thus a duration of one day is always exactly 24 hours. By contrast, a`Period`will add a conceptual day, trying to maintain the local time.

For example, consider adding a period of one day and a duration of one day to 18:00 on the evening before a daylight savings gap. The`Period`will add the conceptual day and result in a`ZonedDateTime`at 18:00 the following day. By contrast, the`Duration`will add exactly 24 hours, resulting in a`ZonedDateTime`at 19:00 the following day (assuming a one hour DST gap).

The supported units of a period are [YEARS](../java/time/temporal/ChronoUnit.md), [MONTHS](../java/time/temporal/ChronoUnit.md) and [DAYS](../java/time/temporal/ChronoUnit.md). All three fields are always present, but may be set to zero.

The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. It is equivalent to the proleptic Gregorian calendar system, in which today's rules for leap years are applied for all time.

The period is modeled as a directed amount of time, meaning that individual parts of the period may be negative.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | [addTo](../java/time/Period.md))`(`temporal:` ` [Temporal](../java/time/temporal/Temporal.md)!`)` Adds this period to the specified temporal object. |
| static [Period](../java/time/Period.md)! | [between](../java/time/Period.md))`(`startDateInclusive:` ` [LocalDate](../java/time/LocalDate.md)!`, `endDateExclusive:` ` [LocalDate](../java/time/LocalDate.md)!`)` Obtains a`Period`consisting of the number of years, months, and days between two dates. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/time/Period.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this period is equal to another period. |
| --- | --- |
| static [Period](../java/time/Period.md)! | [from](../java/time/Period.md))`(`amount:` ` [TemporalAmount](../java/time/temporal/TemporalAmount.md)!`)` Obtains an instance of`Period`from a temporal amount. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](../java/time/Period.md))`(`unit:` ` [TemporalUnit](../java/time/temporal/TemporalUnit.md)!`)` Gets the value of the requested unit. |
| [IsoChronology](../java/time/chrono/IsoChronology.md)! | [getChronology](../java/time/Period.md))`()` Gets the chronology of this period, which is the ISO calendar system. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDays](../java/time/Period.md))`()` Gets the amount of days of this period. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMonths](../java/time/Period.md))`()` Gets the amount of months of this period. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TemporalUnit](../java/time/temporal/TemporalUnit.md)!\>! | [getUnits](../java/time/Period.md))`()` Gets the set of units supported by this period. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYears](../java/time/Period.md))`()` Gets the amount of years of this period. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/time/Period.md))`()` A hash code for this period. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNegative](../java/time/Period.md))`()` Checks if any of the three units of this period are negative. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isZero](../java/time/Period.md))`()` Checks if all three units of this period are zero. |
| [Period](../java/time/Period.md)! | [minus](../java/time/Period.md))`(`amountToSubtract:` ` [TemporalAmount](../java/time/temporal/TemporalAmount.md)!`)` Returns a copy of this period with the specified period subtracted. |
| [Period](../java/time/Period.md)! | [minusDays](../java/time/Period.md))`(`daysToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this period with the specified days subtracted. |
| --- | --- |
| [Period](../java/time/Period.md)! | [minusMonths](../java/time/Period.md))`(`monthsToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this period with the specified months subtracted. |
| [Period](../java/time/Period.md)! | [minusYears](../java/time/Period.md))`(`yearsToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this period with the specified years subtracted. |
| [Period](../java/time/Period.md)! | [multipliedBy](../java/time/Period.md))`(`scalar:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a new instance with each element in this period multiplied by the specified scalar. |
| --- | --- |
| [Period](../java/time/Period.md)! | [negated](../java/time/Period.md))`()` Returns a new instance with each amount in this period negated. |
| [Period](../java/time/Period.md)! | [normalized](../java/time/Period.md))`()` Returns a copy of this period with the years and months normalized. |
| static [Period](../java/time/Period.md)! | [of](../java/time/Period.md))`(`years:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `months:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `days:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`Period`representing a number of years, months and days. |
| --- | --- |
| static [Period](../java/time/Period.md)! | [ofDays](../java/time/Period.md))`(`days:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`Period`representing a number of days. |
| static [Period](../java/time/Period.md)! | [ofMonths](../java/time/Period.md))`(`months:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`Period`representing a number of months. |
| static [Period](../java/time/Period.md)! | [ofWeeks](../java/time/Period.md))`(`weeks:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`Period`representing a number of weeks. |
| --- | --- |
| static [Period](../java/time/Period.md)! | [ofYears](../java/time/Period.md))`(`years:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`Period`representing a number of years. |
| static [Period](../java/time/Period.md)! | [parse](../java/time/Period.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Obtains a`Period`from a text string such as`PnYnMnD`. |
| [Period](../java/time/Period.md)! | [plus](../java/time/Period.md))`(`amountToAdd:` ` [TemporalAmount](../java/time/temporal/TemporalAmount.md)!`)` Returns a copy of this period with the specified period added. |
| --- | --- |
| [Period](../java/time/Period.md)! | [plusDays](../java/time/Period.md))`(`daysToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this period with the specified days added. |
| [Period](../java/time/Period.md)! | [plusMonths](../java/time/Period.md))`(`monthsToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this period with the specified months added. |
| [Period](../java/time/Period.md)! | [plusYears](../java/time/Period.md))`(`yearsToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this period with the specified years added. |
| --- | --- |
| [Temporal](../java/time/temporal/Temporal.md)! | [subtractFrom](../java/time/Period.md))`(`temporal:` ` [Temporal](../java/time/temporal/Temporal.md)!`)` Subtracts this period from the specified temporal object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/time/Period.md))`()` Outputs this period as a`String`, such as`P6Y3M1D`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toTotalMonths](../java/time/Period.md))`()` Gets the total number of months in this period. |
| --- | --- |
| [Period](../java/time/Period.md)! | [withDays](../java/time/Period.md))`(`days:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this period with the specified amount of days. |
| [Period](../java/time/Period.md)! | [withMonths](../java/time/Period.md))`(`months:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this period with the specified amount of months. |
| [Period](../java/time/Period.md)! | [withYears](../java/time/Period.md))`(`years:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a copy of this period with the specified amount of years. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Period](../java/time/Period.md)! | [ZERO](../java/time/Period.md) A constant for a period of zero. |

## Public methods

### addTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addTo(temporal: Temporal!): Temporal!
```

Adds this period to the specified temporal object.

This returns a temporal object of the same observable type as the input with this period added. If the temporal has a chronology, it must be the ISO chronology.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.plus(TemporalAmount)](../java/time/temporal/Temporal.md)). 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    dateTime = thisPeriod.addTo(dateTime);
    dateTime = dateTime.plus(thisPeriod);
  
```

The calculation operates as follows. First, the chronology of the temporal is checked to ensure it is ISO chronology or null. Second, if the months are zero, the years are added if non-zero, otherwise the combination of years and months is added if non-zero. Finally, any days are added.

This approach ensures that a partial period can be added to a partial date. For example, a period of years and/or months can be added to a`YearMonth`, but a period including days cannot. The approach also adds years and months together when necessary, which ensures correct behaviour at the end of the month.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java/time/temporal/Temporal.md)!:the temporal object to adjust, not null |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | an object of the same type with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to add |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### between

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun between(
    startDateInclusive: LocalDate!, 
    endDateExclusive: LocalDate!
): Period!
```

Obtains a`Period`consisting of the number of years, months, and days between two dates.

The start date is included, but the end date is not. The period is calculated by removing complete months, then calculating the remaining number of days, adjusting to ensure that both have the same sign. The number of months is then split into years and months based on a 12 month year. A month is considered if the end day-of-month is greater than or equal to the start day-of-month. For example, from`2010-01-15`to`2011-03-18`is one year, two months and three days.

The result of this method can be a negative period if the end is before the start. The negative sign will be the same in each of year, month and day.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| `startDateInclusive` | [LocalDate](../java/time/LocalDate.md)!:the start date, inclusive, not null |
| `endDateExclusive` | [LocalDate](../java/time/LocalDate.md)!:the end date, exclusive, not null |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------|
| [Period](../java/time/Period.md)! | the period between this date and the end date, not null |

**See Also**

- [java.time.chrono.ChronoLocalDate#until(ChronoLocalDate)](../java/time/chrono/ChronoLocalDate.md)) 

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Checks if this period is equal to another period.

The comparison is based on the type`Period`and each of the three amounts. To be equal, the years, months and days units must be individually equal. Note that this means that a period of "15 Months" is not equal to a period of "1 Year and 3 Months".

| Parameters ||
|-------|-----------------------------------------|
| `obj` | the object to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is equal to the other period |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun from(amount: TemporalAmount!): Period!
```

Obtains an instance of`Period`from a temporal amount.

This obtains a period based on the specified amount. A`TemporalAmount`represents an amount of time, which may be date-based or time-based, which this factory extracts to a`Period`.

The conversion loops around the set of units from the amount and uses the [YEARS](../java/time/temporal/ChronoUnit.md), [MONTHS](../java/time/temporal/ChronoUnit.md) and [DAYS](../java/time/temporal/ChronoUnit.md) units to create a period. If any other units are found then an exception is thrown.

If the amount is a`ChronoPeriod`then it must use the ISO chronology.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](../java/time/temporal/TemporalAmount.md)!:the temporal amount to convert, not null |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------|
| [Period](../java/time/Period.md)! | the equivalent period, not null |

| Exceptions ||
|---------------------------------|-------------------------------------------------------|
| `java.time.DateTimeException` | if unable to convert to a`Period` |
| `java.lang.ArithmeticException` | if the amount of years, months or days exceeds an int |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(unit: TemporalUnit!): Long
```

Gets the value of the requested unit.

This returns a value for each of the three supported units, [YEARS](../java/time/temporal/ChronoUnit.md), [MONTHS](../java/time/temporal/ChronoUnit.md) and [DAYS](../java/time/temporal/ChronoUnit.md). All other units throw an exception.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](../java/time/temporal/TemporalUnit.md)!:the`TemporalUnit`for which to return the value |

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
fun getChronology(): IsoChronology!
```

Gets the chronology of this period, which is the ISO calendar system.

The`Chronology`represents the calendar system in use. The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. It is equivalent to the proleptic Gregorian calendar system, in which today's rules for leap years are applied for all time.

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------|
| [IsoChronology](../java/time/chrono/IsoChronology.md)! | the ISO chronology, not null |

### getDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDays(): Int
```

Gets the amount of days of this period.

This returns the days unit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of days of this period, may be negative |

### getMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMonths(): Int
```

Gets the amount of months of this period.

This returns the months unit.

The months unit is not automatically normalized with the years unit. This means that a period of "15 months" is different to a period of "1 year and 3 months".

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of months of this period, may be negative |

### getUnits

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUnits(): MutableList<TemporalUnit!>!
```

Gets the set of units supported by this period.

The supported units are [YEARS](../java/time/temporal/ChronoUnit.md), [MONTHS](../java/time/temporal/ChronoUnit.md) and [DAYS](../java/time/temporal/ChronoUnit.md). They are returned in the order years, months, days.

This set can be used in conjunction with #get(java.time.temporal.TemporalUnit) to access the entire state of the period.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TemporalUnit](../java/time/temporal/TemporalUnit.md)!>! | a list containing the years, months and days units, not null |

### getYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getYears(): Int
```

Gets the amount of years of this period.

This returns the years unit.

The months unit is not automatically normalized with the years unit. This means that a period of "15 months" is different to a period of "1 year and 3 months".

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of years of this period, may be negative |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

A hash code for this period.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a suitable hash code |

### isNegative

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isNegative(): Boolean
```

Checks if any of the three units of this period are negative.

This checks whether the years, months or days units are less than zero.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any unit of this period is negative |

### isZero

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isZero(): Boolean
```

Checks if all three units of this period are zero.

A zero period has the value zero for the years, months and days units.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this period is zero-length |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(amountToSubtract: TemporalAmount!): Period!
```

Returns a copy of this period with the specified period subtracted.

This operates separately on the years, months and days. No normalization is performed.

For example, "1 year, 6 months and 3 days" minus "2 years, 2 months and 2 days" returns "-1 years, 4 months and 1 day".

The specified amount is typically an instance of`Period`. Other types are interpreted using [Period.from(TemporalAmount)](../java/time/Period.md)).

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [TemporalAmount](../java/time/temporal/TemporalAmount.md)!:the amount to subtract, not null |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the requested period subtracted, not null |

| Exceptions ||
|---------------------------------|------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the specified amount has a non-ISO chronology or contains an invalid unit |

### minusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusDays(daysToSubtract: Long): Period!
```

Returns a copy of this period with the specified days subtracted.

This subtracts the amount from the days unit in a copy of this period. The years and months units are unaffected. For example, "1 year, 6 months and 3 days" minus 2 days returns "1 year, 6 months and 1 day".

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `daysToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the months to subtract, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the specified days subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusMonths(monthsToSubtract: Long): Period!
```

Returns a copy of this period with the specified months subtracted.

This subtracts the amount from the months unit in a copy of this period. The years and days units are unaffected. For example, "1 year, 6 months and 3 days" minus 2 months returns "1 year, 4 months and 3 days".

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| `monthsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the years to subtract, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the specified months subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusYears(yearsToSubtract: Long): Period!
```

Returns a copy of this period with the specified years subtracted.

This subtracts the amount from the years unit in a copy of this period. The months and days units are unaffected. For example, "1 year, 6 months and 3 days" minus 2 years returns "-1 years, 6 months and 3 days".

This instance is immutable and unaffected by this method call.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| `yearsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the years to subtract, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the specified years subtracted, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### multipliedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun multipliedBy(scalar: Int): Period!
```

Returns a new instance with each element in this period multiplied by the specified scalar.

This returns a period with each of the years, months and days units individually multiplied. For example, a period of "2 years, -3 months and 4 days" multiplied by 3 will return "6 years, -9 months and 12 days". No normalization is performed.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `scalar` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the scalar to multiply by, not null |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the amounts multiplied by the scalar, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### negated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun negated(): Period!
```

Returns a new instance with each amount in this period negated.

This returns a period with each of the years, months and days units individually negated. For example, a period of "2 years, -3 months and 4 days" will be negated to "-2 years, 3 months and -4 days". No normalization is performed.

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the amounts negated, not null |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs, which only happens if one of the units has the value`Integer.MIN_VALUE` |

### normalized

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun normalized(): Period!
```

Returns a copy of this period with the years and months normalized.

This normalizes the years and months units, leaving the days unit unchanged. The months unit is adjusted to have an absolute value less than 12, with the years unit being adjusted to compensate. For example, a period of "1 Year and 15 months" will be normalized to "2 years and 3 months".

The sign of the years and months units will be the same after normalization. For example, a period of "1 year and -25 months" will be normalized to "-1 year and -1 month".

This instance is immutable and unaffected by this method call.

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with excess months normalized to years, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    years: Int, 
    months: Int, 
    days: Int
): Period!
```

Obtains a`Period`representing a number of years, months and days.

This creates an instance based on years, months and days.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `years` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of years, may be negative |
| `months` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of months, may be negative |
| `days` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of days, may be negative |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------|
| [Period](../java/time/Period.md)! | the period of years, months and days, not null |

### ofDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofDays(days: Int): Period!
```

Obtains a`Period`representing a number of days.

The resulting period will have the specified days. The years and months units will be zero.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `days` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of days, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|------------------------------|
| [Period](../java/time/Period.md)! | the period of days, not null |

### ofMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofMonths(months: Int): Period!
```

Obtains a`Period`representing a number of months.

The resulting period will have the specified months. The years and days units will be zero.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `months` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of months, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------|
| [Period](../java/time/Period.md)! | the period of months, not null |

### ofWeeks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofWeeks(weeks: Int): Period!
```

Obtains a`Period`representing a number of weeks.

The resulting period will be day-based, with the amount of days equal to the number of weeks multiplied by 7. The years and months units will be zero.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `weeks` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of weeks, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Period](../java/time/Period.md)! | the period, with the input weeks converted to days, not null |

### ofYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofYears(years: Int): Period!
```

Obtains a`Period`representing a number of years.

The resulting period will have the specified years. The months and days units will be zero.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `years` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of years, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------|
| [Period](../java/time/Period.md)! | the period of years, not null |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(text: CharSequence!): Period!
```

Obtains a`Period`from a text string such as`PnYnMnD`.

This will parse the string produced by`toString()`which is based on the ISO-8601 period formats`PnYnMnD`and`PnW`.

The string starts with an optional sign, denoted by the ASCII negative or positive symbol. If negative, the whole period is negated. The ASCII letter "P" is next in upper or lower case. There are then four sections, each consisting of a number and a suffix. At least one of the four sections must be present. The sections have suffixes in ASCII of "Y", "M", "W" and "D" for years, months, weeks and days, accepted in upper or lower case. The suffixes must occur in order. The number part of each section must consist of ASCII digits. The number may be prefixed by the ASCII negative or positive symbol. The number must parse to an`int`.

The leading plus/minus sign, and negative values for other units are not part of the ISO-8601 standard. In addition, ISO-8601 does not permit mixing between the`PnYnMnD`and`PnW`formats. Any week-based input is multiplied by 7 and treated as a number of days.

For example, the following are valid inputs: 

```kotlin
"P2Y"             -- Period.ofYears(2)
    "P3M"             -- Period.ofMonths(3)
    "P4W"             -- Period.ofWeeks(4)
    "P5D"             -- Period.ofDays(5)
    "P1Y2M3D"         -- Period.of(1, 2, 3)
    "P1Y2M3W4D"       -- Period.of(1, 2, 25)
    "P-1Y2M"          -- Period.of(-1, 2, 0)
    "-P1Y2M"          -- Period.of(-1, -2, 0)
  
```

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to parse, not null |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Period](../java/time/Period.md)! | the parsed period, not null |

| Exceptions ||
|-------------------------------------------|------------------------------------------|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed to a period |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(amountToAdd: TemporalAmount!): Period!
```

Returns a copy of this period with the specified period added.

This operates separately on the years, months and days. No normalization is performed.

For example, "1 year, 6 months and 3 days" plus "2 years, 2 months and 2 days" returns "3 years, 8 months and 5 days".

The specified amount is typically an instance of`Period`. Other types are interpreted using [Period.from(TemporalAmount)](../java/time/Period.md)).

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [TemporalAmount](../java/time/temporal/TemporalAmount.md)!:the amount to add, not null |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the requested period added, not null |

| Exceptions ||
|---------------------------------|------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the specified amount has a non-ISO chronology or contains an invalid unit |

### plusDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusDays(daysToAdd: Long): Period!
```

Returns a copy of this period with the specified days added.

This adds the amount to the days unit in a copy of this period. The years and months units are unaffected. For example, "1 year, 6 months and 3 days" plus 2 days returns "1 year, 6 months and 5 days".

This instance is immutable and unaffected by this method call.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------|
| `daysToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the days to add, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the specified days added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusMonths(monthsToAdd: Long): Period!
```

Returns a copy of this period with the specified months added.

This adds the amount to the months unit in a copy of this period. The years and days units are unaffected. For example, "1 year, 6 months and 3 days" plus 2 months returns "1 year, 8 months and 3 days".

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------|
| `monthsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the months to add, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the specified months added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusYears(yearsToAdd: Long): Period!
```

Returns a copy of this period with the specified years added.

This adds the amount to the years unit in a copy of this period. The months and days units are unaffected. For example, "1 year, 6 months and 3 days" plus 2 years returns "3 years, 6 months and 3 days".

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `yearsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the years to add, positive or negative |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the specified years added, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### subtractFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun subtractFrom(temporal: Temporal!): Temporal!
```

Subtracts this period from the specified temporal object.

This returns a temporal object of the same observable type as the input with this period subtracted. If the temporal has a chronology, it must be the ISO chronology.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.minus(TemporalAmount)](../java/time/temporal/Temporal.md)). 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    dateTime = thisPeriod.subtractFrom(dateTime);
    dateTime = dateTime.minus(thisPeriod);
  
```

The calculation operates as follows. First, the chronology of the temporal is checked to ensure it is ISO chronology or null. Second, if the months are zero, the years are subtracted if non-zero, otherwise the combination of years and months is subtracted if non-zero. Finally, any days are subtracted.

This approach ensures that a partial period can be subtracted from a partial date. For example, a period of years and/or months can be subtracted from a`YearMonth`, but a period including days cannot. The approach also subtracts years and months together when necessary, which ensures correct behaviour at the end of the month.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java/time/temporal/Temporal.md)!:the temporal object to adjust, not null |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | an object of the same type with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to subtract |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Outputs this period as a`String`, such as`P6Y3M1D`.

The output will be in the ISO-8601 period format. A zero period will be represented as zero days, 'P0D'.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this period, not null |

### toTotalMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toTotalMonths(): Long
```

Gets the total number of months in this period.

This returns the total number of months in the period by multiplying the number of years by 12 and adding the number of months.

This instance is immutable and unaffected by this method call.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total number of months in the period, may be negative |

### withDays

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withDays(days: Int): Period!
```

Returns a copy of this period with the specified amount of days.

This sets the amount of the days unit in a copy of this period. The years and months units are unaffected.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `days` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the days to represent, may be negative |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the requested days, not null |

### withMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withMonths(months: Int): Period!
```

Returns a copy of this period with the specified amount of months.

This sets the amount of the months unit in a copy of this period. The years and days units are unaffected.

The months unit is not automatically normalized with the years unit. This means that a period of "15 months" is different to a period of "1 year and 3 months".

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `months` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the months to represent, may be negative |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the requested months, not null |

### withYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withYears(years: Int): Period!
```

Returns a copy of this period with the specified amount of years.

This sets the amount of the years unit in a copy of this period. The months and days units are unaffected.

The months unit is not automatically normalized with the years unit. This means that a period of "15 months" is different to a period of "1 year and 3 months".

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `years` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the years to represent, may be negative |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Period](../java/time/Period.md)! | a`Period`based on this period with the requested years, not null |

## Properties

### ZERO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ZERO: Period!
```

A constant for a period of zero.
