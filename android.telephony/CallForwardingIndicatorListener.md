# TelephonyCallback.CallForwardingIndicatorListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallForwardingIndicatorListener

Kotlin| [Java](../android/telephony/TelephonyCallback.CallForwardingIndicatorListener.md) 
| --- | --- |

```
interface CallForwardingIndicatorListener
```

| [android.telephony.TelephonyCallback.CallForwardingIndicatorListener](../android/telephony/TelephonyCallback.CallForwardingIndicatorListener.md) |

Interface for call-forwarding indicator listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCallForwardingIndicatorChanged](../android/telephony/TelephonyCallback.CallForwardingIndicatorListener.md))`(`cfi:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the call-forwarding indicator changes on the registered subscription. |

## Public methods

### onCallForwardingIndicatorChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCallForwardingIndicatorChanged(cfi: Boolean): Unit
```

Callback invoked when the call-forwarding indicator changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](../android/telephony/TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](../android/telephony/TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](../android/telephony/TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](../android/telephony/SubscriptionManager.md)). The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](../android/telephony/TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)
