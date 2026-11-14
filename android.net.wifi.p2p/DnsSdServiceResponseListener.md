# WifiP2pManager.DnsSdServiceResponseListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DnsSdServiceResponseListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.DnsSdServiceResponseListener.md) 
| --- | --- |

```
interface DnsSdServiceResponseListener
```

| [android.net.wifi.p2p.WifiP2pManager.DnsSdServiceResponseListener](../android/net/wifi/p2p/WifiP2pManager.DnsSdServiceResponseListener.md) |

Interface for callback invocation when Bonjour service discovery response is received

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDnsSdServiceAvailable](../android/net/wifi/p2p/WifiP2pManager.DnsSdServiceResponseListener.md))`(`instanceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `registrationType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `srcDevice:` ` [WifiP2pDevice](../android/net/wifi/p2p/WifiP2pDevice.md)!`)` The requested Bonjour service response is available. |

## Public methods

### onDnsSdServiceAvailable

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDnsSdServiceAvailable(
    instanceName: String!, 
    registrationType: String!, 
    srcDevice: WifiP2pDevice!
): Unit
```

The requested Bonjour service response is available.

This function is invoked when the device with the specified Bonjour registration type returned the instance name.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------|
| `instanceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:instance name. e.g) "MyPrinter". |
| `registrationType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: e.g) "_ipp._tcp.local." |
| `srcDevice` | [WifiP2pDevice](../android/net/wifi/p2p/WifiP2pDevice.md)!:source device. |
| --- | --- |
