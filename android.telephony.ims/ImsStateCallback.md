# ImsStateCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsStateCallback

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ims/ImsStateCallback "View this page in Java") 
| --- | --- |

```
abstract class ImsStateCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.ImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#) |

A callback class used for monitoring changes in IMS service connection states for a specific subscription.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_IMS_SERVICE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_IMS_SERVICE_DISCONNECTED:kotlin.Int) The underlying IMS service has died, is reconfiguring, or has never come up yet and as a result is currently unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_IMS_SERVICE_NOT_READY](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_IMS_SERVICE_NOT_READY:kotlin.Int) The IMS service is connected, but in a NOT_READY state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_NO_IMS_SERVICE_CONFIGURED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_NO_IMS_SERVICE_CONFIGURED:kotlin.Int) There is no IMS service configured for the subscription ID specified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_SUBSCRIPTION_INACTIVE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_SUBSCRIPTION_INACTIVE:kotlin.Int) The subscription associated with this Manager has moved to an inactive state (e.g. SIM removed) and the IMS service has torn down the resources related to this subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_UNKNOWN_PERMANENT_ERROR](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_UNKNOWN_PERMANENT_ERROR:kotlin.Int) The underlying IMS service is permanently unavailable for the associated subscription and there will be no Manager available for this subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_UNKNOWN_TEMPORARY_ERROR](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_UNKNOWN_TEMPORARY_ERROR:kotlin.Int) The underlying IMS service is temporarily unavailable for the associated subscription. |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---|
| [ImsStateCallback](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#ImsStateCallback())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAvailable](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#onAvailable())`()` The IMS service is connected and is ready for communication over the provided Manager. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#onError())`()` An unexpected error has occurred and the Telephony process has crashed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUnavailable](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#onUnavailable(kotlin.Int))`(`reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The IMS service has disconnected or is reporting NOT_READY and is no longer available to users. |
| --- | --- |

## Constants

### REASON_IMS_SERVICE_DISCONNECTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_IMS_SERVICE_DISCONNECTED: Int
```

The underlying IMS service has died, is reconfiguring, or has never come up yet and as a result is currently unavailable. [onAvailable](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#onAvailable())will be called when the IMS service becomes available. All callbacks should be unregistered now and registered again if the IMS service moves back to available. 

 Value: 3

### REASON_IMS_SERVICE_NOT_READY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_IMS_SERVICE_NOT_READY: Int
```

The IMS service is connected, but in a NOT_READY state. Once the service moves to ready, [onAvailable](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#onAvailable())will be called. 

 Value: 6

### REASON_NO_IMS_SERVICE_CONFIGURED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_NO_IMS_SERVICE_CONFIGURED: Int
```

There is no IMS service configured for the subscription ID specified. This is a permanent error and there will be no Manager available for this subscription. 

 Value: 4

### REASON_SUBSCRIPTION_INACTIVE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_SUBSCRIPTION_INACTIVE: Int
```

The subscription associated with this Manager has moved to an inactive state (e.g. SIM removed) and the IMS service has torn down the resources related to this subscription. This has caused this callback to be deregistered. The callback must be re-registered when this subscription becomes active in order to continue listening to the IMS service state. 

 Value: 5

### REASON_UNKNOWN_PERMANENT_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_UNKNOWN_PERMANENT_ERROR: Int
```

The underlying IMS service is permanently unavailable for the associated subscription and there will be no Manager available for this subscription. 

 Value: 2

### REASON_UNKNOWN_TEMPORARY_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_UNKNOWN_TEMPORARY_ERROR: Int
```

The underlying IMS service is temporarily unavailable for the associated subscription. [onAvailable](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#onAvailable())will be called when the IMS service becomes available again. 

 Value: 1

## Public constructors

### ImsStateCallback

```
ImsStateCallback()
```

## Public methods

### onAvailable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAvailable(): Unit
```

The IMS service is connected and is ready for communication over the provided Manager. 

### onError

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(): Unit
```

An unexpected error has occurred and the Telephony process has crashed. This has caused this callback to be deregistered. The callback must be re-registered in order to continue listening to the IMS service state. 

### onUnavailable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUnavailable(reason: Int): Unit
```

The IMS service has disconnected or is reporting NOT_READY and is no longer available to users. The user should clean up all related state and unregister callbacks. If it is a temporary error, [onAvailable](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#onAvailable())will be called when the IMS service becomes available again.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the specified reason Value is [android.telephony.ims.ImsStateCallback#REASON_UNKNOWN_TEMPORARY_ERROR](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_UNKNOWN_TEMPORARY_ERROR:kotlin.Int), [android.telephony.ims.ImsStateCallback#REASON_UNKNOWN_PERMANENT_ERROR](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_UNKNOWN_PERMANENT_ERROR:kotlin.Int), [android.telephony.ims.ImsStateCallback#REASON_IMS_SERVICE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_IMS_SERVICE_DISCONNECTED:kotlin.Int), [android.telephony.ims.ImsStateCallback#REASON_NO_IMS_SERVICE_CONFIGURED](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_NO_IMS_SERVICE_CONFIGURED:kotlin.Int), [android.telephony.ims.ImsStateCallback#REASON_SUBSCRIPTION_INACTIVE](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_SUBSCRIPTION_INACTIVE:kotlin.Int), or [android.telephony.ims.ImsStateCallback#REASON_IMS_SERVICE_NOT_READY](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsStateCallback#REASON_IMS_SERVICE_NOT_READY:kotlin.Int) |
