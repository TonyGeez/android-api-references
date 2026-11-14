Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pConfig

```
open class WifiP2pConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.p2p.WifiP2pConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#) |

A class representing a Wi-Fi P2p configuration for setting up a connection

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig.Builder` Builder used to build `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#` objects for creating or joining a group. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_CLIENT_IP_PROVISIONING_MODE_IPV4_DHCP:kotlin.Int` IP provisioning via IPv4 DHCP, when joining a group as a group client. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_CLIENT_IP_PROVISIONING_MODE_IPV6_LINK_LOCAL:kotlin.Int` IP provisioning via IPv6 link-local, when joining a group as a group client. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_2GHZ:kotlin.Int` Allow the system to pick the operating frequency from the 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_5GHZ:kotlin.Int` Allow the system to pick the operating frequency from the 5 GHz band. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_6GHZ:kotlin.Int` Allow the system to pick the operating frequency from the 6 GHz band. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_AUTO:kotlin.Int` Allow the system to pick the operating frequency from all supported bands. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_AUTO:kotlin.Int` The system can choose an appropriate owner intent value, to be filled in the field `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#groupOwnerIntent:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MAX:kotlin.Int` The most inclination to be a group owner, to be filled in the field `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#groupOwnerIntent:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MIN:kotlin.Int` The least inclination to be a group owner, to be filled in the field `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#groupOwnerIntent:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#P2P_VERSION_1:kotlin.Int` P2P Protocol version 1 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#P2P_VERSION_2:kotlin.Int` P2P Protocol version 2 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#PCC_MODE_CONNECTION_TYPE_LEGACY_ONLY:kotlin.Int` Legacy connection type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#PCC_MODE_CONNECTION_TYPE_LEGACY_OR_R2:kotlin.Int` Wi-Fi Direct R1/R2 compatible mode connection type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#PCC_MODE_CONNECTION_TYPE_R2_ONLY:kotlin.Int` This configuration allows only Wi-Fi Direct R2 supported devices to establish connection. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#WifiP2pConfig()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#WifiP2pConfig(android.net.wifi.p2p.WifiP2pConfig)(source: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#!)` copy constructor |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#describeContents()()` Implement the Parcelable interface |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getGroupClientIpProvisioningMode()()` Get the IP provisioning mode when joining a group as a group client. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getGroupOwnerBand()()` Get the required band for the group owner. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getGroupOwnerVersion()()` Get the P2P Group Owner version. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getNetworkId()()` Get the network ID of this P2P configuration. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getNetworkName()()` Get the network name of this P2P configuration, or null if unset. |
| open [WifiP2pPairingBootstrappingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig)? | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getPairingBootstrappingConfig()()` Get the pairing bootstrapping configuration , or null if unset. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getPairingDiscoveryChannelFrequencyMhz()()` Get the discovery channel frequency in MHz for pairing, or 0 if unset. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getPassphrase()()` Get the passphrase of this P2P configuration, or null if unset. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#getPccModeConnectionType()()` Get the PCC Mode connection type. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#isAuthorizeConnectionFromPeerEnabled()()` Query to check if the configuration is for authorizing a connection request from the peer device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#setGroupOwnerVersion(kotlin.Int)(version: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the P2P Group Owner version. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Implement the Parcelable interface |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiP2pConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#CREATOR:android.os.Parcelable.Creator` Implement the Parcelable interface |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#deviceAddress:kotlin.String` The device MAC address uniquely identifies a Wi-Fi p2p device |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#groupOwnerIntent:kotlin.Int` This is an integer value between `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MIN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MAX:kotlin.Int` where `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MIN:kotlin.Int` indicates the least inclination to be a group owner and `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MAX:kotlin.Int` indicates the highest inclination to be a group owner. |
| [WpsInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WpsInfo.html#)! | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#wps:android.net.wifi.WpsInfo` Wi-Fi Protected Setup information |

## Constants

### GROUP_CLIENT_IP_PROVISIONING_MODE_IPV4_DHCP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_CLIENT_IP_PROVISIONING_MODE_IPV4_DHCP: Int
```

IP provisioning via IPv4 DHCP, when joining a group as a group client.

 Value: 0

### GROUP_CLIENT_IP_PROVISIONING_MODE_IPV6_LINK_LOCAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_CLIENT_IP_PROVISIONING_MODE_IPV6_LINK_LOCAL: Int
```

IP provisioning via IPv6 link-local, when joining a group as a group client.

 Value: 1

### GROUP_OWNER_BAND_2GHZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_OWNER_BAND_2GHZ: Int
```

Allow the system to pick the operating frequency from the 2.4 GHz band.

 Value: 1

### GROUP_OWNER_BAND_5GHZ

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_OWNER_BAND_5GHZ: Int
```

Allow the system to pick the operating frequency from the 5 GHz band.

 Value: 2

### GROUP_OWNER_BAND_6GHZ

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_OWNER_BAND_6GHZ: Int
```

Allow the system to pick the operating frequency from the 6 GHz band.

 Value: 3

### GROUP_OWNER_BAND_AUTO

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_OWNER_BAND_AUTO: Int
```

Allow the system to pick the operating frequency from all supported bands.

 Value: 0

### GROUP_OWNER_INTENT_AUTO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_OWNER_INTENT_AUTO: Int
```

The system can choose an appropriate owner intent value, to be filled in the field `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#groupOwnerIntent:kotlin.Int`.

 Value: -1

### GROUP_OWNER_INTENT_MAX

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_OWNER_INTENT_MAX: Int
```

The most inclination to be a group owner, to be filled in the field `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#groupOwnerIntent:kotlin.Int`.

 Value: 15

### GROUP_OWNER_INTENT_MIN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_OWNER_INTENT_MIN: Int
```

The least inclination to be a group owner, to be filled in the field `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#groupOwnerIntent:kotlin.Int`.

 Value: 0

### P2P_VERSION_1

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val P2P_VERSION_1: Int
```

P2P Protocol version 1

 Value: 0

### P2P_VERSION_2

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val P2P_VERSION_2: Int
```

P2P Protocol version 2

 Value: 1

### PCC_MODE_CONNECTION_TYPE_LEGACY_ONLY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PCC_MODE_CONNECTION_TYPE_LEGACY_ONLY: Int
```

Legacy connection type.

Group Owner: Configured to support WPA2-Personal connections.

Group Client: Configured to connect to Group Owner using WPA2-Personal.

 Value: 0

### PCC_MODE_CONNECTION_TYPE_LEGACY_OR_R2

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PCC_MODE_CONNECTION_TYPE_LEGACY_OR_R2: Int
```

Wi-Fi Direct R1/R2 compatible mode connection type.

Group Owner: Configured in WPA3-Personal Compatibility Mode to support WPA3-Personal and WPA2-Personal connections simultaneously.

Group Client: Configured to connect to Group Owner using WPA3-Personal or WPA2-Personal. The system will choose WPA3-Personal if Group Owner support WPA3-Personal.

 Value: 1

### PCC_MODE_CONNECTION_TYPE_R2_ONLY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PCC_MODE_CONNECTION_TYPE_R2_ONLY: Int
```

This configuration allows only Wi-Fi Direct R2 supported devices to establish connection.

Group Owner: Configured to support WPA3-Personal connections.

Group Client: Configured to connect to Group Owner using WPA3-Personal.

 Value: 2

## Public constructors

### WifiP2pConfig

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WifiP2pConfig()
```

### WifiP2pConfig

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WifiP2pConfig(source: WifiP2pConfig!)
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

### getGroupClientIpProvisioningMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupClientIpProvisioningMode(): Int
```

Get the IP provisioning mode when joining a group as a group client. The result will be one of the following: `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_CLIENT_IP_PROVISIONING_MODE_IPV4_DHCP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_CLIENT_IP_PROVISIONING_MODE_IPV6_LINK_LOCAL:kotlin.Int`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_CLIENT_IP_PROVISIONING_MODE_IPV4_DHCP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_CLIENT_IP_PROVISIONING_MODE_IPV6_LINK_LOCAL:kotlin.Int` |

### getGroupOwnerBand

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupOwnerBand(): Int
```

Get the required band for the group owner. The result will be one of the following: `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_2GHZ:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_5GHZ:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_6GHZ:kotlin.Int`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_2GHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_5GHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_BAND_6GHZ:kotlin.Int` |

### getGroupOwnerVersion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupOwnerVersion(): Int
```

Get the P2P Group Owner version. See also `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#setGroupOwnerVersion(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The P2P Group Owner protocol version. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#P2P_VERSION_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#P2P_VERSION_2:kotlin.Int` |

### getNetworkId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkId(): Int
```

Get the network ID of this P2P configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | either a non-negative network ID, or one of `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#NETWORK_ID_PERSISTENT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup#NETWORK_ID_TEMPORARY:kotlin.Int`. |

### getNetworkName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkName(): String?
```

Get the network name of this P2P configuration, or null if unset.

### getPairingBootstrappingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPairingBootstrappingConfig(): WifiP2pPairingBootstrappingConfig?
```

Get the pairing bootstrapping configuration , or null if unset.

### getPairingDiscoveryChannelFrequencyMhz

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPairingDiscoveryChannelFrequencyMhz(): Int
```

Get the discovery channel frequency in MHz for pairing, or 0 if unset.

### getPassphrase

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPassphrase(): String?
```

Get the passphrase of this P2P configuration, or null if unset.

### getPccModeConnectionType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPccModeConnectionType(): Int
```

Get the PCC Mode connection type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | One of the `PCC_MODE_CONNECTION_TYPE_*`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#PCC_MODE_CONNECTION_TYPE_LEGACY_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#PCC_MODE_CONNECTION_TYPE_LEGACY_OR_R2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#PCC_MODE_CONNECTION_TYPE_R2_ONLY:kotlin.Int` |

### isAuthorizeConnectionFromPeerEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAuthorizeConnectionFromPeerEnabled(): Boolean
```

Query to check if the configuration is for authorizing a connection request from the peer device. @see `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig.Builder#setAuthorizeConnectionFromPeerEnabled(kotlin.Boolean)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if configured to authorize a connection request from the Peer device, False otherwise. |

### setGroupOwnerVersion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGroupOwnerVersion(version: Int): Unit
```

Set the P2P Group Owner version.

| Parameters ||
|---|---|
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The P2P Group Owner protocol version. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#P2P_VERSION_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#P2P_VERSION_2:kotlin.Int` |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<WifiP2pConfig!>
```

Implement the Parcelable interface

### deviceAddress

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var deviceAddress: String!
```

The device MAC address uniquely identifies a Wi-Fi p2p device

### groupOwnerIntent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var groupOwnerIntent: Int
```

This is an integer value between `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MIN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MAX:kotlin.Int` where `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MIN:kotlin.Int` indicates the least inclination to be a group owner and `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_MAX:kotlin.Int` indicates the highest inclination to be a group owner. A value of `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_AUTO:kotlin.Int` indicates the system can choose an appropriate value. By default this field is set to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_OWNER_INTENT_AUTO:kotlin.Int`. 
Value is between 0 and 15 inclusive

### wps

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var wps: WpsInfo!
```

Wi-Fi Protected Setup information
