# TemporalAdjusters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalAdjusters

```
class TemporalAdjusters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.temporal.TemporalAdjusters](../java/time/temporal/TemporalAdjusters.md) |

Common and useful TemporalAdjusters.

Adjusters are a key tool for modifying temporal objects. They exist to externalize the process of adjustment, permitting different approaches, as per the strategy design pattern. Examples might be an adjuster that sets the date avoiding weekends, or one that sets the date to the last day of the month.

There are two equivalent ways of using a`TemporalAdjuster`. The first is to invoke the method on the interface directly. The second is to use [Temporal.with(TemporalAdjuster)](../java/time/temporal/Temporal.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisAdjuster.adjustInto(temporal);
    temporal = temporal.with(thisAdjuster);
  
```
It is recommended to use the second approach,`with(TemporalAdjuster)`, as it is a lot clearer to read in code.

This class contains a standard set of adjusters, available as static methods. These include:

- finding the first or last day of the month
- finding the first day of next month
- finding the first or last day of the year
- finding the first day of next year
- finding the first or last day-of-week within a month, such as "first Wednesday in June"
- finding the next or previous day-of-week, such as "next Thursday"

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [dayOfWeekInMonth](../java/time/temporal/TemporalAdjusters.md))`(`ordinal:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfWeek:` ` [DayOfWeek](../java/time/DayOfWeek.md)!`)` Returns the day-of-week in month adjuster, which returns a new date with the ordinal day-of-week based on the month. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [firstDayOfMonth](../java/time/temporal/TemporalAdjusters.md))`()` Returns the "first day of month" adjuster, which returns a new date set to the first day of the current month. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [firstDayOfNextMonth](../java/time/temporal/TemporalAdjusters.md))`()` Returns the "first day of next month" adjuster, which returns a new date set to the first day of the next month. |
| --- | --- |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [firstDayOfNextYear](../java/time/temporal/TemporalAdjusters.md))`()` Returns the "first day of next year" adjuster, which returns a new date set to the first day of the next year. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [firstDayOfYear](../java/time/temporal/TemporalAdjusters.md))`()` Returns the "first day of year" adjuster, which returns a new date set to the first day of the current year. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [firstInMonth](../java/time/temporal/TemporalAdjusters.md))`(`dayOfWeek:` ` [DayOfWeek](../java/time/DayOfWeek.md)!`)` Returns the first in month adjuster, which returns a new date in the same month with the first matching day-of-week. |
| --- | --- |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [lastDayOfMonth](../java/time/temporal/TemporalAdjusters.md))`()` Returns the "last day of month" adjuster, which returns a new date set to the last day of the current month. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [lastDayOfYear](../java/time/temporal/TemporalAdjusters.md))`()` Returns the "last day of year" adjuster, which returns a new date set to the last day of the current year. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [lastInMonth](../java/time/temporal/TemporalAdjusters.md))`(`dayOfWeek:` ` [DayOfWeek](../java/time/DayOfWeek.md)!`)` Returns the last in month adjuster, which returns a new date in the same month with the last matching day-of-week. |
| --- | --- |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [next](../java/time/temporal/TemporalAdjusters.md))`(`dayOfWeek:` ` [DayOfWeek](../java/time/DayOfWeek.md)!`)` Returns the next day-of-week adjuster, which adjusts the date to the first occurrence of the specified day-of-week after the date being adjusted. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [nextOrSame](../java/time/temporal/TemporalAdjusters.md))`(`dayOfWeek:` ` [DayOfWeek](../java/time/DayOfWeek.md)!`)` Returns the next-or-same day-of-week adjuster, which adjusts the date to the first occurrence of the specified day-of-week after the date being adjusted unless it is already on that day in which case the same object is returned. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [ofDateAdjuster](../java/time/temporal/TemporalAdjusters.md))`(`dateBasedAdjuster:` ` [UnaryOperator](../java/util/function/UnaryOperator.md)< [LocalDate](../java/time/LocalDate.md)!>!`)` Obtains a`TemporalAdjuster`that wraps a date adjuster. |
| --- | --- |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [previous](../java/time/temporal/TemporalAdjusters.md))`(`dayOfWeek:` ` [DayOfWeek](../java/time/DayOfWeek.md)!`)` Returns the previous day-of-week adjuster, which adjusts the date to the first occurrence of the specified day-of-week before the date being adjusted. |
| static [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | [previousOrSame](../java/time/temporal/TemporalAdjusters.md))`(`dayOfWeek:` ` [DayOfWeek](../java/time/DayOfWeek.md)!`)` Returns the previous-or-same day-of-week adjuster, which adjusts the date to the first occurrence of the specified day-of-week before the date being adjusted unless it is already on that day in which case the same object is returned. |

## Public methods

### dayOfWeekInMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun dayOfWeekInMonth(
    ordinal: Int, 
    dayOfWeek: DayOfWeek!
): TemporalAdjuster!
```

Returns the day-of-week in month adjuster, which returns a new date with the ordinal day-of-week based on the month. This is used for expressions like the 'second Tuesday in March'.

The ISO calendar system behaves as follows: 
The input 2011-12-15 for (1,TUESDAY) will return 2011-12-06. 
The input 2011-12-15 for (2,TUESDAY) will return 2011-12-13. 
The input 2011-12-15 for (3,TUESDAY) will return 2011-12-20. 
The input 2011-12-15 for (4,TUESDAY) will return 2011-12-27. 
The input 2011-12-15 for (5,TUESDAY) will return 2012-01-03. 
The input 2011-12-15 for (-1,TUESDAY) will return 2011-12-27 (last in month). 
The input 2011-12-15 for (-4,TUESDAY) will return 2011-12-06 (3 weeks before last in month). 
The input 2011-12-15 for (-5,TUESDAY) will return 2011-11-29 (4 weeks before last in month). 
The input 2011-12-15 for (0,TUESDAY) will return 2011-11-29 (last in previous month). 

For a positive or zero ordinal, the algorithm is equivalent to finding the first day-of-week that matches within the month and then adding a number of weeks to it. For a negative ordinal, the algorithm is equivalent to finding the last day-of-week that matches within the month and then subtracting a number of weeks to it. The ordinal number of weeks is not validated and is interpreted leniently according to this algorithm. This definition means that an ordinal of zero finds the last matching day-of-week in the previous month.

The behavior is suitable for use with most calendar systems. It uses the`DAY_OF_WEEK`and`DAY_OF_MONTH`fields and the`DAYS`unit, and assumes a seven day week.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `ordinal` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the week within the month, unbounded but typically from -5 to 5 |
| `dayOfWeek` | [DayOfWeek](../java/time/DayOfWeek.md)!:the day-of-week, not null |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the day-of-week in month adjuster, not null |

### firstDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun firstDayOfMonth(): TemporalAdjuster!
```

Returns the "first day of month" adjuster, which returns a new date set to the first day of the current month.

The ISO calendar system behaves as follows: 
The input 2011-01-15 will return 2011-01-01. 
The input 2011-02-15 will return 2011-02-01.

The behavior is suitable for use with most calendar systems. It is equivalent to: 

```kotlin
temporal.with(DAY_OF_MONTH, 1);
  
```

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the first day-of-month adjuster, not null |

### firstDayOfNextMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun firstDayOfNextMonth(): TemporalAdjuster!
```

Returns the "first day of next month" adjuster, which returns a new date set to the first day of the next month.

The ISO calendar system behaves as follows: 
The input 2011-01-15 will return 2011-02-01. 
The input 2011-02-15 will return 2011-03-01.

The behavior is suitable for use with most calendar systems. It is equivalent to: 

```kotlin
temporal.with(DAY_OF_MONTH, 1).plus(1, MONTHS);
  
```

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the first day of next month adjuster, not null |

### firstDayOfNextYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun firstDayOfNextYear(): TemporalAdjuster!
```

Returns the "first day of next year" adjuster, which returns a new date set to the first day of the next year.

The ISO calendar system behaves as follows: 
The input 2011-01-15 will return 2012-01-01.

The behavior is suitable for use with most calendar systems. It is equivalent to: 

```kotlin
temporal.with(DAY_OF_YEAR, 1).plus(1, YEARS);
  
```

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the first day of next month adjuster, not null |

### firstDayOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun firstDayOfYear(): TemporalAdjuster!
```

Returns the "first day of year" adjuster, which returns a new date set to the first day of the current year.

The ISO calendar system behaves as follows: 
The input 2011-01-15 will return 2011-01-01. 
The input 2011-02-15 will return 2011-01-01. 

The behavior is suitable for use with most calendar systems. It is equivalent to: 

```kotlin
temporal.with(DAY_OF_YEAR, 1);
  
```

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the first day-of-year adjuster, not null |

### firstInMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun firstInMonth(dayOfWeek: DayOfWeek!): TemporalAdjuster!
```

Returns the first in month adjuster, which returns a new date in the same month with the first matching day-of-week. This is used for expressions like 'first Tuesday in March'.

The ISO calendar system behaves as follows: 
The input 2011-12-15 for (MONDAY) will return 2011-12-05. 
The input 2011-12-15 for (FRIDAY) will return 2011-12-02. 

The behavior is suitable for use with most calendar systems. It uses the`DAY_OF_WEEK`and`DAY_OF_MONTH`fields and the`DAYS`unit, and assumes a seven day week.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------|
| `dayOfWeek` | [DayOfWeek](../java/time/DayOfWeek.md)!:the day-of-week, not null |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the first in month adjuster, not null |

### lastDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun lastDayOfMonth(): TemporalAdjuster!
```

Returns the "last day of month" adjuster, which returns a new date set to the last day of the current month.

The ISO calendar system behaves as follows: 
The input 2011-01-15 will return 2011-01-31. 
The input 2011-02-15 will return 2011-02-28. 
The input 2012-02-15 will return 2012-02-29 (leap year). 
The input 2011-04-15 will return 2011-04-30.

The behavior is suitable for use with most calendar systems. It is equivalent to: 

```kotlin
long lastDay = temporal.range(DAY_OF_MONTH).getMaximum();
   temporal.with(DAY_OF_MONTH, lastDay);
  
```

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the last day-of-month adjuster, not null |

### lastDayOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun lastDayOfYear(): TemporalAdjuster!
```

Returns the "last day of year" adjuster, which returns a new date set to the last day of the current year.

The ISO calendar system behaves as follows: 
The input 2011-01-15 will return 2011-12-31. 
The input 2011-02-15 will return 2011-12-31. 

The behavior is suitable for use with most calendar systems. It is equivalent to: 

```kotlin
long lastDay = temporal.range(DAY_OF_YEAR).getMaximum();
   temporal.with(DAY_OF_YEAR, lastDay);
  
```

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the last day-of-year adjuster, not null |

### lastInMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun lastInMonth(dayOfWeek: DayOfWeek!): TemporalAdjuster!
```

Returns the last in month adjuster, which returns a new date in the same month with the last matching day-of-week. This is used for expressions like 'last Tuesday in March'.

The ISO calendar system behaves as follows: 
The input 2011-12-15 for (MONDAY) will return 2011-12-26. 
The input 2011-12-15 for (FRIDAY) will return 2011-12-30. 

The behavior is suitable for use with most calendar systems. It uses the`DAY_OF_WEEK`and`DAY_OF_MONTH`fields and the`DAYS`unit, and assumes a seven day week.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------|
| `dayOfWeek` | [DayOfWeek](../java/time/DayOfWeek.md)!:the day-of-week, not null |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the first in month adjuster, not null |

### next

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun next(dayOfWeek: DayOfWeek!): TemporalAdjuster!
```

Returns the next day-of-week adjuster, which adjusts the date to the first occurrence of the specified day-of-week after the date being adjusted.

The ISO calendar system behaves as follows: 
The input 2011-01-15 (a Saturday) for parameter (MONDAY) will return 2011-01-17 (two days later). 
The input 2011-01-15 (a Saturday) for parameter (WEDNESDAY) will return 2011-01-19 (four days later). 
The input 2011-01-15 (a Saturday) for parameter (SATURDAY) will return 2011-01-22 (seven days later).

The behavior is suitable for use with most calendar systems. It uses the`DAY_OF_WEEK`field and the`DAYS`unit, and assumes a seven day week.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `dayOfWeek` | [DayOfWeek](../java/time/DayOfWeek.md)!:the day-of-week to move the date to, not null |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the next day-of-week adjuster, not null |

### nextOrSame

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun nextOrSame(dayOfWeek: DayOfWeek!): TemporalAdjuster!
```

Returns the next-or-same day-of-week adjuster, which adjusts the date to the first occurrence of the specified day-of-week after the date being adjusted unless it is already on that day in which case the same object is returned.

The ISO calendar system behaves as follows: 
The input 2011-01-15 (a Saturday) for parameter (MONDAY) will return 2011-01-17 (two days later). 
The input 2011-01-15 (a Saturday) for parameter (WEDNESDAY) will return 2011-01-19 (four days later). 
The input 2011-01-15 (a Saturday) for parameter (SATURDAY) will return 2011-01-15 (same as input).

The behavior is suitable for use with most calendar systems. It uses the`DAY_OF_WEEK`field and the`DAYS`unit, and assumes a seven day week.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `dayOfWeek` | [DayOfWeek](../java/time/DayOfWeek.md)!:the day-of-week to check for or move the date to, not null |

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the next-or-same day-of-week adjuster, not null |

### ofDateAdjuster

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofDateAdjuster(dateBasedAdjuster: UnaryOperator<LocalDate!>!): TemporalAdjuster!
```

Obtains a`TemporalAdjuster`that wraps a date adjuster.

The`TemporalAdjuster`is based on the low level`Temporal`interface. This method allows an adjustment from`LocalDate`to`LocalDate`to be wrapped to match the temporal-based interface. This is provided for convenience to make user-written adjusters simpler.

In general, user-written adjusters should be static constants: 

```kotlin
<code>static TemporalAdjuster TWO_DAYS_LATER =
        TemporalAdjusters.ofDateAdjuster(date -&gt; date.plusDays(2));
  </code>
```

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dateBasedAdjuster` | [UnaryOperator](../java/util/function/UnaryOperator.md)\< [LocalDate](../java/time/LocalDate.md)!\>!:the date-based adjuster, not null |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the temporal adjuster wrapping on the date adjuster, not null |

### previous

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun previous(dayOfWeek: DayOfWeek!): TemporalAdjuster!
```

Returns the previous day-of-week adjuster, which adjusts the date to the first occurrence of the specified day-of-week before the date being adjusted.

The ISO calendar system behaves as follows: 
The input 2011-01-15 (a Saturday) for parameter (MONDAY) will return 2011-01-10 (five days earlier). 
The input 2011-01-15 (a Saturday) for parameter (WEDNESDAY) will return 2011-01-12 (three days earlier). 
The input 2011-01-15 (a Saturday) for parameter (SATURDAY) will return 2011-01-08 (seven days earlier).

The behavior is suitable for use with most calendar systems. It uses the`DAY_OF_WEEK`field and the`DAYS`unit, and assumes a seven day week.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `dayOfWeek` | [DayOfWeek](../java/time/DayOfWeek.md)!:the day-of-week to move the date to, not null |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the previous day-of-week adjuster, not null |

### previousOrSame

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun previousOrSame(dayOfWeek: DayOfWeek!): TemporalAdjuster!
```

Returns the previous-or-same day-of-week adjuster, which adjusts the date to the first occurrence of the specified day-of-week before the date being adjusted unless it is already on that day in which case the same object is returned.

The ISO calendar system behaves as follows: 
The input 2011-01-15 (a Saturday) for parameter (MONDAY) will return 2011-01-10 (five days earlier). 
The input 2011-01-15 (a Saturday) for parameter (WEDNESDAY) will return 2011-01-12 (three days earlier). 
The input 2011-01-15 (a Saturday) for parameter (SATURDAY) will return 2011-01-15 (same as input).

The behavior is suitable for use with most calendar systems. It uses the`DAY_OF_WEEK`field and the`DAYS`unit, and assumes a seven day week.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `dayOfWeek` | [DayOfWeek](../java/time/DayOfWeek.md)!:the day-of-week to check for or move the date to, not null |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [TemporalAdjuster](../java/time/temporal/TemporalAdjuster.md)! | the previous-or-same day-of-week adjuster, not null |
