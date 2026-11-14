# DiscoverySessionCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DiscoverySessionCallback

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/aware/DiscoverySessionCallback "View this page in Java") 

```
open class DiscoverySessionCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.aware.DiscoverySessionCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#) |

Base class for Aware session events callbacks. Should be extended by applications wanting notifications. The callbacks are set when a publish or subscribe session is created using [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))or [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#subscribe(android.net.wifi.aware.SubscribeConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler)).

A single callback is set at session creation - it cannot be replaced.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DiscoverySessionCallback](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#DiscoverySessionCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBootstrappingFailed](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onBootstrappingFailed(android.net.wifi.aware.PeerHandle))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)`)` Callback indicating that a Bootstrapping method negotiation failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBootstrappingSucceeded](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onBootstrappingSucceeded(android.net.wifi.aware.PeerHandle,%20kotlin.Int))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)`, `method:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback indicating that a Bootstrapping method negotiation succeeded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageReceived](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)!`, `message:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Called when a message is received from a discovery session peer - in response to the peer's[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageSendFailed](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageSendFailed(kotlin.Int))`(`messageId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when message transmission initiated with[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))fails. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageSendSucceeded](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageSendSucceeded(kotlin.Int))`(`messageId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called in response to[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))when a message is transmitted successfully - i. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingSetupFailed](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupFailed(android.net.wifi.aware.PeerHandle))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)`)` Callback indicating that a pairing setup process failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingSetupRequestReceived](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupRequestReceived(android.net.wifi.aware.PeerHandle,%20kotlin.Int))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)`, `requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback indicating that a pairing request is received from peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingSetupSucceeded](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupSucceeded(android.net.wifi.aware.PeerHandle,%20kotlin.String))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)`, `alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Callback indicating that a pairing setup process succeeded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingVerificationFailed](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingVerificationFailed(android.net.wifi.aware.PeerHandle))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)`)` Callback indicating that a pairing verification process failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPairingVerificationSucceed](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingVerificationSucceed(android.net.wifi.aware.PeerHandle,%20kotlin.String))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)`, `alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Callback indicating that a pairing verification process succeeded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPublishStarted](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPublishStarted(android.net.wifi.aware.PublishDiscoverySession))`(`session:` ` [PublishDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession)`)` Called when a publish operation is started successfully in response to a [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDiscovered](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)!`, `serviceSpecificInfo:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `matchFilter:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>!`)` Called when a subscribe operation results in a service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDiscovered](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo))`(`info:` ` [ServiceDiscoveryInfo](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ServiceDiscoveryInfo)`)` Called when a subscribe operation results in a service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDiscoveredWithinRange](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList,%20kotlin.Int))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)!`, `serviceSpecificInfo:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `matchFilter:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>!`, `distanceMm:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a subscribe operation results in a service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceDiscoveredWithinRange](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscoveredWithinRange(android.net.wifi.aware.ServiceDiscoveryInfo,%20kotlin.Int))`(`info:` ` [ServiceDiscoveryInfo](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ServiceDiscoveryInfo)`, `distanceMm:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a subscribe operation results in a service discovery. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceLost](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceLost(android.net.wifi.aware.PeerHandle,%20kotlin.Int))`(`peerHandle:` ` [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)`, `reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the discovered service is not available. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionConfigFailed](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onSessionConfigFailed())`()` Called when a publish or subscribe discovery session cannot be created: [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))or [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#subscribe(android.net.wifi.aware.SubscribeConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler)), or when a configuration update fails: [PublishDiscoverySession.updatePublish(PublishConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession#updatePublish(android.net.wifi.aware.PublishConfig))or [SubscribeDiscoverySession.updateSubscribe(SubscribeConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession#updateSubscribe(android.net.wifi.aware.SubscribeConfig)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionConfigUpdated](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onSessionConfigUpdated())`()` Called when a publish or subscribe discovery session configuration update request succeeds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionTerminated](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onSessionTerminated())`()` Called when a discovery session (publish or subscribe) terminates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSubscribeStarted](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onSubscribeStarted(android.net.wifi.aware.SubscribeDiscoverySession))`(`session:` ` [SubscribeDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession)`)` Called when a subscribe operation is started successfully in response to a [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#subscribe(android.net.wifi.aware.SubscribeConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))operation. |

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
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle):The bootstrapping peer handle This value cannot be`null`. |

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
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle):The bootstrapping peer handle This value cannot be`null`. |
| `method` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bootstrapping method accept by the peer Value is either`0`or a combination of [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN:kotlin.Int), and [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER:kotlin.Int) |

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
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)!:An opaque handle to the peer matching our discovery operation. |
| `message` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A byte array containing the message. |

### onMessageSendFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMessageSendFailed(messageId: Int): Unit
```

Called when message transmission initiated with[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))fails. E.g. when no ACK is received from the peer.

Note that either this callback or [DiscoverySessionCallback.onMessageSendSucceeded(int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageSendSucceeded(kotlin.Int))will be received - never both.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `messageId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The arbitrary message ID specified when sending the message. |

### onMessageSendSucceeded

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMessageSendSucceeded(messageId: Int): Unit
```

Called in response to[DiscoverySession.sendMessage(PeerHandle, int, byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray))when a message is transmitted successfully - i.e. when it was received successfully by the peer (corresponds to an ACK being received).

Note that either this callback or [DiscoverySessionCallback.onMessageSendFailed(int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageSendFailed(kotlin.Int))will be received - never both.

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
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle):The pairing peer handle. This value cannot be`null`. |

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
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle):The peer's handle where the request is from This value cannot be`null`. |
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
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle):The pairing peer handle. This value cannot be`null`. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This is the paired device alias set by the caller. [DiscoverySession.initiatePairingRequest(PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiatePairingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String))or [DiscoverySession.acceptPairingRequest(int, PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#acceptPairingRequest(kotlin.Int,%20android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String))This value cannot be`null`. |

### onPairingVerificationFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPairingVerificationFailed(peerHandle: PeerHandle): Unit
```

Callback indicating that a pairing verification process failed.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle):The pairing peer handle This value cannot be`null`. |

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
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle):The pairing peer handle This value cannot be`null`. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This is the paired device alias set by the caller. [DiscoverySession.initiatePairingRequest(PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiatePairingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String))or [DiscoverySession.acceptPairingRequest(int, PeerHandle, String, int, String)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#acceptPairingRequest(kotlin.Int,%20android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String))This value cannot be`null`. |

### onPublishStarted

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPublishStarted(session: PublishDiscoverySession): Unit
```

Called when a publish operation is started successfully in response to a [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))operation.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [PublishDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession):The [PublishDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession) used to control the discovery session. This value cannot be`null`. |

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

Note: This method is superseded by [onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo))which returns more information. Note that both legacy and new callback will be triggered on discovery.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)!:An opaque handle to the peer matching our discovery operation. |
| `serviceSpecificInfo` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The service specific information (arbitrary byte array) provided by the peer as part of its discovery configuration. |
| `matchFilter` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>!:The filter which resulted in this service discovery. For [PublishConfig.PUBLISH_TYPE_UNSOLICITED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#PUBLISH_TYPE_UNSOLICITED:kotlin.Int), [SubscribeConfig.SUBSCRIBE_TYPE_PASSIVE](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig#SUBSCRIBE_TYPE_PASSIVE:kotlin.Int) discovery sessions this is the publisher's match filter. For [PublishConfig.PUBLISH_TYPE_SOLICITED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#PUBLISH_TYPE_SOLICITED:kotlin.Int), [SubscribeConfig.SUBSCRIBE_TYPE_ACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig#SUBSCRIBE_TYPE_ACTIVE:kotlin.Int) discovery sessions this is the subscriber's match filter. |

### onServiceDiscovered

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceDiscovered(info: ServiceDiscoveryInfo): Unit
```

Called when a subscribe operation results in a service discovery.

Note: This method supersedes[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))and provides additional information - including cipher suite type and security context of the peer. Both the legacy and the new callback will be triggered on discovery.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [ServiceDiscoveryInfo](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ServiceDiscoveryInfo):A [ServiceDiscoveryInfo](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ServiceDiscoveryInfo) structure containing information on the discovery session and the discovered peer. This value cannot be`null`. |

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

Called when a subscribe operation results in a service discovery. Called when a Subscribe service was configured with a range requirement [SubscribeConfig.Builder.setMinDistanceMm(int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setMinDistanceMm(kotlin.Int))and/or [SubscribeConfig.Builder.setMaxDistanceMm(int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setMaxDistanceMm(kotlin.Int))and the Publish service was configured with [PublishConfig.Builder.setRangingEnabled(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setRangingEnabled(kotlin.Boolean)).

If either Publisher or Subscriber does not enable Ranging, or if Ranging is temporarily disabled by the underlying device, service discovery proceeds without ranging and the[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))is called.

Note that this method and[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))may be called multiple times per service discovery.

Note: This method is superseded by [onServiceDiscoveredWithinRange(android.net.wifi.aware.ServiceDiscoveryInfo,int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscoveredWithinRange(android.net.wifi.aware.ServiceDiscoveryInfo,%20kotlin.Int))which returns more information. Note that both legacy and new callback will be triggered on discovery.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)!:An opaque handle to the peer matching our discovery operation. |
| `serviceSpecificInfo` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The service specific information (arbitrary byte array) provided by the peer as part of its discovery configuration. |
| `matchFilter` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>!:The filter which resulted in this service discovery. For [PublishConfig.PUBLISH_TYPE_UNSOLICITED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#PUBLISH_TYPE_UNSOLICITED:kotlin.Int), [SubscribeConfig.SUBSCRIBE_TYPE_PASSIVE](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig#SUBSCRIBE_TYPE_PASSIVE:kotlin.Int) discovery sessions this is the publisher's match filter. For [PublishConfig.PUBLISH_TYPE_SOLICITED](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig#PUBLISH_TYPE_SOLICITED:kotlin.Int), [SubscribeConfig.SUBSCRIBE_TYPE_ACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig#SUBSCRIBE_TYPE_ACTIVE:kotlin.Int) discovery sessions this is the subscriber's match filter. |
| `distanceMm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The measured distance to the Publisher in mm. Note: the measured distance may be negative for very close devices. |

### onServiceDiscoveredWithinRange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceDiscoveredWithinRange(
    info: ServiceDiscoveryInfo, 
    distanceMm: Int
): Unit
```

Called when a subscribe operation results in a service discovery. Called when a Subscribe service was configured with a range requirement [SubscribeConfig.Builder.setMinDistanceMm(int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setMinDistanceMm(kotlin.Int))and/or [SubscribeConfig.Builder.setMaxDistanceMm(int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setMaxDistanceMm(kotlin.Int))and the Publish service was configured with [PublishConfig.Builder.setRangingEnabled(boolean)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setRangingEnabled(kotlin.Boolean)).

If either Publisher or Subscriber does not enable Ranging, or if Ranging is temporarily disabled by the underlying device, service discovery proceeds without ranging and the[onServiceDiscovered(android.net.wifi.aware.PeerHandle,byte[],java.util.List)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList))is called.

Note: This method supersedes[onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,byte[],java.util.List,int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscoveredWithinRange(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList,%20kotlin.Int))and provides additional information - including cipher suite type and security context of the peer. Both the legacy and the new callback will be triggered on discovery.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [ServiceDiscoveryInfo](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ServiceDiscoveryInfo):A [ServiceDiscoveryInfo](https://developer.android.com/reference/kotlin/android/net/wifi/aware/ServiceDiscoveryInfo) which indicate service config of the descovery sessions. This value cannot be`null`. |
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
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle):An opaque handle to the peer matching our discovery operation. This value cannot be`null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Discovered service lost reason code. One of [WifiAwareManager.WIFI_AWARE_DISCOVERY_LOST_REASON_PEER_NOT_VISIBLE](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DISCOVERY_LOST_REASON_PEER_NOT_VISIBLE:kotlin.Int), [android.net.wifi.aware.WifiAwareManager#WIFI_AWARE_DISCOVERY_LOST_REASON_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DISCOVERY_LOST_REASON_UNKNOWN:kotlin.Int)} |

### onSessionConfigFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSessionConfigFailed(): Unit
```

Called when a publish or subscribe discovery session cannot be created: [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))or [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#subscribe(android.net.wifi.aware.SubscribeConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler)), or when a configuration update fails: [PublishDiscoverySession.updatePublish(PublishConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession#updatePublish(android.net.wifi.aware.PublishConfig))or [SubscribeDiscoverySession.updateSubscribe(SubscribeConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession#updateSubscribe(android.net.wifi.aware.SubscribeConfig)).

For discovery session updates failure leaves the session running with its previous configuration - the discovery session is not terminated. 

### onSessionConfigUpdated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSessionConfigUpdated(): Unit
```

Called when a publish or subscribe discovery session configuration update request succeeds. Called in response to [PublishDiscoverySession.updatePublish(PublishConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession#updatePublish(android.net.wifi.aware.PublishConfig))or [SubscribeDiscoverySession.updateSubscribe(SubscribeConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession#updateSubscribe(android.net.wifi.aware.SubscribeConfig)). 

### onSessionTerminated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSessionTerminated(): Unit
```

Called when a discovery session (publish or subscribe) terminates. Termination may be due to user-request (either directly through [DiscoverySession.close()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#close())or application-specified expiration, e.g. [PublishConfig.Builder.setTtlSec(int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setTtlSec(kotlin.Int))or [SubscribeConfig.Builder.setTtlSec(int)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setTtlSec(kotlin.Int))). 

### onSubscribeStarted

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSubscribeStarted(session: SubscribeDiscoverySession): Unit
```

Called when a subscribe operation is started successfully in response to a [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback,](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#subscribe(android.net.wifi.aware.SubscribeConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))operation.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [SubscribeDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession):The [SubscribeDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession) used to control the discovery session. This value cannot be`null`. |
