# TelephonyCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TelephonyCallback

Kotlin| [Java](TelephonyCallback.md) 
| --- | --- |

```
open class TelephonyCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.TelephonyCallback](TelephonyCallback.md) |

A callback class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others.

To register a callback, use a [TelephonyCallback](TelephonyCallback.md) which implements interfaces regarding EVENT_\*. For example, FakeServiceStateCallback extends [TelephonyCallback](TelephonyCallback.md) implements [TelephonyCallback.ServiceStateListener](../android/telephony/TelephonyCallback.ServiceStateListener.md).

Then override the methods for the state that you wish to receive updates for, and pass the executor and your TelephonyCallback object to android.telephony.TelephonyManager#registerTelephonyCallback. Methods are called when the state changes, as well as once on initial registration.

Note that access to some telephony information is permission-protected. Your application won't receive updates for protected information unless it has the appropriate permissions declared in its manifest file. Where permissions apply, they are noted in the appropriate sub-interfaces.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ActiveDataSubscriptionIdListener](../android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener.md) Interface for active data subscription ID listener. |
| abstract | [BarringInfoListener](../android/telephony/TelephonyCallback.BarringInfoListener.md) Interface for barring information listener. |
| abstract | [CallDisconnectCauseListener](../android/telephony/TelephonyCallback.CallDisconnectCauseListener.md) Interface for call disconnect cause listener. |
| --- | --- |
| abstract | [CallForwardingIndicatorListener](../android/telephony/TelephonyCallback.CallForwardingIndicatorListener.md) Interface for call-forwarding indicator listener. |
| abstract | [CallStateListener](../android/telephony/TelephonyCallback.CallStateListener.md) Interface for call state listener. |
| abstract | [CarrierNetworkListener](../android/telephony/TelephonyCallback.CarrierNetworkListener.md) Interface for carrier network listener. |
| --- | --- |
| abstract | [CellInfoListener](../android/telephony/TelephonyCallback.CellInfoListener.md) Interface for cell info listener. |
| abstract | [CellLocationListener](../android/telephony/TelephonyCallback.CellLocationListener.md) Interface for device cell location listener. |
| abstract | [DataActivationStateListener](../android/telephony/TelephonyCallback.DataActivationStateListener.md) Interface for SIM data activation state listener. |
| --- | --- |
| abstract | [DataActivityListener](../android/telephony/TelephonyCallback.DataActivityListener.md) Interface for data activity state listener. |
| abstract | [DataConnectionStateListener](../android/telephony/TelephonyCallback.DataConnectionStateListener.md) Interface for data connection state listener. |
| abstract | [DisplayInfoListener](../android/telephony/TelephonyCallback.DisplayInfoListener.md) Interface for display info listener. |
| --- | --- |
| abstract | [EmergencyNumberListListener](../android/telephony/TelephonyCallback.EmergencyNumberListListener.md) Interface for the current emergency number list listener. |
| abstract | [ImsCallDisconnectCauseListener](../android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener.md) Interface for IMS call disconnect cause listener. |
| abstract | [MessageWaitingIndicatorListener](../android/telephony/TelephonyCallback.MessageWaitingIndicatorListener.md) Interface for message waiting indicator listener. |
| --- | --- |
| abstract | [PhysicalChannelConfigListener](../android/telephony/TelephonyCallback.PhysicalChannelConfigListener.md) Interface for current physical channel configuration listener. |
| abstract | [PreciseDataConnectionStateListener](../android/telephony/TelephonyCallback.PreciseDataConnectionStateListener.md) Interface for precise data connection state listener. |
| abstract | [RegistrationFailedListener](../android/telephony/TelephonyCallback.RegistrationFailedListener.md) Interface for registration failures listener. |
| --- | --- |
| abstract | [ServiceStateListener](../android/telephony/TelephonyCallback.ServiceStateListener.md) Interface for service state listener. |
| abstract | [SignalStrengthsListener](../android/telephony/TelephonyCallback.SignalStrengthsListener.md) Interface for network signal strengths listener. |
| abstract | [UserMobileDataStateListener](../android/telephony/TelephonyCallback.UserMobileDataStateListener.md) Interface for user mobile data state listener. |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------|---|
| [TelephonyCallback](TelephonyCallback.md))`()` <br /> |

## Public constructors

### TelephonyCallback

```
TelephonyCallback()
```
