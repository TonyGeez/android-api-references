# TelephonyCallback.ServiceStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceStateListener

Kotlin | [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.ServiceStateListener "View this page in Java") 
| --- | --- |

```
interface ServiceStateListener
```

| [android.telephony.TelephonyCallback.ServiceStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener#) |

Interface for service state listener.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceStateChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener#onServiceStateChanged(android.telephony.ServiceState))`(`serviceState:` ` [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState)`)` Callback invoked when device service state changes on the registered subscription. |

## Public methods

### onServiceStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceStateChanged(serviceState: ServiceState): Unit
```

Callback invoked when device service state changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()).

The instance of [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState) passed as an argument here will have various levels of location information stripped from it depending on the location permissions that your app holds. Only apps holding the [Manifest.permission.ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission will receive all the information in [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState), otherwise the cellIdentity will be null if apps only holding the [Manifest.permission.ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) permission. Network operator name in long/short alphanumeric format and numeric id will be null if apps holding neither [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| `serviceState` | [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState): This value cannot be `null`. |

**See Also**

- [android.telephony.ServiceState#STATE_EMERGENCY_ONLY](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_EMERGENCY_ONLY:kotlin.Int)
- [android.telephony.ServiceState#STATE_IN_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_IN_SERVICE:kotlin.Int)
- [android.telephony.ServiceState#STATE_OUT_OF_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_OUT_OF_SERVICE:kotlin.Int)
- [android.telephony.ServiceState#STATE_POWER_OFF](https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_POWER_OFF:kotlin.Int)
