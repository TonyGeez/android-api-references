# TelephonyCallback.PreciseDataConnectionStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreciseDataConnectionStateListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.PreciseDataConnectionStateListener "View this page in Java") 

```
interface PreciseDataConnectionStateListener
```

| [android.telephony.TelephonyCallback.PreciseDataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PreciseDataConnectionStateListener#) |

Interface for precise data connection state listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreciseDataConnectionStateChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PreciseDataConnectionStateListener#onPreciseDataConnectionStateChanged(android.telephony.PreciseDataConnectionState))`(`dataConnectionState:` ` [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState)`)` Callback providing update about the default/internet data connection on the registered subscription. |

## Public methods

### onPreciseDataConnectionStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreciseDataConnectionStateChanged(dataConnectionState: PreciseDataConnectionState): Unit
```

Callback providing update about the default/internet data connection on the registered subscription.

Note, the registration subscription ID comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataConnectionState` | [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState): [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState) This value cannot be`null`. |
