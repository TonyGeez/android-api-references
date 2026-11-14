# TelephonyCallback.CallStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallStateListener

Kotlin| [Java](../android/telephony/TelephonyCallback.CallStateListener.md) 
| --- | --- |

```
interface CallStateListener
```

| [android.telephony.TelephonyCallback.CallStateListener](../android/telephony/TelephonyCallback.CallStateListener.md) |

Interface for call state listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallStateChanged](../android/telephony/TelephonyCallback.CallStateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when device call state changes. |

## Public methods

### onCallStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCallStateChanged(state: Int): Unit
```

Callback invoked when device call state changes.

Reports the state of Telephony (mobile) calls on the device for the registered subscription.

Note: the registration subscription ID comes from [TelephonyManager](../android/telephony/TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](../android/telephony/TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](../android/telephony/TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](../android/telephony/SubscriptionManager.md)).

Note: The state returned here may differ from that returned by [TelephonyManager.getCallState()](../android/telephony/TelephonyManager.md)). Receivers of this callback should be aware that calling [TelephonyManager.getCallState()](../android/telephony/TelephonyManager.md))from within this callback may return a different state than the callback reports. 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current call state Value is [android.telephony.TelephonyManager#CALL_STATE_IDLE](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#CALL_STATE_RINGING](../android/telephony/TelephonyManager.md), or [android.telephony.TelephonyManager#CALL_STATE_OFFHOOK](../android/telephony/TelephonyManager.md) |
