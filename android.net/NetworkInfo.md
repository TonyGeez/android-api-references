# NetworkInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkInfo

Kotlin| [Java](../android/net/NetworkInfo.md) 
| --- | --- |

```
open class NetworkInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.NetworkInfo](../android/net/NetworkInfo.md) |

| **This class was deprecated in API level 29.**
|
| Callers should instead use the [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md) API to learn about connectivity changes, or switch to use [ConnectivityManager.getNetworkCapabilities](../android/net/ConnectivityManager.md))or [ConnectivityManager.getLinkProperties](../android/net/ConnectivityManager.md))to get information synchronously. Keep in mind that while callbacks are guaranteed to be called for every event in order, synchronous calls have no such constraints, and as such it is unadvisable to use the synchronous methods inside the callbacks as they will often not offer a view of networking that is consistent (that is: they may return a past or a future state with respect to the event being processed by the callback). Instead, callers are advised to only use the arguments of the callbacks, possibly memorizing the specific bits of information they need to keep from one callback to another.

Describes the status of a network interface.

Use [ConnectivityManager.getActiveNetworkInfo()](../android/net/ConnectivityManager.md))to get an instance that represents the current network connection.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DetailedState](../android/net/NetworkInfo.DetailedState.md) The fine-grained state of a network connection. |
| | [State](../android/net/NetworkInfo.State.md) Coarse-grained network state. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NetworkInfo](../android/net/NetworkInfo.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subtype:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `subtypeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a new instance of NetworkInfo. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/NetworkInfo.md))`()` <br /> |
| open [NetworkInfo.DetailedState](../android/net/NetworkInfo.DetailedState.md) | [getDetailedState](../android/net/NetworkInfo.md))`()` Reports the current fine-grained state of the network. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExtraInfo](../android/net/NetworkInfo.md))`()` Report the extra information about the network state, if any was provided by the lower networking layers. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](../android/net/NetworkInfo.md))`()` Report the reason an attempt to establish connectivity failed, if one is available. |
| open [NetworkInfo.State](../android/net/NetworkInfo.State.md)! | [getState](../android/net/NetworkInfo.md))`()` Reports the current coarse-grained state of the network. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubtype](../android/net/NetworkInfo.md))`()` Return a network-type-specific integer describing the subtype of the network. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubtypeName](../android/net/NetworkInfo.md))`()` Return a human-readable name describing the subtype of the network. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/net/NetworkInfo.md))`()` Reports the type of network to which the info in this`NetworkInfo`pertains. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTypeName](../android/net/NetworkInfo.md))`()` Return a human-readable name describe the type of the network, for example "WIFI" or "MOBILE". |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAvailable](../android/net/NetworkInfo.md))`()` Indicates whether network connectivity is possible. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/net/NetworkInfo.md))`()` Indicates whether network connectivity exists and it is possible to establish connections and pass data. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnectedOrConnecting](../android/net/NetworkInfo.md))`()` Indicates whether network connectivity exists or is in the process of being established. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFailover](../android/net/NetworkInfo.md))`()` Indicates whether the current attempt to connect to the network resulted from the ConnectivityManager trying to fail over to this network following a disconnect from another network. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRoaming](../android/net/NetworkInfo.md))`()` Indicates whether the device is currently roaming on this network. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDetailedState](../android/net/NetworkInfo.md))`(`detailedState:` ` [NetworkInfo.DetailedState](../android/net/NetworkInfo.DetailedState.md)`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extraInfo:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the fine-grained state of the network. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/NetworkInfo.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/NetworkInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [NetworkInfo](../android/net/NetworkInfo.md)!\> | [CREATOR](../android/net/NetworkInfo.md) <br /> |

## Public constructors

### NetworkInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NetworkInfo(
    type: Int, 
    subtype: Int, 
    typeName: String?, 
    subtypeName: String?)
```

Create a new instance of NetworkInfo. This may be useful for apps to write unit tests.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the legacy type of the network, as one of the ConnectivityManager.TYPE_\* constants. |
| `subtype` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the subtype if applicable, as one of the TelephonyManager.NETWORK_TYPE_\* constants. |
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a human-readable string for the network type, or an empty string or null. |
| --- | --- |
| `subtypeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a human-readable string for the subtype, or an empty string or null. |

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getDetailedState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDetailedState(): NetworkInfo.DetailedState
```

**Deprecated:** *Apps should instead use the [android.net.ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md) API to learn about connectivity changes. See android.net.ConnectivityManager#registerDefaultNetworkCallback and android.net.ConnectivityManager#registerNetworkCallback. These will give a more accurate picture of the connectivity state of the device and let apps react more easily and quickly to changes.*

Reports the current fine-grained state of the network.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [NetworkInfo.DetailedState](../android/net/NetworkInfo.DetailedState.md) | the fine-grained state This value cannot be`null`. |

### getExtraInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtraInfo(): String!
```

**Deprecated:** *Use other services e.g. WifiManager to get additional information passed up from the lower networking layers.*

Report the extra information about the network state, if any was provided by the lower networking layers.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the extra information, or null if not available |

### getReason

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReason(): String!
```

**Deprecated:** *This method does not have a consistent contract that could make it useful to callers.*

Report the reason an attempt to establish connectivity failed, if one is available.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the reason for failure, or null if not available |

### getState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getState(): NetworkInfo.State!
```

**Deprecated:** *Apps should instead use the [android.net.ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md) API to learn about connectivity changes. android.net.ConnectivityManager#registerDefaultNetworkCallback and android.net.ConnectivityManager#registerNetworkCallback. These will give a more accurate picture of the connectivity state of the device and let apps react more easily and quickly to changes.*

Reports the current coarse-grained state of the network.

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------|
| [NetworkInfo.State](../android/net/NetworkInfo.State.md)! | the coarse-grained state |

### getSubtype

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubtype(): Int
```

**Deprecated:** *Use [android.telephony.TelephonyManager#getDataNetworkType](../android/telephony/TelephonyManager.md))instead.*

Return a network-type-specific integer describing the subtype of the network.

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the network subtype |

### getSubtypeName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubtypeName(): String!
```

**Deprecated:** *Use [android.telephony.TelephonyManager#getDataNetworkType](../android/telephony/TelephonyManager.md))instead.*

Return a human-readable name describing the subtype of the network.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the network subtype |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

**Deprecated:** *Callers should switch to checking [NetworkCapabilities.hasTransport](../android/net/NetworkCapabilities.md))instead with one of the NetworkCapabilities#TRANSPORT_\* constants : [getType](../android/net/NetworkInfo.md))and [getTypeName](../android/net/NetworkInfo.md))cannot account for networks using multiple transports. Note that generally apps should not care about transport; [NetworkCapabilities.NET_CAPABILITY_NOT_METERED](../android/net/NetworkCapabilities.md) and [NetworkCapabilities.getLinkDownstreamBandwidthKbps](../android/net/NetworkCapabilities.md))are calls that apps concerned with meteredness or bandwidth should be looking at, as they offer this information with much better accuracy.*

Reports the type of network to which the info in this`NetworkInfo`pertains.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of [ConnectivityManager.TYPE_MOBILE](../android/net/ConnectivityManager.md), [android.net.ConnectivityManager#TYPE_WIFI](../android/net/ConnectivityManager.md), [ConnectivityManager.TYPE_WIMAX](../android/net/ConnectivityManager.md), [android.net.ConnectivityManager#TYPE_ETHERNET](../android/net/ConnectivityManager.md), [ConnectivityManager.TYPE_BLUETOOTH](../android/net/ConnectivityManager.md), or other types defined by [ConnectivityManager](../android/net/ConnectivityManager.md). |

### getTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTypeName(): String!
```

**Deprecated:** *Callers should switch to checking [NetworkCapabilities.hasTransport](../android/net/NetworkCapabilities.md))instead with one of the NetworkCapabilities#TRANSPORT_\* constants : [getType](../android/net/NetworkInfo.md))and [getTypeName](../android/net/NetworkInfo.md))cannot account for networks using multiple transports. Note that generally apps should not care about transport; [NetworkCapabilities.NET_CAPABILITY_NOT_METERED](../android/net/NetworkCapabilities.md) and [NetworkCapabilities.getLinkDownstreamBandwidthKbps](../android/net/NetworkCapabilities.md))are calls that apps concerned with meteredness or bandwidth should be looking at, as they offer this information with much better accuracy.*

Return a human-readable name describe the type of the network, for example "WIFI" or "MOBILE".

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the network type |

### isAvailable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAvailable(): Boolean
```

**Deprecated:** *Apps should instead use the [android.net.ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md) API to learn about connectivity changes. android.net.ConnectivityManager#registerDefaultNetworkCallback and android.net.ConnectivityManager#registerNetworkCallback. These will give a more accurate picture of the connectivity state of the device and let apps react more easily and quickly to changes.*

Indicates whether network connectivity is possible. A network is unavailable when a persistent or semi-persistent condition prevents the possibility of connecting to that network. Examples include

- The device is out of the coverage area for any network of this type.
- The device is on a network other than the home network (i.e., roaming), and data roaming has been disabled.
- The device's radio is turned off, e.g., because airplane mode is enabled.

Since Android L, this always returns`true`, because the system only returns info for available networks.

<br />

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the network is available,`false`otherwise |

### isConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isConnected(): Boolean
```

**Deprecated:** *Apps should instead use the [android.net.ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md) API to learn about connectivity changes. See android.net.ConnectivityManager#registerDefaultNetworkCallback and android.net.ConnectivityManager#registerNetworkCallback. These will give a more accurate picture of the connectivity state of the device and let apps react more easily and quickly to changes.*

Indicates whether network connectivity exists and it is possible to establish connections and pass data.

Always call this before attempting to perform data transactions.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if network connectivity exists,`false`otherwise. |

### isConnectedOrConnecting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isConnectedOrConnecting(): Boolean
```

**Deprecated:** *Apps should instead use the [android.net.ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md) API to learn about connectivity changes. android.net.ConnectivityManager#registerDefaultNetworkCallback and android.net.ConnectivityManager#registerNetworkCallback. These will give a more accurate picture of the connectivity state of the device and let apps react more easily and quickly to changes.*

Indicates whether network connectivity exists or is in the process of being established. This is good for applications that need to do anything related to the network other than read or write data. For the latter, call [isConnected()](../android/net/NetworkInfo.md))instead, which guarantees that the network is fully usable.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if network connectivity exists or is in the process of being established,`false`otherwise. |

### isFailover

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFailover(): Boolean
```

**Deprecated:** *This field is not populated in recent Android releases, and does not make a lot of sense in a multi-network world.*

Indicates whether the current attempt to connect to the network resulted from the ConnectivityManager trying to fail over to this network following a disconnect from another network.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this is a failover attempt,`false`otherwise. |

### isRoaming

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRoaming(): Boolean
```

**Deprecated:** *Callers should switch to checking [NetworkCapabilities.NET_CAPABILITY_NOT_ROAMING](../android/net/NetworkCapabilities.md) instead, since that handles more complex situations, such as VPNs.*

Indicates whether the device is currently roaming on this network. When`true`, it suggests that use of data on this network may incur extra costs.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if roaming is in effect,`false`otherwise. |

### setDetailedState

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDetailedState(
    detailedState: NetworkInfo.DetailedState, 
    reason: String?, 
    extraInfo: String?
): Unit
```

**Deprecated:** *Use [NetworkCapabilities](../android/net/NetworkCapabilities.md) instead.*

Sets the fine-grained state of the network. This is only useful for testing.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `detailedState` | [NetworkInfo.DetailedState](../android/net/NetworkInfo.DetailedState.md):the [DetailedState](../android/net/NetworkInfo.DetailedState.md). This value cannot be`null`. |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a`String`indicating the reason for the state change, if one was supplied. May be`null`. |
| `extraInfo` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:an optional`String`providing additional network state information passed up from the lower networking layers. This value may be`null`. |
| --- | --- |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NetworkInfo!>
```

**Deprecated:** *Deprecated in Java.*
