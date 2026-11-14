Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DiscoverySession

```
open class DiscoverySession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.aware.DiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#) |

| Known Direct Subclasses [PublishDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession), [SubscribeDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession) |---|---| | [PublishDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession) | A class representing a Aware publish session. | | [SubscribeDiscoverySession](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession) | A class representing a Aware subscribe session. | |

A class representing a single publish or subscribe Aware session. This object will not be created directly - only its child classes are available: `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession` and `https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession`. This class provides functionality common to both publish and subscribe discovery sessions:

- Sending messages: `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)` method.
- Creating a network-specifier when requesting a Aware connection using `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder`.

<br />

The `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#close()` method must be called to destroy discovery sessions once they are no longer needed.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#acceptPairingRequest(kotlin.Int,%20android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String)(requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle, peerDeviceAlias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cipherSuite: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Accept and respond to a Wi-Fi Aware Pairing setup request received from peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#close()()` Destroy the publish or subscribe session - free any resources, and stop transmitting packets on-air (for an active session) or listening for matches (for a passive session). |
| open [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#)! | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#createNetworkSpecifierOpen(android.net.wifi.aware.PeerHandle)(peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)` Create a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#setNetworkSpecifier(android.net.NetworkSpecifier)` for an unencrypted WiFi Aware connection (link) to the specified peer. |
| open [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#)! | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#createNetworkSpecifierPassphrase(android.net.wifi.aware.PeerHandle,%20kotlin.String)(peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle, passphrase: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Create a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#setNetworkSpecifier(android.net.NetworkSpecifier)` for an encrypted WiFi Aware connection (link) to the specified peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiateBootstrappingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.Int)(peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle, method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Defined as per Wi-Fi Aware specifications version 4. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiateBootstrappingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)(peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle, method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Defined as per Wi-Fi Aware specifications version 4. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#initiatePairingRequest(android.net.wifi.aware.PeerHandle,%20kotlin.String,%20kotlin.Int,%20kotlin.String)(peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle, peerDeviceAlias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cipherSuite: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Initiate a Wi-Fi Aware Pairing setup request to create a pairing with the target peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#rejectPairingRequest(kotlin.Int,%20android.net.wifi.aware.PeerHandle)(requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)` Reject a Wi-Fi Aware Pairing setup request received from peer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#releaseDataPath(android.net.wifi.aware.PeerHandle)(peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle)` Release the Aware data path to the specified peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)(peerHandle: https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle, messageId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?)` Sends a message to the specified destination. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public methods

### acceptPairingRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acceptPairingRequest(
    requestId: Int, 
    peerHandle: PeerHandle, 
    peerDeviceAlias: String, 
    cipherSuite: Int, 
    password: String?
): Unit
```

Accept and respond to a Wi-Fi Aware Pairing setup request received from peer. This is the response to the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupRequestReceived(android.net.wifi.aware.PeerHandle,%20kotlin.Int)` When the Aware Pairing setup is finished, both sides will receive `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupSucceeded(android.net.wifi.aware.PeerHandle,%20kotlin.String)`

| Parameters ||
|---|---|
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Id to identify the received pairing session, obtained by `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupRequestReceived(android.net.wifi.aware.PeerHandle,%20kotlin.Int)` |
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle for the pairing request. Must be a result of a `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)` events. This value cannot be `null`. |
| `peerDeviceAlias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The alias of paired device set by caller, will help caller to identify the paired device. This value cannot be `null`. |
| `cipherSuite` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The cipher suite to be used to encrypt the link. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256:kotlin.Int` |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The password is used for the pairing setup. If set to empty or null, opportunistic pairing will be used. |

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Destroy the publish or subscribe session - free any resources, and stop transmitting packets on-air (for an active session) or listening for matches (for a passive session). The session may not be used for any additional operations after its destruction.

This operation must be done on a session which is no longer needed. Otherwise system resources will continue to be utilized until the application exits. The only exception is a session for which we received a termination callback, `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onSessionTerminated()`.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### createNetworkSpecifierOpen

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNetworkSpecifierOpen(peerHandle: PeerHandle): NetworkSpecifier!
```

**Deprecated:** *Use the replacement `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder`.*

Create a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#setNetworkSpecifier(android.net.NetworkSpecifier)` for an unencrypted WiFi Aware connection (link) to the specified peer. The `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#addTransportType(kotlin.Int)` should be set to `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#TRANSPORT_WIFI_AWARE:kotlin.Int`.

This method should be used when setting up a connection with a peer discovered through Aware discovery or communication (in such scenarios the MAC address of the peer is shielded by an opaque peer ID handle). If an Aware connection is needed to a peer discovered using other OOB (out-of-band) mechanism then use the alternative `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#createNetworkSpecifierOpen(kotlin.Int,%20kotlin.ByteArray)` method - which uses the peer's MAC address.

Note: per the Wi-Fi Aware specification the roles are fixed - a Subscriber is an INITIATOR and a Publisher is a RESPONDER.

To set up an encrypted link use the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#createNetworkSpecifierPassphrase(android.net.wifi.aware.PeerHandle,%20kotlin.String)` API.

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle obtained through `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)`. On a RESPONDER this value is used to gate the acceptance of a connection request from only that peer. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#!` | A `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#` to be used to construct `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#setNetworkSpecifier(android.net.NetworkSpecifier)` to pass to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` \[or other varieties of that API\]. |

### createNetworkSpecifierPassphrase

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNetworkSpecifierPassphrase(
    peerHandle: PeerHandle, 
    passphrase: String
): NetworkSpecifier!
```

**Deprecated:** *Use the replacement `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder`.*

Create a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#setNetworkSpecifier(android.net.NetworkSpecifier)` for an encrypted WiFi Aware connection (link) to the specified peer. The `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#addTransportType(kotlin.Int)` should be set to `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#TRANSPORT_WIFI_AWARE:kotlin.Int`.

This method should be used when setting up a connection with a peer discovered through Aware discovery or communication (in such scenarios the MAC address of the peer is shielded by an opaque peer ID handle). If an Aware connection is needed to a peer discovered using other OOB (out-of-band) mechanism then use the alternative `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#createNetworkSpecifierPassphrase(kotlin.Int,%20kotlin.ByteArray,%20kotlin.String)` method - which uses the peer's MAC address.

Note: per the Wi-Fi Aware specification the roles are fixed - a Subscriber is an INITIATOR and a Publisher is a RESPONDER.

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle obtained through `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)`. On a RESPONDER this value is used to gate the acceptance of a connection request from only that peer. This value cannot be `null`. |
| `passphrase` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The passphrase to be used to encrypt the link. The PMK is generated from the passphrase. Use the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#createNetworkSpecifierOpen(android.net.wifi.aware.PeerHandle)` API to specify an open (unencrypted) link. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#!` | A `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#` to be used to construct `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#setNetworkSpecifier(android.net.NetworkSpecifier)` to pass to `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback)` \[or other varieties of that API\]. |

### initiateBootstrappingRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun initiateBootstrappingRequest(
    peerHandle: PeerHandle, 
    method: Int
): Unit
```

Defined as per Wi-Fi Aware specifications version 4.0 Section 7.6.4.1. Initiate a Wi-Fi Aware bootstrapping setup request to create a pairing with the target peer. The Aware bootstrapping request should be done in the context of a discovery session - after a publish/subscribe. `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)` event is received. The peer will check if the method can be fulfilled by `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig.Builder#setBootstrappingMethods(kotlin.Int)` When the Aware Bootstrapping setup finished, both side will receive `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onBootstrappingSucceeded(android.net.wifi.aware.PeerHandle,%20kotlin.Int)`

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle for the pairing request. Must be a result of an `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)` events. This value cannot be `null`. |
| `method` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the AwarePairingConfig#PAIRING_BOOTSTRAPPING_ values, should match one of the methods received from `https://developer.android.com/reference/kotlin/android/net/wifi/aware/ServiceDiscoveryInfo#getPairingConfig()` `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#getBootstrappingMethods()` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_SERVICE_MANAGED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_SKIPPED:kotlin.Int` |

### initiateBootstrappingRequest

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun initiateBootstrappingRequest(
    peerHandle: PeerHandle, 
    method: Int, 
    message: ByteArray
): Unit
```

Defined as per Wi-Fi Aware specifications version 4.0 Section 7.6.4.1. Initiate a Wi-Fi Aware bootstrapping setup request to create a pairing with the target peer. The Aware bootstrapping request should be done in the context of a discovery session - after a publish/subscribe `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)` event is received. The peer will check if the method can be fulfilled by `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig.Builder#setBootstrappingMethods(kotlin.Int)` When the Aware Bootstrapping setup finished, both side will receive `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onBootstrappingSucceeded(android.net.wifi.aware.PeerHandle,%20kotlin.Int)`

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle for the pairing request. Must be a result of an `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)` events. This value cannot be `null`. |
| `method` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the AwarePairingConfig#PAIRING_BOOTSTRAPPING_ values, should match one of the methods received from `https://developer.android.com/reference/kotlin/android/net/wifi/aware/ServiceDiscoveryInfo#getPairingConfig()` `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#getBootstrappingMethods()` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_SERVICE_MANAGED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_SKIPPED:kotlin.Int` |
| `message` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): An arbitrary byte array which can be sent as service info in Service Descriptor Extension attribute (SDEA) - see Wi-Fi Aware specification 9.5.4.2 for more details. Recommnaded to use `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#createTxtRecordTlvBuffer(kotlin.collections.MutableMap)` to create key-value message in DNS-SD format. This value cannot be `null`. |

### initiatePairingRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun initiatePairingRequest(
    peerHandle: PeerHandle, 
    peerDeviceAlias: String, 
    cipherSuite: Int, 
    password: String?
): Unit
```

Initiate a Wi-Fi Aware Pairing setup request to create a pairing with the target peer. The Aware pairing request should be done in the context of a discovery session - after a publish/subscribe `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)` event is received. The peer will get a callback indicating a message was received using `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupRequestReceived(android.net.wifi.aware.PeerHandle,%20kotlin.Int)`. When the Aware Pairing setup is finished, both sides will receive `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupSucceeded(android.net.wifi.aware.PeerHandle,%20kotlin.String)`

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle for the pairing request. Must be a result of a `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)` events. This value cannot be `null`. |
| `peerDeviceAlias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The alias of paired device set by caller, will help caller to identify the paired device. This value cannot be `null`. |
| `cipherSuite` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The cipher suite to be used to encrypt the link. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256:kotlin.Int` |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The password used for the pairing setup. If set to empty or null, opportunistic pairing will be used. |

### rejectPairingRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rejectPairingRequest(
    requestId: Int, 
    peerHandle: PeerHandle
): Unit
```

Reject a Wi-Fi Aware Pairing setup request received from peer. This is the response to the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupRequestReceived(android.net.wifi.aware.PeerHandle,%20kotlin.Int)`

| Parameters ||
|---|---|
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Id to identify the received pairing session, get by `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onPairingSetupRequestReceived(android.net.wifi.aware.PeerHandle,%20kotlin.Int)` |
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle for the pairing request. Must be a result of a `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.ServiceDiscoveryInfo)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)` events. This value cannot be `null`. |

### releaseDataPath

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun releaseDataPath(peerHandle: PeerHandle): Boolean
```

Release the Aware data path to the specified peer. The datapath will be disconnected if no other applications are requesting it. `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onDataPathDisconnected(android.net.wifi.aware.PeerHandle)` will be called when the datapath is disconnected.

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle is used in `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishDiscoverySession#acceptDataPathRequest(android.net.wifi.aware.PeerHandle,%20android.net.wifi.aware.AwareDataPathRequest)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeDiscoverySession#initiateDataPathRequest(android.net.wifi.aware.PeerHandle,%20android.net.wifi.aware.AwareDataPathRequest)` This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the data path is released successfully, false otherwise. |

### sendMessage

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendMessage(
    peerHandle: PeerHandle, 
    messageId: Int, 
    message: ByteArray?
): Unit
```

Sends a message to the specified destination. Aware messages are transmitted in the context of a discovery session - executed subsequent to a publish/subscribe `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList)` event.

Aware messages are not guaranteed delivery. Callbacks on `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback` indicate message was transmitted successfully, `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageSendSucceeded(kotlin.Int)`, or transmission failed (possibly after several retries) - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageSendFailed(kotlin.Int)`.

The peer will get a callback indicating a message was received using `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)`.

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle): The peer's handle for the message. Must be a result of an `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onServiceDiscovered(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray,%20kotlin.collections.MutableList)` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySessionCallback#onMessageReceived(android.net.wifi.aware.PeerHandle,%20kotlin.ByteArray)` events. This value cannot be `null`. |
| `messageId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An arbitrary integer used by the caller to identify the message. The same integer ID will be returned in the callbacks indicating message send success or failure. The `messageId` is not used internally by the Aware service - it can be arbitrary and non-unique. |
| `message` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: The message to be transmitted. This value may be `null`. |

## Protected methods

### finalize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
