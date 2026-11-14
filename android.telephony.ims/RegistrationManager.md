# RegistrationManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RegistrationManager

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ims/RegistrationManager "View this page in Java") 

```
interface RegistrationManager
```

| [android.telephony.ims.RegistrationManager](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#) |

| Known Direct Subclasses [ImsMmTelManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager) |---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------| | [ImsMmTelManager](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsMmTelManager) | A manager for the MmTel (Multimedia Telephony) feature of an IMS network, given an associated subscription. | |

Manages IMS Service registration state for associated`ImsFeature`s. 
Requires the [PackageManager#FEATURE_TELEPHONY_IMS](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback) Callback class for receiving IMS network Registration callback events. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_NOT_REGISTERED](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_NOT_REGISTERED:kotlin.Int) The IMS service is currently not registered to the carrier network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_REGISTERED](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERED:kotlin.Int) The IMS service is currently registered to the carrier network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_STATE_REGISTERING](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERING:kotlin.Int) The IMS service is currently in the process of registering to the carrier network. |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRegistrationState](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#getRegistrationState(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `stateCallback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`)` Gets the registration state of the IMS service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRegistrationTransportType](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#getRegistrationTransportType(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `transportTypeCallback:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`)` Gets the Transport Type associated with the current IMS registration. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerImsRegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#registerImsRegistrationCallback(java.util.concurrent.Executor,%20android.telephony.ims.RegistrationManager.RegistrationCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `c:` ` [RegistrationManager.RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback)`)` Registers a [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback) with the system. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterImsRegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#unregisterImsRegistrationCallback(android.telephony.ims.RegistrationManager.RegistrationCallback))`(`c:` ` [RegistrationManager.RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback)`)` Removes an existing [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback). |

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
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that will be used to call the IMS registration state callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `stateCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:A callback called on the supplied [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that will contain the registration state of the IMS service, which will be one of the following: [REGISTRATION_STATE_NOT_REGISTERED](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_NOT_REGISTERED:kotlin.Int), [REGISTRATION_STATE_REGISTERING](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERING:kotlin.Int), or [REGISTRATION_STATE_REGISTERED](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERED:kotlin.Int). This value cannot be`null`. Value is [android.telephony.ims.RegistrationManager#REGISTRATION_STATE_NOT_REGISTERED](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_NOT_REGISTERED:kotlin.Int), [android.telephony.ims.RegistrationManager#REGISTRATION_STATE_REGISTERING](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERING:kotlin.Int), or [android.telephony.ims.RegistrationManager#REGISTRATION_STATE_REGISTERED](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#REGISTRATION_STATE_REGISTERED:kotlin.Int) |

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
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that will be used to call the transportTypeCallback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `transportTypeCallback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:The transport type associated with the current IMS registration, which will be one of following: {@see AccessNetworkConstants#TRANSPORT_TYPE_WWAN}, {@see AccessNetworkConstants#TRANSPORT_TYPE_WLAN}, or {@see AccessNetworkConstants#TRANSPORT_TYPE_INVALID}. This value cannot be`null`. Value is android.telephony.AccessNetworkConstants.TRANSPORT_TYPE_INVALID, [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WWAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.html#TRANSPORT_TYPE_WWAN:kotlin.Int), or [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WLAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.html#TRANSPORT_TYPE_WLAN:kotlin.Int) |

### registerImsRegistrationCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerImsRegistrationCallback(
    executor: Executor, 
    c: RegistrationManager.RegistrationCallback
): Unit
```

Registers a [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback) with the system. Use 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor the callback events should be run on. |
| `c` | [RegistrationManager.RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback):The [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback) to be added. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.telephony.ims.ImsException` | if the subscription associated with this callback is valid, but the`ImsService`associated with the subscription is not available. This can happen if the service crashed, for example. See [ImsException.getCode()](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsException#getCode())for a more detailed reason. |

**See Also**

- [#unregisterImsRegistrationCallback(RegistrationCallback)](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#unregisterImsRegistrationCallback(android.telephony.ims.RegistrationManager.RegistrationCallback)) 

### unregisterImsRegistrationCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterImsRegistrationCallback(c: RegistrationManager.RegistrationCallback): Unit
```

Removes an existing [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback). When the subscription associated with this callback is removed (SIM removed, ESIM swap, etc...), this callback will automatically be removed. If this method is called for an inactive subscription, it will result in a no-op. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [RegistrationManager.RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback):The [RegistrationCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager.RegistrationCallback) to be removed. This value cannot be`null`. |

**See Also**

- [android.telephony.SubscriptionManager.OnSubscriptionsChangedListener](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.OnSubscriptionsChangedListener.html#)
- [#registerImsRegistrationCallback(Executor, RegistrationCallback)](https://developer.android.com/reference/kotlin/android/telephony/ims/RegistrationManager#registerImsRegistrationCallback(java.util.concurrent.Executor,%20android.telephony.ims.RegistrationManager.RegistrationCallback))
