# ConnectivityDiagnosticsManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectivityDiagnosticsManager

Kotlin| [Java](../android/net/ConnectivityDiagnosticsManager.md) 
| --- | --- |

```
open class ConnectivityDiagnosticsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ConnectivityDiagnosticsManager](../android/net/ConnectivityDiagnosticsManager.md) |

Class that provides utilities for collecting network connectivity diagnostics information. Connectivity information is made available through triggerable diagnostics tools and by listening to System validations. Some diagnostics information may be permissions-restricted.

ConnectivityDiagnosticsManager is intended for use by applications offering network connectivity on a user device. These tools will provide several mechanisms for these applications to be alerted to network conditions as well as diagnose potential network issues themselves.

The primary responsibilities of this class are to:

- Allow permissioned applications to register and unregister callbacks for network event notifications
- Invoke callbacks for network event notifications, including:
 - Network validations
 - Data stalls
 - Connectivity reports from applications

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ConnectivityDiagnosticsCallback](../android/net/ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback.md) Abstract base class for Connectivity Diagnostics callbacks. |
| | [ConnectivityReport](../android/net/ConnectivityDiagnosticsManager.ConnectivityReport.md) Class that includes connectivity information for a specific Network at a specific time. |
| | [DataStallReport](../android/net/ConnectivityDiagnosticsManager.DataStallReport.md) Class that includes information for a suspected data stall on a specific Network |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerConnectivityDiagnosticsCallback](../android/net/ConnectivityDiagnosticsManager.md))`(`request:` ` [NetworkRequest](../android/net/NetworkRequest.md)`, `e:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback](../android/net/ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback.md)`)` Registers a ConnectivityDiagnosticsCallback with the System. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterConnectivityDiagnosticsCallback](../android/net/ConnectivityDiagnosticsManager.md))`(`callback:` ` [ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback](../android/net/ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback.md)`)` Unregisters a ConnectivityDiagnosticsCallback with the System. |

## Public methods

### registerConnectivityDiagnosticsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerConnectivityDiagnosticsCallback(
    request: NetworkRequest, 
    e: Executor, 
    callback: ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback
): Unit
```

Registers a ConnectivityDiagnosticsCallback with the System.

Only apps that offer network connectivity to the user should be registering callbacks. These are the only apps whose callbacks will be invoked by the system. Apps considered to meet these conditions include:

- Carrier apps with active subscriptions
- Active VPNs
- WiFi Suggesters

Callbacks registered by apps not meeting the above criteria will not be invoked.

If a registering app loses its relevant permissions, any callbacks it registered will silently stop receiving callbacks. Note that registering apps must also have location permissions to receive callbacks as some Networks may be location-bound (such as WiFi networks).

Each register() call**MUST**use a ConnectivityDiagnosticsCallback instance that is not currently registered. If a ConnectivityDiagnosticsCallback instance is registered with multiple NetworkRequests, an IllegalArgumentException will be thrown.

To avoid performance issues due to apps leaking callbacks, the system will limit the number of outstanding requests to 100 per app (identified by their UID), shared with callbacks in [ConnectivityManager](../android/net/ConnectivityManager.md). Registering a callback with this method will count toward this limit. If this limit is exceeded, an exception will be thrown. To avoid hitting this issue and to conserve resources, make sure to unregister the callbacks with [unregisterConnectivityDiagnosticsCallback](../android/net/ConnectivityDiagnosticsManager.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [NetworkRequest](../android/net/NetworkRequest.md):The NetworkRequest that will be used to match with Networks for which callbacks will be fired This value cannot be`null`. |
| `e` | [Executor](../java/util/concurrent/Executor.md):The Executor to be used for running the callback method invocations This value cannot be`null`. |
| `callback` | [ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback](../android/net/ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback.md):The ConnectivityDiagnosticsCallback that the caller wants registered with the System This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the same callback instance is registered with multiple NetworkRequests |
| `java.lang.RuntimeException` | if the app already has too many callbacks registered. |

### unregisterConnectivityDiagnosticsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterConnectivityDiagnosticsCallback(callback: ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback): Unit
```

Unregisters a ConnectivityDiagnosticsCallback with the System.

If the given callback is not currently registered with the System, this operation will be a no-op.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback](../android/net/ConnectivityDiagnosticsManager.ConnectivityDiagnosticsCallback.md):The ConnectivityDiagnosticsCallback to be unregistered from the System. This value cannot be`null`. |
