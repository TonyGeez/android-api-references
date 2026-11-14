# TemporalAmount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalAmount

```
interface TemporalAmount
```

| [java.time.temporal.TemporalAmount](../java/time/temporal/TemporalAmount.md) |

| Known Direct Subclasses [ChronoPeriod](../java/time/chrono/ChronoPeriod.md), [Duration](../java/time/Duration.md) |----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [ChronoPeriod](../java/time/chrono/ChronoPeriod.md) | A date-based amount of time, such as '3 years, 4 months and 5 days' in an arbitrary chronology, intended for advanced globalization use cases. | | [Duration](../java/time/Duration.md) | A time-based amount of time, such as '34. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [Period](../java/time/Period.md) |---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------| | [Period](../java/time/Period.md) | A date-based amount of time in the ISO-8601 calendar system, such as '2 years, 3 months and 4 days'. | |
| --- | --- | --- | --- | --- | --- | --- |

Framework-level interface defining an amount of time, such as "6 hours", "8 days" or "2 years and 3 months".

This is the base interface type for amounts of time. An amount is distinct from a date or time-of-day in that it is not tied to any specific point on the time-line.

The amount can be thought of as a`Map`of [TemporalUnit](../java/time/temporal/TemporalUnit.md) to`long`, exposed via [getUnits()](../java/time/temporal/TemporalAmount.md))and [get(java.time.temporal.TemporalUnit)](../java/time/temporal/TemporalAmount.md)). A simple case might have a single unit-value pair, such as "6 hours". A more complex case may have multiple unit-value pairs, such as "7 years, 3 months and 5 days".

There are two common implementations. [Period](../java/time/Period.md) is a date-based implementation, storing years, months and days. [Duration](../java/time/Duration.md) is a time-based implementation, storing seconds and nanoseconds, but providing some access using other duration based units such as minutes, hours and fixed 24-hour days.

This interface is a framework-level interface that should not be widely used in application code. Instead, applications should create and pass around instances of concrete types, such as`Period`and`Duration`.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Temporal](../java/time/temporal/Temporal.md)! | [addTo](../java/time/temporal/TemporalAmount.md))`(`temporal:` ` [Temporal](../java/time/temporal/Temporal.md)!`)` Adds to the specified temporal object. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](../java/time/temporal/TemporalAmount.md))`(`unit:` ` [TemporalUnit](../java/time/temporal/TemporalUnit.md)!`)` Returns the value of the requested unit. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TemporalUnit](../java/time/temporal/TemporalUnit.md)!\>! | [getUnits](../java/time/temporal/TemporalAmount.md))`()` Returns the list of units uniquely defining the value of this TemporalAmount. |
| --- | --- |
| abstract [Temporal](../java/time/temporal/Temporal.md)! | [subtractFrom](../java/time/temporal/TemporalAmount.md))`(`temporal:` ` [Temporal](../java/time/temporal/Temporal.md)!`)` Subtracts this object from the specified temporal object. |

## Public methods

### addTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addTo(temporal: Temporal!): Temporal!
```

Adds to the specified temporal object.

Adds the amount to the specified temporal object using the logic encapsulated in the implementing class.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [Temporal.plus(TemporalAmount)](../java/time/temporal/Temporal.md)): 

```kotlin
// These two lines are equivalent, but the second approach is recommended
    dateTime = amount.addTo(dateTime);
    dateTime = dateTime.plus(adder);
  
```
It is recommended to use the second approach,`plus(TemporalAmount)`, as it is a lot clearer to read in code.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java/time/temporal/Temporal.md)!:the temporal object to add the amount to, not null |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | an object of the same observable type with the addition made, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to add |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(unit: TemporalUnit!): Long
```

Returns the value of the requested unit. The units returned from [getUnits()](../java/time/temporal/TemporalAmount.md))uniquely define the value of the`TemporalAmount`. A value must be returned for each unit listed in`getUnits`.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](../java/time/temporal/TemporalUnit.md)!:the`TemporalUnit`for which to return the value |

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the long value of the unit |

| Exceptions ||
|-------------------------------------------------------|--------------------------------------------|
| `java.time.DateTimeException` | if a value for the unit cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the`unit`is not supported |

### getUnits

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUnits(): MutableList<TemporalUnit!>!
```

Returns the list of units uniquely defining the value of this TemporalAmount. The list of`TemporalUnits`is defined by the implementation class. The list is a snapshot of the units at the time`getUnits`is called and is not mutable. The units are ordered from longest duration to the shortest duration of the unit.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TemporalUnit](../java/time/temporal/TemporalUnit.md)!>! | the List of`TemporalUnits`; not null |

### subtractFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subtractFrom(temporal: Temporal!): Temporal!
```

Subtracts this object from the specified temporal object.

Subtracts the amount from the specified temporal object using the logic encapsulated in the implementing class.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [Temporal.minus(TemporalAmount)](../java/time/temporal/Temporal.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    dateTime = amount.subtractFrom(dateTime);
    dateTime = dateTime.minus(amount);
  
```
It is recommended to use the second approach,`minus(TemporalAmount)`, as it is a lot clearer to read in code.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java/time/temporal/Temporal.md)!:the temporal object to subtract the amount from, not null |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | an object of the same observable type with the subtraction made, not null |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to subtract |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
