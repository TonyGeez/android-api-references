# HijrahEra

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HijrahEra

```
class HijrahEra : Era
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.chrono.HijrahEra](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#)\> ||
| | ↳ | [java.time.chrono.HijrahEra](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#) |

| Known Direct Subclasses [HijrahEra.AH](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#ENUM_VALUE:AH) |---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------| | [HijrahEra.AH](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#ENUM_VALUE:AH) | The singleton instance for the current era, 'Anno Hegirae', which has the numeric value 1. | |
| --- | --- | --- | --- | --- | --- | --- |

An era in the Hijrah calendar system.

The Hijrah calendar system has only one era covering the proleptic years greater than zero.

**Do not use`ordinal()`to obtain the numeric representation of`HijrahEra`. Use`getValue()`instead.**

## Summary

| Enum values ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AH](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#ENUM_VALUE:AH) The singleton instance for the current era, 'Anno Hegirae', which has the numeric value 1. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#getDisplayName(java.time.format.TextStyle,%20java.util.Locale))`(`style:` ` [TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle.html#)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Gets the textual representation of this era. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getValue](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#getValue())`()` Gets the numeric era`int`value. |
| static [HijrahEra](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#)! | [of](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#of(kotlin.Int))`(`hijrahEra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains an instance of`HijrahEra`from an`int`value. |
| --- | --- |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | [range](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#range(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` Gets the range of valid values for the specified field. |

| Inherited functions ||
|---|---|
| From class [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)! | [adjustInto](https://developer.android.com/reference/kotlin/java/time/chrono/Era#adjustInto(java.time.temporal.Temporal))`(`temporal:` ` [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#)!`)` <br /> Adjusts the specified temporal object to have the same era as this object. This returns a temporal object of the same observable type as the input with the era changed to be the same as this. The adjustment is equivalent to using [Temporal.with(TemporalField, long)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalField,%20kotlin.Long))passing [ChronoField.ERA](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) as the field. In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal.html#with(java.time.temporal.TemporalAdjuster)): ```kotlin // these two lines are equivalent, but the second approach is recommended temporal = thisEra.adjustInto(temporal); temporal = temporal.with(thisEra); ``` This instance is immutable and unaffected by this method call. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/time/chrono/Era#get(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> Gets the value of the specified field from this era as an`int`. This queries this era for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown. If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The`ERA`field returns the value of the era. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`. If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/time/chrono/Era#getLong(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> Gets the value of the specified field from this era as a`long`. This queries this era for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown. If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The`ERA`field returns the value of the era. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`. If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/java/time/chrono/Era#isSupported(java.time.temporal.TemporalField))`(`field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!`)` <br /> Checks if the specified field is supported. This checks if this era can be queried for the specified field. If false, then calling the [range](https://developer.android.com/reference/kotlin/java/time/chrono/Era#range(java.time.temporal.TemporalField))and [get](https://developer.android.com/reference/kotlin/java/time/chrono/Era#get(java.time.temporal.TemporalField))methods will throw an exception. If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The`ERA`field returns true. All other`ChronoField`instances will return false. If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field. <br /> | | R | [query](https://developer.android.com/reference/kotlin/java/time/chrono/Era#query(java.time.temporal.TemporalQuery))`(`query:` ` [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#)<R>!`)` <br /> Queries this era using the specified query. This queries this era using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be. The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#queryFrom(java.time.temporal.TemporalAccessor))method on the specified query passing`this`as the argument. <br /> | ||

## Enum values

### AH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val AH : HijrahEra
```

The singleton instance for the current era, 'Anno Hegirae', which has the numeric value 1.

## Public methods

### getDisplayName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(
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

### getValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): Int
```

Gets the numeric era`int`value.

The era AH has the value 1.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the era value, 1 (AH) |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(hijrahEra: Int): HijrahEra!
```

Obtains an instance of`HijrahEra`from an`int`value.

The current era, which is the only accepted value, has the value 1

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------|
| `hijrahEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the era to represent, only 1 supported |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------|
| [HijrahEra](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahEra#)! | the HijrahEra.AH singleton, not null |

| Exceptions ||
|-------------------------------|-------------------------|
| `java.time.DateTimeException` | if the value is invalid |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

The range object expresses the minimum and maximum valid values for a field. This era is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#) then the query is implemented here. The`ERA`field returns the range. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.rangeRefinedBy(TemporalAccessor)`passing`this`as the argument. Whether the range can be obtained is determined by the field.

The`ERA`field returns a range for the one valid Hijrah era.

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
