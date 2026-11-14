# TelephonyCallback.CallStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallStateListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.CallStateListener "View this page in Java") 
| --- | --- |

```
interface CallStateListener
```

| [android.telephony.TelephonyCallback.CallStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallStateListener#) |

Interface for call state listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallStateChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallStateListener#onCallStateChanged(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when device call state changes. |

## Public methods

### onCallStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCallStateChanged(state: Int): Unit
```

Callback invoked when device call state changes.

Reports the state of Telephony (mobile) calls on the device for the registered subscription.

Note: the registration subscription ID comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()).

Note: The state returned here may differ from that returned by [TelephonyManager.getCallState()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getCallState()). Receivers of this callback should be aware that calling [TelephonyManager.getCallState()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getCallState())from within this callback may return a different state than the callback reports. 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String)

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current call state Value is [android.telephony.TelephonyManager#CALL_STATE_IDLE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_IDLE:kotlin.Int), [android.telephony.TelephonyManager#CALL_STATE_RINGING](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_RINGING:kotlin.Int), or [android.telephony.TelephonyManager#CALL_STATE_OFFHOOK](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_OFFHOOK:kotlin.Int) |
