Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectivityManager

Kotlin | [Java](ConnectivityManager.md)
| --- | --- |

```
open class ConnectivityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ConnectivityManager](ConnectivityManager.md) |

Class that answers queries about the state of network connectivity. It also notifies applications when network connectivity changes.

The primary responsibilities of this class are to:

1. Monitor network connections (Wi-Fi, GPRS, UMTS, etc.)
2. Send broadcast intents when network connectivity changes
3. Attempt to "fail over" to another network when connectivity to a network is lost
4. Provide an API that allows applications to query the coarse-grained or fine-grained state of the available networks
5. Provide an API that allows applications to request and select networks for their data traffic

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` Base class for `NetworkRequest` callbacks. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.OnNetworkActiveListener` Callback for use with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#addDefaultNetworkActiveListener(android.net.ConnectivityManager.OnNetworkActiveListener)` to find out when the system default network has gone in to a high power state. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#ACTION_BACKGROUND_DATA_SETTING_CHANGED:kotlin.String` Broadcast Action: The setting for background data usage has changed values. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#ACTION_CAPTIVE_PORTAL_SIGN_IN:kotlin.String` The device has connected to a network that has presented a captive portal, which is blocking Internet connectivity. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#ACTION_RESTRICT_BACKGROUND_CHANGED:kotlin.String` A change in the background metered network activity restriction has occurred. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#CONNECTIVITY_ACTION:kotlin.String` A change in network connectivity has occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#DEFAULT_NETWORK_PREFERENCE:kotlin.Int` If you want to set the default network preference,you can directly change the networkAttributes array in framework's config. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_CAPTIVE_PORTAL:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/CaptivePortal` object included with the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#ACTION_CAPTIVE_PORTAL_SIGN_IN:kotlin.String` intent. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_CAPTIVE_PORTAL_URL:kotlin.String` Key for passing a URL to the captive portal login activity. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_EXTRA_INFO:kotlin.String` The lookup key for a string that provides optionally supplied extra information about the network state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_IS_FAILOVER:kotlin.String` The lookup key for a boolean that indicates whether a connect event is for a network to which the connectivity manager was failing over following a disconnect on another network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/Network` object included with the intent after successfully finding a network for the applications request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK_INFO:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK_REQUEST:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` object included with the intent after successfully finding a network for the applications request. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK_TYPE:kotlin.String` Network type which triggered a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#CONNECTIVITY_ACTION:kotlin.String` broadcast. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NO_CONNECTIVITY:kotlin.String` The lookup key for a boolean that indicates whether there is a complete lack of connectivity, i. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_OTHER_NETWORK_INFO:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` object. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_REASON:kotlin.String` The lookup key for a string that indicates why an attempt to connect to a network failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#MULTIPATH_PREFERENCE_HANDOVER:kotlin.Int` It is acceptable to briefly use multipath data to provide seamless connectivity for time-sensitive user-facing operations when the system default network is temporarily unresponsive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#MULTIPATH_PREFERENCE_PERFORMANCE:kotlin.Int` It is acceptable to use metered data to improve network latency and performance. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#MULTIPATH_PREFERENCE_RELIABILITY:kotlin.Int` It is acceptable to use small amounts of multipath data on an ongoing basis to provide a backup channel for traffic that is primarily going over another network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_DISABLED:kotlin.Int` Device is not restricting metered network activity while application is running on background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_ENABLED:kotlin.Int` Device is restricting metered network activity while application is running on background. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_WHITELISTED:kotlin.Int` Device is restricting metered network activity while application is running on background, but application is allowed to bypass it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_BLUETOOTH:kotlin.Int` A Bluetooth data connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_DUMMY:kotlin.Int` Fake data connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_ETHERNET:kotlin.Int` An Ethernet data connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE:kotlin.Int` A Mobile data connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE_DUN:kotlin.Int` A DUN-specific Mobile data connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE_HIPRI:kotlin.Int` A High Priority Mobile data connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE_MMS:kotlin.Int` An MMS-specific Mobile data connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE_SUPL:kotlin.Int` A SUPL-specific Mobile data connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_VPN:kotlin.Int` A virtual network using one or more native bearers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_WIFI:kotlin.Int` A WIFI data connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_WIMAX:kotlin.Int` A WiMAX data connection. |
| --- | --- |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#addDefaultNetworkActiveListener(android.net.ConnectivityManager.OnNetworkActiveListener)(l: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.OnNetworkActiveListener!)` Start listening to reports when the system's default data network is active, meaning it is a good time to perform network traffic. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)(network: https://developer.android.com/reference/kotlin/android/net/Network?)` Binds the current process to `network`. |
| open [SocketKeepalive](SocketKeepalive.md) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#createSocketKeepalive(android.net.Network,%20android.net.IpSecManager.UdpEncapsulationSocket,%20java.net.InetAddress,%20java.net.InetAddress,%20java.util.concurrent.Executor,%20android.net.SocketKeepalive.Callback)(network: https://developer.android.com/reference/kotlin/android/net/Network, socket: https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket, source: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#, destination: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/net/SocketKeepalive.Callback)` Request that keepalives be started on a IPsec NAT-T socket. |
| --- | --- |
| open [Network](Network.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getActiveNetwork()()` Returns a `https://developer.android.com/reference/kotlin/android/net/Network` object corresponding to the currently active default data network. |
| open [NetworkInfo](NetworkInfo.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getActiveNetworkInfo()()` Returns details about the currently active default data network. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [NetworkInfo](NetworkInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getAllNetworkInfo()()` Returns connection status information about all network types supported by the device. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Network](Network.md)!\> | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getAllNetworks()()` Returns an array of all `https://developer.android.com/reference/kotlin/android/net/Network` currently tracked by the framework. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getBackgroundDataSetting()()` Returns the value of the setting for background data usage. |
| open [Network](Network.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getBoundNetworkForProcess()()` Returns the `https://developer.android.com/reference/kotlin/android/net/Network` currently bound to this process via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)`, or `null` if no `https://developer.android.com/reference/kotlin/android/net/Network` is explicitly bound. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getConnectionOwnerUid(kotlin.Int,%20java.net.InetSocketAddress,%20java.net.InetSocketAddress)(protocol: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, local: https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#, remote: https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#)` Returns the `uid` of the owner of a network connection. |
| open [ProxyInfo](ProxyInfo.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getDefaultProxy()()` Get the current default HTTP proxy settings. |
| open [LinkProperties](LinkProperties.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getLinkProperties(android.net.Network)(network: https://developer.android.com/reference/kotlin/android/net/Network?)` Get the `https://developer.android.com/reference/kotlin/android/net/LinkProperties` for the given `https://developer.android.com/reference/kotlin/android/net/Network`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getMultipathPreference(android.net.Network)(network: https://developer.android.com/reference/kotlin/android/net/Network?)` Provides a hint to the calling application on whether it is desirable to use the multinetwork APIs (e.g., android.net.Network#openConnection, android.net.Network#bindSocket, etc.) for multipath data transfer on this network when it is not the system default network. |
| open [NetworkCapabilities](NetworkCapabilities.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkCapabilities(android.net.Network)(network: https://developer.android.com/reference/kotlin/android/net/Network?)` Get the `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for the given `https://developer.android.com/reference/kotlin/android/net/Network`, or null. |
| open [NetworkInfo](NetworkInfo.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkInfo(android.net.Network)(network: https://developer.android.com/reference/kotlin/android/net/Network?)` Returns connection status information about a particular Network. |
| --- | --- |
| open [NetworkInfo](NetworkInfo.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkInfo(kotlin.Int)(networkType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns connection status information about a particular network type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkPreference()()` Retrieves the current preferred network type. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkWatchlistConfigHash()()` The network watchlist is a list of domains and IP addresses that are associated with potentially harmful apps. |
| --- | --- |
| open static [Network](Network.md)? | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getProcessDefaultNetwork()()` Returns the `https://developer.android.com/reference/kotlin/android/net/Network` currently bound to this process via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)`, or `null` if no `https://developer.android.com/reference/kotlin/android/net/Network` is explicitly bound. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getRestrictBackgroundStatus()()` Determines if the calling application is subject to metered network restrictions while running on background. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#isActiveNetworkMetered()()` Returns if the currently active data network is metered. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#isDefaultNetworkActive()()` Return whether the data network is currently active. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#isNetworkTypeValid(kotlin.Int)(networkType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Tests if a given integer represents a valid network type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerBestMatchingNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback,%20android.os.Handler)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#)` Registers to receive notifications about the best matching network which satisfy the given `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerDefaultNetworkCallback(android.net.ConnectivityManager.NetworkCallback)(networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback)` Registers to receive notifications about changes in the application's default network. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerDefaultNetworkCallback(android.net.ConnectivityManager.NetworkCallback,%20android.os.Handler)(networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#)` Registers to receive notifications about changes in the application's default network. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.app.PendingIntent)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, operation: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)` Registers a PendingIntent to be sent when a network is available which satisfies the given `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback)` Registers to receive notifications about all networks which satisfy the given `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback,%20android.os.Handler)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#)` Registers to receive notifications about all networks which satisfy the given `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#releaseNetworkRequest(android.app.PendingIntent)(operation: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)` Removes a request made via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.app.PendingIntent)` |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#removeDefaultNetworkActiveListener(android.net.ConnectivityManager.OnNetworkActiveListener)(l: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.OnNetworkActiveListener)` Remove network active listener previously registered with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#addDefaultNetworkActiveListener(android.net.ConnectivityManager.OnNetworkActiveListener)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#reportBadNetwork(android.net.Network)(network: https://developer.android.com/reference/kotlin/android/net/Network?)` Report a problem network to the framework. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#reportNetworkConnectivity(android.net.Network,%20kotlin.Boolean)(network: https://developer.android.com/reference/kotlin/android/net/Network?, hasConnectivity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Report to the framework whether a network has working connectivity. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestBandwidthUpdate(android.net.Network)(network: https://developer.android.com/reference/kotlin/android/net/Network)` Requests bandwidth update for a given `https://developer.android.com/reference/kotlin/android/net/Network` and returns whether the update request is accepted by ConnectivityService. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.app.PendingIntent)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, operation: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)` Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback)` Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback,%20android.os.Handler)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#)` Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback,%20android.os.Handler,%20kotlin.Int)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#, timeoutMs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`, limited by a timeout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback,%20kotlin.Int)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback, timeoutMs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`, limited by a timeout. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#reserveNetwork(android.net.NetworkRequest,%20android.os.Handler,%20android.net.ConnectivityManager.NetworkCallback)(request: https://developer.android.com/reference/kotlin/android/net/NetworkRequest, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#, networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback)` Reserve a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#setNetworkPreference(kotlin.Int)(preference: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies the preferred network type. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#setProcessDefaultNetwork(android.net.Network)(network: https://developer.android.com/reference/kotlin/android/net/Network?)` Binds the current process to `network`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.app.PendingIntent)(operation: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)` Unregisters a callback previously registered via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.app.PendingIntent)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)(networkCallback: https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback)` Unregisters a `NetworkCallback` and possibly releases networks originating from `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` and `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` calls. |

## Constants

### ACTION_BACKGROUND_DATA_SETTING_CHANGED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_BACKGROUND_DATA_SETTING_CHANGED: String
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, availability of background data depends on several combined factors, and this broadcast is no longer sent. Instead, when background data is unavailable, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getActiveNetworkInfo()` will now appear disconnected. During first boot after a platform upgrade, this broadcast will be sent once if `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getBackgroundDataSetting()` was `false` before the upgrade.*

Broadcast Action: The setting for background data usage has changed values. Use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getBackgroundDataSetting()` to get the current value.

If an application uses the network in the background, it should listen for this broadcast and stop using the background data if the value is `false`.

<br />

 Value: "android.net.conn.BACKGROUND_DATA_SETTING_CHANGED"

### ACTION_CAPTIVE_PORTAL_SIGN_IN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CAPTIVE_PORTAL_SIGN_IN: String
```

The device has connected to a network that has presented a captive portal, which is blocking Internet connectivity. The user was presented with a notification that network sign in is required, and the user invoked the notification's action indicating they desire to sign in to the network. Apps handling this activity should facilitate signing in to the network. This action includes a `https://developer.android.com/reference/kotlin/android/net/Network` typed extra called `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK:kotlin.String` that represents the network presenting the captive portal; all communication with the captive portal must be done using this `Network` object.

<br />

This activity includes a `https://developer.android.com/reference/kotlin/android/net/CaptivePortal` extra named `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_CAPTIVE_PORTAL:kotlin.String` that can be used to indicate different outcomes of the captive portal sign in to the system:

- When the app handling this action believes the user has signed in to the network and the captive portal has been dismissed, the app should call `https://developer.android.com/reference/kotlin/android/net/CaptivePortal#reportCaptivePortalDismissed()` so the system can reevaluate the network. If reevaluation finds the network no longer subject to a captive portal, the network may become the default active data network.
- When the app handling this action believes the user explicitly wants to ignore the captive portal and the network, the app should call `https://developer.android.com/reference/kotlin/android/net/CaptivePortal#ignoreNetwork()`.

 Value: "android.net.conn.CAPTIVE_PORTAL"

### ACTION_RESTRICT_BACKGROUND_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_RESTRICT_BACKGROUND_CHANGED: String
```

A change in the background metered network activity restriction has occurred.

Applications should call `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getRestrictBackgroundStatus()` to check if the restriction applies to them.

This is only sent to registered receivers, not manifest receivers.

 Value: "android.net.conn.RESTRICT_BACKGROUND_CHANGED"

### CONNECTIVITY_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTIVITY_ACTION: String
```

**Deprecated:** *apps should use the more versatile #requestNetwork, #registerNetworkCallback or #registerDefaultNetworkCallback functions instead for faster and more detailed updates about the network changes they care about.*

A change in network connectivity has occurred. A default connection has either been established or lost. The NetworkInfo for the affected network is sent as an extra; it should be consulted to see what kind of connectivity event occurred.

<br />

Apps targeting Android 7.0 (API level 24) and higher do not receive this broadcast if they declare the broadcast receiver in their manifest. Apps will still receive broadcasts if they register their `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` with android.content.Context#registerReceiver and that context is still valid.

<br />

If this is a connection that was the result of failing over from a disconnected network, then the FAILOVER_CONNECTION boolean extra is set to true.

<br />

For a loss of connectivity, if the connectivity manager is attempting to connect (or has already connected) to another network, the NetworkInfo for the new network is also passed as an extra. This lets any receivers of the broadcast know that they should not necessarily tell the user that no data traffic will be possible. Instead, the receiver should expect another broadcast soon, indicating either that the failover attempt succeeded (and so there is still overall data connectivity), or that the failover attempt failed, meaning that all connectivity has been lost.

<br />

For a disconnect event, the boolean extra EXTRA_NO_CONNECTIVITY is set to `true` if there are no connected networks at all.

<br />

Note that this broadcast is deprecated and generally tries to implement backwards compatibility with older versions of Android. As such, it may not reflect new capabilities of the system, like multiple networks being connected at the same time, the details of newer technology, or changes in tethering state.

 Value: "android.net.conn.CONNECTIVITY_CHANGE"

### DEFAULT_NETWORK_PREFERENCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_NETWORK_PREFERENCE: Int
```

**Deprecated:** *Since we support so many more networks now, the single network default network preference can't really express the hierarchy. Instead, the default is defined by the networkAttributes in config.xml. You can determine the current value by calling `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkPreference()` from an App.*

If you want to set the default network preference,you can directly change the networkAttributes array in framework's config.xml.

 Value: 1

### EXTRA_CAPTIVE_PORTAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CAPTIVE_PORTAL: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/CaptivePortal` object included with the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#ACTION_CAPTIVE_PORTAL_SIGN_IN:kotlin.String` intent. The `CaptivePortal` object can be used to either indicate to the system that the captive portal has been dismissed or that the user does not want to pursue signing in to captive portal. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "android.net.extra.CAPTIVE_PORTAL"

### EXTRA_CAPTIVE_PORTAL_URL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CAPTIVE_PORTAL_URL: String
```

Key for passing a URL to the captive portal login activity.

 Value: "android.net.extra.CAPTIVE_PORTAL_URL"

### EXTRA_EXTRA_INFO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EXTRA_INFO: String
```

**Deprecated:** *See `https://developer.android.com/reference/kotlin/android/net/NetworkInfo#getExtraInfo()`.*

The lookup key for a string that provides optionally supplied extra information about the network state. The information may be passed up from the lower networking layers, and its meaning may be specific to a particular network type. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)`.

 Value: "extraInfo"

### EXTRA_IS_FAILOVER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_FAILOVER: String
```

**Deprecated:** *See `https://developer.android.com/reference/kotlin/android/net/NetworkInfo`.*

The lookup key for a boolean that indicates whether a connect event is for a network to which the connectivity manager was failing over following a disconnect on another network. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getBooleanExtra(kotlin.String,%20kotlin.Boolean)`.

 Value: "isFailover"

### EXTRA_NETWORK

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NETWORK: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/Network` object included with the intent after successfully finding a network for the applications request. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

Note that if you intend to invoke `https://developer.android.com/reference/kotlin/android/net/Network#openConnection(java.net.URL)` then you must get a ConnectivityManager instance before doing so.

 Value: "android.net.extra.NETWORK"

### EXTRA_NETWORK_INFO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NETWORK_INFO: String
```

**Deprecated:** *The `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` object is deprecated, as many of its properties can't accurately represent modern network characteristics. Please obtain information about networks from the `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` or `https://developer.android.com/reference/kotlin/android/net/LinkProperties` objects instead.*

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` object. Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "networkInfo"

### EXTRA_NETWORK_REQUEST

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NETWORK_REQUEST: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` object included with the intent after successfully finding a network for the applications request. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "android.net.extra.NETWORK_REQUEST"

### EXTRA_NETWORK_TYPE

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NETWORK_TYPE: String
```

**Deprecated:** *The network type is not rich enough to represent the characteristics of modern networks. Please use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` instead, in particular the transports.*

Network type which triggered a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#CONNECTIVITY_ACTION:kotlin.String` broadcast.

 Value: "networkType"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)`

### EXTRA_NO_CONNECTIVITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NO_CONNECTIVITY: String
```

The lookup key for a boolean that indicates whether there is a complete lack of connectivity, i.e., no network is available. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getBooleanExtra(kotlin.String,%20kotlin.Boolean)`.

 Value: "noConnectivity"

### EXTRA_OTHER_NETWORK_INFO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_OTHER_NETWORK_INFO: String
```

**Deprecated:** *See `https://developer.android.com/reference/kotlin/android/net/NetworkInfo`.*

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` object. This is supplied when there is another network that it may be possible to connect to. Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "otherNetwork"

### EXTRA_REASON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REASON: String
```

The lookup key for a string that indicates why an attempt to connect to a network failed. The string has no particular structure. It is intended to be used in notifications presented to users. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String)`.

 Value: "reason"

### MULTIPATH_PREFERENCE_HANDOVER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPATH_PREFERENCE_HANDOVER: Int
```

It is acceptable to briefly use multipath data to provide seamless connectivity for time-sensitive user-facing operations when the system default network is temporarily unresponsive. The amount of data should be limited (less than one megabyte for every call to this method), and the operation should be infrequent to ensure that data usage is limited. An example of such an operation might be a time-sensitive foreground activity, such as a voice command, that the user is performing while walking out of range of a Wi-Fi network.

 Value: 1

### MULTIPATH_PREFERENCE_PERFORMANCE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPATH_PREFERENCE_PERFORMANCE: Int
```

It is acceptable to use metered data to improve network latency and performance.

 Value: 4

### MULTIPATH_PREFERENCE_RELIABILITY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPATH_PREFERENCE_RELIABILITY: Int
```

It is acceptable to use small amounts of multipath data on an ongoing basis to provide a backup channel for traffic that is primarily going over another network. An example might be maintaining backup connections to peers or servers for the purpose of fast fallback if the default network is temporarily unresponsive or disconnects. The traffic on backup paths should be negligible compared to the traffic on the main path.

 Value: 2

### RESTRICT_BACKGROUND_STATUS_DISABLED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESTRICT_BACKGROUND_STATUS_DISABLED: Int
```

Device is not restricting metered network activity while application is running on background.

 Value: 1

### RESTRICT_BACKGROUND_STATUS_ENABLED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESTRICT_BACKGROUND_STATUS_ENABLED: Int
```

Device is restricting metered network activity while application is running on background.

In this state, application should not try to use the network while running on background, because it would be denied.

 Value: 3

### RESTRICT_BACKGROUND_STATUS_WHITELISTED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESTRICT_BACKGROUND_STATUS_WHITELISTED: Int
```

Device is restricting metered network activity while application is running on background, but application is allowed to bypass it.

In this state, application should take action to mitigate metered network access. For example, a music streaming application should switch to a low-bandwidth bitrate.

 Value: 2

### TYPE_BLUETOOTH

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BLUETOOTH: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasTransport(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request an appropriate network. See `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for supported transports.*

A Bluetooth data connection.

 Value: 7

### TYPE_DUMMY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DUMMY: Int
```

**Deprecated:** *This is not used any more.*

Fake data connection. This should not be used on shipping devices.

 Value: 8

### TYPE_ETHERNET

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ETHERNET: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasTransport(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request an appropriate network. See `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for supported transports.*

An Ethernet data connection.

 Value: 9

### TYPE_MOBILE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MOBILE: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasTransport(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request an appropriate network. See `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for supported transports.*

A Mobile data connection. Devices may support more than one.

 Value: 0

### TYPE_MOBILE_DUN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MOBILE_DUN: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasCapability(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request a network that provides the `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_DUN:kotlin.Int` capability.*

A DUN-specific Mobile data connection. This network type may use the same network interface as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE:kotlin.Int` or it may use a different one. This is sometimes by the system when setting up an upstream connection for tethering so that the carrier is aware of DUN traffic.

 Value: 4

### TYPE_MOBILE_HIPRI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MOBILE_HIPRI: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasTransport(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request an appropriate network. See `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for supported transports.*

A High Priority Mobile data connection. This network type uses the same network interface as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE:kotlin.Int` but the routing setup is different.

 Value: 5

### TYPE_MOBILE_MMS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MOBILE_MMS: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasCapability(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request a network that provides the `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_MMS:kotlin.Int` capability.*

An MMS-specific Mobile data connection. This network type may use the same network interface as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE:kotlin.Int` or it may use a different one. This is used by applications needing to talk to the carrier's Multimedia Messaging Service servers.

 Value: 2

### TYPE_MOBILE_SUPL

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MOBILE_SUPL: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasCapability(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request a network that provides the `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_SUPL:kotlin.Int` capability.*

A SUPL-specific Mobile data connection. This network type may use the same network interface as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#TYPE_MOBILE:kotlin.Int` or it may use a different one. This is used by applications needing to talk to the carrier's Secure User Plane Location servers for help locating the device.

 Value: 3

### TYPE_VPN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VPN: Int
```

**Deprecated:** *Applications should use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#TRANSPORT_VPN:kotlin.Int` instead.*

A virtual network using one or more native bearers. It may or may not be providing security services.

 Value: 17

### TYPE_WIFI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_WIFI: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasTransport(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request an appropriate network. See `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for supported transports.*

A WIFI data connection. Devices may support more than one.

 Value: 1

### TYPE_WIMAX

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_WIMAX: Int
```

**Deprecated:** *Applications should instead use `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#hasTransport(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to request an appropriate network. See `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for supported transports.*

A WiMAX data connection.

 Value: 6

## Public methods

### addDefaultNetworkActiveListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addDefaultNetworkActiveListener(l: ConnectivityManager.OnNetworkActiveListener!): Unit
```

Start listening to reports when the system's default data network is active, meaning it is a good time to perform network traffic. Use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#isDefaultNetworkActive()` to determine the current state of the system's default network after registering the listener.

If the process default network has been set with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)` this function will not reflect the process's default, but the system default.

| Parameters ||
|---|---|
| `l` | [ConnectivityManager.OnNetworkActiveListener](../android/net/ConnectivityManager.OnNetworkActiveListener.md)!: The listener to be told when the network is active. |

### bindProcessToNetwork

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindProcessToNetwork(network: Network?): Boolean
```

Binds the current process to `network`. All Sockets created in the future (and not explicitly bound via a bound SocketFactory from `https://developer.android.com/reference/kotlin/android/net/Network#getSocketFactory()`) will be bound to `network`. All host name resolutions will be limited to `network` as well. Note that if `network` ever disconnects, all Sockets created in this way will cease to work and all host name resolutions will fail. This is by design so an application doesn't accidentally use Sockets it thinks are still bound to a particular `https://developer.android.com/reference/kotlin/android/net/Network`. To clear binding pass `null` for `network`. Using individually bound Sockets created by Network.getSocketFactory().createSocket() and performing network-specific host name resolutions via `https://developer.android.com/reference/kotlin/android/net/Network#getAllByName(kotlin.String)` is preferred to calling `bindProcessToNetwork`.

| Parameters ||
|---|---|
| `network` | [Network](Network.md)?: The `https://developer.android.com/reference/kotlin/android/net/Network` to bind the current process to, or `null` to clear the current binding. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the `https://developer.android.com/reference/kotlin/android/net/Network` is no longer valid. |

### createSocketKeepalive

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createSocketKeepalive(
    network: Network, 
    socket: IpSecManager.UdpEncapsulationSocket, 
    source: InetAddress, 
    destination: InetAddress, 
    executor: Executor, 
    callback: SocketKeepalive.Callback
): SocketKeepalive
```

Request that keepalives be started on a IPsec NAT-T socket.

| Parameters ||
|---|---|
| `network` | [Network](Network.md): The `https://developer.android.com/reference/kotlin/android/net/Network` the socket is on. This value cannot be `null`. |
| `socket` | [IpSecManager.UdpEncapsulationSocket](../android/net/IpSecManager.UdpEncapsulationSocket.md): The socket that needs to be kept alive. This value cannot be `null`. |
| `source` | [InetAddress](../java.net/InetAddress.md): The source address of the `https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket`. This value cannot be `null`. |
| --- | --- |
| `destination` | [InetAddress](../java.net/InetAddress.md): The destination address of the `https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket`. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor on which callback will be invoked. The provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` must run callback sequentially, otherwise the order of callbacks cannot be guaranteed. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [SocketKeepalive.Callback](../android/net/SocketKeepalive.Callback.md): A `https://developer.android.com/reference/kotlin/android/net/SocketKeepalive.Callback`. Used for notifications about keepalive changes. Must be extended by applications that use this API. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/SocketKeepalive` | A `https://developer.android.com/reference/kotlin/android/net/SocketKeepalive` object that can be used to control the keepalive on the given socket. This value cannot be `null`. |

### getActiveNetwork

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveNetwork(): Network?
```

Returns a `https://developer.android.com/reference/kotlin/android/net/Network` object corresponding to the currently active default data network. In the event that the current active default data network disconnects, the returned `Network` object will no longer be usable. This will return `null` when there is no default network, or when the default network is blocked. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Network?` | a `https://developer.android.com/reference/kotlin/android/net/Network` object for the current default network or `null` if no default network is currently active or if the default network is blocked for the caller |

### getActiveNetworkInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveNetworkInfo(): NetworkInfo?
```

**Deprecated:** *See `https://developer.android.com/reference/kotlin/android/net/NetworkInfo`.*

Returns details about the currently active default data network. When connected, this network is the default route for outgoing connections. You should always check `https://developer.android.com/reference/kotlin/android/net/NetworkInfo#isConnected()` before initiating network traffic. This may return `null` when there is no default network. Note that if the default network is a VPN, this method will return the NetworkInfo for one of its underlying networks instead, or null if the VPN agent did not specify any. Apps interested in learning about VPNs should use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkInfo(android.net.Network)` instead. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkInfo?` | a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` object for the current default network or `null` if no default network is currently active |

### getAllNetworkInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllNetworkInfo(): Array<NetworkInfo!>
```

**Deprecated:** *This method does not support multiple connected networks of the same type. Use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getAllNetworks()` and `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkInfo(android.net.Network)` instead.*

Returns connection status information about all network types supported by the device. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/net/NetworkInfo!>` | an array of `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` objects. Check each `https://developer.android.com/reference/kotlin/android/net/NetworkInfo#getType()` for which type each applies. This value cannot be `null`. |

### getAllNetworks

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllNetworks(): Array<Network!>
```

**Deprecated:** *This method does not provide any notification of network state changes, forcing apps to call it repeatedly. This is inefficient and prone to race conditions. Apps should use methods such as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` instead. Apps that desire to obtain information about networks that do not apply to them can use `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder#setIncludeOtherUidNetworks(kotlin.Boolean)`.*

Returns an array of all `https://developer.android.com/reference/kotlin/android/net/Network` currently tracked by the framework. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/net/Network!>` | an array of `https://developer.android.com/reference/kotlin/android/net/Network` objects. This value cannot be `null`. |

### getBackgroundDataSetting

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackgroundDataSetting(): Boolean
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, availability of background data depends on several combined factors, and this method will always return `true`. Instead, when background data is unavailable, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getActiveNetworkInfo()` will now appear disconnected.*

Returns the value of the setting for background data usage. If false, applications should not use the network if the application is not in the foreground. Developers should respect this setting, and check the value of this before performing any background data operations.

All applications that have background services that use the network should listen to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#ACTION_BACKGROUND_DATA_SETTING_CHANGED:kotlin.String`.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether background data usage is allowed. |

### getBoundNetworkForProcess

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBoundNetworkForProcess(): Network?
```

Returns the `https://developer.android.com/reference/kotlin/android/net/Network` currently bound to this process via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)`, or `null` if no `https://developer.android.com/reference/kotlin/android/net/Network` is explicitly bound.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Network?` | `Network` to which this process is bound, or `null`. |

### getConnectionOwnerUid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConnectionOwnerUid(
    protocol: Int, 
    local: InetSocketAddress, 
    remote: InetSocketAddress
): Int
```

Returns the `uid` of the owner of a network connection.

| Parameters ||
|---|---|
| `protocol` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The protocol of the connection. Only `IPPROTO_TCP` and `IPPROTO_UDP` currently supported. |
| `local` | [InetSocketAddress](../java.net/InetSocketAddress.md): The local `https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#` of a connection. This value cannot be `null`. |
| `remote` | [InetSocketAddress](../java.net/InetSocketAddress.md): The remote `https://developer.android.com/reference/kotlin/java/net/InetSocketAddress.html#` of a connection. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `uid` if the connection is found and the app has permission to observe it (e.g., if it is associated with the calling VPN app's VpnService tunnel) or `https://developer.android.com/reference/kotlin/android/os/Process.html#INVALID_UID:kotlin.Int` if the connection is not found. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if an unsupported protocol is requested. |
| `java.lang.SecurityException` | if the caller is not the active VpnService for the current user. |

### getDefaultProxy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDefaultProxy(): ProxyInfo?
```

Get the current default HTTP proxy settings. If a global proxy is set it will be returned, otherwise if this process is bound to a `https://developer.android.com/reference/kotlin/android/net/Network` using `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)` then that `Network`'s proxy is returned, otherwise the default network's proxy is returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ProxyInfo?` | the `https://developer.android.com/reference/kotlin/android/net/ProxyInfo` for the current HTTP proxy, or `null` if no HTTP proxy is active. |

### getLinkProperties

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLinkProperties(network: Network?): LinkProperties?
```

Get the `https://developer.android.com/reference/kotlin/android/net/LinkProperties` for the given `https://developer.android.com/reference/kotlin/android/net/Network`. This will return `null` if the network is unknown. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `network` | [Network](Network.md)?: The `https://developer.android.com/reference/kotlin/android/net/Network` object identifying the network in question. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/LinkProperties?` | The `https://developer.android.com/reference/kotlin/android/net/LinkProperties` for the network, or `null`. |

### getMultipathPreference

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMultipathPreference(network: Network?): Int
```

Provides a hint to the calling application on whether it is desirable to use the multinetwork APIs (e.g., android.net.Network#openConnection, android.net.Network#bindSocket, etc.) for multipath data transfer on this network when it is not the system default network. Applications desiring to use multipath network protocols should call this method before each such operation. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `network` | [Network](Network.md)?: The network on which the application desires to use multipath data. If `null`, this method will return a preference that will generally apply to metered networks. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitwise OR of zero or more of the `MULTIPATH_PREFERENCE_*` constants. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#MULTIPATH_PREFERENCE_HANDOVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#MULTIPATH_PREFERENCE_RELIABILITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#MULTIPATH_PREFERENCE_PERFORMANCE:kotlin.Int` |

### getNetworkCapabilities

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkCapabilities(network: Network?): NetworkCapabilities?
```

Get the `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for the given `https://developer.android.com/reference/kotlin/android/net/Network`, or null. This will remove any location sensitive data in the returned `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`. Some `https://developer.android.com/reference/kotlin/android/net/TransportInfo` instances like `https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo` contain location sensitive information. To retrieve this location sensitive information (subject to the caller's location permissions), use a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` with the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#FLAG_INCLUDE_LOCATION_INFO:kotlin.Int` flag instead. This method returns `null` if the network is unknown or if the |network| argument is null. 
| --- | --- | --- |
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `network` | [Network](Network.md)?: The `https://developer.android.com/reference/kotlin/android/net/Network` object identifying the network in question. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities?` | The `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` for the network, or `null`. |

### getNetworkInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkInfo(network: Network?): NetworkInfo?
```

**Deprecated:** *See `https://developer.android.com/reference/kotlin/android/net/NetworkInfo`.*

Returns connection status information about a particular Network. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `network` | [Network](Network.md)?: `https://developer.android.com/reference/kotlin/android/net/Network` specifying which network in which you're interested. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkInfo?` | a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` object for the requested network or `null` if the `Network` is not valid. |

### getNetworkInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkInfo(networkType: Int): NetworkInfo?
```

**Deprecated:** *This method does not support multiple connected networks of the same type. Use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getAllNetworks()` and `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getNetworkInfo(android.net.Network)` instead.*

Returns connection status information about a particular network type. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): integer specifying which networkType in which you're interested. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkInfo?` | a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo` object for the requested network type or `null` if the type is not supported by the device. If `networkType` is TYPE_VPN and a VPN is active for the calling app, then this method will try to return one of the underlying networks for the VPN or null if the VPN agent didn't specify any. |

### getNetworkPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkPreference(): Int
```

**Deprecated:** *Functionality has been removed as it no longer makes sense, with many more than two networks - we'd need an array to express preference. Instead we use dynamic network properties of the networks to describe their precedence.*

Retrieves the current preferred network type. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an integer representing the preferred network type |

### getNetworkWatchlistConfigHash

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkWatchlistConfigHash(): ByteArray?
```

The network watchlist is a list of domains and IP addresses that are associated with potentially harmful apps. This method returns the SHA-256 of the watchlist config file currently used by the system for validation purposes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | Hash of network watchlist config file. Null if config does not exist. This value may be `null`. |

### getProcessDefaultNetwork

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getProcessDefaultNetwork(): Network?
```

**Deprecated:** *Using this function can lead to other functions throwing `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. Use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getBoundNetworkForProcess()` instead. `getBoundNetworkForProcess` is a direct replacement.*

Returns the `https://developer.android.com/reference/kotlin/android/net/Network` currently bound to this process via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)`, or `null` if no `https://developer.android.com/reference/kotlin/android/net/Network` is explicitly bound.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Network?` | `Network` to which this process is bound, or `null`. |

### getRestrictBackgroundStatus

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRestrictBackgroundStatus(): Int
```

Determines if the calling application is subject to metered network restrictions while running on background.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_DISABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_ENABLED:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_WHITELISTED:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_WHITELISTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#RESTRICT_BACKGROUND_STATUS_ENABLED:kotlin.Int` |

### isActiveNetworkMetered

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isActiveNetworkMetered(): Boolean
```

Returns if the currently active data network is metered. A network is classified as metered when the user is sensitive to heavy data usage on that connection due to monetary costs, data limitations or battery/performance issues. You should check this before doing large data transfers, and warn the user or delay the operation until another network is available. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if large transfers should be avoided, otherwise `false`. |

### isDefaultNetworkActive

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDefaultNetworkActive(): Boolean
```

Return whether the data network is currently active. An active network means that it is currently in a high power state for performing data transmission. On some types of networks, it may be expensive to move and stay in such a state, so it is more power efficient to batch network traffic together when the radio is already in this state. This method tells you whether right now is currently a good time to initiate network traffic, as the network is already active.

### isNetworkTypeValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isNetworkTypeValid(networkType: Int): Boolean
```

**Deprecated:** *All APIs accepting a network type are deprecated. There should be no need to validate a network type.*

Tests if a given integer represents a valid network type.

| Parameters ||
|---|---|
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the type is valid, else `false` |

### registerBestMatchingNetworkCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerBestMatchingNetworkCallback(
    request: NetworkRequest, 
    networkCallback: ConnectivityManager.NetworkCallback, 
    handler: Handler
): Unit
```

Registers to receive notifications about the best matching network which satisfy the given `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`. The callbacks will continue to be called until either the application exits or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)` is called.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with #registerNetworkCallback and its variants and #requestNetwork as well as `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager#registerConnectivityDiagnosticsCallback(android.net.NetworkRequest,%20java.util.concurrent.Executor,%20android.net.ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback)`. Requesting a network with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)`.

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` that the system will call as suitable networks change state. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md): `https://developer.android.com/reference/kotlin/android/os/Handler.html#` to specify the thread upon which the callback will be invoked. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |

### registerDefaultNetworkCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerDefaultNetworkCallback(networkCallback: ConnectivityManager.NetworkCallback): Unit
```

Registers to receive notifications about changes in the application's default network. This may be a physical network or a virtual network, such as a VPN that applies to the application. The callbacks will continue to be called until either the application exits or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)` is called.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with all variants of this method, of #requestNetwork as well as `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager#registerConnectivityDiagnosticsCallback(android.net.NetworkRequest,%20java.util.concurrent.Executor,%20android.net.ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback)`. Requesting a network with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` that the system will call as the application's default network changes. The callback is invoked on the default internal Handler. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |

### registerDefaultNetworkCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerDefaultNetworkCallback(
    networkCallback: ConnectivityManager.NetworkCallback, 
    handler: Handler
): Unit
```

Registers to receive notifications about changes in the application's default network. This may be a physical network or a virtual network, such as a VPN that applies to the application. The callbacks will continue to be called until either the application exits or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)` is called.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with all variants of this method, of #requestNetwork as well as `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager#registerConnectivityDiagnosticsCallback(android.net.NetworkRequest,%20java.util.concurrent.Executor,%20android.net.ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback)`. Requesting a network with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` that the system will call as the application's default network changes. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md): `https://developer.android.com/reference/kotlin/android/os/Handler.html#` to specify the thread upon which the callback will be invoked. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |

### registerNetworkCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerNetworkCallback(
    request: NetworkRequest, 
    operation: PendingIntent
): Unit
```

Registers a PendingIntent to be sent when a network is available which satisfies the given `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`. This function behaves identically to the version that takes a NetworkCallback, but instead of `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` is used. This means the request may outlive the calling application and get called back when a suitable network is found.

The operation is an Intent broadcast that goes to a broadcast receiver that you registered with android.content.Context#registerReceiver or through the \<receiver\> tag in an AndroidManifest.xml file

The operation Intent is delivered with two extras, a `https://developer.android.com/reference/kotlin/android/net/Network` typed extra called `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK:kotlin.String` and a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` typed extra called `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK_REQUEST:kotlin.String` containing the original requests parameters.

If there is already a request for this Intent registered (with the equality of two Intents defined by `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)`), then it will be removed and replaced by this one, effectively releasing the previous `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`.

The request may be released normally by calling `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.app.PendingIntent)`.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with all variants of this method, of #requestNetwork as well as `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager#registerConnectivityDiagnosticsCallback(android.net.NetworkRequest,%20java.util.concurrent.Executor,%20android.net.ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback)`. Requesting a network with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.app.PendingIntent)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#releaseNetworkRequest(android.app.PendingIntent)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `operation` | [PendingIntent](../android.app/PendingIntent.md): Action to perform when the network is available (corresponds to the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onAvailable(android.net.Network)` call. Typically comes from `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`. Cannot be null. |

| Exceptions ||
|---|---|
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |

### registerNetworkCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerNetworkCallback(
    request: NetworkRequest, 
    networkCallback: ConnectivityManager.NetworkCallback
): Unit
```

Registers to receive notifications about all networks which satisfy the given `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`. The callbacks will continue to be called until either the application exits or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)` is called.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with all variants of this method, of #requestNetwork as well as `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager#registerConnectivityDiagnosticsCallback(android.net.NetworkRequest,%20java.util.concurrent.Executor,%20android.net.ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback)`. Requesting a network with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` that the system will call as suitable networks change state. The callback is invoked on the default internal Handler. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |

### registerNetworkCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerNetworkCallback(
    request: NetworkRequest, 
    networkCallback: ConnectivityManager.NetworkCallback, 
    handler: Handler
): Unit
```

Registers to receive notifications about all networks which satisfy the given `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`. The callbacks will continue to be called until either the application exits or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)` is called.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with all variants of this method, of #requestNetwork as well as `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager#registerConnectivityDiagnosticsCallback(android.net.NetworkRequest,%20java.util.concurrent.Executor,%20android.net.ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback)`. Requesting a network with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` that the system will call as suitable networks change state. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md): `https://developer.android.com/reference/kotlin/android/os/Handler.html#` to specify the thread upon which the callback will be invoked. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |

### releaseNetworkRequest

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun releaseNetworkRequest(operation: PendingIntent): Unit
```

Removes a request made via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.app.PendingIntent)`

This method has the same behavior as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.app.PendingIntent)` with respect to releasing network resources and disconnecting.

| Parameters ||
|---|---|
| `operation` | [PendingIntent](../android.app/PendingIntent.md): A PendingIntent equal (as defined by `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)`) to the PendingIntent passed to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.app.PendingIntent)` with the corresponding NetworkRequest you'd like to remove. Cannot be null. |

### removeDefaultNetworkActiveListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeDefaultNetworkActiveListener(l: ConnectivityManager.OnNetworkActiveListener): Unit
```

Remove network active listener previously registered with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#addDefaultNetworkActiveListener(android.net.ConnectivityManager.OnNetworkActiveListener)`.

| Parameters ||
|---|---|
| `l` | [ConnectivityManager.OnNetworkActiveListener](../android/net/ConnectivityManager.OnNetworkActiveListener.md): Previously registered listener. This value cannot be `null`. |

### reportBadNetwork

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reportBadNetwork(network: Network?): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#reportNetworkConnectivity(android.net.Network,%20kotlin.Boolean)` which allows reporting both working and non-working connectivity.*

Report a problem network to the framework. This provides a hint to the system that there might be connectivity problems on this network and may cause the framework to re-evaluate network connectivity and/or switch to another network.

| Parameters ||
|---|---|
| `network` | [Network](Network.md)?: The `https://developer.android.com/reference/kotlin/android/net/Network` the application was attempting to use or `null` to indicate the current default network. |

### reportNetworkConnectivity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reportNetworkConnectivity(
    network: Network?, 
    hasConnectivity: Boolean
): Unit
```

Report to the framework whether a network has working connectivity. This provides a hint to the system that a particular network is providing working connectivity or not. In response the framework may re-evaluate the network's connectivity and might take further action thereafter.

| Parameters ||
|---|---|
| `network` | [Network](Network.md)?: The `https://developer.android.com/reference/kotlin/android/net/Network` the application was attempting to use or `null` to indicate the current default network. |
| `hasConnectivity` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the application was able to successfully access the Internet using `network` or `false` if not. |

### requestBandwidthUpdate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestBandwidthUpdate(network: Network): Boolean
```

Requests bandwidth update for a given `https://developer.android.com/reference/kotlin/android/net/Network` and returns whether the update request is accepted by ConnectivityService. Once accepted, ConnectivityService will poll underlying network connection for updated bandwidth information. The caller will be notified via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` if there is an update. Notice that this method assumes that the caller has previously called `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` to listen for network changes.

| Parameters ||
|---|---|
| `network` | [Network](Network.md): `https://developer.android.com/reference/kotlin/android/net/Network` specifying which network you're interested. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the `https://developer.android.com/reference/kotlin/android/net/Network` is no longer valid. |

### requestNetwork

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestNetwork(
    request: NetworkRequest, 
    operation: PendingIntent
): Unit
```

Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`. This function behaves identically to the version that takes a NetworkCallback, but instead of `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` is used. This means the request may outlive the calling application and get called back when a suitable network is found.

The operation is an Intent broadcast that goes to a broadcast receiver that you registered with android.content.Context#registerReceiver or through the \<receiver\> tag in an AndroidManifest.xml file

The operation Intent is delivered with two extras, a `https://developer.android.com/reference/kotlin/android/net/Network` typed extra called `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK:kotlin.String` and a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` typed extra called `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#EXTRA_NETWORK_REQUEST:kotlin.String` containing the original requests parameters. It is important to create a new, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` based request before completing the processing of the Intent to reserve the network or it will be released shortly after the Intent is processed.

If there is already a request for this Intent registered (with the equality of two Intents defined by `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)`), then it will be removed and replaced by this one, effectively releasing the previous `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`.

The request may be released normally by calling `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#releaseNetworkRequest(android.app.PendingIntent)`.

It is presently unsupported to request a network with either `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_CAPTIVE_PORTAL:kotlin.Int` as these `NetworkCapabilities` represent states that a particular network may never attain, and whether a network will attain these states is unknown prior to bringing up the network so the framework does not know how to go about satisfying a request with these capabilities.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with all variants of this method, of #registerNetworkCallback as well as `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager#registerConnectivityDiagnosticsCallback(android.net.NetworkRequest,%20java.util.concurrent.Executor,%20android.net.ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback)`. Requesting a network with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.app.PendingIntent)` or `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#releaseNetworkRequest(android.app.PendingIntent)`.

This method requires the caller to hold either the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_NETWORK_STATE:kotlin.String` permission or the ability to modify system settings as determined by `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#canWrite(android.content.Context)`.

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `operation` | [PendingIntent](../android.app/PendingIntent.md): Action to perform when the network is available (corresponds to the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onAvailable(android.net.Network)` call. Typically comes from `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getBroadcast(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int)`. Cannot be null. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `request` contains invalid network capabilities. |
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |
| `java.lang.SecurityException` | if missing the appropriate permissions. |
| --- | --- |

### requestNetwork

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestNetwork(
    request: NetworkRequest, 
    networkCallback: ConnectivityManager.NetworkCallback
): Unit
```

Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`.

This method will attempt to find the best network that matches the passed `https://developer.android.com/reference/kotlin/android/net/NetworkRequest`, and to bring up one that does if none currently satisfies the criteria. The platform will evaluate which network is the best at its own discretion. Throughput, latency, cost per byte, policy, user preference and other considerations may be factored in the decision of what is considered the best network.

As long as this request is outstanding, the platform will try to maintain the best network matching this request, while always attempting to match the request to a better network if possible. If a better match is found, the platform will switch this request to the now-best network and inform the app of the newly best network by invoking `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onAvailable(android.net.Network)` on the provided callback. Note that the platform will not try to maintain any other network than the best one currently matching the request: a network not matching any network request may be disconnected at any time.

For example, an application could use this method to obtain a connected cellular network even if the device currently has a data connection over Ethernet. This may cause the cellular radio to consume additional power. Or, an application could inform the system that it wants a network supporting sending MMSes and have the system let it know about the currently best MMS-supporting network through the provided `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback`.

The status of the request can be followed by listening to the various callbacks described in `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback`. The `https://developer.android.com/reference/kotlin/android/net/Network` object passed to the callback methods can be used to direct traffic to the network (although accessing some networks may be subject to holding specific permissions). Callers will learn about the specific characteristics of the network through `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onCapabilitiesChanged(android.net.Network,%20android.net.NetworkCapabilities)` and `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onLinkPropertiesChanged(android.net.Network,%20android.net.LinkProperties)`. The methods of the provided `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` will only be invoked due to changes in the best network matching the request at any given time; therefore when a better network matching the request becomes available, the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onAvailable(android.net.Network)` method is called with the new network after which no further updates are given about the previously-best network, unless it becomes the best again at some later time. All callbacks are invoked in order on the same thread, which by default is a thread created by the framework running in the app. See `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback,%20android.os.Handler)` to change where the callbacks are invoked.

This`https://developer.android.com/reference/kotlin/android/net/NetworkRequest` will live until released via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)` or the calling application exits, at which point the system may let go of the network at any time.

A version of this method which takes a timeout is `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback,%20kotlin.Int)`, that an app can use to only wait for a limited amount of time for the network to become unavailable.

It is presently unsupported to request a network with mutable `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` such as `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_CAPTIVE_PORTAL:kotlin.Int` as these `NetworkCapabilities` represent states that a particular network may never attain, and whether a network will attain these states is unknown prior to bringing up the network so the framework does not know how to go about satisfying a request with these capabilities.

This method requires the caller to hold either the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_NETWORK_STATE:kotlin.String` permission or the ability to modify system settings as determined by `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#canWrite(android.content.Context)`.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with all variants of this method, of #registerNetworkCallback as well as `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager#registerConnectivityDiagnosticsCallback(android.net.NetworkRequest,%20java.util.concurrent.Executor,%20android.net.ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback)`. Requesting a network with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)`.

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` to be utilized for this request. Note the callback must not be shared - it uniquely specifies this request. The callback is invoked on the default internal Handler. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `request` contains invalid network capabilities. |
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |
| `java.lang.SecurityException` | if missing the appropriate permissions. |
| --- | --- |

### requestNetwork

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestNetwork(
    request: NetworkRequest, 
    networkCallback: ConnectivityManager.NetworkCallback, 
    handler: Handler
): Unit
```

Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`. This method behaves identically to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` but runs all the callbacks on the passed Handler.

This method has the same permission requirements as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)`, is subject to the same limitations, and throws the same exceptions in the same conditions.

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` to be utilized for this request. Note the callback must not be shared - it uniquely specifies this request. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md): `https://developer.android.com/reference/kotlin/android/os/Handler.html#` to specify the thread upon which the callback will be invoked. This value cannot be `null`. |
| --- | --- |

### requestNetwork

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestNetwork(
    request: NetworkRequest, 
    networkCallback: ConnectivityManager.NetworkCallback, 
    handler: Handler, 
    timeoutMs: Int
): Unit
```

Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`, limited by a timeout. This method behaves identically to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback,%20kotlin.Int)` but runs all the callbacks on the passed Handler.

This method has the same permission requirements as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)`, is subject to the same limitations, and throws the same exceptions in the same conditions.

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` to be utilized for this request. Note the callback must not be shared - it uniquely specifies this request. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md): `https://developer.android.com/reference/kotlin/android/os/Handler.html#` to specify the thread upon which the callback will be invoked. This value cannot be `null`. |
| --- | --- |
| `timeoutMs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The time in milliseconds to attempt looking for a suitable network before `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onUnavailable()` is called. |

### requestNetwork

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestNetwork(
    request: NetworkRequest, 
    networkCallback: ConnectivityManager.NetworkCallback, 
    timeoutMs: Int
): Unit
```

Request a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`, limited by a timeout. This function behaves identically to the non-timed-out version `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)`, but if a suitable network is not found within the given time (in milliseconds) the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onUnavailable()` callback is called. The request can still be released normally by calling `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#unregisterNetworkCallback(android.net.ConnectivityManager.NetworkCallback)` but does not have to be released if timed-out (it is automatically released). Unregistering a request that timed out is not an error.

Do not use this method to poll for the existence of specific networks (e.g. with a small timeout) - `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` is provided for that purpose. Calling this method will attempt to bring up the requested network.

This method has the same permission requirements as `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)`, is subject to the same limitations, and throws the same exceptions in the same conditions.

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` to be utilized for this request. Note the callback must not be shared - it uniquely specifies this request. This value cannot be `null`. |
| `timeoutMs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The time in milliseconds to attempt looking for a suitable network before `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onUnavailable()` is called. The timeout must be a positive value (i.e. \>0). |
| --- | --- |

### reserveNetwork

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 17](https://developer.android.com/sdkExtensions)

```
open fun reserveNetwork(
    request: NetworkRequest, 
    handler: Handler, 
    networkCallback: ConnectivityManager.NetworkCallback
): Unit
```

Reserve a network to satisfy a set of `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities`. Some types of networks require the system to generate (i.e. reserve) some set of information before a network can be connected. For such networks, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#reserveNetwork(android.net.NetworkRequest,%20android.os.Handler,%20android.net.ConnectivityManager.NetworkCallback)` can be used which may lead to a call to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onReserved(android.net.NetworkCapabilities)` containing the `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities` that were reserved. A reservation reserves at most one network. If the network connects, a reservation request behaves similar to a request filed using #requestNetwork. The provided `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` will only be called for the reserved network. If the system determines that the requested reservation can never be fulfilled, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback#onUnavailable()` is called, the reservation is released by the system, and the provided callback can be reused. Otherwise, the reservation remains in place until the requested network connects. There is no guarantee that the reserved network will ever connect.

| Parameters ||
|---|---|
| `request` | [NetworkRequest](NetworkRequest.md): `https://developer.android.com/reference/kotlin/android/net/NetworkRequest` describing this request. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md): `https://developer.android.com/reference/kotlin/android/os/Handler.html#` to specify the thread upon which the callback will be invoked. This value cannot be `null`. |
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` to be utilized for this request. Note the callback must not be shared - it uniquely specifies this request. This value cannot be `null`. |
| --- | --- |

### setNetworkPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNetworkPreference(preference: Int): Unit
```

**Deprecated:** *Functionality has been removed as it no longer makes sense, with many more than two networks - we'd need an array to express preference. Instead we use dynamic network properties of the networks to describe their precedence.*

Specifies the preferred network type. When the device has more than one type available the preferred network type will be used.

| Parameters ||
|---|---|
| `preference` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the network type to prefer over all others. It is unspecified what happens to the old preferred network in the overall ordering. |

### setProcessDefaultNetwork

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setProcessDefaultNetwork(network: Network?): Boolean
```

**Deprecated:** *This function can throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. Use `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)` instead. `bindProcessToNetwork` is a direct replacement.*

Binds the current process to `network`. All Sockets created in the future (and not explicitly bound via a bound SocketFactory from `https://developer.android.com/reference/kotlin/android/net/Network#getSocketFactory()`) will be bound to `network`. All host name resolutions will be limited to `network` as well. Note that if `network` ever disconnects, all Sockets created in this way will cease to work and all host name resolutions will fail. This is by design so an application doesn't accidentally use Sockets it thinks are still bound to a particular `https://developer.android.com/reference/kotlin/android/net/Network`. To clear binding pass `null` for `network`. Using individually bound Sockets created by Network.getSocketFactory().createSocket() and performing network-specific host name resolutions via `https://developer.android.com/reference/kotlin/android/net/Network#getAllByName(kotlin.String)` is preferred to calling `setProcessDefaultNetwork`.

| Parameters ||
|---|---|
| `network` | [Network](Network.md)?: The `https://developer.android.com/reference/kotlin/android/net/Network` to bind the current process to, or `null` to clear the current binding. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success, `false` if the `https://developer.android.com/reference/kotlin/android/net/Network` is no longer valid. |

### unregisterNetworkCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterNetworkCallback(operation: PendingIntent): Unit
```

Unregisters a callback previously registered via `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.app.PendingIntent)`.

| Parameters ||
|---|---|
| `operation` | [PendingIntent](../android.app/PendingIntent.md): A PendingIntent equal (as defined by `https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent)`) to the PendingIntent passed to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.app.PendingIntent)`. Cannot be null. |

### unregisterNetworkCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterNetworkCallback(networkCallback: ConnectivityManager.NetworkCallback): Unit
```

Unregisters a `NetworkCallback` and possibly releases networks originating from `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` and `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#registerNetworkCallback(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` calls. If the given `NetworkCallback` had previously been used with `requestNetwork`, any networks that the device brought up only to satisfy that request will be disconnected. Notifications that would have triggered that `NetworkCallback` will immediately stop triggering it as soon as this call returns.

| Parameters ||
|---|---|
| `networkCallback` | [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback` used when making the request. This value cannot be `null`. |
