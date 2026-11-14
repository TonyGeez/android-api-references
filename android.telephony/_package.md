# android.telephony

# android.telephony

Kotlin| [Java](https://developer.android.com/reference/android/telephony/package-summary "View this page in Java")

## Interfaces

| [CarrierConfigChangeListener](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.CarrierConfigChangeListener) | Listener interface to get a notification when the carrier configurations have changed. |
| [ActiveDataSubscriptionIdListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ActiveDataSubscriptionIdListener) | Interface for active data subscription ID listener. |
| [BarringInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.BarringInfoListener) | Interface for barring information listener. |
| [CallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallDisconnectCauseListener) | Interface for call disconnect cause listener. |
| [CallForwardingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallForwardingIndicatorListener) | Interface for call-forwarding indicator listener. |
| [CallStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallStateListener) | Interface for call state listener. |
| [CarrierNetworkListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CarrierNetworkListener) | Interface for carrier network listener. |
| [CellInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellInfoListener) | Interface for cell info listener. |
| [CellLocationListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CellLocationListener) | Interface for device cell location listener. |
| [DataActivationStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataActivationStateListener) | Interface for SIM data activation state listener. |
| [DataActivityListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataActivityListener) | Interface for data activity state listener. |
| [DataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DataConnectionStateListener) | Interface for data connection state listener. |
| [DisplayInfoListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.DisplayInfoListener) | Interface for display info listener. |
| [EmergencyNumberListListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.EmergencyNumberListListener) | Interface for the current emergency number list listener. |
| [ImsCallDisconnectCauseListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ImsCallDisconnectCauseListener) | Interface for IMS call disconnect cause listener. |
| [MessageWaitingIndicatorListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.MessageWaitingIndicatorListener) | Interface for message waiting indicator listener. |
| [PhysicalChannelConfigListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PhysicalChannelConfigListener) | Interface for current physical channel configuration listener. |
| [PreciseDataConnectionStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.PreciseDataConnectionStateListener) | Interface for precise data connection state listener. |
| [RegistrationFailedListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.RegistrationFailedListener) | Interface for registration failures listener. |
| [ServiceStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener) | Interface for service state listener. |
| [SignalStrengthsListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.SignalStrengthsListener) | Interface for network signal strengths listener. |
| [UserMobileDataStateListener](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.UserMobileDataStateListener) | Interface for user mobile data state listener. |

## Classes

| [AccessNetworkConstants](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants) | Contains access network related constants. |
| [AvailableNetworkInfo](https://developer.android.com/reference/kotlin/android/telephony/AvailableNetworkInfo) | Defines available network information which includes corresponding subscription id, network plmns and corresponding priority to be used for network selection by Opportunistic Network Service when passed through [TelephonyManager.updateAvailableNetworks](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#updateAvailableNetworks(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20java.util.function.Consumer)) |
| [BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo) | Provides the barring configuration for a particular service type. |
| [CarrierConfigManager](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager) | Provides access to telephony configuration values that are carrier-specific. |
| [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity) | CellIdentity represents the identity of a unique cell. |
| [CellIdentityCdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityCdma) | CellIdentity is to represent a unique CDMA cell |
| [CellIdentityGsm](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityGsm) | CellIdentity to represent a unique GSM cell |
| [CellIdentityLte](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte) | CellIdentity is to represent a unique LTE cell |
| [CellIdentityNr](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr) | Information to represent a unique NR(New Radio 5G) cell. |
| [CellIdentityTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityTdscdma) | CellIdentity is to represent a unique TD-SCDMA cell |
| [CellIdentityWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityWcdma) | CellIdentity to represent a unique UMTS cell |
| [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) | Immutable cell information from a point in time. |
| [CellInfoCdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoCdma) | A [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) representing a CDMA cell that provides identity and measurement info. |
| [CellInfoGsm](https://developer.android.com/reference/kotlin/android/telephony/CellInfoGsm) | A [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) representing a GSM cell that provides identity and measurement info. |
| [CellInfoLte](https://developer.android.com/reference/kotlin/android/telephony/CellInfoLte) | A [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) representing an LTE cell that provides identity and measurement info. |
| [CellInfoNr](https://developer.android.com/reference/kotlin/android/telephony/CellInfoNr) | A [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) representing an 5G NR cell that provides identity and measurement info. |
| [CellInfoTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoTdscdma) | A [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) representing a TD-SCDMA cell that provides identity and measurement info. |
| [CellInfoWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma) | A [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) representing a WCDMA cell that provides identity and measurement info. |
| [CellLocation](https://developer.android.com/reference/kotlin/android/telephony/CellLocation) | Abstract class that represents the location of the device. |
| [CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength) | Abstract base class for cell phone signal strength related information. |
| [CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma) | Signal strength related information. |
| [CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm) | GSM signal strength related information. |
| [CellSignalStrengthLte](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte) | LTE signal strength related information. |
| [CellSignalStrengthNr](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr) | 5G NR signal strength related information. |
| [CellSignalStrengthTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthTdscdma) | Tdscdma signal strength related information. |
| [CellSignalStrengthWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthWcdma) | Wcdma signal strength related information. |
| [ClosedSubscriberGroupInfo](https://developer.android.com/reference/kotlin/android/telephony/ClosedSubscriberGroupInfo) | Information to represent a closed subscriber group. |
| [DataFailCause](https://developer.android.com/reference/kotlin/android/telephony/DataFailCause) | DataFailCause collects data connection failure causes code from different sources. |
| [DisconnectCause](https://developer.android.com/reference/kotlin/android/telephony/DisconnectCause) | Describes the cause of a disconnected call. |
| [IccOpenLogicalChannelResponse](https://developer.android.com/reference/kotlin/android/telephony/IccOpenLogicalChannelResponse) | Response to the android. |
| [MbmsDownloadSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession) | This class provides functionality for file download over MBMS. |
| [MbmsGroupCallSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsGroupCallSession) | This class provides functionality for accessing group call functionality over MBMS. |
| [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession) | This class provides functionality for streaming media over MBMS. |
| [NeighboringCellInfo](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo) | Represents the neighboring cell information, including Received Signal Strength and Cell ID location. |
| [NetworkRegistrationInfo](https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo) | Description of a mobile network registration info |
| [NetworkScan](https://developer.android.com/reference/kotlin/android/telephony/NetworkScan) | The caller of android. |
| [NetworkScanRequest](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest) | Defines a request to perform a network scan. |
| [ParsedPhoneNumber](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber) | Handles the results from PhoneNumberManager by providing Phone number, error code, and is valid number. |
| [PhoneNumberFormattingTextWatcher](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher) | Watches a [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) and if a phone number is entered will format it. |
| [PhoneNumberManager](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberManager) | PhoneNumberManager provides APIs for parsing phone numbers from various sources, such as URIs. |
| [PhoneNumberUtils](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils) | Various utilities for dealing with phone number strings. |
| [PhoneStateListener](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener) | A listener class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others. |
| [PhysicalChannelConfig](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig) | <br /> |
| [PreciseDataConnectionState](https://developer.android.com/reference/kotlin/android/telephony/PreciseDataConnectionState) | Contains precise data connection state. |
| [RadioAccessSpecifier](https://developer.android.com/reference/kotlin/android/telephony/RadioAccessSpecifier) | Describes a particular radio access network to be scanned. |
| [ServiceState](https://developer.android.com/reference/kotlin/android/telephony/ServiceState) | Contains phone state and service related information. |
| [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength) | Contains phone signal strength related information. |
| [SignalStrengthUpdateRequest](https://developer.android.com/reference/kotlin/android/telephony/SignalStrengthUpdateRequest) | Request used to register [SignalThresholdInfo](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo) to be notified when the signal strength breach the specified thresholds. |
| [SignalThresholdInfo](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo) | Defines the threshold value of the signal strength. |
| [SmsManager](https://developer.android.com/reference/kotlin/android/telephony/SmsManager) | Manages SMS operations such as sending data, text, and pdu SMS messages. |
| [SmsMessage](https://developer.android.com/reference/kotlin/android/telephony/SmsMessage) | A Short Message Service message. |
| [SubscriptionInfo](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionInfo) | A Parcelable class for Subscription Information. |
| [SubscriptionManager](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager) | Subscription manager provides the mobile subscription information. |
| [SubscriptionPlan](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan) | Description of a billing relationship plan between a carrier and a specific subscriber. |
| [TelephonyCallback](https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback) | A callback class for monitoring changes in specific telephony states on the device, including service state, signal strength, message waiting indicator (voicemail), and others. |
| [TelephonyDisplayInfo](https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo) | TelephonyDisplayInfo contains telephony-related information used for display purposes only. |
| [TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) | Provides access to information about the telephony services on the device. |
| [TelephonyScanManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyScanManager) | Manages the radio access network scan requests and callbacks. |
| [UiccCardInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo) | The UiccCardInfo represents information about a currently inserted UICC or embedded eUICC. |
| [UiccPortInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccPortInfo) | UiccPortInfo class represents information about a single port contained on [UiccCardInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo). |
| [VisualVoicemailService](https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailService) | This service is implemented by dialer apps that wishes to handle OMTP or similar visual voicemails. |
| [VisualVoicemailSms](https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms) | Represents the content of a visual voicemail SMS. |
| [VisualVoicemailSmsFilterSettings](https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings) | Class to represent various settings for the visual voicemail SMS filter. |
