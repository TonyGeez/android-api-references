# Month

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Month

```
class Month : TemporalAccessor, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.Month](../java/time/Month.md)\> ||
| | ↳ | [java.time.Month](../java/time/Month.md) |

| Known Direct Subclasses [Month.APRIL](../java/time/Month.md), [Month.AUGUST](../java/time/Month.md), [Month.DECEMBER](../java/time/Month.md), [Month.FEBRUARY](../java/time/Month.md), [Month.JANUARY](../java/time/Month.md), [Month.JULY](../java/time/Month.md), [Month.JUNE](../java/time/Month.md), [Month.MARCH](../java/time/Month.md), [Month.MAY](../java/time/Month.md), [Month.NOVEMBER](../java/time/Month.md), [Month.OCTOBER](../java/time/Month.md), [Month.SEPTEMBER](../java/time/Month.md) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------| | [Month.APRIL](../java/time/Month.md) | The singleton instance for the month of April with 30 days. | | [Month.AUGUST](../java/time/Month.md) | The singleton instance for the month of August with 31 days. | | [Month.DECEMBER](../java/time/Month.md) | The singleton instance for the month of December with 31 days. | | [Month.FEBRUARY](../java/time/Month.md) | The singleton instance for the month of February with 28 days, or 29 in a leap year. | | [Month.JANUARY](../java/time/Month.md) | The singleton instance for the month of January with 31 days. | | [Month.JULY](../java/time/Month.md) | The singleton instance for the month of July with 31 days. | | [Month.JUNE](../java/time/Month.md) | The singleton instance for the month of June with 30 days. | | [Month.MARCH](../java/time/Month.md) | The singleton instance for the month of March with 31 days. | | [Month.MAY](../java/time/Month.md) | The singleton instance for the month of May with 31 days. | | [Month.NOVEMBER](../java/time/Month.md) | The singleton instance for the month of November with 30 days. | | [Month.OCTOBER](../java/time/Month.md) | The singleton instance for the month of October with 31 days. | | [Month.SEPTEMBER](../java/time/Month.md) | The singleton instance for the month of September with 30 days. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A month-of-year, such as 'July'.

`Month`is an enum representing the 12 months of the year - January, February, March, April, May, June, July, August, September, October, November and December.

In addition to the textual enum name, each month-of-year has an`int`value. The`int`value follows normal usage and the ISO-8601 standard, from 1 (January) to 12 (December). It is recommended that applications use the enum rather than the`int`value to ensure code clarity.

**Do not use`ordinal()`to obtain the numeric representation of`Month`. Use`getValue()`instead.**

This enum represents a common concept that is found in many calendar systems. As such, this enum may be used by any calendar system that has the month-of-year concept defined exactly equivalent to the ISO-8601 calendar system.

## Summary

| Enum values ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [APRIL](../java/time/Month.md) The singleton instance for the month of April with 30 days. |
| [AUGUST](../java/time/Month.md) The singleton instance for the month of August with 31 days. |
| [DECEMBER](../java/time/Month.md) The singleton instance for the month of December with 31 days. |
| [FEBRUARY](../java/time/Month.md) The singleton instance for the month of February with 28 days, or 29 in a leap year. |
| [JANUARY](../java/time/Month.md) The singleton instance for the month of January with 31 days. |
| [JULY](../java/time/Month.md) The singleton instance for the month of July with 31 days. |
| [JUNE](../java/time/Month.md) The singleton instance for the month of June with 30 days. |
| [MARCH](../java/time/Month.md) The singleton instance for the month of March with 31 days. |
| [MAY](../java/time/Month.md) The singleton instance for the month of May with 31 days. |
| [NOVEMBER](../java/time/Month.md) The singleton instance for the month of November with 30 days. |
| [OCTOBER](../java/time/Month.md) The singleton instance for the month of October with 31 days. |
| [SEPTEMBER](../java/time/Month.md) The singleton instance for the month of September with 30 days. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | [adjustInto](../java/time/Month.md))`(`temporal:` ` [Temporal](../java/time/temporal/Temporal.md)!`)` Adjusts the specified temporal object to have this month-of-year. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [firstDayOfYear](../java/time/Month.md))`(`leapYear:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Gets the day-of-year corresponding to the first day of this month. |
| [Month](../java/time/Month.md)! | [firstMonthOfQuarter](../java/time/Month.md))`()` Gets the month corresponding to the first month of this quarter. |
| --- | --- |
| static [Month](../java/time/Month.md)! | [from](../java/time/Month.md))`(`temporal:` ` [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)!`)` Obtains an instance of`Month`from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](../java/time/Month.md))`(`field:` ` [TemporalField](../java/time/temporal/TemporalField.md)!`)` Gets the value of the specified field from this month-of-year as an`int`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../java/time/Month.md))`(`style:` ` [TextStyle](../java/time/format/TextStyle.md)!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` Gets the textual representation, such as 'Jan' or 'December'. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java/time/Month.md))`(`field:` ` [TemporalField](../java/time/temporal/TemporalField.md)!`)` Gets the value of the specified field from this month-of-year as a`long`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getValue](../java/time/Month.md))`()` Gets the month-of-year`int`value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](../java/time/Month.md))`(`field:` ` [TemporalField](../java/time/temporal/TemporalField.md)!`)` Checks if the specified field is supported. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](../java/time/Month.md))`(`leapYear:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Gets the length of this month in days. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [maxLength](../java/time/Month.md))`()` Gets the maximum length of this month in days. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [minLength](../java/time/Month.md))`()` Gets the minimum length of this month in days. |
| --- | --- |
| [Month](../java/time/Month.md)! | [minus](../java/time/Month.md))`(`months:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the month-of-year that is the specified number of months before this one. |
| static [Month](../java/time/Month.md)! | [of](../java/time/Month.md))`(`month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains an instance of`Month`from an`int`value. |
| [Month](../java/time/Month.md)! | [plus](../java/time/Month.md))`(`months:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the month-of-year that is the specified number of months after this one. |
| --- | --- |
| R | [query](../java/time/Month.md))`(`query:` ` [TemporalQuery](../java/time/temporal/TemporalQuery.md)<R>!`)` Queries this month-of-year using the specified query. |
| [ValueRange](../java/time/temporal/ValueRange.md)! | [range](../java/time/Month.md))`(`field:` ` [TemporalField](../java/time/temporal/TemporalField.md)!`)` Gets the range of valid values for the specified field. |

## Enum values

### APRIL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val APRIL : Month
```

The singleton instance for the month of April with 30 days. This has the numeric value of`4`. 

### AUGUST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val AUGUST : Month
```

The singleton instance for the month of August with 31 days. This has the numeric value of`8`. 

### DECEMBER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DECEMBER : Month
```

The singleton instance for the month of December with 31 days. This has the numeric value of`12`. 

### FEBRUARY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val FEBRUARY : Month
```

The singleton instance for the month of February with 28 days, or 29 in a leap year. This has the numeric value of`2`. 

### JANUARY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val JANUARY : Month
```

The singleton instance for the month of January with 31 days. This has the numeric value of`1`. 

### JULY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val JULY : Month
```

The singleton instance for the month of July with 31 days. This has the numeric value of`7`. 

### JUNE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val JUNE : Month
```

The singleton instance for the month of June with 30 days. This has the numeric value of`6`. 

### MARCH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MARCH : Month
```

The singleton instance for the month of March with 31 days. This has the numeric value of`3`. 

### MAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MAY : Month
```

The singleton instance for the month of May with 31 days. This has the numeric value of`5`. 

### NOVEMBER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NOVEMBER : Month
```

The singleton instance for the month of November with 30 days. This has the numeric value of`11`. 

### OCTOBER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val OCTOBER : Month
```

The singleton instance for the month of October with 31 days. This has the numeric value of`10`. 

### SEPTEMBER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SEPTEMBER : Month
```

The singleton instance for the month of September with 30 days. This has the numeric value of`9`.

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have this month-of-year.

This returns a temporal object of the same observable type as the input with the month-of-year changed to be the same as this.

The adjustment is equivalent to using [Temporal.with(TemporalField, long)](../java/time/temporal/Temporal.md))passing [ChronoField.MONTH_OF_YEAR](../java/time/temporal/ChronoField.md) as the field. If the specified temporal object does not use the ISO calendar system then a`DateTimeException`is thrown.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](../java/time/temporal/Temporal.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisMonth.adjustInto(temporal);
    temporal = temporal.with(thisMonth);
  
```

For example, given a date in May, the following are output: 

```kotlin
dateInMay.with(JANUARY);    // four months earlier
    dateInMay.with(APRIL);      // one months earlier
    dateInMay.with(MAY);        // same date
    dateInMay.with(JUNE);       // one month later
    dateInMay.with(DECEMBER);   // seven months later
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java/time/temporal/Temporal.md)!:the target object to be adjusted, not null |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | the adjusted object, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### firstDayOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun firstDayOfYear(leapYear: Boolean): Int
```

Gets the day-of-year corresponding to the first day of this month.

This returns the day-of-year that this month begins on, using the leap year flag to determine the length of February.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `leapYear` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the length is required for a leap year |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the day of year corresponding to the first day of this month, from 1 to 336 |

### firstMonthOfQuarter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun firstMonthOfQuarter(): Month!
```

Gets the month corresponding to the first month of this quarter.

The year can be divided into four quarters. This method returns the first month of the quarter for the base month. January, February and March return January. April, May and June return April. July, August and September return July. October, November and December return October.

| Return ||
|---------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Month](../java/time/Month.md)! | the first month of the quarter corresponding to this month, not null |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun from(temporal: TemporalAccessor!): Month!
```

Obtains an instance of`Month`from a temporal object.

This obtains a month based on the specified temporal. A`TemporalAccessor`represents an arbitrary set of date and time information, which this factory converts to an instance of`Month`.

The conversion extracts the [MONTH_OF_YEAR](../java/time/temporal/ChronoField.md) field. The extraction is only permitted if the temporal object has an ISO chronology, or can be converted to a`LocalDate`.

This method matches the signature of the functional interface [TemporalQuery](../java/time/temporal/TemporalQuery.md) allowing it to be used as a query via method reference,`Month::from`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)!:the temporal object to convert, not null |

| Return ||
|---------------------------------------------------------------------------|-----------------------------|
| [Month](../java/time/Month.md)! | the month-of-year, not null |

| Exceptions ||
|-------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to convert to a`Month` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this month-of-year as an`int`.

This queries this month for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is [MONTH_OF_YEAR](../java/time/temporal/ChronoField.md) then the value of the month-of-year, from 1 to 12, will be returned. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!:the field to get, not null |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value for the field, within the valid range of values |

| Exceptions ||
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an`int` |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getDisplayName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(
    style: TextStyle!, 
    locale: Locale!
): String!
```

Gets the textual representation, such as 'Jan' or 'December'.

This returns the textual name used to identify the month-of-year, suitable for presentation to the user. The parameters control the style of the returned text and the locale.

If no textual mapping is found then the [numeric value](../java/time/Month.md))is returned.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `style` | [TextStyle](../java/time/format/TextStyle.md)!:the length of the text required, not null |
| `locale` | [Locale](../java/util/Locale.md)!:the locale to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the text value of the month-of-year, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this month-of-year as a`long`.

This queries this month for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is [MONTH_OF_YEAR](../java/time/temporal/ChronoField.md) then the value of the month-of-year, from 1 to 12, will be returned. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!:the field to get, not null |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|---------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): Int
```

Gets the month-of-year`int`value.

The values are numbered following the ISO-8601 standard, from 1 (January) to 12 (December).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the month-of-year, from 1 (January) to 12 (December) |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this month-of-year can be queried for the specified field. If false, then calling the [range](../java/time/Month.md))and [get](../java/time/Month.md))methods will throw an exception.

If the field is [MONTH_OF_YEAR](../java/time/temporal/ChronoField.md) then this method returns true. All other`ChronoField`instances will return false.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!:the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field is supported on this month-of-year, false if not |

### length

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun length(leapYear: Boolean): Int
```

Gets the length of this month in days.

This takes a flag to determine whether to return the length for a leap year or not.

February has 28 days in a standard year and 29 days in a leap year. April, June, September and November have 30 days. All other months have 31 days.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `leapYear` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the length is required for a leap year |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of this month in days, from 28 to 31 |

### maxLength

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun maxLength(): Int
```

Gets the maximum length of this month in days.

February has a maximum length of 29 days. April, June, September and November have 30 days. All other months have 31 days.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum length of this month in days, from 29 to 31 |

### minLength

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minLength(): Int
```

Gets the minimum length of this month in days.

February has a minimum length of 28 days. April, June, September and November have 30 days. All other months have 31 days.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum length of this month in days, from 28 to 31 |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun minus(months: Long): Month!
```

Returns the month-of-year that is the specified number of months before this one.

The calculation rolls around the start of the year from January to December. The specified period may be negative.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `months` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the months to subtract, positive or negative |

| Return ||
|---------------------------------------------------------------------------|-------------------------------|
| [Month](../java/time/Month.md)! | the resulting month, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(month: Int): Month!
```

Obtains an instance of`Month`from an`int`value.

`Month`is an enum representing the 12 months of the year. This factory allows the enum to be obtained from the`int`value. The`int`value follows the ISO-8601 standard, from 1 (January) to 12 (December).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the month-of-year to represent, from 1 (January) to 12 (December) |

| Return ||
|---------------------------------------------------------------------------|-----------------------------|
| [Month](../java/time/Month.md)! | the month-of-year, not null |

| Exceptions ||
|-------------------------------|---------------------------------|
| `java.time.DateTimeException` | if the month-of-year is invalid |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun plus(months: Long): Month!
```

Returns the month-of-year that is the specified number of months after this one.

The calculation rolls around the end of the year from December to January. The specified period may be negative.

This instance is immutable and unaffected by this method call.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `months` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the months to add, positive or negative |

| Return ||
|---------------------------------------------------------------------------|-------------------------------|
| [Month](../java/time/Month.md)! | the resulting month, not null |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this month-of-year using the specified query.

This queries this month-of-year using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](../java/time/temporal/TemporalQuery.md))method on the specified query passing`this`as the argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](../java/time/temporal/TemporalQuery.md)\<R\>!:the query to invoke, not null |

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

The range object expresses the minimum and maximum valid values for a field. This month is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is [MONTH_OF_YEAR](../java/time/temporal/ChronoField.md) then the range of the month-of-year, from 1 to 12, will be returned. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.rangeRefinedBy(TemporalAccessor)`passing`this`as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](../java/time/temporal/ValueRange.md)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
