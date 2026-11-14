# WifiConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiConfiguration

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiConfiguration "View this page in Java") 
| --- | --- |

```
open class WifiConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#) |

A class representing a configured Wi-Fi network, including the security configuration. Non privileged caller should use [WifiNetworkSpecifier.Builder](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder) to create [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#) and [WifiNetworkSuggestion.Builder](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder) to create [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion). This class can still be used with privileged APIs only such as [WifiManager.addNetwork(WifiConfiguration)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration)).

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AuthAlgorithm](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.AuthAlgorithm) Recognized IEEE 802. |
| open | [GroupCipher](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.GroupCipher) Recognized group ciphers. |
| open | [GroupMgmtCipher](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.GroupMgmtCipher) Recognized group management ciphers. |
| --- | --- |
| open | [KeyMgmt](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.KeyMgmt) Recognized key management schemes. |
| open | [PairwiseCipher](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.PairwiseCipher) Recognized pairwise ciphers for WPA. |
| open | [Protocol](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.Protocol) Recognized security protocols. |
| --- | --- |
| open | [Status](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.Status) Possible status of a network configuration. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_AUTO](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_AUTO:kotlin.Int) Let the wifi framework automatically decide the MAC randomization strategy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_NONE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_NONE:kotlin.Int) Use factory MAC when connecting to this network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_NON_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_NON_PERSISTENT:kotlin.Int) Use a randomly generated MAC address for connections to this network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_PERSISTENT:kotlin.Int) Generate a randomized MAC once and reuse it for all connections to this network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_DPP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_DPP:kotlin.Int) Security type for Easy Connect (DPP) network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_EAP:kotlin.Int) Security type for an EAP network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_SUITE_B](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_EAP_SUITE_B:kotlin.Int) Security type for a WPA3-Enterprise in 192-bit security network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_WPA3_ENTERPRISE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_EAP_WPA3_ENTERPRISE:kotlin.Int) Security type for a WPA3-Enterprise network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT:kotlin.Int) Security type for a WPA3-Enterprise in 192-bit security network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OPEN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_OPEN:kotlin.Int) Security type for an open network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OWE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_OWE:kotlin.Int) Security type for an OWE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_PSK](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_PSK:kotlin.Int) Security type for a PSK network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_SAE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_SAE:kotlin.Int) Security type for an SAE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WAPI_CERT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_WAPI_CERT:kotlin.Int) Security type for a WAPI Certificate network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WAPI_PSK](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_WAPI_PSK:kotlin.Int) Security type for a WAPI PSK network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WEP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_WEP:kotlin.Int) Security type for a WEP network. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#WifiConfiguration())`()` <br /> |
| [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#WifiConfiguration(android.net.wifi.WifiConfiguration))`(`source:` ` [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#)`)` Copy constructor |

| Public methods ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo.html#)! | [getHttpProxy](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#getHttpProxy())`()` Returns the HTTP proxy used by this object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getKey](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#getKey())`()` Return a String that can be used to uniquely identify this WifiConfiguration. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMacRandomizationSetting](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#getMacRandomizationSetting())`()` Get the MAC randomization setting for this network. |
| --- | --- |
| open [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#) | [getRandomizedMacAddress](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#getRandomizedMacAddress())`()` Returns MAC address set to be the local randomized MAC address. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDppConfigurator](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#isDppConfigurator())`()` To check if this WifiConfiguration supports configuring a peer Enrollee device with SECURITY_TYPE_DPP |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPasspoint](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#isPasspoint())`()` Identify if this configuration represents a Passpoint network |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHttpProxy](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#setHttpProxy(android.net.ProxyInfo))`(`httpProxy:` ` [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo.html#)!`)` Set the [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo.html#) for this WifiConfiguration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIpConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#setIpConfiguration(android.net.IpConfiguration))`(`ipConfiguration:` ` [IpConfiguration](https://developer.android.com/reference/kotlin/android/net/IpConfiguration.html#)?`)` Set the [IpConfiguration](https://developer.android.com/reference/kotlin/android/net/IpConfiguration.html#) for this network. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMacRandomizationSetting](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#setMacRandomizationSetting(kotlin.Int))`(`macRandomizationSetting:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the MAC randomization setting for this network. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSecurityParams](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#setSecurityParams(kotlin.Int))`(`securityType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the various security params to correspond to the provided security type. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#toString())`()` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [BSSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#BSSID:kotlin.String) When set, this network configuration entry should only be used when associating with the AP having the specified BSSID. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [FQDN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#FQDN:kotlin.String) Fully qualified domain name of a Passpoint configuration |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [SSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SSID:kotlin.String) The network's SSID. |
| --- | --- |
| [BitSet](https://developer.android.com/reference/kotlin/java/util/BitSet.html#) | [allowedAuthAlgorithms](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#allowedAuthAlgorithms:java.util.BitSet) The set of authentication protocols supported by this configuration. |
| [BitSet](https://developer.android.com/reference/kotlin/java/util/BitSet.html#) | [allowedGroupCiphers](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#allowedGroupCiphers:java.util.BitSet) The set of group ciphers supported by this configuration. |
| [BitSet](https://developer.android.com/reference/kotlin/java/util/BitSet.html#) | [allowedGroupManagementCiphers](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#allowedGroupManagementCiphers:java.util.BitSet) The set of group management ciphers supported by this configuration. |
| --- | --- |
| [BitSet](https://developer.android.com/reference/kotlin/java/util/BitSet.html#) | [allowedKeyManagement](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#allowedKeyManagement:java.util.BitSet) The set of key management protocols supported by this configuration. |
| [BitSet](https://developer.android.com/reference/kotlin/java/util/BitSet.html#) | [allowedPairwiseCiphers](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#allowedPairwiseCiphers:java.util.BitSet) The set of pairwise ciphers for WPA supported by this configuration. |
| [BitSet](https://developer.android.com/reference/kotlin/java/util/BitSet.html#) | [allowedProtocols](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#allowedProtocols:java.util.BitSet) The set of security protocols supported by this configuration. |
| --- | --- |
| [BitSet](https://developer.android.com/reference/kotlin/java/util/BitSet.html#) | [allowedSuiteBCiphers](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#allowedSuiteBCiphers:java.util.BitSet) The set of SuiteB ciphers supported by this configuration. |
| [WifiEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig)! | [enterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#enterpriseConfig:android.net.wifi.WifiEnterpriseConfig) The enterprise configuration details specifying the EAP method, certificates and other settings associated with the EAP. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hiddenSSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#hiddenSSID:kotlin.Boolean) This is a network that does not broadcast its SSID, so an SSID-specific probe request must be used for scans. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHomeProviderNetwork](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#isHomeProviderNetwork:kotlin.Boolean) Flag indicating if this network is provided by a home Passpoint provider or a roaming Passpoint provider. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [networkId](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#networkId:kotlin.Int) The ID number that the supplicant uses to identify this network configuration entry. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [preSharedKey](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#preSharedKey:kotlin.String) Pre-shared key for use with WPA-PSK. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [priority](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#priority:kotlin.Int) Priority determines the preference given to a network by`wpa_supplicant`when choosing an access point with which to associate. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [providerFriendlyName](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#providerFriendlyName:kotlin.String) Name of Passpoint credential provider |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [roamingConsortiumIds](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#roamingConsortiumIds:kotlin.LongArray) Roaming Consortium Id list for Passpoint credential; identifies a set of networks where Passpoint credential will be considered valid |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [status](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#status:kotlin.Int) The current status of this network configuration entry. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [wepKeys](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#wepKeys:kotlin.Array) Four WEP keys. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [wepTxKeyIndex](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#wepTxKeyIndex:kotlin.Int) Default WEP key index, ranging from 0 to 3. |
| --- | --- |

## Constants

### RANDOMIZATION_AUTO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANDOMIZATION_AUTO: Int
```

Let the wifi framework automatically decide the MAC randomization strategy. 

 Value: 3

### RANDOMIZATION_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANDOMIZATION_NONE: Int
```

Use factory MAC when connecting to this network 

 Value: 0

### RANDOMIZATION_NON_PERSISTENT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANDOMIZATION_NON_PERSISTENT: Int
```

Use a randomly generated MAC address for connections to this network. This option does not persist the randomized MAC address. 

 Value: 2

### RANDOMIZATION_PERSISTENT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANDOMIZATION_PERSISTENT: Int
```

Generate a randomized MAC once and reuse it for all connections to this network 

 Value: 1

### SECURITY_TYPE_DPP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_DPP: Int
```

Security type for Easy Connect (DPP) network 

 Value: 13

### SECURITY_TYPE_EAP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_EAP: Int
```

Security type for an EAP network. 

 Value: 3

### SECURITY_TYPE_EAP_SUITE_B

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_EAP_SUITE_B: Int
```

**Deprecated:** *Use the [SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT:kotlin.Int) constant (which is the same value).*

Security type for a WPA3-Enterprise in 192-bit security network. 

 Value: 5

### SECURITY_TYPE_EAP_WPA3_ENTERPRISE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_EAP_WPA3_ENTERPRISE: Int
```

Security type for a WPA3-Enterprise network. 

 Value: 9

### SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT: Int
```

Security type for a WPA3-Enterprise in 192-bit security network. This is the same as [SECURITY_TYPE_EAP_SUITE_B](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_EAP_SUITE_B:kotlin.Int) and uses the same value. 

 Value: 5

### SECURITY_TYPE_OPEN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_OPEN: Int
```

Security type for an open network. 

 Value: 0

### SECURITY_TYPE_OWE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_OWE: Int
```

Security type for an OWE network. 

 Value: 6

### SECURITY_TYPE_PSK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_PSK: Int
```

Security type for a PSK network. 

 Value: 2

### SECURITY_TYPE_SAE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_SAE: Int
```

Security type for an SAE network. 

 Value: 4

### SECURITY_TYPE_WAPI_CERT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WAPI_CERT: Int
```

Security type for a WAPI Certificate network. 

 Value: 8

### SECURITY_TYPE_WAPI_PSK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WAPI_PSK: Int
```

Security type for a WAPI PSK network. 

 Value: 7

### SECURITY_TYPE_WEP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WEP: Int
```

Security type for a WEP network. 

 Value: 1

## Public constructors

### WifiConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiConfiguration()
```  

### WifiConfiguration

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiConfiguration(source: WifiConfiguration)
```

Copy constructor

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#):This value cannot be`null`. |

## Public methods

### getHttpProxy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHttpProxy(): ProxyInfo!
```

Returns the HTTP proxy used by this object.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo.html#)! | a [httpProxy](https://developer.android.com/reference/kotlin/android/net/ProxyInfo.html#) representing the proxy specified by this WifiConfiguration, or`null`if no proxy is specified. |

### getKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKey(): String
```

Return a String that can be used to uniquely identify this WifiConfiguration. 
Note: Do not persist this value! This value is not guaranteed to remain backwards compatible.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getMacRandomizationSetting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMacRandomizationSetting(): Int
```

Get the MAC randomization setting for this network.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.WifiConfiguration#RANDOMIZATION_NONE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_NONE:kotlin.Int), [android.net.wifi.WifiConfiguration#RANDOMIZATION_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_PERSISTENT:kotlin.Int), [android.net.wifi.WifiConfiguration#RANDOMIZATION_NON_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_NON_PERSISTENT:kotlin.Int), or [android.net.wifi.WifiConfiguration#RANDOMIZATION_AUTO](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_AUTO:kotlin.Int) |

### getRandomizedMacAddress

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRandomizedMacAddress(): MacAddress
```

Returns MAC address set to be the local randomized MAC address. Depending on user preference, the device may or may not use the returned MAC address for connections to this network.

Information is restricted to Device Owner, Profile Owner, and Carrier apps (which will only obtain addresses for configurations which they create). Other callers will receive a default "02:00:00:00:00:00" MAC address.

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------|
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#) | This value cannot be`null`. |

### isDppConfigurator

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDppConfigurator(): Boolean
```

To check if this WifiConfiguration supports configuring a peer Enrollee device with SECURITY_TYPE_DPP 

### isPasspoint

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPasspoint(): Boolean
```

Identify if this configuration represents a Passpoint network 

### setHttpProxy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHttpProxy(httpProxy: ProxyInfo!): Unit
```

Set the [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo.html#) for this WifiConfiguration. This method should only be used by a device owner or profile owner. When other apps attempt to save a [WifiConfiguration](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#) with modified proxy settings, the methods [WifiManager.addNetwork](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addNetwork(android.net.wifi.WifiConfiguration))and [WifiManager.updateNetwork](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#updateNetwork(android.net.wifi.WifiConfiguration))fail and return`-1`.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `httpProxy` | [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo.html#)!: [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo.html#) representing the httpProxy to be used by this WifiConfiguration. Setting this to`null`will explicitly set no proxy, removing any proxy that was previously set. |

### setIpConfiguration

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIpConfiguration(ipConfiguration: IpConfiguration?): Unit
```

Set the [IpConfiguration](https://developer.android.com/reference/kotlin/android/net/IpConfiguration.html#) for this network.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ipConfiguration` | [IpConfiguration](https://developer.android.com/reference/kotlin/android/net/IpConfiguration.html#)?:a [IpConfiguration](https://developer.android.com/reference/kotlin/android/net/IpConfiguration.html#) to use for this Wi-Fi configuration, or`null`to use the default configuration. |

### setMacRandomizationSetting

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMacRandomizationSetting(macRandomizationSetting: Int): Unit
```

Set the MAC randomization setting for this network.

Caller must satify one of the following conditions:

- Have`android.Manifest.permission#NETWORK_SETTINGS`permission.
- Have`android.Manifest.permission#NETWORK_SETUP_WIZARD`permission.
- Be in Demo Mode.
- Be the creator adding or updating a passpoint network.
- Be an admin updating their own network.

| Parameters ||
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `macRandomizationSetting` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.net.wifi.WifiConfiguration#RANDOMIZATION_NONE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_NONE:kotlin.Int), [android.net.wifi.WifiConfiguration#RANDOMIZATION_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_PERSISTENT:kotlin.Int), [android.net.wifi.WifiConfiguration#RANDOMIZATION_NON_PERSISTENT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_NON_PERSISTENT:kotlin.Int), or [android.net.wifi.WifiConfiguration#RANDOMIZATION_AUTO](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#RANDOMIZATION_AUTO:kotlin.Int) |

### setSecurityParams

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSecurityParams(securityType: Int): Unit
```

Set the various security params to correspond to the provided security type. This is accomplished by setting the various BitSets exposed in WifiConfiguration. 
This API would clear existing security types and add a default one. Before calling this API with [SECURITY_TYPE_DPP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration#SECURITY_TYPE_DPP:kotlin.Int) as securityType, call [android.net.wifi.WifiManager#isEasyConnectDppAkmSupported()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isEasyConnectDppAkmSupported())} 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### BSSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var BSSID: String!
```

When set, this network configuration entry should only be used when associating with the AP having the specified BSSID. The value is a string in the format of an Ethernet MAC address, e.g.,`XX:XX:XX:XX:XX:XX`where each`X`is a hex digit. 

### FQDN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var FQDN: String!
```

Fully qualified domain name of a Passpoint configuration 

### SSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var SSID: String!
```

The network's SSID. Can either be a UTF-8 string, which must be enclosed in double quotation marks (e.g.,`"MyNetwork"`), or a string of hex digits, which are not enclosed in quotes (e.g.,`01a243f405`). 

### allowedAuthAlgorithms

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedAuthAlgorithms: BitSet
```

The set of authentication protocols supported by this configuration. See [AuthAlgorithm](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.AuthAlgorithm) for descriptions of the values. Defaults to automatic selection. 

### allowedGroupCiphers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedGroupCiphers: BitSet
```

The set of group ciphers supported by this configuration. See [GroupCipher](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.GroupCipher) for descriptions of the values. Defaults to CCMP TKIP WEP104 WEP40. 

### allowedGroupManagementCiphers

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedGroupManagementCiphers: BitSet
```

The set of group management ciphers supported by this configuration. See [GroupMgmtCipher](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.GroupMgmtCipher) for descriptions of the values. 

### allowedKeyManagement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedKeyManagement: BitSet
```

The set of key management protocols supported by this configuration. See [KeyMgmt](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.KeyMgmt) for descriptions of the values. Defaults to WPA-PSK WPA-EAP. 

### allowedPairwiseCiphers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedPairwiseCiphers: BitSet
```

The set of pairwise ciphers for WPA supported by this configuration. See [PairwiseCipher](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.PairwiseCipher) for descriptions of the values. Defaults to CCMP TKIP. 

### allowedProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedProtocols: BitSet
```

The set of security protocols supported by this configuration. See [Protocol](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.Protocol) for descriptions of the values. Defaults to WPA RSN. 

### allowedSuiteBCiphers

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedSuiteBCiphers: BitSet
```

The set of SuiteB ciphers supported by this configuration. To be used for WPA3-Enterprise mode. Set automatically by the framework based on the certificate type that is used in this configuration. 

### enterpriseConfig

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var enterpriseConfig: WifiEnterpriseConfig!
```

The enterprise configuration details specifying the EAP method, certificates and other settings associated with the EAP. 

### hiddenSSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var hiddenSSID: Boolean
```

This is a network that does not broadcast its SSID, so an SSID-specific probe request must be used for scans. 

### isHomeProviderNetwork

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var isHomeProviderNetwork: Boolean
```

Flag indicating if this network is provided by a home Passpoint provider or a roaming Passpoint provider. This flag will be`true`if this network is provided by a home Passpoint provider and`false`if is provided by a roaming Passpoint provider or is a non-Passpoint network. 

### networkId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var networkId: Int
```

The ID number that the supplicant uses to identify this network configuration entry. This must be passed as an argument to most calls into the supplicant. 

### preSharedKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var preSharedKey: String!
```

Pre-shared key for use with WPA-PSK. Either an ASCII string enclosed in double quotation marks (e.g.,`"abcdefghij"`for PSK passphrase or a string of 64 hex digits for raw PSK.

<br />

When the value of this key is read, the actual key is not returned, just a "\*" if the key has a value, or the null string otherwise. 

### priority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var priority: Int
```

**Deprecated:** *This field does not exist anymore.*

Priority determines the preference given to a network by`wpa_supplicant`when choosing an access point with which to associate. 

### providerFriendlyName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var providerFriendlyName: String!
```

Name of Passpoint credential provider 

### roamingConsortiumIds

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var roamingConsortiumIds: LongArray!
```

Roaming Consortium Id list for Passpoint credential; identifies a set of networks where Passpoint credential will be considered valid 

### status

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var status: Int
```

The current status of this network configuration entry. 
**See Also**

- [android.net.wifi.WifiConfiguration.Status](https://developer.android.com/reference/kotlin/android/net/wifi/WifiConfiguration.Status) 

### wepKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var wepKeys: Array<String!>!
```

**Deprecated:** *Due to security and performance limitations, use of WEP networks is discouraged.*

Four WEP keys. For each of the four values, provide either an ASCII string enclosed in double quotation marks (e.g.,`"abcdef"`) or a string of hex digits (e.g.,`0102030405`).

<br />

When the value of one of these keys is read, the actual key is not returned, just a "\*" if the key has a value, or the null string otherwise. 

### wepTxKeyIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var wepTxKeyIndex: Int
```

**Deprecated:** *Due to security and performance limitations, use of WEP networks is discouraged.*

Default WEP key index, ranging from 0 to 3.
