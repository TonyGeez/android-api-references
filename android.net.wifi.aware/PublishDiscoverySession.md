Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PublishDiscoverySession

```
open class PublishDiscoverySession : DiscoverySession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.wifi.aware.DiscoverySession](DiscoverySession.md) ||
| | ↳ | [android.net.wifi.aware.PublishDiscoverySession](PublishDiscoverySession.md) |

A class representing a Aware publish session. Created when publish is called and a discovery session is created and returned in onPublishStarted. See baseline functionality of all discovery sessions in DiscoverySession. This object allows updating an existing/running publish discovery session using updatePublish.

## Summary

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | acceptDataPathRequest Accept a Wi-Fi Aware data path request to create a connection with the target peer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | rejectDataPathRequest Reject a Wi-Fi Aware data path request received from peer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | updatePublish Re-configure the currently active publish session. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class DiscoverySession |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | acceptPairingRequest Accept and respond to a Wi-Fi Aware Pairing setup request received from peer. This is the response to the onPairingSetupRequestReceived When the Aware Pairing setup is finished, both sides will receive onPairingSetupSucceeded <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | close Destroy the publish or subscribe session - free any resources, and stop transmitting packets on-air (for an active session) or listening for matches (for a passive session). The session may not be used for any additional operations after its destruction. This operation must be done on a session which is no longer needed. Otherwise system resources will continue to be utilized until the application exits. The only exception is a session for which we received a termination callback, onSessionTerminated. <br /> | | `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#!` | createNetworkSpecifierOpen Create a setNetworkSpecifier for an unencrypted WiFi Aware connection (link) to the specified peer. The addTransportType should be set to `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#TRANSPORT_WIFI_AWARE:kotlin.Int`. This method should be used when setting up a connection with a peer discovered through Aware discovery or communication (in such scenarios the MAC address of the peer is shielded by an opaque peer ID handle). If an Aware connection is needed to a peer discovered using other OOB (out-of-band) mechanism then use the alternative createNetworkSpecifierOpen method - which uses the peer's MAC address. Note: per the Wi-Fi Aware specification the roles are fixed - a Subscriber is an INITIATOR and a Publisher is a RESPONDER. To set up an encrypted link use the createNetworkSpecifierPassphrase API. <br /> | | `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#!` | createNetworkSpecifierPassphrase Create a setNetworkSpecifier for an encrypted WiFi Aware connection (link) to the specified peer. The addTransportType should be set to `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#TRANSPORT_WIFI_AWARE:kotlin.Int`. This method should be used when setting up a connection with a peer discovered through Aware discovery or communication (in such scenarios the MAC address of the peer is shielded by an opaque peer ID handle). If an Aware connection is needed to a peer discovered using other OOB (out-of-band) mechanism then use the alternative createNetworkSpecifierPassphrase method - which uses the peer's MAC address. Note: per the Wi-Fi Aware specification the roles are fixed - a Subscriber is an INITIATOR and a Publisher is a RESPONDER. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | initiateBootstrappingRequest Defined as per Wi-Fi Aware specifications version 4.0 Section 7.6.4.1. Initiate a Wi-Fi Aware bootstrapping setup request to create a pairing with the target peer. The Aware bootstrapping request should be done in the context of a discovery session - after a publish/subscribe. onServiceDiscovered event is received. The peer will check if the method can be fulfilled by setBootstrappingMethods When the Aware Bootstrapping setup finished, both side will receive onBootstrappingSucceeded <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | initiateBootstrappingRequest Defined as per Wi-Fi Aware specifications version 4.0 Section 7.6.4.1. Initiate a Wi-Fi Aware bootstrapping setup request to create a pairing with the target peer. The Aware bootstrapping request should be done in the context of a discovery session - after a publish/subscribe onServiceDiscovered event is received. The peer will check if the method can be fulfilled by setBootstrappingMethods When the Aware Bootstrapping setup finished, both side will receive onBootstrappingSucceeded <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | initiatePairingRequest Initiate a Wi-Fi Aware Pairing setup request to create a pairing with the target peer. The Aware pairing request should be done in the context of a discovery session - after a publish/subscribe onServiceDiscovered event is received. The peer will get a callback indicating a message was received using onPairingSetupRequestReceived. When the Aware Pairing setup is finished, both sides will receive onPairingSetupSucceeded <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | rejectPairingRequest Reject a Wi-Fi Aware Pairing setup request received from peer. This is the response to the onPairingSetupRequestReceived <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | releaseDataPath Release the Aware data path to the specified peer. The datapath will be disconnected if no other applications are requesting it. onDataPathDisconnected will be called when the datapath is disconnected. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | sendMessage Sends a message to the specified destination. Aware messages are transmitted in the context of a discovery session - executed subsequent to a publish/subscribe onServiceDiscovered event. Aware messages are not guaranteed delivery. Callbacks on DiscoverySessionCallback indicate message was transmitted successfully, onMessageSendSucceeded, or transmission failed (possibly after several retries) - onMessageSendFailed. The peer will get a callback indicating a message was received using onMessageReceived. <br /> | ||

## Public methods

### acceptDataPathRequest

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acceptDataPathRequest(
    peerHandle: PeerHandle, 
    request: AwareDataPathRequest
): Boolean
```

Accept a Wi-Fi Aware data path request to create a connection with the target peer. The Aware data path request should be done in the context of a discovery session - after a onDataPathRequestReceived event is received. When the Aware data path setup succeeds, both side will receive onDataPathConnected. Otherwise onDataPathRequestFailed will be called.

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](PeerHandle.md): The peer's handle for the data path request. This value cannot be `null`. |
| `request` | [AwareDataPathRequest](../android/net/wifi/aware/AwareDataPathRequest.md): The data path request. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if framework accept the data path request successfully and start negotiation, false otherwise. |

### rejectDataPathRequest

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rejectDataPathRequest(peerHandle: PeerHandle): Boolean
```

Reject a Wi-Fi Aware data path request received from peer. This is the response to the onDataPathRequestReceived

| Parameters ||
|---|---|
| `peerHandle` | [PeerHandle](PeerHandle.md): The peer's handle for the data path request. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the data path is rejected successfully, false otherwise. |

### updatePublish

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updatePublish(publishConfig: PublishConfig): Unit
```

Re-configure the currently active publish session. The DiscoverySessionCallback is not replaced - the same listener used at creation is still used. The results of the configuration are returned using DiscoverySessionCallback:

- onSessionConfigUpdated: configuration update succeeded.
- onSessionConfigFailed: configuration update failed. The publish discovery session is still running using its previous configuration (i.e. update failure does not terminate the session).

<br />

| Parameters ||
|---|---|
| `publishConfig` | [PublishConfig](PublishConfig.md): The new discovery publish session configuration (PublishConfig). This value cannot be `null`. |
