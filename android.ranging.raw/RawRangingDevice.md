Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RawRangingDevice

```
class RawRangingDevice : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.ranging.raw.RawRangingDevice](RawRangingDevice.md) |

Represents a device participating in ranging operations. This class supports multiple ranging technologies, including UWB, BLE CS, BLE RSSI and Wi-Fi NAN-RTT. The configuration for each technology is provided through corresponding parameter objects.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/ranging/raw/RawRangingDevice.Builder` Builder class for creating instances of RawRangingDevice. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/raw/RawRangingDevice#UPDATE_RATE_FREQUENT:kotlin.Int` Frequent ranging interval. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/raw/RawRangingDevice#UPDATE_RATE_INFREQUENT:kotlin.Int` Infrequent ranging interval. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/raw/RawRangingDevice#UPDATE_RATE_NORMAL:kotlin.Int` Normal ranging interval (Default). |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [BleRssiRangingParams](../android.ranging.ble.rssi/BleRssiRangingParams.md)? | getBleRssiRangingParams Returns the BLE rssi ranging parameters, if applicable. |
| [BleCsRangingParams](../android.ranging.ble.cs/BleCsRangingParams.md)? | getCsRangingParams Returns the CS ranging parameters, if applicable. |
| --- | --- |
| [DlTdoaRangingParams](../android/ranging/uwb/DlTdoaRangingParams.md)? | getDlTdoaRangingParams Returns the DL-TDOA ranging parameters, if applicable. |
| [RangingDevice](../android.ranging/RangingDevice.md) | getRangingDevice Returns the `https://developer.android.com/reference/kotlin/android/ranging/RangingDevice.html#` associated with this instance. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Duration](../java.time/Duration.md)!\> | getRangingIntervalValues Returns a map of ranging technologies to their corresponding ranging interval durations for available ranging technologies parameters. |
| --- | --- |
| [RttRangingParams](../android.ranging.wifi.rtt/RttRangingParams.md)? | getRttRangingParams Returns the RTT ranging parameters, if applicable. |
| [RttStationRangingParams](../android.ranging.wifi.rtt/RttStationRangingParams.md)? | getRttStationRangingParams Returns the Wi-Fi STA-AP ranging parameters, if applicable. |
| [UwbRangingParams](../android.ranging.uwb/UwbRangingParams.md)? | getUwbRangingParams Returns the UWB ranging parameters, if applicable. |
| --- | --- |
| [WifiPdRangingParams](../android/ranging/wifi/pd/WifiPdRangingParams.md)? | getWifiPdRangingParams Returns the Wi-Fi PD ranging parameters, if applicable. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RawRangingDevice](RawRangingDevice.md)!\> | `https://developer.android.com/reference/kotlin/android/ranging/raw/RawRangingDevice#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### UPDATE_RATE_FREQUENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_RATE_FREQUENT: Int
```

Frequent ranging interval.

- UWB - 96 milliseconds for config id `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams.html#CONFIG_PROVISIONED_UNICAST_DS_TWR_VERY_FAST:kotlin.Int`, 120 milliseconds otherwise. See getSupportedRangingUpdateRates to verify Frequent update rate is supported.
- BLE RSSI - 500 milliseconds.
- BLE CS - 100 milliseconds.
- WiFi Rtt - 128 milliseconds if hasPeriodicRangingHardwareFeature is true, 256 milliseconds otherwise.
- WiFi PD - 128 milliseconds.

<br />

 Value: 3

### UPDATE_RATE_INFREQUENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_RATE_INFREQUENT: Int
```

Infrequent ranging interval.

- UWB - 600 milliseconds.
- BLE RSSI - 3 seconds.
- BLE CS - 5 seconds.
- WiFi Rtt - 8192 milliseconds otherwise.
- WiFi PD - 512 milliseconds.

<br />

 Value: 2

### UPDATE_RATE_NORMAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_RATE_NORMAL: Int
```

Normal ranging interval (Default).

- UWB - 200 milliseconds for config ids getConfigId with multicast ranging, 240 milliseconds for unicast.
- BLE RSSI - 1 second.
- BLE CS - 200 ms.
- WiFi Rtt - 256 milliseconds if hasPeriodicRangingHardwareFeature is true, 512 milliseconds otherwise.
- WiFi PD - 256 milliseconds.

<br />

 Value: 1

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getBleRssiRangingParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBleRssiRangingParams(): BleRssiRangingParams?
```

Returns the BLE rssi ranging parameters, if applicable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/ble/rssi/BleRssiRangingParams.html#?` | the `https://developer.android.com/reference/kotlin/android/ranging/ble/rssi/BleRssiRangingParams.html#`, or `null` if not set. |

### getCsRangingParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCsRangingParams(): BleCsRangingParams?
```

Returns the CS ranging parameters, if applicable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/ble/cs/BleCsRangingParams.html#?` | the `https://developer.android.com/reference/kotlin/android/ranging/ble/cs/BleCsRangingParams.html#`, or `null` if not set. |

### getDlTdoaRangingParams

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDlTdoaRangingParams(): DlTdoaRangingParams?
```

Returns the DL-TDOA ranging parameters, if applicable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/uwb/DlTdoaRangingParams.html#?` | the `https://developer.android.com/reference/kotlin/android/ranging/uwb/DlTdoaRangingParams.html#`, or `null` if not set. |

### getRangingDevice

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRangingDevice(): RangingDevice
```

Returns the `https://developer.android.com/reference/kotlin/android/ranging/RangingDevice.html#` associated with this instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/RangingDevice.html#` | the ranging device. This value cannot be `null`. |

### getRangingIntervalValues

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRangingIntervalValues(): MutableMap<Int!, Duration!>
```

Returns a map of ranging technologies to their corresponding ranging interval durations for available ranging technologies parameters.

The duration for each technology is determined by its configured android.ranging.raw.RawRangingDevice.RangingUpdateRate and, in some cases, technology-specific parameters like getConfigId for UWB.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://developer.android.com/reference/kotlin/java/time/Duration.html#!>` | A non-null, possibly empty, map where keys are RangingTechnology integers and values are the calculated `https://developer.android.com/reference/kotlin/java/time/Duration.html#` for that technology's ranging interval. |

### getRttRangingParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRttRangingParams(): RttRangingParams?
```

Returns the RTT ranging parameters, if applicable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/wifi/rtt/RttRangingParams.html#?` | the `https://developer.android.com/reference/kotlin/android/ranging/wifi/rtt/RttRangingParams.html#`, or `null` if not set. |

### getRttStationRangingParams

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRttStationRangingParams(): RttStationRangingParams?
```

Returns the Wi-Fi STA-AP ranging parameters, if applicable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/wifi/rtt/RttStationRangingParams.html#?` | the `https://developer.android.com/reference/kotlin/android/ranging/wifi/rtt/RttStationRangingParams.html#`, or `null` if not set. |

### getUwbRangingParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUwbRangingParams(): UwbRangingParams?
```

Returns the UWB ranging parameters, if applicable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams.html#?` | the `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams.html#`, or `null` if not set. |

### getWifiPdRangingParams

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWifiPdRangingParams(): WifiPdRangingParams?
```

Returns the Wi-Fi PD ranging parameters, if applicable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/wifi/pd/WifiPdRangingParams.html#?` | the `https://developer.android.com/reference/kotlin/android/ranging/wifi/pd/WifiPdRangingParams.html#`, or `null` if not set. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<RawRangingDevice!>
```
