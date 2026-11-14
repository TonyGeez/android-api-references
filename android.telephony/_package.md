# android.telephony

# android.telephony

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [CarrierConfigChangeListener](../android/telephony/CarrierConfigManager.CarrierConfigChangeListener.md) | Listener interface to get a notification when the carrier configurations have changed. |
| --- | --- |
| [ActiveDataSubscriptionIdListener](../android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener.md) | Interface for active data subscription ID listener. |
| [BarringInfoListener](../android/telephony/TelephonyCallback.BarringInfoListener.md) | Interface for barring information listener. |
| [CallDisconnectCauseListener](../android/telephony/TelephonyCallback.CallDisconnectCauseListener.md) | Interface for call disconnect cause listener. |
| --- | --- |
| [CallForwardingIndicatorListener](../android/telephony/TelephonyCallback.CallForwardingIndicatorListener.md) | Interface for call-forwarding indicator listener. |
| [CallStateListener](../android/telephony/TelephonyCallback.CallStateListener.md) | Interface for call state listener. |
| [CarrierNetworkListener](../android/telephony/TelephonyCallback.CarrierNetworkListener.md) | Interface for carrier network listener. |
| --- | --- |
| [CellInfoListener](../android/telephony/TelephonyCallback.CellInfoListener.md) | Interface for cell info listener. |
| [CellLocationListener](../android/telephony/TelephonyCallback.CellLocationListener.md) | Interface for device cell location listener. |
| [DataActivationStateListener](../android/telephony/TelephonyCallback.DataActivationStateListener.md) | Interface for SIM data activation state listener. |
| --- | --- |
| [DataActivityListener](../android/telephony/TelephonyCallback.DataActivityListener.md) | Interface for data activity state listener. |
| [DataConnectionStateListener](../android/telephony/TelephonyCallback.DataConnectionStateListener.md) | Interface for data connection state listener. |
| [DisplayInfoListener](../android/telephony/TelephonyCallback.DisplayInfoListener.md) | Interface for display info listener. |
| --- | --- |
| [EmergencyNumberListListener](../android/telephony/TelephonyCallback.EmergencyNumberListListener.md) | Interface for the current emergency number list listener. |
| [ImsCallDisconnectCauseListener](../android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener.md) | Interface for IMS call disconnect cause listener. |
| [MessageWaitingIndicatorListener](../android/telephony/TelephonyCallback.MessageWaitingIndicatorListener.md) | Interface for message waiting indicator listener. |
| --- | --- |
| [PhysicalChannelConfigListener](../android/telephony/TelephonyCallback.PhysicalChannelConfigListener.md) | Interface for current physical channel configuration listener. |
| [PreciseDataConnectionStateListener](../android/telephony/TelephonyCallback.PreciseDataConnectionStateListener.md) | Interface for precise data connection state listener. |
| [RegistrationFailedListener](../android/telephony/TelephonyCallback.RegistrationFailedListener.md) | Interface for registration failures listener. |
| --- | --- |
| [ServiceStateListener](../android/telephony/TelephonyCallback.ServiceStateListener.md) | Interface for service state listener. |
| [SignalStrengthsListener](../android/telephony/TelephonyCallback.SignalStrengthsListener.md) | Interface for network signal strengths listener. |
| [UserMobileDataStateListener](../android/telephony/TelephonyCallback.UserMobileDataStateListener.md) | Interface for user mobile data state listener. |
| --- | --- |

## Classes

| [AccessNetworkConstants](AccessNetworkConstants.md) | Contains access network related constants. |
| --- | --- |
| [AvailableNetworkInfo](AvailableNetworkInfo.md) | Defines available network information which includes corresponding subscription id, network plmns and corresponding priority to be used for network selection by Opportunistic Network Service when passed through [TelephonyManager.updateAvailableNetworks](TelephonyManager.md)) |
| [BarringInfo](BarringInfo.md) | Provides the barring configuration for a particular service type. |
| [CarrierConfigManager](CarrierConfigManager.md) | Provides access to telephony configuration values that are carrier-specific. |
| --- | --- |
| [CellIdentity](CellIdentity.md) | CellIdentity represents the identity of a unique cell. |
| [CellIdentityCdma](CellIdentityCdma.md) | CellIdentity is to represent a unique CDMA cell |
| [CellIdentityGsm](CellIdentityGsm.md) | CellIdentity to represent a unique GSM cell |
| --- | --- |
| [CellIdentityLte](CellIdentityLte.md) | CellIdentity is to represent a unique LTE cell |
| [CellIdentityNr](CellIdentityNr.md) | Information to represent a unique NR(New Radio 5G) cell. |
| [CellIdentityTdscdma](CellIdentityTdscdma.md) | CellIdentity is to represent a unique TD-SCDMA cell |
| --- | --- |
| [CellIdentityWcdma](CellIdentityWcdma.md) | CellIdentity to represent a unique UMTS cell |
| [CellInfo](CellInfo.md) | Immutable cell information from a point in time. |
| [CellInfoCdma](CellInfoCdma.md) | A [CellInfo](CellInfo.md) representing a CDMA cell that provides identity and measurement info. |
| --- | --- |
| [CellInfoGsm](CellInfoGsm.md) | A [CellInfo](CellInfo.md) representing a GSM cell that provides identity and measurement info. |
| [CellInfoLte](CellInfoLte.md) | A [CellInfo](CellInfo.md) representing an LTE cell that provides identity and measurement info. |
| [CellInfoNr](CellInfoNr.md) | A [CellInfo](CellInfo.md) representing an 5G NR cell that provides identity and measurement info. |
| --- | --- |
| [CellInfoTdscdma](CellInfoTdscdma.md) | A [CellInfo](CellInfo.md) representing a TD-SCDMA cell that provides identity and measurement info. |
| [CellInfoWcdma](CellInfoWcdma.md) | A [CellInfo](CellInfo.md) representing a WCDMA cell that provides identity and measurement info. |
| [CellLocation](CellLocation.md) | Abstract class that represents the location of the device. |
| --- | --- |
| [CellSignalStrength](CellSignalStrength.md) | Abstract base class for cell phone signal strength related information. |
| [CellSignalStrengthCdma](CellSignalStrengthCdma.md) | Signal strength related information. |
| [CellSignalStrengthGsm](CellSignalStrengthGsm.md) | GSM signal strength related information. |
| --- | --- |
| [CellSignalStrengthLte](CellSignalStrengthLte.md) | LTE signal strength related information. |
| [CellSignalStrengthNr](CellSignalStrengthNr.md) | 5G NR signal strength related information. |
| [CellSignalStrengthTdscdma](CellSignalStrengthTdscdma.md) | Tdscdma signal strength related information. |
| --- | --- |
| [CellSignalStrengthWcdma](CellSignalStrengthWcdma.md) | Wcdma signal strength related information. |
| [ClosedSubscriberGroupInfo](ClosedSubscriberGroupInfo.md) | Information to represent a closed subscriber group. |
| [DataFailCause](DataFailCause.md) | DataFailCause collects data connection failure causes code from different sources. |
| --- | --- |
| [DisconnectCause](DisconnectCause.md) | Describes the cause of a disconnected call. |
| [IccOpenLogicalChannelResponse](IccOpenLogicalChannelResponse.md) | Response to the android. |
| [MbmsDownloadSession](MbmsDownloadSession.md) | This class provides functionality for file download over MBMS. |
| --- | --- |
| [MbmsGroupCallSession](MbmsGroupCallSession.md) | This class provides functionality for accessing group call functionality over MBMS. |
| [MbmsStreamingSession](MbmsStreamingSession.md) | This class provides functionality for streaming media over MBMS. |
| [NeighboringCellInfo](NeighboringCellInfo.md) | Represents the neighboring cell information, including Received Signal Strength and Cell ID location. |
| --- | --- |
| [NetworkRegistrationInfo](NetworkRegistrationInfo.md) | Description of a mobile network registration info |
| [NetworkScan](NetworkScan.md) | The caller of android. |
| [NetworkScanRequest](NetworkScanRequest.md) | Defines a request to perform a network scan. |
| --- | --- |
| [ParsedPhoneNumber](ParsedPhoneNumber.md) | Handles the results from PhoneNumberManager by providing Phone number, error code, and is valid number. |
| [PhoneNumberFormattingTextWatcher](PhoneNumberFormattingTextWatcher.md) | Watches a [android.widget.TextView](../android.widget/TextView.md) and if a phone number is entered will format it. |
| [PhoneNumberManager](PhoneNumberManager.md) | PhoneNumberManager provides APIs for parsing phone numbers from various sources, such as URIs. |
| --- | --- |
| [PhoneNumberUtils](PhoneNumberUtils.md) | Various utilities for dealing with phone number strings. |
| [PhoneStateListener](PhoneStateListener.md) | A listener class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others. |
| [PhysicalChannelConfig](PhysicalChannelConfig.md) | <br /> |
| --- | --- |
| [PreciseDataConnectionState](PreciseDataConnectionState.md) | Contains precise data connection state. |
| [RadioAccessSpecifier](RadioAccessSpecifier.md) | Describes a particular radio access network to be scanned. |
| [ServiceState](ServiceState.md) | Contains phone state and service related information. |
| --- | --- |
| [SignalStrength](SignalStrength.md) | Contains phone signal strength related information. |
| [SignalStrengthUpdateRequest](SignalStrengthUpdateRequest.md) | Request used to register [SignalThresholdInfo](SignalThresholdInfo.md) to be notified when the signal strength breach the specified thresholds. |
| [SignalThresholdInfo](SignalThresholdInfo.md) | Defines the threshold value of the signal strength. |
| --- | --- |
| [SmsManager](SmsManager.md) | Manages SMS operations such as sending data, text, and pdu SMS messages. |
| [SmsMessage](SmsMessage.md) | A Short Message Service message. |
| [SubscriptionInfo](SubscriptionInfo.md) | A Parcelable class for Subscription Information. |
| --- | --- |
| [SubscriptionManager](SubscriptionManager.md) | Subscription manager provides the mobile subscription information. |
| [SubscriptionPlan](SubscriptionPlan.md) | Description of a billing relationship plan between a carrier and a specific subscriber. |
| [TelephonyCallback](TelephonyCallback.md) | A callback class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others. |
| --- | --- |
| [TelephonyDisplayInfo](TelephonyDisplayInfo.md) | TelephonyDisplayInfo contains telephony-related information used for display purposes only. |
| [TelephonyManager](TelephonyManager.md) | Provides access to information about the telephony services on the device. |
| [TelephonyScanManager](TelephonyScanManager.md) | Manages the radio access network scan requests and callbacks. |
| --- | --- |
| [UiccCardInfo](UiccCardInfo.md) | The UiccCardInfo represents information about a currently inserted UICC or embedded eUICC. |
| [UiccPortInfo](UiccPortInfo.md) | UiccPortInfo class represents information about a single port contained on [UiccCardInfo](UiccCardInfo.md). |
| [VisualVoicemailService](VisualVoicemailService.md) | This service is implemented by dialer apps that wishes to handle OMTP or similar visual voicemails. |
| --- | --- |
| [VisualVoicemailSms](VisualVoicemailSms.md) | Represents the content of a visual voicemail SMS. |
| [VisualVoicemailSmsFilterSettings](VisualVoicemailSmsFilterSettings.md) | Class to represent various settings for the visual voicemail SMS filter. |
