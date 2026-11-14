# WifiConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiConfiguration

Kotlin| [Java](../android/net/wifi/WifiConfiguration.md) 
| --- | --- |

```
open class WifiConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.WifiConfiguration](../android/net/wifi/WifiConfiguration.md) |

A class representing a configured Wi-Fi network, including the security configuration. Non privileged caller should use [WifiNetworkSpecifier.Builder](../android/net/wifi/WifiNetworkSpecifier.Builder.md) to create [NetworkSpecifier](../android/net/NetworkSpecifier.md) and [WifiNetworkSuggestion.Builder](../android/net/wifi/WifiNetworkSuggestion.Builder.md) to create [WifiNetworkSuggestion](../android/net/wifi/WifiNetworkSuggestion.md). This class can still be used with privileged APIs only such as [WifiManager.addNetwork(WifiConfiguration)](../android/net/wifi/WifiManager.md)).

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AuthAlgorithm](../android/net/wifi/WifiConfiguration.AuthAlgorithm.md) Recognized IEEE 802. |
| open | [GroupCipher](../android/net/wifi/WifiConfiguration.GroupCipher.md) Recognized group ciphers. |
| open | [GroupMgmtCipher](../android/net/wifi/WifiConfiguration.GroupMgmtCipher.md) Recognized group management ciphers. |
| --- | --- |
| open | [KeyMgmt](../android/net/wifi/WifiConfiguration.KeyMgmt.md) Recognized key management schemes. |
| open | [PairwiseCipher](../android/net/wifi/WifiConfiguration.PairwiseCipher.md) Recognized pairwise ciphers for WPA. |
| open | [Protocol](../android/net/wifi/WifiConfiguration.Protocol.md) Recognized security protocols. |
| --- | --- |
| open | [Status](../android/net/wifi/WifiConfiguration.Status.md) Possible status of a network configuration. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_AUTO](../android/net/wifi/WifiConfiguration.md) Let the wifi framework automatically decide the MAC randomization strategy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_NONE](../android/net/wifi/WifiConfiguration.md) Use factory MAC when connecting to this network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_NON_PERSISTENT](../android/net/wifi/WifiConfiguration.md) Use a randomly generated MAC address for connections to this network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANDOMIZATION_PERSISTENT](../android/net/wifi/WifiConfiguration.md) Generate a randomized MAC once and reuse it for all connections to this network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_DPP](../android/net/wifi/WifiConfiguration.md) Security type for Easy Connect (DPP) network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP](../android/net/wifi/WifiConfiguration.md) Security type for an EAP network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_SUITE_B](../android/net/wifi/WifiConfiguration.md) Security type for a WPA3-Enterprise in 192-bit security network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_WPA3_ENTERPRISE](../android/net/wifi/WifiConfiguration.md) Security type for a WPA3-Enterprise network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](../android/net/wifi/WifiConfiguration.md) Security type for a WPA3-Enterprise in 192-bit security network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OPEN](../android/net/wifi/WifiConfiguration.md) Security type for an open network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OWE](../android/net/wifi/WifiConfiguration.md) Security type for an OWE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_PSK](../android/net/wifi/WifiConfiguration.md) Security type for a PSK network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_SAE](../android/net/wifi/WifiConfiguration.md) Security type for an SAE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WAPI_CERT](../android/net/wifi/WifiConfiguration.md) Security type for a WAPI Certificate network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WAPI_PSK](../android/net/wifi/WifiConfiguration.md) Security type for a WAPI PSK network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WEP](../android/net/wifi/WifiConfiguration.md) Security type for a WEP network. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiConfiguration](../android/net/wifi/WifiConfiguration.md))`()` <br /> |
| [WifiConfiguration](../android/net/wifi/WifiConfiguration.md))`(`source:` ` [WifiConfiguration](../android/net/wifi/WifiConfiguration.md)`)` Copy constructor |

| Public methods ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ProxyInfo](../android/net/ProxyInfo.md)! | [getHttpProxy](../android/net/wifi/WifiConfiguration.md))`()` Returns the HTTP proxy used by this object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getKey](../android/net/wifi/WifiConfiguration.md))`()` Return a String that can be used to uniquely identify this WifiConfiguration. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMacRandomizationSetting](../android/net/wifi/WifiConfiguration.md))`()` Get the MAC randomization setting for this network. |
| --- | --- |
| open [MacAddress](../android/net/MacAddress.md) | [getRandomizedMacAddress](../android/net/wifi/WifiConfiguration.md))`()` Returns MAC address set to be the local randomized MAC address. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDppConfigurator](../android/net/wifi/WifiConfiguration.md))`()` To check if this WifiConfiguration supports configuring a peer Enrollee device with SECURITY_TYPE_DPP |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPasspoint](../android/net/wifi/WifiConfiguration.md))`()` Identify if this configuration represents a Passpoint network |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHttpProxy](../android/net/wifi/WifiConfiguration.md))`(`httpProxy:` ` [ProxyInfo](../android/net/ProxyInfo.md)!`)` Set the [ProxyInfo](../android/net/ProxyInfo.md) for this WifiConfiguration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIpConfiguration](../android/net/wifi/WifiConfiguration.md))`(`ipConfiguration:` ` [IpConfiguration](../android/net/IpConfiguration.md)?`)` Set the [IpConfiguration](../android/net/IpConfiguration.md) for this network. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMacRandomizationSetting](../android/net/wifi/WifiConfiguration.md))`(`macRandomizationSetting:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the MAC randomization setting for this network. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSecurityParams](../android/net/wifi/WifiConfiguration.md))`(`securityType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the various security params to correspond to the provided security type. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/wifi/WifiConfiguration.md))`()` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [BSSID](../android/net/wifi/WifiConfiguration.md) When set, this network configuration entry should only be used when associating with the AP having the specified BSSID. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [FQDN](../android/net/wifi/WifiConfiguration.md) Fully qualified domain name of a Passpoint configuration |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [SSID](../android/net/wifi/WifiConfiguration.md) The network's SSID. |
| --- | --- |
| [BitSet](../java/util/BitSet.md) | [allowedAuthAlgorithms](../android/net/wifi/WifiConfiguration.md) The set of authentication protocols supported by this configuration. |
| [BitSet](../java/util/BitSet.md) | [allowedGroupCiphers](../android/net/wifi/WifiConfiguration.md) The set of group ciphers supported by this configuration. |
| [BitSet](../java/util/BitSet.md) | [allowedGroupManagementCiphers](../android/net/wifi/WifiConfiguration.md) The set of group management ciphers supported by this configuration. |
| --- | --- |
| [BitSet](../java/util/BitSet.md) | [allowedKeyManagement](../android/net/wifi/WifiConfiguration.md) The set of key management protocols supported by this configuration. |
| [BitSet](../java/util/BitSet.md) | [allowedPairwiseCiphers](../android/net/wifi/WifiConfiguration.md) The set of pairwise ciphers for WPA supported by this configuration. |
| [BitSet](../java/util/BitSet.md) | [allowedProtocols](../android/net/wifi/WifiConfiguration.md) The set of security protocols supported by this configuration. |
| --- | --- |
| [BitSet](../java/util/BitSet.md) | [allowedSuiteBCiphers](../android/net/wifi/WifiConfiguration.md) The set of SuiteB ciphers supported by this configuration. |
| [WifiEnterpriseConfig](../android/net/wifi/WifiEnterpriseConfig.md)! | [enterpriseConfig](../android/net/wifi/WifiConfiguration.md) The enterprise configuration details specifying the EAP method, certificates and other settings associated with the EAP. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hiddenSSID](../android/net/wifi/WifiConfiguration.md) This is a network that does not broadcast its SSID, so an SSID-specific probe request must be used for scans. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHomeProviderNetwork](../android/net/wifi/WifiConfiguration.md) Flag indicating if this network is provided by a home Passpoint provider or a roaming Passpoint provider. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [networkId](../android/net/wifi/WifiConfiguration.md) The ID number that the supplicant uses to identify this network configuration entry. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [preSharedKey](../android/net/wifi/WifiConfiguration.md) Pre-shared key for use with WPA-PSK. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [priority](../android/net/wifi/WifiConfiguration.md) Priority determines the preference given to a network by`wpa_supplicant`when choosing an access point with which to associate. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [providerFriendlyName](../android/net/wifi/WifiConfiguration.md) Name of Passpoint credential provider |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [roamingConsortiumIds](../android/net/wifi/WifiConfiguration.md) Roaming Consortium Id list for Passpoint credential; identifies a set of networks where Passpoint credential will be considered valid |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [status](../android/net/wifi/WifiConfiguration.md) The current status of this network configuration entry. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [wepKeys](../android/net/wifi/WifiConfiguration.md) Four WEP keys. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [wepTxKeyIndex](../android/net/wifi/WifiConfiguration.md) Default WEP key index, ranging from 0 to 3. |
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

**Deprecated:** *Use the [SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](../android/net/wifi/WifiConfiguration.md) constant (which is the same value).*

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

Security type for a WPA3-Enterprise in 192-bit security network. This is the same as [SECURITY_TYPE_EAP_SUITE_B](../android/net/wifi/WifiConfiguration.md) and uses the same value. 

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
| `source` | [WifiConfiguration](../android/net/wifi/WifiConfiguration.md):This value cannot be`null`. |

## Public methods

### getHttpProxy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHttpProxy(): ProxyInfo!
```

Returns the HTTP proxy used by this object.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ProxyInfo](../android/net/ProxyInfo.md)! | a [httpProxy](../android/net/ProxyInfo.md) representing the proxy specified by this WifiConfiguration, or`null`if no proxy is specified. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.WifiConfiguration#RANDOMIZATION_NONE](../android/net/wifi/WifiConfiguration.md), [android.net.wifi.WifiConfiguration#RANDOMIZATION_PERSISTENT](../android/net/wifi/WifiConfiguration.md), [android.net.wifi.WifiConfiguration#RANDOMIZATION_NON_PERSISTENT](../android/net/wifi/WifiConfiguration.md), or [android.net.wifi.WifiConfiguration#RANDOMIZATION_AUTO](../android/net/wifi/WifiConfiguration.md) |

### getRandomizedMacAddress

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRandomizedMacAddress(): MacAddress
```

Returns MAC address set to be the local randomized MAC address. Depending on user preference, the device may or may not use the returned MAC address for connections to this network.

Information is restricted to Device Owner, Profile Owner, and Carrier apps (which will only obtain addresses for configurations which they create). Other callers will receive a default "02:00:00:00:00:00" MAC address.

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------|
| [MacAddress](../android/net/MacAddress.md) | This value cannot be`null`. |

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

Set the [ProxyInfo](../android/net/ProxyInfo.md) for this WifiConfiguration. This method should only be used by a device owner or profile owner. When other apps attempt to save a [WifiConfiguration](../android/net/wifi/WifiConfiguration.md) with modified proxy settings, the methods [WifiManager.addNetwork](../android/net/wifi/WifiManager.md))and [WifiManager.updateNetwork](../android/net/wifi/WifiManager.md))fail and return`-1`.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `httpProxy` | [ProxyInfo](../android/net/ProxyInfo.md)!: [ProxyInfo](../android/net/ProxyInfo.md) representing the httpProxy to be used by this WifiConfiguration. Setting this to`null`will explicitly set no proxy, removing any proxy that was previously set. |

### setIpConfiguration

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIpConfiguration(ipConfiguration: IpConfiguration?): Unit
```

Set the [IpConfiguration](../android/net/IpConfiguration.md) for this network.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ipConfiguration` | [IpConfiguration](../android/net/IpConfiguration.md)?:a [IpConfiguration](../android/net/IpConfiguration.md) to use for this Wi-Fi configuration, or`null`to use the default configuration. |

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
| `macRandomizationSetting` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.net.wifi.WifiConfiguration#RANDOMIZATION_NONE](../android/net/wifi/WifiConfiguration.md), [android.net.wifi.WifiConfiguration#RANDOMIZATION_PERSISTENT](../android/net/wifi/WifiConfiguration.md), [android.net.wifi.WifiConfiguration#RANDOMIZATION_NON_PERSISTENT](../android/net/wifi/WifiConfiguration.md), or [android.net.wifi.WifiConfiguration#RANDOMIZATION_AUTO](../android/net/wifi/WifiConfiguration.md) |

### setSecurityParams

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSecurityParams(securityType: Int): Unit
```

Set the various security params to correspond to the provided security type. This is accomplished by setting the various BitSets exposed in WifiConfiguration. 
This API would clear existing security types and add a default one. Before calling this API with [SECURITY_TYPE_DPP](../android/net/wifi/WifiConfiguration.md) as securityType, call [android.net.wifi.WifiManager#isEasyConnectDppAkmSupported()](../android/net/wifi/WifiManager.md))} 

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

The set of authentication protocols supported by this configuration. See [AuthAlgorithm](../android/net/wifi/WifiConfiguration.AuthAlgorithm.md) for descriptions of the values. Defaults to automatic selection. 

### allowedGroupCiphers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedGroupCiphers: BitSet
```

The set of group ciphers supported by this configuration. See [GroupCipher](../android/net/wifi/WifiConfiguration.GroupCipher.md) for descriptions of the values. Defaults to CCMP TKIP WEP104 WEP40. 

### allowedGroupManagementCiphers

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedGroupManagementCiphers: BitSet
```

The set of group management ciphers supported by this configuration. See [GroupMgmtCipher](../android/net/wifi/WifiConfiguration.GroupMgmtCipher.md) for descriptions of the values. 

### allowedKeyManagement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedKeyManagement: BitSet
```

The set of key management protocols supported by this configuration. See [KeyMgmt](../android/net/wifi/WifiConfiguration.KeyMgmt.md) for descriptions of the values. Defaults to WPA-PSK WPA-EAP. 

### allowedPairwiseCiphers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedPairwiseCiphers: BitSet
```

The set of pairwise ciphers for WPA supported by this configuration. See [PairwiseCipher](../android/net/wifi/WifiConfiguration.PairwiseCipher.md) for descriptions of the values. Defaults to CCMP TKIP. 

### allowedProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var allowedProtocols: BitSet
```

The set of security protocols supported by this configuration. See [Protocol](../android/net/wifi/WifiConfiguration.Protocol.md) for descriptions of the values. Defaults to WPA RSN. 

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

- [android.net.wifi.WifiConfiguration.Status](../android/net/wifi/WifiConfiguration.Status.md) 

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
