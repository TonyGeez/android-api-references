# SoftApConfiguration

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SoftApConfiguration

Kotlin| [Java](SoftApConfiguration.md) 
| --- | --- |

```
class SoftApConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.SoftApConfiguration](SoftApConfiguration.md) |

Configuration for a soft access point (a.k.a. Soft AP, SAP, Hotspot).

This is input for the framework provided by a client app, i.e. it exposes knobs to instruct the framework how it should configure a hotspot.

System apps can use this to configure a tethered hotspot or local-only hotspot.

Instances of this class are immutable.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/wifi/SoftApConfiguration.Builder.md) Builds a [SoftApConfiguration](SoftApConfiguration.md), which allows an app to configure various aspects of a Soft AP. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BAND_2GHZ](SoftApConfiguration.md) 2GHz band. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BAND_5GHZ](SoftApConfiguration.md) 5GHz band. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BAND_60GHZ](SoftApConfiguration.md) 60GHz band. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BAND_6GHZ](SoftApConfiguration.md) 6GHz band. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OPEN](SoftApConfiguration.md) THe definition of security type OPEN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WPA2_PSK](SoftApConfiguration.md) The definition of security type WPA2-PSK. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WPA3_OWE](SoftApConfiguration.md) The definition of security type WPA3-OWE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WPA3_OWE_TRANSITION](SoftApConfiguration.md) The definition of security type WPA3-OWE Transition. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WPA3_SAE](SoftApConfiguration.md) The definition of security type WPA3-SAE. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WPA3_SAE_TRANSITION](SoftApConfiguration.md) The definition of security type WPA3-SAE Transition mode. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SoftApConfiguration.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](SoftApConfiguration.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MacAddress](../android.net/MacAddress.md)? | [getBssid](SoftApConfiguration.md))`()` Returns MAC address set to be BSSID for the AP. |
| --- | --- |
| [SparseIntArray](../android.util/SparseIntArray.md) | [getChannels](SoftApConfiguration.md))`()` Returns SparseIntArray (key:`BandType`, value: channel) that consists of the configured bands and channels for the AP(s). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPassphrase](SoftApConfiguration.md))`()` Returns String set to be passphrase for current AP. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecurityType](SoftApConfiguration.md))`()` Get security type params which depends on which security passphrase to set. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSsid](SoftApConfiguration.md))`()` Return the UTF-8 String set to be the SSID for the AP. |
| [WifiSsid](WifiSsid.md)? | [getWifiSsid](SoftApConfiguration.md))`()` Return WifiSsid set to be the SSID for the AP. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](SoftApConfiguration.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHiddenSsid](SoftApConfiguration.md))`()` Returns Boolean set to be indicate hidden (true: doesn't broadcast its SSID) or not (false: broadcasts its SSID) for the AP. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SoftApConfiguration.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SoftApConfiguration.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SoftApConfiguration](SoftApConfiguration.md)!\> | [CREATOR](SoftApConfiguration.md) <br /> |

## Constants

### BAND_2GHZ

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BAND_2GHZ: Int
```

2GHz band. 

 Value: 1

### BAND_5GHZ

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BAND_5GHZ: Int
```

5GHz band. 

 Value: 2

### BAND_60GHZ

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BAND_60GHZ: Int
```

60GHz band. 

 Value: 8

### BAND_6GHZ

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BAND_6GHZ: Int
```

6GHz band. 

 Value: 4

### SECURITY_TYPE_OPEN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_OPEN: Int
```

THe definition of security type OPEN. 

 Value: 0

### SECURITY_TYPE_WPA2_PSK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WPA2_PSK: Int
```

The definition of security type WPA2-PSK. 

 Value: 1

### SECURITY_TYPE_WPA3_OWE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WPA3_OWE: Int
```

The definition of security type WPA3-OWE. 

 Value: 5

### SECURITY_TYPE_WPA3_OWE_TRANSITION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WPA3_OWE_TRANSITION: Int
```

The definition of security type WPA3-OWE Transition. 

 Value: 4

### SECURITY_TYPE_WPA3_SAE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WPA3_SAE: Int
```

The definition of security type WPA3-SAE. 

 Value: 3

### SECURITY_TYPE_WPA3_SAE_TRANSITION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WPA3_SAE_TRANSITION: Int
```

The definition of security type WPA3-SAE Transition mode. 

 Value: 2

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getBssid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBssid(): MacAddress?
```

Returns MAC address set to be BSSID for the AP.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------|
| [MacAddress](../android.net/MacAddress.md)? | This value may be`null`. |

### getChannels

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannels(): SparseIntArray
```

Returns SparseIntArray (key:`BandType`, value: channel) that consists of the configured bands and channels for the AP(s). The returned channel value is Wi-Fi channel numbering. Reference the Wi-Fi channel numbering and the channelization in IEEE 802.11-2016 specifications, section 17.3.8.4.2, 17.3.8.4.3 and Table 15-6. Note: return array may only include one channel when current setting is single AP mode. See also [Builder.setChannels(SparseIntArray)](../android/net/wifi/SoftApConfiguration.Builder.md)).

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------|
| [SparseIntArray](../android.util/SparseIntArray.md) | This value cannot be`null`. |

### getPassphrase

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPassphrase(): String?
```

Returns String set to be passphrase for current AP.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getSecurityType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecurityType(): Int
```

Get security type params which depends on which security passphrase to set.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | One of: [SECURITY_TYPE_OPEN](SoftApConfiguration.md), [SECURITY_TYPE_WPA2_PSK](SoftApConfiguration.md), [SECURITY_TYPE_WPA3_SAE_TRANSITION](SoftApConfiguration.md), [SECURITY_TYPE_WPA3_SAE](SoftApConfiguration.md), [SECURITY_TYPE_WPA3_OWE_TRANSITION](SoftApConfiguration.md), [SECURITY_TYPE_WPA3_OWE](SoftApConfiguration.md) Value is [android.net.wifi.SoftApConfiguration#SECURITY_TYPE_OPEN](SoftApConfiguration.md), [android.net.wifi.SoftApConfiguration#SECURITY_TYPE_WPA2_PSK](SoftApConfiguration.md), [android.net.wifi.SoftApConfiguration#SECURITY_TYPE_WPA3_SAE_TRANSITION](SoftApConfiguration.md), [android.net.wifi.SoftApConfiguration#SECURITY_TYPE_WPA3_SAE](SoftApConfiguration.md), [android.net.wifi.SoftApConfiguration#SECURITY_TYPE_WPA3_OWE_TRANSITION](SoftApConfiguration.md), or [android.net.wifi.SoftApConfiguration#SECURITY_TYPE_WPA3_OWE](SoftApConfiguration.md) |

### getSsid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSsid(): String?
```

**Deprecated:** *Use [getWifiSsid()](SoftApConfiguration.md))instead.*

Return the UTF-8 String set to be the SSID for the AP. If the SSID cannot be decoded as UTF-8, then this will return [WifiManager.UNKNOWN_SSID](WifiManager.md).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getWifiSsid

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWifiSsid(): WifiSsid?
```

Return WifiSsid set to be the SSID for the AP.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------|
| [WifiSsid](WifiSsid.md)? | This value may be`null`. |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isHiddenSsid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHiddenSsid(): Boolean
```

Returns Boolean set to be indicate hidden (true: doesn't broadcast its SSID) or not (false: broadcasts its SSID) for the AP. 

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SoftApConfiguration!>
```
