# WifiInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiInfo

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiInfo "View this page in Java") 

```
open class WifiInfo : Parcelable, TransportInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.WifiInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#) |

Describes the state of any Wi-Fi connection that is active or is in the process of being set up. In the connected state, access to location sensitive fields requires the same permissions as [WifiManager.getScanResults](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getScanResults()). If such access is not allowed, [getSSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getSSID())will return [WifiManager.UNKNOWN_SSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#UNKNOWN_SSID:kotlin.String) and [getBSSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getBSSID())will return`"02:00:00:00:00:00"`. [getApMldMacAddress()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getApMldMacAddress())will return null. [getNetworkId()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getNetworkId())will return`-1`. [getPasspointFqdn()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getPasspointFqdn())will return null. [getPasspointProviderFriendlyName()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getPasspointProviderFriendlyName())will return null. [getInformationElements()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getInformationElements())will return null. [getMacAddress()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getMacAddress())will return`"02:00:00:00:00:00"`.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo.Builder) Builder for WifiInfo |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FREQUENCY_UNITS](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#FREQUENCY_UNITS:kotlin.String) Frequency in MHz |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LINK_SPEED_UNITS](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNITS:kotlin.String) The unit in which links speeds are expressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) Constant for unknown link speed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_DPP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_DPP:kotlin.Int) Security type for Easy Connect (DPP) network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP:kotlin.Int) Security type for an EAP network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_WPA3_ENTERPRISE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE:kotlin.Int) Security type for a WPA3-Enterprise network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT:kotlin.Int) Security type for a WPA3-Enterprise in 192-bit security network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OPEN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_OPEN:kotlin.Int) Security type for an open network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OSEN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_OSEN:kotlin.Int) Security type for an OSEN network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OWE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_OWE:kotlin.Int) Security type for an OWE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_PASSPOINT_R1_R2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PASSPOINT_R1_R2:kotlin.Int) Security type for a Passpoint R1/R2 network, where TKIP and WEP are not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_PASSPOINT_R3](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PASSPOINT_R3:kotlin.Int) Security type for a Passpoint R3 network, where TKIP and WEP are not allowed, and PMF must be set to Required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_PSK](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PSK:kotlin.Int) Security type for a PSK network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_SAE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_SAE:kotlin.Int) Security type for an SAE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_UNKNOWN:kotlin.Int) Unknown security type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WAPI_CERT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WAPI_CERT:kotlin.Int) Security type for a WAPI Certificate network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WAPI_PSK](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WAPI_PSK:kotlin.Int) Security type for a WAPI PSK network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WEP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WEP:kotlin.Int) Security type for a WEP network. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MloLink](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink)!\> | [getAffiliatedMloLinks](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getAffiliatedMloLinks())`()` Return the Multi-Link Operation (MLO) affiliated Links for Wi-Fi 7 access points. |
| open [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | [getApMldMacAddress](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getApMldMacAddress())`()` Return the Multi-Link Device (MLD) MAC Address for the connected access point. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getApMloLinkId](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getApMloLinkId())`()` Return the access point Multi-Link Operation (MLO) link-id for Wi-Fi 7 access points. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getApplicableRedactions](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getApplicableRedactions())`()` Returns a bitmask of all the applicable redactions (based on the permissions held by the receiving app) to be performed on this TransportInfo. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MloLink](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink)!\> | [getAssociatedMloLinks](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getAssociatedMloLinks())`()` Return the associated Multi-Link Operation (MLO) Links for Wi-Fi 7 access points. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBSSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getBSSID())`()` Return the basic service set identifier (BSSID) of the current access point. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentSecurityType](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getCurrentSecurityType())`()` Returns the security type of the current 802. |
| openstatic [NetworkInfo.DetailedState](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.DetailedState.html#)! | [getDetailedStateOf](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getDetailedStateOf(android.net.wifi.SupplicantState))`(`suppState:` ` [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState)!`)` Map a supplicant state into a fine-grained network connectivity state. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFrequency](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getFrequency())`()` Returns the current frequency in [FREQUENCY_UNITS](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#FREQUENCY_UNITS:kotlin.String). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getHiddenSSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getHiddenSSID())`()` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult.InformationElement](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.InformationElement)!\>? | [getInformationElements](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getInformationElements())`()` Get all information elements found in the beacon of the connected bssid. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIpAddress](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getIpAddress())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLinkSpeed](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getLinkSpeed())`()` Returns the current link speed in [LINK_SPEED_UNITS](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNITS:kotlin.String). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMacAddress](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getMacAddress())`()` Returns the MAC address used for this connection. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSupportedRxLinkSpeedMbps](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getMaxSupportedRxLinkSpeedMbps())`()` Returns the maximum supported receive link speed in Mbps |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSupportedTxLinkSpeedMbps](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getMaxSupportedTxLinkSpeedMbps())`()` Returns the maximum supported transmit link speed in Mbps |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkId](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getNetworkId())`()` Each configured network has a unique small integer ID, used to identify the network. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPasspointFqdn](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getPasspointFqdn())`()` Returns the Fully Qualified Domain Name of the network if it is a Passpoint network. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPasspointProviderFriendlyName](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getPasspointProviderFriendlyName())`()` Returns the Provider Friendly Name of the network if it is a Passpoint network. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPasspointUniqueId](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getPasspointUniqueId())`()` Get the Passpoint unique identifier for the current connection |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssi](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getRssi())`()` Returns the received signal strength indicator of the current 802. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRxLinkSpeedMbps](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getRxLinkSpeedMbps())`()` Returns the current receive link speed in Mbps. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getSSID())`()` Returns the service set identifier (SSID) of the current 802. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionId](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getSubscriptionId())`()` If this network is provisioned by a carrier, returns subscription Id corresponding to the associated SIM on the device. |
| open [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState)! | [getSupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getSupplicantState())`()` Return the detailed state of the supplicant's negotiation with an access point, in the form of a [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState) object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTxLinkSpeedMbps](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getTxLinkSpeedMbps())`()` Returns the current transmit link speed in Mbps. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWifiStandard](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getWifiStandard())`()` Get connection Wi-Fi standard |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#hashCode())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRestricted](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#isRestricted())`()` Returns true if the current Wifi network is a restricted network, false otherwise. |
| open [WifiInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#) | [makeCopy](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#makeCopy(kotlin.Long))`(`redactions:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a copy of a [WifiInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#) with some fields redacted based on the permissions held by the receiving app. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#toString())`()` <br /> |

## Constants

### FREQUENCY_UNITS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FREQUENCY_UNITS: String
```

Frequency in MHz 

 Value: "MHz"

### LINK_SPEED_UNITS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINK_SPEED_UNITS: String
```

The unit in which links speeds are expressed. 

 Value: "Mbps"

### LINK_SPEED_UNKNOWN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINK_SPEED_UNKNOWN: Int
```

Constant for unknown link speed. 

 Value: -1

### SECURITY_TYPE_DPP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_DPP: Int
```

Security type for Easy Connect (DPP) network 

 Value: 13

### SECURITY_TYPE_EAP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_EAP: Int
```

Security type for an EAP network. 

 Value: 3

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

Security type for a WPA3-Enterprise in 192-bit security network. 

 Value: 5

### SECURITY_TYPE_OPEN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_OPEN: Int
```

Security type for an open network. 

 Value: 0

### SECURITY_TYPE_OSEN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_OSEN: Int
```

Security type for an OSEN network. 

 Value: 10

### SECURITY_TYPE_OWE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_OWE: Int
```

Security type for an OWE network. 

 Value: 6

### SECURITY_TYPE_PASSPOINT_R1_R2

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_PASSPOINT_R1_R2: Int
```

Security type for a Passpoint R1/R2 network, where TKIP and WEP are not allowed. 

 Value: 11

### SECURITY_TYPE_PASSPOINT_R3

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_PASSPOINT_R3: Int
```

Security type for a Passpoint R3 network, where TKIP and WEP are not allowed, and PMF must be set to Required. 

 Value: 12

### SECURITY_TYPE_PSK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_PSK: Int
```

Security type for a PSK network. 

 Value: 2

### SECURITY_TYPE_SAE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_SAE: Int
```

Security type for an SAE network. 

 Value: 4

### SECURITY_TYPE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_UNKNOWN: Int
```

Unknown security type. 

 Value: -1

### SECURITY_TYPE_WAPI_CERT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WAPI_CERT: Int
```

Security type for a WAPI Certificate network. 

 Value: 8

### SECURITY_TYPE_WAPI_PSK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WAPI_PSK: Int
```

Security type for a WAPI PSK network. 

 Value: 7

### SECURITY_TYPE_WEP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_TYPE_WEP: Int
```

Security type for a WEP network. 

 Value: 1

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAffiliatedMloLinks

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAffiliatedMloLinks(): MutableList<MloLink!>
```

Return the Multi-Link Operation (MLO) affiliated Links for Wi-Fi 7 access points. i.e. when [getWifiStandard()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getWifiStandard())returns [ScanResult.WIFI_STANDARD_11BE](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11BE:kotlin.Int). Affiliated links are the links supported by the Access Point Multi Link Device (AP MLD). The Station Multi Link Device (STA MLD) gathers affiliated link information from scan results. Depending on Station's capability, it associates to all or a subset of affiliated links.

**Note:** [getAssociatedMloLinks()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getAssociatedMloLinks())returns associated links.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MloLink](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink)!> | List of affiliated MLO links, or an empty list if access point is not Wi-Fi 7 This value cannot be`null`. |

### getApMldMacAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApMldMacAddress(): MacAddress?
```

Return the Multi-Link Device (MLD) MAC Address for the connected access point.

The returned MLD MAC Address will be`null`in the following cases: There is no network currently connected The connected access point is not an MLD access point, i.e. [getWifiStandard()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getWifiStandard())returns [ScanResult.WIFI_STANDARD_11BE](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11BE:kotlin.Int). The caller has insufficient permissions to access the access point MLD MAC Address.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | the MLD Mac address |

### getApMloLinkId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApMloLinkId(): Int
```

Return the access point Multi-Link Operation (MLO) link-id for Wi-Fi 7 access points. i.e. [getWifiStandard()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getWifiStandard())returns [ScanResult.WIFI_STANDARD_11BE](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11BE:kotlin.Int), otherwise return [MloLink.INVALID_MLO_LINK_ID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int). Valid values are 0-15 as described in IEEE 802.11be Specification, section 9.4.2.295b.2.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MloLink.INVALID_MLO_LINK_ID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int) or a valid value (0-15). Value is between [android.net.wifi.MloLink#INVALID_MLO_LINK_ID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int) and android.net.wifi.MloLink#MAX_MLO_LINK_ID inclusive |

### getApplicableRedactions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApplicableRedactions(): Long
```

Returns a bitmask of all the applicable redactions (based on the permissions held by the receiving app) to be performed on this TransportInfo.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | bitmask of redactions applicable on this instance. |

### getAssociatedMloLinks

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAssociatedMloLinks(): MutableList<MloLink!>
```

Return the associated Multi-Link Operation (MLO) Links for Wi-Fi 7 access points. i.e. when [getWifiStandard()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getWifiStandard())returns [ScanResult.WIFI_STANDARD_11BE](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11BE:kotlin.Int). Affiliated links are the links supported by the Access Point Multi Link Device (AP MLD). The Station Multi Link Device (STA MLD) gathers affiliated link information from scan results. Depending on Station's capability, it associates to all or a subset of affiliated links.

**Note:** [getAffiliatedMloLinks()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#getAffiliatedMloLinks())returns affiliated links.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MloLink](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink)!> | List of associated MLO links, or an empty list if access point is not a multi-link device. This value cannot be`null`. |

### getBSSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBSSID(): String!
```

Return the basic service set identifier (BSSID) of the current access point. In case of Multi Link Operation (MLO), the BSSID corresponds to the BSSID of the link used for association.

The BSSID may be`null`, if there is no network currently connected.`"02:00:00:00:00:00"`, if the caller has insufficient permissions to access the BSSID.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the BSSID, in the form of a six-byte MAC address:`XX:XX:XX:XX:XX:XX` |

### getCurrentSecurityType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentSecurityType(): Int
```

Returns the security type of the current 802.11 network connection.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the security type, or [SECURITY_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_UNKNOWN:kotlin.Int) if not currently connected. Value is [android.net.wifi.WifiInfo#SECURITY_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_UNKNOWN:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_OPEN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_OPEN:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_WEP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WEP:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_PSK](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PSK:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_SAE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_SAE:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_OWE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_OWE:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_WAPI_PSK](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WAPI_PSK:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_WAPI_CERT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_WAPI_CERT:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_PASSPOINT_R1_R2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PASSPOINT_R1_R2:kotlin.Int), [android.net.wifi.WifiInfo#SECURITY_TYPE_PASSPOINT_R3](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_PASSPOINT_R3:kotlin.Int), or [android.net.wifi.WifiInfo#SECURITY_TYPE_DPP](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#SECURITY_TYPE_DPP:kotlin.Int) |

### getDetailedStateOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDetailedStateOf(suppState: SupplicantState!): NetworkInfo.DetailedState!
```

Map a supplicant state into a fine-grained network connectivity state.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `suppState` | [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState)!:the supplicant state |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [NetworkInfo.DetailedState](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.DetailedState.html#)! | the corresponding [DetailedState](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.DetailedState.html#) |

### getFrequency

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrequency(): Int
```

Returns the current frequency in [FREQUENCY_UNITS](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#FREQUENCY_UNITS:kotlin.String). In case of Multi Link Operation (MLO), returned value is the frequency of the associated link with the highest RSSI.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the frequency. |

**See Also**

- [#FREQUENCY_UNITS](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#FREQUENCY_UNITS:kotlin.String) 

### getHiddenSSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHiddenSSID(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this network does not broadcast its SSID, so an SSID-specific probe request must be used for scans. |

### getInformationElements

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInformationElements(): MutableList<ScanResult.InformationElement!>?
```

Get all information elements found in the beacon of the connected bssid.

The information elements will be`null`if there is no network currently connected or if the caller has insufficient permissions to access the info elements.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ScanResult.InformationElement](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.InformationElement)!>? | List of information elements [ScanResult.InformationElement](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.InformationElement) or null. |

### getIpAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIpAddress(): Int
```

**Deprecated:** *Use the methods on [android.net.LinkProperties](https://developer.android.com/reference/kotlin/android/net/LinkProperties.html#) which can be obtained either via [NetworkCallback.onLinkPropertiesChanged(Network, LinkProperties)](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback.html#onLinkPropertiesChanged(android.net.Network,%20android.net.LinkProperties))or [ConnectivityManager.getLinkProperties(Network)](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#getLinkProperties(android.net.Network)).* 

### getLinkSpeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLinkSpeed(): Int
```

Returns the current link speed in [LINK_SPEED_UNITS](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNITS:kotlin.String). In case of Multi Link Operation (MLO), returned value is the current link speed of the associated link with the highest RSSI.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the link speed or [LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) if link speed is unknown. |

**See Also**

- [#LINK_SPEED_UNITS](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNITS:kotlin.String)
- [#LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) 

### getMacAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMacAddress(): String!
```

Returns the MAC address used for this connection. In case of Multi Link Operation (MLO), returned value is the Station MLD MAC address.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | MAC address of the connection or`"02:00:00:00:00:00"`if the caller has insufficient permission. Requires`android.Manifest.permission#LOCAL_MAC_ADDRESS`and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String). |

### getMaxSupportedRxLinkSpeedMbps

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxSupportedRxLinkSpeedMbps(): Int
```

Returns the maximum supported receive link speed in Mbps

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the max supported Rx link speed or [LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) if link speed is unknown. @see #LINK_SPEED_UNKNOWN |

### getMaxSupportedTxLinkSpeedMbps

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxSupportedTxLinkSpeedMbps(): Int
```

Returns the maximum supported transmit link speed in Mbps

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the max supported tx link speed or [LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) if link speed is unknown. @see #LINK_SPEED_UNKNOWN |

### getNetworkId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetworkId(): Int
```

Each configured network has a unique small integer ID, used to identify the network. This method returns the ID for the currently connected network.

The networkId may be`-1`if there is no currently connected network or if the caller has insufficient permissions to access the network ID.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the network ID. |

### getPasspointFqdn

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPasspointFqdn(): String?
```

Returns the Fully Qualified Domain Name of the network if it is a Passpoint network.

The FQDN may be`null`if no network currently connected, currently connected network is not passpoint network or the caller has insufficient permissions to access the FQDN. 

### getPasspointProviderFriendlyName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPasspointProviderFriendlyName(): String?
```

Returns the Provider Friendly Name of the network if it is a Passpoint network.

The Provider Friendly Name may be`null`if no network currently connected, currently connected network is not passpoint network or the caller has insufficient permissions to access the Provider Friendly Name. 

### getPasspointUniqueId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPasspointUniqueId(): String?
```

Get the Passpoint unique identifier for the current connection

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Passpoint unique identifier, or null if this connection is not Passpoint. |

### getRssi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRssi(): Int
```

Returns the received signal strength indicator of the current 802.11 network, in dBm. In case of Multi Link Operation (MLO), returned RSSI is the highest of all associated links.

Use android.net.wifi.WifiManager#calculateSignalLevel to convert this number into an absolute signal level which can be displayed to a user.

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the RSSI. |

### getRxLinkSpeedMbps

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRxLinkSpeedMbps(): Int
```

Returns the current receive link speed in Mbps. In case of Multi Link Operation (MLO), returned value is the receive link speed of the associated link with the highest RSSI.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Rx link speed or [LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) if link speed is unknown. Value is -1 or greater |

**See Also**

- [#LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) 

### getSSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSSID(): String!
```

Returns the service set identifier (SSID) of the current 802.11 network.

If the SSID can be decoded as UTF-8, it will be returned surrounded by double quotation marks. Otherwise, it is returned as a string of hex digits. The SSID may be [WifiManager.UNKNOWN_SSID](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#UNKNOWN_SSID:kotlin.String), if there is no network currently connected or if the caller has insufficient permissions to access the SSID.

Prior to [android.os.Build.VERSION_CODES#JELLY_BEAN_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int), this method always returned the SSID with no quotes around it.

| Return ||
|-----------------------------------------------------------------------------------|-----------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the SSID. |

### getSubscriptionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubscriptionId(): Int
```

If this network is provisioned by a carrier, returns subscription Id corresponding to the associated SIM on the device. If this network is not provisioned by a carrier, returns [android.telephony.SubscriptionManager#INVALID_SUBSCRIPTION_ID](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#INVALID_SUBSCRIPTION_ID:kotlin.Int) 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setSubscriptionId(kotlin.Int))
- [android.telephony.SubscriptionInfo#getSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo.html#getSubscriptionId()) 

### getSupplicantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSupplicantState(): SupplicantState!
```

Return the detailed state of the supplicant's negotiation with an access point, in the form of a [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState) object.

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState)! | the current [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState) |

### getTxLinkSpeedMbps

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTxLinkSpeedMbps(): Int
```

Returns the current transmit link speed in Mbps. In case of Multi Link Operation (MLO), returned value is the current transmit link speed of the associated link with the highest RSSI.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Tx link speed or [LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) if link speed is unknown. Value is -1 or greater |

**See Also**

- [#LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) 

### getWifiStandard

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWifiStandard(): Int
```

Get connection Wi-Fi standard

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the connection Wi-Fi standard Value is [android.net.wifi.ScanResult#WIFI_STANDARD_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_UNKNOWN:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_LEGACY](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_LEGACY:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_11N](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11N:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_11AC](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11AC:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_11AX](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11AX:kotlin.Int), [android.net.wifi.ScanResult#WIFI_STANDARD_11AD](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11AD:kotlin.Int), or [android.net.wifi.ScanResult#WIFI_STANDARD_11BE](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_STANDARD_11BE:kotlin.Int) |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isRestricted

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRestricted(): Boolean
```

Returns true if the current Wifi network is a restricted network, false otherwise. A restricted network has its [NetworkCapabilities.NET_CAPABILITY_NOT_RESTRICTED](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_NOT_RESTRICTED:kotlin.Int) capability removed. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setRestricted(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion.Builder#setRestricted(kotlin.Boolean)) 

### makeCopy

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun makeCopy(redactions: Long): WifiInfo
```

Create a copy of a [WifiInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#) with some fields redacted based on the permissions held by the receiving app.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `redactions` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):bitmask of redactions that needs to be performed on this instance. |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [WifiInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#) | Copy of this instance with the necessary redactions. This value cannot be`null`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
