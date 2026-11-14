# TelephonyCallback.DisplayInfoListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayInfoListener

Kotlin | [Java](../android/telephony/TelephonyCallback.DisplayInfoListener.md) 
| --- | --- |

```
interface DisplayInfoListener
```

| [android.telephony.TelephonyCallback.DisplayInfoListener](../android/telephony/TelephonyCallback.DisplayInfoListener.md) |

Interface for display info listener.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayInfoChanged](../android/telephony/TelephonyCallback.DisplayInfoListener.md))`(`telephonyDisplayInfo:` ` [TelephonyDisplayInfo](TelephonyDisplayInfo.md)`)` Callback invoked when the display info has changed on the registered subscription. |

## Public methods

### onDisplayInfoChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayInfoChanged(telephonyDisplayInfo: TelephonyDisplayInfo): Unit
```

Callback invoked when the display info has changed on the registered subscription.

The [TelephonyDisplayInfo](TelephonyDisplayInfo.md) contains status information shown to the user based on carrier policy.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `telephonyDisplayInfo` | [TelephonyDisplayInfo](TelephonyDisplayInfo.md): The display information. This value cannot be `null`. |
