# WifiAvailableChannel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiAvailableChannel

Kotlin| [Java](../android/net/wifi/WifiAvailableChannel.md) 
| --- | --- |

```
class WifiAvailableChannel : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.WifiAvailableChannel](../android/net/wifi/WifiAvailableChannel.md) |

Contains information about a Wifi channel and bitmask of Wifi operational modes allowed on that channel. Use [WifiManager.getAllowedChannels(int, int)](../android/net/wifi/WifiManager.md))to retrieve the list of channels filtered by regulatory constraints. Use [WifiManager.getUsableChannels(int, int)](../android/net/wifi/WifiManager.md))to retrieve the list of channels filtered by regulatory and dynamic constraints like concurrency and interference due to other radios.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_MODE_SAP](../android/net/wifi/WifiAvailableChannel.md) Wifi SoftAp (Mobile Hotspot) operational mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_MODE_STA](../android/net/wifi/WifiAvailableChannel.md) Wifi Infrastructure client (STA) operational mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_MODE_TDLS](../android/net/wifi/WifiAvailableChannel.md) Wifi Tunneled Direct Link Setup (TDLS) operational mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_MODE_WIFI_AWARE](../android/net/wifi/WifiAvailableChannel.md) Wifi Aware (NAN) operational mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_MODE_WIFI_DIRECT_CLI](../android/net/wifi/WifiAvailableChannel.md) Wifi Direct client (CLI) operational mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_MODE_WIFI_DIRECT_GO](../android/net/wifi/WifiAvailableChannel.md) Wifi Direct Group Owner (GO) operational mode. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiAvailableChannel](../android/net/wifi/WifiAvailableChannel.md))`(`freq:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `opModes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/wifi/WifiAvailableChannel.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/wifi/WifiAvailableChannel.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelWidth](../android/net/wifi/WifiAvailableChannel.md))`()` Get the channel bandwidth, which indicates the amount of frequency spectrum allocated for data transmission within a channel. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFrequencyMhz](../android/net/wifi/WifiAvailableChannel.md))`()` Get the channel frequency in MHz. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOperationalModes](../android/net/wifi/WifiAvailableChannel.md))`()` Get the operational modes allowed on a channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/wifi/WifiAvailableChannel.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/wifi/WifiAvailableChannel.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/wifi/WifiAvailableChannel.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiAvailableChannel](../android/net/wifi/WifiAvailableChannel.md)!\> | [CREATOR](../android/net/wifi/WifiAvailableChannel.md) <br /> |

## Constants

### OP_MODE_SAP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_MODE_SAP: Int
```

Wifi SoftAp (Mobile Hotspot) operational mode. 

 Value: 2

### OP_MODE_STA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_MODE_STA: Int
```

Wifi Infrastructure client (STA) operational mode. 

 Value: 1

### OP_MODE_TDLS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_MODE_TDLS: Int
```

Wifi Tunneled Direct Link Setup (TDLS) operational mode. 

 Value: 32

### OP_MODE_WIFI_AWARE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_MODE_WIFI_AWARE: Int
```

Wifi Aware (NAN) operational mode. 

 Value: 16

### OP_MODE_WIFI_DIRECT_CLI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_MODE_WIFI_DIRECT_CLI: Int
```

Wifi Direct client (CLI) operational mode. 

 Value: 4

### OP_MODE_WIFI_DIRECT_GO

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_MODE_WIFI_DIRECT_GO: Int
```

Wifi Direct Group Owner (GO) operational mode. 

 Value: 8

## Public constructors

### WifiAvailableChannel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiAvailableChannel(
    freq: Int, 
    opModes: Int)
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `opModes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.net.wifi.WifiAvailableChannel#OP_MODE_STA](../android/net/wifi/WifiAvailableChannel.md), [android.net.wifi.WifiAvailableChannel#OP_MODE_SAP](../android/net/wifi/WifiAvailableChannel.md), [android.net.wifi.WifiAvailableChannel#OP_MODE_WIFI_DIRECT_CLI](../android/net/wifi/WifiAvailableChannel.md), [android.net.wifi.WifiAvailableChannel#OP_MODE_WIFI_DIRECT_GO](../android/net/wifi/WifiAvailableChannel.md), [android.net.wifi.WifiAvailableChannel#OP_MODE_WIFI_AWARE](../android/net/wifi/WifiAvailableChannel.md), and [android.net.wifi.WifiAvailableChannel#OP_MODE_TDLS](../android/net/wifi/WifiAvailableChannel.md) |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getChannelWidth

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelWidth(): Int
```

Get the channel bandwidth, which indicates the amount of frequency spectrum allocated for data transmission within a channel.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the bandwidth representation of the Wi-Fi channel from [ScanResult.CHANNEL_WIDTH_20MHZ](../android/net/wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_40MHZ](../android/net/wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_80MHZ](../android/net/wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_160MHZ](../android/net/wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_80MHZ_PLUS_MHZ](../android/net/wifi/ScanResult.md) or [ScanResult.CHANNEL_WIDTH_320MHZ](../android/net/wifi/ScanResult.md). Value is [android.net.wifi.ScanResult#CHANNEL_WIDTH_20MHZ](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#CHANNEL_WIDTH_40MHZ](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#CHANNEL_WIDTH_160MHZ](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ_PLUS_MHZ](../android/net/wifi/ScanResult.md), or [android.net.wifi.ScanResult#CHANNEL_WIDTH_320MHZ](../android/net/wifi/ScanResult.md) |

### getFrequencyMhz

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrequencyMhz(): Int
```

Get the channel frequency in MHz. 

### getOperationalModes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOperationalModes(): Int
```

Get the operational modes allowed on a channel.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.net.wifi.WifiAvailableChannel#OP_MODE_STA](../android/net/wifi/WifiAvailableChannel.md), [android.net.wifi.WifiAvailableChannel#OP_MODE_SAP](../android/net/wifi/WifiAvailableChannel.md), [android.net.wifi.WifiAvailableChannel#OP_MODE_WIFI_DIRECT_CLI](../android/net/wifi/WifiAvailableChannel.md), [android.net.wifi.WifiAvailableChannel#OP_MODE_WIFI_DIRECT_GO](../android/net/wifi/WifiAvailableChannel.md), [android.net.wifi.WifiAvailableChannel#OP_MODE_WIFI_AWARE](../android/net/wifi/WifiAvailableChannel.md), and [android.net.wifi.WifiAvailableChannel#OP_MODE_TDLS](../android/net/wifi/WifiAvailableChannel.md) |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiAvailableChannel!>
```
