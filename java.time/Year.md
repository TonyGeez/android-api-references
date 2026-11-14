# Year

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Year

```
class Year : Comparable<Year!>, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.time.Year](https://developer.android.com/reference/kotlin/java/time/Year#) |

A year in the ISO-8601 calendar system, such as `2007`.

`Year` is an immutable date-time object that represents a year. Any field that can be derived from a year can be obtained.

**Note that years in the ISO chronology only align with years in the Gregorian-Julian system for modern years. Parts of Russia did not switch to the modern Gregorian/ISO rules until 1920. As such, historical years must be treated with caution.**

This class does not store or represent a month, day, time or time-zone. For example, the value "2007" can be stored in a `Year`.

Years represented by this class follow the ISO-8601 standard and use the proleptic numbering system. Year 1 is preceded by year 0, then by year -1.

The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. It is equivalent to the proleptic Gregorian calendar system, in which today's rules for leap years are applied for all time. For most applications written today, the ISO-8601 rules are entirely suitable. However, any application that makes use of historical dates, and requires them to be accurate will find the ISO-8601 approach unsuitable.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_VALUE](https://developer.android.com/reference/kotlin/java/time/Year#MAX_VALUE:kotlin.Int) The maximum supported year, '+999,999,999'. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_VALUE](https://developer.android.com/reference/kotlin/java/time/Year#MIN_VALUE:kotlin.Int) The minimum supported year, '-999,999,999'. |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)! | [adjustInto](https://developer.android.com/reference/kotlin/java/time/Year#adjustInto(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!`)` Adjusts the specified temporal object to have this year. |
| [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)! | [atDay](https://developer.android.com/reference/kotlin/java/time/Year#atDay(kotlin.Int))`(`dayOfYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Combines this year with a day-of-year to create a `LocalDate`. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth)! | [atMonth](https://developer.android.com/reference/kotlin/java/time/Year#atMonth(kotlin.Int))`(`month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Combines this year with a month to create a `YearMonth`. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth)! | [atMonth](https://developer.android.com/reference/kotlin/java/time/Year#atMonth(java.time.Month))`(`month:` ` [Month](https://developer.android.com/reference/kotlin/java/time/Month)!`)` Combines this year with a month to create a `YearMonth`. |
| [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)! | [atMonthDay](https://developer.android.com/reference/kotlin/java/time/Year#atMonthDay(java.time.MonthDay))`(`monthDay:` ` [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay)!`)` Combines this year with a month-day to create a `LocalDate`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/time/Year#compareTo(java.time.Year))`(`other:` ` [Year](https://developer.android.com/reference/kotlin/java/time/Year#)!`)` Compares this year to another year. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/time/Year#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this year is equal to another year. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/time/Year#format(java.time.format.DateTimeFormatter))`(`formatter:` ` [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!`)` Formats this year using the specified formatter. |
| static [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [from](https://developer.android.com/reference/kotlin/java/time/Year#from(java.time.temporal.TemporalAccessor))`(`temporal:` ` [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor)!`)` Obtains an instance of `Year` from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/Year#get(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the value of the specified field from this year as an `int`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/Year#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the value of the specified field from this year as a `long`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getValue](https://developer.android.com/reference/kotlin/java/time/Year#getValue())`()` Gets the year value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/time/Year#hashCode())`()` A hash code for this year. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfter](https://developer.android.com/reference/kotlin/java/time/Year#isAfter(java.time.Year))`(`other:` ` [Year](https://developer.android.com/reference/kotlin/java/time/Year#)!`)` Checks if this year is after the specified year. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBefore](https://developer.android.com/reference/kotlin/java/time/Year#isBefore(java.time.Year))`(`other:` ` [Year](https://developer.android.com/reference/kotlin/java/time/Year#)!`)` Checks if this year is before the specified year. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeap](https://developer.android.com/reference/kotlin/java/time/Year#isLeap())`()` Checks if the year is a leap year, according to the ISO proleptic calendar system rules. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeap](https://developer.android.com/reference/kotlin/java/time/Year#isLeap(kotlin.Long))`(`year:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Checks if the year is a leap year, according to the ISO proleptic calendar system rules. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/Year#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Checks if the specified field is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/Year#isSupported(java.time.temporal.TemporalUnit))`(`unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Checks if the specified unit is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidMonthDay](https://developer.android.com/reference/kotlin/java/time/Year#isValidMonthDay(java.time.MonthDay))`(`monthDay:` ` [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay)!`)` Checks if the month-day is valid for this year. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/java/time/Year#length())`()` Gets the length of this year in days. |
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [minus](https://developer.android.com/reference/kotlin/java/time/Year#minus(java.time.temporal.TemporalAmount))`(`amountToSubtract:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!`)` Returns a copy of this year with the specified amount subtracted. |
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [minus](https://developer.android.com/reference/kotlin/java/time/Year#minus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Returns a copy of this year with the specified amount subtracted. |
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [minusYears](https://developer.android.com/reference/kotlin/java/time/Year#minusYears(kotlin.Long))`(`yearsToSubtract:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this `Year` with the specified number of years subtracted. |
| static [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [now](https://developer.android.com/reference/kotlin/java/time/Year#now())`()` Obtains the current year from the system clock in the default time-zone. |
| static [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [now](https://developer.android.com/reference/kotlin/java/time/Year#now(java.time.Clock))`(`clock:` ` [Clock](https://developer.android.com/reference/kotlin/java/time/Clock)!`)` Obtains the current year from the specified clock. |
| static [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [now](https://developer.android.com/reference/kotlin/java/time/Year#now(java.time.ZoneId))`(`zone:` ` [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!`)` Obtains the current year from the system clock in the specified time-zone. |
| static [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [of](https://developer.android.com/reference/kotlin/java/time/Year#of(kotlin.Int))`(`isoYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains an instance of `Year`. |
| static [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [parse](https://developer.android.com/reference/kotlin/java/time/Year#parse(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Obtains an instance of `Year` from a text string such as `2007`. |
| static [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [parse](https://developer.android.com/reference/kotlin/java/time/Year#parse(kotlin.CharSequence,%20java.time.format.DateTimeFormatter))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `formatter:` ` [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!`)` Obtains an instance of `Year` from a text string using a specific formatter. |
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [plus](https://developer.android.com/reference/kotlin/java/time/Year#plus(java.time.temporal.TemporalAmount))`(`amountToAdd:` ` [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!`)` Returns a copy of this year with the specified amount added. |
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [plus](https://developer.android.com/reference/kotlin/java/time/Year#plus(kotlin.Long,%20java.time.temporal.TemporalUnit))`(`amountToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Returns a copy of this year with the specified amount added. |
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [plusYears](https://developer.android.com/reference/kotlin/java/time/Year#plusYears(kotlin.Long))`(`yearsToAdd:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this `Year` with the specified number of years added. |
| R | [query](https://developer.android.com/reference/kotlin/java/time/Year#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)<R>!`)` Queries this year using the specified query. |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | [range](https://developer.android.com/reference/kotlin/java/time/Year#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Gets the range of valid values for the specified field. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/time/Year#toString())`()` Outputs this year as a `String`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [until](https://developer.android.com/reference/kotlin/java/time/Year#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit))`(`endExclusive:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!`, `unit:` ` [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!`)` Calculates the amount of time until another year in terms of the specified unit. |
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [with](https://developer.android.com/reference/kotlin/java/time/Year#with(java.time.temporal.TemporalAdjuster))`(`adjuster:` ` [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster)!`)` Returns an adjusted copy of this year. |
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | [with](https://developer.android.com/reference/kotlin/java/time/Year#with(java.time.temporal.TemporalField,%20kotlin.Long))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of this year with the specified field set to a new value. |

## Constants

### MAX_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_VALUE: Int
```

The maximum supported year, '+999,999,999'. 

 Value: 999999999

### MIN_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_VALUE: Int
```

The minimum supported year, '-999,999,999'. 

 Value: -999999999

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have this year.

This returns a temporal object of the same observable type as the input with the year changed to be the same as this.

The adjustment is equivalent to using [Temporal.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long)) passing [ChronoField.YEAR](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) as the field. If the specified temporal object does not use the ISO calendar system then a `DateTimeException` is thrown.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisYear.adjustInto(temporal);
    temporal = temporal.with(thisYear);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!: the target object to be adjusted, not null |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)! | the adjusted object, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### atDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun atDay(dayOfYear: Int): LocalDate!
```

Combines this year with a day-of-year to create a `LocalDate`.

This returns a `LocalDate` formed from this year and the specified day-of-year.

The day-of-year value 366 is only valid in a leap year.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------|
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-year to use, from 1 to 365-366 |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)! | the local date formed from this year and the specified date of year, not null |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the day of year is zero or less, 366 or greater or equal to 366 and this is not a leap year |

### atMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun atMonth(month: Int): YearMonth!
```

Combines this year with a month to create a `YearMonth`.

This returns a `YearMonth` formed from this year and the specified month. All possible combinations of year and month are valid.

This method can be used as part of a chain to produce a date: 

```kotlin
LocalDate date = year.atMonth(month).atDay(day);
  
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to use, from 1 (January) to 12 (December) |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth)! | the year-month formed from this year and the specified month, not null |

| Exceptions ||
|-------------------------------|-------------------------|
| `java.time.DateTimeException` | if the month is invalid |

### atMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun atMonth(month: Month!): YearMonth!
```

Combines this year with a month to create a `YearMonth`.

This returns a `YearMonth` formed from this year and the specified month. All possible combinations of year and month are valid.

This method can be used as part of a chain to produce a date: 

```kotlin
LocalDate date = year.atMonth(month).atDay(day);
  
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `month` | [Month](https://developer.android.com/reference/kotlin/java/time/Month)!: the month-of-year to use, not null |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth)! | the year-month formed from this year and the specified month, not null |

### atMonthDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun atMonthDay(monthDay: MonthDay!): LocalDate!
```

Combines this year with a month-day to create a `LocalDate`.

This returns a `LocalDate` formed from this year and the specified month-day.

A month-day of February 29th will be adjusted to February 28th in the resulting date if the year is not a leap year.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `monthDay` | [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay)!: the month-day to use, not null |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)! | the local date formed from this year and the specified month-day, not null |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: Year!): Int
```

Compares this year to another year.

The comparison is based on the value of the year. It is "consistent with equals", as defined by [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [Year](https://developer.android.com/reference/kotlin/java/time/Year#)!: the other year to compare to, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the comparator value, negative if less, positive if greater |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Checks if this year is equal to another year.

The comparison is based on the time-line position of the years.

| Parameters ||
|-------|-----------------------------------------|
| `obj` | the object to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is equal to the other year |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(formatter: DateTimeFormatter!): String!
```

Formats this year using the specified formatter.

This year will be passed to the formatter to produce a string.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `formatter` | [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!: the formatter to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted year string, not null |

| Exceptions ||
|-------------------------------|------------------------------------|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun from(temporal: TemporalAccessor!): Year!
```

Obtains an instance of `Year` from a temporal object.

This obtains a year based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `Year`.

The conversion extracts the [year](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) field. The extraction is only permitted if the temporal object has an ISO chronology, or can be converted to a `LocalDate`.

This method matches the signature of the functional interface [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery) allowing it to be used as a query via method reference, `Year::from`.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor)!: the temporal object to convert, not null |

| Return ||
|-------------------------------------------------------------------------|--------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | the year, not null |

| Exceptions ||
|-------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to convert to a `Year` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this year as an `int`.

This queries this year for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the query is implemented here. The [supported fields](https://developer.android.com/reference/kotlin/java/time/Year#isSupported(java.time.temporal.TemporalField)) will return valid values based on this year. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to get, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an `int` |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this year as a `long`.

This queries this year for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the query is implemented here. The [supported fields](https://developer.android.com/reference/kotlin/java/time/Year#isSupported(java.time.temporal.TemporalField)) will return valid values based on this year. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to get, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### getValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): Int
```

Gets the year value.

The year returned by this method is proleptic as per `get(YEAR)`.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the year, `MIN_VALUE` to `MAX_VALUE` |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

A hash code for this year.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a suitable hash code |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAfter(other: Year!): Boolean
```

Checks if this year is after the specified year.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `other` | [Year](https://developer.android.com/reference/kotlin/java/time/Year#)!: the other year to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is after the specified year |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBefore(other: Year!): Boolean
```

Checks if this year is before the specified year.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `other` | [Year](https://developer.android.com/reference/kotlin/java/time/Year#)!: the other year to compare to, not null |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this point is before the specified year |

### isLeap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLeap(): Boolean
```

Checks if the year is a leap year, according to the ISO proleptic calendar system rules.

This method applies the current rules for leap years across the whole time-line. In general, a year is a leap year if it is divisible by four without remainder. However, years divisible by 100, are not leap years, with the exception of years divisible by 400 which are.

For example, 1904 is a leap year it is divisible by 4. 1900 was not a leap year as it is divisible by 100, however 2000 was a leap year as it is divisible by 400.

The calculation is proleptic - applying the same rules into the far future and far past. This is historically inaccurate, but is correct for the ISO-8601 standard.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the year is leap, false otherwise |

### isLeap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLeap(year: Long): Boolean
```

Checks if the year is a leap year, according to the ISO proleptic calendar system rules.

This method applies the current rules for leap years across the whole time-line. In general, a year is a leap year if it is divisible by four without remainder. However, years divisible by 100, are not leap years, with the exception of years divisible by 400 which are.

For example, 1904 is a leap year it is divisible by 4. 1900 was not a leap year as it is divisible by 100, however 2000 was a leap year as it is divisible by 400.

The calculation is proleptic - applying the same rules into the far future and far past. This is historically inaccurate, but is correct for the ISO-8601 standard.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `year` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the year to check |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the year is leap, false otherwise |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this year can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/Year#range(java.time.temporal.TemporalField)), [get](https://developer.android.com/reference/kotlin/java/time/Year#get(java.time.temporal.TemporalField)) and [with(java.time.temporal.TemporalField,long)](https://developer.android.com/reference/kotlin/java/time/Year#with(java.time.temporal.TemporalField,%20kotlin.Long)) methods will throw an exception.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the query is implemented here. The supported fields are:

- `YEAR_OF_ERA`
- `YEAR`
- `ERA`

All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field is supported on this year, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this year. If false, then calling the [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/Year#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)) and [minus](https://developer.android.com/reference/kotlin/java/time/Year#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)) methods will throw an exception.

If the unit is a [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit) then the query is implemented here. The supported units are:

- `YEARS`
- `DECADES`
- `CENTURIES`
- `MILLENNIA`
- `ERAS`

All other `ChronoUnit` instances will return false.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.isSupportedBy(Temporal)` passing `this` as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the unit can be added/subtracted, false if not |

### isValidMonthDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isValidMonthDay(monthDay: MonthDay!): Boolean
```

Checks if the month-day is valid for this year.

This method checks whether this year and the input month and day form a valid date.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `monthDay` | [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay)!: the month-day to validate, null returns false |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the month and day are valid for this year |

### length

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun length(): Int
```

Gets the length of this year in days.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of this year in days, 365 or 366 |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(amountToSubtract: TemporalAmount!): Year!
```

Returns a copy of this year with the specified amount subtracted.

This returns a `Year`, based on this one, with the specified amount subtracted. The amount is typically [Period](https://developer.android.com/reference/kotlin/java/time/Period) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount) interface.

The calculation is delegated to the amount object by calling [TemporalAmount.subtractFrom(Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#subtractFrom(java.time.temporal.Temporal)). The amount implementation is free to implement the subtraction in any way it wishes, however it typically calls back to [minus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/Year#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)). Consult the documentation of the amount implementation to determine if it can be successfully subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `amount` | the amount to subtract, not null |
| `amountToSubtract` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!: the amount to subtract, not null |

| Return ||
|-------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | a `Year` based on this year with the subtraction made, not null |

| Exceptions ||
|---------------------------------|-----------------------------------|
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): Year!
```

Returns a copy of this year with the specified amount subtracted.

This returns a `Year`, based on this one, with the amount in terms of the unit subtracted. If it is not possible to subtract the amount, because the unit is not supported or for some other reason, an exception is thrown.

This method is equivalent to [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/Year#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)) with the amount negated. See that method for a full description of how addition, and thus subtraction, works.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to subtract from the result, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit of the amount to subtract, not null |

| Return ||
|-------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | a `Year` based on this year with the specified amount subtracted, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------|
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### minusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minusYears(yearsToSubtract: Long): Year!
```

Returns a copy of this `Year` with the specified number of years subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------|
| `yearsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the years to subtract, may be negative |

| Return ||
|-------------------------------------------------------------------------|----------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | a `Year` based on this year with the year subtracted, not null |

| Exceptions ||
|-------------------------------|-------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(): Year!
```

Obtains the current year from the system clock in the default time-zone.

This will query the [system clock](https://developer.android.com/reference/kotlin/java/time/Clock#systemDefaultZone()) in the default time-zone to obtain the current year.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|-------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | the current year using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(clock: Clock!): Year!
```

Obtains the current year from the specified clock.

This will query the specified clock to obtain the current year. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using [dependency injection](https://developer.android.com/reference/kotlin/java/time/Clock).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `clock` | [Clock](https://developer.android.com/reference/kotlin/java/time/Clock)!: the clock to use, not null |

| Return ||
|-------------------------------------------------------------------------|----------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | the current year, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun now(zone: ZoneId!): Year!
```

Obtains the current year from the system clock in the specified time-zone.

This will query the [system clock](https://developer.android.com/reference/kotlin/java/time/Clock#system(java.time.ZoneId)) to obtain the current year. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!: the zone ID to use, not null |

| Return ||
|-------------------------------------------------------------------------|---------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | the current year using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(isoYear: Int): Year!
```

Obtains an instance of `Year`.

This method accepts a year value from the proleptic ISO calendar system.

The year 2AD/CE is represented by 2. 
The year 1AD/CE is represented by 1. 
The year 1BC/BCE is represented by 0. 
The year 2BC/BCE is represented by -1. 

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `isoYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ISO proleptic year to represent, from `MIN_VALUE` to `MAX_VALUE` |

| Return ||
|-------------------------------------------------------------------------|--------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | the year, not null |

| Exceptions ||
|-------------------------------|-------------------------|
| `java.time.DateTimeException` | if the field is invalid |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(text: CharSequence!): Year!
```

Obtains an instance of `Year` from a text string such as `2007`.

The string must represent a valid year.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse such as "2007", not null |

| Return ||
|-------------------------------------------------------------------------|---------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | the parsed year, not null |

| Exceptions ||
|-------------------------------------------|------------------------------|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(
    text: CharSequence!, 
    formatter: DateTimeFormatter!
): Year!
```

Obtains an instance of `Year` from a text string using a specific formatter.

The text is parsed using the formatter, returning a year.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `formatter` | [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!: the formatter to use, not null |

| Return ||
|-------------------------------------------------------------------------|---------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | the parsed year, not null |

| Exceptions ||
|-------------------------------------------|------------------------------|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(amountToAdd: TemporalAmount!): Year!
```

Returns a copy of this year with the specified amount added.

This returns a `Year`, based on this one, with the specified amount added. The amount is typically [Period](https://developer.android.com/reference/kotlin/java/time/Period) but may be any other type implementing the [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount) interface.

The calculation is delegated to the amount object by calling [TemporalAmount.addTo(Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#addTo(java.time.temporal.Temporal)). The amount implementation is free to implement the addition in any way it wishes, however it typically calls back to [plus(long,java.time.temporal.TemporalUnit)](https://developer.android.com/reference/kotlin/java/time/Year#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)). Consult the documentation of the amount implementation to determine if it can be successfully added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------|
| `amount` | the amount to add, not null |
| `amountToAdd` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!: the amount to add, not null |

| Return ||
|-------------------------------------------------------------------------|--------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | a `Year` based on this year with the addition made, not null |

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
): Year!
```

Returns a copy of this year with the specified amount added.

This returns a `Year`, based on this one, with the amount in terms of the unit added. If it is not possible to add the amount, because the unit is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit) then the addition is implemented here. The supported fields behave as follows:

- `YEARS` - Returns a `Year` with the specified number of years added. This is equivalent to [plusYears(long)](https://developer.android.com/reference/kotlin/java/time/Year#plusYears(kotlin.Long)).
- `DECADES` - Returns a `Year` with the specified number of decades added. This is equivalent to calling [plusYears(long)](https://developer.android.com/reference/kotlin/java/time/Year#plusYears(kotlin.Long)) with the amount multiplied by 10.
- `CENTURIES` - Returns a `Year` with the specified number of centuries added. This is equivalent to calling [plusYears(long)](https://developer.android.com/reference/kotlin/java/time/Year#plusYears(kotlin.Long)) with the amount multiplied by 100.
- `MILLENNIA` - Returns a `Year` with the specified number of millennia added. This is equivalent to calling [plusYears(long)](https://developer.android.com/reference/kotlin/java/time/Year#plusYears(kotlin.Long)) with the amount multiplied by 1,000.
- `ERAS` - Returns a `Year` with the specified number of eras added. Only two eras are supported so the amount must be one, zero or minus one. If the amount is non-zero then the year is changed such that the year-of-era is unchanged.

All other `ChronoUnit` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.addTo(Temporal, long)` passing `this` as the argument. In this case, the unit determines whether and how to perform the addition.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to add to the result, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit of the amount to add, not null |

| Return ||
|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | a `Year` based on this year with the specified amount added, not null |

| Exceptions ||
|-------------------------------------------------------|--------------------------------|
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### plusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plusYears(yearsToAdd: Long): Year!
```

Returns a copy of this `Year` with the specified number of years added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------|
| `yearsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the years to add, may be negative |

| Return ||
|-------------------------------------------------------------------------|------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | a `Year` based on this year with the years added, not null |

| Exceptions ||
|-------------------------------|-------------------------------------------|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this year using the specified query.

This queries this year using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery#queryFrom(java.time.temporal.TemporalAccessor)) method on the specified query passing `this` as the argument.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\<R\>!: the query to invoke, not null |

| Return ||
|---|---------------------------------------------------------------|
| R | the query result, null may be returned (defined by the query) |

| Exceptions ||
|---------------------------------|---------------------------------------------------|
| `java.time.DateTimeException` | if unable to query (defined by the query) |
| `java.lang.ArithmeticException` | if numeric overflow occurs (defined by the query) |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

The range object expresses the minimum and maximum valid values for a field. This year is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the query is implemented here. The [supported fields](https://developer.android.com/reference/kotlin/java/time/Year#isSupported(java.time.temporal.TemporalField)) will return appropriate range instances. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.rangeRefinedBy(TemporalAccessor)` passing `this` as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Outputs this year as a `String`.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this year, not null |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

Calculates the amount of time until another year in terms of the specified unit.

This calculates the amount of time between two `Year` objects in terms of a single `TemporalUnit`. The start and end points are `this` and the specified year. The result will be negative if the end is before the start. The `Temporal` passed to this method is converted to a `Year` using [from(java.time.temporal.TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/Year#from(java.time.temporal.TemporalAccessor)). For example, the amount in decades between two year can be calculated using `startYear.until(endYear, DECADES)`.

The calculation returns a whole number, representing the number of complete units between the two years. For example, the amount in decades between 2012 and 2031 will only be one decade as it is one year short of two decades.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use [TemporalUnit.between(Temporal, Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)): 

```kotlin
// these two lines are equivalent
    amount = start.until(end, YEARS);
    amount = YEARS.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit). The units `YEARS`, `DECADES`, `CENTURIES`, `MILLENNIA` and `ERAS` are supported. Other `ChronoUnit` values will throw an exception.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.between(Temporal, Temporal)` passing `this` as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endExclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!: the end date, exclusive, which is converted to a `Year`, not null |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit to measure the amount in, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the amount of time between this year and the end year |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to a `Year` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun with(adjuster: TemporalAdjuster!): Year!
```

Returns an adjusted copy of this year.

This returns a `Year`, based on this one, with the year adjusted. The adjustment takes place using the specified adjuster strategy object. Read the documentation of the adjuster to understand what adjustment will be made.

The result of this method is obtained by invoking the [TemporalAdjuster.adjustInto(Temporal)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster#adjustInto(java.time.temporal.Temporal)) method on the specified adjuster passing `this` as the argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `adjuster` | [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster)!: the adjuster to use, not null |

| Return ||
|-------------------------------------------------------------------------|-------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | a `Year` based on `this` with the adjustment made, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if the adjustment cannot be made |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun with(
    field: TemporalField!, 
    newValue: Long
): Year!
```

Returns a copy of this year with the specified field set to a new value.

This returns a `Year`, based on this one, with the value for the specified field changed. If it is not possible to set the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField) then the adjustment is implemented here. The supported fields behave as follows:

- `YEAR_OF_ERA` - Returns a `Year` with the specified year-of-era The era will be unchanged.
- `YEAR` - Returns a `Year` with the specified year. This completely replaces the date and is equivalent to [of(int)](https://developer.android.com/reference/kotlin/java/time/Year#of(kotlin.Int)).
- `ERA` - Returns a `Year` with the specified era. The year-of-era will be unchanged.

In all cases, if the new value is outside the valid range of values for the field then a `DateTimeException` will be thrown.

All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.adjustInto(Temporal, long)` passing `this` as the argument. In this case, the field determines whether and how to adjust the instant.

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value of the field in the result |

| Return ||
|-------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Year](https://developer.android.com/reference/kotlin/java/time/Year#)! | a `Year` based on `this` with the specified field set, not null |

| Exceptions ||
|-------------------------------------------------------|-------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
