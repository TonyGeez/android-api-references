Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellInfoListener

Kotlin | [Java](../android/telephony/TelephonyCallback.CellInfoListener.md)
| --- | --- |

```
interface CellInfoListener
```

| [android.telephony.TelephonyCallback.CellInfoListener](../android/telephony/TelephonyCallback.CellInfoListener.md) |

Interface for cell info listener.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellInfoListener#onCellInfoChanged(kotlin.collections.MutableList)(cellInfo: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/CellInfo!>)` Callback invoked when an observed cell info has changed or new cells have been added or removed on the registered subscription. |

## Public methods

### onCellInfoChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onCellInfoChanged(cellInfo: MutableList<CellInfo!>): Unit
```

Callback invoked when an observed cell info has changed or new cells have been added or removed on the registered subscription. Note, the registration subscription ID s from `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager` object which registers TelephonyCallback by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)`. If this TelephonyManager object was created with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)`, then the callback applies to the subscription ID. Otherwise, this callback applies to `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`

| Parameters ||
|---|---|
| `cellInfo` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CellInfo](../android/telephony/CellInfo.md)!\>: is the list of currently visible cells. This value cannot be `null`. |
