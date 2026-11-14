Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DayOfWeek

```
class DayOfWeek : TemporalAccessor, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#)\> ||
| | ↳ | [java.time.DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#) |

| Known Direct Subclasses [DayOfWeek.FRIDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:FRIDAY), [DayOfWeek.MONDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:MONDAY), [DayOfWeek.SATURDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:SATURDAY), [DayOfWeek.SUNDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:SUNDAY), [DayOfWeek.THURSDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:THURSDAY), [DayOfWeek.TUESDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:TUESDAY), [DayOfWeek.WEDNESDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:WEDNESDAY) |---|---| | [DayOfWeek.FRIDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:FRIDAY) | The singleton instance for the day-of-week of Friday. | | [DayOfWeek.MONDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:MONDAY) | The singleton instance for the day-of-week of Monday. | | [DayOfWeek.SATURDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:SATURDAY) | The singleton instance for the day-of-week of Saturday. | | [DayOfWeek.SUNDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:SUNDAY) | The singleton instance for the day-of-week of Sunday. | | [DayOfWeek.THURSDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:THURSDAY) | The singleton instance for the day-of-week of Thursday. | | [DayOfWeek.TUESDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:TUESDAY) | The singleton instance for the day-of-week of Tuesday. | | [DayOfWeek.WEDNESDAY](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:WEDNESDAY) | The singleton instance for the day-of-week of Wednesday. | |

A day-of-week, such as 'Tuesday'.

`DayOfWeek` is an enum representing the 7 days of the week - Monday, Tuesday, Wednesday, Thursday, Friday, Saturday and Sunday.

In addition to the textual enum name, each day-of-week has an `int` value. The `int` value follows the ISO-8601 standard, from 1 (Monday) to 7 (Sunday). It is recommended that applications use the enum rather than the `int` value to ensure code clarity.

This enum provides access to the localized textual form of the day-of-week. Some locales also assign different numeric values to the days, declaring Sunday to have the value 1, however this class provides no support for this. See `https://developer.android.com/reference/kotlin/java/time/temporal/WeekFields` for localized week-numbering.

**Do not use `ordinal()` to obtain the numeric representation of `DayOfWeek`. Use `getValue()` instead.**

This enum represents a common concept that is found in many calendar systems. As such, this enum may be used by any calendar system that has the day-of-week concept defined exactly equivalent to the ISO calendar system.

## Summary

| Enum values ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:FRIDAY` The singleton instance for the day-of-week of Friday. |
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:MONDAY` The singleton instance for the day-of-week of Monday. |
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:SATURDAY` The singleton instance for the day-of-week of Saturday. |
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:SUNDAY` The singleton instance for the day-of-week of Sunday. |
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:THURSDAY` The singleton instance for the day-of-week of Thursday. |
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:TUESDAY` The singleton instance for the day-of-week of Tuesday. |
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#ENUM_VALUE:WEDNESDAY` The singleton instance for the day-of-week of Wednesday. |

| Public methods ||
|---|---|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)! | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#adjustInto(java.time.temporal.Temporal)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!)` Adjusts the specified temporal object to have this day-of-week. |
| static [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#)! | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Obtains an instance of `DayOfWeek` from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#get(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this day-of-week as an `int`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#getDisplayName(java.time.format.TextStyle,%20java.util.Locale)(style: https://developer.android.com/reference/kotlin/java/time/format/TextStyle!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Gets the textual representation, such as 'Mon' or 'Friday'. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this day-of-week as a `long`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#getValue()()` Gets the day-of-week `int` value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Checks if the specified field is supported. |
| [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#)! | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#minus(kotlin.Long)(days: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the day-of-week that is the specified number of days before this one. |
| static [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#)! | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#of(kotlin.Int)(dayOfWeek: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains an instance of `DayOfWeek` from an `int` value. |
| [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek#)! | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#plus(kotlin.Long)(days: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the day-of-week that is the specified number of days after this one. |
| R | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<R>!)` Queries this day-of-week using the specified query. |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the range of valid values for the specified field. |

## Enum values

### FRIDAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val FRIDAY : DayOfWeek
```

The singleton instance for the day-of-week of Friday. This has the numeric value of `5`.

### MONDAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val MONDAY : DayOfWeek
```

The singleton instance for the day-of-week of Monday. This has the numeric value of `1`.

### SATURDAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val SATURDAY : DayOfWeek
```

The singleton instance for the day-of-week of Saturday. This has the numeric value of `6`.

### SUNDAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val SUNDAY : DayOfWeek
```

The singleton instance for the day-of-week of Sunday. This has the numeric value of `7`.

### THURSDAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val THURSDAY : DayOfWeek
```

The singleton instance for the day-of-week of Thursday. This has the numeric value of `4`.

### TUESDAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val TUESDAY : DayOfWeek
```

The singleton instance for the day-of-week of Tuesday. This has the numeric value of `2`.

### WEDNESDAY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val WEDNESDAY : DayOfWeek
```

The singleton instance for the day-of-week of Wednesday. This has the numeric value of `3`.

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have this day-of-week.

This returns a temporal object of the same observable type as the input with the day-of-week changed to be the same as this.

The adjustment is equivalent to using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long)` passing `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` as the field. Note that this adjusts forwards or backwards within a Monday to Sunday week. See `https://developer.android.com/reference/kotlin/java/time/temporal/WeekFields#dayOfWeek()` for localized week start days. See `TemporalAdjuster` for other adjusters with more control, such as `next(MONDAY)`.

In most cases, it is clearer to reverse the calling pattern by using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisDayOfWeek.adjustInto(temporal);
    temporal = temporal.with(thisDayOfWeek);
  
```

For example, given a date that is a Wednesday, the following are output:

```kotlin
dateOnWed.with(MONDAY);     // two days earlier
    dateOnWed.with(TUESDAY);    // one day earlier
    dateOnWed.with(WEDNESDAY);  // same date
    dateOnWed.with(THURSDAY);   // one day later
    dateOnWed.with(FRIDAY);     // two days later
    dateOnWed.with(SATURDAY);   // three days later
    dateOnWed.with(SUNDAY);     // four days later
  
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

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): DayOfWeek!
```

Obtains an instance of `DayOfWeek` from a temporal object.

This obtains a day-of-week based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `DayOfWeek`.

The conversion extracts the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` field.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery` allowing it to be used as a query via method reference, `DayOfWeek::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#!` | the day-of-week, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to a `DayOfWeek` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this day-of-week as an `int`.

This queries this day-of-week for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the value of the day-of-week, from 1 to 7, will be returned. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the field, within the valid range of values |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an `int` |

### getDisplayName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(
    style: TextStyle!, 
    locale: Locale!
): String!
```

Gets the textual representation, such as 'Mon' or 'Friday'.

This returns the textual name used to identify the day-of-week, suitable for presentation to the user. The parameters control the style of the returned text and the locale.

If no textual mapping is found then the `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#getValue()` is returned.

| Parameters ||
|---|---|
| `style` | [TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle)!: the length of the text required, not null |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the locale to use, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the text value of the day-of-week, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this day-of-week as a `long`.

This queries this day-of-week for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the value of the day-of-week, from 1 to 7, will be returned. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

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

### getValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getValue(): Int
```

Gets the day-of-week `int` value.

The values are numbered following the ISO-8601 standard, from 1 (Monday) to 7 (Sunday). See `https://developer.android.com/reference/kotlin/java/time/temporal/WeekFields#dayOfWeek()` for localized week-numbering.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the day-of-week, from 1 (Monday) to 7 (Sunday) |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this day-of-week can be queried for the specified field. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#range(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#get(java.time.temporal.TemporalField)` methods will throw an exception.

If the field is `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then this method returns true. All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field is supported on this day-of-week, false if not |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(days: Long): DayOfWeek!
```

Returns the day-of-week that is the specified number of days before this one.

The calculation rolls around the start of the year from Monday to Sunday. The specified period may be negative.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `days` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the days to subtract, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#!` | the resulting day-of-week, not null |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(dayOfWeek: Int): DayOfWeek!
```

Obtains an instance of `DayOfWeek` from an `int` value.

`DayOfWeek` is an enum representing the 7 days of the week. This factory allows the enum to be obtained from the `int` value. The `int` value follows the ISO-8601 standard, from 1 (Monday) to 7 (Sunday).

| Parameters ||
|---|---|
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day-of-week to represent, from 1 (Monday) to 7 (Sunday) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#!` | the day-of-week singleton, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the day-of-week is invalid |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(days: Long): DayOfWeek!
```

Returns the day-of-week that is the specified number of days after this one.

The calculation rolls around the end of the week from Sunday to Monday. The specified period may be negative.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `days` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the days to add, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/DayOfWeek#!` | the resulting day-of-week, not null |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this day-of-week using the specified query.

This queries this day-of-week using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

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

The range object expresses the minimum and maximum valid values for a field. This day-of-week is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the range of the day-of-week, from 1 to 7, will be returned. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

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
