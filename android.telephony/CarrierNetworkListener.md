# TelephonyCallback.CarrierNetworkListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CarrierNetworkListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.CarrierNetworkListener "View this page in Java") 

```
interface CarrierNetworkListener
```

| [android.telephony.TelephonyCallback.CarrierNetworkListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CarrierNetworkListener#) |

Interface for carrier network listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCarrierNetworkChange](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CarrierNetworkListener#onCarrierNetworkChange(kotlin.Boolean))`(`active:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when telephony has received notice from a carrier app that a network action that could result in connectivity loss has been requested by an app using [android.service.carrier.CarrierService#notifyCarrierNetworkChange(boolean)](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierService.html#notifyCarrierNetworkChange(kotlin.Boolean)) |

## Public methods

### onCarrierNetworkChange

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCarrierNetworkChange(active: Boolean): Unit
```

Callback invoked when telephony has received notice from a carrier app that a network action that could result in connectivity loss has been requested by an app using [android.service.carrier.CarrierService#notifyCarrierNetworkChange(boolean)](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierService.html#notifyCarrierNetworkChange(kotlin.Boolean))

This is optional and is only used to allow the system to provide alternative UI while telephony is performing an action that may result in intentional, temporary network lack of connectivity.

Note, this callback is pinned to the registered subscription and will be invoked when the notifying carrier app has carrier privilege rule on the registered subscription. [android.telephony.TelephonyManager#hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `active` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If the carrier network change is or shortly will be active,`true`indicate that showing alternative UI,`false`otherwise. |
