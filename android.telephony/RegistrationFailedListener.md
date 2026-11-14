Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RegistrationFailedListener

Kotlin | [Java](../android/telephony/TelephonyCallback.RegistrationFailedListener.md)
| --- | --- |

```
interface RegistrationFailedListener
```

| [android.telephony.TelephonyCallback.RegistrationFailedListener](../android/telephony/TelephonyCallback.RegistrationFailedListener.md) |

Interface for registration failures listener.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRegistrationFailed Report that Registration or a Location/Routing/Tracking Area update has failed. |

## Public methods

### onRegistrationFailed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onRegistrationFailed(
    cellIdentity: CellIdentity, 
    chosenPlmn: String, 
    domain: Int, 
    causeCode: Int, 
    additionalCauseCode: Int
): Unit
```

Report that Registration or a Location/Routing/Tracking Area update has failed.

Indicate whenever a registration procedure, including a location, routing, or tracking area update fails. This includes procedures that do not necessarily result in a change of the modem's registration status. If the modem's registration status changes, that is reflected in the onNetworkStateChanged() and subsequent get{Voice/Data}RegistrationState().

Because registration failures are ephemeral, this callback is not sticky. Registrants will not receive the most recent past value when registering. The calling app should have carrier privileges (see hasCarrierPrivileges) if it does not have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If the calling app doesn't have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`, it will receive CellIdentity without location-sensitive information included. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`

| Parameters ||
|---|---|
| `cellIdentity` | [CellIdentity](CellIdentity.md): the CellIdentity, which must include the globally unique identifier for the cell (for example, all components of the CGI or ECGI). This value cannot be `null`. |
| `chosenPlmn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): a 5 or 6 digit alphanumeric PLMN (MCC|MNC) among those broadcast by the cell that was chosen for the failed registration attempt. This value cannot be `null`. |
| `domain` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): DOMAIN_CS, DOMAIN_PS or both in case of a combined procedure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_CS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_PS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_CS_PS:kotlin.Int` |
| --- | --- |
| `causeCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the primary failure cause code of the procedure. For GSM/UMTS (MM), values are in TS 24.008 Sec 10.5.95 For GSM/UMTS (GMM), values are in TS 24.008 Sec 10.5.147 For LTE (EMM), cause codes are TS 24.301 Sec 9.9.3.9 For NR (5GMM), cause codes are TS 24.501 Sec 9.11.3.2 Integer.MAX_VALUE if this value is unused. |
| `additionalCauseCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cause code of any secondary/combined procedure if appropriate. For UMTS, if a combined attach succeeds for PS only, then the GMM cause code shall be included as an additionalCauseCode. For LTE (ESM), cause codes are in TS 24.301 9.9.4.4. Integer.MAX_VALUE if this value is unused. |
