# WifiP2pUsdBasedServiceDiscoveryConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pUsdBasedServiceDiscoveryConfig

Kotlin| [Java](WifiP2pUsdBasedServiceDiscoveryConfig.md) 
| --- | --- |

```
class WifiP2pUsdBasedServiceDiscoveryConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.WifiP2pUsdBasedServiceDiscoveryConfig](WifiP2pUsdBasedServiceDiscoveryConfig.md) |

A class representing a Wi-Fi P2P USD based service discovery configuration for discovering the services.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/wifi/p2p/WifiP2pUsdBasedServiceDiscoveryConfig.Builder.md) Builder for [WifiP2pUsdBasedServiceDiscoveryConfig](WifiP2pUsdBasedServiceDiscoveryConfig.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](WifiP2pUsdBasedServiceDiscoveryConfig.md))`()` Implement the Parcelable interface |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBand](WifiP2pUsdBasedServiceDiscoveryConfig.md))`()` Get the band to scan for services. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getFrequenciesMhz](WifiP2pUsdBasedServiceDiscoveryConfig.md))`()` Get the frequencies to scan for services. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](WifiP2pUsdBasedServiceDiscoveryConfig.md))`()` Generates a string of all the defined elements. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](WifiP2pUsdBasedServiceDiscoveryConfig.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiP2pUsdBasedServiceDiscoveryConfig](WifiP2pUsdBasedServiceDiscoveryConfig.md)!\> | [CREATOR](WifiP2pUsdBasedServiceDiscoveryConfig.md) Implement the Parcelable interface |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getBand

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBand(): Int
```

Get the band to scan for services. See [Builder.setBand(int)](../android/net/wifi/p2p/WifiP2pUsdBasedServiceDiscoveryConfig.Builder.md))

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.ScanResult#UNSPECIFIED](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#WIFI_BAND_24_GHZ](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#WIFI_BAND_5_GHZ](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#WIFI_BAND_6_GHZ](../android.net.wifi/ScanResult.md), or [android.net.wifi.ScanResult#WIFI_BAND_60_GHZ](../android.net.wifi/ScanResult.md) |

### getFrequenciesMhz

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrequenciesMhz(): IntArray?
```

Get the frequencies to scan for services. See[Builder.setFrequenciesMhz(int[])](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedServiceDiscoveryConfig.Builder#setFrequenciesMhz(kotlin.IntArray))

| Return ||
|----------------------------------------------------------------------------------------|--------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | This value may be`null`. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Generates a string of all the defined elements.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a compiled string representing all elements |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiP2pUsdBasedServiceDiscoveryConfig!>
```

Implement the Parcelable interface
