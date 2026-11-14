# JapaneseEra

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JapaneseEra

```
class JapaneseEra : Era, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.chrono.JapaneseEra](JapaneseEra.md) |

An era in the Japanese Imperial calendar system.

The Japanese government defines the official name and start date of each era. Eras are consecutive and their date ranges do not overlap, so the end date of one era is always the day before the start date of the next era.

The Java SE Platform supports all eras defined by the Japanese government, beginning with the Meiji era. Each era is identified in the Platform by an integer value and a name. The [of(int)](JapaneseEra.md))and [valueOf(java.lang.String)](JapaneseEra.md))methods may be used to obtain a singleton instance of`JapaneseEra`for each era. The [values()](JapaneseEra.md))method returns the singleton instances of all supported eras.

For convenience, this class declares a number of public static final fields that refer to singleton instances returned by the [values()](JapaneseEra.md))method.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](JapaneseEra.md))`(`style:` ` [TextStyle](../java.time.format/TextStyle.md)!`, `locale:` ` [Locale](../java.util/Locale.md)!`)` Gets the textual representation of this era. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getValue](JapaneseEra.md))`()` Gets the numeric era`int`value. |
| static [JapaneseEra](JapaneseEra.md)! | [of](JapaneseEra.md))`(`japaneseEra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtains an instance of`JapaneseEra`from an`int`value. |
| --- | --- |
| [ValueRange](../java.time.temporal/ValueRange.md)! | [range](JapaneseEra.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` Gets the range of valid values for the specified field. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](JapaneseEra.md))`()` <br /> |
| static [JapaneseEra](JapaneseEra.md)! | [valueOf](JapaneseEra.md))`(`japaneseEra:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the`JapaneseEra`with the name. |
| --- | --- |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [JapaneseEra](JapaneseEra.md)!\>! | [values](JapaneseEra.md))`()` Returns an array of JapaneseEras. |

| Inherited functions ||
|---|---|
| From class [Era](Era.md) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Temporal](../java.time.temporal/Temporal.md)! | [adjustInto](Era.md))`(`temporal:` ` [Temporal](../java.time.temporal/Temporal.md)!`)` <br /> Adjusts the specified temporal object to have the same era as this object. This returns a temporal object of the same observable type as the input with the era changed to be the same as this. The adjustment is equivalent to using [Temporal.with(TemporalField, long)](../java.time.temporal/Temporal.md))passing [ChronoField.ERA](../java.time.temporal/ChronoField.md) as the field. In most cases, it is clearer to reverse the calling pattern by using [Temporal.with(TemporalAdjuster)](../java.time.temporal/Temporal.md)): ```kotlin // these two lines are equivalent, but the second approach is recommended temporal = thisEra.adjustInto(temporal); temporal = temporal.with(thisEra); ``` This instance is immutable and unaffected by this method call. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](Era.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> Gets the value of the specified field from this era as an`int`. This queries this era for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown. If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The`ERA`field returns the value of the era. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`. If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](Era.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> Gets the value of the specified field from this era as a`long`. This queries this era for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown. If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The`ERA`field returns the value of the era. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`. If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.getFrom(TemporalAccessor)`passing`this`as the argument. Whether the value can be obtained, and what the value represents, is determined by the field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](Era.md))`(`field:` ` [TemporalField](../java.time.temporal/TemporalField.md)!`)` <br /> Checks if the specified field is supported. This checks if this era can be queried for the specified field. If false, then calling the [range](Era.md))and [get](Era.md))methods will throw an exception. If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The`ERA`field returns true. All other`ChronoField`instances will return false. If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.isSupportedBy(TemporalAccessor)`passing`this`as the argument. Whether the field is supported is determined by the field. <br /> | | R | [query](Era.md))`(`query:` ` [TemporalQuery](../java.time.temporal/TemporalQuery.md)<R>!`)` <br /> Queries this era using the specified query. This queries this era using the specified query strategy object. The`TemporalQuery`object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be. The result of this method is obtained by invoking the [TemporalQuery.queryFrom(TemporalAccessor)](../java.time.temporal/TemporalQuery.md))method on the specified query passing`this`as the argument. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [JapaneseEra](JapaneseEra.md)! | [HEISEI](JapaneseEra.md) The singleton instance for the 'Heisei' era (1989-01-08 - 2019-04-30) which has the value 2. |
| static [JapaneseEra](JapaneseEra.md)! | [MEIJI](JapaneseEra.md) The singleton instance for the 'Meiji' era (1868-01-01 - 1912-07-29) which has the value -1. |
| static [JapaneseEra](JapaneseEra.md)! | [REIWA](JapaneseEra.md) The singleton instance for the 'Reiwa' era (2019-05-01 - ) which has the value 3. |
| --- | --- |
| static [JapaneseEra](JapaneseEra.md)! | [SHOWA](JapaneseEra.md) The singleton instance for the 'Showa' era (1926-12-25 - 1989-01-07) which has the value 1. |
| static [JapaneseEra](JapaneseEra.md)! | [TAISHO](JapaneseEra.md) The singleton instance for the 'Taisho' era (1912-07-30 - 1926-12-24) which has the value 0. |

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

If no textual mapping is found then the [numeric value](Era.md))is returned.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [TextStyle](../java.time.format/TextStyle.md)!:the style of the text required, not null |
| `locale` | [Locale](../java.util/Locale.md)!:the locale to use, not null |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the text value of the era, not null |

### getValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): Int
```

Gets the numeric era`int`value.

The [SHOWA](JapaneseEra.md) era that contains 1970-01-01 (ISO calendar system) has the value 1. Later eras are numbered from 2 ([HEISEI](JapaneseEra.md)). Earlier eras are numbered 0 ([TAISHO](JapaneseEra.md)), -1 ([MEIJI](JapaneseEra.md))).

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the era value |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(japaneseEra: Int): JapaneseEra!
```

Obtains an instance of`JapaneseEra`from an`int`value.

- The value`1`is associated with the 'Showa' era, because it contains 1970-01-01 (ISO calendar system).
- The values`-1`and`0`are associated with two earlier eras, Meiji and Taisho, respectively.
- A value greater than`1`is associated with a later era, beginning with Heisei (`2`).

<br />

Every instance of`JapaneseEra`that is returned from the [values()](JapaneseEra.md))method has an int value (available via [Era.getValue()](Era.md))which is accepted by this method.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------|
| `japaneseEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the era to represent |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------|
| [JapaneseEra](JapaneseEra.md)! | the`JapaneseEra`singleton, not null |

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

If the field is a [ChronoField](../java.time.temporal/ChronoField.md) then the query is implemented here. The`ERA`field returns the range. All other`ChronoField`instances will throw an`UnsupportedTemporalTypeException`.

If the field is not a`ChronoField`, then the result of this method is obtained by invoking`TemporalField.rangeRefinedBy(TemporalAccessor)`passing`this`as the argument. Whether the range can be obtained is determined by the field.

The range of valid Japanese eras can change over time due to the nature of the Japanese calendar system.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!:the field to query the range for, not null |

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ValueRange](../java.time.temporal/ValueRange.md)! | the range of valid values for the field, not null |

| Exceptions ||
|-------------------------------------------------------|-----------------------------------------------|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun valueOf(japaneseEra: String!): JapaneseEra!
```

Returns the`JapaneseEra`with the name.

The string must match exactly the name of the era. (Extraneous whitespace characters are not permitted.)

Valid era names are the names of eras returned from [values()](JapaneseEra.md)).

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------|
| `japaneseEra` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the japaneseEra name; non-null |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------|
| [JapaneseEra](JapaneseEra.md)! | the`JapaneseEra`singleton, never null |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if there is not JapaneseEra with the specified name |

### values

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun values(): Array<JapaneseEra!>!
```

Returns an array of JapaneseEras. The array may contain eras defined by the Japanese government beyond the known era singletons.

This method may be used to iterate over the JapaneseEras as follows: 

```kotlin
for (JapaneseEra c : JapaneseEra.values())
      System.out.println(c);
  
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [JapaneseEra](JapaneseEra.md)!>! | an array of JapaneseEras |

## Properties

### HEISEI

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEISEI: JapaneseEra!
```

The singleton instance for the 'Heisei' era (1989-01-08 - 2019-04-30) which has the value 2. 

### MEIJI

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEIJI: JapaneseEra!
```

The singleton instance for the 'Meiji' era (1868-01-01 - 1912-07-29) which has the value -1. 

### REIWA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REIWA: JapaneseEra!
```

The singleton instance for the 'Reiwa' era (2019-05-01 - ) which has the value 3. The end date of this era is not specified, unless the Japanese Government defines it. 

### SHOWA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOWA: JapaneseEra!
```

The singleton instance for the 'Showa' era (1926-12-25 - 1989-01-07) which has the value 1. 

### TAISHO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAISHO: JapaneseEra!
```

The singleton instance for the 'Taisho' era (1912-07-30 - 1926-12-24) which has the value 0.
