# AdvertiseSettings

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdvertiseSettings

Kotlin| [Java](AdvertiseSettings.md) 
| --- | --- |

```
class AdvertiseSettings : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.AdvertiseSettings](AdvertiseSettings.md) |

The [AdvertiseSettings](AdvertiseSettings.md) provide a way to adjust advertising preferences for each Bluetooth LE advertisement instance. Use [AdvertiseSettings.Builder](../android/bluetooth/le/AdvertiseSettings.Builder.md) to create an instance of this class.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/bluetooth/le/AdvertiseSettings.Builder.md) Builder class for [AdvertiseSettings](AdvertiseSettings.md). |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_MODE_BALANCED](AdvertiseSettings.md) Perform Bluetooth LE advertising in balanced power mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_MODE_LOW_LATENCY](AdvertiseSettings.md) Perform Bluetooth LE advertising in low latency, high power mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_MODE_LOW_POWER](AdvertiseSettings.md) Perform Bluetooth LE advertising in low power mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_TX_POWER_HIGH](AdvertiseSettings.md) Advertise using high TX power level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_TX_POWER_LOW](AdvertiseSettings.md) Advertise using low TX power level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_TX_POWER_MEDIUM](AdvertiseSettings.md) Advertise using medium TX power level. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_TX_POWER_ULTRA_LOW](AdvertiseSettings.md) Advertise using the lowest transmission (TX) power level. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](AdvertiseSettings.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](AdvertiseSettings.md))`()` Returns the advertise mode. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeout](AdvertiseSettings.md))`()` Returns the advertising time limit in milliseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTxPowerLevel](AdvertiseSettings.md))`()` Returns the TX power level for advertising. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnectable](AdvertiseSettings.md))`()` Returns whether the advertisement will indicate connectable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDiscoverable](AdvertiseSettings.md))`()` Returns whether the advertisement will be discoverable. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AdvertiseSettings.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](AdvertiseSettings.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AdvertiseSettings](AdvertiseSettings.md)!\> | [CREATOR](AdvertiseSettings.md) <br /> |

## Constants

### ADVERTISE_MODE_BALANCED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_MODE_BALANCED: Int
```

Perform Bluetooth LE advertising in balanced power mode. This is balanced between advertising frequency and power consumption. 

 Value: 1

### ADVERTISE_MODE_LOW_LATENCY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_MODE_LOW_LATENCY: Int
```

Perform Bluetooth LE advertising in low latency, high power mode. This has the highest power consumption and should not be used for continuous background advertising. 

 Value: 2

### ADVERTISE_MODE_LOW_POWER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_MODE_LOW_POWER: Int
```

Perform Bluetooth LE advertising in low power mode. This is the default and preferred advertising mode as it consumes the least power. 

 Value: 0

### ADVERTISE_TX_POWER_HIGH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_TX_POWER_HIGH: Int
```

Advertise using high TX power level. This corresponds to largest visibility range of the advertising packet. 

 Value: 3

### ADVERTISE_TX_POWER_LOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_TX_POWER_LOW: Int
```

Advertise using low TX power level. 

 Value: 1

### ADVERTISE_TX_POWER_MEDIUM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_TX_POWER_MEDIUM: Int
```

Advertise using medium TX power level. 

 Value: 2

### ADVERTISE_TX_POWER_ULTRA_LOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_TX_POWER_ULTRA_LOW: Int
```

Advertise using the lowest transmission (TX) power level. Low transmission power can be used to restrict the visibility range of advertising packets. 

 Value: 0

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMode(): Int
```

Returns the advertise mode. 

### getTimeout

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeout(): Int
```

Returns the advertising time limit in milliseconds. 

### getTxPowerLevel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTxPowerLevel(): Int
```

Returns the TX power level for advertising. 

### isConnectable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnectable(): Boolean
```

Returns whether the advertisement will indicate connectable. 

### isDiscoverable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDiscoverable(): Boolean
```

Returns whether the advertisement will be discoverable. 

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AdvertiseSettings!>
```
