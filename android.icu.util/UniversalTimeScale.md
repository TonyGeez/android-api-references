# UniversalTimeScale

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UniversalTimeScale

Kotlin| [Java](https://developer.android.com/reference/android/icu/util/UniversalTimeScale "View this page in Java") 
| --- | --- |

```
class UniversalTimeScale
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.UniversalTimeScale](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#) |

There are quite a few different conventions for binary datetime, depending on different platforms and protocols. Some of these have severe drawbacks. For example, people using Unix time (seconds since Jan 1, 1970, usually in a 32-bit integer) think that they are safe until near the year 2038. But cases can and do arise where arithmetic manipulations causes serious problems. Consider the computation of the average of two datetimes, for example: if one calculates them with`averageTime = (time1 + time2)/2`, there will be overflow even with dates beginning in 2004. Moreover, even if these problems don't occur, there is the issue of conversion back and forth between different systems.

Binary datetimes differ in a number of ways: the datatype, the unit, and the epoch (origin). We refer to these as time scales.

ICU implements a universal time scale that is similar to the .NET framework's System.DateTime. The universal time scale is a 64-bit integer that holds ticks since midnight, January 1st, 0001. (One tick is 100 nanoseconds.) Negative values are supported. This has enough range to guarantee that calculations involving dates around the present are safe.

The universal time scale always measures time according to the proleptic Gregorian calendar. That is, the Gregorian calendar's leap year rules are used for all times, even before 1582 when it was introduced. (This is different from the default ICU calendar which switches from the Julian to the Gregorian calendar in 1582. See GregorianCalendar.setGregorianChange() and ucal_setGregorianChange().) ICU provides conversion functions to and from all other major time scales, allowing datetimes in any time scale to be converted to the universal time scale, safely manipulated, and converted back to any other datetime time scale.

For more details and background, see the [Universal Time Scale](https://unicode-org.github.io/icu/userguide/datetime/universaltimescale) chapter in the ICU User Guide.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DB2_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#DB2_TIME:kotlin.Int) Used in DB2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOTNET_DATE_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#DOTNET_DATE_TIME:kotlin.Int) Used in the . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EPOCH_OFFSET_PLUS_1_VALUE](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#EPOCH_OFFSET_PLUS_1_VALUE:kotlin.Int) The constant used to select the epoch plus one value for a time scale. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EPOCH_OFFSET_VALUE](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#EPOCH_OFFSET_VALUE:kotlin.Int) The constant used to select the epoch offset value for a time scale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXCEL_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#EXCEL_TIME:kotlin.Int) Used in Excel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_MAX_VALUE](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#FROM_MAX_VALUE:kotlin.Int) The constant used to select the maximum from value for a time scale. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_MIN_VALUE](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#FROM_MIN_VALUE:kotlin.Int) The constant used to select the minimum from value for a time scale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ICU4C_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#ICU4C_TIME:kotlin.Int) Used in the ICU4C. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JAVA_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#JAVA_TIME:kotlin.Int) Used in the JDK. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAC_OLD_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#MAC_OLD_TIME:kotlin.Int) Used in older Macintosh systems. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAC_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#MAC_TIME:kotlin.Int) Used in the JDK. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_SCALE](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#MAX_SCALE:kotlin.Int) This is the first unused time scale value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TO_MAX_VALUE](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#TO_MAX_VALUE:kotlin.Int) The constant used to select the maximum to value for a time scale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TO_MIN_VALUE](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#TO_MIN_VALUE:kotlin.Int) The constant used to select the minimum to value for a time scale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNITS_VALUE](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#UNITS_VALUE:kotlin.Int) The constant used to select the units value for a time scale. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNIX_MICROSECONDS_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#UNIX_MICROSECONDS_TIME:kotlin.Int) Data is a`long`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNIX_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#UNIX_TIME:kotlin.Int) Used in Unix systems. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_FILE_TIME](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#WINDOWS_FILE_TIME:kotlin.Int) Used in Windows for file times. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | [bigDecimalFrom](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#bigDecimalFrom(android.icu.math.BigDecimal,%20kotlin.Int))`(`otherTime:` ` [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)!`, `timeScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert a`BigDecimal`datetime from the given time scale to the universal time scale. |
| static [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | [bigDecimalFrom](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#bigDecimalFrom(kotlin.Double,%20kotlin.Int))`(`otherTime:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `timeScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert a`double`datetime from the given time scale to the universal time scale. |
| static [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | [bigDecimalFrom](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#bigDecimalFrom(kotlin.Long,%20kotlin.Int))`(`otherTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `timeScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert a`long`datetime from the given time scale to the universal time scale. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [from](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#from(kotlin.Long,%20kotlin.Int))`(`otherTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `timeScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert a`long`datetime from the given time scale to the universal time scale. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeScaleValue](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#getTimeScaleValue(kotlin.Int,%20kotlin.Int))`(`scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a value associated with a particular time scale. |
| static [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | [toBigDecimal](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#toBigDecimal(android.icu.math.BigDecimal,%20kotlin.Int))`(`universalTime:` ` [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)!`, `timeScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert a datetime from the universal time scale to a`BigDecimal`in the given time scale. |
| --- | --- |
| static [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | [toBigDecimal](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#toBigDecimal(kotlin.Long,%20kotlin.Int))`(`universalTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `timeScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert a datetime from the universal time scale to a`BigDecimal`in the given time scale. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#toLong(kotlin.Long,%20kotlin.Int))`(`universalTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `timeScale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert a datetime from the universal time scale stored as a`BigDecimal`to a`long`in the given time scale. |

## Constants

### DB2_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DB2_TIME: Int
```

Used in DB2. Data is a`?unknown?`. Value is days since December 31, 1899. 

 Value: 8

### DOTNET_DATE_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOTNET_DATE_TIME: Int
```

Used in the .NET framework's`System.DateTime`structure. Data is a`long`. Value is ticks (1 tick == 100 nanoseconds) since January 1, 0001. 

 Value: 4

### EPOCH_OFFSET_PLUS_1_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EPOCH_OFFSET_PLUS_1_VALUE: Int
```

The constant used to select the epoch plus one value for a time scale. NOTE: This is an internal value. DO NOT USE IT. May not actually be equal to the epoch offset value plus one. 

 Value: 6

**See Also**

- [#getTimeScaleValue](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#getTimeScaleValue(kotlin.Int,%20kotlin.Int)) 

### EPOCH_OFFSET_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EPOCH_OFFSET_VALUE: Int
```

The constant used to select the epoch offset value for a time scale. 

 Value: 1

**See Also**

- [#getTimeScaleValue](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#getTimeScaleValue(kotlin.Int,%20kotlin.Int)) 

### EXCEL_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXCEL_TIME: Int
```

Used in Excel. Data is a`?unknown?`. Value is days since December 31, 1899. 

 Value: 7

### FROM_MAX_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_MAX_VALUE: Int
```

The constant used to select the maximum from value for a time scale. 

 Value: 3

**See Also**

- [#getTimeScaleValue](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#getTimeScaleValue(kotlin.Int,%20kotlin.Int)) 

### FROM_MIN_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_MIN_VALUE: Int
```

The constant used to select the minimum from value for a time scale. 

 Value: 2

**See Also**

- [#getTimeScaleValue](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#getTimeScaleValue(kotlin.Int,%20kotlin.Int)) 

### ICU4C_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ICU4C_TIME: Int
```

Used in the ICU4C. Data is a`double`. Value is milliseconds since January 1, 1970. 

 Value: 2

### JAVA_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JAVA_TIME: Int
```

Used in the JDK. Data is a`long`. Value is milliseconds since January 1, 1970. 

 Value: 0

### MAC_OLD_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAC_OLD_TIME: Int
```

Used in older Macintosh systems. Data is an`int`. Value is seconds since January 1, 1904. 

 Value: 5

### MAC_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAC_TIME: Int
```

Used in the JDK. Data is a`double`. Value is milliseconds since January 1, 2001. 

 Value: 6

### MAX_SCALE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_SCALE: Int
```

**Deprecated:** *ICU 59*

This is the first unused time scale value. 

 Value: 10

### TO_MAX_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TO_MAX_VALUE: Int
```

The constant used to select the maximum to value for a time scale. 

 Value: 5

**See Also**

- [#getTimeScaleValue](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#getTimeScaleValue(kotlin.Int,%20kotlin.Int)) 

### TO_MIN_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TO_MIN_VALUE: Int
```

The constant used to select the minimum to value for a time scale. 

 Value: 4

**See Also**

- [#getTimeScaleValue](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale#getTimeScaleValue(kotlin.Int,%20kotlin.Int)) 

### UNITS_VALUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNITS_VALUE: Int
```

The constant used to select the units value for a time scale. 

 Value: 0

### UNIX_MICROSECONDS_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNIX_MICROSECONDS_TIME: Int
```

Data is a`long`. Value is microseconds since January 1, 1970. Similar to Unix time (linear value from 1970) and struct timeval (microseconds resolution). 

 Value: 9

### UNIX_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNIX_TIME: Int
```

Used in Unix systems. Data is an`int`or a`long`. Value is seconds since January 1, 1970. 

 Value: 1

### WINDOWS_FILE_TIME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_FILE_TIME: Int
```

Used in Windows for file times. Data is a`long`. Value is ticks (1 tick == 100 nanoseconds) since January 1, 1601. 

 Value: 3

## Public methods

### bigDecimalFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun bigDecimalFrom(
    otherTime: BigDecimal!, 
    timeScale: Int
): BigDecimal!
```

Convert a`BigDecimal`datetime from the given time scale to the universal time scale. All calculations are done using`BigDecimal`to guarantee that the value does not go out of range.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------|
| `otherTime` | [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)!:The`BigDecimal`datetime |
| `timeScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time scale to convert from |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | The datetime converted to the universal time scale |

### bigDecimalFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun bigDecimalFrom(
    otherTime: Double, 
    timeScale: Int
): BigDecimal!
```

Convert a`double`datetime from the given time scale to the universal time scale. All calculations are done using`BigDecimal`to guarantee that the value does not go out of range.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------|
| `otherTime` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The`double`datetime |
| `timeScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time scale to convert from |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | The datetime converted to the universal time scale |

### bigDecimalFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun bigDecimalFrom(
    otherTime: Long, 
    timeScale: Int
): BigDecimal!
```

Convert a`long`datetime from the given time scale to the universal time scale. All calculations are done using`BigDecimal`to guarantee that the value does not go out of range.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------|
| `otherTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The`long`datetime |
| `timeScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time scale to convert from |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | The datetime converted to the universal time scale |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun from(
    otherTime: Long, 
    timeScale: Int
): Long
```

Convert a`long`datetime from the given time scale to the universal time scale.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------|
| `otherTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The`long`datetime |
| `timeScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time scale to convert from |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The datetime converted to the universal time scale |

### getTimeScaleValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getTimeScaleValue(
    scale: Int, 
    value: Int
): Long
```

Get a value associated with a particular time scale.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):- the time scale |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):- a constant representing the value to get |

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | - the value. |

### toBigDecimal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toBigDecimal(
    universalTime: BigDecimal!, 
    timeScale: Int
): BigDecimal!
```

Convert a datetime from the universal time scale to a`BigDecimal`in the given time scale.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `universalTime` | [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)!:The datetime in the universal time scale |
| `timeScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time scale to convert to |

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | The datetime converted to the given time scale |

### toBigDecimal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toBigDecimal(
    universalTime: Long, 
    timeScale: Int
): BigDecimal!
```

Convert a datetime from the universal time scale to a`BigDecimal`in the given time scale.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------|
| `universalTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The datetime in the universal time scale |
| `timeScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time scale to convert to |

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)! | The datetime converted to the given time scale |

### toLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toLong(
    universalTime: Long, 
    timeScale: Int
): Long
```

Convert a datetime from the universal time scale stored as a`BigDecimal`to a`long`in the given time scale. Since this calculation requires a divide, we must round. The straight forward way to round by adding half of the divisor will push the sum out of range for values within have the divisor of the limits of the precision of a`long`. To get around this, we do the rounding like this:

` (universalTime - units + units/2) / units + 1 `

(i.e. we subtract units first to guarantee that we'll still be in range when we add`units/2`. We then need to add one to the quotent to make up for the extra subtraction. This simplifies to:

` (universalTime - units/2) / units - 1 `

For negative values to round away from zero, we need to flip the signs:

` (universalTime + units/2) / units + 1 `

Since we also need to subtract the epochOffset, we fold the`+/- 1`into the offset value. (i.e.`epochOffsetP1`,`epochOffsetM1`.)

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------|
| `universalTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The datetime in the universal time scale |
| `timeScale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time scale to convert to |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The datetime converted to the given time scale |
