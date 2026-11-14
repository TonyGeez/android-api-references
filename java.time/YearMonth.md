Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# YearMonth

```
class YearMonth : Comparable<YearMonth!>, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.time.YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#) |

A year-month in the ISO-8601 calendar system, such as `2007-12`.

`YearMonth` is an immutable date-time object that represents the combination of a year and month. Any field that can be derived from a year and month, such as quarter-of-year, can be obtained.

This class does not store or represent a day, time or time-zone. For example, the value "October 2007" can be stored in a `YearMonth`.

The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. It is equivalent to the proleptic Gregorian calendar system, in which today's rules for leap years are applied for all time. For most applications written today, the ISO-8601 rules are entirely suitable. However, any application that makes use of historical dates, and requires them to be accurate will find the ISO-8601 approach unsuitable.

## Summary

| Public methods ||
|---|---|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#adjustInto(java.time.temporal.Temporal)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!)` Adjusts the specified temporal object to have this year-month. |
| [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#atDay(kotlin.Int)(dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Combines this year-month with a day-of-month to create a `LocalDate`. |
| [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#atEndOfMonth()()` Returns a `LocalDate` at the end of the month. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#compareTo(java.time.YearMonth)(other: https://developer.android.com/reference/kotlin/java/time/YearMonth#!)` Compares this year-month to another year-month. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks if this year-month is equal to another year-month. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#format(java.time.format.DateTimeFormatter)(formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Formats this year-month using the specified formatter. |
| static [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Obtains an instance of `YearMonth` from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#get(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this year-month as an `int`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this year-month as a `long`. |
| [Month](https://developer.android.com/reference/kotlin/java/time/Month)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#getMonth()()` Gets the month-of-year field using the `Month` enum. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#getMonthValue()()` Gets the month-of-year field from 1 to 12. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#getYear()()` Gets the year field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#hashCode()()` A hash code for this year-month. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#isAfter(java.time.YearMonth)(other: https://developer.android.com/reference/kotlin/java/time/YearMonth#!)` Checks if this year-month is after the specified year-month. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#isBefore(java.time.YearMonth)(other: https://developer.android.com/reference/kotlin/java/time/YearMonth#!)` Checks if this year-month is before the specified year-month. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#isLeapYear()()` Checks if the year is a leap year, according to the ISO proleptic calendar system rules. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Checks if the specified field is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#isSupported(java.time.temporal.TemporalUnit)(unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Checks if the specified unit is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#isValidDay(kotlin.Int)(dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the day-of-month is valid for this year-month. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#lengthOfMonth()()` Returns the length of the month, taking account of the year. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#lengthOfYear()()` Returns the length of the year. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#minus(java.time.temporal.TemporalAmount)(amountToSubtract: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount!)` Returns a copy of this year-month with the specified amount subtracted. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this year-month with the specified amount subtracted. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#minusMonths(kotlin.Long)(monthsToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `YearMonth` with the specified number of months subtracted. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#minusYears(kotlin.Long)(yearsToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `YearMonth` with the specified number of years subtracted. |
| static [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#now()()` Obtains the current year-month from the system clock in the default time-zone. |
| static [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#now(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock!)` Obtains the current year-month from the specified clock. |
| static [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#now(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId!)` Obtains the current year-month from the system clock in the specified time-zone. |
| static [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#of(kotlin.Int,%20kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `YearMonth` from a year and month. |
| static [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#of(kotlin.Int,%20java.time.Month)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://developer.android.com/reference/kotlin/java/time/Month!)` Obtains an instance of `YearMonth` from a year and month. |
| static [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#parse(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Obtains an instance of `YearMonth` from a text string such as `2007-12`. |
| static [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#parse(kotlin.CharSequence,%20java.time.format.DateTimeFormatter)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Obtains an instance of `YearMonth` from a text string using a specific formatter. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#plus(java.time.temporal.TemporalAmount)(amountToAdd: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount!)` Returns a copy of this year-month with the specified amount added. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this year-month with the specified amount added. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#plusMonths(kotlin.Long)(monthsToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `YearMonth` with the specified number of months added. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#plusYears(kotlin.Long)(yearsToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this `YearMonth` with the specified number of years added. |
| R | `https://developer.android.com/reference/kotlin/java/time/YearMonth#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<R>!)` Queries this year-month using the specified query. |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the range of valid values for the specified field. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#toString()()` Outputs this year-month as a `String`, such as `2007-12`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/YearMonth#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit)(endExclusive: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Calculates the amount of time until another year-month in terms of the specified unit. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#with(java.time.temporal.TemporalAdjuster)(adjuster: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster!)` Returns an adjusted copy of this year-month. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#with(java.time.temporal.TemporalField,%20kotlin.Long)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this year-month with the specified field set to a new value. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#withMonth(kotlin.Int)(month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `YearMonth` with the month-of-year altered. |
| [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)! | `https://developer.android.com/reference/kotlin/java/time/YearMonth#withYear(kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `YearMonth` with the year altered. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have this year-month.

This returns a temporal object of the same observable type as the input with the year and month changed to be the same as this.

The adjustment is equivalent to using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long)` passing `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` as the field. If the specified temporal object does not use the ISO calendar system then a `DateTimeException` is thrown.

In most cases, it is clearer to reverse the calling pattern by using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisYearMonth.adjustInto(temporal);
    temporal = temporal.with(thisYearMonth);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!: the target object to be adjusted, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!` | the adjusted object, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if unable to make the adjustment |

### atDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atDay(dayOfMonth: Int): LocalDate!
```

Combines this year-month with a day-of-month to create a `LocalDate`.

This returns a `LocalDate` formed from this year-month and the specified day-of-month.

The day-of-month value must be valid for the year-month.

This method can be used as part of a chain to produce a date:

```kotlin
LocalDate date = year.atMonth(month).atDay(day);
  
```

| Parameters ||
|---|---|
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to use, from 1 to 31 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate!` | the date formed from this year-month and the specified day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the day is invalid for the year-month |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/YearMonth#isValidDay(kotlin.Int)`

### atEndOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atEndOfMonth(): LocalDate!
```

Returns a `LocalDate` at the end of the month.

This returns a `LocalDate` based on this year-month. The day-of-month is set to the last valid day of the month, taking into account leap years.

This method can be used as part of a chain to produce a date:

```kotlin
LocalDate date = year.atMonth(month).atEndOfMonth();
  
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate!` | the last valid date of this year-month, not null |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: YearMonth!): Int
```

Compares this year-month to another year-month.

The comparison is based first on the value of the year, then on the value of the month. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)!: the other year-month to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, negative if less, positive if greater |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this year-month is equal to another year-month.

The comparison is based on the time-line position of the year-months.

| Parameters ||
|---|---|
| `obj` | the object to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is equal to the other year-month |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(formatter: DateTimeFormatter!): String!
```

Formats this year-month using the specified formatter.

This year-month will be passed to the formatter to produce a string.

| Parameters ||
|---|---|
| `formatter` | [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the formatted year-month string, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): YearMonth!
```

Obtains an instance of `YearMonth` from a temporal object.

This obtains a year-month based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `YearMonth`.

The conversion extracts the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` fields. The extraction is only permitted if the temporal object has an ISO chronology, or can be converted to a `LocalDate`.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery` allowing it to be used as a query via method reference, `YearMonth::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | the year-month, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to a `YearMonth` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this year-month as an `int`.

This queries this year-month for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/YearMonth#isSupported(java.time.temporal.TemporalField)` will return valid values based on this year-month, except `PROLEPTIC_MONTH` which is too large to fit in an `int` and throw a `DateTimeException`. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an `int` |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this year-month as a `long`.

This queries this year-month for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/YearMonth#isSupported(java.time.temporal.TemporalField)` will return valid values based on this year-month. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### getMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMonth(): Month!
```

Gets the month-of-year field using the `Month` enum.

This method returns the enum `https://developer.android.com/reference/kotlin/java/time/Month` for the month. This avoids confusion as to what `int` values mean. If you need access to the primitive `int` value then the enum provides the `https://developer.android.com/reference/kotlin/java/time/Month#getValue()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Month!` | the month-of-year, not null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/YearMonth#getMonthValue()`

### getMonthValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMonthValue(): Int
```

Gets the month-of-year field from 1 to 12.

This method returns the month as an `int` from 1 to 12. Application code is frequently clearer if the enum `https://developer.android.com/reference/kotlin/java/time/Month` is used by calling `https://developer.android.com/reference/kotlin/java/time/YearMonth#getMonth()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the month-of-year, from 1 to 12 |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/YearMonth#getMonth()`

### getYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getYear(): Int
```

Gets the year field.

This method returns the primitive `int` value for the year.

The year returned by this method is proleptic as per `get(YEAR)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the year, from MIN_YEAR to MAX_YEAR |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

A hash code for this year-month.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAfter(other: YearMonth!): Boolean
```

Checks if this year-month is after the specified year-month.

| Parameters ||
|---|---|
| `other` | [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)!: the other year-month to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is after the specified year-month |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBefore(other: YearMonth!): Boolean
```

Checks if this year-month is before the specified year-month.

| Parameters ||
|---|---|
| `other` | [YearMonth](https://developer.android.com/reference/kotlin/java/time/YearMonth#)!: the other year-month to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this point is before the specified year-month |

### isLeapYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeapYear(): Boolean
```

Checks if the year is a leap year, according to the ISO proleptic calendar system rules.

This method applies the current rules for leap years across the whole time-line. In general, a year is a leap year if it is divisible by four without remainder. However, years divisible by 100, are not leap years, with the exception of years divisible by 400 which are.

For example, 1904 is a leap year it is divisible by 4. 1900 was not a leap year as it is divisible by 100, however 2000 was a leap year as it is divisible by 400.

The calculation is proleptic - applying the same rules into the far future and far past. This is historically inaccurate, but is correct for the ISO-8601 standard.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the year is leap, false otherwise |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this year-month can be queried for the specified field. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/YearMonth#range(java.time.temporal.TemporalField)`, `https://developer.android.com/reference/kotlin/java/time/YearMonth#get(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/YearMonth#with(java.time.temporal.TemporalField,%20kotlin.Long)` methods will throw an exception.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The supported fields are:

- `MONTH_OF_YEAR`
- `PROLEPTIC_MONTH`
- `YEAR_OF_ERA`
- `YEAR`
- `ERA`

All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field is supported on this year-month, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this year-month. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/YearMonth#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` and `https://developer.android.com/reference/kotlin/java/time/YearMonth#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)` methods will throw an exception.

If the unit is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` then the query is implemented here. The supported units are:

- `MONTHS`
- `YEARS`
- `DECADES`
- `CENTURIES`
- `MILLENNIA`
- `ERAS`

All other `ChronoUnit` instances will return false.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.isSupportedBy(Temporal)` passing `this` as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|---|---|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the unit can be added/subtracted, false if not |

### isValidDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isValidDay(dayOfMonth: Int): Boolean
```

Checks if the day-of-month is valid for this year-month.

This method checks whether this year and month and the input day form a valid date.

| Parameters ||
|---|---|
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to validate, from 1 to 31, invalid value returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the day is valid for this year-month |

### lengthOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lengthOfMonth(): Int
```

Returns the length of the month, taking account of the year.

This returns the length of the month in days. For example, a date in January would return 31.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the length of the month in days, from 28 to 31 |

### lengthOfYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lengthOfYear(): Int
```

Returns the length of the year.

This returns the length of the year in days, either 365 or 366.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | 366 if the year is leap, 365 otherwise |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(amountToSubtract: TemporalAmount!): YearMonth!
```

Returns a copy of this year-month with the specified amount subtracted.

This returns a `YearMonth`, based on this one, with the specified amount subtracted. The amount is typically `https://developer.android.com/reference/kotlin/java/time/Period` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount` interface.

The calculation is delegated to the amount object by calling `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#subtractFrom(java.time.temporal.Temporal)`. The amount implementation is free to implement the subtraction in any way it wishes, however it typically calls back to `https://developer.android.com/reference/kotlin/java/time/YearMonth#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)`. Consult the documentation of the amount implementation to determine if it can be successfully subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to subtract, not null |
| `amountToSubtract` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!: the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the subtraction made, not null |

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
): YearMonth!
```

Returns a copy of this year-month with the specified amount subtracted.

This returns a `YearMonth`, based on this one, with the amount in terms of the unit subtracted. If it is not possible to subtract the amount, because the unit is not supported or for some other reason, an exception is thrown.

This method is equivalent to `https://developer.android.com/reference/kotlin/java/time/YearMonth#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` with the amount negated. See that method for a full description of how addition, and thus subtraction, works.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to subtract from the result, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit of the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the specified amount subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### minusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusMonths(monthsToSubtract: Long): YearMonth!
```

Returns a copy of this `YearMonth` with the specified number of months subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `monthsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the months to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the months subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### minusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusYears(yearsToSubtract: Long): YearMonth!
```

Returns a copy of this `YearMonth` with the specified number of years subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `yearsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the years to subtract, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the years subtracted, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(): YearMonth!
```

Obtains the current year-month from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#systemDefaultZone()` in the default time-zone to obtain the current year-month.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | the current year-month using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(clock: Clock!): YearMonth!
```

Obtains the current year-month from the specified clock.

This will query the specified clock to obtain the current year-month. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock`.

| Parameters ||
|---|---|
| `clock` | [Clock](https://developer.android.com/reference/kotlin/java/time/Clock)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | the current year-month, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(zone: ZoneId!): YearMonth!
```

Obtains the current year-month from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#system(java.time.ZoneId)` to obtain the current year-month. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | the current year-month using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    year: Int, 
    month: Int
): YearMonth!
```

Obtains an instance of `YearMonth` from a year and month.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to represent, from MIN_YEAR to MAX_YEAR |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to represent, from 1 (January) to 12 (December) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | the year-month, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if either field value is invalid |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    year: Int, 
    month: Month!
): YearMonth!
```

Obtains an instance of `YearMonth` from a year and month.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to represent, from MIN_YEAR to MAX_YEAR |
| `month` | [Month](https://developer.android.com/reference/kotlin/java/time/Month)!: the month-of-year to represent, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | the year-month, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the year value is invalid |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(text: CharSequence!): YearMonth!
```

Obtains an instance of `YearMonth` from a text string such as `2007-12`.

The string must represent a valid year-month. The format must be `uuuu-MM`. Years outside the range 0000 to 9999 must be prefixed by the plus or minus symbol.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse such as "2007-12", not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | the parsed year-month, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(
    text: CharSequence!, 
    formatter: DateTimeFormatter!
): YearMonth!
```

Obtains an instance of `YearMonth` from a text string using a specific formatter.

The text is parsed using the formatter, returning a year-month.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `formatter` | [DateTimeFormatter](https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | the parsed year-month, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(amountToAdd: TemporalAmount!): YearMonth!
```

Returns a copy of this year-month with the specified amount added.

This returns a `YearMonth`, based on this one, with the specified amount added. The amount is typically `https://developer.android.com/reference/kotlin/java/time/Period` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount` interface.

The calculation is delegated to the amount object by calling `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#addTo(java.time.temporal.Temporal)`. The amount implementation is free to implement the addition in any way it wishes, however it typically calls back to `https://developer.android.com/reference/kotlin/java/time/YearMonth#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)`. Consult the documentation of the amount implementation to determine if it can be successfully added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to add, not null |
| `amountToAdd` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!: the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the addition made, not null |

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
): YearMonth!
```

Returns a copy of this year-month with the specified amount added.

This returns a `YearMonth`, based on this one, with the amount in terms of the unit added. If it is not possible to add the amount, because the unit is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` then the addition is implemented here. The supported fields behave as follows:

- `MONTHS` - Returns a `YearMonth` with the specified number of months added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/YearMonth#plusMonths(kotlin.Long)`.
- `YEARS` - Returns a `YearMonth` with the specified number of years added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/YearMonth#plusYears(kotlin.Long)`.
- `DECADES` - Returns a `YearMonth` with the specified number of decades added. This is equivalent to calling `https://developer.android.com/reference/kotlin/java/time/YearMonth#plusYears(kotlin.Long)` with the amount multiplied by 10.
- `CENTURIES` - Returns a `YearMonth` with the specified number of centuries added. This is equivalent to calling `https://developer.android.com/reference/kotlin/java/time/YearMonth#plusYears(kotlin.Long)` with the amount multiplied by 100.
- `MILLENNIA` - Returns a `YearMonth` with the specified number of millennia added. This is equivalent to calling `https://developer.android.com/reference/kotlin/java/time/YearMonth#plusYears(kotlin.Long)` with the amount multiplied by 1,000.
- `ERAS` - Returns a `YearMonth` with the specified number of eras added. Only two eras are supported so the amount must be one, zero or minus one. If the amount is non-zero then the year is changed such that the year-of-era is unchanged.

All other `ChronoUnit` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.addTo(Temporal, long)` passing `this` as the argument. In this case, the unit determines whether and how to perform the addition.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to add to the result, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit of the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the specified amount added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### plusMonths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusMonths(monthsToAdd: Long): YearMonth!
```

Returns a copy of this `YearMonth` with the specified number of months added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `monthsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the months to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the months added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### plusYears

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusYears(yearsToAdd: Long): YearMonth!
```

Returns a copy of this `YearMonth` with the specified number of years added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `yearsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the years to add, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the years added, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this year-month using the specified query.

This queries this year-month using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery#queryFrom(java.time.temporal.TemporalAccessor)` method on the specified query passing `this` as the argument.

| Parameters ||
|---|---|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\<R\>!: the query to invoke, not null |

| Return ||
|---|---|
| `R` | the query result, null may be returned (defined by the query) |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs (defined by the query) |
| `java.time.DateTimeException` | if unable to query (defined by the query) |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

The range object expresses the minimum and maximum valid values for a field. This year-month is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/YearMonth#isSupported(java.time.temporal.TemporalField)` will return appropriate range instances. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.rangeRefinedBy(TemporalAccessor)` passing `this` as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to query the range for, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange!` | the range of valid values for the field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Outputs this year-month as a `String`, such as `2007-12`.

The output will be in the format `uuuu-MM`:

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this year-month, not null |

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

Calculates the amount of time until another year-month in terms of the specified unit.

This calculates the amount of time between two `YearMonth` objects in terms of a single `TemporalUnit`. The start and end points are `this` and the specified year-month. The result will be negative if the end is before the start. The `Temporal` passed to this method is converted to a `YearMonth` using `https://developer.android.com/reference/kotlin/java/time/YearMonth#from(java.time.temporal.TemporalAccessor)`. For example, the amount in years between two year-months can be calculated using `startYearMonth.until(endYearMonth, YEARS)`.

The calculation returns a whole number, representing the number of complete units between the two year-months. For example, the amount in decades between 2012-06 and 2032-05 will only be one decade as it is one month short of two decades.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)`:

```kotlin
// these two lines are equivalent
    amount = start.until(end, MONTHS);
    amount = MONTHS.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit`. The units `MONTHS`, `YEARS`, `DECADES`, `CENTURIES`, `MILLENNIA` and `ERAS` are supported. Other `ChronoUnit` values will throw an exception.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.between(Temporal, Temporal)` passing `this` as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `endExclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!: the end date, exclusive, which is converted to a `YearMonth`, not null |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit to measure the amount in, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the amount of time between this year-month and the end year-month |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to a `YearMonth` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(adjuster: TemporalAdjuster!): YearMonth!
```

Returns an adjusted copy of this year-month.

This returns a `YearMonth`, based on this one, with the year-month adjusted. The adjustment takes place using the specified adjuster strategy object. Read the documentation of the adjuster to understand what adjustment will be made.

A simple adjuster might simply set the one of the fields, such as the year field. A more complex adjuster might set the year-month to the next month that Halley's comet will pass the Earth.

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster#adjustInto(java.time.temporal.Temporal)` method on the specified adjuster passing `this` as the argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `adjuster` | [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster)!: the adjuster to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on `this` with the adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the adjustment cannot be made |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(
    field: TemporalField!, 
    newValue: Long
): YearMonth!
```

Returns a copy of this year-month with the specified field set to a new value.

This returns a `YearMonth`, based on this one, with the value for the specified field changed. This can be used to change any supported field, such as the year or month. If it is not possible to set the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the adjustment is implemented here. The supported fields behave as follows:

- `MONTH_OF_YEAR` - Returns a `YearMonth` with the specified month-of-year. The year will be unchanged.
- `PROLEPTIC_MONTH` - Returns a `YearMonth` with the specified proleptic-month. This completely replaces the year and month of this object.
- `YEAR_OF_ERA` - Returns a `YearMonth` with the specified year-of-era The month and era will be unchanged.
- `YEAR` - Returns a `YearMonth` with the specified year. The month will be unchanged.
- `ERA` - Returns a `YearMonth` with the specified era. The month and year-of-era will be unchanged.

In all cases, if the new value is outside the valid range of values for the field then a `DateTimeException` will be thrown.

All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.adjustInto(Temporal, long)` passing `this` as the argument. In this case, the field determines whether and how to adjust the instant.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value of the field in the result |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on `this` with the specified field set, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### withMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withMonth(month: Int): YearMonth!
```

Returns a copy of this `YearMonth` with the month-of-year altered.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to set in the returned year-month, from 1 (January) to 12 (December) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the requested month, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the month-of-year value is invalid |

### withYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withYear(year: Int): YearMonth!
```

Returns a copy of this `YearMonth` with the year altered.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to set in the returned year-month, from MIN_YEAR to MAX_YEAR |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/YearMonth#!` | a `YearMonth` based on this year-month with the requested year, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the year value is invalid |
