# android.net.wifi.p2p

Kotlin | [Java](https://developer.android.com/reference/android/net/wifi/p2p/package-summary "View this page in Java")

## Interfaces

| [ActionListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ActionListener) | Interface for callback invocation on an application action |
| [ChannelListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ChannelListener) | Interface for callback invocation when framework channel is lost |
| [ConnectionInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener) | Interface for callback invocation when connection info is available |
| [DeviceInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener) | Interface for callback invocation when `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice` is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)`. |
| [DiscoveryStateListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener) | Interface for callback invocation when p2p state is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDiscoveryState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DiscoveryStateListener)`. |
| [DnsSdServiceResponseListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DnsSdServiceResponseListener) | Interface for callback invocation when Bonjour service discovery response is received |
| [DnsSdTxtRecordListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DnsSdTxtRecordListener) | Interface for callback invocation when Bonjour TXT record is available for a service |
| [ExternalApproverRequestListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener) | Interface for callback invocation when an incoming request is received. |
| [GroupInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.GroupInfoListener) | Interface for callback invocation when group info is available |
| [NetworkInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener) | Interface for callback invocation when `https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#` is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestNetworkInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.NetworkInfoListener)`. |
| [P2pStateListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.P2pStateListener) | Interface for callback invocation when p2p state is available in response to `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestP2pState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.P2pStateListener)`. |
| [PeerListListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.PeerListListener) | Interface for callback invocation when peer list is available |
| [ServiceResponseListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener) | Interface for callback invocation when service discovery response other than Upnp or Bonjour is received |
| [UpnpServiceResponseListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.UpnpServiceResponseListener) | Interface for callback invocation when upnp service discovery response is received |
| [WifiP2pListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener) | Interface used to listen to Wi-Fi p2p various changes such as device state change, discovery started/stopped, connection change, etc. |

## Classes

| [WifiP2pConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig) | A class representing a Wi-Fi P2p configuration for setting up a connection |
| [WifiP2pConnectionInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo) | A class representing the connection capabilities of a Wi-Fi P2P link. |
| [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice) | A class representing a Wi-Fi p2p device Note that the operations are not thread safe |
| [WifiP2pDeviceList](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDeviceList) | A class representing a Wi-Fi P2p device list. |
| [WifiP2pDirInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo) | This object contains the Device Identity Resolution (DIR) Info to check if the device is a previously paired device. |
| [WifiP2pDiscoveryConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDiscoveryConfig) | A class representing a Wi-Fi P2P scan configuration for setting up discovery. |
| [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup) | A class representing a Wi-Fi P2p group. |
| [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo) | A class representing connection information about a Wi-Fi p2p group |
| [WifiP2pManager](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager) | This class provides the API for managing Wi-Fi peer-to-peer connectivity. |
| [WifiP2pPairingBootstrappingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig) | A class representing Wi-Fi Direct pairing bootstrapping configuration. |
| [WifiP2pUsdBasedLocalServiceAdvertisementConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedLocalServiceAdvertisementConfig) | A class representing a Wi-Fi P2P USD based service advertisement configuration for advertising the services. |
| [WifiP2pUsdBasedServiceDiscoveryConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pUsdBasedServiceDiscoveryConfig) | A class representing a Wi-Fi P2P USD based service discovery configuration for discovering the services. |
| [WifiP2pWfdInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pWfdInfo) | A class representing Wifi Display information for a device. |
