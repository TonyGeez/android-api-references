# IsoEra

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IsoEra

```
class IsoEra : Era
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.chrono.IsoEra](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#)\> ||
| | ↳ | [java.time.chrono.IsoEra](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#) |

| Known Direct Subclasses [IsoEra.BCE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:BCE), [IsoEra.CE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:CE) |-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [IsoEra.BCE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:BCE) | The singleton instance for the era before the current one, 'Before Current Era', which has the numeric value 0. | | [IsoEra.CE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:CE) | The singleton instance for the current era, 'Current Era', which has the numeric value 1. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An era in the ISO calendar system.

The ISO-8601 standard does not define eras. A definition has therefore been created with two eras - 'Current era' (CE) for years on or after 0001-01-01 (ISO), and 'Before current era' (BCE) for years before that.

| year-of-era | era | proleptic-year |
|-------------|-----|----------------|
| 2 | CE | 2 |
| 1 | CE | 1 |
| 1 | BCE | 0 |
| --- | --- | --- |
| 2 | BCE | -1 |

**Do not use `ordinal()` to obtain the numeric representation of `IsoEra`. Use `getValue()` instead.**

## Summary

| Enum values ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BCE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:BCE) The singleton instance for the era before the current one, 'Before Current Era', which has the numeric value 0. |
| [CE](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#ENUM_VALUE:CE) The singleton instance for the current era, 'Current Era', which has the numeric value 1. |

| Public methods ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getValue](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#getValue())`()` Gets the numeric era `int` value. |
| static [IsoEra](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#)! | [of](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#of(kotlin.Int))`(`isoEra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains an instance of `IsoEra` from an `int` value. |

| Inherited functions ||
|---|---|
| From class [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era) |---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | [adjustInto](https://developer.android.com/reference/kotlin/java/time/chrono/Era#adjustInto(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`)` Adjusts the specified temporal object to have the same era as this object. This returns a temporal object of the same observable type as the input with the era changed to be the same as this. The adjustment is equivalent to using [Temporal.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalField,%20kotlin.Long)) passing [ChronoField.ERA](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as the field. In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalAdjuster)): ```kotlin // these two lines are equivalent, but the second approach is recommended temporal = thisEra.adjustInto(temporal); temporal = temporal.with(thisEra); ``` This instance is immutable and unaffected by this method call. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/chrono/Era#get(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Gets the value of the specified field from this era as an `int`. This queries this era for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown. If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The `ERA` field returns the value of the era. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`. If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/time/chrono/Era#getDisplayName(java.time.format.TextStyle,%20java.util.Locale))`(`style:` ` [TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle.html#)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Gets the textual representation of this era. This returns the textual name used to identify the era, suitable for presentation to the user. The parameters control the style of the returned text and the locale. If no textual mapping is found then the [numeric value](https://developer.android.com/reference/kotlin/java/time/chrono/Era#getValue()) is returned. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/chrono/Era#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Gets the value of the specified field from this era as a `long`. This queries this era for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown. If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The `ERA` field returns the value of the era. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`. If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/Era#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Checks if the specified field is supported. This checks if this era can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/chrono/Era#range(java.time.temporal.TemporalField)) and [get](https://developer.android.com/reference/kotlin/java/time/chrono/Era#get(java.time.temporal.TemporalField)) methods will throw an exception. If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The `ERA` field returns true. All other `ChronoField` instances will return false. If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field. <br /> | | R | [query](https://developer.android.com/reference/kotlin/java/time/chrono/Era#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)<R>!`)` Queries this era using the specified query. This queries this era using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be. The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#queryFrom(java.time.temporal.TemporalAccessor)) method on the specified query passing `this` as the argument. <br /> | | [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | [range](https://developer.android.com/reference/kotlin/java/time/chrono/Era#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Gets the range of valid values for the specified field. The range object expresses the minimum and maximum valid values for a field. This era is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown. If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The `ERA` field returns the range. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`. If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.rangeRefinedBy(TemporalAccessor)` passing `this` as the argument. Whether the range can be obtained is determined by the field. The default implementation must return a range for `ERA` from zero to one, suitable for two era calendar systems such as ISO. <br /> | ||

## Enum values

### BCE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val BCE : IsoEra
```

The singleton instance for the era before the current one, 'Before Current Era', which has the numeric value 0. 

### CE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CE : IsoEra
```

The singleton instance for the current era, 'Current Era', which has the numeric value 1.

## Public methods

### getValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): Int
```

Gets the numeric era `int` value.

The era BCE has the value 0, while the era CE has the value 1.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the era value, from 0 (BCE) to 1 (CE) |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(isoEra: Int): IsoEra!
```

Obtains an instance of `IsoEra` from an `int` value.

`IsoEra` is an enum representing the ISO eras of BCE/CE. This factory allows the enum to be obtained from the `int` value.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `isoEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the BCE/CE value to represent, from 0 (BCE) to 1 (CE) |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [IsoEra](https://developer.android.com/reference/kotlin/java/time/chrono/IsoEra#)! | the era singleton, not null |

| Exceptions ||
|-------------------------------|-------------------------|
| `java.time.DateTimeException` | if the value is invalid |
