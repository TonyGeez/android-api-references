Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TelephonyManager

```
open class TelephonyManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.TelephonyManager](TelephonyManager.md) |

Provides access to information about the telephony services on the device. Applications can use the methods in this class to determine telephony services and states, as well as to access some types of subscriber information. Applications can also register a listener to receive notification of telephony state changes.

The returned TelephonyManager will use the default subscription for all calls. To call an API for a specific subscription, use createForSubscriptionId. e.g. ` telephonyManager = defaultSubTelephonyManager.createForSubscriptionId(subId); `

Note that access to some telephony information is permission-protected. Your application cannot access the protected information unless it has the appropriate permissions declared in its manifest file. Where permissions apply, they are noted in the methods through which you access the protected information.

TelephonyManager is intended for use on devices that implement `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`. On devices that do not implement this feature, the behavior is not reliable. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` feature which can be detected using hasSystemFeature.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.CallComposerException` Exception that may be supplied to the callback in #uploadCallComposerPicture if something goes awry. |
| abstract | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.CellInfoCallback` Callback for providing asynchronous CellInfo on request |
| open | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.ModemErrorException` Exception that is supplied to the callback in getNetworkSlicingConfiguration if the modem returned a failure. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.NetworkSlicingException` Exception that may be supplied to the callback in getNetworkSlicingConfiguration if something goes awry. |
| open | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.TimeoutException` Exception that is supplied to the callback in getNetworkSlicingConfiguration if the system timed out waiting for a response from the Radio. |
| abstract | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.UssdResponseCallback` Used to notify callers of sendUssdRequest when the network either successfully executes a USSD request, or if there was a failure while executing the request. |
| --- | --- |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_MESSAGING_CLIENT_SERVICE:kotlin.String` A service action that identifies a `https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingClientService.html#` subclass in the AndroidManifest. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_DEFAULT_NETWORK_AVAILABLE:kotlin.String` Broadcast action sent when the availability of the system default network changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_PCO_VALUE:kotlin.String` Broadcast action sent when a PCO value becomes available from the modem. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_REDIRECTED:kotlin.String` Broadcast action sent when a data connection is redirected with validation failure. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_REQUEST_NETWORK_FAILED:kotlin.String` Broadcast action sent when a data connection setup fails. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_RESET:kotlin.String` Broadcast action sent when carrier apps should reset their internal state. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CONFIGURE_VOICEMAIL:kotlin.String` Open the voicemail settings activity to make changes to voicemail configuration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_MULTI_SIM_CONFIG_CHANGED:kotlin.String` Broadcast action to be received by Broadcast receivers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_NETWORK_COUNTRY_CHANGED:kotlin.String` Broadcast intent action for network country code changes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_PHONE_STATE_CHANGED:kotlin.String` Broadcast intent action indicating that the call state on the device has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_RESET_MOBILE_NETWORK_SETTINGS:kotlin.String` Activity action: Show setting to reset mobile networks. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_RESPOND_VIA_MESSAGE:kotlin.String` The Phone app sends this intent when a user opts to respond-via-message during an incoming call. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SECRET_CODE:kotlin.String` Broadcast Action: A debug code has been entered in the dialer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SHOW_VOICEMAIL_NOTIFICATION:kotlin.String` Broadcast intent action for letting the default dialer to know to show voicemail notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` Broadcast Action: The subscription carrier identity has changed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_SPECIFIC_CARRIER_IDENTITY_CHANGED:kotlin.String` Broadcast Action: The subscription specific carrier identity has changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ALLOWED_NETWORK_TYPES_REASON_CARRIER:kotlin.Int` To indicate allowed network type change is requested by carrier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ALLOWED_NETWORK_TYPES_REASON_USER:kotlin.Int` To indicate allowed network type change is requested by user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#APPTYPE_CSIM:kotlin.Int` UICC application type is CSIM |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#APPTYPE_ISIM:kotlin.Int` UICC application type is ISIM |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#APPTYPE_RUIM:kotlin.Int` UICC application type is RUIM |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#APPTYPE_SIM:kotlin.Int` UICC application type is SIM |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#APPTYPE_UNKNOWN:kotlin.Int` UICC application type is unknown or not specified |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#APPTYPE_USIM:kotlin.Int` UICC application type is USIM |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_EAP_AKA:kotlin.Int` Authentication type for UICC challenge is EAP AKA. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_EAP_SIM:kotlin.Int` Authentication type for UICC challenge is EAP SIM. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_GBA_BOOTSTRAP:kotlin.Int` Authentication type for GBA Bootstrap Challenge. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_GBA_NAF_KEY_EXTERNAL:kotlin.Int` Authentication type for GBA Network Application Functions (NAF) key External Challenge. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_BUSINESS_ONLY:kotlin.Int` Call composer status **Business Only** from user setting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_OFF:kotlin.Int` Call composer status **OFF** from user setting. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_ON:kotlin.Int` Call composer status **ON** from user setting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_IDLE:kotlin.Int` Device call state: No activity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_OFFHOOK:kotlin.Int` Device call state: Off-hook. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_RINGING:kotlin.Int` Device call state: Ringing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CAPABILITY_SLICING_CONFIG_SUPPORTED:kotlin.String` Indicates whether getNetworkSlicingConfiguration is supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_NOT_RESTRICTED:kotlin.Int` The device is not restricted to a carrier |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_RESTRICTED:kotlin.Int` The device is restricted to a carrier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_RESTRICTED_TO_CALLER:kotlin.Int` The device is restricted to the carrier of the calling application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_UNKNOWN:kotlin.Int` Carrier restriction status value is unknown, in case modem did not provide any information about carrier restriction status. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_AFFILIATED:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` which permits roaming on affiliated networks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_ANY:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` which permits roaming on any network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_HOME:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` which only permits connections on home networks. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CDMA_ROAMING_MODE_RADIO_DEFAULT:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` which leaves the roaming mode set to the radio default or to the user's preference if they've indicated one. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_DORMANT:kotlin.Int` Data connection is active, but physical link is down |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_IN:kotlin.Int` Data connection activity: Currently receiving IP PPP traffic. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_INOUT:kotlin.Int` Data connection activity: Currently both sending and receiving IP PPP traffic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_NONE:kotlin.Int` Data connection activity: No traffic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_OUT:kotlin.Int` Data connection activity: Currently sending IP PPP traffic. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_CONNECTED:kotlin.Int` Data connection state: Connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_CONNECTING:kotlin.Int` Data connection state: Currently setting up a data connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_DISCONNECTED:kotlin.Int` Data connection state: Disconnected. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_DISCONNECTING:kotlin.Int` Data connection state: Disconnecting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_CARRIER:kotlin.Int` To indicate enable or disable carrier data by the system based on carrier signalling or carrier privileged apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_OVERRIDE:kotlin.Int` To indicate data was enabled or disabled due to mobile data policy overrides. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_POLICY:kotlin.Int` To indicate that data control due to policy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_THERMAL:kotlin.Int` To indicate enable or disable data by thermal service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_UNKNOWN:kotlin.Int` To indicate that data was enabled or disabled due to an unknown reason. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_USER:kotlin.Int` To indicate that user enabled or disabled data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_HANDOVER_IN_PROGRESS:kotlin.Int` Data connection state: Handover in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_SUSPENDED:kotlin.Int` Data connection state: Suspended. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_UNKNOWN:kotlin.Int` Data connection state: Unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DEFAULT_PORT_INDEX:kotlin.Int` Default port index for a UICC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ERI_FLASH:kotlin.Int` ERI (Enhanced Roaming Indicator) is FLASH i. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ERI_OFF:kotlin.Int` ERI (Enhanced Roaming Indicator) is OFF i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ERI_ON:kotlin.Int` ERI (Enhanced Roaming Indicator) is ON i. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String` Event reported from the Telephony stack to indicate that the `https://developer.android.com/reference/kotlin/android/telecom/Connection.html#` is not able to find any network and likely will not get connected. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_ACTIVE_SIM_SUPPORTED_COUNT:kotlin.String` The number of active SIM supported by current multi-SIM config. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_APN_PROTOCOL:kotlin.String` An integer extra containing the protocol of the apn connection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_APN_TYPE:kotlin.String` An integer extra containing the APN type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_CALL_VOICEMAIL_INTENT:kotlin.String` The intent to call voicemail. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_CARRIER_ID:kotlin.String` An int extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` which indicates the updated carrier id returned by getSimCarrierId. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_CARRIER_NAME:kotlin.String` An string extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` which indicates the updated carrier name of the current subscription. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_DATA_FAIL_CAUSE:kotlin.String` An integer extra containing the data fail cause. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_DEFAULT_NETWORK_AVAILABLE:kotlin.String` A boolean extra indicating the availability of the default network. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE:kotlin.String` Integer extra key used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String` which indicates the type of handover from emergency call to satellite messaging. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_EMERGENCY_CALL_TO_SATELLITE_LAUNCH_INTENT:kotlin.String` Extra key used with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String` for a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` which will be launched by the Dialer app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_HIDE_PUBLIC_SETTINGS:kotlin.String` The boolean value indicating whether the voicemail settings activity launched by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CONFIGURE_VOICEMAIL:kotlin.String` should hide settings accessible through public API. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_INCOMING_NUMBER:kotlin.String` Extra key used with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_PHONE_STATE_CHANGED:kotlin.String` broadcast for a String containing the incoming or outgoing phone number. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_IS_REFRESH:kotlin.String` Boolean value representing whether the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SHOW_VOICEMAIL_NOTIFICATION:kotlin.String` is new or a refresh of an existing notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_LAST_KNOWN_NETWORK_COUNTRY:kotlin.String` The extra used with an `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_NETWORK_COUNTRY_CHANGED:kotlin.String` to specify the last known the country code in ISO-3166-1 alpha-2 format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_LAUNCH_VOICEMAIL_SETTINGS_INTENT:kotlin.String` The intent to launch voicemail settings. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_NETWORK_COUNTRY:kotlin.String` The extra used with an `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_NETWORK_COUNTRY_CHANGED:kotlin.String` to specify the the country code in ISO-3166-1 alpha-2 format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_NOTIFICATION_COUNT:kotlin.String` The number of voice messages associated with the notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PCO_ID:kotlin.String` An integer extra indicating the ID for the PCO data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PCO_VALUE:kotlin.String` A byte array extra containing PCO data read from the modem. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` The extra used with an `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CONFIGURE_VOICEMAIL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SHOW_VOICEMAIL_NOTIFICATION:kotlin.String` `Intent` to specify the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` the configuration or notification is for. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_REDIRECTION_URL:kotlin.String` String extra containing the redirection URL sent with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_REDIRECTED:kotlin.String`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_SPECIFIC_CARRIER_ID:kotlin.String` An int extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_SPECIFIC_CARRIER_IDENTITY_CHANGED:kotlin.String` which indicates the updated specific carrier id returned by getSimSpecificCarrierId. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_SPECIFIC_CARRIER_NAME:kotlin.String` An string extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_SPECIFIC_CARRIER_IDENTITY_CHANGED:kotlin.String` which indicates the updated specific carrier name returned by getSimSpecificCarrierIdName. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` The lookup key used with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_PHONE_STATE_CHANGED:kotlin.String` broadcast for a String containing the new call state. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_SUBSCRIPTION_ID:kotlin.String` An int extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` to indicate the subscription which has changed; or in general whenever a subscription ID needs specified. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_VOICEMAIL_NUMBER:kotlin.String` The voicemail number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_COARSE:kotlin.Int` Include coarse location data. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_FINE:kotlin.Int` Include fine location data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_NONE:kotlin.Int` Specifies to not include any location related data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#METADATA_HIDE_VOICEMAIL_SETTINGS_MENU:kotlin.String` A boolean meta-data value indicating whether the voicemail settings should be hidden in the call settings page launched by `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#ACTION_SHOW_CALL_SETTINGS:kotlin.String`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_ALLOWED:kotlin.Int` The usage of multiple SIM cards at the same time to register on the network (e.g. Dual Standby or Dual Active) is supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_NOT_SUPPORTED_BY_CARRIER:kotlin.Int` The usage of multiple SIM cards at the same time to register on the network (e.g. Dual Standby or Dual Active) is supported by the hardware, but restricted by the carrier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_NOT_SUPPORTED_BY_HARDWARE:kotlin.Int` The usage of multiple SIM cards at the same time to register on the network (e.g. Dual Standby or Dual Active) is not supported by the hardware. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_SELECTION_MODE_AUTO:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_SELECTION_MODE_MANUAL:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_SELECTION_MODE_UNKNOWN:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int` Current network is 1xRTT |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_1xRTT:kotlin.Long` network type bitmask indicating the support of radio tech 1xRTT. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_CDMA:kotlin.Long` network type bitmask indicating the support of radio tech CDMA(IS95A/IS95B). |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EDGE:kotlin.Long` network type bitmask indicating the support of radio tech EDGE. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EHRPD:kotlin.Long` network type bitmask indicating the support of radio tech EHRPD. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_0:kotlin.Long` network type bitmask indicating the support of radio tech EVDO 0. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_A:kotlin.Long` network type bitmask indicating the support of radio tech EVDO A. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_B:kotlin.Long` network type bitmask indicating the support of radio tech EVDO B. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_GPRS:kotlin.Long` network type bitmask indicating the support of radio tech GPRS. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_GSM:kotlin.Long` network type bitmask indicating the support of radio tech GSM. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSDPA:kotlin.Long` network type bitmask indicating the support of radio tech HSDPA. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSPA:kotlin.Long` network type bitmask indicating the support of radio tech HSPA. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSPAP:kotlin.Long` network type bitmask indicating the support of radio tech HSPAP. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSUPA:kotlin.Long` network type bitmask indicating the support of radio tech HSUPA. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_IWLAN:kotlin.Long` network type bitmask indicating the support of radio tech IWLAN. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE:kotlin.Long` network type bitmask indicating the support of radio tech LTE. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE_CA:kotlin.Long` NOT USED; this bitmask is exposed accidentally. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_NR:kotlin.Long` network type bitmask indicating the support of radio tech NR(New Radio) 5G. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_TD_SCDMA:kotlin.Long` network type bitmask indicating the support of radio tech TD_SCDMA. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_UMTS:kotlin.Long` network type bitmask indicating the support of radio tech UMTS. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_UNKNOWN:kotlin.Long` network type bitmask unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int` Current network is CDMA: Either IS95A or IS95B |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int` Current network is EDGE |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int` Current network is eHRPD |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int` Current network is EVDO revision 0 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int` Current network is EVDO revision A |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int` Current network is EVDO revision B |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int` Current network is GPRS |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int` Current network is GSM |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int` Current network is HSDPA |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int` Current network is HSPA |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int` Current network is HSPA+ |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int` Current network is HSUPA |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int` Current network is iDen |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int` Current network is IWLAN |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int` Current network is LTE |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int` Current network is NR (New Radio) 5G. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int` Current network is TD_SCDMA |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int` Current network is UMTS |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int` Network type is unknown |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PHONE_TYPE_CDMA:kotlin.Int` Phone radio is CDMA. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PHONE_TYPE_GSM:kotlin.Int` Phone radio is GSM. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PHONE_TYPE_NONE:kotlin.Int` No phone radio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PHONE_TYPE_SIP:kotlin.Int` Phone is via SIP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PREMIUM_CAPABILITY_PRIORITIZE_LATENCY:kotlin.Int` A premium capability that boosts the network to allow for real-time interactive traffic by prioritizing low latency communication. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_IN_PROGRESS:kotlin.Int` Purchase premium capability failed because a request was already made and is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_PURCHASED:kotlin.Int` Purchase premium capability failed because it is already purchased and available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_DISABLED:kotlin.Int` Purchase premium capability failed because the carrier disabled or does not support the capability, as specified in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTED_PREMIUM_CAPABILITIES_INT_ARRAY:kotlin.String`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_ERROR:kotlin.Int` Purchase premium capability failed because the carrier app did not indicate success. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ENTITLEMENT_CHECK_FAILED:kotlin.Int` Purchase premium capability failed because the entitlement check failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_FEATURE_NOT_SUPPORTED:kotlin.Int` Purchase premium capability failed because the device does not support the feature. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_NETWORK_NOT_AVAILABLE:kotlin.Int` Purchase premium capability failed because the network is not available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_NOT_DEFAULT_DATA_SUBSCRIPTION:kotlin.Int` Purchase premium capability failed because the request was not made on the default data subscription, indicated by getDefaultDataSubscriptionId. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_NOT_FOREGROUND:kotlin.Int` Purchase premium capability failed because the requesting application is not in the foreground. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_PENDING_NETWORK_SETUP:kotlin.Int` Purchase premium capability was successful and is waiting for the network to setup the slicing configuration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_REQUEST_FAILED:kotlin.Int` Purchase premium capability failed because the telephony service is unavailable or there was an error in the phone process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_SUCCESS:kotlin.Int` Purchase premium capability request was successful. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED:kotlin.Int` Purchase premium capability failed because the request is throttled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_TIMEOUT:kotlin.Int` Purchase premium capability failed because we did not receive a response from the user for the performance boost notification within the time specified by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_NOTIFICATION_DISPLAY_TIMEOUT_MILLIS_LONG:kotlin.String`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_CANCELED:kotlin.Int` Purchase premium capability failed because the user canceled the operation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_DISABLED:kotlin.Int` Purchase premium capability failed because the user disabled the feature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SET_OPPORTUNISTIC_SUB_INACTIVE_SUBSCRIPTION:kotlin.Int` The subscription is not valid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SET_OPPORTUNISTIC_SUB_NO_OPPORTUNISTIC_SUB_AVAILABLE:kotlin.Int` The subscription is not valid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SET_OPPORTUNISTIC_SUB_REMOTE_SERVICE_EXCEPTION:kotlin.Int` Subscription service happened remote exception. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SET_OPPORTUNISTIC_SUB_SUCCESS:kotlin.Int` No error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SET_OPPORTUNISTIC_SUB_VALIDATION_FAILED:kotlin.Int` Validation failed when trying to switch to preferred subscription. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_ABSENT:kotlin.Int` SIM card state: no SIM card is available in the device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_IO_ERROR:kotlin.Int` SIM card state: SIM Card Error, present but faulty |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_RESTRICTED:kotlin.Int` SIM card state: SIM Card restricted, present but not usable due to carrier restrictions. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NETWORK_LOCKED:kotlin.Int` SIM card state: Locked: requires a network PIN to unlock |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NOT_READY:kotlin.Int` SIM card state: SIM Card is NOT READY |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PERM_DISABLED:kotlin.Int` SIM card state: SIM Card Error, permanently disabled |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PIN_REQUIRED:kotlin.Int` SIM card state: Locked: requires the user's SIM PIN to unlock |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PUK_REQUIRED:kotlin.Int` SIM card state: Locked: requires the user's SIM PUK to unlock |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_READY:kotlin.Int` SIM card state: Ready |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_UNKNOWN:kotlin.Int` SIM card state: Unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#TTY_MODE_FULL:kotlin.Int` TTY (teletypewriter) mode is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#TTY_MODE_HCO:kotlin.Int` TTY (teletypewriter) mode is in hearing carryover mode (HCO). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#TTY_MODE_OFF:kotlin.Int` TTY (teletypewriter) mode is off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#TTY_MODE_VCO:kotlin.Int` TTY (teletypewriter) mode is in voice carryover mode (VCO). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNINITIALIZED_CARD_ID:kotlin.Int` A UICC card identifier used before the UICC card is loaded. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int` An unknown carrier id. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNSUPPORTED_CARD_ID:kotlin.Int` A UICC card identifier used if the device does not support the operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_ABORTED:kotlin.Int` The request is aborted. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_DISABLE_MODEM_FAIL:kotlin.Int` Disable modem fail. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_ENABLE_MODEM_FAIL:kotlin.Int` Enable modem fail. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_INVALID_ARGUMENTS:kotlin.Int` The parameter passed in is invalid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_MULTIPLE_NETWORKS_NOT_SUPPORTED:kotlin.Int` Carrier app does not support multiple available networks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_NO_CARRIER_PRIVILEGE:kotlin.Int` No carrier privilege. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_NO_OPPORTUNISTIC_SUB_AVAILABLE:kotlin.Int` The subscription is not valid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_REMOTE_SERVICE_EXCEPTION:kotlin.Int` There is no OpportunisticNetworkService. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_SERVICE_IS_DISABLED:kotlin.Int` OpportunisticNetworkService is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_SIM_PORT_NOT_AVAILABLE:kotlin.Int` SIM port is not available to switch to opportunistic subscription. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_SUCCESS:kotlin.Int` No error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_UNKNOWN_FAILURE:kotlin.Int` There is a unknown failure happened. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#USSD_ERROR_NOT_ALLOWED:kotlin.Int` Failure code returned when a USSD request has failed to execute because the calling app is not allowed to send USSD requests. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#USSD_ERROR_SERVICE_UNAVAIL:kotlin.Int` Failure code returned when a USSD request has failed to execute because the Telephony service is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#USSD_RETURN_FAILURE:kotlin.Int` Failed code returned when the mobile network has failed to complete a USSD request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#VVM_TYPE_CVVM:kotlin.String` A flavor of OMTP protocol with a different mobile originated (MO) format |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#VVM_TYPE_OMTP:kotlin.String` The OMTP protocol. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canChangeDtmfToneLength Whether the device supports configuring the DTMF tone length. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearSignalStrengthUpdateRequest Clear a SignalStrengthUpdateRequest from the system. |
| open [TelephonyManager](TelephonyManager.md)? | createForPhoneAccountHandle Create a new TelephonyManager object pinned to the subscription ID associated with the given phone account. |
| --- | --- |
| open [TelephonyManager](TelephonyManager.md)! | createForSubscriptionId Create a new TelephonyManager object pinned to the given subscription ID. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | doesSwitchMultiSimConfigTriggerReboot Get whether making changes to modem configurations by switchMultiSimConfig will trigger device reboot. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getActiveModemCount Returns the number of logical modems currently configured to be activated. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CellInfo](CellInfo.md)!\>! | getAllCellInfo Requests all available cell information from all radios on the device including the camped/registered, serving, and neighboring cells. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAllowedNetworkTypesForReason Get the allowed network types for certain reason. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCallComposerStatus Get the user-set status for enriched calling with call composer. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCallState Returns the state of all calls on the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCallStateForSubscription Retrieve the call state for a specific subscription that was specified when this TelephonyManager instance was created. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCardIdForDefaultEuicc Get the card ID of the default eUICC card. |
| --- | --- |
| open [PersistableBundle](../android.os/PersistableBundle.md)! | getCarrierConfig Returns the carrier config of the subscription ID pinned to the TelephonyManager. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCarrierIdFromSimMccMnc Returns carrier id based on sim MCCMNC (returned by getSimOperator) only. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getCarrierRestrictionStatus Get the carrier restriction status of the device. |
| --- | --- |
| open [CellLocation](CellLocation.md)! | getCellLocation Returns the current location of the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCurrentTtyMode Returns the current TTY mode of the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDataActivity Returns a constant indicating the type of activity on a data connection (cellular). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDataNetworkType Returns a constant indicating the radio technology (network type) currently in use on the device for data transmission. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDataState Returns a constant indicating the current data connection state (cellular). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDeviceId Returns the unique device ID, for example, the IMEI for GSM and the MEID or ESN for CDMA phones. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDeviceId Returns the unique device ID of a subscription, for example, the IMEI for GSM and the MEID for CDMA phones. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getDeviceSoftwareVersion Returns the software version number for the device, for example, the IMEI/SV for GSM phones. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EmergencyNumber](../android.telephony.emergency/EmergencyNumber.md)!\>!\> | getEmergencyNumberList Get the emergency number list based on current locale, sim, default, modem and network. |
| --- | --- |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EmergencyNumber](../android.telephony.emergency/EmergencyNumber.md)!\>!\> | getEmergencyNumberList Get the per-category emergency number list based on current locale, sim, default, modem and network. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getEquivalentHomePlmns Returns a list of the equivalent home PLMNs (EF_EHPLMN) from the USIM app. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getForbiddenPlmns Returns an array of Forbidden PLMNs from the USIM App Returns null if the query fails. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getGroupIdLevel1 Returns the Group Identifier Level1 for a GSM phone. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getIccAuthentication Returns the response of authentication for the default subscription. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getImei Returns the IMEI (International Mobile Equipment Identity). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getImei Returns the IMEI (International Mobile Equipment Identity). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getLine1Number Returns the phone number string for line 1, for example, the MSISDN for a GSM phone for a particular subscription. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getManualNetworkSelectionPlmn Get the PLMN chosen for Manual Network Selection if active. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getManufacturerCode Returns the Manufacturer Code from the MEID. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getManufacturerCode Returns the Manufacturer Code from the MEID. |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getMaximumCallComposerPictureSize Indicates the maximum size of the call composure picture. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getMeid Returns the MEID (Mobile Equipment Identifier). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getMeid Returns the MEID (Mobile Equipment Identifier). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getMmsUAProfUrl Returns the MMS user agent profile URL. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getMmsUserAgent Returns the MMS user agent. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getNai Returns the Network Access Identifier (NAI). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getNetworkCountryIso Returns the ISO-3166-1 alpha-2 country code equivalent of the MCC (Mobile Country Code) of the current registered operator or the cell nearby, if available. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getNetworkCountryIso Returns the ISO-3166-1 alpha-2 country code equivalent of the MCC (Mobile Country Code) of the current registered operator or the cell nearby, if available. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getNetworkOperator Returns the numeric name (MCC+MNC) of current registered operator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getNetworkOperatorName Returns the alphabetic name of current registered operator. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNetworkSelectionMode Get the network selection mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getNetworkSlicingConfiguration Request to get the current slicing configuration including URSP rules and NSSAIs (configured, allowed and rejected). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getNetworkSpecifier Returns the network specifier of the subscription ID pinned to the TelephonyManager. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNetworkType Return the current data network type. |
| open [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md)? | getPhoneAccountHandle Determines the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` associated with this TelephonyManager. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPhoneCount Returns the number of phones available. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPhoneType Returns a constant indicating the device phone type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPreferredOpportunisticDataSubscription Get preferred opportunistic data subscription Id |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getPrimaryImei Returns the primary IMEI (International Mobile Equipment Identity) of the device as mentioned in GSMA TS. |
| --- | --- |
| open [ServiceState](ServiceState.md)? | getServiceState Returns the current ServiceState information. |
| open [ServiceState](ServiceState.md)? | getServiceState Returns the current ServiceState information. |
| open [ServiceState](ServiceState.md)? | getServiceStateForSlot Returns the service state information on specified SIM slot. |
| --- | --- |
| open [SignalStrength](SignalStrength.md)? | getSignalStrength Get the most recently available signal strength information. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSimCarrierId Returns carrier id of the current subscription. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getSimCarrierIdName Returns carrier id name of the current subscription. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getSimCountryIso Returns the ISO-3166-1 alpha-2 country code equivalent for the SIM provider's country code. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getSimOperator Returns the MCC+MNC (mobile country code + mobile network code) of the provider of the SIM. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getSimOperatorName Returns the Service Provider Name (SPN). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getSimSerialNumber Returns the serial number of the SIM, if applicable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSimSpecificCarrierId Returns fine-grained carrier ID of the current subscription. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getSimSpecificCarrierIdName Similar like getSimCarrierIdName, returns user-facing name of the specific carrier id returned by getSimSpecificCarrierId. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSimState Returns a constant indicating the state of the default SIM card. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSimState Returns a constant indicating the state of the device SIM card in a logical slot. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getSubscriberId Returns the unique subscriber ID, for example, the IMSI for a GSM phone. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSubscriptionId Return an appropriate subscription ID for any situation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSubscriptionId Returns the subscription ID for the given phone account handle. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSupportedModemCount Return how many logical modem can be potentially active simultaneously, in terms of hardware capability. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getSupportedRadioAccessFamily Requires android. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getTypeAllocationCode Returns the Type Allocation Code from the IMEI. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getTypeAllocationCode Returns the Type Allocation Code from the IMEI. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UiccCardInfo](UiccCardInfo.md)!\> | getUiccCardsInfo Gets information about currently inserted UICCs (Universal Integrated Circuit Cards) and eUICCs (embedded UICCs). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getVisualVoicemailPackageName Returns the package responsible of processing visual voicemail for the subscription ID pinned to the TelephonyManager. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getVoiceMailAlphaTag Retrieves the alphabetic identifier associated with the voice mail number. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getVoiceMailNumber Returns the voice mail number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVoiceNetworkType Returns the NETWORK_TYPE_xxxx for voice |
| open [Uri](../android.net/Uri.md)? | getVoicemailRingtoneUri Returns the URI for the per-account voicemail ringtone set in Phone settings. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasCarrierPrivileges Has the calling application been granted carrier privileges by the carrier. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasIccCard This API is used to check if there is an ICC card present in the device. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | iccCloseLogicalChannel Closes a previously opened logical channel to the ICC card. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | iccExchangeSimIO Returns the response APDU for a command APDU sent through SIM_IO. |
| open [IccOpenLogicalChannelResponse](IccOpenLogicalChannelResponse.md)! | iccOpenLogicalChannel Opens a logical channel to the ICC card. |
| open [IccOpenLogicalChannelResponse](IccOpenLogicalChannelResponse.md)! | iccOpenLogicalChannel Opens a logical channel to the ICC card. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | iccTransmitApduBasicChannel Transmit an APDU to the ICC card over the basic channel. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | iccTransmitApduLogicalChannel Transmit an APDU to the ICC card over a logical channel. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isConcurrentVoiceAndDataSupported Whether the device is currently on a technology (e.g. UMTS or LTE) which can support voice and data simultaneously. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDataCapable <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDataConnectionAllowed Checks whether cellular data connection is allowed in the device. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDataEnabled Returns whether mobile data is enabled or not per user setting. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDataEnabledForReason Return whether data is enabled for certain reason . |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDataRoamingEnabled Returns whether mobile data roaming is enabled on the subscription. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDeviceSmsCapable <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDeviceVoiceCapable <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEmergencyNumber Identifies if the supplied phone number is an emergency number that matches a known emergency number based on current locale, SIM card(s), Android database, modem, network, or defaults. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHearingAidCompatibilitySupported Whether the phone supports hearing aid compatibility. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isManualNetworkSelectionAllowed Checks if manual network selection is allowed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isModemEnabledForSlot Indicates whether or not there is a modem stack enabled for the given SIM slot. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | isMultiSimSupported Returns if the usage of multiple SIM cards at the same time to register on the network (e.g. Dual Standby or Dual Active) is supported by the device and by the carrier. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isNetworkRoaming Returns true if the device is considered roaming on the current network, for GSM purposes. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPremiumCapabilityAvailableForPurchase Check whether the given premium capability is available for purchase from the carrier. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isRadioInterfaceCapabilitySupported Whether the device supports a given capability on the radio interface. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isRttSupported Determines whether the device currently supports RTT (Real-time text). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSmsCapable <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isTtyModeSupported <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVoiceCapable <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVoicemailVibrationEnabled Returns whether vibration is set for voicemail notification in Phone settings. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isWorldPhone Whether the device is a world phone. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | listen Registers a listener object to receive notification of changes in specified telephony states. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | purchasePremiumCapability Purchase the given premium capability from the carrier. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | rebootModem Reboot and re-initialize the cellular modem and related subsystems below the OS. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerTelephonyCallback Registers a callback object to receive notification of changes in specified telephony states. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerTelephonyCallback Registers a callback object to receive notification of changes in specified telephony states. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestCellInfoUpdate Requests all available cell information from the current subscription for observed camped/registered, serving, and neighboring cells. |
| --- | --- |
| open [NetworkScan](NetworkScan.md)! | requestNetworkScan Request a network scan. |
| open [NetworkScan](NetworkScan.md)? | requestNetworkScan Request a network scan. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendDialerSpecialCode Send the special dialer code. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | sendEnvelopeWithStatus Send ENVELOPE to the SIM and return the response. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendUssdRequest Sends an Unstructured Supplementary Service Data (USSD) request to the mobile network and informs the caller of the response via the supplied `callback`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendVisualVoicemailSms Send a visual voicemail SMS. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAllowedNetworkTypesForReason Set the allowed network types of the device and provide the reason triggering the allowed network change. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCallComposerStatus Set the user-set status for enriched calling with call composer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDataEnabled Turns mobile data on or off. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDataEnabledForReason Control of data connection and provide the reason triggering the data connection control. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | setForbiddenPlmns Replace the contents of the forbidden PLMN SIM file with the provided values. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setLine1NumberForDisplay Set the line 1 phone number string and its alphatag for the current ICCID for display purpose only, for example, displayed in Phone Status. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNetworkSelectionModeAutomatic Sets the network selection mode to automatic. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setNetworkSelectionModeManual Ask the radio to connect to the input network and change selection mode to manual. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setNetworkSelectionModeManual Ask the radio to connect to the input network and change selection mode to manual. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setOperatorBrandOverride Override the branding for the current ICCID. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setPreferredNetworkTypeToGlobal Set the preferred network type to global mode which includes NR, LTE, CDMA, EvDo and GSM/WCDMA. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPreferredOpportunisticDataSubscription Set preferred opportunistic data subscription id. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSignalStrengthUpdateRequest Set a SignalStrengthUpdateRequest to receive notification when signal quality measurements breach the specified thresholds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVisualVoicemailSmsFilterSettings Set the visual voicemail SMS filter settings for the subscription ID pinned to the TelephonyManager. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setVoiceMailNumber Sets the voice mail number. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVoicemailRingtoneUri Sets the per-account voicemail ringtone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVoicemailVibrationEnabled Sets the per-account preference whether vibration is enabled for voicemail notifications. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | switchMultiSimConfig Switch configs to enable multi-sim or switch back to single-sim |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterTelephonyCallback Unregister an existing TelephonyCallback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | updateAvailableNetworks Update availability of a list of networks in the current location. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | uploadCallComposerPicture Uploads a picture to the carrier network for use with call composer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | uploadCallComposerPicture Uploads a picture to the carrier network for use with call composer. |

| Properties ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_IDLE:kotlin.String` Value used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` corresponding to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_IDLE:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_OFFHOOK:kotlin.String` Value used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` corresponding to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_OFFHOOK:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_RINGING:kotlin.String` Value used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` corresponding to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_RINGING:kotlin.Int`. |
| --- | --- |

## Constants

### ACTION_CARRIER_MESSAGING_CLIENT_SERVICE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CARRIER_MESSAGING_CLIENT_SERVICE: String
```

A service action that identifies a `https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingClientService.html#` subclass in the AndroidManifest.xml.

See `https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingClientService.html#` for the details.

 Value: "android.telephony.action.CARRIER_MESSAGING_CLIENT_SERVICE"

### ACTION_CARRIER_SIGNAL_DEFAULT_NETWORK_AVAILABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CARRIER_SIGNAL_DEFAULT_NETWORK_AVAILABLE: String
```

Broadcast action sent when the availability of the system default network changes.

 Value: "android.telephony.action.CARRIER_SIGNAL_DEFAULT_NETWORK_AVAILABLE"

**See Also**

- registerDefaultNetworkCallback

### ACTION_CARRIER_SIGNAL_PCO_VALUE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CARRIER_SIGNAL_PCO_VALUE: String
```

Broadcast action sent when a PCO value becomes available from the modem. This action is intended for sim/account status checks and only sent to the carrier apps specified in the carrier config for the subscription ID that's attached to this intent. The intent will have the following extra values:

<br />

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_APN_TYPE:kotlin.String`
An integer indicating the apn type.
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_APN_PROTOCOL:kotlin.String`
An integer indicating the protocol of the apn connection
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PCO_ID:kotlin.String`
An integer indicating the PCO id for the data.
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PCO_VALUE:kotlin.String`
A byte array of PCO data read from modem.
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String`
The subscription ID for which the PCO info was received.

This is a protected intent that can only be sent by the system.

 Value: "android.telephony.action.CARRIER_SIGNAL_PCO_VALUE"

### ACTION_CARRIER_SIGNAL_REDIRECTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CARRIER_SIGNAL_REDIRECTED: String
```

Broadcast action sent when a data connection is redirected with validation failure. This action is intended for sim/account status checks and only sent to the carrier apps specified in the carrier config for the subscription ID that's attached to this intent. The intent will have the following extra values:

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_APN_TYPE:kotlin.String`
An integer indicating the apn type.
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_REDIRECTION_URL:kotlin.String`
A string indicating the redirection url
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String`
The subscription ID on which the validation failure happened.

<br />

This is a protected intent that can only be sent by the system.

 Value: "android.telephony.action.CARRIER_SIGNAL_REDIRECTED"

### ACTION_CARRIER_SIGNAL_REQUEST_NETWORK_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CARRIER_SIGNAL_REQUEST_NETWORK_FAILED: String
```

Broadcast action sent when a data connection setup fails. This action is intended for sim/account status checks and only sent to the carrier apps specified in the carrier config for the subscription ID that's attached to this intent. The intent will have the following extra values:

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_APN_TYPE:kotlin.String`
An integer indicating the apn type.
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_DATA_FAIL_CAUSE:kotlin.String`
A integer indicating the data fail cause.
- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String`
The subscription ID on which the data setup failure happened.

<br />

This is a protected intent that can only be sent by the system.

 Value: "android.telephony.action.CARRIER_SIGNAL_REQUEST_NETWORK_FAILED"

### ACTION_CARRIER_SIGNAL_RESET

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CARRIER_SIGNAL_RESET: String
```

Broadcast action sent when carrier apps should reset their internal state. Sent when certain events such as turning on/off mobile data, removing the SIM, etc. require carrier apps to reset their state. This action is intended to signal carrier apps to perform cleanup operations. It is only sent to the carrier apps specified in the carrier config for the subscription ID attached to this intent. The intent will have the following extra values:

<br />

- `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#EXTRA_SUBSCRIPTION_INDEX:kotlin.String`
The subscription ID for which state should be reset.

This is a protected intent that can only be sent by the system.

 Value: "android.telephony.action.CARRIER_SIGNAL_RESET"

### ACTION_CONFIGURE_VOICEMAIL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONFIGURE_VOICEMAIL: String
```

Open the voicemail settings activity to make changes to voicemail configuration.

The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` extra indicates which `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` to configure voicemail. The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_HIDE_PUBLIC_SETTINGS:kotlin.String` hides settings the dialer will modify through public API if set.

 Value: "android.telephony.action.CONFIGURE_VOICEMAIL"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_HIDE_PUBLIC_SETTINGS:kotlin.String`

### ACTION_MULTI_SIM_CONFIG_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MULTI_SIM_CONFIG_CHANGED: String
```

Broadcast action to be received by Broadcast receivers. Indicates multi-SIM configuration is changed. For example, it changed from single SIM capable to dual-SIM capable (DSDS or DSDA) or triple-SIM mode. It doesn't indicate how many subscriptions are actually active, or which states SIMs are, or that all steps during multi-SIM change are done. To know those information you still need to listen to SIM_STATE changes or active subscription changes. See extra of `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_ACTIVE_SIM_SUPPORTED_COUNT:kotlin.String` for updated value.

 Value: "android.telephony.action.MULTI_SIM_CONFIG_CHANGED"

### ACTION_NETWORK_COUNTRY_CHANGED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NETWORK_COUNTRY_CHANGED: String
```

Broadcast intent action for network country code changes.

The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_NETWORK_COUNTRY:kotlin.String` extra indicates the country code of the current network returned by getNetworkCountryIso.

There may be a delay of several minutes before reporting that no country is detected.

 Value: "android.telephony.action.NETWORK_COUNTRY_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_NETWORK_COUNTRY:kotlin.String`
- getNetworkCountryIso

### ACTION_PHONE_STATE_CHANGED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PHONE_STATE_CHANGED: String
```

Broadcast intent action indicating that the call state on the device has changed.

The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` extra indicates the new call state. If a receiving app has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CALL_LOG:kotlin.String` permission, a second extra `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_INCOMING_NUMBER:kotlin.String` provides the phone number for incoming and outgoing calls as a String.

If the receiving app has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CALL_LOG:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` permission, it will receive the broadcast twice; one with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_INCOMING_NUMBER:kotlin.String` populated with the phone number, and another with it blank. Due to the nature of broadcasts, you cannot assume the order in which these broadcasts will arrive, however you are guaranteed to receive two in this case. Apps which are interested in the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_INCOMING_NUMBER:kotlin.String` can ignore the broadcasts where `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_INCOMING_NUMBER:kotlin.String` is not present in the extras (e.g. where hasExtra returns `false`).

This was a android.content.Context#sendStickyBroadcast broadcast in version 1.0, but it is no longer sticky. Instead, use getCallState to synchronously query the current call state. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

 Value: "android.intent.action.PHONE_STATE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_INCOMING_NUMBER:kotlin.String`
- getCallState

### ACTION_RESET_MOBILE_NETWORK_SETTINGS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_RESET_MOBILE_NETWORK_SETTINGS: String
```

Activity action: Show setting to reset mobile networks.

On devices with a settings activity to reset mobile networks, the activity should be launched without additional permissions.

On some devices, this settings activity may not exist. Callers should ensure that this case is appropriately handled.

 Value: "android.telephony.action.RESET_MOBILE_NETWORK_SETTINGS"

### ACTION_RESPOND_VIA_MESSAGE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_RESPOND_VIA_MESSAGE: String
```

The Phone app sends this intent when a user opts to respond-via-message during an incoming call. By default, the device's default SMS app consumes this message and sends a text message to the caller. A third party app can also provide this functionality by consuming this Intent with a `https://developer.android.com/reference/kotlin/android/app/Service.html#` and sending the message using its own messaging system.

The intent contains a URI (available from getData) describing the recipient, using either the `sms:`, `smsto:`, `mms:`, or `mmsto:` URI schema. Each of these URI schema carry the recipient information the same way: the path part of the URI contains the recipient's phone number or a comma-separated set of phone numbers if there are multiple recipients. For example, `smsto:2065551234`.

The intent may also contain extras for the message text (in `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String`) and a message subject (in `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SUBJECT:kotlin.String`).

**Note:** The intent-filter that consumes this Intent needs to be in a `https://developer.android.com/reference/kotlin/android/app/Service.html#` that requires the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SEND_RESPOND_VIA_MESSAGE:kotlin.String`.

For example, the service that receives this intent can be declared in the manifest file with an intent filter like this:

```kotlin
<!-- Service that delivers SMS messages received from the phone "quick response" -->
  <service android:name=".HeadlessSmsSendService"
           android:permission="android.permission.SEND_RESPOND_VIA_MESSAGE"
           android:exported="true" >
    <intent-filter>
      <action android:name="android.intent.action.RESPOND_VIA_MESSAGE" />
      <category android:name="android.intent.category.DEFAULT" />
      <data android:scheme="sms" />
      <data android:scheme="smsto" />
      <data android:scheme="mms" />
      <data android:scheme="mmsto" />
    </intent-filter>
  </service>
```

Output: nothing.

 Value: "android.intent.action.RESPOND_VIA_MESSAGE"

### ACTION_SECRET_CODE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SECRET_CODE: String
```

Broadcast Action: A debug code has been entered in the dialer.

This intent is broadcast by the system and OEM telephony apps may need to receive these broadcasts. And it requires the sender to be default dialer or has carrier privileges (see hasCarrierPrivileges).

These "secret codes" are used to activate developer menus by dialing certain codes. And they are of the form `*#*#<code>#*#*`. The intent will have the data URI: `android_secret_code://<code>`. It is possible that a manifest receiver would be woken up even if it is not currently running.

It is supposed to replace `https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Intents.html#SECRET_CODE_ACTION:kotlin.String` in the next Android version. Before that both of these two actions will be broadcast.

 Value: "android.telephony.action.SECRET_CODE"

### ACTION_SHOW_VOICEMAIL_NOTIFICATION

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_VOICEMAIL_NOTIFICATION: String
```

Broadcast intent action for letting the default dialer to know to show voicemail notification.

The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String` extra indicates which `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` the voicemail is received on. The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_NOTIFICATION_COUNT:kotlin.String` extra indicates the total numbers of unheard voicemails. The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_VOICEMAIL_NUMBER:kotlin.String` extra indicates the voicemail number if available. The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_CALL_VOICEMAIL_INTENT:kotlin.String` extra is a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will call the voicemail number when sent. This extra will be empty if the voicemail number is not set, and `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_LAUNCH_VOICEMAIL_SETTINGS_INTENT:kotlin.String` will be set instead. The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_LAUNCH_VOICEMAIL_SETTINGS_INTENT:kotlin.String` extra is a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will launch the voicemail settings. This extra is only available when the voicemail number is not set. The `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_IS_REFRESH:kotlin.String` extra indicates whether the notification is a refresh or a new notification.

 Value: "android.telephony.action.SHOW_VOICEMAIL_NOTIFICATION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_NOTIFICATION_COUNT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_VOICEMAIL_NUMBER:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_CALL_VOICEMAIL_INTENT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_LAUNCH_VOICEMAIL_SETTINGS_INTENT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_IS_REFRESH:kotlin.String`

### ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED: String
```

Broadcast Action: The subscription carrier identity has changed. This intent could be sent on the following events:

- Subscription absent. Carrier identity could change from a valid id to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int`.
- Subscription loaded. Carrier identity could change from `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int` to a valid id.
- The subscription carrier is recognized after a remote update.

The intent will have the following extra values:

<!-- -->

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_CARRIER_ID:kotlin.String` The up-to-date carrier id of the current subscription id.
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_CARRIER_NAME:kotlin.String` The up-to-date carrier name of the current subscription.
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_SUBSCRIPTION_ID:kotlin.String` The subscription id associated with the changed carrier identity.

<br />

This is a protected intent that can only be sent by the system.

 Value: "android.telephony.action.SUBSCRIPTION_CARRIER_IDENTITY_CHANGED"

### ACTION_SUBSCRIPTION_SPECIFIC_CARRIER_IDENTITY_CHANGED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SUBSCRIPTION_SPECIFIC_CARRIER_IDENTITY_CHANGED: String
```

Broadcast Action: The subscription specific carrier identity has changed. A specific carrier ID returns the fine-grained carrier ID of the current subscription. It can represent the fact that a carrier may be in effect an aggregation of other carriers (ie in an MVNO type scenario) where each of these specific carriers which are used to make up the actual carrier service may have different carrier configurations. A specific carrier ID could also be used, for example, in a scenario where a carrier requires different carrier configuration for different service offering such as a prepaid plan. the specific carrier ID would be used for configuration purposes, but apps wishing to know about the carrier itself should use the regular carrier ID returned by getSimCarrierId.

Similar like `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String`, this intent will be sent on the event of `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` while its also possible to be sent without `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` when specific carrier ID changes while carrier ID remains the same. e.g, the same subscription switches to different IMSI could potentially change its specific carrier ID while carrier id remains the same.

 Value: "android.telephony.action.SUBSCRIPTION_SPECIFIC_CARRIER_IDENTITY_CHANGED"

**See Also**

- getSimSpecificCarrierId
- getSimCarrierId

### ALLOWED_NETWORK_TYPES_REASON_CARRIER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALLOWED_NETWORK_TYPES_REASON_CARRIER: Int
```

To indicate allowed network type change is requested by carrier. Carrier configuration won't affect the settings configured through other reasons and will result in allowing network types that are in both configurations (i.e intersection of both sets).

 Value: 2

### ALLOWED_NETWORK_TYPES_REASON_USER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALLOWED_NETWORK_TYPES_REASON_USER: Int
```

To indicate allowed network type change is requested by user.

 Value: 0

### APPTYPE_CSIM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPTYPE_CSIM: Int
```

UICC application type is CSIM

 Value: 4

### APPTYPE_ISIM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPTYPE_ISIM: Int
```

UICC application type is ISIM

 Value: 5

### APPTYPE_RUIM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPTYPE_RUIM: Int
```

UICC application type is RUIM

 Value: 3

### APPTYPE_SIM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPTYPE_SIM: Int
```

UICC application type is SIM

 Value: 1

### APPTYPE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPTYPE_UNKNOWN: Int
```

UICC application type is unknown or not specified

 Value: 0

### APPTYPE_USIM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPTYPE_USIM: Int
```

UICC application type is USIM

 Value: 2

### AUTHTYPE_EAP_AKA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHTYPE_EAP_AKA: Int
```

Authentication type for UICC challenge is EAP AKA. See RFC 4187 for details.

 Value: 129

### AUTHTYPE_EAP_SIM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHTYPE_EAP_SIM: Int
```

Authentication type for UICC challenge is EAP SIM. See RFC 4186 for details.

 Value: 128

### AUTHTYPE_GBA_BOOTSTRAP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHTYPE_GBA_BOOTSTRAP: Int
```

Authentication type for GBA Bootstrap Challenge. Pass this authentication type into the getIccAuthentication API to perform a GBA Bootstrap challenge (BSF), with `data` (generated according to the procedure defined in 3GPP 33.220 Section 5.3.2 step.4) in base64 encoding. This method will return the Bootstrapping response in base64 encoding when ICC authentication is completed. Ref 3GPP 33.220 Section 5.3.2.

 Value: 132

### AUTHTYPE_GBA_NAF_KEY_EXTERNAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHTYPE_GBA_NAF_KEY_EXTERNAL: Int
```

Authentication type for GBA Network Application Functions (NAF) key External Challenge. Pass this authentication type into the getIccAuthentication API to perform a GBA Network Applications Functions (NAF) key External challenge using the NAF_ID parameter as the `data` in base64 encoding. This method will return the Ks_Ext_Naf key in base64 encoding when ICC authentication is completed. Ref 3GPP 33.220 Section 5.3.2.

 Value: 133

### CALL_COMPOSER_STATUS_BUSINESS_ONLY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_COMPOSER_STATUS_BUSINESS_ONLY: Int
```

Call composer status **Business Only** from user setting.

 Value: 2

### CALL_COMPOSER_STATUS_OFF

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_COMPOSER_STATUS_OFF: Int
```

Call composer status **OFF** from user setting.

 Value: 0

### CALL_COMPOSER_STATUS_ON

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_COMPOSER_STATUS_ON: Int
```

Call composer status **ON** from user setting.

 Value: 1

### CALL_STATE_IDLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_STATE_IDLE: Int
```

Device call state: No activity.

 Value: 0

### CALL_STATE_OFFHOOK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_STATE_OFFHOOK: Int
```

Device call state: Off-hook. At least one call exists that is dialing, active, or on hold, and no calls are ringing or waiting.

 Value: 2

### CALL_STATE_RINGING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_STATE_RINGING: Int
```

Device call state: Ringing. A new call arrived and is ringing or waiting. In the latter case, another call is already active.

 Value: 1

### CAPABILITY_SLICING_CONFIG_SUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_SLICING_CONFIG_SUPPORTED: String
```

Indicates whether getNetworkSlicingConfiguration is supported. See comments on respective methods for more information.

 Value: "CAPABILITY_SLICING_CONFIG_SUPPORTED"

### CARRIER_RESTRICTION_STATUS_NOT_RESTRICTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_RESTRICTION_STATUS_NOT_RESTRICTED: Int
```

The device is not restricted to a carrier

 Value: 1

### CARRIER_RESTRICTION_STATUS_RESTRICTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_RESTRICTION_STATUS_RESTRICTED: Int
```

The device is restricted to a carrier.

 Value: 2

### CARRIER_RESTRICTION_STATUS_RESTRICTED_TO_CALLER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_RESTRICTION_STATUS_RESTRICTED_TO_CALLER: Int
```

The device is restricted to the carrier of the calling application.

 Value: 3

### CARRIER_RESTRICTION_STATUS_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARRIER_RESTRICTION_STATUS_UNKNOWN: Int
```

Carrier restriction status value is unknown, in case modem did not provide any information about carrier restriction status.

 Value: 0

### CDMA_ROAMING_MODE_AFFILIATED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_ROAMING_MODE_AFFILIATED: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` which permits roaming on affiliated networks.

 Value: 1

### CDMA_ROAMING_MODE_ANY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_ROAMING_MODE_ANY: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` which permits roaming on any network.

 Value: 2

### CDMA_ROAMING_MODE_HOME

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_ROAMING_MODE_HOME: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` which only permits connections on home networks.

 Value: 0

### CDMA_ROAMING_MODE_RADIO_DEFAULT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CDMA_ROAMING_MODE_RADIO_DEFAULT: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Value for `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_MODE_INT:kotlin.String` which leaves the roaming mode set to the radio default or to the user's preference if they've indicated one.

 Value: -1

### DATA_ACTIVITY_DORMANT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ACTIVITY_DORMANT: Int
```

Data connection is active, but physical link is down

 Value: 4

### DATA_ACTIVITY_IN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ACTIVITY_IN: Int
```

Data connection activity: Currently receiving IP PPP traffic.

 Value: 1

### DATA_ACTIVITY_INOUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ACTIVITY_INOUT: Int
```

Data connection activity: Currently both sending and receiving IP PPP traffic.

 Value: 3

### DATA_ACTIVITY_NONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ACTIVITY_NONE: Int
```

Data connection activity: No traffic.

 Value: 0

### DATA_ACTIVITY_OUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ACTIVITY_OUT: Int
```

Data connection activity: Currently sending IP PPP traffic.

 Value: 2

### DATA_CONNECTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_CONNECTED: Int
```

Data connection state: Connected. IP traffic should be available.

 Value: 2

### DATA_CONNECTING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_CONNECTING: Int
```

Data connection state: Currently setting up a data connection.

 Value: 1

### DATA_DISCONNECTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_DISCONNECTED: Int
```

Data connection state: Disconnected. IP traffic not available.

 Value: 0

### DATA_DISCONNECTING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_DISCONNECTING: Int
```

Data connection state: Disconnecting. IP traffic may be available but will cease working imminently.

 Value: 4

### DATA_ENABLED_REASON_CARRIER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ENABLED_REASON_CARRIER: Int
```

To indicate enable or disable carrier data by the system based on carrier signalling or carrier privileged apps. Carrier data on/off won't affect user settings but will bypass the settings and turns off data internally if set to `false`.

 Value: 2

### DATA_ENABLED_REASON_OVERRIDE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ENABLED_REASON_OVERRIDE: Int
```

To indicate data was enabled or disabled due to mobile data policy overrides. Note that this is not a valid reason for setDataEnabledForReason and is only used to indicate that data enabled was changed due to an override.

 Value: 4

### DATA_ENABLED_REASON_POLICY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ENABLED_REASON_POLICY: Int
```

To indicate that data control due to policy. Usually used when data limit is passed. Policy data on/off won't affect user settings but will bypass the settings and turns off data internally if set to `false`.

 Value: 1

### DATA_ENABLED_REASON_THERMAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ENABLED_REASON_THERMAL: Int
```

To indicate enable or disable data by thermal service. Thermal data on/off won't affect user settings but will bypass the settings and turns off data internally if set to `false`.

 Value: 3

### DATA_ENABLED_REASON_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ENABLED_REASON_UNKNOWN: Int
```

To indicate that data was enabled or disabled due to an unknown reason. Note that this is not a valid reason for setDataEnabledForReason and is only used to indicate that data enabled was changed.

 Value: -1

### DATA_ENABLED_REASON_USER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_ENABLED_REASON_USER: Int
```

To indicate that user enabled or disabled data.

 Value: 0

### DATA_HANDOVER_IN_PROGRESS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_HANDOVER_IN_PROGRESS: Int
```

Data connection state: Handover in progress. The connection is being transited from cellular network to IWLAN, or from IWLAN to cellular network.

 Value: 5

### DATA_SUSPENDED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_SUSPENDED: Int
```

Data connection state: Suspended. The connection is up, but IP traffic is temporarily unavailable. For example, in a 2G network, data activity may be suspended when a voice call arrives.

 Value: 3

### DATA_UNKNOWN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_UNKNOWN: Int
```

Data connection state: Unknown. Used before we know the state.

 Value: -1

### DEFAULT_PORT_INDEX

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_PORT_INDEX: Int
```

Default port index for a UICC. On physical SIM cards the only available port is 0. See UiccPortInfo for more information on ports. See isSimPortAvailable for information on how portIndex is used on eUICCs.

 Value: 0

### ERI_FLASH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERI_FLASH: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

ERI (Enhanced Roaming Indicator) is FLASH i.e value 2 defined by 3GPP2 C.R1001-H v1.0 Table 8.1-1.

 Value: 2

### ERI_OFF

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERI_OFF: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

ERI (Enhanced Roaming Indicator) is OFF i.e value 1 defined by 3GPP2 C.R1001-H v1.0 Table 8.1-1.

 Value: 1

### ERI_ON

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERI_ON: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

ERI (Enhanced Roaming Indicator) is ON i.e value 0 defined by 3GPP2 C.R1001-H v1.0 Table 8.1-1.

 Value: 0

### EVENT_DISPLAY_EMERGENCY_MESSAGE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EVENT_DISPLAY_EMERGENCY_MESSAGE: String
```

Event reported from the Telephony stack to indicate that the `https://developer.android.com/reference/kotlin/android/telecom/Connection.html#` is not able to find any network and likely will not get connected. Upon receiving this event, the dialer app should start the app included in the extras bundle of this event if satellite is provisioned.

The dialer app receives this event via onConnectionEvent.

The `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter is guaranteed to include the following extras if the below conditions are met:

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE:kotlin.String` - the recommending handover type.
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_EMERGENCY_CALL_TO_SATELLITE_LAUNCH_INTENT:kotlin.String` - the `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` which will be launched by the Dialer app when receiving this connection event.

If the device is connected to satellite via carrier within the hysteresis time defined by the carrier config `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SATELLITE_CONNECTION_HYSTERESIS_SEC_INT:kotlin.String`, the component of the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_EMERGENCY_CALL_TO_SATELLITE_LAUNCH_INTENT:kotlin.String` will be set to the default SMS app.

Otherwise, if the overlay config `config_oem_enabled_satellite_handover_app` is present, the app defined by this config will be used as the component of the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_EMERGENCY_CALL_TO_SATELLITE_LAUNCH_INTENT:kotlin.String`. If this overlay config is empty, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_EMERGENCY_CALL_TO_SATELLITE_LAUNCH_INTENT:kotlin.String` will not be included in the event `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String`.

 Value: "android.telephony.event.DISPLAY_EMERGENCY_MESSAGE"

### EXTRA_ACTIVE_SIM_SUPPORTED_COUNT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ACTIVE_SIM_SUPPORTED_COUNT: String
```

The number of active SIM supported by current multi-SIM config. It's not related to how many SIM/subscriptions are currently active. Same value will be returned by getActiveModemCount. For single SIM mode, it's 1. For DSDS or DSDA mode, it's 2. For triple-SIM mode, it's 3. Extra of `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_MULTI_SIM_CONFIG_CHANGED:kotlin.String`. type: integer

 Value: "android.telephony.extra.ACTIVE_SIM_SUPPORTED_COUNT"

### EXTRA_APN_PROTOCOL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APN_PROTOCOL: String
```

An integer extra containing the protocol of the apn connection. Sent with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_PCO_VALUE:kotlin.String` broadcast. See the `PROTOCOL_*` constants in ApnSetting for a list of possible values.

 Value: "android.telephony.extra.APN_PROTOCOL"

### EXTRA_APN_TYPE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APN_TYPE: String
```

An integer extra containing the APN type. Sent with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_REQUEST_NETWORK_FAILED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_REDIRECTED:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_PCO_VALUE:kotlin.String` broadcasts. See the `TYPE_` constants in ApnSetting for a list of possible values.

 Value: "android.telephony.extra.APN_TYPE"

### EXTRA_CALL_VOICEMAIL_INTENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_VOICEMAIL_INTENT: String
```

The intent to call voicemail.

 Value: "android.telephony.extra.CALL_VOICEMAIL_INTENT"

### EXTRA_CARRIER_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CARRIER_ID: String
```

An int extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` which indicates the updated carrier id returned by getSimCarrierId.

Will be `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int` if the subscription is unavailable or the carrier cannot be identified.

 Value: "android.telephony.extra.CARRIER_ID"

### EXTRA_CARRIER_NAME

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CARRIER_NAME: String
```

An string extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` which indicates the updated carrier name of the current subscription.

 Value: "android.telephony.extra.CARRIER_NAME"

**See Also**

- getSimCarrierIdName

### EXTRA_DATA_FAIL_CAUSE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA_FAIL_CAUSE: String
```

An integer extra containing the data fail cause. Sent with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_REQUEST_NETWORK_FAILED:kotlin.String`. See DataFailCause for a list of possible values.

 Value: "android.telephony.extra.DATA_FAIL_CAUSE"

### EXTRA_DEFAULT_NETWORK_AVAILABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DEFAULT_NETWORK_AVAILABLE: String
```

A boolean extra indicating the availability of the default network. Sent with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_DEFAULT_NETWORK_AVAILABLE:kotlin.String` broadcast.

 Value: "android.telephony.extra.DEFAULT_NETWORK_AVAILABLE"

### EXTRA_EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE: String
```

Integer extra key used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String` which indicates the type of handover from emergency call to satellite messaging.

Will be either android.telephony.satellite.SatelliteManager#EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_SOS or android.telephony.satellite.SatelliteManager#EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE_T911

Set in the extras for the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String` connection event.

 Value: "android.telephony.extra.EMERGENCY_CALL_TO_SATELLITE_HANDOVER_TYPE"

### EXTRA_EMERGENCY_CALL_TO_SATELLITE_LAUNCH_INTENT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EMERGENCY_CALL_TO_SATELLITE_LAUNCH_INTENT: String
```

Extra key used with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EVENT_DISPLAY_EMERGENCY_MESSAGE:kotlin.String` for a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` which will be launched by the Dialer app.

 Value: "android.telephony.extra.EMERGENCY_CALL_TO_SATELLITE_LAUNCH_INTENT"

### EXTRA_HIDE_PUBLIC_SETTINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HIDE_PUBLIC_SETTINGS: String
```

The boolean value indicating whether the voicemail settings activity launched by `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CONFIGURE_VOICEMAIL:kotlin.String` should hide settings accessible through public API. This is used by dialer implementations which provides their own voicemail settings UI, but still needs to expose device specific voicemail settings to the user.

 Value: "android.telephony.extra.HIDE_PUBLIC_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CONFIGURE_VOICEMAIL:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#METADATA_HIDE_VOICEMAIL_SETTINGS_MENU:kotlin.String`

### EXTRA_INCOMING_NUMBER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INCOMING_NUMBER: String
```

**Deprecated:** *Companion apps for wearable devices should use the `https://developer.android.com/reference/kotlin/android/telecom/InCallService.html#` API to retrieve the phone number for calls instead. Apps performing call screening should use the `https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService.html#` API instead.*

Extra key used with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_PHONE_STATE_CHANGED:kotlin.String` broadcast for a String containing the incoming or outgoing phone number.

This extra is only populated for receivers of the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_PHONE_STATE_CHANGED:kotlin.String` broadcast which have been granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CALL_LOG:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` permissions.

For incoming calls, the phone number is only guaranteed to be populated when the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` changes from `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_IDLE:kotlin.String` to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_RINGING:kotlin.String`. If the incoming caller is from an unknown number, the extra will be populated with an empty string. For outgoing calls, the phone number is only guaranteed to be populated when the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` changes from `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_IDLE:kotlin.String` to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_OFFHOOK:kotlin.String`.

Retrieve with getStringExtra.

<br />

 Value: "incoming_number"

### EXTRA_IS_REFRESH

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_REFRESH: String
```

Boolean value representing whether the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SHOW_VOICEMAIL_NOTIFICATION:kotlin.String` is new or a refresh of an existing notification. Notification refresh happens after reboot or connectivity changes. The user has already been notified for the voicemail so it should not alert the user, and should not be shown again if the user has dismissed it.

 Value: "android.telephony.extra.IS_REFRESH"

### EXTRA_LAST_KNOWN_NETWORK_COUNTRY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LAST_KNOWN_NETWORK_COUNTRY: String
```

The extra used with an `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_NETWORK_COUNTRY_CHANGED:kotlin.String` to specify the last known the country code in ISO-3166-1 alpha-2 format. This might be an empty string when the country code was never available. The last known country code persists across reboot.

Retrieve with getStringExtra.

 Value: "android.telephony.extra.LAST_KNOWN_NETWORK_COUNTRY"

### EXTRA_LAUNCH_VOICEMAIL_SETTINGS_INTENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LAUNCH_VOICEMAIL_SETTINGS_INTENT: String
```

The intent to launch voicemail settings.

 Value: "android.telephony.extra.LAUNCH_VOICEMAIL_SETTINGS_INTENT"

### EXTRA_NETWORK_COUNTRY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NETWORK_COUNTRY: String
```

The extra used with an `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_NETWORK_COUNTRY_CHANGED:kotlin.String` to specify the the country code in ISO-3166-1 alpha-2 format. This is the same country code returned by getNetworkCountryIso. This might be an empty string when the country code is not available.

Retrieve with getStringExtra.

 Value: "android.telephony.extra.NETWORK_COUNTRY"

### EXTRA_NOTIFICATION_COUNT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_COUNT: String
```

The number of voice messages associated with the notification.

 Value: "android.telephony.extra.NOTIFICATION_COUNT"

### EXTRA_PCO_ID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PCO_ID: String
```

An integer extra indicating the ID for the PCO data. Sent with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_PCO_VALUE:kotlin.String` broadcast.

 Value: "android.telephony.extra.PCO_ID"

### EXTRA_PCO_VALUE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PCO_VALUE: String
```

A byte array extra containing PCO data read from the modem. Sent with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_PCO_VALUE:kotlin.String` broadcast.

 Value: "android.telephony.extra.PCO_VALUE"

### EXTRA_PHONE_ACCOUNT_HANDLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PHONE_ACCOUNT_HANDLE: String
```

The extra used with an `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CONFIGURE_VOICEMAIL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SHOW_VOICEMAIL_NOTIFICATION:kotlin.String` `Intent` to specify the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` the configuration or notification is for.

Retrieve with getParcelableExtra.

 Value: "android.telephony.extra.PHONE_ACCOUNT_HANDLE"

### EXTRA_REDIRECTION_URL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REDIRECTION_URL: String
```

String extra containing the redirection URL sent with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CARRIER_SIGNAL_REDIRECTED:kotlin.String`.

 Value: "android.telephony.extra.REDIRECTION_URL"

### EXTRA_SPECIFIC_CARRIER_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SPECIFIC_CARRIER_ID: String
```

An int extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_SPECIFIC_CARRIER_IDENTITY_CHANGED:kotlin.String` which indicates the updated specific carrier id returned by getSimSpecificCarrierId. Note, its possible specific carrier id changes while `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` remains the same e.g, when subscription switch to different IMSIs.

Will be `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int` if the subscription is unavailable or the carrier cannot be identified.

 Value: "android.telephony.extra.SPECIFIC_CARRIER_ID"

### EXTRA_SPECIFIC_CARRIER_NAME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SPECIFIC_CARRIER_NAME: String
```

An string extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_SPECIFIC_CARRIER_IDENTITY_CHANGED:kotlin.String` which indicates the updated specific carrier name returned by getSimSpecificCarrierIdName.

it's a user-facing name of the specific carrier id `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_SPECIFIC_CARRIER_ID:kotlin.String` e.g, Tracfone-AT\&T

 Value: "android.telephony.extra.SPECIFIC_CARRIER_NAME"

### EXTRA_STATE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_STATE: String
```

The lookup key used with the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_PHONE_STATE_CHANGED:kotlin.String` broadcast for a String containing the new call state.

Retrieve with getStringExtra.

 Value: "state"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_IDLE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_RINGING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE_OFFHOOK:kotlin.String`

### EXTRA_SUBSCRIPTION_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUBSCRIPTION_ID: String
```

An int extra used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_SUBSCRIPTION_CARRIER_IDENTITY_CHANGED:kotlin.String` to indicate the subscription which has changed; or in general whenever a subscription ID needs specified.

 Value: "android.telephony.extra.SUBSCRIPTION_ID"

### EXTRA_VOICEMAIL_NUMBER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VOICEMAIL_NUMBER: String
```

The voicemail number.

 Value: "android.telephony.extra.VOICEMAIL_NUMBER"

### INCLUDE_LOCATION_DATA_COARSE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INCLUDE_LOCATION_DATA_COARSE: Int
```

Include coarse location data. Indicates whether the caller would not like to receive location related information which will be sent if the caller already possess `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` and do not renounce the permissions.

 Value: 1

### INCLUDE_LOCATION_DATA_FINE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INCLUDE_LOCATION_DATA_FINE: Int
```

Include fine location data. Indicates whether the caller would not like to receive location related information which will be sent if the caller already possess `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` and do not renounce the permissions.

 Value: 2

### INCLUDE_LOCATION_DATA_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INCLUDE_LOCATION_DATA_NONE: Int
```

Specifies to not include any location related data. Indicates whether the caller would not like to receive location related information which will be sent if the caller already possess `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` and do not renounce the permissions.

 Value: 0

### METADATA_HIDE_VOICEMAIL_SETTINGS_MENU

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_HIDE_VOICEMAIL_SETTINGS_MENU: String
```

A boolean meta-data value indicating whether the voicemail settings should be hidden in the call settings page launched by `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#ACTION_SHOW_CALL_SETTINGS:kotlin.String`. Dialer implementations (see getDefaultDialerPackage) which would also like to manage voicemail settings should set this meta-data to `true` in the manifest registration of their application.

 Value: "android.telephony.HIDE_VOICEMAIL_SETTINGS_MENU"

**See Also**

- `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#ACTION_SHOW_CALL_SETTINGS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ACTION_CONFIGURE_VOICEMAIL:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_HIDE_PUBLIC_SETTINGS:kotlin.String`

### MULTISIM_ALLOWED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTISIM_ALLOWED: Int
```

The usage of multiple SIM cards at the same time to register on the network (e.g. Dual Standby or Dual Active) is supported.

 Value: 0

### MULTISIM_NOT_SUPPORTED_BY_CARRIER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTISIM_NOT_SUPPORTED_BY_CARRIER: Int
```

The usage of multiple SIM cards at the same time to register on the network (e.g. Dual Standby or Dual Active) is supported by the hardware, but restricted by the carrier.

 Value: 2

### MULTISIM_NOT_SUPPORTED_BY_HARDWARE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTISIM_NOT_SUPPORTED_BY_HARDWARE: Int
```

The usage of multiple SIM cards at the same time to register on the network (e.g. Dual Standby or Dual Active) is not supported by the hardware.

 Value: 1

### NETWORK_SELECTION_MODE_AUTO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_SELECTION_MODE_AUTO: Int
```

 Value: 1

### NETWORK_SELECTION_MODE_MANUAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_SELECTION_MODE_MANUAL: Int
```

 Value: 2

### NETWORK_SELECTION_MODE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_SELECTION_MODE_UNKNOWN: Int
```

 Value: 0

### NETWORK_TYPE_1xRTT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_1xRTT: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Current network is 1xRTT

 Value: 7

### NETWORK_TYPE_BITMASK_1xRTT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_1xRTT: Long
```

network type bitmask indicating the support of radio tech 1xRTT.

 Value: 64L

### NETWORK_TYPE_BITMASK_CDMA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_CDMA: Long
```

**Deprecated:** *Legacy CDMA is unsupported.*

network type bitmask indicating the support of radio tech CDMA(IS95A/IS95B).

 Value: 8L

### NETWORK_TYPE_BITMASK_EDGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_EDGE: Long
```

network type bitmask indicating the support of radio tech EDGE.

 Value: 2L

### NETWORK_TYPE_BITMASK_EHRPD

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_EHRPD: Long
```

**Deprecated:** *Legacy CDMA is unsupported.*

network type bitmask indicating the support of radio tech EHRPD.

 Value: 8192L

### NETWORK_TYPE_BITMASK_EVDO_0

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_EVDO_0: Long
```

network type bitmask indicating the support of radio tech EVDO 0.

 Value: 16L

### NETWORK_TYPE_BITMASK_EVDO_A

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_EVDO_A: Long
```

network type bitmask indicating the support of radio tech EVDO A.

 Value: 32L

### NETWORK_TYPE_BITMASK_EVDO_B

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_EVDO_B: Long
```

network type bitmask indicating the support of radio tech EVDO B.

 Value: 2048L

### NETWORK_TYPE_BITMASK_GPRS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_GPRS: Long
```

network type bitmask indicating the support of radio tech GPRS.

 Value: 1L

### NETWORK_TYPE_BITMASK_GSM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_GSM: Long
```

network type bitmask indicating the support of radio tech GSM.

 Value: 32768L

### NETWORK_TYPE_BITMASK_HSDPA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_HSDPA: Long
```

network type bitmask indicating the support of radio tech HSDPA.

 Value: 128L

### NETWORK_TYPE_BITMASK_HSPA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_HSPA: Long
```

network type bitmask indicating the support of radio tech HSPA.

 Value: 512L

### NETWORK_TYPE_BITMASK_HSPAP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_HSPAP: Long
```

network type bitmask indicating the support of radio tech HSPAP.

 Value: 16384L

### NETWORK_TYPE_BITMASK_HSUPA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_HSUPA: Long
```

network type bitmask indicating the support of radio tech HSUPA.

 Value: 256L

### NETWORK_TYPE_BITMASK_IWLAN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_IWLAN: Long
```

network type bitmask indicating the support of radio tech IWLAN.

 Value: 131072L

### NETWORK_TYPE_BITMASK_LTE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_LTE: Long
```

network type bitmask indicating the support of radio tech LTE.

 Value: 4096L

### NETWORK_TYPE_BITMASK_LTE_CA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_LTE_CA: Long
```

**Deprecated:** *Please use `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE:kotlin.Long` instead. Deprecated in Android U.*

NOT USED; this bitmask is exposed accidentally. If used, will be converted to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE:kotlin.Long`. network type bitmask indicating the support of radio tech LTE CA (carrier aggregation).

 Value: 262144L

### NETWORK_TYPE_BITMASK_NR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_NR: Long
```

network type bitmask indicating the support of radio tech NR(New Radio) 5G.

 Value: 524288L

### NETWORK_TYPE_BITMASK_TD_SCDMA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_TD_SCDMA: Long
```

network type bitmask indicating the support of radio tech TD_SCDMA.

 Value: 65536L

### NETWORK_TYPE_BITMASK_UMTS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_UMTS: Long
```

network type bitmask indicating the support of radio tech UMTS.

 Value: 4L

### NETWORK_TYPE_BITMASK_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_BITMASK_UNKNOWN: Long
```

network type bitmask unknown.

 Value: 0L

### NETWORK_TYPE_CDMA

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_CDMA: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Current network is CDMA: Either IS95A or IS95B

 Value: 4

### NETWORK_TYPE_EDGE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_EDGE: Int
```

Current network is EDGE

 Value: 2

### NETWORK_TYPE_EHRPD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_EHRPD: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Current network is eHRPD

 Value: 14

### NETWORK_TYPE_EVDO_0

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_EVDO_0: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Current network is EVDO revision 0

 Value: 5

### NETWORK_TYPE_EVDO_A

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_EVDO_A: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Current network is EVDO revision A

 Value: 6

### NETWORK_TYPE_EVDO_B

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_EVDO_B: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Current network is EVDO revision B

 Value: 12

### NETWORK_TYPE_GPRS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_GPRS: Int
```

Current network is GPRS

 Value: 1

### NETWORK_TYPE_GSM

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_GSM: Int
```

Current network is GSM

 Value: 16

### NETWORK_TYPE_HSDPA

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_HSDPA: Int
```

Current network is HSDPA

 Value: 8

### NETWORK_TYPE_HSPA

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_HSPA: Int
```

Current network is HSPA

 Value: 10

### NETWORK_TYPE_HSPAP

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_HSPAP: Int
```

Current network is HSPA+

 Value: 15

### NETWORK_TYPE_HSUPA

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_HSUPA: Int
```

Current network is HSUPA

 Value: 9

### NETWORK_TYPE_IDEN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_IDEN: Int
```

**Deprecated:** *Legacy network type no longer being used starting in Android U.*

Current network is iDen

 Value: 11

### NETWORK_TYPE_IWLAN

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_IWLAN: Int
```

Current network is IWLAN

 Value: 18

### NETWORK_TYPE_LTE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_LTE: Int
```

Current network is LTE

 Value: 13

### NETWORK_TYPE_NR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_NR: Int
```

Current network is NR (New Radio) 5G. This will only be returned for 5G SA. For 5G NSA, the network type will be `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int`.

 Value: 20

### NETWORK_TYPE_TD_SCDMA

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_TD_SCDMA: Int
```

Current network is TD_SCDMA

 Value: 17

### NETWORK_TYPE_UMTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_UMTS: Int
```

Current network is UMTS

 Value: 3

### NETWORK_TYPE_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_UNKNOWN: Int
```

Network type is unknown

 Value: 0

### PHONE_TYPE_CDMA

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_TYPE_CDMA: Int
```

**Deprecated:** *Legacy CDMA is unsupported.*

Phone radio is CDMA.

 Value: 2

### PHONE_TYPE_GSM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_TYPE_GSM: Int
```

Phone radio is GSM.

 Value: 1

### PHONE_TYPE_NONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_TYPE_NONE: Int
```

No phone radio.

 Value: 0

### PHONE_TYPE_SIP

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_TYPE_SIP: Int
```

Phone is via SIP.

 Value: 3

### PREMIUM_CAPABILITY_PRIORITIZE_LATENCY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREMIUM_CAPABILITY_PRIORITIZE_LATENCY: Int
```

A premium capability that boosts the network to allow for real-time interactive traffic by prioritizing low latency communication. Corresponds to `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_PRIORITIZE_LATENCY:kotlin.Int`.

 Value: 34

### PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_IN_PROGRESS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_IN_PROGRESS: Int
```

Purchase premium capability failed because a request was already made and is in progress. This may have been requested by either the same app or another app. Subsequent attempts will return the same error until the previous request completes.

 Value: 4

### PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_PURCHASED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_PURCHASED: Int
```

Purchase premium capability failed because it is already purchased and available. Subsequent attempts will return the same error until the performance boost expires.

 Value: 3

### PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_DISABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_DISABLED: Int
```

Purchase premium capability failed because the carrier disabled or does not support the capability, as specified in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTED_PREMIUM_CAPABILITIES_INT_ARRAY:kotlin.String`. Subsequent attempts will return the same error until the carrier enables the feature.

 Value: 7

### PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_ERROR: Int
```

Purchase premium capability failed because the carrier app did not indicate success. Subsequent attempts will be throttled for the amount of time specified by CarrierConfigManager and return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED:kotlin.Int`.

 Value: 8

### PURCHASE_PREMIUM_CAPABILITY_RESULT_ENTITLEMENT_CHECK_FAILED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_ENTITLEMENT_CHECK_FAILED: Int
```

Purchase premium capability failed because the entitlement check failed. Subsequent attempts will be throttled for the amount of time specified by CarrierConfigManager and return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED:kotlin.Int`. Throttling will be reevaluated when the network is no longer congested.

 Value: 13

### PURCHASE_PREMIUM_CAPABILITY_RESULT_FEATURE_NOT_SUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_FEATURE_NOT_SUPPORTED: Int
```

Purchase premium capability failed because the device does not support the feature. Subsequent attempts will return the same error.

 Value: 10

### PURCHASE_PREMIUM_CAPABILITY_RESULT_NETWORK_NOT_AVAILABLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_NETWORK_NOT_AVAILABLE: Int
```

Purchase premium capability failed because the network is not available. Subsequent attempts will return the same error until network conditions change.

 Value: 12

### PURCHASE_PREMIUM_CAPABILITY_RESULT_NOT_DEFAULT_DATA_SUBSCRIPTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_NOT_DEFAULT_DATA_SUBSCRIPTION: Int
```

Purchase premium capability failed because the request was not made on the default data subscription, indicated by getDefaultDataSubscriptionId. Subsequent attempts will return the same error until the request is made on the default data subscription.

 Value: 14

### PURCHASE_PREMIUM_CAPABILITY_RESULT_NOT_FOREGROUND

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_NOT_FOREGROUND: Int
```

Purchase premium capability failed because the requesting application is not in the foreground. Subsequent attempts will return the same error until the requesting application moves to the foreground.

 Value: 5

### PURCHASE_PREMIUM_CAPABILITY_RESULT_PENDING_NETWORK_SETUP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_PENDING_NETWORK_SETUP: Int
```

Purchase premium capability was successful and is waiting for the network to setup the slicing configuration. If the setup is complete within the time specified by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_NETWORK_SETUP_TIME_MILLIS_LONG:kotlin.String`, subsequent requests will return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_PURCHASED:kotlin.Int` until the purchase expires. If the setup is not complete within the time specified above, applications can request the premium capability again.

 Value: 15

### PURCHASE_PREMIUM_CAPABILITY_RESULT_REQUEST_FAILED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_REQUEST_FAILED: Int
```

Purchase premium capability failed because the telephony service is unavailable or there was an error in the phone process. Subsequent attempts will return the same error until request conditions are satisfied.

 Value: 11

### PURCHASE_PREMIUM_CAPABILITY_RESULT_SUCCESS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_SUCCESS: Int
```

Purchase premium capability request was successful. Once the purchase result is successful, the network must set up a slicing configuration for the purchased premium capability within the timeout specified by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_NETWORK_SETUP_TIME_MILLIS_LONG:kotlin.String`. During the setup time, subsequent attempts will return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_PENDING_NETWORK_SETUP:kotlin.Int`. After setup is complete, subsequent attempts will return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_PURCHASED:kotlin.Int` until the boost expires. The expiry time is determined by the type or duration of boost purchased from the carrier, provided at `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_PURCHASE_URL_STRING:kotlin.String`.

 Value: 1

### PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED: Int
```

Purchase premium capability failed because the request is throttled. If purchasing premium capabilities is throttled, it will be for the amount of time specified by CarrierConfigManager. If displaying the performance boost notification is throttled, it will be for the amount of time specified by CarrierConfigManager. We will show the performance boost notification to the user up to the daily and monthly maximum number of times specified by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_MAXIMUM_DAILY_NOTIFICATION_COUNT_INT:kotlin.String` and `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_MAXIMUM_MONTHLY_NOTIFICATION_COUNT_INT:kotlin.String`. Subsequent attempts will return the same error until the request is no longer throttled or throttling conditions change.

 Value: 2

### PURCHASE_PREMIUM_CAPABILITY_RESULT_TIMEOUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_TIMEOUT: Int
```

Purchase premium capability failed because we did not receive a response from the user for the performance boost notification within the time specified by `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_PREMIUM_CAPABILITY_NOTIFICATION_DISPLAY_TIMEOUT_MILLIS_LONG:kotlin.String`. The performance boost notification will be automatically dismissed and subsequent attempts will be throttled for the amount of time specified by CarrierConfigManager and return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED:kotlin.Int`.

 Value: 9

### PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_CANCELED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_CANCELED: Int
```

Purchase premium capability failed because the user canceled the operation. Subsequent attempts will be throttled for the amount of time specified by CarrierConfigManager and return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED:kotlin.Int`.

 Value: 6

### PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_DISABLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_DISABLED: Int
```

Purchase premium capability failed because the user disabled the feature. Subsequent attempts will be throttled for the amount of time specified by CarrierConfigManager and return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED:kotlin.Int`.

 Value: 16

### SET_OPPORTUNISTIC_SUB_INACTIVE_SUBSCRIPTION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SET_OPPORTUNISTIC_SUB_INACTIVE_SUBSCRIPTION: Int
```

The subscription is not valid. It must be an active opportunistic subscription.

 Value: 2

### SET_OPPORTUNISTIC_SUB_NO_OPPORTUNISTIC_SUB_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SET_OPPORTUNISTIC_SUB_NO_OPPORTUNISTIC_SUB_AVAILABLE: Int
```

The subscription is not valid. It must be an opportunistic subscription.

 Value: 3

### SET_OPPORTUNISTIC_SUB_REMOTE_SERVICE_EXCEPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SET_OPPORTUNISTIC_SUB_REMOTE_SERVICE_EXCEPTION: Int
```

Subscription service happened remote exception.

 Value: 4

### SET_OPPORTUNISTIC_SUB_SUCCESS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SET_OPPORTUNISTIC_SUB_SUCCESS: Int
```

No error. Operation succeeded.

 Value: 0

### SET_OPPORTUNISTIC_SUB_VALIDATION_FAILED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SET_OPPORTUNISTIC_SUB_VALIDATION_FAILED: Int
```

Validation failed when trying to switch to preferred subscription.

 Value: 1

### SIM_STATE_ABSENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_ABSENT: Int
```

SIM card state: no SIM card is available in the device

 Value: 1

### SIM_STATE_CARD_IO_ERROR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_CARD_IO_ERROR: Int
```

SIM card state: SIM Card Error, present but faulty

 Value: 8

### SIM_STATE_CARD_RESTRICTED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_CARD_RESTRICTED: Int
```

SIM card state: SIM Card restricted, present but not usable due to carrier restrictions.

 Value: 9

### SIM_STATE_NETWORK_LOCKED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_NETWORK_LOCKED: Int
```

SIM card state: Locked: requires a network PIN to unlock

 Value: 4

### SIM_STATE_NOT_READY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_NOT_READY: Int
```

SIM card state: SIM Card is NOT READY

 Value: 6

### SIM_STATE_PERM_DISABLED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_PERM_DISABLED: Int
```

SIM card state: SIM Card Error, permanently disabled

 Value: 7

### SIM_STATE_PIN_REQUIRED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_PIN_REQUIRED: Int
```

SIM card state: Locked: requires the user's SIM PIN to unlock

 Value: 2

### SIM_STATE_PUK_REQUIRED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_PUK_REQUIRED: Int
```

SIM card state: Locked: requires the user's SIM PUK to unlock

 Value: 3

### SIM_STATE_READY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_READY: Int
```

SIM card state: Ready

 Value: 5

### SIM_STATE_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIM_STATE_UNKNOWN: Int
```

SIM card state: Unknown. Signifies that the SIM is in transition between states. For example, when the user inputs the SIM pin under PIN_REQUIRED state, a query for sim status returns this state before turning to SIM_STATE_READY. These are the ordinal value of IccCardConstants.State.

 Value: 0

### TTY_MODE_FULL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TTY_MODE_FULL: Int
```

TTY (teletypewriter) mode is on. The speaker is off and the microphone is muted. The user will communicate with the remote party by sending and receiving text messages.

 Value: 1

### TTY_MODE_HCO

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TTY_MODE_HCO: Int
```

TTY (teletypewriter) mode is in hearing carryover mode (HCO). The microphone is muted but the speaker is on. The user will communicate with the remote party by sending text messages and hearing an audible reply.

 Value: 2

### TTY_MODE_OFF

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TTY_MODE_OFF: Int
```

TTY (teletypewriter) mode is off.

 Value: 0

### TTY_MODE_VCO

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TTY_MODE_VCO: Int
```

TTY (teletypewriter) mode is in voice carryover mode (VCO). The speaker is off but the microphone is still on. User will communicate with the remote party by speaking and receiving text message replies.

 Value: 3

### UNINITIALIZED_CARD_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNINITIALIZED_CARD_ID: Int
```

A UICC card identifier used before the UICC card is loaded. See getCardIdForDefaultEuicc and getCardId.

Note that once the UICC card is loaded, the card ID may become `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNSUPPORTED_CARD_ID:kotlin.Int`.

 Value: -2

### UNKNOWN_CARRIER_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN_CARRIER_ID: Int
```

An unknown carrier id. It could either be subscription unavailable or the subscription carrier cannot be recognized. Unrecognized carriers here means getSimOperator cannot be identified.

 Value: -1

### UNSUPPORTED_CARD_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNSUPPORTED_CARD_ID: Int
```

A UICC card identifier used if the device does not support the operation. For example, getCardIdForDefaultEuicc returns this value if the device has no eUICC, or the eUICC cannot be read.

 Value: -1

### UPDATE_AVAILABLE_NETWORKS_ABORTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_ABORTED: Int
```

The request is aborted.

 Value: 2

### UPDATE_AVAILABLE_NETWORKS_DISABLE_MODEM_FAIL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_DISABLE_MODEM_FAIL: Int
```

Disable modem fail.

 Value: 5

### UPDATE_AVAILABLE_NETWORKS_ENABLE_MODEM_FAIL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_ENABLE_MODEM_FAIL: Int
```

Enable modem fail.

 Value: 6

### UPDATE_AVAILABLE_NETWORKS_INVALID_ARGUMENTS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_INVALID_ARGUMENTS: Int
```

The parameter passed in is invalid.

 Value: 3

### UPDATE_AVAILABLE_NETWORKS_MULTIPLE_NETWORKS_NOT_SUPPORTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_MULTIPLE_NETWORKS_NOT_SUPPORTED: Int
```

Carrier app does not support multiple available networks.

 Value: 7

### UPDATE_AVAILABLE_NETWORKS_NO_CARRIER_PRIVILEGE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_NO_CARRIER_PRIVILEGE: Int
```

No carrier privilege.

 Value: 4

### UPDATE_AVAILABLE_NETWORKS_NO_OPPORTUNISTIC_SUB_AVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_NO_OPPORTUNISTIC_SUB_AVAILABLE: Int
```

The subscription is not valid. It must be an opportunistic subscription.

 Value: 8

### UPDATE_AVAILABLE_NETWORKS_REMOTE_SERVICE_EXCEPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_REMOTE_SERVICE_EXCEPTION: Int
```

There is no OpportunisticNetworkService.

 Value: 9

### UPDATE_AVAILABLE_NETWORKS_SERVICE_IS_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_SERVICE_IS_DISABLED: Int
```

OpportunisticNetworkService is disabled.

 Value: 10

### UPDATE_AVAILABLE_NETWORKS_SIM_PORT_NOT_AVAILABLE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_SIM_PORT_NOT_AVAILABLE: Int
```

SIM port is not available to switch to opportunistic subscription.

 Value: 11

### UPDATE_AVAILABLE_NETWORKS_SUCCESS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_SUCCESS: Int
```

No error. Operation succeeded.

 Value: 0

### UPDATE_AVAILABLE_NETWORKS_UNKNOWN_FAILURE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPDATE_AVAILABLE_NETWORKS_UNKNOWN_FAILURE: Int
```

There is a unknown failure happened.

 Value: 1

### USSD_ERROR_NOT_ALLOWED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USSD_ERROR_NOT_ALLOWED: Int
```

Failure code returned when a USSD request has failed to execute because the calling app is not allowed to send USSD requests.

Returned via onReceiveUssdResponseFailed.

 Value: -3

### USSD_ERROR_SERVICE_UNAVAIL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USSD_ERROR_SERVICE_UNAVAIL: Int
```

Failure code returned when a USSD request has failed to execute because the Telephony service is unavailable.

Returned via onReceiveUssdResponseFailed.

 Value: -2

### USSD_RETURN_FAILURE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USSD_RETURN_FAILURE: Int
```

Failed code returned when the mobile network has failed to complete a USSD request.

Returned via onReceiveUssdResponseFailed.

 Value: -1

### VVM_TYPE_CVVM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VVM_TYPE_CVVM: String
```

A flavor of OMTP protocol with a different mobile originated (MO) format

 Value: "vvm_type_cvvm"

### VVM_TYPE_OMTP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VVM_TYPE_OMTP: String
```

The OMTP protocol.

 Value: "vvm_type_omtp"

## Public methods

### canChangeDtmfToneLength

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canChangeDtmfToneLength(): Boolean
```

Whether the device supports configuring the DTMF tone length. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the DTMF tone length can be changed, and `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### clearSignalStrengthUpdateRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearSignalStrengthUpdateRequest(request: SignalStrengthUpdateRequest): Unit
```

Clear a SignalStrengthUpdateRequest from the system.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges).

If the given request was not set before, this operation is a no-op. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `request` | [SignalStrengthUpdateRequest](SignalStrengthUpdateRequest.md): the SignalStrengthUpdateRequest to be cleared from the System. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

**See Also**

- setSignalStrengthUpdateRequest

### createForPhoneAccountHandle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createForPhoneAccountHandle(phoneAccountHandle: PhoneAccountHandle!): TelephonyManager?
```

Create a new TelephonyManager object pinned to the subscription ID associated with the given phone account.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#?` | a TelephonyManager that uses the given phone account for all calls, or `null` if the phone account does not correspond to a valid subscription ID. |

### createForSubscriptionId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createForSubscriptionId(subId: Int): TelephonyManager!
```

Create a new TelephonyManager object pinned to the given subscription ID.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#!` | a TelephonyManager that uses the given subId for all calls. |

### doesSwitchMultiSimConfigTriggerReboot

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun doesSwitchMultiSimConfigTriggerReboot(): Boolean
```

Get whether making changes to modem configurations by switchMultiSimConfig will trigger device reboot. The modem configuration change refers to switching from single SIM configuration to DSDS or the other way around.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if reboot will be triggered after making changes to modem configurations, otherwise return `false`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getActiveModemCount

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveModemCount(): Int
```

Returns the number of logical modems currently configured to be activated.

- Returns 0 if none of voice, sms, data is supported.
- Returns 1 for Single standby mode (Single SIM functionality).
- Returns 2 for Dual standby mode (Dual SIM functionality).
- Returns 3 for Tri standby mode (Tri SIM functionality).

<br />

### getAllCellInfo

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllCellInfo(): MutableList<CellInfo!>!
```

Requests all available cell information from all radios on the device including the camped/registered, serving, and neighboring cells.

The response can include one or more CellInfoGsm, CellInfoCdma, CellInfoTdscdma, CellInfoLte, and CellInfoWcdma objects, in any combination. It is typical to see instances of one or more of any these in the list. In addition, zero or more of the returned objects may be considered registered; that is, their isRegistered methods may return true, indicating that the cell is being used or would be used for signaling communication if necessary.

Beginning with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, if this API results in a change of the cached CellInfo, that change will be reported via onCellInfoChanged.

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or higher will no longer trigger a refresh of the cached CellInfo by invoking this API. Instead, those apps will receive the latest cached results, which may not be current. Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or higher that wish to request updated CellInfo should call requestCellInfoUpdate; however, in all cases, updates will be rate-limited and are not guaranteed. To determine the recency of CellInfo data, callers should check getTimeStamp.

This method returns valid data for devices with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`. In cases where only partial information is available for a particular CellInfo entry, unavailable fields will be reported as `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int`. All reported cells will include at least a valid set of technology-specific identification info and a power level measurement.

This method is preferred over using getCellLocation. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/CellInfo!>!` | List of CellInfo; null if cell information is unavailable. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getAllowedNetworkTypesForReason

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowedNetworkTypesForReason(reason: Int): Long
```

Get the allowed network types for certain reason. getAllowedNetworkTypesForReason returns allowed network type for a specific reason.

Requires permission: android.Manifest.READ_PRIVILEGED_PHONE_STATE or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the TelephonyManager#CAPABILITY_USES_ALLOWED_NETWORK_TYPES_BITMASK feature which can be detected using isRadioInterfaceCapabilitySupported.

| Parameters ||
|---|---|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the reason the allowed network type change is taking place. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ALLOWED_NETWORK_TYPES_REASON_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ALLOWED_NETWORK_TYPES_REASON_CARRIER:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the allowed network type bitmask. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_UNKNOWN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_GSM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_GPRS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EDGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_CDMA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_1xRTT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_0:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_A:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_B:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EHRPD:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSUPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSDPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSPAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_UMTS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_TD_SCDMA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE_CA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_NR:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_IWLAN:kotlin.Long` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if invalid AllowedNetworkTypesReason is passed. |
| `java.lang.IllegalStateException` | if the Telephony process is not currently available. |
| `java.lang.SecurityException` | if the caller does not have the required permission/privileges |
| --- | --- |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getCallComposerStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCallComposerStatus(): Int
```

Get the user-set status for enriched calling with call composer.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the user-set status for enriched calling with call composer, either of `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_ON:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_OFF:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_ON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_BUSINESS_ONLY:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have the permission. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### getCallState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCallState(): Int
```

**Deprecated:** *Use getCallStateForSubscription to retrieve the call state for a specific telephony subscription (which allows carrier privileged apps), `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.CallStateListener` for real-time call state updates, or isInCall, which supplies an aggregate "in call" state for the entire device.*

Returns the state of all calls on the device.

This method considers not only calls in the Telephony stack, but also calls via other `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#` implementations.

Note: The call state returned via this method may differ from what is reported by onCallStateChanged, as that callback only considers Telephony (mobile) calls.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` for applications targeting API level 31+.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current call state. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_IDLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_RINGING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_OFFHOOK:kotlin.Int` |

### getCallStateForSubscription

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCallStateForSubscription(): Int
```

Retrieve the call state for a specific subscription that was specified when this TelephonyManager instance was created.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling application has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The call state of the subscription associated with this TelephonyManager instance. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_IDLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_RINGING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_OFFHOOK:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

**See Also**

- createForSubscriptionId
- createForPhoneAccountHandle

### getCardIdForDefaultEuicc

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCardIdForDefaultEuicc(): Int
```

Get the card ID of the default eUICC card. If the eUICCs have not yet been loaded, returns `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNINITIALIZED_CARD_ID:kotlin.Int`. If there is no eUICC or the device does not support card IDs for eUICCs, returns `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNSUPPORTED_CARD_ID:kotlin.Int`.

The card ID is a unique identifier associated with a UICC or eUICC card. Card IDs are unique to a device, and always refer to the same UICC or eUICC card unless the device goes through a factory reset. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | card ID of the default eUICC card, if loaded. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`. |

### getCarrierConfig

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCarrierConfig(): PersistableBundle!
```

Returns the carrier config of the subscription ID pinned to the TelephonyManager. If an invalid subscription ID is pinned to the TelephonyManager, the returned config will contain default values.

This method may take several seconds to complete, so it should only be called from a worker thread.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
This method may take several seconds to complete, so it should only be called from a worker thread. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- getConfigForSubId
- createForSubscriptionId
- createForPhoneAccountHandle

### getCarrierIdFromSimMccMnc

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCarrierIdFromSimMccMnc(): Int
```

Returns carrier id based on sim MCCMNC (returned by getSimOperator) only. This is used for fallback when configurations/logic for exact carrier id getSimCarrierId are not found. Android carrier id table [here](https://android.googlesource.com/platform/packages/providers/TelephonyProvider/+/master/assets/latest_carrier_id/carrier_list.textpb) can be updated out-of-band, its possible a MVNO (Mobile Virtual Network Operator) carrier was not fully recognized and assigned to its MNO (Mobile Network Operator) carrier id by default. After carrier id table update, a new carrier id was assigned. If apps don't take the update with the new id, it might be helpful to always fallback by using carrier id based on MCCMNC if there is no match. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | matching carrier id from sim MCCMNC. Return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int` if the subscription is unavailable or the carrier cannot be identified. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getCarrierRestrictionStatus

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCarrierRestrictionStatus(
    executor: Executor, 
    resultListener: Consumer<Int!>
): Unit
```

Get the carrier restriction status of the device.

To fetch the carrier restriction status of the device the calling application needs to be allowlisted to Android at [here](https://android.googlesource.com/platform/packages/services/Telephony/+/master/assets/CarrierRestrictionOperatorDetails.json). The calling application also needs the READ_PHONE_STATE permission. The return value of the API is as follows.

- return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_RESTRICTED_TO_CALLER:kotlin.Int` if the caller and the device locked by the network are same
- return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_RESTRICTED:kotlin.Int` if the caller and the device locked by the network are different
- return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_NOT_RESTRICTED:kotlin.Int` if the device is not locked
- return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_UNKNOWN:kotlin.Int` if the device locking state is unavailable or radio does not supports the feature

. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor on which the result listener will be called. This value cannot be `null`. |
| `resultListener` | [Consumer](../java.util.function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: `https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#` that will be called with the carrier restriction status result fetched from the radio. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_NOT_RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CARRIER_RESTRICTION_STATUS_RESTRICTED_TO_CALLER:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have the required permission/privileges or if the caller is not pre-registered. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getCellLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCellLocation(): CellLocation!
```

**Deprecated:** *use getAllCellInfo instead, which returns a superset of this API.*

Returns the current location of the device.

If there is only one radio in the device and that radio has an LTE connection, this method will return null. The implementation must not to try add LTE identifiers into the existing cdma/gsm classes.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/CellLocation!` | Current location of the device or null if not available. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getCurrentTtyMode

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentTtyMode(): Int
```

Returns the current TTY mode of the device. For TTY to be on the user must enable it in settings and have a wired headset plugged in. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#TTY_MODE_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#TTY_MODE_FULL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#TTY_MODE_HCO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#TTY_MODE_VCO:kotlin.Int` |

### getDataActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDataActivity(): Int
```

Returns a constant indicating the type of activity on a data connection (cellular). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_IN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_OUT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_INOUT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ACTIVITY_DORMANT:kotlin.Int`

### getDataNetworkType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDataNetworkType(): Int
```

Returns a constant indicating the radio technology (network type) currently in use on the device for data transmission. If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getActiveDataSubscriptionId. Note: Before getActiveDataSubscriptionId was introduced in API level 30, it was applied to getDefaultDataSubscriptionId which may be different now from getActiveDataSubscriptionId, e.g. when opportunistic network is providing cellular internet connection to the user.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the network type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int`

### getDataState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDataState(): Int
```

Returns a constant indicating the current data connection state (cellular). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_DISCONNECTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_CONNECTING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_CONNECTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_SUSPENDED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_DISCONNECTING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_HANDOVER_IN_PROGRESS:kotlin.Int`

### getDeviceId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceId(): String!
```

**Deprecated:** *Use #getImei which returns IMEI for GSM or #getMeid which returns MEID for CDMA.*

Returns the unique device ID, for example, the IMEI for GSM and the MEID or ESN for CDMA phones. Return null if device ID is not available.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges) on any active subscription.
- If the calling app is the default SMS role holder (see isRoleHeld).

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

### getDeviceId

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceId(slotIndex: Int): String!
```

**Deprecated:** *Use #getImei which returns IMEI for GSM or #getMeid which returns MEID for CDMA.*

Returns the unique device ID of a subscription, for example, the IMEI for GSM and the MEID for CDMA phones. Return null if device ID is not available.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges) on any active subscription.
- If the calling app is the default SMS role holder (see isRoleHeld).

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of which deviceID is returned |

### getDeviceSoftwareVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceSoftwareVersion(): String?
```

Returns the software version number for the device, for example, the IMEI/SV for GSM phones. Return null if the software version is not available.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`. |

### getEmergencyNumberList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEmergencyNumberList(): MutableMap<Int!, MutableList<EmergencyNumber!>!>
```

Get the emergency number list based on current locale, sim, default, modem and network.

In each returned list, the emergency number EmergencyNumber coming from higher priority sources will be located at the smaller index; the priority order of sources are: `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_NETWORK_SIGNALING:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_SIM:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_DATABASE:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_DEFAULT:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_MODEM_CONFIG:kotlin.Int`

The subscriptions which the returned list would be based on, are all the active subscriptions, no matter which subscription could be used to create TelephonyManager.

Requires permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber!>!>` | Map including the keys as the active subscription IDs (Note: if there is no active subscription, the key is getDefaultSubscriptionId) and the value as the list of EmergencyNumber; empty Map if this information is not available; or throw a SecurityException if the caller does not have the permission. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getEmergencyNumberList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEmergencyNumberList(categories: Int): MutableMap<Int!, MutableList<EmergencyNumber!>!>
```

Get the per-category emergency number list based on current locale, sim, default, modem and network.

In each returned list, the emergency number EmergencyNumber coming from higher priority sources will be located at the smaller index; the priority order of sources are: `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_NETWORK_SIGNALING:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_SIM:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_DATABASE:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_DEFAULT:kotlin.Int` \> `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_MODEM_CONFIG:kotlin.Int`

The subscriptions which the returned list would be based on, are all the active subscriptions, no matter which subscription could be used to create TelephonyManager.

Requires permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`

| Parameters ||
|---|---|
| `categories` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the emergency service categories which are the bitwise-OR combination of the following constants: 1. `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED:kotlin.Int` 2. `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_POLICE:kotlin.Int` 3. `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_AMBULANCE:kotlin.Int` 4. `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_FIRE_BRIGADE:kotlin.Int` 5. `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MARINE_GUARD:kotlin.Int` 6. `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MOUNTAIN_RESCUE:kotlin.Int` 7. `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MIEC:kotlin.Int` 8. `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_AIEC:kotlin.Int` . Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_POLICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_AMBULANCE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_FIRE_BRIGADE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MARINE_GUARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MOUNTAIN_RESCUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MIEC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_AIEC:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber!>!>` | Map including the keys as the active subscription IDs (Note: if there is no active subscription, the key is getDefaultSubscriptionId) and the value as the list of EmergencyNumber; empty Map if this information is not available; or throw a SecurityException if the caller does not have the permission. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the Telephony process is not currently available. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getEquivalentHomePlmns

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEquivalentHomePlmns(): MutableList<String!>
```

Returns a list of the equivalent home PLMNs (EF_EHPLMN) from the USIM app.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | A list of equivalent home PLMNs. Returns an empty list if EF_EHPLMN is empty or does not exist on the SIM card. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the Telephony process is not currently available. |
| `java.lang.SecurityException` | if the caller doesn't have the permission. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |
| --- | --- |

### getForbiddenPlmns

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getForbiddenPlmns(): Array<String!>!
```

Returns an array of Forbidden PLMNs from the USIM App Returns null if the query fails.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of forbidden PLMNs or null if not available |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getGroupIdLevel1

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupIdLevel1(): String!
```

Returns the Group Identifier Level1 for a GSM phone. Return null if it is unavailable.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getIccAuthentication

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIccAuthentication(
    appType: Int, 
    authType: Int, 
    data: String!
): String!
```

Returns the response of authentication for the default subscription. Returns null if the authentication hasn't been successful

Requires one of the following permissions:

- the calling app has carrier privileges (see hasCarrierPrivileges).
- the calling app has been granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_ICC_AUTH_WITH_DEVICE_IDENTIFIER:kotlin.String` permission.
- the calling app has been granted the android.Manifest.permission#USE_ICC_AUTH permission.

The use of android.Manifest.permission#READ_PRIVILEGED_PHONE_STATE is no longer supported. Use android.Manifest.permission#USE_ICC_AUTH instead. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `appType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the icc application type, like `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#APPTYPE_USIM:kotlin.Int` |
| `authType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the authentication type, any one of `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_EAP_AKA:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_EAP_SIM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_GBA_BOOTSTRAP:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_GBA_NAF_KEY_EXTERNAL:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_EAP_SIM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_EAP_AKA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_GBA_BOOTSTRAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#AUTHTYPE_GBA_NAF_KEY_EXTERNAL:kotlin.Int` |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: authentication challenge data, base64 encoded. See 3GPP TS 31.102 7.1.2 for more details. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the response of authentication. This value will be null in the following cases: Authentication error, incorrect MAC Authentication error, security context not supported Key freshness failure Authentication error, no memory space available Authentication error, no memory space available in EFMUK |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` or doesn't support given authType. |

### getImei

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getImei(): String!
```

Returns the IMEI (International Mobile Equipment Identity). Return null if IMEI is not available. See getImei for details on the required permissions and behavior when the caller does not hold sufficient permissions. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

### getImei

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getImei(slotIndex: Int): String!
```

Returns the IMEI (International Mobile Equipment Identity). Return null if IMEI is not available.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges) on any active subscription.
- If the calling app is the default SMS role holder (see isRoleHeld).
- If the calling app has been granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_ICC_AUTH_WITH_DEVICE_IDENTIFIER:kotlin.String` permission.

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of which IMEI is returned |

### getLine1Number

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLine1Number(): String!
```

**Deprecated:** *use getPhoneNumber instead.*

Returns the phone number string for line 1, for example, the MSISDN for a GSM phone for a particular subscription. Return null if it is unavailable.

The default SMS app can also use this.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SMS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_NUMBERS:kotlin.String`, that the caller is the default SMS app, or that the caller has carrier privileges (see hasCarrierPrivileges) for any API level. `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` for apps targeting SDK API level 29 and below. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SMS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_NUMBERS:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getManualNetworkSelectionPlmn

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getManualNetworkSelectionPlmn(): String
```

Get the PLMN chosen for Manual Network Selection if active. Return empty string if in automatic selection.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | manually selected network info on success or empty string on failure. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getManufacturerCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getManufacturerCode(): String?
```

**Deprecated:** *Legacy CDMA is unsupported.*

Returns the Manufacturer Code from the MEID. Return null if Manufacturer Code is not available. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String`. |

### getManufacturerCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getManufacturerCode(slotIndex: Int): String?
```

**Deprecated:** *Legacy CDMA is unsupported.*

Returns the Manufacturer Code from the MEID. Return null if Manufacturer Code is not available. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of which Type Allocation Code is returned |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String`. |

### getMaximumCallComposerPictureSize

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMaximumCallComposerPictureSize(): Long
```

Indicates the maximum size of the call composure picture. Pictures sent via uploadCallComposerPicture or uploadCallComposerPicture must not exceed this size, or an error will be returned via the callback in those methods. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Maximum file size in bytes. Value is a non-negative number of bytes. |

### getMeid

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMeid(): String!
```

**Deprecated:** *Legacy CDMA is unsupported.*

Returns the MEID (Mobile Equipment Identifier). Return null if MEID is not available.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges) on any active subscription.
- If the calling app is the default SMS role holder (see isRoleHeld).

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the device is running Android 25Q2 or later, then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device is running Android 25Q1 or earlier and does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String`. |

### getMeid

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMeid(slotIndex: Int): String!
```

**Deprecated:** *Legacy CDMA is unsupported.*

Returns the MEID (Mobile Equipment Identifier). Return null if MEID is not available.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges) on any active subscription.
- If the calling app is the default SMS role holder (see isRoleHeld).

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of which MEID is returned |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String`. |

### getMmsUAProfUrl

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMmsUAProfUrl(): String!
```

Returns the MMS user agent profile URL. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getMmsUserAgent

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMmsUserAgent(): String!
```

Returns the MMS user agent. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### getNai

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNai(): String!
```

Returns the Network Access Identifier (NAI). Return null if NAI is not available.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges).
- If the calling app is the default SMS role holder (see isRoleHeld).

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getNetworkCountryIso

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkCountryIso(): String!
```

Returns the ISO-3166-1 alpha-2 country code equivalent of the MCC (Mobile Country Code) of the current registered operator or the cell nearby, if available.

. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the lowercase 2 character ISO-3166-1 alpha-2 country code, or empty string if not available. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getNetworkCountryIso

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkCountryIso(slotIndex: Int): String
```

Returns the ISO-3166-1 alpha-2 country code equivalent of the MCC (Mobile Country Code) of the current registered operator or the cell nearby, if available. This is same as getNetworkCountryIso but allowing specifying the SIM slot index. This is used for accessing network country info from the SIM slot that does not have SIM inserted. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the SIM slot index to get network country ISO. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the lowercase 2 character ISO-3166-1 alpha-2 country code, or empty string if not available. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when the slotIndex is invalid. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getNetworkOperator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkOperator(): String!
```

Returns the numeric name (MCC+MNC) of current registered operator. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

### getNetworkOperatorName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkOperatorName(): String!
```

Returns the alphabetic name of current registered operator. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

### getNetworkSelectionMode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkSelectionMode(): Int
```

Get the network selection mode.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the network selection mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_SELECTION_MODE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_SELECTION_MODE_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_SELECTION_MODE_MANUAL:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getNetworkSlicingConfiguration

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkSlicingConfiguration(
    executor: Executor, 
    callback: OutcomeReceiver<NetworkSlicingConfig!, TelephonyManager.NetworkSlicingException!>
): Unit
```

Request to get the current slicing configuration including URSP rules and NSSAIs (configured, allowed and rejected). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app has carrier privileges (see hasCarrierPrivileges).

This will be invalid if the device does not support android.telephony.TelephonyManager#CAPABILITY_SLICING_CONFIG_SUPPORTED. 
Requires the `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CAPABILITY_SLICING_CONFIG_SUPPORTED:kotlin.String` feature which can be detected using isRadioInterfaceCapabilitySupported. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

<br />

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [NetworkSlicingConfig](../android.telephony.data/NetworkSlicingConfig.md)!, [TelephonyManager.NetworkSlicingException](../android/telephony/TelephonyManager.NetworkSlicingException.md)!\>: a callback to receive the current slicing configuration. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getNetworkSpecifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkSpecifier(): String!
```

Returns the network specifier of the subscription ID pinned to the TelephonyManager. The network specifier is used by setNetworkSpecifier to create a `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.html#` that connects through the subscription. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.
**See Also**

- setNetworkSpecifier
- createForSubscriptionId
- createForPhoneAccountHandle

### getNetworkType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkType(): Int
```

**Deprecated:** *use getDataNetworkType*

Return the current data network type. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the NETWORK_TYPE_xxxx for current data connection. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getPhoneAccountHandle

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPhoneAccountHandle(): PhoneAccountHandle?
```

Determines the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` associated with this TelephonyManager.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId

Requires Permission android.Manifest.permission#READ_PRIVILEGED_PHONE_STATE or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#?` | The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` associated with the TelphonyManager, or `null` if there is no associated `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#`; this can happen if the subscription is data-only or an opportunistic subscription. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### getPhoneCount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPhoneCount(): Int
```

**Deprecated:** *Use getActiveModemCount instead.*

Returns the number of phones available.

- Returns 0 if none of voice, sms, data is supported.
- Returns 1 for Single standby mode (Single SIM functionality).
- Returns 2 for Dual standby mode (Dual SIM functionality).
- Returns 3 for Tri standby mode (Tri SIM functionality).

<br />

### getPhoneType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPhoneType(): Int
```

Returns a constant indicating the device phone type. This indicates the type of radio used to transmit voice/data calls. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PHONE_TYPE_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PHONE_TYPE_GSM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PHONE_TYPE_CDMA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PHONE_TYPE_SIP:kotlin.Int`

### getPreferredOpportunisticDataSubscription

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreferredOpportunisticDataSubscription(): Int
```

Get preferred opportunistic data subscription Id

Requires that the calling app has carrier privileges (see hasCarrierPrivileges), or has either READ_PRIVILEGED_PHONE_STATE or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` permission. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | subId preferred opportunistic subscription id or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DEFAULT_SUBSCRIPTION_ID:kotlin.Int` if there are no preferred subscription id |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### getPrimaryImei

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPrimaryImei(): String
```

Returns the primary IMEI (International Mobile Equipment Identity) of the device as mentioned in GSMA TS.37. getImei returns the IMEI that belongs to the selected slotID whereas this API getPrimaryImei returns primary IMEI of the device. A single SIM device with only one IMEI will be set by default as primary IMEI. A multi-SIM device with multiple IMEIs will have one of the IMEIs set as primary as mentioned in GSMA TS37_2.2_REQ_8.

Requires one of the following permissions

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges) on any active subscription.
- If the calling app is the default SMS role holder (see isRoleHeld).
- If the calling app has been granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_ICC_AUTH_WITH_DEVICE_IDENTIFIER:kotlin.String` permission.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | Primary IMEI of type string. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have the required permission/privileges |

### getServiceState

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getServiceState(): ServiceState?
```

Returns the current ServiceState information.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId If you want continuous updates of service state info, register a TelephonyCallback that implements `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener` through #registerTelephonyCallback.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges) and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. May return `null` when the subscription is inactive or when there was an error communicating with the phone process. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getServiceState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getServiceState(includeLocationData: Int): ServiceState?
```

Returns the current ServiceState information.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId If you want continuous updates of service state info, register a TelephonyCallback that implements `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener` through #registerTelephonyCallback. There's another way to renounce permissions with a custom context `AttributionSource.Builder#setRenouncedPermissions(Set<String>)` but only for system apps. To avoid confusion, calling this method supersede renouncing permissions with a custom context.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges) and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `includeLocationData` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies if the caller would like to receive location related information. May return `null` when the subscription is inactive or when there was an error communicating with the phone process. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_COARSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_FINE:kotlin.Int` |

| Return ||
|---|---|
| ServiceState | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getServiceStateForSlot

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getServiceStateForSlot(slotIndex: Int): ServiceState?
```

Returns the service state information on specified SIM slot. If you want continuous updates of service state info, register a TelephonyCallback that implements `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener` through #registerTelephonyCallback. May return `null` when the `slotIndex` is invalid or when there was an error communicating with the phone process See getActiveModemCount to get the total number of slots that are active on the device. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of phone whose service state is returned |

| Return ||
|---|---|
| ServiceState | ServiceState on specified SIM slot. |

### getSignalStrength

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSignalStrength(): SignalStrength?
```

Get the most recently available signal strength information. Get the most recent SignalStrength information reported by the modem. Due to power saving this information may not always be current. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| SignalStrength | the most recent cached signal strength info from the modem. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getSimCarrierId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimCarrierId(): Int
```

Returns carrier id of the current subscription.

To recognize a carrier (including MVNO) as a first-class identity, Android assigns each carrier with a canonical integer a.k.a. carrier id. The carrier ID is an Android platform-wide identifier for a carrier. AOSP maintains carrier ID assignments in [here](https://android.googlesource.com/platform/packages/providers/TelephonyProvider/+/master/assets/latest_carrier_id/carrier_list.textpb)

Apps which have carrier-specific configurations or business logic can use the carrier id as an Android platform-wide identifier for carriers. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Carrier id of the current subscription. Return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int` if the subscription is unavailable or the carrier cannot be identified. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getSimCarrierIdName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimCarrierIdName(): CharSequence?
```

Returns carrier id name of the current subscription.

Carrier id name is a user-facing name of carrier id returned by getSimCarrierId, usually the brand name of the subsidiary (e.g. T-Mobile). Each carrier could configure multiple getSimOperatorName but should have a single carrier name. Carrier name is not a canonical identity, use getSimCarrierId instead.

The returned carrier name is unlocalized. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | Carrier name of the current subscription. Return `null` if the subscription is unavailable or the carrier cannot be identified. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getSimCountryIso

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimCountryIso(): String!
```

Returns the ISO-3166-1 alpha-2 country code equivalent for the SIM provider's country code.

The ISO-3166-1 alpha-2 country code is provided in lowercase 2 character format. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the lowercase 2 character ISO-3166-1 alpha-2 country code, or empty string is not available. |

### getSimOperator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimOperator(): String!
```

Returns the MCC+MNC (mobile country code + mobile network code) of the provider of the SIM. 5 or 6 decimal digits.

Availability: SIM state must be `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_READY:kotlin.Int` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.
**See Also**

### getSimOperatorName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimOperatorName(): String!
```

Returns the Service Provider Name (SPN).

Availability: SIM state must be `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_READY:kotlin.Int` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.
**See Also**

### getSimSerialNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimSerialNumber(): String!
```

Returns the serial number of the SIM, if applicable. Return null if it is unavailable.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges).
- If the calling app is the default SMS role holder (see isRoleHeld).

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getSimSpecificCarrierId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimSpecificCarrierId(): Int
```

Returns fine-grained carrier ID of the current subscription. A specific carrier ID can represent the fact that a carrier may be in effect an aggregation of other carriers (ie in an MVNO type scenario) where each of these specific carriers which are used to make up the actual carrier service may have different carrier configurations. A specific carrier ID could also be used, for example, in a scenario where a carrier requires different carrier configuration for different service offering such as a prepaid plan. the specific carrier ID would be used for configuration purposes, but apps wishing to know about the carrier itself should use the regular carrier ID returned by getSimCarrierId. e.g, Tracfone SIMs could return different specific carrier ID based on IMSI from current subscription while carrier ID remains the same.

For carriers without fine-grained specific carrier ids, return getSimCarrierId

Specific carrier ids are defined in the same way as carrier id [here](https://android.googlesource.com/platform/packages/providers/TelephonyProvider/+/master/assets/latest_carrier_id/carrier_list.textpb) except each with a "parent" id linking to its top-level carrier id. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns fine-grained carrier id of the current subscription. Return `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UNKNOWN_CARRIER_ID:kotlin.Int` if the subscription is unavailable or the carrier cannot be identified. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getSimSpecificCarrierIdName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimSpecificCarrierIdName(): CharSequence?
```

Similar like getSimCarrierIdName, returns user-facing name of the specific carrier id returned by getSimSpecificCarrierId. The specific carrier ID would be used for configuration purposes, but apps wishing to know about the carrier itself should use the regular carrier ID returned by getSimCarrierIdName.

The returned name is unlocalized. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | user-facing name of the subscription specific carrier id. Return `null` if the subscription is unavailable or the carrier cannot be identified. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getSimState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimState(): Int
```

Returns a constant indicating the state of the default SIM card. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_ABSENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PIN_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PUK_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NETWORK_LOCKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_READY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NOT_READY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PERM_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_IO_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_RESTRICTED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_ABSENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PIN_REQUIRED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PUK_REQUIRED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NETWORK_LOCKED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_READY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NOT_READY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PERM_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_IO_ERROR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_RESTRICTED:kotlin.Int`

### getSimState

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSimState(slotIndex: Int): Int
```

Returns a constant indicating the state of the device SIM card in a logical slot. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): logical slot index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_ABSENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PIN_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PUK_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NETWORK_LOCKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_READY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NOT_READY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PERM_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_IO_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_RESTRICTED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_ABSENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PIN_REQUIRED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PUK_REQUIRED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NETWORK_LOCKED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_READY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_NOT_READY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_PERM_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_IO_ERROR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#SIM_STATE_CARD_RESTRICTED:kotlin.Int`

### getSubscriberId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubscriberId(): String!
```

Returns the unique subscriber ID, for example, the IMSI for a GSM phone. Return null if it is unavailable.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see getEnrollmentSpecificId).
- If the calling app has carrier privileges (see hasCarrierPrivileges).
- If the calling app is the default SMS role holder (see isRoleHeld).
- If the calling app has been granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_ICC_AUTH_WITH_DEVICE_IDENTIFIER:kotlin.String` permission.

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then null is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### getSubscriptionId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubscriptionId(): Int
```

Return an appropriate subscription ID for any situation. If this object has been created with createForSubscriptionId, then the provided subscription ID is returned. Otherwise, the default subscription ID will be returned. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

### getSubscriptionId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubscriptionId(phoneAccountHandle: PhoneAccountHandle): Int
```

Returns the subscription ID for the given phone account handle. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `phoneAccountHandle` | [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md): the phone account handle for outgoing calls. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | subscription ID for the given phone account handle; or `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#INVALID_SUBSCRIPTION_ID:kotlin.Int` if not available; or throw a SecurityException if the caller doesn't have the permission. |

### getSupportedModemCount

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupportedModemCount(): Int
```

Return how many logical modem can be potentially active simultaneously, in terms of hardware capability. It might return different value from getActiveModemCount. For example, for a dual-SIM capable device operating in single SIM mode (only one logical modem is turned on), getActiveModemCount returns 1 while this API returns 2.

### getSupportedRadioAccessFamily

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupportedRadioAccessFamily(): Long
```

Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Modem supported radio access family bitmask Requires permission: android.Manifest.READ_PRIVILEGED_PHONE_STATE or that the calling app has carrier privileges (see hasCarrierPrivileges). Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_UNKNOWN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_GSM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_GPRS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EDGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_CDMA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_1xRTT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_0:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_A:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_B:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EHRPD:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSUPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSDPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSPAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_UMTS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_TD_SCDMA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE_CA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_NR:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_IWLAN:kotlin.Long` |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have the required permission |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### getTypeAllocationCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTypeAllocationCode(): String?
```

Returns the Type Allocation Code from the IMEI. Return null if Type Allocation Code is not available.

### getTypeAllocationCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTypeAllocationCode(slotIndex: Int): String?
```

Returns the Type Allocation Code from the IMEI. Return null if Type Allocation Code is not available.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of which Type Allocation Code is returned |

### getUiccCardsInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUiccCardsInfo(): MutableList<UiccCardInfo!>
```

Gets information about currently inserted UICCs (Universal Integrated Circuit Cards) and eUICCs (embedded UICCs).

The details returned for each UiccCardInfo object depend on the permissions held by the calling application. The specific fields populated within each `UiccCardInfo` are determined as follows:

- With `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String`: The `UiccCardInfo` will include whether the card is an eUICC (isEuicc) and its getPhysicalSlotIndex.
- With carrier privileges on any active subscription (see hasCarrierPrivileges): The `UiccCardInfo` will include the card ID (getCardId), whether it's an eUICC (isEuicc), and its getPhysicalSlotIndex.
- With carrier privileges on the specific UICC or eUICC card: Sensitive identifiers like the EID (getEid) and ICCID (getIccId) for that particular card can be accessed.

If an application lacks the necessary permissions for certain details of a card (e.g.,the EID due to missing specific carrier privileges for that card), those fields will not be populated in the `UiccCardInfo` object for that card.

See UiccCardInfo for a comprehensive description of all possible card attributes and their individual data protection considerations. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or hasCarrierPrivileges 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo!>` | A list of `UiccCardInfo` objects, representing the currently inserted UICCs and eUICCs. Each object contains information filtered according to the caller's permissions for that specific card. Returns an empty list if no cards are present or accessible. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not declare the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature. |

### getVisualVoicemailPackageName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVisualVoicemailPackageName(): String?
```

Returns the package responsible of processing visual voicemail for the subscription ID pinned to the TelephonyManager. Returns `null` when there is no package responsible for processing visual voicemail for the subscription.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

**See Also**

- createForSubscriptionId
- createForPhoneAccountHandle
- VisualVoicemailService

### getVoiceMailAlphaTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVoiceMailAlphaTag(): String!
```

Retrieves the alphabetic identifier associated with the voice mail number.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### getVoiceMailNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVoiceMailNumber(): String!
```

Returns the voice mail number. Return null if it is unavailable.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### getVoiceNetworkType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVoiceNetworkType(): Int
```

Returns the NETWORK_TYPE_xxxx for voice

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### getVoicemailRingtoneUri

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVoicemailRingtoneUri(accountHandle: PhoneAccountHandle!): Uri?
```

Returns the URI for the per-account voicemail ringtone set in Phone settings. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md)!: The handle for the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#` for which to retrieve the voicemail ringtone. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | The URI for the ringtone to play when receiving a voicemail from a specific PhoneAccount. May be `null` if no ringtone is set. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### hasCarrierPrivileges

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasCarrierPrivileges(): Boolean
```

Has the calling application been granted carrier privileges by the carrier. If any of the packages in the calling UID has carrier privileges, the call will return true. This access is granted by the owner of the UICC card and does not depend on the registered carrier. Note that this API applies to both physical and embedded subscriptions and is a superset of the checks done in SubscriptionManager#canManageSubscription. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the app has carrier privileges. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### hasIccCard

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasIccCard(): Boolean
```

This API is used to check if there is an ICC card present in the device. An ICC card is a smart card that contains a subscriber identity module (SIM) and is used to identify and authenticate users to a mobile network. Note: In case of embedded SIM there is an ICC card always present irrespective of whether an active SIM profile is present or not so this API would always return true. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a ICC card is present. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### iccCloseLogicalChannel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iccCloseLogicalChannel(channel: Int): Boolean
```

Closes a previously opened logical channel to the ICC card. Input parameters equivalent to TS 27.007 AT+CCHC command. It is strongly recommended that callers of this API should firstly create new TelephonyManager instance by calling createForSubscriptionId. Failure to do so can result in unpredictable and detrimental behavior like callers can end up talking to the wrong SIM card.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `channel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): is the channel id to be closed as returned by a successful iccOpenLogicalChannel. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the channel was closed successfully. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input parameters are wrong. e.g., invalid channel |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### iccExchangeSimIO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iccExchangeSimIO(
    fileID: Int, 
    command: Int, 
    p1: Int, 
    p2: Int, 
    p3: Int, 
    filePath: String!
): ByteArray!
```

Returns the response APDU for a command APDU sent through SIM_IO.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `fileID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `command` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `p1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P1 value of the APDU command. |
| --- | --- |
| `p2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P2 value of the APDU command. |
| `p3` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P3 value of the APDU command. |
| `filePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | The APDU response. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### iccOpenLogicalChannel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iccOpenLogicalChannel(AID: String!): IccOpenLogicalChannelResponse!
```

**Deprecated:** *Replaced by iccOpenLogicalChannel*

Opens a logical channel to the ICC card. Input parameters equivalent to TS 27.007 AT+CCHO command.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `AID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Application id. See ETSI 102.221 and 101.220. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/IccOpenLogicalChannelResponse!` | an IccOpenLogicalChannelResponse object. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### iccOpenLogicalChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iccOpenLogicalChannel(
    AID: String!, 
    p2: Int
): IccOpenLogicalChannelResponse!
```

Opens a logical channel to the ICC card. This operation wraps two APDU instructions:

- MANAGE CHANNEL to open a logical channel
- SELECT the given `AID` using the given `p2`

Per Open Mobile API Specification v3.2 section 6.2.7.h, only p2 values of 0x00, 0x04, 0x08, and 0x0C are guaranteed to be supported. If the SELECT command's status word is not '9000', '62xx', or '63xx', the status word will be considered an error and the channel shall not be opened. Input parameters equivalent to TS 27.007 AT+CCHO command. It is strongly recommended that callers of this should firstly create a new TelephonyManager instance by calling createForSubscriptionId. Failure to do so can result in unpredictable and detrimental behavior like callers can end up talking to the wrong SIM card.

<br />

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `AID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Application id. See ETSI 102.221 and 101.220. |
| `p2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P2 parameter (described in ISO 7816-4). |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/IccOpenLogicalChannelResponse!` | an IccOpenLogicalChannelResponse object. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### iccTransmitApduBasicChannel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iccTransmitApduBasicChannel(
    cla: Int, 
    instruction: Int, 
    p1: Int, 
    p2: Int, 
    p3: Int, 
    data: String!
): String!
```

Transmit an APDU to the ICC card over the basic channel. Input parameters equivalent to TS 27.007 AT+CSIM command.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `cla` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Class of the APDU command. |
| `instruction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Instruction of the APDU command. |
| `p1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P1 value of the APDU command. |
| --- | --- |
| `p2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P2 value of the APDU command. |
| `p3` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P3 value of the APDU command. If p3 is negative a 4 byte APDU is sent to the SIM. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Data to be sent with the APDU. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The APDU response from the ICC card with the status appended at the end. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### iccTransmitApduLogicalChannel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iccTransmitApduLogicalChannel(
    channel: Int, 
    cla: Int, 
    instruction: Int, 
    p1: Int, 
    p2: Int, 
    p3: Int, 
    data: String!
): String!
```

Transmit an APDU to the ICC card over a logical channel. Input parameters equivalent to TS 27.007 AT+CGLA command. It is strongly recommended that callers of this API should firstly create a new TelephonyManager instance by calling createForSubscriptionId. Failure to do so can result in unpredictable and detrimental behavior like callers can end up talking to the wrong SIM card.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `channel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): is the channel id to be closed as returned by a successful iccOpenLogicalChannel. |
| `cla` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Class of the APDU command. |
| `instruction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Instruction of the APDU command. |
| --- | --- |
| `p1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P1 value of the APDU command. |
| `p2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P2 value of the APDU command. |
| `p3` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): P3 value of the APDU command. If p3 is negative a 4 byte APDU is sent to the SIM. |
| --- | --- |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Data to be sent with the APDU. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The APDU response from the ICC card with the status appended at the end. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### isConcurrentVoiceAndDataSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isConcurrentVoiceAndDataSupported(): Boolean
```

Whether the device is currently on a technology (e.g. UMTS or LTE) which can support voice and data simultaneously. This can change based on location or network condition. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if simultaneous voice and data supported, and `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### isDataCapable

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDataCapable(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current device is "data capable" over a radio on the device. "Data capable" means that this device supports packet-switched data connections over the telephony network. <br /> |

### isDataConnectionAllowed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDataConnectionAllowed(): Boolean
```

Checks whether cellular data connection is allowed in the device.

Whether cellular data connection is allowed considers all factors below:

- User turned on data setting isDataEnabled.
- Carrier allows data to be on.
- Network policy.
- And possibly others.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the overall data connection is allowed; `false` if not. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### isDataEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDataEnabled(): Boolean
```

Returns whether mobile data is enabled or not per user setting. There are other factors that could disable mobile data, but they are not considered here. If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultDataSubscriptionId

Requires one of the following permissions: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges).

Note that this does not take into account any data restrictions that may be present on the calling app. Such restrictions may be inspected with getRestrictBackgroundStatus. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if mobile data is enabled. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### isDataEnabledForReason

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDataEnabledForReason(reason: Int): Boolean
```

Return whether data is enabled for certain reason . If isDataEnabledForReason returns false, it means in data enablement for a specific reason is turned off. If any of the reason is off, then it will result in bypassing user preference and result in data to be turned off. Call isDataConnectionAllowed in order to know whether data connection is allowed on the device.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultDataSubscriptionId 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the reason the data enable change is taking place. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_POLICY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_CARRIER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_THERMAL:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether data is enabled for a reason. Requires Permission: The calling app has carrier privileges (see hasCarrierPrivileges) or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the Telephony process is not currently available. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### isDataRoamingEnabled

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDataRoamingEnabled(): Boolean
```

Returns whether mobile data roaming is enabled on the subscription.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultDataSubscriptionId

Requires one of the following permissions: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_NETWORK_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the data roaming is enabled on the subscription, otherwise return |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. `false`. |

### isDeviceSmsCapable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDeviceSmsCapable(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current device supports SMS service. If true, this means that the device supports both sending and receiving SMS via the telephony network. Note: Voicemail waiting SMS, cell broadcasting SMS, and MMS are disabled when device doesn't support SMS. Starting from Android 15, SMS capability may also be overridden by carriers for a given subscription on an SMS capable device. To check if a subscription is "SMS capable", call method getServiceCapabilities and check if `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#SERVICE_CAPABILITY_SMS:kotlin.Int` is included. |

**See Also**

- getServiceCapabilities

### isDeviceVoiceCapable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDeviceVoiceCapable(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current device is "voice capable". "Voice capable" means that this device supports circuit-switched or IMS packet switched (i.e. voice) phone calls over the telephony network, and is allowed to display the in-call UI while a cellular voice call is active. This will be false on "data only" devices which can't make voice calls and don't support any in-call UI. Note: the meaning of this flag is subtly different from the PackageManager .FEATURE_TELEPHONY system feature, which is available on any device with a telephony radio, even if the device is data-only. Starting from Android 15, voice capability may also be overridden by carrier for a given subscription on a voice capable device. To check if a subscription is "voice capable", call method getServiceCapabilities and check if `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#SERVICE_CAPABILITY_VOICE:kotlin.Int` is included. |

**See Also**

- getServiceCapabilities

### isEmergencyNumber

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmergencyNumber(number: String): Boolean
```

Identifies if the supplied phone number is an emergency number that matches a known emergency number based on current locale, SIM card(s), Android database, modem, network, or defaults.

This method assumes that only dialable phone numbers are passed in; non-dialable numbers are not considered emergency numbers. A dialable phone number consists only of characters/digits identified by isDialable.

The subscriptions which the identification would be based on, are all the active subscriptions, no matter which subscription could be used to create TelephonyManager.

| Parameters ||
|---|---|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): - the number to look up. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given number is an emergency number based on current locale, SIM card(s), Android database, modem, network or defaults; `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the Telephony process is not currently available. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`. |

### isHearingAidCompatibilitySupported

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHearingAidCompatibilitySupported(): Boolean
```

Whether the phone supports hearing aid compatibility. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the device supports hearing aid compatibility, and `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### isManualNetworkSelectionAllowed

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isManualNetworkSelectionAllowed(): Boolean
```

Checks if manual network selection is allowed.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges)

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PRECISE_PHONE_STATE:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if manual network selection is allowed, otherwise return `false`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### isModemEnabledForSlot

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isModemEnabledForSlot(slotIndex: Int): Boolean
```

Indicates whether or not there is a modem stack enabled for the given SIM slot.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`, READ_PRIVILEGED_PHONE_STATE or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` or android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `slotIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): which slot it's checking. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`. |

### isMultiSimSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isMultiSimSupported(): Int
```

Returns if the usage of multiple SIM cards at the same time to register on the network (e.g. Dual Standby or Dual Active) is supported by the device and by the carrier.

Requires Permission:`https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_PHONE_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_ALLOWED:kotlin.Int` if the device supports multiple SIMs. `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_NOT_SUPPORTED_BY_HARDWARE:kotlin.Int` if the device does not support multiple SIMs. `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_NOT_SUPPORTED_BY_CARRIER:kotlin.Int` in the device supports multiple SIMs, but the functionality is restricted by the carrier. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_NOT_SUPPORTED_BY_HARDWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#MULTISIM_NOT_SUPPORTED_BY_CARRIER:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### isNetworkRoaming

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNetworkRoaming(): Boolean
```

Returns true if the device is considered roaming on the current network, for GSM purposes.

Availability: Only when user registered to a network. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

### isPremiumCapabilityAvailableForPurchase

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPremiumCapabilityAvailableForPurchase(capability: Int): Boolean
```

Check whether the given premium capability is available for purchase from the carrier. If this is `true`, the capability can be purchased from the carrier using purchasePremiumCapability. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The premium capability to check. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PREMIUM_CAPABILITY_PRIORITIZE_LATENCY:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the given premium capability is available to purchase. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not hold permission READ_BASIC_PHONE_STATE. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### isRadioInterfaceCapabilitySupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRadioInterfaceCapabilitySupported(capability: String): Boolean
```

Whether the device supports a given capability on the radio interface. If the capability is not in the set of radio interface capabilities, false is returned. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `capability` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the capability to check for. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CAPABILITY_SLICING_CONFIG_SUPPORTED:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the availability of the capability |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### isRttSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRttSupported(): Boolean
```

Determines whether the device currently supports RTT (Real-time text). Based both on carrier support for the feature and device firmware support. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the device and carrier both support RTT, `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String`. |

### isSmsCapable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSmsCapable(): Boolean
```

**Deprecated:** *Replaced by isDeviceSmsCapable. Starting from Android 15, SMS capability may also be overridden by carriers for a given subscription. For SMS capable device (when isDeviceSmsCapable return `true`), caller should check for subscription-level SMS capability as well. See isDeviceSmsCapable for details.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current device supports sms service. If true, this means that the device supports both sending and receiving sms via the telephony network. Note: Voicemail waiting sms, cell broadcasting sms, and MMS are disabled when device doesn't support sms. |

### isTtyModeSupported

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTtyModeSupported(): Boolean
```

**Deprecated:** *Use isTtySupported instead Whether the phone supports TTY mode.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the device supports TTY mode, and `false` otherwise. |

### isVoiceCapable

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVoiceCapable(): Boolean
```

**Deprecated:** *Replaced by isDeviceVoiceCapable. Starting from Android 15, voice capability may also be overridden by carriers for a given subscription. For voice capable device (when isDeviceVoiceCapable return `true`), caller should check for subscription-level voice capability as well. See isDeviceVoiceCapable for details.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current device is "voice capable". "Voice capable" means that this device supports circuit-switched (i.e. voice) phone calls over the telephony network, and is allowed to display the in-call UI while a cellular voice call is active. This will be false on "data only" devices which can't make voice calls and don't support any in-call UI. Note: the meaning of this flag is subtly different from the PackageManager.FEATURE_TELEPHONY system feature, which is available on any device with a telephony radio, even if the device is data-only. |

### isVoicemailVibrationEnabled

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVoicemailVibrationEnabled(accountHandle: PhoneAccountHandle!): Boolean
```

Returns whether vibration is set for voicemail notification in Phone settings. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md)!: The handle for the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#` for which to retrieve the voicemail vibration setting. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the vibration is set for this PhoneAccount, `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### isWorldPhone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWorldPhone(): Boolean
```

Whether the device is a world phone. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the device is a world phone, and `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`. |

### listen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun listen(
    listener: PhoneStateListener!, 
    events: Int
): Unit
```

**Deprecated:** *Use registerTelephonyCallback.*

Registers a listener object to receive notification of changes in specified telephony states.

To register a listener, pass a PhoneStateListener and specify at least one telephony state of interest in the events argument. At registration, and when a specified telephony state changes, the telephony manager invokes the appropriate callback method on the listener object and passes the current (updated) values.

To un-register a listener, pass the listener object and set the events argument to `https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_NONE:kotlin.Int` (0). If this TelephonyManager object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId. To listen events for multiple subIds, pass a separate listener object to each TelephonyManager object created with createForSubscriptionId. Note: if you call this method while in the middle of a binder transaction, you **must** call clearCallingIdentity before calling this method. A `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown otherwise. This API should be used sparingly -- large numbers of listeners will cause system instability. If a process has registered too many listeners without unregistering them, it may encounter an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` when trying to register more listeners.

| Parameters ||
|---|---|
| `listener` | [PhoneStateListener](PhoneStateListener.md)!: The PhoneStateListener object to register (or unregister) |
| `events` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The telephony state(s) of interest to the listener, as a bitwise-OR combination of PhoneStateListener LISTEN_ flags. |

### purchasePremiumCapability

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun purchasePremiumCapability(
    capability: Int, 
    executor: Executor, 
    callback: Consumer<Int!>
): Unit
```

Purchase the given premium capability from the carrier. This requires user action to purchase the boost from the carrier. If this returns `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_SUCCESS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_PURCHASED:kotlin.Int`, applications can request the premium capability via android.net.ConnectivityManager#requestNetwork. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_BASIC_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The premium capability to purchase. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PREMIUM_CAPABILITY_PRIORITIZE_LATENCY:kotlin.Int` |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The callback executor for the response. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: The result of the purchase request. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_THROTTLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_PURCHASED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ALREADY_IN_PROGRESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_NOT_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_CANCELED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_CARRIER_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_FEATURE_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_NETWORK_NOT_AVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_ENTITLEMENT_CHECK_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_NOT_DEFAULT_DATA_SUBSCRIPTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_PENDING_NETWORK_SETUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#PURCHASE_PREMIUM_CAPABILITY_RESULT_USER_DISABLED:kotlin.Int` |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not hold permissions READ_BASIC_PHONE_STATE or INTERNET. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

**See Also**

- isPremiumCapabilityAvailableForPurchase

### rebootModem

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rebootModem(): Unit
```

Reboot and re-initialize the cellular modem and related subsystems below the OS. Used for device provisioning and reconfiguration by some carriers.

Device-specific and App-specific support information:

- This method is required to be supported on devices that launch with hardware support for `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` and which declare `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`.
- On other devices which either do not include hardware support for `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` or do not declare `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`, support is likely but not guaranteed.
- For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` or lower, if this method is not supported, it may fail silently.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the Telephony process is not currently available. |
| `java.lang.RuntimeException` | |
| `java.lang.UnsupportedOperationException` | If the method is unsupported. |
| --- | --- |

### registerTelephonyCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerTelephonyCallback(
    includeLocationData: Int, 
    executor: Executor, 
    callback: TelephonyCallback
): Unit
```

Registers a callback object to receive notification of changes in specified telephony states.

To register a callback, pass a TelephonyCallback which implements interfaces of events. For example, FakeServiceStateCallback extends TelephonyCallback implements `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener`. At registration, and when a specified telephony state changes, the telephony manager invokes the appropriate callback method on the callback object and passes the current (updated) values.

If this TelephonyManager object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId. To register events for multiple subIds, pass a separate callback object to each TelephonyManager object created with createForSubscriptionId. Note: if you call this method while in the middle of a binder transaction, you **must** call clearCallingIdentity before calling this method. A `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown otherwise. This API should be used sparingly -- large numbers of callbacks will cause system instability. If a process has registered too many callbacks without unregistering them, it may encounter an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` when trying to register more callbacks.

There's another way to renounce permissions with a custom context `AttributionSource.Builder#setRenouncedPermissions(Set<String>)` but only for system apps. To avoid confusion, calling this method supersede renouncing permissions with a custom context.

| Parameters ||
|---|---|
| `includeLocationData` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies if the caller would like to receive location related information. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_COARSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_FINE:kotlin.Int` |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor of where the callback will execute. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [TelephonyCallback](TelephonyCallback.md): The TelephonyCallback object to register. The caller should hold a reference to the callback. The framework only holds a weak reference. This value cannot be `null`. |
| --- | --- |

### registerTelephonyCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerTelephonyCallback(
    executor: Executor, 
    callback: TelephonyCallback
): Unit
```

Registers a callback object to receive notification of changes in specified telephony states.

To register a callback, pass a TelephonyCallback which implements interfaces of events. For example, FakeServiceStateCallback extends TelephonyCallback implements `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.ServiceStateListener`. At registration, and when a specified telephony state changes, the telephony manager invokes the appropriate callback method on the callback object and passes the current (updated) values.

Note: Be aware of the permission requirements stated on the TelephonyCallback listeners you implement. Your application must be granted these permissions in order to register a TelephonyCallback which requires them; a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown if you do not hold the required permissions for all TelephonyCallback listeners you implement.

If this TelephonyManager object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId. To register events for multiple subIds, pass a separate callback object to each TelephonyManager object created with createForSubscriptionId. Note: if you call this method while in the middle of a binder transaction, you **must** call clearCallingIdentity before calling this method. A `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown otherwise. This API should be used sparingly -- large numbers of callbacks will cause system instability. If a process has registered too many callbacks without unregistering them, it may encounter an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` when trying to register more callbacks.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor of where the callback will execute. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [TelephonyCallback](TelephonyCallback.md): The TelephonyCallback object to register. The caller should hold a reference to the callback. The framework only holds a weak reference. This value cannot be `null`. |

### requestCellInfoUpdate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestCellInfoUpdate(
    executor: Executor, 
    callback: TelephonyManager.CellInfoCallback
): Unit
```

Requests all available cell information from the current subscription for observed camped/registered, serving, and neighboring cells.

Any available results from this request will be provided by calls to onCellInfoChanged for each active subscription.

This method returns valid data for devices with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`. On devices that do not implement this feature, the behavior is not reliable. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor on which callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [TelephonyManager.CellInfoCallback](../android/telephony/TelephonyManager.CellInfoCallback.md): a callback to receive CellInfo. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### requestNetworkScan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestNetworkScan(
    request: NetworkScanRequest!, 
    executor: Executor!, 
    callback: TelephonyScanManager.NetworkScanCallback!
): NetworkScan!
```

Request a network scan. This method is asynchronous, so the network scan results will be returned by callback. The returned NetworkScan will contain a callback method which can be used to stop the scan.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges) and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`. If the system-wide location switch is off, apps may still call this API, with the following constraints:

1. The app must hold the `android.permission.NETWORK_SCAN` permission.
2. The app must not supply any specific bands or channels to scan.
3. The app must only specify MCC/MNC pairs that are associated to a SIM in the device.
4. Returned results will have no meaningful info other than signal strength and MCC/MNC info.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `request` | [NetworkScanRequest](NetworkScanRequest.md)!: Contains all the RAT with bands/channels that need to be scanned. |
| `executor` | [Executor](../java.util.concurrent/Executor.md)!: The executor through which the callback should be invoked. Since the scan request may trigger multiple callbacks and they must be invoked in the same order as they are received by the platform, the user should provide an executor which executes tasks one at a time in serial order. |
| `callback` | [TelephonyScanManager.NetworkScanCallback](../android/telephony/TelephonyScanManager.NetworkScanCallback.md)!: Returns network scan results or errors. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/NetworkScan!` | A NetworkScan obj which contains a callback which can be used to stop the scan. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### requestNetworkScan

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestNetworkScan(
    includeLocationData: Int, 
    request: NetworkScanRequest, 
    executor: Executor, 
    callback: TelephonyScanManager.NetworkScanCallback
): NetworkScan?
```

Request a network scan. This method is asynchronous, so the network scan results will be returned by callback. The returned NetworkScan will contain a callback method which can be used to stop the scan.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges) and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` if includeLocationData is set to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_FINE:kotlin.Int`. If the system-wide location switch is off, apps may still call this API, with the following constraints:

1. The app must hold the `android.permission.NETWORK_SCAN` permission.
2. The app must not supply any specific bands or channels to scan.
3. The app must only specify MCC/MNC pairs that are associated to a SIM in the device.
4. Returned results will have no meaningful info other than signal strength and MCC/MNC info.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `includeLocationData` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies if the caller would like to receive location related information. If this parameter is set to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_FINE:kotlin.Int` then the application will be checked for `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission and available location related information received during network scan will be sent to the caller. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_COARSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#INCLUDE_LOCATION_DATA_FINE:kotlin.Int` |
| `request` | [NetworkScanRequest](NetworkScanRequest.md): Contains all the RAT with bands/channels that need to be scanned. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor through which the callback should be invoked. Since the scan request may trigger multiple callbacks and they must be invoked in the same order as they are received by the platform, the user should provide an executor which executes tasks one at a time in serial order. This value cannot be `null`. |
| --- | --- |
| `callback` | [TelephonyScanManager.NetworkScanCallback](../android/telephony/TelephonyScanManager.NetworkScanCallback.md): Returns network scan results or errors. This value cannot be `null`. |

| Return ||
|---|---|
| NetworkScan | A NetworkScan obj which contains a callback which can be used to stop the scan. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### sendDialerSpecialCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendDialerSpecialCode(inputCode: String!): Unit
```

Send the special dialer code. The IPC caller must be the current default dialer or have carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `inputCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The special dialer code to send |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have carrier privileges or is not the current default dialer |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### sendEnvelopeWithStatus

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendEnvelopeWithStatus(content: String!): String!
```

Send ENVELOPE to the SIM and return the response.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `content` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: String containing SAT/USAT response in hexadecimal format starting with command tag. See TS 102 223 for details. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The APDU response from the ICC card in hexadecimal format with the last 4 bytes being the status word. If the command fails, returns an empty string. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### sendUssdRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendUssdRequest(
    ussdRequest: String!, 
    callback: TelephonyManager.UssdResponseCallback!, 
    handler: Handler!
): Unit
```

Sends an Unstructured Supplementary Service Data (USSD) request to the mobile network and informs the caller of the response via the supplied `callback`.

Carriers define USSD codes which can be sent by the user to request information such as the user's current data balance or minutes balance.

Note: Call forwarding USSD requests are restricted to protect user security. Callers must have carrier privileges, be a system app, hold the call screening role, hold the device policy management role, or be running on a fully managed device to perform these actions. Otherwise, the request will fail and the callback will be invoked with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#USSD_ERROR_NOT_ALLOWED:kotlin.Int`.

Requires permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CALL_PHONE:kotlin.String` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CALL_PHONE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `ussdRequest` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the USSD command to be executed. |
| `callback` | [TelephonyManager.UssdResponseCallback](../android/telephony/TelephonyManager.UssdResponseCallback.md)!: called by the framework to inform the caller of the result of executing the USSD request (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.UssdResponseCallback`). |
| `handler` | [Handler](../android.os/Handler.md)!: the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` to run the request on. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### sendVisualVoicemailSms

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendVisualVoicemailSms(
    number: String!, 
    port: Int, 
    text: String!, 
    sentIntent: PendingIntent!
): Unit
```

Send a visual voicemail SMS. The caller must be the current default dialer. A VisualVoicemailService uses this method to send a command via SMS to the carrier's visual voicemail server. Some examples for carriers using the OMTP standard include activating and deactivating visual voicemail, or requesting the current visual voicemail provisioning status. See the OMTP Visual Voicemail specification for more information on the format of these SMS messages.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SEND_SMS:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The destination number. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The destination port for data SMS, or 0 for text SMS. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The message content. For data sms, it will be encoded as a UTF-8 byte stream. |
| --- | --- |
| `sentIntent` | [PendingIntent](../android.app/PendingIntent.md)!: The sent intent passed to the SmsManager |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is not the current default dialer |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

**See Also**

- sendDataMessage
- sendTextMessage

### setAllowedNetworkTypesForReason

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowedNetworkTypesForReason(
    reason: Int, 
    allowedNetworkTypes: Long
): Unit
```

Set the allowed network types of the device and provide the reason triggering the allowed network change.

Requires permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). This can be called for following reasons:

1. Allowed network types control by USER `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ALLOWED_NETWORK_TYPES_REASON_USER:kotlin.Int`
2. Allowed network types control by carrier `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ALLOWED_NETWORK_TYPES_REASON_CARRIER:kotlin.Int`

This API will result in allowing an intersection of allowed network types for all reasons, including the configuration done through other reasons. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the TelephonyManager#CAPABILITY_USES_ALLOWED_NETWORK_TYPES_BITMASK feature which can be detected using isRadioInterfaceCapabilitySupported.

| Parameters ||
|---|---|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the reason the allowed network type change is taking place. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ALLOWED_NETWORK_TYPES_REASON_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#ALLOWED_NETWORK_TYPES_REASON_CARRIER:kotlin.Int` |
| `allowedNetworkTypes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The bitmask of allowed network type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_UNKNOWN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_GSM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_GPRS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EDGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_CDMA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_1xRTT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_0:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_A:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EVDO_B:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_EHRPD:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSUPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSDPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSPA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_HSPAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_UMTS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_TD_SCDMA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_LTE_CA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_NR:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_BITMASK_IWLAN:kotlin.Long` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if invalid AllowedNetworkTypesReason is passed. |
| `java.lang.IllegalStateException` | if the Telephony process is not currently available. |
| `java.lang.SecurityException` | if the caller does not have the required privileges or if the |
| --- | --- |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### setCallComposerStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCallComposerStatus(status: Int): Unit
```

Set the user-set status for enriched calling with call composer. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): user-set status for enriched calling with call composer. If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_ON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_COMPOSER_STATUS_BUSINESS_ONLY:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if requested state is invalid. |
| `java.lang.SecurityException` | if the caller does not have the permission. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |
| --- | --- |

### setDataEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDataEnabled(enable: Boolean): Unit
```

**Deprecated:** *use setDataEnabledForReason with reason DATA_ENABLED_REASON_USER instead.*

Turns mobile data on or off. If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultDataSubscriptionId

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to enable mobile data. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### setDataEnabledForReason

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDataEnabledForReason(
    reason: Int, 
    enabled: Boolean
): Unit
```

Control of data connection and provide the reason triggering the data connection control. This can be called for following reasons

1. data limit is passed `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_POLICY:kotlin.Int`
2. data disabled by carrier `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_CARRIER:kotlin.Int`
3. data disabled by user `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_USER:kotlin.Int`
4. data disabled due to thermal `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_THERMAL:kotlin.Int`

If any of the reason is off, then it will result in bypassing user preference and result in data to be turned off.

<br />

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultDataSubscriptionId 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the reason the data enable change is taking place. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_POLICY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_CARRIER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_THERMAL:kotlin.Int` |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if enabling the data, otherwise disabling. Requires Permission: The calling app has carrier privileges (see hasCarrierPrivileges) if the reason is `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_USER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#DATA_ENABLED_REASON_CARRIER:kotlin.Int`, or the calling app has `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` irrespective of the reason. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the Telephony process is not currently available. |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### setForbiddenPlmns

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setForbiddenPlmns(fplmns: MutableList<String!>): Int
```

Replace the contents of the forbidden PLMN SIM file with the provided values. Passing an empty list will clear the contents of the EFfplmn file. If the provided list is shorter than the size of EFfplmn, then the list will be padded up to the file size with 'FFFFFF'. (required by 3GPP TS 31.102 spec 4.2.16) If the list is longer than the size of EFfplmn, then the file will be written from the beginning of the list up to the file size.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `fplmns` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: a list of PLMNs to be forbidden. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of PLMNs that were successfully written to the SIM FPLMN list. This may be less than the number of PLMNs passed in where the SIM file does not have enough room for all of the values passed in. Return -1 in the event of an unexpected failure |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### setLine1NumberForDisplay

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLine1NumberForDisplay(
    alphaTag: String!, 
    number: String!
): Boolean
```

**Deprecated:** *use setCarrierPhoneNumber instead.*

Set the line 1 phone number string and its alphatag for the current ICCID for display purpose only, for example, displayed in Phone Status. It won't change the actual MSISDN/MDN. To unset alphatag or number, pass in a null value.

Requires that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `alphaTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: alpha-tagging of the dailing nubmer |
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The dialing number |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the operation was executed correctly. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### setNetworkSelectionModeAutomatic

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNetworkSelectionModeAutomatic(): Unit
```

Sets the network selection mode to automatic.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### setNetworkSelectionModeManual

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNetworkSelectionModeManual(
    operatorNumeric: String!, 
    persistSelection: Boolean
): Boolean
```

Ask the radio to connect to the input network and change selection mode to manual.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `operatorNumeric` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the PLMN ID of the network to select. |
| `persistSelection` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the selection will persist until reboot. If true, only allows attaching to the selected PLMN until reboot; otherwise, attach to the chosen PLMN and resume normal network selection next time. For devices launching with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this API will return `true` if the setting is applied successfully, regardless of whether attaching to the network is successful. Previously this behavior was ambiguous. For all hardware versions callers may always call getNetworkSelectionMode to unambiguously determine the state of the setting subsequent to calling #setNetworkSelectionModeManual. Regardless of the API level, rather than relying on the result of this method, callers should monitor ServiceState for the state of network registration; they may also monitor getIsManualSelection for state changes in real time. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the settings is successful; `false` if the setting fails. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### setNetworkSelectionModeManual

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNetworkSelectionModeManual(
    operatorNumeric: String, 
    persistSelection: Boolean, 
    ran: Int
): Boolean
```

Ask the radio to connect to the input network and change selection mode to manual.

If this object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `operatorNumeric` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the PLMN ID of the network to select. This value cannot be `null`. |
| `persistSelection` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the selection will persist until reboot. If true, only allows attaching to the selected PLMN until reboot; otherwise, attach to the chosen PLMN and resume normal network selection next time. |
| `ran` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial suggested radio access network type. If registration fails, the RAN is not available after, the RAN is not within the network types specified by the preferred network types, or the value is `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#UNKNOWN:kotlin.Int`, modem will select the next best RAN for network registration. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#GERAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#UTRAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#EUTRAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#CDMA2000:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#IWLAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#NGRAN:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` on success; `false` on any failure. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### setOperatorBrandOverride

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOperatorBrandOverride(brand: String!): Boolean
```

Override the branding for the current ICCID. Once set, whenever the SIM is present in the device, the service provider name (SPN) and the operator name will both be replaced by the brand value input. To unset the value, the same function should be called with a null brand value.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `brand` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The brand name to display/set. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the operation was executed correctly. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### setPreferredNetworkTypeToGlobal

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPreferredNetworkTypeToGlobal(): Boolean
```

Set the preferred network type to global mode which includes NR, LTE, CDMA, EvDo and GSM/WCDMA.

Requires that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success; false on any failure. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### setPreferredOpportunisticDataSubscription

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPreferredOpportunisticDataSubscription(
    subId: Int, 
    needValidation: Boolean, 
    executor: Executor?, 
    callback: Consumer<Int!>?
): Unit
```

Set preferred opportunistic data subscription id. Switch internet data to preferred opportunistic data subscription id. This api can result in lose of internet connectivity for short period of time while internet data is handed over.

Requires that the calling app has carrier privileges on both primary and secondary subscriptions (see hasCarrierPrivileges), or has permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `subId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): which opportunistic subscription getOpportunisticSubscriptions is preferred for cellular data. Pass `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager#DEFAULT_SUBSCRIPTION_ID:kotlin.Int` to unset the preference |
| `needValidation` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether validation is needed before switch happens. |
| `executor` | [Executor](../java.util.concurrent/Executor.md)?: The executor of where the callback will execute. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>?: Callback will be triggered once it succeeds or failed. See the `SET_OPPORTUNISTIC_SUB_*` constants for more details. Pass null if don't care about the result. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`. |

### setSignalStrengthUpdateRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSignalStrengthUpdateRequest(request: SignalStrengthUpdateRequest): Unit
```

Set a SignalStrengthUpdateRequest to receive notification when signal quality measurements breach the specified thresholds. To be notified, set the signal strength update request and then register TelephonyCallback that implements `https://developer.android.com/reference/kotlin/android/telephony/TelephonyCallback.SignalStrengthsListener` through #registerTelephonyCallback. The notification will arrive through onSignalStrengthsChanged. To stop receiving the notification over the specified thresholds, pass the same SignalStrengthUpdateRequest object to clearSignalStrengthUpdateRequest. System will clean up the SignalStrengthUpdateRequest if the caller process died without calling clearSignalStrengthUpdateRequest. If this TelephonyManager object has been created with createForSubscriptionId, applies to the given subId. Otherwise, applies to getDefaultSubscriptionId. To request for multiple subIds, pass a request object to each TelephonyManager object created with createForSubscriptionId.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). Note that the thresholds in the request will be used on a best-effort basis; the system may modify requests to multiplex various request sources or to optimize power consumption. The caller should not expect to be notified with the exactly the same thresholds. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `request` | [SignalStrengthUpdateRequest](SignalStrengthUpdateRequest.md): the SignalStrengthUpdateRequest to be set into the System. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if a new request is set with same subId from the same caller |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

**See Also**

- clearSignalStrengthUpdateRequest

### setVisualVoicemailSmsFilterSettings

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVisualVoicemailSmsFilterSettings(settings: VisualVoicemailSmsFilterSettings!): Unit
```

Set the visual voicemail SMS filter settings for the subscription ID pinned to the TelephonyManager. When the filter is enabled, onSmsReceived will be called when a SMS matching the settings is received. Caller must be the default dialer, system dialer, or carrier visual voicemail app. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `settings` | [VisualVoicemailSmsFilterSettings](VisualVoicemailSmsFilterSettings.md)!: The settings for the filter, or `null` to disable the filter. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

**See Also**

- getDefaultDialerPackage
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CARRIER_VVM_PACKAGE_NAME_STRING_ARRAY:kotlin.String`

### setVoiceMailNumber

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVoiceMailNumber(
    alphaTag: String!, 
    number: String!
): Boolean
```

Sets the voice mail number.

Requires that the calling app has carrier privileges (see hasCarrierPrivileges). 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `alphaTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The alpha tag to display. |
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The voicemail number. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### setVoicemailRingtoneUri

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVoicemailRingtoneUri(
    phoneAccountHandle: PhoneAccountHandle!, 
    uri: Uri!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_CHANNEL_NOTIFICATION_SETTINGS:kotlin.String` instead.*

Sets the per-account voicemail ringtone.

Requires that the calling app is the default dialer, or has carrier privileges (see hasCarrierPrivileges, or has permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `phoneAccountHandle` | [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md)!: The handle for the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#` for which to set the voicemail ringtone. |
| `uri` | [Uri](../android.net/Uri.md)!: The URI for the ringtone to play when receiving a voicemail from a specific PhoneAccount. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### setVoicemailVibrationEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVoicemailVibrationEnabled(
    phoneAccountHandle: PhoneAccountHandle!, 
    enabled: Boolean
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_CHANNEL_NOTIFICATION_SETTINGS:kotlin.String` instead.*

Sets the per-account preference whether vibration is enabled for voicemail notifications.

Requires that the calling app is the default dialer, or has carrier privileges (see hasCarrierPrivileges, or has permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `phoneAccountHandle` | [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md)!: The handle for the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#` for which to set the voicemail vibration setting. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to enable or disable vibration for voicemail notifications from a specific PhoneAccount. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### switchMultiSimConfig

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun switchMultiSimConfig(numOfSims: Int): Unit
```

Switch configs to enable multi-sim or switch back to single-sim

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` or that the calling app has carrier privileges (see hasCarrierPrivileges). Note: with only carrier privileges, it is not allowed to switch from multi-sim to single-sim. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String` 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `numOfSims` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of live SIMs we want to switch to |

| Exceptions ||
|---|---|
| `android.os.RemoteException` | |
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`. |

### unregisterTelephonyCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterTelephonyCallback(callback: TelephonyCallback): Unit
```

Unregister an existing TelephonyCallback.

| Parameters ||
|---|---|
| `callback` | [TelephonyCallback](TelephonyCallback.md): The TelephonyCallback object to unregister. This value cannot be `null`. |

### updateAvailableNetworks

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateAvailableNetworks(
    availableNetworks: MutableList<AvailableNetworkInfo!>, 
    executor: Executor?, 
    callback: Consumer<Int!>?
): Unit
```

Update availability of a list of networks in the current location. This api should be called to inform OpportunisticNetwork Service about the availability of a network at the current location. This information will be used by OpportunisticNetwork service to enable modem stack and to attach to the network. If an empty list is passed, it is assumed that no network is available and will result in disabling the modem stack to save power. This api do not switch internet data once network attach is completed. Use setPreferredOpportunisticDataSubscription to switch internet data after network attach is complete. Requires that the calling app has carrier privileges on both primary and secondary subscriptions (see hasCarrierPrivileges), or has permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `availableNetworks` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AvailableNetworkInfo](AvailableNetworkInfo.md)!\>: is a list of available network information. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md)?: The executor of where the callback will execute. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>?: Callback will be triggered once it succeeds or failed. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_UNKNOWN_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_ABORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_INVALID_ARGUMENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_NO_CARRIER_PRIVILEGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_DISABLE_MODEM_FAIL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_ENABLE_MODEM_FAIL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_MULTIPLE_NETWORKS_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_NO_OPPORTUNISTIC_SUB_AVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_REMOTE_SERVICE_EXCEPTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_SERVICE_IS_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#UPDATE_AVAILABLE_NETWORKS_SIM_PORT_NOT_AVAILABLE:kotlin.Int` . This value may be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`. |

### uploadCallComposerPicture

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun uploadCallComposerPicture(
    pictureToUpload: InputStream, 
    contentType: String, 
    executor: Executor, 
    callback: OutcomeReceiver<ParcelUuid!, TelephonyManager.CallComposerException!>
): Unit
```

Uploads a picture to the carrier network for use with call composer. This method allows a dialer app to upload a picture to the carrier network that can then later be attached to an outgoing call. In order to attach the picture to a call, use the `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#` returned from `callback` upon successful upload as the value to `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#EXTRA_OUTGOING_PICTURE:kotlin.String`. This functionality is only available to the app filling the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_DIALER:kotlin.String` role on the device. This functionality is only available when `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_SUPPORTS_CALL_COMPOSER_BOOL:kotlin.String` is set to `true` in the bundle returned from getCarrierConfig. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `pictureToUpload` | [InputStream](../java.io/InputStream.md): An `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` that supplies the bytes representing the picture to upload. The client bears responsibility for closing this stream after `callback` is called with success or failure. Additionally, if the stream supplies more bytes than the return value of getMaximumCallComposerPictureSize, the upload will be aborted and the callback will be called with an exception containing `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.CallComposerException#ERROR_FILE_TOO_LARGE:kotlin.Int`. This value cannot be `null`. |
| `contentType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The MIME type of the picture you're uploading (e.g. image/jpeg). The list of acceptable content types can be found at 3GPP TS 26.141 sections 4.2 and 4.3. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which the `pictureToUpload` stream will be read, as well as on which the callback will be called. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [ParcelUuid](../android.os/ParcelUuid.md)!, [TelephonyManager.CallComposerException](../android/telephony/TelephonyManager.CallComposerException.md)!\>: A callback called when the upload operation terminates, either in success or in error. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

### uploadCallComposerPicture

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun uploadCallComposerPicture(
    pictureToUpload: Path, 
    contentType: String, 
    executor: Executor, 
    callback: OutcomeReceiver<ParcelUuid!, TelephonyManager.CallComposerException!>
): Unit
```

Uploads a picture to the carrier network for use with call composer. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String` feature which can be detected using hasSystemFeature.

| Parameters ||
|---|---|
| `pictureToUpload` | [Path](../java.nio.file/Path.md): Path to a local file containing the picture to upload. This value cannot be `null`. |
| `contentType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The MIME type of the picture you're uploading (e.g. image/jpeg). This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which the `pictureToUpload` file will be read from disk, as well as on which `callback` will be called. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [ParcelUuid](../android.os/ParcelUuid.md)!, [TelephonyManager.CallComposerException](../android/telephony/TelephonyManager.CallComposerException.md)!\>: A callback called when the upload operation terminates, either in success or in error. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If the device does not have `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`. |

**See Also**

- uploadCallComposerPicture

## Properties

### EXTRA_STATE_IDLE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_STATE_IDLE: String!
```

Value used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` corresponding to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_IDLE:kotlin.Int`.

### EXTRA_STATE_OFFHOOK

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_STATE_OFFHOOK: String!
```

Value used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` corresponding to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_OFFHOOK:kotlin.Int`.

### EXTRA_STATE_RINGING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_STATE_RINGING: String!
```

Value used with `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#EXTRA_STATE:kotlin.String` corresponding to `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#CALL_STATE_RINGING:kotlin.Int`.
