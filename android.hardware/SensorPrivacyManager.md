# SensorPrivacyManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorPrivacyManager

Kotlin| [Java](https://developer.android.com/reference/android/hardware/SensorPrivacyManager "View this page in Java") 
| --- | --- |

```
class SensorPrivacyManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.SensorPrivacyManager](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager#) |

This class provides information about the microphone and camera toggles.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Sensors](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager.Sensors) Sensor constants which are used in [SensorPrivacyManager](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager#) |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOGGLE_TYPE_HARDWARE](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager#TOGGLE_TYPE_HARDWARE:kotlin.Int) Constant for hardware toggle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOGGLE_TYPE_SOFTWARE](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager#TOGGLE_TYPE_SOFTWARE:kotlin.Int) Constant for software toggle. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSensorToggle](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager#supportsSensorToggle(kotlin.Int))`(`sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given toggle is supported on this device |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSensorToggle](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager#supportsSensorToggle(kotlin.Int,%20kotlin.Int))`(`toggleType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given toggle is supported on this device |

## Constants

### TOGGLE_TYPE_HARDWARE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOGGLE_TYPE_HARDWARE: Int
```

Constant for hardware toggle. 

 Value: 2

### TOGGLE_TYPE_SOFTWARE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOGGLE_TYPE_SOFTWARE: Int
```

Constant for software toggle. 

 Value: 1

## Public methods

### supportsSensorToggle

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun supportsSensorToggle(sensor: Int): Boolean
```

Checks if the given toggle is supported on this device

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sensor to check Value is [android.hardware.SensorPrivacyManager.Sensors#MICROPHONE](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager.Sensors#MICROPHONE:kotlin.Int), or [android.hardware.SensorPrivacyManager.Sensors#CAMERA](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager.Sensors#CAMERA:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the toggle for the sensor is supported on this device. |

### supportsSensorToggle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun supportsSensorToggle(
    toggleType: Int, 
    sensor: Int
): Boolean
```

Checks if the given toggle is supported on this device

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sensor to check Value is [android.hardware.SensorPrivacyManager.Sensors#MICROPHONE](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager.Sensors#MICROPHONE:kotlin.Int), or [android.hardware.SensorPrivacyManager.Sensors#CAMERA](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager.Sensors#CAMERA:kotlin.Int) |
| `toggleType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.SensorPrivacyManager#TOGGLE_TYPE_SOFTWARE](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager#TOGGLE_TYPE_SOFTWARE:kotlin.Int), or [android.hardware.SensorPrivacyManager#TOGGLE_TYPE_HARDWARE](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager#TOGGLE_TYPE_HARDWARE:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the toggle for the sensor is supported on this device. |
