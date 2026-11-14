# GpuHeadroomParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GpuHeadroomParams

Kotlin| [Java](../android/os/GpuHeadroomParams.md) 
| --- | --- |

```
class GpuHeadroomParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.GpuHeadroomParams](../android/os/GpuHeadroomParams.md) |

Headroom request params used by [SystemHealthManager.getGpuHeadroom(GpuHeadroomParams)](../android/os/health/SystemHealthManager.md)).

This class is immutable and one should use the [Builder](../android/os/GpuHeadroomParams.Builder.md) to build a new instance.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------|
| | [Builder](../android/os/GpuHeadroomParams.Builder.md) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_HEADROOM_CALCULATION_TYPE_AVERAGE](../android/os/GpuHeadroomParams.md) The headroom calculation type bases on average value over a specified window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_HEADROOM_CALCULATION_TYPE_MIN](../android/os/GpuHeadroomParams.md) The headroom calculation type bases on minimum value over a specified window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MAX](../android/os/GpuHeadroomParams.md) The maximum size of the window to compute the headroom over. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MIN](../android/os/GpuHeadroomParams.md) The minimum size of the window to compute the headroom over. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/os/GpuHeadroomParams.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCalculationType](../android/os/GpuHeadroomParams.md))`()` Gets the headroom calculation type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCalculationWindowMillis](../android/os/GpuHeadroomParams.md))`()` Gets the headroom calculation window size in milliseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/os/GpuHeadroomParams.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/os/GpuHeadroomParams.md))`()` <br /> |

## Constants

### GPU_HEADROOM_CALCULATION_TYPE_AVERAGE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPU_HEADROOM_CALCULATION_TYPE_AVERAGE: Int
```

The headroom calculation type bases on average value over a specified window. 

 Value: 1

### GPU_HEADROOM_CALCULATION_TYPE_MIN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPU_HEADROOM_CALCULATION_TYPE_MIN: Int
```

The headroom calculation type bases on minimum value over a specified window. 

 Value: 0

### GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MAX

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MAX: Int
```

The maximum size of the window to compute the headroom over. 

 Value: 10000

### GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MIN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MIN: Int
```

The minimum size of the window to compute the headroom over. 

 Value: 50

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.os.GpuHeadroomParams#GPU_HEADROOM_CALCULATION_TYPE_MIN](../android/os/GpuHeadroomParams.md), or [android.os.GpuHeadroomParams#GPU_HEADROOM_CALCULATION_TYPE_AVERAGE](../android/os/GpuHeadroomParams.md) |

### getCalculationWindowMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCalculationWindowMillis(): Int
```

Gets the headroom calculation window size in milliseconds.

This will return the default value chosen by the device if not set. 

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
