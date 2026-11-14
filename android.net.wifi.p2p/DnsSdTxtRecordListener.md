# WifiP2pManager.DnsSdTxtRecordListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DnsSdTxtRecordListener

Kotlin | [Java](../android/net/wifi/p2p/WifiP2pManager.DnsSdTxtRecordListener.md) 
| --- | --- |

```
interface DnsSdTxtRecordListener
```

| [android.net.wifi.p2p.WifiP2pManager.DnsSdTxtRecordListener](../android/net/wifi/p2p/WifiP2pManager.DnsSdTxtRecordListener.md) |

Interface for callback invocation when Bonjour TXT record is available for a service

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDnsSdTxtRecordAvailable](../android/net/wifi/p2p/WifiP2pManager.DnsSdTxtRecordListener.md))`(`fullDomainName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `txtRecordMap:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `srcDevice:` ` [WifiP2pDevice](WifiP2pDevice.md)!`)` The requested Bonjour service response is available. |

## Public methods

### onDnsSdTxtRecordAvailable

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDnsSdTxtRecordAvailable(
    fullDomainName: String!, 
    txtRecordMap: MutableMap<String!, String!>!, 
    srcDevice: WifiP2pDevice!
): Unit
```

The requested Bonjour service response is available.

This function is invoked when the device with the specified full service domain service returned TXT record.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fullDomainName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: full domain name. e.g) "MyPrinter._ipp._tcp.local.". |
| `txtRecordMap` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: TXT record data as a map of key/value pairs |
| `srcDevice` | [WifiP2pDevice](WifiP2pDevice.md)!: source device. |
| --- | --- |
