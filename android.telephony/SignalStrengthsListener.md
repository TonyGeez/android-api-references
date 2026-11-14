# TelephonyCallback.SignalStrengthsListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalStrengthsListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.SignalStrengthsListener "View this page in Java") 
| --- | --- |

```
interface SignalStrengthsListener
```

| [android.telephony.TelephonyCallback.SignalStrengthsListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.SignalStrengthsListener#) |

Interface for network signal strengths listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSignalStrengthsChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.SignalStrengthsListener#onSignalStrengthsChanged(android.telephony.SignalStrength))`(`signalStrength:` ` [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength)`)` Callback invoked when network signal strengths changes on the registered subscription. |

## Public methods

### onSignalStrengthsChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSignalStrengthsChanged(signalStrength: SignalStrength): Unit
```

Callback invoked when network signal strengths changes on the registered subscription. Note, the registration subscription ID comes from [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) object which registers TelephonyCallback by [TelephonyManager.registerTelephonyCallback(Executor, TelephonyCallback)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)). If this TelephonyManager object was created with [TelephonyManager.createForSubscriptionId(int)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)), then the callback applies to the subscription ID. Otherwise, this callback applies to [SubscriptionManager.getDefaultSubscriptionId()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()).

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `signalStrength` | [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength):This value cannot be`null`. |
