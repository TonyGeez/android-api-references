Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsRcsManager

```
open class ImsRcsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.ImsRcsManager](ImsRcsManager.md) |

Manager for interfacing with the framework RCS services, including the User Capability Exchange (UCE) service, as well as managing user settings. Use getImsRcsManager to create an instance of this manager. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String` feature which can be detected using hasSystemFeature.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#ACTION_SHOW_CAPABILITY_DISCOVERY_OPT_IN:kotlin.String` Activity Action: Show the opt-in dialog for enabling or disabling RCS contact discovery using User Capability Exchange (UCE), which enables a service that periodically shares the phone numbers of all of the contacts in the user's address book with the carrier to refresh the RCS capabilities associated with those contacts as the local cache becomes stale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_NONE:kotlin.Int` Undefined capability type for initialization |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_OPTIONS_UCE:kotlin.Int` This carrier supports User Capability Exchange using SIP OPTIONS as defined by the framework. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRcsManager#CAPABILITY_TYPE_PRESENCE_UCE:kotlin.Int` This carrier supports User Capability Exchange using a presence server as defined by the framework. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getRegistrationState Gets the registration state of the IMS service. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getRegistrationTransportType Gets the Transport Type associated with the current IMS registration. |
| open [RcsUceAdapter](RcsUceAdapter.md) | getUceAdapter <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerImsRegistrationCallback Registers a `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback` with the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerImsStateCallback Register a new callback, which is used to notify the registrant of changes to the state of the underlying IMS service that is attached to telephony to implement IMS functionality. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterImsRegistrationCallback Removes an existing `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterImsStateCallback Unregisters a previously registered callback. |

## Constants

### ACTION_SHOW_CAPABILITY_DISCOVERY_OPT_IN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_CAPABILITY_DISCOVERY_OPT_IN: String
```

Activity Action: Show the opt-in dialog for enabling or disabling RCS contact discovery using User Capability Exchange (UCE), which enables a service that periodically shares the phone numbers of all of the contacts in the user's address book with the carrier to refresh the RCS capabilities associated with those contacts as the local cache becomes stale.

An application that depends on RCS contact discovery being enabled must send this intent using startActivity to ask the user to opt-in for contacts upload for capability exchange if it is currently disabled. Whether or not RCS contact discovery has been enabled by the user can be queried using isUceSettingEnabled.

This intent will always be handled by the system, however the application should only send this Intent if the carrier supports bulk RCS contact exchange, which will be true if either key `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.Ims.html#KEY_RCS_BULK_CAPABILITY_EXCHANGE_BOOL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_USE_RCS_PRESENCE_BOOL:kotlin.String` is set to true. Otherwise, the RCS contact discovery opt-in dialog will not be shown.

Input: A mandatory `https://developer.android.com/reference/kotlin/android/provider/Settings.html#EXTRA_SUB_ID:kotlin.String` extra containing the subscription that the setting will be be shown for.

Output: Nothing

 Value: "android.telephony.ims.action.SHOW_CAPABILITY_DISCOVERY_OPT_IN"

**See Also**

- RcsUceAdapter

### CAPABILITY_TYPE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_TYPE_NONE: Int
```

Undefined capability type for initialization

 Value: 0

### CAPABILITY_TYPE_OPTIONS_UCE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_TYPE_OPTIONS_UCE: Int
```

This carrier supports User Capability Exchange using SIP OPTIONS as defined by the framework. If set, the RcsFeature should support capability exchange using SIP OPTIONS. If not set, this RcsFeature should not service capability requests.

 Value: 1

### CAPABILITY_TYPE_PRESENCE_UCE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_TYPE_PRESENCE_UCE: Int
```

This carrier supports User Capability Exchange using a presence server as defined by the framework. If set, the RcsFeature should support capability exchange using a presence server. If not set, this RcsFeature should not publish capabilities or service capability requests using presence.

 Value: 2

## Public methods

### getRegistrationState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRegistrationState(
    executor: Executor, 
    stateCallback: Consumer<Int!>
): Unit
```

Gets the registration state of the IMS service. Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will be used to call the IMS registration state callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `stateCallback` | [Consumer](../java.util.function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: A callback called on the supplied `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will contain the registration state of the IMS service, which will be one of the following: `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_NOT_REGISTERED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERING:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERED:kotlin.Int`. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_NOT_REGISTERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String`. |

### getRegistrationTransportType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRegistrationTransportType(
    executor: Executor, 
    transportTypeCallback: Consumer<Int!>
): Unit
```

Gets the Transport Type associated with the current IMS registration. Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will be used to call the transportTypeCallback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `transportTypeCallback` | [Consumer](../java.util.function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: The transport type associated with the current IMS registration. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.html#TRANSPORT_TYPE_WWAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.html#TRANSPORT_TYPE_WLAN:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String`. |

### getUceAdapter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUceAdapter(): RcsUceAdapter
```

| Return ||
|---|---|
| RcsUceAdapter | A RcsUceAdapter used for User Capability Exchange (UCE) operations for this subscription. This value cannot be `null`. |

### registerImsRegistrationCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerImsRegistrationCallback(
    executor: Executor, 
    c: RegistrationManager.RegistrationCallback
): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback` with the system. When the callback is registered, it will initiate the callback c to be called with the current registration state. Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor the callback events should be run on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `c` | [RegistrationManager.RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md): The `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback` to be added. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.telephony.ims.ImsException` | if the subscription associated with this callback is valid, but the `ImsService` associated with the subscription is not available. This can happen if the service crashed, for example. See getCode for a more detailed reason. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String`. |

**See Also**

- unregisterImsRegistrationCallback

### registerImsStateCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerImsStateCallback(
    executor: Executor, 
    callback: ImsStateCallback
): Unit
```

Register a new callback, which is used to notify the registrant of changes to the state of the underlying IMS service that is attached to telephony to implement IMS functionality. If the manager is created for the `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#DEFAULT_SUBSCRIPTION_ID:kotlin.Int`, this throws an ImsException.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or android.Manifest.permission.ACCESS_RCS_USER_CAPABILITY_EXCHANGE

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): the Executor that will be used to call the ImsStateCallback. This value cannot be `null`. |
| `callback` | [ImsStateCallback](ImsStateCallback.md): The callback instance being registered. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.telephony.ims.ImsException` | in the case that the callback can not be registered. See getCode for more information on when this is called. |

### unregisterImsRegistrationCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterImsRegistrationCallback(c: RegistrationManager.RegistrationCallback): Unit
```

Removes an existing `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback`. When the subscription associated with this callback is removed (SIM removed, ESIM swap, etc...), this callback will automatically be removed. If this method is called for an inactive subscription, it will result in a no-op. Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `c` | [RegistrationManager.RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md): The `https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback` to be removed. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener.html#`
- registerImsRegistrationCallback

### unregisterImsStateCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterImsStateCallback(callback: ImsStateCallback): Unit
```

Unregisters a previously registered callback.

| Parameters ||
|---|---|
| `callback` | [ImsStateCallback](ImsStateCallback.md): The callback instance to be unregistered. This value cannot be `null`. |
