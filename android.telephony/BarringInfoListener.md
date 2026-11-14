# TelephonyCallback.BarringInfoListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BarringInfoListener

Kotlin| [Java](../android/telephony/TelephonyCallback.BarringInfoListener.md) 
| --- | --- |

```
interface BarringInfoListener
```

| [android.telephony.TelephonyCallback.BarringInfoListener](../android/telephony/TelephonyCallback.BarringInfoListener.md) |

Interface for barring information listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBarringInfoChanged](../android/telephony/TelephonyCallback.BarringInfoListener.md))`(`barringInfo:` ` [BarringInfo](BarringInfo.md)`)` Report updated barring information for the current camped/registered cell. |

## Public methods

### onBarringInfoChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBarringInfoChanged(barringInfo: BarringInfo): Unit
```

Report updated barring information for the current camped/registered cell.

Barring info is provided for all services applicable to the current camped/registered cell, for the registered PLMN and current access class/access category. The calling app should have carrier privileges (see [TelephonyManager.hasCarrierPrivileges](TelephonyManager.md))) if it does not have the [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md). If the calling app doesn't have [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md), it will receive [BarringInfo](BarringInfo.md) including [CellIdentity](CellIdentity.md) without location-sensitive information included. 
Requires [android.Manifest.permission#READ_PRECISE_PHONE_STATE](../android/Manifest.permission.md) and [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `barringInfo` | [BarringInfo](BarringInfo.md):for all services on the current cell. This value cannot be`null`. |

**See Also**

- [android.telephony.BarringInfo](BarringInfo.md)
