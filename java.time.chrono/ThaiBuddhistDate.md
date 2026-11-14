Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThaiBuddhistDate

```
class ThaiBuddhistDate : ChronoLocalDate, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.chrono.ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#) |

A date in the Thai Buddhist calendar system.

This date operates using the [Thai Buddhist calendar](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology). This calendar system is primarily used in Thailand. Dates are aligned such that `2484-01-01 (Buddhist)` is `1941-01-01 (ISO)`.

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#equals(kotlin.Any)) as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. The `equals` method should be used for comparisons.

## Summary

| Public methods ||
|---|---|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime)\< [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#atTime(java.time.LocalTime)(localTime: https://developer.android.com/reference/kotlin/java/time/LocalTime.html#!)` Combines this date with a time to create a `ChronoLocalDateTime`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this date to another date, including the chronology. |
| static [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains a `ThaiBuddhistDate` from a temporal object. |
| --- | --- |
| [ThaiBuddhistChronology](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#getChronology()()` Gets the chronology of this date, which is the Thai Buddhist calendar system. |
| [ThaiBuddhistEra](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#getEra()()` Gets the era applicable at this date. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Gets the value of the specified field as a `long`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#hashCode()()` A hash code for this date. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#lengthOfMonth()()` Returns the length of the month represented by this date. |
| [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#minus(java.time.temporal.TemporalAmount)(amount: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#!)` Returns an object of the same type as this object with an amount subtracted. |
| --- | --- |
| [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#!)` Returns an object of the same type as this object with the specified period subtracted. |
| static [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#now()()` Obtains the current `ThaiBuddhistDate` from the system clock in the default time-zone. |
| static [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#now(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock.html#!)` Obtains the current `ThaiBuddhistDate` from the specified clock. |
| --- | --- |
| static [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#now(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Obtains the current `ThaiBuddhistDate` from the system clock in the specified time-zone. |
| static [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#of(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a `ThaiBuddhistDate` representing a date in the Thai Buddhist calendar system from the proleptic-year, month-of-year and day-of-month fields. |
| [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#plus(java.time.temporal.TemporalAmount)(amount: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#!)` Returns an object of the same type as this object with an amount added. |
| --- | --- |
| [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#!)` Returns an object of the same type as this object with the specified period added. |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Gets the range of valid values for the specified field. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#toEpochDay()()` Converts this date to the Epoch Day. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#toString()()` Returns a string representation of the object. |
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#until(java.time.chrono.ChronoLocalDate)(endDate: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Calculates the period between this date and another date as a `ChronoPeriod`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit)(endExclusive: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#!)` Calculates the amount of time until another date in terms of the specified unit. |
| --- | --- |
| [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#with(java.time.temporal.TemporalAdjuster)(adjuster: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster.html#!)` Returns an adjusted object of the same type as this object with the adjustment made. |
| [ThaiBuddhistDate](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#with(java.time.temporal.TemporalField,%20kotlin.Long)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns an object of the same type as this object with the specified field altered. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate` |---|---| | `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#adjustInto(java.time.temporal.Temporal)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#!)` Adjusts the specified temporal object to have the same date as this object. This returns a temporal object of the same observable type as the input with the date changed to be the same as this. The adjustment is equivalent to using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalField,%20kotlin.Long)` passing `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` as the field. In most cases, it is clearer to reverse the calling pattern by using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalAdjuster)`: ```kotlin // these two lines are equivalent, but the second approach is recommended temporal = thisLocalDate.adjustInto(temporal); temporal = temporal.with(thisLocalDate); ``` This instance is immutable and unaffected by this method call. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Compares this date to another date, including the chronology. The comparison is based first on the underlying time-line date, then on the chronology. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`. For example, the following is the comparator order: 1. `2012-12-03 (ISO)` 2. `2012-12-04 (ISO)` 3. `2555-12-04 (ThaiBuddhist)` 4. `2012-12-05 (ISO)` Values #2 and #3 represent the same date on the time-line. When two values represent the same date, the chronology ID is compared to distinguish them. This step is needed to make the ordering "consistent with equals". If all the date objects being compared are in the same chronology, then the additional chronology stage is not required and only the local date is used. To compare the dates of two `TemporalAccessor` instances, including dates in two different chronologies, use `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` as a comparator. This default implementation performs the comparison defined above. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#format(java.time.format.DateTimeFormatter)(formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#!)` Formats this date using the specified formatter. This date will be passed to the formatter to produce a string. The default implementation must behave as follows: ```kotlin return formatter.format(this); ``` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isAfter(java.time.chrono.ChronoLocalDate)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Checks if this date is after the specified date ignoring the chronology. This method differs from the comparison in `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate)` in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using `date1.toEpochDay() > date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isBefore(java.time.chrono.ChronoLocalDate)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Checks if this date is before the specified date ignoring the chronology. This method differs from the comparison in `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate)` in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using `date1.toEpochDay() < date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isEqual(java.time.chrono.ChronoLocalDate)(other: https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!)` Checks if this date is equal to the specified date ignoring the chronology. This method differs from the comparison in `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate)` in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using `date1.toEpochDay() == date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isLeapYear()()` Checks if the year is a leap year, as defined by the calendar system. A leap-year is a year of a longer length than normal. The exact meaning is determined by the chronology with the constraint that a leap-year must imply a year-length longer than a non leap-year. This default implementation uses `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#isLeapYear(kotlin.Long)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!)` Checks if the specified field is supported. This checks if the specified field can be queried on this date. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#range(java.time.temporal.TemporalField)`, `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#get(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#with(java.time.temporal.TemporalField,%20kotlin.Long)` methods will throw an exception. The set of supported fields is defined by the chronology and normally includes all `ChronoField` date fields. If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isSupported(java.time.temporal.TemporalUnit)(unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#!)` Checks if the specified unit is supported. This checks if the specified unit can be added to or subtracted from this date. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` and `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)` methods will throw an exception. The set of supported units is defined by the chronology and normally includes all `ChronoUnit` date units except `FOREVER`. If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.isSupportedBy(Temporal)` passing `this` as the argument. Whether the unit is supported is determined by the unit. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#lengthOfYear()()` Returns the length of the year represented by this date, as defined by the calendar system. This returns the length of the year in days. The default implementation uses `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isLeapYear()` and returns 365 or 366. <br /> | | `R` | `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#<R>!)` Queries this date using the specified query. This queries this date using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be. The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#queryFrom(java.time.temporal.TemporalAccessor)` method on the specified query passing `this` as the argument. <br /> | ||

## Public methods

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atTime(localTime: LocalTime!): ChronoLocalDateTime<ThaiBuddhistDate!>!
```

Combines this date with a time to create a `ChronoLocalDateTime`.

This returns a `ChronoLocalDateTime` formed from this date at the specified time. All possible combinations of date and time are valid.

| Parameters ||
|---|---|
| `localTime` | [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)!: the local time to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime<https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!>!` | the local date-time formed from this date and the specified time, not null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compares this date to another date, including the chronology.

Compares this `ThaiBuddhistDate` with another ensuring that the date is the same.

Only objects of type `ThaiBuddhistDate` are compared, other types return false. To compare the dates of two `TemporalAccessor` instances, including dates in two different chronologies, use `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` as a comparator.

| Parameters ||
|---|---|
| `obj` | the object to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is equal to the other date |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): ThaiBuddhistDate!
```

Obtains a `ThaiBuddhistDate` from a temporal object.

This obtains a date in the Thai Buddhist calendar system based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ThaiBuddhistDate`.

The conversion typically uses the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` field, which is standardized across calendar systems.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `ThaiBuddhistDate::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | the date in Thai Buddhist calendar system, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to a `ThaiBuddhistDate` |

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChronology(): ThaiBuddhistChronology!
```

Gets the chronology of this date, which is the Thai Buddhist calendar system.

The `Chronology` represents the calendar system in use. The era and other fields in `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` are defined by the chronology.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology!` | the Thai Buddhist chronology, not null |

### getEra

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEra(): ThaiBuddhistEra!
```

Gets the era applicable at this date.

The Thai Buddhist calendar system has two eras, 'BE' and 'BEFORE_BE', defined by `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra!` | the era applicable at this date, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field as a `long`.

This queries the date-time for the value of the specified field. The returned value may be outside the valid range of values for the field. If the date-time cannot return the value, because the field is unsupported or for some other reason, an exception will be thrown.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

A hash code for this date.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code based only on the Chronology and the date |

### lengthOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lengthOfMonth(): Int
```

Returns the length of the month represented by this date.

This returns the length of the month in days. Month lengths match those of the ISO calendar system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the length of the month in days |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(amount: TemporalAmount!): ThaiBuddhistDate!
```

Returns an object of the same type as this object with an amount subtracted.

This adjusts this temporal, subtracting according to the rules of the specified amount. The amount is typically a `https://developer.android.com/reference/kotlin/java/time/Period.html#` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#` interface, such as `https://developer.android.com/reference/kotlin/java/time/Duration.html#`.

Some example code indicating how and why this method is used:

```kotlin
date = date.minus(period);               // subtract a Period instance
   date = date.minus(duration);             // subtract a Duration instance
   date = date.minus(workingDays(6));       // example user-written workingDays method
  
```

Note that calling `plus` followed by `minus` is not guaranteed to return the same date-time.

| Parameters ||
|---|---|
| `amount` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!: the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): ThaiBuddhistDate!
```

Returns an object of the same type as this object with the specified period subtracted.

This method returns a new object based on this one with the specified period subtracted. For example, on a `LocalDate`, this could be used to subtract a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st March, then subtracting one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---|---|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the specified unit to subtract, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!: the unit of the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | an object of the same type with the specified period subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the unit cannot be subtracted |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(): ThaiBuddhistDate!
```

Obtains the current `ThaiBuddhistDate` from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#systemDefaultZone()` in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | the current date using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(clock: Clock!): ThaiBuddhistDate!
```

Obtains the current `ThaiBuddhistDate` from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using [dependency injection](https://developer.android.com/reference/kotlin/java/time/Clock.html#).

| Parameters ||
|---|---|
| `clock` | [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | the current date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the current date cannot be obtained |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(zone: ZoneId!): ThaiBuddhistDate!
```

Obtains the current `ThaiBuddhistDate` from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#system(java.time.ZoneId)` to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | the current date using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    prolepticYear: Int, 
    month: Int, 
    dayOfMonth: Int
): ThaiBuddhistDate!
```

Obtains a `ThaiBuddhistDate` representing a date in the Thai Buddhist calendar system from the proleptic-year, month-of-year and day-of-month fields.

This returns a `ThaiBuddhistDate` with the specified fields. The day must be valid for the year and month, otherwise an exception will be thrown.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the Thai Buddhist proleptic-year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the Thai Buddhist month-of-year, from 1 to 12 |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the Thai Buddhist day-of-month, from 1 to 31 |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | the date in Thai Buddhist calendar system, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month-year |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(amount: TemporalAmount!): ThaiBuddhistDate!
```

Returns an object of the same type as this object with an amount added.

This adjusts this temporal, adding according to the rules of the specified amount. The amount is typically a `https://developer.android.com/reference/kotlin/java/time/Period.html#` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#` interface, such as `https://developer.android.com/reference/kotlin/java/time/Duration.html#`.

Some example code indicating how and why this method is used:

```kotlin
date = date.plus(period);                // add a Period instance
   date = date.plus(duration);              // add a Duration instance
   date = date.plus(workingDays(6));        // example user-written workingDays method
  
```

Note that calling `plus` followed by `minus` is not guaranteed to return the same date-time.

| Parameters ||
|---|---|
| `amount` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!: the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): ThaiBuddhistDate!
```

Returns an object of the same type as this object with the specified period added.

This method returns a new object based on this one with the specified period added. For example, on a `LocalDate`, this could be used to add a number of years, months or days. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then adding one month would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---|---|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the specified unit to add, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!: the unit of the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | an object of the same type with the specified period added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the unit cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

All fields can be expressed as a `long` integer. This method returns an object that describes the valid range for that value. The value of this temporal object is used to enhance the accuracy of the returned range. If the date-time cannot return the range, because the field is unsupported or for some other reason, an exception will be thrown.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!: the field to query the range for, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#!` | the range of valid values for the field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toEpochDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toEpochDay(): Long
```

Converts this date to the Epoch Day.

The `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` is a simple incrementing count of days where day 0 is 1970-01-01 (ISO). This definition is the same for all chronologies, enabling conversion.

This default implementation queries the `EPOCH_DAY` field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the Epoch Day equivalent to this date |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the formatted date, not null |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun until(endDate: ChronoLocalDate!): ChronoPeriod!
```

Calculates the period between this date and another date as a `ChronoPeriod`.

This calculates the period between two dates. All supplied chronologies calculate the period using years, months and days, however the `ChronoPeriod` API allows the period to be represented using other units.

The start and end points are `this` and the specified date. The result will be negative if the end is before the start. The negative sign will be the same in each of year, month and day.

The calculation is performed using the chronology of this date. If necessary, the input date will be converted to match.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `endDateExclusive` | the end date, exclusive, which may be in any chronology, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod!` | the period between this date and the end date, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the period cannot be calculated |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

Calculates the amount of time until another date in terms of the specified unit.

This calculates the amount of time between two `ChronoLocalDate` objects in terms of a single `TemporalUnit`. The start and end points are `this` and the specified date. The result will be negative if the end is before the start. The `Temporal` passed to this method is converted to a `ChronoLocalDate` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.temporal.TemporalAccessor)`. The calculation returns a whole number, representing the number of complete units between the two dates. For example, the amount in days between two dates can be calculated using `startDate.until(endDate, DAYS)`.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)`:

```kotlin
// these two lines are equivalent
    amount = start.until(end, MONTHS);
    amount = MONTHS.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#`. The units `DAYS`, `WEEKS`, `MONTHS`, `YEARS`, `DECADES`, `CENTURIES`, `MILLENNIA` and `ERAS` should be supported by all implementations. Other `ChronoUnit` values will throw an exception.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.between(Temporal, Temporal)` passing `this` as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `endExclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!: the end temporal, exclusive, converted to be of the same type as this object, not null |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!: the unit to measure the amount in, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the amount of time between this temporal object and the specified one in terms of the unit; positive if the specified object is later than this one, negative if it is earlier than this one |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to the same type as this temporal |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| --- | --- |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(adjuster: TemporalAdjuster!): ThaiBuddhistDate!
```

Returns an adjusted object of the same type as this object with the adjustment made.

This adjusts this date-time according to the rules of the specified adjuster. A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the date to the last day of the month. A selection of common adjustments is provided in `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjusters.html#`. These include finding the "last day of the month" and "next Wednesday". The adjuster is responsible for handling special cases, such as the varying lengths of month and leap years.

Some example code indicating how and why this method is used:

```kotlin
date = date.with(Month.JULY);        // most key classes implement TemporalAdjuster
   date = date.with(lastDayOfMonth());  // static import from Adjusters
   date = date.with(next(WEDNESDAY));   // static import from Adjusters and DayOfWeek
  
```

| Parameters ||
|---|---|
| `adjuster` | [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster.html#)!: the adjuster to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | an object of the same type with the specified adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if unable to make the adjustment |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(
    field: TemporalField!, 
    newValue: Long
): ThaiBuddhistDate!
```

Returns an object of the same type as this object with the specified field altered.

This returns a new object based on this one with the value for the specified field changed. For example, on a `LocalDate`, this could be used to set the year, month or day-of-month. The returned object will have the same observable type as this object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then changing the month to February would be unclear. In cases like this, the field is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!: the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value of the field in the result |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistDate#!` | an object of the same type with the specified field set, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |
