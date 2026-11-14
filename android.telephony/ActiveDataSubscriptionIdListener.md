# TelephonyCallback.ActiveDataSubscriptionIdListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActiveDataSubscriptionIdListener

Kotlin| [Java](../android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener.md) 
| --- | --- |

```
interface ActiveDataSubscriptionIdListener
```

| [android.telephony.TelephonyCallback.ActiveDataSubscriptionIdListener](../android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener.md) |

Interface for active data subscription ID listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActiveDataSubscriptionIdChanged](../android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener.md))`(`subId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when active data subscription ID changes. |

## Public methods

### onActiveDataSubscriptionIdChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActiveDataSubscriptionIdChanged(subId: Int): Unit
```

Callback invoked when active data subscription ID changes. Note, this callback triggers regardless of registered subscription. 
Requires [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):current subscription used to setup Cellular Internet data. The data is only active on the subscription at a time, even it is multi-SIM mode. For example, it could be the current active opportunistic subscription in use, or the subscription user selected as default data subscription in DSDS mode. The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](../android/telephony/TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PHONE_STATE](../android/Manifest.permission.md). |
