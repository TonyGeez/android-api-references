# WifiP2pManager.ServiceResponseListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceResponseListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener "View this page in Java") 
| --- | --- |

```
interface ServiceResponseListener
```

| [android.net.wifi.p2p.WifiP2pManager.ServiceResponseListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener#) |

Interface for callback invocation when service discovery response other than Upnp or Bonjour is received

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener#onServiceAvailable(kotlin.Int,%20kotlin.ByteArray,%20android.net.wifi.p2p.WifiP2pDevice))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `responseData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `srcDevice:` ` [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice)!`)` The requested service response is available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUsdBasedServiceAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ServiceResponseListener#onUsdBasedServiceAvailable(android.net.wifi.p2p.WifiP2pDevice,%20android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceResponse))`(`srcDevice:` ` [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice)`, `usdResponseData:` ` [WifiP2pUsdBasedServiceResponse](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceResponse)`)` The requested USD based service response is available. |

## Public methods

### onServiceAvailable

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceAvailable(
    protocolType: Int, 
    responseData: ByteArray!, 
    srcDevice: WifiP2pDevice!
): Unit
```

The requested service response is available.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `protocolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):protocol type. currently only [WifiP2pServiceInfo.SERVICE_TYPE_VENDOR_SPECIFIC](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo#SERVICE_TYPE_VENDOR_SPECIFIC:kotlin.Int). |
| `responseData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:service discovery response data based on the requested service protocol type. The format depends on the service type. |
| `srcDevice` | [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice)!:source device. |
| --- | --- |

### onUsdBasedServiceAvailable

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUsdBasedServiceAvailable(
    srcDevice: WifiP2pDevice, 
    usdResponseData: WifiP2pUsdBasedServiceResponse
): Unit
```

The requested USD based service response is available.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcDevice` | [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice):source device. This value cannot be`null`. |
| `usdResponseData` | [WifiP2pUsdBasedServiceResponse](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceResponse): [WifiP2pUsdBasedServiceResponse](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceResponse). This value cannot be`null`. |
