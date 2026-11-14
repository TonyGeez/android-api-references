Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsCallDisconnectCauseListener

Kotlin | [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener "View this page in Java")

```
interface ImsCallDisconnectCauseListener
```

| [android.telephony.TelephonyCallback.ImsCallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener#) |

Interface for IMS call disconnect cause listener.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener#onImsCallDisconnectCauseChanged(android.telephony.ims.ImsReasonInfo)(imsReasonInfo: https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo)` Callback invoked when IMS call disconnect cause changes on the registered subscription. |

## Public methods

### onImsCallDisconnectCauseChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onImsCallDisconnectCauseChanged(imsReasonInfo: ImsReasonInfo): Unit
```

Callback invoked when IMS call disconnect cause changes on the registered subscription. Note, the registration subscription ID comes from `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager` object which registers TelephonyCallback by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#registerTelephonyCallback(java.util.concurrent.Executor,%20android.telephony.TelephonyCallback)`. If this TelephonyManager object was created with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#createForSubscriptionId(kotlin.Int)`, then the callback applies to the subscription ID. Otherwise, this callback applies to `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#getDefaultSubscriptionId()`. The calling app should have carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#hasCarrierPrivileges()`) if it does not have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `imsReasonInfo` | [ImsReasonInfo](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo): `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsReasonInfo` contains details on why IMS call failed. This value cannot be `null`. |
