# JapaneseDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JapaneseDate

```
class JapaneseDate : ChronoLocalDate, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.chrono.JapaneseDate](JapaneseDate.md) |

A date in the Japanese Imperial calendar system.

This date operates using the [Japanese Imperial calendar](JapaneseChronology.md). This calendar system is primarily used in Japan.

The Japanese Imperial calendar system is the same as the ISO calendar system apart from the era-based year numbering. The proleptic-year is defined to be equal to the ISO proleptic-year.

Japan introduced the Gregorian calendar starting with Meiji 6. Only Meiji and later eras are supported; dates before Meiji 6, January 1 are not supported.

For example, the Japanese year "Heisei 24" corresponds to ISO year "2012". 
Calling`japaneseDate.get(YEAR_OF_ERA)`will return 24. 
Calling`japaneseDate.get(YEAR)`will return 2012. 
Calling`japaneseDate.get(ERA)`will return 2, corresponding to`JapaneseChronology.ERA_HEISEI`. 

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ChronoLocalDateTime](ChronoLocalDateTime.md)\< [JapaneseDate](JapaneseDate.md)!\>! | [atTime](JapaneseDate.md))`(`localTime:` ` [LocalTime](../java.time/LocalTime.md)!`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](JapaneseDate.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this date to another date, including the chronology. |
| static [JapaneseDate](JapaneseDate.md)! | [from](JapaneseDate.md))`(`temporal:` ` [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!`)` Obtains a`JapaneseDate`from a temporal object. |
| --- | --- |
| [JapaneseChronology](JapaneseChronology.md)! | [getChronology](JapaneseDate.md))`()` Gets the chronology of this date, which is the Japanese calendar system. |
| [JapaneseEra](JapaneseEra.md)! | [getEra](JapaneseDate.md))`()` Gets the era applicable at this date. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](JapaneseDate.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](JapaneseDate.md))`()` A hash code for this date. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](JapaneseDate.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` Checks if the specified field is supported. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lengthOfMonth](JapaneseDate.md))`()` Returns the length of the month represented by this date. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lengthOfYear](JapaneseDate.md))`()` <br /> |
| [JapaneseDate](JapaneseDate.md)! | [minus](JapaneseDate.md))`(`amount:` ` [TemporalAmount](../java.time.temporal/TemporalAmount.md)!`)` Returns an object of the same type as this object with an amount subtracted. |
| [JapaneseDate](JapaneseDate.md)! | [minus](JapaneseDate.md))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` <br /> |
| --- | --- |
| static [JapaneseDate](JapaneseDate.md)! | [now](JapaneseDate.md))`()` Obtains the current`JapaneseDate`from the system clock in the default time-zone. |
| static [JapaneseDate](JapaneseDate.md)! | [now](JapaneseDate.md))`(`clock:` ` [Clock](../java.time/Clock.md)!`)` Obtains the current`JapaneseDate`from the specified clock. |
| static [JapaneseDate](JapaneseDate.md)! | [now](JapaneseDate.md))`(`zone:` ` [ZoneId](../java.time/ZoneId.md)!`)` Obtains the current`JapaneseDate`from the system clock in the specified time-zone. |
| --- | --- |
| static [JapaneseDate](JapaneseDate.md)! | [of](JapaneseDate.md))`(`prolepticYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`JapaneseDate`representing a date in the Japanese calendar system from the proleptic-year, month-of-year and day-of-month fields. |
| static [JapaneseDate](JapaneseDate.md)! | [of](JapaneseDate.md))`(`era:` ` [JapaneseEra](JapaneseEra.md)!`, `yearOfEra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`JapaneseDate`representing a date in the Japanese calendar system from the era, year-of-era, month-of-year and day-of-month fields. |
| [JapaneseDate](JapaneseDate.md)! | [plus](JapaneseDate.md))`(`amount:` ` [TemporalAmount](../java.time.temporal/TemporalAmount.md)!`)` Returns an object of the same type as this object with an amount added. |
| --- | --- |
| [JapaneseDate](JapaneseDate.md)! | [plus](JapaneseDate.md))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` <br /> |
| [ValueRange](../java.time.temporal/ValueRange.md)! | [range](JapaneseDate.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toEpochDay](JapaneseDate.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](JapaneseDate.md))`()` <br /> |
| [ChronoPeriod](ChronoPeriod.md)! | [until](JapaneseDate.md))`(`endDate:` ` [ChronoLocalDate](ChronoLocalDate.md)!`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](JapaneseDate.md))`(`endExclusive:` ` [Temporal](../java.time.temporal/Temporal.md)!`, `unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` <br /> |
| --- | --- |
| [JapaneseDate](JapaneseDate.md)! | [with](JapaneseDate.md))`(`adjuster:` ` [TemporalAdjuster](../java.time.temporal/TemporalAdjuster.md)!`)` Returns an adjusted object of the same type as this object with the adjustment made. |
| [JapaneseDate](JapaneseDate.md)! | [with](JapaneseDate.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [ChronoLocalDate](ChronoLocalDate.md) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Temporal](../java.time.temporal/Temporal.md)! | [adjustInto](ChronoLocalDate.md))`(`temporal:` ` [Temporal](../java.time.temporal/Temporal.md)!`)` <br /> Adjusts the specified temporal object to have the same date as this object. This returns a temporal object of the same observable type as the input with the date changed to be the same as this. The adjustment is equivalent to using [Temporal.with(TemporalField, long)](../java.time.temporal/Temporal.md))passing [ChronoField.EPOCH_DAY](../java.time.temporal/ChronoField.md) as the field. In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](../java.time.temporal/Temporal.md)): ```kotlin // these two lines are equivalent, but the second approach is recommended temporal = thisLocalDate.adjustInto(temporal); temporal = temporal.with(thisLocalDate); ``` This instance is immutable and unaffected by this method call. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](ChronoLocalDate.md))`(`other:` ` [ChronoLocalDate](ChronoLocalDate.md)!`)` <br /> Compares this date to another date, including the chronology. The comparison is based first on the underlying time-line date, then on the chronology. It is "consistent with equals", as defined by [Comparable](../java.lang/Comparable.md). For example, the following is the comparator order: 1. `2012-12-03 (ISO)` 2. `2012-12-04 (ISO)` 3. `2555-12-04 (ThaiBuddhist)` 4. `2012-12-05 (ISO)` Values #2 and #3 represent the same date on the time-line. When two values represent the same date, the chronology ID is compared to distinguish them. This step is needed to make the ordering "consistent with equals". If all the date objects being compared are in the same chronology, then the additional chronology stage is not required and only the local date is used. To compare the dates of two`TemporalAccessor`instances, including dates in two different chronologies, use [ChronoField.EPOCH_DAY](../java.time.temporal/ChronoField.md) as a comparator. This default implementation performs the comparison defined above. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](ChronoLocalDate.md))`(`formatter:` ` [DateTimeFormatter](../java.time.format/DateTimeFormatter.md)!`)` <br /> Formats this date using the specified formatter. This date will be passed to the formatter to produce a string. The default implementation must behave as follows: ```kotlin return formatter.format(this); ``` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfter](ChronoLocalDate.md))`(`other:` ` [ChronoLocalDate](ChronoLocalDate.md)!`)` <br /> Checks if this date is after the specified date ignoring the chronology. This method differs from the comparison in [compareTo](ChronoLocalDate.md))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() > date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBefore](ChronoLocalDate.md))`(`other:` ` [ChronoLocalDate](ChronoLocalDate.md)!`)` <br /> Checks if this date is before the specified date ignoring the chronology. This method differs from the comparison in [compareTo](ChronoLocalDate.md))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() < date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqual](ChronoLocalDate.md))`(`other:` ` [ChronoLocalDate](ChronoLocalDate.md)!`)` <br /> Checks if this date is equal to the specified date ignoring the chronology. This method differs from the comparison in [compareTo](ChronoLocalDate.md))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() == date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeapYear](ChronoLocalDate.md))`()` <br /> Checks if the year is a leap year, as defined by the calendar system. A leap-year is a year of a longer length than normal. The exact meaning is determined by the chronology with the constraint that a leap-year must imply a year-length longer than a non leap-year. This default implementation uses [Chronology.isLeapYear(long)](Chronology.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](ChronoLocalDate.md))`(`unit:` ` [TemporalUnit](../java.time.temporal/TemporalUnit.md)!`)` <br /> Checks if the specified unit is supported. This checks if the specified unit can be added to or subtracted from this date. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](ChronoLocalDate.md))and [minus](ChronoLocalDate.md))methods will throw an exception. The set of supported units is defined by the chronology and normally includes all`ChronoUnit`date units except`FOREVER`. If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.isSupportedBy(Temporal)`passing`this`as the argument. Whether the unit is supported is determined by the unit. <br /> | | R | [query](ChronoLocalDate.md))`(`query:` ` [TemporalQuery](../java.time.temporal/TemporalQuery.md)<R>!`)` <br /> Queries this date using the specified query. This queries this date using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be. The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](../java.time.temporal/TemporalQuery.md))method on the specified query passing`this`as the argument. <br /> | ||

## Public methods

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun atTime(localTime: LocalTime!): ChronoLocalDateTime<JapaneseDate!>!
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `localTime` | [LocalTime](../java.time/LocalTime.md)!:the local time to use, not null |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ChronoLocalDateTime](ChronoLocalDateTime.md)< [JapaneseDate](JapaneseDate.md)!>! | the local date-time formed from this date and the specified time, not null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this date to another date, including the chronology.

Compares this`JapaneseDate`with another ensuring that the date is the same.

Only objects of type`JapaneseDate`are compared, other types return false. To compare the dates of two`TemporalAccessor`instances, including dates in two different chronologies, use [ChronoField.EPOCH_DAY](../java.time.temporal/ChronoField.md) as a comparator.

| Parameters ||
|-------|-----------------------------------------|
| `obj` | the object to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is equal to the other date |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun from(temporal: TemporalAccessor!): JapaneseDate!
```

Obtains a`JapaneseDate`from a temporal object.

This obtains a date in the Japanese calendar system based on the specified temporal. A`TemporalAccessor`represents an arbitrary set of date and time information, which this factory converts to an instance of`JapaneseDate`.

The conversion typically uses the [EPOCH_DAY](../java.time.temporal/ChronoField.md) field, which is standardized across calendar systems.

This method matches the signature of the functional interface [TemporalQuery](../java.time.temporal/TemporalQuery.md) allowing it to be used as a query via method reference,`JapaneseDate::from`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!:the temporal object to convert, not null |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | the date in Japanese calendar system, not null |

| Exceptions ||
|-------------------------------|-----------------------------------------|
| `java.time.DateTimeException` | if unable to convert to a`JapaneseDate` |

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChronology(): JapaneseChronology!
```

Gets the chronology of this date, which is the Japanese calendar system.

The`Chronology`represents the calendar system in use. The era and other fields in [ChronoField](../java.time.temporal/ChronoField.md) are defined by the chronology.

| Return ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------------|
| [JapaneseChronology](JapaneseChronology.md)! | the Japanese chronology, not null |

### getEra

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEra(): JapaneseEra!
```

Gets the era applicable at this date.

The Japanese calendar system has multiple eras defined by [JapaneseEra](JapaneseEra.md).

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------|
| [JapaneseEra](JapaneseEra.md)! | the era applicable at this date, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLong(field: TemporalField!): Long
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to get, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

A hash code for this date.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a suitable hash code based only on the Chronology and the date |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this date can be queried for the specified field. If false, then calling the [range](JapaneseDate.md))and [get](../java.time.temporal/TemporalAccessor.md))methods will throw an exception.

If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The supported fields are:

- `DAY_OF_WEEK`
- `DAY_OF_MONTH`
- `DAY_OF_YEAR`
- `EPOCH_DAY`
- `MONTH_OF_YEAR`
- `PROLEPTIC_MONTH`
- `YEAR_OF_ERA`
- `YEAR`
- `ERA`

All other`ChronoField`instances will return false.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field is supported on this date, false if not |

### lengthOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lengthOfMonth(): Int
```

Returns the length of the month represented by this date.

This returns the length of the month in days. Month lengths match those of the ISO calendar system.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the month in days |

### lengthOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lengthOfYear(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the year in days |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(amount: TemporalAmount!): JapaneseDate!
```

Returns an object of the same type as this object with an amount subtracted.

This adjusts this temporal, subtracting according to the rules of the specified amount. The amount is typically a [java.time.Period](../java.time/Period.md) but may be any other type implementing the [TemporalAmount](../java.time.temporal/TemporalAmount.md) interface, such as [java.time.Duration](../java.time/Duration.md).

Some example code indicating how and why this method is used: 

```kotlin
date = date.minus(period);               // subtract a Period instance
   date = date.minus(duration);             // subtract a Duration instance
   date = date.minus(workingDays(6));       // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!:the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|-----------------------------------|
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): JapaneseDate!
```

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | the amount of the specified unit to subtract, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit of the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | an object of the same type with the specified period subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the unit cannot be subtracted |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(): JapaneseDate!
```

Obtains the current`JapaneseDate`from the system clock in the default time-zone.

This will query the [system clock](../java.time/Clock.md))in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | the current date using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(clock: Clock!): JapaneseDate!
```

Obtains the current`JapaneseDate`from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using [dependency injection](../java.time/Clock.md).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `clock` | [Clock](../java.time/Clock.md)!:the clock to use, not null |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [JapaneseDate](JapaneseDate.md)! | the current date, not null |

| Exceptions ||
|-------------------------------|----------------------------------------|
| `java.time.DateTimeException` | if the current date cannot be obtained |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(zone: ZoneId!): JapaneseDate!
```

Obtains the current`JapaneseDate`from the system clock in the specified time-zone.

This will query the [system clock](../java.time/Clock.md))to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](../java.time/ZoneId.md)!:the zone ID to use, not null |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | the current date using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    prolepticYear: Int, 
    month: Int, 
    dayOfMonth: Int
): JapaneseDate!
```

Obtains a`JapaneseDate`representing a date in the Japanese calendar system from the proleptic-year, month-of-year and day-of-month fields.

This returns a`JapaneseDate`with the specified fields. The day must be valid for the year and month, otherwise an exception will be thrown.

The Japanese proleptic year, month and day-of-month are the same as those in the ISO calendar system. They are not reset when the era changes.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese proleptic-year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese month-of-year, from 1 to 12 |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese day-of-month, from 1 to 31 |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | the date in Japanese calendar system, not null |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month-year |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    era: JapaneseEra!, 
    yearOfEra: Int, 
    month: Int, 
    dayOfMonth: Int
): JapaneseDate!
```

Obtains a`JapaneseDate`representing a date in the Japanese calendar system from the era, year-of-era, month-of-year and day-of-month fields.

This returns a`JapaneseDate`with the specified fields. The day must be valid for the year and month, otherwise an exception will be thrown.

The Japanese month and day-of-month are the same as those in the ISO calendar system. They are not reset when the era changes. For example: 

```kotlin
6th Jan Showa 64 = ISO 1989-01-06
   7th Jan Showa 64 = ISO 1989-01-07
   8th Jan Heisei 1 = ISO 1989-01-08
   9th Jan Heisei 1 = ISO 1989-01-09
  
```

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------|
| `era` | [JapaneseEra](JapaneseEra.md)!:the Japanese era, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese year-of-era |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese month-of-year, from 1 to 12 |
| --- | --- |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese day-of-month, from 1 to 31 |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | the date in Japanese calendar system, not null |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month-year, or if the date is not a Japanese era |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(amount: TemporalAmount!): JapaneseDate!
```

Returns an object of the same type as this object with an amount added.

This adjusts this temporal, adding according to the rules of the specified amount. The amount is typically a [java.time.Period](../java.time/Period.md) but may be any other type implementing the [TemporalAmount](../java.time.temporal/TemporalAmount.md) interface, such as [java.time.Duration](../java.time/Duration.md).

Some example code indicating how and why this method is used: 

```kotlin
date = date.plus(period);                // add a Period instance
   date = date.plus(duration);              // add a Duration instance
   date = date.plus(workingDays(6));        // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](../java.time.temporal/TemporalAmount.md)!:the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): JapaneseDate!
```

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the specified unit to add, may be negative |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit of the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | an object of the same type with the specified period added, not null |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if the unit cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun range(field: TemporalField!): ValueRange!
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](../java.time.temporal/ValueRange.md)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toEpochDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toEpochDay(): Long
```

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the Epoch Day equivalent to this date |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the formatted date, not null |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun until(endDate: ChronoLocalDate!): ChronoPeriod!
```

| Parameters ||
|--------------------|-------------------------------------------------------------------|
| `endDateExclusive` | the end date, exclusive, which may be in any chronology, not null |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [ChronoPeriod](ChronoPeriod.md)! | the period between this date and the end date, not null |

| Exceptions ||
|---------------------------------|------------------------------------|
| `java.time.DateTimeException` | if the period cannot be calculated |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endExclusive` | [Temporal](../java.time.temporal/Temporal.md)!:the end temporal, exclusive, converted to be of the same type as this object, not null |
| `unit` | [TemporalUnit](../java.time.temporal/TemporalUnit.md)!:the unit to measure the amount in, not null |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between this temporal object and the specified one in terms of the unit; positive if the specified object is later than this one, negative if it is earlier than this one |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to the same type as this temporal |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun with(adjuster: TemporalAdjuster!): JapaneseDate!
```

Returns an adjusted object of the same type as this object with the adjustment made.

This adjusts this date-time according to the rules of the specified adjuster. A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in [TemporalAdjusters](../java.time.temporal/TemporalAdjusters.md). These include finding the "last day of the month" and "next Wednesday". The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

Some example code indicating how and why this method is used: 

```kotlin
date = date.with(Month.JULY);        // most key classes implement TemporalAdjuster
   date = date.with(lastDayOfMonth());  // static import from Adjusters
   date = date.with(next(WEDNESDAY));   // static import from Adjusters and DayOfWeek
  
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `adjuster` | [TemporalAdjuster](../java.time.temporal/TemporalAdjuster.md)!:the adjuster to use, not null |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun with(
    field: TemporalField!, 
    newValue: Long
): JapaneseDate!
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field in the result |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [JapaneseDate](JapaneseDate.md)! | an object of the same type with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |
