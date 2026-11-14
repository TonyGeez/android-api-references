Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsCallDisconnectCauseListener

Kotlin | [Java](../android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener.md)
| --- | --- |

```
interface ImsCallDisconnectCauseListener
```

| [android.telephony.TelephonyCallback.ImsCallDisconnectCauseListener](../android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener.md) |

Interface for IMS call disconnect cause listener.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onImsCallDisconnectCauseChanged Callback invoked when IMS call disconnect cause changes on the registered subscription. |

## Public methods

### onImsCallDisconnectCauseChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onImsCallDisconnectCauseChanged(imsReasonInfo: ImsReasonInfo): Unit
```

Callback invoked when IMS call disconnect cause changes on the registered subscription. Note, the registration subscription ID comes from TelephonyManager object which registers TelephonyCallback by registerTelephonyCallback. If this TelephonyManager object was created with createForSubscriptionId, then the callback applies to the subscription ID. Otherwise, this callback applies to getDefaultSubscriptionId. The calling app should have carrier privileges (see hasCarrierPrivileges) if it does not have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `imsReasonInfo` | [ImsReasonInfo](../android.telephony.ims/ImsReasonInfo.md): ImsReasonInfo contains details on why IMS call failed. This value cannot be `null`. |
