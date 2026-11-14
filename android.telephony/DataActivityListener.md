# TelephonyCallback.DataActivityListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataActivityListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.DataActivityListener "View this page in Java") 
| --- | --- |

```
interface DataActivityListener
```

| [android.telephony.TelephonyCallback.DataActivityListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataActivityListener#) |

Interface for data activity state listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataActivity](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataActivityListener#onDataActivity(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when data activity state changes on the registered subscription. |

## Public methods

### onDataActivity

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDataActivity(direction: Int): Unit
```

Callback invoked when data activity state changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.TelephonyManager#DATA_ACTIVITY_NONE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_NONE:kotlin.Int), [android.telephony.TelephonyManager#DATA_ACTIVITY_IN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_IN:kotlin.Int), [android.telephony.TelephonyManager#DATA_ACTIVITY_OUT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_OUT:kotlin.Int), [android.telephony.TelephonyManager#DATA_ACTIVITY_INOUT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_INOUT:kotlin.Int), or [android.telephony.TelephonyManager#DATA_ACTIVITY_DORMANT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_DORMANT:kotlin.Int) |

**See Also**

- [android.telephony.TelephonyManager#DATA_ACTIVITY_NONE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_NONE:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_IN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_IN:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_OUT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_OUT:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_INOUT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_INOUT:kotlin.Int)
- [android.telephony.TelephonyManager#DATA_ACTIVITY_DORMANT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_DORMANT:kotlin.Int)
