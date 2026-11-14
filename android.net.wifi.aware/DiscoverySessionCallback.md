# DiscoverySessionCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DiscoverySessionCallback

Kotlin| [Java](../android/net/wifi/aware/DiscoverySessionCallback.md) 
| --- | --- |

```
open class DiscoverySessionCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.DiscoverySessionCallback](../android/net/wifi/aware/DiscoverySessionCallback.md) |

Base class for Aware session events callbacks. Should be extended by applications wanting notifications. The callbacks are set when a publish or subscribe session is created using [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md))or [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md)).

A single callback is set at session creation - it cannot be replaced.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DiscoverySessionCallback](../android/net/wifi/aware/DiscoverySessionCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBootstrappingFailed](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)`)` Callback indicating that a Bootstrapping method negotiation failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBootstrappingSucceeded](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)`, `method:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback indicating that a Bootstrapping method negotiation succeeded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageReceived](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)!`, `message:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Called when a message is received from a discovery session peer - in response to the peer's[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageSendFailed](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`messageId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when message transmission initiated with[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))fails. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageSendSucceeded](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`messageId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called in response to[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))when a message is transmitted successfully - i. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingSetupFailed](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)`)` Callback indicating that a pairing setup process failed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingSetupRequestReceived](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)`, `requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback indicating that a pairing request is received from peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingSetupSucceeded](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)`, `alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Callback indicating that a pairing setup process succeeded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingVerificationFailed](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)`)` Callback indicating that a pairing verification process failed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingVerificationSucceed](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)`, `alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Callback indicating that a pairing verification process succeeded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPublishStarted](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`session:` ` [PublishDiscoverySession](../android/net/wifi/aware/PublishDiscoverySession.md)`)` Called when a publish operation is started successfully in response to a [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md))operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDiscovered](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)!`, `serviceSpecificInfo:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `matchFilter:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>!`)` Called when a subscribe operation results in a service discovery. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDiscovered](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`info:` ` [ServiceDiscoveryInfo](../android/net/wifi/aware/ServiceDiscoveryInfo.md)`)` Called when a subscribe operation results in a service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDiscoveredWithinRange](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)!`, `serviceSpecificInfo:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `matchFilter:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>!`, `distanceMm:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a subscribe operation results in a service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDiscoveredWithinRange](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`info:` ` [ServiceDiscoveryInfo](../android/net/wifi/aware/ServiceDiscoveryInfo.md)`, `distanceMm:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a subscribe operation results in a service discovery. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceLost](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`peerHandle:` ` [PeerHandle](../android/net/wifi/aware/PeerHandle.md)`, `reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the discovered service is not available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionConfigFailed](../android/net/wifi/aware/DiscoverySessionCallback.md))`()` Called when a publish or subscribe discovery session cannot be created: [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md))or [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md)), or when a configuration update fails: [PublishDiscoverySession.updatePublish(PublishConfig)](../android/net/wifi/aware/PublishDiscoverySession.md))or [SubscribeDiscoverySession.updateSubscribe(SubscribeConfig)](../android/net/wifi/aware/SubscribeDiscoverySession.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionConfigUpdated](../android/net/wifi/aware/DiscoverySessionCallback.md))`()` Called when a publish or subscribe discovery session configuration update request succeeds. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionTerminated](../android/net/wifi/aware/DiscoverySessionCallback.md))`()` Called when a discovery session (publish or subscribe) terminates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSubscribeStarted](../android/net/wifi/aware/DiscoverySessionCallback.md))`(`session:` ` [SubscribeDiscoverySession](../android/net/wifi/aware/SubscribeDiscoverySession.md)`)` Called when a subscribe operation is started successfully in response to a [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md))operation. |

## Public constructors

### DiscoverySessionCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DiscoverySessionCallback()
```

## Public methods

### onBootstrappingFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBootstrappingFailed(peerHandle: PeerHandle): Unit
```

Callback indicating that a Bootstrapping method negotiation failed.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md):The bootstrapping peer handle This value cannot be`null`. |

### onBootstrappingSucceeded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBootstrappingSucceeded(
    peerHandle: PeerHandle, 
    method: Int
): Unit
```

Callback indicating that a Bootstrapping method negotiation succeeded. The follow-up out-of-band bootstrapping can start

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md):The bootstrapping peer handle This value cannot be`null`. |
| `method` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bootstrapping method accept by the peer Value is either`0`or a combination of [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC](../android/net/wifi/aware/AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY](../android/net/wifi/aware/AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY](../android/net/wifi/aware/AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY](../android/net/wifi/aware/AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG](../android/net/wifi/aware/AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD](../android/net/wifi/aware/AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD](../android/net/wifi/aware/AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN](../android/net/wifi/aware/AwarePairingConfig.md), and [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER](../android/net/wifi/aware/AwarePairingConfig.md) |

### onMessageReceived

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMessageReceived(
    peerHandle: PeerHandle!, 
    message: ByteArray!
): Unit
```

Called when a message is received from a discovery session peer - in response to the peer's[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md)!:An opaque handle to the peer matching our discovery operation. |
| `message` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A byte array containing the message. |

### onMessageSendFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMessageSendFailed(messageId: Int): Unit
```

Called when message transmission initiated with[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))fails. E.g. when no ACK is received from the peer.

Note that either this callback or [DiscoverySessionCallback.onMessageSendSucceeded(int)](../android/net/wifi/aware/DiscoverySessionCallback.md))will be received - never both.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `messageId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The arbitrary message ID specified when sending the message. |

### onMessageSendSucceeded

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMessageSendSucceeded(messageId: Int): Unit
```

Called in response to[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))when a message is transmitted successfully - i.e. when it was received successfully by the peer (corresponds to an ACK being received).

Note that either this callback or [DiscoverySessionCallback.onMessageSendFailed(int)](../android/net/wifi/aware/DiscoverySessionCallback.md))will be received - never both.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `messageId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The arbitrary message ID specified when sending the message. |

### onPairingSetupFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPairingSetupFailed(peerHandle: PeerHandle): Unit
```

Callback indicating that a pairing setup process failed.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md):The pairing peer handle. This value cannot be`null`. |

### onPairingSetupRequestReceived

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPairingSetupRequestReceived(
    peerHandle: PeerHandle, 
    requestId: Int
): Unit
```

Callback indicating that a pairing request is received from peer.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md):The peer's handle where the request is from This value cannot be`null`. |
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the Aware pairing session |

### onPairingSetupSucceeded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPairingSetupSucceeded(
    peerHandle: PeerHandle, 
    alias: String
): Unit
```

Callback indicating that a pairing setup process succeeded.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md):The pairing peer handle. This value cannot be`null`. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This is the paired device alias set by the caller. [DiscoverySession.initiatePairingRequest(PeerHandle, String, int, String)](../android/net/wifi/aware/DiscoverySession.md))or [DiscoverySession.acceptPairingRequest(int, PeerHandle, String, int, String)](../android/net/wifi/aware/DiscoverySession.md))This value cannot be`null`. |

### onPairingVerificationFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPairingVerificationFailed(peerHandle: PeerHandle): Unit
```

Callback indicating that a pairing verification process failed.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md):The pairing peer handle This value cannot be`null`. |

### onPairingVerificationSucceed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPairingVerificationSucceed(
    peerHandle: PeerHandle, 
    alias: String
): Unit
```

Callback indicating that a pairing verification process succeeded.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md):The pairing peer handle This value cannot be`null`. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This is the paired device alias set by the caller. [DiscoverySession.initiatePairingRequest(PeerHandle, String, int, String)](../android/net/wifi/aware/DiscoverySession.md))or [DiscoverySession.acceptPairingRequest(int, PeerHandle, String, int, String)](../android/net/wifi/aware/DiscoverySession.md))This value cannot be`null`. |

### onPublishStarted

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPublishStarted(session: PublishDiscoverySession): Unit
```

Called when a publish operation is started successfully in response to a [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md))operation.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [PublishDiscoverySession](../android/net/wifi/aware/PublishDiscoverySession.md):The [PublishDiscoverySession](../android/net/wifi/aware/PublishDiscoverySession.md) used to control the discovery session. This value cannot be`null`. |

### onServiceDiscovered

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceDiscovered(
    peerHandle: PeerHandle!, 
    serviceSpecificInfo: ByteArray!, 
    matchFilter: MutableList<ByteArray!>!
): Unit
```

Called when a subscribe operation results in a service discovery.

Note that this method and[onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,byte[],java.util.List,int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList,%20kotlin.Int))may be called multiple times per service discovery.

Note: This method is superseded by [onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)](../android/net/wifi/aware/DiscoverySessionCallback.md))which returns more information. Note that both legacy and new callback will be triggered on discovery.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md)!:An opaque handle to the peer matching our discovery operation. |
| `serviceSpecificInfo` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The service specific information (arbitrary byte array) provided by the peer as part of its discovery configuration. |
| `matchFilter` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>!:The filter which resulted in this service discovery. For [PublishConfig.PUBLISH_TYPE_UNSOLICITED](../android/net/wifi/aware/PublishConfig.md), [SubscribeConfig.SUBSCRIBE_TYPE_PASSIVE](../android/net/wifi/aware/SubscribeConfig.md) discovery sessions this is the publisher's match filter. For [PublishConfig.PUBLISH_TYPE_SOLICITED](../android/net/wifi/aware/PublishConfig.md), [SubscribeConfig.SUBSCRIBE_TYPE_ACTIVE](../android/net/wifi/aware/SubscribeConfig.md) discovery sessions this is the subscriber's match filter. |
| --- | --- |

### onServiceDiscovered

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceDiscovered(info: ServiceDiscoveryInfo): Unit
```

Called when a subscribe operation results in a service discovery.

Note: This method supersedes[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))and provides additional information - including cipher suite type and security context of the peer. Both the legacy and the new callback will be triggered on discovery.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [ServiceDiscoveryInfo](../android/net/wifi/aware/ServiceDiscoveryInfo.md):A [ServiceDiscoveryInfo](../android/net/wifi/aware/ServiceDiscoveryInfo.md) structure containing information on the discovery session and the discovered peer. This value cannot be`null`. |

### onServiceDiscoveredWithinRange

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceDiscoveredWithinRange(
    peerHandle: PeerHandle!, 
    serviceSpecificInfo: ByteArray!, 
    matchFilter: MutableList<ByteArray!>!, 
    distanceMm: Int
): Unit
```

Called when a subscribe operation results in a service discovery. Called when a Subscribe service was configured with a range requirement [SubscribeConfig.Builder.setMinDistanceMm(int)](../android/net/wifi/aware/SubscribeConfig.Builder.md))and/or [SubscribeConfig.Builder.setMaxDistanceMm(int)](../android/net/wifi/aware/SubscribeConfig.Builder.md))and the Publish service was configured with [PublishConfig.Builder.setRangingEnabled(boolean)](../android/net/wifi/aware/PublishConfig.Builder.md)).

If either Publisher or Subscriber does not enable Ranging, or if Ranging is temporarily disabled by the underlying device, service discovery proceeds without ranging and the[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))is called.

Note that this method and[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))may be called multiple times per service discovery.

Note: This method is superseded by [onServiceDiscoveredWithinRange(android.net.wifi.aware.ServiceDiscoveryInfo,int)](../android/net/wifi/aware/DiscoverySessionCallback.md))which returns more information. Note that both legacy and new callback will be triggered on discovery.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md)!:An opaque handle to the peer matching our discovery operation. |
| `serviceSpecificInfo` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The service specific information (arbitrary byte array) provided by the peer as part of its discovery configuration. |
| `matchFilter` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>!:The filter which resulted in this service discovery. For [PublishConfig.PUBLISH_TYPE_UNSOLICITED](../android/net/wifi/aware/PublishConfig.md), [SubscribeConfig.SUBSCRIBE_TYPE_PASSIVE](../android/net/wifi/aware/SubscribeConfig.md) discovery sessions this is the publisher's match filter. For [PublishConfig.PUBLISH_TYPE_SOLICITED](../android/net/wifi/aware/PublishConfig.md), [SubscribeConfig.SUBSCRIBE_TYPE_ACTIVE](../android/net/wifi/aware/SubscribeConfig.md) discovery sessions this is the subscriber's match filter. |
| --- | --- |
| `distanceMm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The measured distance to the Publisher in mm. Note: the measured distance may be negative for very close devices. |

### onServiceDiscoveredWithinRange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceDiscoveredWithinRange(
    info: ServiceDiscoveryInfo, 
    distanceMm: Int
): Unit
```

Called when a subscribe operation results in a service discovery. Called when a Subscribe service was configured with a range requirement [SubscribeConfig.Builder.setMinDistanceMm(int)](../android/net/wifi/aware/SubscribeConfig.Builder.md))and/or [SubscribeConfig.Builder.setMaxDistanceMm(int)](../android/net/wifi/aware/SubscribeConfig.Builder.md))and the Publish service was configured with [PublishConfig.Builder.setRangingEnabled(boolean)](../android/net/wifi/aware/PublishConfig.Builder.md)).

If either Publisher or Subscriber does not enable Ranging, or if Ranging is temporarily disabled by the underlying device, service discovery proceeds without ranging and the[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))is called.

Note: This method supersedes[onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,byte[],java.util.List,int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList,%20kotlin.Int))and provides additional information - including cipher suite type and security context of the peer. Both the legacy and the new callback will be triggered on discovery.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [ServiceDiscoveryInfo](../android/net/wifi/aware/ServiceDiscoveryInfo.md):A [ServiceDiscoveryInfo](../android/net/wifi/aware/ServiceDiscoveryInfo.md) which indicate service config of the descovery sessions. This value cannot be`null`. |
| `distanceMm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The measured distance to the Publisher in mm. Note: the measured distance may be negative for very close devices. |

### onServiceLost

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceLost(
    peerHandle: PeerHandle, 
    reason: Int
): Unit
```

Called when the discovered service is not available. All further operations on this discovery session will fail. If the service is available again,[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))or[onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,byte[],java.util.List,int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList,%20kotlin.Int))will be called.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](../android/net/wifi/aware/PeerHandle.md):An opaque handle to the peer matching our discovery operation. This value cannot be`null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Discovered service lost reason code. One of [WifiAwareManager.WIFI_AWARE_DISCOVERY_LOST_REASON_PEER_NOT_VISIBLE](../android/net/wifi/aware/WifiAwareManager.md), [android.net.wifi.aware.WifiAwareManager#WIFI_AWARE_DISCOVERY_LOST_REASON_UNKNOWN](../android/net/wifi/aware/WifiAwareManager.md)} |

### onSessionConfigFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSessionConfigFailed(): Unit
```

Called when a publish or subscribe discovery session cannot be created: [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md))or [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md)), or when a configuration update fails: [PublishDiscoverySession.updatePublish(PublishConfig)](../android/net/wifi/aware/PublishDiscoverySession.md))or [SubscribeDiscoverySession.updateSubscribe(SubscribeConfig)](../android/net/wifi/aware/SubscribeDiscoverySession.md)).

For discovery session updates failure leaves the session running with its previous configuration - the discovery session is not terminated. 

### onSessionConfigUpdated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSessionConfigUpdated(): Unit
```

Called when a publish or subscribe discovery session configuration update request succeeds. Called in response to [PublishDiscoverySession.updatePublish(PublishConfig)](../android/net/wifi/aware/PublishDiscoverySession.md))or [SubscribeDiscoverySession.updateSubscribe(SubscribeConfig)](../android/net/wifi/aware/SubscribeDiscoverySession.md)). 

### onSessionTerminated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSessionTerminated(): Unit
```

Called when a discovery session (publish or subscribe) terminates. Termination may be due to user-request (either directly through [DiscoverySession.close()](../android/net/wifi/aware/DiscoverySession.md))or application-specified expiration, e.g. [PublishConfig.Builder.setTtlSec(int)](../android/net/wifi/aware/PublishConfig.Builder.md))or [SubscribeConfig.Builder.setTtlSec(int)](../android/net/wifi/aware/SubscribeConfig.Builder.md))). 

### onSubscribeStarted

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSubscribeStarted(session: SubscribeDiscoverySession): Unit
```

Called when a subscribe operation is started successfully in response to a [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](../android/net/wifi/aware/WifiAwareSession.md))operation.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [SubscribeDiscoverySession](../android/net/wifi/aware/SubscribeDiscoverySession.md):The [SubscribeDiscoverySession](../android/net/wifi/aware/SubscribeDiscoverySession.md) used to control the discovery session. This value cannot be`null`. |
