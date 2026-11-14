# Era

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Era

```
interface Era : TemporalAccessor, TemporalAdjuster
```

| [java.time.chrono.Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era#) |

| Known Direct Subclasses [HijrahEra](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra), [IsoEra](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra), [JapaneseEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra), [MinguoEra](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra), [ThaiBuddhistEra](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra) |----------------------------------------------------------------------------------------------------|--------------------------------------------------| | [HijrahEra](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra) | An era in the Hijrah calendar system. | | [IsoEra](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra) | An era in the ISO calendar system. | | [JapaneseEra](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseEra) | An era in the Japanese Imperial calendar system. | | [MinguoEra](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra) | An era in the Minguo calendar system. | | [ThaiBuddhistEra](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra) | An era in the Thai Buddhist calendar system. | |

| Known Indirect Subclasses [HijrahEra.AH](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#ENUM_VALUE:AH), [IsoEra.BCE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:BCE), [IsoEra.CE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:CE), [MinguoEra.BEFORE_ROC](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra#ENUM_VALUE:BEFORE_ROC), [MinguoEra.ROC](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra#ENUM_VALUE:ROC), [ThaiBuddhistEra.BE](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra#ENUM_VALUE:BE), [ThaiBuddhistEra.BEFORE_BE](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra#ENUM_VALUE:BEFORE_BE) |-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [HijrahEra.AH](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#ENUM_VALUE:AH) | The singleton instance for the current era, 'Anno Hegirae', which has the numeric value 1. | | [IsoEra.BCE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:BCE) | The singleton instance for the era before the current one, 'Before Current Era', which has the numeric value 0. | | [IsoEra.CE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:CE) | The singleton instance for the current era, 'Current Era', which has the numeric value 1. | | [MinguoEra.BEFORE_ROC](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra#ENUM_VALUE:BEFORE_ROC) | The singleton instance for the era before the current one, 'Before Republic of China Era', which has the numeric value 0. | | [MinguoEra.ROC](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoEra#ENUM_VALUE:ROC) | The singleton instance for the current era, 'Republic of China Era', which has the numeric value 1. | | [ThaiBuddhistEra.BE](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra#ENUM_VALUE:BE) | The singleton instance for the current era, 'Buddhist Era', which has the numeric value 1. | | [ThaiBuddhistEra.BEFORE_BE](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistEra#ENUM_VALUE:BEFORE_BE) | The singleton instance for the era before the current one, 'Before Buddhist Era', which has the numeric value 0. | |

An era of the time-line.

Most calendar systems have a single epoch dividing the time-line into two eras. However, some calendar systems, have multiple eras, such as one for the reign of each leader. In all cases, the era is conceptually the largest division of the time-line. Each chronology defines the Era's that are known Eras and a [Chronology.eras](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#eras())to get the valid eras.

For example, the Thai Buddhist calendar system divides time into two eras, before and after a single date. By contrast, the Japanese calendar system has one era for the reign of each Emperor.

Instances of`Era`may be compared using the`==`operator.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | [adjustInto](https://developer.android.com/reference/kotlin/java/time/chrono/Era#adjustInto(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`)` Adjusts the specified temporal object to have the same era as this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/chrono/Era#get(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Gets the value of the specified field from this era as an`int`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/time/chrono/Era#getDisplayName(java.time.format.TextStyle,%20java.util.Locale))`(`style:` ` [TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle.html#)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Gets the textual representation of this era. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/chrono/Era#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Gets the value of the specified field from this era as a`long`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getValue](https://developer.android.com/reference/kotlin/java/time/chrono/Era#getValue())`()` Gets the numeric value associated with the era as defined by the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/Era#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Checks if the specified field is supported. |
| openR | [query](https://developer.android.com/reference/kotlin/java/time/chrono/Era#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)<R>!`)` Queries this era using the specified query. |
| open [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | [range](https://developer.android.com/reference/kotlin/java/time/chrono/Era#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Gets the range of valid values for the specified field. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same era as this object.

This returns a temporal object of the same observable type as the input with the era changed to be the same as this.

The adjustment is equivalent to using [Temporal.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalField,%20kotlin.Long))passing [ChronoField.ERA](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as the field.

In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalAdjuster)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisEra.adjustInto(temporal);
    temporal = temporal.with(thisEra);
  
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

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this era as an`int`.

This queries this era for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The`ERA`field returns the value of the era. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to get, not null |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value for the field |

| Exceptions ||
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an`int` |
| `java.lang.ArithmeticException` | if numeric overflow occurs |

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

If no textual mapping is found then the [numeric value](https://developer.android.com/reference/kotlin/java/time/chrono/Era#getValue())is returned.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle.html#)!:the style of the text required, not null |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale to use, not null |

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

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The`ERA`field returns the value of the era. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

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

This checks if this era can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/chrono/Era#range(java.time.temporal.TemporalField))and [get](https://developer.android.com/reference/kotlin/java/time/chrono/Era#get(java.time.temporal.TemporalField))methods will throw an exception.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The`ERA`field returns true. All other`ChronoField`instances will return false.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to check, null returns false |

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

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

The range object expresses the minimum and maximum valid values for a field. This era is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The`ERA`field returns the range. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.rangeRefinedBy(TemporalAccessor)`passing`this`as the argument. Whether the range can be obtained is determined by the field.

The default implementation must return a range for`ERA`from zero to one, suitable for two era calendar systems such as ISO.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |
