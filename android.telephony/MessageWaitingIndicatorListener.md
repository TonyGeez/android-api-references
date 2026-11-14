# TelephonyCallback.MessageWaitingIndicatorListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageWaitingIndicatorListener

Kotlin| [Java](../android/telephony/TelephonyCallback.MessageWaitingIndicatorListener.md) 
| --- | --- |

```
interface MessageWaitingIndicatorListener
```

| [android.telephony.TelephonyCallback.MessageWaitingIndicatorListener](../android/telephony/TelephonyCallback.MessageWaitingIndicatorListener.md) |

Interface for message waiting indicator listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMessageWaitingIndicatorChanged](../android/telephony/TelephonyCallback.MessageWaitingIndicatorListener.md))`(`mwi:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the message-waiting indicator changes on the registered subscription. |

## Public methods

### onMessageWaitingIndicatorChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMessageWaitingIndicatorChanged(mwi: Boolean): Unit
```

Callback invoked when the message-waiting indicator changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](../android/telephony/TelephonyManager.md) object by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](../android/telephony/TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](../android/telephony/TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](../android/telephony/SubscriptionManager.md)). The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](../android/telephony/TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)
