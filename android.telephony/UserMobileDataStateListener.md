# TelephonyCallback.UserMobileDataStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserMobileDataStateListener

Kotlin | [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.UserMobileDataStateListener "View this page in Java") 
| --- | --- |

```
interface UserMobileDataStateListener
```

| [android.telephony.TelephonyCallback.UserMobileDataStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.UserMobileDataStateListener#) |

Interface for user mobile data state listener.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUserMobileDataStateChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.UserMobileDataStateListener#onUserMobileDataStateChanged(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when the user mobile data state has changed on the registered subscription. |

## Public methods

### onUserMobileDataStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUserMobileDataStateChanged(enabled: Boolean): Unit
```

Callback invoked when the user mobile data state has changed on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): indicates whether the current user mobile data state is enabled or disabled. |
