# WifiNetworkSuggestion

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiNetworkSuggestion

Kotlin| [Java](../android/net/wifi/WifiNetworkSuggestion.md) 
| --- | --- |

```
class WifiNetworkSuggestion : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.WifiNetworkSuggestion](../android/net/wifi/WifiNetworkSuggestion.md) |

The Network Suggestion object is used to provide a Wi-Fi network for consideration when auto-connecting to networks. Apps cannot directly create this object, they must use [WifiNetworkSuggestion.Builder.build()](../android/net/wifi/WifiNetworkSuggestion.Builder.md))to obtain an instance of this object.

Apps can provide a list of such networks to the platform using [WifiManager.addNetworkSuggestions(List)](../android/net/wifi/WifiManager.md)).

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/wifi/WifiNetworkSuggestion.Builder.md) Builder used to create [WifiNetworkSuggestion](../android/net/wifi/WifiNetworkSuggestion.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_NON_PERSISTENT](../android/net/wifi/WifiNetworkSuggestion.md) With this option, the randomized MAC address will periodically get re-randomized, and the randomized MAC address will change if the suggestion is removed and then added back. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_PERSISTENT](../android/net/wifi/WifiNetworkSuggestion.md) Generate a randomized MAC from a secret seed and information from the Wi-Fi configuration (SSID or Passpoint profile) and reuse it for all connections to this network. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/wifi/WifiNetworkSuggestion.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MacAddress](../android/net/MacAddress.md)? | [getBssid](../android/net/wifi/WifiNetworkSuggestion.md))`()` Get the BSSID, or null if unset. |
| --- | --- |
| [WifiEnterpriseConfig](../android/net/wifi/WifiEnterpriseConfig.md)? | [getEnterpriseConfig](../android/net/wifi/WifiNetworkSuggestion.md))`()` Get the WifiEnterpriseConfig, or null if unset. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMacRandomizationSetting](../android/net/wifi/WifiNetworkSuggestion.md))`()` Get the MAC randomization method. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPassphrase](../android/net/wifi/WifiNetworkSuggestion.md))`()` Get the passphrase, or null if unset. |
| --- | --- |
| [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md)? | [getPasspointConfig](../android/net/wifi/WifiNetworkSuggestion.md))`()` Get the [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md) associated with this Suggestion, or null if this Suggestion is not for a Passpoint network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriority](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityGroup](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSsid](../android/net/wifi/WifiNetworkSuggestion.md))`()` Return the unicode SSID of the network, or null if this is a Passpoint network or the SSID is non-unicode. |
| [ParcelUuid](../android/os/ParcelUuid.md)? | [getSubscriptionGroup](../android/net/wifi/WifiNetworkSuggestion.md))`()` Get the subscription Group UUID of the suggestion |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionId](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| --- | --- |
| [WifiSsid](../android/net/wifi/WifiSsid.md)? | [getWifiSsid](../android/net/wifi/WifiNetworkSuggestion.md))`()` Return the [WifiSsid](../android/net/wifi/WifiSsid.md) of the network, or null if this is a Passpoint network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAppInteractionRequired](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCarrierMerged](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCredentialSharedWithUser](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnhancedOpen](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHiddenSsid](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInitialAutojoinEnabled](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetered](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRestricted](../android/net/wifi/WifiNetworkSuggestion.md))`()` Return if a suggestion is for a restricted network |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUntrusted](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserInteractionRequired](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWifi7Enabled](../android/net/wifi/WifiNetworkSuggestion.md))`()` See [Builder.setWifi7Enabled(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/wifi/WifiNetworkSuggestion.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/wifi/WifiNetworkSuggestion.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiNetworkSuggestion](../android/net/wifi/WifiNetworkSuggestion.md)!\> | [CREATOR](../android/net/wifi/WifiNetworkSuggestion.md) <br /> |

## Constants

### RANDOMIZATION_NON_PERSISTENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANDOMIZATION_NON_PERSISTENT: Int
```

With this option, the randomized MAC address will periodically get re-randomized, and the randomized MAC address will change if the suggestion is removed and then added back. 

 Value: 1

### RANDOMIZATION_PERSISTENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANDOMIZATION_PERSISTENT: Int
```

Generate a randomized MAC from a secret seed and information from the Wi-Fi configuration (SSID or Passpoint profile) and reuse it for all connections to this network. The randomized MAC address for this network will stay the same for each subsequent association until the device undergoes factory reset. 

 Value: 0

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Get the BSSID, or null if unset. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setBssid(MacAddress)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getEnterpriseConfig

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEnterpriseConfig(): WifiEnterpriseConfig?
```

Get the WifiEnterpriseConfig, or null if unset. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setWapiEnterpriseConfig(WifiEnterpriseConfig)](../android/net/wifi/WifiNetworkSuggestion.Builder.md))
- [android.net.wifi.WifiNetworkSuggestion.Builder#setWpa2EnterpriseConfig(WifiEnterpriseConfig)](../android/net/wifi/WifiNetworkSuggestion.Builder.md))
- [android.net.wifi.WifiNetworkSuggestion.Builder#setWpa3EnterpriseConfig(WifiEnterpriseConfig)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getMacRandomizationSetting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMacRandomizationSetting(): Int
```

Get the MAC randomization method.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of`RANDOMIZATION_*`values Value is [android.net.wifi.WifiNetworkSuggestion#RANDOMIZATION_PERSISTENT](../android/net/wifi/WifiNetworkSuggestion.md), or [android.net.wifi.WifiNetworkSuggestion#RANDOMIZATION_NON_PERSISTENT](../android/net/wifi/WifiNetworkSuggestion.md) |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setMacRandomizationSetting(int)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getPassphrase

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPassphrase(): String?
```

Get the passphrase, or null if unset. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setWapiPassphrase(String)](../android/net/wifi/WifiNetworkSuggestion.Builder.md))
- [android.net.wifi.WifiNetworkSuggestion.Builder#setWpa2Passphrase(String)](../android/net/wifi/WifiNetworkSuggestion.Builder.md))
- [android.net.wifi.WifiNetworkSuggestion.Builder#setWpa3Passphrase(String)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getPasspointConfig

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPasspointConfig(): PasspointConfiguration?
```

Get the [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md) associated with this Suggestion, or null if this Suggestion is not for a Passpoint network. 

### getPriority

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriority(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setPriority(int)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getPriorityGroup

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityGroup(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setPriorityGroup(int)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getSsid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSsid(): String?
```

Return the unicode SSID of the network, or null if this is a Passpoint network or the SSID is non-unicode.

Note: use [getWifiSsid()](../android/net/wifi/WifiNetworkSuggestion.md))which supports both unicode and non-unicode SSID. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setSsid(String)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getSubscriptionGroup

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubscriptionGroup(): ParcelUuid?
```

Get the subscription Group UUID of the suggestion

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [ParcelUuid](../android/os/ParcelUuid.md)? | Uuid represent a Subscription Group This value may be`null`. |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setSubscriptionGroup(ParcelUuid)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getSubscriptionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubscriptionId(): Int
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setSubscriptionId(int)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### getWifiSsid

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWifiSsid(): WifiSsid?
```

Return the [WifiSsid](../android/net/wifi/WifiSsid.md) of the network, or null if this is a Passpoint network.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [WifiSsid](../android/net/wifi/WifiSsid.md)? | An object representing the SSID the network.`null`for passpoint network. |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setWifiSsid(WifiSsid)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isAppInteractionRequired

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAppInteractionRequired(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsAppInteractionRequired(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isCarrierMerged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCarrierMerged(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setCarrierMerged(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isCredentialSharedWithUser

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCredentialSharedWithUser(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setCredentialSharedWithUser(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isEnhancedOpen

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnhancedOpen(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsEnhancedOpen(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isHiddenSsid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHiddenSsid(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsHiddenSsid(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isInitialAutojoinEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInitialAutojoinEnabled(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsInitialAutojoinEnabled(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isMetered

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMetered(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsMetered(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isRestricted

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRestricted(): Boolean
```

Return if a suggestion is for a restricted network

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the suggestion is restricted, false otherwise |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setRestricted(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isUntrusted

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUntrusted(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setUntrusted(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isUserInteractionRequired

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUserInteractionRequired(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsUserInteractionRequired(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### isWifi7Enabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isWifi7Enabled(): Boolean
```

See [Builder.setWifi7Enabled(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiNetworkSuggestion!>
```
