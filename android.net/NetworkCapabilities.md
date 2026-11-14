Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkCapabilities

Kotlin | [Java](https://developer.android.com/reference/android/net/NetworkCapabilities "View this page in Java")
| --- | --- |

```
class NetworkCapabilities : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.NetworkCapabilities](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#) |

Representation of the capabilities of an active network.

@see [hasCapability(int)](https://developer.android.com/training/basics/network-ops/reading-network-state>
this general guide</a> on how to use NetworkCapabilities and related classes.

<p>NetworkCapabilities represent what a network can do and what its
characteristics are like. The principal attribute of NetworkCapabilities
is in the capabilities bits, which are checked with
<code><a docref=). See the list of capabilities and each capability for a description of what it means.

Some prime examples include `NET_CAPABILITY_MMS`, which means that the network is capable of sending MMS. A network without this capability is not capable of sending MMS.

The `NET_CAPABILITY_INTERNET` capability means that the network is configured to reach the general Internet. It may or may not actually provide connectivity ; the `NET_CAPABILITY_VALIDATED` bit indicates that the system found actual connectivity to the general Internet the last time it checked. Apps interested in actual connectivity should usually look at both these capabilities.

The `NET_CAPABILITY_NOT_METERED` capability is set for networks that do not bill the user for consumption of bytes. Applications are encouraged to consult this to determine appropriate usage, and to limit usage of metered network where possible, including deferring big downloads until such a time that an unmetered network is connected. Also see `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` to help with scheduling such downloads, in particular `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#setRequiredNetwork(android.net.NetworkRequest)`.

NetworkCapabilities contain a number of other capabilities that represent what modern networks can and can't do. Look up the individual capabilities in this class to learn about each of them.

NetworkCapabilities typically represent attributes that can apply to any network. The attributes that apply only to specific transports like cellular or Wi-Fi can be found in the specifier (for requestable attributes) or in the transport info (for non-requestable ones). See `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getNetworkSpecifier()` and `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getTransportInfo()`. An app would downcast these to the specific class for the transport they need if they are interested in transport-specific attributes. Also see `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier` or `https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo` for some examples of each of these.

NetworkCapabilities also contains other attributes like the estimated upstream and downstream bandwidth and the specific transport of that network (e.g. `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_CELLULAR:kotlin.Int`). Generally, apps should normally have little reason to check for the type of transport ; for example, to query whether a network costs money to the user, do not look at the transport, but instead look at the absence or presence of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_METERED:kotlin.Int` which will correctly account for metered Wi-Fis and free of charge cell connections.

The system communicates with apps about connected networks and uses NetworkCapabilities to express these capabilities about these networks. Apps should register callbacks with the android.net.ConnectivityManager#requestNetwork or android.net.ConnectivityManager#registerNetworkCallback family of methods to learn about the capabilities of a network on a continuous basis and be able to react to changes to capabilities. For quick debugging Android also provides `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkCapabilities(android.net.Network)`, but the dynamic nature of networking makes this ill-suited to production code since capabilities obtained in this way can go stale immediately.

Also see `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` which uses the same capabilities together with android.net.ConnectivityManager#requestNetwork for how to request the system brings up the kind of network your application needs.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_CAPTIVE_PORTAL:kotlin.Int` Indicates that this network was found to have a captive portal in place last time it was probed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_CBS:kotlin.Int` Indicates this is a network that has the ability to reach the carrier's CBS servers, used for carrier specific services. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_DUN:kotlin.Int` Indicates this is a network that has the ability to reach the carrier's DUN or tethering gateway. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_EIMS:kotlin.Int` Indicates this is a network that has the ability to reach a carrier's Emergency IMS servers or other services, used for network signaling during emergency calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_ENTERPRISE:kotlin.Int` Indicates that this network is intended for enterprise use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_FOREGROUND:kotlin.Int` Indicates that this network is available for use by apps, and not a network that is being kept up in the background to facilitate fast network switching. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_FOTA:kotlin.Int` Indicates this is a network that has the ability to reach the carrier's FOTA portal, used for over the air updates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_HEAD_UNIT:kotlin.Int` Indicates that this network is connected to an automotive head unit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_IA:kotlin.Int` Indicates this is a network that has the ability to reach a carrier's Initial Attach servers. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_IMS:kotlin.Int` Indicates this is a network that has the ability to reach the carrier's IMS servers, used for network registration and signaling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_INTERNET:kotlin.Int` Indicates that this network should be able to reach the internet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_LOCAL_NETWORK:kotlin.Int` Indicates that this network is a local network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MCX:kotlin.Int` Indicates this is a network that has the ability to reach a carrier's Mission Critical servers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MMS:kotlin.Int` Indicates this is a network that has the ability to reach the carrier's MMSC for sending and receiving MMS messages. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MMTEL:kotlin.Int` Indicates that this network has ability to support MMTEL (Multimedia Telephony service). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_BANDWIDTH_CONSTRAINED:kotlin.Int` Indicates that this is not a bandwidth-constrained network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_CONGESTED:kotlin.Int` Indicates that this network is not congested. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_METERED:kotlin.Int` Indicates that this network is unmetered. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_RESTRICTED:kotlin.Int` Indicates that this network is available for general use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_ROAMING:kotlin.Int` Indicates that this network is not roaming. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_SUSPENDED:kotlin.Int` Indicates that this network is not currently suspended. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_VPN:kotlin.Int` Indicates that this network is not a VPN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_BANDWIDTH:kotlin.Int` Indicates that this network should be able to prioritize bandwidth for the internet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_LATENCY:kotlin.Int` Indicates that this network should be able to prioritize latency for the internet. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_UNIFIED_COMMUNICATIONS:kotlin.Int` Indicates that this network is optimized for real-time unified communications, such as Over-the-Top (OTT) voice and video calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_RCS:kotlin.Int` Indicates this is a network that has the ability to reach a carrier's RCS servers, used for Rich Communication Services. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_SUPL:kotlin.Int` Indicates this is a network that has the ability to reach the carrier's SUPL server, used to retrieve GPS information. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_TEMPORARILY_NOT_METERED:kotlin.Int` Indicates that this network is temporarily unmetered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_TRUSTED:kotlin.Int` Indicates that the user has indicated implicit trust of this network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int` Indicates that connectivity on this network was successfully validated. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_WIFI_P2P:kotlin.Int` Indicates this is a network that has the ability to reach a Wi-Fi direct peer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_XCAP:kotlin.Int` Indicates this is a network that has the ability to reach a carrier's XCAP servers, used for configuration and control. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_1:kotlin.Int` Enterprise capability identifier 1. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_2:kotlin.Int` Enterprise capability identifier 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_3:kotlin.Int` Enterprise capability identifier 3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_4:kotlin.Int` Enterprise capability identifier 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_5:kotlin.Int` Enterprise capability identifier 5. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#SIGNAL_STRENGTH_UNSPECIFIED:kotlin.Int` Magic value that indicates no signal strength provided. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_BLUETOOTH:kotlin.Int` Indicates this network uses a Bluetooth transport. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_CELLULAR:kotlin.Int` Indicates this network uses a Cellular transport. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_ETHERNET:kotlin.Int` Indicates this network uses an Ethernet transport. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_LOWPAN:kotlin.Int` Indicates this network uses a LoWPAN transport. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_SATELLITE:kotlin.Int` Indicates this network uses a Satellite transport. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_THREAD:kotlin.Int` Indicates this network uses a Thread transport. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_USB:kotlin.Int` Indicates this network uses a USB transport. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_VPN:kotlin.Int` Indicates this network uses a VPN transport. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_WIFI:kotlin.Int` Indicates this network uses a Wi-Fi transport. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_WIFI_AWARE:kotlin.Int` Indicates this network uses a Wi-Fi Aware transport. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NetworkCapabilities()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NetworkCapabilities(android.net.NetworkCapabilities)(nc: https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#!)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getCapabilities()()` Gets all the capabilities set on this `NetworkCapability` instance. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getEnterpriseIds()()` Get enteprise identifiers set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getLinkDownstreamBandwidthKbps()()` Retrieves the downstream bandwidth for this network in Kbps. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getLinkUpstreamBandwidthKbps()()` Retrieves the upstream bandwidth for this network in Kbps. |
| --- | --- |
| [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier)? | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getNetworkSpecifier()()` Gets the optional bearer specific network specifier. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getOwnerUid()()` Retrieves the UID of the app that owns this network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getSignalStrength()()` Retrieves the signal strength. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getSubscriptionIds()()` Gets the subscription ID set that associated to this network or request. |
| [TransportInfo](https://developer.android.com/reference/kotlin/android/net/TransportInfo)? | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getTransportInfo()()` Returns a transport-specific information container. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasCapability(kotlin.Int)(capability: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Tests for the presence of a capability on this instance. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasEnterpriseId(kotlin.Int)(enterpriseId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Tests for the presence of an enterprise capability identifier on this instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasTransport(kotlin.Int)(transportType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Tests for the presence of a transport on this instance. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [NetworkCapabilities](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#)!\> | `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### NET_CAPABILITY_CAPTIVE_PORTAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_CAPTIVE_PORTAL: Int
```

Indicates that this network was found to have a captive portal in place last time it was probed.

 Value: 17

### NET_CAPABILITY_CBS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_CBS: Int
```

Indicates this is a network that has the ability to reach the carrier's CBS servers, used for carrier specific services.

 Value: 5

### NET_CAPABILITY_DUN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_DUN: Int
```

Indicates this is a network that has the ability to reach the carrier's DUN or tethering gateway.

 Value: 2

### NET_CAPABILITY_EIMS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_EIMS: Int
```

Indicates this is a network that has the ability to reach a carrier's Emergency IMS servers or other services, used for network signaling during emergency calls.

 Value: 10

### NET_CAPABILITY_ENTERPRISE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_ENTERPRISE: Int
```

Indicates that this network is intended for enterprise use.

5G URSP rules may indicate that all data should use a connection dedicated for enterprise use. If the enterprise capability is requested, all enterprise traffic will be routed over the connection with this capability.

 Value: 29

### NET_CAPABILITY_FOREGROUND

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_FOREGROUND: Int
```

Indicates that this network is available for use by apps, and not a network that is being kept up in the background to facilitate fast network switching.

 Value: 19

### NET_CAPABILITY_FOTA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_FOTA: Int
```

Indicates this is a network that has the ability to reach the carrier's FOTA portal, used for over the air updates.

 Value: 3

### NET_CAPABILITY_HEAD_UNIT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_HEAD_UNIT: Int
```

Indicates that this network is connected to an automotive head unit.

 Value: 32

### NET_CAPABILITY_IA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_IA: Int
```

Indicates this is a network that has the ability to reach a carrier's Initial Attach servers.

 Value: 7

### NET_CAPABILITY_IMS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_IMS: Int
```

Indicates this is a network that has the ability to reach the carrier's IMS servers, used for network registration and signaling.

 Value: 4

### NET_CAPABILITY_INTERNET

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_INTERNET: Int
```

Indicates that this network should be able to reach the internet.

 Value: 12

### NET_CAPABILITY_LOCAL_NETWORK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 12](https://developer.android.com/sdkExtensions)

```
static val NET_CAPABILITY_LOCAL_NETWORK: Int
```

Indicates that this network is a local network. Local networks are networks where the device is not obtaining IP addresses from the network, but advertising IP addresses itself. Examples of local networks are:

- USB tethering or Wi-Fi hotspot networks to which the device is sharing its Internet connectivity.
- Thread networks where the current device is the Thread Border Router.
- Wi-Fi P2P networks where the current device is the Group Owner.

Networks used to obtain Internet access are never local networks. Apps that target an SDK before `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` will not see networks with this capability unless they explicitly set the NET_CAPABILITY_LOCAL_NETWORK in their NetworkRequests.

<br />

 Value: 36

### NET_CAPABILITY_MCX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_MCX: Int
```

Indicates this is a network that has the ability to reach a carrier's Mission Critical servers.

 Value: 23

### NET_CAPABILITY_MMS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_MMS: Int
```

Indicates this is a network that has the ability to reach the carrier's MMSC for sending and receiving MMS messages.

 Value: 0

### NET_CAPABILITY_MMTEL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_MMTEL: Int
```

Indicates that this network has ability to support MMTEL (Multimedia Telephony service).

 Value: 33

### NET_CAPABILITY_NOT_BANDWIDTH_CONSTRAINED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val NET_CAPABILITY_NOT_BANDWIDTH_CONSTRAINED: Int
```

Indicates that this is not a bandwidth-constrained network. Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, this capability is by default set in `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`s and true for most networks. If a network lacks this capability, it is bandwidth-constrained. Bandwidth constrained networks cannot support high-bandwidth data transfers and applications that request and use them must ensure that they limit bandwidth usage to below the values returned by `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getLinkDownstreamBandwidthKbps()` and `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getLinkUpstreamBandwidthKbps()` and limit the frequency of their network usage. If applications perform high-bandwidth data transfers on constrained networks or perform network access too frequently, the system may block the app's access to the network. The system may take other measures to reduce network usage on constrained networks, such as disabling network access to apps that are not in the foreground.

 Value: 37

### NET_CAPABILITY_NOT_CONGESTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_NOT_CONGESTED: Int
```

Indicates that this network is not congested.

When a network is congested, applications should defer network traffic that can be done at a later time, such as uploading analytics.

 Value: 20

### NET_CAPABILITY_NOT_METERED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_NOT_METERED: Int
```

Indicates that this network is unmetered.

 Value: 11

### NET_CAPABILITY_NOT_RESTRICTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_NOT_RESTRICTED: Int
```

Indicates that this network is available for general use. If this is not set applications should not attempt to communicate on this network. Note that this is simply informative and not enforcement - enforcement is handled via other means. Set by default.

 Value: 13

### NET_CAPABILITY_NOT_ROAMING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_NOT_ROAMING: Int
```

Indicates that this network is not roaming.

 Value: 18

### NET_CAPABILITY_NOT_SUSPENDED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_NOT_SUSPENDED: Int
```

Indicates that this network is not currently suspended.

When a network is suspended, the network's IP addresses and any connections established on the network remain valid, but the network is temporarily unable to transfer data. This can happen, for example, if a cellular network experiences a temporary loss of signal, such as when driving through a tunnel, etc. A network with this capability is not suspended, so is expected to be able to transfer data.

 Value: 21

### NET_CAPABILITY_NOT_VPN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_NOT_VPN: Int
```

Indicates that this network is not a VPN. This capability is set by default and should be explicitly cleared for VPN networks.

 Value: 15

### NET_CAPABILITY_PRIORITIZE_BANDWIDTH

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_PRIORITIZE_BANDWIDTH: Int
```

Indicates that this network should be able to prioritize bandwidth for the internet. Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher, requesting this capability with android.net.ConnectivityManager#requestNetwork requires declaration in the self-certified network capabilities. See `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` for the self-certification documentation.

 Value: 35

### NET_CAPABILITY_PRIORITIZE_LATENCY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_PRIORITIZE_LATENCY: Int
```

Indicates that this network should be able to prioritize latency for the internet. Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher, requesting this capability with android.net.ConnectivityManager#requestNetwork requires declaration in the self-certified network capabilities. See `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` for the self-certification documentation.

 Value: 34

### NET_CAPABILITY_PRIORITIZE_UNIFIED_COMMUNICATIONS

Added in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val NET_CAPABILITY_PRIORITIZE_UNIFIED_COMMUNICATIONS: Int
```

Indicates that this network is optimized for real-time unified communications, such as Over-the-Top (OTT) voice and video calls.

This capability is intended specifically for applications that handle Over-the-Top (OTT) voice and video calls. It is not intended for non ott applications.

This capability signals to the system that the network may offer a dedicated slice for high-priority, low-latency data paths. It can be used in two ways:

- The system can request a network with this capability on behalf of an eligible application when it detects an active OTT call to improve Quality of Service (QoS).
- An ott application can request a network with this capability directly using android.net.ConnectivityManager#requestNetwork.

This capability is a hint from the network and does not guarantee that it will be used for any given call. Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` or higher, requesting this capability with android.net.ConnectivityManager#requestNetwork requires declaration in the self-certified network capabilities. See `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` for the self-certification documentation.

 Value: 38

### NET_CAPABILITY_RCS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_RCS: Int
```

Indicates this is a network that has the ability to reach a carrier's RCS servers, used for Rich Communication Services.

 Value: 8

### NET_CAPABILITY_SUPL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_SUPL: Int
```

Indicates this is a network that has the ability to reach the carrier's SUPL server, used to retrieve GPS information.

 Value: 1

### NET_CAPABILITY_TEMPORARILY_NOT_METERED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_TEMPORARILY_NOT_METERED: Int
```

Indicates that this network is temporarily unmetered.

This capability will be set for networks that are generally metered, but are currently unmetered, e.g., because the user is in a particular area. This capability can be changed at any time. When it is removed, applications are responsible for stopping any data transfer that should not occur on a metered network. Note that most apps should use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_METERED:kotlin.Int` instead. For more information, see https://developer.android.com/about/versions/11/features/5g#meteredness.

 Value: 25

### NET_CAPABILITY_TRUSTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_TRUSTED: Int
```

Indicates that the user has indicated implicit trust of this network. This generally means it's a sim-selected carrier, a plugged in ethernet, a paired BT device or a wifi the user asked to connect to. Untrusted networks are probably limited to unknown wifi AP. Set by default.

 Value: 14

### NET_CAPABILITY_VALIDATED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_VALIDATED: Int
```

Indicates that connectivity on this network was successfully validated. For example, for a network with NET_CAPABILITY_INTERNET, it means that Internet connectivity was successfully detected.

 Value: 16

### NET_CAPABILITY_WIFI_P2P

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_WIFI_P2P: Int
```

Indicates this is a network that has the ability to reach a Wi-Fi direct peer.

 Value: 6

### NET_CAPABILITY_XCAP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_CAPABILITY_XCAP: Int
```

Indicates this is a network that has the ability to reach a carrier's XCAP servers, used for configuration and control.

 Value: 9

### NET_ENTERPRISE_ID_1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_ENTERPRISE_ID_1: Int
```

Enterprise capability identifier 1. It will be used to uniquely identify specific enterprise network.

 Value: 1

### NET_ENTERPRISE_ID_2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_ENTERPRISE_ID_2: Int
```

Enterprise capability identifier 2. It will be used to uniquely identify specific enterprise network.

 Value: 2

### NET_ENTERPRISE_ID_3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_ENTERPRISE_ID_3: Int
```

Enterprise capability identifier 3. It will be used to uniquely identify specific enterprise network.

 Value: 3

### NET_ENTERPRISE_ID_4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_ENTERPRISE_ID_4: Int
```

Enterprise capability identifier 4. It will be used to uniquely identify specific enterprise network.

 Value: 4

### NET_ENTERPRISE_ID_5

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NET_ENTERPRISE_ID_5: Int
```

Enterprise capability identifier 5. It will be used to uniquely identify specific enterprise network.

 Value: 5

### SIGNAL_STRENGTH_UNSPECIFIED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNAL_STRENGTH_UNSPECIFIED: Int
```

Magic value that indicates no signal strength provided. A request specifying this value is always satisfied.

 Value: -2147483648

### TRANSPORT_BLUETOOTH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_BLUETOOTH: Int
```

Indicates this network uses a Bluetooth transport.

 Value: 2

### TRANSPORT_CELLULAR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_CELLULAR: Int
```

Indicates this network uses a Cellular transport.

 Value: 0

### TRANSPORT_ETHERNET

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_ETHERNET: Int
```

Indicates this network uses an Ethernet transport.

 Value: 3

### TRANSPORT_LOWPAN

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_LOWPAN: Int
```

Indicates this network uses a LoWPAN transport.

 Value: 6

### TRANSPORT_SATELLITE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 12](https://developer.android.com/sdkExtensions)

```
static val TRANSPORT_SATELLITE: Int
```

Indicates this network uses a Satellite transport.

 Value: 10

### TRANSPORT_THREAD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val TRANSPORT_THREAD: Int
```

Indicates this network uses a Thread transport.

 Value: 9

### TRANSPORT_USB

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_USB: Int
```

Indicates this network uses a USB transport.

 Value: 8

### TRANSPORT_VPN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_VPN: Int
```

Indicates this network uses a VPN transport.

 Value: 4

### TRANSPORT_WIFI

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_WIFI: Int
```

Indicates this network uses a Wi-Fi transport.

 Value: 1

### TRANSPORT_WIFI_AWARE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_WIFI_AWARE: Int
```

Indicates this network uses a Wi-Fi Aware transport.

 Value: 5

## Public constructors

### NetworkCapabilities

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
NetworkCapabilities()
```

### NetworkCapabilities

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
NetworkCapabilities(nc: NetworkCapabilities!)
```

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getCapabilities

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCapabilities(): IntArray
```

Gets all the capabilities set on this `NetworkCapability` instance.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | an array of capability values for this instance. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_SUPL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_DUN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_FOTA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_IMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_CBS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_WIFI_P2P:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_IA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_RCS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_XCAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_EIMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_METERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_INTERNET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_TRUSTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_VPN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_CAPTIVE_PORTAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_ROAMING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_CONGESTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_SUSPENDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MCX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_TEMPORARILY_NOT_METERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_ENTERPRISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_HEAD_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MMTEL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_LATENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_BANDWIDTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_LOCAL_NETWORK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_BANDWIDTH_CONSTRAINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_UNIFIED_COMMUNICATIONS:kotlin.Int` |

### getEnterpriseIds

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnterpriseIds(): IntArray
```

Get enteprise identifiers set. Get all the enterprise capabilities identifier set on this `NetworkCapability` If NET_CAPABILITY_ENTERPRISE is set and no enterprise ID is set, it is considered to have NET_CAPABILITY_ENTERPRISE by default.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | all the enterprise capabilities identifier set. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_5:kotlin.Int` |

### getLinkDownstreamBandwidthKbps

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLinkDownstreamBandwidthKbps(): Int
```

Retrieves the downstream bandwidth for this network in Kbps. This always only refers to the estimated first hop transport bandwidth.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The estimated first hop downstream (network to device) bandwidth. |

### getLinkUpstreamBandwidthKbps

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLinkUpstreamBandwidthKbps(): Int
```

Retrieves the upstream bandwidth for this network in Kbps. This always only refers to the estimated first hop transport bandwidth.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The estimated first hop upstream (device to network) bandwidth. |

### getNetworkSpecifier

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNetworkSpecifier(): NetworkSpecifier?
```

Gets the optional bearer specific network specifier. May be `null` if not set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier?` | The optional `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier` specifying the bearer specific network specifier or `null`. |

### getOwnerUid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOwnerUid(): Int
```

Retrieves the UID of the app that owns this network.

For user privacy reasons, this field will only be populated if the following conditions are met:

The caller is the network owner, AND one of the following sets of requirements is met:

1. The described Network is a VPN

OR:

1. The calling app is the network owner
2. The calling app has the ACCESS_FINE_LOCATION permission granted
3. The user's location toggle is on

Instances of NetworkCapabilities sent to apps without the appropriate permissions will have this field cleared out.

This field will only be populated for VPN and wifi network suggestor apps (i.e using `https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion`), and only for the network they own. In the case of wifi network suggestors apps, this field is also location sensitive, so the app needs to hold `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission. If the app targets SDK version greater than or equal to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, then they also need to use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#FLAG_INCLUDE_LOCATION_INFO:kotlin.Int` to get the info in their callback. If the apps targets SDK version equal to {`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, this field will always be included. The app will be blamed for location access if this field is included.

### getSignalStrength

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSignalStrength(): Int
```

Retrieves the signal strength.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The bearer-specific signal strength. |

### getSubscriptionIds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 12](https://developer.android.com/sdkExtensions)

```
fun getSubscriptionIds(): MutableSet<Int!>
```

Gets the subscription ID set that associated to this network or request.

Instances of NetworkCapabilities will only have this field populated by the system if the receiver holds the NETWORK_FACTORY permission. In all other cases, it will be the empty set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | This value cannot be `null`. |

### getTransportInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransportInfo(): TransportInfo?
```

Returns a transport-specific information container. The application may cast this container to a concrete sub-class based on its knowledge of the network request. The application should be able to deal with a `null` return value or an invalid case, e.g. use `instanceof` operator to verify expected type.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/TransportInfo?` | A concrete implementation of the `https://developer.android.com/reference/kotlin/android/net/TransportInfo` class or null if not available for the network. |

### hasCapability

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCapability(capability: Int): Boolean
```

Tests for the presence of a capability on this instance.

| Parameters ||
|---|---|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the capability to be tested for. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_SUPL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_DUN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_FOTA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_IMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_CBS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_WIFI_P2P:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_IA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_RCS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_XCAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_EIMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_METERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_INTERNET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_TRUSTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_VPN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_CAPTIVE_PORTAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_ROAMING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_CONGESTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_SUSPENDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MCX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_TEMPORARILY_NOT_METERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_ENTERPRISE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_HEAD_UNIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MMTEL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_LATENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_BANDWIDTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_LOCAL_NETWORK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_NOT_BANDWIDTH_CONSTRAINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_UNIFIED_COMMUNICATIONS:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if set on this instance. |

### hasEnterpriseId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasEnterpriseId(enterpriseId: Int): Boolean
```

Tests for the presence of an enterprise capability identifier on this instance. If NET_CAPABILITY_ENTERPRISE is set and no enterprise ID is set, it is considered to have NET_CAPABILITY_ENTERPRISE by default.

| Parameters ||
|---|---|
| `enterpriseId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the enterprise capability identifier to be tested for. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_ENTERPRISE_ID_5:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if set on this instance. |

### hasTransport

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasTransport(transportType: Int): Boolean
```

Tests for the presence of a transport on this instance.

| Parameters ||
|---|---|
| `transportType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the transport type to be tested for. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_CELLULAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_WIFI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_BLUETOOTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_ETHERNET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_VPN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_WIFI_AWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_LOWPAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_USB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_THREAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_SATELLITE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if set on this instance. |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<NetworkCapabilities!>
```
