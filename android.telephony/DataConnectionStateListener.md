# TelephonyCallback.DataConnectionStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataConnectionStateListener

Kotlin| [Java](../android/telephony/TelephonyCallback.DataConnectionStateListener.md) 
| --- | --- |

```
interface DataConnectionStateListener
```

| [android.telephony.TelephonyCallback.DataConnectionStateListener](../android/telephony/TelephonyCallback.DataConnectionStateListener.md) |

Interface for data connection state listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataConnectionStateChanged](../android/telephony/TelephonyCallback.DataConnectionStateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `networkType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when connection state changes on the registered subscription. |

## Public methods

### onDataConnectionStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDataConnectionStateChanged(
    state: Int, 
    networkType: Int
): Unit
```

Callback invoked when connection state changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](../android/telephony/TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](../android/telephony/TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](../android/telephony/TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](../android/telephony/SubscriptionManager.md)).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the current state of data connection. Value is [android.telephony.TelephonyManager#DATA_UNKNOWN](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#DATA_DISCONNECTED](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#DATA_CONNECTING](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#DATA_CONNECTED](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#DATA_SUSPENDED](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#DATA_DISCONNECTING](../android/telephony/TelephonyManager.md), or [android.telephony.TelephonyManager#DATA_HANDOVER_IN_PROGRESS](../android/telephony/TelephonyManager.md) |
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the current network type of data connection. Value is [android.telephony.TelephonyManager#NETWORK_TYPE_UNKNOWN](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_GPRS](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EDGE](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_UMTS](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_CDMA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_0](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_A](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_1xRTT](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSDPA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSUPA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_IDEN](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_B](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_LTE](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EHRPD](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPAP](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_GSM](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_TD_SCDMA](../android/telephony/TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_IWLAN](../android/telephony/TelephonyManager.md), or [android.telephony.TelephonyManager#NETWORK_TYPE_NR](../android/telephony/TelephonyManager.md) |

**See Also**

- [android.telephony.TelephonyManager#DATA_DISCONNECTED](../android/telephony/TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_CONNECTING](../android/telephony/TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_CONNECTED](../android/telephony/TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_SUSPENDED](../android/telephony/TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_HANDOVER_IN_PROGRESS](../android/telephony/TelephonyManager.md)
