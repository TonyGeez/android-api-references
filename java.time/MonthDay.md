Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MonthDay

```
class MonthDay : Comparable<MonthDay!>, Serializable, TemporalAccessor, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.MonthDay](../java/time/MonthDay.md) |

A month-day in the ISO-8601 calendar system, such as `--12-03`.

`MonthDay` is an immutable date-time object that represents the combination of a month and day-of-month. Any field that can be derived from a month and day, such as quarter-of-year, can be obtained.

This class does not store or represent a year, time or time-zone. For example, the value "December 3rd" can be stored in a `MonthDay`.

Since a `MonthDay` does not possess a year, the leap day of February 29th is considered valid.

This class implements `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor` rather than `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal`. This is because it is not possible to define whether February 29th is valid or not without external information, preventing the implementation of plus/minus. Related to this, `MonthDay` only provides access to query and set the fields `MONTH_OF_YEAR` and `DAY_OF_MONTH`.

The ISO-8601 calendar system is the modern civil calendar system used today in most of the world. It is equivalent to the proleptic Gregorian calendar system, in which today's rules for leap years are applied for all time. For most applications written today, the ISO-8601 rules are entirely suitable. However, any application that makes use of historical dates, and requires them to be accurate will find the ISO-8601 approach unsuitable.

## Summary

| Public methods ||
|---|---|
| [Temporal](../java/time/temporal/Temporal.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#adjustInto(java.time.temporal.Temporal)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!)` Adjusts the specified temporal object to have this month-day. |
| [LocalDate](../java/time/LocalDate.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#atYear(kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Combines this month-day with a year to create a `LocalDate`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#compareTo(java.time.MonthDay)(other: https://developer.android.com/reference/kotlin/java/time/MonthDay#!)` Compares this month-day to another month-day. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks if this month-day is equal to another month-day. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#format(java.time.format.DateTimeFormatter)(formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Formats this month-day using the specified formatter. |
| static [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Obtains an instance of `MonthDay` from a temporal object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#get(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this month-day as an `int`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#getDayOfMonth()()` Gets the day-of-month field. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this month-day as a `long`. |
| --- | --- |
| [Month](../java/time/Month.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#getMonth()()` Gets the month-of-year field using the `Month` enum. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#getMonthValue()()` Gets the month-of-year field from 1 to 12. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#hashCode()()` A hash code for this month-day. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#isAfter(java.time.MonthDay)(other: https://developer.android.com/reference/kotlin/java/time/MonthDay#!)` Checks if this month-day is after the specified month-day. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#isBefore(java.time.MonthDay)(other: https://developer.android.com/reference/kotlin/java/time/MonthDay#!)` Checks if this month-day is before the specified month-day. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Checks if the specified field is supported. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#isValidYear(kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the year is valid for this month-day. |
| static [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#now()()` Obtains the current month-day from the system clock in the default time-zone. |
| static [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#now(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock!)` Obtains the current month-day from the specified clock. |
| --- | --- |
| static [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#now(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId!)` Obtains the current month-day from the system clock in the specified time-zone. |
| static [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#of(kotlin.Int,%20kotlin.Int)(month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `MonthDay`. |
| static [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#of(java.time.Month,%20kotlin.Int)(month: https://developer.android.com/reference/kotlin/java/time/Month!, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `MonthDay`. |
| --- | --- |
| static [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#parse(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Obtains an instance of `MonthDay` from a text string such as `--12-03`. |
| static [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#parse(kotlin.CharSequence,%20java.time.format.DateTimeFormatter)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, formatter: https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter!)` Obtains an instance of `MonthDay` from a text string using a specific formatter. |
| R | `https://developer.android.com/reference/kotlin/java/time/MonthDay#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<R>!)` Queries this month-day using the specified query. |
| --- | --- |
| [ValueRange](../java/time/temporal/ValueRange.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the range of valid values for the specified field. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/MonthDay#toString()()` Outputs this month-day as a `String`, such as `--12-03`. |
| [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#with(java.time.Month)(month: https://developer.android.com/reference/kotlin/java/time/Month!)` Returns a copy of this `MonthDay` with the month-of-year altered. |
| --- | --- |
| [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#withDayOfMonth(kotlin.Int)(dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `MonthDay` with the day-of-month altered. |
| [MonthDay](../java/time/MonthDay.md)! | `https://developer.android.com/reference/kotlin/java/time/MonthDay#withMonth(kotlin.Int)(month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a copy of this `MonthDay` with the month-of-year altered. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have this month-day.

This returns a temporal object of the same observable type as the input with the month and day-of-month changed to be the same as this.

The adjustment is equivalent to using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long)` twice, passing `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` as the fields. If the specified temporal object does not use the ISO calendar system then a `DateTimeException` is thrown.

In most cases, it is clearer to reverse the calling pattern by using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisMonthDay.adjustInto(temporal);
    temporal = temporal.with(thisMonthDay);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `temporal` | [Temporal](../java/time/temporal/Temporal.md)!: the target object to be adjusted, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!` | the adjusted object, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if unable to make the adjustment |

### atYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atYear(year: Int): LocalDate!
```

Combines this month-day with a year to create a `LocalDate`.

This returns a `LocalDate` formed from this month-day and the specified year.

A month-day of February 29th will be adjusted to February 28th in the resulting date if the year is not a leap year.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to use, from MIN_YEAR to MAX_YEAR |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate!` | the local date formed from this month-day and the specified year, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the year is outside the valid range of years |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: MonthDay!): Int
```

Compares this month-day to another month-day.

The comparison is based first on value of the month, then on the value of the day. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [MonthDay](../java/time/MonthDay.md)!: the other month-day to compare to, not null |

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

Checks if this month-day is equal to another month-day.

The comparison is based on the time-line position of the month-day within a year.

| Parameters ||
|---|---|
| `obj` | the object to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is equal to the other month-day |

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(formatter: DateTimeFormatter!): String!
```

Formats this month-day using the specified formatter.

This month-day will be passed to the formatter to produce a string.

| Parameters ||
|---|---|
| `formatter` | [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the formatted month-day string, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if an error occurs during printing |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): MonthDay!
```

Obtains an instance of `MonthDay` from a temporal object.

This obtains a month-day based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `MonthDay`.

The conversion extracts the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` fields. The extraction is only permitted if the temporal object has an ISO chronology, or can be converted to a `LocalDate`.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery` allowing it to be used as a query via method reference, `MonthDay::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | the month-day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to a `MonthDay` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this month-day as an `int`.

This queries this month-day for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/MonthDay#isSupported(java.time.temporal.TemporalField)` will return valid values based on this month-day. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an `int` |
| --- | --- |

### getDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDayOfMonth(): Int
```

Gets the day-of-month field.

This method returns the primitive `int` value for the day-of-month.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the day-of-month, from 1 to 31 |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this month-day as a `long`.

This queries this month-day for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/MonthDay#isSupported(java.time.temporal.TemporalField)` will return valid values based on this month-day. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |

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

- `https://developer.android.com/reference/kotlin/java/time/MonthDay#getMonthValue()`

### getMonthValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMonthValue(): Int
```

Gets the month-of-year field from 1 to 12.

This method returns the month as an `int` from 1 to 12. Application code is frequently clearer if the enum `https://developer.android.com/reference/kotlin/java/time/Month` is used by calling `https://developer.android.com/reference/kotlin/java/time/MonthDay#getMonth()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the month-of-year, from 1 to 12 |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/MonthDay#getMonth()`

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

A hash code for this month-day.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAfter(other: MonthDay!): Boolean
```

Checks if this month-day is after the specified month-day.

| Parameters ||
|---|---|
| `other` | [MonthDay](../java/time/MonthDay.md)!: the other month-day to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is after the specified month-day |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBefore(other: MonthDay!): Boolean
```

Checks if this month-day is before the specified month-day.

| Parameters ||
|---|---|
| `other` | [MonthDay](../java/time/MonthDay.md)!: the other month-day to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this point is before the specified month-day |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this month-day can be queried for the specified field. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/MonthDay#range(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/MonthDay#get(java.time.temporal.TemporalField)` methods will throw an exception.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The supported fields are:

- `MONTH_OF_YEAR`
- `YEAR`

All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field is supported on this month-day, false if not |

### isValidYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isValidYear(year: Int): Boolean
```

Checks if the year is valid for this month-day.

This method checks whether this month and day and the input year form a valid date. This can only return false for February 29th.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year to validate |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the year is valid for this month-day |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/Year#isValidMonthDay(java.time.MonthDay)`

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(): MonthDay!
```

Obtains the current month-day from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#systemDefaultZone()` in the default time-zone to obtain the current month-day.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | the current month-day using the system clock and default time-zone, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(clock: Clock!): MonthDay!
```

Obtains the current month-day from the specified clock.

This will query the specified clock to obtain the current month-day. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock`.

| Parameters ||
|---|---|
| `clock` | [Clock](../java/time/Clock.md)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | the current month-day, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(zone: ZoneId!): MonthDay!
```

Obtains the current month-day from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#system(java.time.ZoneId)` to obtain the current month-day. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](../java/time/ZoneId.md)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | the current month-day using the system clock, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    month: Int, 
    dayOfMonth: Int
): MonthDay!
```

Obtains an instance of `MonthDay`.

The day-of-month must be valid for the month within a leap year. Hence, for month 2 (February), day 29 is valid.

For example, passing in month 4 (April) and day 31 will throw an exception, as there can never be April 31st in any year. By contrast, passing in February 29th is permitted, as that month-day can sometimes be valid.

| Parameters ||
|---|---|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to represent, from 1 (January) to 12 (December) |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to represent, from 1 to 31 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | the month-day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    month: Month!, 
    dayOfMonth: Int
): MonthDay!
```

Obtains an instance of `MonthDay`.

The day-of-month must be valid for the month within a leap year. Hence, for February, day 29 is valid.

For example, passing in April and day 31 will throw an exception, as there can never be April 31st in any year. By contrast, passing in February 29th is permitted, as that month-day can sometimes be valid.

| Parameters ||
|---|---|
| `month` | [Month](../java/time/Month.md)!: the month-of-year to represent, not null |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to represent, from 1 to 31 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | the month-day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the value of any field is out of range, or if the day-of-month is invalid for the month |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(text: CharSequence!): MonthDay!
```

Obtains an instance of `MonthDay` from a text string such as `--12-03`.

The string must represent a valid month-day. The format is `--MM-dd`.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse such as "--12-03", not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | the parsed month-day, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(
    text: CharSequence!, 
    formatter: DateTimeFormatter!
): MonthDay!
```

Obtains an instance of `MonthDay` from a text string using a specific formatter.

The text is parsed using the formatter, returning a month-day.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |
| `formatter` | [DateTimeFormatter](../java/time/format/DateTimeFormatter.md)!: the formatter to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | the parsed month-day, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this month-day using the specified query.

This queries this month-day using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery#queryFrom(java.time.temporal.TemporalAccessor)` method on the specified query passing `this` as the argument.

| Parameters ||
|---|---|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](../java/time/temporal/TemporalQuery.md)\<R\>!: the query to invoke, not null |

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

The range object expresses the minimum and maximum valid values for a field. This month-day is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/MonthDay#isSupported(java.time.temporal.TemporalField)` will return appropriate range instances. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.rangeRefinedBy(TemporalAccessor)` passing `this` as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!: the field to query the range for, not null |

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

Outputs this month-day as a `String`, such as `--12-03`.

The output will be in the format `--MM-dd`:

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this month-day, not null |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(month: Month!): MonthDay!
```

Returns a copy of this `MonthDay` with the month-of-year altered.

This returns a month-day with the specified month. If the day-of-month is invalid for the specified month, the day will be adjusted to the last valid day-of-month.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `month` | [Month](../java/time/Month.md)!: the month-of-year to set in the returned month-day, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | a `MonthDay` based on this month-day with the requested month, not null |

### withDayOfMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withDayOfMonth(dayOfMonth: Int): MonthDay!
```

Returns a copy of this `MonthDay` with the day-of-month altered.

This returns a month-day with the specified day-of-month. If the day-of-month is invalid for the month, an exception is thrown.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-month to set in the return month-day, from 1 to 31 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | a `MonthDay` based on this month-day with the requested day, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the day-of-month value is invalid, or if the day-of-month is invalid for the month |

### withMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun withMonth(month: Int): MonthDay!
```

Returns a copy of this `MonthDay` with the month-of-year altered.

This returns a month-day with the specified month. If the day-of-month is invalid for the specified month, the day will be adjusted to the last valid day-of-month.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the month-of-year to set in the returned month-day, from 1 (January) to 12 (December) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/MonthDay#!` | a `MonthDay` based on this month-day with the requested month, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the month-of-year value is invalid |
