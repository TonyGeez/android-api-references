# TelephonyCallback.EmergencyNumberListListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EmergencyNumberListListener

Kotlin | [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.EmergencyNumberListListener "View this page in Java") 
| --- | --- |

```
interface EmergencyNumberListListener
```

| [android.telephony.TelephonyCallback.EmergencyNumberListListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.EmergencyNumberListListener#) |

Interface for the current emergency number list listener.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEmergencyNumberListChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.EmergencyNumberListListener#onEmergencyNumberListChanged(kotlin.collections.MutableMap))`(`emergencyNumberList:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [EmergencyNumber](https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber)!>!>`)` Callback invoked when the current emergency number list has changed on the registered subscription. |

## Public methods

### onEmergencyNumberListChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEmergencyNumberListChanged(emergencyNumberList: MutableMap<Int!, MutableList<EmergencyNumber!>!>): Unit
```

Callback invoked when the current emergency number list has changed on the registered subscription.

Note, the registered subscription is associated with [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object on which [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)) was called. If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the given subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())) if it does not have the [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String). 
Requires [android.Manifest.permission#READ_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String)

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `emergencyNumberList` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EmergencyNumber](https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber)!\>!\>: Map associating all active subscriptions on the device with the list of emergency numbers originating from that subscription. If there are no active subscriptions, the map will contain a single entry with [SubscriptionManager.INVALID_SUBSCRIPTION_ID](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int) as the key and a list of emergency numbers as the value. If no emergency number information is available, the value will be empty. This value cannot be `null`. |
