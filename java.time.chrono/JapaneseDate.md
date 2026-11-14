# JapaneseDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JapaneseDate

```
class JapaneseDate : ChronoLocalDate, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.time.chrono.JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#) |

A date in the Japanese Imperial calendar system.

This date operates using the [Japanese Imperial calendar](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology). This calendar system is primarily used in Japan.

The Japanese Imperial calendar system is the same as the ISO calendar system apart from the era-based year numbering. The proleptic-year is defined to be equal to the ISO proleptic-year.

Japan introduced the Gregorian calendar starting with Meiji 6. Only Meiji and later eras are supported; dates before Meiji 6, January 1 are not supported.

For example, the Japanese year "Heisei 24" corresponds to ISO year "2012". 
Calling`japaneseDate.get(YEAR_OF_ERA)`will return 24. 
Calling`japaneseDate.get(YEAR)`will return 2012. 
Calling`japaneseDate.get(ERA)`will return 2, corresponding to`JapaneseChronology.ERA_HEISEI`. 

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime)\< [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)!\>! | [atTime](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#atTime(java.time.LocalTime))`(`localTime:` ` [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)!`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this date to another date, including the chronology. |
| static [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [from](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#from(java.time.temporal.TemporalAccessor))`(`temporal:` ` [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!`)` Obtains a`JapaneseDate`from a temporal object. |
| [JapaneseChronology](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology)! | [getChronology](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#getChronology())`()` Gets the chronology of this date, which is the Japanese calendar system. |
| [JapaneseEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra)! | [getEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#getEra())`()` Gets the era applicable at this date. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#hashCode())`()` A hash code for this date. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Checks if the specified field is supported. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lengthOfMonth](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#lengthOfMonth())`()` Returns the length of the month represented by this date. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lengthOfYear](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#lengthOfYear())`()` <br /> |
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [minus](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#minus(java.time.temporal.TemporalAmount))`(`amount:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!`)` Returns an object of the same type as this object with an amount subtracted. |
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [minus](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` <br /> |
| static [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [now](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#now())`()` Obtains the current`JapaneseDate`from the system clock in the default time-zone. |
| static [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [now](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#now(java.time.Clock))`(`clock:` ` [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#)!`)` Obtains the current`JapaneseDate`from the specified clock. |
| static [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [now](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#now(java.time.ZoneId))`(`zone:` ` [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!`)` Obtains the current`JapaneseDate`from the system clock in the specified time-zone. |
| static [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [of](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#of(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`prolepticYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`JapaneseDate`representing a date in the Japanese calendar system from the proleptic-year, month-of-year and day-of-month fields. |
| static [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [of](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#of(java.time.chrono.JapaneseEra,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`era:` ` [JapaneseEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra)!`, `yearOfEra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains a`JapaneseDate`representing a date in the Japanese calendar system from the era, year-of-era, month-of-year and day-of-month fields. |
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [plus](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#plus(java.time.temporal.TemporalAmount))`(`amount:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount.html#)!`)` Returns an object of the same type as this object with an amount added. |
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [plus](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` <br /> |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | [range](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toEpochDay](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#toEpochDay())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#toString())`()` <br /> |
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod)! | [until](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#until(java.time.chrono.ChronoLocalDate))`(`endDate:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit))`(`endExclusive:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` <br /> |
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [with](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#with(java.time.temporal.TemporalAdjuster))`(`adjuster:` ` [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster.html#)!`)` Returns an adjusted object of the same type as this object with the adjustment made. |
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | [with](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#with(java.time.temporal.TemporalField,%20kotlin.Long))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | [adjustInto](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#adjustInto(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`)` <br /> Adjusts the specified temporal object to have the same date as this object. This returns a temporal object of the same observable type as the input with the date changed to be the same as this. The adjustment is equivalent to using [Temporal.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalField,%20kotlin.Long))passing [ChronoField.EPOCH_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as the field. In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalAdjuster)): ```kotlin // these two lines are equivalent, but the second approach is recommended temporal = thisLocalDate.adjustInto(temporal); temporal = temporal.with(thisLocalDate); ``` This instance is immutable and unaffected by this method call. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))`(`other:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!`)` <br /> Compares this date to another date, including the chronology. The comparison is based first on the underlying time-line date, then on the chronology. It is "consistent with equals", as defined by [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#). For example, the following is the comparator order: 1. `2012-12-03 (ISO)` 2. `2012-12-04 (ISO)` 3. `2555-12-04 (ThaiBuddhist)` 4. `2012-12-05 (ISO)` Values #2 and #3 represent the same date on the time-line. When two values represent the same date, the chronology ID is compared to distinguish them. This step is needed to make the ordering "consistent with equals". If all the date objects being compared are in the same chronology, then the additional chronology stage is not required and only the local date is used. To compare the dates of two`TemporalAccessor`instances, including dates in two different chronologies, use [ChronoField.EPOCH_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as a comparator. This default implementation performs the comparison defined above. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#format(java.time.format.DateTimeFormatter))`(`formatter:` ` [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter.html#)!`)` <br /> Formats this date using the specified formatter. This date will be passed to the formatter to produce a string. The default implementation must behave as follows: ```kotlin return formatter.format(this); ``` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfter](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isAfter(java.time.chrono.ChronoLocalDate))`(`other:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!`)` <br /> Checks if this date is after the specified date ignoring the chronology. This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() > date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBefore](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isBefore(java.time.chrono.ChronoLocalDate))`(`other:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!`)` <br /> Checks if this date is before the specified date ignoring the chronology. This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() < date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqual](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isEqual(java.time.chrono.ChronoLocalDate))`(`other:` ` [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!`)` <br /> Checks if this date is equal to the specified date ignoring the chronology. This method differs from the comparison in [compareTo](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#compareTo(java.time.chrono.ChronoLocalDate))in that it only compares the underlying date and not the chronology. This allows dates in different calendar systems to be compared based on the time-line position. This is equivalent to using`date1.toEpochDay() == date2.toEpochDay()`. This default implementation performs the comparison based on the epoch-day. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeapYear](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isLeapYear())`()` <br /> Checks if the year is a leap year, as defined by the calendar system. A leap-year is a year of a longer length than normal. The exact meaning is determined by the chronology with the constraint that a leap-year must imply a year-length longer than a non leap-year. This default implementation uses [Chronology.isLeapYear(long)](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#isLeapYear(kotlin.Long)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#isSupported(java.time.temporal.TemporalUnit))`(`unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!`)` <br /> Checks if the specified unit is supported. This checks if the specified unit can be added to or subtracted from this date. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))and [minus](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))methods will throw an exception. The set of supported units is defined by the chronology and normally includes all`ChronoUnit`date units except`FOREVER`. If the unit is not a`ChronoUnit`, then the result of this method is obtained by invoking`TemporalUnit.isSupportedBy(Temporal)`passing`this`as the argument. Whether the unit is supported is determined by the unit. <br /> | | R | [query](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)<R>!`)` <br /> Queries this date using the specified query. This queries this date using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be. The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#queryFrom(java.time.temporal.TemporalAccessor))method on the specified query passing`this`as the argument. <br /> | ||

## Public methods

### atTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun atTime(localTime: LocalTime!): ChronoLocalDateTime<JapaneseDate!>!
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `localTime` | [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)!:the local time to use, not null |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime)< [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)!>! | the local date-time formed from this date and the specified time, not null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this date to another date, including the chronology.

Compares this`JapaneseDate`with another ensuring that the date is the same.

Only objects of type`JapaneseDate`are compared, other types return false. To compare the dates of two`TemporalAccessor`instances, including dates in two different chronologies, use [ChronoField.EPOCH_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as a comparator.

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

The conversion typically uses the [EPOCH_DAY](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) field, which is standardized across calendar systems.

This method matches the signature of the functional interface [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#) allowing it to be used as a query via method reference,`JapaneseDate::from`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!:the temporal object to convert, not null |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | the date in Japanese calendar system, not null |

| Exceptions ||
|-------------------------------|-----------------------------------------|
| `java.time.DateTimeException` | if unable to convert to a`JapaneseDate` |

### getChronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChronology(): JapaneseChronology!
```

Gets the chronology of this date, which is the Japanese calendar system.

The`Chronology`represents the calendar system in use. The era and other fields in [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) are defined by the chronology.

| Return ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------------|
| [JapaneseChronology](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology)! | the Japanese chronology, not null |

### getEra

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEra(): JapaneseEra!
```

Gets the era applicable at this date.

The Japanese calendar system has multiple eras defined by [JapaneseEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra).

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------|
| [JapaneseEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra)! | the era applicable at this date, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLong(field: TemporalField!): Long
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to get, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

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

This checks if this date can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#range(java.time.temporal.TemporalField))and [get](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#get(java.time.temporal.TemporalField))methods will throw an exception.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The supported fields are:

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
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to check, null returns false |

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
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | an object of the same type with the specified adjustment made, not null |

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
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit of the amount to subtract, not null |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | an object of the same type with the specified period subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the unit cannot be subtracted |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(): JapaneseDate!
```

Obtains the current`JapaneseDate`from the system clock in the default time-zone.

This will query the [system clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#systemDefaultZone())in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | the current date using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(clock: Clock!): JapaneseDate!
```

Obtains the current`JapaneseDate`from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using [dependency injection](https://developer.android.com/reference/kotlin/java/time/Clock.html#).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `clock` | [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#)!:the clock to use, not null |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | the current date, not null |

| Exceptions ||
|-------------------------------|----------------------------------------|
| `java.time.DateTimeException` | if the current date cannot be obtained |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(zone: ZoneId!): JapaneseDate!
```

Obtains the current`JapaneseDate`from the system clock in the specified time-zone.

This will query the [system clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#system(java.time.ZoneId))to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!:the zone ID to use, not null |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | the current date using the system clock, not null |

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

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | the date in Japanese calendar system, not null |

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
| `era` | [JapaneseEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra)!:the Japanese era, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese year-of-era |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese month-of-year, from 1 to 12 |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the Japanese day-of-month, from 1 to 31 |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | the date in Japanese calendar system, not null |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month-year, or if the date is not a Japanese era |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(amount: TemporalAmount!): JapaneseDate!
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
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | an object of the same type with the specified adjustment made, not null |

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
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit of the amount to add, not null |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | an object of the same type with the specified period added, not null |

| Exceptions ||
|-------------------------------------------------------|------------------------------|
| `java.time.DateTimeException` | if the unit cannot be added |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun range(field: TemporalField!): ValueRange!
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | the range of valid values for the field, not null |

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
| [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod)! | the period between this date and the end date, not null |

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
| `endExclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!:the end temporal, exclusive, converted to be of the same type as this object, not null |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit.html#)!:the unit to measure the amount in, not null |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between this temporal object and the specified one in terms of the unit; positive if the specified object is later than this one, negative if it is earlier than this one |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to the same type as this temporal |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun with(adjuster: TemporalAdjuster!): JapaneseDate!
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
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | an object of the same type with the specified adjustment made, not null |

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
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field in the result |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [JapaneseDate](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseDate#)! | an object of the same type with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
