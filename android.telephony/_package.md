# android.telephony

# android.telephony

Kotlin| [Java](../android/telephony/_package.md)
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

| [AccessNetworkConstants](../android/telephony/AccessNetworkConstants.md) | Contains access network related constants. |
| --- | --- |
| [AvailableNetworkInfo](../android/telephony/AvailableNetworkInfo.md) | Defines available network information which includes corresponding subscription id, network plmns and corresponding priority to be used for network selection by Opportunistic Network Service when passed through [TelephonyManager.updateAvailableNetworks](../android/telephony/TelephonyManager.md)) |
| [BarringInfo](../android/telephony/BarringInfo.md) | Provides the barring configuration for a particular service type. |
| [CarrierConfigManager](../android/telephony/CarrierConfigManager.md) | Provides access to telephony configuration values that are carrier-specific. |
| --- | --- |
| [CellIdentity](../android/telephony/CellIdentity.md) | CellIdentity represents the identity of a unique cell. |
| [CellIdentityCdma](../android/telephony/CellIdentityCdma.md) | CellIdentity is to represent a unique CDMA cell |
| [CellIdentityGsm](../android/telephony/CellIdentityGsm.md) | CellIdentity to represent a unique GSM cell |
| --- | --- |
| [CellIdentityLte](../android/telephony/CellIdentityLte.md) | CellIdentity is to represent a unique LTE cell |
| [CellIdentityNr](../android/telephony/CellIdentityNr.md) | Information to represent a unique NR(New Radio 5G) cell. |
| [CellIdentityTdscdma](../android/telephony/CellIdentityTdscdma.md) | CellIdentity is to represent a unique TD-SCDMA cell |
| --- | --- |
| [CellIdentityWcdma](../android/telephony/CellIdentityWcdma.md) | CellIdentity to represent a unique UMTS cell |
| [CellInfo](../android/telephony/CellInfo.md) | Immutable cell information from a point in time. |
| [CellInfoCdma](../android/telephony/CellInfoCdma.md) | A [CellInfo](../android/telephony/CellInfo.md) representing a CDMA cell that provides identity and measurement info. |
| --- | --- |
| [CellInfoGsm](../android/telephony/CellInfoGsm.md) | A [CellInfo](../android/telephony/CellInfo.md) representing a GSM cell that provides identity and measurement info. |
| [CellInfoLte](../android/telephony/CellInfoLte.md) | A [CellInfo](../android/telephony/CellInfo.md) representing an LTE cell that provides identity and measurement info. |
| [CellInfoNr](../android/telephony/CellInfoNr.md) | A [CellInfo](../android/telephony/CellInfo.md) representing an 5G NR cell that provides identity and measurement info. |
| --- | --- |
| [CellInfoTdscdma](../android/telephony/CellInfoTdscdma.md) | A [CellInfo](../android/telephony/CellInfo.md) representing a TD-SCDMA cell that provides identity and measurement info. |
| [CellInfoWcdma](../android/telephony/CellInfoWcdma.md) | A [CellInfo](../android/telephony/CellInfo.md) representing a WCDMA cell that provides identity and measurement info. |
| [CellLocation](../android/telephony/CellLocation.md) | Abstract class that represents the location of the device. |
| --- | --- |
| [CellSignalStrength](../android/telephony/CellSignalStrength.md) | Abstract base class for cell phone signal strength related information. |
| [CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md) | Signal strength related information. |
| [CellSignalStrengthGsm](../android/telephony/CellSignalStrengthGsm.md) | GSM signal strength related information. |
| --- | --- |
| [CellSignalStrengthLte](../android/telephony/CellSignalStrengthLte.md) | LTE signal strength related information. |
| [CellSignalStrengthNr](../android/telephony/CellSignalStrengthNr.md) | 5G NR signal strength related information. |
| [CellSignalStrengthTdscdma](../android/telephony/CellSignalStrengthTdscdma.md) | Tdscdma signal strength related information. |
| --- | --- |
| [CellSignalStrengthWcdma](../android/telephony/CellSignalStrengthWcdma.md) | Wcdma signal strength related information. |
| [ClosedSubscriberGroupInfo](../android/telephony/ClosedSubscriberGroupInfo.md) | Information to represent a closed subscriber group. |
| [DataFailCause](../android/telephony/DataFailCause.md) | DataFailCause collects data connection failure causes code from different sources. |
| --- | --- |
| [DisconnectCause](../android/telephony/DisconnectCause.md) | Describes the cause of a disconnected call. |
| [IccOpenLogicalChannelResponse](../android/telephony/IccOpenLogicalChannelResponse.md) | Response to the android. |
| [MbmsDownloadSession](../android/telephony/MbmsDownloadSession.md) | This class provides functionality for file download over MBMS. |
| --- | --- |
| [MbmsGroupCallSession](../android/telephony/MbmsGroupCallSession.md) | This class provides functionality for accessing group call functionality over MBMS. |
| [MbmsStreamingSession](../android/telephony/MbmsStreamingSession.md) | This class provides functionality for streaming media over MBMS. |
| [NeighboringCellInfo](../android/telephony/NeighboringCellInfo.md) | Represents the neighboring cell information, including Received Signal Strength and Cell ID location. |
| --- | --- |
| [NetworkRegistrationInfo](../android/telephony/NetworkRegistrationInfo.md) | Description of a mobile network registration info |
| [NetworkScan](../android/telephony/NetworkScan.md) | The caller of android. |
| [NetworkScanRequest](../android/telephony/NetworkScanRequest.md) | Defines a request to perform a network scan. |
| --- | --- |
| [ParsedPhoneNumber](../android/telephony/ParsedPhoneNumber.md) | Handles the results from PhoneNumberManager by providing Phone number, error code, and is valid number. |
| [PhoneNumberFormattingTextWatcher](../android/telephony/PhoneNumberFormattingTextWatcher.md) | Watches a [android.widget.TextView](../android/widget/TextView.md) and if a phone number is entered will format it. |
| [PhoneNumberManager](../android/telephony/PhoneNumberManager.md) | PhoneNumberManager provides APIs for parsing phone numbers from various sources, such as URIs. |
| --- | --- |
| [PhoneNumberUtils](../android/telephony/PhoneNumberUtils.md) | Various utilities for dealing with phone number strings. |
| [PhoneStateListener](../android/telephony/PhoneStateListener.md) | A listener class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others. |
| [PhysicalChannelConfig](../android/telephony/PhysicalChannelConfig.md) | <br /> |
| --- | --- |
| [PreciseDataConnectionState](../android/telephony/PreciseDataConnectionState.md) | Contains precise data connection state. |
| [RadioAccessSpecifier](../android/telephony/RadioAccessSpecifier.md) | Describes a particular radio access network to be scanned. |
| [ServiceState](../android/telephony/ServiceState.md) | Contains phone state and service related information. |
| --- | --- |
| [SignalStrength](../android/telephony/SignalStrength.md) | Contains phone signal strength related information. |
| [SignalStrengthUpdateRequest](../android/telephony/SignalStrengthUpdateRequest.md) | Request used to register [SignalThresholdInfo](../android/telephony/SignalThresholdInfo.md) to be notified when the signal strength breach the specified thresholds. |
| [SignalThresholdInfo](../android/telephony/SignalThresholdInfo.md) | Defines the threshold value of the signal strength. |
| --- | --- |
| [SmsManager](../android/telephony/SmsManager.md) | Manages SMS operations such as sending data, text, and pdu SMS messages. |
| [SmsMessage](../android/telephony/SmsMessage.md) | A Short Message Service message. |
| [SubscriptionInfo](../android/telephony/SubscriptionInfo.md) | A Parcelable class for Subscription Information. |
| --- | --- |
| [SubscriptionManager](../android/telephony/SubscriptionManager.md) | Subscription manager provides the mobile subscription information. |
| [SubscriptionPlan](../android/telephony/SubscriptionPlan.md) | Description of a billing relationship plan between a carrier and a specific subscriber. |
| [TelephonyCallback](../android/telephony/TelephonyCallback.md) | A callback class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others. |
| --- | --- |
| [TelephonyDisplayInfo](../android/telephony/TelephonyDisplayInfo.md) | TelephonyDisplayInfo contains telephony-related information used for display purposes only. |
| [TelephonyManager](../android/telephony/TelephonyManager.md) | Provides access to information about the telephony services on the device. |
| [TelephonyScanManager](../android/telephony/TelephonyScanManager.md) | Manages the radio access network scan requests and callbacks. |
| --- | --- |
| [UiccCardInfo](../android/telephony/UiccCardInfo.md) | The UiccCardInfo represents information about a currently inserted UICC or embedded eUICC. |
| [UiccPortInfo](../android/telephony/UiccPortInfo.md) | UiccPortInfo class represents information about a single port contained on [UiccCardInfo](../android/telephony/UiccCardInfo.md). |
| [VisualVoicemailService](../android/telephony/VisualVoicemailService.md) | This service is implemented by dialer apps that wishes to handle OMTP or similar visual voicemails. |
| --- | --- |
| [VisualVoicemailSms](../android/telephony/VisualVoicemailSms.md) | Represents the content of a visual voicemail SMS. |
| [VisualVoicemailSmsFilterSettings](../android/telephony/VisualVoicemailSmsFilterSettings.md) | Class to represent various settings for the visual voicemail SMS filter. |
