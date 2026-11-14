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

Callback invoked when connection state changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the current state of data connection. Value is [android.telephony.TelephonyManager#DATA_UNKNOWN](TelephonyManager.md), [android.telephony.TelephonyManager#DATA_DISCONNECTED](TelephonyManager.md), [android.telephony.TelephonyManager#DATA_CONNECTING](TelephonyManager.md), [android.telephony.TelephonyManager#DATA_CONNECTED](TelephonyManager.md), [android.telephony.TelephonyManager#DATA_SUSPENDED](TelephonyManager.md), [android.telephony.TelephonyManager#DATA_DISCONNECTING](TelephonyManager.md), or [android.telephony.TelephonyManager#DATA_HANDOVER_IN_PROGRESS](TelephonyManager.md) |
| `networkType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the current network type of data connection. Value is [android.telephony.TelephonyManager#NETWORK_TYPE_UNKNOWN](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_GPRS](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EDGE](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_UMTS](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_CDMA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_0](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_A](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_1xRTT](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSDPA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSUPA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_IDEN](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_B](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_LTE](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EHRPD](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPAP](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_GSM](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_TD_SCDMA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_IWLAN](TelephonyManager.md), or [android.telephony.TelephonyManager#NETWORK_TYPE_NR](TelephonyManager.md) |

**See Also**

- [android.telephony.TelephonyManager#DATA_DISCONNECTED](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_CONNECTING](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_CONNECTED](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_SUSPENDED](TelephonyManager.md)
- [android.telephony.TelephonyManager#DATA_HANDOVER_IN_PROGRESS](TelephonyManager.md)
