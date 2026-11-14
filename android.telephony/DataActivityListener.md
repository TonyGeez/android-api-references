# TelephonyCallback.DataActivityListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataActivityListener

Kotlin| [Java](../android/telephony/TelephonyCallback.DataActivityListener.md) 
| --- | --- |

```
interface DataActivityListener
```

| [android.telephony.TelephonyCallback.DataActivityListener](../android/telephony/TelephonyCallback.DataActivityListener.md) |

Interface for data activity state listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataActivity](../android/telephony/TelephonyCallback.DataActivityListener.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when data activity state changes on the registered subscription. |

## Public methods

### onDataActivity

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDataActivity(direction: Int): Unit
```

Callback invoked when data activity state changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.TelephonyManager#DATA_ACTIVITY_NONE](TelephonyManager.md), [android.telephony.TelephonyManager#DATA_ACTIVITY_IN](TelephonyManager.md), [android.telephony.TelephonyManager#DATA_ACTIVITY_OUT](TelephonyManager.md), [android.telephony.TelephonyManager#DATA_ACTIVITY_INOUT](TelephonyManager.md), or [android.telephony.TelephonyManager#DATA_ACTIVITY_DORMANT](TelephonyManager.md) |

**See Also**

- [android.telephony.TelephonyManager#DATA_ACTIVITY_NONE](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_IN](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_OUT](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_INOUT](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_DORMANT](TelephonyManager.md)
