# LutProperties

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LutProperties

Kotlin| [Java](https://developer.android.com/reference/android/hardware/LutProperties "View this page in Java") 

```
class LutProperties
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.LutProperties](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#) |

Provides Lut properties of the device.

A Lut (Look-Up Table) is a pre-calculated table for color correction. Applications may be interested in the Lut properties exposed by this class to determine if the Lut(s) they select using [android.view.SurfaceControl.Transaction#setLuts](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction.html#setLuts(android.view.SurfaceControl,%20android.hardware.DisplayLuts))are by the HWC.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONE_DIMENSION](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#ONE_DIMENSION:kotlin.Int) The Lut is one dimensional |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLING_KEY_CIE_Y](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#SAMPLING_KEY_CIE_Y:kotlin.Int) use y of CIE XYZ as the gain value of a lut |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLING_KEY_MAX_RGB](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#SAMPLING_KEY_MAX_RGB:kotlin.Int) use max of r,g,b channel as the gain value of a Lut |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLING_KEY_RGB](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#SAMPLING_KEY_RGB:kotlin.Int) use r,g,b channel as the gain value of a Lut |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THREE_DIMENSION](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#THREE_DIMENSION:kotlin.Int) The Lut is three dimensional |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimension](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#getDimension())`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getSamplingKeys](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#getSamplingKeys())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#getSize())`()` <br /> |

## Constants

### ONE_DIMENSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ONE_DIMENSION: Int
```

The Lut is one dimensional 

 Value: 1

### SAMPLING_KEY_CIE_Y

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLING_KEY_CIE_Y: Int
```

use y of CIE XYZ as the gain value of a lut 

 Value: 2

### SAMPLING_KEY_MAX_RGB

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLING_KEY_MAX_RGB: Int
```

use max of r,g,b channel as the gain value of a Lut 

 Value: 1

### SAMPLING_KEY_RGB

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLING_KEY_RGB: Int
```

use r,g,b channel as the gain value of a Lut 

 Value: 0

### THREE_DIMENSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val THREE_DIMENSION: Int
```

The Lut is three dimensional 

 Value: 3

## Public methods

### getDimension

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDimension(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.hardware.LutProperties#ONE_DIMENSION](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#ONE_DIMENSION:kotlin.Int), or [android.hardware.LutProperties#THREE_DIMENSION](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#THREE_DIMENSION:kotlin.Int) |

### getSamplingKeys

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSamplingKeys(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the list of sampling keys This value cannot be`null`. Value is [android.hardware.LutProperties#SAMPLING_KEY_RGB](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#SAMPLING_KEY_RGB:kotlin.Int), [android.hardware.LutProperties#SAMPLING_KEY_MAX_RGB](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#SAMPLING_KEY_MAX_RGB:kotlin.Int), or [android.hardware.LutProperties#SAMPLING_KEY_CIE_Y](https://developer.android.com/reference/kotlin/android/hardware/LutProperties#SAMPLING_KEY_CIE_Y:kotlin.Int) |

### getSize

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the size of the Lut for each dimension |
