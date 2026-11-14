# RegistrationManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RegistrationManager

Kotlin| [Java](../android/telephony/ims/RegistrationManager.md) 
| --- | --- |

```
interface RegistrationManager
```

| [android.telephony.ims.RegistrationManager](../android/telephony/ims/RegistrationManager.md) |

| Known Direct Subclasses [ImsMmTelManager](../android/telephony/ims/ImsMmTelManager.md) |---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------| | [ImsMmTelManager](../android/telephony/ims/ImsMmTelManager.md) | A manager for the MmTel (Multimedia Telephony) feature of an IMS network, given an associated subscription. | |
| --- | --- | --- | --- | --- | --- | --- |

Manages IMS Service registration state for associated`ImsFeature`s. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](../android/content/pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md) Callback class for receiving IMS network Registration callback events. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_NOT_REGISTERED](../android/telephony/ims/RegistrationManager.md) The IMS service is currently not registered to the carrier network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_REGISTERED](../android/telephony/ims/RegistrationManager.md) The IMS service is currently registered to the carrier network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_REGISTERING](../android/telephony/ims/RegistrationManager.md) The IMS service is currently in the process of registering to the carrier network. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRegistrationState](../android/telephony/ims/RegistrationManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `stateCallback:` ` [Consumer](../java/util/function/Consumer.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`)` Gets the registration state of the IMS service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRegistrationTransportType](../android/telephony/ims/RegistrationManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `transportTypeCallback:` ` [Consumer](../java/util/function/Consumer.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`)` Gets the Transport Type associated with the current IMS registration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerImsRegistrationCallback](../android/telephony/ims/RegistrationManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `c:` ` [RegistrationManager.RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md)`)` Registers a [RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md) with the system. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterImsRegistrationCallback](../android/telephony/ims/RegistrationManager.md))`(`c:` ` [RegistrationManager.RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md)`)` Removes an existing [RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md). |

## Constants

### REGISTRATION_STATE_NOT_REGISTERED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_STATE_NOT_REGISTERED: Int
```

The IMS service is currently not registered to the carrier network. 

 Value: 0

### REGISTRATION_STATE_REGISTERED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_STATE_REGISTERED: Int
```

The IMS service is currently registered to the carrier network. 

 Value: 2

### REGISTRATION_STATE_REGISTERING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_STATE_REGISTERING: Int
```

The IMS service is currently in the process of registering to the carrier network. 

 Value: 1

## Public methods

### getRegistrationState

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRegistrationState(
    executor: Executor, 
    stateCallback: Consumer<Int!>
): Unit
```

Gets the registration state of the IMS service. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):The [Executor](../java/util/concurrent/Executor.md) that will be used to call the IMS registration state callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `stateCallback` | [Consumer](../java/util/function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:A callback called on the supplied [Executor](../java/util/concurrent/Executor.md) that will contain the registration state of the IMS service, which will be one of the following: [REGISTRATION_STATE_NOT_REGISTERED](../android/telephony/ims/RegistrationManager.md), [REGISTRATION_STATE_REGISTERING](../android/telephony/ims/RegistrationManager.md), or [REGISTRATION_STATE_REGISTERED](../android/telephony/ims/RegistrationManager.md). This value cannot be`null`. Value is [android.telephony.ims.RegistrationManager#REGISTRATION_STATE_NOT_REGISTERED](../android/telephony/ims/RegistrationManager.md), [android.telephony.ims.RegistrationManager#REGISTRATION_STATE_REGISTERING](../android/telephony/ims/RegistrationManager.md), or [android.telephony.ims.RegistrationManager#REGISTRATION_STATE_REGISTERED](../android/telephony/ims/RegistrationManager.md) |

### getRegistrationTransportType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRegistrationTransportType(
    executor: Executor, 
    transportTypeCallback: Consumer<Int!>
): Unit
```

Gets the Transport Type associated with the current IMS registration. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):The [Executor](../java/util/concurrent/Executor.md) that will be used to call the transportTypeCallback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `transportTypeCallback` | [Consumer](../java/util/function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:The transport type associated with the current IMS registration, which will be one of following: {@see AccessNetworkConstants#TRANSPORT_TYPE_WWAN}, {@see AccessNetworkConstants#TRANSPORT_TYPE_WLAN}, or {@see AccessNetworkConstants#TRANSPORT_TYPE_INVALID}. This value cannot be`null`. Value is android.telephony.AccessNetworkConstants.TRANSPORT_TYPE_INVALID, [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WWAN](../android/telephony/AccessNetworkConstants.md), or [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WLAN](../android/telephony/AccessNetworkConstants.md) |

### registerImsRegistrationCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerImsRegistrationCallback(
    executor: Executor, 
    c: RegistrationManager.RegistrationCallback
): Unit
```

Registers a [RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md) with the system. Use 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):The executor the callback events should be run on. |
| `c` | [RegistrationManager.RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md):The [RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md) to be added. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the subscription associated with this callback is valid, but the`ImsService`associated with the subscription is not available. This can happen if the service crashed, for example. See [ImsException.getCode()](../android/telephony/ims/ImsException.md))for a more detailed reason. |

**See Also**

- [#unregisterImsRegistrationCallback(RegistrationCallback)](../android/telephony/ims/RegistrationManager.md)) 

### unregisterImsRegistrationCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterImsRegistrationCallback(c: RegistrationManager.RegistrationCallback): Unit
```

Removes an existing [RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md). When the subscription associated with this callback is removed (SIM removed, ESIM swap, etc...), this callback will automatically be removed. If this method is called for an inactive subscription, it will result in a no-op. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [RegistrationManager.RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md):The [RegistrationCallback](../android/telephony/ims/RegistrationManager.RegistrationCallback.md) to be removed. This value cannot be`null`. |

**See Also**

- [android.telephony.SubscriptionManager.OnSubscriptionsChangedListener](../android/telephony/SubscriptionManager.OnSubscriptionsChangedListener.md)
- [#registerImsRegistrationCallback(Executor, RegistrationCallback)](../android/telephony/ims/RegistrationManager.md))
