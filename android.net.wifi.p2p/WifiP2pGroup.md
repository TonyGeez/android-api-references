Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pGroup

```
open class WifiP2pGroup : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.WifiP2pGroup](../android/net/wifi/p2p/WifiP2pGroup.md) |

A class representing a Wi-Fi P2p group. A p2p group consists of a single group owner and one or more clients. In the case of a group with only two devices, one will be the group owner and the other will be a group client.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#NETWORK_ID_PERSISTENT:kotlin.Int` The persistent network id. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#NETWORK_ID_TEMPORARY:kotlin.Int` The temporary network id. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#SECURITY_TYPE_UNKNOWN:kotlin.Int` The definition of security type unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#SECURITY_TYPE_WPA2_PSK:kotlin.Int` The definition of security type WPA2-PSK. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#SECURITY_TYPE_WPA3_COMPATIBILITY:kotlin.Int` The definition of security type WPA3-Compatibility Mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#SECURITY_TYPE_WPA3_SAE:kotlin.Int` The definition of security type WPA3-SAE. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#WifiP2pGroup()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#WifiP2pGroup(android.net.wifi.p2p.WifiP2pGroup)(source: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#!)` copy constructor |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#describeContents()()` Implement the Parcelable interface |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [WifiP2pDevice](../android/net/wifi/p2p/WifiP2pDevice.md)!\>! | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getClientList()()` Get the list of clients currently part of the p2p group |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getFrequency()()` Get the operating frequency (in MHz) of the p2p group |
| --- | --- |
| open [MacAddress](../android/net/MacAddress.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getGroupOwnerBssid()()` Returns the BSSID, if this device is the group owner of the P2P group supporting Wi-Fi Direct R2 protocol. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getInterface()()` Get the interface name on which the group is created |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getNetworkId()()` The network ID of the P2P group in wpa_supplicant. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getNetworkName()()` Get the network name (SSID) of the group. |
| open [WifiP2pDevice](../android/net/wifi/p2p/WifiP2pDevice.md)! | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getOwner()()` Get the details of the group owner as a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` object |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getPassphrase()()` Get the passphrase of the group. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getSecurityType()()` Get the security type of the group. |
| open [WifiP2pConnectionInfo](../android/net/wifi/p2p/WifiP2pConnectionInfo.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getWifiP2pGroupClientConnectionInfo()()` Gets the P2P connection information for this device if it is a client in the group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#isGroupOwner()()` Check whether this device is the group owner of the created p2p group |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Implement the Parcelable interface |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiP2pGroup](../android/net/wifi/p2p/WifiP2pGroup.md)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#CREATOR:android.os.Parcelable.Creator` Implement the Parcelable interface |

## Constants

### NETWORK_ID_PERSISTENT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_ID_PERSISTENT: Int
```

The persistent network id. If a matching persistent profile is found, use it. Otherwise, create a new persistent profile.

 Value: -2

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getNetworkId()`

### NETWORK_ID_TEMPORARY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_ID_TEMPORARY: Int
```

The temporary network id.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getNetworkId()`

### SECURITY_TYPE_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECURITY_TYPE_UNKNOWN: Int
```

The definition of security type unknown. It is set when framework fails to derive the security type from the authentication key management provided by wpa_supplicant.

 Value: -1

### SECURITY_TYPE_WPA2_PSK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECURITY_TYPE_WPA2_PSK: Int
```

The definition of security type WPA2-PSK.

 Value: 0

### SECURITY_TYPE_WPA3_COMPATIBILITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECURITY_TYPE_WPA3_COMPATIBILITY: Int
```

The definition of security type WPA3-Compatibility Mode.

 Value: 1

### SECURITY_TYPE_WPA3_SAE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECURITY_TYPE_WPA3_SAE: Int
```

The definition of security type WPA3-SAE.

 Value: 2

## Public constructors

### WifiP2pGroup

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WifiP2pGroup()
```

### WifiP2pGroup

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WifiP2pGroup(source: WifiP2pGroup!)
```

copy constructor

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getClientList

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClientList(): MutableCollection<WifiP2pDevice!>!
```

Get the list of clients currently part of the p2p group

### getFrequency

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFrequency(): Int
```

Get the operating frequency (in MHz) of the p2p group

### getGroupOwnerBssid

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupOwnerBssid(): MacAddress?
```

Returns the BSSID, if this device is the group owner of the P2P group supporting Wi-Fi Direct R2 protocol.

The interface address of a Wi-Fi Direct R2 supported device is randomized. So for every group owner session a randomized interface address will be returned.

The BSSID returned will be `null`, if this device is a client device or a group owner which doesn't support Wi-Fi Direct R2 protocol.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/MacAddress.html#?` | the BSSID. |

### getInterface

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInterface(): String!
```

Get the interface name on which the group is created

### getNetworkId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkId(): Int
```

The network ID of the P2P group in wpa_supplicant.

### getNetworkName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkName(): String!
```

Get the network name (SSID) of the group. Legacy Wi-Fi clients will discover the p2p group using the network name.

### getOwner

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOwner(): WifiP2pDevice!
```

Get the details of the group owner as a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` object

### getPassphrase

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPassphrase(): String!
```

Get the passphrase of the group. This function will return a valid passphrase only at the group owner. Legacy Wi-Fi clients will need this passphrase alongside network name obtained from `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#getNetworkName()` to join the group

### getSecurityType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSecurityType(): Int
```

Get the security type of the group.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of the `SECURITY_TYPE_*`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#SECURITY_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#SECURITY_TYPE_WPA2_PSK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#SECURITY_TYPE_WPA3_COMPATIBILITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#SECURITY_TYPE_WPA3_SAE:kotlin.Int` |

### getWifiP2pGroupClientConnectionInfo

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWifiP2pGroupClientConnectionInfo(): WifiP2pConnectionInfo?
```

Gets the P2P connection information for this device if it is a client in the group. If this device is the Group Owner, this will return `null`.

To get the most up-to-date information, an application should listen for the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_CONNECTION_CHANGED_ACTION:kotlin.String` broadcast. When this device joins a group as a client, the system updates the connection information and broadcasts the new group details in the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_GROUP:kotlin.String` extra.

Alternatively, an application can call `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestGroupInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.GroupInfoListener)` to get the latest group details.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo?` | A `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo` object if this device is a client, or `null` if it is the Group Owner. |

### isGroupOwner

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isGroupOwner(): Boolean
```

Check whether this device is the group owner of the created p2p group

### toString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<WifiP2pGroup!>
```

Implement the Parcelable interface
