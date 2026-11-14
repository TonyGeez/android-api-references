# TelephonyCallback.PreciseDataConnectionStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreciseDataConnectionStateListener

Kotlin| [Java](../android/telephony/TelephonyCallback.PreciseDataConnectionStateListener.md) 
| --- | --- |

```
interface PreciseDataConnectionStateListener
```

| [android.telephony.TelephonyCallback.PreciseDataConnectionStateListener](../android/telephony/TelephonyCallback.PreciseDataConnectionStateListener.md) |

Interface for precise data connection state listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreciseDataConnectionStateChanged](../android/telephony/TelephonyCallback.PreciseDataConnectionStateListener.md))`(`dataConnectionState:` ` [PreciseDataConnectionState](../android/telephony/PreciseDataConnectionState.md)`)` Callback providing update about the default/internet data connection on the registered subscription. |

## Public methods

### onPreciseDataConnectionStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreciseDataConnectionStateChanged(dataConnectionState: PreciseDataConnectionState): Unit
```

Callback providing update about the default/internet data connection on the registered subscription.

Note, the registration subscription ID comes from [TelephonyManager](../android/telephony/TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](../android/telephony/TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](../android/telephony/TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](../android/telephony/SubscriptionManager.md)). The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](../android/telephony/TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataConnectionState` | [PreciseDataConnectionState](../android/telephony/PreciseDataConnectionState.md): [PreciseDataConnectionState](../android/telephony/PreciseDataConnectionState.md) This value cannot be`null`. |
