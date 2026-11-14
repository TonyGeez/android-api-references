# TemporalField

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalField

```
interface TemporalField
```

| [java.time.temporal.TemporalField](TemporalField.md) |

| Known Direct Subclasses [ChronoField](ChronoField.md) |----------------------------------------------------------------------------------------------|---------------------------| | [ChronoField](ChronoField.md) | A standard set of fields. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ChronoField.ALIGNED_DAY_OF_WEEK_IN_MONTH](ChronoField.md), [ChronoField.ALIGNED_DAY_OF_WEEK_IN_YEAR](ChronoField.md), [ChronoField.ALIGNED_WEEK_OF_MONTH](ChronoField.md), [ChronoField.ALIGNED_WEEK_OF_YEAR](ChronoField.md), [ChronoField.AMPM_OF_DAY](ChronoField.md), [ChronoField.CLOCK_HOUR_OF_AMPM](ChronoField.md), [ChronoField.CLOCK_HOUR_OF_DAY](ChronoField.md), [ChronoField.DAY_OF_MONTH](ChronoField.md), [ChronoField.DAY_OF_WEEK](ChronoField.md), [ChronoField.DAY_OF_YEAR](ChronoField.md), [ChronoField.EPOCH_DAY](ChronoField.md), [ChronoField.ERA](ChronoField.md), and 18 others. |-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [ChronoField.ALIGNED_DAY_OF_WEEK_IN_MONTH](ChronoField.md) | The aligned day-of-week within a month. | | [ChronoField.ALIGNED_DAY_OF_WEEK_IN_YEAR](ChronoField.md) | The aligned day-of-week within a year. | | [ChronoField.ALIGNED_WEEK_OF_MONTH](ChronoField.md) | The aligned week within a month. | | [ChronoField.ALIGNED_WEEK_OF_YEAR](ChronoField.md) | The aligned week within a year. | | [ChronoField.AMPM_OF_DAY](ChronoField.md) | The am-pm-of-day. | | [ChronoField.CLOCK_HOUR_OF_AMPM](ChronoField.md) | The clock-hour-of-am-pm. | | [ChronoField.CLOCK_HOUR_OF_DAY](ChronoField.md) | The clock-hour-of-day. | | [ChronoField.DAY_OF_MONTH](ChronoField.md) | The day-of-month. | | [ChronoField.DAY_OF_WEEK](ChronoField.md) | The day-of-week, such as Tuesday. | | [ChronoField.DAY_OF_YEAR](ChronoField.md) | The day-of-year. | | [ChronoField.EPOCH_DAY](ChronoField.md) | The epoch-day, based on the Java epoch of 1970-01-01 (ISO). | | [ChronoField.ERA](ChronoField.md) | The era. | | [ChronoField.HOUR_OF_AMPM](ChronoField.md) | The hour-of-am-pm. | | [ChronoField.HOUR_OF_DAY](ChronoField.md) | The hour-of-day. | | [ChronoField.INSTANT_SECONDS](ChronoField.md) | The instant epoch-seconds. | | [ChronoField.MICRO_OF_DAY](ChronoField.md) | The micro-of-day. | | [ChronoField.MICRO_OF_SECOND](ChronoField.md) | The micro-of-second. | | [ChronoField.MILLI_OF_DAY](ChronoField.md) | The milli-of-day. | | [ChronoField.MILLI_OF_SECOND](ChronoField.md) | The milli-of-second. | | [ChronoField.MINUTE_OF_DAY](ChronoField.md) | The minute-of-day. | | [ChronoField.MINUTE_OF_HOUR](ChronoField.md) | The minute-of-hour. | | [ChronoField.MONTH_OF_YEAR](ChronoField.md) | The month-of-year, such as March. | | [ChronoField.NANO_OF_DAY](ChronoField.md) | The nano-of-day. | | [ChronoField.NANO_OF_SECOND](ChronoField.md) | The nano-of-second. | | [ChronoField.OFFSET_SECONDS](ChronoField.md) | The offset from UTC/Greenwich. | | [ChronoField.PROLEPTIC_MONTH](ChronoField.md) | The proleptic-month based, counting months sequentially from year 0. | | [ChronoField.SECOND_OF_DAY](ChronoField.md) | The second-of-day. | | [ChronoField.SECOND_OF_MINUTE](ChronoField.md) | The second-of-minute. | | [ChronoField.YEAR](ChronoField.md) | The proleptic year, such as 2012. | | [ChronoField.YEAR_OF_ERA](ChronoField.md) | The year within the era. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A field of date-time, such as month-of-year or minute-of-hour.

Date and time is expressed using fields which partition the time-line into something meaningful for humans. Implementations of this interface represent those fields.

The most commonly used units are defined in [ChronoField](ChronoField.md). Further fields are supplied in [IsoFields](IsoFields.md), [WeekFields](WeekFields.md) and [JulianFields](JulianFields.md). Fields can also be written by application code by implementing this interface.

The field works using double dispatch. Client code calls methods on a date-time like`LocalDateTime`which check if the field is a`ChronoField`. If it is, then the date-time must handle it. Otherwise, the method call is re-dispatched to the matching method in this interface.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [adjustInto](TemporalField.md))`(`temporal:` `R`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a copy of the specified temporal object with the value of this field set. |
| abstract [TemporalUnit](TemporalUnit.md)! | [getBaseUnit](TemporalField.md))`()` Gets the unit that the field is measured in. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](TemporalField.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`)` Gets the display name for the field in the requested locale. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFrom](TemporalField.md))`(`temporal:` ` [TemporalAccessor](TemporalAccessor.md)!`)` Gets the value of this field from the specified temporal object. |
| abstract [TemporalUnit](TemporalUnit.md)! | [getRangeUnit](TemporalField.md))`()` Gets the range that the field is bound by. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDateBased](TemporalField.md))`()` Checks if this field represents a component of a date. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupportedBy](TemporalField.md))`(`temporal:` ` [TemporalAccessor](TemporalAccessor.md)!`)` Checks if this field is supported by the temporal object. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTimeBased](TemporalField.md))`()` Checks if this field represents a component of a time. |
| abstract [ValueRange](ValueRange.md)! | [range](TemporalField.md))`()` Gets the range of valid values for the field. |
| --- | --- |
| abstract [ValueRange](ValueRange.md)! | [rangeRefinedBy](TemporalField.md))`(`temporal:` ` [TemporalAccessor](TemporalAccessor.md)!`)` Get the range of valid values for this field using the temporal object to refine the result. |
| open [TemporalAccessor](TemporalAccessor.md)! | [resolve](TemporalField.md))`(`fieldValues:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [TemporalField](TemporalField.md)!,` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!>!`, `partialTemporal:` ` [TemporalAccessor](TemporalAccessor.md)!`, `resolverStyle:` ` [ResolverStyle](../java.time.format/ResolverStyle.md)!`)` Resolves this field to provide a simpler alternative or a date. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Temporal!> adjustInto(
    temporal: R, 
    newValue: Long
): R
```

Returns a copy of the specified temporal object with the value of this field set.

This returns a new temporal object based on the specified one with the value for this field changed. For example, on a`LocalDate`, this could be used to set the year, month or day-of-month. The returned object has the same observable type as the specified object.

In some cases, changing a field is not fully defined. For example, if the target object is a date representing the 31st January, then changing the month to February would be unclear. In cases like this, the implementation is responsible for resolving the result. Typically it will choose the previous valid date, which would be the last valid day of February in this example.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [Temporal.with(TemporalField, long)](Temporal.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisField.adjustInto(temporal);
    temporal = temporal.with(thisField);
  
```
It is recommended to use the second approach,`with(TemporalField)`, as it is a lot clearer to read in code.

Implementations should perform any queries or calculations using the fields available in [ChronoField](ChronoField.md). If the field is not supported an`UnsupportedTemporalTypeException`must be thrown.

Implementations must not alter the specified temporal object. Instead, an adjusted copy of the original must be returned. This provides equivalent, safe behavior for immutable and mutable implementations.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the Temporal object |
| `temporal` | R:the temporal object to adjust, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the field |
| --- | --- |

| Return ||
|---|----------------------------------------|
| R | the adjusted temporal object, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported by the temporal |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getBaseUnit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBaseUnit(): TemporalUnit!
```

Gets the unit that the field is measured in.

The unit of the field is the period that varies within the range. For example, in the field 'MonthOfYear', the unit is 'Months'. See also [getRangeUnit()](TemporalField.md)).

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [TemporalUnit](TemporalUnit.md)! | the unit defining the base unit of the field, not null |

### getDisplayName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayName(locale: Locale!): String!
```

Gets the display name for the field in the requested locale.

If there is no display name for the locale then a suitable default must be returned.

The default implementation must check the locale is not null and return`toString()`.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the locale to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name for the locale or a suitable default, not null |

### getFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFrom(temporal: TemporalAccessor!): Long
```

Gets the value of this field from the specified temporal object.

This queries the temporal object for the value of this field.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [TemporalAccessor.getLong(TemporalField)](TemporalAccessor.md))(or [TemporalAccessor.get(TemporalField)](TemporalAccessor.md))): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisField.getFrom(temporal);
    temporal = temporal.getLong(thisField);
  
```
It is recommended to use the second approach,`getLong(TemporalField)`, as it is a lot clearer to read in code.

Implementations should perform any queries or calculations using the fields available in [ChronoField](ChronoField.md). If the field is not supported an`UnsupportedTemporalTypeException`must be thrown.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](TemporalAccessor.md)!:the temporal object to query, not null |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of this field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported by the temporal |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getRangeUnit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRangeUnit(): TemporalUnit!
```

Gets the range that the field is bound by.

The range of the field is the period that the field varies within. For example, in the field 'MonthOfYear', the range is 'Years'. See also [getBaseUnit()](TemporalField.md)).

The range is never null. For example, the 'Year' field is shorthand for 'YearOfForever'. It therefore has a unit of 'Years' and a range of 'Forever'.

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [TemporalUnit](TemporalUnit.md)! | the unit defining the range of the field, not null |

### isDateBased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDateBased(): Boolean
```

Checks if this field represents a component of a date.

A field is date-based if it can be derived from [EPOCH_DAY](ChronoField.md). Note that it is valid for both`isDateBased()`and`isTimeBased()`to return false, such as when representing a field like minute-of-week.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this field is a component of a date |

### isSupportedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSupportedBy(temporal: TemporalAccessor!): Boolean
```

Checks if this field is supported by the temporal object.

This determines whether the temporal accessor supports this field. If this returns false, then the temporal cannot be queried for this field.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [TemporalAccessor.isSupported(TemporalField)](TemporalAccessor.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisField.isSupportedBy(temporal);
    temporal = temporal.isSupported(thisField);
  
```
It is recommended to use the second approach,`isSupported(TemporalField)`, as it is a lot clearer to read in code.

Implementations should determine whether they are supported using the fields available in [ChronoField](ChronoField.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](TemporalAccessor.md)!:the temporal object to query, not null |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the date-time can be queried for this field, false if not |

### isTimeBased

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isTimeBased(): Boolean
```

Checks if this field represents a component of a time.

A field is time-based if it can be derived from [NANO_OF_DAY](ChronoField.md). Note that it is valid for both`isDateBased()`and`isTimeBased()`to return false, such as when representing a field like minute-of-week.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this field is a component of a time |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun range(): ValueRange!
```

Gets the range of valid values for the field.

All fields can be expressed as a`long`integer. This method returns an object that describes the valid range for that value. This method is generally only applicable to the ISO-8601 calendar system.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](ValueRange.md)! | the range of valid values for the field, not null |

### rangeRefinedBy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun rangeRefinedBy(temporal: TemporalAccessor!): ValueRange!
```

Get the range of valid values for this field using the temporal object to refine the result.

This uses the temporal object to find the range of valid values for the field. This is similar to [range()](TemporalField.md)), however this method refines the result using the temporal. For example, if the field is`DAY_OF_MONTH`the`range`method is not accurate as there are four possible month lengths, 28, 29, 30 and 31 days. Using this method with a date allows the range to be accurate, returning just one of those four options.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [TemporalAccessor.range(TemporalField)](TemporalAccessor.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisField.rangeRefinedBy(temporal);
    temporal = temporal.range(thisField);
  
```
It is recommended to use the second approach,`range(TemporalField)`, as it is a lot clearer to read in code.

Implementations should perform any queries or calculations using the fields available in [ChronoField](ChronoField.md). If the field is not supported an`UnsupportedTemporalTypeException`must be thrown.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](TemporalAccessor.md)!:the temporal object used to refine the result, not null |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------|
| [ValueRange](ValueRange.md)! | the range of valid values for this field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported by the temporal |

### resolve

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolve(
    fieldValues: MutableMap<TemporalField!, Long!>!, 
    partialTemporal: TemporalAccessor!, 
    resolverStyle: ResolverStyle!
): TemporalAccessor!
```

Resolves this field to provide a simpler alternative or a date.

This method is invoked during the resolve phase of parsing. It is designed to allow application defined fields to be simplified into more standard fields, such as those on`ChronoField`, or into a date.

Applications should not normally invoke this method directly.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fieldValues` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [TemporalField](TemporalField.md)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>!:the map of fields to values, which can be updated, not null |
| `partialTemporal` | [TemporalAccessor](TemporalAccessor.md)!:the partially complete temporal to query for zone and chronology; querying for other things is undefined and not recommended, not null |
| `resolverStyle` | [ResolverStyle](../java.time.format/ResolverStyle.md)!:the requested type of resolve, not null |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [TemporalAccessor](TemporalAccessor.md)! | the resolved temporal object; null if resolving only changed the map, or no resolve occurred |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if resolving results in an error. This must not be thrown by querying a field on the temporal without first checking if it is supported |
