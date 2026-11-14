# SensorPrivacyManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorPrivacyManager

Kotlin| [Java](SensorPrivacyManager.md) 
| --- | --- |

```
class SensorPrivacyManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.SensorPrivacyManager](SensorPrivacyManager.md) |

This class provides information about the microphone and camera toggles.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Sensors](../android/hardware/SensorPrivacyManager.Sensors.md) Sensor constants which are used in [SensorPrivacyManager](SensorPrivacyManager.md) |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOGGLE_TYPE_HARDWARE](SensorPrivacyManager.md) Constant for hardware toggle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOGGLE_TYPE_SOFTWARE](SensorPrivacyManager.md) Constant for software toggle. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSensorToggle](SensorPrivacyManager.md))`(`sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given toggle is supported on this device |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSensorToggle](SensorPrivacyManager.md))`(`toggleType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sensor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given toggle is supported on this device |

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
| `sensor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sensor to check Value is [android.hardware.SensorPrivacyManager.Sensors#MICROPHONE](../android/hardware/SensorPrivacyManager.Sensors.md), or [android.hardware.SensorPrivacyManager.Sensors#CAMERA](../android/hardware/SensorPrivacyManager.Sensors.md) |

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
| `sensor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sensor to check Value is [android.hardware.SensorPrivacyManager.Sensors#MICROPHONE](../android/hardware/SensorPrivacyManager.Sensors.md), or [android.hardware.SensorPrivacyManager.Sensors#CAMERA](../android/hardware/SensorPrivacyManager.Sensors.md) |
| `toggleType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.SensorPrivacyManager#TOGGLE_TYPE_SOFTWARE](SensorPrivacyManager.md), or [android.hardware.SensorPrivacyManager#TOGGLE_TYPE_HARDWARE](SensorPrivacyManager.md) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the toggle for the sensor is supported on this device. |
