# android.net.wifi.p2p

Kotlin | [Java](_package.md)
| --- | --- |

## Interfaces

| [ActionListener](../android/net/wifi/p2p/WifiP2pManager.ActionListener.md) | Interface for callback invocation on an application action |
| --- | --- |
| [ChannelListener](../android/net/wifi/p2p/WifiP2pManager.ChannelListener.md) | Interface for callback invocation when framework channel is lost |
| [ConnectionInfoListener](../android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener.md) | Interface for callback invocation when connection info is available |
| [DeviceInfoListener](../android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener.md) | Interface for callback invocation when `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)`. |
| --- | --- |
| [DiscoveryStateListener](../android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener.md) | Interface for callback invocation when p2p state is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDiscoveryState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DiscoveryStateListener)`. |
| [DnsSdServiceResponseListener](../android/net/wifi/p2p/WifiP2pManager.DnsSdServiceResponseListener.md) | Interface for callback invocation when Bonjour service discovery response is received |
| [DnsSdTxtRecordListener](../android/net/wifi/p2p/WifiP2pManager.DnsSdTxtRecordListener.md) | Interface for callback invocation when Bonjour TXT record is available for a service |
| --- | --- |
| [ExternalApproverRequestListener](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) | Interface for callback invocation when an incoming request is received. |
| [GroupInfoListener](../android/net/wifi/p2p/WifiP2pManager.GroupInfoListener.md) | Interface for callback invocation when group info is available |
| [NetworkInfoListener](../android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener.md) | Interface for callback invocation when `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestNetworkInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.NetworkInfoListener)`. |
| --- | --- |
| [P2pStateListener](../android/net/wifi/p2p/WifiP2pManager.P2pStateListener.md) | Interface for callback invocation when p2p state is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestP2pState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.P2pStateListener)`. |
| [PeerListListener](../android/net/wifi/p2p/WifiP2pManager.PeerListListener.md) | Interface for callback invocation when peer list is available |
| [ServiceResponseListener](../android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener.md) | Interface for callback invocation when service discovery response other than Upnp or Bonjour is received |
| --- | --- |
| [UpnpServiceResponseListener](../android/net/wifi/p2p/WifiP2pManager.UpnpServiceResponseListener.md) | Interface for callback invocation when upnp service discovery response is received |
| [WifiP2pListener](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md) | Interface used to listen to Wi-Fi p2p various changes such as device state change, discovery started/stopped, connection change, etc. |

## Classes

| [WifiP2pConfig](WifiP2pConfig.md) | A class representing a Wi-Fi P2p configuration for setting up a connection |
| --- | --- |
| [WifiP2pConnectionInfo](WifiP2pConnectionInfo.md) | A class representing the connection capabilities of a Wi-Fi P2P link. |
| [WifiP2pDevice](WifiP2pDevice.md) | A class representing a Wi-Fi p2p device Note that the operations are not thread safe |
| [WifiP2pDeviceList](WifiP2pDeviceList.md) | A class representing a Wi-Fi P2p device list. |
| --- | --- |
| [WifiP2pDirInfo](WifiP2pDirInfo.md) | This object contains the Device Identity Resolution (DIR) Info to check if the device is a previously paired device. |
| [WifiP2pDiscoveryConfig](WifiP2pDiscoveryConfig.md) | A class representing a Wi-Fi P2P scan configuration for setting up discovery. |
| [WifiP2pGroup](WifiP2pGroup.md) | A class representing a Wi-Fi P2p group. |
| --- | --- |
| [WifiP2pInfo](WifiP2pInfo.md) | A class representing connection information about a Wi-Fi p2p group |
| [WifiP2pManager](WifiP2pManager.md) | This class provides the API for managing Wi-Fi peer-to-peer connectivity. |
| [WifiP2pPairingBootstrappingConfig](WifiP2pPairingBootstrappingConfig.md) | A class representing Wi-Fi Direct pairing bootstrapping configuration. |
| --- | --- |
| [WifiP2pUsdBasedLocalServiceAdvertisementConfig](WifiP2pUsdBasedLocalServiceAdvertisementConfig.md) | A class representing a Wi-Fi P2P USD based service advertisement configuration for advertising the services. |
| [WifiP2pUsdBasedServiceDiscoveryConfig](WifiP2pUsdBasedServiceDiscoveryConfig.md) | A class representing a Wi-Fi P2P USD based service discovery configuration for discovering the services. |
| [WifiP2pWfdInfo](WifiP2pWfdInfo.md) | A class representing Wifi Display information for a device. |
| --- | --- |
