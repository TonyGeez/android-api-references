# IdentityChangedListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/aware/IdentityChangedListener "View this page in Java") 
| --- | --- |

```
open class IdentityChangedListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.IdentityChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener#) |

Base class for Aware identity/cluster changes callbacks. Should be extended by applications and set when calling [WifiAwareManager.attach(AttachCallback, IdentityChangedListener,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.net.wifi.aware.IdentityChangedListener,%20android.os.Handler)). These are callbacks applying to the Aware connection as a whole - not to specific publish or subscribe sessions - for that see [DiscoverySessionCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLUSTER_CHANGE_EVENT_JOINED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener#CLUSTER_CHANGE_EVENT_JOINED:kotlin.Int) Wi-Fi Aware cluster change event type when joining a cluster. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLUSTER_CHANGE_EVENT_STARTED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener#CLUSTER_CHANGE_EVENT_STARTED:kotlin.Int) Wi-Fi Aware cluster change event type when starting a cluster. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IdentityChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener#IdentityChangedListener())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClusterIdChanged](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener#onClusterIdChanged(kotlin.Int,%20android.net.MacAddress))`(`clusterEventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `clusterId:` ` [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)`)` Cluster ID changes could be trigger by either cluster started event or cluster joined event. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onIdentityChanged](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener#onIdentityChanged(kotlin.ByteArray))`(`mac:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Identity change may be due to device joining a cluster, starting a cluster, or discovery interface change (addresses are randomized at regular intervals). |

## Constants

### CLUSTER_CHANGE_EVENT_JOINED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLUSTER_CHANGE_EVENT_JOINED: Int
```

Wi-Fi Aware cluster change event type when joining a cluster. 

 Value: 1

### CLUSTER_CHANGE_EVENT_STARTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLUSTER_CHANGE_EVENT_STARTED: Int
```

Wi-Fi Aware cluster change event type when starting a cluster. 

 Value: 0

## Public constructors

### IdentityChangedListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IdentityChangedListener()
```

## Public methods

### onClusterIdChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onClusterIdChanged(
    clusterEventType: Int, 
    clusterId: MacAddress
): Unit
```

Cluster ID changes could be trigger by either cluster started event or cluster joined event.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clusterEventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of events that triggered the change of the cluster ID. Value is [android.net.wifi.aware.IdentityChangedListener#CLUSTER_CHANGE_EVENT_STARTED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener#CLUSTER_CHANGE_EVENT_STARTED:kotlin.Int), or [android.net.wifi.aware.IdentityChangedListener#CLUSTER_CHANGE_EVENT_JOINED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener#CLUSTER_CHANGE_EVENT_JOINED:kotlin.Int) |
| `clusterId` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#):The cluster id that the device just joined. This value cannot be`null`. |

### onIdentityChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onIdentityChanged(mac: ByteArray!): Unit
```

Identity change may be due to device joining a cluster, starting a cluster, or discovery interface change (addresses are randomized at regular intervals). The implication is that peers you've been communicating with may no longer recognize you and you need to re-establish your identity - e.g. by starting a discovery session.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mac` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The MAC address of the Aware discovery interface. The application must have the [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) to get the actual MAC address, otherwise all 0's will be provided. |
