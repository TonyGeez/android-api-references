# TelephonyCallback.UserMobileDataStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserMobileDataStateListener

Kotlin | [Java](../android/telephony/TelephonyCallback.UserMobileDataStateListener.md) 
| --- | --- |

```
interface UserMobileDataStateListener
```

| [android.telephony.TelephonyCallback.UserMobileDataStateListener](../android/telephony/TelephonyCallback.UserMobileDataStateListener.md) |

Interface for user mobile data state listener.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUserMobileDataStateChanged](../android/telephony/TelephonyCallback.UserMobileDataStateListener.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the user mobile data state has changed on the registered subscription. |

## Public methods

### onUserMobileDataStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUserMobileDataStateChanged(enabled: Boolean): Unit
```

Callback invoked when the user mobile data state has changed on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](../android/telephony/TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](../android/telephony/TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](../android/telephony/TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](../android/telephony/SubscriptionManager.md)).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): indicates whether the current user mobile data state is enabled or disabled. |
