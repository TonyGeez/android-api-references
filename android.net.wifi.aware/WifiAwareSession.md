Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiAwareSession

```
open class WifiAwareSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.WifiAwareSession](WifiAwareSession.md) |

This class represents a Wi-Fi Aware session - an attachment to the Wi-Fi Aware service through which the app can execute discovery operations.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Destroy the Wi-Fi Aware service session and, if no other applications are attached to Aware, also disable Aware. |
| open [NetworkSpecifier](../android.net/NetworkSpecifier.md)! | createNetworkSpecifierOpen Create a setNetworkSpecifier for an unencrypted WiFi Aware connection (link) to the specified peer. |
| open [NetworkSpecifier](../android.net/NetworkSpecifier.md)! | createNetworkSpecifierPassphrase Create a setNetworkSpecifier for an encrypted WiFi Aware connection (link) to the specified peer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | publish Issue a request to the Aware service to create a new Aware publish discovery session, using the specified `publishConfig` configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | subscribe Issue a request to the Aware service to create a new Aware subscribe discovery session, using the specified `subscribeConfig` configuration. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Destroy the Wi-Fi Aware service session and, if no other applications are attached to Aware, also disable Aware. This method destroys all outstanding operations - i.e. all publish and subscribes are terminated, and any outstanding data-links are shut-down. However, it is good practice to destroy these discovery sessions and connections explicitly before a session-wide destroy.

An application may re-attach after a destroy using attach .

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### createNetworkSpecifierOpen

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNetworkSpecifierOpen(
    role: Int, 
    peer: ByteArray
): NetworkSpecifier!
```

**Deprecated:** *Please use in-band data-path setup, refer to `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder`, publish and subscribe*

Create a setNetworkSpecifier for an unencrypted WiFi Aware connection (link) to the specified peer. The addTransportType should be set to `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#TRANSPORT_WIFI_AWARE:kotlin.Int`.

This API is targeted for applications which can obtain the peer MAC address using OOB (out-of-band) discovery. Aware discovery does not provide the MAC address of the peer - when using Aware discovery use the alternative network specifier method - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder`.

To set up an encrypted link use the createNetworkSpecifierPassphrase API.

| Parameters ||
|---|---|
| `role` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The role of this device: `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_INITIATOR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_RESPONDER:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_INITIATOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_RESPONDER:kotlin.Int` |
| `peer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The MAC address of the peer's Aware discovery interface. On a RESPONDER this value is used to gate the acceptance of a connection request from only that peer. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#!` | A `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#` to be used to construct setNetworkSpecifier to pass to requestNetwork \[or other varieties of that API\]. |

### createNetworkSpecifierPassphrase

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNetworkSpecifierPassphrase(
    role: Int, 
    peer: ByteArray, 
    passphrase: String
): NetworkSpecifier!
```

**Deprecated:** *Please use in-band data-path setup, refer to `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder`, publish and subscribe*

Create a setNetworkSpecifier for an encrypted WiFi Aware connection (link) to the specified peer. The addTransportType should be set to `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#TRANSPORT_WIFI_AWARE:kotlin.Int`.

This API is targeted for applications which can obtain the peer MAC address using OOB (out-of-band) discovery. Aware discovery does not provide the MAC address of the peer - when using Aware discovery use the alternative network specifier method - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder`.

| Parameters ||
|---|---|
| `role` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The role of this device: `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_INITIATOR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_RESPONDER:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_INITIATOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager#WIFI_AWARE_DATA_PATH_ROLE_RESPONDER:kotlin.Int` |
| `peer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The MAC address of the peer's Aware discovery interface. On a RESPONDER this value is used to gate the acceptance of a connection request from only that peer. This value cannot be `null`. |
| `passphrase` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The passphrase to be used to encrypt the link. The PMK is generated from the passphrase. Use createNetworkSpecifierOpen to specify an open (unencrypted) link. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#!` | A `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#` to be used to construct setNetworkSpecifier to pass to requestNetwork \[or other varieties of that API\]. |

### publish

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun publish(
    publishConfig: PublishConfig, 
    callback: DiscoverySessionCallback, 
    handler: Handler?
): Unit
```

Issue a request to the Aware service to create a new Aware publish discovery session, using the specified `publishConfig` configuration. The results of the publish operation are routed to the callbacks of DiscoverySessionCallback:

- onPublishStarted is called when the publish session is created and provides a handle to the session. Further operations on the publish session can be executed on that object.
- onSessionConfigFailed is called if the publish operation failed.

<br />

Other results of the publish session operations will also be routed to callbacks on the `callback` object. The resulting publish session can be modified using updatePublish.

The total count of currently available Wi-Fi Aware publish sessions is limited and is available via the getAvailablePublishSessionsCount method.

An application must use the close to terminate the publish discovery session once it isn't needed. This will free resources as well terminate any on-air transmissions.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `publishConfig` | [PublishConfig](PublishConfig.md): The PublishConfig specifying the configuration of the requested publish session. This value cannot be `null`. |
| `callback` | [DiscoverySessionCallback](DiscoverySessionCallback.md): A DiscoverySessionCallback derived object to be used for session event callbacks. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: The Handler on whose thread to execute the callbacks of the `callback` object. If a null is provided then the application's main thread will be used. |
| --- | --- |

### subscribe

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun subscribe(
    subscribeConfig: SubscribeConfig, 
    callback: DiscoverySessionCallback, 
    handler: Handler?
): Unit
```

Issue a request to the Aware service to create a new Aware subscribe discovery session, using the specified `subscribeConfig` configuration. The results of the subscribe operation are routed to the callbacks of DiscoverySessionCallback:

- onSubscribeStarted is called when the subscribe session is created and provides a handle to the session. Further operations on the subscribe session can be executed on that object.
- onSessionConfigFailed is called if the subscribe operation failed.

<br />

Other results of the subscribe session operations will also be routed to callbacks on the `callback` object. The resulting subscribe session can be modified using updateSubscribe.

The total count of currently available Wi-Fi Aware subscribe sessions is limited and is available via the getAvailableSubscribeSessionsCount method.

An application must use the close to terminate the subscribe discovery session once it isn't needed. This will free resources as well terminate any on-air transmissions.

If targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or later, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NEARBY_WIFI_DEVICES:kotlin.String` with android:usesPermissionFlags="neverForLocation". If the application does not declare android:usesPermissionFlags="neverForLocation", then it must also have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If targeting an earlier release than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the application must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `subscribeConfig` | [SubscribeConfig](SubscribeConfig.md): The SubscribeConfig specifying the configuration of the requested subscribe session. This value cannot be `null`. |
| `callback` | [DiscoverySessionCallback](DiscoverySessionCallback.md): A DiscoverySessionCallback derived object to be used for session event callbacks. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: The Handler on whose thread to execute the callbacks of the `callback` object. If a null is provided then the application's main thread will be used. |
| --- | --- |

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
