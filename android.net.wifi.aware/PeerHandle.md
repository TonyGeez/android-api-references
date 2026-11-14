# PeerHandle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PeerHandle

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/aware/PeerHandle "View this page in Java") 
| --- | --- |

```
open class PeerHandle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle#) |

| Known Direct Subclasses [ParcelablePeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ParcelablePeerHandle) |--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [ParcelablePeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ParcelablePeerHandle) | A Parcelable [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle#). | |
| --- | --- | --- | --- | --- | --- | --- |

Opaque object used to represent a Wi-Fi Aware peer. Obtained from discovery sessions in[DiscoverySessionCallback.onServiceDiscovered(PeerHandle, byte[], java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))or received messages in[DiscoverySessionCallback.onMessageReceived(PeerHandle, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)), and used when sending messages e,g,[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)), or when configuring a network link to a peer, e.g. [DiscoverySession.createNetworkSpecifierOpen(PeerHandle)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#createNetworkSpecifierOpen(android.net.wifi.aware.PeerHandle))or [DiscoverySession.createNetworkSpecifierPassphrase(PeerHandle, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#createNetworkSpecifierPassphrase(android.net.wifi.aware.PeerHandle,%20kotlin.String)).

Note that while a`PeerHandle`can be used to track a particular peer (i.e. you can compare the values received from subsequent messages) - it is good practice not to rely on it. Instead use an application level peer identifier encoded in the message,[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)), and/or in the Publish configuration's service-specific information field,[PublishConfig.Builder.setServiceSpecificInfo(byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setServiceSpecificInfo(kotlin.ByteArray)), or match filter, [PublishConfig.Builder.setMatchFilter(java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setMatchFilter(kotlin.collections.MutableList)).

A parcelable handle object is available with [ParcelablePeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ParcelablePeerHandle).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle#hashCode())`()` <br /> |

## Public methods

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
