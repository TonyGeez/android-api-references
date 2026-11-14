# TelephonyCallback.CellLocationListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellLocationListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.CellLocationListener "View this page in Java") 
| --- | --- |

```
interface CellLocationListener
```

| [android.telephony.TelephonyCallback.CellLocationListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellLocationListener#) |

Interface for device cell location listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCellLocationChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellLocationListener#onCellLocationChanged(android.telephony.CellLocation))`(`location:` ` [CellLocation](https://developer.android.com/reference/kotlin/android/telephony/CellLocation)`)` Callback invoked when device cell location changes on the registered subscription. |

## Public methods

### onCellLocationChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCellLocationChanged(location: CellLocation): Unit
```

Callback invoked when device cell location changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()). 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `location` | [CellLocation](https://developer.android.com/reference/kotlin/android/telephony/CellLocation):This value cannot be`null`. |
