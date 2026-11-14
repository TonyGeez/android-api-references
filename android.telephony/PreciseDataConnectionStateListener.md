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
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreciseDataConnectionStateChanged](../android/telephony/TelephonyCallback.PreciseDataConnectionStateListener.md))`(`dataConnectionState:` ` [PreciseDataConnectionState](PreciseDataConnectionState.md)`)` Callback providing update about the default/internet data connection on the registered subscription. |

## Public methods

### onPreciseDataConnectionStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreciseDataConnectionStateChanged(dataConnectionState: PreciseDataConnectionState): Unit
```

Callback providing update about the default/internet data connection on the registered subscription.

Note, the registration subscription ID comes from [TelephonyManager](TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataConnectionState` | [PreciseDataConnectionState](PreciseDataConnectionState.md): [PreciseDataConnectionState](PreciseDataConnectionState.md) This value cannot be`null`. |
