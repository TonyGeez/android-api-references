# WifiInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiInfo

Kotlin| [Java](../android/net/wifi/WifiInfo.md) 
| --- | --- |

```
open class WifiInfo : Parcelable, TransportInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.WifiInfo](../android/net/wifi/WifiInfo.md) |

Describes the state of any Wi-Fi connection that is active or is in the process of being set up. In the connected state, access to location sensitive fields requires the same permissions as [WifiManager.getScanResults](../android/net/wifi/WifiManager.md)). If such access is not allowed, [getSSID](../android/net/wifi/WifiInfo.md))will return [WifiManager.UNKNOWN_SSID](../android/net/wifi/WifiManager.md) and [getBSSID](../android/net/wifi/WifiInfo.md))will return`"02:00:00:00:00:00"`. [getApMldMacAddress()](../android/net/wifi/WifiInfo.md))will return null. [getNetworkId()](../android/net/wifi/WifiInfo.md))will return`-1`. [getPasspointFqdn()](../android/net/wifi/WifiInfo.md))will return null. [getPasspointProviderFriendlyName()](../android/net/wifi/WifiInfo.md))will return null. [getInformationElements()](../android/net/wifi/WifiInfo.md))will return null. [getMacAddress()](../android/net/wifi/WifiInfo.md))will return`"02:00:00:00:00:00"`.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/wifi/WifiInfo.Builder.md) Builder for WifiInfo |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FREQUENCY_UNITS](../android/net/wifi/WifiInfo.md) Frequency in MHz |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LINK_SPEED_UNITS](../android/net/wifi/WifiInfo.md) The unit in which links speeds are expressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) Constant for unknown link speed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_DPP](../android/net/wifi/WifiInfo.md) Security type for Easy Connect (DPP) network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP](../android/net/wifi/WifiInfo.md) Security type for an EAP network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_WPA3_ENTERPRISE](../android/net/wifi/WifiInfo.md) Security type for a WPA3-Enterprise network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](../android/net/wifi/WifiInfo.md) Security type for a WPA3-Enterprise in 192-bit security network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OPEN](../android/net/wifi/WifiInfo.md) Security type for an open network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OSEN](../android/net/wifi/WifiInfo.md) Security type for an OSEN network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_OWE](../android/net/wifi/WifiInfo.md) Security type for an OWE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_PASSPOINT_R1_R2](../android/net/wifi/WifiInfo.md) Security type for a Passpoint R1/R2 network, where TKIP and WEP are not allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_PASSPOINT_R3](../android/net/wifi/WifiInfo.md) Security type for a Passpoint R3 network, where TKIP and WEP are not allowed, and PMF must be set to Required. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_PSK](../android/net/wifi/WifiInfo.md) Security type for a PSK network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_SAE](../android/net/wifi/WifiInfo.md) Security type for an SAE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_UNKNOWN](../android/net/wifi/WifiInfo.md) Unknown security type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WAPI_CERT](../android/net/wifi/WifiInfo.md) Security type for a WAPI Certificate network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WAPI_PSK](../android/net/wifi/WifiInfo.md) Security type for a WAPI PSK network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_TYPE_WEP](../android/net/wifi/WifiInfo.md) Security type for a WEP network. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/wifi/WifiInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MloLink](../android/net/wifi/MloLink.md)!\> | [getAffiliatedMloLinks](../android/net/wifi/WifiInfo.md))`()` Return the Multi-Link Operation (MLO) affiliated Links for Wi-Fi 7 access points. |
| open [MacAddress](../android/net/MacAddress.md)? | [getApMldMacAddress](../android/net/wifi/WifiInfo.md))`()` Return the Multi-Link Device (MLD) MAC Address for the connected access point. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getApMloLinkId](../android/net/wifi/WifiInfo.md))`()` Return the access point Multi-Link Operation (MLO) link-id for Wi-Fi 7 access points. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getApplicableRedactions](../android/net/wifi/WifiInfo.md))`()` Returns a bitmask of all the applicable redactions (based on the permissions held by the receiving app) to be performed on this TransportInfo. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MloLink](../android/net/wifi/MloLink.md)!\> | [getAssociatedMloLinks](../android/net/wifi/WifiInfo.md))`()` Return the associated Multi-Link Operation (MLO) Links for Wi-Fi 7 access points. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBSSID](../android/net/wifi/WifiInfo.md))`()` Return the basic service set identifier (BSSID) of the current access point. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentSecurityType](../android/net/wifi/WifiInfo.md))`()` Returns the security type of the current 802. |
| openstatic [NetworkInfo.DetailedState](../android/net/NetworkInfo.DetailedState.md)! | [getDetailedStateOf](../android/net/wifi/WifiInfo.md))`(`suppState:` ` [SupplicantState](../android/net/wifi/SupplicantState.md)!`)` Map a supplicant state into a fine-grained network connectivity state. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFrequency](../android/net/wifi/WifiInfo.md))`()` Returns the current frequency in [FREQUENCY_UNITS](../android/net/wifi/WifiInfo.md). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getHiddenSSID](../android/net/wifi/WifiInfo.md))`()` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult.InformationElement](../android/net/wifi/ScanResult.InformationElement.md)!\>? | [getInformationElements](../android/net/wifi/WifiInfo.md))`()` Get all information elements found in the beacon of the connected bssid. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIpAddress](../android/net/wifi/WifiInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLinkSpeed](../android/net/wifi/WifiInfo.md))`()` Returns the current link speed in [LINK_SPEED_UNITS](../android/net/wifi/WifiInfo.md). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMacAddress](../android/net/wifi/WifiInfo.md))`()` Returns the MAC address used for this connection. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSupportedRxLinkSpeedMbps](../android/net/wifi/WifiInfo.md))`()` Returns the maximum supported receive link speed in Mbps |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSupportedTxLinkSpeedMbps](../android/net/wifi/WifiInfo.md))`()` Returns the maximum supported transmit link speed in Mbps |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkId](../android/net/wifi/WifiInfo.md))`()` Each configured network has a unique small integer ID, used to identify the network. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPasspointFqdn](../android/net/wifi/WifiInfo.md))`()` Returns the Fully Qualified Domain Name of the network if it is a Passpoint network. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPasspointProviderFriendlyName](../android/net/wifi/WifiInfo.md))`()` Returns the Provider Friendly Name of the network if it is a Passpoint network. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPasspointUniqueId](../android/net/wifi/WifiInfo.md))`()` Get the Passpoint unique identifier for the current connection |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssi](../android/net/wifi/WifiInfo.md))`()` Returns the received signal strength indicator of the current 802. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRxLinkSpeedMbps](../android/net/wifi/WifiInfo.md))`()` Returns the current receive link speed in Mbps. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSSID](../android/net/wifi/WifiInfo.md))`()` Returns the service set identifier (SSID) of the current 802. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionId](../android/net/wifi/WifiInfo.md))`()` If this network is provisioned by a carrier, returns subscription Id corresponding to the associated SIM on the device. |
| open [SupplicantState](../android/net/wifi/SupplicantState.md)! | [getSupplicantState](../android/net/wifi/WifiInfo.md))`()` Return the detailed state of the supplicant's negotiation with an access point, in the form of a [SupplicantState](../android/net/wifi/SupplicantState.md) object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTxLinkSpeedMbps](../android/net/wifi/WifiInfo.md))`()` Returns the current transmit link speed in Mbps. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWifiStandard](../android/net/wifi/WifiInfo.md))`()` Get connection Wi-Fi standard |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/wifi/WifiInfo.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRestricted](../android/net/wifi/WifiInfo.md))`()` Returns true if the current Wifi network is a restricted network, false otherwise. |
| --- | --- |
| open [WifiInfo](../android/net/wifi/WifiInfo.md) | [makeCopy](../android/net/wifi/WifiInfo.md))`(`redactions:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a copy of a [WifiInfo](../android/net/wifi/WifiInfo.md) with some fields redacted based on the permissions held by the receiving app. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/wifi/WifiInfo.md))`()` <br /> |

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

Return the Multi-Link Operation (MLO) affiliated Links for Wi-Fi 7 access points. i.e. when [getWifiStandard()](../android/net/wifi/WifiInfo.md))returns [ScanResult.WIFI_STANDARD_11BE](../android/net/wifi/ScanResult.md). Affiliated links are the links supported by the Access Point Multi Link Device (AP MLD). The Station Multi Link Device (STA MLD) gathers affiliated link information from scan results. Depending on Station's capability, it associates to all or a subset of affiliated links.

**Note:** [getAssociatedMloLinks()](../android/net/wifi/WifiInfo.md))returns associated links.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MloLink](../android/net/wifi/MloLink.md)!> | List of affiliated MLO links, or an empty list if access point is not Wi-Fi 7 This value cannot be`null`. |

### getApMldMacAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApMldMacAddress(): MacAddress?
```

Return the Multi-Link Device (MLD) MAC Address for the connected access point.

The returned MLD MAC Address will be`null`in the following cases: There is no network currently connected The connected access point is not an MLD access point, i.e. [getWifiStandard()](../android/net/wifi/WifiInfo.md))returns [ScanResult.WIFI_STANDARD_11BE](../android/net/wifi/ScanResult.md). The caller has insufficient permissions to access the access point MLD MAC Address.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [MacAddress](../android/net/MacAddress.md)? | the MLD Mac address |

### getApMloLinkId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApMloLinkId(): Int
```

Return the access point Multi-Link Operation (MLO) link-id for Wi-Fi 7 access points. i.e. [getWifiStandard()](../android/net/wifi/WifiInfo.md))returns [ScanResult.WIFI_STANDARD_11BE](../android/net/wifi/ScanResult.md), otherwise return [MloLink.INVALID_MLO_LINK_ID](../android/net/wifi/MloLink.md). Valid values are 0-15 as described in IEEE 802.11be Specification, section 9.4.2.295b.2.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MloLink.INVALID_MLO_LINK_ID](../android/net/wifi/MloLink.md) or a valid value (0-15). Value is between [android.net.wifi.MloLink#INVALID_MLO_LINK_ID](../android/net/wifi/MloLink.md) and android.net.wifi.MloLink#MAX_MLO_LINK_ID inclusive |

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

Return the associated Multi-Link Operation (MLO) Links for Wi-Fi 7 access points. i.e. when [getWifiStandard()](../android/net/wifi/WifiInfo.md))returns [ScanResult.WIFI_STANDARD_11BE](../android/net/wifi/ScanResult.md). Affiliated links are the links supported by the Access Point Multi Link Device (AP MLD). The Station Multi Link Device (STA MLD) gathers affiliated link information from scan results. Depending on Station's capability, it associates to all or a subset of affiliated links.

**Note:** [getAffiliatedMloLinks()](../android/net/wifi/WifiInfo.md))returns affiliated links.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MloLink](../android/net/wifi/MloLink.md)!> | List of associated MLO links, or an empty list if access point is not a multi-link device. This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the security type, or [SECURITY_TYPE_UNKNOWN](../android/net/wifi/WifiInfo.md) if not currently connected. Value is [android.net.wifi.WifiInfo#SECURITY_TYPE_UNKNOWN](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_OPEN](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_WEP](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_PSK](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_SAE](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_OWE](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_WAPI_PSK](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_WAPI_CERT](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_EAP_WPA3_ENTERPRISE_192_BIT](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_PASSPOINT_R1_R2](../android/net/wifi/WifiInfo.md), [android.net.wifi.WifiInfo#SECURITY_TYPE_PASSPOINT_R3](../android/net/wifi/WifiInfo.md), or [android.net.wifi.WifiInfo#SECURITY_TYPE_DPP](../android/net/wifi/WifiInfo.md) |

### getDetailedStateOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDetailedStateOf(suppState: SupplicantState!): NetworkInfo.DetailedState!
```

Map a supplicant state into a fine-grained network connectivity state.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `suppState` | [SupplicantState](../android/net/wifi/SupplicantState.md)!:the supplicant state |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [NetworkInfo.DetailedState](../android/net/NetworkInfo.DetailedState.md)! | the corresponding [DetailedState](../android/net/NetworkInfo.DetailedState.md) |

### getFrequency

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrequency(): Int
```

Returns the current frequency in [FREQUENCY_UNITS](../android/net/wifi/WifiInfo.md). In case of Multi Link Operation (MLO), returned value is the frequency of the associated link with the highest RSSI.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the frequency. |

**See Also**

- [#FREQUENCY_UNITS](../android/net/wifi/WifiInfo.md) 

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ScanResult.InformationElement](../android/net/wifi/ScanResult.InformationElement.md)!>? | List of information elements [ScanResult.InformationElement](../android/net/wifi/ScanResult.InformationElement.md) or null. |

### getIpAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIpAddress(): Int
```

**Deprecated:** *Use the methods on [android.net.LinkProperties](../android/net/LinkProperties.md) which can be obtained either via [NetworkCallback.onLinkPropertiesChanged(Network, LinkProperties)](../android/net/ConnectivityManager.NetworkCallback.md))or [ConnectivityManager.getLinkProperties(Network)](../android/net/ConnectivityManager.md)).* 

### getLinkSpeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLinkSpeed(): Int
```

Returns the current link speed in [LINK_SPEED_UNITS](../android/net/wifi/WifiInfo.md). In case of Multi Link Operation (MLO), returned value is the current link speed of the associated link with the highest RSSI.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the link speed or [LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) if link speed is unknown. |

**See Also**

- [#LINK_SPEED_UNITS](../android/net/wifi/WifiInfo.md)
- [#LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) 

### getMacAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMacAddress(): String!
```

Returns the MAC address used for this connection. In case of Multi Link Operation (MLO), returned value is the Station MLD MAC address.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | MAC address of the connection or`"02:00:00:00:00:00"`if the caller has insufficient permission. Requires`android.Manifest.permission#LOCAL_MAC_ADDRESS`and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md). |

### getMaxSupportedRxLinkSpeedMbps

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxSupportedRxLinkSpeedMbps(): Int
```

Returns the maximum supported receive link speed in Mbps

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the max supported Rx link speed or [LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) if link speed is unknown. @see #LINK_SPEED_UNKNOWN |

### getMaxSupportedTxLinkSpeedMbps

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxSupportedTxLinkSpeedMbps(): Int
```

Returns the maximum supported transmit link speed in Mbps

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the max supported tx link speed or [LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) if link speed is unknown. @see #LINK_SPEED_UNKNOWN |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Rx link speed or [LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) if link speed is unknown. Value is -1 or greater |

**See Also**

- [#LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) 

### getSSID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSSID(): String!
```

Returns the service set identifier (SSID) of the current 802.11 network.

If the SSID can be decoded as UTF-8, it will be returned surrounded by double quotation marks. Otherwise, it is returned as a string of hex digits. The SSID may be [WifiManager.UNKNOWN_SSID](../android/net/wifi/WifiManager.md), if there is no network currently connected or if the caller has insufficient permissions to access the SSID.

Prior to [android.os.Build.VERSION_CODES#JELLY_BEAN_MR1](../android/os/Build.VERSION_CODES.md), this method always returned the SSID with no quotes around it.

| Return ||
|-----------------------------------------------------------------------------------|-----------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the SSID. |

### getSubscriptionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubscriptionId(): Int
```

If this network is provisioned by a carrier, returns subscription Id corresponding to the associated SIM on the device. If this network is not provisioned by a carrier, returns [android.telephony.SubscriptionManager#INVALID_SUBSCRIPTION_ID](../android/telephony/SubscriptionManager.md) 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setSubscriptionId(int)](../android/net/wifi/WifiNetworkSuggestion.Builder.md))
- [android.telephony.SubscriptionInfo#getSubscriptionId()](../android/telephony/SubscriptionInfo.md)) 

### getSupplicantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSupplicantState(): SupplicantState!
```

Return the detailed state of the supplicant's negotiation with an access point, in the form of a [SupplicantState](../android/net/wifi/SupplicantState.md) object.

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SupplicantState](../android/net/wifi/SupplicantState.md)! | the current [SupplicantState](../android/net/wifi/SupplicantState.md) |

### getTxLinkSpeedMbps

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTxLinkSpeedMbps(): Int
```

Returns the current transmit link speed in Mbps. In case of Multi Link Operation (MLO), returned value is the current transmit link speed of the associated link with the highest RSSI.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Tx link speed or [LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) if link speed is unknown. Value is -1 or greater |

**See Also**

- [#LINK_SPEED_UNKNOWN](../android/net/wifi/WifiInfo.md) 

### getWifiStandard

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWifiStandard(): Int
```

Get connection Wi-Fi standard

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the connection Wi-Fi standard Value is [android.net.wifi.ScanResult#WIFI_STANDARD_UNKNOWN](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#WIFI_STANDARD_LEGACY](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#WIFI_STANDARD_11N](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#WIFI_STANDARD_11AC](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#WIFI_STANDARD_11AX](../android/net/wifi/ScanResult.md), [android.net.wifi.ScanResult#WIFI_STANDARD_11AD](../android/net/wifi/ScanResult.md), or [android.net.wifi.ScanResult#WIFI_STANDARD_11BE](../android/net/wifi/ScanResult.md) |

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

Returns true if the current Wifi network is a restricted network, false otherwise. A restricted network has its [NetworkCapabilities.NET_CAPABILITY_NOT_RESTRICTED](../android/net/NetworkCapabilities.md) capability removed. 
**See Also**

- [android.net.wifi.WifiNetworkSuggestion.Builder#setRestricted(boolean)](../android/net/wifi/WifiNetworkSuggestion.Builder.md)) 

### makeCopy

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun makeCopy(redactions: Long): WifiInfo
```

Create a copy of a [WifiInfo](../android/net/wifi/WifiInfo.md) with some fields redacted based on the permissions held by the receiving app.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `redactions` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):bitmask of redactions that needs to be performed on this instance. |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [WifiInfo](../android/net/wifi/WifiInfo.md) | Copy of this instance with the necessary redactions. This value cannot be`null`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
