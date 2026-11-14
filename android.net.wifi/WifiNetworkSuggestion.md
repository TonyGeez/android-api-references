# WifiNetworkSuggestion

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiNetworkSuggestion

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiNetworkSuggestion "View this page in Java") 

```
class WifiNetworkSuggestion : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#) |

The Network Suggestion object is used to provide a Wi-Fi network for consideration when auto-connecting to networks. Apps cannot directly create this object, they must use [WifiNetworkSuggestion.Builder.build()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#build())to obtain an instance of this object.

Apps can provide a list of such networks to the platform using [WifiManager.addNetworkSuggestions(List)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetworkSuggestions(kotlin.collections.MutableList)).

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder) Builder used to create [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_NON_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#RANDOMIZATION_NON_PERSISTENT:kotlin.Int) With this option, the randomized MAC address will periodically get re-randomized, and the randomized MAC address will change if the suggestion is removed and then added back. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#RANDOMIZATION_PERSISTENT:kotlin.Int) Generate a randomized MAC from a secret seed and information from the Wi-Fi configuration (SSID or Passpoint profile) and reuse it for all connections to this network. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | [getBssid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getBssid())`()` Get the BSSID, or null if unset. |
| [WifiEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig)? | [getEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getEnterpriseConfig())`()` Get the WifiEnterpriseConfig, or null if unset. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMacRandomizationSetting](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getMacRandomizationSetting())`()` Get the MAC randomization method. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPassphrase](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getPassphrase())`()` Get the passphrase, or null if unset. |
| [PasspointConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration)? | [getPasspointConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getPasspointConfig())`()` Get the [PasspointConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration) associated with this Suggestion, or null if this Suggestion is not for a Passpoint network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriority](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getPriority())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityGroup](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getPriorityGroup())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getSsid())`()` Return the unicode SSID of the network, or null if this is a Passpoint network or the SSID is non-unicode. |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | [getSubscriptionGroup](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getSubscriptionGroup())`()` Get the subscription Group UUID of the suggestion |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionId](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getSubscriptionId())`()` <br /> |
| [WifiSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid)? | [getWifiSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getWifiSsid())`()` Return the [WifiSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid) of the network, or null if this is a Passpoint network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAppInteractionRequired](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isAppInteractionRequired())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCarrierMerged](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isCarrierMerged())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCredentialSharedWithUser](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isCredentialSharedWithUser())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnhancedOpen](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isEnhancedOpen())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHiddenSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isHiddenSsid())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInitialAutojoinEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isInitialAutojoinEnabled())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetered](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isMetered())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRestricted](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isRestricted())`()` Return if a suggestion is for a restricted network |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUntrusted](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isUntrusted())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserInteractionRequired](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isUserInteractionRequired())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWifi7Enabled](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#isWifi7Enabled())`()` See [Builder.setWifi7Enabled(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWifi7Enabled(kotlin.Boolean)) |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

- [android.net.wifi.WifiNetworkSuggestion.Builder#setBssid(MacAddress)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setBssid(android.net.MacAddress)) 

### getEnterpriseConfig

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEnterpriseConfig(): WifiEnterpriseConfig?
```

Get the WifiEnterpriseConfig, or null if unset. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setWapiEnterpriseConfig(WifiEnterpriseConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWapiEnterpriseConfig(android.net.wifi.WifiEnterpriseConfig))
- [android.net.wifi.WifiNetworkSuggestion.Builder#setWpa2EnterpriseConfig(WifiEnterpriseConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWpa2EnterpriseConfig(android.net.wifi.WifiEnterpriseConfig))
- [android.net.wifi.WifiNetworkSuggestion.Builder#setWpa3EnterpriseConfig(WifiEnterpriseConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWpa3EnterpriseConfig(android.net.wifi.WifiEnterpriseConfig)) 

### getMacRandomizationSetting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMacRandomizationSetting(): Int
```

Get the MAC randomization method.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of`RANDOMIZATION_*`values Value is [android.net.wifi.WifiNetworkSuggestion#RANDOMIZATION_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#RANDOMIZATION_PERSISTENT:kotlin.Int), or [android.net.wifi.WifiNetworkSuggestion#RANDOMIZATION_NON_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#RANDOMIZATION_NON_PERSISTENT:kotlin.Int) |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setMacRandomizationSetting(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setMacRandomizationSetting(kotlin.Int)) 

### getPassphrase

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPassphrase(): String?
```

Get the passphrase, or null if unset. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setWapiPassphrase(String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWapiPassphrase(kotlin.String))
- [android.net.wifi.WifiNetworkSuggestion.Builder#setWpa2Passphrase(String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWpa2Passphrase(kotlin.String))
- [android.net.wifi.WifiNetworkSuggestion.Builder#setWpa3Passphrase(String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWpa3Passphrase(kotlin.String)) 

### getPasspointConfig

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPasspointConfig(): PasspointConfiguration?
```

Get the [PasspointConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration) associated with this Suggestion, or null if this Suggestion is not for a Passpoint network. 

### getPriority

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriority(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setPriority(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setPriority(kotlin.Int)) 

### getPriorityGroup

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityGroup(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setPriorityGroup(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setPriorityGroup(kotlin.Int)) 

### getSsid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSsid(): String?
```

Return the unicode SSID of the network, or null if this is a Passpoint network or the SSID is non-unicode.

Note: use [getWifiSsid()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion#getWifiSsid())which supports both unicode and non-unicode SSID. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setSsid(String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setSsid(kotlin.String)) 

### getSubscriptionGroup

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubscriptionGroup(): ParcelUuid?
```

Get the subscription Group UUID of the suggestion

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | Uuid represent a Subscription Group This value may be`null`. |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setSubscriptionGroup(ParcelUuid)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setSubscriptionGroup(android.os.ParcelUuid)) 

### getSubscriptionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubscriptionId(): Int
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setSubscriptionId(kotlin.Int)) 

### getWifiSsid

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWifiSsid(): WifiSsid?
```

Return the [WifiSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid) of the network, or null if this is a Passpoint network.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [WifiSsid](https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid)? | An object representing the SSID the network.`null`for passpoint network. |

**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setWifiSsid(WifiSsid)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWifiSsid(android.net.wifi.WifiSsid)) 

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

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsAppInteractionRequired(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setIsAppInteractionRequired(kotlin.Boolean)) 

### isCarrierMerged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCarrierMerged(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setCarrierMerged(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setCarrierMerged(kotlin.Boolean)) 

### isCredentialSharedWithUser

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCredentialSharedWithUser(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setCredentialSharedWithUser(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setCredentialSharedWithUser(kotlin.Boolean)) 

### isEnhancedOpen

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnhancedOpen(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsEnhancedOpen(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setIsEnhancedOpen(kotlin.Boolean)) 

### isHiddenSsid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHiddenSsid(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsHiddenSsid(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setIsHiddenSsid(kotlin.Boolean)) 

### isInitialAutojoinEnabled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInitialAutojoinEnabled(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsInitialAutojoinEnabled(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setIsInitialAutojoinEnabled(kotlin.Boolean)) 

### isMetered

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMetered(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsMetered(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setIsMetered(kotlin.Boolean)) 

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

- [android.net.wifi.WifiNetworkSuggestion.Builder#setRestricted(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setRestricted(kotlin.Boolean)) 

### isUntrusted

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUntrusted(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setUntrusted(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setUntrusted(kotlin.Boolean)) 

### isUserInteractionRequired

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUserInteractionRequired(): Boolean
```  
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setIsUserInteractionRequired(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setIsUserInteractionRequired(kotlin.Boolean)) 

### isWifi7Enabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isWifi7Enabled(): Boolean
```

See [Builder.setWifi7Enabled(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setWifi7Enabled(kotlin.Boolean)) 

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiNetworkSuggestion!>
```
