# TelephonyCallback.BarringInfoListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BarringInfoListener

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.BarringInfoListener "View this page in Java") 
| --- | --- |

```
interface BarringInfoListener
```

| [android.telephony.TelephonyCallback.BarringInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.BarringInfoListener#) |

Interface for barring information listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBarringInfoChanged](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.BarringInfoListener#onBarringInfoChanged(android.telephony.BarringInfo))`(`barringInfo:` ` [BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo)`)` Report updated barring information for the current camped/registered cell. |

## Public methods

### onBarringInfoChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBarringInfoChanged(barringInfo: BarringInfo): Unit
```

Report updated barring information for the current camped/registered cell.

Barring info is provided for all services applicable to the current camped/registered cell, for the registered PLMN and current access class/access category. The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges())) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String). If the calling app doesn't have [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String), it will receive [BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo) including [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity) without location-sensitive information included. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String) and [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `barringInfo` | [BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo):for all services on the current cell. This value cannot be`null`. |

**See Also**

- [android.telephony.BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo)
