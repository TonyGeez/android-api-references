Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VcnManager

Kotlin | [Java](VcnManager.md)
| --- | --- |

```
open class VcnManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.vcn.VcnManager](VcnManager.md) |

VcnManager publishes APIs for applications to configure and manage Virtual Carrier Networks.

A VCN creates a virtualization layer to allow carriers to aggregate heterogeneous physical networks, unifying them as a single carrier network. This enables infrastructure flexibility on the part of carriers without impacting user connectivity, abstracting the physical network technologies as an implementation detail of their public network.

Each VCN virtualizes a carrier's network by building tunnels to a carrier's core network over carrier-managed physical links and supports a IP mobility layer to ensure seamless transitions between the underlying networks. Each VCN is configured based on a Subscription Group (see `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#`) and aggregates all networks that are brought up based on a profile or suggestion in the specified Subscription Group.

The VCN can be configured to expose one or more `https://developer.android.com/reference/kotlin/android/net/Network.html#`(s), each with different capabilities, allowing for APN virtualization.

If a tunnel fails to connect, or otherwise encounters a fatal error, the VCN will attempt to reestablish the connection. If the tunnel still has not reconnected after a system-determined timeout, the VCN Safe Mode (see below) will be entered.

The VCN Safe Mode ensures that users (and carriers) have a fallback to restore system connectivity to update profiles, diagnose issues, contact support, or perform other remediation tasks. In Safe Mode, the system will allow underlying cellular networks to be used as default. Additionally, during Safe Mode, the VCN will continue to retry the connections, and will automatically exit Safe Mode if all active tunnels connect successfully.

Apps targeting Android 15 or newer should check the existence of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` before querying the service. If the feature is absent, android.content.Context#getSystemService may return null. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback` VcnStatusCallback is the interface for Carrier apps to receive updates for their VCNs. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#VCN_ERROR_CODE_CONFIG_ERROR:kotlin.Int` Value indicating that an error with this Gateway Connection's configuration occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#VCN_ERROR_CODE_INTERNAL_ERROR:kotlin.Int` Value indicating that an internal failure occurred in this Gateway Connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#VCN_ERROR_CODE_NETWORK_ERROR:kotlin.Int` Value indicating that a Network error occurred with this Gateway Connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#VCN_STATUS_CODE_ACTIVE:kotlin.Int` Value indicating that the VCN for the subscription group is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#VCN_STATUS_CODE_INACTIVE:kotlin.Int` Value indicating that the VCN for the subscription group is inactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#VCN_STATUS_CODE_NOT_CONFIGURED:kotlin.Int` Value indicating that the VCN for the subscription group is not configured, or that the callback is not privileged for the subscription group. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#VCN_STATUS_CODE_SAFE_MODE:kotlin.Int` Value indicating that the VCN for the subscription group is in Safe Mode. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#clearVcnConfig(android.os.ParcelUuid)(subscriptionGroup: https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)` Clears the VCN configuration for a given subscription group. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ParcelUuid](../android.os/ParcelUuid.md)!\> | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#getConfiguredSubscriptionGroups()()` Retrieves the list of Subscription Groups for which a VCN Configuration has been set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#registerVcnStatusCallback(android.os.ParcelUuid,%20java.util.concurrent.Executor,%20android.net.vcn.VcnManager.VcnStatusCallback)(subscriptionGroup: https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback)` Registers the given callback to receive status updates for the specified subscription. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#setVcnConfig(android.os.ParcelUuid,%20android.net.vcn.VcnConfig)(subscriptionGroup: https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#, config: https://developer.android.com/reference/kotlin/android/net/vcn/VcnConfig)` Sets the VCN configuration for a given subscription group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#unregisterVcnStatusCallback(android.net.vcn.VcnManager.VcnStatusCallback)(callback: https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback)` Unregisters the given callback. |

## Constants

### VCN_ERROR_CODE_CONFIG_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VCN_ERROR_CODE_CONFIG_ERROR: Int
```

Value indicating that an error with this Gateway Connection's configuration occurred.

For example, this error code will be returned after authentication failures.

 Value: 1

### VCN_ERROR_CODE_INTERNAL_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VCN_ERROR_CODE_INTERNAL_ERROR: Int
```

Value indicating that an internal failure occurred in this Gateway Connection.

 Value: 0

### VCN_ERROR_CODE_NETWORK_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VCN_ERROR_CODE_NETWORK_ERROR: Int
```

Value indicating that a Network error occurred with this Gateway Connection.

For example, this error code will be returned if an underlying `https://developer.android.com/reference/kotlin/android/net/Network.html#` for this Gateway Connection is lost, or if an error occurs while resolving the connection endpoint address.

 Value: 2

### VCN_STATUS_CODE_ACTIVE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VCN_STATUS_CODE_ACTIVE: Int
```

Value indicating that the VCN for the subscription group is active.

A VCN is active if a `https://developer.android.com/reference/kotlin/android/net/vcn/VcnConfig` is present for the subscription, the provisioning package is privileged, and the VCN is not in Safe Mode. In other words, a VCN is considered active while it is connecting, fully connected, and disconnecting.

 Value: 2

### VCN_STATUS_CODE_INACTIVE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VCN_STATUS_CODE_INACTIVE: Int
```

Value indicating that the VCN for the subscription group is inactive.

A VCN is inactive if a `https://developer.android.com/reference/kotlin/android/net/vcn/VcnConfig` is present for the subscription group, but the provisioning package is not privileged.

 Value: 1

### VCN_STATUS_CODE_NOT_CONFIGURED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VCN_STATUS_CODE_NOT_CONFIGURED: Int
```

Value indicating that the VCN for the subscription group is not configured, or that the callback is not privileged for the subscription group.

 Value: 0

### VCN_STATUS_CODE_SAFE_MODE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VCN_STATUS_CODE_SAFE_MODE: Int
```

Value indicating that the VCN for the subscription group is in Safe Mode.

A VCN will be put into Safe Mode if any of the gateway connections were unable to establish a connection within a system-determined timeout (while underlying networks were available).

 Value: 3

## Public methods

### clearVcnConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearVcnConfig(subscriptionGroup: ParcelUuid): Unit
```

Clears the VCN configuration for a given subscription group.

An app that has carrier privileges for any of the subscriptions in the given group may clear a VCN configuration. This API is ONLY permitted for callers running as the primary user. Any active VCN associated with this configuration will be torn down. 
Requires `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()`

| Parameters ||
|---|---|
| `subscriptionGroup` | [ParcelUuid](../android.os/ParcelUuid.md): the subscription group that the configuration should be applied to. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the configuration failed to be cleared from disk. This may occur due to temporary disk errors, or more permanent conditions such as a full disk. |
| `java.lang.SecurityException` | if the caller does not have carrier privileges, is not the owner of the associated configuration, or is not running as the primary user |

### getConfiguredSubscriptionGroups

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfiguredSubscriptionGroups(): MutableList<ParcelUuid!>
```

Retrieves the list of Subscription Groups for which a VCN Configuration has been set.

The returned list will include only subscription groups for which an associated `https://developer.android.com/reference/kotlin/android/net/vcn/VcnConfig` exists, and the app is either:

- Carrier privileged for that subscription group, or
- Is the provisioning package of the config

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#!>` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is not running as the primary user |

### registerVcnStatusCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerVcnStatusCallback(
    subscriptionGroup: ParcelUuid, 
    executor: Executor, 
    callback: VcnManager.VcnStatusCallback
): Unit
```

Registers the given callback to receive status updates for the specified subscription.

Callbacks can be registered for a subscription before `https://developer.android.com/reference/kotlin/android/net/vcn/VcnConfig`s are set for it.

A `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback` may only be registered for one subscription at a time. `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback`s may be reused once unregistered.

A `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback` will only be invoked if the registering package has carrier privileges for the specified subscription at the time of invocation.

A `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback` is eligible to begin receiving callbacks once it is registered and there is a VCN active for its specified subscription group (this may happen after the callback is registered).

`https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback#onStatusChanged(kotlin.Int)` will be invoked on registration with the current status for the specified subscription group's VCN. If the registrant is not privileged for this subscription group, `https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#VCN_STATUS_CODE_NOT_CONFIGURED:kotlin.Int` will be returned.

| Parameters ||
|---|---|
| `subscriptionGroup` | [ParcelUuid](../android.os/ParcelUuid.md): The subscription group to match for callbacks. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` to be used for invoking callbacks. This value cannot be `null`. |
| `callback` | [VcnManager.VcnStatusCallback](../android/net/vcn/VcnManager.VcnStatusCallback.md): The VcnStatusCallback to be registered. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if callback is currently registered with VcnManager |

### setVcnConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVcnConfig(
    subscriptionGroup: ParcelUuid, 
    config: VcnConfig
): Unit
```

Sets the VCN configuration for a given subscription group.

An app that has carrier privileges for any of the subscriptions in the given group may set a VCN configuration. If a configuration already exists for the given subscription group, it will be overridden. Any active VCN(s) may be forced to restart to use the new configuration.

This API is ONLY permitted for callers running as the primary user. 
Requires `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()`

| Parameters ||
|---|---|
| `subscriptionGroup` | [ParcelUuid](../android.os/ParcelUuid.md): the subscription group that the configuration should be applied to. This value cannot be `null`. |
| `config` | [VcnConfig](VcnConfig.md): the configuration parameters for the VCN. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the configuration failed to be saved and persisted to disk. This may occur due to temporary disk errors, or more permanent conditions such as a full disk. |
| `java.lang.SecurityException` | if the caller does not have carrier privileges for the provided subscriptionGroup, or is not running as the primary user |

### unregisterVcnStatusCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterVcnStatusCallback(callback: VcnManager.VcnStatusCallback): Unit
```

Unregisters the given callback.

Once unregistered, the callback will stop receiving status updates for the subscription it was registered with.

| Parameters ||
|---|---|
| `callback` | [VcnManager.VcnStatusCallback](../android/net/vcn/VcnManager.VcnStatusCallback.md): The callback to be unregistered. This value cannot be `null`. |
