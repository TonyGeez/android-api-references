# Era

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Era

```
interface Era : TemporalAccessor, TemporalAdjuster
```

| [java.time.chrono.Era](../java/time/chrono/Era.md) |

| Known Direct Subclasses [HijrahEra](../java/time/chrono/HijrahEra.md), [IsoEra](../java/time/chrono/IsoEra.md), [JapaneseEra](../java/time/chrono/JapaneseEra.md), [MinguoEra](../java/time/chrono/MinguoEra.md), [ThaiBuddhistEra](../java/time/chrono/ThaiBuddhistEra.md) |----------------------------------------------------------------------------------------------------|--------------------------------------------------| | [HijrahEra](../java/time/chrono/HijrahEra.md) | An era in the Hijrah calendar system. | | [IsoEra](../java/time/chrono/IsoEra.md) | An era in the ISO calendar system. | | [JapaneseEra](../java/time/chrono/JapaneseEra.md) | An era in the Japanese Imperial calendar system. | | [MinguoEra](../java/time/chrono/MinguoEra.md) | An era in the Minguo calendar system. | | [ThaiBuddhistEra](../java/time/chrono/ThaiBuddhistEra.md) | An era in the Thai Buddhist calendar system. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [HijrahEra.AH](../java/time/chrono/HijrahEra.md), [IsoEra.BCE](../java/time/chrono/IsoEra.md), [IsoEra.CE](../java/time/chrono/IsoEra.md), [MinguoEra.BEFORE_ROC](../java/time/chrono/MinguoEra.md), [MinguoEra.ROC](../java/time/chrono/MinguoEra.md), [ThaiBuddhistEra.BE](../java/time/chrono/ThaiBuddhistEra.md), [ThaiBuddhistEra.BEFORE_BE](../java/time/chrono/ThaiBuddhistEra.md) |-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [HijrahEra.AH](../java/time/chrono/HijrahEra.md) | The singleton instance for the current era, 'Anno Hegirae', which has the numeric value 1. | | [IsoEra.BCE](../java/time/chrono/IsoEra.md) | The singleton instance for the era before the current one, 'Before Current Era', which has the numeric value 0. | | [IsoEra.CE](../java/time/chrono/IsoEra.md) | The singleton instance for the current era, 'Current Era', which has the numeric value 1. | | [MinguoEra.BEFORE_ROC](../java/time/chrono/MinguoEra.md) | The singleton instance for the era before the current one, 'Before Republic of China Era', which has the numeric value 0. | | [MinguoEra.ROC](../java/time/chrono/MinguoEra.md) | The singleton instance for the current era, 'Republic of China Era', which has the numeric value 1. | | [ThaiBuddhistEra.BE](../java/time/chrono/ThaiBuddhistEra.md) | The singleton instance for the current era, 'Buddhist Era', which has the numeric value 1. | | [ThaiBuddhistEra.BEFORE_BE](../java/time/chrono/ThaiBuddhistEra.md) | The singleton instance for the era before the current one, 'Before Buddhist Era', which has the numeric value 0. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An era of the time-line.

Most calendar systems have a single epoch dividing the time-line into two eras. However, some calendar systems, have multiple eras, such as one for the reign of each leader. In all cases, the era is conceptually the largest division of the time-line. Each chronology defines the Era's that are known Eras and a [Chronology.eras](../java/time/chrono/Chronology.md))to get the valid eras.

For example, the Thai Buddhist calendar system divides time into two eras, before and after a single date. By contrast, the Japanese calendar system has one era for the reign of each Emperor.

Instances of`Era`may be compared using the`==`operator.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Temporal](../java/time/temporal/Temporal.md)! | [adjustInto](../java/time/chrono/Era.md))`(`temporal:` ` [Temporal](../java/time/temporal/Temporal.md)!`)` Adjusts the specified temporal object to have the same era as this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](../java/time/chrono/Era.md))`(`field:` ` [TemporalField](../java/time/temporal/TemporalField.md)!`)` Gets the value of the specified field from this era as an`int`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../java/time/chrono/Era.md))`(`style:` ` [TextStyle](../java/time/format/TextStyle.md)!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` Gets the textual representation of this era. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java/time/chrono/Era.md))`(`field:` ` [TemporalField](../java/time/temporal/TemporalField.md)!`)` Gets the value of the specified field from this era as a`long`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getValue](../java/time/chrono/Era.md))`()` Gets the numeric value associated with the era as defined by the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](../java/time/chrono/Era.md))`(`field:` ` [TemporalField](../java/time/temporal/TemporalField.md)!`)` Checks if the specified field is supported. |
| --- | --- |
| openR | [query](../java/time/chrono/Era.md))`(`query:` ` [TemporalQuery](../java/time/temporal/TemporalQuery.md)<R>!`)` Queries this era using the specified query. |
| open [ValueRange](../java/time/temporal/ValueRange.md)! | [range](../java/time/chrono/Era.md))`(`field:` ` [TemporalField](../java/time/temporal/TemporalField.md)!`)` Gets the range of valid values for the specified field. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same era as this object.

This returns a temporal object of the same observable type as the input with the era changed to be the same as this.

The adjustment is equivalent to using [Temporal.with(TemporalField, long)](../java/time/temporal/Temporal.md))passing [ChronoField.ERA](../java/time/temporal/ChronoField.md) as the field.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](../java/time/temporal/Temporal.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisEra.adjustInto(temporal);
    temporal = temporal.with(thisEra);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [Temporal](../java/time/temporal/Temporal.md)!:the target object to be adjusted, not null |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------|
| [Temporal](../java/time/temporal/Temporal.md)! | the adjusted object, not null |

| Exceptions ||
|---------------------------------|----------------------------------|
| `java.time.DateTimeException` | if unable to make the adjustment |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this era as an`int`.

This queries this era for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](../java/time/temporal/ChronoField.md) then the query is implemented here. The`ERA`field returns the value of the era. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!:the field to get, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an`int` |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| --- | --- |

### getDisplayName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayName(
    style: TextStyle!, 
    locale: Locale!
): String!
```

Gets the textual representation of this era.

This returns the textual name used to identify the era, suitable for presentation to the user. The parameters control the style of the returned text and the locale.

If no textual mapping is found then the [numeric value](../java/time/chrono/Era.md))is returned.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [TextStyle](../java/time/format/TextStyle.md)!:the style of the text required, not null |
| `locale` | [Locale](../java/util/Locale.md)!:the locale to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the text value of the era, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this era as a`long`.

This queries this era for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](../java/time/temporal/ChronoField.md) then the query is implemented here. The`ERA`field returns the value of the era. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
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
abstract fun getValue(): Int
```

Gets the numeric value associated with the era as defined by the chronology. Each chronology defines the predefined Eras and methods to list the Eras of the chronology.

All fields, including eras, have an associated numeric value. The meaning of the numeric value for era is determined by the chronology according to these principles:

- The era in use at the epoch 1970-01-01 (ISO) has the value 1.
- Later eras have sequentially higher values.
- Earlier eras have sequentially lower values, which may be negative.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric era value |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this era can be queried for the specified field. If false, then calling the [range](../java/time/chrono/Era.md))and [get](../java/time/chrono/Era.md))methods will throw an exception.

If the field is a [ChronoField](../java/time/temporal/ChronoField.md) then the query is implemented here. The`ERA`field returns true. All other`ChronoField`instances will return false.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!:the field to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field is supported on this era, false if not |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this era using the specified query.

This queries this era using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](../java/time/temporal/TemporalQuery.md))method on the specified query passing`this`as the argument.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------|
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
open fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

The range object expresses the minimum and maximum valid values for a field. This era is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](../java/time/temporal/ChronoField.md) then the query is implemented here. The`ERA`field returns the range. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.rangeRefinedBy(TemporalAccessor)`passing`this`as the argument. Whether the range can be obtained is determined by the field.

The default implementation must return a range for`ERA`from zero to one, suitable for two era calendar systems such as ISO.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java/time/temporal/TemporalField.md)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](../java/time/temporal/ValueRange.md)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
