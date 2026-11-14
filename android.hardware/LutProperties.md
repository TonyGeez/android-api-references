# LutProperties

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LutProperties

Kotlin| [Java](../android/hardware/LutProperties.md) 
| --- | --- |

```
class LutProperties
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.LutProperties](../android/hardware/LutProperties.md) |

Provides Lut properties of the device.

A Lut (Look-Up Table) is a pre-calculated table for color correction. Applications may be interested in the Lut properties exposed by this class to determine if the Lut(s) they select using [android.view.SurfaceControl.Transaction#setLuts](../android/view/SurfaceControl.Transaction.md))are by the HWC.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONE_DIMENSION](../android/hardware/LutProperties.md) The Lut is one dimensional |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLING_KEY_CIE_Y](../android/hardware/LutProperties.md) use y of CIE XYZ as the gain value of a lut |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLING_KEY_MAX_RGB](../android/hardware/LutProperties.md) use max of r,g,b channel as the gain value of a Lut |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLING_KEY_RGB](../android/hardware/LutProperties.md) use r,g,b channel as the gain value of a Lut |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THREE_DIMENSION](../android/hardware/LutProperties.md) The Lut is three dimensional |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimension](../android/hardware/LutProperties.md))`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getSamplingKeys](../android/hardware/LutProperties.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](../android/hardware/LutProperties.md))`()` <br /> |
| --- | --- |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.hardware.LutProperties#ONE_DIMENSION](../android/hardware/LutProperties.md), or [android.hardware.LutProperties#THREE_DIMENSION](../android/hardware/LutProperties.md) |

### getSamplingKeys

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSamplingKeys(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the list of sampling keys This value cannot be`null`. Value is [android.hardware.LutProperties#SAMPLING_KEY_RGB](../android/hardware/LutProperties.md), [android.hardware.LutProperties#SAMPLING_KEY_MAX_RGB](../android/hardware/LutProperties.md), or [android.hardware.LutProperties#SAMPLING_KEY_CIE_Y](../android/hardware/LutProperties.md) |

### getSize

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the size of the Lut for each dimension |
