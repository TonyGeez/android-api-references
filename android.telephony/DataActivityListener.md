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

Callback invoked when data activity state changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](../android/telephony/TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](../android/telephony/TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](../android/telephony/TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](../android/telephony/SubscriptionManager.md)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.TelephonyManager#DATA_ACTIVITY_NONE](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#DATA_ACTIVITY_IN](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#DATA_ACTIVITY_OUT](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#DATA_ACTIVITY_INOUT](../android/telephony/TelephonyManager.md), or [android.telephony.TelephonyManager#DATA_ACTIVITY_DORMANT](../android/telephony/TelephonyManager.md) |

**See Also**

- [android.telephony.TelephonyManager#DATA_ACTIVITY_NONE](../android/telephony/TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_IN](../android/telephony/TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_OUT](../android/telephony/TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_INOUT](../android/telephony/TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_DORMANT](../android/telephony/TelephonyManager.md)
