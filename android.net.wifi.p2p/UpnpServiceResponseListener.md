# WifiP2pManager.UpnpServiceResponseListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UpnpServiceResponseListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.UpnpServiceResponseListener.md) 
| --- | --- |

```
interface UpnpServiceResponseListener
```

| [android.net.wifi.p2p.WifiP2pManager.UpnpServiceResponseListener](../android/net/wifi/p2p/WifiP2pManager.UpnpServiceResponseListener.md) |

Interface for callback invocation when upnp service discovery response is received

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUpnpServiceAvailable](../android/net/wifi/p2p/WifiP2pManager.UpnpServiceResponseListener.md))`(`uniqueServiceNames:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `srcDevice:` ` [WifiP2pDevice](../android/net/wifi/p2p/WifiP2pDevice.md)!`)` The requested upnp service response is available. |

## Public methods

### onUpnpServiceAvailable

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUpnpServiceAvailable(
    uniqueServiceNames: MutableList<String!>!, 
    srcDevice: WifiP2pDevice!
): Unit
```

The requested upnp service response is available.

This function is invoked when the specified device or service is found.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uniqueServiceNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The list of unique service names. e.g) uuid:6859dede-8574-59ab-9332-123456789012::urn:schemas-upnp-org:device: MediaServer:1 |
| `srcDevice` | [WifiP2pDevice](../android/net/wifi/p2p/WifiP2pDevice.md)!:source device. |
