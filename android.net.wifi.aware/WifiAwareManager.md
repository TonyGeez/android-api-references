# WifiAwareManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiAwareManager

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/aware/WifiAwareManager "View this page in Java") 

```
open class WifiAwareManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.aware.WifiAwareManager](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#) |

This class provides the primary API for managing Wi-Fi Aware operations: discovery and peer-to-peer data connections.

The class provides access to:

- Initialize a Aware cluster (peer-to-peer synchronization). Refer to [attach(android.net.wifi.aware.AttachCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler)).
- Create discovery sessions (publish or subscribe sessions). Refer to [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback, Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))and [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback, Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#subscribe(android.net.wifi.aware.SubscribeConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler)).
- Create a Aware network specifier to be used with [ConnectivityManager.requestNetwork(NetworkRequest, ConnectivityManager.NetworkCallback)](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback))to set-up a Aware connection with a peer. Refer to [WifiAwareNetworkSpecifier.Builder](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder).

Aware may not be usable when Wi-Fi is disabled (and other conditions). To validate that the functionality is available use the [isAvailable()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#isAvailable())function. To track changes in Aware usability register for the [ACTION_WIFI_AWARE_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#ACTION_WIFI_AWARE_STATE_CHANGED:kotlin.String) broadcast. Note that this broadcast is not sticky - you should register for it and then check the above API to avoid a race condition.

An application must use [attach(android.net.wifi.aware.AttachCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))to initialize a Aware cluster - before making any other Aware operation. Aware cluster membership is a device-wide operation - the API guarantees that the device is in a cluster or joins a Aware cluster (or starts one if none can be found). Information about attach success (or failure) are returned in callbacks of [AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback). Proceed with Aware discovery or connection setup only after receiving confirmation that Aware attach succeeded - [AttachCallback.onAttached(WifiAwareSession)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback#onAttached(android.net.wifi.aware.WifiAwareSession)). When an application is finished using Aware it**must** use the [WifiAwareSession.close()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#close())API to indicate to the Aware service that the device may detach from the Aware cluster. The device will actually disable Aware once the last application detaches.

Once a Aware attach is confirmed use the [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback, Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))or [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#subscribe(android.net.wifi.aware.SubscribeConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))to create publish or subscribe Aware discovery sessions. Events are called on the provided callback object [DiscoverySessionCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback). Specifically, the [DiscoverySessionCallback.onPublishStarted(PublishDiscoverySession)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPublishStarted(android.net.wifi.aware.PublishDiscoverySession))and [DiscoverySessionCallback.onSubscribeStarted(](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onSubscribeStarted(android.net.wifi.aware.SubscribeDiscoverySession))return [PublishDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession) and [SubscribeDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession) objects respectively on which additional session operations can be performed, e.g. updating the session [PublishDiscoverySession.updatePublish(PublishConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession#updatePublish(android.net.wifi.aware.PublishConfig))and [SubscribeDiscoverySession.updateSubscribe(SubscribeConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession#updateSubscribe(android.net.wifi.aware.SubscribeConfig)). Sessions can also be used to send messages using the[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))APIs. When an application is finished with a discovery session it**must** terminate it using the [DiscoverySession.close()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#close())API.

Creating connections between Aware devices is managed by the standard [ConnectivityManager.requestNetwork(NetworkRequest,](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)). The [NetworkRequest](https://developer.android.com/reference/kotlin/android/net/NetworkRequest.html#) object should be constructed with:

- [NetworkRequest.Builder.addTransportType(int)](https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#addTransportType(kotlin.Int))of [android.net.NetworkCapabilities#TRANSPORT_WIFI_AWARE](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#TRANSPORT_WIFI_AWARE:kotlin.Int).
- [NetworkRequest.Builder.setNetworkSpecifier(String)](https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#setNetworkSpecifier(kotlin.String))using [WifiAwareNetworkSpecifier.Builder](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder).

<br />

Restricted for SDK Runtime environment in API level 34.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_WIFI_AWARE_RESOURCE_CHANGED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#ACTION_WIFI_AWARE_RESOURCE_CHANGED:kotlin.String) Intent broadcast sent whenever Wi-Fi Aware resource availability has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_WIFI_AWARE_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#ACTION_WIFI_AWARE_STATE_CHANGED:kotlin.String) Broadcast intent action to indicate that the state of Wi-Fi Aware availability has changed and all active Aware sessions are no longer usable. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AWARE_RESOURCES](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#EXTRA_AWARE_RESOURCES:kotlin.String) Sent as a part of [ACTION_WIFI_AWARE_RESOURCE_CHANGED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#ACTION_WIFI_AWARE_RESOURCE_CHANGED:kotlin.String) that contains an instance of [AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources) representing the current Wi-Fi Aware resources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_AWARE_DATA_PATH_ROLE_INITIATOR](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_INITIATOR:kotlin.Int) Connection creation role is that of INITIATOR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_AWARE_DATA_PATH_ROLE_RESPONDER](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_RESPONDER:kotlin.Int) Connection creation role is that of RESPONDER. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_AWARE_DISCOVERY_LOST_REASON_PEER_NOT_VISIBLE](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DISCOVERY_LOST_REASON_PEER_NOT_VISIBLE:kotlin.Int) Reason code provided in [DiscoverySessionCallback.onServiceLost(PeerHandle, int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceLost(android.net.wifi.aware.PeerHandle,%20kotlin.Int))indicating that the service advertised by the peer is no longer visible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIFI_AWARE_DISCOVERY_LOST_REASON_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DISCOVERY_LOST_REASON_UNKNOWN:kotlin.Int) Reason code provided in [DiscoverySessionCallback.onServiceLost(PeerHandle, int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceLost(android.net.wifi.aware.PeerHandle,%20kotlin.Int))indicating that the service was lost for unknown reason. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attach](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.net.wifi.aware.IdentityChangedListener,%20android.os.Handler))`(`attachCallback:` ` [AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback)`, `identityChangedListener:` ` [IdentityChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Attach to the Wi-Fi Aware service - enabling the application to create discovery sessions or create connections to peers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attach](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))`(`attachCallback:` ` [AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Attach to the Wi-Fi Aware service - enabling the application to create discovery sessions or create connections to peers. |
| open [AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources)? | [getAvailableAwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#getAvailableAwareResources())`()` Return the available resources of the Wi-Fi aware service: a set of parameters which specify limitations on service usage, e. |
| open [Characteristics](https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics)? | [getCharacteristics](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#getCharacteristics())`()` Returns the characteristics of the Wi-Fi Aware interface: a set of parameters which specify limitations on configurations, e. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getPairedDevices](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#getPairedDevices(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `resultsCallback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>`)` Get all the paired devices configured by the calling app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#isAvailable())`()` Returns the current status of Aware API: whether or not Aware is available. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeviceAttached](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#isDeviceAttached())`()` Return the current status of the Aware service: whether or not the device is already attached to an Aware cluster. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInstantCommunicationModeEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#isInstantCommunicationModeEnabled())`()` Return the current status of the Wifi Aware instant communication mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [isOpportunisticModeEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#isOpportunisticModeEnabled(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `resultsCallback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!>`)` Indicate whether all Wi-Fi Aware sessions created by the calling app are opportunistic as defined and configured by [setOpportunisticModeEnabled(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#setOpportunisticModeEnabled(kotlin.Boolean)) Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSetChannelOnDataPathSupported](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#isSetChannelOnDataPathSupported())`()` Return the device support for setting a channel requirement in a data-path request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePairedDevice](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#removePairedDevice(kotlin.String))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Remove the target paired device setup by the caller by [DiscoverySession.initiatePairingRequest(PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiatePairingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String))and [DiscoverySession.acceptPairingRequest(int, PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#acceptPairingRequest(kotlin.Int,%20android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String)) Requires [android.Manifest.permission#CHANGE_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetPairedDevices](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#resetPairedDevices())`()` Reset all paired devices setup by the caller by [DiscoverySession.initiatePairingRequest(PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiatePairingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String))and [DiscoverySession.acceptPairingRequest(int, PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#acceptPairingRequest(kotlin.Int,%20android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String)) Requires [android.Manifest.permission#CHANGE_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpportunisticModeEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#setOpportunisticModeEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set all Wi-Fi Aware sessions created by the calling app to be opportunistic. |

## Constants

### ACTION_WIFI_AWARE_RESOURCE_CHANGED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_WIFI_AWARE_RESOURCE_CHANGED: String
```

Intent broadcast sent whenever Wi-Fi Aware resource availability has changed. The resources are attached with the [EXTRA_AWARE_RESOURCES](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#EXTRA_AWARE_RESOURCES:kotlin.String) extra. The resources can also be obtained using the [getAvailableAwareResources()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#getAvailableAwareResources())method. To receive this broadcast, apps must hold [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String).

Note: The broadcast is only delivered to registered receivers - no manifest registered components will be launched. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String) 

 Value: "android.net.wifi.aware.action.WIFI_AWARE_RESOURCE_CHANGED"

### ACTION_WIFI_AWARE_STATE_CHANGED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_WIFI_AWARE_STATE_CHANGED: String
```

Broadcast intent action to indicate that the state of Wi-Fi Aware availability has changed and all active Aware sessions are no longer usable. Use the [isAvailable()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#isAvailable())to query the current status. This broadcast is**not** sticky, use the [isAvailable()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#isAvailable())API after registering the broadcast to check the current state of Wi-Fi Aware.

Note: The broadcast is only delivered to registered receivers - no manifest registered components will be launched. 

 Value: "android.net.wifi.aware.action.WIFI_AWARE_STATE_CHANGED"

### EXTRA_AWARE_RESOURCES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AWARE_RESOURCES: String
```

Sent as a part of [ACTION_WIFI_AWARE_RESOURCE_CHANGED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#ACTION_WIFI_AWARE_RESOURCE_CHANGED:kotlin.String) that contains an instance of [AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources) representing the current Wi-Fi Aware resources. 

 Value: "android.net.wifi.aware.extra.AWARE_RESOURCES"

### WIFI_AWARE_DATA_PATH_ROLE_INITIATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_AWARE_DATA_PATH_ROLE_INITIATOR: Int
```

Connection creation role is that of INITIATOR. Used to create a network specifier string when requesting a Aware network. 

 Value: 0

**See Also**

- [android.net.wifi.aware.WifiAwareSession#createNetworkSpecifierOpen(int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#createNetworkSpecifierOpen(kotlin.Int,%20kotlin.ByteArray))
- [android.net.wifi.aware.WifiAwareSession#createNetworkSpecifierPassphrase(int, byte[], String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#createNetworkSpecifierPassphrase(kotlin.Int,%20kotlin.ByteArray,%20kotlin.String)) 

### WIFI_AWARE_DATA_PATH_ROLE_RESPONDER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_AWARE_DATA_PATH_ROLE_RESPONDER: Int
```

Connection creation role is that of RESPONDER. Used to create a network specifier string when requesting a Aware network. 

 Value: 1

**See Also**

- [android.net.wifi.aware.WifiAwareSession#createNetworkSpecifierOpen(int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#createNetworkSpecifierOpen(kotlin.Int,%20kotlin.ByteArray))
- [android.net.wifi.aware.WifiAwareSession#createNetworkSpecifierPassphrase(int, byte[], String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#createNetworkSpecifierPassphrase(kotlin.Int,%20kotlin.ByteArray,%20kotlin.String)) 

### WIFI_AWARE_DISCOVERY_LOST_REASON_PEER_NOT_VISIBLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_AWARE_DISCOVERY_LOST_REASON_PEER_NOT_VISIBLE: Int
```

Reason code provided in [DiscoverySessionCallback.onServiceLost(PeerHandle, int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceLost(android.net.wifi.aware.PeerHandle,%20kotlin.Int))indicating that the service advertised by the peer is no longer visible. This may be because the peer is out of range or because the peer stopped advertising this service. 

 Value: 1

### WIFI_AWARE_DISCOVERY_LOST_REASON_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIFI_AWARE_DISCOVERY_LOST_REASON_UNKNOWN: Int
```

Reason code provided in [DiscoverySessionCallback.onServiceLost(PeerHandle, int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceLost(android.net.wifi.aware.PeerHandle,%20kotlin.Int))indicating that the service was lost for unknown reason. 

 Value: 0

## Public methods

### attach

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attach(
    attachCallback: AttachCallback, 
    identityChangedListener: IdentityChangedListener, 
    handler: Handler?
): Unit
```

Attach to the Wi-Fi Aware service - enabling the application to create discovery sessions or create connections to peers. The device will attach to an existing cluster if it can find one or create a new cluster (if it is the first to enable Aware in its vicinity). Results (e.g. successful attach to a cluster) are provided to the`attachCallback`object. An application**must** call [WifiAwareSession.close()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#close())when done with the Wi-Fi Aware object.

Note: a Aware cluster is a shared resource - if the device is already attached to a cluster then this function will simply indicate success immediately using the same`attachCallback`.

This version of the API attaches a listener to receive the MAC address of the Aware interface on startup and whenever it is updated (it is randomized at regular intervals for privacy). If targeting [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int) or later, the application must have [android.Manifest.permission#NEARBY_WIFI_DEVICES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String) with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String). If targeting an earlier release than [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int), the application must have [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String). Apps without [android.Manifest.permission#NEARBY_WIFI_DEVICES](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) can use the [attach(android.net.wifi.aware.AttachCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))version. Note that aside from permission requirements the [IdentityChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener) will wake up the host at regular intervals causing higher power consumption, do not use it unless the information is necessary (e.g. for out-of-band discovery).

| Parameters ||
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attachCallback` | [AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback):A callback for attach events, extended from [AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback). This value cannot be`null`. |
| `identityChangedListener` | [IdentityChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener):A callback for changed identity or cluster ID, extended from [IdentityChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/aware/IdentityChangedListener). This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:The Handler on whose thread to execute the callbacks of the`attachCallback`and`identityChangedListener`objects. If a null is provided then the application's main thread will be used. |

### attach

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attach(
    attachCallback: AttachCallback, 
    handler: Handler?
): Unit
```

Attach to the Wi-Fi Aware service - enabling the application to create discovery sessions or create connections to peers. The device will attach to an existing cluster if it can find one or create a new cluster (if it is the first to enable Aware in its vicinity). Results (e.g. successful attach to a cluster) are provided to the`attachCallback`object. An application**must** call [WifiAwareSession.close()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#close())when done with the Wi-Fi Aware object.

Note: a Aware cluster is a shared resource - if the device is already attached to a cluster then this function will simply indicate success immediately using the same`attachCallback`. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String) and [android.Manifest.permission#CHANGE_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String)

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attachCallback` | [AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback):A callback for attach events, extended from [AttachCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AttachCallback). This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:The Handler on whose thread to execute the callbacks of the`attachCallback`object. If a null is provided then the application's main thread will be used. |

### getAvailableAwareResources

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAvailableAwareResources(): AwareResources?
```

Return the available resources of the Wi-Fi aware service: a set of parameters which specify limitations on service usage, e.g the number of data-paths which could be created.

May return`null`if the Wi-Fi Aware service is not initialized. Use [attach(android.net.wifi.aware.AttachCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))or [attach(android.net.wifi.aware.AttachCallback,android.net.wifi.aware.IdentityChangedListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.net.wifi.aware.IdentityChangedListener,%20android.os.Handler))to initialize the Wi-Fi Aware service. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String)

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources)? | An object specifying the currently available resource of the Wi-Fi Aware service. |

### getCharacteristics

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacteristics(): Characteristics?
```

Returns the characteristics of the Wi-Fi Aware interface: a set of parameters which specify limitations on configurations, e.g. the maximum service name length.

May return`null`if the Wi-Fi Aware service is not initialized. Use [attach(android.net.wifi.aware.AttachCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))or [attach(android.net.wifi.aware.AttachCallback,android.net.wifi.aware.IdentityChangedListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.net.wifi.aware.IdentityChangedListener,%20android.os.Handler))to initialize the Wi-Fi Aware service. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String)

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Characteristics](https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics)? | An object specifying configuration limitations of Aware. |

### getPairedDevices

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPairedDevices(
    executor: Executor, 
    resultsCallback: Consumer<MutableList<String!>!>
): Unit
```

Get all the paired devices configured by the calling app. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String)

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor on which callback will be invoked. This value cannot be`null`. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>:An asynchronous callback that will return a list of paired devices' alias This value cannot be`null`. |

### isAvailable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAvailable(): Boolean
```

Returns the current status of Aware API: whether or not Aware is available. To track changes in the state of Aware API register for the [ACTION_WIFI_AWARE_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#ACTION_WIFI_AWARE_STATE_CHANGED:kotlin.String) broadcast. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | A boolean indicating whether the app can use the Aware API at this time (true) or not (false). |

### isDeviceAttached

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDeviceAttached(): Boolean
```

Return the current status of the Aware service: whether or not the device is already attached to an Aware cluster. To attach to an Aware cluster, please use [attach(android.net.wifi.aware.AttachCallback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.os.Handler))or [attach(android.net.wifi.aware.AttachCallback,android.net.wifi.aware.IdentityChangedListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#attach(android.net.wifi.aware.AttachCallback,%20android.net.wifi.aware.IdentityChangedListener,%20android.os.Handler)). 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | A boolean indicating whether the device is attached to a cluster at this time (true) or not (false). |

### isInstantCommunicationModeEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInstantCommunicationModeEnabled(): Boolean
```

Return the current status of the Wifi Aware instant communication mode. If the device doesn't support this feature, return will always be false. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if it is enabled, false otherwise. |

**See Also**

- [android.net.wifi.aware.Characteristics#isInstantCommunicationModeSupported()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#isInstantCommunicationModeSupported()) 

### isOpportunisticModeEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOpportunisticModeEnabled(
    executor: Executor, 
    resultsCallback: Consumer<Boolean!>
): Unit
```

Indicate whether all Wi-Fi Aware sessions created by the calling app are opportunistic as defined and configured by [setOpportunisticModeEnabled(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#setOpportunisticModeEnabled(kotlin.Boolean)) 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String)

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor on which callback will be invoked. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>:An asynchronous callback that will return boolean This value cannot be`null`. |

### isSetChannelOnDataPathSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSetChannelOnDataPathSupported(): Boolean
```

Return the device support for setting a channel requirement in a data-path request. If true the channel set by [WifiAwareNetworkSpecifier.Builder.setChannelFrequencyMhz(int, boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder#setChannelFrequencyMhz(kotlin.Int,%20kotlin.Boolean))will be honored, otherwise it will be ignored. 
Requires [android.Manifest.permission#ACCESS_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True is the device support set channel on data-path request, false otherwise. |

### removePairedDevice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePairedDevice(alias: String): Unit
```

Remove the target paired device setup by the caller by [DiscoverySession.initiatePairingRequest(PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiatePairingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String))and [DiscoverySession.acceptPairingRequest(int, PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#acceptPairingRequest(kotlin.Int,%20android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String)) 
Requires [android.Manifest.permission#CHANGE_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String)

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The alias set by the caller This value cannot be`null`. |

### resetPairedDevices

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resetPairedDevices(): Unit
```

Reset all paired devices setup by the caller by [DiscoverySession.initiatePairingRequest(PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiatePairingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String))and [DiscoverySession.acceptPairingRequest(int, PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#acceptPairingRequest(kotlin.Int,%20android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String)) 
Requires [android.Manifest.permission#CHANGE_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String) 

### setOpportunisticModeEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOpportunisticModeEnabled(enabled: Boolean): Unit
```

Set all Wi-Fi Aware sessions created by the calling app to be opportunistic. Opportunistic Wi-Fi Aware sessions are considered low priority and may be torn down (the sessions or the Aware interface) if there are resource conflicts. 
Requires [android.Manifest.permission#CHANGE_WIFI_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String)

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True to configure all Wi-Fi Aware sessions by the calling app as Opportunistic. False by default. |
