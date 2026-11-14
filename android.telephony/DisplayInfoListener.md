# TelephonyCallback.DisplayInfoListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayInfoListener

Kotlin | [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.DisplayInfoListener "View this page in Java") 
| --- | --- |

```
interface DisplayInfoListener
```

| [android.telephony.TelephonyCallback.DisplayInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DisplayInfoListener#) |

Interface for display info listener.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayInfoChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DisplayInfoListener#onDisplayInfoChanged(android.telephony.TelephonyDisplayInfo))`(`telephonyDisplayInfo:` ` [TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo)`)` Callback invoked when the display info has changed on the registered subscription. |

## Public methods

### onDisplayInfoChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayInfoChanged(telephonyDisplayInfo: TelephonyDisplayInfo): Unit
```

Callback invoked when the display info has changed on the registered subscription.

The [TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo) contains status information shown to the user based on carrier policy.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `telephonyDisplayInfo` | [TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo): The display information. This value cannot be `null`. |
