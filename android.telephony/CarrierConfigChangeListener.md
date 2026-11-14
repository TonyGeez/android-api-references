# CarrierConfigManager.CarrierConfigChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CarrierConfigChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/CarrierConfigManager.CarrierConfigChangeListener "View this page in Java") 
| --- | --- |

```
interface CarrierConfigChangeListener
```

| [android.telephony.CarrierConfigManager.CarrierConfigChangeListener](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener#) |

Listener interface to get a notification when the carrier configurations have changed. Use this listener to receive timely updates when the carrier configuration changes. System components should prefer this listener over [ACTION_CARRIER_CONFIG_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String) whenever possible. To register the listener, call [registerCarrierConfigChangeListener(java.util.concurrent.Executor,android.telephony.CarrierConfigManager.CarrierConfigChangeListener)](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#registerCarrierConfigChangeListener(java.util.concurrent.Executor,%20android.telephony.CarrierConfigManager.CarrierConfigChangeListener)). To unregister, call [unregisterCarrierConfigChangeListener(android.telephony.CarrierConfigManager.CarrierConfigChangeListener)](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#unregisterCarrierConfigChangeListener(android.telephony.CarrierConfigManager.CarrierConfigChangeListener)). Note that on registration, registrants will NOT receive a notification on last carrier config change. Only carrier configs change AFTER the registration will be sent to registrants. And unlike [ACTION_CARRIER_CONFIG_CHANGED](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#ACTION_CARRIER_CONFIG_CHANGED:kotlin.String), notification wouldn't send when the device is unlocked. Registrants only receive the notification when there has been real carrier config changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCarrierConfigChanged](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener#onCarrierConfigChanged(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`logicalSlotIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `subscriptionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `carrierId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `specificCarrierId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when carrier configurations have changed. |

## Public methods

### onCarrierConfigChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCarrierConfigChanged(
    logicalSlotIndex: Int, 
    subscriptionId: Int, 
    carrierId: Int, 
    specificCarrierId: Int
): Unit
```

Called when carrier configurations have changed.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `logicalSlotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The logical SIM slot index on which to monitor and get notification. It is guaranteed to be valid. |
| `subscriptionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The subscription on the SIM slot. May be [SubscriptionManager.INVALID_SUBSCRIPTION_ID](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int). |
| `carrierId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The optional carrier Id, may be [TelephonyManager.UNKNOWN_CARRIER_ID](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int). See [TelephonyManager.getSimCarrierId()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getSimCarrierId()). |
| --- | --- |
| `specificCarrierId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The optional fine-grained carrierId, may be [android.telephony.TelephonyManager#UNKNOWN_CARRIER_ID](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int). A specific carrierId may be different from the carrierId above in a MVNO scenario. See detail in [TelephonyManager.getSimSpecificCarrierId()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getSimSpecificCarrierId()). |
