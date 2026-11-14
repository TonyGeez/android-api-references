# TelephonyCallback.DataActivationStateListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataActivationStateListener

Kotlin| [Java](../android/telephony/TelephonyCallback.DataActivationStateListener.md) 
| --- | --- |

```
interface DataActivationStateListener
```

| [android.telephony.TelephonyCallback.DataActivationStateListener](../android/telephony/TelephonyCallback.DataActivationStateListener.md) |

Interface for SIM data activation state listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDataActivationStateChanged](../android/telephony/TelephonyCallback.DataActivationStateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback invoked when the SIM data activation state has changed on the registered subscription. |

## Public methods

### onDataActivationStateChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDataActivationStateChanged(state: Int): Unit
```

Callback invoked when the SIM data activation state has changed on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the current SIM data activation state Value is android.telephony.TelephonyManager.SIM_ACTIVATION_STATE_UNKNOWN, android.telephony.TelephonyManager.SIM_ACTIVATION_STATE_ACTIVATING, android.telephony.TelephonyManager.SIM_ACTIVATION_STATE_ACTIVATED, android.telephony.TelephonyManager.SIM_ACTIVATION_STATE_DEACTIVATED, or android.telephony.TelephonyManager.SIM_ACTIVATION_STATE_RESTRICTED |
