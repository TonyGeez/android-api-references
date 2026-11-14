# CpuHeadroomParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CpuHeadroomParams

Kotlin| [Java](CpuHeadroomParams.md) 
| --- | --- |

```
class CpuHeadroomParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.CpuHeadroomParams](CpuHeadroomParams.md) |

Headroom request params used by [SystemHealthManager.getCpuHeadroom(CpuHeadroomParams)](../android.os.health/SystemHealthManager.md)).

This class is immutable and one should use the [Builder](../android/os/CpuHeadroomParams.Builder.md) to build a new instance.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------|
| | [Builder](../android/os/CpuHeadroomParams.Builder.md) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CPU_HEADROOM_CALCULATION_TYPE_AVERAGE](CpuHeadroomParams.md) The headroom calculation type bases on average value over a specified window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CPU_HEADROOM_CALCULATION_TYPE_MIN](CpuHeadroomParams.md) The headroom calculation type bases on minimum value over a specified window. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](CpuHeadroomParams.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCalculationType](CpuHeadroomParams.md))`()` Gets the headroom calculation type. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCalculationWindowMillis](CpuHeadroomParams.md))`()` Gets the headroom calculation window size in milliseconds. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getTids](CpuHeadroomParams.md))`()` Gets the TIDs to track. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](CpuHeadroomParams.md))`()` <br /> |
| [CpuHeadroomParams.Builder](../android/os/CpuHeadroomParams.Builder.md) | [toBuilder](CpuHeadroomParams.md))`()` Returns a new builder with the same values as this object. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](CpuHeadroomParams.md))`()` <br /> |

## Constants

### CPU_HEADROOM_CALCULATION_TYPE_AVERAGE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CPU_HEADROOM_CALCULATION_TYPE_AVERAGE: Int
```

The headroom calculation type bases on average value over a specified window. 

 Value: 1

### CPU_HEADROOM_CALCULATION_TYPE_MIN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CPU_HEADROOM_CALCULATION_TYPE_MIN: Int
```

The headroom calculation type bases on minimum value over a specified window. 

 Value: 0

## Public methods

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCalculationType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCalculationType(): Int
```

Gets the headroom calculation type.

This will return the default value chosen by the device if not set.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.os.CpuHeadroomParams#CPU_HEADROOM_CALCULATION_TYPE_MIN](CpuHeadroomParams.md), or [android.os.CpuHeadroomParams#CPU_HEADROOM_CALCULATION_TYPE_AVERAGE](CpuHeadroomParams.md) |

### getCalculationWindowMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCalculationWindowMillis(): Long
```

Gets the headroom calculation window size in milliseconds.

This will return the default value chosen by the device if not set. 

### getTids

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTids(): IntArray
```

Gets the TIDs to track.

This will return a copy of the TIDs in the params, or null if the params is not set. 

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toBuilder

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toBuilder(): CpuHeadroomParams.Builder
```

Returns a new builder with the same values as this object.

| Return ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [CpuHeadroomParams.Builder](../android/os/CpuHeadroomParams.Builder.md) | This value cannot be`null`. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
