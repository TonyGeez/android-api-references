# BatteryState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BatteryState

Kotlin| [Java](../android/hardware/BatteryState.md) 
| --- | --- |

```
abstract class BatteryState
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.BatteryState](../android/hardware/BatteryState.md) |

The BatteryState class is a representation of a single battery on a device.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_CHARGING](../android/hardware/BatteryState.md) Battery is charging. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_DISCHARGING](../android/hardware/BatteryState.md) Battery is discharging. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FULL](../android/hardware/BatteryState.md) Battery is full. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_NOT_CHARGING](../android/hardware/BatteryState.md) Battery is connected to power but not charging. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_UNKNOWN](../android/hardware/BatteryState.md) Battery status is unknown. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [BatteryState](../android/hardware/BatteryState.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCapacity](../android/hardware/BatteryState.md))`()` Get remaining battery capacity as float percentage \[0. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](../android/hardware/BatteryState.md))`()` Get the battery status. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPresent](../android/hardware/BatteryState.md))`()` Check whether the hardware has a battery. |
| --- | --- |

## Constants

### STATUS_CHARGING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_CHARGING: Int
```

Battery is charging. 

 Value: 2

### STATUS_DISCHARGING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_DISCHARGING: Int
```

Battery is discharging. 

 Value: 3

### STATUS_FULL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FULL: Int
```

Battery is full. 

 Value: 5

### STATUS_NOT_CHARGING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_NOT_CHARGING: Int
```

Battery is connected to power but not charging. 

 Value: 4

### STATUS_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_UNKNOWN: Int
```

Battery status is unknown. 

 Value: 1

## Public constructors

### BatteryState

```
BatteryState()
```

## Public methods

### getCapacity

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCapacity(): Float
```

Get remaining battery capacity as float percentage \[0.0f, 1.0f\] of total capacity Returns NaN when battery capacity can't be read.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the battery capacity. Value is between -1.0f and 1.0f inclusive |

### getStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getStatus(): Int
```

Get the battery status.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the battery status. Value is [android.hardware.BatteryState#STATUS_UNKNOWN](../android/hardware/BatteryState.md), [android.hardware.BatteryState#STATUS_CHARGING](../android/hardware/BatteryState.md), [android.hardware.BatteryState#STATUS_DISCHARGING](../android/hardware/BatteryState.md), [android.hardware.BatteryState#STATUS_NOT_CHARGING](../android/hardware/BatteryState.md), or [android.hardware.BatteryState#STATUS_FULL](../android/hardware/BatteryState.md) |

### isPresent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isPresent(): Boolean
```

Check whether the hardware has a battery.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the hardware has a battery, else false. |
