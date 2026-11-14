# TelephonyCallback.PhysicalChannelConfigListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhysicalChannelConfigListener

Kotlin| [Java](../android/telephony/TelephonyCallback.PhysicalChannelConfigListener.md) 
| --- | --- |

```
interface PhysicalChannelConfigListener
```

| [android.telephony.TelephonyCallback.PhysicalChannelConfigListener](../android/telephony/TelephonyCallback.PhysicalChannelConfigListener.md) |

Interface for current physical channel configuration listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPhysicalChannelConfigChanged](../android/telephony/TelephonyCallback.PhysicalChannelConfigListener.md))`(`configs:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PhysicalChannelConfig](PhysicalChannelConfig.md)!>`)` Callback invoked when the current physical channel configuration has changed The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md). |

## Public methods

### onPhysicalChannelConfigChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPhysicalChannelConfigChanged(configs: MutableList<PhysicalChannelConfig!>): Unit
```

Callback invoked when the current physical channel configuration has changed The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md)

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PhysicalChannelConfig](PhysicalChannelConfig.md)!\>:List of the current [PhysicalChannelConfig](PhysicalChannelConfig.md) s This value cannot be`null`. |
