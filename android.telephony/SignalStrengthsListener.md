# TelephonyCallback.SignalStrengthsListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalStrengthsListener

Kotlin| [Java](../android/telephony/TelephonyCallback.SignalStrengthsListener.md) 
| --- | --- |

```
interface SignalStrengthsListener
```

| [android.telephony.TelephonyCallback.SignalStrengthsListener](../android/telephony/TelephonyCallback.SignalStrengthsListener.md) |

Interface for network signal strengths listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSignalStrengthsChanged](../android/telephony/TelephonyCallback.SignalStrengthsListener.md))`(`signalStrength:` ` [SignalStrength](SignalStrength.md)`)` Callback invoked when network signal strengths changes on the registered subscription. |

## Public methods

### onSignalStrengthsChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSignalStrengthsChanged(signalStrength: SignalStrength): Unit
```

Callback invoked when network signal strengths changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](TelephonyManager.md) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](TelephonyManager.md)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](TelephonyManager.md)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](SubscriptionManager.md)).

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `signalStrength` | [SignalStrength](SignalStrength.md):This value cannot be`null`. |
