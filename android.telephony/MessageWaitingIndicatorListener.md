# TelephonyCallback.MessageWaitingIndicatorListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageWaitingIndicatorListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.MessageWaitingIndicatorListener "View this page in Java") 
| --- | --- |

```
interface MessageWaitingIndicatorListener
```

| [android.telephony.TelephonyCallback.MessageWaitingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.MessageWaitingIndicatorListener#) |

Interface for message waiting indicator listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageWaitingIndicatorChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.MessageWaitingIndicatorListener#onMessageWaitingIndicatorChanged(kotlin.Boolean))`(`mwi:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the message-waiting indicator changes on the registered subscription. |

## Public methods

### onMessageWaitingIndicatorChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMessageWaitingIndicatorChanged(mwi: Boolean): Unit
```

Callback invoked when the message-waiting indicator changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())) if it does not have the [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String). 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String)
