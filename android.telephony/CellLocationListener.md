# TelephonyCallback.CellLocationListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellLocationListener

Kotlin| [Java](../android/telephony/TelephonyCallback.CellLocationListener.md) 
| --- | --- |

```
interface CellLocationListener
```

| [android.telephony.TelephonyCallback.CellLocationListener](../android/telephony/TelephonyCallback.CellLocationListener.md) |

Interface for device cell location listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCellLocationChanged](../android/telephony/TelephonyCallback.CellLocationListener.md))`(`location:` ` [CellLocation](CellLocation.md)`)` Callback invoked when device cell location changes on the registered subscription. |

## Public methods

### onCellLocationChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCellLocationChanged(location: CellLocation): Unit
```

Callback invoked when device cell location changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)). 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `location` | [CellLocation](CellLocation.md):This value cannot be`null`. |
