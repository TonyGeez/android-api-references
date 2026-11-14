# ScanResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

ScanResult
==========

Kotlin | [Java](/reference/android/net/wifi/ScanResult "View this page in Java") 

```
class ScanResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.ScanResult](#) |

Describes information about a detected access point. In addition to the attributes described here, the supplicant keeps track of `quality`, `noise`, and `maxbitrate` attributes, but does not currently report them to external clients.

Summary
-------

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------|
| | [InformationElement](/reference/kotlin/android/net/wifi/ScanResult.InformationElement) information elements from beacon. |

| Constants ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_WIDTH_160MHZ](#CHANNEL_WIDTH_160MHZ:kotlin.Int) AP Channel bandwidth is 160 MHZ |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_WIDTH_20MHZ](#CHANNEL_WIDTH_20MHZ:kotlin.Int) AP Channel bandwidth is 20 MHZ |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_WIDTH_320MHZ](#CHANNEL_WIDTH_320MHZ:kotlin.Int) AP Channel bandwidth is 320 MHZ |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_WIDTH_40MHZ](#CHANNEL_WIDTH_40MHZ:kotlin.Int) AP Channel bandwidth is 40 MHZ |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_WIDTH_80MHZ](#CHANNEL_WIDTH_80MHZ:kotlin.Int) AP Channel bandwidth is 80 MHZ |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_WIDTH_80MHZ_PLUS_MHZ](#CHANNEL_WIDTH_80MHZ_PLUS_MHZ:kotlin.Int) AP Channel bandwidth is 160 MHZ, but 80MHZ + 80MHZ |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREAMBLE_EHT](#PREAMBLE_EHT:kotlin.Int) Preamble type: EHT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREAMBLE_HE](#PREAMBLE_HE:kotlin.Int) Preamble type: HE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREAMBLE_HT](#PREAMBLE_HT:kotlin.Int) Preamble type: HT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREAMBLE_LEGACY](#PREAMBLE_LEGACY:kotlin.Int) Preamble type: Legacy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREAMBLE_VHT](#PREAMBLE_VHT:kotlin.Int) Preamble type: VHT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNSPECIFIED](#UNSPECIFIED:kotlin.Int) The unspecified value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_BAND_24_GHZ](#WIFI_BAND_24_GHZ:kotlin.Int) Wi-Fi 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_BAND_5_GHZ](#WIFI_BAND_5_GHZ:kotlin.Int) Wi-Fi 5 GHz band. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_BAND_60_GHZ](#WIFI_BAND_60_GHZ:kotlin.Int) Wi-Fi 60 GHz band. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_BAND_6_GHZ](#WIFI_BAND_6_GHZ:kotlin.Int) Wi-Fi 6 GHz band. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STANDARD_11AC](#WIFI_STANDARD_11AC:kotlin.Int) Wi-Fi 802. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STANDARD_11AD](#WIFI_STANDARD_11AD:kotlin.Int) Wi-Fi 802. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STANDARD_11AX](#WIFI_STANDARD_11AX:kotlin.Int) Wi-Fi 802. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STANDARD_11BE](#WIFI_STANDARD_11BE:kotlin.Int) Wi-Fi 802. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STANDARD_11N](#WIFI_STANDARD_11N:kotlin.Int) Wi-Fi 802. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STANDARD_LEGACY](#WIFI_STANDARD_LEGACY:kotlin.Int) Wi-Fi 802. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_STANDARD_UNKNOWN](#WIFI_STANDARD_UNKNOWN:kotlin.Int) Wi-Fi unknown standard |

| Inherited constants ||
|---|---|
| From class [Parcelable](../../os/Parcelable.html#) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../../os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](../../os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../../os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](../../os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------|---|
| [ScanResult](#ScanResult())`()` Construct an empty scan result. |
| [ScanResult](#ScanResult(android.net.wifi.ScanResult))`(`source:` ` [ScanResult](#)`)` copy constructor |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [convertChannelToFrequencyMhzIfSupported](#convertChannelToFrequencyMhzIfSupported(kotlin.Int,%20kotlin.Int))`(`channel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Utility function to convert Wi-Fi channel number to frequency in MHz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [convertFrequencyMhzToChannelIfSupported](#convertFrequencyMhzToChannelIfSupported(kotlin.Int))`(`freqMhz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Utility function to convert frequency in MHz to channel number. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](#describeContents())`()` Implement the Parcelable interface {@hide} |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MloLink](/reference/kotlin/android/net/wifi/MloLink)!\> | [getAffiliatedMloLinks](#getAffiliatedMloLinks())`()` Return the Multi-Link Operation (MLO) affiliated Links for Wi-Fi 7 access points. |
| [MacAddress](../MacAddress.html#)? | [getApMldMacAddress](#getApMldMacAddress())`()` Return the access point Multi-Link Device (MLD) MAC Address for Wi-Fi 7 access points. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getApMloLinkId](#getApMloLinkId())`()` Return the access point Multi-Link Operation (MLO) link-id for Wi-Fi 7 access points. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult.InformationElement](/reference/kotlin/android/net/wifi/ScanResult.InformationElement)!\> | [getInformationElements](#getInformationElements())`()` Get all information elements found in the beacon. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getSecurityTypes](#getSecurityTypes())`()` Get all the security types supported by this ScanResult. |
| [WifiSsid](/reference/kotlin/android/net/wifi/WifiSsid)? | [getWifiSsid](#getWifiSsid())`()` The SSID of the access point. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWifiStandard](#getWifiStandard())`()` return the AP wifi standard. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [is80211azNtbResponder](#is80211azNtbResponder())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [is80211mcResponder](#is80211mcResponder())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPasspointNetwork](#isPasspointNetwork())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRangingFrameProtectionRequired](#isRangingFrameProtectionRequired())`()` Returns whether the AP requires frame protection for ranging measurement. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSecureHeLtfSupported](#isSecureHeLtfSupported())`()` Returns whether the AP supports secure HE-LTF for ranging measurement. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTwtResponder](#isTwtResponder())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](../../os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface {@hide} |

| Properties ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [BSSID](#BSSID:kotlin.String) The address of the access point. |
| static [Parcelable.Creator](../../os/Parcelable.Creator.html#)\< [ScanResult](#)!\> | [CREATOR](#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [SSID](#SSID:kotlin.String) The network name. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [capabilities](#capabilities:kotlin.String) Describes the authentication, key management, and encryption schemes supported by the access point. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [centerFreq0](#centerFreq0:kotlin.Int) Not used if the AP bandwidth is 20 MHz If the AP use 40, 80, 160 or 320MHz, this is the center frequency (in MHz) if the AP use 80 + 80 MHz, this is the center frequency of the first segment (in MHz) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [centerFreq1](#centerFreq1:kotlin.Int) Only used if the AP bandwidth is 80 + 80 MHz if the AP use 80 + 80 MHz, this is the center frequency of the second segment (in MHz) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [channelWidth](#channelWidth:kotlin.Int) AP Channel bandwidth; one of [CHANNEL_WIDTH_20MHZ](#CHANNEL_WIDTH_20MHZ:kotlin.Int), [CHANNEL_WIDTH_40MHZ](#CHANNEL_WIDTH_40MHZ:kotlin.Int), [CHANNEL_WIDTH_80MHZ](#CHANNEL_WIDTH_80MHZ:kotlin.Int), [CHANNEL_WIDTH_160MHZ](#CHANNEL_WIDTH_160MHZ:kotlin.Int), [CHANNEL_WIDTH_320MHZ](#CHANNEL_WIDTH_320MHZ:kotlin.Int), or [CHANNEL_WIDTH_80MHZ_PLUS_MHZ](#CHANNEL_WIDTH_80MHZ_PLUS_MHZ:kotlin.Int), or [CHANNEL_WIDTH_320MHZ](#CHANNEL_WIDTH_320MHZ:kotlin.Int) Value is [android.net.wifi.ScanResult#CHANNEL_WIDTH_20MHZ](#CHANNEL_WIDTH_20MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_40MHZ](#CHANNEL_WIDTH_40MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ](#CHANNEL_WIDTH_80MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_160MHZ](#CHANNEL_WIDTH_160MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ_PLUS_MHZ](#CHANNEL_WIDTH_80MHZ_PLUS_MHZ:kotlin.Int), or [android.net.wifi.ScanResult#CHANNEL_WIDTH_320MHZ](#CHANNEL_WIDTH_320MHZ:kotlin.Int) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [frequency](#frequency:kotlin.Int) The center frequency of the primary 20 MHz frequency (in MHz) of the channel over which the client is communicating with the access point. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [level](#level:kotlin.Int) The detected signal level in dBm, also known as the RSSI. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [operatorFriendlyName](#operatorFriendlyName:kotlin.CharSequence) Indicates Passpoint operator name published by access point. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [timestamp](#timestamp:kotlin.Long) timestamp in microseconds (since boot) when this result was last seen. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [venueName](#venueName:kotlin.CharSequence) Indicates venue name (such as 'San Francisco Airport') published by access point; only available on Passpoint network and if published by access point. |

Constants
---------

### CHANNEL_WIDTH_160MHZ

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_WIDTH_160MHZ: Int
```

AP Channel bandwidth is 160 MHZ 

 Value: 3

### CHANNEL_WIDTH_20MHZ

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_WIDTH_20MHZ: Int
```

AP Channel bandwidth is 20 MHZ 

 Value: 0

### CHANNEL_WIDTH_320MHZ

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_WIDTH_320MHZ: Int
```

AP Channel bandwidth is 320 MHZ 

 Value: 5

### CHANNEL_WIDTH_40MHZ

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_WIDTH_40MHZ: Int
```

AP Channel bandwidth is 40 MHZ 

 Value: 1

### CHANNEL_WIDTH_80MHZ

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_WIDTH_80MHZ: Int
```

AP Channel bandwidth is 80 MHZ 

 Value: 2

### CHANNEL_WIDTH_80MHZ_PLUS_MHZ

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_WIDTH_80MHZ_PLUS_MHZ: Int
```

AP Channel bandwidth is 160 MHZ, but 80MHZ + 80MHZ 

 Value: 4

### PREAMBLE_EHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREAMBLE_EHT: Int
```

Preamble type: EHT. 

 Value: 4

### PREAMBLE_HE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREAMBLE_HE: Int
```

Preamble type: HE. 

 Value: 3

### PREAMBLE_HT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREAMBLE_HT: Int
```

Preamble type: HT. 

 Value: 1

### PREAMBLE_LEGACY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREAMBLE_LEGACY: Int
```

Preamble type: Legacy. 

 Value: 0

### PREAMBLE_VHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREAMBLE_VHT: Int
```

Preamble type: VHT. 

 Value: 2

### UNSPECIFIED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNSPECIFIED: Int
```

The unspecified value. 

 Value: -1

### WIFI_BAND_24_GHZ

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_BAND_24_GHZ: Int
```

Wi-Fi 2.4 GHz band. 

 Value: 1

### WIFI_BAND_5_GHZ

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_BAND_5_GHZ: Int
```

Wi-Fi 5 GHz band. 

 Value: 2

### WIFI_BAND_60_GHZ

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_BAND_60_GHZ: Int
```

Wi-Fi 60 GHz band. 

 Value: 16

### WIFI_BAND_6_GHZ

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_BAND_6_GHZ: Int
```

Wi-Fi 6 GHz band. 

 Value: 8

### WIFI_STANDARD_11AC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_STANDARD_11AC: Int
```

Wi-Fi 802.11ac 

 Value: 5

### WIFI_STANDARD_11AD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_STANDARD_11AD: Int
```

Wi-Fi 802.11ad 

 Value: 7

### WIFI_STANDARD_11AX

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_STANDARD_11AX: Int
```

Wi-Fi 802.11ax 

 Value: 6

### WIFI_STANDARD_11BE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_STANDARD_11BE: Int
```

Wi-Fi 802.11be 

 Value: 8

### WIFI_STANDARD_11N

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_STANDARD_11N: Int
```

Wi-Fi 802.11n 

 Value: 4

### WIFI_STANDARD_LEGACY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_STANDARD_LEGACY: Int
```

Wi-Fi 802.11a/b/g 

 Value: 1

### WIFI_STANDARD_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_STANDARD_UNKNOWN: Int
```

Wi-Fi unknown standard 

 Value: 0

Public constructors
-------------------

### ScanResult

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScanResult()
```

Construct an empty scan result. 

### ScanResult

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScanResult(source: ScanResult)
```

copy constructor

| Parameters ||
|----------|-----------------------------------------------|
| `source` | [ScanResult](#): This value cannot be `null`. |

Public methods
--------------

### convertChannelToFrequencyMhzIfSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun convertChannelToFrequencyMhzIfSupported(
    channel: Int, 
    band: Int
): Int
```

Utility function to convert Wi-Fi channel number to frequency in MHz. Reference the Wi-Fi channel numbering and the channelization in IEEE 802.11-2016 specifications, section 17.3.8.4.2, 17.3.8.4.3 and Table 15-6. See also [convertFrequencyMhzToChannelIfSupported(int)](#convertFrequencyMhzToChannelIfSupported(kotlin.Int)).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `channel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number to convert. |
| `band` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of channel to convert. One of the following bands: [WIFI_BAND_24_GHZ](#WIFI_BAND_24_GHZ:kotlin.Int), [WIFI_BAND_5_GHZ](#WIFI_BAND_5_GHZ:kotlin.Int), [WIFI_BAND_6_GHZ](#WIFI_BAND_6_GHZ:kotlin.Int), [WIFI_BAND_60_GHZ](#WIFI_BAND_60_GHZ:kotlin.Int). Value is [android.net.wifi.ScanResult#UNSPECIFIED](#UNSPECIFIED:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_24_GHZ](#WIFI_BAND_24_GHZ:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_5_GHZ](#WIFI_BAND_5_GHZ:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_6_GHZ](#WIFI_BAND_6_GHZ:kotlin.Int), or [android.net.wifi.ScanResult#WIFI_BAND_60_GHZ](#WIFI_BAND_60_GHZ:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | center frequency in Mhz of the channel, [UNSPECIFIED](#UNSPECIFIED:kotlin.Int) if no match |

### convertFrequencyMhzToChannelIfSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun convertFrequencyMhzToChannelIfSupported(freqMhz: Int): Int
```

Utility function to convert frequency in MHz to channel number. See also [convertChannelToFrequencyMhzIfSupported(int,int)](#convertChannelToFrequencyMhzIfSupported(kotlin.Int,%20kotlin.Int)).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------|
| `freqMhz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): frequency in MHz |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | channel number associated with given frequency, [UNSPECIFIED](#UNSPECIFIED:kotlin.Int) if no match |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface {@hide}

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../../os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAffiliatedMloLinks

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAffiliatedMloLinks(): MutableList<MloLink!>
```

Return the Multi-Link Operation (MLO) affiliated Links for Wi-Fi 7 access points. i.e. when [getWifiStandard()](#getWifiStandard()) returns [WIFI_STANDARD_11BE](#WIFI_STANDARD_11BE:kotlin.Int).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MloLink](/reference/kotlin/android/net/wifi/MloLink)!> | List of affiliated MLO links, or an empty list if access point is not Wi-Fi 7 This value cannot be `null`. |

### getApMldMacAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getApMldMacAddress(): MacAddress?
```

Return the access point Multi-Link Device (MLD) MAC Address for Wi-Fi 7 access points. i.e. [getWifiStandard()](#getWifiStandard()) returns [WIFI_STANDARD_11BE](#WIFI_STANDARD_11BE:kotlin.Int).

| Return ||
|------------------------------------|-------------------------------------------------------------------------------------|
| [MacAddress](../MacAddress.html#)? | MLD MAC Address for access point if exists (Wi-Fi 7 access points), null otherwise. |

### getApMloLinkId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getApMloLinkId(): Int
```

Return the access point Multi-Link Operation (MLO) link-id for Wi-Fi 7 access points. i.e. when [getWifiStandard()](#getWifiStandard()) returns [WIFI_STANDARD_11BE](#WIFI_STANDARD_11BE:kotlin.Int), otherwise return [MloLink.INVALID_MLO_LINK_ID](/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int). Valid values are 0-15 as described in IEEE 802.11be Specification, section 9.4.2.295b.2.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MloLink.INVALID_MLO_LINK_ID](/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int) or a valid value (0-15). Value is between [android.net.wifi.MloLink#INVALID_MLO_LINK_ID](/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int) and android.net.wifi.MloLink#MAX_MLO_LINK_ID inclusive |

### getInformationElements

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInformationElements(): MutableList<ScanResult.InformationElement!>
```

Get all information elements found in the beacon.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ScanResult.InformationElement](/reference/kotlin/android/net/wifi/ScanResult.InformationElement)!> | This value cannot be `null`. |

### getSecurityTypes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecurityTypes(): IntArray
```

Get all the security types supported by this ScanResult.

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | array of `WifiInfo#SECURITY_TYPE_*`. This value cannot be `null`. Value is [android.net.wifi.WifiInfo#SECURITY_TYPE_UNKNOWN](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_UNKNOWN:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_OPEN](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_OPEN:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_WEP](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WEP:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_PSK](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PSK:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_SAE](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_SAE:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_OWE](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_OWE:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_WAPI_PSK](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WAPI_PSK:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_WAPI_CERT](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WAPI_CERT:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_PASSPOINT_R1_R2](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PASSPOINT_R1_R2:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_PASSPOINT_R3](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PASSPOINT_R3:kotlin.Int), or [android.net.wifi.WifiInfo#SECURITY_TYPE_DPP](/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_DPP:kotlin.Int) |

### getWifiSsid

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWifiSsid(): WifiSsid?
```

The SSID of the access point.

| Return ||
|----------------------------------------------------------|---------------------------|
| [WifiSsid](/reference/kotlin/android/net/wifi/WifiSsid)? | This value may be `null`. |

### getWifiStandard

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWifiStandard(): Int
```

return the AP wifi standard.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.ScanResult#WIFI_STANDARD_UNKNOWN](#WIFI_STANDARD_UNKNOWN:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_LEGACY](#WIFI_STANDARD_LEGACY:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_11N](#WIFI_STANDARD_11N:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_11AC](#WIFI_STANDARD_11AC:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_11AX](#WIFI_STANDARD_11AX:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_11AD](#WIFI_STANDARD_11AD:kotlin.Int), or [android.net.wifi.ScanResult#WIFI_STANDARD_11BE](#WIFI_STANDARD_11BE:kotlin.Int) |

### is80211azNtbResponder

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun is80211azNtbResponder(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether AP is a IEEE802.11az Non-Trigger based Ranging Responder. |

### is80211mcResponder

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun is80211mcResponder(): Boolean
```  

### isPasspointNetwork

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPasspointNetwork(): Boolean
```  

### isRangingFrameProtectionRequired

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRangingFrameProtectionRequired(): Boolean
```

Returns whether the AP requires frame protection for ranging measurement. Ranging frame protection in IEEE 802.11az, also known as URNM-MFPR (Unassociated Range Negotiation and Measurement Management Frame Protection Required), is a security policy that dictates whether ranging frames are required to be protected even without a formal association between the Initiating STA (ISTA) and Responding STA (RSTA) 

### isSecureHeLtfSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSecureHeLtfSupported(): Boolean
```

Returns whether the AP supports secure HE-LTF for ranging measurement. Secure HE-LTF (High Efficiency Long Training Field), is a security enhancement for the HE PHY (High Efficiency Physical Layer) that aims to protect ranging measurements by using randomized HE-LTF sequences. This prevents attackers from exploiting predictable HE-LTF patterns. IEEE 802.11az adds secure HE-LTF support in Extended RSN capabilities. 

### isTwtResponder

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isTwtResponder(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether AP is Target Wake Time (TWT) Responder. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface {@hide}

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../../os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../../os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../../os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

Properties
----------

### BSSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var BSSID: String!
```

The address of the access point. 

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ScanResult!>
```

Implement the Parcelable interface 

### SSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var SSID: String!
```

**Deprecated:** *Use [getWifiSsid()](#getWifiSsid()) instead.*

The network name. 

### capabilities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var capabilities: String!
```

Describes the authentication, key management, and encryption schemes supported by the access point. 

### centerFreq0

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var centerFreq0: Int
```

Not used if the AP bandwidth is 20 MHz If the AP use 40, 80, 160 or 320MHz, this is the center frequency (in MHz) if the AP use 80 + 80 MHz, this is the center frequency of the first segment (in MHz) 

### centerFreq1

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var centerFreq1: Int
```

Only used if the AP bandwidth is 80 + 80 MHz if the AP use 80 + 80 MHz, this is the center frequency of the second segment (in MHz) 

### channelWidth

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var channelWidth: Int
```

AP Channel bandwidth; one of [CHANNEL_WIDTH_20MHZ](#CHANNEL_WIDTH_20MHZ:kotlin.Int), [CHANNEL_WIDTH_40MHZ](#CHANNEL_WIDTH_40MHZ:kotlin.Int), [CHANNEL_WIDTH_80MHZ](#CHANNEL_WIDTH_80MHZ:kotlin.Int), [CHANNEL_WIDTH_160MHZ](#CHANNEL_WIDTH_160MHZ:kotlin.Int), [CHANNEL_WIDTH_320MHZ](#CHANNEL_WIDTH_320MHZ:kotlin.Int), or [CHANNEL_WIDTH_80MHZ_PLUS_MHZ](#CHANNEL_WIDTH_80MHZ_PLUS_MHZ:kotlin.Int), or [CHANNEL_WIDTH_320MHZ](#CHANNEL_WIDTH_320MHZ:kotlin.Int) 
Value is [android.net.wifi.ScanResult#CHANNEL_WIDTH_20MHZ](#CHANNEL_WIDTH_20MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_40MHZ](#CHANNEL_WIDTH_40MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ](#CHANNEL_WIDTH_80MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_160MHZ](#CHANNEL_WIDTH_160MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ_PLUS_MHZ](#CHANNEL_WIDTH_80MHZ_PLUS_MHZ:kotlin.Int), or [android.net.wifi.ScanResult#CHANNEL_WIDTH_320MHZ](#CHANNEL_WIDTH_320MHZ:kotlin.Int) 

### frequency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var frequency: Int
```

The center frequency of the primary 20 MHz frequency (in MHz) of the channel over which the client is communicating with the access point. 

### level

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var level: Int
```

The detected signal level in dBm, also known as the RSSI.

Use android.net.wifi.WifiManager#calculateSignalLevel to convert this number into an absolute signal level which can be displayed to a user. 

### operatorFriendlyName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var operatorFriendlyName: CharSequence!
```

**Deprecated:** *- Use [WifiInfo.getPasspointProviderFriendlyName()](/reference/kotlin/android/net/wifi/WifiInfo#getPasspointProviderFriendlyName())*

Indicates Passpoint operator name published by access point. 

### timestamp

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var timestamp: Long
```

timestamp in microseconds (since boot) when this result was last seen. 

### venueName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var venueName: CharSequence!
```

**Deprecated:** *- This information is not provided*

Indicates venue name (such as 'San Francisco Airport') published by access point; only available on Passpoint network and if published by access point.
