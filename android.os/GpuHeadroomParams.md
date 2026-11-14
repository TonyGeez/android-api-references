# GpuHeadroomParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GpuHeadroomParams

Kotlin| [Java](https://developer.android.com/reference/android/os/GpuHeadroomParams "View this page in Java") 
| --- | --- |

```
class GpuHeadroomParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.GpuHeadroomParams](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#) |

Headroom request params used by [SystemHealthManager.getGpuHeadroom(GpuHeadroomParams)](https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroom(android.os.GpuHeadroomParams)).

This class is immutable and one should use the [Builder](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams.Builder) to build a new instance.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams.Builder) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_HEADROOM_CALCULATION_TYPE_AVERAGE](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#GPU_HEADROOM_CALCULATION_TYPE_AVERAGE:kotlin.Int) The headroom calculation type bases on average value over a specified window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_HEADROOM_CALCULATION_TYPE_MIN](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#GPU_HEADROOM_CALCULATION_TYPE_MIN:kotlin.Int) The headroom calculation type bases on minimum value over a specified window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MAX](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MAX:kotlin.Int) The maximum size of the window to compute the headroom over. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MIN](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#GPU_HEADROOM_CALCULATION_WINDOW_MILLIS_MIN:kotlin.Int) The minimum size of the window to compute the headroom over. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCalculationType](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#getCalculationType())`()` Gets the headroom calculation type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCalculationWindowMillis](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#getCalculationWindowMillis())`()` Gets the headroom calculation window size in milliseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#toString())`()` <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.os.GpuHeadroomParams#GPU_HEADROOM_CALCULATION_TYPE_MIN](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#GPU_HEADROOM_CALCULATION_TYPE_MIN:kotlin.Int), or [android.os.GpuHeadroomParams#GPU_HEADROOM_CALCULATION_TYPE_AVERAGE](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams#GPU_HEADROOM_CALCULATION_TYPE_AVERAGE:kotlin.Int) |

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
