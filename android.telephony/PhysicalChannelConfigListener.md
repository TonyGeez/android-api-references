# TelephonyCallback.PhysicalChannelConfigListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhysicalChannelConfigListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.PhysicalChannelConfigListener "View this page in Java") 

```
interface PhysicalChannelConfigListener
```

| [android.telephony.TelephonyCallback.PhysicalChannelConfigListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PhysicalChannelConfigListener#) |

Interface for current physical channel configuration listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPhysicalChannelConfigChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PhysicalChannelConfigListener#onPhysicalChannelConfigChanged(kotlin.collections.MutableList))`(`configs:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PhysicalChannelConfig](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig)!>`)` Callback invoked when the current physical channel configuration has changed The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String). |

## Public methods

### onPhysicalChannelConfigChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPhysicalChannelConfigChanged(configs: MutableList<PhysicalChannelConfig!>): Unit
```

Callback invoked when the current physical channel configuration has changed The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String). 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String)

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PhysicalChannelConfig](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig)!\>:List of the current [PhysicalChannelConfig](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig) s This value cannot be`null`. |
