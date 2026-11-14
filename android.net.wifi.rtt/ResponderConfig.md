# ResponderConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResponderConfig

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/rtt/ResponderConfig "View this page in Java") 

```
class ResponderConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.rtt.ResponderConfig](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#) |

Defines the configuration of an IEEE 802.11mc Responder. The Responder may be an Access Point (AP), a Wi-Fi Aware device, or a manually configured Responder.

A Responder configuration may be constructed from a [ScanResult](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#) or manually (with the data obtained out-of-band from a peer).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig.Builder) Builder class used to construct [ResponderConfig](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONDER_AP](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#RESPONDER_AP:kotlin.Int) Responder is an access point(AP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONDER_STA](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#RESPONDER_STA:kotlin.Int) Responder is a client device(STA). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [ResponderConfig](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#) | [fromScanResult](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#fromScanResult(android.net.wifi.ScanResult))`(`scanResult:` ` [ScanResult](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#)`)` Creates a Responder configuration from a [ScanResult](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#) corresponding to an Access Point (AP), which can be obtained from [android.net.wifi.WifiManager#getScanResults()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#getScanResults()). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCenterFreq0Mhz](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#getCenterFreq0Mhz())`()` If the Access Point (AP) bandwidth is 20 MHz, 0 MHz is returned. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCenterFreq1Mhz](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#getCenterFreq1Mhz())`()` If the Access Point (AP) bandwidth is 80 + 80 MHz, this param is not used and returns 0. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelWidth](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#getChannelWidth())`()` AP Channel bandwidth; one of [ScanResult.CHANNEL_WIDTH_20MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_20MHZ:kotlin.Int), [ScanResult.CHANNEL_WIDTH_40MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_40MHZ:kotlin.Int), [ScanResult.CHANNEL_WIDTH_80MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ:kotlin.Int), [ScanResult.CHANNEL_WIDTH_160MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_160MHZ:kotlin.Int), [CHANNEL_WIDTH_80MHZ_PLUS_MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#) or [ScanResult.CHANNEL_WIDTH_320MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_320MHZ:kotlin.Int). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFrequencyMhz](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#getFrequencyMhz())`()` <br /> |
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | [getMacAddress](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#getMacAddress())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPreamble](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#getPreamble())`()` Get the preamble type of the channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponderType](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#getResponderType())`()` Get responder type. |
| [SecureRangingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/SecureRangingConfig)? | [getSecureRangingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#getSecureRangingConfig())`()` Get secure ranging configuration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [is80211azNtbSupported](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#is80211azNtbSupported())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [is80211mcSupported](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#is80211mcSupported())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ResponderConfig](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### RESPONDER_AP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONDER_AP: Int
```

Responder is an access point(AP). 

 Value: 0

### RESPONDER_STA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONDER_STA: Int
```

Responder is a client device(STA). 

 Value: 1

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### fromScanResult

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromScanResult(scanResult: ScanResult): ResponderConfig
```

Creates a Responder configuration from a [ScanResult](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#) corresponding to an Access Point (AP), which can be obtained from [android.net.wifi.WifiManager#getScanResults()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#getScanResults()).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `scanResult` | [ScanResult](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [ResponderConfig](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#) | This value cannot be`null`. |

### getCenterFreq0Mhz

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCenterFreq0Mhz(): Int
```

If the Access Point (AP) bandwidth is 20 MHz, 0 MHz is returned. If the AP use 40, 80 or 160 MHz, this is the center frequency (in MHz). if the AP uses 80 + 80 MHz, this is the center frequency of the first segment (in MHz).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the center frequency in MHz of the first channel segment Value is 0 or greater |

### getCenterFreq1Mhz

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCenterFreq1Mhz(): Int
```

If the Access Point (AP) bandwidth is 80 + 80 MHz, this param is not used and returns 0. If the AP uses 80 + 80 MHz, this is the center frequency of the second segment in MHz.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the center frequency in MHz of the second channel segment (if used) Value is 0 or greater |

### getChannelWidth

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelWidth(): Int
```

AP Channel bandwidth; one of [ScanResult.CHANNEL_WIDTH_20MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_20MHZ:kotlin.Int), [ScanResult.CHANNEL_WIDTH_40MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_40MHZ:kotlin.Int), [ScanResult.CHANNEL_WIDTH_80MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ:kotlin.Int), [ScanResult.CHANNEL_WIDTH_160MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_160MHZ:kotlin.Int), [CHANNEL_WIDTH_80MHZ_PLUS_MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#) or [ScanResult.CHANNEL_WIDTH_320MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_320MHZ:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the bandwidth repsentation of the Wi-Fi channel Value is [android.net.wifi.ScanResult#CHANNEL_WIDTH_20MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_20MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_40MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_40MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_160MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_160MHZ:kotlin.Int), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ_PLUS_MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ_PLUS_MHZ:kotlin.Int), or [android.net.wifi.ScanResult#CHANNEL_WIDTH_320MHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_320MHZ:kotlin.Int) |

### getFrequencyMhz

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrequencyMhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the frequency in MHz of the Wi-Fi channel Value is 0 or greater |

### getMacAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMacAddress(): MacAddress?
```

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | the MAC address of the responder This value may be`null`. |

### getPreamble

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreamble(): Int
```

Get the preamble type of the channel.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the preamble used for this channel Value is [android.net.wifi.ScanResult#PREAMBLE_LEGACY](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#PREAMBLE_LEGACY:kotlin.Int), [android.net.wifi.ScanResult#PREAMBLE_HT](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#PREAMBLE_HT:kotlin.Int), [android.net.wifi.ScanResult#PREAMBLE_VHT](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#PREAMBLE_VHT:kotlin.Int), [android.net.wifi.ScanResult#PREAMBLE_HE](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#PREAMBLE_HE:kotlin.Int), or [android.net.wifi.ScanResult#PREAMBLE_EHT](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#PREAMBLE_EHT:kotlin.Int) |

### getResponderType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResponderType(): Int
```

Get responder type.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The type of this responder Value is [android.net.wifi.rtt.ResponderConfig#RESPONDER_AP](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#RESPONDER_AP:kotlin.Int), [android.net.wifi.rtt.ResponderConfig#RESPONDER_STA](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig#RESPONDER_STA:kotlin.Int), android.net.wifi.rtt.ResponderConfig.RESPONDER_P2P_GO, android.net.wifi.rtt.ResponderConfig.RESPONDER_P2P_CLIENT, or android.net.wifi.rtt.ResponderConfig.RESPONDER_AWARE |

**See Also**

- [android.net.wifi.rtt.ResponderConfig.Builder#setResponderType(int)](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderConfig.Builder#setResponderType(kotlin.Int)) 

### getSecureRangingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecureRangingConfig(): SecureRangingConfig?
```

Get secure ranging configuration.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [SecureRangingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/SecureRangingConfig)? | Secure ranging configuration. Returns null for non-secure ranging configuration. |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### is80211azNtbSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun is80211azNtbSupported(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the Responder supports the 802.11az non-trigger based ranging protocol, false otherwise. |

### is80211mcSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun is80211mcSupported(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the Responder supports the 802.11mc protocol, false otherwise. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ResponderConfig!>
```
