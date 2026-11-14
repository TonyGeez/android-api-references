# ChronoLocalDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChronoLocalDate

```
interface ChronoLocalDate : Comparable<ChronoLocalDate!>, Temporal, TemporalAdjuster
```

| [java.time.chrono.ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#) |

| Known Direct Subclasses [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate), [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate), [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#), [MinguoDate](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoDate), [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------| | [HijrahDate](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahDate) | A date in the Hijrah calendar system. | | [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate) | A date in the Japanese Imperial calendar system. | | [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#) | A date without a time-zone in the ISO-8601 calendar system, such as`2007-12-03`. | | [MinguoDate](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoDate) | A date in the Minguo calendar system. | | [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate) | A date in the Thai Buddhist calendar system. | |

A date without time-of-day or time-zone in an arbitrary chronology, intended for advanced globalization use cases.

**Most applications should declare method signatures, fields and variables as [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#), not this interface.**

A`ChronoLocalDate`is the abstract representation of a date where the`Chronology chronology`, or calendar system, is pluggable. The date is defined in terms of fields expressed by [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#), where most common implementations are defined in [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#). The chronology defines how the calendar system operates and the meaning of the standard fields.

## When to use this interface

The design of the API encourages the use of`LocalDate`rather than this interface, even in the case where the application needs to deal with multiple calendar systems.

This concept can seem surprising at first, as the natural way to globalize an application might initially appear to be to abstract the calendar system. However, as explored below, abstracting the calendar system is usually the wrong approach, resulting in logic errors and hard to find bugs. As such, it should be considered an application-wide architectural decision to choose to use this interface as opposed to`LocalDate`.

### Architectural issues to consider

These are some of the points that must be considered before using this interface throughout an application.

1) Applications using this interface, as opposed to using just`LocalDate`, face a significantly higher probability of bugs. This is because the calendar system in use is not known at development time. A key cause of bugs is where the developer applies assumptions from their day-to-day knowledge of the ISO calendar system to code that is intended to deal with any arbitrary calendar system. The section below outlines how those assumptions can cause problems The primary mechanism for reducing this increased risk of bugs is a strong code review process. This should also be considered a extra cost in maintenance for the lifetime of the code.

2) This interface does not enforce immutability of implementations. While the implementation notes indicate that all implementations must be immutable there is nothing in the code or type system to enforce this. Any method declared to accept a`ChronoLocalDate`could therefore be passed a poorly or maliciously written mutable implementation.

3) Applications using this interface must consider the impact of eras.`LocalDate`shields users from the concept of eras, by ensuring that`getYear()`returns the proleptic year. That decision ensures that developers can think of`LocalDate`instances as consisting of three fields - year, month-of-year and day-of-month. By contrast, users of this interface must think of dates as consisting of four fields - era, year-of-era, month-of-year and day-of-month. The extra era field is frequently forgotten, yet it is of vital importance to dates in an arbitrary calendar system. For example, in the Japanese calendar system, the era represents the reign of an Emperor. Whenever one reign ends and another starts, the year-of-era is reset to one.

4) The only agreed international standard for passing a date between two systems is the ISO-8601 standard which requires the ISO calendar system. Using this interface throughout the application will inevitably lead to the requirement to pass the date across a network or component boundary, requiring an application specific protocol or format.

5) Long term persistence, such as a database, will almost always only accept dates in the ISO-8601 calendar system (or the related Julian-Gregorian). Passing around dates in other calendar systems increases the complications of interacting with persistence.

6) Most of the time, passing a`ChronoLocalDate`throughout an application is unnecessary, as discussed in the last section below.

### False assumptions causing bugs in multi-calendar system code

As indicated above, there are many issues to consider when try to use and manipulate a date in an arbitrary calendar system. These are some of the key issues.

Code that queries the day-of-month and assumes that the value will never be more than 31 is invalid. Some calendar systems have more than 31 days in some months.

Code that adds 12 months to a date and assumes that a year has been added is invalid. Some calendar systems have a different number of months, such as 13 in the Coptic or Ethiopic.

Code that adds one month to a date and assumes that the month-of-year value will increase by one or wrap to the next year is invalid. Some calendar systems have a variable number of months in a year, such as the Hebrew.

Code that adds one month, then adds a second one month and assumes that the day-of-month will remain close to its original value is invalid. Some calendar systems have a large difference between the length of the longest month and the length of the shortest month. For example, the Coptic or Ethiopic have 12 months of 30 days and 1 month of 5 days.

Code that adds seven days and assumes that a week has been added is invalid. Some calendar systems have weeks of other than seven days, such as the French Revolutionary.

Code that assumes that because the year of`date1`is greater than the year of`date2`then`date1`is after`date2`is invalid. This is invalid for all calendar systems when referring to the year-of-era, and especially untrue of the Japanese calendar system where the year-of-era restarts with the reign of every new Emperor.

Code that treats month-of-year one and day-of-month one as the start of the year is invalid. Not all calendar systems start the year when the month value is one.

In general, manipulating a date, and even querying a date, is wide open to bugs when the calendar system is unknown at development time. This is why it is essential that code using this interface is subjected to additional code reviews. It is also why an architectural decision to avoid this interface type is usually the correct one.

### Using LocalDate instead

The primary alternative to using this interface throughout your application is as follows.

- Declare all method signatures referring to dates in terms of`LocalDate`.
- Either store the chronology (calendar system) in the user profile or lookup the chronology from the user locale
- Convert the ISO`LocalDate`to and from the user's preferred calendar system during printing and parsing

This approach treats the problem of globalized calendar systems as a localization issue and confines it to the UI layer. This approach is in keeping with other localization issues in the java platform.

As discussed above, performing calculations on a date where the rules of the calendar system are pluggable requires skill and is not recommended. Fortunately, the need to perform calculations on a date in an arbitrary calendar system is extremely rare. For example, it is highly unlikely that the business rules of a library book rental scheme will allow rentals to be for one month, where meaning of the month is dependent on the user's preferred calendar system.

A key use case for calculations on a date in an arbitrary calendar system is producing a month-by-month calendar for display and user interaction. Again, this is a UI issue, and use of this interface solely within a few methods of the UI layer may be justified.

In any other part of the system, where a date must be manipulated in a calendar system other than ISO, the use case will generally specify the calendar system to use. For example, an application may need to calculate the next Islamic or Hebrew holiday which may require manipulating the date. This kind of use case can be handled as follows:

- start from the ISO`LocalDate`being passed to the method
- convert the date to the alternate calendar system, which for this use case is known rather than arbitrary
- perform the calculation
- convert back to`LocalDate`

Developers writing low-level frameworks or libraries should also avoid this interface. Instead, one of the two general purpose access interfaces should be used. Use [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#) if read-only access is required, or use [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#) if read-write access is required.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | [adjustInto](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#adjustInto(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`)` Adjusts the specified temporal object to have the same date as this object. |
| open [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime)\<\*\>! | [atTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#atTime(java.time.LocalTime))`(`localTime:` ` [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)!`)` Combines this date with a time to create a`ChronoLocalDateTime`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))`(`other:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!`)` Compares this date to another date, including the chronology. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#format(java.time.format.DateTimeFormatter))`(`formatter:` ` [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#)!`)` Formats this date using the specified formatter. |
| openstatic [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | [from](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#from(java.time.temporal.TemporalAccessor))`(`temporal:` ` [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!`)` Obtains an instance of`ChronoLocalDate`from a temporal object. |
| abstract [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology)! | [getChronology](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#getChronology())`()` Gets the chronology of this date. |
| open [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era)! | [getEra](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#getEra())`()` Gets the era, as defined by the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfter](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isAfter(java.time.chrono.ChronoLocalDate))`(`other:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!`)` Checks if this date is after the specified date ignoring the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBefore](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isBefore(java.time.chrono.ChronoLocalDate))`(`other:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!`)` Checks if this date is before the specified date ignoring the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqual](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isEqual(java.time.chrono.ChronoLocalDate))`(`other:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!`)` Checks if this date is equal to the specified date ignoring the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeapYear](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isLeapYear())`()` Checks if the year is a leap year, as defined by the calendar system. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Checks if the specified field is supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isSupported(java.time.temporal.TemporalUnit))`(`unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` Checks if the specified unit is supported. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lengthOfMonth](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#lengthOfMonth())`()` Returns the length of the month represented by this date, as defined by the calendar system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lengthOfYear](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#lengthOfYear())`()` Returns the length of the year represented by this date, as defined by the calendar system. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | [minus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#minus(java.time.temporal.TemporalAmount))`(`amount:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!`)` Returns an object of the same type as this object with an amount subtracted. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | [minus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` Returns an object of the same type as this object with the specified period subtracted. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | [plus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#plus(java.time.temporal.TemporalAmount))`(`amount:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!`)` Returns an object of the same type as this object with an amount added. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | [plus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` Returns an object of the same type as this object with the specified period added. |
| openR | [query](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)<R>!`)` Queries this date using the specified query. |
| openstatic [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\< [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!\>! | [timeLineOrder](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#timeLineOrder())`()` Gets a comparator that compares`ChronoLocalDate`in time-line order ignoring the chronology. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toEpochDay](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#toEpochDay())`()` Converts this date to the Epoch Day. |
| abstract [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod)! | [until](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#until(java.time.chrono.ChronoLocalDate))`(`endDateExclusive:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!`)` Calculates the period between this date and another date as a`ChronoPeriod`. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit))`(`endExclusive:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` Calculates the amount of time until another date in terms of the specified unit. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | [with](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#with(java.time.temporal.TemporalAdjuster))`(`adjuster:` ` [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster.html#)!`)` Returns an adjusted object of the same type as this object with the adjustment made. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | [with](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#with(java.time.temporal.TemporalField,%20kotlin.Long))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns an object of the same type as this object with the specified field altered. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same date as this object.

This returns a temporal object of the same observable type as the input with the date changed to be the same as this.

The adjustment is equivalent to using [Temporal.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalField,%20kotlin.Long))passing [ChronoField.EPOCH_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as the field.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalAdjuster)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisLocalDate.adjustInto(temporal);
    temporal = temporal.with(thisLocalDate);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!:the target object to be adjusted, not null |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | the adjusted object, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun atTime(localTime: LocalTime!): ChronoLocalDateTime<*>!
```

Combines this date with a time to create a`ChronoLocalDateTime`.

This returns a`ChronoLocalDateTime`formed from this date at the specified time. All possible combinations of date and time are valid.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `localTime` | [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)!:the local time to use, not null |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime)<*>! | the local date-time formed from this date and the specified time, not null |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: ChronoLocalDate!): Int
```

Compares this date to another date, including the chronology.

The comparison is based first on the underlying time-line date, then on the chronology. It is "consistent with equals", as defined by [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#).

For example, the following is the comparator order:

1. `2012-12-03 (ISO)`
2. `2012-12-04 (ISO)`
3. `2555-12-04 (ThaiBuddhist)`
4. `2012-12-05 (ISO)`

Values #2 and #3 represent the same date on the time-line. When two values represent the same date, the chronology ID is compared to distinguish them. This step is needed to make the ordering "consistent with equals".

If all the date objects being compared are in the same chronology, then the additional chronology stage is not required and only the local date is used. To compare the dates of two`TemporalAccessor`instances, including dates in two different chronologies, use [ChronoField.EPOCH_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as a comparator.

This default implementation performs the comparison defined above.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!:the other date to compare to, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the comparator value, negative if less, positive if greater |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(formatter: DateTimeFormatter!): String!
```

Formats this date using the specified formatter.

This date will be passed to the formatter to produce a string.

The default implementation must behave as follows: 

```kotlin
return formatter.format(this);
  
```

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `formatter` | [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#)!:the formatter to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted date string, not null |

| Exceptions ||
|-------------------------------|------------------------------------|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun from(temporal: TemporalAccessor!): ChronoLocalDate!
```

Obtains an instance of`ChronoLocalDate`from a temporal object.

This obtains a local date based on the specified temporal. A`TemporalAccessor`represents an arbitrary set of date and time information, which this factory converts to an instance of`ChronoLocalDate`.

The conversion extracts and combines the chronology and the date from the temporal object. The behavior is equivalent to using [Chronology.date(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.temporal.TemporalAccessor))with the extracted chronology. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects.

This method matches the signature of the functional interface [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#) allowing it to be used as a query via method reference,`ChronoLocalDate::from`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!:the temporal object to convert, not null |

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------|
| [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | the date, not null |

| Exceptions ||
|-------------------------------|--------------------------------------------|
| `java.time.DateTimeException` | if unable to convert to a`ChronoLocalDate` |

**See Also**

- [java.time.chrono.Chronology#date(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.temporal.TemporalAccessor)) 

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChronology(): Chronology!
```

Gets the chronology of this date.

The`Chronology`represents the calendar system in use. The era and other fields in [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) are defined by the chronology.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology)! | the chronology, not null |

### getEra

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEra(): Era!
```

Gets the era, as defined by the chronology.

The era is, conceptually, the largest division of the time-line. Most calendar systems have a single epoch dividing the time-line into two eras. However, some have multiple eras, such as one for the reign of each leader. The exact meaning is determined by the`Chronology`.

All correctly implemented`Era`classes are singletons, thus it is valid code to write`date.getEra() == SomeChrono.ERA_NAME)`.

This default implementation uses [Chronology.eraOf(int)](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#eraOf(kotlin.Int)).

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era)! | the chronology specific era constant applicable at this date, not null |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAfter(other: ChronoLocalDate!): Boolean
```

Checks if this date is after the specified date ignoring the chronology.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() > date2.toEpochDay()`.

This default implementation performs the comparison based on the epoch-day.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!:the other date to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is after the specified date |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBefore(other: ChronoLocalDate!): Boolean
```

Checks if this date is before the specified date ignoring the chronology.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() < date2.toEpochDay()`.

This default implementation performs the comparison based on the epoch-day.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!:the other date to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is before the specified date |

### isEqual

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEqual(other: ChronoLocalDate!): Boolean
```

Checks if this date is equal to the specified date ignoring the chronology.

This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() == date2.toEpochDay()`.

This default implementation performs the comparison based on the epoch-day.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!:the other date to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the underlying date is equal to the specified date |

### isLeapYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLeapYear(): Boolean
```

Checks if the year is a leap year, as defined by the calendar system.

A leap-year is a year of a longer length than normal. The exact meaning is determined by the chronology with the constraint that a leap-year must imply a year-length longer than a non leap-year.

This default implementation uses [Chronology.isLeapYear(long)](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#isLeapYear(kotlin.Long)).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this date is in a leap year, false otherwise |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if the specified field can be queried on this date. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#range(java.time.temporal.TemporalField)), [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#get(java.time.temporal.TemporalField))and [with(java.time.temporal.TemporalField,long)](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#with(java.time.temporal.TemporalField,%20kotlin.Long))methods will throw an exception.

The set of supported fields is defined by the chronology and normally includes all`ChronoField`date fields.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field can be queried, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to or subtracted from this date. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))and [minus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))methods will throw an exception.

The set of supported units is defined by the chronology and normally includes all`ChronoUnit`date units except`FOREVER`.

If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.isSupportedBy(Temporal)`passing`this`as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit can be added/subtracted, false if not |

### lengthOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lengthOfMonth(): Int
```

Returns the length of the month represented by this date, as defined by the calendar system.

This returns the length of the month in days.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the month in days |

### lengthOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lengthOfYear(): Int
```

Returns the length of the year represented by this date, as defined by the calendar system.

This returns the length of the year in days.

The default implementation uses [isLeapYear()](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isLeapYear())and returns 365 or 366.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the year in days |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun minus(amount: TemporalAmount!): ChronoLocalDate!
```

Returns an object of the same type as this object with an amount subtracted.

This adjusts this temporal, subtracting according to the rules of the specified amount. The amount is typically a [java.time.Period](https://developer.android.com/reference/kotlin/java/time/Period.html#) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#) interface, such as [java.time.Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#).

Some example code indicating how and why this method is used: 

```kotlin
date = date.minus(period);               // subtract a Period instance
   date = date.minus(duration);             // subtract a Duration instance
   date = date.minus(workingDays(6));       // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!:the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|-----------------------------------|
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): ChronoLocalDate!
```

Returns an object of the same type as this object with the specified period subtracted.

This method returns a new object based on this one with the specified period subtracted. For example, on a`LocalDate`, this could be used to subtract a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st March, then subtracting one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the specified unit to subtract, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit of the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | an object of the same type with the specified period subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the unit cannot be subtracted |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun plus(amount: TemporalAmount!): ChronoLocalDate!
```

Returns an object of the same type as this object with an amount added.

This adjusts this temporal, adding according to the rules of the specified amount. The amount is typically a [java.time.Period](https://developer.android.com/reference/kotlin/java/time/Period.html#) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#) interface, such as [java.time.Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#).

Some example code indicating how and why this method is used: 

```kotlin
date = date.plus(period);                // add a Period instance
   date = date.plus(duration);              // add a Duration instance
   date = date.plus(workingDays(6));        // example user-written workingDays method
  
```

Note that calling`plus`followed by`minus`is not guaranteed to return the same date-time.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!:the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): ChronoLocalDate!
```

Returns an object of the same type as this object with the specified period added.

This method returns a new object based on this one with the specified period added. For example, on a`LocalDate`, this could be used to add a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then adding one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the amount of the specified unit to add, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit of the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | an object of the same type with the specified period added, not null |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if the unit cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this date using the specified query.

This queries this date using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#queryFrom(java.time.temporal.TemporalAccessor))method on the specified query passing`this`as the argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)\<R\>!:the query to invoke, not null |

| Return ||
|---|---------------------------------------------------------------|
| R | the query result, null may be returned (defined by the query) |

| Exceptions ||
|---------------------------------|---------------------------------------------------|
| `java.time.DateTimeException` | if unable to query (defined by the query) |
| `java.lang.ArithmeticException` | if numeric overflow occurs (defined by the query) |

### timeLineOrder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun timeLineOrder(): Comparator<ChronoLocalDate!>!
```

Gets a comparator that compares`ChronoLocalDate`in time-line order ignoring the chronology.

This comparator differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the position of the date on the local time-line. The underlying comparison is equivalent to comparing the epoch-day.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)< [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!>! | a comparator that compares in time-line order ignoring the chronology |

**See Also**

- [#isAfter](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isAfter(java.time.chrono.ChronoLocalDate))
- [#isBefore](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isBefore(java.time.chrono.ChronoLocalDate))
- [#isEqual](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isEqual(java.time.chrono.ChronoLocalDate)) 

### toEpochDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toEpochDay(): Long
```

Converts this date to the Epoch Day.

The [Epoch Day count](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) is a simple incrementing count of days where day 0 is 1970-01-01 (ISO). This definition is the same for all chronologies, enabling conversion.

This default implementation queries the`EPOCH_DAY`field.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the Epoch Day equivalent to this date |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun until(endDateExclusive: ChronoLocalDate!): ChronoPeriod!
```

Calculates the period between this date and another date as a`ChronoPeriod`.

This calculates the period between two dates. All supplied chronologies calculate the period using years, months and days, however the`ChronoPeriod`API allows the period to be represented using other units.

The start and end points are`this`and the specified date. The result will be negative if the end is before the start. The negative sign will be the same in each of year, month and day.

The calculation is performed using the chronology of this date. If necessary, the input date will be converted to match.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endDateExclusive` | [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)!:the end date, exclusive, which may be in any chronology, not null |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod)! | the period between this date and the end date, not null |

| Exceptions ||
|---------------------------------|------------------------------------|
| `java.time.DateTimeException` | if the period cannot be calculated |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

Calculates the amount of time until another date in terms of the specified unit.

This calculates the amount of time between two`ChronoLocalDate`objects in terms of a single`TemporalUnit`. The start and end points are`this`and the specified date. The result will be negative if the end is before the start. The`Temporal`passed to this method is converted to a`ChronoLocalDate`using [Chronology.date(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.temporal.TemporalAccessor)). The calculation returns a whole number, representing the number of complete units between the two dates. For example, the amount in days between two dates can be calculated using`startDate.until(endDate, DAYS)`.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use [TemporalUnit.between(Temporal, Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)): 

```kotlin
// these two lines are equivalent
    amount = start.until(end, MONTHS);
    amount = MONTHS.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#). The units`DAYS`,`WEEKS`,`MONTHS`,`YEARS`,`DECADES`,`CENTURIES`,`MILLENNIA`and`ERAS`should be supported by all implementations. Other`ChronoUnit`values will throw an exception.

If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.between(Temporal, Temporal)`passing`this`as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endExclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!:the end date, exclusive, which is converted to a`ChronoLocalDate`in the same chronology, not null |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit to measure the amount in, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between this date and the end date |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to a`ChronoLocalDate` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun with(adjuster: TemporalAdjuster!): ChronoLocalDate!
```

Returns an adjusted object of the same type as this object with the adjustment made.

This adjusts this date-time according to the rules of the specified adjuster. A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in [TemporalAdjusters](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjusters.html#). These include finding the "last day of the month" and "next Wednesday". The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

Some example code indicating how and why this method is used: 

```kotlin
date = date.with(Month.JULY);        // most key classes implement TemporalAdjuster
   date = date.with(lastDayOfMonth());  // static import from Adjusters
   date = date.with(next(WEDNESDAY));   // static import from Adjusters and DayOfWeek
  
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `adjuster` | [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster.html#)!:the adjuster to use, not null |

| Return ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun with(
    field: TemporalField!, 
    newValue: Long
): ChronoLocalDate!
```

Returns an object of the same type as this object with the specified field altered.

This returns a new object based on this one with the value for the specified field changed. For example, on a`LocalDate`, this could be used to set the year, month or day-of-month. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then changing the month to February would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field in the result |

| Return ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#)! | an object of the same type with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
