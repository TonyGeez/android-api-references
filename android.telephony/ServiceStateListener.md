# TelephonyCallback.ServiceStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceStateListener

Kotlin | [Java](../android/telephony/TelephonyCallback.ServiceStateListener.md) 
| --- | --- |

```
interface ServiceStateListener
```

| [android.telephony.TelephonyCallback.ServiceStateListener](../android/telephony/TelephonyCallback.ServiceStateListener.md) |

Interface for service state listener.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceStateChanged](../android/telephony/TelephonyCallback.ServiceStateListener.md))`(`serviceState:` ` [ServiceState](ServiceState.md)`)` Callback invoked when device service state changes on the registered subscription. |

## Public methods

### onServiceStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceStateChanged(serviceState: ServiceState): Unit
```

Callback invoked when device service state changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)).

The instance of [ServiceState](ServiceState.md) passed as an argument here will have various levels of location information stripped from it depending on the location permissions that your app holds. Only apps holding the [Manifest.permission.ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission will receive all the information in [ServiceState](ServiceState.md), otherwise the cellIdentity will be null if apps only holding the [Manifest.permission.ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) permission. Network operator name in long/short alphanumeric format and numeric id will be null if apps holding neither [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| `serviceState` | [ServiceState](ServiceState.md): This value cannot be `null`. |

**See Also**

- [android.telephony.ServiceState#STATE_EMERGENCY_ONLY](ServiceState.md)
- [android.telephony.ServiceState#STATE_IN_SERVICE](ServiceState.md)
- [android.telephony.ServiceState#STATE_OUT_OF_SERVICE](ServiceState.md)
- [android.telephony.ServiceState#STATE_POWER_OFF](ServiceState.md)
