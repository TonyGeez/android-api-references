# TelephonyCallback.CarrierNetworkListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CarrierNetworkListener

Kotlin| [Java](../android/telephony/TelephonyCallback.CarrierNetworkListener.md) 
| --- | --- |

```
interface CarrierNetworkListener
```

| [android.telephony.TelephonyCallback.CarrierNetworkListener](../android/telephony/TelephonyCallback.CarrierNetworkListener.md) |

Interface for carrier network listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCarrierNetworkChange](../android/telephony/TelephonyCallback.CarrierNetworkListener.md))`(`active:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback invoked when telephony has received notice from a carrier app that a network action that could result in connectivity loss has been requested by an app using [android.service.carrier.CarrierService#notifyCarrierNetworkChange(boolean)](../android.service.carrier/CarrierService.md)) |

## Public methods

### onCarrierNetworkChange

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCarrierNetworkChange(active: Boolean): Unit
```

Callback invoked when telephony has received notice from a carrier app that a network action that could result in connectivity loss has been requested by an app using [android.service.carrier.CarrierService#notifyCarrierNetworkChange(boolean)](../android.service.carrier/CarrierService.md))

This is optional and is only used to allow the system to provide alternative UI while telephony is performing an action that may result in intentional, temporary network lack of connectivity.

Note, this callback is pinned to the registered subscription and will be invoked when the notifying carrier app has carrier privilege rule on the registered subscription. [android.telephony.TelephonyManager#hasCarrierPrivileges](TelephonyManager.md))

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `active` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If the carrier network change is or shortly will be active,`true`indicate that showing alternative UI,`false`otherwise. |
