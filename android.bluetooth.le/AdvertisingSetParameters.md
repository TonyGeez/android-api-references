Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdvertisingSetParameters

Kotlin | [Java](https://developer.android.com/reference/android/bluetooth/le/AdvertisingSetParameters "View this page in Java")

```
class AdvertisingSetParameters : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.le.AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#) |

The `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#` provide a way to adjust advertising preferences for each Bluetooth LE advertising set. Use `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters.Builder` to create an instance of this class.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#INTERVAL_HIGH:kotlin.Int` Advertise on low frequency, around every 1000ms. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#INTERVAL_LOW:kotlin.Int` Perform high frequency, low latency advertising, around every 100ms. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#INTERVAL_MAX:kotlin.Int` Maximum value for advertising interval. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#INTERVAL_MEDIUM:kotlin.Int` Advertise on medium frequency, around every 250ms. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#INTERVAL_MIN:kotlin.Int` Minimum value for advertising interval. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#TX_POWER_HIGH:kotlin.Int` Advertise using high TX power level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#TX_POWER_LOW:kotlin.Int` Advertise using low TX power level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#TX_POWER_MAX:kotlin.Int` Maximum value for TX power. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#TX_POWER_MEDIUM:kotlin.Int` Advertise using medium TX power level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#TX_POWER_MIN:kotlin.Int` Minimum value for TX power. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#TX_POWER_ULTRA_LOW:kotlin.Int` Advertise using the lowest transmission (TX) power level. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#getInterval()()` Returns the advertising interval. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#getPrimaryPhy()()` Returns the primary advertising phy. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#getSecondaryPhy()()` Returns the secondary advertising phy. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#getTxPowerLevel()()` Returns the TX power level for advertising. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#includeTxPower()()` Returns whether the TX Power will be included. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#isAnonymous()()` Returns whether the advertisement will be anonymous. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#isConnectable()()` Returns whether the advertisement will be connectable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#isDiscoverable()()` Returns whether the advertisement will be discoverable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#isLegacy()()` Returns whether the legacy advertisement will be used. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#isScannable()()` Returns whether the advertisement will be scannable. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### INTERVAL_HIGH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_HIGH: Int
```

Advertise on low frequency, around every 1000ms. This is the default and preferred advertising mode as it consumes the least power.

 Value: 1600

### INTERVAL_LOW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_LOW: Int
```

Perform high frequency, low latency advertising, around every 100ms. This has the highest power consumption and should not be used for continuous background advertising.

 Value: 160

### INTERVAL_MAX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_MAX: Int
```

Maximum value for advertising interval.

 Value: 16777215

### INTERVAL_MEDIUM

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_MEDIUM: Int
```

Advertise on medium frequency, around every 250ms. This is balanced between advertising frequency and power consumption.

 Value: 400

### INTERVAL_MIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_MIN: Int
```

Minimum value for advertising interval.

 Value: 160

### TX_POWER_HIGH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TX_POWER_HIGH: Int
```

Advertise using high TX power level. This corresponds to largest visibility range of the advertising packet.

 Value: 1

### TX_POWER_LOW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TX_POWER_LOW: Int
```

Advertise using low TX power level.

 Value: -15

### TX_POWER_MAX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TX_POWER_MAX: Int
```

Maximum value for TX power.

 Value: 1

### TX_POWER_MEDIUM

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TX_POWER_MEDIUM: Int
```

Advertise using medium TX power level.

 Value: -7

### TX_POWER_MIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TX_POWER_MIN: Int
```

Minimum value for TX power.

 Value: -127

### TX_POWER_ULTRA_LOW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TX_POWER_ULTRA_LOW: Int
```

Advertise using the lowest transmission (TX) power level. Low transmission power can be used to restrict the visibility range of advertising packets.

 Value: -21

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getInterval

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInterval(): Int
```

Returns the advertising interval.

### getPrimaryPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPrimaryPhy(): Int
```

Returns the primary advertising phy.

### getSecondaryPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSecondaryPhy(): Int
```

Returns the secondary advertising phy.

### getTxPowerLevel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTxPowerLevel(): Int
```

Returns the TX power level for advertising.

### includeTxPower

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun includeTxPower(): Boolean
```

Returns whether the TX Power will be included.

### isAnonymous

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAnonymous(): Boolean
```

Returns whether the advertisement will be anonymous.

### isConnectable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isConnectable(): Boolean
```

Returns whether the advertisement will be connectable.

### isDiscoverable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDiscoverable(): Boolean
```

Returns whether the advertisement will be discoverable.

### isLegacy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLegacy(): Boolean
```

Returns whether the legacy advertisement will be used.

### isScannable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isScannable(): Boolean
```

Returns whether the advertisement will be scannable.

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AdvertisingSetParameters!>
```
