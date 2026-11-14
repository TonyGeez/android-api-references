# TelephonyCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TelephonyCallback

Kotlin| [Java](https://developer.android.com/reference/android/telephony/TelephonyCallback "View this page in Java") 

```
open class TelephonyCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.TelephonyCallback](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback#) |

A callback class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others.

To register a callback, use a [TelephonyCallback](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback#) which implements interfaces regarding EVENT_\*. For example, FakeServiceStateCallback extends [TelephonyCallback](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback#) implements [TelephonyCallback.ServiceStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener).

Then override the methods for the state that you wish to receive updates for, and pass the executor and your TelephonyCallback object to android.telephony.TelephonyManager#registerTelephonyCallback. Methods are called when the state changes, as well as once on initial registration.

Note that access to some telephony information is permission-protected. Your application won't receive updates for protected information unless it has the appropriate permissions declared in its manifest file. Where permissions apply, they are noted in the appropriate sub-interfaces.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ActiveDataSubscriptionIdListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener) Interface for active data subscription ID listener. |
| abstract | [BarringInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.BarringInfoListener) Interface for barring information listener. |
| abstract | [CallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallDisconnectCauseListener) Interface for call disconnect cause listener. |
| abstract | [CallForwardingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallForwardingIndicatorListener) Interface for call-forwarding indicator listener. |
| abstract | [CallStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallStateListener) Interface for call state listener. |
| abstract | [CarrierNetworkListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CarrierNetworkListener) Interface for carrier network listener. |
| abstract | [CellInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellInfoListener) Interface for cell info listener. |
| abstract | [CellLocationListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellLocationListener) Interface for device cell location listener. |
| abstract | [DataActivationStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataActivationStateListener) Interface for SIM data activation state listener. |
| abstract | [DataActivityListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataActivityListener) Interface for data activity state listener. |
| abstract | [DataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataConnectionStateListener) Interface for data connection state listener. |
| abstract | [DisplayInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DisplayInfoListener) Interface for display info listener. |
| abstract | [EmergencyNumberListListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.EmergencyNumberListListener) Interface for the current emergency number list listener. |
| abstract | [ImsCallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener) Interface for IMS call disconnect cause listener. |
| abstract | [MessageWaitingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.MessageWaitingIndicatorListener) Interface for message waiting indicator listener. |
| abstract | [PhysicalChannelConfigListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PhysicalChannelConfigListener) Interface for current physical channel configuration listener. |
| abstract | [PreciseDataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PreciseDataConnectionStateListener) Interface for precise data connection state listener. |
| abstract | [RegistrationFailedListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.RegistrationFailedListener) Interface for registration failures listener. |
| abstract | [ServiceStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener) Interface for service state listener. |
| abstract | [SignalStrengthsListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.SignalStrengthsListener) Interface for network signal strengths listener. |
| abstract | [UserMobileDataStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.UserMobileDataStateListener) Interface for user mobile data state listener. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------|---|
| [TelephonyCallback](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback#TelephonyCallback())`()` <br /> |

## Public constructors

### TelephonyCallback

```
TelephonyCallback()
```
