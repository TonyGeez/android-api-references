# TelephonyCallback.EmergencyNumberListListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EmergencyNumberListListener

Kotlin | [Java](../android/telephony/TelephonyCallback.EmergencyNumberListListener.md) 
| --- | --- |

```
interface EmergencyNumberListListener
```

| [android.telephony.TelephonyCallback.EmergencyNumberListListener](../android/telephony/TelephonyCallback.EmergencyNumberListListener.md) |

Interface for the current emergency number list listener.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEmergencyNumberListChanged](../android/telephony/TelephonyCallback.EmergencyNumberListListener.md))`(`emergencyNumberList:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [EmergencyNumber](../android/telephony/emergency/EmergencyNumber.md)!>!>`)` Callback invoked when the current emergency number list has changed on the registered subscription. |

## Public methods

### onEmergencyNumberListChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEmergencyNumberListChanged(emergencyNumberList: MutableMap<Int!, MutableList<EmergencyNumber!>!>): Unit
```

Callback invoked when the current emergency number list has changed on the registered subscription.

Note, the registered subscription is associated with [TelephonyManager](../android/telephony/TelephonyManager.md) object on which [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](../android/telephony/TelephonyManager.md)) was called. If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](../android/telephony/TelephonyManager.md)), then the callback applies to the given subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](../android/telephony/SubscriptionManager.md)). The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](../android/telephony/TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md). 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `emergencyNumberList` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EmergencyNumber](../android/telephony/emergency/EmergencyNumber.md)!\>!\>: Map associating all active subscriptions on the device with the list of emergency numbers originating from that subscription. If there are no active subscriptions, the map will contain a single entry with [SubscriptionManager.INVALID_SUBSCRIPTION_ID](../android/telephony/SubscriptionManager.md) as the key and a list of emergency numbers as the value. If no emergency number information is available, the value will be empty. This value cannot be `null`. |
