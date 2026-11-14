Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pManager

```
open class WifiP2pManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.WifiP2pManager](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#) |

This class provides the API for managing Wi-Fi peer-to-peer connectivity. This lets an application discover available peers, setup connection to peers and query for the list of peers. When a p2p connection is formed over wifi, the device continues to maintain the uplink connection over mobile or any other available network for internet connectivity on the device.

The API is asynchronous and responses to requests from an application are on listener callbacks provided by the application. The application needs to do an initialization with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` before doing any p2p operation.

Most application calls need a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener` instance for receiving callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. Action callbacks indicate whether the initiation of the action was a success or a failure. Upon failure, the reason of failure can be one of `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ERROR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#P2P_UNSUPPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#BUSY:kotlin.Int`.

An application can initiate discovery of peers with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. An initiated discovery request from an application stays active until the device starts connecting to a peer ,forms a p2p group or there is an explicit `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#stopPeerDiscovery(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. Applications can listen to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_CHANGED_ACTION:kotlin.String` to know if a peer-to-peer discovery is running or stopped. Additionally, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` indicates if the peer list has changed.

When an application needs to fetch the current list of peers, it can request the list of peers with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.PeerListListener)`. When the peer list is available `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.PeerListListener#onPeersAvailable(android.net.wifi.p2p.WifiP2pDeviceList)` is called with the device list.

An application can initiate a connection request to a peer through `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#connect(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. See `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig` for details on setting up the configuration. For communication with legacy Wi-Fi devices that do not support p2p, an app can create a group using #createGroup which creates an access point whose details can be fetched with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestGroupInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.GroupInfoListener)`.

After a successful group formation through #createGroup or through `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#connect(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`, use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestConnectionInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ConnectionInfoListener)` to fetch the connection details. The connection info `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo` contains the address of the group owner `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo#groupOwnerAddress:java.net.InetAddress` and a flag `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo#isGroupOwner:kotlin.Boolean` to indicate if the current device is a p2p group owner. A p2p client can thus communicate with the p2p group owner through a socket connection. If the current device is the p2p group owner, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo#groupOwnerAddress:java.net.InetAddress` is anonymized unless the caller holds the `android.Manifest.permission#LOCAL_MAC_ADDRESS` permission.

With peer discovery using `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`, an application discovers the neighboring peers, but has no good way to figure out which peer to establish a connection with. For example, if a game application is interested in finding all the neighboring peers that are also running the same game, it has no way to find out until after the connection is setup. Pre-association service discovery is meant to address this issue of filtering the peers based on the running services.

With pre-association service discovery, an application can advertise a service for a application on a peer device prior to a connection setup between the devices. Currently, DNS based service discovery (Bonjour) and Upnp are the higher layer protocols supported. Get Bonjour resources at dns-sd.org and Upnp resources at upnp.org As an example, a video application can discover a Upnp capable media renderer prior to setting up a Wi-fi p2p connection with the device.

An application can advertise a Upnp or a Bonjour service with a call to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addLocalService(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. After a local service is added, the framework automatically responds to a peer application discovering the service prior to establishing a p2p connection. A call to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeLocalService(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` removes a local service and `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#clearLocalServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` can be used to clear all local services.

An application that is looking for peer devices that support certain services can do so with a call to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. Prior to initiating the discovery, application can add service discovery request with a call to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`, remove a service discovery request with a call to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` or clear all requests with a call to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#clearServiceRequests(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. When no service requests remain, a previously running service discovery will stop. The application is notified of a result of service discovery request through listener callbacks set through `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setDnsSdResponseListeners(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DnsSdServiceResponseListener,%20android.net.wifi.p2p.WifiP2pManager.DnsSdTxtRecordListener)` for Bonjour or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setUpnpServiceResponseListener(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.UpnpServiceResponseListener)` for Upnp.

**Note:** Registering an application handler with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` requires the permissions `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CHANGE_WIFI_STATE:kotlin.String` to perform any further peer-to-peer operations. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener` Interface for callback invocation on an application action |
| open | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel` A channel that connects the application to the Wifi p2p framework. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ChannelListener` Interface for callback invocation when framework channel is lost |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener` Interface for callback invocation when connection info is available |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener` Interface for callback invocation when `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)`. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener` Interface for callback invocation when p2p state is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDiscoveryState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DiscoveryStateListener)`. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DnsSdServiceResponseListener` Interface for callback invocation when Bonjour service discovery response is received |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DnsSdTxtRecordListener` Interface for callback invocation when Bonjour TXT record is available for a service |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener` Interface for callback invocation when an incoming request is received. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.GroupInfoListener` Interface for callback invocation when group info is available |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener` Interface for callback invocation when `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestNetworkInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.NetworkInfoListener)`. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.P2pStateListener` Interface for callback invocation when p2p state is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestP2pState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.P2pStateListener)`. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.PeerListListener` Interface for callback invocation when peer list is available |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener` Interface for callback invocation when service discovery response other than Upnp or Bonjour is received |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.UpnpServiceResponseListener` Interface for callback invocation when upnp service discovery response is received |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener` Interface used to listen to Wi-Fi p2p various changes such as device state change, discovery started/stopped, connection change, etc. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ACTION_WIFI_P2P_LISTEN_STATE_CHANGED:kotlin.String` Broadcast intent action indicating that peer listen has either started or stopped. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ACTION_WIFI_P2P_REQUEST_RESPONSE_CHANGED:kotlin.String` Broadcast intent action indicating whether or not current connecting request is accepted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#BUSY:kotlin.Int` Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_ACCEPT:kotlin.Int` Accept the incoming request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_SHOW_PASSWORD_TO_SERVICE:kotlin.Int` Defer the Wi-Fi Direct R2 pairing bootstrapping password display to the Wi-Fi service (which will display a dialog to the user). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_SHOW_PIN_TO_SERVICE:kotlin.Int` Defer the WPS PIN or Wi-Fi Direct R2 pairing bootstrapping PIN display to the Wi-Fi service (which will display a dialog to the user). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_TO_SERVICE:kotlin.Int` Defer the decision back to the Wi-Fi service (which will display a dialog to the user). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_REJECT:kotlin.Int` Reject the incoming request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ERROR:kotlin.Int` Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_DISCOVERY_STATE:kotlin.String` The lookup key for an int that indicates whether p2p discovery has started or stopped. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_LISTEN_STATE:kotlin.String` The lookup key for an int that indicates whether p2p listen has started or stopped. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_NETWORK_INFO:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` object associated with the p2p network. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_P2P_DEVICE_LIST:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDeviceList` object representing the new peer list when `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` broadcast is sent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_REQUEST_CONFIG:kotlin.String` The lookup key for the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig` object of a request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_REQUEST_RESPONSE:kotlin.String` The lookup key for the result of a request, true if accepted, false otherwise. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_DEVICE:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` object Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_GROUP:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup` object associated with the p2p network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_INFO:kotlin.String` The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo` object Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_STATE:kotlin.String` The lookup key for an int that indicates whether Wi-Fi p2p is enabled or disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_CONNECTION_CANCELLED:kotlin.Int` P2p group creation failed because the connection has been cancelled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_GROUP_REMOVED:kotlin.Int` P2p group creation failed because the group has been removed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_INVITATION_FAILED:kotlin.Int` P2p group creation failed because invitation has failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_PROVISION_DISCOVERY_FAILED:kotlin.Int` P2p group creation failed because provision discovery has failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_TIMED_OUT:kotlin.Int` P2p group creation failed because it has timed out. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_USER_REJECTED:kotlin.Int` P2p group creation failed because user has rejected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#NO_PERMISSION:kotlin.Int` Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#NO_SERVICE_REQUESTS:kotlin.Int` Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#P2P_UNSUPPORTED:kotlin.Int` Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_CONNECTION_CHANGED_ACTION:kotlin.String` Broadcast intent action indicating that the state of Wi-Fi p2p connectivity has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_CHANGED_ACTION:kotlin.String` Broadcast intent action indicating that peer discovery has either started or stopped. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED:kotlin.Int` p2p discovery has started |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED:kotlin.Int` p2p discovery has stopped |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STARTED:kotlin.Int` p2p listen has started |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STOPPED:kotlin.Int` p2p listen has stopped |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` Broadcast intent action indicating that the available peer list has changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_SCAN_FULL:kotlin.Int` Run P2P scan on all channels. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_SCAN_SINGLE_FREQ:kotlin.Int` Run P2P scan only on a specific channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_SCAN_SOCIAL:kotlin.Int` Run P2P scan only on social channels. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_CHANGED_ACTION:kotlin.String` Broadcast intent action to indicate whether Wi-Fi p2p is enabled or disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_DISABLED:kotlin.Int` Wi-Fi p2p is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int` Wi-Fi p2p is enabled. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_THIS_DEVICE_CHANGED_ACTION:kotlin.String` Broadcast intent action indicating that this device details have changed. |
| --- | --- |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, deviceAddress: https://developer.android.com/reference/kotlin/android/net/MacAddress.html#, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener)` Set the external approver for a specific peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addLocalService(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, servInfo: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Register a local service for service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, req: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Add a service discovery request. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#cancelConnect(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Cancel any ongoing p2p group negotiation |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#clearLocalServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Clear all registered local services of service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#clearServiceRequests(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Clear all registered service discovery requests. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#connect(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, config: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Start a p2p connection to a device with the specified configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#createGroup(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, config: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig?, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Create a p2p group with the current device as the group owner. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#createGroup(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Create a p2p group with the current device as the group owner. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Initiate peer discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeersOnSocialChannels(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Scan only the social channels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeersOnSpecificFrequency(android.net.wifi.p2p.WifiP2pManager.Channel,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, frequencyMhz: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Scan only a single channel specified by frequency. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Initiate service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverUsdBasedServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pUsdBasedServiceDiscoveryConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, config: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedServiceDiscoveryConfig, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Initiate Un-synchronized service discovery (USD) based service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#getListenState(android.net.wifi.p2p.WifiP2pManager.Channel,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, resultsCallback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>)` Get p2p listen state. |
| --- | --- |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#getP2pMaxAllowedVendorElementsLengthBytes()()` Return the maximum total length (in bytes) of all Vendor specific information elements (VSIEs) which can be set using the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setVendorElements(android.net.wifi.p2p.WifiP2pManager.Channel,%20kotlin.collections.MutableList,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. |
| open [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)! | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)(srcContext: https://developer.android.com/reference/kotlin/android/content/Context.html#!, srcLooper: https://developer.android.com/reference/kotlin/android/os/Looper.html#!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ChannelListener!)` Registers the application with the Wi-Fi framework. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isChannelConstrainedDiscoverySupported()()` Check if this device supports discovery limited to a specific frequency or the social channels. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isGroupClientRemovalSupported()()` Check if this device supports removing clients from a group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isGroupOwnerIPv6LinkLocalAddressProvided()()` Checks whether this device, while being a group client, can discover and deliver the group owner's IPv6 link-local address. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isPccModeSupported()()` Check if this device supports P2P Connection Compatibility Mode(R1/R2 compatibility mode). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isSetVendorElementsSupported()()` Check if this device supports setting vendor elements. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()()` Check if this device supports Wi-Fi Direct R2 (P2P2). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#registerWifiP2pListener(java.util.concurrent.Executor,%20android.net.wifi.p2p.WifiP2pManager.WifiP2pListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener)` Add a listener to listen to Wi-Fi p2p various changes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeClient(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, peerAddress: https://developer.android.com/reference/kotlin/android/net/MacAddress.html#, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Remove the client with the MAC address from the group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, deviceAddress: https://developer.android.com/reference/kotlin/android/net/MacAddress.html#, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Remove the external approver for a specific peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeGroup(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Remove the current p2p group. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeLocalService(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, servInfo: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Remove a registered local service added with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addLocalService(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, req: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Remove a specified service discovery request added with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestConnectionInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ConnectionInfoListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener!)` Request device connection info. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener)` Request Device Info |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDirInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Get the Device Identity Resolution (DIR) Information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDiscoveryState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DiscoveryStateListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener)` Request p2p discovery state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestGroupInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.GroupInfoListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.GroupInfoListener!)` Request p2p group info. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestNetworkInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.NetworkInfoListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener)` Request network info. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestP2pState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.P2pStateListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.P2pStateListener)` Request p2p enabled state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.PeerListListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.PeerListListener!)` Request the current list of peers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, deviceAddress: https://developer.android.com/reference/kotlin/android/net/MacAddress.html#, result: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Set the result for the incoming request from a specific peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20kotlin.String,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, deviceAddress: https://developer.android.com/reference/kotlin/android/net/MacAddress.html#, result: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, pinOrPassword: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Set the result with PIN for the incoming request from a specific peer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setDnsSdResponseListeners(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DnsSdServiceResponseListener,%20android.net.wifi.p2p.WifiP2pManager.DnsSdTxtRecordListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, servListener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DnsSdServiceResponseListener!, txtListener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DnsSdTxtRecordListener!)` Register a callback to be invoked on receiving Bonjour service discovery response. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setServiceResponseListener(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ServiceResponseListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener!)` Register a callback to be invoked on receiving service discovery response. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setUpnpServiceResponseListener(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.UpnpServiceResponseListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.UpnpServiceResponseListener!)` Register a callback to be invoked on receiving upnp service discovery response. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setVendorElements(android.net.wifi.p2p.WifiP2pManager.Channel,%20kotlin.collections.MutableList,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, vendorElements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.InformationElement.html#!>, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Set/Clear vendor specific information elements (VSIEs) to be published during Wi-Fi Direct (P2P) discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setWfdInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pWfdInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, wfdInfo: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Set Wifi Display information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#startListening(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Force p2p to enter listen state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#startPeerDiscovery(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pDiscoveryConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, config: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDiscoveryConfig, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Initiate peer discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#startUsdBasedLocalServiceAdvertisement(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pUsdBasedLocalServiceAdvertisementConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, servInfo: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo, config: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedLocalServiceAdvertisementConfig, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Start a service discovery advertisement using Un-synchronized service discovery (USD). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#stopListening(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener?)` Force p2p to exit listen state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#stopPeerDiscovery(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)(channel: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!, listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener!)` Stop an ongoing peer discovery |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#unregisterWifiP2pListener(android.net.wifi.p2p.WifiP2pManager.WifiP2pListener)(listener: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener)` Remove a listener added using `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#registerWifiP2pListener(java.util.concurrent.Executor,%20android.net.wifi.p2p.WifiP2pManager.WifiP2pListener)` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#validateDirInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pDirInfo,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(c: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel, dirInfo: https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Validate the Device Identity Resolution (DIR) Information of a P2P device. |
| --- | --- |

## Constants

### ACTION_WIFI_P2P_LISTEN_STATE_CHANGED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WIFI_P2P_LISTEN_STATE_CHANGED: String
```

Broadcast intent action indicating that peer listen has either started or stopped. One extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_LISTEN_STATE:kotlin.String` indicates whether listen has started or stopped.

 Value: "android.net.wifi.p2p.action.WIFI_P2P_LISTEN_STATE_CHANGED"

### ACTION_WIFI_P2P_REQUEST_RESPONSE_CHANGED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_WIFI_P2P_REQUEST_RESPONSE_CHANGED: String
```

Broadcast intent action indicating whether or not current connecting request is accepted. The connecting request is initiated by `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#connect(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

The `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_REQUEST_RESPONSE:kotlin.String` extra indicates whether or not current request is accepted or rejected.

The `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_REQUEST_CONFIG:kotlin.String` extra indicates the responsed configuration.

 Value: "android.net.wifi.p2p.action.WIFI_P2P_REQUEST_RESPONSE_CHANGED"

### BUSY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUSY: Int
```

Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. Indicates that the operation failed because the framework is busy and unable to service the request

 Value: 2

### CONNECTION_REQUEST_ACCEPT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_REQUEST_ACCEPT: Int
```

Accept the incoming request. Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

 Value: 0

### CONNECTION_REQUEST_DEFER_SHOW_PASSWORD_TO_SERVICE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_REQUEST_DEFER_SHOW_PASSWORD_TO_SERVICE: Int
```

Defer the Wi-Fi Direct R2 pairing bootstrapping password display to the Wi-Fi service (which will display a dialog to the user). Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

 Value: 4

### CONNECTION_REQUEST_DEFER_SHOW_PIN_TO_SERVICE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_REQUEST_DEFER_SHOW_PIN_TO_SERVICE: Int
```

Defer the WPS PIN or Wi-Fi Direct R2 pairing bootstrapping PIN display to the Wi-Fi service (which will display a dialog to the user). Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

 Value: 3

### CONNECTION_REQUEST_DEFER_TO_SERVICE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_REQUEST_DEFER_TO_SERVICE: Int
```

Defer the decision back to the Wi-Fi service (which will display a dialog to the user). Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

 Value: 2

### CONNECTION_REQUEST_REJECT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_REQUEST_REJECT: Int
```

Reject the incoming request. Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

 Value: 1

### ERROR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR: Int
```

Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. Indicates that the operation failed due to an internal error.

 Value: 0

### EXTRA_DISCOVERY_STATE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DISCOVERY_STATE: String
```

The lookup key for an int that indicates whether p2p discovery has started or stopped. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)`.

 Value: "discoveryState"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED:kotlin.Int`

### EXTRA_LISTEN_STATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LISTEN_STATE: String
```

The lookup key for an int that indicates whether p2p listen has started or stopped. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)`.

 Value: "android.net.wifi.p2p.extra.LISTEN_STATE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STARTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STOPPED:kotlin.Int`

### EXTRA_NETWORK_INFO

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NETWORK_INFO: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` object associated with the p2p network. Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "networkInfo"

### EXTRA_P2P_DEVICE_LIST

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_P2P_DEVICE_LIST: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDeviceList` object representing the new peer list when `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` broadcast is sent.

Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "wifiP2pDeviceList"

### EXTRA_REQUEST_CONFIG

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REQUEST_CONFIG: String
```

The lookup key for the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig` object of a request.

 Value: "android.net.wifi.p2p.extra.REQUEST_CONFIG"

### EXTRA_REQUEST_RESPONSE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REQUEST_RESPONSE: String
```

The lookup key for the result of a request, true if accepted, false otherwise.

 Value: "android.net.wifi.p2p.extra.REQUEST_RESPONSE"

### EXTRA_WIFI_P2P_DEVICE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIFI_P2P_DEVICE: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` object Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "wifiP2pDevice"

### EXTRA_WIFI_P2P_GROUP

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIFI_P2P_GROUP: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup` object associated with the p2p network. Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "p2pGroupInfo"

### EXTRA_WIFI_P2P_INFO

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIFI_P2P_INFO: String
```

The lookup key for a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo` object Retrieve with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String)`.

 Value: "wifiP2pInfo"

### EXTRA_WIFI_STATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIFI_STATE: String
```

The lookup key for an int that indicates whether Wi-Fi p2p is enabled or disabled. Retrieve it with `https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int)`.

 Value: "wifi_p2p_state"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int`

### GROUP_CREATION_FAILURE_REASON_CONNECTION_CANCELLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_CREATION_FAILURE_REASON_CONNECTION_CANCELLED: Int
```

P2p group creation failed because the connection has been cancelled. Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreationFailed(kotlin.Int)`.

 Value: 0

### GROUP_CREATION_FAILURE_REASON_GROUP_REMOVED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_CREATION_FAILURE_REASON_GROUP_REMOVED: Int
```

P2p group creation failed because the group has been removed. Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreationFailed(kotlin.Int)`.

 Value: 4

### GROUP_CREATION_FAILURE_REASON_INVITATION_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_CREATION_FAILURE_REASON_INVITATION_FAILED: Int
```

P2p group creation failed because invitation has failed. Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreationFailed(kotlin.Int)`.

 Value: 5

### GROUP_CREATION_FAILURE_REASON_PROVISION_DISCOVERY_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_CREATION_FAILURE_REASON_PROVISION_DISCOVERY_FAILED: Int
```

P2p group creation failed because provision discovery has failed. Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreationFailed(kotlin.Int)`.

 Value: 3

### GROUP_CREATION_FAILURE_REASON_TIMED_OUT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_CREATION_FAILURE_REASON_TIMED_OUT: Int
```

P2p group creation failed because it has timed out. Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreationFailed(kotlin.Int)`.

 Value: 1

### GROUP_CREATION_FAILURE_REASON_USER_REJECTED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_CREATION_FAILURE_REASON_USER_REJECTED: Int
```

P2p group creation failed because user has rejected. Used in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreationFailed(kotlin.Int)`.

 Value: 2

### NO_PERMISSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_PERMISSION: Int
```

Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. Indicates that the operation failed due to calling app doesn't have permission to call the API.

 Value: 4

### NO_SERVICE_REQUESTS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_SERVICE_REQUESTS: Int
```

Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. Indicates that the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` failed because no service requests are added. Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` to add a service request.

 Value: 3

### P2P_UNSUPPORTED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val P2P_UNSUPPORTED: Int
```

Passed with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`. Indicates that the operation failed because p2p is unsupported on the device.

 Value: 1

### WIFI_P2P_CONNECTION_CHANGED_ACTION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_CONNECTION_CHANGED_ACTION: String
```

Broadcast intent action indicating that the state of Wi-Fi p2p connectivity has changed. One extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_INFO:kotlin.String` provides the p2p connection info in the form of a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo` object. Another extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_NETWORK_INFO:kotlin.String` provides the network info in the form of a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#`. A third extra provides the details of the group and may contain a `null`. All of these permissions are required to receive this broadcast: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` and either `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String`

 Value: "android.net.wifi.p2p.CONNECTION_STATE_CHANGE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_INFO:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_NETWORK_INFO:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_GROUP:kotlin.String`

### WIFI_P2P_DISCOVERY_CHANGED_ACTION

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_DISCOVERY_CHANGED_ACTION: String
```

Broadcast intent action indicating that peer discovery has either started or stopped. One extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_DISCOVERY_STATE:kotlin.String` indicates whether discovery has started or stopped.

Note that discovery will be stopped during a connection setup. If the application tries to re-initiate discovery during this time, it can fail.

 Value: "android.net.wifi.p2p.DISCOVERY_STATE_CHANGE"

### WIFI_P2P_DISCOVERY_STARTED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_DISCOVERY_STARTED: Int
```

p2p discovery has started

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_CHANGED_ACTION:kotlin.String`

### WIFI_P2P_DISCOVERY_STOPPED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_DISCOVERY_STOPPED: Int
```

p2p discovery has stopped

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_CHANGED_ACTION:kotlin.String`

### WIFI_P2P_LISTEN_STARTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_LISTEN_STARTED: Int
```

p2p listen has started

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ACTION_WIFI_P2P_LISTEN_STATE_CHANGED:kotlin.String`

### WIFI_P2P_LISTEN_STOPPED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_LISTEN_STOPPED: Int
```

p2p listen has stopped

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ACTION_WIFI_P2P_LISTEN_STATE_CHANGED:kotlin.String`

### WIFI_P2P_PEERS_CHANGED_ACTION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_PEERS_CHANGED_ACTION: String
```

Broadcast intent action indicating that the available peer list has changed. This can be sent as a result of peers being found, lost or updated. All of these permissions are required to receive this broadcast: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` and either `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String`

An extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_P2P_DEVICE_LIST:kotlin.String` provides the full list of current peers. The full list of peers can also be obtained any time with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.PeerListListener)`.

 Value: "android.net.wifi.p2p.PEERS_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_P2P_DEVICE_LIST:kotlin.String`

### WIFI_P2P_SCAN_FULL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_SCAN_FULL: Int
```

Run P2P scan on all channels.

 Value: 0

### WIFI_P2P_SCAN_SINGLE_FREQ

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_SCAN_SINGLE_FREQ: Int
```

Run P2P scan only on a specific channel.

 Value: 2

### WIFI_P2P_SCAN_SOCIAL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_SCAN_SOCIAL: Int
```

Run P2P scan only on social channels.

 Value: 1

### WIFI_P2P_STATE_CHANGED_ACTION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_STATE_CHANGED_ACTION: String
```

Broadcast intent action to indicate whether Wi-Fi p2p is enabled or disabled. An extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_STATE:kotlin.String` provides the state information as int.

 Value: "android.net.wifi.p2p.STATE_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_STATE:kotlin.String`

### WIFI_P2P_STATE_DISABLED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_STATE_DISABLED: Int
```

Wi-Fi p2p is disabled.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_CHANGED_ACTION:kotlin.String`

### WIFI_P2P_STATE_ENABLED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_STATE_ENABLED: Int
```

Wi-Fi p2p is enabled.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_CHANGED_ACTION:kotlin.String`

### WIFI_P2P_THIS_DEVICE_CHANGED_ACTION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_P2P_THIS_DEVICE_CHANGED_ACTION: String
```

Broadcast intent action indicating that this device details have changed.

An extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_DEVICE:kotlin.String` provides this device details. The valid device details can also be obtained with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)` when p2p is enabled. To get information notifications on P2P getting enabled refers `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int`.

The `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_DEVICE:kotlin.String` extra contains an anonymized version of the device's MAC address. Callers holding the `android.Manifest.permission#LOCAL_MAC_ADDRESS` permission can use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)` to obtain the actual MAC address of this device. All of these permissions are required to receive this broadcast: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_WIFI_STATE:kotlin.String` and either `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String`

 Value: "android.net.wifi.p2p.THIS_DEVICE_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_DEVICE:kotlin.String`

## Public methods

### addExternalApprover

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addExternalApprover(
    c: WifiP2pManager.Channel, 
    deviceAddress: MacAddress, 
    listener: WifiP2pManager.ExternalApproverRequestListener
): Unit
```

Set the external approver for a specific peer. This API associates a specific peer with an approver. When an incoming request is received from a peer, an authorization request is routed to the attached approver. The approver then calls `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` to send the result to the WiFi service. A specific peer (identified by its `MacAddress`) can only be attached to a single approver. The previous approver will be detached once a new approver is attached. The approver will also be detached automatically when the channel is closed.

When an approver is attached, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onAttached(android.net.MacAddress)` is called. When an approver is detached, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onDetached(android.net.MacAddress,%20kotlin.Int)` is called. When an incoming request is received, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onConnectionRequested(kotlin.Int,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pDevice)` is called. When a WPS PIN or a Wi-Fi Direct R2 pairing bootstrapping PIN is generated, `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onPinGenerated(android.net.MacAddress,%20kotlin.String)` is called.

The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_WIFI_NETWORK_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `deviceAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#): the peer which is bound to the external approver. This value cannot be `null`. |
| `listener` | [WifiP2pManager.ExternalApproverRequestListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener): for callback when the framework needs to notify the external approver. This value cannot be `null`. |
| --- | --- |

### addLocalService

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLocalService(
    channel: WifiP2pManager.Channel!, 
    servInfo: WifiP2pServiceInfo!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Register a local service for service discovery. If a local service is registered, the framework automatically responds to a service discovery request from a peer.

The function call immediately returns after sending a request to add a local service to the framework. The application is notified of a success or failure to add service through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The service information is set through `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo`. 
or its subclass calls `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceInfo#newInstance(kotlin.String,%20kotlin.String,%20kotlin.collections.MutableList)` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceInfo#newInstance(kotlin.String,%20kotlin.String,%20kotlin.collections.MutableMap)` for a Upnp or Bonjour service respectively

The service information can be cleared with calls to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeLocalService(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#clearLocalServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `servInfo` | [WifiP2pServiceInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo)!: is a local service information. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |
| --- | --- |

### addServiceRequest

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addServiceRequest(
    channel: WifiP2pManager.Channel!, 
    req: WifiP2pServiceRequest!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Add a service discovery request.

The function call immediately returns after sending a request to add service discovery request to the framework. The application is notified of a success or failure to add service through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The USD based service information are set in the service request through `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#WifiP2pServiceRequest(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)`. Application must use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` to determine whether the device supports USD based service discovery. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#` for service request information containing USD service configuration.

After service discovery request is added, you can initiate service discovery by `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

The added service requests can be cleared with calls to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#clearServiceRequests(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `req` | [WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest)!: is the service discovery request. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |
| --- | --- |

### cancelConnect

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelConnect(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Cancel any ongoing p2p group negotiation

The function call immediately returns after sending a connection cancellation request to the framework. The application is notified of a success or failure to initiate cancellation through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |

### clearLocalServices

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearLocalServices(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Clear all registered local services of service discovery.

The function call immediately returns after sending a request to clear all local services to the framework. The application is notified of a success or failure to add service through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |

### clearServiceRequests

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearServiceRequests(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Clear all registered service discovery requests.

The function call immediately returns after sending a request to clear all service discovery requests to the framework. The application is notified of a success or failure to add service through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |

### connect

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun connect(
    channel: WifiP2pManager.Channel!, 
    config: WifiP2pConfig!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Start a p2p connection to a device with the specified configuration.

The function call immediately returns after sending a connection request to the framework. The application is notified of a success or failure to initiate connect through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

An app should use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig.Builder` to build the configuration for this API, ex. call `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig.Builder#setDeviceAddress(android.net.MacAddress)` to set the peer MAC address and `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig.Builder#enablePersistentMode(kotlin.Boolean)` to configure the persistent mode.

Register for `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_CONNECTION_CHANGED_ACTION:kotlin.String` intent to determine when the framework notifies of a change in connectivity.

If the current device is not part of a p2p group, a connect request initiates a group negotiation with the peer.

If the current device is part of an existing p2p group or has created a p2p group with #createGroup, an invitation to join the group is sent to the peer device.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `config` | [WifiP2pConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig)!: options as described in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig` class |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |
| --- | --- |

### createGroup

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createGroup(
    channel: WifiP2pManager.Channel, 
    config: WifiP2pConfig?, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Create a p2p group with the current device as the group owner. This essentially creates an access point that can accept connections from legacy clients as well as other p2p devices.

An app should use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig.Builder` to build the configuration for a group.

**Note:** This function would normally not be used unless the current device needs to form a p2p group as a Group Owner and allow peers to join it as either Group Clients or legacy Wi-Fi STAs.

The function call immediately returns after sending a group creation request to the framework. The application is notified of a success or failure to initiate group creation through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

Application can request for the group details with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestGroupInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.GroupInfoListener)`.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `config` | [WifiP2pConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig)?: the configuration of a p2p group. This value may be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. Can be null. |
| --- | --- |

### createGroup

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createGroup(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Create a p2p group with the current device as the group owner. This essentially creates an access point that can accept connections from legacy clients as well as other p2p devices.

**Note:** This function would normally not be used unless the current device needs to form a p2p connection with a legacy client

The function call immediately returns after sending a group creation request to the framework. The application is notified of a success or failure to initiate group creation through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

Application can request for the group details with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestGroupInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.GroupInfoListener)`.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |

### discoverPeers

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun discoverPeers(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Initiate peer discovery. A discovery process involves scanning for available Wi-Fi peers for the purpose of establishing a connection.

The function call immediately returns after sending a discovery request to the framework. The application is notified of a success or failure to initiate discovery through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The discovery remains active until a connection is initiated or a p2p group is formed. Register for `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` intent to determine when the framework notifies of a change as peers are discovered.

Upon receiving a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` intent, an application can request the list of peers using `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.PeerListListener)`.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |

### discoverPeersOnSocialChannels

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun discoverPeersOnSocialChannels(
    channel: WifiP2pManager.Channel, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Scan only the social channels. A discovery process involves scanning for available Wi-Fi peers for the purpose of establishing a connection.

The function call immediately returns after sending a discovery request to the framework. The application is notified of a success or failure to initiate discovery through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The discovery remains active until a connection is initiated or a p2p group is formed. Register for `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` intent to determine when the framework notifies of a change as peers are discovered.

Upon receiving a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` intent, an application can request the list of peers using `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.PeerListListener)`.

The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isChannelConstrainedDiscoverySupported()` to determine whether the device supports this feature. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isChannelConstrainedDiscoverySupported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. This value may be `null`. |

### discoverPeersOnSpecificFrequency

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun discoverPeersOnSpecificFrequency(
    channel: WifiP2pManager.Channel, 
    frequencyMhz: Int, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Scan only a single channel specified by frequency. A discovery process involves scanning for available Wi-Fi peers for the purpose of establishing a connection.

The function call immediately returns after sending a discovery request to the framework. The application is notified of a success or failure to initiate discovery through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The discovery remains active until a connection is initiated or a p2p group is formed. Register for `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` intent to determine when the framework notifies of a change as peers are discovered.

Upon receiving a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String` intent, an application can request the list of peers using `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.PeerListListener)`.

The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isChannelConstrainedDiscoverySupported()` to determine whether the device supports this feature. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isChannelConstrainedDiscoverySupported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `frequencyMhz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): is the frequency of the channel to use for peer discovery. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. This value may be `null`. |
| --- | --- |

### discoverServices

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun discoverServices(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Initiate service discovery. A discovery process involves scanning for requested services for the purpose of establishing a connection to a peer that supports an available service.

The function call immediately returns after sending a request to start service discovery to the framework. The application is notified of a success or failure to initiate discovery through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The services to be discovered are specified with calls to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

The application is notified of the response against the service discovery request through listener callbacks registered by `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setServiceResponseListener(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ServiceResponseListener)` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setDnsSdResponseListeners(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DnsSdServiceResponseListener,%20android.net.wifi.p2p.WifiP2pManager.DnsSdTxtRecordListener)`, or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setUpnpServiceResponseListener(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.UpnpServiceResponseListener)`.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |

### discoverUsdBasedServices

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun discoverUsdBasedServices(
    channel: WifiP2pManager.Channel, 
    config: WifiP2pUsdBasedServiceDiscoveryConfig, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Initiate Un-synchronized service discovery (USD) based service discovery. A discovery process involves scanning for requested services for the purpose of establishing a connection to a peer that supports an available service using USD protocol. This method accepts a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedServiceDiscoveryConfig` object specifying the desired parameters for the service discovery. The configuration object allows to specify either a band or frequency list to scan for service.

The function call immediately returns after sending a request to start service discovery to the framework. The application is notified of a success or failure to initiate discovery through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The USD based services to be discovered are specified with calls to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` with the service request information set through `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#WifiP2pServiceRequest(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)`

The application is notified of the response against the service discovery request via `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener#onUsdBasedServiceAvailable(android.net.wifi.p2p.WifiP2pDevice,%20android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceResponse)` listener callback registered by `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setServiceResponseListener(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ServiceResponseListener)` .

Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` to determine whether the device supports this feature. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `config` | [WifiP2pUsdBasedServiceDiscoveryConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedServiceDiscoveryConfig): is the configuration for this USD based service discovery. This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. Can be null. |
| --- | --- |

### getListenState

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getListenState(
    c: WifiP2pManager.Channel, 
    executor: Executor, 
    resultsCallback: Consumer<Int!>
): Unit
```

Get p2p listen state.

This state indicates whether p2p listen has started or stopped. The valid value is one of `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STOPPED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STARTED:kotlin.Int`.

This state is also included in the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ACTION_WIFI_P2P_LISTEN_STATE_CHANGED:kotlin.String` broadcast event with extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_LISTEN_STATE:kotlin.String`.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): It is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `resultsCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: A callback that will return listen state `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STOPPED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STARTED:kotlin.Int` This value cannot be `null`. |
| --- | --- |

### getP2pMaxAllowedVendorElementsLengthBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getP2pMaxAllowedVendorElementsLengthBytes(): Int
```

Return the maximum total length (in bytes) of all Vendor specific information elements (VSIEs) which can be set using the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setVendorElements(android.net.wifi.p2p.WifiP2pManager.Channel,%20kotlin.collections.MutableList,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. The length is calculated adding the payload length + 2 bytes for each VSIE (2 bytes: 1 byte for type and 1 byte for length).

### initialize

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun initialize(
    srcContext: Context!, 
    srcLooper: Looper!, 
    listener: WifiP2pManager.ChannelListener!
): WifiP2pManager.Channel!
```

Registers the application with the Wi-Fi framework. This function must be the first to be called before any p2p operations are performed.

| Parameters ||
|---|---|
| `srcContext` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: is the context of the source |
| `srcLooper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)!: is the Looper on which the callbacks are receivied |
| `listener` | [WifiP2pManager.ChannelListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ChannelListener)!: for callback at loss of framework communication. Can be null. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel!` | Channel instance that is necessary for performing any further p2p operations |

### isChannelConstrainedDiscoverySupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isChannelConstrainedDiscoverySupported(): Boolean
```

Check if this device supports discovery limited to a specific frequency or the social channels. Gates whether `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeersOnSpecificFrequency(android.net.wifi.p2p.WifiP2pManager.Channel,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` and `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeersOnSocialChannels(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` methods are functional on this device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### isGroupClientRemovalSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isGroupClientRemovalSupported(): Boolean
```

Check if this device supports removing clients from a group. Gates whether the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeClient(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` method is functional on this device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### isGroupOwnerIPv6LinkLocalAddressProvided

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isGroupOwnerIPv6LinkLocalAddressProvided(): Boolean
```

Checks whether this device, while being a group client, can discover and deliver the group owner's IPv6 link-local address.

If this method returns `true` and `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#connect(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` method is called with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig` having `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig#GROUP_CLIENT_IP_PROVISIONING_MODE_IPV6_LINK_LOCAL:kotlin.Int` as the group client IP provisioning mode, then the group owner's IPv6 link-local address will be delivered in the group client via `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_CONNECTION_CHANGED_ACTION:kotlin.String` broadcast intent (i.e, group owner address in `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_INFO:kotlin.String`). If this method returns `false`, then IPv6 link-local addresses can still be used, but it is the responsibility of the caller to discover that address in other ways, e.g. using out-of-band communication.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### isPccModeSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPccModeSupported(): Boolean
```

Check if this device supports P2P Connection Compatibility Mode(R1/R2 compatibility mode).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports hosting an autonomous Group Owner which allows legacy P2P clients and R2 clients to join the group in PCC Mode and also supports connecting to a Group Owner either using legacy security mode (WPA2-PSK) or R2 mandated security mode(WPA3-SAE) in PCC Mode. |

### isSetVendorElementsSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSetVendorElementsSupported(): Boolean
```

Check if this device supports setting vendor elements. Gates whether the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setVendorElements(android.net.wifi.p2p.WifiP2pManager.Channel,%20kotlin.collections.MutableList,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` method is functional on this device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if supported, `false` otherwise. |

### isWiFiDirectR2Supported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWiFiDirectR2Supported(): Boolean
```

Check if this device supports Wi-Fi Direct R2 (P2P2).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this device supports Wi-Fi Alliance Wi-Fi Direct R2 (Support for P2P2 IE and establishing connection by using the P2P pairing protocol), false otherwise. For more details, visit <https://www.wi-fi.org/> and search for "Wi-Fi Direct" . |

### registerWifiP2pListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerWifiP2pListener(
    executor: Executor, 
    listener: WifiP2pManager.WifiP2pListener
): Unit
```

Add a listener to listen to Wi-Fi p2p various changes.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the Executor on which to execute the callbacks. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [WifiP2pManager.WifiP2pListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener): listener for the Wi-Fi p2p connection changes. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if incorrect input arguments are provided. |
| `java.lang.SecurityException` | if the caller is missing required permissions. |

### removeClient

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeClient(
    channel: WifiP2pManager.Channel, 
    peerAddress: MacAddress, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Remove the client with the MAC address from the group.

The function call immediately returns after sending a client removal request to the framework. The application is notified of a success or failure to initiate client removal through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The callbacks are triggered on the thread specified when initializing the `channel`, see `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`.

Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isGroupClientRemovalSupported()` to determine whether the device supports this feature. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isGroupClientRemovalSupported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `peerAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#): MAC address of the client. This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. Can be null. |
| --- | --- |

### removeExternalApprover

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeExternalApprover(
    c: WifiP2pManager.Channel, 
    deviceAddress: MacAddress, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Remove the external approver for a specific peer. The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_WIFI_NETWORK_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `deviceAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#): the peer which is bound to the external approver. This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callback on success or failure. This value may be `null`. |
| --- | --- |

### removeGroup

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeGroup(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Remove the current p2p group.

The function call immediately returns after sending a group removal request to the framework. The application is notified of a success or failure to initiate group removal through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |

### removeLocalService

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLocalService(
    channel: WifiP2pManager.Channel!, 
    servInfo: WifiP2pServiceInfo!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Remove a registered local service added with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addLocalService(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`

The function call immediately returns after sending a request to remove a local service to the framework. The application is notified of a success or failure to add service through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `servInfo` | [WifiP2pServiceInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo)!: is the local service information. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |
| --- | --- |

### removeServiceRequest

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeServiceRequest(
    channel: WifiP2pManager.Channel!, 
    req: WifiP2pServiceRequest!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Remove a specified service discovery request added with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`

The function call immediately returns after sending a request to remove service discovery request to the framework. The application is notified of a success or failure to add service through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `req` | [WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest)!: is the service discovery request. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |
| --- | --- |

### requestConnectionInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestConnectionInfo(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ConnectionInfoListener!
): Unit
```

Request device connection info.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ConnectionInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener)!: for callback when connection info is available. Can be null. |

### requestDeviceInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestDeviceInfo(
    c: WifiP2pManager.Channel, 
    listener: WifiP2pManager.DeviceInfoListener
): Unit
```

Request Device Info

This method provides the device info in the form of a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice`. Valid `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` is returned when p2p is enabled. To get information notifications on P2P getting enabled refers `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int`.

This `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` is returned using the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener` listener.

`https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice#deviceAddress:kotlin.String` is only available if the caller holds the `android.Manifest.permission#LOCAL_MAC_ADDRESS` permission, and holds the anonymized MAC address (02:00:00:00:00:00) otherwise.

This information is also included in the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_THIS_DEVICE_CHANGED_ACTION:kotlin.String` broadcast event with extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_P2P_DEVICE:kotlin.String`.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `listener` | [WifiP2pManager.DeviceInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener): for callback when network info is available. This value cannot be `null`. |

### requestDirInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestDirInfo(
    c: WifiP2pManager.Channel, 
    executor: Executor, 
    callback: OutcomeReceiver<WifiP2pDirInfo!, Exception!>
): Unit
```

Get the Device Identity Resolution (DIR) Information. See `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo` for details Note: The results callback returns null if the device doesn't have any persistent group with device identity key information.

Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` to determine whether the device supports this feature. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

The caller must hold the android.Manifest.permission#LOCAL_MAC_ADDRESS permission to obtain `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo`. If the caller does not hold this permission, `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)` is called with a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): It is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [WifiP2pDirInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>: An OutcomeReceiver callback for receiving `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo` via `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)`. This callback will return null when DIR info doesn't exist. When this API call fails due to permission issues, state machine is busy etc., `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)` is called. |
| --- | --- |

### requestDiscoveryState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestDiscoveryState(
    c: WifiP2pManager.Channel, 
    listener: WifiP2pManager.DiscoveryStateListener
): Unit
```

Request p2p discovery state.

This state indicates whether p2p discovery has started or stopped. The valid value is one of `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED:kotlin.Int`. The state is returned using the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener` listener.

This state is also included in the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_CHANGED_ACTION:kotlin.String` broadcast event with extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_DISCOVERY_STATE:kotlin.String`.

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `listener` | [WifiP2pManager.DiscoveryStateListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener): for callback when discovery state is available. This value cannot be `null`. |

### requestGroupInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestGroupInfo(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.GroupInfoListener!
): Unit
```

Request p2p group info.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.GroupInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.GroupInfoListener)!: for callback when group info is available. Can be null. |

### requestNetworkInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestNetworkInfo(
    c: WifiP2pManager.Channel, 
    listener: WifiP2pManager.NetworkInfoListener
): Unit
```

Request network info.

This method provides the network info in the form of a `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#`. `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#isAvailable()` indicates the p2p availability and `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#getDetailedState()` reports the current fine-grained state of the network. This `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` is returned using the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener` listener.

This information is also included in the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_CONNECTION_CHANGED_ACTION:kotlin.String` broadcast event with extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_NETWORK_INFO:kotlin.String`.

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `listener` | [WifiP2pManager.NetworkInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener): for callback when network info is available. This value cannot be `null`. |

### requestP2pState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestP2pState(
    c: WifiP2pManager.Channel, 
    listener: WifiP2pManager.P2pStateListener
): Unit
```

Request p2p enabled state.

This state indicates whether Wi-Fi p2p is enabled or disabled. The valid value is one of `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_DISABLED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int`. The state is returned using the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.P2pStateListener` listener.

This state is also included in the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_CHANGED_ACTION:kotlin.String` broadcast event with extra `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#EXTRA_WIFI_STATE:kotlin.String`.

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `listener` | [WifiP2pManager.P2pStateListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.P2pStateListener): for callback when p2p state is available. This value cannot be `null`. |

### requestPeers

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestPeers(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.PeerListListener!
): Unit
```

Request the current list of peers.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.PeerListListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.PeerListListener)!: for callback when peer list is available. Can be null. |

### setConnectionRequestResult

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setConnectionRequestResult(
    c: WifiP2pManager.Channel, 
    deviceAddress: MacAddress, 
    result: Int, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Set the result for the incoming request from a specific peer. The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_WIFI_NETWORK_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `deviceAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#): the peer which is bound to the external approver. This value cannot be `null`. |
| `result` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the response for the incoming request. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_ACCEPT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_REJECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_TO_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_SHOW_PIN_TO_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_SHOW_PASSWORD_TO_SERVICE:kotlin.Int` |
| --- | --- |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callback on success or failure. This value may be `null`. |

### setConnectionRequestResult

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setConnectionRequestResult(
    c: WifiP2pManager.Channel, 
    deviceAddress: MacAddress, 
    result: Int, 
    pinOrPassword: String?, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Set the result with PIN for the incoming request from a specific peer. The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_WIFI_NETWORK_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `deviceAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#): the peer which is bound to the external approver. This value cannot be `null`. |
| `result` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the response for the incoming request. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_ACCEPT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_REJECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_TO_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_SHOW_PIN_TO_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_SHOW_PASSWORD_TO_SERVICE:kotlin.Int` |
| --- | --- |
| `pinOrPassword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the WPS PIN or Wi-Fi Direct R2 pairing bootstrapping PIN/Password for the incoming request. This value may be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callback on success or failure. This value may be `null`. |

### setDnsSdResponseListeners

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDnsSdResponseListeners(
    channel: WifiP2pManager.Channel!, 
    servListener: WifiP2pManager.DnsSdServiceResponseListener!, 
    txtListener: WifiP2pManager.DnsSdTxtRecordListener!
): Unit
```

Register a callback to be invoked on receiving Bonjour service discovery response.

see `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` for the detail.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: |
| `servListener` | [WifiP2pManager.DnsSdServiceResponseListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DnsSdServiceResponseListener)!: is for listening to a Bonjour service response |
| `txtListener` | [WifiP2pManager.DnsSdTxtRecordListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DnsSdTxtRecordListener)!: is for listening to a Bonjour TXT record response |
| --- | --- |

### setServiceResponseListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setServiceResponseListener(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ServiceResponseListener!
): Unit
```

Register a callback to be invoked on receiving service discovery response. Used only for vendor specific protocol right now. For Bonjour or Upnp, use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setDnsSdResponseListeners(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DnsSdServiceResponseListener,%20android.net.wifi.p2p.WifiP2pManager.DnsSdTxtRecordListener)` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setUpnpServiceResponseListener(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.UpnpServiceResponseListener)` respectively.

see `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` for the detail.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ServiceResponseListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener)!: for callbacks on receiving service discovery response. |

### setUpnpServiceResponseListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUpnpServiceResponseListener(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.UpnpServiceResponseListener!
): Unit
```

Register a callback to be invoked on receiving upnp service discovery response.

see `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` for the detail.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.UpnpServiceResponseListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.UpnpServiceResponseListener)!: for callbacks on receiving service discovery response. |

### setVendorElements

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVendorElements(
    c: WifiP2pManager.Channel, 
    vendorElements: MutableList<ScanResult.InformationElement!>, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Set/Clear vendor specific information elements (VSIEs) to be published during Wi-Fi Direct (P2P) discovery. Once `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel#close()` is called, the vendor information elements will be cleared from framework. The information element format is defined in the IEEE 802.11-2016 spec Table 9-77.

To clear the previously set vendor elements, call this API with an empty List.

The maximum accumulated length of all VSIEs must be before the limit specified by `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#getP2pMaxAllowedVendorElementsLengthBytes()`.

To publish vendor elements, this API should be called before peer discovery API, ex. `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isSetVendorElementsSupported()` to determine whether the device supports this feature. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isSetVendorElementsSupported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#OVERRIDE_WIFI_CONFIG:kotlin.String`

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `vendorElements` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult.InformationElement](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.InformationElement.html#)!\>: application information as vendor-specific information elements. This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callback when network info is available. This value may be `null`. |
| --- | --- |

### setWfdInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWfdInfo(
    channel: WifiP2pManager.Channel, 
    wfdInfo: WifiP2pWfdInfo, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Set Wifi Display information. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CONFIGURE_WIFI_DISPLAY:kotlin.String`

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `wfdInfo` | [WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo): the Wifi Display information to set. This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. Can be null. |
| --- | --- |

### startListening

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startListening(
    channel: WifiP2pManager.Channel, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Force p2p to enter listen state. When this API is called, this device will periodically enter LISTENING state until `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#stopListening(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#stopPeerDiscovery(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` are called. While in LISTENING state, this device will dwell at its social channel and respond to probe requests from other Wi-Fi Direct peers.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. This value may be `null`. |

### startPeerDiscovery

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startPeerDiscovery(
    channel: WifiP2pManager.Channel, 
    config: WifiP2pDiscoveryConfig, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Initiate peer discovery. A discovery process involves scanning for available Wi-Fi peers for the purpose of establishing a connection. See `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` for more details. This method accepts a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDiscoveryConfig` object specifying the desired parameters for the peer discovery. The configuration object allows the specification of the scan type (ex. FULL, SOCIAL) and the inclusion of vendor-specific configuration data. The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `config` | [WifiP2pDiscoveryConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDiscoveryConfig): is the configuration for this peer discovery. This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. This value may be `null`. |
| --- | --- |

### startUsdBasedLocalServiceAdvertisement

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startUsdBasedLocalServiceAdvertisement(
    channel: WifiP2pManager.Channel, 
    servInfo: WifiP2pServiceInfo, 
    config: WifiP2pUsdBasedLocalServiceAdvertisementConfig, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Start a service discovery advertisement using Un-synchronized service discovery (USD). Once `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#startUsdBasedLocalServiceAdvertisement(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pUsdBasedLocalServiceAdvertisementConfig,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` is called, the device will go to the channel frequency requested via `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedLocalServiceAdvertisementConfig` and responds to a service discovery request from a peer.

The service information is set through `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo#WifiP2pServiceInfo(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)`

The function call immediately returns after sending a request to start the service advertisement to the framework. The application is notified of a success or failure to start service advertisement through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

The service information can be cleared with calls to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeLocalService(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceInfo,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#clearLocalServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`.

Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` to determine whether the device supports this feature. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `servInfo` | [WifiP2pServiceInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo): is a local service information. This value cannot be `null`. |
| `config` | [WifiP2pUsdBasedLocalServiceAdvertisementConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedLocalServiceAdvertisementConfig): is the configuration for this service discovery advertisement. This value cannot be `null`. |
| --- | --- |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. Can be null. |

### stopListening

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopListening(
    channel: WifiP2pManager.Channel, 
    listener: WifiP2pManager.ActionListener?
): Unit
```

Force p2p to exit listen state. When this API is called, this device will stop entering LISTENING state periodically which is triggered by `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#startListening(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`. If there are running peer discovery which is triggered by `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)` or running service discovery which is triggered by `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#discoverServices(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)`, they will be stopped as well.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` This value cannot be `null`. |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)?: for callbacks on success or failure. This value may be `null`. |

### stopPeerDiscovery

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopPeerDiscovery(
    channel: WifiP2pManager.Channel!, 
    listener: WifiP2pManager.ActionListener!
): Unit
```

Stop an ongoing peer discovery

The function call immediately returns after sending a stop request to the framework. The application is notified of a success or failure to initiate stop through listener callbacks `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onSuccess()` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener#onFailure(kotlin.Int)`.

If P2P Group is in the process of being created, this call will fail (report failure via `listener`. The applicantion should listen to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_CONNECTION_CHANGED_ACTION:kotlin.String` to ensure the state is not `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.State.html#` and repeat calling when the state changes.

| Parameters ||
|---|---|
| `channel` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel)!: is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)` |
| `listener` | [WifiP2pManager.ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener)!: for callbacks on success or failure. Can be null. |

### unregisterWifiP2pListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterWifiP2pListener(listener: WifiP2pManager.WifiP2pListener): Unit
```

Remove a listener added using `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#registerWifiP2pListener(java.util.concurrent.Executor,%20android.net.wifi.p2p.WifiP2pManager.WifiP2pListener)`

| Parameters ||
|---|---|
| `listener` | [WifiP2pManager.WifiP2pListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener): the listener to be removed. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if incorrect input arguments are provided. |

### validateDirInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun validateDirInfo(
    c: WifiP2pManager.Channel, 
    dirInfo: WifiP2pDirInfo, 
    executor: Executor, 
    callback: OutcomeReceiver<Boolean!, Exception!>
): Unit
```

Validate the Device Identity Resolution (DIR) Information of a P2P device. See `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo` for details. Framework takes the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo` and derives a set of Tag values based on the cached Device Identity Keys (DevIK) of all paired peers saved in the device. If a derived Tag value matches the Tag value received in the `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo`, the device is identified as a paired peer and returns true.

Use `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` to determine whether the device supports this feature. If `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#isWiFiDirectR2Supported()` return `false` then this method will throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

The application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `c` | [WifiP2pManager.Channel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel): It is the channel created at `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener)`. This value cannot be `null`. |
| `dirInfo` | [WifiP2pDirInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo): `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo` to validate. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>: An OutcomeReceiver callback for receiving the result via `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)` indicating whether the DIR info of P2P device is of a paired device. {code true} for paired, `false` for not paired. When this API call fails due to permission issues, state machine is busy etc., `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)` is called. This value cannot be `null`. |
