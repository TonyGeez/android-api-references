# ResponderConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResponderConfig

Kotlin| [Java](ResponderConfig.md) 
| --- | --- |

```
class ResponderConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.rtt.ResponderConfig](ResponderConfig.md) |

Defines the configuration of an IEEE 802.11mc Responder. The Responder may be an Access Point (AP), a Wi-Fi Aware device, or a manually configured Responder.

A Responder configuration may be constructed from a [ScanResult](../android.net.wifi/ScanResult.md) or manually (with the data obtained out-of-band from a peer).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/wifi/rtt/ResponderConfig.Builder.md) Builder class used to construct [ResponderConfig](ResponderConfig.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONDER_AP](ResponderConfig.md) Responder is an access point(AP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONDER_STA](ResponderConfig.md) Responder is a client device(STA). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](ResponderConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ResponderConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [ResponderConfig](ResponderConfig.md) | [fromScanResult](ResponderConfig.md))`(`scanResult:` ` [ScanResult](../android.net.wifi/ScanResult.md)`)` Creates a Responder configuration from a [ScanResult](../android.net.wifi/ScanResult.md) corresponding to an Access Point (AP), which can be obtained from [android.net.wifi.WifiManager#getScanResults()](../android.net.wifi/WifiManager.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCenterFreq0Mhz](ResponderConfig.md))`()` If the Access Point (AP) bandwidth is 20 MHz, 0 MHz is returned. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCenterFreq1Mhz](ResponderConfig.md))`()` If the Access Point (AP) bandwidth is 80 + 80 MHz, this param is not used and returns 0. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelWidth](ResponderConfig.md))`()` AP Channel bandwidth; one of [ScanResult.CHANNEL_WIDTH_20MHZ](../android.net.wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_40MHZ](../android.net.wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_80MHZ](../android.net.wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_160MHZ](../android.net.wifi/ScanResult.md), [CHANNEL_WIDTH_80MHZ_PLUS_MHZ](../android.net.wifi/ScanResult.md) or [ScanResult.CHANNEL_WIDTH_320MHZ](../android.net.wifi/ScanResult.md). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFrequencyMhz](ResponderConfig.md))`()` <br /> |
| [MacAddress](../android.net/MacAddress.md)? | [getMacAddress](ResponderConfig.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPreamble](ResponderConfig.md))`()` Get the preamble type of the channel. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponderType](ResponderConfig.md))`()` Get responder type. |
| [SecureRangingConfig](SecureRangingConfig.md)? | [getSecureRangingConfig](ResponderConfig.md))`()` Get secure ranging configuration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](ResponderConfig.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [is80211azNtbSupported](ResponderConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [is80211mcSupported](ResponderConfig.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ResponderConfig.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](ResponderConfig.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ResponderConfig](ResponderConfig.md)!\> | [CREATOR](ResponderConfig.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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

Creates a Responder configuration from a [ScanResult](../android.net.wifi/ScanResult.md) corresponding to an Access Point (AP), which can be obtained from [android.net.wifi.WifiManager#getScanResults()](../android.net.wifi/WifiManager.md)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `scanResult` | [ScanResult](../android.net.wifi/ScanResult.md):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [ResponderConfig](ResponderConfig.md) | This value cannot be`null`. |

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

AP Channel bandwidth; one of [ScanResult.CHANNEL_WIDTH_20MHZ](../android.net.wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_40MHZ](../android.net.wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_80MHZ](../android.net.wifi/ScanResult.md), [ScanResult.CHANNEL_WIDTH_160MHZ](../android.net.wifi/ScanResult.md), [CHANNEL_WIDTH_80MHZ_PLUS_MHZ](../android.net.wifi/ScanResult.md) or [ScanResult.CHANNEL_WIDTH_320MHZ](../android.net.wifi/ScanResult.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the bandwidth repsentation of the Wi-Fi channel Value is [android.net.wifi.ScanResult#CHANNEL_WIDTH_20MHZ](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#CHANNEL_WIDTH_40MHZ](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#CHANNEL_WIDTH_160MHZ](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#CHANNEL_WIDTH_80MHZ_PLUS_MHZ](../android.net.wifi/ScanResult.md), or [android.net.wifi.ScanResult#CHANNEL_WIDTH_320MHZ](../android.net.wifi/ScanResult.md) |

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
| [MacAddress](../android.net/MacAddress.md)? | the MAC address of the responder This value may be`null`. |

### getPreamble

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreamble(): Int
```

Get the preamble type of the channel.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the preamble used for this channel Value is [android.net.wifi.ScanResult#PREAMBLE_LEGACY](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#PREAMBLE_HT](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#PREAMBLE_VHT](../android.net.wifi/ScanResult.md), [android.net.wifi.ScanResult#PREAMBLE_HE](../android.net.wifi/ScanResult.md), or [android.net.wifi.ScanResult#PREAMBLE_EHT](../android.net.wifi/ScanResult.md) |

### getResponderType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResponderType(): Int
```

Get responder type.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The type of this responder Value is [android.net.wifi.rtt.ResponderConfig#RESPONDER_AP](ResponderConfig.md), [android.net.wifi.rtt.ResponderConfig#RESPONDER_STA](ResponderConfig.md), android.net.wifi.rtt.ResponderConfig.RESPONDER_P2P_GO, android.net.wifi.rtt.ResponderConfig.RESPONDER_P2P_CLIENT, or android.net.wifi.rtt.ResponderConfig.RESPONDER_AWARE |

**See Also**

- [android.net.wifi.rtt.ResponderConfig.Builder#setResponderType(int)](../android/net/wifi/rtt/ResponderConfig.Builder.md)) 

### getSecureRangingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecureRangingConfig(): SecureRangingConfig?
```

Get secure ranging configuration.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [SecureRangingConfig](SecureRangingConfig.md)? | Secure ranging configuration. Returns null for non-secure ranging configuration. |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ResponderConfig!>
```
